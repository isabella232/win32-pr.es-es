---
title: Problemas de migración del libro de contabilidad de IRIS especial
description: Problemas de migración del libro de contabilidad de IRIS especial
ms.assetid: dcf7967a-2867-4443-a1c8-8335c6fe016a
keywords:
- OpenGL en Windows, migración de la contabilidad de IRIS
- trasladar a OpenGL, IRIS GL
- Portabilidad de OpenGL, IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1273a873f3a39a5d237f9a5845a72f87156e001c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665729"
---
# <a name="special-iris-gl-porting-issues"></a><span data-ttu-id="effdb-106">Problemas de migración del libro de contabilidad de IRIS especial</span><span class="sxs-lookup"><span data-stu-id="effdb-106">Special IRIS GL Porting Issues</span></span>

<span data-ttu-id="effdb-107">En los temas siguientes se describen las técnicas para portar partes específicas del código de la contabilidad de IRIS a código OpenGL.</span><span class="sxs-lookup"><span data-stu-id="effdb-107">The following topics describe techniques for porting specific parts of your IRIS GL code to OpenGL code.</span></span>

-   [<span data-ttu-id="effdb-108">Trasladar greset</span><span class="sxs-lookup"><span data-stu-id="effdb-108">Porting greset</span></span>](porting-greset.md)
-   [<span data-ttu-id="effdb-109">Trasladar funciones de "obtener" de IRIS GL</span><span class="sxs-lookup"><span data-stu-id="effdb-109">Porting IRIS GL "Get" Functions</span></span>](porting-iris-gl-get-functions.md)
-   [<span data-ttu-id="effdb-110">Trasladar código que requiere una posición de gráficos actual</span><span class="sxs-lookup"><span data-stu-id="effdb-110">Porting Code that Requires a Current Graphics Position</span></span>](porting-code-that-requires-a-current-graphics-position.md)
-   [<span data-ttu-id="effdb-111">Trasladar funciones de dibujo</span><span class="sxs-lookup"><span data-stu-id="effdb-111">Porting Drawing Functions</span></span>](porting-drawing-functions.md)
-   [<span data-ttu-id="effdb-112">Trasladar el código de color, sombreado y Writemask</span><span class="sxs-lookup"><span data-stu-id="effdb-112">Porting Color, Shading, and Writemask Code</span></span>](porting-color--shading--and-writemask-code.md)
-   [<span data-ttu-id="effdb-113">Trasladar operaciones de píxeles</span><span class="sxs-lookup"><span data-stu-id="effdb-113">Porting Pixel Operations</span></span>](porting-pixel-operations.md)
-   [<span data-ttu-id="effdb-114">Comandos de cueing y niebla de profundidad de portabilidad</span><span class="sxs-lookup"><span data-stu-id="effdb-114">Porting Depth Cueing and Fog Commands</span></span>](porting-depth-cueing-and-fog-commands.md)
-   [<span data-ttu-id="effdb-115">Trasladar funciones de curva y superficie</span><span class="sxs-lookup"><span data-stu-id="effdb-115">Porting Curve and Surface Functions</span></span>](porting-curve-and-surface-functions.md)
-   [<span data-ttu-id="effdb-116">Trasladar funciones de suavizado de contorno</span><span class="sxs-lookup"><span data-stu-id="effdb-116">Porting Antialiasing Functions</span></span>](porting-antialiasing-functions.md)
-   [<span data-ttu-id="effdb-117">Trasladar llamadas del búfer de acumulación</span><span class="sxs-lookup"><span data-stu-id="effdb-117">Porting Accumulation Buffer Calls</span></span>](porting-accumulation-buffer-calls.md)
-   [<span data-ttu-id="effdb-118">Trasladar llamadas de plano de estarcido</span><span class="sxs-lookup"><span data-stu-id="effdb-118">Porting Stencil Plane Calls</span></span>](porting-stencil-plane-calls.md)
-   [<span data-ttu-id="effdb-119">Portabilidad de listas de presentación</span><span class="sxs-lookup"><span data-stu-id="effdb-119">Porting Display Lists</span></span>](porting-display-lists.md)
-   [<span data-ttu-id="effdb-120">Portabilidad de los conjuntos, enlaces y conjuntos</span><span class="sxs-lookup"><span data-stu-id="effdb-120">Porting Defs, Binds, and Sets</span></span>](porting-defs--binds--and-sets.md)
-   [<span data-ttu-id="effdb-121">Trasladar funciones de iluminación y de materiales</span><span class="sxs-lookup"><span data-stu-id="effdb-121">Porting Lighting and Materials Functions</span></span>](porting-lighting-and-materials-functions.md)
-   [<span data-ttu-id="effdb-122">Trasladar funciones de textura</span><span class="sxs-lookup"><span data-stu-id="effdb-122">Porting Texture Functions</span></span>](porting-texture-functions.md)
-   [<span data-ttu-id="effdb-123">Trasladar funciones de picking</span><span class="sxs-lookup"><span data-stu-id="effdb-123">Porting Picking Functions</span></span>](porting-picking-functions.md)
-   [<span data-ttu-id="effdb-124">Trasladar funciones de comentarios</span><span class="sxs-lookup"><span data-stu-id="effdb-124">Porting Feedback Functions</span></span>](porting-feedback-functions.md)

 

 




