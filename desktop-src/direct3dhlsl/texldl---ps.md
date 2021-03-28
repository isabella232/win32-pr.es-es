---
title: texldl-PS
description: Muestra una textura con una muestra determinada. Se debe especificar el nivel de detalle de los mapas de bits concreto que se muestra como el cuarto componente de la coordenada de textura. | texldl-PS
ms.assetid: f0ca8a1d-ac98-49ef-850a-c534e986c7ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6ab8a6f55ce5e069a01edb5d281bfe506c5fee6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986230"
---
# <a name="texldl---ps"></a><span data-ttu-id="de934-105">texldl-PS</span><span class="sxs-lookup"><span data-stu-id="de934-105">texldl - ps</span></span>

<span data-ttu-id="de934-106">Muestra una textura con una muestra determinada.</span><span class="sxs-lookup"><span data-stu-id="de934-106">Sample a texture with a particular sampler.</span></span> <span data-ttu-id="de934-107">Se debe especificar el nivel de detalle de los mapas de bits concreto que se muestra como el cuarto componente de la coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="de934-107">The particular mipmap level-of-detail being sampled has to be specified as the fourth component of the texture coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="de934-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de934-108">Syntax</span></span>



| <span data-ttu-id="de934-109">texldl DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="de934-109">texldl dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="de934-110">Donde:</span><span class="sxs-lookup"><span data-stu-id="de934-110">Where:</span></span>

-   <span data-ttu-id="de934-111">DST es un registro de destino.</span><span class="sxs-lookup"><span data-stu-id="de934-111">dst is a destination register.</span></span>
-   <span data-ttu-id="de934-112">src0 es un registro de origen que proporciona las coordenadas de textura para el ejemplo de textura.</span><span class="sxs-lookup"><span data-stu-id="de934-112">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="de934-113">Vea [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="de934-113">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="de934-114">SRC1 identifica los registros de la muestra de origen \# , donde \# especifica el número de muestra de textura que se muestra.</span><span class="sxs-lookup"><span data-stu-id="de934-114">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="de934-115">La muestra le ha asociado una textura y un estado de control definido por la enumeración [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (por ejemplo, D3DSAMP \_ MINFILTER).</span><span class="sxs-lookup"><span data-stu-id="de934-115">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (for example, D3DSAMP\_MINFILTER).</span></span>

## <a name="remarks"></a><span data-ttu-id="de934-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de934-116">Remarks</span></span>



| <span data-ttu-id="de934-117">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="de934-117">Pixel shader versions</span></span> | <span data-ttu-id="de934-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="de934-118">1\_1</span></span> | <span data-ttu-id="de934-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="de934-119">1\_2</span></span> | <span data-ttu-id="de934-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="de934-120">1\_3</span></span> | <span data-ttu-id="de934-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="de934-121">1\_4</span></span> | <span data-ttu-id="de934-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="de934-122">2\_0</span></span> | <span data-ttu-id="de934-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="de934-123">2\_x</span></span> | <span data-ttu-id="de934-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="de934-124">2\_sw</span></span> | <span data-ttu-id="de934-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="de934-125">3\_0</span></span> | <span data-ttu-id="de934-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="de934-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="de934-127">texldl</span><span class="sxs-lookup"><span data-stu-id="de934-127">texldl</span></span>                |      |      |      |      |      |      |       | <span data-ttu-id="de934-128">x</span><span class="sxs-lookup"><span data-stu-id="de934-128">x</span></span>    | <span data-ttu-id="de934-129">x</span><span class="sxs-lookup"><span data-stu-id="de934-129">x</span></span>     |



 

<span data-ttu-id="de934-130">texldl busca el conjunto de texturas en la fase de muestra a la que hace referencia SRC1.</span><span class="sxs-lookup"><span data-stu-id="de934-130">texldl looks up the texture set at the sampler stage referenced by src1.</span></span> <span data-ttu-id="de934-131">El nivel de detalle se selecciona de src0. w.</span><span class="sxs-lookup"><span data-stu-id="de934-131">The level-of-detail is selected from src0.w.</span></span> <span data-ttu-id="de934-132">Este valor puede ser negativo, en cuyo caso el nivel de detalle seleccionado es el inicial (el mapa más grande) con el MAGFILTER.</span><span class="sxs-lookup"><span data-stu-id="de934-132">This value can be negative in which case the level-of-detail selected is the zeroth one (biggest map) with the MAGFILTER.</span></span> <span data-ttu-id="de934-133">Dado que src0. w es un valor de punto flotante, el valor fraccionario se usa para interpolar (si MIPFILTER es lineal) entre dos niveles de MIP.</span><span class="sxs-lookup"><span data-stu-id="de934-133">Since src0.w is a floating point value, the fractional value is used to interpolate (if MIPFILTER is LINEAR) between two mip levels.</span></span> <span data-ttu-id="de934-134">Se respetan los Estados de muestra MIPMAPLODBIAS y MAXMIPLEVEL.</span><span class="sxs-lookup"><span data-stu-id="de934-134">Sampler states MIPMAPLODBIAS and MAXMIPLEVEL are honored.</span></span> <span data-ttu-id="de934-135">Para obtener más información sobre los Estados de muestra, vea [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="de934-135">For more information about sampler states, see [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="de934-136">Si un programa de sombreador muestrea desde una muestra que no tiene un conjunto de texturas, se obtiene 0001 en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="de934-136">If a shader program samples from a sampler that does not have a texture set, then 0001 is obtained in the destination register.</span></span>

<span data-ttu-id="de934-137">A continuación se muestra un algoritmo aproximado que sigue el dispositivo de referencia:</span><span class="sxs-lookup"><span data-stu-id="de934-137">The following is a rough algorithm that the reference device follows:</span></span>


```
LOD = src0.w + LODBIAS;
if (LOD <= 0 )
{
   LOD = 0;
   Filter = MagFilter;
   tex = Lookup( MAX(MAXMIPLEVEL, LOD), Filter );
}
else
{
   Filter = MinFilter;
   LOD = MAX( MAXMIPLEVEL, LOD );
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



<span data-ttu-id="de934-138">Restricciones:</span><span class="sxs-lookup"><span data-stu-id="de934-138">Restrictions:</span></span>

-   <span data-ttu-id="de934-139">Las coordenadas de textura no se deben escalar por tamaño de textura.</span><span class="sxs-lookup"><span data-stu-id="de934-139">The texture coordinates should not be scaled by texture size.</span></span>
-   <span data-ttu-id="de934-140">DST debe ser un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="de934-140">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="de934-141">DST puede aceptar un writemask.</span><span class="sxs-lookup"><span data-stu-id="de934-141">dst can accept a writemask.</span></span> <span data-ttu-id="de934-142">Consulte [máscara de escritura de registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span><span class="sxs-lookup"><span data-stu-id="de934-142">See [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>
-   <span data-ttu-id="de934-143">Los valores predeterminados de los componentes que faltan son 0 o 1 y dependen del formato de textura.</span><span class="sxs-lookup"><span data-stu-id="de934-143">Defaults for missing components are either 0 or 1, and depend on the texture format.</span></span>
-   <span data-ttu-id="de934-144">SRC1 debe ser una [muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# .</span><span class="sxs-lookup"><span data-stu-id="de934-144">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#).</span></span> <span data-ttu-id="de934-145">SRC1 no puede usar un modificador Negate (consulte [máscara de escritura de registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)).</span><span class="sxs-lookup"><span data-stu-id="de934-145">src1 may not use a negate modifier (see [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)).</span></span> <span data-ttu-id="de934-146">SRC1 puede usar swizzle (consulte [registro de origen permutación](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)), que se aplica después del muestreo, pero antes de que se respete la máscara de escritura (consulte máscara de escritura de registro de destino).</span><span class="sxs-lookup"><span data-stu-id="de934-146">src1 may use swizzle (see [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)), which is applied after sampling, but before the write mask (see Destination Register Write Mask) is honored.</span></span> <span data-ttu-id="de934-147">La muestra debe haberse declarado (mediante [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)) al principio del sombreador.</span><span class="sxs-lookup"><span data-stu-id="de934-147">The sampler must have been declared (using [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)) at the beginning of the shader.</span></span>
-   <span data-ttu-id="de934-148">El número de coordenadas necesarias para realizar el ejemplo de textura depende de cómo se declaró la muestra.</span><span class="sxs-lookup"><span data-stu-id="de934-148">The number of coordinates required to perform the texture sample depends on how the sampler was declared.</span></span> <span data-ttu-id="de934-149">Si se declaró como un cubo, se necesita una coordenada de textura de tres componentes (. RGB).</span><span class="sxs-lookup"><span data-stu-id="de934-149">If it was declared as a cube, a three-component texture coordinate is required (.rgb).</span></span> <span data-ttu-id="de934-150">La validación exige que las coordenadas proporcionadas a Tex \_ LDL sean suficientes para la dimensión de textura declarada para la muestra.</span><span class="sxs-lookup"><span data-stu-id="de934-150">Validation enforces that coordinates provided to tex\_ldl Are sufficient for the texture dimension declared for the sampler.</span></span> <span data-ttu-id="de934-151">Sin embargo, no se garantiza que la aplicación establezca realmente una textura (a través de la API) con dimensiones iguales a la dimensión declarada para la muestra.</span><span class="sxs-lookup"><span data-stu-id="de934-151">However, it is not guaranteed that the application actually sets a texture (through the API) with dimensions equal to the dimension declared for the sampler.</span></span> <span data-ttu-id="de934-152">En tal caso, el tiempo de ejecución intentará detectar discrepancias (posiblemente solo en depuración).</span><span class="sxs-lookup"><span data-stu-id="de934-152">In such a case, the runtime will attempt to detect mismatches (possibly in debug only).</span></span> <span data-ttu-id="de934-153">El muestreo de una textura con menos dimensiones que los que se encuentran en la coordenada de textura se permitirá y se asumirá que omite los componentes de coordenadas de textura adicionales.</span><span class="sxs-lookup"><span data-stu-id="de934-153">Sampling a texture with fewer dimensions than are present in the texture coordinate will be allowed and assumed to ignore the extra texture coordinate components.</span></span> <span data-ttu-id="de934-154">Por el contrario, el muestreo de una textura con más dimensiones que las que se encuentran en la coordenada de textura no es válido.</span><span class="sxs-lookup"><span data-stu-id="de934-154">Conversely, sampling a texture with more dimensions than are present in the texture coordinate is illegal.</span></span>
-   <span data-ttu-id="de934-155">Si el src0 (coordenada de textura) es un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md), los componentes necesarios para la búsqueda (descrita anteriormente) deben haberse escrito previamente.</span><span class="sxs-lookup"><span data-stu-id="de934-155">If the src0 (texture coordinate) is [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md), the components required for the lookup (described above) must have been previously written.</span></span>
-   <span data-ttu-id="de934-156">El muestreo de texturas RGB sin signo dará como resultado valores Float entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="de934-156">Sampling unsigned RGB textures will result in float values between 0.0 and 1.0.</span></span>
-   <span data-ttu-id="de934-157">Las texturas con signo de muestreo darán como resultado valores Float entre-1,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="de934-157">Sampling signed textures will result in float values between -1.0 to 1.0.</span></span>
-   <span data-ttu-id="de934-158">Al tomar muestras de texturas de punto flotante, Float16 significa que los datos se van a rangos dentro de \_ FLOAT16 máx.</span><span class="sxs-lookup"><span data-stu-id="de934-158">When sampling floating-point textures, Float16 means that the data will range within MAX\_FLOAT16.</span></span> <span data-ttu-id="de934-159">Float32 significa que se usará el intervalo máximo de la canalización.</span><span class="sxs-lookup"><span data-stu-id="de934-159">Float32 means the maximum range of the pipeline will be used.</span></span> <span data-ttu-id="de934-160">El muestreo fuera de cualquier intervalo está sin definir.</span><span class="sxs-lookup"><span data-stu-id="de934-160">Sampling outside of either range is undefined.</span></span>
-   <span data-ttu-id="de934-161">No hay ningún límite de lectura dependiente.</span><span class="sxs-lookup"><span data-stu-id="de934-161">There is no dependent read limit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de934-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="de934-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de934-163">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="de934-163">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
