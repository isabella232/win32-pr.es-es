---
title: Un puerto de ejemplo de una lista de visualización
description: En este tema se proporciona un ejemplo de GL de IRIS de código que define tres listas de presentación. una de las listas de visualización hace referencia a las demás en su definición. A continuación, se muestra un ejemplo de la apariencia del código cuando se traslada a OpenGL.
ms.assetid: 03283b00-fb5b-4e89-9384-171b38f141ee
keywords:
- Migración de la contabilidad de IRIS, mostrar listas
- trasladar de IRIS GL, mostrar listas
- trasladar a OpenGL desde IRIS GL, mostrar listas
- Exportación de OpenGL desde IRIS GL, mostrar listas
- Mostrar listas, trasladar de IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a856350a0a248bf7dcac51c36b9d35cf114956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775967"
---
# <a name="a-sample-port-of-a-display-list"></a>Un puerto de ejemplo de una lista de visualización

En este tema se proporciona un ejemplo de GL de IRIS de código que define tres listas de presentación. una de las listas de visualización hace referencia a las demás en su definición. A continuación, se muestra un ejemplo de la apariencia del código cuando se traslada a OpenGL.

## <a name="iris-gl-sample-display-list-code"></a>Ejemplo de código de lista de visualización de la contabilidad de IRIS


```C++
makeobj(10);  // 10 object  
    cpack(0x0000FF); 
    recti(164, 33, 364, 600);   // Hollow rectangle  
closeobj(); 
 
makeobj(20);  // 20 object  
    cpack(0xFFFF00); 
    circle(0, 0, 25);           // Unfilled circle  
    recti(100, 100, 200, 200);  // Filled rectangle  
closeobj(); 
 
makeobj(30);  // 30 object  
    callobj(10); 
    cpack(0xFFFFFF); 
    recti(400, 100, 500, 300);  // Draw filled rectangle  
    callobj(20); 
closeobj(); 
 
// Now draw by calling the lists  
call(30);
```



## <a name="opengl-sample-display-list-code"></a>Ejemplo de código de lista de visualización de OpenGL

Este es el código de contabilidad del IRIS anterior que se traduce a OpenGL:


```C++
glNewList(10, GL_COMPILE);            // List #10  
    glColor3f(1, 0, 0); 
    glRecti(164, 33, 364, 600); 
glEndList(); 
 
glNewList(20, GL_COMPILE);            //List #20  
    glColor3f(1, 1, 0);               // Set color to YELLOW  
    glPolygonMode(GL_BOTH, GL_LINE);  // Unfilled mode  
    glBegin(GL_POLYGON);  // Use polygon to approximate a circle  
        for(i=0; i<100; i++) { 
            cosine = 25 * cos(i * 2 * PI/100.0); 
            sine =   25 * sin(i * 2 * PI/100.0); 
            glVertex2f(cosine, sine); 
        } 
    glEnd(); 
    glBegin(GL_QUADS); 
        glColorf(0, 1, 1);            // Set color to CYAN  
        glVertex2i(100, 100); 
        glVertex2i(100, 200); 
        glVertex2i(200, 200); 
        glVertex2i(100, 200); 
    glEnd(); 
glEndList(); 
 
glNewList(30, GL_COMPILE);            // List #30  
    glCallList(10); 
        glColorf(1, 1, 1);            // Set color to WHITE  
        glRecti(400, 100, 500, 300); 
    glCallList(20); 
glEndList(); 
 
// Execute the display lists  
glCallList(30);
```



 

 




