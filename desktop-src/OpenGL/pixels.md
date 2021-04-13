---
title: píxeles
description: Los fragmentos se convierten en píxeles en el fotogramas.
ms.assetid: 1925b455-ae6e-4f95-899c-4bcac641f549
keywords:
- OpenGL, píxeles
- Canalización de procesamiento de OpenGL, píxeles
- OpenGL de píxeles
- framebuffers, convertir fragmentos en píxeles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6660452930683943da780fad3aeb001e531711
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419126"
---
# <a name="pixels"></a><span data-ttu-id="3726f-107">píxeles</span><span class="sxs-lookup"><span data-stu-id="3726f-107">Pixels</span></span>

<span data-ttu-id="3726f-108">Los fragmentos se convierten en píxeles en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="3726f-108">Fragments are converted to pixels in the framebuffer.</span></span> <span data-ttu-id="3726f-109">El fotogramas se organiza en un conjunto de búferes lógicos, el color, la profundidad, el estarcido y los búferes de acumulación.</span><span class="sxs-lookup"><span data-stu-id="3726f-109">The framebuffer is organized into a set of logical buffers the color, depth, stencil, and accumulation buffers.</span></span> <span data-ttu-id="3726f-110">El búfer de color se compone de una parte delantera izquierda, frontal derecha, posterior izquierda, atrás a la derecha y un número de búferes auxiliares.</span><span class="sxs-lookup"><span data-stu-id="3726f-110">The color buffer itself consists of a front left, front right, back left, back right, and some number of auxiliary buffers.</span></span> <span data-ttu-id="3726f-111">Puede emitir funciones para controlar estos búferes y leer o copiar directamente píxeles de ellos.</span><span class="sxs-lookup"><span data-stu-id="3726f-111">You can issue functions to control these buffers, and directly read or copy pixels from them.</span></span> <span data-ttu-id="3726f-112">(Tenga en cuenta que el contexto de OpenGL concreto que está usando no puede proporcionar todos estos búferes).</span><span class="sxs-lookup"><span data-stu-id="3726f-112">(Note that the particular OpenGL context you're using may not provide all these buffers.)</span></span>

-   [<span data-ttu-id="3726f-113">Operaciones de fotogramas</span><span class="sxs-lookup"><span data-stu-id="3726f-113">Framebuffer Operations</span></span>](framebuffer-operations.md)
-   [<span data-ttu-id="3726f-114">Leer o copiar píxeles</span><span class="sxs-lookup"><span data-stu-id="3726f-114">Reading or Copying Pixels</span></span>](reading-or-copying-pixels.md)
-   [<span data-ttu-id="3726f-115">Referencia de píxeles</span><span class="sxs-lookup"><span data-stu-id="3726f-115">Pixels Reference</span></span>](pixels-reference.md)

 

 




