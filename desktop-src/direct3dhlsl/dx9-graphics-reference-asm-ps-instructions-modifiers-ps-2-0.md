---
title: Modificadores para ps_2_0 y superiores
description: Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino. Obtenga información sobre los modificadores ps_2_0 y posteriores.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc8ed91f8e103ebbab7c43ffe53201f0e1d5dfcf
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989290"
---
# <a name="modifiers-for-ps_2_0-and-above"></a><span data-ttu-id="159c8-104">Modificadores para ps \_ 2 \_ 0 y superiores</span><span class="sxs-lookup"><span data-stu-id="159c8-104">Modifiers for ps\_2\_0 and Above</span></span>

<span data-ttu-id="159c8-105">Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="159c8-105">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

<span data-ttu-id="159c8-106">Esta sección contiene información de referencia para los modificadores de instrucción implementados por el sombreador de píxeles versión 2 \_ 0 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="159c8-106">This section contains reference information for the instruction modifiers implemented by pixel shader version 2\_0 and above.</span></span>



| <span data-ttu-id="159c8-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="159c8-107">Name</span></span>                                     | <span data-ttu-id="159c8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="159c8-108">Syntax</span></span>     | <span data-ttu-id="159c8-109">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="159c8-109">2\_0</span></span> | <span data-ttu-id="159c8-110">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="159c8-110">2\_x</span></span> | <span data-ttu-id="159c8-111">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="159c8-111">2\_sw</span></span> | <span data-ttu-id="159c8-112">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="159c8-112">3\_0</span></span> | <span data-ttu-id="159c8-113">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="159c8-113">3\_sw</span></span> |
|------------------------------------------|------------|------|------|-------|------|-------|
| [<span data-ttu-id="159c8-114">Centroide</span><span class="sxs-lookup"><span data-stu-id="159c8-114">Centroid</span></span>](#centroid)                    | <span data-ttu-id="159c8-115">\_Centroide</span><span class="sxs-lookup"><span data-stu-id="159c8-115">\_centroid</span></span> | <span data-ttu-id="159c8-116">x</span><span class="sxs-lookup"><span data-stu-id="159c8-116">x</span></span>    | <span data-ttu-id="159c8-117">x</span><span class="sxs-lookup"><span data-stu-id="159c8-117">x</span></span>    | <span data-ttu-id="159c8-118">x</span><span class="sxs-lookup"><span data-stu-id="159c8-118">x</span></span>     | <span data-ttu-id="159c8-119">x</span><span class="sxs-lookup"><span data-stu-id="159c8-119">x</span></span>    | <span data-ttu-id="159c8-120">x</span><span class="sxs-lookup"><span data-stu-id="159c8-120">x</span></span>     |
| [<span data-ttu-id="159c8-121">Precisión \_ parcial</span><span class="sxs-lookup"><span data-stu-id="159c8-121">Partial\_Precision</span></span>](#partial-precision) | <span data-ttu-id="159c8-122">\_Pp</span><span class="sxs-lookup"><span data-stu-id="159c8-122">\_pp</span></span>       | <span data-ttu-id="159c8-123">x</span><span class="sxs-lookup"><span data-stu-id="159c8-123">x</span></span>    | <span data-ttu-id="159c8-124">x</span><span class="sxs-lookup"><span data-stu-id="159c8-124">x</span></span>    | <span data-ttu-id="159c8-125">x</span><span class="sxs-lookup"><span data-stu-id="159c8-125">x</span></span>     | <span data-ttu-id="159c8-126">x</span><span class="sxs-lookup"><span data-stu-id="159c8-126">x</span></span>    | <span data-ttu-id="159c8-127">x</span><span class="sxs-lookup"><span data-stu-id="159c8-127">x</span></span>     |
| [<span data-ttu-id="159c8-128">Saturate</span><span class="sxs-lookup"><span data-stu-id="159c8-128">Saturate</span></span>](#saturate)                    | <span data-ttu-id="159c8-129">\_Sentado</span><span class="sxs-lookup"><span data-stu-id="159c8-129">\_sat</span></span>      | <span data-ttu-id="159c8-130">x</span><span class="sxs-lookup"><span data-stu-id="159c8-130">x</span></span>    | <span data-ttu-id="159c8-131">x</span><span class="sxs-lookup"><span data-stu-id="159c8-131">x</span></span>    | <span data-ttu-id="159c8-132">x</span><span class="sxs-lookup"><span data-stu-id="159c8-132">x</span></span>     | <span data-ttu-id="159c8-133">x</span><span class="sxs-lookup"><span data-stu-id="159c8-133">x</span></span>    | <span data-ttu-id="159c8-134">x</span><span class="sxs-lookup"><span data-stu-id="159c8-134">x</span></span>     |



 

## <a name="centroid"></a><span data-ttu-id="159c8-135">Centroide</span><span class="sxs-lookup"><span data-stu-id="159c8-135">Centroid</span></span>

<span data-ttu-id="159c8-136">El modificador centroide es un modificador opcional que fija la interpolación de atributos dentro del intervalo de la primitiva cuando un centro de píxeles de varias muestras no está cubierto por la primitiva.</span><span class="sxs-lookup"><span data-stu-id="159c8-136">The centroid modifier is an optional modifier that clamps attribute interpolation within the range of the primitive when a multisample pixel center is not covered by the primitive.</span></span> <span data-ttu-id="159c8-137">Esto se puede ver en [Muestreo de centroide.](https://msdn.microsoft.com/library/ee415231(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="159c8-137">This can be seen in [Centroid Sampling](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).</span></span>

<span data-ttu-id="159c8-138">Puede aplicar el modificador centroide a una instrucción de ensamblado como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="159c8-138">You can apply the centroid modifier to an assembly instruction as shown here:</span></span>


```
dcl_texcoord0_centroid v0
```



<span data-ttu-id="159c8-139">También puede aplicar el modificador centroide a una semántica, como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="159c8-139">You can also apply the centroid modifier to a semantic as shown here:</span></span>


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



<span data-ttu-id="159c8-140">Además, cualquier [registro de color de](dx9-graphics-reference-asm-ps-registers-input-color.md) entrada (v ) declarado con una semántica de color se aplicará \# automáticamente.</span><span class="sxs-lookup"><span data-stu-id="159c8-140">In addition, any [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) declared with a color semantic will automatically have centroid applied.</span></span> <span data-ttu-id="159c8-141">No se garantiza que los degradados calculados a partir de atributos muestreados en centroide sean precisos.</span><span class="sxs-lookup"><span data-stu-id="159c8-141">Gradients computed from attributes that are centroid sampled are not guaranteed to be accurate.</span></span>

## <a name="partial-precision"></a><span data-ttu-id="159c8-142">Precisión parcial</span><span class="sxs-lookup"><span data-stu-id="159c8-142">Partial Precision</span></span>

<span data-ttu-id="159c8-143">El modificador de instrucción de precisión parcial (pp) indica las áreas en las que la precisión parcial es aceptable, siempre que \_ la implementación subyacente lo admita.</span><span class="sxs-lookup"><span data-stu-id="159c8-143">The partial precision instruction modifier (\_pp) indicates areas where partial precision is acceptable, provided that the underlying implementation supports it.</span></span> <span data-ttu-id="159c8-144">Las implementaciones siempre pueden omitir el modificador y realizar las operaciones afectadas con precisión completa.</span><span class="sxs-lookup"><span data-stu-id="159c8-144">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="159c8-145">El \_ modificador pp puede producirse en dos contextos:</span><span class="sxs-lookup"><span data-stu-id="159c8-145">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="159c8-146">En una declaración de coordenadas de textura para permitir pasar coordenadas de textura al sombreador de píxeles en forma de precisión parcial.</span><span class="sxs-lookup"><span data-stu-id="159c8-146">On a texture coordinate declaration to enable passing texture coordinates to the pixel shader in partial-precision form.</span></span> <span data-ttu-id="159c8-147">Esto permite, por ejemplo, el uso de coordenadas de textura para retransmitir datos de color al sombreador de píxeles, que puede ser más rápido con precisión parcial que con precisión completa en algunas implementaciones.</span><span class="sxs-lookup"><span data-stu-id="159c8-147">This allows, for example, the use of texture coordinates to relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span> <span data-ttu-id="159c8-148">En ausencia de este modificador, las coordenadas de textura se deben pasar con precisión completa.</span><span class="sxs-lookup"><span data-stu-id="159c8-148">In the absence of this modifier, texture coordinates must be passed in full precision.</span></span>
-   <span data-ttu-id="159c8-149">En cualquier instrucción, incluidas las instrucciones de carga de textura.</span><span class="sxs-lookup"><span data-stu-id="159c8-149">On any instruction including texture load instructions.</span></span> <span data-ttu-id="159c8-150">Esto indica que la implementación puede ejecutar la instrucción con precisión parcial y almacenar un resultado de precisión parcial.</span><span class="sxs-lookup"><span data-stu-id="159c8-150">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial precision result.</span></span> <span data-ttu-id="159c8-151">En ausencia de un modificador explícito, la instrucción debe realizarse con precisión completa (independientemente de la precisión de entrada).</span><span class="sxs-lookup"><span data-stu-id="159c8-151">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the input precision).</span></span>

<span data-ttu-id="159c8-152">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="159c8-152">Examples:</span></span>


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a><span data-ttu-id="159c8-153">Saturar</span><span class="sxs-lookup"><span data-stu-id="159c8-153">Saturate</span></span>

<span data-ttu-id="159c8-154">El modificador de instrucción saturada (sat) satura (o fija) el resultado de la instrucción en el intervalo \_ 0, 1 antes de escribir en el \[ \] registro de destino.</span><span class="sxs-lookup"><span data-stu-id="159c8-154">The saturate instruction modifier (\_sat) saturates (or clamps) the instruction result to the range \[0, 1\] before writing to the destination register.</span></span>

<span data-ttu-id="159c8-155">El modificador de instrucción sat se puede usar con cualquier instrucción excepto \_ [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md)y cualquier instrucción de \* texas.</span><span class="sxs-lookup"><span data-stu-id="159c8-155">The \_sat instruction modifier can be used with any instruction except [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md), and any tex\* instructions.</span></span>

<span data-ttu-id="159c8-156">Para ps \_ 2 \_ 0, ps 2 x y \_ ps \_ \_ 2 \_ sw, \_ [](dx9-graphics-reference-asm-ps-registers-output-color.md) [](dx9-graphics-reference-asm-ps-registers-output-depth.md)el modificador de instrucción sat no se puede usar con instrucciones que escriban en ningún registro de salida (Registro de color de salida o Registro de profundidad de salida).</span><span class="sxs-lookup"><span data-stu-id="159c8-156">For ps\_2\_0, ps\_2\_x, and ps\_2\_sw, the \_sat instruction modifier cannot be used with instructions writing to any output registers ([Output Color Register](dx9-graphics-reference-asm-ps-registers-output-color.md) or [Output Depth Register](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span></span> <span data-ttu-id="159c8-157">Esta restricción no se aplica a ps \_ 3 \_ 0 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="159c8-157">This restriction does not apply to ps\_3\_0 and above.</span></span>

<span data-ttu-id="159c8-158">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="159c8-158">Example:</span></span>


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a><span data-ttu-id="159c8-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="159c8-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="159c8-160">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="159c8-160">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




