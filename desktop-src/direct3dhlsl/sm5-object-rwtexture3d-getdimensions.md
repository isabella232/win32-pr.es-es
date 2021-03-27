---
title: 'RWTexture3D:: Getdimensions ((función)'
description: 'Devuelve las dimensiones del recurso. | RWTexture3D:: Getdimensions ((función)'
ms.assetid: ba70b955-1e80-4f27-84f1-fc9d26a1f1ab
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
ms.openlocfilehash: 499ab493851257030921e9d55f4873eef8726915
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362192"
---
# <a name="rwtexture3dgetdimensions-function"></a><span data-ttu-id="892fd-105">RWTexture3D:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="892fd-105">RWTexture3D::GetDimensions function</span></span>

<span data-ttu-id="892fd-106">Devuelve las dimensiones del recurso.</span><span class="sxs-lookup"><span data-stu-id="892fd-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="892fd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="892fd-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Depth
);
```

## <a name="parameters"></a><span data-ttu-id="892fd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="892fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="892fd-109">*Ancho* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="892fd-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="892fd-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="892fd-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="892fd-111">El ancho del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="892fd-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="892fd-112">*Alto* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="892fd-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="892fd-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="892fd-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="892fd-114">El alto del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="892fd-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="892fd-115">*Nivel de detalle* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="892fd-115">*Depth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="892fd-116">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="892fd-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="892fd-117">La profundidad de recursos, en textura.</span><span class="sxs-lookup"><span data-stu-id="892fd-117">The resource depth, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="892fd-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="892fd-118">Return value</span></span>

<span data-ttu-id="892fd-119">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="892fd-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="892fd-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="892fd-120">Remarks</span></span>

<span data-ttu-id="892fd-121">Esta es una lista de las versiones sobrecargadas de este método.</span><span class="sxs-lookup"><span data-stu-id="892fd-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



<span data-ttu-id="892fd-122">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="892fd-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="892fd-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="892fd-123">Vertex</span></span> | <span data-ttu-id="892fd-124">Casco</span><span class="sxs-lookup"><span data-stu-id="892fd-124">Hull</span></span> | <span data-ttu-id="892fd-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="892fd-125">Domain</span></span> | <span data-ttu-id="892fd-126">Geometría</span><span class="sxs-lookup"><span data-stu-id="892fd-126">Geometry</span></span> | <span data-ttu-id="892fd-127">Píxel</span><span class="sxs-lookup"><span data-stu-id="892fd-127">Pixel</span></span> | <span data-ttu-id="892fd-128">Compute</span><span class="sxs-lookup"><span data-stu-id="892fd-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="892fd-129">x</span><span class="sxs-lookup"><span data-stu-id="892fd-129">x</span></span>     | <span data-ttu-id="892fd-130">x</span><span class="sxs-lookup"><span data-stu-id="892fd-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="892fd-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="892fd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="892fd-132">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="892fd-132">RWTexture3D</span></span>](sm5-object-rwtexture3d.md)
</dt> <dt>

[<span data-ttu-id="892fd-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="892fd-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
