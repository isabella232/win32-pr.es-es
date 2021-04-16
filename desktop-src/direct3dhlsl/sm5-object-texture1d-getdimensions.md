---
title: 'Texture1D:: Getdimensions ((función)'
description: 'Devuelve las dimensiones del recurso. | Texture1D:: Getdimensions ((función)'
ms.assetid: eb8fc02f-01c8-44b9-9d7e-faf59660c287
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
ms.openlocfilehash: fdd9b79a1cc1fa2a5a8db3e0db7a7163878b066b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547635"
---
# <a name="texture1dgetdimensions-function"></a><span data-ttu-id="8054d-105">Texture1D:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="8054d-105">Texture1D::GetDimensions function</span></span>

<span data-ttu-id="8054d-106">Devuelve las dimensiones del recurso.</span><span class="sxs-lookup"><span data-stu-id="8054d-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="8054d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8054d-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="8054d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8054d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8054d-109">*MipLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8054d-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8054d-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8054d-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8054d-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8054d-111">Optional.</span></span> <span data-ttu-id="8054d-112">Nivel de mipmap (debe especificarse si se usa *NumberOfLevels* ).</span><span class="sxs-lookup"><span data-stu-id="8054d-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="8054d-113">*Ancho* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8054d-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8054d-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8054d-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8054d-115">El ancho del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="8054d-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="8054d-116">*NumberOfLevels* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8054d-116">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8054d-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8054d-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8054d-118">El número de niveles de mipmap (requiere también *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="8054d-118">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8054d-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8054d-119">Return value</span></span>

<span data-ttu-id="8054d-120">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8054d-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8054d-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8054d-121">Remarks</span></span>

<span data-ttu-id="8054d-122">Esta es una lista de las versiones sobrecargadas de este método.</span><span class="sxs-lookup"><span data-stu-id="8054d-122">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float NumberOfLevels);

void GetDimensions(out float Width);
```



<span data-ttu-id="8054d-123">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="8054d-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8054d-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="8054d-124">Vertex</span></span> | <span data-ttu-id="8054d-125">Casco</span><span class="sxs-lookup"><span data-stu-id="8054d-125">Hull</span></span> | <span data-ttu-id="8054d-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="8054d-126">Domain</span></span> | <span data-ttu-id="8054d-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="8054d-127">Geometry</span></span> | <span data-ttu-id="8054d-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="8054d-128">Pixel</span></span> | <span data-ttu-id="8054d-129">Compute</span><span class="sxs-lookup"><span data-stu-id="8054d-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8054d-130">x</span><span class="sxs-lookup"><span data-stu-id="8054d-130">x</span></span>     | <span data-ttu-id="8054d-131">x</span><span class="sxs-lookup"><span data-stu-id="8054d-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8054d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="8054d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8054d-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="8054d-133">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="8054d-134">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8054d-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
