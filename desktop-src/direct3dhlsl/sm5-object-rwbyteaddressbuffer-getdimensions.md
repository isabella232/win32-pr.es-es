---
title: 'RWByteAddressBuffer:: Getdimensions ((función)'
description: 'Obtiene la longitud del búfer. | RWByteAddressBuffer:: Getdimensions ((función)'
ms.assetid: 7d78aa0d-75b8-43d5-85d9-0a6fb04ae64f
keywords:
- Getdimensions (de función HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d22b6f655802d77a92611fe8699a405aa323873
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362315"
---
# <a name="rwbyteaddressbuffergetdimensions-function"></a><span data-ttu-id="6bfd7-105">RWByteAddressBuffer:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="6bfd7-105">RWByteAddressBuffer::GetDimensions function</span></span>

<span data-ttu-id="6bfd7-106">Obtiene la longitud del búfer.</span><span class="sxs-lookup"><span data-stu-id="6bfd7-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bfd7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6bfd7-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="6bfd7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6bfd7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bfd7-109">*atenuar* \[\]</span><span class="sxs-lookup"><span data-stu-id="6bfd7-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6bfd7-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="6bfd7-110">Type: **uint**</span></span>

<span data-ttu-id="6bfd7-111">La longitud, en bytes, del búfer.</span><span class="sxs-lookup"><span data-stu-id="6bfd7-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bfd7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6bfd7-112">Return value</span></span>

<span data-ttu-id="6bfd7-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6bfd7-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bfd7-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6bfd7-114">Remarks</span></span>

<span data-ttu-id="6bfd7-115">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="6bfd7-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6bfd7-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="6bfd7-116">Vertex</span></span> | <span data-ttu-id="6bfd7-117">Casco</span><span class="sxs-lookup"><span data-stu-id="6bfd7-117">Hull</span></span> | <span data-ttu-id="6bfd7-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="6bfd7-118">Domain</span></span> | <span data-ttu-id="6bfd7-119">Geometría</span><span class="sxs-lookup"><span data-stu-id="6bfd7-119">Geometry</span></span> | <span data-ttu-id="6bfd7-120">Píxel</span><span class="sxs-lookup"><span data-stu-id="6bfd7-120">Pixel</span></span> | <span data-ttu-id="6bfd7-121">Compute</span><span class="sxs-lookup"><span data-stu-id="6bfd7-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6bfd7-122">x</span><span class="sxs-lookup"><span data-stu-id="6bfd7-122">x</span></span>     | <span data-ttu-id="6bfd7-123">x</span><span class="sxs-lookup"><span data-stu-id="6bfd7-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6bfd7-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="6bfd7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bfd7-125">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="6bfd7-125">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="6bfd7-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6bfd7-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




