---
title: 'Texture1D:: MIPS. Operador (función)'
description: Devuelve una variable de recurso de solo lectura o una Texture1D.
ms.assetid: 0b64f0d3-f9a1-474b-b229-d91d18922d5c
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
ms.openlocfilehash: 4713fe20fa52e948113a220969229c413c5dc4d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104359644"
---
# <a name="texture1dmipsoperator----function"></a><span data-ttu-id="09f5c-104">Texture1D:: MIPS. Operador (función)</span><span class="sxs-lookup"><span data-stu-id="09f5c-104">Texture1D::mips.Operator    function</span></span>

<span data-ttu-id="09f5c-105">Devuelve una variable de recurso de solo lectura o una [**Texture1D**](sm5-object-texture1d.md).</span><span class="sxs-lookup"><span data-stu-id="09f5c-105">Returns a read-only resource variable or a [**Texture1D**](sm5-object-texture1d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="09f5c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09f5c-106">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="09f5c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09f5c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09f5c-108">*mipSlice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="09f5c-108">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09f5c-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="09f5c-109">Type: **uint**</span></span>

<span data-ttu-id="09f5c-110">Índice del segmento MIP.</span><span class="sxs-lookup"><span data-stu-id="09f5c-110">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="09f5c-111">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="09f5c-111">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09f5c-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="09f5c-112">Type: **uint**</span></span>

<span data-ttu-id="09f5c-113">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="09f5c-113">The index position.</span></span> <span data-ttu-id="09f5c-114">Contiene la coordenada x.</span><span class="sxs-lookup"><span data-stu-id="09f5c-114">Contains the x-coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09f5c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09f5c-115">Return value</span></span>

<span data-ttu-id="09f5c-116">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="09f5c-116">Type: **R**</span></span>

<span data-ttu-id="09f5c-117">Variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09f5c-117">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="09f5c-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09f5c-118">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="09f5c-119">Ejemplo de uso</span><span class="sxs-lookup"><span data-stu-id="09f5c-119">Usage Example</span></span>


```
Texture1D<float4> tex;
uint mip = 2;
uint pos = 1234;
float4 f = tex.mips[mip][pos];
      
```



<span data-ttu-id="09f5c-120">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="09f5c-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="09f5c-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="09f5c-121">Vertex</span></span> | <span data-ttu-id="09f5c-122">Casco</span><span class="sxs-lookup"><span data-stu-id="09f5c-122">Hull</span></span> | <span data-ttu-id="09f5c-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="09f5c-123">Domain</span></span> | <span data-ttu-id="09f5c-124">Geometría</span><span class="sxs-lookup"><span data-stu-id="09f5c-124">Geometry</span></span> | <span data-ttu-id="09f5c-125">Píxel</span><span class="sxs-lookup"><span data-stu-id="09f5c-125">Pixel</span></span> | <span data-ttu-id="09f5c-126">Compute</span><span class="sxs-lookup"><span data-stu-id="09f5c-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="09f5c-127">x</span><span class="sxs-lookup"><span data-stu-id="09f5c-127">x</span></span>      | <span data-ttu-id="09f5c-128">x</span><span class="sxs-lookup"><span data-stu-id="09f5c-128">x</span></span>    | <span data-ttu-id="09f5c-129">x</span><span class="sxs-lookup"><span data-stu-id="09f5c-129">x</span></span>      | <span data-ttu-id="09f5c-130">x</span><span class="sxs-lookup"><span data-stu-id="09f5c-130">x</span></span>        | <span data-ttu-id="09f5c-131">x</span><span class="sxs-lookup"><span data-stu-id="09f5c-131">x</span></span>     | <span data-ttu-id="09f5c-132">x</span><span class="sxs-lookup"><span data-stu-id="09f5c-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="09f5c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="09f5c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09f5c-134">Texture1D</span><span class="sxs-lookup"><span data-stu-id="09f5c-134">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="09f5c-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="09f5c-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




