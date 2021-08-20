---
title: Porte del código de modo MSINGLE
description: OpenGL no tiene ningún equivalente para MSINGLE, modo de matriz única.
ms.assetid: 7de933b8-150c-432d-89ee-5f5799ad8443
keywords:
- Porte de IRIS GL, modo MSINGLE
- porting from IRIS GL,MSINGLE mode
- porte a OpenGL desde IRIS GL, modo MSINGLE
- Porte de OpenGL desde IRIS GL, modo MSINGLE
- Modo MSINGLE
- Porte de IRIS GL, modo de matriz única
- porte desde IRIS GL, modo de matriz única
- porte a OpenGL desde IRIS GL, modo de matriz única
- Porte de OpenGL desde IRIS GL, modo de matriz única
- modo de matriz única
- modo de doble matriz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83716cead9134ba7823f4206fb6479d323bd35bddee480e9353a7ceb9aad38ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132394"
---
# <a name="porting-msingle-mode-code"></a>Porte del código de modo MSINGLE

OpenGL no tiene ningún equivalente para **MSINGLE,** modo de matriz única. Aunque no se ha desaconsejado el uso de este modo, es el valor predeterminado para IRIS GL. Si el programa IRIS GL usa el modo de matriz única, debe volver a escribirlo para usar solo el modo de doble matriz. OpenGL siempre está en modo de doble matriz y está inicialmente en modo \_ GL MODELVIEW.

La mayoría del código GL de IRIS en el modo MSINGLE tiene este aspecto:

``` syntax
projectionmatrix();
```

donde *projectionmatrix* es uno de: **ortosto,** **orto2,** **perspectiva** o **ventana.** Para portear a OpenGL, reemplace la función **MSINGLE** -mode *projectionmatrix* por:


```C++
glMatrixMode( GL_PROJECTION ); 
glLoadMatrix( identity matrix ); 
 
/* call one of these functions here: */ 
/* glFrustrum(), glOrtho(), glOrtho2(), gluPerspective()}; */ 
 
glMatrixMode( GL_MODELVIEW ); 
glLoadMatrix( identity matrix );
```



 

 




