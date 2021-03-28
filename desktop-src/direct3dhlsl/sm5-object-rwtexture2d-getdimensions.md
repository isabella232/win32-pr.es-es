---
title: 'RWTexture2D:: Getdimensions ((función)'
description: 'Devuelve las dimensiones del recurso. | RWTexture2D:: Getdimensions ((función)'
ms.assetid: bc55622d-fbff-4aeb-aceb-4eb2cfc7ac28
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
ms.openlocfilehash: 19a6711e8f04afdb2f5ec66ff33c8aaf1d59b40c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104157109"
---
# <a name="rwtexture2dgetdimensions-function"></a><span data-ttu-id="fbcb0-105">RWTexture2D:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="fbcb0-105">RWTexture2D::GetDimensions function</span></span>

<span data-ttu-id="fbcb0-106">Devuelve las dimensiones del recurso.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbcb0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fbcb0-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height
);
```

## <a name="parameters"></a><span data-ttu-id="fbcb0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fbcb0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbcb0-109">*Ancho* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fbcb0-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbcb0-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fbcb0-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fbcb0-111">El ancho del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="fbcb0-112">*Alto* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fbcb0-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbcb0-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fbcb0-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fbcb0-114">El alto del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-114">The resource height, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbcb0-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fbcb0-115">Return value</span></span>

<span data-ttu-id="fbcb0-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbcb0-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fbcb0-117">Remarks</span></span>

<span data-ttu-id="fbcb0-118">Esta es una lista de las versiones sobrecargadas de este método.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-118">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height);

void GetDimensions(out float Width,
  out float Height);
```



<span data-ttu-id="fbcb0-119">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="fbcb0-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fbcb0-120">Vértice</span><span class="sxs-lookup"><span data-stu-id="fbcb0-120">Vertex</span></span> | <span data-ttu-id="fbcb0-121">Casco</span><span class="sxs-lookup"><span data-stu-id="fbcb0-121">Hull</span></span> | <span data-ttu-id="fbcb0-122">Dominio</span><span class="sxs-lookup"><span data-stu-id="fbcb0-122">Domain</span></span> | <span data-ttu-id="fbcb0-123">Geometría</span><span class="sxs-lookup"><span data-stu-id="fbcb0-123">Geometry</span></span> | <span data-ttu-id="fbcb0-124">Píxel</span><span class="sxs-lookup"><span data-stu-id="fbcb0-124">Pixel</span></span> | <span data-ttu-id="fbcb0-125">Compute</span><span class="sxs-lookup"><span data-stu-id="fbcb0-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="fbcb0-126">x</span><span class="sxs-lookup"><span data-stu-id="fbcb0-126">x</span></span>     | <span data-ttu-id="fbcb0-127">x</span><span class="sxs-lookup"><span data-stu-id="fbcb0-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fbcb0-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbcb0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbcb0-129">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="fbcb0-129">RWTexture2D</span></span>](sm5-object-rwtexture2d.md)
</dt> <dt>

[<span data-ttu-id="fbcb0-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="fbcb0-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
