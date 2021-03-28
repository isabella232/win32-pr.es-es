---
title: 'Texture2D:: Getdimensions ((función)'
description: 'Devuelve las dimensiones del recurso. | Texture2D:: Getdimensions ((función)'
ms.assetid: 921e425d-c0dd-4b8d-b590-0599fabfe606
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
ms.openlocfilehash: ba1fa832b51e86b5df3193895caa293bb006d82a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998181"
---
# <a name="texture2dgetdimensions-function"></a><span data-ttu-id="aabb8-105">Texture2D:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="aabb8-105">Texture2D::GetDimensions function</span></span>

<span data-ttu-id="aabb8-106">Devuelve las dimensiones del recurso.</span><span class="sxs-lookup"><span data-stu-id="aabb8-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="aabb8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aabb8-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  
            uint MipLevel,
  out 
            uint Width,
  out uint Height,
  out 
            uint NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="aabb8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aabb8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aabb8-109">*MipLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aabb8-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aabb8-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="aabb8-110">Type: **uint**</span></span>

<span data-ttu-id="aabb8-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="aabb8-111">Optional.</span></span> <span data-ttu-id="aabb8-112">Nivel de mipmap (debe especificarse si se usa *NumberOfLevels* ).</span><span class="sxs-lookup"><span data-stu-id="aabb8-112">The mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="aabb8-113">*Ancho* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aabb8-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aabb8-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="aabb8-114">Type: **uint**</span></span>

<span data-ttu-id="aabb8-115">El ancho del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="aabb8-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="aabb8-116">*Alto* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aabb8-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aabb8-117">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="aabb8-117">Type: **uint**</span></span>

<span data-ttu-id="aabb8-118">El alto del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="aabb8-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="aabb8-119">*NumberOfLevels* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aabb8-119">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aabb8-120">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="aabb8-120">Type: **uint**</span></span>

<span data-ttu-id="aabb8-121">El número de niveles de mipmap (requiere también *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="aabb8-121">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aabb8-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aabb8-122">Return value</span></span>

<span data-ttu-id="aabb8-123">Nada</span><span class="sxs-lookup"><span data-stu-id="aabb8-123">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="aabb8-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aabb8-124">Remarks</span></span>

<span data-ttu-id="aabb8-125">Esta es una lista de las versiones sobrecargadas de este método.</span><span class="sxs-lookup"><span data-stu-id="aabb8-125">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(uint MipLevel, 
  out uint Width,
  out uint Height,
  out uint NumberOfLevels);

void GetDimensions (out uint Width,
  out uint Height);

void GetDimensions(uint MipLevel,
  out float Width,
  out float Height,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height);
```



<span data-ttu-id="aabb8-126">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="aabb8-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="aabb8-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="aabb8-127">Vertex</span></span> | <span data-ttu-id="aabb8-128">Casco</span><span class="sxs-lookup"><span data-stu-id="aabb8-128">Hull</span></span> | <span data-ttu-id="aabb8-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="aabb8-129">Domain</span></span> | <span data-ttu-id="aabb8-130">Geometría</span><span class="sxs-lookup"><span data-stu-id="aabb8-130">Geometry</span></span> | <span data-ttu-id="aabb8-131">Píxel</span><span class="sxs-lookup"><span data-stu-id="aabb8-131">Pixel</span></span> | <span data-ttu-id="aabb8-132">Compute</span><span class="sxs-lookup"><span data-stu-id="aabb8-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="aabb8-133">x</span><span class="sxs-lookup"><span data-stu-id="aabb8-133">x</span></span>     | <span data-ttu-id="aabb8-134">x</span><span class="sxs-lookup"><span data-stu-id="aabb8-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="aabb8-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="aabb8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aabb8-136">Texture2D</span><span class="sxs-lookup"><span data-stu-id="aabb8-136">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="aabb8-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="aabb8-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




