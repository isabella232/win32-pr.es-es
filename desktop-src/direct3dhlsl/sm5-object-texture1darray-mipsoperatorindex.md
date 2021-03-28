---
title: 'Texture1DArray:: MIPS. Operador (función)'
description: 'Devuelve una variable de recurso de solo lectura. | Texture1DArray:: MIPS. Operador (función)'
ms.assetid: b8f2ef78-4b50-4051-a00f-5b81cd77d1e0
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
ms.openlocfilehash: cbe2d1116839cede8dda69f1b0b8cf9a049595e9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083656"
---
# <a name="texture1darraymipsoperator----function"></a><span data-ttu-id="56c27-105">Texture1DArray:: MIPS. Operador (función)</span><span class="sxs-lookup"><span data-stu-id="56c27-105">Texture1DArray::mips.Operator    function</span></span>

<span data-ttu-id="56c27-106">Devuelve una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="56c27-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="56c27-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56c27-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="56c27-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56c27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56c27-109">*mipSlice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="56c27-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56c27-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="56c27-110">Type: **uint**</span></span>

<span data-ttu-id="56c27-111">Índice del segmento MIP.</span><span class="sxs-lookup"><span data-stu-id="56c27-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="56c27-112">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="56c27-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56c27-113">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="56c27-113">Type: **uint2**</span></span>

<span data-ttu-id="56c27-114">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="56c27-114">The index position.</span></span> <span data-ttu-id="56c27-115">El primer componente contiene la coordenada x.</span><span class="sxs-lookup"><span data-stu-id="56c27-115">The first component contains the x-coordinate.</span></span> <span data-ttu-id="56c27-116">El segundo componente indica el segmento de matriz deseado.</span><span class="sxs-lookup"><span data-stu-id="56c27-116">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56c27-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56c27-117">Return value</span></span>

<span data-ttu-id="56c27-118">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="56c27-118">Type: **R**</span></span>

<span data-ttu-id="56c27-119">Variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="56c27-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="56c27-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56c27-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="56c27-121">Ejemplo de uso</span><span class="sxs-lookup"><span data-stu-id="56c27-121">Usage Example</span></span>


```
Texture1DArray<float4> tex;
uint mip = 2;
uint2 pos_x_and_array = {1234, 3};
float4 f = tex.mips[mip][pos_x_and_array];        
        
```



<span data-ttu-id="56c27-122">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="56c27-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="56c27-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="56c27-123">Vertex</span></span> | <span data-ttu-id="56c27-124">Casco</span><span class="sxs-lookup"><span data-stu-id="56c27-124">Hull</span></span> | <span data-ttu-id="56c27-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="56c27-125">Domain</span></span> | <span data-ttu-id="56c27-126">Geometría</span><span class="sxs-lookup"><span data-stu-id="56c27-126">Geometry</span></span> | <span data-ttu-id="56c27-127">Píxel</span><span class="sxs-lookup"><span data-stu-id="56c27-127">Pixel</span></span> | <span data-ttu-id="56c27-128">Compute</span><span class="sxs-lookup"><span data-stu-id="56c27-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="56c27-129">x</span><span class="sxs-lookup"><span data-stu-id="56c27-129">x</span></span>      | <span data-ttu-id="56c27-130">x</span><span class="sxs-lookup"><span data-stu-id="56c27-130">x</span></span>    | <span data-ttu-id="56c27-131">x</span><span class="sxs-lookup"><span data-stu-id="56c27-131">x</span></span>      | <span data-ttu-id="56c27-132">x</span><span class="sxs-lookup"><span data-stu-id="56c27-132">x</span></span>        | <span data-ttu-id="56c27-133">x</span><span class="sxs-lookup"><span data-stu-id="56c27-133">x</span></span>     | <span data-ttu-id="56c27-134">x</span><span class="sxs-lookup"><span data-stu-id="56c27-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="56c27-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="56c27-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56c27-136">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="56c27-136">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="56c27-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="56c27-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




