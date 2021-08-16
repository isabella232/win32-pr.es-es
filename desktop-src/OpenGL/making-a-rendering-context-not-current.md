---
title: Hacer que un contexto de representación no sea actual
description: Para separar un contexto de representación de un subproceso, haga que no sea actual. Para ello, llame a la función wglMakeCurrent con los parámetros establecidos en NULL. A continuación se muestra un ejemplo de esta tarea sencilla.
ms.assetid: fe76e3d3-5480-448d-95aa-a5af0da309f3
keywords:
- OpenGL en Windows, contextos de representación
- contextos de representación OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914bbed6e2d595d23cfcf8dc38820efc18153f4433a2a48446090ec16818b671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937368"
---
# <a name="making-a-rendering-context-not-current"></a>Hacer que un contexto de representación no sea actual

Para separar un contexto de representación de un subproceso, haga que no sea actual. Para ello, llame a la [**función wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) con los parámetros establecidos en **NULL.** A continuación se muestra un ejemplo de esta tarea sencilla.

``` syntax
// detach the current rendering context from the thread  
wglMakeCurrent(NULL, NULL);
```

 

 




