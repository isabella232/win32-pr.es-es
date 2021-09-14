---
title: Hacer que un contexto de representación no sea actual
description: Para separar un contexto de representación de un subproceso, haga que no sea actual. Para ello, llame a la función wglMakeCurrent con los parámetros establecidos en NULL. A continuación se muestra un ejemplo de esta tarea sencilla.
ms.assetid: fe76e3d3-5480-448d-95aa-a5af0da309f3
keywords:
- OpenGL en Windows, contextos de representación
- contextos de representación OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12b3e0184a606faef7792b990d674054c5ddf07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171345"
---
# <a name="making-a-rendering-context-not-current"></a>Hacer que un contexto de representación no sea actual

Para separar un contexto de representación de un subproceso, haga que no sea actual. Para ello, llame a la [**función wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) con los parámetros establecidos en **NULL.** A continuación se muestra un ejemplo de esta tarea sencilla.

``` syntax
// detach the current rendering context from the thread  
wglMakeCurrent(NULL, NULL);
```

 

 




