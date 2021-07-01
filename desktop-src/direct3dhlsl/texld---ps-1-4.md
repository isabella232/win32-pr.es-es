---
title: 'ld: ps_1_4'
description: Carga el registro de destino con datos de color (RGBA) muestreados mediante el contenido del registro de origen como coordenadas de textura. La textura muestreada es la textura asociada al número de registro de destino.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d956d9176a6356dc3837ee4f4d13b5bb700dda98
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118830"
---
# <a name="texld---ps_1_4"></a><span data-ttu-id="a3cb7-104">ld- ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="a3cb7-104">texld - ps\_1\_4</span></span>

<span data-ttu-id="a3cb7-105">Carga el registro de destino con datos de color (RGBA) muestreados mediante el contenido del registro de origen como coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-105">Loads the destination register with color data (RGBA) sampled using the contents of the source register as texture coordinates.</span></span> <span data-ttu-id="a3cb7-106">La textura muestreada es la textura asociada al número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-106">The sampled texture is the texture associated with the destination register number.</span></span>



| <span data-ttu-id="a3cb7-107">ld dst, src</span><span class="sxs-lookup"><span data-stu-id="a3cb7-107">texld dst, src</span></span> |
|----------------|



 

## <a name="registers"></a><span data-ttu-id="a3cb7-108">Registros</span><span class="sxs-lookup"><span data-stu-id="a3cb7-108">Registers</span></span>



| <span data-ttu-id="a3cb7-109">Valor</span><span class="sxs-lookup"><span data-stu-id="a3cb7-109">Value</span></span>         | <span data-ttu-id="a3cb7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3cb7-110">Description</span></span>                     | <span data-ttu-id="a3cb7-111">Vn</span><span class="sxs-lookup"><span data-stu-id="a3cb7-111">vₙ</span></span>        | <span data-ttu-id="a3cb7-112">Cn</span><span class="sxs-lookup"><span data-stu-id="a3cb7-112">cₙ</span></span>  | <span data-ttu-id="a3cb7-113">Tn</span><span class="sxs-lookup"><span data-stu-id="a3cb7-113">tₙ</span></span>  | <span data-ttu-id="a3cb7-114">Rn</span><span class="sxs-lookup"><span data-stu-id="a3cb7-114">rₙ</span></span>  | <span data-ttu-id="a3cb7-115">Versión del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="a3cb7-115">Pixel shader version</span></span>              |
|----------|----------------------|-----------|-----|-----|-----|--------------|
| <span data-ttu-id="a3cb7-116">dst</span><span class="sxs-lookup"><span data-stu-id="a3cb7-116">dst</span></span>      | <span data-ttu-id="a3cb7-117">Registro de destino</span><span class="sxs-lookup"><span data-stu-id="a3cb7-117">Destination register</span></span> |           |     |     | <span data-ttu-id="a3cb7-118">x</span><span class="sxs-lookup"><span data-stu-id="a3cb7-118">x</span></span>   | <span data-ttu-id="a3cb7-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="a3cb7-119">1\_4</span></span>         |
| <span data-ttu-id="a3cb7-120">src</span><span class="sxs-lookup"><span data-stu-id="a3cb7-120">src</span></span>      | <span data-ttu-id="a3cb7-121">Registro de origen</span><span class="sxs-lookup"><span data-stu-id="a3cb7-121">Source register</span></span>      |           |     | <span data-ttu-id="a3cb7-122">x</span><span class="sxs-lookup"><span data-stu-id="a3cb7-122">x</span></span>   |     | <span data-ttu-id="a3cb7-123">1 \_ 4 fase 1</span><span class="sxs-lookup"><span data-stu-id="a3cb7-123">1\_4 phase 1</span></span> |
|          |                      |           |     | <span data-ttu-id="a3cb7-124">x</span><span class="sxs-lookup"><span data-stu-id="a3cb7-124">x</span></span>   | <span data-ttu-id="a3cb7-125">x</span><span class="sxs-lookup"><span data-stu-id="a3cb7-125">x</span></span>   | <span data-ttu-id="a3cb7-126">1 \_ fase 4</span><span class="sxs-lookup"><span data-stu-id="a3cb7-126">1\_4 phase</span></span>   |



 

<span data-ttu-id="a3cb7-127">Cuando se usa r(n) como registro de origen, los tres primeros componentes (XYZ) se deben haber inicializado en la fase anterior del sombreador.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-127">When using r(n) as a source register, the first three components (XYZ) must have been initialized in the previous phase of the shader.</span></span>

<span data-ttu-id="a3cb7-128">Para más información sobre los registros, [consulte ps \_ 1 \_ 1 ps \_ \_ \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="a3cb7-128">To learn more about registers, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a3cb7-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3cb7-129">Remarks</span></span>

<span data-ttu-id="a3cb7-130">Esta instrucción muestrea la textura en la fase de textura asociada al número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-130">This instruction samples the texture in the texture stage associated with the destination register number.</span></span> <span data-ttu-id="a3cb7-131">La textura se muestrea mediante datos de coordenadas de textura del registro de origen.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-131">The texture is sampled using texture coordinate data from the source register.</span></span>

<span data-ttu-id="a3cb7-132">La sintaxis de las instrucciones regld y texcrd expone compatibilidad con una división projective con un modificador de registro de textura.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-132">The syntax for the texld and texcrd instructions expose support for a projective divide with a Texture Register Modifier.</span></span> <span data-ttu-id="a3cb7-133">Para la versión 1.4 del sombreador de píxeles, la marca de transformación de textura D3DTTFF \_ PROJECTED siempre se omite.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-133">For pixel shader version 1.4, the D3DTTFF\_PROJECTED texture transform flag is always ignored.</span></span>

<span data-ttu-id="a3cb7-134">Reglas para usar regld:</span><span class="sxs-lookup"><span data-stu-id="a3cb7-134">Rules for using texld:</span></span>

1.  <span data-ttu-id="a3cb7-135">El mismo modificador .xyz o .xyw debe aplicarse a todas las lecturas de un registro t(n) individual dentro de las instrucciones de tipo texcrd old.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-135">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within both texcrd or texld instructions.</span></span> <span data-ttu-id="a3cb7-136">Si se usa .xyw en lecturas de registro t(n), se puede mezclar con otras lecturas del mismo registro t(n) mediante .xyw \_ dw.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-136">If .xyw is being used on t(n) register reads, this can be mixed with other reads of the same t(n) register using .xyw\_dw.</span></span>
2.  <span data-ttu-id="a3cb7-137">El modificador de origen de modificadores sólo es válido en regld con el registro de \_ origen r(n) (por lo tanto, solo en la fase 2).</span><span class="sxs-lookup"><span data-stu-id="a3cb7-137">The \_dz source modifier is only valid on texld with r(n) source register (thus phase 2 only).</span></span>
3.  <span data-ttu-id="a3cb7-138">El \_ modificador de origen de color no se puede usar más de dos veces por sombreador.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-138">The \_dz source modifier may be used no more than two times per shader.</span></span>



| <span data-ttu-id="a3cb7-139">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="a3cb7-139">Pixel shader versions</span></span> | <span data-ttu-id="a3cb7-140">1\_1</span><span class="sxs-lookup"><span data-stu-id="a3cb7-140">1\_1</span></span> | <span data-ttu-id="a3cb7-141">1\_2</span><span class="sxs-lookup"><span data-stu-id="a3cb7-141">1\_2</span></span> | <span data-ttu-id="a3cb7-142">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a3cb7-142">1\_3</span></span> | <span data-ttu-id="a3cb7-143">1\_4</span><span class="sxs-lookup"><span data-stu-id="a3cb7-143">1\_4</span></span> | <span data-ttu-id="a3cb7-144">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a3cb7-144">2\_0</span></span> | <span data-ttu-id="a3cb7-145">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a3cb7-145">2\_x</span></span> | <span data-ttu-id="a3cb7-146">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="a3cb7-146">2\_sw</span></span> | <span data-ttu-id="a3cb7-147">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a3cb7-147">3\_0</span></span> | <span data-ttu-id="a3cb7-148">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="a3cb7-148">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a3cb7-149">ld</span><span class="sxs-lookup"><span data-stu-id="a3cb7-149">texld</span></span>                 |      |      |      | <span data-ttu-id="a3cb7-150">x</span><span class="sxs-lookup"><span data-stu-id="a3cb7-150">x</span></span>    |      |      |       |      |       |



 

## <a name="examples"></a><span data-ttu-id="a3cb7-151">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a3cb7-151">Examples</span></span>

<span data-ttu-id="a3cb7-152">La instrucciónld ofrece cierto control sobre qué componentes de los datos de coordenadas de textura de origen se usan.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-152">The texld instruction offers some control over which components of the source texture coordinate data are used.</span></span> <span data-ttu-id="a3cb7-153">El conjunto completo de sintaxis permitida para las combinaciones de máscaras de escritura e incluye todos los modificadores de registro de origen, selectores y combinaciones de máscara de escritura válidos.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-153">The complete set of allowed syntax for texld follows, and includes all valid source register modifiers, selectors, and write mask combinations.</span></span>


```
texld  r(m), t(n).xyz
// Uses xyz from t(n) to sample 1D, 2D, or 3D texture
```




```
texld  r(m), t(n)
// Same as previous
```




```
texld  r(m), t(n).xyw
// Uses xyw (skipping z) from t(n) to sample 1D, 2D or 3D texture
```




```
texld  r(m), t(n)_dw.xyw  
// Samples 1D or 2D texture at x/w, y/w from t(n). The result
// is undefined for a cube-map lookup.
```




```
texld  r(m), r(n).xyz
// Samples 1D, 2D, or 3D texture at xyz from r(m) 
// This is possible in the second phase of the shader
```




```
texld  r(m), r(n)
// Same as previous
```




```
texld  r(m), r(n)_dz.xyz
// Samples 1D or 2D texture at x/z, y/z from r(m)
// Possible only in second phase
// The result is undefined for a cube-map lookup
```




```
texld  r(n), r(n)_dz
// Same as previous
```



## <a name="related-topics"></a><span data-ttu-id="a3cb7-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3cb7-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3cb7-155">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="a3cb7-155">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




