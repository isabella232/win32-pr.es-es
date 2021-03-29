---
title: Extender funciones de OpenGL
description: La biblioteca de OpenGL admite varias implementaciones de sus funciones.
ms.assetid: 9eb08fd4-899a-4610-9491-d7f377a19b46
keywords:
- OpenGL en Windows, funciones de extensión
- funciones de extensión OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcbb59aa15a9690ac05728548f0d8073a334a2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994490"
---
# <a name="extending-opengl-functions"></a><span data-ttu-id="2b210-105">Extender funciones de OpenGL</span><span class="sxs-lookup"><span data-stu-id="2b210-105">Extending OpenGL Functions</span></span>

<span data-ttu-id="2b210-106">La biblioteca de OpenGL admite varias implementaciones de sus funciones.</span><span class="sxs-lookup"><span data-stu-id="2b210-106">The OpenGL library supports multiple implementations of its functions.</span></span> <span data-ttu-id="2b210-107">Las funciones de extensión que se admiten en un contexto de representación no se admiten necesariamente en un contexto de representación diferente.</span><span class="sxs-lookup"><span data-stu-id="2b210-107">Extension functions supported in one rendering context aren't necessarily supported in a different rendering context.</span></span> <span data-ttu-id="2b210-108">Para un contexto de representación determinado en una aplicación que usa funciones de extensión, use solo las direcciones de función devueltas por la función [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="2b210-108">For a given rendering context in an application using extension functions, use only the function addresses returned by the [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) function.</span></span>

 

 




