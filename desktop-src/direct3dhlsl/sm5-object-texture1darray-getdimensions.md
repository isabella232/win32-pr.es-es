---
title: 'Texture1DArray:: Getdimensions ((función)'
description: 'Devuelve las dimensiones del recurso. | Texture1DArray:: Getdimensions ((función)'
ms.assetid: a15f1808-296d-43ac-80c0-5cbec0bcb801
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
ms.openlocfilehash: 46cc7e93fc01e14ff34091da4549308730d7cd7c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820706"
---
# <a name="texture1darraygetdimensions-function"></a><span data-ttu-id="9fafa-105">Texture1DArray:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="9fafa-105">Texture1DArray::GetDimensions function</span></span>

<span data-ttu-id="9fafa-106">Devuelve las dimensiones del recurso.</span><span class="sxs-lookup"><span data-stu-id="9fafa-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fafa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fafa-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Elements,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="9fafa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9fafa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fafa-109">*MipLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9fafa-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fafa-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9fafa-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9fafa-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9fafa-111">Optional.</span></span> <span data-ttu-id="9fafa-112">Nivel de mipmap (debe especificarse si se usa *NumberOfLevels* ).</span><span class="sxs-lookup"><span data-stu-id="9fafa-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="9fafa-113">*Ancho* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9fafa-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fafa-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9fafa-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9fafa-115">El ancho del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="9fafa-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="9fafa-116">*Elementos* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9fafa-116">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fafa-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9fafa-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9fafa-118">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="9fafa-118">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="9fafa-119">*NumberOfLevels* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9fafa-119">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fafa-120">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9fafa-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9fafa-121">El número de niveles de mipmap (requiere también *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="9fafa-121">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fafa-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9fafa-122">Return value</span></span>

<span data-ttu-id="9fafa-123">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9fafa-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fafa-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fafa-124">Remarks</span></span>

<span data-ttu-id="9fafa-125">Esta es una lista de las versiones sobrecargadas de este método.</span><span class="sxs-lookup"><span data-stu-id="9fafa-125">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Elements,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Elements);

void GetDimensions(UINT MipLevel,
  out float Width,
  out UINT Elements,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out UINT Elements);
```



<span data-ttu-id="9fafa-126">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="9fafa-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9fafa-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="9fafa-127">Vertex</span></span> | <span data-ttu-id="9fafa-128">Casco</span><span class="sxs-lookup"><span data-stu-id="9fafa-128">Hull</span></span> | <span data-ttu-id="9fafa-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="9fafa-129">Domain</span></span> | <span data-ttu-id="9fafa-130">Geometría</span><span class="sxs-lookup"><span data-stu-id="9fafa-130">Geometry</span></span> | <span data-ttu-id="9fafa-131">Píxel</span><span class="sxs-lookup"><span data-stu-id="9fafa-131">Pixel</span></span> | <span data-ttu-id="9fafa-132">Compute</span><span class="sxs-lookup"><span data-stu-id="9fafa-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="9fafa-133">x</span><span class="sxs-lookup"><span data-stu-id="9fafa-133">x</span></span>     | <span data-ttu-id="9fafa-134">x</span><span class="sxs-lookup"><span data-stu-id="9fafa-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9fafa-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fafa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fafa-136">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="9fafa-136">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="9fafa-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="9fafa-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
