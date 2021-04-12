---
title: Comandos de cueing y niebla de profundidad de portabilidad
description: Comandos de cueing y niebla de profundidad de portabilidad
ms.assetid: 16982d11-88a1-4a35-960f-28f10491e0ac
keywords:
- Migración de la contabilidad de IRIS, profundidad cueing
- portabilidad de IRIS GL, Depth cueing
- trasladar a OpenGL desde IRIS GL, Depth cueing
- Exportación de OpenGL desde IRIS GL, profundidad cueing
- Migración de la contabilidad de IRIS, niebla
- portabilidad de IRIS GL, niebla
- trasladar a OpenGL desde IRIS GL, niebla
- Exportación de OpenGL desde IRIS GL, niebla
- profundidad cueing
- luz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd9f65a29e0ae594bf9344cd960d3fc2b9aa646
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269169"
---
# <a name="porting-depth-cueing-and-fog-commands"></a>Comandos de cueing y niebla de profundidad de portabilidad

Al migrar los comandos Depth-cueing y niebla, tenga en cuenta los puntos siguientes:

-   La llamada de GL de IRIS, **fogvertex**, establece un modo y los parámetros que afectan a ese modo. En OpenGL, se llama una vez a [**glFog**](glfog.md) para establecer el modo y, a continuación, de nuevo dos veces o más para establecer varios parámetros.
-   En OpenGL, Depth cueing no es una característica independiente. Usar niebla lineal en lugar de cueing de profundidad. (En esta sección se proporciona un ejemplo de cómo hacerlo). Las siguientes funciones de la contabilidad de IRIS no tienen un equivalente de OpenGL directo:

    **depthcue**

    **lRGBrange**

    **lshaderange**

    **getdcm**

-   Para ajustar la calidad de la niebla, use [**glHint**](glhint.md)(sugerencia de niebla de GL \_ \_ ).

En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para administrar la niebla y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS         | Función OpenGL                                     | Significado                           |
|--------------------------|-----------------------------------------------------|-----------------------------------|
| **fogvertex**            | [**glFog**](glfog.md)                              | Establece varios parámetros de niebla.      |
| **fogvertex**(FG \_ en)  | [**glEnable**](glenable.md) (niebla de contabilidad \_ )            | Activa la niebla.                     |
| **fogvertex**(FG \_ desactivado) | [**glDisable**](gldisable.md) (niebla de contabilidad \_ )          | Desactiva la niebla.                    |
| **depthcue**             | [**glFog**](glfog.md) ( \_ \_ módulo de niebla de contabilidad general, GL \_ lineal) | Utiliza la niebla lineal para cueing de profundidad. |



 

En la tabla siguiente se enumeran los parámetros que se pueden pasar a **glFog**.



| Parámetro de niebla    | Significado                       | Valor predeterminado                  |
|------------------|-------------------------------|--------------------------|
| \_densidad de niebla de GL \_ | Densidad de niebla.                  | 1,0                      |
| \_Inicio de niebla de GL \_   | Cerca de distancia para la niebla lineal. | 0,0                      |
| finalización de la niebla de GL \_ \_     | Distancia lejana para la niebla lineal.  | 1,0                      |
| \_Índice de niebla de GL \_   | Índice de color de niebla.              | 0,0                      |
| \_color de niebla de GL \_   | Color RGBA de niebla.               | (0, 0, 0, 0)             |
| \_modo de niebla de contabilidad \_    | Modo de niebla.                     | Consulte la tabla siguiente. |



 

El parámetro niebla-density de OpenGL difiere del de IRIS GL. Se relacionan de la siguiente manera:

-   Si *fogMode* = EXP2
     

    *openGLfogDensity* = (*irisGLfogDensity* ) ( **sqrt** ( **log** (1/255)))
-   Si *fogMode* = exp
     

    *openGLfogDensity* = (*irisGLfogDensity* ) ( **log** (1/255))

donde **sqrt** es la operación de raíz cuadrada, **log** es el logaritmo natural, *irisGLfogDensity* es la densidad de niebla de la contabilidad de iris y *OpenGLfogDensity* es la densidad de niebla de OpenGL.

Para cambiar entre el cálculo de la niebla en modo por píxel y el modo por vértice, use [**glHint**](glhint.md)( \_ sugerencia de niebla de GL \_ , *hintMode*). Hay dos modos de sugerencia disponibles:

-   \_Cálculo de niebla por píxel más bonito
-   \_Cálculo de niebla por vértice más rápido de GL

En la tabla siguiente se enumeran los modos de niebla de la contabilidad de IRIS y sus equivalentes de OpenGL.



| Modo de niebla de GL de IRIS                       | Modo de niebla de OpenGL | Modo de sugerencia                         | Significado                                  |
|----------------------------------------|-----------------|-----------------------------------|------------------------------------------|
| FG \_ VTX \_ exp, FG \_ PIX \_ exp<br/>   | contabilidad \_ General         | GL \_ más rápido, libro de contabilidad más \_ agradable<br/> | Modo de niebla pesada (valor predeterminado).                |
| FG \_ VTX \_ EXP2, FG \_ PIX \_ EXP2<br/> | GL \_ EXP2        | GL \_ más rápido, libro de contabilidad más \_ agradable<br/> | Modo Haze.                               |
| FG \_ VTX- \_ foto, FG \_ PIX \_<br/>   | CONTABILIDAD \_ lineal      | GL \_ más rápido, libro de contabilidad más \_ agradable<br/> | Modo de niebla lineal. (Se usa para cueing de profundidad). |



 

En el ejemplo de código siguiente se muestra la profundidad cueing en OpenGL:


```C++
/* 
 *  depthcue.c 
 *  This program draws a wire frame model, which uses 
 *  intensity (brightness) to give clues to distance 
 *  Fog is used to achieve this effect 
 */ 
#include <GL/gl.h> 
#include <GL/glu.h> 
#include "aux.h" 
 
/*  Initialize linear fog for depth cueing 
 */ 
void myinit(void) 
{ 
    GLfloat fogColor[4] = {0.0, 0.0, 0.0, 1.0}; 
 
    glEnable(GL_FOG); 
    glFogi (GL_FOG_MODE, GL_LINEAR); 
    glHint (GL_FOG_HINT, GL_NICEST);  /*  per pixel  */ 
    glFogf (GL_FOG_START, 3.0); 
    glFogf (GL_FOG_END, 5.0); 
    glFogfv (GL_FOG_COLOR, fogColor); 
    glClearColor(0.0, 0.0, 0.0, 1.0); 
 
    glDepthFunc(GL_LEQUAL); 
    glEnable(GL_DEPTH_TEST); 
    glShadeModel(GL_FLAT); 
} 
 
/*  display() draws an icosahedron 
 */ 
void display(void) 
{ 
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT); 
    glColor3f (1.0, 1.0, 1.0); 
    auxWireIcosahedron(1.0); 
    glFlush(); 
} 
 
void myReshape(GLsizei w, GLsizei h) 
{ 
    glViewport(0, 0, w, h); 
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective (45.0, (GLfloat) w/(GLfloat) h, 3.0, 5.0); 
    glMatrixMode(GL_MODELVIEW); 
    glLoadIdentity (); 
    glTranslatef (0.0, 0.0, -4.0); /*move object into view*/ 
} 
/*  Main Loop 
 */ 
int main(int argc, char** argv) 
{ 
    auxInitDisplayMode (AUX_SINGLE | AUX_RGBA | AUX_DEPTH); 
    auxInitPosition (0, 0, 400, 400); 
    auxInitWindow (argv[0]); 
    myinit(); 
    auxReshapeFunc (myReshape); 
    auxMainLoop(display); 
}
```



 

 





