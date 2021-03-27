---
title: 'Texture2DArray:: MIPS. Operador (función)'
description: 'Devuelve una variable de recurso de solo lectura. | Texture2DArray:: MIPS. Operador (función)'
ms.assetid: 66639bf6-74dd-4c69-9cc1-74cc9314de57
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
ms.openlocfilehash: 17f24dd54768f3583f508527b7e03f72399bf98e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820791"
---
# <a name="texture2darraymipsoperator----function"></a><span data-ttu-id="37867-105">Texture2DArray:: MIPS. Operador (función)</span><span class="sxs-lookup"><span data-stu-id="37867-105">Texture2DArray::mips.Operator    function</span></span>

<span data-ttu-id="37867-106">Devuelve una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="37867-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="37867-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37867-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="37867-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37867-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37867-109">*mipSlice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="37867-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37867-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="37867-110">Type: **uint**</span></span>

<span data-ttu-id="37867-111">Índice del segmento MIP.</span><span class="sxs-lookup"><span data-stu-id="37867-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="37867-112">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="37867-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37867-113">Tipo: **UInt3**</span><span class="sxs-lookup"><span data-stu-id="37867-113">Type: **uint3**</span></span>

<span data-ttu-id="37867-114">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="37867-114">The index position.</span></span> <span data-ttu-id="37867-115">Los componentes primero y segundo contienen las coordenadas (x, y).</span><span class="sxs-lookup"><span data-stu-id="37867-115">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="37867-116">El tercer componente indica el segmento de matriz deseado.</span><span class="sxs-lookup"><span data-stu-id="37867-116">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37867-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37867-117">Return value</span></span>

<span data-ttu-id="37867-118">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="37867-118">Type: **R**</span></span>

<span data-ttu-id="37867-119">Variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="37867-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="37867-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37867-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="37867-121">Ejemplo de uso</span><span class="sxs-lookup"><span data-stu-id="37867-121">Usage Example</span></span>


```
Texture2DArray<float4> tex;
uint mip = 2;
uint2 pos_xy_and_array = {123, 456, 3};
float4 f = tex.mips[mip][pos_xy_and_array];
        
```



<span data-ttu-id="37867-122">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="37867-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="37867-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="37867-123">Vertex</span></span> | <span data-ttu-id="37867-124">Casco</span><span class="sxs-lookup"><span data-stu-id="37867-124">Hull</span></span> | <span data-ttu-id="37867-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="37867-125">Domain</span></span> | <span data-ttu-id="37867-126">Geometría</span><span class="sxs-lookup"><span data-stu-id="37867-126">Geometry</span></span> | <span data-ttu-id="37867-127">Píxel</span><span class="sxs-lookup"><span data-stu-id="37867-127">Pixel</span></span> | <span data-ttu-id="37867-128">Compute</span><span class="sxs-lookup"><span data-stu-id="37867-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="37867-129">x</span><span class="sxs-lookup"><span data-stu-id="37867-129">x</span></span>      | <span data-ttu-id="37867-130">x</span><span class="sxs-lookup"><span data-stu-id="37867-130">x</span></span>    | <span data-ttu-id="37867-131">x</span><span class="sxs-lookup"><span data-stu-id="37867-131">x</span></span>      | <span data-ttu-id="37867-132">x</span><span class="sxs-lookup"><span data-stu-id="37867-132">x</span></span>        | <span data-ttu-id="37867-133">x</span><span class="sxs-lookup"><span data-stu-id="37867-133">x</span></span>     | <span data-ttu-id="37867-134">x</span><span class="sxs-lookup"><span data-stu-id="37867-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="37867-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="37867-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37867-136">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="37867-136">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="37867-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="37867-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




