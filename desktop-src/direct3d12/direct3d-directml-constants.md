---
title: Constantes de DirectML
description: Las siguientes constantes se declaran en `DirectML.h` .
keywords:
- Constantes
topic_type:
- apiref
api_name:
- DirectML constants
api_location:
- DirectML.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: ad4ff8c409f79a03cb4021974fe374498926c3e2
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803406"
---
# <a name="directml-constants"></a><span data-ttu-id="18de1-104">Constantes de DirectML</span><span class="sxs-lookup"><span data-stu-id="18de1-104">DirectML constants</span></span>

<span data-ttu-id="18de1-105">Las siguientes constantes se declaran en `DirectML.h` .</span><span class="sxs-lookup"><span data-stu-id="18de1-105">The following constants are declared in `DirectML.h`.</span></span>

| <span data-ttu-id="18de1-106">Constante</span><span class="sxs-lookup"><span data-stu-id="18de1-106">Constant</span></span> | <span data-ttu-id="18de1-107">Value</span><span class="sxs-lookup"><span data-stu-id="18de1-107">Value</span></span> | <span data-ttu-id="18de1-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="18de1-108">Description</span></span> |
|-|-|-|
| <span data-ttu-id="18de1-109">DML_TENSOR_DIMENSION_COUNT_MAX</span><span class="sxs-lookup"><span data-stu-id="18de1-109">DML_TENSOR_DIMENSION_COUNT_MAX</span></span> | <span data-ttu-id="18de1-110">5</span><span class="sxs-lookup"><span data-stu-id="18de1-110">5</span></span> | <span data-ttu-id="18de1-111">Los tensores de DirectML admiten un máximo de 5 dimensiones para DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="18de1-111">DirectML tensors support a maximum of 5 dimensions for DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="18de1-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span><span class="sxs-lookup"><span data-stu-id="18de1-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span></span> | <span data-ttu-id="18de1-113">8</span><span class="sxs-lookup"><span data-stu-id="18de1-113">8</span></span> | <span data-ttu-id="18de1-114">Los tensores de DirectML admiten un máximo de 8 dimensiones para DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="18de1-114">DirectML tensors support a maximum of 8 dimensions for DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="18de1-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="18de1-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="18de1-116">256</span><span class="sxs-lookup"><span data-stu-id="18de1-116">256</span></span> | <span data-ttu-id="18de1-117">Los búferes temporales y persistentes deben tener una dirección base alineada con 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="18de1-117">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="18de1-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="18de1-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="18de1-119">256</span><span class="sxs-lookup"><span data-stu-id="18de1-119">256</span></span> | <span data-ttu-id="18de1-120">Los búferes temporales y persistentes deben tener una dirección base alineada con 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="18de1-120">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="18de1-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="18de1-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span></span> | <span data-ttu-id="18de1-122">16</span><span class="sxs-lookup"><span data-stu-id="18de1-122">16</span></span> | <span data-ttu-id="18de1-123">Los tensores de búfer tienen un requisito mínimo de alineación de direcciones base de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="18de1-123">Buffer tensors have a minimum base address alignment requirement of 16 bytes.</span></span> |

## <a name="requirements"></a><span data-ttu-id="18de1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18de1-124">Requirements</span></span>

| <span data-ttu-id="18de1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="18de1-125">Requirement</span></span> | <span data-ttu-id="18de1-126">Value</span><span class="sxs-lookup"><span data-stu-id="18de1-126">Value</span></span> |
|-|-|
| <span data-ttu-id="18de1-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18de1-127">Header</span></span> | <span data-ttu-id="18de1-128">DirectML.h</span><span class="sxs-lookup"><span data-stu-id="18de1-128">DirectML.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="18de1-129">Consulta también</span><span class="sxs-lookup"><span data-stu-id="18de1-129">See also</span></span>

* [<span data-ttu-id="18de1-130">Referencia de DirectML</span><span class="sxs-lookup"><span data-stu-id="18de1-130">DirectML reference</span></span>](direct3d-directml-reference.md)
* [<span data-ttu-id="18de1-131">Referencia principal</span><span class="sxs-lookup"><span data-stu-id="18de1-131">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="18de1-132">Referencia de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="18de1-132">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
