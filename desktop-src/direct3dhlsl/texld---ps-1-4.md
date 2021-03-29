---
title: texld-ps_1_4
description: Carga el ejemplo de registro de destino con datos de color (RGBA) mediante el contenido del registro de origen como coordenadas de textura. La textura muestreada es la textura asociada al número de registro de destino.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 23827dffc396a40be134be4db3996d2e9f498288
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996940"
---
# <a name="texld---ps_1_4"></a><span data-ttu-id="a8ded-104">texld-PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="a8ded-104">texld - ps\_1\_4</span></span>

<span data-ttu-id="a8ded-105">Carga el ejemplo de registro de destino con datos de color (RGBA) mediante el contenido del registro de origen como coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="a8ded-105">Loads the destination register with color data (RGBA) sampled using the contents of the source register as texture coordinates.</span></span> <span data-ttu-id="a8ded-106">La textura muestreada es la textura asociada al número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="a8ded-106">The sampled texture is the texture associated with the destination register number.</span></span>



| <span data-ttu-id="a8ded-107">texld DST, src</span><span class="sxs-lookup"><span data-stu-id="a8ded-107">texld dst, src</span></span> |
|----------------|



 

## <a name="registers"></a><span data-ttu-id="a8ded-108">Registros</span><span class="sxs-lookup"><span data-stu-id="a8ded-108">Registers</span></span>



| <span data-ttu-id="a8ded-109">Argumento</span><span class="sxs-lookup"><span data-stu-id="a8ded-109">Argument</span></span> | <span data-ttu-id="a8ded-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8ded-110">Description</span></span>          | <span data-ttu-id="a8ded-111">Registros</span><span class="sxs-lookup"><span data-stu-id="a8ded-111">Registers</span></span> |     |     |     | <span data-ttu-id="a8ded-112">Versión</span><span class="sxs-lookup"><span data-stu-id="a8ded-112">Version</span></span>      |
|----------|----------------------|-----------|-----|-----|-----|--------------|
|          |                      | <span data-ttu-id="a8ded-113">vn</span><span class="sxs-lookup"><span data-stu-id="a8ded-113">vₙ</span></span>        | <span data-ttu-id="a8ded-114">CN</span><span class="sxs-lookup"><span data-stu-id="a8ded-114">cₙ</span></span>  | <span data-ttu-id="a8ded-115">TN</span><span class="sxs-lookup"><span data-stu-id="a8ded-115">tₙ</span></span>  | <span data-ttu-id="a8ded-116">RN</span><span class="sxs-lookup"><span data-stu-id="a8ded-116">rₙ</span></span>  |              |
| <span data-ttu-id="a8ded-117">DST</span><span class="sxs-lookup"><span data-stu-id="a8ded-117">dst</span></span>      | <span data-ttu-id="a8ded-118">Registro de destino</span><span class="sxs-lookup"><span data-stu-id="a8ded-118">Destination register</span></span> |           |     |     | <span data-ttu-id="a8ded-119">x</span><span class="sxs-lookup"><span data-stu-id="a8ded-119">x</span></span>   | <span data-ttu-id="a8ded-120">1\_4</span><span class="sxs-lookup"><span data-stu-id="a8ded-120">1\_4</span></span>         |
| <span data-ttu-id="a8ded-121">src</span><span class="sxs-lookup"><span data-stu-id="a8ded-121">src</span></span>      | <span data-ttu-id="a8ded-122">Registro de origen</span><span class="sxs-lookup"><span data-stu-id="a8ded-122">Source register</span></span>      |           |     | <span data-ttu-id="a8ded-123">x</span><span class="sxs-lookup"><span data-stu-id="a8ded-123">x</span></span>   |     | <span data-ttu-id="a8ded-124">1 \_ 4 fase 1</span><span class="sxs-lookup"><span data-stu-id="a8ded-124">1\_4 phase 1</span></span> |
|          |                      |           |     | <span data-ttu-id="a8ded-125">x</span><span class="sxs-lookup"><span data-stu-id="a8ded-125">x</span></span>   | <span data-ttu-id="a8ded-126">x</span><span class="sxs-lookup"><span data-stu-id="a8ded-126">x</span></span>   | <span data-ttu-id="a8ded-127">1 \_ 4 fase</span><span class="sxs-lookup"><span data-stu-id="a8ded-127">1\_4 phase</span></span>   |



 

<span data-ttu-id="a8ded-128">Al usar r (n) como registro de origen, los tres primeros componentes (XYZ) deben haberse inicializado en la fase anterior del sombreador.</span><span class="sxs-lookup"><span data-stu-id="a8ded-128">When using r(n) as a source register, the first three components (XYZ) must have been initialized in the previous phase of the shader.</span></span>

<span data-ttu-id="a8ded-129">Para obtener más información acerca de los registros, consulte [PS 1 \_ \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="a8ded-129">To learn more about registers, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a8ded-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8ded-130">Remarks</span></span>

<span data-ttu-id="a8ded-131">Esta instrucción muestrea la textura en la fase de textura asociada al número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="a8ded-131">This instruction samples the texture in the texture stage associated with the destination register number.</span></span> <span data-ttu-id="a8ded-132">La textura se muestrea utilizando los datos de coordenadas de textura del registro de origen.</span><span class="sxs-lookup"><span data-stu-id="a8ded-132">The texture is sampled using texture coordinate data from the source register.</span></span>

<span data-ttu-id="a8ded-133">La sintaxis de las instrucciones texld y texcrd expone la compatibilidad con una división proyectada con un modificador de registro de textura.</span><span class="sxs-lookup"><span data-stu-id="a8ded-133">The syntax for the texld and texcrd instructions expose support for a projective divide with a Texture Register Modifier.</span></span> <span data-ttu-id="a8ded-134">Para el sombreador de píxeles versión 1,4, la \_ marca de transformación de textura proyectada D3DTTFF siempre se omite.</span><span class="sxs-lookup"><span data-stu-id="a8ded-134">For pixel shader version 1.4, the D3DTTFF\_PROJECTED texture transform flag is always ignored.</span></span>

<span data-ttu-id="a8ded-135">Reglas para usar texld:</span><span class="sxs-lookup"><span data-stu-id="a8ded-135">Rules for using texld:</span></span>

1.  <span data-ttu-id="a8ded-136">Se debe aplicar el mismo modificador. XYZ o. xyw a cada lectura de un registro t (n) individual en las instrucciones texcrd o texld.</span><span class="sxs-lookup"><span data-stu-id="a8ded-136">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within both texcrd or texld instructions.</span></span> <span data-ttu-id="a8ded-137">Si se usa. xyw en las lecturas de registro t (n), esto se puede mezclar con otras lecturas del mismo registro t (n) mediante el almacenamiento de xyw. \_</span><span class="sxs-lookup"><span data-stu-id="a8ded-137">If .xyw is being used on t(n) register reads, this can be mixed with other reads of the same t(n) register using .xyw\_dw.</span></span>
2.  <span data-ttu-id="a8ded-138">El \_ modificador de origen DZ solo es válido en texld con el registro de origen r (n) (solo en la fase 2).</span><span class="sxs-lookup"><span data-stu-id="a8ded-138">The \_dz source modifier is only valid on texld with r(n) source register (thus phase 2 only).</span></span>
3.  <span data-ttu-id="a8ded-139">El \_ modificador de origen DZ no se puede usar más de dos veces por sombreador.</span><span class="sxs-lookup"><span data-stu-id="a8ded-139">The \_dz source modifier may be used no more than two times per shader.</span></span>



| <span data-ttu-id="a8ded-140">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="a8ded-140">Pixel shader versions</span></span> | <span data-ttu-id="a8ded-141">1\_1</span><span class="sxs-lookup"><span data-stu-id="a8ded-141">1\_1</span></span> | <span data-ttu-id="a8ded-142">1\_2</span><span class="sxs-lookup"><span data-stu-id="a8ded-142">1\_2</span></span> | <span data-ttu-id="a8ded-143">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a8ded-143">1\_3</span></span> | <span data-ttu-id="a8ded-144">1\_4</span><span class="sxs-lookup"><span data-stu-id="a8ded-144">1\_4</span></span> | <span data-ttu-id="a8ded-145">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a8ded-145">2\_0</span></span> | <span data-ttu-id="a8ded-146">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a8ded-146">2\_x</span></span> | <span data-ttu-id="a8ded-147">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a8ded-147">2\_sw</span></span> | <span data-ttu-id="a8ded-148">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a8ded-148">3\_0</span></span> | <span data-ttu-id="a8ded-149">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a8ded-149">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a8ded-150">texld</span><span class="sxs-lookup"><span data-stu-id="a8ded-150">texld</span></span>                 |      |      |      | <span data-ttu-id="a8ded-151">x</span><span class="sxs-lookup"><span data-stu-id="a8ded-151">x</span></span>    |      |      |       |      |       |



 

## <a name="examples"></a><span data-ttu-id="a8ded-152">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a8ded-152">Examples</span></span>

<span data-ttu-id="a8ded-153">La instrucción texld ofrece cierto control sobre qué componentes de los datos de coordenadas de textura de origen se usan.</span><span class="sxs-lookup"><span data-stu-id="a8ded-153">The texld instruction offers some control over which components of the source texture coordinate data are used.</span></span> <span data-ttu-id="a8ded-154">A continuación se muestra el conjunto completo de sintaxis permitida para texld e incluye todos los modificadores de registro de origen válidos, selectores y combinaciones de máscara de escritura.</span><span class="sxs-lookup"><span data-stu-id="a8ded-154">The complete set of allowed syntax for texld follows, and includes all valid source register modifiers, selectors, and write mask combinations.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a8ded-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8ded-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8ded-156">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="a8ded-156">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




