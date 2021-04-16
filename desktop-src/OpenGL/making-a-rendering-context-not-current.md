---
title: Convertir un contexto de representación en no actual
description: Para desasociar un contexto de representación de un subproceso, conviértalo en no actual. Para ello, puede llamar a la función wglMakeCurrent con los parámetros establecidos en NULL. A continuación se muestra un ejemplo de esta tarea sencilla.
ms.assetid: fe76e3d3-5480-448d-95aa-a5af0da309f3
keywords:
- OpenGL en Windows, contextos de representación
- contextos de representación OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12b3e0184a606faef7792b990d674054c5ddf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356981"
---
# <a name="making-a-rendering-context-not-current"></a>Convertir un contexto de representación en no actual

Para desasociar un contexto de representación de un subproceso, conviértalo en no actual. Para ello, puede llamar a la función [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) con los parámetros establecidos en **null**. A continuación se muestra un ejemplo de esta tarea sencilla.

``` syntax
// detach the current rendering context from the thread  
wglMakeCurrent(NULL, NULL);
```

 

 




