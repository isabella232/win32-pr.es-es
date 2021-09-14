---
title: Porte de listas de presentación editadas
description: Aunque no puede editar las listas de presentación de OpenGL, puede obtener resultados similares anidando listas de presentación y, a continuación, destruyendo y creando nuevas versiones de las sublistas.
ms.assetid: b7f7ffed-c3de-43d4-bff2-f244faa3a27a
keywords:
- Porte de IRIS GL, listas de visualización
- porting from IRIS GL,display lists
- porte a OpenGL desde IRIS GL, mostrar listas
- Porte de OpenGL desde IRIS GL, mostrar listas
- mostrar listas, porte desde IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5555c850d4695ba3732b61c0a41b7aedd8af0a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169169"
---
# <a name="porting-edited-display-lists"></a>Porte de listas de presentación editadas

Aunque no puede editar las listas de presentación de OpenGL, puede obtener resultados similares anidando listas de presentación y, a continuación, destruyendo y creando nuevas versiones de las sublistas. Por ejemplo:

``` syntax
glNewList (1, GL_COMPILE); 
    glIndexi(MY_RED); 
glEndlist(); 
 
glNewList(2, GL_COMPILE); 
    glScalef(1.2, 1.2, 1.0); 
glEndList(); 
 
glNewList(3, GL_COMPILE); 
    glCallList(1); 
    glCallList(2); 
glEndList(); 
 
glDeleteLists(1, 2); 
glNewList(1, GL_COMPILE); 
    glIndexi(MY_CYAN); 
glEndList(); 
glNewList(2, GL_COPILE); 
    glScalef(0.5, 0.5, 1.0); 
glEndList;
```

 

 




