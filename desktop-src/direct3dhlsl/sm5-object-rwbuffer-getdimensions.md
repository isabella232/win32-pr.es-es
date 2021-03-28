---
title: 'RWBuffer:: Getdimensions ((función)'
description: 'Obtiene la longitud del búfer. | RWBuffer:: Getdimensions ((función)'
ms.assetid: 600147cb-9513-4b74-a873-1ed22b31cdf7
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
ms.openlocfilehash: 98e419d3e77a27f211f0e063573caffcd6c61ce8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998209"
---
# <a name="rwbuffergetdimensions-function"></a><span data-ttu-id="d9a4c-105">RWBuffer:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="d9a4c-105">RWBuffer::GetDimensions function</span></span>

<span data-ttu-id="d9a4c-106">Obtiene la longitud del búfer.</span><span class="sxs-lookup"><span data-stu-id="d9a4c-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9a4c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9a4c-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="d9a4c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9a4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9a4c-109">*atenuar* \[\]</span><span class="sxs-lookup"><span data-stu-id="d9a4c-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9a4c-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d9a4c-110">Type: **uint**</span></span>

<span data-ttu-id="d9a4c-111">La longitud, en bytes, del búfer.</span><span class="sxs-lookup"><span data-stu-id="d9a4c-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9a4c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9a4c-112">Return value</span></span>

<span data-ttu-id="d9a4c-113">Nada</span><span class="sxs-lookup"><span data-stu-id="d9a4c-113">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="d9a4c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9a4c-114">Remarks</span></span>

<span data-ttu-id="d9a4c-115">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="d9a4c-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d9a4c-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="d9a4c-116">Vertex</span></span> | <span data-ttu-id="d9a4c-117">Casco</span><span class="sxs-lookup"><span data-stu-id="d9a4c-117">Hull</span></span> | <span data-ttu-id="d9a4c-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="d9a4c-118">Domain</span></span> | <span data-ttu-id="d9a4c-119">Geometría</span><span class="sxs-lookup"><span data-stu-id="d9a4c-119">Geometry</span></span> | <span data-ttu-id="d9a4c-120">Píxel</span><span class="sxs-lookup"><span data-stu-id="d9a4c-120">Pixel</span></span> | <span data-ttu-id="d9a4c-121">Compute</span><span class="sxs-lookup"><span data-stu-id="d9a4c-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d9a4c-122">x</span><span class="sxs-lookup"><span data-stu-id="d9a4c-122">x</span></span>     | <span data-ttu-id="d9a4c-123">x</span><span class="sxs-lookup"><span data-stu-id="d9a4c-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d9a4c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9a4c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9a4c-125">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="d9a4c-125">RWBuffer</span></span>](sm5-object-rwbuffer.md)
</dt> <dt>

[<span data-ttu-id="d9a4c-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d9a4c-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




