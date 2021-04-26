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
ms.openlocfilehash: cb9265734663881981f1626db6e23c6b7dd9415a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996512"
---
# <a name="sv_domainlocation"></a><span data-ttu-id="91291-104">SV \_ DomainLocation</span><span class="sxs-lookup"><span data-stu-id="91291-104">SV\_DomainLocation</span></span>

<span data-ttu-id="91291-105">Define la ubicación en el casco del punto de dominio actual que se está evaluando.</span><span class="sxs-lookup"><span data-stu-id="91291-105">Defines the location on the hull of the current domain point being evaluated.</span></span>

## <a name="type"></a><span data-ttu-id="91291-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="91291-106">Type</span></span>



|        |                |
|--------|----------------|
| <span data-ttu-id="91291-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="91291-107">Type</span></span>   | <span data-ttu-id="91291-108">Topología de entrada</span><span class="sxs-lookup"><span data-stu-id="91291-108">Input Topology</span></span> |
| <span data-ttu-id="91291-109">float2</span><span class="sxs-lookup"><span data-stu-id="91291-109">float2</span></span> | <span data-ttu-id="91291-110">revisión quad</span><span class="sxs-lookup"><span data-stu-id="91291-110">quad patch</span></span>     |
| <span data-ttu-id="91291-111">float3</span><span class="sxs-lookup"><span data-stu-id="91291-111">float3</span></span> | <span data-ttu-id="91291-112">revisión tri</span><span class="sxs-lookup"><span data-stu-id="91291-112">tri patch</span></span>      |
| <span data-ttu-id="91291-113">float2</span><span class="sxs-lookup"><span data-stu-id="91291-113">float2</span></span> | <span data-ttu-id="91291-114">Isolínea</span><span class="sxs-lookup"><span data-stu-id="91291-114">isoline</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="91291-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="91291-115">Remarks</span></span>

<span data-ttu-id="91291-116">Este valor del sistema es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="91291-116">This system value is required.</span></span>

<span data-ttu-id="91291-117">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="91291-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="91291-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="91291-118">Vertex</span></span> | <span data-ttu-id="91291-119">Casco</span><span class="sxs-lookup"><span data-stu-id="91291-119">Hull</span></span> | <span data-ttu-id="91291-120">Domain</span><span class="sxs-lookup"><span data-stu-id="91291-120">Domain</span></span> | <span data-ttu-id="91291-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="91291-121">Geometry</span></span> | <span data-ttu-id="91291-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="91291-122">Pixel</span></span> | <span data-ttu-id="91291-123">Proceso</span><span class="sxs-lookup"><span data-stu-id="91291-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      | <span data-ttu-id="91291-124">x</span><span class="sxs-lookup"><span data-stu-id="91291-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="91291-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="91291-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91291-126">Semántica</span><span class="sxs-lookup"><span data-stu-id="91291-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="91291-127">Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="91291-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




