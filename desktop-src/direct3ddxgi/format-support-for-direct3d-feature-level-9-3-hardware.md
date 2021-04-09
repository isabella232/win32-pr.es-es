---
description: En esta sección se especifican los formatos ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que se admiten en el hardware de 10Level9 9,3 de la característica Direct3D.
ms.assetid: B2A843D5-6A6B-4180-8B94-D032B1322798
title: Compatibilidad con el formato de hardware de la característica de nivel 9.3 de Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79185ddb360fe9359371671e3722372c3a1615f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079928"
---
# <a name="format-support-for-direct3d-feature-10level9-93-hardware"></a><span data-ttu-id="e1135-103">Compatibilidad con el formato de hardware de la característica de nivel 9.3 de Direct3D</span><span class="sxs-lookup"><span data-stu-id="e1135-103">Format support for Direct3D Feature 10Level9 9.3 hardware</span></span>

<span data-ttu-id="e1135-104">En esta sección se especifican los formatos ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que se admiten en el hardware de 10Level9 9,3 de la característica Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e1135-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature 10Level9 9.3 hardware.</span></span>

<span data-ttu-id="e1135-105">En la tabla se resume la compatibilidad de las características con la siguiente clave.</span><span class="sxs-lookup"><span data-stu-id="e1135-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="e1135-106">Símbolo</span><span class="sxs-lookup"><span data-stu-id="e1135-106">Symbol</span></span>                            | <span data-ttu-id="e1135-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1135-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="e1135-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="e1135-108">_ *-*\*</span></span>                             | <span data-ttu-id="e1135-109">No permitido o no disponible.</span><span class="sxs-lookup"><span data-stu-id="e1135-109">Disallowed or not available.</span></span>                                                  |
| ![requerido](images/letter-r.jpg)  | <span data-ttu-id="e1135-111">Se requiere compatibilidad con hardware.</span><span class="sxs-lookup"><span data-stu-id="e1135-111">Hardware support is required.</span></span>                                                 |
| ![opcional](images/letter-o.jpg)  | <span data-ttu-id="e1135-113">Compatibilidad de hardware opcional, el formato puede ser o no acelerado por hardware.</span><span class="sxs-lookup"><span data-stu-id="e1135-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dependientes](images/letter-d.jpg) | <span data-ttu-id="e1135-115">Requerido si se admite la característica opcional relacionada.</span><span class="sxs-lookup"><span data-stu-id="e1135-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="e1135-116">Este tema contiene una sección por formato.</span><span class="sxs-lookup"><span data-stu-id="e1135-116">This topic contains a section per format.</span></span> <span data-ttu-id="e1135-117">Un *destino* de formato (las tablas contienen una fila por destino) puede ser un tipo de recurso, una función intrínseca de HLSL o una funcionalidad determinada que depende de un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="e1135-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="e1135-118">Para comprobar mediante programación la compatibilidad de formato en D3D11 y D3D12, consulte Comprobación de la compatibilidad de las [características de hardware](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="e1135-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="e1135-119">Los números de los formatos son principalmente, pero no todos, en orden numérico ascendente; &mdash; algunos están fuera del orden numérico y se enumeran junto con otros formatos relevantes.</span><span class="sxs-lookup"><span data-stu-id="e1135-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="e1135-120">Tenga en cuenta también que los *tipos sin tipo* en un nombre de formato pueden significar un tipo *parcial* y no tienen un tipo estricto (consulte la sección [notas de formato](#format-notes) al final del tema).</span><span class="sxs-lookup"><span data-stu-id="e1135-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="e1135-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="e1135-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="e1135-122">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-122">Target</span></span> | <span data-ttu-id="e1135-123">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-123">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-124">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-125">0</span><span class="sxs-lookup"><span data-stu-id="e1135-125">0</span></span> |
| <span data-ttu-id="e1135-126">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-126">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-127">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-127">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-128">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-128">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-129">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-129">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-130">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-130">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-131">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-131">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-132">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-132">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-133">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-134">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-135">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-135">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-136">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-137">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-138">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-139">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-139">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-140">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-141">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-141">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-142">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-143">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-144">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-145">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-146">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-147">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-148">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-149">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-149">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-150">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-151">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-152">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-153">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-154">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-154">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-155">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-156">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-157">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-158">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-158">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-159">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-159">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-160">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-160">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-161">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-161">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-162">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-163">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-163">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-164">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-165">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-166">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-167">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-168">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-169">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-169">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-170">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="e1135-171">DXGI_FORMAT_R32G32B32A32 de \_ <sup>equipos</sup> sin tipo (1)</span><span class="sxs-lookup"><span data-stu-id="e1135-171">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="e1135-172">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-172">Target</span></span> | <span data-ttu-id="e1135-173">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-173">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-174">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-175">128</span><span class="sxs-lookup"><span data-stu-id="e1135-175">128</span></span> |
| <span data-ttu-id="e1135-176">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-176">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-177">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-177">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-178">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-178">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-179">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-179">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-180">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-180">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-181">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-181">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-182">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-182">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-183">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-184">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-185">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-185">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-186">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-186">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-187">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-187">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-188">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-188">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-189">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-189">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-190">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-190">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-191">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-191">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-192">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-192">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-193">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-193">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-194">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-194">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-195">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-195">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-196">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-196">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-197">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-197">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-198">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-198">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-199">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-199">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-200">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-200">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-201">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-201">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-202">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-202">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-203">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-203">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-204">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-204">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-205">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-205">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-206">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-206">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-207">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-207">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-208">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-208">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-209">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-209">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-210">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-210">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-211">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-211">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-212">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-212">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-213">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-213">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-214">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-214">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-215">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-215">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-216">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-216">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-217">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-217">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-218">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-218">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-219">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-219">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-220">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-220">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a><span data-ttu-id="e1135-221">DXGI_FORMAT_R32G32B32A32 \_ float<sup>FNS</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="e1135-221">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FNS</sup> (2)</span></span>
| <span data-ttu-id="e1135-222">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-222">Target</span></span> | <span data-ttu-id="e1135-223">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-223">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-224">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-224">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-225">128</span><span class="sxs-lookup"><span data-stu-id="e1135-225">128</span></span> |
| <span data-ttu-id="e1135-226">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-226">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-228">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-228">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-229">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-229">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-231">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-232">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-233">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-234">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-234">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-236">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-236">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-238">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-238">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-240">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-240">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-242">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-242">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-243">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-243">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-244">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-244">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-245">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-245">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-246">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-246">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-247">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-247">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-249">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-249">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-251">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-251">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-253">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-253">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-254">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-254">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-255">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-255">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-256">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-256">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-257">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-257">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-258">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-258">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-259">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-259">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-260">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-260">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-261">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-261">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-262">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-262">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-263">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-263">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-264">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-264">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-265">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-265">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-266">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-266">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-267">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-267">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-269">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-269">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-271">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-271">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-273">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-273">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-275">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-275">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-277">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-277">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-278">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-278">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-279">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-279">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-280">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-280">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-281">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-281">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-282">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-282">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-283">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-283">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-284">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-284">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a><span data-ttu-id="e1135-285">DXGI_FORMAT_R32G32B32A32 \_ uint<sup>FNS</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="e1135-285">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FNS</sup> (3)</span></span>
| <span data-ttu-id="e1135-286">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-286">Target</span></span> | <span data-ttu-id="e1135-287">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-287">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-288">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-288">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-289">128</span><span class="sxs-lookup"><span data-stu-id="e1135-289">128</span></span> |
| <span data-ttu-id="e1135-290">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-290">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-291">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-291">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-292">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-292">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-293">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-293">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-294">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-294">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-295">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-295">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-296">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-296">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-297">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-297">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-298">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-298">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-299">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-299">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-300">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-300">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-301">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-301">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-302">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-302">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-303">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-303">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-304">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-304">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-305">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-305">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-306">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-306">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-307">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-307">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-308">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-308">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-309">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-309">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-310">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-310">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-311">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-311">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-312">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-312">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-313">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-313">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-314">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-314">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-315">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-315">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-316">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-316">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-317">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-317">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-318">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-318">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-319">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-319">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-320">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-320">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-321">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-321">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-322">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-322">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-323">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-323">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-324">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-324">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-325">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-325">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-326">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-326">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-327">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-327">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-328">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-328">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-329">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-329">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-330">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-330">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-331">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-331">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-332">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-332">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-333">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-333">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-334">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-334">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a><span data-ttu-id="e1135-335">DXGI_FORMAT_R32G32B32A32 \_ San<sup>FNS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="e1135-335">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FNS</sup> (4)</span></span>
| <span data-ttu-id="e1135-336">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-336">Target</span></span> | <span data-ttu-id="e1135-337">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-337">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-338">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-338">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-339">128</span><span class="sxs-lookup"><span data-stu-id="e1135-339">128</span></span> |
| <span data-ttu-id="e1135-340">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-340">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-341">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-341">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-342">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-342">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-343">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-343">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-344">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-344">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-345">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-345">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-346">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-346">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-347">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-347">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-348">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-349">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-349">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-350">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-350">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-351">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-351">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-352">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-352">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-353">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-353">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-354">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-354">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-355">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-355">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-356">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-356">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-357">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-357">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-358">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-358">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-359">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-359">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-360">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-360">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-361">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-361">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-362">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-362">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-363">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-363">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-364">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-364">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-365">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-365">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-366">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-366">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-367">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-367">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-368">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-368">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-369">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-369">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-370">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-370">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-371">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-371">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-372">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-372">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-373">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-373">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-374">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-374">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-375">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-375">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-376">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-376">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-377">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-377">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-378">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-378">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-379">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-379">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-380">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-380">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-381">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-381">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-382">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-382">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-383">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-383">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-384">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-384">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="e1135-385">DXGI_FORMAT_R32G32B32 de \_ <sup>equipos</sup> sin tipo (5)</span><span class="sxs-lookup"><span data-stu-id="e1135-385">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="e1135-386">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-386">Target</span></span> | <span data-ttu-id="e1135-387">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-387">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-388">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-388">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-389">96</span><span class="sxs-lookup"><span data-stu-id="e1135-389">96</span></span> |
| <span data-ttu-id="e1135-390">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-390">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-391">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-391">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-392">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-392">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-393">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-393">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-394">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-394">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-395">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-395">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-396">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-396">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-397">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-397">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-398">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-398">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-399">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-399">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-400">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-401">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-401">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-402">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-402">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-403">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-403">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-404">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-404">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-405">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-405">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-406">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-406">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-407">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-407">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-408">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-409">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-410">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-411">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-412">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-413">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-414">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-415">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-416">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-417">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-418">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-419">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-420">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-421">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-422">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-422">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-423">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-423">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-424">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-424">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-425">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-425">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-426">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-426">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-427">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-427">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-428">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-428">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-429">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-429">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-430">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-430">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-431">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-431">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-432">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-432">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-433">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-433">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-434">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-434">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a><span data-ttu-id="e1135-435">DXGI_FORMAT_R32G32B32 \_ float<sup>FNS</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="e1135-435">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FNS</sup> (6)</span></span>
| <span data-ttu-id="e1135-436">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-436">Target</span></span> | <span data-ttu-id="e1135-437">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-437">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-438">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-438">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-439">96</span><span class="sxs-lookup"><span data-stu-id="e1135-439">96</span></span> |
| <span data-ttu-id="e1135-440">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-440">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-442">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-442">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-443">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-443">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-445">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-446">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-447">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-448">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-449">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-449">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-450">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-450">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-451">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-451">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-452">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-452">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-453">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-454">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-455">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-455">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-456">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-457">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-457">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-458">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-458">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-459">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-459">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-460">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-460">Blendable RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="e1135-462">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-462">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-463">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-463">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-464">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-464">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-465">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-465">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-466">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-466">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-467">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-467">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-468">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-468">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-469">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-469">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-470">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-470">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-471">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-471">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-472">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-472">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-473">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-473">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-474">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-474">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-475">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-475">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-476">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-476">4x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="e1135-478">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-478">8x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="e1135-480">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-480">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-481">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-481">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-482">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-482">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-483">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-483">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-484">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-484">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-485">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-485">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-486">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-486">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-487">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-487">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-488">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-488">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-489">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-489">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a><span data-ttu-id="e1135-490">DXGI_FORMAT_R32G32B32 \_ uint<sup>FNS</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="e1135-490">DXGI_FORMAT_R32G32B32\_UINT<sup>FNS</sup> (7)</span></span>
| <span data-ttu-id="e1135-491">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-491">Target</span></span> | <span data-ttu-id="e1135-492">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-492">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-493">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-493">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-494">96</span><span class="sxs-lookup"><span data-stu-id="e1135-494">96</span></span> |
| <span data-ttu-id="e1135-495">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-495">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-496">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-496">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-497">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-498">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-499">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-500">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-501">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-502">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-502">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-503">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-503">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-504">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-504">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-505">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-505">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-506">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-507">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-508">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-508">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-509">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-510">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-510">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-511">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-511">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-512">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-512">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-513">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-513">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-514">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-514">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-515">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-515">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-516">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-516">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-517">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-517">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-518">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-518">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-519">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-519">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-520">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-520">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-521">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-521">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-522">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-522">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-523">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-523">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-524">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-524">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-525">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-525">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-526">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-526">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-527">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-527">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-528">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-528">4x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="e1135-530">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-530">8x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="e1135-532">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-533">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-534">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-534">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-535">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-536">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-537">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-538">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-539">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-540">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-540">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-541">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a><span data-ttu-id="e1135-542">DXGI_FORMAT_R32G32B32 \_ San<sup>FNS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="e1135-542">DXGI_FORMAT_R32G32B32\_SINT<sup>FNS</sup> (8)</span></span>
| <span data-ttu-id="e1135-543">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-543">Target</span></span> | <span data-ttu-id="e1135-544">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-544">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-545">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-546">96</span><span class="sxs-lookup"><span data-stu-id="e1135-546">96</span></span> |
| <span data-ttu-id="e1135-547">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-547">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-548">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-548">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-549">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-550">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-551">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-552">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-553">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-554">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-555">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-556">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-557">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-558">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-559">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-560">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-560">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-561">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-562">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-562">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-563">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-564">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-564">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-565">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-566">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-567">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-568">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-569">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-570">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-570">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-571">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-572">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-573">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-574">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-575">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-576">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-577">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-578">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-579">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-580">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-580">4x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="e1135-582">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-582">8x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="e1135-584">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-584">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-585">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-585">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-586">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-586">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-587">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-587">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-588">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-588">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-589">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-590">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-591">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-592">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-592">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-593">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-593">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="e1135-594">DXGI_FORMAT_R16G16B16A16 de \_ <sup>equipos</sup> sin tipo (9)</span><span class="sxs-lookup"><span data-stu-id="e1135-594">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="e1135-595">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-595">Target</span></span> | <span data-ttu-id="e1135-596">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-596">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-597">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-597">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-598">64</span><span class="sxs-lookup"><span data-stu-id="e1135-598">64</span></span> |
| <span data-ttu-id="e1135-599">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-599">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-600">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-600">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-601">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-601">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-602">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-602">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-603">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-603">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-604">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-604">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-605">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-605">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-606">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-606">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-607">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-607">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-608">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-608">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-609">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-609">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-610">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-610">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-611">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-611">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-612">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-612">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-613">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-613">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-614">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-614">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-615">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-615">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-616">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-616">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-617">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-617">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-618">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-618">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-619">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-619">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-620">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-620">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-621">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-621">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-622">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-622">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-623">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-623">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-624">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-624">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-625">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-625">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-626">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-626">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-627">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-627">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-628">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-628">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-629">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-629">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-630">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-630">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-631">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-631">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-632">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-632">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-633">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-633">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-634">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-634">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-635">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-635">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-636">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-636">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-637">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-637">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-638">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-638">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-639">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-639">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-640">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-640">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-641">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-641">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-642">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-642">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-643">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-643">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a><span data-ttu-id="e1135-644">DXGI_FORMAT_R16G16B16A16 \_ float<sup>FNS</sup> (10)</span><span class="sxs-lookup"><span data-stu-id="e1135-644">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FNS</sup> (10)</span></span>
| <span data-ttu-id="e1135-645">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-645">Target</span></span> | <span data-ttu-id="e1135-646">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-646">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-647">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-647">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-648">64</span><span class="sxs-lookup"><span data-stu-id="e1135-648">64</span></span> |
| <span data-ttu-id="e1135-649">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-649">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-651">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-651">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-652">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-652">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-654">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-654">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-655">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-655">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-656">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-656">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-657">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-657">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-659">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-659">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-661">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-661">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-663">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-663">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-665">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-665">Shader sample (any filter)</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-667">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-667">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-668">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-668">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-669">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-669">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-670">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-670">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-671">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-671">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-673">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-673">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-675">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-675">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-677">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-677">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-679">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-679">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-680">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-680">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-681">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-681">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-682">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-682">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-683">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-683">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-684">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-684">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-685">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-685">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-686">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-686">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-687">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-687">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-688">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-688">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-689">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-689">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-690">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-690">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-691">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-691">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-692">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-692">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-694">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-694">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-696">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-696">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-698">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-698">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-700">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-700">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-702">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-702">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-703">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-703">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-704">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-704">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-705">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-705">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-706">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-706">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-707">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-707">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-708">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-708">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-710">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-710">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a><span data-ttu-id="e1135-711">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FNS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="e1135-711">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FNS</sup> (11)</span></span>
| <span data-ttu-id="e1135-712">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-712">Target</span></span> | <span data-ttu-id="e1135-713">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-713">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-714">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-714">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-715">64</span><span class="sxs-lookup"><span data-stu-id="e1135-715">64</span></span> |
| <span data-ttu-id="e1135-716">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-716">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-718">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-718">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-719">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-719">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-720">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-720">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-721">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-721">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-722">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-722">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-723">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-723">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-725">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-725">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-727">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-727">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-729">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-729">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-731">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-731">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-733">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-733">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-734">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-734">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-735">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-735">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-736">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-736">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-737">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-737">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-739">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-739">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-741">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-741">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-743">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-743">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-744">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-744">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-745">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-745">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-746">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-746">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-747">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-747">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-748">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-748">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-749">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-749">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-750">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-750">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-751">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-751">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-752">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-752">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-753">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-753">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-754">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-754">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-755">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-755">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-756">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-756">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-757">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-757">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-759">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-759">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-761">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-761">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-763">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-763">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-765">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-765">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-767">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-767">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-768">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-768">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-769">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-769">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-770">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-770">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-771">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-771">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-772">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-772">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-773">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-773">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-774">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-774">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a><span data-ttu-id="e1135-775">DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FNS</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="e1135-775">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FNS</sup> (12)</span></span>
| <span data-ttu-id="e1135-776">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-776">Target</span></span> | <span data-ttu-id="e1135-777">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-777">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-778">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-778">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-779">64</span><span class="sxs-lookup"><span data-stu-id="e1135-779">64</span></span> |
| <span data-ttu-id="e1135-780">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-780">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-781">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-781">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-782">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-782">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-783">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-783">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-784">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-784">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-785">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-785">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-786">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-786">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-787">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-787">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-788">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-788">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-789">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-789">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-790">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-790">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-791">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-791">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-792">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-792">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-793">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-793">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-794">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-794">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-795">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-795">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-796">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-796">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-797">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-797">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-798">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-798">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-799">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-799">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-800">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-800">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-801">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-801">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-802">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-802">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-803">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-803">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-804">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-804">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-805">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-805">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-806">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-806">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-807">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-807">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-808">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-808">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-809">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-809">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-810">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-810">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-811">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-811">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-812">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-812">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-813">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-813">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-814">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-814">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-815">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-815">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-816">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-816">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-817">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-817">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-818">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-818">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-819">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-819">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-820">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-820">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-821">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-821">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-822">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-822">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-823">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-823">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-824">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-824">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a><span data-ttu-id="e1135-825">DXGI_FORMAT_R16G16B16A16 \_ SNORM<sup>FNS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="e1135-825">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FNS</sup> (13)</span></span>
| <span data-ttu-id="e1135-826">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-826">Target</span></span> | <span data-ttu-id="e1135-827">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-827">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-828">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-828">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-829">64</span><span class="sxs-lookup"><span data-stu-id="e1135-829">64</span></span> |
| <span data-ttu-id="e1135-830">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-830">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-832">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-832">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-833">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-833">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-835">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-835">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-836">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-836">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-837">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-837">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-838">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-838">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-839">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-839">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-840">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-840">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-841">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-841">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-842">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-842">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-843">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-843">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-844">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-844">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-845">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-845">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-846">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-846">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-847">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-847">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-848">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-848">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-849">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-849">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-850">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-850">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-851">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-851">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-852">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-852">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-853">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-853">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-854">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-854">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-855">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-855">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-856">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-856">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-857">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-857">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-858">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-858">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-859">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-859">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-860">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-860">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-861">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-861">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-862">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-862">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-863">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-863">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-864">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-864">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-865">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-865">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-866">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-866">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-867">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-867">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-868">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-868">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-869">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-869">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-870">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-870">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-871">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-871">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-872">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-872">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-873">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-873">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-874">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-874">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-875">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-875">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-876">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-876">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a><span data-ttu-id="e1135-877">DXGI_FORMAT_R16G16B16A16 \_ San<sup>FNS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="e1135-877">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FNS</sup> (14)</span></span>
| <span data-ttu-id="e1135-878">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-878">Target</span></span> | <span data-ttu-id="e1135-879">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-879">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-880">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-880">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-881">64</span><span class="sxs-lookup"><span data-stu-id="e1135-881">64</span></span> |
| <span data-ttu-id="e1135-882">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-882">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-884">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-884">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-885">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-885">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-887">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-887">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-888">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-888">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-889">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-889">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-890">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-890">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-891">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-891">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-892">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-893">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-893">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-894">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-894">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-895">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-895">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-896">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-896">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-897">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-897">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-898">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-898">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-899">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-899">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-900">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-900">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-901">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-901">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-902">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-902">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-903">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-903">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-904">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-904">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-905">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-905">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-906">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-906">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-907">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-907">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-908">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-908">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-909">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-909">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-910">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-910">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-911">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-911">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-912">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-912">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-913">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-913">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-914">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-914">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-915">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-915">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-916">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-916">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-917">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-917">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-918">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-918">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-919">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-919">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-920">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-920">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-921">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-921">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-922">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-922">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-923">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-923">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-924">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-924">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-925">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-925">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-926">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-926">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-927">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-927">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-928">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="e1135-929">DXGI_FORMAT_R32G32 de \_ <sup>equipos</sup> sin tipo (15)</span><span class="sxs-lookup"><span data-stu-id="e1135-929">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="e1135-930">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-930">Target</span></span> | <span data-ttu-id="e1135-931">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-931">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-932">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-933">64</span><span class="sxs-lookup"><span data-stu-id="e1135-933">64</span></span> |
| <span data-ttu-id="e1135-934">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-934">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-935">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-935">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-936">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-936">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-937">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-937">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-938">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-938">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-939">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-939">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-940">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-940">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-941">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-941">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-942">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-942">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-943">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-943">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-944">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-944">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-945">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-945">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-946">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-946">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-947">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-947">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-948">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-948">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-949">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-949">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-950">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-950">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-951">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-951">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-952">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-952">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-953">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-953">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-954">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-954">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-955">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-955">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-956">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-956">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-957">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-957">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-958">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-958">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-959">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-959">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-960">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-960">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-961">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-961">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-962">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-962">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-963">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-963">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-964">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-964">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-965">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-965">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-966">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-966">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-967">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-967">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-968">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-968">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-969">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-969">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-970">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-970">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-971">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-971">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-972">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-972">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-973">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-973">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-974">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-974">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-975">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-975">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-976">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-977">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-977">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-978">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-978">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a><span data-ttu-id="e1135-979">DXGI_FORMAT_R32G32 \_ float<sup>FNS</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="e1135-979">DXGI_FORMAT_R32G32\_FLOAT<sup>FNS</sup> (16)</span></span>
| <span data-ttu-id="e1135-980">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-980">Target</span></span> | <span data-ttu-id="e1135-981">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-981">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-982">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-982">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-983">64</span><span class="sxs-lookup"><span data-stu-id="e1135-983">64</span></span> |
| <span data-ttu-id="e1135-984">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-984">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-986">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-986">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-987">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-987">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-989">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-990">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-991">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-992">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-992">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-994">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-994">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-996">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-996">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-998">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-998">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1000">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1000">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-1001">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1001">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1002">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1002">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1003">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1003">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1004">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1004">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1005">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1005">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-1006">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1006">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-1007">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1007">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1009">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1009">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1010">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1010">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1011">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1011">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1012">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1012">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1013">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1013">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1014">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1014">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1015">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1015">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1016">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1016">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1017">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1017">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1018">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1018">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1019">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1019">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1020">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1020">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1021">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1021">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1022">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1022">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1023">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1023">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1025">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1025">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-1027">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1027">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-1029">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1029">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-1031">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1031">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1033">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1033">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1034">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1034">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-1035">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1035">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1036">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1036">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1037">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1037">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-1038">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1038">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-1039">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1039">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-1040">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1040">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a><span data-ttu-id="e1135-1041">DXGI_FORMAT_R32G32 \_ uint<sup>FNS</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="e1135-1041">DXGI_FORMAT_R32G32\_UINT<sup>FNS</sup> (17)</span></span>
| <span data-ttu-id="e1135-1042">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1042">Target</span></span> | <span data-ttu-id="e1135-1043">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1043">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1044">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1044">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1045">64</span><span class="sxs-lookup"><span data-stu-id="e1135-1045">64</span></span> |
| <span data-ttu-id="e1135-1046">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1046">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-1047">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1047">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1048">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1048">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1049">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1049">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1050">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-1050">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1051">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-1051">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-1052">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-1052">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-1053">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-1053">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-1054">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-1054">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-1055">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-1055">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-1056">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1056">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-1057">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1057">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1058">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1058">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1059">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1059">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1060">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1060">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1061">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1061">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-1062">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1062">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-1063">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1063">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1064">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1064">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1065">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1065">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1066">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1066">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1067">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1067">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1068">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1068">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1069">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1069">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1070">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1070">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1071">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1071">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1072">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1072">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1073">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1073">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1074">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1074">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1075">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1075">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1076">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1076">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1077">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1077">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1078">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1078">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-1079">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1079">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1080">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1080">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1081">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1081">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-1082">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1082">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-1083">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1083">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1084">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1084">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-1085">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1085">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1086">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1086">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1087">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1087">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-1088">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1088">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-1089">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1089">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-1090">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1090">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a><span data-ttu-id="e1135-1091">DXGI_FORMAT_R32G32 \_ San<sup>FNS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="e1135-1091">DXGI_FORMAT_R32G32\_SINT<sup>FNS</sup> (18)</span></span>
| <span data-ttu-id="e1135-1092">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1092">Target</span></span> | <span data-ttu-id="e1135-1093">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1093">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1094">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1094">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1095">64</span><span class="sxs-lookup"><span data-stu-id="e1135-1095">64</span></span> |
| <span data-ttu-id="e1135-1096">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1096">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-1097">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1097">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1098">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1098">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1099">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1099">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1100">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-1100">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1101">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-1101">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-1102">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-1102">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-1103">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-1103">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-1104">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-1104">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-1105">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-1105">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-1106">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1106">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-1107">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1107">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1108">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1108">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1109">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1109">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1110">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1110">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1111">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1111">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-1112">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1112">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-1113">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1113">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1114">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1114">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1115">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1115">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1116">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1116">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1117">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1117">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1118">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1118">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1119">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1119">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1120">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1120">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1121">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1121">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1122">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1122">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1123">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1123">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1124">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1124">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1125">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1125">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1126">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1126">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1127">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1127">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1128">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1128">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-1129">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1129">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1130">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1130">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1131">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1131">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-1132">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1132">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-1133">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1133">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1134">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1134">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-1135">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1135">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1136">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1136">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1137">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1137">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-1138">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1138">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-1139">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1139">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-1140">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1140">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="e1135-1141">DXGI_FORMAT_R32G8X24 de \_ <sup>equipos</sup> sin tipo (19)</span><span class="sxs-lookup"><span data-stu-id="e1135-1141">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="e1135-1142">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1142">Target</span></span> | <span data-ttu-id="e1135-1143">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1143">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1144">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1144">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1145">64</span><span class="sxs-lookup"><span data-stu-id="e1135-1145">64</span></span> |
| <span data-ttu-id="e1135-1146">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1146">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-1147">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1147">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1148">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1148">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1149">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1149">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1150">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-1150">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1151">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-1151">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-1152">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-1152">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-1153">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-1153">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-1154">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-1154">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-1155">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-1155">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-1156">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1156">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-1157">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1157">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1158">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1158">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1159">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1159">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1160">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1160">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1161">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1161">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-1162">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1162">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-1163">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1163">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1164">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1164">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1165">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1165">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1166">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1166">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1167">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1167">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1168">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1168">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1169">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1169">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1170">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1170">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1171">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1172">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1173">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1174">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1174">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1175">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1176">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1176">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1177">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1177">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1178">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1178">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-1179">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1179">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1180">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1180">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1181">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1181">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-1182">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1182">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-1183">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1183">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1184">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1184">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-1185">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1185">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1186">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1186">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1187">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1187">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-1188">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1188">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-1189">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1189">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-1190">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1190">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a><span data-ttu-id="e1135-1191">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FNS</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="e1135-1191">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FNS</sup> (20)</span></span>
| <span data-ttu-id="e1135-1192">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1192">Target</span></span> | <span data-ttu-id="e1135-1193">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1193">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1194">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1194">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1195">64</span><span class="sxs-lookup"><span data-stu-id="e1135-1195">64</span></span> |
| <span data-ttu-id="e1135-1196">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1196">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-1197">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1197">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1198">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1198">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1199">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1199">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1200">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-1200">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1201">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-1201">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-1202">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-1202">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-1203">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-1203">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-1204">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-1204">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-1205">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-1205">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-1206">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1206">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-1207">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1207">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1208">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1208">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1209">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1209">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1210">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1210">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1211">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1211">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-1212">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1212">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-1213">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1213">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1214">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1214">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1215">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1215">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1216">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1216">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1217">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1217">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1218">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1218">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1219">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1219">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1220">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1220">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1221">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1221">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1222">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1222">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1223">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1223">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1224">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1224">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1225">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1225">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1226">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1226">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1227">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1227">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1228">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1228">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-1229">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1229">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1230">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1230">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1231">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1231">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-1232">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1232">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-1233">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1233">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1234">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1234">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-1235">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1235">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1236">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1236">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1237">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1237">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-1238">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1238">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-1239">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1239">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-1240">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1240">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a><span data-ttu-id="e1135-1241">DXGI_FORMAT_R32 \_ float \_ \_ <sup>FNS</sup> typeless X8X24 (21)</span><span class="sxs-lookup"><span data-stu-id="e1135-1241">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FNS</sup> (21)</span></span>
| <span data-ttu-id="e1135-1242">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1242">Target</span></span> | <span data-ttu-id="e1135-1243">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1243">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1244">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1244">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1245">64</span><span class="sxs-lookup"><span data-stu-id="e1135-1245">64</span></span> |
| <span data-ttu-id="e1135-1246">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1246">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-1247">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1247">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1248">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1248">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1249">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1249">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1250">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-1250">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1251">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-1251">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-1252">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-1252">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-1253">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-1253">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-1254">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-1254">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-1255">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-1255">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-1256">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1256">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-1257">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1257">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1258">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1258">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1259">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1259">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1260">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1260">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1261">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1261">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-1262">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1262">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-1263">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1263">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1264">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1264">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1265">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1265">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1266">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1266">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1267">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1267">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1268">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1268">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1269">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1269">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1270">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1270">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1271">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1271">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1272">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1272">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1273">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1273">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1274">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1274">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1275">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1275">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1276">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1276">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1277">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1277">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1278">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1278">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-1279">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1279">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1280">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1280">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1281">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1281">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-1282">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1282">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-1283">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1283">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1284">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1284">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-1285">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1285">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1286">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1286">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1287">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1287">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-1288">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1288">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-1289">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1289">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-1290">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1290">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a><span data-ttu-id="e1135-1291">DXGI_FORMAT_X32 \_ \_ G8X24 \_ uint<sup>FNS</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="e1135-1291">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FNS</sup> (22)</span></span>
| <span data-ttu-id="e1135-1292">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1292">Target</span></span> | <span data-ttu-id="e1135-1293">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1293">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1294">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1294">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1295">64</span><span class="sxs-lookup"><span data-stu-id="e1135-1295">64</span></span> |
| <span data-ttu-id="e1135-1296">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1296">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-1297">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1297">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1298">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1298">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1299">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1299">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1300">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-1300">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1301">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-1301">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-1302">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-1302">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-1303">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-1303">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-1304">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-1304">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-1305">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-1305">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-1306">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1306">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-1307">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1307">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1308">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1308">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1309">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1309">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1310">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1310">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1311">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1311">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-1312">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1312">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-1313">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1313">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1314">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1314">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1315">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1315">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1316">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1316">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1317">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1317">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1318">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1318">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1319">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1319">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1320">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1320">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1321">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1321">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1322">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1322">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1323">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1323">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1324">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1324">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1325">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1325">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1326">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1326">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1327">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1327">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1328">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1328">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-1329">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1329">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1330">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1330">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1331">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1331">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-1332">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1332">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-1333">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1333">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1334">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1334">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-1335">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1335">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1336">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1336">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1337">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1337">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-1338">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1338">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-1339">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1339">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-1340">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1340">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="e1135-1341">DXGI_FORMAT_R10G10B10A2 de \_ <sup>equipos</sup> sin tipo (23)</span><span class="sxs-lookup"><span data-stu-id="e1135-1341">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="e1135-1342">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1342">Target</span></span> | <span data-ttu-id="e1135-1343">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1343">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1344">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1344">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1345">32</span><span class="sxs-lookup"><span data-stu-id="e1135-1345">32</span></span> |
| <span data-ttu-id="e1135-1346">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1346">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-1347">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1347">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1348">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1348">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1349">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1349">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1350">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-1350">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1351">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-1351">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-1352">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-1352">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-1353">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-1353">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-1354">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-1354">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-1355">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-1355">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-1356">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1356">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-1357">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1357">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1358">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1358">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1359">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1359">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1360">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1360">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1361">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1361">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-1362">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1362">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-1363">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1363">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1364">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1364">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1365">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1365">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1366">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1366">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1367">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1367">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1368">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1368">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1369">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1369">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1370">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1370">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1371">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1371">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1372">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1372">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1373">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1373">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1374">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1374">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1375">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1375">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1376">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1376">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1377">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1377">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1378">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1378">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-1379">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1379">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1380">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1380">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1381">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1381">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-1382">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1382">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-1383">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1383">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1384">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1384">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-1385">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1385">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1386">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1386">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1387">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1387">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-1388">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1388">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-1389">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1389">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-1390">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1390">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a><span data-ttu-id="e1135-1391">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FNS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="e1135-1391">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FNS</sup> (24)</span></span>
| <span data-ttu-id="e1135-1392">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1392">Target</span></span> | <span data-ttu-id="e1135-1393">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1393">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1394">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1394">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1395">32</span><span class="sxs-lookup"><span data-stu-id="e1135-1395">32</span></span> |
| <span data-ttu-id="e1135-1396">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1396">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-1397">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1397">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1398">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1398">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1399">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1399">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1400">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-1400">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1401">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-1401">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-1402">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-1402">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-1403">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-1403">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-1404">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-1404">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-1405">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-1405">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-1406">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1406">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-1407">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1407">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1408">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1408">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1409">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1409">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1410">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1410">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1411">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1411">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-1412">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1412">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-1413">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1413">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1414">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1414">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1415">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1415">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1416">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1416">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1417">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1417">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1418">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1418">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1419">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1419">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1420">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1420">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1421">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1421">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1422">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1422">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1423">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1423">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1424">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1424">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1425">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1425">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1426">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1426">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1427">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1427">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1428">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1428">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-1429">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1429">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1430">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1430">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1431">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1431">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-1432">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1432">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-1433">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1433">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1434">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1434">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-1435">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1435">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1436">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1437">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-1438">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-1439">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1439">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1441">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a><span data-ttu-id="e1135-1442">DXGI_FORMAT_R10G10B10A2 \_ uint<sup>FNS</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="e1135-1442">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FNS</sup> (25)</span></span>
| <span data-ttu-id="e1135-1443">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1443">Target</span></span> | <span data-ttu-id="e1135-1444">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1444">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1445">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1446">32</span><span class="sxs-lookup"><span data-stu-id="e1135-1446">32</span></span> |
| <span data-ttu-id="e1135-1447">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1447">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-1448">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1448">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1449">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1449">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1450">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1450">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1451">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-1451">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1452">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-1452">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-1453">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-1453">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-1454">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-1454">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-1455">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-1455">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-1456">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-1456">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-1457">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1457">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-1458">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1458">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1459">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1459">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1460">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1460">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1461">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1461">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1462">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1462">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-1463">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1463">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-1464">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1464">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1465">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1465">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1466">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1466">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1467">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1467">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1468">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1468">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1469">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1469">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1470">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1470">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1471">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1471">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1472">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1472">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1473">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1473">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1474">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1474">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1475">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1475">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1476">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1476">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1477">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1477">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1478">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1478">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1479">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1479">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-1480">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1480">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1481">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1481">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1482">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1482">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-1483">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1483">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-1484">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1484">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1485">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1485">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-1486">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1486">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1487">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1487">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1488">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1488">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-1489">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1489">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-1490">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1490">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-1491">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1491">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a><span data-ttu-id="e1135-1492">DXGI_FORMAT_R10G10B10 \_ la \_ inclinación de XR \_ a2 \_ UNORM<sup>FNS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="e1135-1492">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FNS</sup> (89)</span></span>
| <span data-ttu-id="e1135-1493">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1493">Target</span></span> | <span data-ttu-id="e1135-1494">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1494">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1495">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1495">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1496">32</span><span class="sxs-lookup"><span data-stu-id="e1135-1496">32</span></span> |
| <span data-ttu-id="e1135-1497">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1497">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-1498">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1498">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1499">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1499">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1500">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1500">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1501">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-1501">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1502">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-1502">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-1503">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-1503">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-1504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-1504">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-1505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-1505">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-1506">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-1506">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-1507">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1507">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-1508">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1509">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1510">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1510">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1511">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1512">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1512">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-1513">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1513">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-1514">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1514">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1515">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1515">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1516">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1516">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1517">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1517">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1518">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1518">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1519">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1519">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1520">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1520">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1521">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1521">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1522">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1522">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1523">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1523">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1524">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1524">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1525">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1525">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1526">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1526">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1527">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1527">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1528">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1528">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1529">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1529">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-1530">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1530">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1531">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1531">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1532">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-1533">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-1534">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1534">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1535">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-1536">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1537">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1538">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-1539">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-1540">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1540">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-1541">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="e1135-1542">DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="e1135-1542">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="e1135-1543">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1543">Target</span></span> | <span data-ttu-id="e1135-1544">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1544">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1545">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1546">32</span><span class="sxs-lookup"><span data-stu-id="e1135-1546">32</span></span> |
| <span data-ttu-id="e1135-1547">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1547">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-1548">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1548">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1549">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1550">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1551">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-1551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-1552">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-1553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-1553">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-1554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-1554">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-1555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-1555">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-1556">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-1556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-1557">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-1558">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1559">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1560">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1560">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1561">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1562">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1562">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-1563">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-1564">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1564">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1565">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1566">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1567">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1568">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1569">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1570">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1570">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1571">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1572">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1573">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1574">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1575">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1576">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1577">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1578">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1579">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-1580">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1581">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1582">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-1583">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-1584">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1584">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1585">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-1586">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1587">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1587">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1588">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1588">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-1589">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1589">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-1590">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1590">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-1591">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1591">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="e1135-1592">DXGI_FORMAT_R8G8B8A8 de \_ <sup>equipos</sup> sin tipo (27)</span><span class="sxs-lookup"><span data-stu-id="e1135-1592">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="e1135-1593">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1593">Target</span></span> | <span data-ttu-id="e1135-1594">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1594">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1595">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1595">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1596">32</span><span class="sxs-lookup"><span data-stu-id="e1135-1596">32</span></span> |
| <span data-ttu-id="e1135-1597">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1597">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-1598">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1598">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1599">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1599">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1600">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1601">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-1601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-1602">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-1603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-1603">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-1604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-1604">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-1605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-1605">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-1606">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-1606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-1607">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-1608">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1609">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1610">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1610">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1611">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1612">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1612">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-1613">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-1614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1614">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1615">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1616">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1617">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1618">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1619">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1620">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1620">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1621">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1622">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1623">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1624">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1626">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1627">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1628">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1629">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1629">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-1630">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1630">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1631">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1631">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1632">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1632">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-1633">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1633">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-1634">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1634">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1635">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1635">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-1636">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1636">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1637">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1637">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1638">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1638">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-1639">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1639">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-1640">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1640">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-1641">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1641">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a><span data-ttu-id="e1135-1642">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FNS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="e1135-1642">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FNS</sup> (28)</span></span>
| <span data-ttu-id="e1135-1643">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1643">Target</span></span> | <span data-ttu-id="e1135-1644">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1644">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1645">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1645">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1646">32</span><span class="sxs-lookup"><span data-stu-id="e1135-1646">32</span></span> |
| <span data-ttu-id="e1135-1647">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1647">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1649">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1649">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1650">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1650">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1652">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1652">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1653">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-1653">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1654">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-1654">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-1655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-1655">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-1657">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-1659">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1661">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-1661">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1663">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1663">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1665">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1665">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1666">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1666">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1667">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1667">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1668">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1668">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1669">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1669">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1671">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1671">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1673">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1673">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1675">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1675">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1677">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1677">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1678">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1678">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1679">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1679">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1680">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1680">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1681">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1681">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1682">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1682">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1683">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1683">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1684">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1684">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1685">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1685">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1686">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1686">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1687">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1687">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1688">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1688">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1689">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1689">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1690">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1690">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1692">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1692">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-1694">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1694">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-1696">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1696">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-1698">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1698">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1700">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1700">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1701">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1701">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1703">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1703">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1704">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1704">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1705">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1705">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-1707">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1707">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1709">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1709">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1711">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1711">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a><span data-ttu-id="e1135-1712">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRGB<sup>FNS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="e1135-1712">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FNS</sup> (29)</span></span>
| <span data-ttu-id="e1135-1713">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1713">Target</span></span> | <span data-ttu-id="e1135-1714">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1714">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1715">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1715">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1716">32</span><span class="sxs-lookup"><span data-stu-id="e1135-1716">32</span></span> |
| <span data-ttu-id="e1135-1717">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1717">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1719">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1719">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1720">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1720">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1721">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1721">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1722">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-1722">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1723">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-1723">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-1724">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-1724">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1726">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-1726">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1728">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-1728">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1730">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-1730">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1732">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1732">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1734">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1734">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1735">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1735">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1736">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1736">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1737">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1737">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1738">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1738">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1740">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1740">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1742">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1742">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1744">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1744">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1746">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1746">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1747">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1747">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1748">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1748">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1749">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1749">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1750">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1750">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1751">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1751">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1752">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1752">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1753">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1753">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1754">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1754">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1755">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1755">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1756">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1756">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1757">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1757">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1758">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1758">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1759">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1759">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1761">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1761">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-1763">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1763">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-1765">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1765">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-1767">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1767">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1769">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1769">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1770">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1770">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1772">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1772">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1773">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1773">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1774">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1774">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-1776">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1776">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1778">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1778">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1780">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1780">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a><span data-ttu-id="e1135-1781">DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FNS</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="e1135-1781">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FNS</sup> (30)</span></span>
| <span data-ttu-id="e1135-1782">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1782">Target</span></span> | <span data-ttu-id="e1135-1783">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1783">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1784">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1784">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1785">32</span><span class="sxs-lookup"><span data-stu-id="e1135-1785">32</span></span> |
| <span data-ttu-id="e1135-1786">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1786">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1788">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1788">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1789">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1789">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1791">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1791">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1792">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-1792">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1793">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-1793">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-1794">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-1794">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-1795">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-1795">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-1796">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-1796">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-1797">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-1797">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-1798">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1798">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-1799">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1799">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1800">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1800">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1801">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1801">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1802">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1802">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1803">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1803">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-1804">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1804">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-1805">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1805">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1806">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1806">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1807">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1807">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1808">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1808">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1809">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1809">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1810">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1810">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1811">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1811">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1812">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1812">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1813">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1813">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1814">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1814">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1815">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1815">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1816">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1816">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1817">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1817">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1818">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1818">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1819">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1819">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1820">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1820">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-1821">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1821">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1822">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1822">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1823">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1823">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-1824">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1824">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-1825">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1825">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1826">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1826">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-1827">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1827">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1828">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1828">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1829">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1829">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-1830">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1830">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-1831">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1831">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-1832">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1832">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a><span data-ttu-id="e1135-1833">DXGI_FORMAT_R8G8B8A8 \_ SNORM<sup>FNS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="e1135-1833">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FNS</sup> (31)</span></span>
| <span data-ttu-id="e1135-1834">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1834">Target</span></span> | <span data-ttu-id="e1135-1835">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1835">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1836">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1836">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1837">32</span><span class="sxs-lookup"><span data-stu-id="e1135-1837">32</span></span> |
| <span data-ttu-id="e1135-1838">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1838">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1840">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1840">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1841">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1841">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1842">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1842">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1843">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-1843">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1844">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-1844">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-1845">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-1845">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1847">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-1847">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-1848">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-1848">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1850">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-1850">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1852">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1852">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1854">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1854">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1855">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1855">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1856">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1856">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1857">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1857">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1858">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1858">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1860">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1860">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-1861">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1861">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1862">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1862">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1863">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1863">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1864">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1864">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1865">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1865">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1866">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1866">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1867">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1867">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1868">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1868">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1869">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1869">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1870">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1870">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1871">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1871">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1872">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1872">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1873">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1873">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1874">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1874">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1875">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1875">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1876">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1876">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1878">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1878">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1879">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1879">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1880">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1880">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-1881">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1881">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-1882">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1882">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1883">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1883">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-1884">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1884">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1885">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1885">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1886">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1886">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-1887">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1887">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-1888">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1888">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-1889">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1889">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a><span data-ttu-id="e1135-1890">DXGI_FORMAT_R8G8B8A8 \_ Sint<sup>FNS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="e1135-1890">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FNS</sup> (32)</span></span>
| <span data-ttu-id="e1135-1891">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1891">Target</span></span> | <span data-ttu-id="e1135-1892">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1892">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1893">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1893">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1894">32</span><span class="sxs-lookup"><span data-stu-id="e1135-1894">32</span></span> |
| <span data-ttu-id="e1135-1895">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1895">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-1896">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1896">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1897">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1897">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1898">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1898">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1899">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-1899">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1900">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-1900">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-1901">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-1901">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-1902">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-1902">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-1903">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-1903">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-1904">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-1904">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-1905">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1905">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-1906">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1906">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1907">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1907">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1908">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1908">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1909">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1909">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1910">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1910">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-1911">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1911">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-1912">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1912">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1913">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1913">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1914">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1914">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1915">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1915">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1916">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1916">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1917">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1917">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1918">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1918">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1919">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1919">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1920">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1920">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1921">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1921">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1922">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1922">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1923">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1923">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1924">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1924">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1925">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1925">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1926">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1926">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1927">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1927">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-1928">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1928">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1929">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1929">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1930">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1930">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-1931">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1931">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-1932">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1932">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1933">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1933">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-1934">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1934">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1935">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1935">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1936">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1936">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-1937">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1937">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-1938">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1938">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-1939">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1939">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="e1135-1940">DXGI_FORMAT_R16G16 de \_ <sup>equipos</sup> sin tipo (33)</span><span class="sxs-lookup"><span data-stu-id="e1135-1940">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="e1135-1941">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1941">Target</span></span> | <span data-ttu-id="e1135-1942">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1942">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1943">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1943">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1944">32</span><span class="sxs-lookup"><span data-stu-id="e1135-1944">32</span></span> |
| <span data-ttu-id="e1135-1945">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1945">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-1946">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1946">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1947">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1947">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1948">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1948">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1949">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-1949">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1950">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-1950">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-1951">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-1951">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-1952">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-1952">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-1953">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-1953">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-1954">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-1954">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-1955">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-1955">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-1956">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-1956">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-1957">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-1957">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-1958">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-1958">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-1959">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-1959">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-1960">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-1960">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-1961">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-1961">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-1962">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-1962">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1963">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-1963">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1964">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-1964">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-1965">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-1965">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-1966">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1966">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1967">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-1967">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-1968">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-1968">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-1969">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-1969">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-1970">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1970">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-1971">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-1971">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-1972">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1972">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-1973">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-1973">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-1974">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-1974">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-1975">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1975">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1976">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-1976">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-1977">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-1977">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-1978">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-1978">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1979">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1979">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-1980">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-1980">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-1981">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-1981">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-1982">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-1982">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-1983">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-1983">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-1984">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-1984">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-1985">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1985">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-1986">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1986">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-1987">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-1987">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-1988">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-1988">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-1989">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-1989">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a><span data-ttu-id="e1135-1990">DXGI_FORMAT_R16G16 \_ float<sup>FNS</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="e1135-1990">DXGI_FORMAT_R16G16\_FLOAT<sup>FNS</sup> (34)</span></span>
| <span data-ttu-id="e1135-1991">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-1991">Target</span></span> | <span data-ttu-id="e1135-1992">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-1992">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-1993">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-1993">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-1994">32</span><span class="sxs-lookup"><span data-stu-id="e1135-1994">32</span></span> |
| <span data-ttu-id="e1135-1995">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-1995">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-1997">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-1997">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-1998">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-1998">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2000">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2000">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2001">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2001">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2002">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2002">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2003">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2003">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2005">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2005">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2007">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2007">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2009">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2009">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2011">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2011">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-2012">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2012">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2013">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2013">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2014">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2014">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2015">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2015">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2016">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2016">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2018">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2018">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2020">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2020">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2022">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2022">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2023">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2023">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2024">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2024">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-2025">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2025">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2026">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2026">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2027">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2027">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2028">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2028">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2029">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2029">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2030">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2030">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2031">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2031">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2032">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2032">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2033">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2033">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-2034">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2034">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2035">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2035">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2036">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-2036">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2038">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-2038">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-2040">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2040">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-2042">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-2042">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-2044">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-2044">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2046">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2046">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-2047">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-2047">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-2048">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-2048">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-2049">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2049">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-2050">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2050">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-2051">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2051">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-2052">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-2052">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-2053">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-2053">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a><span data-ttu-id="e1135-2054">DXGI_FORMAT_R16G16 \_ UNORM<sup>FNS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="e1135-2054">DXGI_FORMAT_R16G16\_UNORM<sup>FNS</sup> (35)</span></span>
| <span data-ttu-id="e1135-2055">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-2055">Target</span></span> | <span data-ttu-id="e1135-2056">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-2056">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-2057">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-2057">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-2058">32</span><span class="sxs-lookup"><span data-stu-id="e1135-2058">32</span></span> |
| <span data-ttu-id="e1135-2059">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2059">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2061">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-2061">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2062">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2062">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2063">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2063">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2064">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2064">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2065">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2065">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2066">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2066">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2068">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2068">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2070">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2070">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2072">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2072">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2074">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2074">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2076">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2076">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2077">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2077">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2078">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2078">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2079">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2079">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2080">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2080">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2082">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2082">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2084">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2084">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2086">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2086">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2087">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2088">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-2089">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2090">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2091">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2091">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2092">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2092">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2093">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2093">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2094">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2094">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2095">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2095">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2096">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2096">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2097">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2097">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-2098">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2098">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2099">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2099">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2100">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-2100">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2102">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-2102">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-2104">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2104">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-2106">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-2106">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-2108">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-2108">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2110">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2110">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-2111">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-2111">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-2112">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-2112">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-2113">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2113">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-2114">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2114">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-2115">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2115">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-2116">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-2116">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-2117">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-2117">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a><span data-ttu-id="e1135-2118">DXGI_FORMAT_R16G16 \_ uint<sup>FNS</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="e1135-2118">DXGI_FORMAT_R16G16\_UINT<sup>FNS</sup> (36)</span></span>
| <span data-ttu-id="e1135-2119">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-2119">Target</span></span> | <span data-ttu-id="e1135-2120">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-2120">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-2121">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-2121">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-2122">32</span><span class="sxs-lookup"><span data-stu-id="e1135-2122">32</span></span> |
| <span data-ttu-id="e1135-2123">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2123">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-2124">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-2124">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2125">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2125">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2126">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2126">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2127">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2127">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2128">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2128">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2129">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2129">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-2130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2130">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-2131">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2131">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-2132">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2132">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-2133">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2133">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-2134">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2134">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2135">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2135">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2136">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2136">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2137">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2137">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2138">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2138">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-2139">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2139">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-2140">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2140">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2141">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2141">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2142">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2142">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2143">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2143">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-2144">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2144">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2145">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2145">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2146">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2146">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2147">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2147">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2148">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2148">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2149">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2149">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2150">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2150">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2151">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2151">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2152">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2152">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-2153">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2153">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2154">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2154">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2155">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-2155">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-2156">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-2156">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2157">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2157">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2158">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-2158">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-2159">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-2159">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-2160">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2160">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-2161">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-2161">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-2162">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-2162">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-2163">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2163">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-2164">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2164">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-2165">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2165">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-2166">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-2166">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-2167">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-2167">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a><span data-ttu-id="e1135-2168">DXGI_FORMAT_R16G16 \_ SNORM<sup>FNS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="e1135-2168">DXGI_FORMAT_R16G16\_SNORM<sup>FNS</sup> (37)</span></span>
| <span data-ttu-id="e1135-2169">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-2169">Target</span></span> | <span data-ttu-id="e1135-2170">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-2170">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-2171">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-2171">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-2172">32</span><span class="sxs-lookup"><span data-stu-id="e1135-2172">32</span></span> |
| <span data-ttu-id="e1135-2173">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2173">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2175">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-2175">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2176">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2176">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2178">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2178">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2179">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2179">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2180">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2180">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2181">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2181">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2183">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2185">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2185">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2187">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2187">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2189">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2189">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2191">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2191">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2192">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2192">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2193">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2193">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2194">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2194">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2195">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2195">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2197">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2197">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-2198">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2198">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2199">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2199">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2200">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2200">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2201">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2201">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-2202">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2202">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2203">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2203">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2204">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2204">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2205">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2205">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2206">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2206">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2207">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2207">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2208">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2208">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2209">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2209">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2210">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2210">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-2211">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2211">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2212">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2212">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2213">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-2213">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2215">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-2215">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2216">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2216">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2217">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-2217">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-2218">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-2218">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-2219">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2219">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-2220">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-2220">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-2221">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-2221">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-2222">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2222">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-2223">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2223">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-2224">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2224">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-2225">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-2225">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-2226">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-2226">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a><span data-ttu-id="e1135-2227">DXGI_FORMAT_R16G16 \_ Sint<sup>FNS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="e1135-2227">DXGI_FORMAT_R16G16\_SINT<sup>FNS</sup> (38)</span></span>
| <span data-ttu-id="e1135-2228">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-2228">Target</span></span> | <span data-ttu-id="e1135-2229">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-2229">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-2230">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-2230">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-2231">32</span><span class="sxs-lookup"><span data-stu-id="e1135-2231">32</span></span> |
| <span data-ttu-id="e1135-2232">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2232">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2234">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-2234">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2235">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2235">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2237">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2237">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2238">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2238">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2239">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2239">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2240">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2240">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-2241">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2241">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-2242">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2242">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-2243">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2243">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-2244">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2244">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-2245">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2245">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2246">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2246">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2247">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2247">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2248">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2248">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2249">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2249">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-2250">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2250">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-2251">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2251">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2252">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2252">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2253">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2253">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2254">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2254">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-2255">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2255">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2256">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2256">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2257">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2257">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2258">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2258">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2259">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2259">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2260">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2260">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2261">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2261">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2262">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2262">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2263">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2263">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-2264">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2264">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2265">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2265">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2266">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-2266">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-2267">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-2267">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2268">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2268">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2269">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-2269">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-2270">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-2270">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-2271">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2271">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-2272">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-2272">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-2273">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-2273">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-2274">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2274">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-2275">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2275">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-2276">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2276">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-2277">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-2277">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-2278">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-2278">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="e1135-2279">DXGI_FORMAT_R32 de \_ <sup>equipos</sup> sin tipo (39)</span><span class="sxs-lookup"><span data-stu-id="e1135-2279">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="e1135-2280">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-2280">Target</span></span> | <span data-ttu-id="e1135-2281">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-2281">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-2282">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-2282">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-2283">32</span><span class="sxs-lookup"><span data-stu-id="e1135-2283">32</span></span> |
| <span data-ttu-id="e1135-2284">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2284">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-2285">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-2285">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2286">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2286">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2287">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2287">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2288">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2288">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2289">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2289">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2290">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2290">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-2291">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2291">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-2292">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2292">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-2293">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2293">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-2294">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2294">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-2295">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2295">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2296">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2296">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2297">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2297">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2298">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2298">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2299">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2299">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-2300">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2300">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-2301">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2301">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2302">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2302">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2303">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2303">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2304">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2304">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-2305">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2305">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2306">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2306">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2307">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2307">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2308">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2308">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2309">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2309">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2310">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2310">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2311">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2311">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2312">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2312">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2313">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2313">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-2314">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2314">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2315">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2315">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2316">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-2316">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-2317">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-2317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2318">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2319">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-2319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-2320">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-2320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-2321">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2321">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-2322">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-2322">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-2323">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-2323">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-2324">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2324">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-2325">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2325">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-2326">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2326">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-2327">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-2327">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-2328">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-2328">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a><span data-ttu-id="e1135-2329">DXGI_FORMAT_D32 \_ float<sup>FNS</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="e1135-2329">DXGI_FORMAT_D32\_FLOAT<sup>FNS</sup> (40)</span></span>
| <span data-ttu-id="e1135-2330">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-2330">Target</span></span> | <span data-ttu-id="e1135-2331">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-2331">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-2332">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-2332">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-2333">32</span><span class="sxs-lookup"><span data-stu-id="e1135-2333">32</span></span> |
| <span data-ttu-id="e1135-2334">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2334">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-2335">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-2335">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2336">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2336">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2337">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2337">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2338">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2338">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2339">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2339">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2340">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2340">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-2341">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2341">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-2342">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2342">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-2343">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2343">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-2344">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2344">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-2345">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2345">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2346">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2346">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2347">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2347">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2348">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2348">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2349">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2349">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-2350">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2350">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-2351">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2351">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2352">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2352">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2353">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2353">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2354">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2354">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-2355">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2355">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2356">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2356">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2357">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2357">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2358">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2358">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2359">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2359">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2360">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2360">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2361">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2361">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2362">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2362">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2363">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2363">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-2364">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2364">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2365">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2365">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2366">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-2366">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-2367">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-2367">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2368">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2368">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2369">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-2369">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-2370">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-2370">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-2371">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2371">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-2372">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-2372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-2373">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-2373">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-2374">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-2375">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-2376">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-2377">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-2377">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-2378">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-2378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a><span data-ttu-id="e1135-2379">DXGI_FORMAT_R32 \_ float<sup>FNS</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="e1135-2379">DXGI_FORMAT_R32\_FLOAT<sup>FNS</sup> (41)</span></span>
| <span data-ttu-id="e1135-2380">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-2380">Target</span></span> | <span data-ttu-id="e1135-2381">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-2381">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-2382">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-2382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-2383">32</span><span class="sxs-lookup"><span data-stu-id="e1135-2383">32</span></span> |
| <span data-ttu-id="e1135-2384">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2384">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2386">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-2386">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2387">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2387">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2389">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2390">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2391">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2392">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2394">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2394">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2396">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2396">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2398">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2398">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2400">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-2401">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2401">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2402">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2402">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2403">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2403">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2404">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2404">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2405">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2405">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2407">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2407">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2409">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2409">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2411">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2411">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2412">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2412">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2413">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2413">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-2414">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2414">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2415">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2415">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2416">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2416">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2417">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2417">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2418">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2418">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2419">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2419">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2420">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2420">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2421">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2421">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2422">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2422">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-2423">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2423">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2424">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2424">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2425">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-2425">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2427">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-2427">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-2429">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2429">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-2431">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-2431">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-2433">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-2433">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2435">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2435">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-2436">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-2436">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-2437">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-2437">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-2438">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2438">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-2439">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2439">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-2440">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2440">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-2441">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-2441">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-2442">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-2442">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a><span data-ttu-id="e1135-2443">DXGI_FORMAT_R32 \_ uint<sup>FNS</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="e1135-2443">DXGI_FORMAT_R32\_UINT<sup>FNS</sup> (42)</span></span>
| <span data-ttu-id="e1135-2444">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-2444">Target</span></span> | <span data-ttu-id="e1135-2445">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-2445">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-2446">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-2446">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-2447">32</span><span class="sxs-lookup"><span data-stu-id="e1135-2447">32</span></span> |
| <span data-ttu-id="e1135-2448">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2448">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2450">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-2450">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2451">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2451">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2452">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2452">Input Assembler Index Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2454">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2454">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2455">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2455">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2456">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2456">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-2457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2457">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-2458">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2458">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-2459">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2459">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-2460">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2460">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-2461">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2461">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2462">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2462">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2463">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2463">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2464">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2464">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2465">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2465">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-2466">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2466">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-2467">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2467">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2468">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2468">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2469">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2469">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2470">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2470">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-2471">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2471">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2472">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2472">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2473">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2473">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2474">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2474">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2475">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2475">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2476">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2476">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2477">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2477">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2478">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2478">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2479">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2479">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-2480">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2480">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2481">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2481">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2482">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-2482">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-2483">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-2483">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2484">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2484">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2485">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-2485">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-2486">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-2486">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-2487">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2487">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-2488">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-2488">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-2489">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-2489">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-2490">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2490">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-2491">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2491">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-2492">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2492">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-2493">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-2493">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-2494">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-2494">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a><span data-ttu-id="e1135-2495">DXGI_FORMAT_R32 \_ Sint<sup>FNS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="e1135-2495">DXGI_FORMAT_R32\_SINT<sup>FNS</sup> (43)</span></span>
| <span data-ttu-id="e1135-2496">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-2496">Target</span></span> | <span data-ttu-id="e1135-2497">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-2497">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-2498">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-2498">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-2499">32</span><span class="sxs-lookup"><span data-stu-id="e1135-2499">32</span></span> |
| <span data-ttu-id="e1135-2500">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2500">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-2501">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-2501">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2502">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2502">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2503">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2503">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2504">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2504">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2505">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2505">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2506">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2506">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-2507">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2507">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-2508">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2508">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-2509">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2509">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-2510">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2510">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-2511">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2511">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2512">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2512">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2513">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2513">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2514">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2514">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2515">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2515">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-2516">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2516">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-2517">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2517">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2518">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2518">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2519">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2519">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2520">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2520">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-2521">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2521">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2522">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2522">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2523">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2523">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2524">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2524">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2525">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2525">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2526">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2526">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2527">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2527">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2528">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2528">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2529">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2529">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-2530">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2530">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2531">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2531">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2532">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-2532">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-2533">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-2533">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2534">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2534">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2535">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-2535">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-2536">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-2536">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-2537">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2537">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-2538">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-2538">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-2539">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-2539">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-2540">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2540">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-2541">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2541">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-2542">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2542">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-2543">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-2543">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-2544">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-2544">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="e1135-2545">DXGI_FORMAT_R24G8 de \_ <sup>equipos</sup> sin tipo (44)</span><span class="sxs-lookup"><span data-stu-id="e1135-2545">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="e1135-2546">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-2546">Target</span></span> | <span data-ttu-id="e1135-2547">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-2547">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-2548">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-2548">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-2549">32</span><span class="sxs-lookup"><span data-stu-id="e1135-2549">32</span></span> |
| <span data-ttu-id="e1135-2550">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2550">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-2551">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-2551">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2552">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2552">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2553">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2553">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2554">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2554">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2555">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2555">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2556">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2556">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-2557">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2557">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-2558">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2558">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-2559">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2559">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-2560">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2560">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-2561">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2561">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2562">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2562">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2563">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2563">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2564">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2564">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2565">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2565">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-2566">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2566">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-2567">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2567">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2568">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2568">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2569">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2569">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2570">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2570">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-2571">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2571">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2572">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2572">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2573">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2573">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2574">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2574">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2575">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2575">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2576">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2576">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2577">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2577">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2578">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2578">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2579">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2579">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-2580">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2580">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2581">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2581">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2582">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-2582">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-2583">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-2583">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2584">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2584">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2585">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-2585">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-2586">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-2586">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-2587">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2587">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-2588">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-2588">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-2589">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-2589">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-2590">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2590">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-2591">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2591">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-2592">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2592">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-2593">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-2593">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-2594">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-2594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a><span data-ttu-id="e1135-2595">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FNS</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="e1135-2595">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FNS</sup> (45)</span></span>
| <span data-ttu-id="e1135-2596">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-2596">Target</span></span> | <span data-ttu-id="e1135-2597">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-2597">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-2598">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-2598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-2599">32</span><span class="sxs-lookup"><span data-stu-id="e1135-2599">32</span></span> |
| <span data-ttu-id="e1135-2600">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2600">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2602">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-2602">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2603">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2603">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2604">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2604">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2605">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2605">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2606">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2606">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2607">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2607">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2609">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2609">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-2610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2610">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-2611">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2611">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-2612">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2612">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-2613">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2614">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2615">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2615">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2616">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2617">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2617">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-2618">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2618">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-2619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2619">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2620">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2620">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2621">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2621">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2622">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2622">Depth/Stencil Target</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2624">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2624">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2625">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2625">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2626">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2626">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2627">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2627">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2628">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2628">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2629">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2629">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2630">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2630">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2631">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2631">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2632">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2632">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-2633">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2633">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2634">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2634">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2635">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-2635">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-2636">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-2636">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-2638">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2638">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-2640">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-2640">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-2642">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-2642">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-2643">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2643">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-2644">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-2644">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-2645">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-2645">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-2646">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2646">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-2647">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2647">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-2648">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2648">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-2649">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-2649">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-2650">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-2650">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a><span data-ttu-id="e1135-2651">DXGI_FORMAT_R24 \_ UNORM \_ X8 \_ <sup>FNS</sup> sin tipo (46)</span><span class="sxs-lookup"><span data-stu-id="e1135-2651">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FNS</sup> (46)</span></span>
| <span data-ttu-id="e1135-2652">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-2652">Target</span></span> | <span data-ttu-id="e1135-2653">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-2653">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-2654">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-2654">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-2655">32</span><span class="sxs-lookup"><span data-stu-id="e1135-2655">32</span></span> |
| <span data-ttu-id="e1135-2656">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2656">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-2657">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-2657">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2658">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2658">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2659">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2659">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2660">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2660">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2661">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2661">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2662">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2662">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-2663">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2663">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-2664">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2664">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-2665">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2665">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-2666">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2666">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-2667">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2667">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2668">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2668">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2669">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2669">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2670">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2670">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2671">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2671">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-2672">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2672">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-2673">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2673">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2674">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2674">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2675">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2675">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2676">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2676">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-2677">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2677">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2678">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2678">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2679">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2679">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2680">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2680">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2681">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2681">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2682">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2682">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2683">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2683">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2684">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2684">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2685">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2685">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-2686">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2686">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2687">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2687">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2688">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-2688">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-2689">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-2689">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2690">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2690">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2691">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-2691">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-2692">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-2692">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-2693">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2693">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-2694">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-2694">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-2695">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-2695">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-2696">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2696">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-2697">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2697">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-2698">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2698">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-2699">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-2699">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-2700">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-2700">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a><span data-ttu-id="e1135-2701">DXGI_FORMAT_X24 \_ tipos de \_ G8 \_ <sup>FNS</sup> (47)</span><span class="sxs-lookup"><span data-stu-id="e1135-2701">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FNS</sup> (47)</span></span>
| <span data-ttu-id="e1135-2702">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-2702">Target</span></span> | <span data-ttu-id="e1135-2703">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-2703">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-2704">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-2704">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-2705">32</span><span class="sxs-lookup"><span data-stu-id="e1135-2705">32</span></span> |
| <span data-ttu-id="e1135-2706">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2706">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-2707">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-2707">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2708">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2708">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2709">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2709">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2710">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2710">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2711">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2711">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2712">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2712">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-2713">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2713">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-2714">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2714">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-2715">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2715">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-2716">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2716">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-2717">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2717">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2718">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2718">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2719">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2719">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2720">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2720">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2721">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2721">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-2722">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2722">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-2723">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2723">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2724">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2724">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2725">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2725">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2726">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2726">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-2727">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2727">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2728">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2728">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2729">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2729">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2730">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2730">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2731">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2731">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2732">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2732">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2733">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2733">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2734">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2734">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2735">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2735">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-2736">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2736">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2737">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2737">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2738">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-2738">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-2739">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-2739">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2740">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2740">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2741">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-2741">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-2742">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-2742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-2743">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2743">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-2744">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-2744">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-2745">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-2745">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-2746">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2746">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-2747">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2747">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-2748">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2748">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-2749">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-2749">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-2750">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-2750">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="e1135-2751">DXGI_FORMAT_R8G8 de \_ <sup>equipos</sup> sin tipo (48)</span><span class="sxs-lookup"><span data-stu-id="e1135-2751">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="e1135-2752">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-2752">Target</span></span> | <span data-ttu-id="e1135-2753">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-2753">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-2754">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-2754">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-2755">16</span><span class="sxs-lookup"><span data-stu-id="e1135-2755">16</span></span> |
| <span data-ttu-id="e1135-2756">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2756">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-2757">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-2757">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2758">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2758">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2759">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2760">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2761">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2762">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2762">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-2763">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2763">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-2764">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2764">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-2765">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2765">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-2766">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2766">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-2767">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2767">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2768">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2768">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2769">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2769">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2770">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2770">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2771">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2771">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-2772">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2772">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-2773">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2773">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2774">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2774">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2775">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2775">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2776">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2776">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-2777">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2777">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2778">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2778">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2779">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2779">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2780">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2780">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2781">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2781">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2782">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2782">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2783">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2783">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2784">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2784">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2785">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2785">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-2786">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2786">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2787">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2787">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2788">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-2788">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-2789">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-2789">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2790">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2790">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2791">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-2791">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-2792">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-2792">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-2793">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2793">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-2794">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-2794">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-2795">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-2795">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-2796">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2796">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-2797">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2797">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-2798">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2798">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-2799">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-2799">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-2800">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-2800">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a><span data-ttu-id="e1135-2801">DXGI_FORMAT_R8G8 \_ UNORM<sup>FNS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="e1135-2801">DXGI_FORMAT_R8G8\_UNORM<sup>FNS</sup> (49)</span></span>
| <span data-ttu-id="e1135-2802">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-2802">Target</span></span> | <span data-ttu-id="e1135-2803">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-2803">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-2804">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-2804">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-2805">16</span><span class="sxs-lookup"><span data-stu-id="e1135-2805">16</span></span> |
| <span data-ttu-id="e1135-2806">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2806">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2808">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-2808">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2809">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2809">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2810">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2810">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2811">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2811">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2812">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2812">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2813">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2813">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2815">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2815">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-2816">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2816">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-2817">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2817">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2819">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2819">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2821">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2821">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2822">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2822">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2823">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2823">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2824">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2824">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2825">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2825">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-2826">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2826">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-2827">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2827">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2829">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2829">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2831">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2831">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2832">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2832">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-2833">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2833">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2834">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2834">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2835">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2835">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2836">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2836">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2837">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2837">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2838">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2838">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2839">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2839">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2840">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2840">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2841">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2841">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-2842">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2842">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2843">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2843">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2844">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-2844">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2846">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-2846">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2847">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2847">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2848">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-2848">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-2849">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-2849">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-2850">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2850">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-2851">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-2851">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-2852">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-2852">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-2853">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2853">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-2854">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2854">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-2855">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2855">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-2856">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-2856">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2858">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-2858">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a><span data-ttu-id="e1135-2859">DXGI_FORMAT_R8G8 \_ uint<sup>FNS</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="e1135-2859">DXGI_FORMAT_R8G8\_UINT<sup>FNS</sup> (50)</span></span>
| <span data-ttu-id="e1135-2860">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-2860">Target</span></span> | <span data-ttu-id="e1135-2861">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-2861">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-2862">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-2862">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-2863">16</span><span class="sxs-lookup"><span data-stu-id="e1135-2863">16</span></span> |
| <span data-ttu-id="e1135-2864">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2864">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-2865">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-2865">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2866">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2866">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2867">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2867">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2868">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2868">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2869">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2869">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2870">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2870">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-2871">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2871">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-2872">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2872">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-2873">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2873">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-2874">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2874">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-2875">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2875">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2876">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2876">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2877">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2877">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2878">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2878">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2879">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2879">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-2880">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2880">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-2881">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2881">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2882">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2883">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2884">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-2885">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2886">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2887">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2887">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2888">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2888">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2889">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2889">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2890">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2890">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2891">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2891">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2892">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2892">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2893">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2893">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-2894">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2894">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2895">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2895">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2896">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-2896">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-2897">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-2897">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2898">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2898">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2899">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-2899">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-2900">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-2900">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-2901">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2901">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-2902">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-2902">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-2903">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-2903">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-2904">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-2905">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-2906">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-2907">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-2907">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-2908">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-2908">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a><span data-ttu-id="e1135-2909">DXGI_FORMAT_R8G8 \_ SNORM<sup>FNS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="e1135-2909">DXGI_FORMAT_R8G8\_SNORM<sup>FNS</sup> (51)</span></span>
| <span data-ttu-id="e1135-2910">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-2910">Target</span></span> | <span data-ttu-id="e1135-2911">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-2911">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-2912">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-2912">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-2913">16</span><span class="sxs-lookup"><span data-stu-id="e1135-2913">16</span></span> |
| <span data-ttu-id="e1135-2914">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2914">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2916">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-2916">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2917">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2917">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2918">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2918">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2919">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2919">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2920">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2920">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2921">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2921">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2923">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2923">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-2924">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2924">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-2925">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2925">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2927">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2927">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2929">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2929">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2930">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2930">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2931">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2931">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2932">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2932">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2933">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2933">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2935">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2935">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-2936">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2936">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2937">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2937">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2938">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2938">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2939">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2939">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-2940">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2940">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2941">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2941">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2942">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2942">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2943">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2943">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2944">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2944">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2945">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2945">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2946">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2946">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2947">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2947">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2948">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2948">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-2949">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2949">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2950">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-2950">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-2951">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-2951">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-2953">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-2953">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2954">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2954">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2955">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-2955">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-2956">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-2956">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-2957">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-2957">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-2958">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-2958">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-2959">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-2959">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-2960">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2960">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-2961">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2961">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-2962">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-2962">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-2963">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-2963">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-2964">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-2964">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a><span data-ttu-id="e1135-2965">DXGI_FORMAT_R8G8 \_ Sint<sup>FNS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="e1135-2965">DXGI_FORMAT_R8G8\_SINT<sup>FNS</sup> (52)</span></span>
| <span data-ttu-id="e1135-2966">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-2966">Target</span></span> | <span data-ttu-id="e1135-2967">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-2967">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-2968">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-2968">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-2969">16</span><span class="sxs-lookup"><span data-stu-id="e1135-2969">16</span></span> |
| <span data-ttu-id="e1135-2970">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2970">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-2971">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-2971">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2972">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2972">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2973">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-2973">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2974">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-2974">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-2975">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-2975">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-2976">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-2976">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-2977">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-2977">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-2978">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-2978">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-2979">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-2979">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-2980">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-2980">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-2981">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-2981">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-2982">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-2982">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-2983">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-2983">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-2984">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-2984">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-2985">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-2985">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-2986">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-2986">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-2987">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-2987">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2988">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-2988">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-2989">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-2989">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-2990">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-2990">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-2991">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-2991">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2992">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-2992">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-2993">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-2993">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-2994">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-2994">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-2995">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2995">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-2996">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-2996">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-2997">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2997">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-2998">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-2998">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-2999">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-2999">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3000">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3000">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3001">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3001">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3002">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3002">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-3003">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3003">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3004">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3004">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3005">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3005">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-3006">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3006">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3007">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3007">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3008">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3008">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3009">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3009">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3010">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3010">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3011">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3011">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3012">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3012">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3013">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3013">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-3014">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3014">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="e1135-3015">DXGI_FORMAT_R16 de \_ <sup>equipos</sup> sin tipo (53)</span><span class="sxs-lookup"><span data-stu-id="e1135-3015">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="e1135-3016">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3016">Target</span></span> | <span data-ttu-id="e1135-3017">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3017">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3018">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3018">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3019">16</span><span class="sxs-lookup"><span data-stu-id="e1135-3019">16</span></span> |
| <span data-ttu-id="e1135-3020">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3020">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-3021">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3021">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3022">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3022">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3023">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3023">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3024">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3024">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3025">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3025">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3026">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3026">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-3027">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3027">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-3028">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3028">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-3029">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3029">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-3030">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3030">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-3031">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3032">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3033">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3033">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3034">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3035">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3035">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-3036">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3036">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3037">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3037">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3038">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3038">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3039">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3039">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3040">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3040">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-3041">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3041">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3042">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3042">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3043">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3043">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3044">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3044">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3045">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3045">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3046">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3046">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3047">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3047">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3048">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3048">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-3049">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3049">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3050">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3050">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3051">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3051">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3052">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3052">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-3053">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3053">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3054">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3054">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3055">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3055">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-3056">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3056">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3057">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3057">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3058">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3058">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3059">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3059">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3060">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3060">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3061">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3061">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3062">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3062">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3063">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3063">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-3064">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3064">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a><span data-ttu-id="e1135-3065">DXGI_FORMAT_R16 \_ float<sup>FNS</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="e1135-3065">DXGI_FORMAT_R16\_FLOAT<sup>FNS</sup> (54)</span></span>
| <span data-ttu-id="e1135-3066">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3066">Target</span></span> | <span data-ttu-id="e1135-3067">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3067">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3068">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3068">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3069">16</span><span class="sxs-lookup"><span data-stu-id="e1135-3069">16</span></span> |
| <span data-ttu-id="e1135-3070">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3070">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-3071">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3071">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3072">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3072">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3073">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3073">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3074">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3074">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3075">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3075">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3076">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3076">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-3077">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3077">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-3078">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3078">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-3079">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3079">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-3080">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3080">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-3081">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3081">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3082">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3082">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3083">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3083">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3084">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3084">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3085">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3085">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-3086">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3086">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3087">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3087">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3088">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3088">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3089">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3089">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3090">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3090">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-3091">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3091">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3092">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3092">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3093">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3093">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3094">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3094">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3095">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3095">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3096">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3096">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3097">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3097">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3098">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3098">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-3099">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3099">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3100">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3100">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3101">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3101">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3102">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3102">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-3103">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3103">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3104">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3104">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3105">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3105">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-3106">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3106">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3107">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3107">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3108">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3108">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3109">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3109">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3110">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3111">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3112">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3113">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3113">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-3114">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3114">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a><span data-ttu-id="e1135-3115">DXGI_FORMAT_D16 \_ UNORM<sup>FNS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="e1135-3115">DXGI_FORMAT_D16\_UNORM<sup>FNS</sup> (55)</span></span>
| <span data-ttu-id="e1135-3116">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3116">Target</span></span> | <span data-ttu-id="e1135-3117">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3117">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3118">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3118">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3119">16</span><span class="sxs-lookup"><span data-stu-id="e1135-3119">16</span></span> |
| <span data-ttu-id="e1135-3120">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3120">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3122">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3122">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3123">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3123">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3124">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3124">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3125">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3125">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3126">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3127">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3127">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3129">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3129">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-3130">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3130">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-3131">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3131">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-3132">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3132">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-3133">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3133">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3134">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3134">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3135">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3135">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3136">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3136">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3137">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3137">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-3138">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3138">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3139">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3139">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3140">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3140">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3141">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3141">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3142">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3142">Depth/Stencil Target</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3144">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3144">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3145">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3145">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3146">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3146">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3147">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3147">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3148">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3148">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3149">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3149">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3150">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3150">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3151">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3151">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-3152">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3152">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3153">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3153">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3154">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3154">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3155">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3155">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-3156">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3156">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-3158">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3158">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-3160">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3160">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-3162">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3163">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3163">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3164">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3165">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3166">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3167">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3168">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3169">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3169">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-3170">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a><span data-ttu-id="e1135-3171">DXGI_FORMAT_R16 \_ UNORM<sup>FNS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="e1135-3171">DXGI_FORMAT_R16\_UNORM<sup>FNS</sup> (56)</span></span>
| <span data-ttu-id="e1135-3172">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3172">Target</span></span> | <span data-ttu-id="e1135-3173">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3173">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3174">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3175">16</span><span class="sxs-lookup"><span data-stu-id="e1135-3175">16</span></span> |
| <span data-ttu-id="e1135-3176">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3176">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3178">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3178">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3179">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3179">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3180">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3180">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3181">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3181">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3182">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3182">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3183">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3183">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3185">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3185">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3187">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3187">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3189">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3189">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3191">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3191">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3193">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3193">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3194">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3194">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3195">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3195">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3196">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3196">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3197">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3197">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3199">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3199">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3200">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3200">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3201">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3201">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3202">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3202">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3203">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3203">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-3204">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3204">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3205">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3205">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3206">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3206">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3207">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3207">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3208">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3208">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3209">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3209">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3210">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3210">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3211">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3211">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-3212">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3212">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3213">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3213">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3214">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3214">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3215">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3215">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3217">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3217">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3218">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3218">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3219">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3219">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-3220">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3220">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3221">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3221">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3222">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3222">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3223">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3223">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3224">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3224">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3225">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3225">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3226">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3226">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3227">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3227">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-3228">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3228">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a><span data-ttu-id="e1135-3229">DXGI_FORMAT_R16 \_ uint<sup>FNS</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="e1135-3229">DXGI_FORMAT_R16\_UINT<sup>FNS</sup> (57)</span></span>
| <span data-ttu-id="e1135-3230">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3230">Target</span></span> | <span data-ttu-id="e1135-3231">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3231">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3232">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3232">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3233">16</span><span class="sxs-lookup"><span data-stu-id="e1135-3233">16</span></span> |
| <span data-ttu-id="e1135-3234">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3234">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3236">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3236">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3237">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3237">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3238">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3238">Input Assembler Index Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3240">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3240">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3241">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3241">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3242">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3242">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-3243">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3243">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-3244">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3244">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-3245">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3245">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-3246">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3246">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-3247">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3247">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3248">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3248">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3249">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3249">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3250">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3250">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3251">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3251">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-3252">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3252">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3253">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3253">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3254">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3254">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3255">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3255">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3256">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3256">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-3257">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3257">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3258">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3258">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3259">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3259">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3260">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3260">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3261">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3261">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3262">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3262">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3263">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3263">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3264">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3264">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-3265">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3265">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3266">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3266">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3267">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3267">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3268">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3268">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-3269">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3269">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3270">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3270">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3271">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3271">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-3272">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3272">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3273">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3273">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3274">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3274">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3275">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3275">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3276">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3276">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3277">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3277">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3278">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3278">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3279">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3279">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-3280">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3280">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a><span data-ttu-id="e1135-3281">DXGI_FORMAT_R16 \_ SNORM<sup>FNS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="e1135-3281">DXGI_FORMAT_R16\_SNORM<sup>FNS</sup> (58)</span></span>
| <span data-ttu-id="e1135-3282">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3282">Target</span></span> | <span data-ttu-id="e1135-3283">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3283">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3284">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3284">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3285">16</span><span class="sxs-lookup"><span data-stu-id="e1135-3285">16</span></span> |
| <span data-ttu-id="e1135-3286">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3286">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-3287">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3287">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3288">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3288">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3289">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3289">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3290">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3290">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3291">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3291">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3292">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3292">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-3293">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3293">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-3294">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3294">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-3295">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3295">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-3296">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3296">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-3297">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3297">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3298">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3298">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3299">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3299">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3300">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3300">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3301">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3301">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-3302">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3302">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3303">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3303">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3304">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3304">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3305">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3305">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3306">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3306">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-3307">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3307">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3308">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3308">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3309">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3309">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3310">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3310">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3311">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3311">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3312">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3312">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3313">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3313">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3314">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3314">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-3315">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3315">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3316">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3316">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3317">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3317">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3318">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3318">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-3319">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3319">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3320">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3320">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3321">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3321">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-3322">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3322">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3323">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3323">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3324">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3324">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3325">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3325">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3326">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3326">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3327">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3327">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3328">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3328">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3329">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3329">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-3330">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3330">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a><span data-ttu-id="e1135-3331">DXGI_FORMAT_R16 \_ Sint<sup>FNS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="e1135-3331">DXGI_FORMAT_R16\_SINT<sup>FNS</sup> (59)</span></span>
| <span data-ttu-id="e1135-3332">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3332">Target</span></span> | <span data-ttu-id="e1135-3333">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3333">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3334">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3334">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3335">16</span><span class="sxs-lookup"><span data-stu-id="e1135-3335">16</span></span> |
| <span data-ttu-id="e1135-3336">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3336">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-3337">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3337">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3338">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3338">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3339">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3339">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3340">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3340">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3341">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3341">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3342">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3342">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-3343">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3343">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-3344">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3344">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-3345">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3345">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-3346">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3346">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-3347">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3347">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3348">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3348">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3349">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3349">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3350">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3350">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3351">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3351">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-3352">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3352">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3353">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3353">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3354">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3354">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3355">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3355">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3356">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3356">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-3357">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3357">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3358">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3358">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3359">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3359">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3360">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3360">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3361">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3361">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3362">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3362">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3363">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3363">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3364">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3364">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-3365">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3365">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3366">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3366">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3367">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3367">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3368">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3368">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-3369">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3369">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3370">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3370">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3371">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3371">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-3372">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3372">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3373">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3373">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3374">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3374">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3375">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3375">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3376">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3376">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3377">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3377">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3378">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3378">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3379">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3379">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-3380">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3380">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="e1135-3381">DXGI_FORMAT_R8 de \_ <sup>equipos</sup> sin tipo (60)</span><span class="sxs-lookup"><span data-stu-id="e1135-3381">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="e1135-3382">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3382">Target</span></span> | <span data-ttu-id="e1135-3383">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3383">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3384">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3384">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3385">8</span><span class="sxs-lookup"><span data-stu-id="e1135-3385">8</span></span> |
| <span data-ttu-id="e1135-3386">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3386">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-3387">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3387">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3388">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3388">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3389">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3390">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3391">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3392">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-3393">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3393">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-3394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3394">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-3395">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3395">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-3396">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3396">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-3397">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3397">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3398">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3398">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3399">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3399">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3400">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3400">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3401">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3401">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-3402">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3402">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3403">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3403">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3404">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3404">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3405">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3405">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3406">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3406">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-3407">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3407">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3408">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3408">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3409">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3409">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3410">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3410">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3411">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3411">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3412">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3412">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3413">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3413">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3414">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3414">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-3415">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3415">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3416">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3416">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3417">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3417">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3418">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3418">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-3419">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3419">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3420">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3420">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3421">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3421">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-3422">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3422">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3423">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3423">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3424">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3424">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3425">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3425">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3426">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3426">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3427">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3427">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3428">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3428">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3429">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3429">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-3430">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3430">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a><span data-ttu-id="e1135-3431">DXGI_FORMAT_R8 \_ UNORM<sup>FNS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="e1135-3431">DXGI_FORMAT_R8\_UNORM<sup>FNS</sup> (61)</span></span>
| <span data-ttu-id="e1135-3432">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3432">Target</span></span> | <span data-ttu-id="e1135-3433">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3433">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3434">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3434">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3435">8</span><span class="sxs-lookup"><span data-stu-id="e1135-3435">8</span></span> |
| <span data-ttu-id="e1135-3436">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3436">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3438">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3438">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3439">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3439">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3440">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3440">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3441">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3441">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3442">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3442">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3443">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3443">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3445">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3445">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3447">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3447">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3449">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3449">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3451">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3451">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3453">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3454">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3455">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3455">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3456">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3457">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3457">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3459">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3459">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3460">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3460">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3462">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3462">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3464">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3465">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-3466">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3467">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3468">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3468">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3469">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3470">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3471">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3472">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3473">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3473">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-3474">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3475">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3476">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3477">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3477">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3479">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3479">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3480">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3480">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3481">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3481">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-3482">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3482">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3483">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3483">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3484">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3484">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3485">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3485">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3486">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3486">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3487">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3487">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3488">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3488">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3489">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3489">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3491">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3491">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a><span data-ttu-id="e1135-3492">DXGI_FORMAT_R8 \_ uint<sup>FNS</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="e1135-3492">DXGI_FORMAT_R8\_UINT<sup>FNS</sup> (62)</span></span>
| <span data-ttu-id="e1135-3493">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3493">Target</span></span> | <span data-ttu-id="e1135-3494">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3494">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3495">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3495">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3496">8</span><span class="sxs-lookup"><span data-stu-id="e1135-3496">8</span></span> |
| <span data-ttu-id="e1135-3497">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3497">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-3498">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3498">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3499">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3499">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3500">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3500">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3501">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3501">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3502">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3502">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3503">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3503">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-3504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3504">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-3505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3505">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-3506">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3506">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-3507">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3507">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-3508">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3509">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3510">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3510">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3511">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3512">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3512">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-3513">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3513">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3514">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3514">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3515">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3515">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3516">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3516">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3517">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3517">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-3518">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3518">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3519">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3519">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3520">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3520">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3521">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3521">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3522">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3522">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3523">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3523">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3524">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3524">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3525">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3525">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-3526">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3526">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3527">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3527">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3528">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3528">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3529">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3529">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-3530">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3530">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3531">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3531">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3532">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-3533">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3534">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3534">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3535">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3536">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3537">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3538">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3539">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3540">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3540">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-3541">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a><span data-ttu-id="e1135-3542">DXGI_FORMAT_R8 \_ SNORM<sup>FNS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="e1135-3542">DXGI_FORMAT_R8\_SNORM<sup>FNS</sup> (63)</span></span>
| <span data-ttu-id="e1135-3543">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3543">Target</span></span> | <span data-ttu-id="e1135-3544">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3544">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3545">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3546">8</span><span class="sxs-lookup"><span data-stu-id="e1135-3546">8</span></span> |
| <span data-ttu-id="e1135-3547">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3547">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-3548">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3548">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3549">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3550">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3551">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3552">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3553">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-3554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3554">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-3555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3555">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-3556">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-3557">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-3558">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3559">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3560">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3560">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3561">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3562">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3562">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-3563">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3564">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3564">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3565">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3566">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3567">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-3568">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3569">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3570">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3570">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3571">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3572">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3573">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3574">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3575">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-3576">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3577">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3578">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3579">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-3580">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3581">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3582">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-3583">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3584">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3584">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3585">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3586">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3587">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3587">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3588">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3588">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3589">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3589">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3590">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3590">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-3591">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3591">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a><span data-ttu-id="e1135-3592">DXGI_FORMAT_R8 \_ Sint<sup>FNS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="e1135-3592">DXGI_FORMAT_R8\_SINT<sup>FNS</sup> (64)</span></span>
| <span data-ttu-id="e1135-3593">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3593">Target</span></span> | <span data-ttu-id="e1135-3594">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3594">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3595">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3595">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3596">8</span><span class="sxs-lookup"><span data-stu-id="e1135-3596">8</span></span> |
| <span data-ttu-id="e1135-3597">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3597">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-3598">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3598">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3599">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3599">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3600">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3601">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3602">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3603">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-3604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3604">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-3605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3605">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-3606">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-3607">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-3608">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3609">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3610">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3610">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3611">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3612">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3612">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-3613">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3614">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3615">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3616">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3617">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-3618">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3619">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3620">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3620">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3621">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3622">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3623">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3624">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-3626">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3627">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3628">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3629">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3629">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-3630">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3630">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3631">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3631">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3632">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3632">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-3633">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3633">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3634">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3634">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3635">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3635">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3636">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3636">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3637">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3637">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3638">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3638">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3639">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3639">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3640">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3640">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-3641">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3641">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="e1135-3642">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="e1135-3642">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="e1135-3643">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3643">Target</span></span> | <span data-ttu-id="e1135-3644">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3644">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3645">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3645">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3646">8</span><span class="sxs-lookup"><span data-stu-id="e1135-3646">8</span></span> |
| <span data-ttu-id="e1135-3647">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3647">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3649">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3649">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3650">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3650">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3651">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3651">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3652">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3652">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3653">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3654">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3654">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3656">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3656">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3658">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3658">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3660">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3660">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3662">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3662">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3664">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3665">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3666">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3666">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3667">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3668">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3668">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-3669">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3669">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3670">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3670">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3672">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3672">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3674">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3675">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-3676">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3677">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3678">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3678">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3679">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3680">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3681">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3682">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3683">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3683">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-3684">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3685">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3686">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3687">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3687">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3689">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3689">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3690">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3690">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3691">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3691">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-3692">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3692">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3693">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3693">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3694">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3694">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3695">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3695">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3696">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3696">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3697">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3697">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3698">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3698">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3699">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3699">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3701">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="e1135-3702">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="e1135-3702">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="e1135-3703">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3703">Target</span></span> | <span data-ttu-id="e1135-3704">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3704">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3705">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3706">32</span><span class="sxs-lookup"><span data-stu-id="e1135-3706">32</span></span> |
| <span data-ttu-id="e1135-3707">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3707">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-3708">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3708">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3709">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3709">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3710">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3710">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3711">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3711">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3712">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3712">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3713">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3713">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-3714">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3714">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-3715">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3715">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-3716">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3716">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-3717">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3717">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-3718">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3718">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3719">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3719">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3720">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3720">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3721">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3721">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3722">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3722">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-3723">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3723">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3724">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3724">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3725">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3725">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3726">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3726">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3727">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3727">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-3728">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3728">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3729">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3729">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3730">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3730">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3731">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3731">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3732">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3732">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3733">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3733">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3734">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3734">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3735">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3735">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-3736">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3736">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3737">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3737">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3738">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3738">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3739">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3739">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-3740">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3740">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3741">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3741">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3742">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3742">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-3743">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3743">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3744">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3744">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3745">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3745">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3746">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3746">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3747">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3747">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3748">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3748">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3749">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3749">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3750">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3750">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-3751">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3751">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="e1135-3752">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="e1135-3752">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="e1135-3753">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3753">Target</span></span> | <span data-ttu-id="e1135-3754">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3754">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3755">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3755">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3756">16</span><span class="sxs-lookup"><span data-stu-id="e1135-3756">16</span></span> |
| <span data-ttu-id="e1135-3757">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3757">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-3758">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3758">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3759">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3759">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3760">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3760">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3761">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3761">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3762">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3762">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3763">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3763">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-3764">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3764">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-3765">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3765">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-3766">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3766">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-3767">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3767">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-3768">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3768">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3769">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3769">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3770">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3770">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3771">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3771">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3772">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3772">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-3773">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3773">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3774">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3774">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3775">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3775">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3776">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3776">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3777">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3777">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-3778">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3778">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3779">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3779">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3780">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3780">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3781">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3781">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3782">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3782">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3783">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3783">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3784">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3784">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3785">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3785">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-3786">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3786">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3787">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3787">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3788">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3788">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3789">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3789">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-3790">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3790">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3791">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3791">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3792">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3792">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-3793">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3793">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3794">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3794">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3795">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3795">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3796">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3796">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3797">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3797">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3798">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3798">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3799">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3799">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3800">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3800">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-3801">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3801">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="e1135-3802">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="e1135-3802">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="e1135-3803">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3803">Target</span></span> | <span data-ttu-id="e1135-3804">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3804">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3805">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3805">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3806">16</span><span class="sxs-lookup"><span data-stu-id="e1135-3806">16</span></span> |
| <span data-ttu-id="e1135-3807">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3807">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-3808">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3808">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3809">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3809">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3810">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3810">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3811">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3811">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3812">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3812">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3813">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3813">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-3814">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3814">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-3815">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3815">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-3816">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3816">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-3817">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3817">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-3818">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3818">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3819">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3819">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3820">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3820">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3821">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3821">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3822">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3822">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-3823">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3823">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3824">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3824">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3825">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3825">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3826">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3826">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3827">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3827">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-3828">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3828">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3829">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3829">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3830">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3830">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3831">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3831">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3832">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3832">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3833">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3833">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3834">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3834">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3835">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3835">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-3836">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3836">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3837">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3837">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3838">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3838">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3839">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3839">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-3840">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3840">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3841">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3841">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3842">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3842">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-3843">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3843">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3844">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3844">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3845">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3845">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3846">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3846">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3847">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3847">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3848">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3848">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3849">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3849">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3850">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3850">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-3851">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3851">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="e1135-3852">DXGI_FORMAT_BC1 \_ <sup>PCC</sup> sin tipo (70)</span><span class="sxs-lookup"><span data-stu-id="e1135-3852">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="e1135-3853">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3853">Target</span></span> | <span data-ttu-id="e1135-3854">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3854">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3855">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3855">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3856">4</span><span class="sxs-lookup"><span data-stu-id="e1135-3856">4</span></span> |
| <span data-ttu-id="e1135-3857">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3857">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-3858">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3858">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3859">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3859">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3860">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3861">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3862">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3863">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3863">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-3864">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3864">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-3865">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3865">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-3866">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3866">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-3867">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3867">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-3868">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3868">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3869">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3869">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3870">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3870">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3871">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3871">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3872">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3872">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-3873">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3873">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3874">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3874">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3875">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3875">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3876">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3877">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-3878">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3879">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3880">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3880">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3881">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3882">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3883">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3884">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3885">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-3886">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3887">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3888">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3889">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3889">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-3890">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3890">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3891">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3891">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3892">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3892">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-3893">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3893">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3894">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3894">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3895">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3895">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3896">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3896">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3897">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3897">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3898">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3898">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3899">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3899">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3900">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3900">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-3901">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3901">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a><span data-ttu-id="e1135-3902">DXGI_FORMAT_BC1 \_ UNORM<sup>FNC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="e1135-3902">DXGI_FORMAT_BC1\_UNORM<sup>FNC</sup> (71)</span></span>
| <span data-ttu-id="e1135-3903">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3903">Target</span></span> | <span data-ttu-id="e1135-3904">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3904">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3905">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3905">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3906">4</span><span class="sxs-lookup"><span data-stu-id="e1135-3906">4</span></span> |
| <span data-ttu-id="e1135-3907">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3907">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3909">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3909">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3910">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3910">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3911">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3911">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3912">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3912">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3913">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3913">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3914">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3914">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3916">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3916">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-3917">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3917">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3919">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3919">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3921">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3921">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3923">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3923">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3924">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3924">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3925">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3925">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3926">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3926">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3927">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3927">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3929">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3929">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3930">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3930">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3931">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3931">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3932">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3932">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3933">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3933">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-3934">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3934">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3935">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3935">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3936">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3936">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3937">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3937">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3938">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3938">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3939">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3939">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3940">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3940">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3941">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3941">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-3942">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3942">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-3943">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3943">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3944">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-3944">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-3945">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-3945">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3947">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-3947">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3948">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3948">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3949">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-3949">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-3950">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-3950">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-3951">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-3951">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-3952">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-3952">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-3953">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-3953">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-3954">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3954">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-3955">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3955">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-3956">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-3956">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-3957">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-3957">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3959">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-3959">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a><span data-ttu-id="e1135-3960">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FNC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="e1135-3960">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FNC</sup> (72)</span></span>
| <span data-ttu-id="e1135-3961">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-3961">Target</span></span> | <span data-ttu-id="e1135-3962">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-3962">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-3963">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-3963">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-3964">4</span><span class="sxs-lookup"><span data-stu-id="e1135-3964">4</span></span> |
| <span data-ttu-id="e1135-3965">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3965">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3967">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-3967">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3968">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3968">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3969">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-3969">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3970">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-3970">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-3971">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-3971">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-3972">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-3972">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3974">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-3974">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-3975">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-3975">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3977">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-3977">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3979">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-3979">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3981">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-3981">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-3982">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-3982">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-3983">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-3983">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-3984">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-3984">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-3985">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-3985">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-3987">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-3987">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-3988">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-3988">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3989">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-3989">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-3990">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-3990">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-3991">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-3991">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-3992">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-3992">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3993">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-3993">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-3994">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-3994">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-3995">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-3995">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-3996">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3996">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-3997">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-3997">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-3998">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-3998">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-3999">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-3999">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4000">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4000">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4001">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4001">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4002">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4002">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4003">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4003">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4005">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4005">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4006">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4006">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4007">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4007">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-4008">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-4008">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-4009">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4009">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-4010">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-4010">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-4011">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-4011">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-4012">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4012">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-4013">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4013">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-4014">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4014">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-4015">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-4015">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4017">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-4017">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="e1135-4018">DXGI_FORMAT_BC2 \_ <sup>PCC</sup> sin tipo (73)</span><span class="sxs-lookup"><span data-stu-id="e1135-4018">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="e1135-4019">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-4019">Target</span></span> | <span data-ttu-id="e1135-4020">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-4020">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-4021">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-4021">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-4022">8</span><span class="sxs-lookup"><span data-stu-id="e1135-4022">8</span></span> |
| <span data-ttu-id="e1135-4023">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4023">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-4024">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-4024">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4025">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4025">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4026">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4026">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4027">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-4027">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4028">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-4028">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-4029">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-4029">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-4030">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-4030">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-4031">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-4031">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-4032">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-4032">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-4033">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-4033">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-4034">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-4034">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-4035">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-4035">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-4036">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-4036">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-4037">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-4037">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-4038">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-4038">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-4039">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-4039">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-4040">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-4040">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4041">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-4041">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4042">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-4042">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-4043">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-4043">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-4044">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4044">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4045">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-4045">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4046">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-4046">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-4047">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-4047">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-4048">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4048">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-4049">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-4049">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-4050">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4050">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-4051">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-4051">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4052">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4052">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4053">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4053">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4054">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4054">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4055">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4055">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-4056">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4056">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4057">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4057">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4058">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4058">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-4059">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-4059">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-4060">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4060">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-4061">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-4061">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-4062">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-4062">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-4063">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4063">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-4064">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4064">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-4065">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4065">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-4066">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-4066">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-4067">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-4067">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a><span data-ttu-id="e1135-4068">DXGI_FORMAT_BC2 \_ UNORM<sup>FNC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="e1135-4068">DXGI_FORMAT_BC2\_UNORM<sup>FNC</sup> (74)</span></span>
| <span data-ttu-id="e1135-4069">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-4069">Target</span></span> | <span data-ttu-id="e1135-4070">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-4070">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-4071">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-4071">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-4072">8</span><span class="sxs-lookup"><span data-stu-id="e1135-4072">8</span></span> |
| <span data-ttu-id="e1135-4073">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4073">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4075">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-4075">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4076">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4076">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4077">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4077">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4078">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-4078">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4079">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-4079">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-4080">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-4080">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4082">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-4082">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-4083">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-4083">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4085">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-4085">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4087">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-4087">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4089">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-4089">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-4090">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-4090">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-4091">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-4091">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-4092">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-4092">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-4093">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-4093">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4095">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-4095">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-4096">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-4096">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4097">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-4097">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4098">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-4098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-4099">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-4099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-4100">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4101">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-4101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4102">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-4102">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-4103">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-4103">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-4104">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4104">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-4105">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-4105">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-4106">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4106">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-4107">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-4107">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4108">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4108">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4109">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4109">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4110">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4110">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4111">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4111">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4113">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4113">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4114">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4114">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4115">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4115">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-4116">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-4116">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-4117">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4117">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-4118">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-4118">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-4119">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-4119">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-4120">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4120">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-4121">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4121">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-4122">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4122">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-4123">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-4123">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4125">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-4125">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a><span data-ttu-id="e1135-4126">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FNC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="e1135-4126">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FNC</sup> (75)</span></span>
| <span data-ttu-id="e1135-4127">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-4127">Target</span></span> | <span data-ttu-id="e1135-4128">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-4128">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-4129">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-4129">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-4130">8</span><span class="sxs-lookup"><span data-stu-id="e1135-4130">8</span></span> |
| <span data-ttu-id="e1135-4131">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4131">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4133">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-4133">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4134">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4134">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4135">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4135">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4136">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-4136">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4137">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-4137">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-4138">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-4138">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4140">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-4140">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-4141">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-4141">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4143">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-4143">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4145">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-4145">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4147">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-4147">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-4148">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-4148">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-4149">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-4149">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-4150">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-4150">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-4151">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-4151">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4153">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-4153">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-4154">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-4154">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4155">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-4155">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4156">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-4156">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-4157">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-4157">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-4158">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4158">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4159">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-4159">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4160">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-4160">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-4161">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-4161">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-4162">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4162">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-4163">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-4163">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-4164">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4164">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-4165">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-4165">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4166">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4166">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4167">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4167">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4168">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4168">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4169">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4169">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4171">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4171">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4172">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4172">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4173">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4173">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-4174">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-4174">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-4175">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4175">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-4176">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-4176">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-4177">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-4177">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-4178">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4178">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-4179">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4179">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-4180">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4180">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-4181">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-4181">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4183">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-4183">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="e1135-4184">DXGI_FORMAT_BC3 \_ <sup>PCC</sup> sin tipo (76)</span><span class="sxs-lookup"><span data-stu-id="e1135-4184">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="e1135-4185">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-4185">Target</span></span> | <span data-ttu-id="e1135-4186">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-4186">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-4187">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-4187">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-4188">8</span><span class="sxs-lookup"><span data-stu-id="e1135-4188">8</span></span> |
| <span data-ttu-id="e1135-4189">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4189">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-4190">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-4190">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4191">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4191">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4192">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4192">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4193">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-4193">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4194">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-4194">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-4195">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-4195">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-4196">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-4196">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-4197">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-4197">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-4198">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-4198">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-4199">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-4199">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-4200">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-4200">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-4201">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-4201">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-4202">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-4202">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-4203">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-4203">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-4204">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-4204">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-4205">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-4205">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-4206">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-4206">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4207">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-4207">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4208">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-4208">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-4209">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-4209">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-4210">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4210">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4211">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-4211">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4212">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-4212">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-4213">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-4213">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-4214">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4214">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-4215">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-4215">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-4216">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4216">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-4217">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-4217">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4218">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4218">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4219">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4219">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4220">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4220">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4221">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4221">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-4222">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4223">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4224">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-4225">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-4225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-4226">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4226">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-4227">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-4227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-4228">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-4228">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-4229">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4229">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-4230">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4230">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-4231">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4231">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-4232">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-4232">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-4233">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-4233">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a><span data-ttu-id="e1135-4234">DXGI_FORMAT_BC3 \_ UNORM<sup>FNC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="e1135-4234">DXGI_FORMAT_BC3\_UNORM<sup>FNC</sup> (77)</span></span>
| <span data-ttu-id="e1135-4235">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-4235">Target</span></span> | <span data-ttu-id="e1135-4236">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-4236">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-4237">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-4237">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-4238">8</span><span class="sxs-lookup"><span data-stu-id="e1135-4238">8</span></span> |
| <span data-ttu-id="e1135-4239">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4239">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4241">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-4241">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4242">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4242">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4243">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4243">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4244">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-4244">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4245">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-4245">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-4246">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-4246">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4248">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-4248">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-4249">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-4249">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4251">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-4251">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4253">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-4253">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4255">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-4255">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-4256">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-4256">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-4257">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-4257">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-4258">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-4258">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-4259">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-4259">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4261">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-4261">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-4262">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-4262">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4263">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-4263">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4264">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-4264">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-4265">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-4265">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-4266">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4266">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4267">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-4267">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4268">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-4268">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-4269">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-4269">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-4270">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4270">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-4271">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-4271">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-4272">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4272">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-4273">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-4273">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4274">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4274">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4275">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4275">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4276">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4276">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4277">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4277">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4279">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4279">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4280">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4280">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4281">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4281">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-4282">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-4282">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-4283">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4283">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-4284">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-4284">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-4285">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-4285">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-4286">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4286">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-4287">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4287">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-4288">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4288">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-4289">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-4289">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4291">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-4291">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a><span data-ttu-id="e1135-4292">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FNC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="e1135-4292">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FNC</sup> (78)</span></span>
| <span data-ttu-id="e1135-4293">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-4293">Target</span></span> | <span data-ttu-id="e1135-4294">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-4294">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-4295">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-4295">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-4296">8</span><span class="sxs-lookup"><span data-stu-id="e1135-4296">8</span></span> |
| <span data-ttu-id="e1135-4297">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4297">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4299">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-4299">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4300">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4300">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4301">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4301">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4302">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-4302">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4303">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-4303">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-4304">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-4304">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4306">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-4306">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-4307">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-4307">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4309">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-4309">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4311">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-4311">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4313">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-4313">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-4314">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-4314">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-4315">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-4315">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-4316">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-4316">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-4317">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-4317">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4319">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-4319">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-4320">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-4320">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4321">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-4321">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4322">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-4322">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-4323">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-4323">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-4324">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4324">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4325">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-4325">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4326">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-4326">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-4327">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-4327">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-4328">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4328">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-4329">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-4329">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-4330">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4330">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-4331">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-4331">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4332">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4332">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4333">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4333">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4334">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4334">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4335">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4335">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4337">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4337">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4338">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4338">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4339">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4339">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-4340">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-4340">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-4341">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4341">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-4342">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-4342">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-4343">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-4343">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-4344">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4344">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-4345">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4345">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-4346">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4346">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-4347">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-4347">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4349">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-4349">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="e1135-4350">DXGI_FORMAT_BC4 \_ <sup>PCC</sup> sin tipo (79)</span><span class="sxs-lookup"><span data-stu-id="e1135-4350">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="e1135-4351">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-4351">Target</span></span> | <span data-ttu-id="e1135-4352">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-4352">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-4353">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-4353">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-4354">4</span><span class="sxs-lookup"><span data-stu-id="e1135-4354">4</span></span> |
| <span data-ttu-id="e1135-4355">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4355">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-4356">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-4356">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4357">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4357">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4358">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4358">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4359">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-4359">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4360">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-4360">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-4361">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-4361">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-4362">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-4362">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-4363">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-4363">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-4364">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-4364">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-4365">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-4365">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-4366">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-4366">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-4367">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-4367">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-4368">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-4368">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-4369">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-4369">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-4370">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-4370">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-4371">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-4371">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-4372">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-4372">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4373">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-4373">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4374">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-4374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-4375">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-4375">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-4376">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4376">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4377">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-4377">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4378">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-4378">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-4379">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-4379">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-4380">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4380">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-4381">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-4381">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-4382">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4382">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-4383">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-4383">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4384">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4384">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4385">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4385">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4386">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4386">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4387">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4387">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-4388">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4388">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4389">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4389">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4390">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4390">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-4391">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-4391">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-4392">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4392">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-4393">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-4393">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-4394">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-4394">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-4395">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4395">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-4396">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4396">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-4397">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4397">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-4398">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-4398">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-4399">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-4399">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a><span data-ttu-id="e1135-4400">DXGI_FORMAT_BC4 \_ UNORM<sup>FNC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="e1135-4400">DXGI_FORMAT_BC4\_UNORM<sup>FNC</sup> (80)</span></span>
| <span data-ttu-id="e1135-4401">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-4401">Target</span></span> | <span data-ttu-id="e1135-4402">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-4402">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-4403">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-4403">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-4404">4</span><span class="sxs-lookup"><span data-stu-id="e1135-4404">4</span></span> |
| <span data-ttu-id="e1135-4405">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4405">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-4406">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-4406">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4407">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4407">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4408">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4408">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4409">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-4409">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4410">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-4410">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-4411">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-4411">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-4412">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-4412">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-4413">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-4413">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-4414">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-4414">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-4415">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-4415">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-4416">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-4416">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-4417">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-4417">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-4418">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-4418">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-4419">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-4419">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-4420">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-4420">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-4421">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-4421">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-4422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-4422">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4423">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-4423">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4424">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-4424">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-4425">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-4425">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-4426">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4426">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4427">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-4427">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4428">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-4428">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-4429">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-4429">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-4430">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4430">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-4431">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-4431">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-4432">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4432">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-4433">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-4433">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4434">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4434">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4435">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4435">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4436">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4436">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4437">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4437">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-4438">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4438">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4439">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4439">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4440">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4440">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-4441">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-4441">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-4442">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4442">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-4443">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-4443">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-4444">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-4444">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-4445">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4445">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-4446">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4446">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-4447">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4447">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-4448">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-4448">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-4449">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-4449">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a><span data-ttu-id="e1135-4450">DXGI_FORMAT_BC4 \_ SNORM<sup>FNC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="e1135-4450">DXGI_FORMAT_BC4\_SNORM<sup>FNC</sup> (81)</span></span>
| <span data-ttu-id="e1135-4451">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-4451">Target</span></span> | <span data-ttu-id="e1135-4452">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-4452">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-4453">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-4453">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-4454">4</span><span class="sxs-lookup"><span data-stu-id="e1135-4454">4</span></span> |
| <span data-ttu-id="e1135-4455">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4455">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-4456">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-4456">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4457">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4457">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4458">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4458">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4459">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-4459">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4460">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-4460">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-4461">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-4461">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-4462">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-4462">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-4463">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-4463">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-4464">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-4464">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-4465">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-4465">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-4466">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-4466">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-4467">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-4467">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-4468">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-4468">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-4469">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-4469">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-4470">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-4470">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-4471">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-4471">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-4472">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-4472">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4473">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-4473">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4474">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-4474">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-4475">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-4475">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-4476">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4476">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4477">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-4477">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4478">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-4478">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-4479">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-4479">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-4480">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4480">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-4481">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-4481">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-4482">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4482">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-4483">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-4483">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4484">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4484">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4485">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4485">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4486">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4486">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4487">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4487">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-4488">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4488">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4489">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4489">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4490">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4490">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-4491">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-4491">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-4492">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4492">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-4493">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-4493">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-4494">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-4494">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-4495">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-4496">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-4497">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-4498">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-4498">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-4499">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-4499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="e1135-4500">DXGI_FORMAT_BC5 \_ <sup>PCC</sup> sin tipo (82)</span><span class="sxs-lookup"><span data-stu-id="e1135-4500">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="e1135-4501">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-4501">Target</span></span> | <span data-ttu-id="e1135-4502">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-4502">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-4503">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-4503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-4504">8</span><span class="sxs-lookup"><span data-stu-id="e1135-4504">8</span></span> |
| <span data-ttu-id="e1135-4505">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4505">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-4506">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-4506">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4507">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4507">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4508">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4508">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4509">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-4509">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4510">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-4510">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-4511">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-4511">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-4512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-4512">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-4513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-4513">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-4514">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-4514">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-4515">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-4515">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-4516">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-4516">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-4517">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-4517">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-4518">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-4518">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-4519">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-4519">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-4520">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-4520">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-4521">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-4521">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-4522">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-4522">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4523">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-4523">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4524">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-4524">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-4525">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-4525">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-4526">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4526">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4527">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-4527">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4528">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-4528">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-4529">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-4529">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-4530">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4530">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-4531">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-4531">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-4532">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4532">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-4533">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-4533">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4534">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4534">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4535">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4535">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4536">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4536">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4537">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4537">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-4538">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4538">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4539">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4539">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4540">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4540">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-4541">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-4541">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-4542">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4542">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-4543">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-4543">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-4544">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-4544">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-4545">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4545">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-4546">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4546">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-4547">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4547">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-4548">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-4548">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-4549">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-4549">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a><span data-ttu-id="e1135-4550">DXGI_FORMAT_BC5 \_ UNORM<sup>FNC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="e1135-4550">DXGI_FORMAT_BC5\_UNORM<sup>FNC</sup> (83)</span></span>
| <span data-ttu-id="e1135-4551">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-4551">Target</span></span> | <span data-ttu-id="e1135-4552">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-4552">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-4553">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-4553">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-4554">8</span><span class="sxs-lookup"><span data-stu-id="e1135-4554">8</span></span> |
| <span data-ttu-id="e1135-4555">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4555">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-4556">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-4556">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4557">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4557">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4558">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4558">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4559">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-4559">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4560">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-4560">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-4561">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-4561">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-4562">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-4562">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-4563">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-4563">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-4564">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-4564">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-4565">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-4565">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-4566">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-4566">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-4567">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-4567">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-4568">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-4568">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-4569">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-4569">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-4570">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-4570">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-4571">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-4571">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-4572">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-4572">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4573">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-4573">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4574">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-4574">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-4575">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-4575">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-4576">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4576">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4577">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-4577">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4578">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-4578">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-4579">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-4579">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-4580">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4580">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-4581">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-4581">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-4582">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4582">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-4583">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-4583">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4584">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4584">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4585">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4585">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4586">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4586">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4587">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4587">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-4588">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4588">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4589">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4589">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4590">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4590">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-4591">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-4591">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-4592">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4592">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-4593">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-4593">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-4594">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-4594">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-4595">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4595">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-4596">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4596">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-4597">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4597">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-4598">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-4598">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-4599">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-4599">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a><span data-ttu-id="e1135-4600">DXGI_FORMAT_BC5 \_ SNORM<sup>FNC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="e1135-4600">DXGI_FORMAT_BC5\_SNORM<sup>FNC</sup> (84)</span></span>
| <span data-ttu-id="e1135-4601">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-4601">Target</span></span> | <span data-ttu-id="e1135-4602">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-4602">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-4603">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-4603">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-4604">8</span><span class="sxs-lookup"><span data-stu-id="e1135-4604">8</span></span> |
| <span data-ttu-id="e1135-4605">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4605">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-4606">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-4606">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4607">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4607">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4608">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4608">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4609">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-4609">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4610">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-4610">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-4611">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-4611">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-4612">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-4612">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-4613">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-4613">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-4614">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-4614">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-4615">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-4615">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-4616">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-4616">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-4617">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-4617">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-4618">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-4618">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-4619">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-4619">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-4620">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-4620">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-4621">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-4621">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-4622">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-4622">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4623">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-4623">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4624">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-4624">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-4625">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-4625">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-4626">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4626">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4627">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-4627">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4628">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-4628">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-4629">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-4629">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-4630">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4630">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-4631">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-4631">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-4632">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4632">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-4633">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-4633">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4634">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4634">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4635">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4635">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4636">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4636">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4637">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4637">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-4638">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4638">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4639">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4639">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4640">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4640">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-4641">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-4641">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-4642">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4642">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-4643">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-4643">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-4644">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-4644">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-4645">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4645">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-4646">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4646">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-4647">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4647">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-4648">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-4648">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-4649">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-4649">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="e1135-4650">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="e1135-4650">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="e1135-4651">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-4651">Target</span></span> | <span data-ttu-id="e1135-4652">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-4652">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-4653">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-4653">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-4654">16</span><span class="sxs-lookup"><span data-stu-id="e1135-4654">16</span></span> |
| <span data-ttu-id="e1135-4655">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4655">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4657">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-4657">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4658">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4658">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4659">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4659">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4660">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-4660">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4661">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-4661">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-4662">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-4662">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4664">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-4664">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-4665">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-4665">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4667">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-4667">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4669">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-4669">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4671">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-4671">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-4672">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-4672">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-4673">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-4673">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-4674">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-4674">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-4675">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-4675">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4677">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-4677">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4679">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-4679">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4681">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-4681">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4683">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-4683">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-4684">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-4684">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-4685">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4685">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4686">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-4686">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4687">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-4687">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-4688">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-4688">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-4689">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4689">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-4690">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-4690">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-4691">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4691">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-4692">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-4692">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4693">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4693">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4694">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4694">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4695">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4695">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4696">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4696">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4698">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4698">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-4700">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4700">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-4702">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4702">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-4704">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-4704">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4706">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4706">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-4707">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-4707">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-4708">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-4708">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-4709">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4709">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-4710">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4710">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-4711">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4711">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-4712">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-4712">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-4713">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-4713">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="e1135-4714">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="e1135-4714">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="e1135-4715">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-4715">Target</span></span> | <span data-ttu-id="e1135-4716">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-4716">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-4717">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-4717">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-4718">16</span><span class="sxs-lookup"><span data-stu-id="e1135-4718">16</span></span> |
| <span data-ttu-id="e1135-4719">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4719">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4721">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-4721">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4722">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4722">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4723">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4723">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4724">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-4724">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4725">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-4725">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-4726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-4726">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-4728">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-4729">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-4729">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4731">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-4731">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4733">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-4733">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4735">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-4735">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-4736">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-4736">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-4737">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-4737">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-4738">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-4738">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-4739">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-4739">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4741">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-4741">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-4742">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-4742">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4743">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-4743">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4744">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-4744">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-4745">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-4745">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-4746">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4746">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4747">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-4747">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4748">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-4748">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-4749">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-4749">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-4750">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4750">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-4751">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-4751">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-4752">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4752">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-4753">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-4753">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4754">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4754">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4755">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4755">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4756">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4756">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4757">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4757">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4759">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4759">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4760">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4760">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4761">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4761">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-4762">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-4762">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-4763">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4763">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-4764">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-4764">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-4765">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-4765">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-4766">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4766">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-4767">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4767">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-4768">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4768">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-4769">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-4769">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-4770">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-4770">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="e1135-4771">DXGI_FORMAT_B8G8R8A8 de \_ <sup>equipos</sup> sin tipo (90)</span><span class="sxs-lookup"><span data-stu-id="e1135-4771">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="e1135-4772">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-4772">Target</span></span> | <span data-ttu-id="e1135-4773">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-4773">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-4774">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-4774">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-4775">32</span><span class="sxs-lookup"><span data-stu-id="e1135-4775">32</span></span> |
| <span data-ttu-id="e1135-4776">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4776">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-4777">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-4777">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4778">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4778">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4779">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4779">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4780">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-4780">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4781">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-4781">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-4782">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-4782">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-4783">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-4783">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-4784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-4784">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-4785">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-4785">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-4786">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-4786">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-4787">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-4787">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-4788">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-4788">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-4789">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-4789">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-4790">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-4790">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-4791">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-4791">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-4792">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-4792">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-4793">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-4793">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4794">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-4794">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4795">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-4795">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-4796">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-4796">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-4797">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4797">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4798">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-4798">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4799">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-4799">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-4800">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-4800">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-4801">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4801">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-4802">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-4802">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-4803">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4803">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-4804">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-4804">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4805">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4805">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4806">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4806">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4807">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4807">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4808">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4808">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-4809">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4809">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4810">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4810">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4811">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4811">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-4812">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-4812">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-4813">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4813">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-4814">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-4814">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-4815">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-4815">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-4816">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4816">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-4817">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4817">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-4818">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4818">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-4819">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-4819">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-4820">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-4820">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a><span data-ttu-id="e1135-4821">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FNS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="e1135-4821">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FNS</sup> (87)</span></span>
| <span data-ttu-id="e1135-4822">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-4822">Target</span></span> | <span data-ttu-id="e1135-4823">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-4823">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-4824">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-4824">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-4825">32</span><span class="sxs-lookup"><span data-stu-id="e1135-4825">32</span></span> |
| <span data-ttu-id="e1135-4826">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4826">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4828">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-4828">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4829">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4829">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4830">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4830">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4831">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-4831">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4832">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-4832">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-4833">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-4833">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4835">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-4835">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4837">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-4837">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4839">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-4839">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4841">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-4841">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4843">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-4843">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-4844">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-4844">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-4845">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-4845">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-4846">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-4846">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-4847">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-4847">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4849">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-4849">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4851">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-4851">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4853">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-4853">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4855">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-4855">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-4856">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-4856">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-4857">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4857">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4858">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-4858">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4859">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-4859">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-4860">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-4860">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-4861">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4861">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-4862">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-4862">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-4863">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4863">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-4864">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-4864">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4865">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4865">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4866">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4866">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4867">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4867">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4868">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4868">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4870">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4870">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-4872">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4872">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-4874">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4874">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-4876">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-4876">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4878">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4878">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-4879">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-4879">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4881">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-4881">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-4882">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4882">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-4883">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4883">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-4885">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4885">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4887">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-4887">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4889">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-4889">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a><span data-ttu-id="e1135-4890">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRGB<sup>FNS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="e1135-4890">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FNS</sup> (91)</span></span>
| <span data-ttu-id="e1135-4891">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-4891">Target</span></span> | <span data-ttu-id="e1135-4892">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-4892">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-4893">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-4893">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-4894">32</span><span class="sxs-lookup"><span data-stu-id="e1135-4894">32</span></span> |
| <span data-ttu-id="e1135-4895">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4895">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4897">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-4897">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4898">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4898">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4899">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4899">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4900">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-4900">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4901">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-4901">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-4902">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-4902">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4904">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-4904">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4906">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-4906">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4908">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-4908">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4910">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-4910">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4912">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-4912">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-4913">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-4913">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-4914">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-4914">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-4915">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-4915">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-4916">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-4916">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4918">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-4918">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4920">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-4920">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4922">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-4922">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4924">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-4924">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-4925">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-4925">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-4926">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4926">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4927">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-4927">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4928">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-4928">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-4929">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-4929">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-4930">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4930">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-4931">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-4931">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-4932">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4932">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-4933">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-4933">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4934">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4934">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4935">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4935">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4936">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4936">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4937">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4937">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4939">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4939">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-4941">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4941">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-4943">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4943">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-4945">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-4945">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4947">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4947">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-4948">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-4948">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4950">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-4950">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-4951">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4951">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-4952">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4952">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-4954">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-4954">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4956">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-4956">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-4958">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-4958">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="e1135-4959">DXGI_FORMAT_B8G8R8X8 de \_ <sup>equipos</sup> sin tipo (92)</span><span class="sxs-lookup"><span data-stu-id="e1135-4959">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="e1135-4960">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-4960">Target</span></span> | <span data-ttu-id="e1135-4961">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-4961">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-4962">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-4962">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-4963">32</span><span class="sxs-lookup"><span data-stu-id="e1135-4963">32</span></span> |
| <span data-ttu-id="e1135-4964">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4964">Format Support</span></span> | \- |
| <span data-ttu-id="e1135-4965">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-4965">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4966">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4966">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4967">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-4967">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4968">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-4968">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-4969">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-4969">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-4970">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-4970">Texture2D</span></span> | \- |
| <span data-ttu-id="e1135-4971">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-4971">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-4972">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-4972">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-4973">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-4973">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-4974">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-4974">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-4975">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-4975">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-4976">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-4976">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-4977">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-4977">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-4978">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-4978">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-4979">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-4979">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-4980">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-4980">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-4981">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-4981">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4982">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-4982">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4983">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-4983">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-4984">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-4984">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-4985">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-4985">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4986">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-4986">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-4987">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-4987">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-4988">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-4988">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-4989">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4989">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-4990">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-4990">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-4991">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4991">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-4992">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-4992">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-4993">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-4993">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-4994">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4994">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4995">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-4995">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-4996">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-4996">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-4997">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-4997">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4998">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-4998">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-4999">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-4999">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-5000">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-5000">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-5001">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5001">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-5002">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-5002">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-5003">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-5003">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-5004">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5004">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-5005">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5005">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-5006">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5006">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-5007">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-5007">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-5008">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-5008">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a><span data-ttu-id="e1135-5009">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FNS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="e1135-5009">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FNS</sup> (88)</span></span>
| <span data-ttu-id="e1135-5010">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-5010">Target</span></span> | <span data-ttu-id="e1135-5011">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-5011">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-5012">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-5012">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-5013">32</span><span class="sxs-lookup"><span data-stu-id="e1135-5013">32</span></span> |
| <span data-ttu-id="e1135-5014">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5014">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5016">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-5016">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5017">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5017">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5018">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5018">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5019">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-5019">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5020">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-5020">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-5021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-5021">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-5023">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-5025">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5027">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-5027">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5029">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-5029">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5031">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-5031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-5032">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-5032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-5033">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-5033">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-5034">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-5034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-5035">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-5035">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5037">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-5037">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5039">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-5039">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5041">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-5041">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5043">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-5043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-5044">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-5044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-5045">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5046">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-5046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5047">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-5047">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-5048">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-5048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-5049">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-5050">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-5050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-5051">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-5052">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-5052">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-5053">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-5054">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5055">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5056">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-5056">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5058">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-5058">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5060">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5060">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5062">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-5062">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5064">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-5064">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5066">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5066">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-5067">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-5067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-5068">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-5068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-5069">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-5070">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5070">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5072">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5072">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5074">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-5074">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5076">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-5076">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a><span data-ttu-id="e1135-5077">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRGB<sup>FNS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="e1135-5077">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FNS</sup> (93)</span></span>
| <span data-ttu-id="e1135-5078">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-5078">Target</span></span> | <span data-ttu-id="e1135-5079">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-5079">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-5080">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-5080">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-5081">32</span><span class="sxs-lookup"><span data-stu-id="e1135-5081">32</span></span> |
| <span data-ttu-id="e1135-5082">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5082">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5084">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-5084">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5085">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5085">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5086">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5086">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5087">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-5087">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5088">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-5088">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-5089">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-5089">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5091">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-5091">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5093">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-5093">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5095">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-5095">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5097">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-5097">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5099">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-5099">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-5100">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-5100">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-5101">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-5101">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-5102">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-5102">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-5103">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-5103">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5105">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-5105">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5107">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-5107">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5109">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-5109">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5111">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-5111">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-5112">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-5112">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-5113">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5113">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5114">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-5114">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5115">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-5115">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-5116">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-5116">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-5117">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5117">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-5118">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-5118">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-5119">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5119">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-5120">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-5120">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-5121">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5121">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-5122">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5122">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5123">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5123">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5124">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-5124">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5126">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-5126">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5128">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5128">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5130">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-5130">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5132">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-5132">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5134">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5134">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-5135">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-5135">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-5136">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-5136">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-5137">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5137">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-5138">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5138">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-5139">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5139">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-5140">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-5140">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5142">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-5142">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="e1135-5143">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="e1135-5143">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="e1135-5144">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-5144">Target</span></span> | <span data-ttu-id="e1135-5145">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-5145">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-5146">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-5146">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-5147">32</span><span class="sxs-lookup"><span data-stu-id="e1135-5147">32</span></span> |
| <span data-ttu-id="e1135-5148">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5148">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5150">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-5150">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5151">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5151">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5152">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5152">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5153">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-5153">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5154">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-5154">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-5155">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-5155">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5157">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-5157">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-5158">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-5158">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-5159">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-5159">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-5160">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-5160">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-5161">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-5161">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-5162">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-5162">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-5163">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-5163">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-5164">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-5164">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-5165">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-5165">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-5166">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-5166">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-5167">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-5167">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5168">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-5168">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5169">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-5169">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-5170">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-5170">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-5171">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5171">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5172">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-5172">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5173">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-5173">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-5174">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-5174">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-5175">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5175">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-5176">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-5176">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-5177">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5177">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-5178">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-5178">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-5179">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5179">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-5180">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5180">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5181">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5181">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5182">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-5182">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5184">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-5184">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5185">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5185">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5186">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-5186">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-5187">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-5187">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-5188">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5188">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-5189">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-5189">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-5190">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-5190">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-5191">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5191">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5193">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5193">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5195">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5195">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5197">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-5197">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-5198">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-5198">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="e1135-5199">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="e1135-5199">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="e1135-5200">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-5200">Target</span></span> | <span data-ttu-id="e1135-5201">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-5201">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-5202">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-5202">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-5203">32</span><span class="sxs-lookup"><span data-stu-id="e1135-5203">32</span></span> |
| <span data-ttu-id="e1135-5204">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5204">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5206">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-5206">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5207">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5207">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5208">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5208">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5209">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-5209">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5210">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-5210">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-5211">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-5211">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5213">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-5213">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-5214">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-5214">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-5215">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-5215">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-5216">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-5216">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-5217">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-5217">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-5218">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-5218">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-5219">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-5219">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-5220">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-5220">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-5221">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-5221">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-5222">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-5222">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-5223">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-5223">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5224">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-5224">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5225">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-5225">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-5226">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-5226">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-5227">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5227">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5228">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-5228">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5229">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-5229">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-5230">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-5230">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-5231">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5231">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-5232">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-5232">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-5233">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5233">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-5234">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-5234">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-5235">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5235">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-5236">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5236">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5237">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5237">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5238">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-5238">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5240">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-5240">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5241">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5241">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5242">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-5242">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-5243">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-5243">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-5244">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5244">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-5245">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-5245">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-5246">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-5246">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-5247">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5247">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5249">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5249">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5251">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5251">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5253">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-5253">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-5254">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-5254">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="e1135-5255">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="e1135-5255">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="e1135-5256">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-5256">Target</span></span> | <span data-ttu-id="e1135-5257">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-5257">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-5258">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-5258">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-5259">64</span><span class="sxs-lookup"><span data-stu-id="e1135-5259">64</span></span> |
| <span data-ttu-id="e1135-5260">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5260">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5262">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-5262">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5263">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5263">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5264">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5264">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5265">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-5265">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5266">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-5266">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-5267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-5267">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-5269">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-5270">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-5270">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-5271">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-5271">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-5272">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-5272">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-5273">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-5273">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-5274">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-5274">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-5275">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-5275">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-5276">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-5276">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-5277">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-5277">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-5278">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-5278">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-5279">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-5279">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5280">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-5280">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5281">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-5281">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-5282">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-5282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-5283">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5284">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-5284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5285">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-5285">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-5286">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-5286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-5287">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-5288">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-5288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-5289">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-5290">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-5290">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-5291">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-5292">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5293">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5294">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-5294">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5296">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-5296">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5297">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5297">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5298">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-5298">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-5299">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-5299">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-5300">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5300">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-5301">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-5301">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-5302">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-5302">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-5303">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5303">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5305">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5305">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5307">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5307">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5309">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-5309">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-5310">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-5310">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="e1135-5311">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="e1135-5311">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="e1135-5312">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-5312">Target</span></span> | <span data-ttu-id="e1135-5313">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-5313">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-5314">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-5314">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-5315">8</span><span class="sxs-lookup"><span data-stu-id="e1135-5315">8</span></span> |
| <span data-ttu-id="e1135-5316">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5316">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5318">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-5318">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5319">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5319">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5320">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5321">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-5321">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5322">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-5322">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-5323">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-5323">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5325">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-5325">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-5326">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-5326">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-5327">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-5327">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-5328">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-5328">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-5329">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-5329">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-5330">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-5330">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-5331">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-5331">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-5332">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-5332">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-5333">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-5333">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-5334">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-5334">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-5335">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-5335">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5336">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-5336">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5337">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-5337">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-5338">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-5338">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-5339">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5339">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5340">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-5340">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5341">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-5341">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-5342">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-5342">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-5343">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5343">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-5344">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-5344">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-5345">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5345">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-5346">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-5346">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-5347">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5347">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-5348">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5348">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5349">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5349">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5350">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-5350">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5352">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-5352">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5353">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5353">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5354">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-5354">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-5355">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-5355">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-5356">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5356">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-5357">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-5357">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-5358">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-5358">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-5359">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5359">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5361">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5361">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5363">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5363">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5365">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-5365">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-5366">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-5366">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="e1135-5367">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="e1135-5367">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="e1135-5368">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-5368">Target</span></span> | <span data-ttu-id="e1135-5369">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-5369">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-5370">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-5370">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-5371">16</span><span class="sxs-lookup"><span data-stu-id="e1135-5371">16</span></span> |
| <span data-ttu-id="e1135-5372">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5372">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5374">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-5374">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5375">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5375">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5376">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5376">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5377">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-5377">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5378">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-5378">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-5379">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-5379">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5381">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-5381">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-5382">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-5382">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-5383">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-5383">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-5384">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-5384">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-5385">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-5385">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-5386">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-5386">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-5387">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-5387">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-5388">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-5388">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-5389">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-5389">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-5390">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-5390">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-5391">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-5391">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5392">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-5392">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5393">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-5393">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-5394">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-5394">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-5395">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5395">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5396">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-5396">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5397">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-5397">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-5398">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-5398">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-5399">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5399">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-5400">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-5400">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-5401">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5401">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-5402">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-5402">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-5403">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5403">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-5404">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5404">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5405">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5405">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5406">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-5406">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5408">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-5408">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5409">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5409">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5410">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-5410">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-5411">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-5411">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-5412">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5412">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-5413">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-5413">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-5414">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-5414">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-5415">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5415">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5417">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5417">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5419">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5419">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5421">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-5421">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-5422">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-5422">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="e1135-5423">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="e1135-5423">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="e1135-5424">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-5424">Target</span></span> | <span data-ttu-id="e1135-5425">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-5425">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-5426">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-5426">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-5427">16</span><span class="sxs-lookup"><span data-stu-id="e1135-5427">16</span></span> |
| <span data-ttu-id="e1135-5428">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5428">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5430">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-5430">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5431">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5431">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5432">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5432">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5433">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-5433">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5434">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-5434">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-5435">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-5435">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5437">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-5437">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-5438">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-5438">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-5439">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-5439">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-5440">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-5440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-5441">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-5441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-5442">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-5442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-5443">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-5443">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-5444">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-5444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-5445">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-5445">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-5446">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-5446">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-5447">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-5447">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5448">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-5448">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5449">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-5449">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-5450">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-5450">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-5451">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5451">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5452">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-5452">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5453">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-5453">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-5454">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-5454">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-5455">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5455">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-5456">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-5456">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-5457">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5457">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-5458">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-5458">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-5459">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5459">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-5460">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5460">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5461">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5461">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5462">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-5462">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5464">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-5464">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5465">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5465">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5466">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-5466">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-5467">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-5467">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-5468">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5468">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-5469">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-5469">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-5470">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-5470">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-5471">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5471">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5473">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5473">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5475">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5475">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5477">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-5477">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-5478">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-5478">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="e1135-5479">DXGI_FORMAT_420 \_ opaca<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="e1135-5479">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="e1135-5480">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-5480">Target</span></span> | <span data-ttu-id="e1135-5481">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-5481">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-5482">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-5482">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-5483">8</span><span class="sxs-lookup"><span data-stu-id="e1135-5483">8</span></span> |
| <span data-ttu-id="e1135-5484">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5484">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5486">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-5486">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5487">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5487">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5488">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5488">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5489">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-5489">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5490">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-5490">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-5491">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-5491">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5493">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-5493">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-5494">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-5494">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-5495">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-5495">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-5496">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-5496">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-5497">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-5497">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-5498">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-5498">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-5499">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-5499">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-5500">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-5500">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-5501">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-5501">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-5502">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-5502">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-5503">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-5503">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5504">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-5504">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5505">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-5505">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-5506">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-5506">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-5507">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5507">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5508">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-5508">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5509">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-5509">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-5510">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-5510">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-5511">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5511">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-5512">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-5512">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-5513">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5513">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-5514">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-5514">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-5515">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5515">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-5516">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5516">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5517">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5517">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5518">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-5518">CPU Lockable</span></span> | \- |
| <span data-ttu-id="e1135-5519">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-5519">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5520">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5520">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5521">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-5521">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-5522">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-5522">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-5523">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5523">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-5524">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-5524">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-5525">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-5525">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-5526">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5526">Video Decoder Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5528">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5528">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5530">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5530">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5532">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-5532">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-5533">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-5533">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="e1135-5534">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="e1135-5534">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="e1135-5535">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-5535">Target</span></span> | <span data-ttu-id="e1135-5536">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-5536">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-5537">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-5537">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-5538">16</span><span class="sxs-lookup"><span data-stu-id="e1135-5538">16</span></span> |
| <span data-ttu-id="e1135-5539">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5539">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5541">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-5541">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5542">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5542">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5543">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5543">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5544">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-5544">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5545">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-5545">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-5546">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-5546">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5548">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-5548">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-5549">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-5549">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-5550">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-5550">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-5551">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-5551">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-5552">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-5552">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-5553">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-5553">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-5554">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-5554">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-5555">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-5555">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-5556">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-5556">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-5557">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-5557">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-5558">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-5558">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5559">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-5559">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5560">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-5560">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-5561">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-5561">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-5562">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5562">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5563">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-5563">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5564">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-5564">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-5565">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-5565">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-5566">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5566">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-5567">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-5567">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-5568">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5568">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-5569">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-5569">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-5570">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5570">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-5571">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5571">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5572">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5572">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5573">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-5573">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5575">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-5575">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5576">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5576">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5577">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-5577">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-5578">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-5578">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-5579">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5579">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-5580">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-5580">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-5581">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-5581">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-5582">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5582">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5584">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5584">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5586">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5586">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5588">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-5588">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-5589">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-5589">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="e1135-5590">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="e1135-5590">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="e1135-5591">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-5591">Target</span></span> | <span data-ttu-id="e1135-5592">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-5592">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-5593">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-5593">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-5594">32</span><span class="sxs-lookup"><span data-stu-id="e1135-5594">32</span></span> |
| <span data-ttu-id="e1135-5595">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5595">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5597">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-5597">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5598">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5598">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5599">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5599">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5600">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-5600">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5601">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-5601">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-5602">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-5602">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-5604">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-5605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-5605">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-5606">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-5606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-5607">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-5607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-5608">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-5608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-5609">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-5609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-5610">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-5610">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-5611">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-5611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-5612">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-5612">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-5613">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-5613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-5614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-5614">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5615">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-5615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5616">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-5616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-5617">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-5617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-5618">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5619">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-5619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5620">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-5620">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-5621">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-5621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-5622">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-5623">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-5623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-5624">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-5625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-5625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-5626">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-5627">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5628">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5629">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-5629">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5631">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-5631">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5632">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5632">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5633">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-5633">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-5634">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-5634">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-5635">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5635">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-5636">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-5636">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-5637">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-5637">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-5638">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5638">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5640">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5640">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5642">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5642">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5644">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-5644">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-5645">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-5645">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="e1135-5646">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="e1135-5646">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="e1135-5647">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-5647">Target</span></span> | <span data-ttu-id="e1135-5648">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-5648">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-5649">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-5649">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-5650">32</span><span class="sxs-lookup"><span data-stu-id="e1135-5650">32</span></span> |
| <span data-ttu-id="e1135-5651">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5651">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5653">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-5653">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5654">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5654">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5655">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5655">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5656">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-5656">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5657">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-5657">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-5658">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-5658">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5660">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-5660">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-5661">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-5661">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-5662">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-5662">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-5663">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-5663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-5664">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-5664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-5665">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-5665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-5666">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-5666">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-5667">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-5667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-5668">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-5668">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-5669">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-5669">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-5670">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-5670">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5671">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-5671">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5672">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-5672">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-5673">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-5673">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-5674">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5674">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5675">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-5675">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5676">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-5676">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-5677">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-5677">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-5678">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5678">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-5679">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-5679">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-5680">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5680">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-5681">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-5681">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-5682">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5682">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-5683">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5683">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5684">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5684">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5685">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-5685">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5687">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-5687">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5688">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5688">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5689">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-5689">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-5690">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-5690">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-5691">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5691">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-5692">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-5692">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-5693">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-5693">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-5694">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5694">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5696">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5696">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5698">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5698">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5700">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-5700">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-5701">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-5701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="e1135-5702">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="e1135-5702">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="e1135-5703">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-5703">Target</span></span> | <span data-ttu-id="e1135-5704">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-5704">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-5705">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-5705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-5706">8</span><span class="sxs-lookup"><span data-stu-id="e1135-5706">8</span></span> |
| <span data-ttu-id="e1135-5707">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5707">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5709">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-5709">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5710">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5710">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5711">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5711">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5712">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-5712">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5713">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-5713">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-5714">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-5714">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5716">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-5716">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-5717">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-5717">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-5718">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-5718">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-5719">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-5719">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-5720">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-5720">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-5721">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-5721">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-5722">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-5722">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-5723">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-5723">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-5724">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-5724">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-5725">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-5725">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-5726">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-5726">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5727">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-5727">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5728">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-5728">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-5729">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-5729">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-5730">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5730">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5731">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-5731">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5732">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-5732">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-5733">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-5733">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-5734">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5734">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-5735">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-5735">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-5736">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5736">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-5737">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-5737">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-5738">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5738">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-5739">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5739">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5740">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5740">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5741">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-5741">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5743">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-5743">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5744">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5744">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5745">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-5745">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-5746">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-5746">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-5747">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5747">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-5748">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-5748">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-5749">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-5749">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-5750">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5750">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5752">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5752">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5754">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5754">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5756">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-5756">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-5757">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-5757">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="e1135-5758">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="e1135-5758">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="e1135-5759">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-5759">Target</span></span> | <span data-ttu-id="e1135-5760">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-5760">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-5761">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-5761">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-5762">8</span><span class="sxs-lookup"><span data-stu-id="e1135-5762">8</span></span> |
| <span data-ttu-id="e1135-5763">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5763">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5765">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-5765">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5766">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5766">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5767">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5767">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5768">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-5768">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5769">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-5769">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-5770">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-5770">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5772">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-5772">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-5773">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-5773">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-5774">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-5774">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-5775">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-5775">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-5776">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-5776">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-5777">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-5777">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-5778">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-5778">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-5779">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-5779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-5780">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-5780">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-5781">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-5781">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-5782">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-5782">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5783">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-5783">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5784">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-5784">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-5785">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-5785">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-5786">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5786">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5787">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-5787">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5788">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-5788">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-5789">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-5789">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-5790">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5790">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-5791">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-5791">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-5792">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5792">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-5793">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-5793">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-5794">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5794">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-5795">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5795">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5796">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5796">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5797">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-5797">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5799">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-5799">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5800">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5800">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5801">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-5801">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-5802">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-5802">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-5803">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5803">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-5804">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-5804">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-5805">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-5805">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-5806">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5806">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-5807">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5807">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5809">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5809">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-5810">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-5810">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-5811">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-5811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="e1135-5812">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="e1135-5812">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="e1135-5813">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-5813">Target</span></span> | <span data-ttu-id="e1135-5814">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-5814">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-5815">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-5815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-5816">8</span><span class="sxs-lookup"><span data-stu-id="e1135-5816">8</span></span> |
| <span data-ttu-id="e1135-5817">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5817">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5819">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-5819">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5820">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5821">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5822">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-5822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-5823">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-5824">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-5824">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5826">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-5826">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-5827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-5827">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-5828">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-5828">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-5829">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-5829">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-5830">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-5830">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-5831">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-5831">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-5832">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-5832">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-5833">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-5833">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-5834">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-5834">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-5835">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-5835">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-5836">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-5836">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5837">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-5837">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5838">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-5838">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-5839">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-5839">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-5840">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5840">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5841">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-5841">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5842">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-5842">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-5843">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-5843">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-5844">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5844">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-5845">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-5845">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-5846">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5846">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-5847">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-5847">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-5848">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5848">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-5849">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5849">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5850">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5850">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5851">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-5851">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5853">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-5853">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5854">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5854">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5855">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-5855">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-5856">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-5856">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-5857">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5857">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-5858">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-5858">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-5859">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-5859">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-5860">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5860">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-5861">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5861">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5863">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5863">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-5864">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-5864">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-5865">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-5865">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="e1135-5866">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="e1135-5866">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="e1135-5867">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-5867">Target</span></span> | <span data-ttu-id="e1135-5868">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-5868">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-5869">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-5869">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-5870">8</span><span class="sxs-lookup"><span data-stu-id="e1135-5870">8</span></span> |
| <span data-ttu-id="e1135-5871">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5871">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5873">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-5873">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5874">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5874">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5875">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5875">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5876">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-5876">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5877">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-5877">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-5878">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-5878">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5880">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-5880">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-5881">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-5881">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-5882">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-5882">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-5883">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-5883">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-5884">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-5884">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-5885">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-5885">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-5886">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-5886">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-5887">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-5887">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-5888">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-5888">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-5889">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-5889">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-5890">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-5890">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5891">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-5891">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5892">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-5892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-5893">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-5893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-5894">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5895">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-5895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5896">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-5896">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-5897">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-5897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-5898">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-5899">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-5899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-5900">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-5901">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-5901">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-5902">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-5903">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5904">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5905">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-5905">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5907">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-5907">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5908">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5908">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5909">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-5909">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-5910">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-5910">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-5911">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5911">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-5912">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-5912">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-5913">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-5913">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-5914">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5914">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-5915">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5915">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5917">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5917">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-5918">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-5918">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-5919">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-5919">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="e1135-5920">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="e1135-5920">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="e1135-5921">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-5921">Target</span></span> | <span data-ttu-id="e1135-5922">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-5922">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-5923">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-5923">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-5924">16</span><span class="sxs-lookup"><span data-stu-id="e1135-5924">16</span></span> |
| <span data-ttu-id="e1135-5925">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5925">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-5927">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-5927">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5928">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5928">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5929">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5929">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5930">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-5930">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5931">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-5931">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-5932">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-5932">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5934">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-5934">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-5935">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-5935">TextureCube</span></span> | \- |
| <span data-ttu-id="e1135-5936">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-5936">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="e1135-5937">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-5937">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="e1135-5938">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-5938">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-5939">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-5939">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-5940">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-5940">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-5941">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-5941">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-5942">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-5942">Mipmap</span></span> | \- |
| <span data-ttu-id="e1135-5943">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-5943">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="e1135-5944">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-5944">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5945">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-5945">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5946">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-5946">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-5947">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-5947">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-5948">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5948">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5949">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-5949">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-5950">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-5950">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-5951">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-5951">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-5952">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5952">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-5953">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-5953">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-5954">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5954">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-5955">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-5955">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-5956">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-5956">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-5957">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5957">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5958">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-5958">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-5959">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-5959">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5961">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-5961">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5962">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5962">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-5963">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-5963">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-5964">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-5964">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-5965">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-5965">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-5966">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-5966">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-5967">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-5967">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-5968">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5968">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-5969">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5969">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5971">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-5971">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-5972">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-5972">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-5973">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-5973">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="e1135-5974">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="e1135-5974">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="e1135-5975">Destino</span><span class="sxs-lookup"><span data-stu-id="e1135-5975">Target</span></span> | <span data-ttu-id="e1135-5976">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e1135-5976">Support</span></span> |
| - | - |
| <span data-ttu-id="e1135-5977">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="e1135-5977">Bits Per Element (BPE)</span></span> | <span data-ttu-id="e1135-5978">16</span><span class="sxs-lookup"><span data-stu-id="e1135-5978">16</span></span> |
| <span data-ttu-id="e1135-5979">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="e1135-5979">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5981">Buffer</span><span class="sxs-lookup"><span data-stu-id="e1135-5981">Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5982">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5982">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5983">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="e1135-5983">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5984">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="e1135-5984">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="e1135-5985">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1135-5985">Texture1D</span></span> | \- |
| <span data-ttu-id="e1135-5986">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1135-5986">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5988">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1135-5988">Texture3D</span></span> | \- |
| <span data-ttu-id="e1135-5989">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1135-5989">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5991">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="e1135-5991">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5993">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="e1135-5993">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-5995">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="e1135-5995">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="e1135-5996">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="e1135-5996">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="e1135-5997">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="e1135-5997">Shader gather4</span></span> | \- |
| <span data-ttu-id="e1135-5998">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="e1135-5998">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="e1135-5999">Mapa</span><span class="sxs-lookup"><span data-stu-id="e1135-5999">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-6001">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="e1135-6001">Mipmap Auto-Generation</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="e1135-6003">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="e1135-6003">RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-6004">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="e1135-6004">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-6005">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="e1135-6005">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="e1135-6006">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="e1135-6006">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="e1135-6007">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="e1135-6007">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-6008">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="e1135-6008">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="e1135-6009">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-6009">Typed UAV</span></span> | \- |
| <span data-ttu-id="e1135-6010">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="e1135-6010">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="e1135-6011">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-6011">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="e1135-6012">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="e1135-6012">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="e1135-6013">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-6013">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="e1135-6014">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="e1135-6014">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="e1135-6015">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="e1135-6015">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="e1135-6016">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-6016">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-6017">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="e1135-6017">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="e1135-6018">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="e1135-6018">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="e1135-6020">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="e1135-6020">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-6021">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-6021">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="e1135-6022">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="e1135-6022">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="e1135-6023">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="e1135-6023">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="e1135-6024">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="e1135-6024">Multisample Load</span></span> | \- |
| <span data-ttu-id="e1135-6025">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="e1135-6025">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="e1135-6026">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="e1135-6026">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="e1135-6027">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-6027">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="e1135-6028">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-6028">Video Processor Input</span></span> | \- |
| <span data-ttu-id="e1135-6029">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-6029">Video Processor Output</span></span> | \- |
| <span data-ttu-id="e1135-6030">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="e1135-6030">Shared Resource</span></span> | \- |
| <span data-ttu-id="e1135-6031">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="e1135-6031">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="e1135-6032">Dar formato a notas</span><span class="sxs-lookup"><span data-stu-id="e1135-6032">Format notes</span></span>

<span data-ttu-id="e1135-6033">El propósito del formato puede cambiar de un nivel de característica de hardware a otro.</span><span class="sxs-lookup"><span data-stu-id="e1135-6033">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="e1135-6034"><sup>L</sup> : formato sin tipo</span><span class="sxs-lookup"><span data-stu-id="e1135-6034"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="e1135-6035"><sup>PC</sup> : diseño parcialmente tipado, de conversión de tipos y sencillo</span><span class="sxs-lookup"><span data-stu-id="e1135-6035"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="e1135-6036"><sup>FCS</sup> : diseño totalmente tipado, convertible y sencillo</span><span class="sxs-lookup"><span data-stu-id="e1135-6036"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="e1135-6037"><sup>FNS</sup> : diseño totalmente tipado, sin conversión y simple</span><span class="sxs-lookup"><span data-stu-id="e1135-6037"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="e1135-6038"><sup>PCC</sup> : diseño parcialmente tipado, convertible y complejo</span><span class="sxs-lookup"><span data-stu-id="e1135-6038"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="e1135-6039"><sup>FCC</sup> : diseño totalmente tipado, convertible y complejo</span><span class="sxs-lookup"><span data-stu-id="e1135-6039"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="e1135-6040"><sup>FNC</sup> : diseño totalmente tipado, no convertible y complejo</span><span class="sxs-lookup"><span data-stu-id="e1135-6040"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="e1135-6041"><sup>V</sup> : formato de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1135-6041"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="e1135-6042">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1135-6042">Related topics</span></span>

[<span data-ttu-id="e1135-6043">Niveles de características de hardware de D3D12</span><span class="sxs-lookup"><span data-stu-id="e1135-6043">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

<span data-ttu-id="e1135-6044">[Implementación de búferes de sombra para el nivel de característica 9 de Direct3D](/previous-versions/windows/apps/jj262110(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="e1135-6044">[Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10))</span></span>

[<span data-ttu-id="e1135-6045">Asignar formatos heredados</span><span class="sxs-lookup"><span data-stu-id="e1135-6045">Mapping Legacy Formats</span></span>](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[<span data-ttu-id="e1135-6046">Guía de programación para DXGI</span><span class="sxs-lookup"><span data-stu-id="e1135-6046">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
