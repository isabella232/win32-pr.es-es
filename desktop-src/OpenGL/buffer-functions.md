---
title: Funciones de búfer
description: Para copiar el contenido de un búfer fuera de pantalla en un búfer en pantalla, llame a SwapBuffers.
ms.assetid: 605eba4e-ee38-4e62-adf8-1b7894030cb0
keywords:
- Funciones de WGL, búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a93858b8085171a9139bc5ab329e531ddbb699
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105678613"
---
# <a name="buffer-functions"></a><span data-ttu-id="1b1bc-104">Funciones de búfer</span><span class="sxs-lookup"><span data-stu-id="1b1bc-104">Buffer Functions</span></span>

<span data-ttu-id="1b1bc-105">Para copiar el contenido de un búfer fuera de pantalla en un búfer en pantalla, llame a [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span><span class="sxs-lookup"><span data-stu-id="1b1bc-105">To copy the contents of an off-screen buffer to an on-screen buffer, call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span> <span data-ttu-id="1b1bc-106">La función **SwapBuffers** toma un identificador de un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b1bc-106">The **SwapBuffers** function takes a handle to a device context.</span></span> <span data-ttu-id="1b1bc-107">El formato de píxel actual para el contexto de dispositivo especificado debe incluir un búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="1b1bc-107">The current pixel format for the specified device context must include a back buffer.</span></span> <span data-ttu-id="1b1bc-108">De forma predeterminada, el búfer de reserva está fuera de la pantalla y el búfer frontal está en pantalla.</span><span class="sxs-lookup"><span data-stu-id="1b1bc-108">By default, the back buffer is off-screen, and the front buffer is on-screen.</span></span>

> [!Note]  
> <span data-ttu-id="1b1bc-109">En realidad, la función **SwapBuffers** no intercambia el contenido de los dos búferes, sino que copia el contenido de un búfer en otro.</span><span class="sxs-lookup"><span data-stu-id="1b1bc-109">The **SwapBuffers** function does not really swap the contents of the two buffers, but rather copies the contents of one buffer to another.</span></span> <span data-ttu-id="1b1bc-110">El contenido del búfer fuera de pantalla no está definido después de una llamada a **SwapBuffers**.</span><span class="sxs-lookup"><span data-stu-id="1b1bc-110">The contents of the off-screen buffer are undefined after a call to **SwapBuffers**.</span></span> <span data-ttu-id="1b1bc-111">Por lo tanto, el resultado de dos llamadas consecutivas a **SwapBuffers** es undefined.</span><span class="sxs-lookup"><span data-stu-id="1b1bc-111">Thus, the result of two consecutive calls to **SwapBuffers** is undefined.</span></span>

 

<span data-ttu-id="1b1bc-112">En la ilustración siguiente se muestra cómo se copia el contenido de los búferes al llamar a **SwapBuffers**.</span><span class="sxs-lookup"><span data-stu-id="1b1bc-112">The following illustration shows how the contents of the buffers are copied when calling **SwapBuffers**.</span></span>

![Diagrama que muestra los resultados no definidos de llamadas consecutivas a la función SwapBuffers.](images/opengl00.png)

<span data-ttu-id="1b1bc-114">Varias funciones básicas de OpenGL también administran los búferes.</span><span class="sxs-lookup"><span data-stu-id="1b1bc-114">Several OpenGL core functions also manage buffers.</span></span> <span data-ttu-id="1b1bc-115">La función [**glDrawBuffer**](gldrawbuffer.md) es la más relevante para el doble búfer; especifica los fotogramas o búferes en los que se dibuja OpenGL.</span><span class="sxs-lookup"><span data-stu-id="1b1bc-115">The [**glDrawBuffer**](gldrawbuffer.md) function is the one most relevant to double buffering; it specifies the framebuffer or buffers that OpenGL draws into.</span></span>

<span data-ttu-id="1b1bc-116">Las siguientes funciones también afectan a los búferes:</span><span class="sxs-lookup"><span data-stu-id="1b1bc-116">The following functions also affect buffers:</span></span>

-   [<span data-ttu-id="1b1bc-117">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="1b1bc-117">**glReadBuffer**</span></span>](glreadbuffer.md)
-   [<span data-ttu-id="1b1bc-118">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="1b1bc-118">**glReadPixels**</span></span>](glreadpixels.md)
-   [<span data-ttu-id="1b1bc-119">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="1b1bc-119">**glCopyPixels**</span></span>](glcopypixels.md)
-   [<span data-ttu-id="1b1bc-120">**glAccum**</span><span class="sxs-lookup"><span data-stu-id="1b1bc-120">**glAccum**</span></span>](glaccum.md)
-   [<span data-ttu-id="1b1bc-121">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="1b1bc-121">**glColorMask**</span></span>](glcolormask.md)
-   [<span data-ttu-id="1b1bc-122">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="1b1bc-122">**glDepthMask**</span></span>](gldepthmask.md)
-   [<span data-ttu-id="1b1bc-123">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="1b1bc-123">**glIndexMask**</span></span>](glindexmask.md)
-   [<span data-ttu-id="1b1bc-124">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="1b1bc-124">**glStencilMask**</span></span>](glstencilmask.md)
-   [<span data-ttu-id="1b1bc-125">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="1b1bc-125">**glClearAccum**</span></span>](glclearaccum.md)
-   [<span data-ttu-id="1b1bc-126">**glClearColor**</span><span class="sxs-lookup"><span data-stu-id="1b1bc-126">**glClearColor**</span></span>](glclearcolor.md)
-   [<span data-ttu-id="1b1bc-127">**glClearDepth**</span><span class="sxs-lookup"><span data-stu-id="1b1bc-127">**glClearDepth**</span></span>](glcleardepth.md)
-   [<span data-ttu-id="1b1bc-128">**glClearIndex**</span><span class="sxs-lookup"><span data-stu-id="1b1bc-128">**glClearIndex**</span></span>](glclearindex.md)
-   [<span data-ttu-id="1b1bc-129">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="1b1bc-129">**glClearStencil**</span></span>](glclearstencil.md)

 

 




