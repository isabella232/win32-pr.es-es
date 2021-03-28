---
title: 'Texture3D:: Getdimensions ((función)'
description: 'Devuelve las dimensiones del recurso. | Texture3D:: Getdimensions ((función)'
ms.assetid: 4a08f14f-7489-4ed1-bf94-4f63f1002eab
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
ms.openlocfilehash: 7a700e0ff065e5f4758241ee0c8252965209a21f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998268"
---
# <a name="texture3dgetdimensions-function"></a><span data-ttu-id="a4734-105">Texture3D:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="a4734-105">Texture3D::GetDimensions function</span></span>

<span data-ttu-id="a4734-106">Devuelve las dimensiones del recurso.</span><span class="sxs-lookup"><span data-stu-id="a4734-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4734-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4734-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="a4734-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4734-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4734-109">*MipLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a4734-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4734-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a4734-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a4734-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a4734-111">Optional.</span></span> <span data-ttu-id="a4734-112">Nivel de mipmap (debe especificarse si se usa *NumberOfLevels* ).</span><span class="sxs-lookup"><span data-stu-id="a4734-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="a4734-113">*Ancho* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a4734-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4734-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a4734-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a4734-115">El ancho del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="a4734-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="a4734-116">*Alto* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a4734-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4734-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a4734-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a4734-118">El alto del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="a4734-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="a4734-119">*Nivel de detalle* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a4734-119">*Depth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4734-120">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a4734-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a4734-121">La profundidad de recursos, en textura.</span><span class="sxs-lookup"><span data-stu-id="a4734-121">The resource depth, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="a4734-122">*NumberOfLevels* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a4734-122">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4734-123">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a4734-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a4734-124">El número de niveles de mipmap (requiere también *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="a4734-124">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4734-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4734-125">Return value</span></span>

<span data-ttu-id="a4734-126">Nada</span><span class="sxs-lookup"><span data-stu-id="a4734-126">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="a4734-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4734-127">Remarks</span></span>

<span data-ttu-id="a4734-128">Esta es una lista de las versiones sobrecargadas de este método.</span><span class="sxs-lookup"><span data-stu-id="a4734-128">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Depth,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



<span data-ttu-id="a4734-129">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="a4734-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a4734-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="a4734-130">Vertex</span></span> | <span data-ttu-id="a4734-131">Casco</span><span class="sxs-lookup"><span data-stu-id="a4734-131">Hull</span></span> | <span data-ttu-id="a4734-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="a4734-132">Domain</span></span> | <span data-ttu-id="a4734-133">Geometría</span><span class="sxs-lookup"><span data-stu-id="a4734-133">Geometry</span></span> | <span data-ttu-id="a4734-134">Píxel</span><span class="sxs-lookup"><span data-stu-id="a4734-134">Pixel</span></span> | <span data-ttu-id="a4734-135">Compute</span><span class="sxs-lookup"><span data-stu-id="a4734-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="a4734-136">x</span><span class="sxs-lookup"><span data-stu-id="a4734-136">x</span></span>     | <span data-ttu-id="a4734-137">x</span><span class="sxs-lookup"><span data-stu-id="a4734-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a4734-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4734-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4734-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a4734-139">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="a4734-140">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a4734-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
