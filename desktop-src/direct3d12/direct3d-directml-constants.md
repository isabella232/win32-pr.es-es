---
title: Constantes de DirectML
description: Las constantes siguientes se declaran en `DirectML.h` .
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
ms.openlocfilehash: d6c3791812f3ac1191f1959150bd5ac7059c54fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670215"
---
# <a name="directml-constants"></a><span data-ttu-id="62c1a-104">Constantes de DirectML</span><span class="sxs-lookup"><span data-stu-id="62c1a-104">DirectML constants</span></span>

<span data-ttu-id="62c1a-105">Las constantes siguientes se declaran en `DirectML.h` .</span><span class="sxs-lookup"><span data-stu-id="62c1a-105">The following constants are declared in `DirectML.h`.</span></span>

| <span data-ttu-id="62c1a-106">Constante</span><span class="sxs-lookup"><span data-stu-id="62c1a-106">Constant</span></span> | <span data-ttu-id="62c1a-107">Value</span><span class="sxs-lookup"><span data-stu-id="62c1a-107">Value</span></span> | <span data-ttu-id="62c1a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="62c1a-108">Description</span></span> |
|-|-|-|
| <span data-ttu-id="62c1a-109">DML_TENSOR_DIMENSION_COUNT_MAX</span><span class="sxs-lookup"><span data-stu-id="62c1a-109">DML_TENSOR_DIMENSION_COUNT_MAX</span></span> | <span data-ttu-id="62c1a-110">5</span><span class="sxs-lookup"><span data-stu-id="62c1a-110">5</span></span> | <span data-ttu-id="62c1a-111">Los DirectML de tamaño máximo admiten un máximo de 5 dimensiones para el DML_FEATURE_LEVEL_3_0 de < de DML_TARGET_VERSION.</span><span class="sxs-lookup"><span data-stu-id="62c1a-111">DirectML tensors support a maximum of 5 dimensions for DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="62c1a-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span><span class="sxs-lookup"><span data-stu-id="62c1a-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span></span> | <span data-ttu-id="62c1a-113">8</span><span class="sxs-lookup"><span data-stu-id="62c1a-113">8</span></span> | <span data-ttu-id="62c1a-114">Los DirectMLs de tamaño máximo admiten un máximo de 8 dimensiones para DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="62c1a-114">DirectML tensors support a maximum of 8 dimensions for DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="62c1a-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="62c1a-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="62c1a-116">256</span><span class="sxs-lookup"><span data-stu-id="62c1a-116">256</span></span> | <span data-ttu-id="62c1a-117">Los búferes temporales y persistentes deben tener una dirección base que se alinee con 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="62c1a-117">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="62c1a-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="62c1a-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="62c1a-119">256</span><span class="sxs-lookup"><span data-stu-id="62c1a-119">256</span></span> | <span data-ttu-id="62c1a-120">Los búferes temporales y persistentes deben tener una dirección base que se alinee con 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="62c1a-120">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="62c1a-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="62c1a-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span></span> | <span data-ttu-id="62c1a-122">16</span><span class="sxs-lookup"><span data-stu-id="62c1a-122">16</span></span> | <span data-ttu-id="62c1a-123">Los separadores de búfer tienen un requisito de alineación de dirección base mínimo de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="62c1a-123">Buffer tensors have a minimum base address alignment requirement of 16 bytes.</span></span> |

## <a name="requirements"></a><span data-ttu-id="62c1a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62c1a-124">Requirements</span></span>

| <span data-ttu-id="62c1a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="62c1a-125">Requirement</span></span> | <span data-ttu-id="62c1a-126">Value</span><span class="sxs-lookup"><span data-stu-id="62c1a-126">Value</span></span> |
|-|-|
| <span data-ttu-id="62c1a-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62c1a-127">Header</span></span> | <span data-ttu-id="62c1a-128">D3D12. h</span><span class="sxs-lookup"><span data-stu-id="62c1a-128">D3D12.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="62c1a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="62c1a-129">See also</span></span>

* [<span data-ttu-id="62c1a-130">Referencia de DirectML</span><span class="sxs-lookup"><span data-stu-id="62c1a-130">DirectML reference</span></span>](direct3d-directml-reference.md)
* [<span data-ttu-id="62c1a-131">Referencia principal</span><span class="sxs-lookup"><span data-stu-id="62c1a-131">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="62c1a-132">Referencia de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="62c1a-132">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
