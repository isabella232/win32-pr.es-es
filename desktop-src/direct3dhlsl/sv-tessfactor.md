---
title: SV_TessFactor
description: Define la cantidad de teselación en cada borde de una revisión.
ms.assetid: 970ff744-da5b-4933-866c-dd38b85fb48d
keywords:
- SV_TessFactor HLSL
topic_type:
- apiref
api_name:
- SV_TessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 808365fbcba4a1180c1838b94a6c098aa4c6f9ac
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999062"
---
# <a name="sv_tessfactor"></a><span data-ttu-id="2d9cc-104">SV \_ TessFactor</span><span class="sxs-lookup"><span data-stu-id="2d9cc-104">SV\_TessFactor</span></span>

<span data-ttu-id="2d9cc-105">Define la cantidad de teselación en cada borde de una revisión.</span><span class="sxs-lookup"><span data-stu-id="2d9cc-105">Defines the tessellation amount on each edge of a patch.</span></span>

## <a name="type"></a><span data-ttu-id="2d9cc-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="2d9cc-106">Type</span></span>



|            |                |
|------------|----------------|
| <span data-ttu-id="2d9cc-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="2d9cc-107">Type</span></span>       | <span data-ttu-id="2d9cc-108">Topología de entrada</span><span class="sxs-lookup"><span data-stu-id="2d9cc-108">Input Topology</span></span> |
| <span data-ttu-id="2d9cc-109">float \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="2d9cc-109">float\[4\]</span></span> | <span data-ttu-id="2d9cc-110">revisión quad</span><span class="sxs-lookup"><span data-stu-id="2d9cc-110">quad patch</span></span>     |
| <span data-ttu-id="2d9cc-111">float \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="2d9cc-111">float\[3\]</span></span> | <span data-ttu-id="2d9cc-112">tri patch</span><span class="sxs-lookup"><span data-stu-id="2d9cc-112">tri patch</span></span>      |
| <span data-ttu-id="2d9cc-113">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="2d9cc-113">float\[2\]</span></span> | <span data-ttu-id="2d9cc-114">Isolínea</span><span class="sxs-lookup"><span data-stu-id="2d9cc-114">isoline</span></span>        |



 

<span data-ttu-id="2d9cc-115">Los factores de teselación deben declararse como una matriz; no se pueden empaquetar en un solo vector.</span><span class="sxs-lookup"><span data-stu-id="2d9cc-115">Tessellation factors must be declared as an array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d9cc-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2d9cc-116">Remarks</span></span>

<span data-ttu-id="2d9cc-117">El valor del factor de teselación debe definirse durante la función de constante de revisión del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="2d9cc-117">The value for tessellation factor must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="2d9cc-118">Valor de salida necesario para el sombreador de casco si se usan revisiones quad o tri.</span><span class="sxs-lookup"><span data-stu-id="2d9cc-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="2d9cc-119">Este valor también es un valor de entrada necesario para que el sombreador de dominio coincida con las firmas de datos de revisión constante entre las fases de teselación.</span><span class="sxs-lookup"><span data-stu-id="2d9cc-119">This value is also a required input value for the domain shader to match the patch-constant data signatures between the tessellation stages.</span></span>

<span data-ttu-id="2d9cc-120">Para una isolínea, el primer valor de SV TessFactor es el factor de teselación de densidad de línea, el segundo valor es el factor de teselación de detalle \_ de línea.</span><span class="sxs-lookup"><span data-stu-id="2d9cc-120">For an isoline, the first value in SV\_TessFactor is the line-density tessellation factor, the second value is the line-detail tessellation factor.</span></span>

### <a name="tri-patch-tessellation-factors"></a><span data-ttu-id="2d9cc-121">Tres factores de teselación de revisión</span><span class="sxs-lookup"><span data-stu-id="2d9cc-121">Tri Patch Tessellation Factors</span></span>

<span data-ttu-id="2d9cc-122">El primer componente proporciona el factor de tesselation para el borde u==0 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="2d9cc-122">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="2d9cc-123">El segundo componente proporciona el factor de tesselation para el borde v==0 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="2d9cc-123">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="2d9cc-124">El tercer componente proporciona el factor de tesselation para el borde w==0 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="2d9cc-124">The third component provides the tesselation factor for the w==0 edge of the patch.</span></span>

### <a name="quad-patch-tessellation-factors"></a><span data-ttu-id="2d9cc-125">Factores de teselación de cuatro revisiones</span><span class="sxs-lookup"><span data-stu-id="2d9cc-125">Quad Patch Tessellation Factors</span></span>

<span data-ttu-id="2d9cc-126">El primer componente proporciona el factor de tesselation para el borde u==0 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="2d9cc-126">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="2d9cc-127">El segundo componente proporciona el factor de tesselation para el borde v==0 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="2d9cc-127">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="2d9cc-128">El tercer componente proporciona el factor de tesselation para el borde u==1 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="2d9cc-128">The third component provides the tesselation factor for the u==1 edge of the patch.</span></span> <span data-ttu-id="2d9cc-129">El cuarto componente proporciona el factor de tesselation para el borde v==1 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="2d9cc-129">The fourth component provides the tesselation factor for the v==1 edge of the patch.</span></span> <span data-ttu-id="2d9cc-130">El orden de los bordes es en el sentido de las agujas del reloj, empezando por el borde u==0, que es el lado izquierdo de la revisión, y desde el borde v==0, que es la parte superior de la revisión.</span><span class="sxs-lookup"><span data-stu-id="2d9cc-130">The ordering of the edges is clockwise, starting from the u==0 edge, which is the left side of the patch, and from the v==0 edge, which is the top of the patch.</span></span>

<span data-ttu-id="2d9cc-131">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="2d9cc-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="2d9cc-132">Vértice</span><span class="sxs-lookup"><span data-stu-id="2d9cc-132">Vertex</span></span> | <span data-ttu-id="2d9cc-133">Casco</span><span class="sxs-lookup"><span data-stu-id="2d9cc-133">Hull</span></span> | <span data-ttu-id="2d9cc-134">Domain</span><span class="sxs-lookup"><span data-stu-id="2d9cc-134">Domain</span></span> | <span data-ttu-id="2d9cc-135">Geometría</span><span class="sxs-lookup"><span data-stu-id="2d9cc-135">Geometry</span></span> | <span data-ttu-id="2d9cc-136">Píxel</span><span class="sxs-lookup"><span data-stu-id="2d9cc-136">Pixel</span></span> | <span data-ttu-id="2d9cc-137">Proceso</span><span class="sxs-lookup"><span data-stu-id="2d9cc-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="2d9cc-138">x</span><span class="sxs-lookup"><span data-stu-id="2d9cc-138">x</span></span>    | <span data-ttu-id="2d9cc-139">x</span><span class="sxs-lookup"><span data-stu-id="2d9cc-139">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="2d9cc-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d9cc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d9cc-141">Semántica</span><span class="sxs-lookup"><span data-stu-id="2d9cc-141">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="2d9cc-142">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2d9cc-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




