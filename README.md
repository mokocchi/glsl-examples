# glsl examples

Este es un repo con ejemplos y algunos experimentos con shaders glsl tomados de [Lewis Lepton's Shaders Tutorial Series](https://www.youtube.com/watch?v=HIvNePu7UEE&list=PL4neAtv21WOmIrTrkNO3xCyrxg4LKkrF7)

## Armando el ambiente

*Nota: para encontrar los comandos de VSCode abrir el Command Palette en View/Command Palette o F1 o Ctrl+Shift+P*
1.  Extensiones para VSCode:
    - Shader languages support for VS Code (slevesque.shader) by slevesque
    - glsl-canvas (circledev.glsl-canvas) by circledev
    - GLSL Linter (mrjjot.vscode-glsl-linter) by Jacek Wieczorek
2. Validador de glsl:
    - Descargar el binario `glslangValidator` de [github](https://github.com/KhronosGroup/glslang/releases/tag/master-tot) en `/usr/local/bin`
    - Agregar lo siguiente a las user settings de vscode (JSON)
    ```json
        "glsl-linter.validatorPath": "/usr/local/bin/glslangValidator",
        "glsl-linter.fileExtensions": {
            ".fs.glsl": "frag",
            ".vs.glsl": "vert",
            ".tes.glsl": "tese",
            ".tcs.glsl": "tesc",
            ".gs.glsl": "geom"
        }
    ```
3. Snippets de autocompletado para glsl
    - Descargar json de [https://gist.github.com/lewislepton/8b17f56baa7f1790a70284e7520f9623]
    - Pegarlo en Configure User Snippets -> glsl
4. Abrir cualquier fragment shader (*.frag) y poner Open glslcanvas desde el Command Palette

## Ejemplo mínimo
```glsl
#ifdef GL_ES
precision mediump float;
#endif

void main() {
    gl_FragColor = vec4(1.0, 0.0, 0.0, 1.0);
}
```