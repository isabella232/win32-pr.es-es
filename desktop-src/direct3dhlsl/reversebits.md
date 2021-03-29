---
title: reversebits (función)
description: Invierte el orden de los bits, por componente.
ms.assetid: dad46e25-9980-4645-98eb-d834db704fc8
keywords:
- reversebits (de función HLSL
topic_type:
- apiref
api_name:
- reversebits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d98b824883ddc4f06e6c11d30c2759bb0fc2be26
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487142"
---
# <a name="reversebits-function"></a><span data-ttu-id="4d178-104">reversebits (función)</span><span class="sxs-lookup"><span data-stu-id="4d178-104">reversebits function</span></span>

<span data-ttu-id="4d178-105">Invierte el orden de los bits, por componente.</span><span class="sxs-lookup"><span data-stu-id="4d178-105">Reverses the order of the bits, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d178-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d178-106">Syntax</span></span>

``` syntax
uint reversebits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="4d178-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d178-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d178-108">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4d178-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d178-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4d178-109">Type: **uint**</span></span>

<span data-ttu-id="4d178-110">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="4d178-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d178-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d178-111">Return value</span></span>

<span data-ttu-id="4d178-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4d178-112">Type: **uint**</span></span>

<span data-ttu-id="4d178-113">Valor de entrada, con el orden de bits invertido.</span><span class="sxs-lookup"><span data-stu-id="4d178-113">The input value, with the bit order reversed.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d178-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d178-114">Remarks</span></span>

<span data-ttu-id="4d178-115">También están disponibles las siguientes versiones sobrecargadas:</span><span class="sxs-lookup"><span data-stu-id="4d178-115">The following overloaded versions are also available:</span></span>

``` syntax
uint2 reversebits(uint2 value);
uint3 reversebits(uint3 value);
uint4 reversebits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="4d178-116">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="4d178-116">Minimum Shader Model</span></span>

<span data-ttu-id="4d178-117">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4d178-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4d178-118">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="4d178-118">Shader Model</span></span>                                                                | <span data-ttu-id="4d178-119">Compatible</span><span class="sxs-lookup"><span data-stu-id="4d178-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4d178-120">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="4d178-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="4d178-121">sí</span><span class="sxs-lookup"><span data-stu-id="4d178-121">yes</span></span>       |



 

<span data-ttu-id="4d178-122">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="4d178-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="4d178-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="4d178-123">Vertex</span></span> | <span data-ttu-id="4d178-124">Casco</span><span class="sxs-lookup"><span data-stu-id="4d178-124">Hull</span></span> | <span data-ttu-id="4d178-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="4d178-125">Domain</span></span> | <span data-ttu-id="4d178-126">Geometría</span><span class="sxs-lookup"><span data-stu-id="4d178-126">Geometry</span></span> | <span data-ttu-id="4d178-127">Píxel</span><span class="sxs-lookup"><span data-stu-id="4d178-127">Pixel</span></span> | <span data-ttu-id="4d178-128">Compute</span><span class="sxs-lookup"><span data-stu-id="4d178-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4d178-129">x</span><span class="sxs-lookup"><span data-stu-id="4d178-129">x</span></span>      | <span data-ttu-id="4d178-130">x</span><span class="sxs-lookup"><span data-stu-id="4d178-130">x</span></span>    | <span data-ttu-id="4d178-131">x</span><span class="sxs-lookup"><span data-stu-id="4d178-131">x</span></span>      | <span data-ttu-id="4d178-132">x</span><span class="sxs-lookup"><span data-stu-id="4d178-132">x</span></span>        | <span data-ttu-id="4d178-133">x</span><span class="sxs-lookup"><span data-stu-id="4d178-133">x</span></span>     | <span data-ttu-id="4d178-134">x</span><span class="sxs-lookup"><span data-stu-id="4d178-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4d178-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d178-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d178-136">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="4d178-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="4d178-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4d178-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




