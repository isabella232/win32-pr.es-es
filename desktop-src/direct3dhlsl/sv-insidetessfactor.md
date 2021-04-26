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
ms.openlocfilehash: 4d047f7961868de020ac50ffce22b6ce02d078a5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996922"
---
# <a name="sv_insidetessfactor"></a><span data-ttu-id="fe629-104">SV \_ InsideTessFactor</span><span class="sxs-lookup"><span data-stu-id="fe629-104">SV\_InsideTessFactor</span></span>

<span data-ttu-id="fe629-105">Define la cantidad de teselación dentro de una superficie de revisión.</span><span class="sxs-lookup"><span data-stu-id="fe629-105">Defines the tessellation amount within a patch surface.</span></span>

## <a name="type"></a><span data-ttu-id="fe629-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="fe629-106">Type</span></span>



|            |                |
|------------|----------------|
| <span data-ttu-id="fe629-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="fe629-107">Type</span></span>       | <span data-ttu-id="fe629-108">Topología de entrada</span><span class="sxs-lookup"><span data-stu-id="fe629-108">Input Topology</span></span> |
| <span data-ttu-id="fe629-109">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="fe629-109">float\[2\]</span></span> | <span data-ttu-id="fe629-110">revisión quad</span><span class="sxs-lookup"><span data-stu-id="fe629-110">quad patch</span></span>     |
| <span data-ttu-id="fe629-111">FLOAT</span><span class="sxs-lookup"><span data-stu-id="fe629-111">float</span></span>      | <span data-ttu-id="fe629-112">tri patch</span><span class="sxs-lookup"><span data-stu-id="fe629-112">tri patch</span></span>      |
| <span data-ttu-id="fe629-113">unused</span><span class="sxs-lookup"><span data-stu-id="fe629-113">unused</span></span>     | <span data-ttu-id="fe629-114">Isolínea</span><span class="sxs-lookup"><span data-stu-id="fe629-114">isoline</span></span>        |



 

<span data-ttu-id="fe629-115">Los factores de teselación deben declararse como matriz; no se pueden empaquetar en un solo vector.</span><span class="sxs-lookup"><span data-stu-id="fe629-115">Tessellation factors must be declared as array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe629-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fe629-116">Remarks</span></span>

<span data-ttu-id="fe629-117">Este valor debe definirse durante la función de constante de revisión del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="fe629-117">This value must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="fe629-118">Valor de salida necesario para el sombreador de casco si se usan revisiones quad o tri.</span><span class="sxs-lookup"><span data-stu-id="fe629-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="fe629-119">Este valor es una entrada necesaria para el sombreador de dominio con el fin de que el hardware coincida con las firmas a través del teselador.</span><span class="sxs-lookup"><span data-stu-id="fe629-119">This value is a required input for the domain shader in order for hardware to match the signatures through the tessellator.</span></span>

<span data-ttu-id="fe629-120">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="fe629-120">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="fe629-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="fe629-121">Vertex</span></span> | <span data-ttu-id="fe629-122">Casco</span><span class="sxs-lookup"><span data-stu-id="fe629-122">Hull</span></span> | <span data-ttu-id="fe629-123">Domain</span><span class="sxs-lookup"><span data-stu-id="fe629-123">Domain</span></span> | <span data-ttu-id="fe629-124">Geometría</span><span class="sxs-lookup"><span data-stu-id="fe629-124">Geometry</span></span> | <span data-ttu-id="fe629-125">Píxel</span><span class="sxs-lookup"><span data-stu-id="fe629-125">Pixel</span></span> | <span data-ttu-id="fe629-126">Proceso</span><span class="sxs-lookup"><span data-stu-id="fe629-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="fe629-127">x</span><span class="sxs-lookup"><span data-stu-id="fe629-127">x</span></span>    | <span data-ttu-id="fe629-128">x</span><span class="sxs-lookup"><span data-stu-id="fe629-128">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="fe629-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe629-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe629-130">Semántica</span><span class="sxs-lookup"><span data-stu-id="fe629-130">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="fe629-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="fe629-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




