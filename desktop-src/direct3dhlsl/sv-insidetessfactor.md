---
title: SV_InsideTessFactor
description: Define la cantidad de teselación dentro de una superficie de revisión.
ms.assetid: f0762aca-d84d-44c0-a163-9737ef92c1e5
keywords:
- SV_InsideTessFactor HLSL
topic_type:
- apiref
api_name:
- SV_InsideTessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a05cabbb9410136d2bd82ee272ad92ff1b1f430
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104983766"
---
# <a name="sv_insidetessfactor"></a><span data-ttu-id="b6a90-104">VP \_ InsideTessFactor</span><span class="sxs-lookup"><span data-stu-id="b6a90-104">SV\_InsideTessFactor</span></span>

<span data-ttu-id="b6a90-105">Define la cantidad de teselación dentro de una superficie de revisión.</span><span class="sxs-lookup"><span data-stu-id="b6a90-105">Defines the tessellation amount within a patch surface.</span></span>

## <a name="type"></a><span data-ttu-id="b6a90-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6a90-106">Type</span></span>



|            |                |
|------------|----------------|
| <span data-ttu-id="b6a90-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6a90-107">Type</span></span>       | <span data-ttu-id="b6a90-108">Topología de entrada</span><span class="sxs-lookup"><span data-stu-id="b6a90-108">Input Topology</span></span> |
| <span data-ttu-id="b6a90-109">Float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="b6a90-109">float\[2\]</span></span> | <span data-ttu-id="b6a90-110">revisión cuádruple</span><span class="sxs-lookup"><span data-stu-id="b6a90-110">quad patch</span></span>     |
| <span data-ttu-id="b6a90-111">FLOAT</span><span class="sxs-lookup"><span data-stu-id="b6a90-111">float</span></span>      | <span data-ttu-id="b6a90-112">Tri patch</span><span class="sxs-lookup"><span data-stu-id="b6a90-112">tri patch</span></span>      |
| <span data-ttu-id="b6a90-113">unused</span><span class="sxs-lookup"><span data-stu-id="b6a90-113">unused</span></span>     | <span data-ttu-id="b6a90-114">isolínea</span><span class="sxs-lookup"><span data-stu-id="b6a90-114">isoline</span></span>        |



 

<span data-ttu-id="b6a90-115">Los factores de teselación se deben declarar como una matriz; no se pueden empaquetar en un único vector.</span><span class="sxs-lookup"><span data-stu-id="b6a90-115">Tessellation factors must be declared as array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6a90-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6a90-116">Remarks</span></span>

<span data-ttu-id="b6a90-117">Este valor debe definirse durante la función constante patch del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="b6a90-117">This value must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="b6a90-118">Valor de salida necesario para el sombreador de casco si se usan cuatro o tres revisiones.</span><span class="sxs-lookup"><span data-stu-id="b6a90-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="b6a90-119">Este valor es una entrada necesaria para el sombreador de dominios con el fin de que el hardware coincida con las firmas a través de del teselador.</span><span class="sxs-lookup"><span data-stu-id="b6a90-119">This value is a required input for the domain shader in order for hardware to match the signatures through the tessellator.</span></span>

<span data-ttu-id="b6a90-120">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="b6a90-120">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b6a90-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="b6a90-121">Vertex</span></span> | <span data-ttu-id="b6a90-122">Casco</span><span class="sxs-lookup"><span data-stu-id="b6a90-122">Hull</span></span> | <span data-ttu-id="b6a90-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="b6a90-123">Domain</span></span> | <span data-ttu-id="b6a90-124">Geometría</span><span class="sxs-lookup"><span data-stu-id="b6a90-124">Geometry</span></span> | <span data-ttu-id="b6a90-125">Píxel</span><span class="sxs-lookup"><span data-stu-id="b6a90-125">Pixel</span></span> | <span data-ttu-id="b6a90-126">Compute</span><span class="sxs-lookup"><span data-stu-id="b6a90-126">Compute</span></span> |
|        | <span data-ttu-id="b6a90-127">x</span><span class="sxs-lookup"><span data-stu-id="b6a90-127">x</span></span>    | <span data-ttu-id="b6a90-128">x</span><span class="sxs-lookup"><span data-stu-id="b6a90-128">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="b6a90-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6a90-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6a90-130">Semántica</span><span class="sxs-lookup"><span data-stu-id="b6a90-130">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="b6a90-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b6a90-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




