---
title: 'ByteAddressBuffer:: Getdimensions ((función)'
description: 'Obtiene la longitud del búfer. | ByteAddressBuffer:: Getdimensions ((función)'
ms.assetid: 32099118-8d8a-440e-96ba-2580d905f068
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
ms.openlocfilehash: 1cbb705789e444a6fa54aeb87190912996f65621
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998013"
---
# <a name="byteaddressbuffergetdimensions-function"></a><span data-ttu-id="46863-105">ByteAddressBuffer:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="46863-105">ByteAddressBuffer::GetDimensions function</span></span>

<span data-ttu-id="46863-106">Obtiene la longitud del búfer.</span><span class="sxs-lookup"><span data-stu-id="46863-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="46863-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46863-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="46863-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46863-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46863-109">*atenuar* \[\]</span><span class="sxs-lookup"><span data-stu-id="46863-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46863-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="46863-110">Type: **uint**</span></span>

<span data-ttu-id="46863-111">La longitud, en bytes, del búfer.</span><span class="sxs-lookup"><span data-stu-id="46863-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46863-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46863-112">Return value</span></span>

<span data-ttu-id="46863-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="46863-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="46863-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46863-114">Remarks</span></span>

<span data-ttu-id="46863-115">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="46863-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="46863-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="46863-116">Vertex</span></span> | <span data-ttu-id="46863-117">Casco</span><span class="sxs-lookup"><span data-stu-id="46863-117">Hull</span></span> | <span data-ttu-id="46863-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="46863-118">Domain</span></span> | <span data-ttu-id="46863-119">Geometría</span><span class="sxs-lookup"><span data-stu-id="46863-119">Geometry</span></span> | <span data-ttu-id="46863-120">Píxel</span><span class="sxs-lookup"><span data-stu-id="46863-120">Pixel</span></span> | <span data-ttu-id="46863-121">Compute</span><span class="sxs-lookup"><span data-stu-id="46863-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="46863-122">x</span><span class="sxs-lookup"><span data-stu-id="46863-122">x</span></span>      | <span data-ttu-id="46863-123">x</span><span class="sxs-lookup"><span data-stu-id="46863-123">x</span></span>    | <span data-ttu-id="46863-124">x</span><span class="sxs-lookup"><span data-stu-id="46863-124">x</span></span>      | <span data-ttu-id="46863-125">x</span><span class="sxs-lookup"><span data-stu-id="46863-125">x</span></span>        | <span data-ttu-id="46863-126">x</span><span class="sxs-lookup"><span data-stu-id="46863-126">x</span></span>     | <span data-ttu-id="46863-127">x</span><span class="sxs-lookup"><span data-stu-id="46863-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="46863-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="46863-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46863-129">ByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="46863-129">ByteAddressBuffer</span></span>](sm5-object-byteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="46863-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="46863-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




