---
title: texm3x2depth-PS
description: Calcular el valor de profundidad que se va a usar en las pruebas de profundidad para este píxel.
ms.assetid: bacdd471-a6ee-4998-badd-93ffd4fd61d4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26d2c3efd1a31681520828b18d606d618d8c900a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983854"
---
# <a name="texm3x2depth---ps"></a><span data-ttu-id="4f0ce-103">texm3x2depth-PS</span><span class="sxs-lookup"><span data-stu-id="4f0ce-103">texm3x2depth - ps</span></span>

<span data-ttu-id="4f0ce-104">Calcular el valor de profundidad que se va a usar en las pruebas de profundidad para este píxel.</span><span class="sxs-lookup"><span data-stu-id="4f0ce-104">Calculate the depth value to be used in depth testing for this pixel.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f0ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f0ce-105">Syntax</span></span>



| <span data-ttu-id="4f0ce-106">texm3x2depth DST, src</span><span class="sxs-lookup"><span data-stu-id="4f0ce-106">texm3x2depth dst, src</span></span> |
|-----------------------|



 

<span data-ttu-id="4f0ce-107">, donde</span><span class="sxs-lookup"><span data-stu-id="4f0ce-107">where</span></span>

-   <span data-ttu-id="4f0ce-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="4f0ce-108">dst is the destination register.</span></span>
-   <span data-ttu-id="4f0ce-109">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="4f0ce-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f0ce-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f0ce-110">Remarks</span></span>



| <span data-ttu-id="4f0ce-111">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="4f0ce-111">Pixel shader versions</span></span> | <span data-ttu-id="4f0ce-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="4f0ce-112">1\_1</span></span> | <span data-ttu-id="4f0ce-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="4f0ce-113">1\_2</span></span> | <span data-ttu-id="4f0ce-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4f0ce-114">1\_3</span></span> | <span data-ttu-id="4f0ce-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="4f0ce-115">1\_4</span></span> | <span data-ttu-id="4f0ce-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4f0ce-116">2\_0</span></span> | <span data-ttu-id="4f0ce-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4f0ce-117">2\_x</span></span> | <span data-ttu-id="4f0ce-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4f0ce-118">2\_sw</span></span> | <span data-ttu-id="4f0ce-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4f0ce-119">3\_0</span></span> | <span data-ttu-id="4f0ce-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4f0ce-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="4f0ce-121">texm3x2depth</span><span class="sxs-lookup"><span data-stu-id="4f0ce-121">texm3x2depth</span></span>          |      |      | <span data-ttu-id="4f0ce-122">x</span><span class="sxs-lookup"><span data-stu-id="4f0ce-122">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="4f0ce-123">Esta instrucción debe usarse con la instrucción [texm3x2pad-PS](texm3x2pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="4f0ce-123">This instruction must be used with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

<span data-ttu-id="4f0ce-124">Al utilizar estas dos instrucciones, los registros de textura deben usar la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="4f0ce-124">When using these two instructions, texture registers must use the following sequence.</span></span>


```
 
tex t(n)                     // Define tn as a standard 3-vector.(tn must be 
                             // defined in some way before it is used
texm3x2pad   t(m),   t(n)    // Where m > n
                             // Calculate z value
texm3x2depth t(m+1), t(n)    // Calculate w value; use both z and w to
                             // find depth
```



<span data-ttu-id="4f0ce-125">El cálculo de profundidad se realiza después de usar una operación de producto punto para buscar z y w.</span><span class="sxs-lookup"><span data-stu-id="4f0ce-125">The depth calculation is done after using a dot product operation to find z and w.</span></span> <span data-ttu-id="4f0ce-126">Aquí encontrará más detalles sobre cómo se realiza el cálculo de profundidad.</span><span class="sxs-lookup"><span data-stu-id="4f0ce-126">Here is more detail about how the depth calculation is accomplished.</span></span>

<span data-ttu-id="4f0ce-127">La instrucción texm3x2pad calcula z.</span><span class="sxs-lookup"><span data-stu-id="4f0ce-127">The texm3x2pad instruction calculates z.</span></span>

<span data-ttu-id="4f0ce-128">z = TextureCoordinates (Stage m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="4f0ce-128">z = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="4f0ce-129">La instrucción texm3x2depth calcula w.</span><span class="sxs-lookup"><span data-stu-id="4f0ce-129">The texm3x2depth instruction calculates w.</span></span>

<span data-ttu-id="4f0ce-130">w = TextureCoordinates (fase m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="4f0ce-130">w = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="4f0ce-131">Calcule la profundidad y almacene el resultado en t (m + 1).</span><span class="sxs-lookup"><span data-stu-id="4f0ce-131">Calculate depth and store the result in t(m+1).</span></span>


```
 
if (w == 0)
  t(m+1) = 1.0
else
  t(m+1) = z/w
```



<span data-ttu-id="4f0ce-132">La profundidad calculada se etiqueta para usarse en la prueba de profundidad del píxel, reemplazando el valor de prueba de profundidad existente para el píxel.</span><span class="sxs-lookup"><span data-stu-id="4f0ce-132">The calculated depth is tagged to be used in the depth test for the pixel, replacing the existing depth test value for the pixel.</span></span>

<span data-ttu-id="4f0ce-133">Asegúrese de fijar z/w en el intervalo de (0-1).</span><span class="sxs-lookup"><span data-stu-id="4f0ce-133">Be sure to clamp z/w to be in the range of (0-1).</span></span> <span data-ttu-id="4f0ce-134">Si z/w está fuera de este intervalo, el resultado almacenado en el búfer de profundidad no estará definido.</span><span class="sxs-lookup"><span data-stu-id="4f0ce-134">If z/w is outside this range, the result stored in the depth buffer will be undefined.</span></span>

<span data-ttu-id="4f0ce-135">Después de ejecutar texm3x2depth, el registro t (m + 1) ya no está disponible para su uso en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="4f0ce-135">After running texm3x2depth, register t(m+1) is no longer available for use in the shader.</span></span>

<span data-ttu-id="4f0ce-136">Cuando se usa el muestreo múltiple, el uso de esta instrucción elimina la mayoría de las ventajas del búfer de profundidad de mayor resolución.</span><span class="sxs-lookup"><span data-stu-id="4f0ce-136">When multisampling, using this instruction eliminates most of the benefit of the higher resolution depth buffer.</span></span> <span data-ttu-id="4f0ce-137">Dado que el sombreador de píxeles se ejecuta una vez por píxel, se usará la salida de un solo valor de profundidad por texm3x2depth o [texdepth-PS](texdepth---ps.md) para cada una de las pruebas de comparación de profundidad de subpíxeles.</span><span class="sxs-lookup"><span data-stu-id="4f0ce-137">Because the pixel shader runs once per pixel, the single depth value output by texm3x2depth or [texdepth - ps](texdepth---ps.md) will be used for each of the subpixel depth comparison tests.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f0ce-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4f0ce-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f0ce-139">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="4f0ce-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




