---
title: 'RWTexture1DArray:: Getdimensions ((función)'
description: 'Devuelve las dimensiones del recurso. | RWTexture1DArray:: Getdimensions ((función)'
ms.assetid: 64f2757e-c03c-4f72-b081-1c57656d6e95
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
ms.openlocfilehash: d31d04ccf62b42fede209589a5e4a6760a3091d9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280080"
---
# <a name="rwtexture1darraygetdimensions-function"></a><span data-ttu-id="4cffc-105">RWTexture1DArray:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="4cffc-105">RWTexture1DArray::GetDimensions function</span></span>

<span data-ttu-id="4cffc-106">Devuelve las dimensiones del recurso.</span><span class="sxs-lookup"><span data-stu-id="4cffc-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cffc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4cffc-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Elements
);
```

## <a name="parameters"></a><span data-ttu-id="4cffc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4cffc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cffc-109">*Ancho* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4cffc-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cffc-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4cffc-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4cffc-111">El ancho del recurso, en textura.</span><span class="sxs-lookup"><span data-stu-id="4cffc-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="4cffc-112">*Elementos* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4cffc-112">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cffc-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4cffc-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4cffc-114">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="4cffc-114">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cffc-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4cffc-115">Return value</span></span>

<span data-ttu-id="4cffc-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4cffc-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cffc-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4cffc-117">Remarks</span></span>

<span data-ttu-id="4cffc-118">Esta es una lista de las versiones sobrecargadas de este método.</span><span class="sxs-lookup"><span data-stu-id="4cffc-118">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Elements);

void GetDimensions(out float Width,
  out UINT Elements);
```



<span data-ttu-id="4cffc-119">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="4cffc-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4cffc-120">Vértice</span><span class="sxs-lookup"><span data-stu-id="4cffc-120">Vertex</span></span> | <span data-ttu-id="4cffc-121">Casco</span><span class="sxs-lookup"><span data-stu-id="4cffc-121">Hull</span></span> | <span data-ttu-id="4cffc-122">Dominio</span><span class="sxs-lookup"><span data-stu-id="4cffc-122">Domain</span></span> | <span data-ttu-id="4cffc-123">Geometría</span><span class="sxs-lookup"><span data-stu-id="4cffc-123">Geometry</span></span> | <span data-ttu-id="4cffc-124">Píxel</span><span class="sxs-lookup"><span data-stu-id="4cffc-124">Pixel</span></span> | <span data-ttu-id="4cffc-125">Compute</span><span class="sxs-lookup"><span data-stu-id="4cffc-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4cffc-126">x</span><span class="sxs-lookup"><span data-stu-id="4cffc-126">x</span></span>     | <span data-ttu-id="4cffc-127">x</span><span class="sxs-lookup"><span data-stu-id="4cffc-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4cffc-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cffc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cffc-129">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="4cffc-129">RWTexture1DArray</span></span>](sm5-object-rwtexture1darray.md)
</dt> <dt>

[<span data-ttu-id="4cffc-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4cffc-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
