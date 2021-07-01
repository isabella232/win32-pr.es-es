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
ms.openlocfilehash: 308034fe607283ef9f1213cca1cabb4a7229765e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118900"
---
# <a name="sv_tessfactor"></a><span data-ttu-id="3cf9c-104">SV \_ TessFactor</span><span class="sxs-lookup"><span data-stu-id="3cf9c-104">SV\_TessFactor</span></span>

<span data-ttu-id="3cf9c-105">Define la cantidad de teselación en cada borde de una revisión.</span><span class="sxs-lookup"><span data-stu-id="3cf9c-105">Defines the tessellation amount on each edge of a patch.</span></span>

## <a name="type"></a><span data-ttu-id="3cf9c-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="3cf9c-106">Type</span></span>



|  <span data-ttu-id="3cf9c-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="3cf9c-107">Type</span></span>          |  <span data-ttu-id="3cf9c-108">Topología de entrada</span><span class="sxs-lookup"><span data-stu-id="3cf9c-108">Input topology</span></span>              |
|------------|----------------|
| <span data-ttu-id="3cf9c-109">float \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="3cf9c-109">float\[4\]</span></span> | <span data-ttu-id="3cf9c-110">revisión quad</span><span class="sxs-lookup"><span data-stu-id="3cf9c-110">quad patch</span></span>     |
| <span data-ttu-id="3cf9c-111">float \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="3cf9c-111">float\[3\]</span></span> | <span data-ttu-id="3cf9c-112">tri patch</span><span class="sxs-lookup"><span data-stu-id="3cf9c-112">tri patch</span></span>      |
| <span data-ttu-id="3cf9c-113">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="3cf9c-113">float\[2\]</span></span> | <span data-ttu-id="3cf9c-114">Isolínea</span><span class="sxs-lookup"><span data-stu-id="3cf9c-114">isoline</span></span>        |



 

<span data-ttu-id="3cf9c-115">Los factores de teselación deben declararse como una matriz; no se pueden empaquetar en un solo vector.</span><span class="sxs-lookup"><span data-stu-id="3cf9c-115">Tessellation factors must be declared as an array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cf9c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3cf9c-116">Remarks</span></span>

<span data-ttu-id="3cf9c-117">El valor del factor de teselación debe definirse durante la función constante de revisión del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="3cf9c-117">The value for tessellation factor must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="3cf9c-118">Valor de salida necesario para el sombreador de casco si se usan revisiones quad o tri.</span><span class="sxs-lookup"><span data-stu-id="3cf9c-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="3cf9c-119">Este valor también es un valor de entrada necesario para que el sombreador de dominio coincida con las firmas de datos de revisión constante entre las fases de teselación.</span><span class="sxs-lookup"><span data-stu-id="3cf9c-119">This value is also a required input value for the domain shader to match the patch-constant data signatures between the tessellation stages.</span></span>

<span data-ttu-id="3cf9c-120">Para una isolínea, el primer valor de SV TessFactor es el factor de teselación de densidad de línea, el segundo valor es el factor de teselación de detalle \_ de línea.</span><span class="sxs-lookup"><span data-stu-id="3cf9c-120">For an isoline, the first value in SV\_TessFactor is the line-density tessellation factor, the second value is the line-detail tessellation factor.</span></span>

### <a name="tri-patch-tessellation-factors"></a><span data-ttu-id="3cf9c-121">Factores de teselación de tres revisiones</span><span class="sxs-lookup"><span data-stu-id="3cf9c-121">Tri Patch Tessellation Factors</span></span>

<span data-ttu-id="3cf9c-122">El primer componente proporciona el factor de tesselation para el borde u==0 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="3cf9c-122">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="3cf9c-123">El segundo componente proporciona el factor de tesselation para el borde v==0 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="3cf9c-123">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="3cf9c-124">El tercer componente proporciona el factor de tesselation para el borde w==0 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="3cf9c-124">The third component provides the tesselation factor for the w==0 edge of the patch.</span></span>

### <a name="quad-patch-tessellation-factors"></a><span data-ttu-id="3cf9c-125">Factores de teselación de cuatro revisiones</span><span class="sxs-lookup"><span data-stu-id="3cf9c-125">Quad Patch Tessellation Factors</span></span>

<span data-ttu-id="3cf9c-126">El primer componente proporciona el factor de tesselation para el borde u==0 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="3cf9c-126">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="3cf9c-127">El segundo componente proporciona el factor de tesselation para el borde v==0 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="3cf9c-127">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="3cf9c-128">El tercer componente proporciona el factor de tesselation para el borde u==1 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="3cf9c-128">The third component provides the tesselation factor for the u==1 edge of the patch.</span></span> <span data-ttu-id="3cf9c-129">El cuarto componente proporciona el factor de tesselation para el borde v==1 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="3cf9c-129">The fourth component provides the tesselation factor for the v==1 edge of the patch.</span></span> <span data-ttu-id="3cf9c-130">El orden de los bordes es en el sentido de las agujas del reloj, empezando por el borde u==0, que es el lado izquierdo de la revisión, y desde el borde v==0, que es la parte superior de la revisión.</span><span class="sxs-lookup"><span data-stu-id="3cf9c-130">The ordering of the edges is clockwise, starting from the u==0 edge, which is the left side of the patch, and from the v==0 edge, which is the top of the patch.</span></span>

<span data-ttu-id="3cf9c-131">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="3cf9c-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="3cf9c-132">Vértice</span><span class="sxs-lookup"><span data-stu-id="3cf9c-132">Vertex</span></span> | <span data-ttu-id="3cf9c-133">Casco</span><span class="sxs-lookup"><span data-stu-id="3cf9c-133">Hull</span></span> | <span data-ttu-id="3cf9c-134">Domain</span><span class="sxs-lookup"><span data-stu-id="3cf9c-134">Domain</span></span> | <span data-ttu-id="3cf9c-135">Geometría</span><span class="sxs-lookup"><span data-stu-id="3cf9c-135">Geometry</span></span> | <span data-ttu-id="3cf9c-136">Píxel</span><span class="sxs-lookup"><span data-stu-id="3cf9c-136">Pixel</span></span> | <span data-ttu-id="3cf9c-137">Proceso</span><span class="sxs-lookup"><span data-stu-id="3cf9c-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="3cf9c-138">x</span><span class="sxs-lookup"><span data-stu-id="3cf9c-138">x</span></span>    | <span data-ttu-id="3cf9c-139">x</span><span class="sxs-lookup"><span data-stu-id="3cf9c-139">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="3cf9c-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3cf9c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cf9c-141">Semántica</span><span class="sxs-lookup"><span data-stu-id="3cf9c-141">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="3cf9c-142">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3cf9c-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




