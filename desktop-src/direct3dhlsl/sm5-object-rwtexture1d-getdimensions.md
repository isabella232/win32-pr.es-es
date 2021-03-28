---
title: 'RWTexture1D:: Getdimensions ((función)'
description: 'Devuelve las dimensiones del recurso. | RWTexture1D:: Getdimensions ((función)'
ms.assetid: 1bbd53ed-9396-4e8e-b2f3-3bd85f6e1a90
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
ms.openlocfilehash: b65f0113ecf2c91786e45c35f5e8e832744bc952
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986199"
---
# <a name="rwtexture1dgetdimensions-function"></a><span data-ttu-id="a41f9-105">RWTexture1D:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="a41f9-105">RWTexture1D::GetDimensions function</span></span>

<span data-ttu-id="a41f9-106">Devuelve las dimensiones del recurso.</span><span class="sxs-lookup"><span data-stu-id="a41f9-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="a41f9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a41f9-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width
);
```

## <a name="parameters"></a><span data-ttu-id="a41f9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a41f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a41f9-109">*Ancho* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a41f9-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a41f9-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a41f9-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a41f9-111">El ancho del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="a41f9-111">The resource width, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a41f9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a41f9-112">Return value</span></span>

<span data-ttu-id="a41f9-113">Nada</span><span class="sxs-lookup"><span data-stu-id="a41f9-113">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="a41f9-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a41f9-114">Remarks</span></span>

<span data-ttu-id="a41f9-115">Esta es una lista de las versiones sobrecargadas de este método.</span><span class="sxs-lookup"><span data-stu-id="a41f9-115">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width);

void GetDimensions(out float Width);
```



<span data-ttu-id="a41f9-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="a41f9-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a41f9-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="a41f9-117">Vertex</span></span> | <span data-ttu-id="a41f9-118">Casco</span><span class="sxs-lookup"><span data-stu-id="a41f9-118">Hull</span></span> | <span data-ttu-id="a41f9-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="a41f9-119">Domain</span></span> | <span data-ttu-id="a41f9-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="a41f9-120">Geometry</span></span> | <span data-ttu-id="a41f9-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="a41f9-121">Pixel</span></span> | <span data-ttu-id="a41f9-122">Compute</span><span class="sxs-lookup"><span data-stu-id="a41f9-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="a41f9-123">x</span><span class="sxs-lookup"><span data-stu-id="a41f9-123">x</span></span>     | <span data-ttu-id="a41f9-124">x</span><span class="sxs-lookup"><span data-stu-id="a41f9-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a41f9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a41f9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a41f9-126">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="a41f9-126">RWTexture1D</span></span>](sm5-object-rwtexture1d.md)
</dt> <dt>

[<span data-ttu-id="a41f9-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a41f9-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
