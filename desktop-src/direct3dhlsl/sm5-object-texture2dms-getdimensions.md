---
title: 'Texture2DMS:: Getdimensions ((función)'
description: 'Devuelve las dimensiones del recurso. | Texture2DMS:: Getdimensions ((función)'
ms.assetid: badf4127-2498-4c2e-acc7-20507488fc6b
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
ms.openlocfilehash: f720a10ac73f48ce1f27c5676d706a75178aa8ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003597"
---
# <a name="texture2dmsgetdimensions-function"></a><span data-ttu-id="c9f60-105">Texture2DMS:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="c9f60-105">Texture2DMS::GetDimensions function</span></span>

<span data-ttu-id="c9f60-106">Devuelve las dimensiones del recurso.</span><span class="sxs-lookup"><span data-stu-id="c9f60-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9f60-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9f60-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a><span data-ttu-id="c9f60-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9f60-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9f60-109">*Ancho* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c9f60-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9f60-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c9f60-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c9f60-111">El ancho del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="c9f60-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="c9f60-112">*Alto* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c9f60-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9f60-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c9f60-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c9f60-114">El alto del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="c9f60-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="c9f60-115">*NumberOfSamples* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c9f60-115">*NumberOfSamples* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9f60-116">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c9f60-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c9f60-117">El número de ubicaciones de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c9f60-117">The number of sample locations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9f60-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9f60-118">Return value</span></span>

<span data-ttu-id="c9f60-119">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c9f60-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9f60-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9f60-120">Remarks</span></span>

<span data-ttu-id="c9f60-121">Esta es una lista de las versiones sobrecargadas de este método.</span><span class="sxs-lookup"><span data-stu-id="c9f60-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(out float Width,
  out float Height,
  out float NumberOfSamples);
```



<span data-ttu-id="c9f60-122">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="c9f60-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c9f60-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="c9f60-123">Vertex</span></span> | <span data-ttu-id="c9f60-124">Casco</span><span class="sxs-lookup"><span data-stu-id="c9f60-124">Hull</span></span> | <span data-ttu-id="c9f60-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="c9f60-125">Domain</span></span> | <span data-ttu-id="c9f60-126">Geometría</span><span class="sxs-lookup"><span data-stu-id="c9f60-126">Geometry</span></span> | <span data-ttu-id="c9f60-127">Píxel</span><span class="sxs-lookup"><span data-stu-id="c9f60-127">Pixel</span></span> | <span data-ttu-id="c9f60-128">Compute</span><span class="sxs-lookup"><span data-stu-id="c9f60-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c9f60-129">x</span><span class="sxs-lookup"><span data-stu-id="c9f60-129">x</span></span>     | <span data-ttu-id="c9f60-130">x</span><span class="sxs-lookup"><span data-stu-id="c9f60-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c9f60-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9f60-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9f60-132">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="c9f60-132">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="c9f60-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c9f60-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
