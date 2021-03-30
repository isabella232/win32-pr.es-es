---
title: 'Buffer:: Getdimensions ((función)'
description: 'Obtiene la longitud del búfer. | Buffer:: Getdimensions ((función)'
ms.assetid: 704890e8-43e4-4e72-b7e2-eeef331bef1c
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
ms.openlocfilehash: c7f1ad1da7600e65d7442c1b2431535e2fdcf38c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986206"
---
# <a name="buffergetdimensions-function"></a><span data-ttu-id="efc47-105">Buffer:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="efc47-105">Buffer::GetDimensions function</span></span>

<span data-ttu-id="efc47-106">Obtiene la longitud del búfer.</span><span class="sxs-lookup"><span data-stu-id="efc47-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="efc47-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="efc47-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="efc47-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="efc47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efc47-109">*atenuar* \[\]</span><span class="sxs-lookup"><span data-stu-id="efc47-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efc47-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="efc47-110">Type: **uint**</span></span>

<span data-ttu-id="efc47-111">La longitud, en bytes, del búfer.</span><span class="sxs-lookup"><span data-stu-id="efc47-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efc47-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="efc47-112">Return value</span></span>

<span data-ttu-id="efc47-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="efc47-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="efc47-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="efc47-114">Remarks</span></span>

<span data-ttu-id="efc47-115">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="efc47-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="efc47-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="efc47-116">Vertex</span></span> | <span data-ttu-id="efc47-117">Casco</span><span class="sxs-lookup"><span data-stu-id="efc47-117">Hull</span></span> | <span data-ttu-id="efc47-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="efc47-118">Domain</span></span> | <span data-ttu-id="efc47-119">Geometría</span><span class="sxs-lookup"><span data-stu-id="efc47-119">Geometry</span></span> | <span data-ttu-id="efc47-120">Píxel</span><span class="sxs-lookup"><span data-stu-id="efc47-120">Pixel</span></span> | <span data-ttu-id="efc47-121">Compute</span><span class="sxs-lookup"><span data-stu-id="efc47-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="efc47-122">x</span><span class="sxs-lookup"><span data-stu-id="efc47-122">x</span></span>      | <span data-ttu-id="efc47-123">x</span><span class="sxs-lookup"><span data-stu-id="efc47-123">x</span></span>    | <span data-ttu-id="efc47-124">x</span><span class="sxs-lookup"><span data-stu-id="efc47-124">x</span></span>      | <span data-ttu-id="efc47-125">x</span><span class="sxs-lookup"><span data-stu-id="efc47-125">x</span></span>        | <span data-ttu-id="efc47-126">x</span><span class="sxs-lookup"><span data-stu-id="efc47-126">x</span></span>     | <span data-ttu-id="efc47-127">x</span><span class="sxs-lookup"><span data-stu-id="efc47-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="efc47-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="efc47-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efc47-129">Buffer</span><span class="sxs-lookup"><span data-stu-id="efc47-129">Buffer</span></span>](sm5-object-buffer.md)
</dt> <dt>

[<span data-ttu-id="efc47-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="efc47-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




