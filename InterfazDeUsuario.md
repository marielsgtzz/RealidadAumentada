# Interfaz de Usuario

| Orientación de            |                                  pantalla                                   |
| ------------------------- | :-------------------------------------------------------------------------: |
| Portrait                  |                                  Landscape                                  |
| Se puede usar solo 1 mano | Se necesitan dos manos pero hay más espacio para la experiencia en pantalla |

<img src="imgMds/PortraitVsLandscape.png" alt="PortraitVsLandscape" width="400" height="250"/>

Una buena interfaz es una que no se tiene que explicar porque es intuitiva. Es importante cuidar que no haya contaminación visual, tener solo lo más importante visible de forma directa.

El estándar de la pantalla es 16:9 Portrait.
Es más fácil editar la UI cuando la perspectiva del editor está en 2D.
![VistaEditor2D](imgMds/VistaEditor2D.png)

## Elementos de UI

Para agregar los elementos hay que posicionarse sobre la ventana de hierarchy (donde están los objetos de la escena) y darle click derecho -> UI

> Aparecen enlistados los elementos para una interfaz gráfica. El principal elemento es el Canvas, todo lo de la GIU necesita estar dentro de un canvas (ser su hijo).

![AgregarElementoUI](imgMds/AgregarElementoUI.png)

Se puede distinguir un objeto de UI de otros objetos con el tipo de transform (los de tipo UI son Rect Transform):

| Objeto común                                               |                     Objeto UI                      |
| ---------------------------------------------------------- | :------------------------------------------------: |
| ![TransformObjetoBasico](imgMds/TransformObjetoBasico.png) | ![TransformObjetoUI](imgMds/TransformObjetoUI.png) |

En el inspector del Canvas:

- Render Mode:
  - Screen Space - Overlay es para poder trabajar la UI sin que "estorben" los elementos de la experiencia
  - Screen Space - Camera para poder colocar la UI sobre una cámara en específico
    - Ej. Si una cámara simula una cámara de seguridad probablemente querríamos
  - Screen Space - World Space más utilizado en VR para colocar la UI dentro del mundo
- Sort Order es para cuando hay múltiples Canvas y se le quiere dar prioridad de visibilidad a alguno.

![InspectorCanvas](imgMds/InspectorCanvas.png)

- UI Scale Mode:
  - Scale With Screen Size - Toma como referencia una resolución en específico y si cambia la del dispositivo, cambia la de la interfaz de forma responsiva.
    ![InspectoCanvasScaler](imgMds/InspectoCanvasScaler.png)

En un texto solo se deja la opción de raycast activada si se va a tener alguna interacción con el texto.
El text mesh pro evita que se pixelee el texto.
