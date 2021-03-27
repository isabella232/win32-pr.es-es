---
title: Modificadores para ps_2_0 y versiones posteriores
description: Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7141576b80b7a05a3e61ee9a98fa36958b1d5530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903894"
---
# <a name="modifiers-for-ps_2_0-and-above"></a><span data-ttu-id="277c5-103">Modificadores para PS \_ 2 \_ 0 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="277c5-103">Modifiers for ps\_2\_0 and Above</span></span>

<span data-ttu-id="277c5-104">Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="277c5-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

<span data-ttu-id="277c5-105">Esta sección contiene información de referencia para los modificadores de instrucción implementados por el sombreador de píxeles versión 2 \_ 0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="277c5-105">This section contains reference information for the instruction modifiers implemented by pixel shader version 2\_0 and above.</span></span>



| <span data-ttu-id="277c5-106">Nombre</span><span class="sxs-lookup"><span data-stu-id="277c5-106">Name</span></span>                                     | <span data-ttu-id="277c5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="277c5-107">Syntax</span></span>     | <span data-ttu-id="277c5-108">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="277c5-108">2\_0</span></span> | <span data-ttu-id="277c5-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="277c5-109">2\_x</span></span> | <span data-ttu-id="277c5-110">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="277c5-110">2\_sw</span></span> | <span data-ttu-id="277c5-111">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="277c5-111">3\_0</span></span> | <span data-ttu-id="277c5-112">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="277c5-112">3\_sw</span></span> |
|------------------------------------------|------------|------|------|-------|------|-------|
| [<span data-ttu-id="277c5-113">Centroide</span><span class="sxs-lookup"><span data-stu-id="277c5-113">Centroid</span></span>](#centroid)                    | <span data-ttu-id="277c5-114">\_centroide</span><span class="sxs-lookup"><span data-stu-id="277c5-114">\_centroid</span></span> | <span data-ttu-id="277c5-115">x</span><span class="sxs-lookup"><span data-stu-id="277c5-115">x</span></span>    | <span data-ttu-id="277c5-116">x</span><span class="sxs-lookup"><span data-stu-id="277c5-116">x</span></span>    | <span data-ttu-id="277c5-117">x</span><span class="sxs-lookup"><span data-stu-id="277c5-117">x</span></span>     | <span data-ttu-id="277c5-118">x</span><span class="sxs-lookup"><span data-stu-id="277c5-118">x</span></span>    | <span data-ttu-id="277c5-119">x</span><span class="sxs-lookup"><span data-stu-id="277c5-119">x</span></span>     |
| [<span data-ttu-id="277c5-120">\_Precisión parcial</span><span class="sxs-lookup"><span data-stu-id="277c5-120">Partial\_Precision</span></span>](#partial-precision) | <span data-ttu-id="277c5-121">\_páginas</span><span class="sxs-lookup"><span data-stu-id="277c5-121">\_pp</span></span>       | <span data-ttu-id="277c5-122">x</span><span class="sxs-lookup"><span data-stu-id="277c5-122">x</span></span>    | <span data-ttu-id="277c5-123">x</span><span class="sxs-lookup"><span data-stu-id="277c5-123">x</span></span>    | <span data-ttu-id="277c5-124">x</span><span class="sxs-lookup"><span data-stu-id="277c5-124">x</span></span>     | <span data-ttu-id="277c5-125">x</span><span class="sxs-lookup"><span data-stu-id="277c5-125">x</span></span>    | <span data-ttu-id="277c5-126">x</span><span class="sxs-lookup"><span data-stu-id="277c5-126">x</span></span>     |
| [<span data-ttu-id="277c5-127">Saturate</span><span class="sxs-lookup"><span data-stu-id="277c5-127">Saturate</span></span>](#saturate)                    | <span data-ttu-id="277c5-128">\_sábado</span><span class="sxs-lookup"><span data-stu-id="277c5-128">\_sat</span></span>      | <span data-ttu-id="277c5-129">x</span><span class="sxs-lookup"><span data-stu-id="277c5-129">x</span></span>    | <span data-ttu-id="277c5-130">x</span><span class="sxs-lookup"><span data-stu-id="277c5-130">x</span></span>    | <span data-ttu-id="277c5-131">x</span><span class="sxs-lookup"><span data-stu-id="277c5-131">x</span></span>     | <span data-ttu-id="277c5-132">x</span><span class="sxs-lookup"><span data-stu-id="277c5-132">x</span></span>    | <span data-ttu-id="277c5-133">x</span><span class="sxs-lookup"><span data-stu-id="277c5-133">x</span></span>     |



 

## <a name="centroid"></a><span data-ttu-id="277c5-134">Centroide</span><span class="sxs-lookup"><span data-stu-id="277c5-134">Centroid</span></span>

<span data-ttu-id="277c5-135">El modificador centroide es un modificador opcional que fija la interpolación de atributos dentro del intervalo de la primitiva cuando un centro de píxeles de muestreo Multimuestra no está incluido en el primitivo.</span><span class="sxs-lookup"><span data-stu-id="277c5-135">The centroid modifier is an optional modifier that clamps attribute interpolation within the range of the primitive when a multisample pixel center is not covered by the primitive.</span></span> <span data-ttu-id="277c5-136">Esto puede verse en el [muestreo de centroide](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="277c5-136">This can be seen in [Centroid Sampling](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).</span></span>

<span data-ttu-id="277c5-137">Puede aplicar el modificador centroide a una instrucción de ensamblado como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="277c5-137">You can apply the centroid modifier to an assembly instruction as shown here:</span></span>


```
dcl_texcoord0_centroid v0
```



<span data-ttu-id="277c5-138">También puede aplicar el modificador centroide a una semántica como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="277c5-138">You can also apply the centroid modifier to a semantic as shown here:</span></span>


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



<span data-ttu-id="277c5-139">Además, cualquier [registro de color de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) declarado con una semántica de color se aplicará automáticamente a centroide.</span><span class="sxs-lookup"><span data-stu-id="277c5-139">In addition, any [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) declared with a color semantic will automatically have centroid applied.</span></span> <span data-ttu-id="277c5-140">No se garantiza que los degradados calculados a partir de los atributos que se centroide muestrean sean precisos.</span><span class="sxs-lookup"><span data-stu-id="277c5-140">Gradients computed from attributes that are centroid sampled are not guaranteed to be accurate.</span></span>

## <a name="partial-precision"></a><span data-ttu-id="277c5-141">Precisión parcial</span><span class="sxs-lookup"><span data-stu-id="277c5-141">Partial Precision</span></span>

<span data-ttu-id="277c5-142">El modificador de instrucciones de precisión parcial ( \_ PP) indica áreas en las que la precisión parcial es aceptable, siempre que la implementación subyacente la admita.</span><span class="sxs-lookup"><span data-stu-id="277c5-142">The partial precision instruction modifier (\_pp) indicates areas where partial precision is acceptable, provided that the underlying implementation supports it.</span></span> <span data-ttu-id="277c5-143">Las implementaciones siempre son gratuitas para omitir el modificador y realizar las operaciones afectadas con precisión completa.</span><span class="sxs-lookup"><span data-stu-id="277c5-143">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="277c5-144">El \_ modificador PP puede producirse en dos contextos:</span><span class="sxs-lookup"><span data-stu-id="277c5-144">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="277c5-145">En una declaración de coordenadas de textura para habilitar el paso de coordenadas de textura al sombreador de píxeles en formato de precisión parcial.</span><span class="sxs-lookup"><span data-stu-id="277c5-145">On a texture coordinate declaration to enable passing texture coordinates to the pixel shader in partial-precision form.</span></span> <span data-ttu-id="277c5-146">Esto permite, por ejemplo, el uso de coordenadas de textura para retransmitir datos de color al sombreador de píxeles, que puede ser más rápido con una precisión parcial que con precisión completa en algunas implementaciones.</span><span class="sxs-lookup"><span data-stu-id="277c5-146">This allows, for example, the use of texture coordinates to relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span> <span data-ttu-id="277c5-147">En ausencia de este modificador, las coordenadas de textura se deben pasar con precisión completa.</span><span class="sxs-lookup"><span data-stu-id="277c5-147">In the absence of this modifier, texture coordinates must be passed in full precision.</span></span>
-   <span data-ttu-id="277c5-148">En cualquier instrucción, incluidas las instrucciones de carga de textura.</span><span class="sxs-lookup"><span data-stu-id="277c5-148">On any instruction including texture load instructions.</span></span> <span data-ttu-id="277c5-149">Esto indica que la implementación puede ejecutar la instrucción con precisión parcial y almacenar un resultado de precisión parcial.</span><span class="sxs-lookup"><span data-stu-id="277c5-149">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial precision result.</span></span> <span data-ttu-id="277c5-150">En ausencia de un modificador explícito, la instrucción se debe realizar a plena precisión (independientemente de la precisión de entrada).</span><span class="sxs-lookup"><span data-stu-id="277c5-150">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the input precision).</span></span>

<span data-ttu-id="277c5-151">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="277c5-151">Examples:</span></span>


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a><span data-ttu-id="277c5-152">Saturar</span><span class="sxs-lookup"><span data-stu-id="277c5-152">Saturate</span></span>

<span data-ttu-id="277c5-153">El modificador de instrucciones saturadas ( \_ SAT) satura (o fija) el resultado de la instrucción en el intervalo de \[ 0 a 1 antes de \] escribir en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="277c5-153">The saturate instruction modifier (\_sat) saturates (or clamps) the instruction result to the range \[0, 1\] before writing to the destination register.</span></span>

<span data-ttu-id="277c5-154">El \_ modificador de instrucciones SAT se puede usar con cualquier instrucción excepto [FRC-PS](frc---ps.md), [sincos (-PS](sincos---ps.md)y cualquier instrucción Tex \* .</span><span class="sxs-lookup"><span data-stu-id="277c5-154">The \_sat instruction modifier can be used with any instruction except [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md), and any tex\* instructions.</span></span>

<span data-ttu-id="277c5-155">Para PS \_ 2 \_ 0, PS \_ 2 \_ x y PS \_ 2 \_ SW, \_ no se puede usar el modificador de instrucciones de SAT con instrucciones para escribir en los registros de salida (registro de[color de salida](dx9-graphics-reference-asm-ps-registers-output-color.md) o registro de [profundidad de salida](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span><span class="sxs-lookup"><span data-stu-id="277c5-155">For ps\_2\_0, ps\_2\_x, and ps\_2\_sw, the \_sat instruction modifier cannot be used with instructions writing to any output registers ([Output Color Register](dx9-graphics-reference-asm-ps-registers-output-color.md) or [Output Depth Register](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span></span> <span data-ttu-id="277c5-156">Esta restricción no se aplica a PS \_ 3 \_ 0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="277c5-156">This restriction does not apply to ps\_3\_0 and above.</span></span>

<span data-ttu-id="277c5-157">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="277c5-157">Example:</span></span>


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a><span data-ttu-id="277c5-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="277c5-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="277c5-159">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="277c5-159">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




