---
title: Porting Depth Cueing and Fog Commands
description: Porting Depth Cueing and Fog Commands
ms.assetid: 16982d11-88a1-4a35-960f-28f10491e0ac
keywords:
- Porte de IRIS GL, indicaciones de profundidad
- porting from IRIS GL,depth cueing
- porte a OpenGL desde IRIS GL, indicaciones de profundidad
- Porte de OpenGL desde IRIS GL, indicaciones de profundidad
- Porte de IRIS GL, iris
- porting from IRIS GL,gl
- porte a OpenGL desde IRIS GL, iris
- Porte de OpenGL desde IRIS GL,gl
- indicaciones de profundidad
- luz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd9f65a29e0ae594bf9344cd960d3fc2b9aa646
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169189"
---
# <a name="porting-depth-cueing-and-fog-commands"></a>Porting Depth Cueing and Fog Commands

Al portear comandos de indicaciones de profundidad y de sonido, tenga en cuenta los siguientes puntos:

-   La llamada a IRIS **GL,vertex,** establece un modo y los parámetros que afectan a ese modo. En OpenGL, se llama [**a glFog**](glfog.md) una vez para establecer el modo y, a continuación, dos o más veces para establecer varios parámetros.
-   En OpenGL, la indicación de profundidad no es una característica independiente. Use la cola lineal en lugar de la indicación de profundidad. (En esta sección se proporciona un ejemplo de cómo hacerlo). Las siguientes funciones GL de IRIS no tienen ningún equivalente directo de OpenGL:

    **depthcue**

    **lRGBrange**

    **lshaderange**

    **getdcm**

-   Para ajustar la calidad de los ángulos, use [**glHint**](glhint.md)(GL \_ GL GL \_ HINT).

En la tabla siguiente se enumeran las funciones GL de IRIS para administrar el espacio y sus funciones OpenGL equivalentes.



| Función GL de IRIS         | Función OpenGL                                     | Significado                           |
|--------------------------|-----------------------------------------------------|-----------------------------------|
| **yvertex**            | [**glFog**](glfog.md)                              | Establece varios parámetros de zona.      |
| **vertex (** FG \_ ON )  | [**glEnable**](glenable.md) ( GL \_ GL GL )            | Activa el giro.                     |
| **vertex (** FG \_ OFF ) | [**glDisable**](gldisable.md) ( GL \_ GL GL )          | Desactiva la curva.                    |
| **depthcue**             | [**glFog**](glfog.md) ( GL \_ GL GL \_ MOD, GL LINEAR \_ ) | Usa la línea lineal para la indicación de profundidad. |



 

En la tabla siguiente se enumeran los parámetros que se pueden pasar **a glFog.**



| Parámetro Desmaeste    | Significado                       | Valor predeterminado                  |
|------------------|-------------------------------|--------------------------|
| DENSIDAD \_ GL \_ DE GL | Densidad de densidad.                  | 1.0                      |
| GL \_ FOG \_ START   | Distancia cercana para el recorrido lineal. | 0,0                      |
| GL \_ END DE GL \_     | Distancia lejana para el recorrido lineal.  | 1.0                      |
| GL \_ FOG \_ INDEX   | Índice de color rojo.              | 0,0                      |
| GL \_ FOG \_ COLOR   | Color RGBA blanco.               | (0, 0, 0, 0)             |
| MODO \_ GL GL \_    | Modo de fusión.                     | Consulte la tabla siguiente. |



 

El parámetro de densidad de densidad de densidad de OpenGL difiere del de IRIS GL. Están relacionados de la siguiente manera:

-   *simodemode =* EXP2
     

    *openGLfogDensity* = (*irisGLfogDensity* ) ( **sqrt** ( **log** ( 1 / 255 ) ))
-   ifmode *=* EXP
     

    *openGLfogDensity* = (*irisGLfogDensity* ) ( **log** ( 1 / 255 ) )

donde **sqrt** es la operación de raíz cuadrada, **log** es el logaritmo natural, *irisGLfogDensity* es la densidad de densidad gl de IRIS y *openGLfogDensity* es la densidad de OpenGL.

Para cambiar entre calcular el ángulo en modo por píxel y el modo por vértice, use [**glHint**](glhint.md)(GL \_ \_ HINT, *hintMode).* Hay dos modos de sugerencias disponibles:

-   Cálculo \_ de píxeles DE GL NICEST por píxel
-   Cálculo gl \_ fastest por vértice de vértice

En la tabla siguiente se enumeran los modos iris gl y sus equivalentes de OpenGL.



| Modo gl de iris                       | OpenGL mode (Modo de fusión de OpenGL) | Modo de sugerencia                         | Significado                                  |
|----------------------------------------|-----------------|-----------------------------------|------------------------------------------|
| FG \_ VTX \_ EXP,FG \_ PIXEL \_ EXP<br/>   | GL \_ EXP         | GL \_ FASTEST,GL \_ NICEST<br/> | Modo heavy heavy (valor predeterminado).                |
| FG \_ VTX \_ EXP2,FG \_ PIXEL \_ EXP2<br/> | GL \_ EXP2        | GL \_ FASTEST,GL \_ NICEST<br/> | Modo haze.                               |
| FG \_ VTX \_ LIN,FG \_ PIXEL \_ LIN<br/>   | GL \_ LINEAR      | GL \_ FASTEST,GL \_ NICEST<br/> | Modo de regresión lineal. (Se usa para la indicación de profundidad). |



 

En el ejemplo de código siguiente se muestra la indicación de profundidad en OpenGL:


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



 

 





