---
title: 'Texture2DMSArray:: sample. Operador (función)'
description: 'Devuelve una variable de recurso de solo lectura. | Texture2DMSArray:: sample. Operador (función)'
ms.assetid: 5334c1d5-dfbd-4987-875c-0b92967b0f13
keywords:
- AdventureWorks. Función de operador HLSL
topic_type:
- apiref
api_name:
- sample.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e78746e0afe03e65a313982ca35c27a75ea14f1b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986677"
---
# <a name="texture2dmsarraysampleoperator----function"></a><span data-ttu-id="50831-105">Texture2DMSArray:: sample. Operador (función)</span><span class="sxs-lookup"><span data-stu-id="50831-105">Texture2DMSArray::sample.Operator    function</span></span>

<span data-ttu-id="50831-106">Devuelve una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="50831-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="50831-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50831-107">Syntax</span></span>

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="50831-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50831-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50831-109">*sampleSlice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="50831-109">*sampleSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50831-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="50831-110">Type: **uint**</span></span>

<span data-ttu-id="50831-111">Índice del segmento de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="50831-111">The sample slice index.</span></span>

</dd> <dt>

<span data-ttu-id="50831-112">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="50831-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50831-113">Tipo: **UInt3**</span><span class="sxs-lookup"><span data-stu-id="50831-113">Type: **uint3**</span></span>

<span data-ttu-id="50831-114">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="50831-114">The index position.</span></span> <span data-ttu-id="50831-115">Los componentes primero y segundo contienen las coordenadas (x, y).</span><span class="sxs-lookup"><span data-stu-id="50831-115">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="50831-116">El tercer componente indica el segmento de matriz deseado.</span><span class="sxs-lookup"><span data-stu-id="50831-116">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50831-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50831-117">Return value</span></span>

<span data-ttu-id="50831-118">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="50831-118">Type: **R**</span></span>

<span data-ttu-id="50831-119">Variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="50831-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="50831-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50831-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="50831-121">Ejemplo de uso</span><span class="sxs-lookup"><span data-stu-id="50831-121">Usage Example</span></span>


```
Texture2DMSArray<float4, 4> alpha;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



<span data-ttu-id="50831-122">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="50831-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="50831-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="50831-123">Vertex</span></span> | <span data-ttu-id="50831-124">Casco</span><span class="sxs-lookup"><span data-stu-id="50831-124">Hull</span></span> | <span data-ttu-id="50831-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="50831-125">Domain</span></span> | <span data-ttu-id="50831-126">Geometría</span><span class="sxs-lookup"><span data-stu-id="50831-126">Geometry</span></span> | <span data-ttu-id="50831-127">Píxel</span><span class="sxs-lookup"><span data-stu-id="50831-127">Pixel</span></span> | <span data-ttu-id="50831-128">Compute</span><span class="sxs-lookup"><span data-stu-id="50831-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="50831-129">x</span><span class="sxs-lookup"><span data-stu-id="50831-129">x</span></span>      | <span data-ttu-id="50831-130">x</span><span class="sxs-lookup"><span data-stu-id="50831-130">x</span></span>    | <span data-ttu-id="50831-131">x</span><span class="sxs-lookup"><span data-stu-id="50831-131">x</span></span>      | <span data-ttu-id="50831-132">x</span><span class="sxs-lookup"><span data-stu-id="50831-132">x</span></span>        | <span data-ttu-id="50831-133">x</span><span class="sxs-lookup"><span data-stu-id="50831-133">x</span></span>     | <span data-ttu-id="50831-134">x</span><span class="sxs-lookup"><span data-stu-id="50831-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="50831-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="50831-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50831-136">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="50831-136">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="50831-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="50831-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




