---
title: 'Texture2D:: MIPS. Operador (función)'
description: 'Devuelve una variable de recurso de solo lectura. | Texture2D:: MIPS. Operador (función)'
ms.assetid: 201996a7-741f-4457-ab77-9cd653f3682b
keywords:
- MIPS. Función de operador HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 994ede49563b1d4e568769be48a0e60592fe3dde
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986246"
---
# <a name="texture2dmipsoperator----function"></a><span data-ttu-id="088c9-105">Texture2D:: MIPS. Operador (función)</span><span class="sxs-lookup"><span data-stu-id="088c9-105">Texture2D::mips.Operator    function</span></span>

<span data-ttu-id="088c9-106">Devuelve una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="088c9-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="088c9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="088c9-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="088c9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="088c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="088c9-109">*mipSlice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="088c9-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="088c9-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="088c9-110">Type: **uint**</span></span>

<span data-ttu-id="088c9-111">Índice del segmento MIP.</span><span class="sxs-lookup"><span data-stu-id="088c9-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="088c9-112">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="088c9-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="088c9-113">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="088c9-113">Type: **uint2**</span></span>

<span data-ttu-id="088c9-114">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="088c9-114">The index position.</span></span> <span data-ttu-id="088c9-115">Contiene las coordenadas (x, y).</span><span class="sxs-lookup"><span data-stu-id="088c9-115">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="088c9-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="088c9-116">Return value</span></span>

<span data-ttu-id="088c9-117">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="088c9-117">Type: **R**</span></span>

<span data-ttu-id="088c9-118">Variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="088c9-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="088c9-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="088c9-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="088c9-120">Ejemplo de uso</span><span class="sxs-lookup"><span data-stu-id="088c9-120">Usage Example</span></span>


```
Texture2D<float4> tex;
uint mip = 2;
uint2 pos_xy = {123, 456};
float4 f = tex.mips[mip][pos_xy];
        
```



<span data-ttu-id="088c9-121">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="088c9-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="088c9-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="088c9-122">Vertex</span></span> | <span data-ttu-id="088c9-123">Casco</span><span class="sxs-lookup"><span data-stu-id="088c9-123">Hull</span></span> | <span data-ttu-id="088c9-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="088c9-124">Domain</span></span> | <span data-ttu-id="088c9-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="088c9-125">Geometry</span></span> | <span data-ttu-id="088c9-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="088c9-126">Pixel</span></span> | <span data-ttu-id="088c9-127">Compute</span><span class="sxs-lookup"><span data-stu-id="088c9-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="088c9-128">x</span><span class="sxs-lookup"><span data-stu-id="088c9-128">x</span></span>      | <span data-ttu-id="088c9-129">x</span><span class="sxs-lookup"><span data-stu-id="088c9-129">x</span></span>    | <span data-ttu-id="088c9-130">x</span><span class="sxs-lookup"><span data-stu-id="088c9-130">x</span></span>      | <span data-ttu-id="088c9-131">x</span><span class="sxs-lookup"><span data-stu-id="088c9-131">x</span></span>        | <span data-ttu-id="088c9-132">x</span><span class="sxs-lookup"><span data-stu-id="088c9-132">x</span></span>     | <span data-ttu-id="088c9-133">x</span><span class="sxs-lookup"><span data-stu-id="088c9-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="088c9-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="088c9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="088c9-135">Texture2D</span><span class="sxs-lookup"><span data-stu-id="088c9-135">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="088c9-136">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="088c9-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




