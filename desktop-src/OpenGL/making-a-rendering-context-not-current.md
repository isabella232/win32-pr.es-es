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
# <a name="making-a-rendering-context-not-current"></a><span data-ttu-id="39b9e-107">Convertir un contexto de representación en no actual</span><span class="sxs-lookup"><span data-stu-id="39b9e-107">Making a Rendering Context Not Current</span></span>

<span data-ttu-id="39b9e-108">Para desasociar un contexto de representación de un subproceso, conviértalo en no actual.</span><span class="sxs-lookup"><span data-stu-id="39b9e-108">To detach a rendering context from a thread, make it not current.</span></span> <span data-ttu-id="39b9e-109">Para ello, puede llamar a la función [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) con los parámetros establecidos en **null**.</span><span class="sxs-lookup"><span data-stu-id="39b9e-109">You can do this by calling the [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) function with the parameters set to **NULL**.</span></span> <span data-ttu-id="39b9e-110">A continuación se muestra un ejemplo de esta tarea sencilla.</span><span class="sxs-lookup"><span data-stu-id="39b9e-110">The following is a sample of this simple task.</span></span>

``` syntax
// detach the current rendering context from the thread  
wglMakeCurrent(NULL, NULL);
```

 

 




