---
title: Portabilidad de las funciones de prueba de afunction
description: En la tabla siguiente se enumeran las funciones de prueba alfa de IRIS GL disponibles y sus funciones de OpenGL equivalentes.
ms.assetid: cd4082fe-2fd6-43d8-a9a7-37fd448c084b
keywords:
- Migración de la contabilidad de IRIS, funciones de prueba de afunction
- portabilidad desde IRIS GL, afunction test Functions
- trasladar a OpenGL desde IRIS GL, afunction test Functions
- Exportación de OpenGL desde IRIS GL, afunction test Functions
- funciones de prueba de afunction
- funciones de prueba alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3abfd3ba46d99f8b70ecfb97c0160efea944ccd2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903842"
---
# <a name="porting-afunction-test-functions"></a><span data-ttu-id="556cb-109">Portabilidad de las funciones de prueba de afunction</span><span class="sxs-lookup"><span data-stu-id="556cb-109">Porting afunction Test Functions</span></span>

<span data-ttu-id="556cb-110">En la tabla siguiente se enumeran las funciones de prueba alfa de IRIS GL disponibles y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="556cb-110">The following table lists the available IRIS GL alpha test functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="556cb-111">afunction</span><span class="sxs-lookup"><span data-stu-id="556cb-111">afunction</span></span>    | <span data-ttu-id="556cb-112">glAlphaFunc</span><span class="sxs-lookup"><span data-stu-id="556cb-112">glAlphaFunc</span></span>  |
|--------------|--------------|
| <span data-ttu-id="556cb-113">NOTEQUAL de AF \_</span><span class="sxs-lookup"><span data-stu-id="556cb-113">AF\_NOTEQUAL</span></span> | <span data-ttu-id="556cb-114">NOTEQUAL en GL \_</span><span class="sxs-lookup"><span data-stu-id="556cb-114">GL\_NOTEQUAL</span></span> |
| <span data-ttu-id="556cb-115">AF \_ siempre</span><span class="sxs-lookup"><span data-stu-id="556cb-115">AF\_ALWAYS</span></span>   | <span data-ttu-id="556cb-116">GL \_ siempre</span><span class="sxs-lookup"><span data-stu-id="556cb-116">GL\_ALWAYS</span></span>   |
| <span data-ttu-id="556cb-117">AF \_ nunca</span><span class="sxs-lookup"><span data-stu-id="556cb-117">AF\_NEVER</span></span>    | <span data-ttu-id="556cb-118">GL \_ nunca</span><span class="sxs-lookup"><span data-stu-id="556cb-118">GL\_NEVER</span></span>    |
| <span data-ttu-id="556cb-119">AF \_ menos</span><span class="sxs-lookup"><span data-stu-id="556cb-119">AF\_LESS</span></span>     | <span data-ttu-id="556cb-120">CONTABILIDAD \_ inferior</span><span class="sxs-lookup"><span data-stu-id="556cb-120">GL\_LESS</span></span>     |
| <span data-ttu-id="556cb-121">igual a AF \_</span><span class="sxs-lookup"><span data-stu-id="556cb-121">AF\_EQUAL</span></span>    | <span data-ttu-id="556cb-122">igual a GL \_</span><span class="sxs-lookup"><span data-stu-id="556cb-122">GL\_EQUAL</span></span>    |
| <span data-ttu-id="556cb-123">AF \_ LEQUAL</span><span class="sxs-lookup"><span data-stu-id="556cb-123">AF\_LEQUAL</span></span>   | <span data-ttu-id="556cb-124">GL \_ LEQUAL</span><span class="sxs-lookup"><span data-stu-id="556cb-124">GL\_LEQUAL</span></span>   |
| <span data-ttu-id="556cb-125">AF \_ mayor</span><span class="sxs-lookup"><span data-stu-id="556cb-125">AF\_GREATER</span></span>  | <span data-ttu-id="556cb-126">LIBRO \_ superior</span><span class="sxs-lookup"><span data-stu-id="556cb-126">GL\_GREATER</span></span>  |
| <span data-ttu-id="556cb-127">AF \_ GEQUAL</span><span class="sxs-lookup"><span data-stu-id="556cb-127">AF\_GEQUAL</span></span>   | <span data-ttu-id="556cb-128">GL \_ GEQUAL</span><span class="sxs-lookup"><span data-stu-id="556cb-128">GL\_GEQUAL</span></span>   |



 

 

 




