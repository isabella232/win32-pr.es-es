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
ms.openlocfilehash: 90d31aa6a11ce8e2bdd75ff1171705cc9b3de437
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826619"
---
# <a name="sv_insidetessfactor"></a><span data-ttu-id="f8668-104">SV \_ InsideTessFactor</span><span class="sxs-lookup"><span data-stu-id="f8668-104">SV\_InsideTessFactor</span></span>

<span data-ttu-id="f8668-105">Define la cantidad de teselación dentro de una superficie de revisión.</span><span class="sxs-lookup"><span data-stu-id="f8668-105">Defines the tessellation amount within a patch surface.</span></span>

## <a name="type"></a><span data-ttu-id="f8668-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="f8668-106">Type</span></span>



|  <span data-ttu-id="f8668-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="f8668-107">Type</span></span>          | <span data-ttu-id="f8668-108">Topología de entrada</span><span class="sxs-lookup"><span data-stu-id="f8668-108">Input topology</span></span>               |
|------------|----------------|
| <span data-ttu-id="f8668-109">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="f8668-109">float\[2\]</span></span> | <span data-ttu-id="f8668-110">revisión quad</span><span class="sxs-lookup"><span data-stu-id="f8668-110">quad patch</span></span>     |
| <span data-ttu-id="f8668-111">FLOAT</span><span class="sxs-lookup"><span data-stu-id="f8668-111">float</span></span>      | <span data-ttu-id="f8668-112">revisión tri</span><span class="sxs-lookup"><span data-stu-id="f8668-112">tri patch</span></span>      |
| <span data-ttu-id="f8668-113">unused</span><span class="sxs-lookup"><span data-stu-id="f8668-113">unused</span></span>     | <span data-ttu-id="f8668-114">Isolínea</span><span class="sxs-lookup"><span data-stu-id="f8668-114">isoline</span></span>        |



 

<span data-ttu-id="f8668-115">Los factores de teselación deben declararse como matriz; no se pueden empaquetar en un solo vector.</span><span class="sxs-lookup"><span data-stu-id="f8668-115">Tessellation factors must be declared as array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8668-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f8668-116">Remarks</span></span>

<span data-ttu-id="f8668-117">Este valor debe definirse durante la función de constante de revisión del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="f8668-117">This value must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="f8668-118">Valor de salida requerido para el sombreador de casco si se usan revisiones quad o tri.</span><span class="sxs-lookup"><span data-stu-id="f8668-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="f8668-119">Este valor es una entrada necesaria para el sombreador de dominio con el fin de que el hardware coincida con las firmas a través del teselador.</span><span class="sxs-lookup"><span data-stu-id="f8668-119">This value is a required input for the domain shader in order for hardware to match the signatures through the tessellator.</span></span>

<span data-ttu-id="f8668-120">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="f8668-120">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="f8668-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="f8668-121">Vertex</span></span> | <span data-ttu-id="f8668-122">Casco</span><span class="sxs-lookup"><span data-stu-id="f8668-122">Hull</span></span> | <span data-ttu-id="f8668-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="f8668-123">Domain</span></span> | <span data-ttu-id="f8668-124">Geometría</span><span class="sxs-lookup"><span data-stu-id="f8668-124">Geometry</span></span> | <span data-ttu-id="f8668-125">Píxel</span><span class="sxs-lookup"><span data-stu-id="f8668-125">Pixel</span></span> | <span data-ttu-id="f8668-126">Compute</span><span class="sxs-lookup"><span data-stu-id="f8668-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="f8668-127">x</span><span class="sxs-lookup"><span data-stu-id="f8668-127">x</span></span>    | <span data-ttu-id="f8668-128">x</span><span class="sxs-lookup"><span data-stu-id="f8668-128">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="f8668-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8668-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8668-130">Semántica</span><span class="sxs-lookup"><span data-stu-id="f8668-130">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="f8668-131">Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="f8668-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




