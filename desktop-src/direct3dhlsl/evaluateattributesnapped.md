---
title: EvaluateAttributeSnapped función)
description: Evalúa en el píxel centroide con un desplazamiento.
ms.assetid: f5085016-0e94-49bb-96b6-42fa15c30b9f
keywords:
- EvaluateAttributeSnapped de función HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeSnapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70a9389ed9e9f4fff16f82610cb611bc4da2c7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104996816"
---
# <a name="evaluateattributesnapped-function"></a><span data-ttu-id="f03e3-104">EvaluateAttributeSnapped función)</span><span class="sxs-lookup"><span data-stu-id="f03e3-104">EvaluateAttributeSnapped function</span></span>

<span data-ttu-id="f03e3-105">Evalúa en el píxel centroide con un desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="f03e3-105">Evaluates at the pixel centroid with an offset.</span></span>

## <a name="syntax"></a><span data-ttu-id="f03e3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f03e3-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeSnapped(
  in attrib numeric value,
  in 
            int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="f03e3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f03e3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f03e3-108">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f03e3-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f03e3-109">Tipo: **attrib Numeric**</span><span class="sxs-lookup"><span data-stu-id="f03e3-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="f03e3-110">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="f03e3-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="f03e3-111">*desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f03e3-111">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f03e3-112">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="f03e3-112">Type: **int2**</span></span>

<span data-ttu-id="f03e3-113">Desplazamiento 2D desde el centro de píxeles mediante una cuadrícula de 16x16.</span><span class="sxs-lookup"><span data-stu-id="f03e3-113">A 2D offset from the pixel center using a 16x16 grid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f03e3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f03e3-114">Remarks</span></span>

<span data-ttu-id="f03e3-115">El intervalo para el parámetro de *desplazamiento* debe definirse mediante el siguiente código de byte.</span><span class="sxs-lookup"><span data-stu-id="f03e3-115">The range for the *offset* parameter must be defined by the following byte code.</span></span>

<span data-ttu-id="f03e3-116">Solo se usan los 4 bits menos significativos de los dos primeros componentes (U, V) del desplazamiento de píxeles.</span><span class="sxs-lookup"><span data-stu-id="f03e3-116">Only the least significant 4 bits of the first two components (U, V) of the pixel offset are used.</span></span> <span data-ttu-id="f03e3-117">La conversión del punto fijo de 4 bits a Float es la siguiente (MSB... LSB), donde el MSB es una parte de la fracción y determina el signo:</span><span class="sxs-lookup"><span data-stu-id="f03e3-117">The conversion from the 4-bit fixed point to float is as follows (MSB...LSB), where the MSB is both a part of the fraction and determines the sign:</span></span>

-   <span data-ttu-id="f03e3-118">1000 =-0.5 f (-8/16)</span><span class="sxs-lookup"><span data-stu-id="f03e3-118">1000 = -0.5f (-8 / 16)</span></span>
-   <span data-ttu-id="f03e3-119">1001 =-0.4375 f (-7/16)</span><span class="sxs-lookup"><span data-stu-id="f03e3-119">1001 = -0.4375f (-7 / 16)</span></span>
-   <span data-ttu-id="f03e3-120">1010 =-0.375 f (-6/16)</span><span class="sxs-lookup"><span data-stu-id="f03e3-120">1010 = -0.375f (-6 / 16)</span></span>
-   <span data-ttu-id="f03e3-121">1011 =-0.3125 f (-5/16)</span><span class="sxs-lookup"><span data-stu-id="f03e3-121">1011 = -0.3125f (-5 / 16)</span></span>
-   <span data-ttu-id="f03e3-122">1100 =-0,25 f (-4/16)</span><span class="sxs-lookup"><span data-stu-id="f03e3-122">1100 = -0.25f (-4 / 16)</span></span>
-   <span data-ttu-id="f03e3-123">1101 =-0.1875 f (-3/16)</span><span class="sxs-lookup"><span data-stu-id="f03e3-123">1101 = -0.1875f (-3 / 16)</span></span>
-   <span data-ttu-id="f03e3-124">1110 =-0,125 f (-2/16)</span><span class="sxs-lookup"><span data-stu-id="f03e3-124">1110 = -0.125f (-2 / 16)</span></span>
-   <span data-ttu-id="f03e3-125">1111 =-0.0625 f (-1/16)</span><span class="sxs-lookup"><span data-stu-id="f03e3-125">1111 = -0.0625f (-1 / 16)</span></span>
-   <span data-ttu-id="f03e3-126">0000 = 0.0 f (0/16)</span><span class="sxs-lookup"><span data-stu-id="f03e3-126">0000 = 0.0f ( 0 / 16)</span></span>
-   <span data-ttu-id="f03e3-127">0001 = 0.0625 f (1/16)</span><span class="sxs-lookup"><span data-stu-id="f03e3-127">0001 = 0.0625f ( 1 / 16)</span></span>
-   <span data-ttu-id="f03e3-128">0010 = 0,125 f (2/16)</span><span class="sxs-lookup"><span data-stu-id="f03e3-128">0010 = 0.125f ( 2 / 16)</span></span>
-   <span data-ttu-id="f03e3-129">0011 = 0.1875 f (3/16)</span><span class="sxs-lookup"><span data-stu-id="f03e3-129">0011 = 0.1875f ( 3 / 16)</span></span>
-   <span data-ttu-id="f03e3-130">0100 = 0,25 f (4/16)</span><span class="sxs-lookup"><span data-stu-id="f03e3-130">0100 = 0.25f ( 4 / 16)</span></span>
-   <span data-ttu-id="f03e3-131">0101 = 0.3125 f (5/16)</span><span class="sxs-lookup"><span data-stu-id="f03e3-131">0101 = 0.3125f ( 5 / 16)</span></span>
-   <span data-ttu-id="f03e3-132">0110 = 0.375 f (6/16)</span><span class="sxs-lookup"><span data-stu-id="f03e3-132">0110 = 0.375f ( 6 / 16)</span></span>
-   <span data-ttu-id="f03e3-133">0111 = 0.4375 f (7/16)</span><span class="sxs-lookup"><span data-stu-id="f03e3-133">0111 = 0.4375f ( 7 / 16)</span></span>

> [!Note]  
> <span data-ttu-id="f03e3-134">Los bordes izquierdo y superior de un píxel se incluyen en el desplazamiento; sin embargo, no se incluyen los bordes inferior y derecho.</span><span class="sxs-lookup"><span data-stu-id="f03e3-134">The left and top edges of a pixel are included in the offset; however, the bottom and right edges are not included.</span></span> <span data-ttu-id="f03e3-135">Se omiten todos los demás bits del entero de 32 bits y los valores de desplazamiento de V.</span><span class="sxs-lookup"><span data-stu-id="f03e3-135">All other bits in the 32-bit integer U and V offset values are ignored.</span></span>

 

<span data-ttu-id="f03e3-136">Una implementación puede tomar el desplazamiento proporcionado por el sombreador y obtener un valor de punto fijo de 32 bits completo (28,4), que abarca el intervalo válido, realizando el siguiente cálculo:</span><span class="sxs-lookup"><span data-stu-id="f03e3-136">An implementation can take the offset provided by the shader and obtain a full 32-bit fixed point value (28.4), which spans the valid range, by performing the following calculation:</span></span>


```
iU = (iU<<28)>>28  // keep lowest 4 bits and sign extend, which yields [-8..7]
```



<span data-ttu-id="f03e3-137">Si una implementación de debe asignar el desplazamiento a un desplazamiento de punto flotante, realiza el cálculo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f03e3-137">If an implementation must map the offset to a floating-point offset, it performs the following calculation:</span></span>


```
fU = ((float)iU)/16
```



### <a name="minimum-shader-model"></a><span data-ttu-id="f03e3-138">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="f03e3-138">Minimum Shader Model</span></span>

<span data-ttu-id="f03e3-139">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f03e3-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f03e3-140">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="f03e3-140">Shader Model</span></span>                                                                | <span data-ttu-id="f03e3-141">Compatible</span><span class="sxs-lookup"><span data-stu-id="f03e3-141">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="f03e3-142">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="f03e3-142">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="f03e3-143">sí</span><span class="sxs-lookup"><span data-stu-id="f03e3-143">yes</span></span>       |



 

<span data-ttu-id="f03e3-144">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="f03e3-144">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="f03e3-145">Vértice</span><span class="sxs-lookup"><span data-stu-id="f03e3-145">Vertex</span></span> | <span data-ttu-id="f03e3-146">Casco</span><span class="sxs-lookup"><span data-stu-id="f03e3-146">Hull</span></span> | <span data-ttu-id="f03e3-147">Dominio</span><span class="sxs-lookup"><span data-stu-id="f03e3-147">Domain</span></span> | <span data-ttu-id="f03e3-148">Geometría</span><span class="sxs-lookup"><span data-stu-id="f03e3-148">Geometry</span></span> | <span data-ttu-id="f03e3-149">Píxel</span><span class="sxs-lookup"><span data-stu-id="f03e3-149">Pixel</span></span> | <span data-ttu-id="f03e3-150">Compute</span><span class="sxs-lookup"><span data-stu-id="f03e3-150">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f03e3-151">x</span><span class="sxs-lookup"><span data-stu-id="f03e3-151">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="f03e3-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="f03e3-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f03e3-153">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="f03e3-153">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="f03e3-154">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f03e3-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




