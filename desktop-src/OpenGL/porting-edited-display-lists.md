---
title: Trasladar listas de visualización editadas
description: Aunque no puede editar las listas de visualización de OpenGL, puede obtener resultados similares anidando listas de visualización y, a continuación, destruyendo y creando nuevas versiones de las sublistas.
ms.assetid: b7f7ffed-c3de-43d4-bff2-f244faa3a27a
keywords:
- Migración de la contabilidad de IRIS, mostrar listas
- trasladar de IRIS GL, mostrar listas
- trasladar a OpenGL desde IRIS GL, mostrar listas
- Exportación de OpenGL desde IRIS GL, mostrar listas
- Mostrar listas, trasladar de IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5555c850d4695ba3732b61c0a41b7aedd8af0a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665699"
---
# <a name="porting-edited-display-lists"></a>Trasladar listas de visualización editadas

Aunque no puede editar las listas de visualización de OpenGL, puede obtener resultados similares anidando listas de visualización y, a continuación, destruyendo y creando nuevas versiones de las sublistas. Por ejemplo:

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

 

 




