---
title: Getdimensions ((objeto de textura de HLSL de DirectX)
description: Obtiene la información de tamaño de la textura. El bloque de sintaxis muestra todos los parámetros que son posibles en la declaración del método. En la tabla de la sección comentarios se muestran los parámetros que se implementan para cada tipo de objeto de textura.
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ad4be68049c92955c5ddb06a0c5eccfe2c26b77
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904282"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a><span data-ttu-id="d112c-105">Getdimensions ((objeto de textura de HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="d112c-105">GetDimensions (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="d112c-106">Obtiene la información de tamaño de la textura.</span><span class="sxs-lookup"><span data-stu-id="d112c-106">Gets texture size information.</span></span> <span data-ttu-id="d112c-107">El bloque de sintaxis muestra todos los parámetros que son posibles en la declaración del método.</span><span class="sxs-lookup"><span data-stu-id="d112c-107">The syntax block shows all the parameters that are possible in the method declaration.</span></span> <span data-ttu-id="d112c-108">En la tabla de la sección comentarios se muestran los parámetros que se implementan para cada tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="d112c-108">The table in the Remarks section shows which parameters are implemented for each texture-object type.</span></span>



|                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d112c-109">void Object. Getdimensions ((UINT MipLevel, typeX width, typeX height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples);</span><span class="sxs-lookup"><span data-stu-id="d112c-109">void Object.GetDimensions( UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples );</span></span> |



 

<span data-ttu-id="d112c-110">typeX denota que hay dos tipos posibles: **uint** o **float**.</span><span class="sxs-lookup"><span data-stu-id="d112c-110">typeX denotes that there are two possible types: **uint** or **float**.</span></span>

## <a name="parameters"></a><span data-ttu-id="d112c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d112c-111">Parameters</span></span>



| <span data-ttu-id="d112c-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="d112c-112">Item</span></span>                                                                                                                               | <span data-ttu-id="d112c-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="d112c-113">Description</span></span>                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d112c-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*</span><span class="sxs-lookup"><span data-stu-id="d112c-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/>                                     | <span data-ttu-id="d112c-115">Cualquier tipo [de objeto de textura,](dx-graphics-hlsl-to-type.md) excepto un objeto de **búfer** .</span><span class="sxs-lookup"><span data-stu-id="d112c-115">Any [texture-object](dx-graphics-hlsl-to-type.md) type except a **Buffer** object.</span></span><br/>                                       |
| <span data-ttu-id="d112c-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span><span class="sxs-lookup"><span data-stu-id="d112c-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span></span><br/>                             | <span data-ttu-id="d112c-117">\[en \] un índice de base cero que identifica el nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="d112c-117">\[in\] A zero-based index that identifies the mipmap level.</span></span> <span data-ttu-id="d112c-118">Si no se usa este argumento, se supone el primer nivel de MIP.</span><span class="sxs-lookup"><span data-stu-id="d112c-118">If this argument is not used, the first mip level is assumed.</span></span><br/> |
| <span data-ttu-id="d112c-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Ancho*</span><span class="sxs-lookup"><span data-stu-id="d112c-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Width*</span></span><br/>                                         | <span data-ttu-id="d112c-120">\[\]el ancho de la textura, en textura.</span><span class="sxs-lookup"><span data-stu-id="d112c-120">\[out\] The texture width, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="d112c-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Alto*</span><span class="sxs-lookup"><span data-stu-id="d112c-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Height*</span></span><br/>                                     | <span data-ttu-id="d112c-122">\[\]el alto de la textura, en textura.</span><span class="sxs-lookup"><span data-stu-id="d112c-122">\[out\] The texture height, in texels.</span></span><br/>                                                                                    |
| <span data-ttu-id="d112c-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elemento*</span><span class="sxs-lookup"><span data-stu-id="d112c-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elements*</span></span><br/>                             | <span data-ttu-id="d112c-124">\[\]el número de elementos de una matriz.</span><span class="sxs-lookup"><span data-stu-id="d112c-124">\[out\] The number of elements in an array.</span></span><br/>                                                                               |
| <span data-ttu-id="d112c-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Amplia*</span><span class="sxs-lookup"><span data-stu-id="d112c-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Depth*</span></span><br/>                                         | <span data-ttu-id="d112c-126">\[\]profundidad de textura, en textura.</span><span class="sxs-lookup"><span data-stu-id="d112c-126">\[out\] The texture depth, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="d112c-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span><span class="sxs-lookup"><span data-stu-id="d112c-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span></span><br/>     | <span data-ttu-id="d112c-128">\[\]el número de niveles de mipmap.</span><span class="sxs-lookup"><span data-stu-id="d112c-128">\[out\] The number of mipmap levels.</span></span><br/>                                                                                      |
| <span data-ttu-id="d112c-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span><span class="sxs-lookup"><span data-stu-id="d112c-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span></span><br/> | <span data-ttu-id="d112c-130">\[\]el número de muestras.</span><span class="sxs-lookup"><span data-stu-id="d112c-130">\[out\] The number of samples.</span></span><br/>                                                                                            |



 

## <a name="return-value"></a><span data-ttu-id="d112c-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d112c-131">Return Value</span></span>

<span data-ttu-id="d112c-132">None</span><span class="sxs-lookup"><span data-stu-id="d112c-132">None</span></span>

## <a name="overloaded-methods"></a><span data-ttu-id="d112c-133">Métodos sobrecargados</span><span class="sxs-lookup"><span data-stu-id="d112c-133">Overloaded Methods</span></span>

<span data-ttu-id="d112c-134">En esta tabla se enumeran todas las versiones diferentes del método; las versiones difieren en función del número de parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="d112c-134">This table lists all the different versions of the method; versions differs by the number of input parameters.</span></span> <span data-ttu-id="d112c-135">Observe que para cada método que toma parámetros de entero, hay un método sobrecargado que toma parámetros de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="d112c-135">Notice that for every method that takes integer parameters, there is an overloaded method that takes floating-point parameters.</span></span>



| <span data-ttu-id="d112c-136">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="d112c-136">Texture-Object Type</span></span> | <span data-ttu-id="d112c-137">Parámetros de entrada</span><span class="sxs-lookup"><span data-stu-id="d112c-137">Input Parameters</span></span>                                                               |
|---------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="d112c-138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d112c-138">Texture1D</span></span>           | <span data-ttu-id="d112c-139">UINT MipLevel, UINT width, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d112c-139">UINT MipLevel, UINT Width, UINT NumberOfLevels</span></span>                                 |
| <span data-ttu-id="d112c-140">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d112c-140">Texture1D</span></span>           | <span data-ttu-id="d112c-141">Ancho de UINT</span><span class="sxs-lookup"><span data-stu-id="d112c-141">UINT Width</span></span>                                                                     |
| <span data-ttu-id="d112c-142">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d112c-142">Texture1D</span></span>           | <span data-ttu-id="d112c-143">UINT MipLevel, ancho flotante, Float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d112c-143">UINT MipLevel, float Width, float NumberOfLevels</span></span>                               |
| <span data-ttu-id="d112c-144">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d112c-144">Texture1D</span></span>           | <span data-ttu-id="d112c-145">Ancho flotante</span><span class="sxs-lookup"><span data-stu-id="d112c-145">float Width</span></span>                                                                    |
| <span data-ttu-id="d112c-146">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d112c-146">Texture1DArray</span></span>      | <span data-ttu-id="d112c-147">UINT MipLevel, UINT width, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d112c-147">UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="d112c-148">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d112c-148">Texture1DArray</span></span>      | <span data-ttu-id="d112c-149">UINT width, elementos UINT</span><span class="sxs-lookup"><span data-stu-id="d112c-149">UINT Width, UINT Elements</span></span>                                                      |
| <span data-ttu-id="d112c-150">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d112c-150">Texture1DArray</span></span>      | <span data-ttu-id="d112c-151">UINT MipLevel, ancho flotante, elementos Float, Float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d112c-151">UINT MipLevel, float Width, float Elements, float NumberOfLevels</span></span>               |
| <span data-ttu-id="d112c-152">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d112c-152">Texture1DArray</span></span>      | <span data-ttu-id="d112c-153">Ancho flotante, elementos Float</span><span class="sxs-lookup"><span data-stu-id="d112c-153">float Width, float Elements</span></span>                                                    |
| <span data-ttu-id="d112c-154">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d112c-154">Texture2D</span></span>           | <span data-ttu-id="d112c-155">UINT MipLevel, UINT width, UINT height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d112c-155">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="d112c-156">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d112c-156">Texture2D</span></span>           | <span data-ttu-id="d112c-157">UINT width, alto de UINT</span><span class="sxs-lookup"><span data-stu-id="d112c-157">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="d112c-158">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d112c-158">Texture2D</span></span>           | <span data-ttu-id="d112c-159">UINT MipLevel, ancho flotante, alto Float, Float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d112c-159">UINT MipLevel, float Width, float Height, float NumberOfLevels</span></span>                 |
| <span data-ttu-id="d112c-160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d112c-160">Texture2D</span></span>           | <span data-ttu-id="d112c-161">Ancho flotante, alto flotante</span><span class="sxs-lookup"><span data-stu-id="d112c-161">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="d112c-162">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d112c-162">Texture2DArray</span></span>      | <span data-ttu-id="d112c-163">UINT MipLevel, UINT width, UINT height, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d112c-163">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="d112c-164">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d112c-164">Texture2DArray</span></span>      | <span data-ttu-id="d112c-165">UINT width, UINT height, UINT (elementos)</span><span class="sxs-lookup"><span data-stu-id="d112c-165">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="d112c-166">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d112c-166">Texture2DArray</span></span>      | <span data-ttu-id="d112c-167">UINT MipLevel, ancho flotante, alto Float, elementos Float, Float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d112c-167">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="d112c-168">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d112c-168">Texture2DArray</span></span>      | <span data-ttu-id="d112c-169">Ancho flotante, alto flotante, elementos Float</span><span class="sxs-lookup"><span data-stu-id="d112c-169">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="d112c-170">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d112c-170">Texture3D</span></span>           | <span data-ttu-id="d112c-171">UINT MipLevel, UINT width, UINT height, UINT Depth, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d112c-171">UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels</span></span>        |
| <span data-ttu-id="d112c-172">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d112c-172">Texture3D</span></span>           | <span data-ttu-id="d112c-173">UINT width, UINT height, UINT Depth</span><span class="sxs-lookup"><span data-stu-id="d112c-173">UINT Width, UINT Height, UINT Depth</span></span>                                            |
| <span data-ttu-id="d112c-174">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d112c-174">Texture3D</span></span>           | <span data-ttu-id="d112c-175">UINT MipLevel, ancho flotante, alto flotante, profundidad Float, Float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d112c-175">UINT MipLevel, float Width, float Height, float Depth, float NumberOfLevels</span></span>    |
| <span data-ttu-id="d112c-176">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d112c-176">Texture3D</span></span>           | <span data-ttu-id="d112c-177">Ancho flotante, alto flotante, profundidad de punto flotante</span><span class="sxs-lookup"><span data-stu-id="d112c-177">float Width, float Height, float Depth</span></span>                                         |
| <span data-ttu-id="d112c-178">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d112c-178">TextureCube</span></span>         | <span data-ttu-id="d112c-179">UINT MipLevel, UINT width, UINT height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d112c-179">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="d112c-180">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d112c-180">TextureCube</span></span>         | <span data-ttu-id="d112c-181">UINT width, alto de UINT</span><span class="sxs-lookup"><span data-stu-id="d112c-181">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="d112c-182">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d112c-182">TextureCube</span></span>         | <span data-ttu-id="d112c-183">UINT MipLevel, ancho flotante, alto Float, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d112c-183">UINT MipLevel, float Width, float Height, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="d112c-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d112c-184">TextureCube</span></span>         | <span data-ttu-id="d112c-185">Ancho flotante, alto flotante</span><span class="sxs-lookup"><span data-stu-id="d112c-185">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="d112c-186">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d112c-186">TextureCubeArray</span></span>    | <span data-ttu-id="d112c-187">UINT MipLevel, UINT width, UINT height, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d112c-187">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="d112c-188">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d112c-188">TextureCubeArray</span></span>    | <span data-ttu-id="d112c-189">UINT width, UINT height, UINT (elementos)</span><span class="sxs-lookup"><span data-stu-id="d112c-189">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="d112c-190">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d112c-190">TextureCubeArray</span></span>    | <span data-ttu-id="d112c-191">UINT MipLevel, ancho flotante, alto Float, elementos Float, Float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d112c-191">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="d112c-192">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d112c-192">TextureCubeArray</span></span>    | <span data-ttu-id="d112c-193">Ancho flotante, alto flotante, elementos Float</span><span class="sxs-lookup"><span data-stu-id="d112c-193">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="d112c-194">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="d112c-194">Texture2DMS</span></span>         | <span data-ttu-id="d112c-195">UINT width, UINT height, UINT samples</span><span class="sxs-lookup"><span data-stu-id="d112c-195">UINT Width, UINT Height, UINT Samples</span></span>                                          |
| <span data-ttu-id="d112c-196">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="d112c-196">Texture2DMS</span></span>         | <span data-ttu-id="d112c-197">Ancho flotante, alto flotante, ejemplos Float</span><span class="sxs-lookup"><span data-stu-id="d112c-197">float Width, float Height, float Samples</span></span>                                       |
| <span data-ttu-id="d112c-198">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="d112c-198">Texture2DMSArray</span></span>    | <span data-ttu-id="d112c-199">UINT width, UINT height, UINT (elementos), ejemplos de UINT</span><span class="sxs-lookup"><span data-stu-id="d112c-199">UINT Width, UINT Height, UINT Elements, UINT Samples</span></span>                           |
| <span data-ttu-id="d112c-200">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="d112c-200">Texture2DMSArray</span></span>    | <span data-ttu-id="d112c-201">Ancho flotante, alto Float, elementos Float, ejemplos Float</span><span class="sxs-lookup"><span data-stu-id="d112c-201">float Width, float Height, float Elements, float Samples</span></span>                       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d112c-202">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="d112c-202">Minimum Shader Model</span></span>

<span data-ttu-id="d112c-203">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d112c-203">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d112c-204">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d112c-204">vs\_4\_0</span></span> | <span data-ttu-id="d112c-205">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d112c-205">vs\_4\_1</span></span>  | <span data-ttu-id="d112c-206">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d112c-206">ps\_4\_0</span></span> | <span data-ttu-id="d112c-207">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d112c-207">ps\_4\_1</span></span>  | <span data-ttu-id="d112c-208">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d112c-208">gs\_4\_0</span></span> | <span data-ttu-id="d112c-209">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d112c-209">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="d112c-210">x</span><span class="sxs-lookup"><span data-stu-id="d112c-210">x</span></span>        | <span data-ttu-id="d112c-211">x</span><span class="sxs-lookup"><span data-stu-id="d112c-211">x</span></span>         | <span data-ttu-id="d112c-212">x</span><span class="sxs-lookup"><span data-stu-id="d112c-212">x</span></span>        | <span data-ttu-id="d112c-213">x</span><span class="sxs-lookup"><span data-stu-id="d112c-213">x</span></span>         | <span data-ttu-id="d112c-214">x</span><span class="sxs-lookup"><span data-stu-id="d112c-214">x</span></span>        | <span data-ttu-id="d112c-215">x</span><span class="sxs-lookup"><span data-stu-id="d112c-215">x</span></span>         |



 

1.  <span data-ttu-id="d112c-216">Devuelve dimensiones para el nivel de mipmap más grande (inicial).</span><span class="sxs-lookup"><span data-stu-id="d112c-216">Returns dimensions for the largest (zeroth) mipmap level.</span></span>
2.  <span data-ttu-id="d112c-217">TextureCubeArray está disponible en el modelo de sombreador 4,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="d112c-217">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
3.  <span data-ttu-id="d112c-218">El modelo de sombreador 4,1 está disponible en Direct3D 10,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="d112c-218">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d112c-219">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d112c-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d112c-220">Texture-objeto</span><span class="sxs-lookup"><span data-stu-id="d112c-220">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





