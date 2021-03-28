---
title: texldl-vs
description: Muestra una textura con una muestra determinada. Se debe especificar el nivel de detalle de los mapas de bits concreto que se muestra como el cuarto componente de la coordenada de textura. | texldl-vs
ms.assetid: 774c058d-7b3e-46a9-adce-c9a44efefd78
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: be9240f5307bb1e70b1f10cc1e392b92e5833fd8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083638"
---
# <a name="texldl---vs"></a><span data-ttu-id="0a0b6-105">texldl-vs</span><span class="sxs-lookup"><span data-stu-id="0a0b6-105">texldl - vs</span></span>

<span data-ttu-id="0a0b6-106">Muestra una textura con una muestra determinada.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-106">Sample a texture with a particular sampler.</span></span> <span data-ttu-id="0a0b6-107">Se debe especificar el nivel de detalle de los mapas de bits concreto que se muestra como el cuarto componente de la coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-107">The particular mipmap level-of-detail being sampled has to be specified as the fourth component of the texture coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a0b6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a0b6-108">Syntax</span></span>



| <span data-ttu-id="0a0b6-109">texldl DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="0a0b6-109">texldl dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="0a0b6-110">Donde:</span><span class="sxs-lookup"><span data-stu-id="0a0b6-110">Where:</span></span>

-   <span data-ttu-id="0a0b6-111">DST es un registro de destino.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-111">dst is a destination register.</span></span>
-   <span data-ttu-id="0a0b6-112">src0 es un registro de origen que proporciona las coordenadas de textura para el ejemplo de textura.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-112">src0 is a source register that provides the texture coordinates for the texture sample.</span></span>
-   <span data-ttu-id="0a0b6-113">SRC1 identifica los registros de la muestra de origen \# , donde \# especifica el número de muestra de textura que se muestra.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-113">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="0a0b6-114">La muestra le ha asociado una textura y un estado de control definido por la enumeración [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (por ejemplo, D3DSAMP \_ MINFILTER).</span><span class="sxs-lookup"><span data-stu-id="0a0b6-114">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (for example, D3DSAMP\_MINFILTER).</span></span>

## <a name="remarks"></a><span data-ttu-id="0a0b6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a0b6-115">Remarks</span></span>



| <span data-ttu-id="0a0b6-116">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="0a0b6-116">Vertex shader versions</span></span> | <span data-ttu-id="0a0b6-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="0a0b6-117">1\_1</span></span> | <span data-ttu-id="0a0b6-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0a0b6-118">2\_0</span></span> | <span data-ttu-id="0a0b6-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0a0b6-119">2\_x</span></span> | <span data-ttu-id="0a0b6-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0a0b6-120">2\_sw</span></span> | <span data-ttu-id="0a0b6-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0a0b6-121">3\_0</span></span> | <span data-ttu-id="0a0b6-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0a0b6-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="0a0b6-123">texldl</span><span class="sxs-lookup"><span data-stu-id="0a0b6-123">texldl</span></span>                 |      |      |      |       | <span data-ttu-id="0a0b6-124">x</span><span class="sxs-lookup"><span data-stu-id="0a0b6-124">x</span></span>    | <span data-ttu-id="0a0b6-125">x</span><span class="sxs-lookup"><span data-stu-id="0a0b6-125">x</span></span>     |



 

<span data-ttu-id="0a0b6-126">texldl busca el conjunto de texturas en la fase de muestra a la que hace referencia SRC1.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-126">texldl looks up the texture set at the sampler stage referenced by src1.</span></span> <span data-ttu-id="0a0b6-127">El nivel de detalle se selecciona de src0. w.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-127">The level-of-detail is selected from src0.w.</span></span> <span data-ttu-id="0a0b6-128">Este valor puede ser negativo, en cuyo caso el nivel de detalle seleccionado es el "inicial uno" (el mapa más grande) con el MAGFILTER.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-128">This value can be negative, in which case the level-of-detail selected is the "zeroth one" (biggest map) with the MAGFILTER.</span></span> <span data-ttu-id="0a0b6-129">Dado que src0. w es un valor de punto flotante, el valor fraccionario se usa para interpolar (si MIPFILTER es lineal) entre dos niveles de MIP.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-129">Because src0.w is a floating point value, the fractional value is used to interpolate (if MIPFILTER is LINEAR) between two mip levels.</span></span> <span data-ttu-id="0a0b6-130">Se respetan los Estados de muestra MIPMAPLODBIAS y MAXMIPLEVEL.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-130">Sampler states MIPMAPLODBIAS and MAXMIPLEVEL are honored.</span></span> <span data-ttu-id="0a0b6-131">Para obtener más información sobre los Estados de muestra, vea [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="0a0b6-131">For more information about sampler states, see [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="0a0b6-132">Si un programa de sombreador muestrea desde una muestra que no tiene un conjunto de texturas, se obtiene 0001 en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-132">If a shader program samples from a sampler that does not have a texture set, 0001 is obtained in the destination register.</span></span>

<span data-ttu-id="0a0b6-133">Se trata de una aproximación al algoritmo de dispositivo de referencia.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-133">This is an approximation to the reference device algorithm.</span></span>


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
   LOD = MAX( MAXMIPLEVEL, LOD);
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



<span data-ttu-id="0a0b6-134">Restricciones:</span><span class="sxs-lookup"><span data-stu-id="0a0b6-134">Restrictions:</span></span>

-   <span data-ttu-id="0a0b6-135">Las coordenadas de textura no se deben escalar por tamaño de textura.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-135">The texture coordinates should not be scaled by texture size.</span></span>
-   <span data-ttu-id="0a0b6-136">DST debe ser un [registro temporal](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="0a0b6-136">dst must be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="0a0b6-137">DST puede aceptar una máscara de escritura.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-137">dst can accept a write mask.</span></span> <span data-ttu-id="0a0b6-138">Vea [enmascaramiento del registro de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).</span><span class="sxs-lookup"><span data-stu-id="0a0b6-138">See [Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).</span></span>
-   <span data-ttu-id="0a0b6-139">Los valores predeterminados de los componentes que faltan son 0 o 1 y dependen del formato de textura.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-139">Defaults for missing components are either 0 or 1, and depend on the texture format.</span></span>
-   <span data-ttu-id="0a0b6-140">SRC1 debe ser un [muestreador (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) \# .</span><span class="sxs-lookup"><span data-stu-id="0a0b6-140">src1 must be a [Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s\#).</span></span> <span data-ttu-id="0a0b6-141">SRC1 no puede usar un modificador Negate.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-141">src1 may not use a negate modifier.</span></span> <span data-ttu-id="0a0b6-142">SRC1 puede usar swizzle, que se aplica después del muestreo antes de que se respete la máscara de escritura.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-142">src1 may use swizzle, which is applied after sampling before the write mask is honored.</span></span> <span data-ttu-id="0a0b6-143">La muestra debe haberse declarado (mediante [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md)) al principio del sombreador.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-143">The sampler must have been declared (using [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md)) at the beginning of the shader.</span></span>
-   <span data-ttu-id="0a0b6-144">El número de coordenadas necesarias para realizar el ejemplo de textura depende de cómo se declaró la muestra.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-144">The number of coordinates required to perform the texture sample depends on how the sampler was declared.</span></span> <span data-ttu-id="0a0b6-145">Si se declaró como un cubo, se necesita una coordenada de textura de tres componentes (. RGB).</span><span class="sxs-lookup"><span data-stu-id="0a0b6-145">If it was declared as a cube, a three-component texture coordinate is required (.rgb).</span></span> <span data-ttu-id="0a0b6-146">La validación exige que las coordenadas proporcionadas a texldl sean suficientes para la dimensión de textura declarada para la muestra.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-146">Validation enforces that coordinates provided to texldl Are sufficient for the texture dimension declared for the sampler.</span></span> <span data-ttu-id="0a0b6-147">Sin embargo, no se garantiza que la aplicación establezca realmente una textura (a través de la API) con dimensiones iguales a la dimensión declarada para la muestra.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-147">However, it is not guaranteed that the application actually set a texture (through the API) with dimensions equal to the dimension declared for the sampler.</span></span> <span data-ttu-id="0a0b6-148">En tal caso, el tiempo de ejecución intentará detectar discrepancias (posiblemente solo en depuración).</span><span class="sxs-lookup"><span data-stu-id="0a0b6-148">In such a case, the runtime will attempt to detect mismatches (possibly in debug only).</span></span> <span data-ttu-id="0a0b6-149">Se permitirá el muestreo de una textura con menos dimensiones que las presentes en la coordenada de textura y se asumirá que omite los componentes de coordenadas de textura adicionales.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-149">Sampling a texture with fewer dimensions than are present in the texture coordinate will be allowed, and will be assumed to ignore the extra texture coordinate components.</span></span> <span data-ttu-id="0a0b6-150">Por el contrario, no se permite el muestreo de una textura con más dimensiones que las presentes en la coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-150">Conversely, sampling a texture with more dimensions than are present in the texture coordinate is not allowed.</span></span>
-   <span data-ttu-id="0a0b6-151">Si src0 (coordenada de textura) es un [registro temporal](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ), los componentes necesarios para la búsqueda (descrito anteriormente) deben haberse escrito previamente.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-151">If the src0 (texture coordinate) is a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#), the components required for the lookup (described above) must have been previously written.</span></span>
-   <span data-ttu-id="0a0b6-152">El muestreo de texturas RGB sin signo dará como resultado valores Float entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-152">Sampling unsigned RGB textures will result in float values between 0.0 and 1.0.</span></span>
-   <span data-ttu-id="0a0b6-153">Las texturas con signo de muestreo darán como resultado valores Float entre-1,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-153">Sampling signed textures will result in float values between -1.0 to 1.0.</span></span>
-   <span data-ttu-id="0a0b6-154">Al muestrear texturas de punto flotante, Float16 significa que los datos se van a rangos dentro de \_ FLOAT16 máx.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-154">When sampling floating point textures, Float16 means that the data will range within MAX\_FLOAT16.</span></span> <span data-ttu-id="0a0b6-155">Float32 significa que se usará el intervalo máximo de la canalización.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-155">Float32 means the maximum range of the pipeline will be used.</span></span> <span data-ttu-id="0a0b6-156">El muestreo fuera de cualquier intervalo está sin definir.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-156">Sampling outside of either range is undefined.</span></span>
-   <span data-ttu-id="0a0b6-157">No hay ningún límite de lectura dependiente.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-157">There is no dependent read limit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a0b6-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0a0b6-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a0b6-159">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="0a0b6-159">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
