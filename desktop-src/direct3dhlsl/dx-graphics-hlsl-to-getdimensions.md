---
title: GetDimensions (objeto de textura HLSL de DirectX)
description: Obtiene información de tamaño de textura. El bloque de sintaxis muestra todos los parámetros que son posibles en la declaración del método. La tabla de la sección Comentarios muestra qué parámetros se implementan para cada tipo de objeto de textura.
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb6ef3c35af60ea776622718099acdedb5188ba8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119841"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a><span data-ttu-id="d0198-105">GetDimensions (objeto de textura HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="d0198-105">GetDimensions (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="d0198-106">Obtiene información de tamaño de textura.</span><span class="sxs-lookup"><span data-stu-id="d0198-106">Gets texture size information.</span></span> <span data-ttu-id="d0198-107">El bloque de sintaxis muestra todos los parámetros que son posibles en la declaración del método.</span><span class="sxs-lookup"><span data-stu-id="d0198-107">The syntax block shows all the parameters that are possible in the method declaration.</span></span> <span data-ttu-id="d0198-108">La tabla de la sección Comentarios muestra qué parámetros se implementan para cada tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="d0198-108">The table in the Remarks section shows which parameters are implemented for each texture-object type.</span></span>

<span data-ttu-id="d0198-109">void Object.GetDimensions( UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples );</span><span class="sxs-lookup"><span data-stu-id="d0198-109">void Object.GetDimensions( UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples );</span></span>



 

<span data-ttu-id="d0198-110">typeX indica que hay dos tipos posibles: **uint** o **float.**</span><span class="sxs-lookup"><span data-stu-id="d0198-110">typeX denotes that there are two possible types: **uint** or **float**.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0198-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0198-111">Parameters</span></span>



| <span data-ttu-id="d0198-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="d0198-112">Item</span></span>                                                                                                                               | <span data-ttu-id="d0198-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0198-113">Description</span></span>                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0198-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*</span><span class="sxs-lookup"><span data-stu-id="d0198-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/>                                     | <span data-ttu-id="d0198-115">Cualquier [tipo de objeto de textura,](dx-graphics-hlsl-to-type.md) excepto un objeto **Buffer.**</span><span class="sxs-lookup"><span data-stu-id="d0198-115">Any [texture-object](dx-graphics-hlsl-to-type.md) type except a **Buffer** object.</span></span><br/>                                       |
| <span data-ttu-id="d0198-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span><span class="sxs-lookup"><span data-stu-id="d0198-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span></span><br/>                             | <span data-ttu-id="d0198-117">\[en \] Un índice de base cero que identifica el nivel de mapa mip.</span><span class="sxs-lookup"><span data-stu-id="d0198-117">\[in\] A zero-based index that identifies the mipmap level.</span></span> <span data-ttu-id="d0198-118">Si no se usa este argumento, se asume el primer nivel de mip.</span><span class="sxs-lookup"><span data-stu-id="d0198-118">If this argument is not used, the first mip level is assumed.</span></span><br/> |
| <span data-ttu-id="d0198-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Ancho*</span><span class="sxs-lookup"><span data-stu-id="d0198-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Width*</span></span><br/>                                         | <span data-ttu-id="d0198-120">\[out \] Ancho de textura, en texturas.</span><span class="sxs-lookup"><span data-stu-id="d0198-120">\[out\] The texture width, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="d0198-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Altura*</span><span class="sxs-lookup"><span data-stu-id="d0198-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Height*</span></span><br/>                                     | <span data-ttu-id="d0198-122">\[out \] Alto de textura, en texturas.</span><span class="sxs-lookup"><span data-stu-id="d0198-122">\[out\] The texture height, in texels.</span></span><br/>                                                                                    |
| <span data-ttu-id="d0198-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elementos*</span><span class="sxs-lookup"><span data-stu-id="d0198-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elements*</span></span><br/>                             | <span data-ttu-id="d0198-124">\[out \] Número de elementos de una matriz.</span><span class="sxs-lookup"><span data-stu-id="d0198-124">\[out\] The number of elements in an array.</span></span><br/>                                                                               |
| <span data-ttu-id="d0198-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Profundidad*</span><span class="sxs-lookup"><span data-stu-id="d0198-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Depth*</span></span><br/>                                         | <span data-ttu-id="d0198-126">\[out \] Profundidad de textura, en texturas.</span><span class="sxs-lookup"><span data-stu-id="d0198-126">\[out\] The texture depth, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="d0198-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span><span class="sxs-lookup"><span data-stu-id="d0198-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span></span><br/>     | <span data-ttu-id="d0198-128">\[out \] Número de niveles de mapa mip.</span><span class="sxs-lookup"><span data-stu-id="d0198-128">\[out\] The number of mipmap levels.</span></span><br/>                                                                                      |
| <span data-ttu-id="d0198-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span><span class="sxs-lookup"><span data-stu-id="d0198-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span></span><br/> | <span data-ttu-id="d0198-130">\[out \] Número de muestras.</span><span class="sxs-lookup"><span data-stu-id="d0198-130">\[out\] The number of samples.</span></span><br/>                                                                                            |



 

## <a name="return-value"></a><span data-ttu-id="d0198-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0198-131">Return Value</span></span>

<span data-ttu-id="d0198-132">None</span><span class="sxs-lookup"><span data-stu-id="d0198-132">None</span></span>

## <a name="overloaded-methods"></a><span data-ttu-id="d0198-133">Métodos sobrecargados</span><span class="sxs-lookup"><span data-stu-id="d0198-133">Overloaded Methods</span></span>

<span data-ttu-id="d0198-134">En esta tabla se enumeran todas las distintas versiones del método . las versiones difieren en el número de parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="d0198-134">This table lists all the different versions of the method; versions differs by the number of input parameters.</span></span> <span data-ttu-id="d0198-135">Observe que para cada método que toma parámetros enteros, hay un método sobrecargado que toma parámetros de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="d0198-135">Notice that for every method that takes integer parameters, there is an overloaded method that takes floating-point parameters.</span></span>



| <span data-ttu-id="d0198-136">Texture-Object tipo</span><span class="sxs-lookup"><span data-stu-id="d0198-136">Texture-Object Type</span></span> | <span data-ttu-id="d0198-137">Parámetros de entrada</span><span class="sxs-lookup"><span data-stu-id="d0198-137">Input Parameters</span></span>                                                               |
|---------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="d0198-138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d0198-138">Texture1D</span></span>           | <span data-ttu-id="d0198-139">UINT MipLevel, UINT Width, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d0198-139">UINT MipLevel, UINT Width, UINT NumberOfLevels</span></span>                                 |
| <span data-ttu-id="d0198-140">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d0198-140">Texture1D</span></span>           | <span data-ttu-id="d0198-141">Ancho UINT</span><span class="sxs-lookup"><span data-stu-id="d0198-141">UINT Width</span></span>                                                                     |
| <span data-ttu-id="d0198-142">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d0198-142">Texture1D</span></span>           | <span data-ttu-id="d0198-143">UINT MipLevel, float Width, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d0198-143">UINT MipLevel, float Width, float NumberOfLevels</span></span>                               |
| <span data-ttu-id="d0198-144">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d0198-144">Texture1D</span></span>           | <span data-ttu-id="d0198-145">float Width</span><span class="sxs-lookup"><span data-stu-id="d0198-145">float Width</span></span>                                                                    |
| <span data-ttu-id="d0198-146">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d0198-146">Texture1DArray</span></span>      | <span data-ttu-id="d0198-147">UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d0198-147">UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="d0198-148">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d0198-148">Texture1DArray</span></span>      | <span data-ttu-id="d0198-149">UINT Width, UINT Elements</span><span class="sxs-lookup"><span data-stu-id="d0198-149">UINT Width, UINT Elements</span></span>                                                      |
| <span data-ttu-id="d0198-150">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d0198-150">Texture1DArray</span></span>      | <span data-ttu-id="d0198-151">UINT MipLevel, float Width, float Elements, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d0198-151">UINT MipLevel, float Width, float Elements, float NumberOfLevels</span></span>               |
| <span data-ttu-id="d0198-152">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d0198-152">Texture1DArray</span></span>      | <span data-ttu-id="d0198-153">float Width, float Elements</span><span class="sxs-lookup"><span data-stu-id="d0198-153">float Width, float Elements</span></span>                                                    |
| <span data-ttu-id="d0198-154">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d0198-154">Texture2D</span></span>           | <span data-ttu-id="d0198-155">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d0198-155">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="d0198-156">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d0198-156">Texture2D</span></span>           | <span data-ttu-id="d0198-157">UINT Width, UINT Height</span><span class="sxs-lookup"><span data-stu-id="d0198-157">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="d0198-158">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d0198-158">Texture2D</span></span>           | <span data-ttu-id="d0198-159">UINT MipLevel, float Width, float Height, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d0198-159">UINT MipLevel, float Width, float Height, float NumberOfLevels</span></span>                 |
| <span data-ttu-id="d0198-160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d0198-160">Texture2D</span></span>           | <span data-ttu-id="d0198-161">float Width, float Height</span><span class="sxs-lookup"><span data-stu-id="d0198-161">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="d0198-162">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d0198-162">Texture2DArray</span></span>      | <span data-ttu-id="d0198-163">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d0198-163">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="d0198-164">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d0198-164">Texture2DArray</span></span>      | <span data-ttu-id="d0198-165">UINT Width, UINT Height, UINT Elements</span><span class="sxs-lookup"><span data-stu-id="d0198-165">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="d0198-166">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d0198-166">Texture2DArray</span></span>      | <span data-ttu-id="d0198-167">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d0198-167">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="d0198-168">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d0198-168">Texture2DArray</span></span>      | <span data-ttu-id="d0198-169">float Width, float Height, float Elements</span><span class="sxs-lookup"><span data-stu-id="d0198-169">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="d0198-170">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d0198-170">Texture3D</span></span>           | <span data-ttu-id="d0198-171">UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d0198-171">UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels</span></span>        |
| <span data-ttu-id="d0198-172">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d0198-172">Texture3D</span></span>           | <span data-ttu-id="d0198-173">UINT Width, UINT Height, UINT Depth</span><span class="sxs-lookup"><span data-stu-id="d0198-173">UINT Width, UINT Height, UINT Depth</span></span>                                            |
| <span data-ttu-id="d0198-174">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d0198-174">Texture3D</span></span>           | <span data-ttu-id="d0198-175">UINT MipLevel, float Width, float Height, float Depth, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d0198-175">UINT MipLevel, float Width, float Height, float Depth, float NumberOfLevels</span></span>    |
| <span data-ttu-id="d0198-176">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d0198-176">Texture3D</span></span>           | <span data-ttu-id="d0198-177">float Width, float Height, float Depth</span><span class="sxs-lookup"><span data-stu-id="d0198-177">float Width, float Height, float Depth</span></span>                                         |
| <span data-ttu-id="d0198-178">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d0198-178">TextureCube</span></span>         | <span data-ttu-id="d0198-179">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d0198-179">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="d0198-180">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d0198-180">TextureCube</span></span>         | <span data-ttu-id="d0198-181">UINT Width, UINT Height</span><span class="sxs-lookup"><span data-stu-id="d0198-181">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="d0198-182">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d0198-182">TextureCube</span></span>         | <span data-ttu-id="d0198-183">UINT MipLevel, float Width, float Height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d0198-183">UINT MipLevel, float Width, float Height, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="d0198-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d0198-184">TextureCube</span></span>         | <span data-ttu-id="d0198-185">float Width, float Height</span><span class="sxs-lookup"><span data-stu-id="d0198-185">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="d0198-186">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d0198-186">TextureCubeArray</span></span>    | <span data-ttu-id="d0198-187">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d0198-187">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="d0198-188">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d0198-188">TextureCubeArray</span></span>    | <span data-ttu-id="d0198-189">UINT Width, UINT Height, UINT Elements</span><span class="sxs-lookup"><span data-stu-id="d0198-189">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="d0198-190">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d0198-190">TextureCubeArray</span></span>    | <span data-ttu-id="d0198-191">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="d0198-191">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="d0198-192">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d0198-192">TextureCubeArray</span></span>    | <span data-ttu-id="d0198-193">float Width, float Height, float Elements</span><span class="sxs-lookup"><span data-stu-id="d0198-193">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="d0198-194">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="d0198-194">Texture2DMS</span></span>         | <span data-ttu-id="d0198-195">UINT Width, UINT Height, UINT Samples</span><span class="sxs-lookup"><span data-stu-id="d0198-195">UINT Width, UINT Height, UINT Samples</span></span>                                          |
| <span data-ttu-id="d0198-196">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="d0198-196">Texture2DMS</span></span>         | <span data-ttu-id="d0198-197">float Width, float Height, float Samples</span><span class="sxs-lookup"><span data-stu-id="d0198-197">float Width, float Height, float Samples</span></span>                                       |
| <span data-ttu-id="d0198-198">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="d0198-198">Texture2DMSArray</span></span>    | <span data-ttu-id="d0198-199">UINT Width, UINT Height, UINT Elements, UINT Samples</span><span class="sxs-lookup"><span data-stu-id="d0198-199">UINT Width, UINT Height, UINT Elements, UINT Samples</span></span>                           |
| <span data-ttu-id="d0198-200">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="d0198-200">Texture2DMSArray</span></span>    | <span data-ttu-id="d0198-201">float Width, float Height, float Elements, float Samples</span><span class="sxs-lookup"><span data-stu-id="d0198-201">float Width, float Height, float Elements, float Samples</span></span>                       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d0198-202">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="d0198-202">Minimum Shader Model</span></span>

<span data-ttu-id="d0198-203">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d0198-203">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d0198-204">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d0198-204">vs\_4\_0</span></span> | <span data-ttu-id="d0198-205">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d0198-205">vs\_4\_1</span></span>  | <span data-ttu-id="d0198-206">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d0198-206">ps\_4\_0</span></span> | <span data-ttu-id="d0198-207">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d0198-207">ps\_4\_1</span></span>  | <span data-ttu-id="d0198-208">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d0198-208">gs\_4\_0</span></span> | <span data-ttu-id="d0198-209">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d0198-209">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="d0198-210">x</span><span class="sxs-lookup"><span data-stu-id="d0198-210">x</span></span>        | <span data-ttu-id="d0198-211">x</span><span class="sxs-lookup"><span data-stu-id="d0198-211">x</span></span>         | <span data-ttu-id="d0198-212">x</span><span class="sxs-lookup"><span data-stu-id="d0198-212">x</span></span>        | <span data-ttu-id="d0198-213">x</span><span class="sxs-lookup"><span data-stu-id="d0198-213">x</span></span>         | <span data-ttu-id="d0198-214">x</span><span class="sxs-lookup"><span data-stu-id="d0198-214">x</span></span>        | <span data-ttu-id="d0198-215">x</span><span class="sxs-lookup"><span data-stu-id="d0198-215">x</span></span>         |



 

1.  <span data-ttu-id="d0198-216">Devuelve dimensiones para el nivel de mapa mip más grande (cero).</span><span class="sxs-lookup"><span data-stu-id="d0198-216">Returns dimensions for the largest (zeroth) mipmap level.</span></span>
2.  <span data-ttu-id="d0198-217">TextureCubeArray está disponible en El modelo de sombreador 4.1 o superior.</span><span class="sxs-lookup"><span data-stu-id="d0198-217">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
3.  <span data-ttu-id="d0198-218">El modelo de sombreador 4.1 está disponible en Direct3D 10.1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="d0198-218">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0198-219">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d0198-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0198-220">Texture-Object</span><span class="sxs-lookup"><span data-stu-id="d0198-220">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





