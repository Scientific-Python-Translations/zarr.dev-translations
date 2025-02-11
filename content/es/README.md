## Dependencies

Los temas se escriben usando Sass para mantener las cosas modulares y reducir la necesidad de selectores repetidos entre archivos. Asegúrese de tener instalado el entorno de desarrollo reveal.js, incluidas las dependencias de Grunt, antes de continuar: https://github.com/hakimel/reveal.js#full-setup

## Creando un tema

Para crear su propio tema, comience duplicando un archivo `.scss` en [/css/theme/source](https://github.com/hakimel/reveal.js/blob/master/css/theme/source). Grunt lo compilará automáticamente de Sass a CSS (consulte [Gruntfile] (https://github.com/hakimel/reveal.js/blob/master/Gruntfile.js)) cuando ejecute `npm run build - css-themes`.

Cada archivo de tema hace cuatro cosas en el siguiente orden:

1. **Incluir [/css/theme/template/mixins.scss](https://github.com/hakimel/reveal.js/blob/master/css/theme/template/mixins.scss)**
   Funciones de utilidad compartida.

2. **Incluir [/css/theme/template/settings.scss](https://github.com/hakimel/reveal.js/blob/master/css/theme/template/settings.scss)**
   Declara un conjunto de variables personalizadas que espera el archivo de plantilla (paso 4). Se puede anular en el paso 3.

3. **Anular**
   Aquí es donde anulas el tema predeterminado. Ya sea especificando variables (consulte [settings.scss](https://github.com/hakimel/reveal.js/blob/master/css/theme/template/settings.scss) como referencia) o agregando los selectores y estilos que desee.

4. **Incluir [/css/theme/template/theme.scss](https://github.com/hakimel/reveal.js/blob/master/css/theme/template/theme.scss)**
   El archivo de tema de plantilla que generará una salida CSS final basada en las variables definidas actualmente.
