---
title: firstbithigh (función)
description: Obtiene la ubicación del primer bit establecido empezando por el bit de orden más alto y trabajando hacia abajo, por componente.
ms.assetid: 0fa89a9e-1706-44f7-8dd3-c37af5c11ddc
keywords:
- firstbithigh (de función HLSL
topic_type:
- apiref
api_name:
- firstbithigh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4da4956aa3a12d064566a3767423f42039b01355
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420900"
---
# <a name="firstbithigh-function"></a><span data-ttu-id="8f2ba-104">firstbithigh (función)</span><span class="sxs-lookup"><span data-stu-id="8f2ba-104">firstbithigh function</span></span>

<span data-ttu-id="8f2ba-105">Obtiene la ubicación del primer bit establecido empezando por el bit de orden más alto y trabajando hacia abajo, por componente.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-105">Gets the location of the first set bit starting from the highest order bit and working downward, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f2ba-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f2ba-106">Syntax</span></span>

``` syntax
int firstbithigh(
  in int value
);
```

## <a name="parameters"></a><span data-ttu-id="8f2ba-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f2ba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f2ba-108">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8f2ba-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f2ba-109">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f2ba-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8f2ba-110">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f2ba-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f2ba-111">Return value</span></span>

<span data-ttu-id="8f2ba-112">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f2ba-112">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8f2ba-113">La ubicación del primer bit establecido.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-113">The location of the first set bit.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f2ba-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f2ba-114">Remarks</span></span>

<span data-ttu-id="8f2ba-115">Para un entero con signo, el primer bit significativo es cero para un número negativo.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-115">For a signed integer, the first significant bit is zero for a negative number.</span></span>

<span data-ttu-id="8f2ba-116">También están disponibles las siguientes versiones sobrecargadas:</span><span class="sxs-lookup"><span data-stu-id="8f2ba-116">The following overloaded versions are also available:</span></span>

``` syntax
int2 firstbithigh(int2 value);
int3 firstbithigh(int3 value);
int4 firstbithigh(int4 value);
uint firstbithigh(uint value);
uint2 firstbithigh(uint2 value);
uint3 firstbithigh(uint3 value);
uint4 firstbithigh(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="8f2ba-117">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="8f2ba-117">Minimum Shader Model</span></span>

<span data-ttu-id="8f2ba-118">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8f2ba-119">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="8f2ba-119">Shader Model</span></span>                                                                | <span data-ttu-id="8f2ba-120">Compatible</span><span class="sxs-lookup"><span data-stu-id="8f2ba-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8f2ba-121">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8f2ba-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="8f2ba-122">sí</span><span class="sxs-lookup"><span data-stu-id="8f2ba-122">yes</span></span>       |



 

<span data-ttu-id="8f2ba-123">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="8f2ba-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="8f2ba-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="8f2ba-124">Vertex</span></span> | <span data-ttu-id="8f2ba-125">Casco</span><span class="sxs-lookup"><span data-stu-id="8f2ba-125">Hull</span></span> | <span data-ttu-id="8f2ba-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="8f2ba-126">Domain</span></span> | <span data-ttu-id="8f2ba-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="8f2ba-127">Geometry</span></span> | <span data-ttu-id="8f2ba-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="8f2ba-128">Pixel</span></span> | <span data-ttu-id="8f2ba-129">Compute</span><span class="sxs-lookup"><span data-stu-id="8f2ba-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8f2ba-130">x</span><span class="sxs-lookup"><span data-stu-id="8f2ba-130">x</span></span>      | <span data-ttu-id="8f2ba-131">x</span><span class="sxs-lookup"><span data-stu-id="8f2ba-131">x</span></span>    | <span data-ttu-id="8f2ba-132">x</span><span class="sxs-lookup"><span data-stu-id="8f2ba-132">x</span></span>      | <span data-ttu-id="8f2ba-133">x</span><span class="sxs-lookup"><span data-stu-id="8f2ba-133">x</span></span>        | <span data-ttu-id="8f2ba-134">x</span><span class="sxs-lookup"><span data-stu-id="8f2ba-134">x</span></span>     | <span data-ttu-id="8f2ba-135">x</span><span class="sxs-lookup"><span data-stu-id="8f2ba-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8f2ba-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f2ba-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f2ba-137">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="8f2ba-137">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="8f2ba-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8f2ba-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 