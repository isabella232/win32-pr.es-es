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
ms.openlocfilehash: 8fa49b19109985b590747098826199b33a32dd2d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104983767"
---
# <a name="sv_tessfactor"></a><span data-ttu-id="c6e17-104">VP \_ TessFactor</span><span class="sxs-lookup"><span data-stu-id="c6e17-104">SV\_TessFactor</span></span>

<span data-ttu-id="c6e17-105">Define la cantidad de teselación en cada borde de una revisión.</span><span class="sxs-lookup"><span data-stu-id="c6e17-105">Defines the tessellation amount on each edge of a patch.</span></span>

## <a name="type"></a><span data-ttu-id="c6e17-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6e17-106">Type</span></span>



|            |                |
|------------|----------------|
| <span data-ttu-id="c6e17-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6e17-107">Type</span></span>       | <span data-ttu-id="c6e17-108">Topología de entrada</span><span class="sxs-lookup"><span data-stu-id="c6e17-108">Input Topology</span></span> |
| <span data-ttu-id="c6e17-109">Float \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="c6e17-109">float\[4\]</span></span> | <span data-ttu-id="c6e17-110">revisión cuádruple</span><span class="sxs-lookup"><span data-stu-id="c6e17-110">quad patch</span></span>     |
| <span data-ttu-id="c6e17-111">Float \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="c6e17-111">float\[3\]</span></span> | <span data-ttu-id="c6e17-112">Tri patch</span><span class="sxs-lookup"><span data-stu-id="c6e17-112">tri patch</span></span>      |
| <span data-ttu-id="c6e17-113">Float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="c6e17-113">float\[2\]</span></span> | <span data-ttu-id="c6e17-114">isolínea</span><span class="sxs-lookup"><span data-stu-id="c6e17-114">isoline</span></span>        |



 

<span data-ttu-id="c6e17-115">Los factores de teselación se deben declarar como una matriz; no se pueden empaquetar en un único vector.</span><span class="sxs-lookup"><span data-stu-id="c6e17-115">Tessellation factors must be declared as an array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6e17-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6e17-116">Remarks</span></span>

<span data-ttu-id="c6e17-117">El valor del factor de teselación debe definirse durante la función de constante patch del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="c6e17-117">The value for tessellation factor must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="c6e17-118">Valor de salida necesario para el sombreador de casco si se usan cuatro o tres revisiones.</span><span class="sxs-lookup"><span data-stu-id="c6e17-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="c6e17-119">Este valor también es un valor de entrada necesario para que el sombreador de dominios coincida con las firmas de datos constantes de revisión entre las fases de teselación.</span><span class="sxs-lookup"><span data-stu-id="c6e17-119">This value is also a required input value for the domain shader to match the patch-constant data signatures between the tessellation stages.</span></span>

<span data-ttu-id="c6e17-120">En el caso de una isolínea, el primer valor de VP \_ TessFactor es el factor de teselación de densidad de línea, el segundo valor es el factor de teselación de detalles de línea.</span><span class="sxs-lookup"><span data-stu-id="c6e17-120">For an isoline, the first value in SV\_TessFactor is the line-density tessellation factor, the second value is the line-detail tessellation factor.</span></span>

### <a name="tri-patch-tessellation-factors"></a><span data-ttu-id="c6e17-121">Tri factores de teselación de revisiones</span><span class="sxs-lookup"><span data-stu-id="c6e17-121">Tri Patch Tessellation Factors</span></span>

<span data-ttu-id="c6e17-122">El primer componente proporciona el factor tesselation para el borde u = = 0 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="c6e17-122">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="c6e17-123">El segundo componente proporciona el factor tesselation para el borde v = = 0 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="c6e17-123">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="c6e17-124">El tercer componente proporciona el factor tesselation para el borde w = = 0 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="c6e17-124">The third component provides the tesselation factor for the w==0 edge of the patch.</span></span>

### <a name="quad-patch-tessellation-factors"></a><span data-ttu-id="c6e17-125">Factores de teselación de cuatro revisiones</span><span class="sxs-lookup"><span data-stu-id="c6e17-125">Quad Patch Tessellation Factors</span></span>

<span data-ttu-id="c6e17-126">El primer componente proporciona el factor tesselation para el borde u = = 0 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="c6e17-126">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="c6e17-127">El segundo componente proporciona el factor tesselation para el borde v = = 0 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="c6e17-127">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="c6e17-128">El tercer componente proporciona el factor tesselation para el borde u = = 1 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="c6e17-128">The third component provides the tesselation factor for the u==1 edge of the patch.</span></span> <span data-ttu-id="c6e17-129">El cuarto componente proporciona el factor tesselation para el borde v = = 1 de la revisión.</span><span class="sxs-lookup"><span data-stu-id="c6e17-129">The fourth component provides the tesselation factor for the v==1 edge of the patch.</span></span> <span data-ttu-id="c6e17-130">El orden de los bordes es en el sentido de las agujas del reloj, empezando desde el borde u = = 0, que es el lado izquierdo de la revisión, y desde el borde v = = 0, que es la parte superior de la revisión.</span><span class="sxs-lookup"><span data-stu-id="c6e17-130">The ordering of the edges is clockwise, starting from the u==0 edge, which is the left side of the patch, and from the v==0 edge, which is the top of the patch.</span></span>

<span data-ttu-id="c6e17-131">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="c6e17-131">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c6e17-132">Vértice</span><span class="sxs-lookup"><span data-stu-id="c6e17-132">Vertex</span></span> | <span data-ttu-id="c6e17-133">Casco</span><span class="sxs-lookup"><span data-stu-id="c6e17-133">Hull</span></span> | <span data-ttu-id="c6e17-134">Dominio</span><span class="sxs-lookup"><span data-stu-id="c6e17-134">Domain</span></span> | <span data-ttu-id="c6e17-135">Geometría</span><span class="sxs-lookup"><span data-stu-id="c6e17-135">Geometry</span></span> | <span data-ttu-id="c6e17-136">Píxel</span><span class="sxs-lookup"><span data-stu-id="c6e17-136">Pixel</span></span> | <span data-ttu-id="c6e17-137">Compute</span><span class="sxs-lookup"><span data-stu-id="c6e17-137">Compute</span></span> |
|        | <span data-ttu-id="c6e17-138">x</span><span class="sxs-lookup"><span data-stu-id="c6e17-138">x</span></span>    | <span data-ttu-id="c6e17-139">x</span><span class="sxs-lookup"><span data-stu-id="c6e17-139">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="c6e17-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6e17-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6e17-141">Semántica</span><span class="sxs-lookup"><span data-stu-id="c6e17-141">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="c6e17-142">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c6e17-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




