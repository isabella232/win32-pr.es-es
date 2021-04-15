---
title: Fragments
description: Fragments
ms.assetid: bc400251-32c4-4477-ba0c-a0046fe85327
keywords:
- OpenGL, fragmentos
- Canalización de procesamiento de OpenGL, fragmentos
- fragmentos OpenGL
- framebuffers, fragmentos modificar píxeles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e2b4c2dc36e24c4fd9baa82b28fa4d336f69b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676193"
---
# <a name="fragments"></a><span data-ttu-id="0e0cd-107">Fragments</span><span class="sxs-lookup"><span data-stu-id="0e0cd-107">Fragments</span></span>

<span data-ttu-id="0e0cd-108">Un fragmento generado mediante la rasterización modifica el píxel correspondiente en el fotogramas solo si pasa las siguientes pruebas:</span><span class="sxs-lookup"><span data-stu-id="0e0cd-108">A fragment produced by rasterization modifies the corresponding pixel in the framebuffer only if it passes the following tests:</span></span>

-   [<span data-ttu-id="0e0cd-109">Prueba de propiedad de píxeles</span><span class="sxs-lookup"><span data-stu-id="0e0cd-109">Pixel ownership test</span></span>](pixel-ownership-test.md)
-   [<span data-ttu-id="0e0cd-110">Prueba de tijera</span><span class="sxs-lookup"><span data-stu-id="0e0cd-110">Scissor test</span></span>](scissor-test.md)
-   [<span data-ttu-id="0e0cd-111">Prueba alfa</span><span class="sxs-lookup"><span data-stu-id="0e0cd-111">Alpha test</span></span>](alpha-test.md)
-   [<span data-ttu-id="0e0cd-112">Prueba de estarcido</span><span class="sxs-lookup"><span data-stu-id="0e0cd-112">Stencil test</span></span>](stencil-test.md)
-   [<span data-ttu-id="0e0cd-113">Prueba de búfer de profundidad</span><span class="sxs-lookup"><span data-stu-id="0e0cd-113">Depth-buffer test</span></span>](depth-buffer-test.md)

<span data-ttu-id="0e0cd-114">Si se supera, los datos del fragmento pueden reemplazar los valores de fotogramas existentes o puede combinarlos con los datos existentes en el fotogramas, en función del estado de ciertos modos.</span><span class="sxs-lookup"><span data-stu-id="0e0cd-114">If it passes, the fragment's data can replace the existing framebuffer values, or you can combine it with existing data in the framebuffer, depending on the state of certain modes.</span></span> <span data-ttu-id="0e0cd-115">Puede combinar el fragmento con datos en fotogramas por:</span><span class="sxs-lookup"><span data-stu-id="0e0cd-115">You can combine the fragment with data in the framebuffer by:</span></span>

-   [<span data-ttu-id="0e0cd-116">Combinación</span><span class="sxs-lookup"><span data-stu-id="0e0cd-116">Blending</span></span>](blending.md)
-   [<span data-ttu-id="0e0cd-117">Interpolación</span><span class="sxs-lookup"><span data-stu-id="0e0cd-117">Dithering</span></span>](dithering.md)
-   [<span data-ttu-id="0e0cd-118">Operaciones lógicas</span><span class="sxs-lookup"><span data-stu-id="0e0cd-118">Logical operations</span></span>](logical-operations.md)

 

 




