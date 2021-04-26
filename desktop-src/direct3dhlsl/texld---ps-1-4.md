---
title: 'texld: ps_1_4'
description: Carga el registro de destino con datos de color (RGBA) muestreados utilizando el contenido del registro de origen como coordenadas de textura. La textura muestreada es la textura asociada al número de registro de destino.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca305b16db0f390354962a3e959f08b6e956f2ef
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996872"
---
# <a name="texld---ps_1_4"></a><span data-ttu-id="fe983-104">texld: ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="fe983-104">texld - ps\_1\_4</span></span>

<span data-ttu-id="fe983-105">Carga el registro de destino con datos de color (RGBA) muestreados utilizando el contenido del registro de origen como coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="fe983-105">Loads the destination register with color data (RGBA) sampled using the contents of the source register as texture coordinates.</span></span> <span data-ttu-id="fe983-106">La textura muestreada es la textura asociada al número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="fe983-106">The sampled texture is the texture associated with the destination register number.</span></span>



| <span data-ttu-id="fe983-107">texld dst, src</span><span class="sxs-lookup"><span data-stu-id="fe983-107">texld dst, src</span></span> |
|----------------|



 

## <a name="registers"></a><span data-ttu-id="fe983-108">Registros</span><span class="sxs-lookup"><span data-stu-id="fe983-108">Registers</span></span>



|          |                      | <span data-ttu-id="fe983-109">Vn</span><span class="sxs-lookup"><span data-stu-id="fe983-109">vₙ</span></span>        | <span data-ttu-id="fe983-110">Cn</span><span class="sxs-lookup"><span data-stu-id="fe983-110">cₙ</span></span>  | <span data-ttu-id="fe983-111">Tn</span><span class="sxs-lookup"><span data-stu-id="fe983-111">tₙ</span></span>  | <span data-ttu-id="fe983-112">Rn</span><span class="sxs-lookup"><span data-stu-id="fe983-112">rₙ</span></span>  |              |
|----------|----------------------|-----------|-----|-----|-----|--------------|
| <span data-ttu-id="fe983-113">dst</span><span class="sxs-lookup"><span data-stu-id="fe983-113">dst</span></span>      | <span data-ttu-id="fe983-114">Registro de destino</span><span class="sxs-lookup"><span data-stu-id="fe983-114">Destination register</span></span> |           |     |     | <span data-ttu-id="fe983-115">x</span><span class="sxs-lookup"><span data-stu-id="fe983-115">x</span></span>   | <span data-ttu-id="fe983-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="fe983-116">1\_4</span></span>         |
| <span data-ttu-id="fe983-117">src</span><span class="sxs-lookup"><span data-stu-id="fe983-117">src</span></span>      | <span data-ttu-id="fe983-118">Registro de origen</span><span class="sxs-lookup"><span data-stu-id="fe983-118">Source register</span></span>      |           |     | <span data-ttu-id="fe983-119">x</span><span class="sxs-lookup"><span data-stu-id="fe983-119">x</span></span>   |     | <span data-ttu-id="fe983-120">1 \_ 4 fase 1</span><span class="sxs-lookup"><span data-stu-id="fe983-120">1\_4 phase 1</span></span> |
|          |                      |           |     | <span data-ttu-id="fe983-121">x</span><span class="sxs-lookup"><span data-stu-id="fe983-121">x</span></span>   | <span data-ttu-id="fe983-122">x</span><span class="sxs-lookup"><span data-stu-id="fe983-122">x</span></span>   | <span data-ttu-id="fe983-123">1 \_ fase 4</span><span class="sxs-lookup"><span data-stu-id="fe983-123">1\_4 phase</span></span>   |



 

<span data-ttu-id="fe983-124">Cuando se usa r(n) como registro de origen, los tres primeros componentes (XYZ) se deben haber inicializado en la fase anterior del sombreador.</span><span class="sxs-lookup"><span data-stu-id="fe983-124">When using r(n) as a source register, the first three components (XYZ) must have been initialized in the previous phase of the shader.</span></span>

<span data-ttu-id="fe983-125">Para obtener más información sobre los registros, [vea ps \_ \_ 1 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="fe983-125">To learn more about registers, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe983-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fe983-126">Remarks</span></span>

<span data-ttu-id="fe983-127">Esta instrucción muestrea la textura en la fase de textura asociada al número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="fe983-127">This instruction samples the texture in the texture stage associated with the destination register number.</span></span> <span data-ttu-id="fe983-128">La textura se muestrea mediante datos de coordenadas de textura del registro de origen.</span><span class="sxs-lookup"><span data-stu-id="fe983-128">The texture is sampled using texture coordinate data from the source register.</span></span>

<span data-ttu-id="fe983-129">La sintaxis de las instrucciones texld y texcrd expone compatibilidad con una división projective con un modificador de registro de textura.</span><span class="sxs-lookup"><span data-stu-id="fe983-129">The syntax for the texld and texcrd instructions expose support for a projective divide with a Texture Register Modifier.</span></span> <span data-ttu-id="fe983-130">Para la versión 1.4 del sombreador de píxeles, la marca de transformación de textura PROJECTED de D3DTTFF \_ siempre se omite.</span><span class="sxs-lookup"><span data-stu-id="fe983-130">For pixel shader version 1.4, the D3DTTFF\_PROJECTED texture transform flag is always ignored.</span></span>

<span data-ttu-id="fe983-131">Reglas para usar texld:</span><span class="sxs-lookup"><span data-stu-id="fe983-131">Rules for using texld:</span></span>

1.  <span data-ttu-id="fe983-132">El mismo modificador .xyz o .xyw debe aplicarse a cada lectura de un registro t(n) individual dentro de las instrucciones de texcrd o texld.</span><span class="sxs-lookup"><span data-stu-id="fe983-132">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within both texcrd or texld instructions.</span></span> <span data-ttu-id="fe983-133">Si se usa .xyw en lecturas de registro t(n), se puede mezclar con otras lecturas del mismo registro t(n) mediante .xyw \_ dw.</span><span class="sxs-lookup"><span data-stu-id="fe983-133">If .xyw is being used on t(n) register reads, this can be mixed with other reads of the same t(n) register using .xyw\_dw.</span></span>
2.  <span data-ttu-id="fe983-134">El modificador de origen de tipo así solo es válido en el registro de origen \_ r(n) (por lo tanto, solo en la fase 2).</span><span class="sxs-lookup"><span data-stu-id="fe983-134">The \_dz source modifier is only valid on texld with r(n) source register (thus phase 2 only).</span></span>
3.  <span data-ttu-id="fe983-135">El \_ modificador de origen de color no se puede usar más de dos veces por sombreador.</span><span class="sxs-lookup"><span data-stu-id="fe983-135">The \_dz source modifier may be used no more than two times per shader.</span></span>



| <span data-ttu-id="fe983-136">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="fe983-136">Pixel shader versions</span></span> | <span data-ttu-id="fe983-137">1\_1</span><span class="sxs-lookup"><span data-stu-id="fe983-137">1\_1</span></span> | <span data-ttu-id="fe983-138">1\_2</span><span class="sxs-lookup"><span data-stu-id="fe983-138">1\_2</span></span> | <span data-ttu-id="fe983-139">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="fe983-139">1\_3</span></span> | <span data-ttu-id="fe983-140">1\_4</span><span class="sxs-lookup"><span data-stu-id="fe983-140">1\_4</span></span> | <span data-ttu-id="fe983-141">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fe983-141">2\_0</span></span> | <span data-ttu-id="fe983-142">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fe983-142">2\_x</span></span> | <span data-ttu-id="fe983-143">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="fe983-143">2\_sw</span></span> | <span data-ttu-id="fe983-144">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fe983-144">3\_0</span></span> | <span data-ttu-id="fe983-145">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="fe983-145">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="fe983-146">texld</span><span class="sxs-lookup"><span data-stu-id="fe983-146">texld</span></span>                 |      |      |      | <span data-ttu-id="fe983-147">x</span><span class="sxs-lookup"><span data-stu-id="fe983-147">x</span></span>    |      |      |       |      |       |



 

## <a name="examples"></a><span data-ttu-id="fe983-148">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fe983-148">Examples</span></span>

<span data-ttu-id="fe983-149">La instrucción texld ofrece cierto control sobre qué componentes de los datos de coordenadas de textura de origen se usan.</span><span class="sxs-lookup"><span data-stu-id="fe983-149">The texld instruction offers some control over which components of the source texture coordinate data are used.</span></span> <span data-ttu-id="fe983-150">El conjunto completo de sintaxis permitida para texld sigue e incluye todos los modificadores de registro de origen, selectores y combinaciones de máscara de escritura válidos.</span><span class="sxs-lookup"><span data-stu-id="fe983-150">The complete set of allowed syntax for texld follows, and includes all valid source register modifiers, selectors, and write mask combinations.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="fe983-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fe983-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe983-152">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="fe983-152">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




