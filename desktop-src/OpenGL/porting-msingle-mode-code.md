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
ms.openlocfilehash: 1b8c62f93fa8e027dd1c91ca0bd40bc8e6ffaf9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074009"
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



 

 




