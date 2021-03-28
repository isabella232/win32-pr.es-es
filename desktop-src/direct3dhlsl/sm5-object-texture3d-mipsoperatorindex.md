---
title: 'Texture3D:: MIPS. Operador (función)'
description: 'Devuelve una variable de recurso de solo lectura. | Texture3D:: MIPS. Operador (función)'
ms.assetid: d5f6cb3b-4163-44c2-8379-ac8a412b1aa6
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
ms.openlocfilehash: e8f7064459354ec4827ba6d96795e82ccab3800c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279995"
---
# <a name="texture3dmipsoperator----function"></a><span data-ttu-id="f5d1a-105">Texture3D:: MIPS. Operador (función)</span><span class="sxs-lookup"><span data-stu-id="f5d1a-105">Texture3D::mips.Operator    function</span></span>

<span data-ttu-id="f5d1a-106">Devuelve una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f5d1a-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5d1a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5d1a-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="f5d1a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5d1a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5d1a-109">*mipSlice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f5d1a-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5d1a-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="f5d1a-110">Type: **uint**</span></span>

<span data-ttu-id="f5d1a-111">Índice del segmento MIP.</span><span class="sxs-lookup"><span data-stu-id="f5d1a-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="f5d1a-112">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f5d1a-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5d1a-113">Tipo: **UInt3**</span><span class="sxs-lookup"><span data-stu-id="f5d1a-113">Type: **uint3**</span></span>

<span data-ttu-id="f5d1a-114">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="f5d1a-114">The index position.</span></span> <span data-ttu-id="f5d1a-115">Contiene las coordenadas (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="f5d1a-115">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5d1a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5d1a-116">Return value</span></span>

<span data-ttu-id="f5d1a-117">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="f5d1a-117">Type: **R**</span></span>

<span data-ttu-id="f5d1a-118">Variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f5d1a-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5d1a-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5d1a-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="f5d1a-120">Ejemplo de uso</span><span class="sxs-lookup"><span data-stu-id="f5d1a-120">Usage Example</span></span>


```
Texture3D<float4> tex;
uint mip = 2;
uint3 pos_xyz = {123, 456, 789};
float4 f = tex.mips[mip][pos_xyz];
        
```



<span data-ttu-id="f5d1a-121">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="f5d1a-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f5d1a-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="f5d1a-122">Vertex</span></span> | <span data-ttu-id="f5d1a-123">Casco</span><span class="sxs-lookup"><span data-stu-id="f5d1a-123">Hull</span></span> | <span data-ttu-id="f5d1a-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="f5d1a-124">Domain</span></span> | <span data-ttu-id="f5d1a-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="f5d1a-125">Geometry</span></span> | <span data-ttu-id="f5d1a-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="f5d1a-126">Pixel</span></span> | <span data-ttu-id="f5d1a-127">Compute</span><span class="sxs-lookup"><span data-stu-id="f5d1a-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f5d1a-128">x</span><span class="sxs-lookup"><span data-stu-id="f5d1a-128">x</span></span>      | <span data-ttu-id="f5d1a-129">x</span><span class="sxs-lookup"><span data-stu-id="f5d1a-129">x</span></span>    | <span data-ttu-id="f5d1a-130">x</span><span class="sxs-lookup"><span data-stu-id="f5d1a-130">x</span></span>      | <span data-ttu-id="f5d1a-131">x</span><span class="sxs-lookup"><span data-stu-id="f5d1a-131">x</span></span>        | <span data-ttu-id="f5d1a-132">x</span><span class="sxs-lookup"><span data-stu-id="f5d1a-132">x</span></span>     | <span data-ttu-id="f5d1a-133">x</span><span class="sxs-lookup"><span data-stu-id="f5d1a-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f5d1a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5d1a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5d1a-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f5d1a-135">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="f5d1a-136">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f5d1a-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




