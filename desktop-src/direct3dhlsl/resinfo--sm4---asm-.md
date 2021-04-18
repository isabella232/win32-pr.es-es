---
title: resinfo (SM4-ASM)
description: Consultar las dimensiones de un recurso de entrada determinado.
ms.assetid: 5D549AC6-E0CB-4395-953C-5E5ECEEE234D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a252195a4b59ed791f6ac625fe1d95bbd9925f1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419916"
---
# <a name="resinfo-sm4---asm"></a><span data-ttu-id="9665d-103">resinfo (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9665d-103">resinfo (sm4 - asm)</span></span>

<span data-ttu-id="9665d-104">Consultar las dimensiones de un recurso de entrada determinado.</span><span class="sxs-lookup"><span data-stu-id="9665d-104">Query the dimensions of a given input resource.</span></span>



| <span data-ttu-id="9665d-105">resinfo \[ \_ uint </span><span class="sxs-lookup"><span data-stu-id="9665d-105">resinfo\[\_uint</span></span>\|<span data-ttu-id="9665d-106">\_rcpFloat \] dest \[ . Mask \] , srcMipLevel. Select \_ componente, srcResource \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9665d-106">\_rcpFloat\] dest\[.mask\], srcMipLevel.select\_component, srcResource\[.swizzle\]</span></span> |
|-----------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="9665d-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="9665d-107">Item</span></span>                                                                                                               | <span data-ttu-id="9665d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="9665d-108">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9665d-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9665d-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="9665d-110">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="9665d-110">\[in\] The address of the result of the operation.</span></span><br/>                             |
| <span data-ttu-id="9665d-111"><span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*</span><span class="sxs-lookup"><span data-stu-id="9665d-111"><span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*</span></span><br/> | <span data-ttu-id="9665d-112">\[en \] el nivel de MIP.</span><span class="sxs-lookup"><span data-stu-id="9665d-112">\[in\] The mip level.</span></span><br/>                                                          |
| <span data-ttu-id="9665d-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="9665d-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="9665d-114">\[en \] una \# \# textura de entrada t o u para la que se consultan las dimensiones.</span><span class="sxs-lookup"><span data-stu-id="9665d-114">\[in\] A t\# or u\# input texture for which the dimensions are being queried.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="9665d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9665d-115">Remarks</span></span>

<span data-ttu-id="9665d-116">*srcMipLevel* se lee como un entero sin signo, por lo que se requiere un selector de componente único para el registro de origen, si no es un valor inmediato escalar.</span><span class="sxs-lookup"><span data-stu-id="9665d-116">*srcMipLevel* is read as an unsigned integer scalar so a single component selector is required for the source register, if it is not a scalar immediate value.</span></span>

<span data-ttu-id="9665d-117">*dest* recibe \[ el ancho, el alto, la profundidad o el tamaño de la matriz, total-MIP-Count \] , seleccionado por la máscara de escritura.</span><span class="sxs-lookup"><span data-stu-id="9665d-117">*dest* receives \[width, height, depth or array size, total-mip-count\], selected by the write mask.</span></span>

<span data-ttu-id="9665d-118">Los valores de ancho, alto y profundidad devueltos son para el nivel de MIP seleccionado por el parámetro *srcMipLevel* y están en el número de textura, independientemente del tamaño de los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="9665d-118">The returned width, height and depth values are for the mip-level selected by the *srcMipLevel* parameter, and are in number of texels, independent of texel data size.</span></span> <span data-ttu-id="9665d-119">En el caso de los recursos multiejemplo (texture2D \[ array \] MS \# ), el ancho y el alto también se devuelven en textura, no ejemplos.</span><span class="sxs-lookup"><span data-stu-id="9665d-119">For multisample resources (texture2D\[Array\]MS\#), width and height are also returned in texels, not samples.</span></span>

<span data-ttu-id="9665d-120">El número total de MIP devuelto en *dest. w* no se ve afectado por el parámetro *srcMipLevel* .</span><span class="sxs-lookup"><span data-stu-id="9665d-120">The total mip count returned in *dest.w* is unaffected by the *srcMipLevel* parameter.</span></span>

<span data-ttu-id="9665d-121">En el caso de UAVs (u \# ), el número de niveles de MIP es siempre 1.</span><span class="sxs-lookup"><span data-stu-id="9665d-121">For UAVs (u\#), the number of mip levels is always 1.</span></span>

<span data-ttu-id="9665d-122">Todos los aspectos de esta instrucción se basan en las características de la vista de recursos enlazadas a la t \# /u \# , no en el recurso base subyacente.</span><span class="sxs-lookup"><span data-stu-id="9665d-122">All aspects of this instruction are based on the characteristics of the resource view bound at the t\#/u\#, not the underlying base resource.</span></span>

<span data-ttu-id="9665d-123">Los valores devueltos son todos los puntos flotantes, a menos que \_ se use el modificador uint, en cuyo caso los valores devueltos son enteros.</span><span class="sxs-lookup"><span data-stu-id="9665d-123">Returned values are all floating point, unless the \_uint modifier is used, in which case the returned values are all integers.</span></span> <span data-ttu-id="9665d-124">Si \_ se usa el modificador rcpFloat, todos los valores devueltos son de punto flotante y el ancho, el alto y la profundidad se devuelven como recíprocos (1,0 f/width, 1,0 f/height, 1,0 f/Depth), incluido el archivo INF si width/Height/Depth son 0 del comportamiento de *srcMipLevel* fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="9665d-124">If the \_rcpFloat modifier is used, all returned values are floating point, and the width, height and depth are returned as reciprocals (1.0f/width, 1.0f/height, 1.0f/depth), including INF if width/height/depth are 0 from out-of-range *srcMipLevel* behavior.</span></span> <span data-ttu-id="9665d-125">El \_ modificador rcpFloat solo se aplica a los valores de ancho, alto y profundidad devueltos, y no se aplica a los valores establecidos en 0 y, por tanto, no se devuelven, y tampoco se aplica a las devoluciones de tamaño de matriz.</span><span class="sxs-lookup"><span data-stu-id="9665d-125">The \_rcpFloat modifier only applies to width, height, and depth returned values and does not apply to values that are set to 0 and thus not returned, and also does not apply to array size returns.</span></span>

<span data-ttu-id="9665d-126">Swizzle en *srcResource* permite que los valores devueltos se swizzled arbitrariamente antes de que se escriban en el destino.</span><span class="sxs-lookup"><span data-stu-id="9665d-126">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="9665d-127">Si *srcResource* es Texture1D, el ancho se devuelve en *dest. x* y *dest. YZ* se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="9665d-127">If *srcResource* is a Texture1D, then width is returned in *dest.x*, and *dest.yz* are set to 0.</span></span>

<span data-ttu-id="9665d-128">Si *srcResource* es un Texture1DArray, se devuelve el ancho en *dest. x*, el tamaño de la matriz se devuelve en *dest. y* y *dest. z* se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="9665d-128">If *srcResource* is a Texture1DArray, then width is returned in *dest.x*, the array size is returned in *dest.y*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="9665d-129">Si *srcResource* es Texture2D, el ancho y el alto se devuelven en *dest. XY* y *dest. z* se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="9665d-129">If *srcResource* is a Texture2D, then width and height are returned in *dest.xy*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="9665d-130">Si *srcResource* es un Texture2DArray, el ancho y el alto se devuelven en *dest. XY* y el tamaño de la matriz se devuelve en *dest. z*.</span><span class="sxs-lookup"><span data-stu-id="9665d-130">If *srcResource* is a Texture2DArray, then width and height are returned in *dest.xy*, and the array size is returned in *dest.z*.</span></span>

<span data-ttu-id="9665d-131">Si *srcResource* es Texture3D, el ancho, el alto y la profundidad se devuelven en *dest.XYZ*.</span><span class="sxs-lookup"><span data-stu-id="9665d-131">If *srcResource* is a Texture3D, then width, height and depth are returned in *dest.xyz*.</span></span>

<span data-ttu-id="9665d-132">Si *srcResource* es un TextureCube, el ancho y el alto de las dimensiones del cubo individual se devuelven en *dest. XY* y *dest. z* se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="9665d-132">If *srcResource* is a TextureCube, then the width and height of the individual cube face dimensions are returned in *dest.xy*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="9665d-133">Si *srcResource* es TextureCubeArray, el ancho y el alto de las dimensiones de la superficie del cubo individual se devuelven en *dest. XY*.</span><span class="sxs-lookup"><span data-stu-id="9665d-133">If *srcResource* is a TextureCubeArray, then the width and height the individual cube face dimensions are returned in *dest.xy*.</span></span> <span data-ttu-id="9665d-134">*dest. z* se establece en un valor indefinido.</span><span class="sxs-lookup"><span data-stu-id="9665d-134">*dest.z* is set to an undefined value.</span></span>

<span data-ttu-id="9665d-135">Si se ha especificado una abrazadera de MIP por recurso en *srcResource*, resinfo siempre devuelve el número total de mapas de bits en la vista para el número de MIP, independientemente de la abrazadera.</span><span class="sxs-lookup"><span data-stu-id="9665d-135">If the a per-resource mip clamp has been specified on *srcResource*, resinfo always returns the total number of mipmaps in the view for the mip count, regardless of the clamp.</span></span> <span data-ttu-id="9665d-136">Sin embargo, si resinfo solicita las dimensiones de un miplevel determinado y se ha fijado el miplevel (por ejemplo, una abrazadera de 2,2 significa que se han fijado MIPS 0 y 1), las dimensiones devueltas no están definidas.</span><span class="sxs-lookup"><span data-stu-id="9665d-136">However, if the dimensions of a given miplevel are requested by resinfo and the miplevel has been clamped off (e.g. a clamp of 2.2 means that mips 0 and 1 have been clamped off), the dimensions returned are undefined.</span></span> <span data-ttu-id="9665d-137">Algunas implementaciones devolverán el comportamiento fuera del límite especificado para resinfo cuando el miplevel está fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="9665d-137">Some implementations will return the out of bounds behavior specified for resinfo when the miplevel is out of range.</span></span> <span data-ttu-id="9665d-138">Otras implementaciones devolverán las dimensiones de MIP como si no se hubieran fijado.</span><span class="sxs-lookup"><span data-stu-id="9665d-138">Other implementations will return the dimensions of the mip as if it had not been clamped.</span></span>

### <a name="restrictions"></a><span data-ttu-id="9665d-139">Restricciones</span><span class="sxs-lookup"><span data-stu-id="9665d-139">Restrictions</span></span>

-   <span data-ttu-id="9665d-140">*srcResource* debe ser un \# registro t o u \# que no sea un búfer, pero es una textura \* .</span><span class="sxs-lookup"><span data-stu-id="9665d-140">*srcResource* must be a t\# or u\# register that is not a Buffer, but is a Texture\*.</span></span>
-   <span data-ttu-id="9665d-141">No se permite el direccionamiento relativo de *srcResource* .</span><span class="sxs-lookup"><span data-stu-id="9665d-141">Relative addressing of *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="9665d-142">*srcMipLevel* debe usar un selector de componente único si no es un escalar inmediato.</span><span class="sxs-lookup"><span data-stu-id="9665d-142">*srcMipLevel* must use a single component selector if it is not a scalar immediate.</span></span>
-   <span data-ttu-id="9665d-143">La captura de t \# o u \# que no tiene nada enlazado devuelve 0 para width, height, Depth o tamaño y total-MIP-Count.</span><span class="sxs-lookup"><span data-stu-id="9665d-143">Fetching from t\# or u\# that has nothing bound to it returns 0 for width, height, depth or arraysize, and total-mip-count.</span></span> <span data-ttu-id="9665d-144">\_En este caso, se sigue respetando el modificador rcpFloat, con lo que se devuelve inf para los valores devueltos aplicables.</span><span class="sxs-lookup"><span data-stu-id="9665d-144">The \_rcpFloat modifier is still honored in this case, thus returning INF for the applicable returned values.</span></span>
-   <span data-ttu-id="9665d-145">Si *srcMipLevel* está fuera del intervalo del número de miplevels disponible en el recurso, el comportamiento de la devolución de tamaño (*dest.XYZ*) es idéntico al de un \# recurso t o u no enlazado \# .</span><span class="sxs-lookup"><span data-stu-id="9665d-145">If *srcMipLevel* is out of the range of the available number of miplevels in the resource, the behavior for the size return (*dest.xyz*) is identical to that of an unbound t\# or u\# resource.</span></span> <span data-ttu-id="9665d-146">El número total de MIP todavía se devuelve en *dest. w* para este caso.</span><span class="sxs-lookup"><span data-stu-id="9665d-146">The total mip count is still returned in *dest.w* for this case.</span></span>

<span data-ttu-id="9665d-147">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="9665d-147">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9665d-148">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="9665d-148">Vertex Shader</span></span> | <span data-ttu-id="9665d-149">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="9665d-149">Geometry Shader</span></span> | <span data-ttu-id="9665d-150">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="9665d-150">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9665d-151">x</span><span class="sxs-lookup"><span data-stu-id="9665d-151">x</span></span>             | <span data-ttu-id="9665d-152">x</span><span class="sxs-lookup"><span data-stu-id="9665d-152">x</span></span>               | <span data-ttu-id="9665d-153">x</span><span class="sxs-lookup"><span data-stu-id="9665d-153">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9665d-154">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="9665d-154">Minimum Shader Model</span></span>

<span data-ttu-id="9665d-155">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9665d-155">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9665d-156">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="9665d-156">Shader Model</span></span>                                              | <span data-ttu-id="9665d-157">Compatible</span><span class="sxs-lookup"><span data-stu-id="9665d-157">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9665d-158">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="9665d-158">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9665d-159">sí</span><span class="sxs-lookup"><span data-stu-id="9665d-159">yes</span></span>       |
| [<span data-ttu-id="9665d-160">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="9665d-160">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9665d-161">sí</span><span class="sxs-lookup"><span data-stu-id="9665d-161">yes</span></span>       |
| [<span data-ttu-id="9665d-162">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="9665d-162">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9665d-163">sí</span><span class="sxs-lookup"><span data-stu-id="9665d-163">yes</span></span>       |
| [<span data-ttu-id="9665d-164">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9665d-164">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9665d-165">no</span><span class="sxs-lookup"><span data-stu-id="9665d-165">no</span></span>        |
| [<span data-ttu-id="9665d-166">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9665d-166">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9665d-167">no</span><span class="sxs-lookup"><span data-stu-id="9665d-167">no</span></span>        |
| [<span data-ttu-id="9665d-168">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9665d-168">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9665d-169">no</span><span class="sxs-lookup"><span data-stu-id="9665d-169">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9665d-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9665d-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9665d-171">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9665d-171">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





