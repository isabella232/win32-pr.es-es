---
title: texdepth-PS
description: Calcular los valores de profundidad que se van a usar en la prueba de comparación de búfer de profundidad para este píxel.
ms.assetid: f7128dbb-a5f3-4e95-b53b-7432439ae0c4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3eb5cd337108d08efee465c136adf1afb4921123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904278"
---
# <a name="texdepth---ps"></a><span data-ttu-id="d27cc-103">texdepth-PS</span><span class="sxs-lookup"><span data-stu-id="d27cc-103">texdepth - ps</span></span>

<span data-ttu-id="d27cc-104">Calcular los valores de profundidad que se van a usar en la prueba de comparación de búfer de profundidad para este píxel.</span><span class="sxs-lookup"><span data-stu-id="d27cc-104">Calculate depth values to be used in the depth buffer comparison test for this pixel.</span></span>

## <a name="syntax"></a><span data-ttu-id="d27cc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d27cc-105">Syntax</span></span>



| <span data-ttu-id="d27cc-106">texdepth DST</span><span class="sxs-lookup"><span data-stu-id="d27cc-106">texdepth dst</span></span> |
|--------------|



 

<span data-ttu-id="d27cc-107">, donde</span><span class="sxs-lookup"><span data-stu-id="d27cc-107">where</span></span>

-   <span data-ttu-id="d27cc-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="d27cc-108">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d27cc-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d27cc-109">Remarks</span></span>



| <span data-ttu-id="d27cc-110">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="d27cc-110">Pixel shader versions</span></span> | <span data-ttu-id="d27cc-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="d27cc-111">1\_1</span></span> | <span data-ttu-id="d27cc-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="d27cc-112">1\_2</span></span> | <span data-ttu-id="d27cc-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="d27cc-113">1\_3</span></span> | <span data-ttu-id="d27cc-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="d27cc-114">1\_4</span></span> | <span data-ttu-id="d27cc-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d27cc-115">2\_0</span></span> | <span data-ttu-id="d27cc-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d27cc-116">2\_x</span></span> | <span data-ttu-id="d27cc-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d27cc-117">2\_sw</span></span> | <span data-ttu-id="d27cc-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d27cc-118">3\_0</span></span> | <span data-ttu-id="d27cc-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d27cc-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="d27cc-120">texdepth</span><span class="sxs-lookup"><span data-stu-id="d27cc-120">texdepth</span></span>              |      |      |      | <span data-ttu-id="d27cc-121">x</span><span class="sxs-lookup"><span data-stu-id="d27cc-121">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="d27cc-122">Esta instrucción usa R5. r/R5. g en la prueba de comparación del búfer de profundidad para este píxel.</span><span class="sxs-lookup"><span data-stu-id="d27cc-122">This instruction uses r5.r / r5.g in the depth buffer comparison test for this pixel.</span></span> <span data-ttu-id="d27cc-123">Se omiten los datos de los canales azul y alfa.</span><span class="sxs-lookup"><span data-stu-id="d27cc-123">The data in the blue and alpha channels is ignored.</span></span> <span data-ttu-id="d27cc-124">Si R5. g = 0, el resultado de R5. r/R5. g = 1,0.</span><span class="sxs-lookup"><span data-stu-id="d27cc-124">If r5.g = 0, the result of r5.r / r5.g = 1.0.</span></span>

<span data-ttu-id="d27cc-125">El registro temporal R5 es el único registro que puede usar esta instrucción.</span><span class="sxs-lookup"><span data-stu-id="d27cc-125">Temporary register r5 is the only register that this instruction can use.</span></span>

<span data-ttu-id="d27cc-126">Después de ejecutar esta instrucción, el registro no temporal R5 no está disponible para su uso adicional en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="d27cc-126">After executing this instruction, temporary register r5 is unavailable for additional use in the shader.</span></span>

<span data-ttu-id="d27cc-127">Cuando se usa el muestreo múltiple, el uso de esta instrucción elimina la mayoría de las ventajas del búfer de profundidad de mayor resolución.</span><span class="sxs-lookup"><span data-stu-id="d27cc-127">When multisampling, using this instruction eliminates most of the benefit of the higher resolution depth buffer.</span></span> <span data-ttu-id="d27cc-128">Dado que el sombreador de píxeles se ejecuta una vez por píxel, se usará la salida de valor de profundidad único de [texm3x2depth-PS](texm3x2depth---ps.md) o texdepth para cada una de las pruebas de comparación de profundidad de subpíxeles.</span><span class="sxs-lookup"><span data-stu-id="d27cc-128">Because the pixel shader runs once per pixel, the single depth value output by [texm3x2depth - ps](texm3x2depth---ps.md) or texdepth will be used for each of the subpixel depth comparison tests.</span></span>

## <a name="examples"></a><span data-ttu-id="d27cc-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d27cc-129">Examples</span></span>

<span data-ttu-id="d27cc-130">Este es un ejemplo de uso de texdepth.</span><span class="sxs-lookup"><span data-stu-id="d27cc-130">Here is an example using texdepth.</span></span>


```
ps_1_4              
texld  r0, t0        // Sample texture from texture stage 0 (dest 
                     //   register number) into r0
                     // Use texture coordinate data from t0
texcrd r1.rgb, t1    // Load a second set of texture coordinate data into r1
add    r5.rg, r0, r1 // Add the two sets of texture coordinate data
phase                // Phase marker, required when using texdepth instruction
texdepth  r5         // Calculate pixel depth as r5.r / r5.g
                     // Do other color calculations with shader output r0
```



## <a name="related-topics"></a><span data-ttu-id="d27cc-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d27cc-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d27cc-132">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="d27cc-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




