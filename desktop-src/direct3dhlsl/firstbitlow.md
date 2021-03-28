---
title: firstbitlow (función)
description: Devuelve la ubicación del primer bit establecido empezando por el bit de orden más bajo y trabajando hacia arriba, por componente.
ms.assetid: 204250f3-1a9b-445d-bd16-4cc9a5d9d60a
keywords:
- firstbitlow (de función HLSL
topic_type:
- apiref
api_name:
- firstbitlow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a647314383bc022b7c3b3e1b5a255a42a099c620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077945"
---
# <a name="firstbitlow-function"></a><span data-ttu-id="401ef-104">firstbitlow (función)</span><span class="sxs-lookup"><span data-stu-id="401ef-104">firstbitlow function</span></span>

<span data-ttu-id="401ef-105">Devuelve la ubicación del primer bit establecido empezando por el bit de orden más bajo y trabajando hacia arriba, por componente.</span><span class="sxs-lookup"><span data-stu-id="401ef-105">Returns the location of the first set bit starting from the lowest order bit and working upward, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="401ef-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="401ef-106">Syntax</span></span>

``` syntax
int firstbitlow(
  in int value
);
```

## <a name="parameters"></a><span data-ttu-id="401ef-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="401ef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="401ef-108">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="401ef-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="401ef-109">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="401ef-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="401ef-110">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="401ef-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="401ef-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="401ef-111">Return value</span></span>

<span data-ttu-id="401ef-112">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="401ef-112">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="401ef-113">La ubicación del primer bit establecido.</span><span class="sxs-lookup"><span data-stu-id="401ef-113">The location of the first set bit.</span></span>

## <a name="remarks"></a><span data-ttu-id="401ef-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="401ef-114">Remarks</span></span>

<span data-ttu-id="401ef-115">También están disponibles las siguientes versiones sobrecargadas:</span><span class="sxs-lookup"><span data-stu-id="401ef-115">The following overloaded versions are also available:</span></span>

``` syntax
uint2 firstbitlow(uint2 value);
uint3 firstbitlow(uint3 value);
uint4 firstbitlow(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="401ef-116">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="401ef-116">Minimum Shader Model</span></span>

<span data-ttu-id="401ef-117">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="401ef-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="401ef-118">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="401ef-118">Shader Model</span></span>                                                                | <span data-ttu-id="401ef-119">Compatible</span><span class="sxs-lookup"><span data-stu-id="401ef-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="401ef-120">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="401ef-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="401ef-121">sí</span><span class="sxs-lookup"><span data-stu-id="401ef-121">yes</span></span>       |



 

<span data-ttu-id="401ef-122">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="401ef-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="401ef-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="401ef-123">Vertex</span></span> | <span data-ttu-id="401ef-124">Casco</span><span class="sxs-lookup"><span data-stu-id="401ef-124">Hull</span></span> | <span data-ttu-id="401ef-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="401ef-125">Domain</span></span> | <span data-ttu-id="401ef-126">Geometría</span><span class="sxs-lookup"><span data-stu-id="401ef-126">Geometry</span></span> | <span data-ttu-id="401ef-127">Píxel</span><span class="sxs-lookup"><span data-stu-id="401ef-127">Pixel</span></span> | <span data-ttu-id="401ef-128">Compute</span><span class="sxs-lookup"><span data-stu-id="401ef-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="401ef-129">x</span><span class="sxs-lookup"><span data-stu-id="401ef-129">x</span></span>      | <span data-ttu-id="401ef-130">x</span><span class="sxs-lookup"><span data-stu-id="401ef-130">x</span></span>    | <span data-ttu-id="401ef-131">x</span><span class="sxs-lookup"><span data-stu-id="401ef-131">x</span></span>      | <span data-ttu-id="401ef-132">x</span><span class="sxs-lookup"><span data-stu-id="401ef-132">x</span></span>        | <span data-ttu-id="401ef-133">x</span><span class="sxs-lookup"><span data-stu-id="401ef-133">x</span></span>     | <span data-ttu-id="401ef-134">x</span><span class="sxs-lookup"><span data-stu-id="401ef-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="401ef-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="401ef-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="401ef-136">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="401ef-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="401ef-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="401ef-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 