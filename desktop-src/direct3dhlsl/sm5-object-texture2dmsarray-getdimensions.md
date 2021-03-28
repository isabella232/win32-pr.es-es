---
title: 'Texture2DMSArray:: Getdimensions ((función)'
description: 'Devuelve las dimensiones del recurso. | Texture2DMSArray:: Getdimensions ((función)'
ms.assetid: 86d54e0d-f168-479f-b2af-f021b8994741
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
ms.openlocfilehash: e22a225178c2fa965ea842b8c86692d09b87168f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362343"
---
# <a name="texture2dmsarraygetdimensions-function"></a><span data-ttu-id="aa6e7-105">Texture2DMSArray:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="aa6e7-105">Texture2DMSArray::GetDimensions function</span></span>

<span data-ttu-id="aa6e7-106">Devuelve las dimensiones del recurso.</span><span class="sxs-lookup"><span data-stu-id="aa6e7-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa6e7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa6e7-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a><span data-ttu-id="aa6e7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa6e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa6e7-109">*Ancho* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aa6e7-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa6e7-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="aa6e7-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="aa6e7-111">El ancho del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="aa6e7-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="aa6e7-112">*Alto* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aa6e7-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa6e7-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="aa6e7-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="aa6e7-114">El alto del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="aa6e7-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="aa6e7-115">*Elementos* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aa6e7-115">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa6e7-116">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="aa6e7-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="aa6e7-117">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="aa6e7-117">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="aa6e7-118">*NumberOfSamples* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aa6e7-118">*NumberOfSamples* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa6e7-119">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="aa6e7-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="aa6e7-120">El número de ubicaciones de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="aa6e7-120">The number of sample locations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa6e7-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa6e7-121">Return value</span></span>

<span data-ttu-id="aa6e7-122">Nada</span><span class="sxs-lookup"><span data-stu-id="aa6e7-122">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="aa6e7-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa6e7-123">Remarks</span></span>

<span data-ttu-id="aa6e7-124">Esta es una lista de las versiones sobrecargadas de este método.</span><span class="sxs-lookup"><span data-stu-id="aa6e7-124">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(out float Width,
  out float Height,
  out float Elements,
  out float NumberOfSamples);
```



<span data-ttu-id="aa6e7-125">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="aa6e7-125">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="aa6e7-126">Vértice</span><span class="sxs-lookup"><span data-stu-id="aa6e7-126">Vertex</span></span> | <span data-ttu-id="aa6e7-127">Casco</span><span class="sxs-lookup"><span data-stu-id="aa6e7-127">Hull</span></span> | <span data-ttu-id="aa6e7-128">Dominio</span><span class="sxs-lookup"><span data-stu-id="aa6e7-128">Domain</span></span> | <span data-ttu-id="aa6e7-129">Geometría</span><span class="sxs-lookup"><span data-stu-id="aa6e7-129">Geometry</span></span> | <span data-ttu-id="aa6e7-130">Píxel</span><span class="sxs-lookup"><span data-stu-id="aa6e7-130">Pixel</span></span> | <span data-ttu-id="aa6e7-131">Compute</span><span class="sxs-lookup"><span data-stu-id="aa6e7-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="aa6e7-132">x</span><span class="sxs-lookup"><span data-stu-id="aa6e7-132">x</span></span>     | <span data-ttu-id="aa6e7-133">x</span><span class="sxs-lookup"><span data-stu-id="aa6e7-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="aa6e7-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa6e7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa6e7-135">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="aa6e7-135">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="aa6e7-136">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="aa6e7-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
