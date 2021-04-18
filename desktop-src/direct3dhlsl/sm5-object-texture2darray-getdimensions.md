---
title: 'Texture2DArray:: Getdimensions ((función)'
description: 'Devuelve las dimensiones del recurso. | Texture2DArray:: Getdimensions ((función)'
ms.assetid: 0f6d88b3-195d-4f8c-ac31-ac90129a233e
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
ms.openlocfilehash: b3a78bd12f6924c85d4d395c3cdf73443ae51478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986195"
---
# <a name="texture2darraygetdimensions-function"></a><span data-ttu-id="c8eee-105">Texture2DArray:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="c8eee-105">Texture2DArray::GetDimensions function</span></span>

<span data-ttu-id="c8eee-106">Devuelve las dimensiones del recurso.</span><span class="sxs-lookup"><span data-stu-id="c8eee-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8eee-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8eee-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="c8eee-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8eee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8eee-109">*MipLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8eee-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8eee-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c8eee-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c8eee-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c8eee-111">Optional.</span></span> <span data-ttu-id="c8eee-112">Nivel de mipmap (debe especificarse si se usa *NumberOfLevels* ).</span><span class="sxs-lookup"><span data-stu-id="c8eee-112">The mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="c8eee-113">*Ancho* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c8eee-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8eee-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c8eee-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c8eee-115">El ancho del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="c8eee-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="c8eee-116">*Alto* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c8eee-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8eee-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c8eee-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c8eee-118">El alto del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="c8eee-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="c8eee-119">*Elementos* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c8eee-119">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8eee-120">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c8eee-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c8eee-121">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="c8eee-121">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="c8eee-122">*NumberOfLevels* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c8eee-122">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8eee-123">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c8eee-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c8eee-124">El número de niveles de mipmap (requiere también *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="c8eee-124">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8eee-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8eee-125">Return value</span></span>

<span data-ttu-id="c8eee-126">Nada</span><span class="sxs-lookup"><span data-stu-id="c8eee-126">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="c8eee-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8eee-127">Remarks</span></span>

<span data-ttu-id="c8eee-128">Esta es una lista de las versiones sobrecargadas de este método.</span><span class="sxs-lookup"><span data-stu-id="c8eee-128">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out float Height,
  out float Elements);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Elements,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Elements);
```



<span data-ttu-id="c8eee-129">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="c8eee-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c8eee-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="c8eee-130">Vertex</span></span> | <span data-ttu-id="c8eee-131">Casco</span><span class="sxs-lookup"><span data-stu-id="c8eee-131">Hull</span></span> | <span data-ttu-id="c8eee-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="c8eee-132">Domain</span></span> | <span data-ttu-id="c8eee-133">Geometría</span><span class="sxs-lookup"><span data-stu-id="c8eee-133">Geometry</span></span> | <span data-ttu-id="c8eee-134">Píxel</span><span class="sxs-lookup"><span data-stu-id="c8eee-134">Pixel</span></span> | <span data-ttu-id="c8eee-135">Compute</span><span class="sxs-lookup"><span data-stu-id="c8eee-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c8eee-136">x</span><span class="sxs-lookup"><span data-stu-id="c8eee-136">x</span></span>     | <span data-ttu-id="c8eee-137">x</span><span class="sxs-lookup"><span data-stu-id="c8eee-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c8eee-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8eee-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8eee-139">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c8eee-139">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="c8eee-140">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c8eee-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
