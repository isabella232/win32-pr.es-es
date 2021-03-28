---
title: 'RWTexture2DArray:: Getdimensions ((función)'
description: 'Devuelve las dimensiones del recurso. | RWTexture2DArray:: Getdimensions ((función)'
ms.assetid: 473b3f41-854d-4881-a80b-2d2dd7e5d479
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
ms.openlocfilehash: 6d95148cb6dc51c739ee4546bd64ce22666d5fd7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279924"
---
# <a name="rwtexture2darraygetdimensions-function"></a><span data-ttu-id="e48f5-105">RWTexture2DArray:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="e48f5-105">RWTexture2DArray::GetDimensions function</span></span>

<span data-ttu-id="e48f5-106">Devuelve las dimensiones del recurso.</span><span class="sxs-lookup"><span data-stu-id="e48f5-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="e48f5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e48f5-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Elements
);
```

## <a name="parameters"></a><span data-ttu-id="e48f5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e48f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e48f5-109">*Ancho* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e48f5-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e48f5-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e48f5-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e48f5-111">El ancho del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="e48f5-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="e48f5-112">*Alto* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e48f5-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e48f5-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e48f5-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e48f5-114">El alto del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="e48f5-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="e48f5-115">*Elementos* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e48f5-115">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e48f5-116">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e48f5-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e48f5-117">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="e48f5-117">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e48f5-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e48f5-118">Return value</span></span>

<span data-ttu-id="e48f5-119">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e48f5-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e48f5-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e48f5-120">Remarks</span></span>

<span data-ttu-id="e48f5-121">Esta es una lista de las versiones sobrecargadas de este método.</span><span class="sxs-lookup"><span data-stu-id="e48f5-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Elements);

void GetDimensions(out float Width,
  out float Height,
  out float Elements);
```



<span data-ttu-id="e48f5-122">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="e48f5-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e48f5-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="e48f5-123">Vertex</span></span> | <span data-ttu-id="e48f5-124">Casco</span><span class="sxs-lookup"><span data-stu-id="e48f5-124">Hull</span></span> | <span data-ttu-id="e48f5-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="e48f5-125">Domain</span></span> | <span data-ttu-id="e48f5-126">Geometría</span><span class="sxs-lookup"><span data-stu-id="e48f5-126">Geometry</span></span> | <span data-ttu-id="e48f5-127">Píxel</span><span class="sxs-lookup"><span data-stu-id="e48f5-127">Pixel</span></span> | <span data-ttu-id="e48f5-128">Compute</span><span class="sxs-lookup"><span data-stu-id="e48f5-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e48f5-129">x</span><span class="sxs-lookup"><span data-stu-id="e48f5-129">x</span></span>     | <span data-ttu-id="e48f5-130">x</span><span class="sxs-lookup"><span data-stu-id="e48f5-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e48f5-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e48f5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e48f5-132">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="e48f5-132">RWTexture2DArray</span></span>](sm5-object-rwtexture2darray.md)
</dt> <dt>

[<span data-ttu-id="e48f5-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e48f5-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
