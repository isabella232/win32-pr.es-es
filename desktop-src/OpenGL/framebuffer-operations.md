---
title: Operaciones de fotogramas
description: Para seleccionar el búfer en el que se escriben los valores de color, use glDrawBuffer.
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- Canalización de procesamiento de OpenGL, operaciones fotogramas
- framebuffers, operaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6199700d00a6628548404870dd6ef6ce3e2c825
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531983"
---
# <a name="framebuffer-operations"></a><span data-ttu-id="41a48-105">Operaciones de fotogramas</span><span class="sxs-lookup"><span data-stu-id="41a48-105">Framebuffer Operations</span></span>

<span data-ttu-id="41a48-106">Para seleccionar el búfer en el que se escriben los valores de color, use [**glDrawBuffer**](gldrawbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="41a48-106">To select the buffer into which color values are written, use [**glDrawBuffer**](gldrawbuffer.md).</span></span> <span data-ttu-id="41a48-107">Se usan cuatro funciones diferentes para enmascarar la escritura de bits en cada una de las framebuffers lógicas después de que se hayan realizado todas las operaciones por fragmento:</span><span class="sxs-lookup"><span data-stu-id="41a48-107">You use four different functions to mask the writing of bits to each of the logical framebuffers after all per-fragment operations have been performed:</span></span>

-   [<span data-ttu-id="41a48-108">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="41a48-108">**glIndexMask**</span></span>](glindexmask.md)
-   [<span data-ttu-id="41a48-109">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="41a48-109">**glColorMask**</span></span>](glcolormask.md)
-   [<span data-ttu-id="41a48-110">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="41a48-110">**glDepthMask**</span></span>](gldepthmask.md)
-   [<span data-ttu-id="41a48-111">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="41a48-111">**glStencilMask**</span></span>](glstencilmask.md)

<span data-ttu-id="41a48-112">La función [**glAccum**](glaccum.md) controla el funcionamiento del búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="41a48-112">The [**glAccum**](glaccum.md) function controls the operation of the accumulation buffer.</span></span> <span data-ttu-id="41a48-113">Por último, [**glClear**](glclear.md) establece cada píxel de un subconjunto especificado de los búferes en el valor especificado con [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)o [**glClearAccum**](glclearaccum.md).</span><span class="sxs-lookup"><span data-stu-id="41a48-113">Finally, [**glClear**](glclear.md) sets every pixel in a specified subset of the buffers to the value specified with [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md), or [**glClearAccum**](glclearaccum.md).</span></span>

 

 




