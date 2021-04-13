---
title: Trasladar triángulos
description: Puede dibujar tres tipos de triángulos en OpenGL independientes triángulos, franjas de triángulo y ventiladores de triángulo.
ms.assetid: 48617892-c9a0-4c67-b42e-afa4243023e7
keywords:
- Migración de la contabilidad de IRIS, triángulos
- trasladar de IRIS GL, triángulos
- trasladar a OpenGL desde IRIS GL, triángulos
- Exportación de OpenGL desde IRIS GL, triángulos
- dibujar funciones, triángulos
- triángulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c7a0af4b538bb951cf0d1c5f2e12b2e1badda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357350"
---
# <a name="porting-triangles"></a><span data-ttu-id="e5e5b-109">Trasladar triángulos</span><span class="sxs-lookup"><span data-stu-id="e5e5b-109">Porting Triangles</span></span>

<span data-ttu-id="e5e5b-110">Puede dibujar tres tipos de triángulos en OpenGL: triángulos, tiras de triángulo y ventiladores de triángulo independientes.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-110">You can draw three types of triangles in OpenGL: separate triangles, triangle strips, and triangle fans.</span></span>

<span data-ttu-id="e5e5b-111">OpenGL no tiene equivalente a la función **swaptmesh** de la contabilidad de iris.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-111">OpenGL has no equivalent for the IRIS GL **swaptmesh** function.</span></span> <span data-ttu-id="e5e5b-112">Puede lograr el mismo efecto mediante una combinación de triángulos, tiras de triángulo y ventiladores de triángulo.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-112">You can achieve the same effect using a combination of triangles, triangle strips, and triangle fans.</span></span>

<span data-ttu-id="e5e5b-113">En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para dibujar triángulos y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-113">The following table lists the IRIS GL functions for drawing triangles and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="e5e5b-114">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="e5e5b-114">IRIS GL function</span></span>           | <span data-ttu-id="e5e5b-115">Parámetro glBegin equivalente</span><span class="sxs-lookup"><span data-stu-id="e5e5b-115">Equivalent glBegin parameter</span></span> | <span data-ttu-id="e5e5b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="e5e5b-116">Meaning</span></span>                                       |
|----------------------------|------------------------------|-----------------------------------------------|
|                            | <span data-ttu-id="e5e5b-117">triángulos de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="e5e5b-117">GL\_TRIANGLES</span></span>                | <span data-ttu-id="e5e5b-118">Las tripas de los vértices se interpretan como triángulos.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-118">Triples of vertices interpreted as triangles.</span></span> |
| <span data-ttu-id="e5e5b-119">**bgntmesh**, **endtmesh**</span><span class="sxs-lookup"><span data-stu-id="e5e5b-119">**bgntmesh**, **endtmesh**</span></span> | <span data-ttu-id="e5e5b-120">\_franja de triángulo de GL \_</span><span class="sxs-lookup"><span data-stu-id="e5e5b-120">GL\_TRIANGLE\_STRIP</span></span>          | <span data-ttu-id="e5e5b-121">Bandas de triángulos vinculadas.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-121">Linked strips of triangles.</span></span>                   |
|                            | <span data-ttu-id="e5e5b-122">\_ventilador de triángulo GL \_</span><span class="sxs-lookup"><span data-stu-id="e5e5b-122">GL\_TRIANGLE\_FAN</span></span>            | <span data-ttu-id="e5e5b-123">Ventiladores vinculados de triángulos.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-123">Linked fans of triangles.</span></span>                     |



 

<span data-ttu-id="e5e5b-124">??</span><span class="sxs-lookup"><span data-stu-id="e5e5b-124">??</span></span>

 

 




