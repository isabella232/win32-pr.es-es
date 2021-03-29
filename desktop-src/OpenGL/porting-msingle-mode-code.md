---
title: Trasladar código de modo MSINGLE
description: OpenGL no tiene equivalente para MSINGLE, modo de matriz única.
ms.assetid: 7de933b8-150c-432d-89ee-5f5799ad8443
keywords:
- Migración de la contabilidad de IRIS, modo MSINGLE
- portabilidad de IRIS GL, modo MSINGLE
- migración a OpenGL desde IRIS GL, modo MSINGLE
- Exportación de OpenGL desde IRIS GL, modo MSINGLE
- Modo MSINGLE
- Migración de la contabilidad de IRIS, modo de matriz única
- portabilidad de IRIS GL, modo de matriz única
- trasladar a OpenGL desde IRIS GL, modo de matriz única
- Exportación de OpenGL desde IRIS GL, modo de matriz única
- modo de matriz única
- modo de doble matriz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b8c62f93fa8e027dd1c91ca0bd40bc8e6ffaf9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418879"
---
# <a name="porting-msingle-mode-code"></a>Trasladar código de modo MSINGLE

OpenGL no tiene equivalente para **MSINGLE**, modo de matriz única. Aunque no se recomienda el uso de este modo, es el valor predeterminado para la contabilidad de IRIS. Si el programa de contabilidad de IRIS usa el modo de matriz única, debe volver a escribirlo para usar solo el modo de matriz doble. OpenGL siempre está en modo de doble matriz y se encuentra inicialmente en \_ modo GL MODELVIEW.

La mayoría del código de la contabilidad de IRIS en el modo MSINGLE tiene el siguiente aspecto:

``` syntax
projectionmatrix();
```

donde *projectionmatrix* es uno de los siguientes: **Ortho**, **ortho2**, **Perspective** o **Window**. Para migrar a OpenGL, reemplace la función **MSINGLE** en modo *projectionmatrix* por:


```C++
glMatrixMode( GL_PROJECTION ); 
glLoadMatrix( identity matrix ); 
 
/* call one of these functions here: */ 
/* glFrustrum(), glOrtho(), glOrtho2(), gluPerspective()}; */ 
 
glMatrixMode( GL_MODELVIEW ); 
glLoadMatrix( identity matrix );
```



 

 




