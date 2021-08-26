---
title: Un puerto de ejemplo de una lista de visualización
description: En este tema se proporciona un ejemplo de código de IRIS GL que define tres listas de visualización; una de las listas de visualización hace referencia a las demás en su definición. Después del ejemplo de IRIS GL se muestra el aspecto del código cuando se porte a OpenGL.
ms.assetid: 03283b00-fb5b-4e89-9384-171b38f141ee
keywords:
- Porte de IRIS GL, listas de visualización
- porting from IRIS GL,display lists
- porte a OpenGL desde IRIS GL, mostrar listas
- Porte de OpenGL desde IRIS GL, mostrar listas
- mostrar listas, porte desde IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fbb696673da7f4dc83abd625bb616b67449de64a40df1cfc99bd429a2a980e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962435"
---
# <a name="a-sample-port-of-a-display-list"></a>Un puerto de ejemplo de una lista de visualización

En este tema se proporciona un ejemplo de código de IRIS GL que define tres listas de visualización; una de las listas de visualización hace referencia a las demás en su definición. Después del ejemplo de IRIS GL se muestra el aspecto del código cuando se porte a OpenGL.

## <a name="iris-gl-sample-display-list-code"></a>Código de lista de visualización de ejemplo de IRIS GL


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



## <a name="opengl-sample-display-list-code"></a>Código de lista de visualización de ejemplo de OpenGL

Este es el código GL de IRIS anterior traducido a OpenGL:


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



 

 




