---
title: SV_DomainLocation
description: Define la ubicación en el casco del punto de dominio actual que se está evaluando.
ms.assetid: 907f568c-7c45-41e5-96c4-6e6b816a4a53
keywords:
- SV_DomainLocation HLSL
topic_type:
- apiref
api_name:
- SV_DomainLocation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c5195881df438c94cdaed7de8484d0df65e4d54
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419729"
---
# <a name="sv_domainlocation"></a><span data-ttu-id="f697b-104">VP \_ DomainLocation</span><span class="sxs-lookup"><span data-stu-id="f697b-104">SV\_DomainLocation</span></span>

<span data-ttu-id="f697b-105">Define la ubicación en el casco del punto de dominio actual que se está evaluando.</span><span class="sxs-lookup"><span data-stu-id="f697b-105">Defines the location on the hull of the current domain point being evaluated.</span></span>

## <a name="type"></a><span data-ttu-id="f697b-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="f697b-106">Type</span></span>



|        |                |
|--------|----------------|
| <span data-ttu-id="f697b-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="f697b-107">Type</span></span>   | <span data-ttu-id="f697b-108">Topología de entrada</span><span class="sxs-lookup"><span data-stu-id="f697b-108">Input Topology</span></span> |
| <span data-ttu-id="f697b-109">float2</span><span class="sxs-lookup"><span data-stu-id="f697b-109">float2</span></span> | <span data-ttu-id="f697b-110">revisión cuádruple</span><span class="sxs-lookup"><span data-stu-id="f697b-110">quad patch</span></span>     |
| <span data-ttu-id="f697b-111">float3</span><span class="sxs-lookup"><span data-stu-id="f697b-111">float3</span></span> | <span data-ttu-id="f697b-112">Tri patch</span><span class="sxs-lookup"><span data-stu-id="f697b-112">tri patch</span></span>      |
| <span data-ttu-id="f697b-113">float2</span><span class="sxs-lookup"><span data-stu-id="f697b-113">float2</span></span> | <span data-ttu-id="f697b-114">isolínea</span><span class="sxs-lookup"><span data-stu-id="f697b-114">isoline</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="f697b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f697b-115">Remarks</span></span>

<span data-ttu-id="f697b-116">Este valor del sistema es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f697b-116">This system value is required.</span></span>

<span data-ttu-id="f697b-117">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="f697b-117">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f697b-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="f697b-118">Vertex</span></span> | <span data-ttu-id="f697b-119">Casco</span><span class="sxs-lookup"><span data-stu-id="f697b-119">Hull</span></span> | <span data-ttu-id="f697b-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="f697b-120">Domain</span></span> | <span data-ttu-id="f697b-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="f697b-121">Geometry</span></span> | <span data-ttu-id="f697b-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="f697b-122">Pixel</span></span> | <span data-ttu-id="f697b-123">Compute</span><span class="sxs-lookup"><span data-stu-id="f697b-123">Compute</span></span> |
|        |      | <span data-ttu-id="f697b-124">x</span><span class="sxs-lookup"><span data-stu-id="f697b-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="f697b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f697b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f697b-126">Semántica</span><span class="sxs-lookup"><span data-stu-id="f697b-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="f697b-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f697b-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




