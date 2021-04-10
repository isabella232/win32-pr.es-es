---
description: En esta sección se especifican los formatos ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que se admiten en el hardware de nivel de característica de Direct3D 10,0.
ms.assetid: 3C1CCA7D-9F2F-4B1B-8424-BA9C6DED4974
title: Compatibilidad con el formato de hardware de la característica de nivel 10.0 de Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f298460330feb2143b20da37ae82c3a6d63790
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274662"
---
# <a name="format-support-for-direct3d-feature-level-100-hardware"></a><span data-ttu-id="0fc30-103">Compatibilidad con el formato de hardware de la característica de nivel 10.0 de Direct3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-103">Format support for Direct3D Feature Level 10.0 hardware</span></span>

<span data-ttu-id="0fc30-104">En esta sección se especifican los formatos ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que se admiten en el hardware de nivel de característica de Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="0fc30-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 10.0 hardware.</span></span>

<span data-ttu-id="0fc30-105">En la tabla se resume la compatibilidad de las características con la siguiente clave.</span><span class="sxs-lookup"><span data-stu-id="0fc30-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="0fc30-106">Símbolo</span><span class="sxs-lookup"><span data-stu-id="0fc30-106">Symbol</span></span>                            | <span data-ttu-id="0fc30-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fc30-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="0fc30-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="0fc30-108">_ *-*\*</span></span>                             | <span data-ttu-id="0fc30-109">No permitido o no disponible.</span><span class="sxs-lookup"><span data-stu-id="0fc30-109">Disallowed or not available.</span></span>                                                  |
| ![requerido](images/letter-r.jpg)  | <span data-ttu-id="0fc30-111">Se requiere compatibilidad con hardware.</span><span class="sxs-lookup"><span data-stu-id="0fc30-111">Hardware support is required.</span></span>                                                 |
| ![opcional](images/letter-o.jpg)  | <span data-ttu-id="0fc30-113">Compatibilidad de hardware opcional, el formato puede ser o no acelerado por hardware.</span><span class="sxs-lookup"><span data-stu-id="0fc30-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dependientes](images/letter-d.jpg) | <span data-ttu-id="0fc30-115">Requerido si se admite la característica opcional relacionada.</span><span class="sxs-lookup"><span data-stu-id="0fc30-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="0fc30-116">Este tema contiene una sección por formato.</span><span class="sxs-lookup"><span data-stu-id="0fc30-116">This topic contains a section per format.</span></span> <span data-ttu-id="0fc30-117">Un *destino* de formato (las tablas contienen una fila por destino) puede ser un tipo de recurso, una función intrínseca de HLSL o una funcionalidad determinada que depende de un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="0fc30-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="0fc30-118">Para comprobar mediante programación la compatibilidad de formato en D3D11 y D3D12, consulte Comprobación de la compatibilidad de las [características de hardware](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="0fc30-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="0fc30-119">Los números de los formatos son principalmente, pero no todos, en orden numérico ascendente; &mdash; algunos están fuera del orden numérico y se enumeran junto con otros formatos relevantes.</span><span class="sxs-lookup"><span data-stu-id="0fc30-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="0fc30-120">Tenga en cuenta también que los *tipos sin tipo* en un nombre de formato pueden significar un tipo *parcial* y no tienen un tipo estricto (consulte la sección [notas de formato](#format-notes) al final del tema).</span><span class="sxs-lookup"><span data-stu-id="0fc30-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>
 
## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="0fc30-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="0fc30-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="0fc30-122">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-122">Target</span></span> | <span data-ttu-id="0fc30-123">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-123">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-124">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-125">0</span><span class="sxs-lookup"><span data-stu-id="0fc30-125">0</span></span> |
| <span data-ttu-id="0fc30-126">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-126">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-128">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-128">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-130">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-131">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-132">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-133">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-134">Texture2D</span></span> | \- |
| <span data-ttu-id="0fc30-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-135">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-136">TextureCube</span></span> | \- |
| <span data-ttu-id="0fc30-137">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-137">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-138">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-139">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-139">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-140">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-140">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-141">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-142">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-142">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-143">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-143">Mipmap</span></span> | \- |
| <span data-ttu-id="0fc30-144">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-146">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-147">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-148">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-149">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-150">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-151">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-151">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-152">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-153">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-154">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-155">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-156">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-157">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-158">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-159">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-160">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-160">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-162">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-163">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-164">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-165">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-166">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-166">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-167">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-168">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-168">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-169">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-170">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-171">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-172">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-172">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-173">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="0fc30-174">DXGI_FORMAT_R32G32B32A32 de \_ <sup>equipos</sup> sin tipo (1)</span><span class="sxs-lookup"><span data-stu-id="0fc30-174">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="0fc30-175">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-175">Target</span></span> | <span data-ttu-id="0fc30-176">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-176">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-177">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-178">128</span><span class="sxs-lookup"><span data-stu-id="0fc30-178">128</span></span> |
| <span data-ttu-id="0fc30-179">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-179">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-181">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-181">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-182">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-182">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-183">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-183">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-184">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-184">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-185">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-185">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-187">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-189">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-189">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-191">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-191">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-193">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-193">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-194">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-194">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-195">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-195">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-196">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-196">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-197">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-197">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-198">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-198">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-199">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-199">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-201">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-201">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-202">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-202">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-203">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-203">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-204">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-204">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-205">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-206">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-207">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-208">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-208">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-209">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-209">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-210">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-210">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-211">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-211">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-212">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-212">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-213">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-213">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-214">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-214">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-215">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-215">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-216">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-216">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-217">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-217">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-219">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-219">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-220">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-220">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-221">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-221">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-222">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-222">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-223">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-223">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-224">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-224">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-225">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-225">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-227">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-227">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-228">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-228">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-229">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-229">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-230">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-230">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-232">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-232">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="0fc30-233">DXGI_FORMAT_R32G32B32A32 \_ float<sup>FCS</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="0fc30-233">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="0fc30-234">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-234">Target</span></span> | <span data-ttu-id="0fc30-235">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-235">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-236">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-236">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-237">128</span><span class="sxs-lookup"><span data-stu-id="0fc30-237">128</span></span> |
| <span data-ttu-id="0fc30-238">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-238">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-240">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-240">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-242">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-242">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-244">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-244">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-245">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-245">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-247">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-249">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-249">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-251">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-253">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-253">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-255">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-255">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-257">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-257">Shader sample (any filter)</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-259">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-260">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-261">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-261">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-262">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-263">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-263">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-265">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-265">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-267">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-267">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-269">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-269">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-271">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-272">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-273">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-274">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-275">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-275">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-276">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-276">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-277">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-277">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-278">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-278">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-279">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-279">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-280">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-280">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-281">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-281">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-282">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-282">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-283">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-283">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-284">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-284">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-286">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-286">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-288">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-288">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-290">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-290">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-292">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-292">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-294">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-294">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-296">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-296">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-297">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-297">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-299">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-299">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-300">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-300">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-301">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-301">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-302">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-302">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-304">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-304">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="0fc30-305">DXGI_FORMAT_R32G32B32A32 \_ uint<sup>FCS</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="0fc30-305">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="0fc30-306">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-306">Target</span></span> | <span data-ttu-id="0fc30-307">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-307">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-308">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-308">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-309">128</span><span class="sxs-lookup"><span data-stu-id="0fc30-309">128</span></span> |
| <span data-ttu-id="0fc30-310">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-310">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-312">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-312">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-314">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-314">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-316">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-316">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-317">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-317">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-319">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-319">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-321">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-321">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-323">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-323">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-325">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-325">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-327">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-327">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-329">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-329">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-330">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-330">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-331">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-331">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-332">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-332">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-333">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-333">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-334">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-334">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-336">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-336">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-337">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-337">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-339">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-339">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-340">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-340">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-342">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-342">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-343">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-343">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-344">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-344">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-345">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-345">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-346">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-346">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-347">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-347">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-348">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-348">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-349">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-349">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-350">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-350">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-351">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-351">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-352">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-352">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-353">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-353">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-354">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-354">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-356">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-356">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-358">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-358">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-360">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-360">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-362">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-362">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-363">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-363">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-365">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-365">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-366">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-366">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-368">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-369">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-370">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-371">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-371">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-373">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-373">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="0fc30-374">DXGI_FORMAT_R32G32B32A32 \_ San<sup>FCS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="0fc30-374">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="0fc30-375">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-375">Target</span></span> | <span data-ttu-id="0fc30-376">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-376">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-377">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-377">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-378">128</span><span class="sxs-lookup"><span data-stu-id="0fc30-378">128</span></span> |
| <span data-ttu-id="0fc30-379">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-379">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-381">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-381">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-383">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-383">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-385">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-385">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-386">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-386">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-388">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-388">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-390">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-390">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-392">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-392">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-394">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-396">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-396">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-398">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-399">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-400">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-401">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-401">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-402">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-403">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-403">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-405">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-406">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-406">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-408">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-409">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-410">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-411">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-412">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-413">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-414">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-415">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-416">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-417">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-419">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-420">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-421">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-422">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-422">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-424">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-424">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-426">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-426">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-428">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-428">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-430">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-430">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-431">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-431">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-433">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-434">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-434">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-436">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-437">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-438">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-439">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-439">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-441">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="0fc30-442">DXGI_FORMAT_R32G32B32 de \_ <sup>equipos</sup> sin tipo (5)</span><span class="sxs-lookup"><span data-stu-id="0fc30-442">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="0fc30-443">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-443">Target</span></span> | <span data-ttu-id="0fc30-444">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-444">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-445">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-446">96</span><span class="sxs-lookup"><span data-stu-id="0fc30-446">96</span></span> |
| <span data-ttu-id="0fc30-447">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-447">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-449">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-449">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-450">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-451">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-452">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-453">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-455">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-455">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-457">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-459">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-459">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-461">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-461">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-462">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-462">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-463">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-463">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-464">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-464">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-465">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-465">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-466">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-466">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-467">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-467">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-469">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-470">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-471">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-472">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-473">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-474">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-475">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-476">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-476">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-477">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-478">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-479">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-480">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-481">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-481">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-482">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-483">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-484">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-485">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-485">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-487">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-487">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-488">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-488">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-489">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-489">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-490">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-490">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-491">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-491">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-492">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-492">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-493">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-493">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-495">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-496">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-497">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-498">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-498">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-499">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="0fc30-500">DXGI_FORMAT_R32G32B32 \_ float<sup>FCS</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="0fc30-500">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="0fc30-501">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-501">Target</span></span> | <span data-ttu-id="0fc30-502">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-502">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-503">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-504">96</span><span class="sxs-lookup"><span data-stu-id="0fc30-504">96</span></span> |
| <span data-ttu-id="0fc30-505">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-505">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-507">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-507">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-509">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-509">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-511">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-511">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-512">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-512">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-514">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-514">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-516">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-518">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-520">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-522">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-522">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-524">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-524">Shader sample (any filter)</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-526">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-526">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-527">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-527">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-528">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-528">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-529">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-529">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-530">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-530">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-532">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-532">Mipmap Auto-Generation</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-534">RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-536">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-536">Blendable RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="0fc30-538">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-538">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-539">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-539">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-540">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-540">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-541">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-541">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-542">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-542">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-543">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-543">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-544">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-544">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-545">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-545">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-546">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-546">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-547">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-547">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-548">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-548">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-549">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-549">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-550">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-550">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-551">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-551">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-553">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-553">4x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="0fc30-555">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-555">8x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="0fc30-557">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-557">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-559">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-559">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-561">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-561">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-563">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-563">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-564">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-564">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-566">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-566">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-567">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-567">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-568">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-568">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-569">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-569">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-570">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-570">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="0fc30-571">DXGI_FORMAT_R32G32B32 \_ uint<sup>FCS</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="0fc30-571">DXGI_FORMAT_R32G32B32\_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="0fc30-572">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-572">Target</span></span> | <span data-ttu-id="0fc30-573">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-573">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-574">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-574">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-575">96</span><span class="sxs-lookup"><span data-stu-id="0fc30-575">96</span></span> |
| <span data-ttu-id="0fc30-576">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-576">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-578">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-578">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-580">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-580">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-582">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-583">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-583">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-585">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-587">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-589">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-591">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-591">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-593">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-593">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-595">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-595">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-596">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-596">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-597">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-597">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-598">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-598">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-599">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-600">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-600">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-602">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-602">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-603">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-603">RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-605">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-606">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-606">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-608">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-608">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-609">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-609">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-610">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-610">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-611">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-611">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-612">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-612">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-613">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-613">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-614">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-614">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-615">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-615">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-616">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-616">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-617">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-617">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-618">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-618">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-619">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-619">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-620">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-620">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-622">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-622">4x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="0fc30-624">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-624">8x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="0fc30-626">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-626">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-628">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-628">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-629">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-629">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-631">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-631">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-632">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-632">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-634">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-634">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-635">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-635">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-636">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-636">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-637">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-637">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-638">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-638">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="0fc30-639">DXGI_FORMAT_R32G32B32 \_ San<sup>FCS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="0fc30-639">DXGI_FORMAT_R32G32B32\_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="0fc30-640">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-640">Target</span></span> | <span data-ttu-id="0fc30-641">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-641">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-642">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-642">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-643">96</span><span class="sxs-lookup"><span data-stu-id="0fc30-643">96</span></span> |
| <span data-ttu-id="0fc30-644">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-644">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-646">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-646">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-648">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-648">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-650">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-650">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-651">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-651">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-653">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-655">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-657">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-659">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-661">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-661">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-663">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-664">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-665">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-666">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-666">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-667">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-668">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-668">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-670">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-670">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-671">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-671">RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-673">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-673">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-674">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-675">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-676">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-677">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-678">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-678">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-679">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-680">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-681">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-682">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-683">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-683">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-684">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-685">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-686">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-687">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-687">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-689">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-689">4x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="0fc30-691">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-691">8x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="0fc30-693">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-693">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-695">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-696">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-696">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-698">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-698">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-699">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-699">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-701">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-701">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-702">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-702">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-703">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-703">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-704">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-704">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-705">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-705">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="0fc30-706">DXGI_FORMAT_R16G16B16A16 de \_ <sup>equipos</sup> sin tipo (9)</span><span class="sxs-lookup"><span data-stu-id="0fc30-706">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="0fc30-707">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-707">Target</span></span> | <span data-ttu-id="0fc30-708">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-708">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-709">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-709">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-710">64</span><span class="sxs-lookup"><span data-stu-id="0fc30-710">64</span></span> |
| <span data-ttu-id="0fc30-711">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-711">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-713">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-713">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-714">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-714">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-715">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-715">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-716">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-716">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-717">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-717">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-719">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-719">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-721">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-721">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-723">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-723">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-725">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-725">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-726">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-726">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-727">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-727">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-728">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-728">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-729">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-729">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-730">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-730">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-731">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-731">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-733">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-733">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-734">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-734">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-735">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-735">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-736">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-736">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-737">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-738">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-739">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-740">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-740">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-741">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-741">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-742">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-742">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-743">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-743">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-744">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-744">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-745">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-745">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-746">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-746">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-747">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-747">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-748">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-748">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-749">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-749">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-751">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-751">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-752">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-752">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-753">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-753">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-754">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-754">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-755">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-755">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-756">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-756">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-757">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-757">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-759">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-759">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-760">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-760">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-761">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-761">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-762">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-762">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-764">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-764">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="0fc30-765">DXGI_FORMAT_R16G16B16A16 \_ de<sup>FCS</sup> Float (10)</span><span class="sxs-lookup"><span data-stu-id="0fc30-765">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="0fc30-766">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-766">Target</span></span> | <span data-ttu-id="0fc30-767">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-767">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-768">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-768">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-769">64</span><span class="sxs-lookup"><span data-stu-id="0fc30-769">64</span></span> |
| <span data-ttu-id="0fc30-770">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-770">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-772">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-772">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-774">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-774">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-776">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-776">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-777">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-777">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-778">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-778">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-780">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-780">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-782">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-782">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-784">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-786">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-786">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-788">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-788">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-790">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-790">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-791">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-791">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-792">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-792">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-793">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-793">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-794">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-794">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-796">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-796">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-798">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-798">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-800">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-800">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-802">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-802">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-803">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-803">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-804">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-804">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-805">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-805">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-806">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-806">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-807">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-807">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-808">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-808">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-809">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-809">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-810">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-810">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-811">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-811">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-812">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-812">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-813">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-813">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-814">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-814">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-815">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-815">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-817">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-817">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-819">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-819">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-821">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-821">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-823">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-823">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-825">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-825">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-827">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-827">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-829">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-829">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-831">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-831">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-832">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-832">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-834">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-834">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-836">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-836">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-838">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-838">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="0fc30-839">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FCS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="0fc30-839">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="0fc30-840">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-840">Target</span></span> | <span data-ttu-id="0fc30-841">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-841">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-842">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-842">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-843">64</span><span class="sxs-lookup"><span data-stu-id="0fc30-843">64</span></span> |
| <span data-ttu-id="0fc30-844">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-844">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-846">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-846">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-848">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-848">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-850">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-850">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-851">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-851">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-852">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-852">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-854">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-854">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-856">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-856">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-858">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-860">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-860">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-862">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-862">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-864">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-864">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-865">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-865">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-866">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-866">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-867">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-867">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-868">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-868">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-870">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-870">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-872">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-872">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-874">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-874">Blendable RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-876">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-877">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-878">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-879">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-880">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-880">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-881">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-882">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-883">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-884">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-885">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-886">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-887">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-888">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-889">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-889">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-891">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-891">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-893">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-893">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-895">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-895">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-897">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-897">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-899">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-899">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-901">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-901">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-902">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-902">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-904">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-905">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-906">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-907">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-907">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-909">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-909">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="0fc30-910">DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FCS</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="0fc30-910">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="0fc30-911">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-911">Target</span></span> | <span data-ttu-id="0fc30-912">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-912">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-913">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-913">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-914">64</span><span class="sxs-lookup"><span data-stu-id="0fc30-914">64</span></span> |
| <span data-ttu-id="0fc30-915">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-915">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-917">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-917">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-919">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-919">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-921">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-921">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-922">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-922">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-923">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-923">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-925">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-927">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-929">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-929">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-931">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-931">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-933">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-934">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-935">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-936">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-936">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-937">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-938">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-938">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-940">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-940">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-941">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-941">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-943">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-943">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-944">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-944">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-946">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-946">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-947">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-947">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-948">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-948">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-949">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-949">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-950">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-950">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-951">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-951">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-952">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-952">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-953">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-953">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-954">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-954">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-955">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-955">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-956">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-956">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-957">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-957">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-958">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-958">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-960">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-960">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-962">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-962">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-964">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-964">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-966">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-966">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-967">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-967">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-969">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-969">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-970">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-970">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-972">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-972">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-973">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-973">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-974">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-974">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-975">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-975">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-977">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-977">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="0fc30-978">DXGI_FORMAT_R16G16B16A16 \_ SNORM<sup>FCS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="0fc30-978">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="0fc30-979">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-979">Target</span></span> | <span data-ttu-id="0fc30-980">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-980">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-981">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-981">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-982">64</span><span class="sxs-lookup"><span data-stu-id="0fc30-982">64</span></span> |
| <span data-ttu-id="0fc30-983">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-983">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-985">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-985">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-987">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-987">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-989">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-990">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-991">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-993">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-993">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-995">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-995">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-997">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-997">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-999">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-999">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1001">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1001">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1003">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1003">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1004">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1004">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1005">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-1005">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-1006">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-1006">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-1007">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-1007">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1009">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-1009">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-1011">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1013">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-1013">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1014">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-1014">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-1015">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-1015">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-1016">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1016">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1017">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1017">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1018">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1018">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-1019">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-1019">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-1020">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1020">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-1021">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-1021">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-1022">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1022">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-1023">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-1023">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-1024">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1024">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-1025">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1025">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1026">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1026">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1027">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1027">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1029">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-1029">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1031">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1031">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1033">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-1033">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1035">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1035">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1037">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1037">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1039">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-1039">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-1040">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-1040">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1042">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1042">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-1043">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1043">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-1044">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1044">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-1045">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-1045">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1047">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1047">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="0fc30-1048">DXGI_FORMAT_R16G16B16A16 \_ San<sup>FCS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1048">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="0fc30-1049">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-1049">Target</span></span> | <span data-ttu-id="0fc30-1050">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1050">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-1051">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1051">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-1052">64</span><span class="sxs-lookup"><span data-stu-id="0fc30-1052">64</span></span> |
| <span data-ttu-id="0fc30-1053">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1053">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1055">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-1055">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1057">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1057">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1059">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1059">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1060">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1060">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1061">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1061">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1063">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1063">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1065">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1065">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1067">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-1067">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1069">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-1069">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1071">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1071">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1072">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1072">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1073">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1073">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1074">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-1074">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-1075">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-1075">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-1076">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-1076">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1078">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-1078">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-1079">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-1079">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1081">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-1081">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1082">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-1082">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-1083">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-1083">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-1084">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1084">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1085">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1085">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1086">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1086">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-1087">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-1087">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-1088">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1088">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-1089">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-1089">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-1090">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1090">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-1091">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-1091">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-1092">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1092">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-1093">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1093">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1094">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1094">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1095">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1095">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1097">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-1097">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1099">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1099">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1101">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-1101">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1103">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1103">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-1104">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1104">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1106">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-1106">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-1107">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-1107">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1109">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1109">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-1110">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1110">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-1111">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1111">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-1112">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-1112">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1114">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1114">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="0fc30-1115">DXGI_FORMAT_R32G32 de \_ <sup>equipos</sup> sin tipo (15)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1115">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="0fc30-1116">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-1116">Target</span></span> | <span data-ttu-id="0fc30-1117">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1117">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-1118">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1118">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-1119">64</span><span class="sxs-lookup"><span data-stu-id="0fc30-1119">64</span></span> |
| <span data-ttu-id="0fc30-1120">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1120">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1122">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-1122">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1123">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1123">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1124">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1124">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1125">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1125">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1126">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1128">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1130">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1132">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-1132">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1134">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-1134">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-1135">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1135">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1136">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1136">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1137">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1137">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1138">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-1138">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-1139">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-1139">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-1140">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-1140">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1142">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-1142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-1143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-1143">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1144">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-1144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1145">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-1145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-1146">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-1146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-1147">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1148">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1149">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1149">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-1150">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-1150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-1151">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-1152">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-1152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-1153">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-1154">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-1154">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-1155">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-1156">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1157">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1158">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1158">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1160">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-1160">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1161">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1161">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1162">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-1162">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-1163">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1163">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-1164">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1164">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-1165">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-1165">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-1166">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-1166">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1168">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1168">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-1169">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1169">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-1170">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1170">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-1171">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-1171">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-1172">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1172">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="0fc30-1173">DXGI_FORMAT_R32G32 \_ float<sup>FCS</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1173">DXGI_FORMAT_R32G32\_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="0fc30-1174">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-1174">Target</span></span> | <span data-ttu-id="0fc30-1175">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1175">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-1176">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1176">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-1177">64</span><span class="sxs-lookup"><span data-stu-id="0fc30-1177">64</span></span> |
| <span data-ttu-id="0fc30-1178">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1178">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1180">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-1180">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1182">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1182">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1184">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1184">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1185">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1185">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1187">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1187">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1189">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1189">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1191">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1191">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1193">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-1193">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1195">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-1195">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1197">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1197">Shader sample (any filter)</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1199">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1199">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1200">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1200">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1201">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-1201">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-1202">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-1202">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-1203">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-1203">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1205">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-1205">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1207">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-1207">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1209">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-1209">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1211">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-1211">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-1212">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-1212">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-1213">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1213">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1214">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1214">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1215">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1215">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-1216">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-1216">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-1217">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1217">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-1218">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-1218">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-1219">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1219">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-1220">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-1220">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-1221">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1221">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-1222">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1222">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1223">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1223">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1224">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1224">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1226">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-1226">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1228">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1228">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1230">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-1230">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1232">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1232">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1234">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1234">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1236">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-1236">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-1237">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-1237">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1239">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1239">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-1240">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1240">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-1241">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1241">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-1242">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-1242">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-1243">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1243">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="0fc30-1244">DXGI_FORMAT_R32G32 \_ uint<sup>FCS</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1244">DXGI_FORMAT_R32G32\_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="0fc30-1245">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-1245">Target</span></span> | <span data-ttu-id="0fc30-1246">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1246">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-1247">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1247">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-1248">64</span><span class="sxs-lookup"><span data-stu-id="0fc30-1248">64</span></span> |
| <span data-ttu-id="0fc30-1249">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1249">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1251">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-1251">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1253">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1253">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1255">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1255">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1256">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1256">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1258">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1258">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1260">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1260">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1262">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1262">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1264">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-1264">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1266">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-1266">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1268">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1268">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1269">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1269">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1270">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1270">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1271">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-1271">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-1272">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-1272">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-1273">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-1273">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1275">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-1275">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-1276">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-1276">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1278">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-1278">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1279">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-1279">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1281">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-1281">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-1282">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1282">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1283">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1283">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1284">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1284">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-1285">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-1285">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-1286">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1286">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-1287">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-1287">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-1288">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1288">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-1289">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-1289">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-1290">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1290">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-1291">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1291">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1292">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1292">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1293">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1293">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1295">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-1295">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1297">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1297">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1299">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-1299">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1301">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1301">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-1302">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1302">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1304">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-1304">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-1305">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-1305">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1307">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1307">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-1308">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1308">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-1309">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1309">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-1310">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-1310">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-1311">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1311">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="0fc30-1312">DXGI_FORMAT_R32G32 \_ San<sup>FCS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1312">DXGI_FORMAT_R32G32\_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="0fc30-1313">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-1313">Target</span></span> | <span data-ttu-id="0fc30-1314">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1314">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-1315">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1315">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-1316">64</span><span class="sxs-lookup"><span data-stu-id="0fc30-1316">64</span></span> |
| <span data-ttu-id="0fc30-1317">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1317">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1319">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-1319">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1321">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1321">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1323">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1323">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1324">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1324">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1326">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1326">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1328">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1328">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1330">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1330">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1332">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-1332">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1334">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-1334">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1336">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1336">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1337">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1337">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1338">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1338">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1339">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-1339">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-1340">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-1340">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-1341">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-1341">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1343">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-1343">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-1344">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-1344">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1346">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-1346">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1347">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-1347">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-1348">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-1348">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-1349">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1349">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1350">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1350">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1351">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1351">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-1352">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-1352">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-1353">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1353">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-1354">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-1354">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-1355">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1355">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-1356">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-1356">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-1357">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1357">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-1358">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1358">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1359">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1359">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1360">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1360">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1362">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-1362">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1364">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1364">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1366">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-1366">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1368">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1368">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-1369">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1369">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1371">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-1371">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-1372">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-1372">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1374">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-1375">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-1376">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-1377">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-1377">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-1378">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="0fc30-1379">DXGI_FORMAT_R32G8X24 de \_ <sup>equipos</sup> sin tipo (19)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1379">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="0fc30-1380">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-1380">Target</span></span> | <span data-ttu-id="0fc30-1381">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1381">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-1382">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-1383">64</span><span class="sxs-lookup"><span data-stu-id="0fc30-1383">64</span></span> |
| <span data-ttu-id="0fc30-1384">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1384">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1386">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-1386">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1387">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1387">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1388">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1388">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1389">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1389">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1390">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1390">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1392">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1394">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1394">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-1395">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-1395">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1397">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-1397">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-1398">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1399">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1400">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1401">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-1401">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-1402">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-1402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-1403">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-1403">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1405">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-1405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-1406">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-1406">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1407">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-1407">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1408">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-1408">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-1409">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-1409">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-1410">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1410">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1411">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1411">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1412">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1412">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-1413">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-1413">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-1414">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1414">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-1415">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-1415">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-1416">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1416">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-1417">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-1417">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-1418">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1418">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-1419">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1419">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1420">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1420">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1421">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1421">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1423">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-1423">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1424">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1424">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1425">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-1425">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-1426">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1426">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-1427">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1427">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-1428">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-1428">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-1429">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-1429">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1431">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1431">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-1432">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1432">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-1433">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1433">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-1434">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-1434">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-1435">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1435">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfcssup-20"></a><span data-ttu-id="0fc30-1436">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FCS</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1436">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FCS</sup> (20)</span></span>
| <span data-ttu-id="0fc30-1437">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-1437">Target</span></span> | <span data-ttu-id="0fc30-1438">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1438">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-1439">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1439">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-1440">64</span><span class="sxs-lookup"><span data-stu-id="0fc30-1440">64</span></span> |
| <span data-ttu-id="0fc30-1441">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1441">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1443">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-1443">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1444">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1444">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1445">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1446">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1447">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1449">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1449">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1451">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1451">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-1452">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-1452">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1454">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-1454">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-1455">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1455">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1456">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1456">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1457">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1457">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1458">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-1458">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-1459">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-1459">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-1460">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-1460">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1462">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-1462">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-1463">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-1463">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1464">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-1464">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1465">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-1465">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-1466">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-1466">Depth/Stencil Target</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1468">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1468">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1469">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1469">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1470">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1470">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-1471">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-1471">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-1472">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1472">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-1473">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-1473">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-1474">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1474">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-1475">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-1475">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-1476">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1476">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-1477">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1477">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1478">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1478">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1479">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1479">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1481">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-1481">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1483">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1483">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1485">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-1485">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1487">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1487">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-1488">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1488">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-1489">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-1489">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-1490">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-1490">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1492">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1492">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-1493">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1493">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-1494">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1494">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-1495">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-1495">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-1496">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1496">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfcssup-21"></a><span data-ttu-id="0fc30-1497">DXGI_FORMAT_R32 \_ \_ X8X24 Float \_ sin tipo,<sup>FCS</sup> (21)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1497">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FCS</sup> (21)</span></span>
| <span data-ttu-id="0fc30-1498">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-1498">Target</span></span> | <span data-ttu-id="0fc30-1499">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1499">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-1500">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1500">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-1501">64</span><span class="sxs-lookup"><span data-stu-id="0fc30-1501">64</span></span> |
| <span data-ttu-id="0fc30-1502">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1502">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1504">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-1504">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1505">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1505">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1506">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1506">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1507">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1507">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1508">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1508">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1510">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1510">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1512">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-1513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-1513">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1515">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-1515">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1517">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1517">Shader sample (any filter)</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1519">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1519">Shader sample\_c (comparison filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1521">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1521">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1522">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-1522">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-1523">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-1523">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-1524">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-1524">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1526">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-1526">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-1527">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-1527">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1528">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-1528">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1529">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-1529">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-1530">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-1530">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-1531">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1531">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1532">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1532">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1533">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1533">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-1534">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-1534">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-1535">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1535">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-1536">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-1536">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-1537">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1537">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-1538">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-1538">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-1539">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1539">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-1540">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1540">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1541">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1541">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1542">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1542">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1544">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-1544">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1545">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1545">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1546">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-1546">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-1547">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1547">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-1548">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1548">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-1549">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-1549">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-1550">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-1550">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1552">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1552">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-1553">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1553">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-1554">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1554">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-1555">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-1555">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-1556">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1556">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfcssup-22"></a><span data-ttu-id="0fc30-1557">DXGI_FORMAT_X32 \_ \_ G8X24 \_ uint<sup>FC FCS</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1557">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FCS</sup> (22)</span></span>
| <span data-ttu-id="0fc30-1558">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-1558">Target</span></span> | <span data-ttu-id="0fc30-1559">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1559">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-1560">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1560">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-1561">64</span><span class="sxs-lookup"><span data-stu-id="0fc30-1561">64</span></span> |
| <span data-ttu-id="0fc30-1562">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1562">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1564">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-1564">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1565">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1565">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1566">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1566">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1567">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1567">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1568">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1568">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1570">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1570">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1572">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1572">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-1573">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-1573">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1575">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-1575">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1577">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1577">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1578">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1578">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1579">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1579">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1580">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-1580">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-1581">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-1581">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-1582">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-1582">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1584">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-1584">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-1585">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-1585">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1586">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-1586">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1587">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-1587">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-1588">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-1588">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-1589">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1589">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1590">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1590">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1591">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1591">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-1592">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-1592">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-1593">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1593">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-1594">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-1594">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-1595">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1595">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-1596">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-1596">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-1597">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1597">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-1598">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1598">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1599">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1599">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1600">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1600">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1602">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-1602">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1603">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1603">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1604">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-1604">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-1605">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1605">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-1606">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1606">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-1607">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-1607">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-1608">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-1608">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1610">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1610">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-1611">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1611">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-1612">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1612">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-1613">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-1613">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-1614">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1614">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="0fc30-1615">DXGI_FORMAT_R10G10B10A2 de \_ <sup>equipos</sup> sin tipo (23)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1615">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="0fc30-1616">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-1616">Target</span></span> | <span data-ttu-id="0fc30-1617">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1617">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-1618">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1618">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-1619">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-1619">32</span></span> |
| <span data-ttu-id="0fc30-1620">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1620">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1622">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-1622">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1623">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1623">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1624">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1624">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1625">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1625">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1626">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1626">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1628">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1628">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1630">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1630">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1632">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-1632">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1634">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-1634">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-1635">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1635">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1636">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1636">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1637">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1637">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1638">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-1638">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-1639">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-1639">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-1640">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-1640">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1642">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-1642">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-1643">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-1643">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1644">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-1644">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1645">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-1645">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-1646">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-1646">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-1647">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1647">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1648">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1648">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1649">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1649">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-1650">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-1650">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-1651">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1651">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-1652">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-1652">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-1653">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1653">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-1654">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-1654">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-1655">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1655">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-1656">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1656">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1657">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1657">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1658">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1658">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1660">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-1660">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1661">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1661">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1662">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-1662">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-1663">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1663">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-1664">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1664">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-1665">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-1665">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-1666">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-1666">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1668">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1668">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-1669">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1669">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-1670">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1670">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-1671">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-1671">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1673">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1673">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="0fc30-1674">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FCS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1674">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="0fc30-1675">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-1675">Target</span></span> | <span data-ttu-id="0fc30-1676">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1676">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-1677">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1677">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-1678">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-1678">32</span></span> |
| <span data-ttu-id="0fc30-1679">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1679">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1681">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-1681">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1683">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1683">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1685">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1685">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1686">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1686">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1687">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1687">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1689">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1689">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1691">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1691">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1693">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-1693">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1695">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-1695">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1697">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1697">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1699">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1699">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1700">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1700">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1701">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-1701">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-1702">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-1702">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-1703">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-1703">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1705">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-1705">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1707">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-1707">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1709">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-1709">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1711">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-1711">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-1712">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-1712">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-1713">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1713">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1714">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1714">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1715">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1715">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-1716">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-1716">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-1717">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1717">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-1718">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-1718">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-1719">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1719">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-1720">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-1720">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-1721">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1721">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-1722">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1722">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1723">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1723">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1724">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1724">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1726">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-1726">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1728">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1728">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1730">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-1730">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1732">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1732">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1734">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1734">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1736">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-1736">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1738">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-1738">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1740">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1740">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-1741">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1741">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1743">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1743">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1745">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-1745">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1747">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1747">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="0fc30-1748">DXGI_FORMAT_R10G10B10A2 \_ uint<sup>FCS</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1748">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="0fc30-1749">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-1749">Target</span></span> | <span data-ttu-id="0fc30-1750">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1750">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-1751">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1751">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-1752">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-1752">32</span></span> |
| <span data-ttu-id="0fc30-1753">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1753">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1755">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-1755">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1757">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1757">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1759">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1760">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1761">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1763">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1763">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1765">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1765">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1767">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-1767">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1769">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-1769">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1771">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1771">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1772">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1772">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1773">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1773">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1774">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-1774">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-1775">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-1775">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-1776">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-1776">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1778">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-1778">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-1779">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-1779">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1781">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-1781">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1782">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-1782">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1784">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-1784">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-1785">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1785">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1786">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1786">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1787">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1787">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-1788">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-1788">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-1789">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1789">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-1790">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-1790">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-1791">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1791">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-1792">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-1792">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-1793">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1793">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-1794">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1794">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1795">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1795">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1796">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1796">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1798">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-1798">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1800">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1800">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1802">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-1802">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1804">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1804">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-1805">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1805">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1807">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-1807">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-1808">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-1808">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1810">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1810">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-1811">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1811">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-1812">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1812">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-1813">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-1813">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1815">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1815">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="0fc30-1816">DXGI_FORMAT_R10G10B10 \_ la \_ inclinación de XR \_ a2 \_ UNORM<sup>FCS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1816">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="0fc30-1817">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-1817">Target</span></span> | <span data-ttu-id="0fc30-1818">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1818">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-1819">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1819">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-1820">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-1820">32</span></span> |
| <span data-ttu-id="0fc30-1821">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1821">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1823">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-1823">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1824">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1824">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1825">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1825">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1826">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1826">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1827">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1827">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-1828">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1828">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1830">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1830">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-1831">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-1831">TextureCube</span></span> | \- |
| <span data-ttu-id="0fc30-1832">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-1832">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-1833">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1833">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1834">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1834">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1835">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1835">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1836">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-1836">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-1837">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-1837">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-1838">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-1838">Mipmap</span></span> | \- |
| <span data-ttu-id="0fc30-1839">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-1839">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-1840">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-1840">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1841">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-1841">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1842">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-1842">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-1843">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-1843">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-1844">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1844">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1845">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1845">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1846">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1846">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-1847">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-1847">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-1848">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1848">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-1849">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-1849">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-1850">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1850">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-1851">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-1851">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-1852">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1852">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-1853">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1853">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1854">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1854">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1855">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1855">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1857">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-1857">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1858">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1858">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1859">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-1859">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-1860">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1860">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-1861">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1861">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-1862">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-1862">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1864">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-1864">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1866">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1866">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-1867">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1867">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1869">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1869">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1871">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-1871">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1873">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1873">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="0fc30-1874">DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1874">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="0fc30-1875">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-1875">Target</span></span> | <span data-ttu-id="0fc30-1876">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1876">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-1877">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1877">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-1878">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-1878">32</span></span> |
| <span data-ttu-id="0fc30-1879">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1879">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1881">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-1881">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1883">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1883">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1885">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1885">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1886">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1886">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1887">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1887">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1889">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1889">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1891">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1891">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1893">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-1893">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1895">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-1895">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1897">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1897">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1899">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1899">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1900">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1900">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1901">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-1901">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-1902">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-1902">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-1903">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-1903">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1905">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-1905">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1907">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-1907">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1909">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-1909">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1911">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-1911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-1912">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-1912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-1913">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1914">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1915">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1915">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-1916">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-1916">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-1917">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1917">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-1918">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-1918">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-1919">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1919">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-1920">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-1920">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-1921">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1921">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-1922">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1922">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1923">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1923">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1924">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1924">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1926">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-1926">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1928">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1928">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1930">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-1930">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1932">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1932">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1934">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1934">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-1936">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-1936">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-1937">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-1937">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-1938">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1938">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-1939">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1939">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-1940">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1940">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-1941">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-1941">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-1942">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1942">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="0fc30-1943">DXGI_FORMAT_R8G8B8A8 de \_ <sup>equipos</sup> sin tipo (27)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1943">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="0fc30-1944">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-1944">Target</span></span> | <span data-ttu-id="0fc30-1945">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-1945">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-1946">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1946">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-1947">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-1947">32</span></span> |
| <span data-ttu-id="0fc30-1948">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1948">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1950">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-1950">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1951">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1951">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1952">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1952">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1953">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1953">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-1954">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1954">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1956">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1956">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1958">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-1958">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1960">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-1960">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1962">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-1962">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-1963">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1963">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1964">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1964">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1965">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-1965">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-1966">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-1966">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-1967">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-1967">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-1968">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-1968">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1970">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-1970">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-1971">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-1971">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1972">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-1972">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1973">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-1973">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-1974">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-1974">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-1975">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-1975">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1976">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1976">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-1977">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1977">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-1978">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-1978">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-1979">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1979">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-1980">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-1980">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-1981">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1981">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-1982">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-1982">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-1983">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-1983">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-1984">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1984">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1985">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-1985">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-1986">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-1986">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1988">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-1988">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1989">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1989">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-1990">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-1990">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-1991">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1991">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-1992">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-1992">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-1993">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-1993">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-1994">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-1994">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-1996">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1996">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-1997">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1997">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-1998">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-1998">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-1999">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-1999">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2001">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2001">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="0fc30-2002">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FCS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2002">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="0fc30-2003">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-2003">Target</span></span> | <span data-ttu-id="0fc30-2004">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2004">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-2005">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2005">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-2006">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-2006">32</span></span> |
| <span data-ttu-id="0fc30-2007">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2007">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2009">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-2009">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2011">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2011">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2013">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2013">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2014">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2014">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2015">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2015">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2017">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2017">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2019">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2019">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2021">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-2021">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2023">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-2023">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2025">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2025">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2027">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2027">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2028">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2028">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2029">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-2029">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-2030">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-2030">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-2031">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-2031">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2033">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-2033">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2035">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-2035">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2037">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-2037">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2039">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-2039">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-2040">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-2040">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-2041">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2041">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2042">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2042">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2043">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2043">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-2044">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-2044">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-2045">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2045">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-2046">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-2046">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-2047">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2047">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-2048">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-2048">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-2049">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2049">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-2050">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2050">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2051">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2051">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2052">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2052">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2054">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-2054">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2056">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2056">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2058">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-2058">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2060">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2060">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2062">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2062">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2064">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-2064">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2066">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-2066">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2068">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2068">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-2069">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2069">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2071">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2071">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2073">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-2073">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2075">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2075">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="0fc30-2076">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRGB<sup>FCS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2076">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="0fc30-2077">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-2077">Target</span></span> | <span data-ttu-id="0fc30-2078">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2078">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-2079">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2079">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-2080">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-2080">32</span></span> |
| <span data-ttu-id="0fc30-2081">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2081">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2083">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-2083">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2084">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2085">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2086">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2087">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2089">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2089">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2091">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2091">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2093">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-2093">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2095">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-2095">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2097">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2097">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2099">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2099">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2100">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2100">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2101">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-2101">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-2102">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-2102">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-2103">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-2103">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2105">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-2105">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2107">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-2107">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2109">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-2109">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2111">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-2111">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-2112">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-2112">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-2113">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2113">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2114">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2114">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2115">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2115">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-2116">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-2116">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-2117">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2117">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-2118">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-2118">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-2119">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2119">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-2120">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-2120">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-2121">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2121">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-2122">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2122">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2123">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2123">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2124">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2124">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2126">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-2126">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2128">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2128">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2130">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-2130">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2132">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2132">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2134">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2134">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2136">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-2136">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2138">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-2138">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2140">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2140">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-2141">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2141">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2143">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2143">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2145">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-2145">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2147">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="0fc30-2148">DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FCS</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2148">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="0fc30-2149">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-2149">Target</span></span> | <span data-ttu-id="0fc30-2150">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2150">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-2151">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-2152">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-2152">32</span></span> |
| <span data-ttu-id="0fc30-2153">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2153">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2155">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-2155">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2157">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2157">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2159">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2159">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2160">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2160">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2161">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2161">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2163">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2163">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2165">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2165">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2167">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-2167">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2169">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-2169">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2171">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2171">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2172">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2172">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2173">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2173">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2174">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-2174">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-2175">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-2175">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-2176">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-2176">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2178">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-2178">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-2179">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-2179">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2181">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-2181">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-2182">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-2182">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2184">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-2184">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-2185">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2185">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2186">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2186">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2187">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2187">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-2188">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-2188">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-2189">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2189">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-2190">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-2190">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-2191">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2191">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-2192">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-2192">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-2193">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2193">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-2194">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2194">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2195">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2195">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2196">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2196">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2198">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-2198">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2200">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2200">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2202">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-2202">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2204">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2204">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-2205">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2205">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2207">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-2207">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-2208">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-2208">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2210">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2210">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-2211">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2211">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-2212">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2212">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-2213">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-2213">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2215">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2215">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="0fc30-2216">DXGI_FORMAT_R8G8B8A8 \_ SNORM<sup>FCS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2216">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="0fc30-2217">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-2217">Target</span></span> | <span data-ttu-id="0fc30-2218">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2218">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-2219">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2219">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-2220">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-2220">32</span></span> |
| <span data-ttu-id="0fc30-2221">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2221">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2223">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-2223">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2225">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2225">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2227">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2227">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2228">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2228">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2229">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2229">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2231">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2231">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2233">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2233">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2235">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-2235">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2237">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-2237">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2239">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2239">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2241">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2241">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2242">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2242">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2243">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-2243">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-2244">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-2244">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-2245">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-2245">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2247">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-2247">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2249">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-2249">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2251">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-2251">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-2252">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-2252">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-2253">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-2253">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-2254">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2254">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2255">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2255">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2256">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2256">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-2257">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-2257">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-2258">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2258">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-2259">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-2259">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-2260">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2260">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-2261">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-2261">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-2262">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2262">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-2263">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2263">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2264">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2264">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2265">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2265">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2267">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-2267">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2269">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2269">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2271">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-2271">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2273">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2273">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2275">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2275">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2277">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-2277">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-2278">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-2278">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2280">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2280">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-2281">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2281">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-2282">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2282">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-2283">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-2283">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2285">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2285">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="0fc30-2286">DXGI_FORMAT_R8G8B8A8 \_ San<sup>FCS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2286">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="0fc30-2287">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-2287">Target</span></span> | <span data-ttu-id="0fc30-2288">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2288">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-2289">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2289">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-2290">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-2290">32</span></span> |
| <span data-ttu-id="0fc30-2291">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2291">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2293">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-2293">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2295">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2295">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2297">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2297">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2298">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2298">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2299">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2299">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2301">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2301">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2303">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2303">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2305">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-2305">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2307">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-2307">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2309">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2309">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2310">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2310">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2311">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2311">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2312">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-2312">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-2313">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-2313">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-2314">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-2314">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2316">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-2316">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-2317">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-2317">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2319">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-2319">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-2320">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-2320">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-2321">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-2321">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-2322">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2322">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2323">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2323">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2324">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2324">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-2325">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-2325">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-2326">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2326">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-2327">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-2327">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-2328">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2328">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-2329">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-2329">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-2330">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2330">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-2331">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2331">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2332">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2332">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2333">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2333">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2335">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-2335">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2337">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2337">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2339">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-2339">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2341">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2341">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-2342">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2342">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2344">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-2344">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-2345">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-2345">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2347">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2347">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-2348">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2348">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-2349">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2349">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-2350">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-2350">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2352">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2352">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="0fc30-2353">DXGI_FORMAT_R16G16 de \_ <sup>equipos</sup> sin tipo (33)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2353">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="0fc30-2354">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-2354">Target</span></span> | <span data-ttu-id="0fc30-2355">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2355">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-2356">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2356">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-2357">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-2357">32</span></span> |
| <span data-ttu-id="0fc30-2358">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2358">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2360">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-2360">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2361">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2361">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2362">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2362">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2363">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2363">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2364">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2364">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2366">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2366">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2368">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2368">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2370">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-2370">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2372">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-2372">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-2373">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2373">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2374">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2374">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2375">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2375">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2376">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-2376">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-2377">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-2377">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-2378">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-2378">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2380">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-2380">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-2381">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-2381">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-2382">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-2382">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-2383">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-2383">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-2384">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-2384">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-2385">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2385">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2386">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2386">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2387">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2387">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-2388">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-2388">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-2389">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2389">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-2390">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-2390">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-2391">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2391">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-2392">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-2392">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-2393">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2393">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-2394">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2394">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2395">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2395">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2396">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2396">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2398">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-2398">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-2399">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2399">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-2400">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-2400">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-2401">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2401">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-2402">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2402">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-2403">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-2403">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-2404">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-2404">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2406">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2406">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-2407">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2407">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-2408">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2408">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-2409">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-2409">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-2410">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2410">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="0fc30-2411">DXGI_FORMAT_R16G16 \_ float<sup>FCS</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2411">DXGI_FORMAT_R16G16\_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="0fc30-2412">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-2412">Target</span></span> | <span data-ttu-id="0fc30-2413">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2413">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-2414">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2414">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-2415">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-2415">32</span></span> |
| <span data-ttu-id="0fc30-2416">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2416">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2418">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-2418">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2420">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2420">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2422">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2422">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2423">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2423">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2424">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2424">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2426">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2426">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2428">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2428">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2430">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-2430">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2432">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-2432">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2434">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2434">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2436">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2436">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2437">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2437">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2438">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-2438">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-2439">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-2439">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-2440">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-2440">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2442">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-2442">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2444">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-2444">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2446">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-2446">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2448">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-2448">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-2449">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-2449">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-2450">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2450">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2451">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2451">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2452">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2452">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-2453">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-2453">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-2454">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2454">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-2455">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-2455">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-2456">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2456">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-2457">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-2457">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-2458">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2458">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-2459">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2459">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2460">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2460">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2461">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2461">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2463">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-2463">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2465">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2465">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2467">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-2467">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2469">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2469">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2471">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2471">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2473">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-2473">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-2474">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-2474">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2476">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2476">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-2477">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2477">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-2478">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2478">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-2479">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-2479">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-2480">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2480">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="0fc30-2481">DXGI_FORMAT_R16G16 \_ UNORM<sup>FCS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2481">DXGI_FORMAT_R16G16\_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="0fc30-2482">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-2482">Target</span></span> | <span data-ttu-id="0fc30-2483">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2483">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-2484">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2484">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-2485">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-2485">32</span></span> |
| <span data-ttu-id="0fc30-2486">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2486">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2488">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-2488">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2490">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2490">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2492">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2492">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2493">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2493">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2494">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2494">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2496">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2496">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2498">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2498">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2500">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-2500">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2502">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-2502">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2504">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2504">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2506">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2507">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2508">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-2508">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-2509">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-2509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-2510">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-2510">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2512">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-2512">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2514">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-2514">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2516">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-2516">Blendable RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2518">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-2518">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-2519">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-2519">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-2520">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2520">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2521">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2521">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2522">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2522">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-2523">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-2523">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-2524">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2524">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-2525">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-2525">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-2526">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2526">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-2527">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-2527">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-2528">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2528">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-2529">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2529">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2530">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2530">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2531">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2531">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2533">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-2533">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2535">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2535">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2537">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-2537">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2539">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2539">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2541">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2541">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2543">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-2543">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-2544">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-2544">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2546">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2546">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-2547">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2547">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-2548">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2548">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-2549">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-2549">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-2550">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2550">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="0fc30-2551">DXGI_FORMAT_R16G16 \_ uint<sup>FCS</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2551">DXGI_FORMAT_R16G16\_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="0fc30-2552">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-2552">Target</span></span> | <span data-ttu-id="0fc30-2553">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2553">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-2554">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2554">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-2555">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-2555">32</span></span> |
| <span data-ttu-id="0fc30-2556">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2556">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2558">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-2558">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2560">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2560">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2562">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2562">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2563">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2563">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2564">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2564">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2566">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2566">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2568">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2568">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2570">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-2570">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2572">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-2572">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2574">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2574">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2575">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2575">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2576">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2576">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2577">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-2577">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-2578">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-2578">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-2579">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-2579">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2581">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-2581">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-2582">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-2582">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2584">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-2584">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-2585">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-2585">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2587">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-2587">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-2588">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2588">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2589">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2589">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2590">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2590">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-2591">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-2591">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-2592">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2592">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-2593">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-2593">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-2594">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2594">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-2595">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-2595">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-2596">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2596">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-2597">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2597">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2598">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2598">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2599">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2599">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2601">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-2601">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2603">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2603">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2605">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-2605">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2607">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2607">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-2608">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2608">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2610">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-2610">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-2611">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-2611">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2613">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2613">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-2614">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2614">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-2615">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2615">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-2616">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-2616">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-2617">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2617">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="0fc30-2618">DXGI_FORMAT_R16G16 \_ SNORM<sup>FCS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2618">DXGI_FORMAT_R16G16\_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="0fc30-2619">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-2619">Target</span></span> | <span data-ttu-id="0fc30-2620">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2620">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-2621">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2621">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-2622">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-2622">32</span></span> |
| <span data-ttu-id="0fc30-2623">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2623">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2625">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-2625">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2627">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2627">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2629">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2629">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2630">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2630">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2631">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2631">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2633">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2633">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2635">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2635">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2637">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-2637">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2639">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-2639">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2641">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2641">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2643">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2643">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2644">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2644">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2645">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-2645">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-2646">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-2646">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-2647">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-2647">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2649">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-2649">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2651">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-2651">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2653">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-2653">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-2654">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-2654">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-2655">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-2655">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-2656">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2656">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2657">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2657">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2658">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2658">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-2659">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-2659">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-2660">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2660">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-2661">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-2661">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-2662">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2662">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-2663">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-2663">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-2664">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2664">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-2665">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2665">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2666">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2666">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2667">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2667">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2669">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-2669">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2671">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2671">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2673">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-2673">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2675">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2675">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2677">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2677">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2679">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-2679">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-2680">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-2680">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2682">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2682">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-2683">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2683">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-2684">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2684">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-2685">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-2685">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-2686">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2686">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="0fc30-2687">DXGI_FORMAT_R16G16 \_ San<sup>FCS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2687">DXGI_FORMAT_R16G16\_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="0fc30-2688">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-2688">Target</span></span> | <span data-ttu-id="0fc30-2689">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2689">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-2690">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2690">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-2691">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-2691">32</span></span> |
| <span data-ttu-id="0fc30-2692">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2692">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2694">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-2694">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2696">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2696">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2698">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2698">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2699">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2699">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2700">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2700">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2702">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2702">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2704">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2704">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2706">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-2706">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2708">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-2708">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2710">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2710">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2711">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2711">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2712">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2712">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2713">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-2713">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-2714">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-2714">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-2715">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-2715">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2717">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-2717">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-2718">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-2718">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2720">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-2720">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-2721">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-2721">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-2722">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-2722">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-2723">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2723">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2724">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2724">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2725">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2725">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-2726">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-2726">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-2727">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2727">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-2728">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-2728">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-2729">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2729">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-2730">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-2730">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-2731">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2731">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-2732">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2732">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2733">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2733">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2734">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2734">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2736">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-2736">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2738">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2738">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2740">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-2740">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2742">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-2743">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2743">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2745">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-2745">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-2746">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-2746">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2748">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2748">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-2749">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2749">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-2750">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2750">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-2751">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-2751">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-2752">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2752">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="0fc30-2753">DXGI_FORMAT_R32 de \_ <sup>equipos</sup> sin tipo (39)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2753">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="0fc30-2754">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-2754">Target</span></span> | <span data-ttu-id="0fc30-2755">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2755">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-2756">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2756">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-2757">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-2757">32</span></span> |
| <span data-ttu-id="0fc30-2758">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2758">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2760">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-2760">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2761">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2761">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2762">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2762">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2763">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2763">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2764">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2764">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2766">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2766">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2768">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2768">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2770">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-2770">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2772">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-2772">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-2773">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2773">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2774">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2774">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2775">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2775">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2776">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-2776">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-2777">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-2777">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-2778">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-2778">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2780">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-2780">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-2781">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-2781">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-2782">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-2782">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-2783">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-2783">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-2784">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-2784">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-2785">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2785">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2786">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2786">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2787">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2787">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-2788">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-2788">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-2789">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2789">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-2790">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-2790">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-2791">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2791">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-2792">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-2792">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-2793">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2793">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-2794">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2794">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2795">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2795">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2796">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2796">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2798">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-2798">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-2799">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2799">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-2800">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-2800">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-2801">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2801">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-2802">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2802">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-2803">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-2803">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-2804">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-2804">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2806">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2806">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-2807">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2807">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-2808">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2808">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-2809">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-2809">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2811">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="0fc30-2812">DXGI_FORMAT_D32 \_ float<sup>FCS</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2812">DXGI_FORMAT_D32\_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="0fc30-2813">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-2813">Target</span></span> | <span data-ttu-id="0fc30-2814">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2814">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-2815">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-2816">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-2816">32</span></span> |
| <span data-ttu-id="0fc30-2817">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2817">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2819">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-2819">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2820">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2821">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2822">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2823">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2825">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2825">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2827">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2827">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-2828">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-2828">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2830">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-2830">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-2831">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2831">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2832">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2832">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2833">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2833">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2834">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-2834">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-2835">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-2835">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-2836">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-2836">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2838">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-2838">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-2839">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-2839">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-2840">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-2840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-2841">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-2841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-2842">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-2842">Depth/Stencil Target</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2844">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2844">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2845">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2845">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2846">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2846">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-2847">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-2847">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-2848">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2848">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-2849">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-2849">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-2850">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2850">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-2851">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-2851">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-2852">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2852">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-2853">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2853">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2854">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2854">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2855">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2855">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2857">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-2857">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2859">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2859">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2861">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-2861">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2863">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2863">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-2864">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2864">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-2865">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-2865">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-2866">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-2866">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2868">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2868">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-2869">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2869">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-2870">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2870">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-2871">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-2871">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2873">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2873">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="0fc30-2874">DXGI_FORMAT_R32 \_ float<sup>FCS</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2874">DXGI_FORMAT_R32\_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="0fc30-2875">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-2875">Target</span></span> | <span data-ttu-id="0fc30-2876">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2876">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-2877">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2877">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-2878">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-2878">32</span></span> |
| <span data-ttu-id="0fc30-2879">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2879">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2881">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-2881">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2883">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2883">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2885">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2885">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-2886">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2886">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2888">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2888">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2890">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2890">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2892">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2892">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2894">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-2894">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2896">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-2896">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2898">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2898">Shader sample (any filter)</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2900">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2900">Shader sample\_c (comparison filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2902">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2902">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2903">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-2903">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-2904">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-2904">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-2905">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-2905">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2907">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-2907">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2909">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-2909">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2911">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-2911">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2913">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-2913">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-2914">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-2914">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-2915">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2915">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2916">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2916">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2917">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2917">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-2918">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-2918">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-2919">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2919">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-2920">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-2920">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-2921">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2921">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-2922">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-2922">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-2923">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2923">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-2924">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2924">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2925">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2925">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2926">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2926">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2928">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-2928">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2930">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2930">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2932">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-2932">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2934">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2934">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2936">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-2936">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2938">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-2938">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-2939">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-2939">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2941">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2941">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-2942">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2942">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-2943">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2943">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-2944">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-2944">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2946">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="0fc30-2947">DXGI_FORMAT_R32 \_ uint<sup>FCS</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2947">DXGI_FORMAT_R32\_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="0fc30-2948">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-2948">Target</span></span> | <span data-ttu-id="0fc30-2949">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-2949">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-2950">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-2951">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-2951">32</span></span> |
| <span data-ttu-id="0fc30-2952">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2952">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2954">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-2954">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2956">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2956">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2958">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2958">Input Assembler Index Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2960">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2960">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2962">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2962">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2964">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2964">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2966">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-2966">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2968">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-2968">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2970">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-2970">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2972">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2972">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2973">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2973">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2974">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-2974">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-2975">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-2975">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-2976">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-2976">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-2977">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-2977">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2979">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-2979">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-2980">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-2980">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2982">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-2982">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-2983">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-2983">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-2985">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-2985">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-2986">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-2986">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2987">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2987">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-2988">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-2988">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-2989">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-2989">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-2990">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2990">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-2991">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-2991">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-2992">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2992">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-2993">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-2993">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-2994">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-2994">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-2995">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2995">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2996">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-2996">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-2997">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-2997">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-2999">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-2999">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3001">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3001">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3003">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-3003">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3005">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3005">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-3006">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3006">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3008">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-3008">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-3009">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-3009">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3011">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3011">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-3012">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3012">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-3013">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3013">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-3014">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-3014">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3016">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3016">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="0fc30-3017">DXGI_FORMAT_R32 \_ San<sup>FCS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3017">DXGI_FORMAT_R32\_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="0fc30-3018">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-3018">Target</span></span> | <span data-ttu-id="0fc30-3019">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3019">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-3020">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3020">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-3021">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-3021">32</span></span> |
| <span data-ttu-id="0fc30-3022">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3022">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3024">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-3024">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3026">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3026">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3028">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3028">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3029">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3029">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3031">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3031">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3033">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3033">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3035">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3035">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3037">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-3037">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3039">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-3039">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3041">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3041">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3042">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3042">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3043">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3043">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3044">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-3044">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-3045">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-3045">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-3046">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-3046">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3048">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-3048">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-3049">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-3049">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3051">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-3051">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3052">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-3052">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-3053">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-3053">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-3054">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3054">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3055">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3055">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3056">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3056">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-3057">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-3057">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-3058">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3058">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-3059">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-3059">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-3060">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3060">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-3061">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-3061">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-3062">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3062">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-3063">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3063">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3064">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3064">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3065">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3065">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3067">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-3067">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3069">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3069">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3071">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-3071">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3073">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3073">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-3074">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3074">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3076">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-3076">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-3077">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-3077">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3079">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3079">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-3080">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3080">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-3081">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3081">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-3082">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-3082">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3084">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3084">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="0fc30-3085">DXGI_FORMAT_R24G8 de \_ <sup>equipos</sup> sin tipo (44)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3085">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="0fc30-3086">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-3086">Target</span></span> | <span data-ttu-id="0fc30-3087">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3087">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-3088">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3088">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-3089">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-3089">32</span></span> |
| <span data-ttu-id="0fc30-3090">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3090">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3092">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-3092">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3093">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3093">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3094">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3094">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3095">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3095">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3096">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3096">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3098">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3098">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3100">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3100">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-3101">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-3101">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3103">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-3103">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-3104">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3104">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3105">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3105">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3106">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3106">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3107">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-3107">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-3108">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-3108">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-3109">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-3109">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3111">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-3111">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-3112">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-3112">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3113">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-3113">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3114">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-3114">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-3115">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-3115">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-3116">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3116">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3117">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3117">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3118">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3118">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-3119">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-3119">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-3120">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3120">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-3121">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-3121">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-3122">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3122">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-3123">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-3123">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-3124">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3124">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-3125">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3125">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3126">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3126">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3127">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3127">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3129">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-3129">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3130">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3130">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3131">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-3131">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-3132">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3132">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-3133">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3133">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-3134">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-3134">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-3135">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-3135">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3137">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3137">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-3138">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3138">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-3139">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3139">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-3140">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-3140">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-3141">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3141">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfcssup-45"></a><span data-ttu-id="0fc30-3142">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FCS</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3142">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FCS</sup> (45)</span></span>
| <span data-ttu-id="0fc30-3143">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-3143">Target</span></span> | <span data-ttu-id="0fc30-3144">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3144">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-3145">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3145">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-3146">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-3146">32</span></span> |
| <span data-ttu-id="0fc30-3147">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3147">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3149">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-3149">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3150">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3150">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3151">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3151">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3152">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3152">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3153">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3153">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3155">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3155">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3157">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3157">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-3158">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-3158">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3160">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-3160">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-3161">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3161">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3162">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3162">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3163">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3163">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3164">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-3164">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-3165">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-3165">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-3166">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-3166">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3168">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-3168">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-3169">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-3169">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3170">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-3170">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3171">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-3171">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-3172">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-3172">Depth/Stencil Target</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3174">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3174">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3175">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3175">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3176">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3176">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-3177">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-3177">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-3178">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3178">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-3179">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-3179">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-3180">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3180">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-3181">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-3181">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-3182">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3182">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-3183">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3183">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3184">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3184">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3185">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3185">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3187">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-3187">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3189">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3189">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3191">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-3191">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3193">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3193">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-3194">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3194">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-3195">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-3195">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-3196">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-3196">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3198">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3198">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-3199">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3199">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-3200">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3200">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-3201">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-3201">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-3202">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3202">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfcssup-46"></a><span data-ttu-id="0fc30-3203">DXGI_FORMAT_R24 \_ UNORM \_ X8 \_ sin tipo de<sup>FCS</sup> (46)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3203">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FCS</sup> (46)</span></span>
| <span data-ttu-id="0fc30-3204">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-3204">Target</span></span> | <span data-ttu-id="0fc30-3205">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3205">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-3206">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3206">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-3207">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-3207">32</span></span> |
| <span data-ttu-id="0fc30-3208">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3208">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3210">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-3210">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3211">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3211">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3212">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3212">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3213">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3213">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3214">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3214">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3216">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3216">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3218">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3218">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-3219">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-3219">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3221">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-3221">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3223">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3223">Shader sample (any filter)</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3225">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3225">Shader sample\_c (comparison filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3227">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3227">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3228">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-3228">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-3229">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-3229">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-3230">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-3230">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3232">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-3232">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-3233">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-3233">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3234">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-3234">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3235">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-3235">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-3236">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-3236">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-3237">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3237">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3238">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3238">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3239">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3239">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-3240">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-3240">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-3241">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3241">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-3242">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-3242">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-3243">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3243">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-3244">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-3244">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-3245">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3245">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-3246">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3246">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3247">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3247">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3248">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3248">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3250">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-3250">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3251">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3251">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3252">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-3252">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-3253">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3253">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-3254">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3254">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-3255">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-3255">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-3256">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-3256">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3258">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3258">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-3259">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3259">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-3260">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3260">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-3261">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-3261">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-3262">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3262">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfcssup-47"></a><span data-ttu-id="0fc30-3263">DXGI_FORMAT_X24 de \_ G8 no typeless \_ \_ (47)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="0fc30-3263">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FCS</sup> (47)</span></span>
| <span data-ttu-id="0fc30-3264">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-3264">Target</span></span> | <span data-ttu-id="0fc30-3265">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3265">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-3266">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3266">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-3267">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-3267">32</span></span> |
| <span data-ttu-id="0fc30-3268">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3268">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3270">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-3270">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3271">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3271">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3272">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3272">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3273">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3273">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3274">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3274">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3276">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3276">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3278">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3278">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-3279">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-3279">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3281">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-3281">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3283">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3283">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3284">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3284">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3285">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3285">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3286">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-3286">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-3287">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-3287">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-3288">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-3288">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3290">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-3290">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-3291">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-3291">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3292">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-3292">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3293">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-3293">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-3294">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-3294">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-3295">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3295">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3296">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3296">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3297">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3297">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-3298">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-3298">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-3299">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3299">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-3300">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-3300">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-3301">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3301">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-3302">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-3302">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-3303">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3303">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-3304">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3304">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3305">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3305">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3306">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3306">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3308">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-3308">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3309">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3309">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3310">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-3310">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-3311">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3311">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-3312">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3312">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-3313">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-3313">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-3314">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-3314">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3316">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3316">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-3317">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3317">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-3318">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3318">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-3319">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-3319">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-3320">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3320">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="0fc30-3321">DXGI_FORMAT_R8G8 de \_ <sup>equipos</sup> sin tipo (48)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3321">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="0fc30-3322">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-3322">Target</span></span> | <span data-ttu-id="0fc30-3323">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3323">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-3324">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3324">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-3325">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-3325">16</span></span> |
| <span data-ttu-id="0fc30-3326">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3326">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3328">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-3328">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3329">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3329">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3330">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3330">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3331">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3331">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3332">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3332">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3334">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3336">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3336">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3338">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-3338">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3340">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-3340">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-3341">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3341">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3342">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3342">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3343">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3343">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3344">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-3344">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-3345">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-3345">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-3346">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-3346">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3348">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-3348">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-3349">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-3349">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3350">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-3350">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3351">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-3351">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-3352">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-3352">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-3353">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3353">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3354">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3354">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3355">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3355">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-3356">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-3356">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-3357">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3357">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-3358">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-3358">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-3359">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3359">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-3360">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-3360">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-3361">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3361">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-3362">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3362">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3363">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3363">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3364">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3364">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3366">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-3366">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3367">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3367">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3368">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-3368">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-3369">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-3370">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3370">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-3371">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-3371">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-3372">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-3372">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3374">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-3375">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-3376">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-3377">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-3377">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-3378">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="0fc30-3379">DXGI_FORMAT_R8G8 \_ UNORM<sup>FCS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3379">DXGI_FORMAT_R8G8\_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="0fc30-3380">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-3380">Target</span></span> | <span data-ttu-id="0fc30-3381">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3381">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-3382">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-3383">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-3383">16</span></span> |
| <span data-ttu-id="0fc30-3384">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3384">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3386">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-3386">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3388">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3388">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3390">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3390">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3391">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3391">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3392">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3392">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3394">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3394">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3396">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3396">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3398">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-3398">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3400">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-3400">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3402">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3402">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3404">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3404">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3405">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3405">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3406">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-3406">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-3407">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-3407">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-3408">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-3408">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3410">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-3410">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3412">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-3412">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3414">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-3414">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3416">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-3416">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-3417">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-3417">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-3418">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3418">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3419">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3419">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3420">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3420">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-3421">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-3421">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-3422">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3422">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-3423">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-3423">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-3424">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3424">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-3425">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-3425">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-3426">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3426">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-3427">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3427">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3428">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3428">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3429">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3429">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3431">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-3431">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3433">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3433">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3435">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-3435">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3437">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3437">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3439">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3439">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3441">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-3441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-3442">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-3442">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3444">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3444">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-3445">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3445">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-3446">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3446">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-3447">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-3447">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3449">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3449">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="0fc30-3450">DXGI_FORMAT_R8G8 \_ uint<sup>FCS</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3450">DXGI_FORMAT_R8G8\_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="0fc30-3451">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-3451">Target</span></span> | <span data-ttu-id="0fc30-3452">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3452">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-3453">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3453">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-3454">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-3454">16</span></span> |
| <span data-ttu-id="0fc30-3455">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3455">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3457">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-3457">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3459">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3459">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3461">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3461">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3462">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3462">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3463">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3463">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3465">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3465">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3467">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3467">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3469">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-3469">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3471">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-3471">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3473">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3473">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3474">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3474">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3475">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3475">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3476">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-3476">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-3477">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-3477">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-3478">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-3478">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3480">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-3480">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-3481">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-3481">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3483">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-3483">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3484">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-3484">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3486">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-3486">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-3487">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3487">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3488">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3488">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3489">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3489">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-3490">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-3490">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-3491">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3491">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-3492">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-3492">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-3493">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3493">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-3494">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-3494">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-3495">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3495">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-3496">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3496">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3497">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3497">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3498">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3498">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3500">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-3500">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3502">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3502">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3504">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-3504">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3506">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3506">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-3507">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3507">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3509">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-3509">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-3510">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-3510">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3512">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3512">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-3513">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3513">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-3514">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3514">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-3515">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-3515">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-3516">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3516">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="0fc30-3517">DXGI_FORMAT_R8G8 \_ SNORM<sup>FCS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3517">DXGI_FORMAT_R8G8\_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="0fc30-3518">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-3518">Target</span></span> | <span data-ttu-id="0fc30-3519">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3519">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-3520">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3520">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-3521">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-3521">16</span></span> |
| <span data-ttu-id="0fc30-3522">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3522">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3524">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-3524">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3526">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3526">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3528">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3528">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3529">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3529">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3530">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3530">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3532">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3532">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3534">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3534">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3536">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-3536">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3538">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-3538">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3540">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3540">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3542">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3542">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3543">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3543">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3544">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-3544">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-3545">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-3545">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-3546">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-3546">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3548">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-3548">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3550">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-3550">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3552">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-3552">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3553">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-3553">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-3554">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-3554">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-3555">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3555">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3556">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3556">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3557">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3557">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-3558">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-3558">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-3559">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3559">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-3560">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-3560">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-3561">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3561">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-3562">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-3562">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-3563">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3563">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-3564">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3564">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3565">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3565">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3566">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3566">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3568">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-3568">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3570">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3570">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3572">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-3572">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3574">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3574">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3576">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3576">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3578">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-3578">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-3579">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-3579">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3581">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3581">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-3582">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3582">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-3583">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3583">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-3584">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-3584">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-3585">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3585">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="0fc30-3586">DXGI_FORMAT_R8G8 \_ San<sup>FCS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3586">DXGI_FORMAT_R8G8\_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="0fc30-3587">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-3587">Target</span></span> | <span data-ttu-id="0fc30-3588">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3588">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-3589">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3589">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-3590">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-3590">16</span></span> |
| <span data-ttu-id="0fc30-3591">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3591">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3593">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-3593">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3595">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3595">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3597">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3597">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3598">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3598">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3599">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3599">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3601">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3601">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3603">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3603">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-3605">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3607">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-3607">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3609">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3609">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3610">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3610">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3611">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3611">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3612">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-3612">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-3613">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-3613">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-3614">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-3614">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3616">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-3616">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-3617">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-3617">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3619">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-3619">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3620">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-3620">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-3621">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-3621">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-3622">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3622">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3623">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3623">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3624">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3624">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-3625">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-3625">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-3626">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3626">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-3627">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-3627">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-3628">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3628">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-3629">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-3629">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-3630">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3630">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-3631">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3631">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3632">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3632">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3633">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3633">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3635">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-3635">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3637">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3637">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3639">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-3639">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3641">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3641">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-3642">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3642">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3644">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-3644">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-3645">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-3645">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3647">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3647">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-3648">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3648">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-3649">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3649">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-3650">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-3650">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-3651">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3651">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="0fc30-3652">DXGI_FORMAT_R16 de \_ <sup>equipos</sup> sin tipo (53)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3652">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="0fc30-3653">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-3653">Target</span></span> | <span data-ttu-id="0fc30-3654">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3654">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-3655">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3655">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-3656">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-3656">16</span></span> |
| <span data-ttu-id="0fc30-3657">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3657">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3659">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-3659">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3660">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3660">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3661">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3661">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3662">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3662">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3663">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3663">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3665">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3665">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3667">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3667">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3669">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-3669">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3671">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-3671">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-3672">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3672">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3673">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3673">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3674">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3674">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3675">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-3675">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-3676">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-3676">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-3677">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-3677">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3679">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-3679">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-3680">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-3680">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3681">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-3681">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3682">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-3682">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-3683">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-3683">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-3684">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3684">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3685">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3685">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3686">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3686">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-3687">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-3687">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-3688">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3688">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-3689">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-3689">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-3690">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3690">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-3691">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-3691">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-3692">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3692">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-3693">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3693">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3694">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3694">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3695">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3695">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3697">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-3697">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3698">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3698">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3699">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-3699">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-3700">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3700">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-3701">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3701">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-3702">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-3702">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-3703">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-3703">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3705">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3705">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-3706">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3706">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-3707">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3707">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-3708">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-3708">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3710">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3710">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="0fc30-3711">DXGI_FORMAT_R16 \_ float<sup>FCS</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3711">DXGI_FORMAT_R16\_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="0fc30-3712">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-3712">Target</span></span> | <span data-ttu-id="0fc30-3713">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3713">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-3714">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3714">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-3715">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-3715">16</span></span> |
| <span data-ttu-id="0fc30-3716">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3716">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3718">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-3718">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3720">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3720">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3722">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3722">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3723">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3723">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3724">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3724">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3726">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3728">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3730">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-3730">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3732">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-3732">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3734">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3734">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3736">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3736">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3737">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3737">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3738">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-3738">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-3739">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-3739">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-3740">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-3740">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3742">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-3742">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3744">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-3744">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3746">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-3746">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3748">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-3748">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-3749">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-3749">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-3750">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3750">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3751">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3751">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3752">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3752">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-3753">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-3753">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-3754">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3754">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-3755">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-3755">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-3756">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3756">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-3757">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-3757">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-3758">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3758">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-3759">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3759">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3760">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3760">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3761">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3761">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3763">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-3763">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3765">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3765">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3767">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-3767">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3769">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3769">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3771">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3771">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3773">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-3773">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-3774">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-3774">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3776">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3776">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-3777">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3777">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-3778">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3778">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-3779">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-3779">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3781">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3781">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="0fc30-3782">DXGI_FORMAT_D16 \_ UNORM<sup>FCS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3782">DXGI_FORMAT_D16\_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="0fc30-3783">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-3783">Target</span></span> | <span data-ttu-id="0fc30-3784">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3784">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-3785">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3785">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-3786">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-3786">16</span></span> |
| <span data-ttu-id="0fc30-3787">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3787">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3789">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-3789">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3790">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3790">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3791">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3791">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3792">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3792">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3793">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3793">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3795">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3795">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3797">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-3798">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-3798">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3800">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-3800">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-3801">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3801">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3802">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3802">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3803">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3803">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3804">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-3804">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-3805">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-3805">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-3806">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-3806">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3808">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-3808">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-3809">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-3809">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3810">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-3810">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3811">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-3811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-3812">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-3812">Depth/Stencil Target</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3814">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3814">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3815">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3815">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3816">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3816">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-3817">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-3817">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-3818">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3818">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-3819">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-3819">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-3820">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3820">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-3821">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-3821">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-3822">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3822">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-3823">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3823">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3824">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3824">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3825">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3825">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3827">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-3827">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3829">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3829">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3831">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-3831">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3833">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3833">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-3834">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3834">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-3835">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-3835">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-3836">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-3836">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3838">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3838">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-3839">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3839">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-3840">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3840">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-3841">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-3841">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3843">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3843">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="0fc30-3844">DXGI_FORMAT_R16 \_ UNORM<sup>FCS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3844">DXGI_FORMAT_R16\_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="0fc30-3845">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-3845">Target</span></span> | <span data-ttu-id="0fc30-3846">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3846">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-3847">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3847">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-3848">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-3848">16</span></span> |
| <span data-ttu-id="0fc30-3849">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3849">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3851">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-3851">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3853">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3853">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3855">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3855">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3856">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3856">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3857">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3857">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3859">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3859">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3861">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3861">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3863">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-3863">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3865">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-3865">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3867">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3867">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3869">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3869">Shader sample\_c (comparison filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3871">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3871">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3872">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-3872">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-3873">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-3873">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-3874">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-3874">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3876">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-3876">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3878">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-3878">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3880">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-3880">Blendable RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3882">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-3882">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-3883">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-3883">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-3884">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3884">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3885">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3885">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3886">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3886">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-3887">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-3887">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-3888">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3888">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-3889">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-3889">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-3890">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3890">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-3891">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-3891">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-3892">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3892">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-3893">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3893">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3894">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3894">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3895">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3895">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3897">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-3897">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3899">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3899">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3901">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-3901">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3903">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3903">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3905">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3905">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3907">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-3907">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-3908">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-3908">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3910">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3910">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-3911">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3911">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-3912">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3912">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-3913">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-3913">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3915">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3915">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="0fc30-3916">DXGI_FORMAT_R16 \_ uint<sup>FCS</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3916">DXGI_FORMAT_R16\_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="0fc30-3917">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-3917">Target</span></span> | <span data-ttu-id="0fc30-3918">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3918">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-3919">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3919">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-3920">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-3920">16</span></span> |
| <span data-ttu-id="0fc30-3921">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3921">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3923">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-3923">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3925">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3925">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3927">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3927">Input Assembler Index Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3929">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3929">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3930">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3930">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3932">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3932">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3934">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3934">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3936">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-3936">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3938">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-3938">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3940">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3940">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3941">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3941">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3942">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3942">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-3943">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-3943">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-3944">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-3944">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-3945">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-3945">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3947">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-3947">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-3948">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-3948">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3950">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-3950">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-3951">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-3951">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3953">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-3953">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-3954">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3954">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3955">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3955">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-3956">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3956">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-3957">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-3957">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-3958">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3958">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-3959">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-3959">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-3960">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3960">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-3961">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-3961">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-3962">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-3962">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-3963">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3963">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3964">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-3964">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-3965">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3965">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3967">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-3967">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3969">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3969">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3971">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-3971">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3973">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3973">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-3974">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-3974">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-3976">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-3976">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-3977">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-3977">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3979">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3979">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-3980">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3980">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-3981">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3981">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-3982">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-3982">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3984">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3984">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="0fc30-3985">DXGI_FORMAT_R16 \_ SNORM<sup>FCS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3985">DXGI_FORMAT_R16\_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="0fc30-3986">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-3986">Target</span></span> | <span data-ttu-id="0fc30-3987">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-3987">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-3988">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-3988">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-3989">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-3989">16</span></span> |
| <span data-ttu-id="0fc30-3990">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-3990">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3992">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-3992">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3994">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3994">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-3996">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-3996">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3997">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-3997">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-3998">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-3998">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4000">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4000">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4002">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4002">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4004">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-4004">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4006">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-4006">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4008">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4008">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4010">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4010">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4011">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4011">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4012">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4012">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-4013">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-4013">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-4014">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-4014">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4016">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-4016">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4018">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-4018">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4020">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-4020">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4021">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-4021">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-4022">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-4022">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-4023">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4023">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4024">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4024">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4025">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4025">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-4026">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-4026">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-4027">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4027">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-4028">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-4028">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-4029">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4029">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-4030">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-4030">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-4031">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4031">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-4032">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4032">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4033">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4033">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4034">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4034">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4036">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-4036">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4038">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4038">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4040">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-4040">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4042">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4042">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4044">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4044">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4046">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-4046">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-4047">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-4047">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4049">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4049">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-4050">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4050">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-4051">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4051">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-4052">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-4052">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4054">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4054">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="0fc30-4055">DXGI_FORMAT_R16 \_ San<sup>FCS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4055">DXGI_FORMAT_R16\_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="0fc30-4056">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-4056">Target</span></span> | <span data-ttu-id="0fc30-4057">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4057">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-4058">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4058">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-4059">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-4059">16</span></span> |
| <span data-ttu-id="0fc30-4060">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4060">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4062">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-4062">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4064">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4064">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4066">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4066">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4067">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4067">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4068">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4068">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4070">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4070">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4072">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4072">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4074">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-4074">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4076">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-4076">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4078">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4078">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4079">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4079">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4080">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4080">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4081">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4081">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-4082">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-4082">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-4083">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-4083">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4085">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-4085">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-4086">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-4086">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4088">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-4088">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4089">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-4089">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-4090">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-4090">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-4091">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4091">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4092">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4092">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4093">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4093">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-4094">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-4094">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-4095">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4095">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-4096">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-4096">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-4097">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4097">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-4098">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-4098">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-4099">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4099">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-4100">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4100">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4101">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4101">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4102">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4102">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4104">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-4104">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4106">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4106">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4108">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-4108">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4110">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4110">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-4111">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4111">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4113">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-4113">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-4114">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-4114">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4116">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4116">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-4117">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4117">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-4118">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4118">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-4119">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-4119">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4121">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4121">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="0fc30-4122">DXGI_FORMAT_R8 de \_ <sup>equipos</sup> sin tipo (60)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4122">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="0fc30-4123">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-4123">Target</span></span> | <span data-ttu-id="0fc30-4124">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4124">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-4125">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4125">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-4126">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-4126">8</span></span> |
| <span data-ttu-id="0fc30-4127">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4127">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4129">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-4129">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4130">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4131">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4132">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4133">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4135">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4135">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4137">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4137">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4139">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-4139">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4141">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-4141">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-4142">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4142">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4143">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4143">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4144">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4144">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4145">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4145">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-4146">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-4146">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-4147">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-4147">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4149">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-4149">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-4150">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-4150">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4151">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-4151">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4152">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-4152">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-4153">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-4153">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-4154">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4154">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4155">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4155">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4156">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4156">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-4157">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-4157">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-4158">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4158">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-4159">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-4159">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-4160">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4160">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-4161">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-4161">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-4162">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4162">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-4163">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4163">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4164">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4164">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4165">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4165">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4167">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-4167">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4168">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4168">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4169">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-4169">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-4170">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4170">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-4171">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4171">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-4172">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-4172">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-4173">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-4173">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4175">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4175">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-4176">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4176">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-4177">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4177">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-4178">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-4178">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4180">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4180">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="0fc30-4181">DXGI_FORMAT_R8 \_ UNORM<sup>FCS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4181">DXGI_FORMAT_R8\_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="0fc30-4182">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-4182">Target</span></span> | <span data-ttu-id="0fc30-4183">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4183">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-4184">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4184">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-4185">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-4185">8</span></span> |
| <span data-ttu-id="0fc30-4186">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4186">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4188">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-4188">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4190">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4190">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4192">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4192">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4193">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4193">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4194">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4194">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4196">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4196">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4198">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4198">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4200">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-4200">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4202">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-4202">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4204">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4204">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4206">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4206">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4207">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4207">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4208">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4208">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-4209">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-4209">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-4210">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-4210">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4212">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-4212">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4214">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-4214">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4216">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-4216">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4218">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-4218">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-4219">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-4219">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-4220">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4220">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4221">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4221">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4222">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4222">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-4223">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-4223">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-4224">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4224">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-4225">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-4225">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-4226">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4226">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-4227">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-4227">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-4228">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4228">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-4229">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4229">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4230">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4230">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4231">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4231">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4233">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-4233">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4235">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4235">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4237">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-4237">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4239">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4239">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4241">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4241">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4243">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-4243">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-4244">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-4244">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4246">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4246">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-4247">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4247">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-4248">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4248">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-4249">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-4249">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4251">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4251">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="0fc30-4252">DXGI_FORMAT_R8 \_ uint<sup>FCS</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4252">DXGI_FORMAT_R8\_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="0fc30-4253">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-4253">Target</span></span> | <span data-ttu-id="0fc30-4254">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4254">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-4255">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4255">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-4256">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-4256">8</span></span> |
| <span data-ttu-id="0fc30-4257">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4257">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4259">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-4259">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4261">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4261">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4263">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4263">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4264">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4264">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4265">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4265">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4267">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4269">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4271">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-4271">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4273">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-4273">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4275">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4275">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4276">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4276">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4277">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4277">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4278">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4278">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-4279">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-4279">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-4280">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-4280">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4282">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-4282">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-4283">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-4283">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4285">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-4285">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4286">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-4286">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4288">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-4288">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-4289">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4289">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4290">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4290">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4291">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4291">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-4292">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-4292">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-4293">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4293">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-4294">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-4294">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-4295">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4295">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-4296">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-4296">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-4297">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4297">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-4298">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4298">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4299">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4299">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4300">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4300">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4302">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-4302">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4304">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4304">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4306">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-4306">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4308">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4308">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-4309">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4309">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4311">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-4311">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-4312">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-4312">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4314">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4314">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-4315">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4315">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-4316">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4316">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-4317">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-4317">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4319">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4319">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="0fc30-4320">DXGI_FORMAT_R8 \_ SNORM<sup>FCS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4320">DXGI_FORMAT_R8\_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="0fc30-4321">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-4321">Target</span></span> | <span data-ttu-id="0fc30-4322">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4322">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-4323">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4323">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-4324">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-4324">8</span></span> |
| <span data-ttu-id="0fc30-4325">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4325">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4327">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-4327">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4329">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4329">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4331">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4331">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4332">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4332">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4333">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4333">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4335">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4335">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4337">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4337">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4339">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-4339">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4341">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-4341">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4343">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4343">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4345">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4345">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4346">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4346">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4347">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4347">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-4348">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-4348">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-4349">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-4349">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4351">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-4351">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4353">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-4353">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4355">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-4355">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4356">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-4356">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-4357">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-4357">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-4358">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4358">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4359">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4359">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4360">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4360">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-4361">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-4361">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-4362">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4362">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-4363">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-4363">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-4364">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4364">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-4365">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-4365">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-4366">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4366">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-4367">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4367">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4368">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4368">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4369">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4369">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4371">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-4371">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4373">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4373">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4375">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-4375">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4377">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4377">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4379">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4379">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4381">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-4381">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-4382">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-4382">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4384">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-4385">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-4386">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-4387">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-4387">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4389">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4389">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="0fc30-4390">DXGI_FORMAT_R8 \_ San<sup>FCS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4390">DXGI_FORMAT_R8\_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="0fc30-4391">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-4391">Target</span></span> | <span data-ttu-id="0fc30-4392">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4392">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-4393">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-4394">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-4394">8</span></span> |
| <span data-ttu-id="0fc30-4395">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4395">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4397">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-4397">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4399">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4399">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4401">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4402">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4402">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4403">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4403">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4405">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4405">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4407">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4407">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4409">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-4409">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4411">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-4411">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4413">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4413">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4414">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4415">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4416">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4416">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-4417">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-4417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-4418">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-4418">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4420">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-4420">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-4421">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-4421">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4423">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-4423">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4424">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-4424">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-4425">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-4425">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-4426">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4426">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4427">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4427">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4428">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4428">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-4429">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-4429">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-4430">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4430">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-4431">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-4431">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-4432">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4432">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-4433">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-4433">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-4434">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4434">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-4435">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4435">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4436">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4436">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4437">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4437">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4439">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-4439">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4441">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4441">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4443">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-4443">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4445">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4445">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-4446">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4446">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4448">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-4448">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-4449">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-4449">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4451">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4451">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-4452">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4452">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-4453">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4453">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-4454">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-4454">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4456">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4456">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="0fc30-4457">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4457">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="0fc30-4458">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-4458">Target</span></span> | <span data-ttu-id="0fc30-4459">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4459">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-4460">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4460">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-4461">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-4461">8</span></span> |
| <span data-ttu-id="0fc30-4462">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4462">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4464">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-4464">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4465">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4465">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4466">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4466">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4467">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4467">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4468">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4468">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4470">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4470">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4472">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4472">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4474">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-4474">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4476">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-4476">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4478">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4478">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4480">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4480">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4481">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4481">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4482">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4482">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-4483">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-4483">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-4484">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-4484">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4486">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-4486">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4488">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-4488">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4490">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-4490">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4492">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-4492">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-4493">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-4493">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-4494">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4494">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4495">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4495">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4496">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4496">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-4497">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-4497">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-4498">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4498">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-4499">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-4499">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-4500">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4500">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-4501">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-4501">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-4502">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4502">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-4503">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4503">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4504">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4504">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4505">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4505">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4507">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-4507">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4509">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4509">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4511">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-4511">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4513">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4513">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4515">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4515">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-4517">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-4517">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-4518">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-4518">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-4519">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4519">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-4520">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4520">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-4521">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4521">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-4522">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-4522">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4524">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4524">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="0fc30-4525">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4525">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="0fc30-4526">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-4526">Target</span></span> | <span data-ttu-id="0fc30-4527">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4527">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-4528">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4528">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-4529">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-4529">32</span></span> |
| <span data-ttu-id="0fc30-4530">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4530">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4532">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-4532">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4533">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4533">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4534">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4534">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4535">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4535">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4536">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4536">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4538">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4538">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4540">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4540">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4542">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-4542">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4544">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-4544">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4546">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4546">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4548">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4548">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4549">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4549">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4550">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4550">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-4551">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-4551">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-4552">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-4552">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4554">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-4554">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-4555">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-4555">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4556">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-4556">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4557">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-4557">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-4558">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-4558">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-4559">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4559">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4560">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4560">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4561">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4561">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-4562">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-4562">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-4563">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4563">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-4564">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-4564">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-4565">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4565">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-4566">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-4566">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-4567">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4567">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-4568">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4568">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4569">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4569">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4570">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4570">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4572">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-4572">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4573">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4573">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4574">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-4574">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-4575">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4575">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-4576">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4576">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-4577">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-4577">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-4578">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-4578">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-4579">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4579">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-4580">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4580">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-4581">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4581">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-4582">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-4582">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-4583">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4583">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="0fc30-4584">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4584">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="0fc30-4585">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-4585">Target</span></span> | <span data-ttu-id="0fc30-4586">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4586">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-4587">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4587">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-4588">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-4588">16</span></span> |
| <span data-ttu-id="0fc30-4589">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4589">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4591">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-4591">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4592">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4592">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4593">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4593">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4594">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4594">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4595">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4595">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4597">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4597">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4599">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4599">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4601">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-4601">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4603">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-4603">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4605">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4605">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4607">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4607">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4608">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4608">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4609">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4609">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-4610">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-4610">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-4611">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-4611">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4613">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-4613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-4614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-4614">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4615">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-4615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4616">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-4616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-4617">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-4617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-4618">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4619">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4620">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4620">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-4621">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-4621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-4622">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-4623">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-4623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-4624">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-4625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-4625">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-4626">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-4627">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4628">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4629">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4629">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4631">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-4631">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4632">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4632">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4633">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-4633">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-4634">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4634">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-4635">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4635">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-4636">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-4636">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-4637">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-4637">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-4638">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4638">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-4639">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4639">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-4640">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4640">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-4641">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-4641">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-4642">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4642">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="0fc30-4643">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4643">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="0fc30-4644">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-4644">Target</span></span> | <span data-ttu-id="0fc30-4645">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4645">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-4646">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4646">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-4647">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-4647">16</span></span> |
| <span data-ttu-id="0fc30-4648">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4648">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4650">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-4650">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4651">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4651">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4652">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4652">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4653">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4653">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4654">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4654">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4656">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4656">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4658">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4658">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4660">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-4660">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4662">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-4662">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4664">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4664">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4666">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4666">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4667">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4667">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4668">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4668">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-4669">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-4669">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-4670">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-4670">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4672">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-4672">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-4673">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-4673">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4674">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-4674">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4675">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-4675">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-4676">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-4676">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-4677">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4677">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4678">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4678">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4679">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4679">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-4680">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-4680">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-4681">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4681">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-4682">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-4682">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-4683">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4683">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-4684">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-4684">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-4685">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4685">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-4686">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4686">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4687">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4687">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4688">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4688">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4690">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-4690">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4691">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4691">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4692">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-4692">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-4693">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4693">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-4694">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4694">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-4695">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-4695">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-4696">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-4696">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-4697">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4697">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-4698">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4698">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-4699">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4699">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-4700">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-4700">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-4701">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="0fc30-4702">DXGI_FORMAT_BC1 \_ <sup>PCC</sup> sin tipo (70)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4702">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="0fc30-4703">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-4703">Target</span></span> | <span data-ttu-id="0fc30-4704">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4704">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-4705">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-4706">4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4706">4</span></span> |
| <span data-ttu-id="0fc30-4707">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4707">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4709">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-4709">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4710">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4710">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4711">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4711">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4712">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4712">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4713">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4713">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-4714">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4714">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4716">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4716">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4718">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-4718">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4720">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-4720">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-4721">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4721">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4722">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4722">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4723">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4723">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4724">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4724">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-4725">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-4725">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-4726">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-4726">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4728">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-4728">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-4729">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-4729">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4730">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-4730">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4731">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-4731">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-4732">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-4732">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-4733">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4733">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4734">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4734">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4735">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4735">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-4736">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-4736">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-4737">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4737">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-4738">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-4738">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-4739">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4739">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-4740">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-4740">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-4741">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4741">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-4742">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4742">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4743">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4743">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4744">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4744">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4746">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-4746">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4747">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4747">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4748">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-4748">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-4749">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4749">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-4750">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4750">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-4751">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-4751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-4752">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-4752">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4754">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4754">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-4755">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4755">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-4756">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-4757">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-4757">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4759">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4759">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfccsup-71"></a><span data-ttu-id="0fc30-4760">DXGI_FORMAT_BC1 \_ UNORM<sup>FCC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4760">DXGI_FORMAT_BC1\_UNORM<sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="0fc30-4761">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-4761">Target</span></span> | <span data-ttu-id="0fc30-4762">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4762">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-4763">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4763">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-4764">4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4764">4</span></span> |
| <span data-ttu-id="0fc30-4765">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4765">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4767">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-4767">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4768">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4768">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4769">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4769">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4770">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4770">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4771">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4771">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-4772">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4772">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4774">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4776">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-4776">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4778">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-4778">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4780">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4780">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4782">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4782">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4783">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4783">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4784">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4784">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-4785">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-4785">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-4786">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-4786">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4788">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-4788">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-4789">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-4789">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4790">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-4790">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4791">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-4791">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-4792">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-4792">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-4793">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4793">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4794">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4794">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4795">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4795">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-4796">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-4796">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-4797">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4797">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-4798">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-4798">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-4799">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4799">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-4800">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-4800">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-4801">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4801">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-4802">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4802">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4803">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4803">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4804">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4804">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4806">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-4806">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4807">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4807">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4808">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-4808">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-4809">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4809">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-4810">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4810">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-4811">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-4811">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-4812">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-4812">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4814">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4814">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-4815">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4815">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-4816">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4816">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-4817">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-4817">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4819">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4819">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfccsup-72"></a><span data-ttu-id="0fc30-4820">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FCC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4820">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="0fc30-4821">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-4821">Target</span></span> | <span data-ttu-id="0fc30-4822">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4822">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-4823">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4823">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-4824">4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4824">4</span></span> |
| <span data-ttu-id="0fc30-4825">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4825">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4827">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-4827">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4828">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4828">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4829">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4829">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4830">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4830">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4831">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4831">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-4832">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4832">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4834">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4834">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4836">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-4836">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4838">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-4838">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4840">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4840">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4842">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4842">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4843">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4843">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4844">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4844">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-4845">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-4845">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-4846">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-4846">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4848">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-4848">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-4849">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-4849">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4850">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-4850">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4851">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-4851">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-4852">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-4852">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-4853">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4853">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4854">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4854">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4855">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4855">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-4856">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-4856">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-4857">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4857">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-4858">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-4858">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-4859">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4859">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-4860">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-4860">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-4861">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4861">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-4862">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4862">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4863">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4863">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4864">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4864">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4866">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-4866">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4867">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4867">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4868">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-4868">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-4869">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4869">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-4870">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4870">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-4871">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-4871">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-4872">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-4872">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4874">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4874">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-4875">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4875">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-4876">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4876">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-4877">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-4877">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4879">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4879">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="0fc30-4880">DXGI_FORMAT_BC2 \_ <sup>PCC</sup> sin tipo (73)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4880">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="0fc30-4881">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-4881">Target</span></span> | <span data-ttu-id="0fc30-4882">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4882">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-4883">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4883">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-4884">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-4884">8</span></span> |
| <span data-ttu-id="0fc30-4885">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4885">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4887">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-4887">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4888">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4888">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4889">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4889">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4890">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4890">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4891">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4891">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-4892">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4892">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4894">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4894">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4896">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-4896">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4898">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-4898">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-4899">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4899">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4900">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4900">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4901">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4901">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4902">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4902">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-4903">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-4903">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-4904">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-4904">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4906">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-4906">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-4907">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-4907">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4908">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-4908">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4909">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-4909">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-4910">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-4910">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-4911">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4911">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4912">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4912">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4913">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4913">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-4914">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-4914">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-4915">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4915">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-4916">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-4916">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-4917">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4917">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-4918">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-4918">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-4919">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4919">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-4920">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4920">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4921">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4921">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4922">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4922">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4924">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-4924">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4925">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4925">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4926">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-4926">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-4927">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4927">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-4928">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4928">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-4929">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-4929">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-4930">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-4930">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4932">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4932">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-4933">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4933">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-4934">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4934">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-4935">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-4935">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4937">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4937">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfccsup-74"></a><span data-ttu-id="0fc30-4938">DXGI_FORMAT_BC2 \_ UNORM<sup>FCC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4938">DXGI_FORMAT_BC2\_UNORM<sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="0fc30-4939">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-4939">Target</span></span> | <span data-ttu-id="0fc30-4940">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4940">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-4941">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4941">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-4942">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-4942">8</span></span> |
| <span data-ttu-id="0fc30-4943">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4943">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4945">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-4945">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4946">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4946">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4947">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4947">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4948">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4948">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-4949">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4949">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-4950">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4950">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4952">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-4952">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4954">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-4954">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4956">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-4956">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4958">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4958">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4960">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4960">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4961">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4961">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-4962">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-4962">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-4963">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-4963">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-4964">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-4964">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4966">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-4966">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-4967">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-4967">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4968">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-4968">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4969">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-4969">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-4970">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-4970">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-4971">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-4971">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4972">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4972">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-4973">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4973">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-4974">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-4974">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-4975">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4975">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-4976">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-4976">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-4977">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4977">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-4978">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-4978">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-4979">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-4979">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-4980">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4980">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4981">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-4981">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-4982">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-4982">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4984">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-4984">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4985">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4985">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-4986">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-4986">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-4987">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4987">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-4988">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-4988">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-4989">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-4989">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-4990">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-4990">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4992">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4992">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-4993">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4993">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-4994">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-4994">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-4995">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-4995">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-4997">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-4997">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfccsup-75"></a><span data-ttu-id="0fc30-4998">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FCC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="0fc30-4998">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="0fc30-4999">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-4999">Target</span></span> | <span data-ttu-id="0fc30-5000">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5000">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-5001">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5001">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-5002">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-5002">8</span></span> |
| <span data-ttu-id="0fc30-5003">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5003">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5005">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-5005">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5006">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5006">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5007">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5007">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5008">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5008">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5009">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5009">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-5010">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5010">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5012">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5012">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5014">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-5014">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5016">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-5016">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5018">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5018">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5020">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5020">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5021">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5021">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5022">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5022">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-5023">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-5023">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-5024">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-5024">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5026">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-5026">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-5027">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-5027">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5028">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-5028">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5029">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-5029">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-5030">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-5030">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-5031">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5031">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5032">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5032">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5033">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5033">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-5034">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-5034">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-5035">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5035">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-5036">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-5036">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-5037">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5037">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-5038">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-5038">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-5039">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5039">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-5040">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5040">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5041">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5041">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5042">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5042">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5044">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-5044">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5045">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5045">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5046">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-5046">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-5047">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5047">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-5048">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5048">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-5049">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-5049">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-5050">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-5050">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5052">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5052">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-5053">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5053">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-5054">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5054">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-5055">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-5055">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5057">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5057">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="0fc30-5058">DXGI_FORMAT_BC3 \_ <sup>PCC</sup> sin tipo (76)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5058">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="0fc30-5059">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-5059">Target</span></span> | <span data-ttu-id="0fc30-5060">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5060">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-5061">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5061">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-5062">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-5062">8</span></span> |
| <span data-ttu-id="0fc30-5063">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5063">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5065">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-5065">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5066">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5066">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5067">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5067">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5068">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5068">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5069">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5069">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-5070">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5070">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5072">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5072">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5074">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-5074">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5076">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-5076">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-5077">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5077">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5078">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5078">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5079">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5079">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5080">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5080">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-5081">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-5081">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-5082">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-5082">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5084">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-5084">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-5085">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-5085">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5086">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-5086">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5087">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-5087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-5088">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-5088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-5089">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5090">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5091">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5091">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-5092">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-5092">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-5093">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5093">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-5094">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-5094">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-5095">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5095">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-5096">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-5096">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-5097">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5097">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-5098">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5098">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5099">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5099">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5100">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5100">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5102">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-5102">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5103">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5103">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5104">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-5104">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-5105">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5105">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-5106">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5106">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-5107">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-5107">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-5108">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-5108">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5110">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-5111">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-5112">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-5113">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-5113">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5115">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5115">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfccsup-77"></a><span data-ttu-id="0fc30-5116">DXGI_FORMAT_BC3 \_ UNORM<sup>FCC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5116">DXGI_FORMAT_BC3\_UNORM<sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="0fc30-5117">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-5117">Target</span></span> | <span data-ttu-id="0fc30-5118">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5118">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-5119">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5119">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-5120">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-5120">8</span></span> |
| <span data-ttu-id="0fc30-5121">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5121">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5123">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-5123">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5124">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5124">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5125">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5125">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5126">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5126">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5127">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5127">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-5128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5128">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5130">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5132">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-5132">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5134">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-5134">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5136">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5136">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5138">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5138">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5139">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5139">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5140">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5140">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-5141">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-5141">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-5142">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-5142">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5144">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-5144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-5145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-5145">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5146">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-5146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5147">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-5147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-5148">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-5148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-5149">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5150">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5151">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5151">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-5152">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-5152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-5153">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-5154">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-5154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-5155">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-5156">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-5156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-5157">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-5158">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5159">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5160">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5160">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5162">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-5162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5163">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5164">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-5164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-5165">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-5166">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5166">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-5167">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-5167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-5168">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-5168">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5170">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5170">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-5171">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5171">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-5172">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5172">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-5173">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-5173">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5175">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5175">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfccsup-78"></a><span data-ttu-id="0fc30-5176">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FCC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5176">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="0fc30-5177">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-5177">Target</span></span> | <span data-ttu-id="0fc30-5178">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5178">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-5179">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5179">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-5180">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-5180">8</span></span> |
| <span data-ttu-id="0fc30-5181">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5181">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5183">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-5183">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5184">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5184">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5185">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5185">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5186">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5186">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5187">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5187">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-5188">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5188">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5190">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5190">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5192">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-5192">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5194">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-5194">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5196">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5196">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5198">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5198">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5199">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5199">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5200">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5200">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-5201">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-5201">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-5202">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-5202">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5204">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-5204">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-5205">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-5205">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5206">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-5206">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5207">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-5207">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-5208">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-5208">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-5209">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5209">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5210">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5210">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5211">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5211">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-5212">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-5212">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-5213">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5213">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-5214">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-5214">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-5215">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5215">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-5216">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-5216">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-5217">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5217">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-5218">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5218">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5219">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5219">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5220">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5220">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5222">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-5222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5223">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5224">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-5224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-5225">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-5226">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5226">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-5227">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-5227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-5228">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-5228">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5230">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5230">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-5231">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5231">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-5232">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5232">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-5233">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-5233">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5235">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5235">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="0fc30-5236">DXGI_FORMAT_BC4 \_ <sup>PCC</sup> sin tipo (79)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5236">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="0fc30-5237">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-5237">Target</span></span> | <span data-ttu-id="0fc30-5238">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5238">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-5239">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5239">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-5240">4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5240">4</span></span> |
| <span data-ttu-id="0fc30-5241">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5241">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5243">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-5243">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5244">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5244">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5245">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5245">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5246">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5246">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5247">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-5248">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5248">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5250">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5250">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-5252">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5254">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-5254">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-5255">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5255">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5256">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5256">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5257">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5257">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5258">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5258">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-5259">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-5259">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-5260">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-5260">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5262">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-5262">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-5263">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-5263">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5264">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-5264">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5265">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-5265">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-5266">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-5266">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-5267">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5267">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5268">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5268">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5269">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5269">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-5270">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-5270">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-5271">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5271">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-5272">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-5272">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-5273">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5273">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-5274">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-5274">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-5275">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5275">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-5276">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5276">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5277">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5277">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5278">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5278">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5280">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-5280">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5281">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5281">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5282">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-5282">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-5283">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5283">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-5284">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5284">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-5285">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-5285">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-5286">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-5286">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5288">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5288">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-5289">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5289">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-5290">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5290">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-5291">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-5291">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-5292">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5292">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfccsup-80"></a><span data-ttu-id="0fc30-5293">DXGI_FORMAT_BC4 \_ UNORM<sup>FCC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5293">DXGI_FORMAT_BC4\_UNORM<sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="0fc30-5294">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-5294">Target</span></span> | <span data-ttu-id="0fc30-5295">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5295">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-5296">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5296">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-5297">4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5297">4</span></span> |
| <span data-ttu-id="0fc30-5298">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5298">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5300">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-5300">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5301">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5301">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5302">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5302">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5303">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5303">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5304">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5304">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-5305">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5305">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5307">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5307">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5309">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-5309">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5311">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-5311">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5313">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5313">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5315">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5315">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5316">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5316">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5317">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5317">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-5318">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-5318">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-5319">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-5319">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5321">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-5321">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-5322">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-5322">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5323">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-5323">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5324">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-5324">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-5325">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-5325">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-5326">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5326">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5327">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5327">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5328">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5328">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-5329">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-5329">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-5330">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5330">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-5331">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-5331">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-5332">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5332">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-5333">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-5333">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-5334">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5334">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-5335">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5335">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5336">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5336">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5337">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5337">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5339">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-5339">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5340">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5340">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5341">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-5341">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-5342">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5342">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-5343">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5343">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-5344">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-5344">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-5345">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-5345">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5347">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5347">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-5348">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5348">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-5349">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5349">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-5350">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-5350">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-5351">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5351">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfccsup-81"></a><span data-ttu-id="0fc30-5352">DXGI_FORMAT_BC4 \_ SNORM<sup>FCC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5352">DXGI_FORMAT_BC4\_SNORM<sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="0fc30-5353">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-5353">Target</span></span> | <span data-ttu-id="0fc30-5354">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5354">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-5355">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5355">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-5356">4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5356">4</span></span> |
| <span data-ttu-id="0fc30-5357">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5357">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5359">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-5359">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5360">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5360">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5361">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5361">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5362">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5362">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5363">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5363">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-5364">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5364">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5366">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5366">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5368">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-5368">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5370">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-5370">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5372">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5372">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5374">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5374">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5375">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5375">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5376">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5376">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-5377">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-5377">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-5378">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-5378">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5380">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-5380">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-5381">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-5381">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5382">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-5382">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5383">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-5383">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-5384">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-5384">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-5385">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5385">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5386">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5386">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5387">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5387">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-5388">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-5388">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-5389">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5389">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-5390">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-5390">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-5391">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5391">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-5392">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-5392">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-5393">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5393">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-5394">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5394">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5395">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5395">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5396">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5396">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5398">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-5398">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5399">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5399">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5400">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-5400">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-5401">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5401">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-5402">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5402">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-5403">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-5403">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-5404">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-5404">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5406">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5406">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-5407">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5407">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-5408">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5408">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-5409">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-5409">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-5410">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5410">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="0fc30-5411">DXGI_FORMAT_BC5 \_ <sup>PCC</sup> sin tipo (82)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5411">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="0fc30-5412">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-5412">Target</span></span> | <span data-ttu-id="0fc30-5413">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5413">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-5414">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5414">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-5415">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-5415">8</span></span> |
| <span data-ttu-id="0fc30-5416">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5416">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5418">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-5418">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5419">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5419">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5420">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5420">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5421">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5421">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5422">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5422">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-5423">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5423">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5425">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5425">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5427">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-5427">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5429">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-5429">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-5430">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5430">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5431">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5431">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5432">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5432">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5433">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5433">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-5434">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-5434">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-5435">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-5435">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5437">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-5437">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-5438">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-5438">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5439">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-5439">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5440">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-5440">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-5441">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-5441">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-5442">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5442">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5443">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5443">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5444">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5444">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-5445">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-5445">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-5446">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5446">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-5447">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-5447">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-5448">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5448">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-5449">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-5449">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-5450">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5450">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-5451">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5451">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5452">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5452">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5453">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5453">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5455">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-5455">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5456">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5456">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5457">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-5457">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-5458">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5458">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-5459">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5459">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-5460">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-5460">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-5461">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-5461">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5463">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5463">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-5464">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5464">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-5465">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5465">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-5466">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-5466">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-5467">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5467">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfccsup-83"></a><span data-ttu-id="0fc30-5468">DXGI_FORMAT_BC5 \_ UNORM<sup>FCC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5468">DXGI_FORMAT_BC5\_UNORM<sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="0fc30-5469">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-5469">Target</span></span> | <span data-ttu-id="0fc30-5470">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5470">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-5471">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5471">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-5472">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-5472">8</span></span> |
| <span data-ttu-id="0fc30-5473">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5473">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5475">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-5475">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5476">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5476">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5477">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5477">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5478">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5478">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5479">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5479">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-5480">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5480">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5482">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5482">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5484">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-5484">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5486">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-5486">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5488">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5488">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5490">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5490">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5491">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5491">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5492">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5492">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-5493">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-5493">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-5494">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-5494">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5496">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-5496">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-5497">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-5497">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5498">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-5498">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5499">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-5499">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-5500">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-5500">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-5501">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5501">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5502">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5502">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5503">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5503">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-5504">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-5504">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-5505">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5505">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-5506">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-5506">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-5507">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5507">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-5508">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-5508">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-5509">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5509">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-5510">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5510">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5511">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5511">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5512">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5512">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5514">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-5514">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5515">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5515">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5516">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-5516">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-5517">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5517">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-5518">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5518">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-5519">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-5519">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-5520">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-5520">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5522">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5522">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-5523">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5523">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-5524">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5524">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-5525">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-5525">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-5526">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5526">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfccsup-84"></a><span data-ttu-id="0fc30-5527">DXGI_FORMAT_BC5 \_ SNORM<sup>FCC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5527">DXGI_FORMAT_BC5\_SNORM<sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="0fc30-5528">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-5528">Target</span></span> | <span data-ttu-id="0fc30-5529">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5529">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-5530">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5530">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-5531">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-5531">8</span></span> |
| <span data-ttu-id="0fc30-5532">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5532">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5534">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-5534">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5535">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5535">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5536">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5536">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5537">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5537">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5538">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5538">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-5539">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5539">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5541">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5541">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5543">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-5543">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5545">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-5545">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5547">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5547">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5549">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5549">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5550">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5550">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5551">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5551">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-5552">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-5552">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-5553">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-5553">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5555">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-5555">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-5556">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-5556">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5557">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-5557">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5558">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-5558">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-5559">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-5559">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-5560">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5560">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5561">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5561">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5562">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5562">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-5563">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-5563">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-5564">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5564">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-5565">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-5565">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-5566">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5566">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-5567">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-5567">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-5568">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5568">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-5569">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5569">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5570">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5570">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5571">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5571">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5573">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-5573">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5574">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5574">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5575">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-5575">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-5576">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5576">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-5577">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5577">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-5578">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-5578">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-5579">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-5579">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5581">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5581">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-5582">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5582">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-5583">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5583">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-5584">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-5584">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-5585">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5585">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="0fc30-5586">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5586">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="0fc30-5587">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-5587">Target</span></span> | <span data-ttu-id="0fc30-5588">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5588">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-5589">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5589">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-5590">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-5590">16</span></span> |
| <span data-ttu-id="0fc30-5591">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5591">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5593">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-5593">Buffer</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5595">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5595">Input Assembler Vertex Buffer</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5597">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5597">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5598">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5598">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5599">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5599">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5601">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5601">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5603">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5603">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-5605">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5607">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-5607">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5609">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5609">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5611">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5611">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5612">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5612">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5613">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5613">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-5614">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-5614">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-5615">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-5615">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5617">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-5617">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-5619">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5621">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-5621">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5623">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-5623">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-5624">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-5624">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-5625">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5625">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5626">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5626">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5627">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5627">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-5628">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-5628">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-5629">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5629">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-5630">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-5630">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-5631">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5631">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-5632">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-5632">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-5633">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5633">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-5634">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5634">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5635">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5635">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5636">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5636">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5638">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-5638">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5640">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5640">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5642">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-5642">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5644">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5644">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5646">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5646">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5648">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-5648">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-5649">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-5649">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-5650">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5650">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-5651">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5651">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-5652">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5652">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-5653">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-5653">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-5654">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5654">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="0fc30-5655">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5655">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="0fc30-5656">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-5656">Target</span></span> | <span data-ttu-id="0fc30-5657">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5657">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-5658">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5658">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-5659">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-5659">16</span></span> |
| <span data-ttu-id="0fc30-5660">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5660">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5662">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-5662">Buffer</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5664">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5664">Input Assembler Vertex Buffer</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5666">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5666">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5667">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5667">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5668">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5668">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5670">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5670">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5672">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5672">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5674">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-5674">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5676">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-5676">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5678">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5678">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5680">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5680">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5681">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5681">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5682">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5682">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-5683">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-5683">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-5684">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-5684">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5686">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-5686">Mipmap Auto-Generation</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5688">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-5688">RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5690">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-5690">Blendable RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5692">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-5692">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-5693">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-5693">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-5694">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5694">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5695">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5695">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5696">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5696">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-5697">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-5697">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-5698">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5698">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-5699">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-5699">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-5700">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5700">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-5701">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-5701">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-5702">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5702">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-5703">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5703">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5704">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5704">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5705">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5705">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5707">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-5707">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5709">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5709">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5711">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-5711">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5713">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5713">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5715">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5715">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5717">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-5717">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-5718">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-5718">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-5719">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5719">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-5720">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5720">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-5721">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5721">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-5722">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-5722">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-5723">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5723">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="0fc30-5724">DXGI_FORMAT_B8G8R8A8 de \_ <sup>equipos</sup> sin tipo (90)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5724">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="0fc30-5725">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-5725">Target</span></span> | <span data-ttu-id="0fc30-5726">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5726">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-5727">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5727">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-5728">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-5728">32</span></span> |
| <span data-ttu-id="0fc30-5729">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5729">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5731">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-5731">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5732">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5732">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5733">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5733">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5734">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5734">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5735">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5735">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5737">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5737">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5739">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5739">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5741">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-5741">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5743">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-5743">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-5744">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5744">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5745">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5745">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5746">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5746">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5747">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5747">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-5748">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-5748">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-5749">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-5749">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5751">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-5751">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-5752">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-5752">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5753">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-5753">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5754">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-5754">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-5755">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-5755">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-5756">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5756">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5757">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5757">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5758">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5758">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-5759">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-5759">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-5760">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5760">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-5761">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-5761">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-5762">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5762">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-5763">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-5763">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-5764">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5764">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-5765">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5765">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5766">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5766">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5767">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5767">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5769">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-5769">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5770">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5770">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5771">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-5771">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-5772">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5772">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-5773">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5773">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-5774">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-5774">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-5775">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-5775">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5777">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5777">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-5778">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5778">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-5779">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5779">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-5780">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-5780">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5782">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="0fc30-5783">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FCS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5783">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="0fc30-5784">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-5784">Target</span></span> | <span data-ttu-id="0fc30-5785">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5785">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-5786">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-5787">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-5787">32</span></span> |
| <span data-ttu-id="0fc30-5788">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5788">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5790">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-5790">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5792">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5792">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5794">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5794">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5795">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5795">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5796">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5796">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5798">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5798">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5800">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5800">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5802">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-5802">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5804">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-5804">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5806">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5806">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5808">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5808">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5809">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5809">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5810">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5810">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-5811">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-5811">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-5812">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-5812">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5814">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-5814">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5816">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-5816">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5818">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-5818">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5820">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-5820">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-5821">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-5821">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-5822">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5822">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5823">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5823">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5824">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5824">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-5825">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-5825">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-5826">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5826">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-5827">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-5827">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-5828">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5828">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-5829">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-5829">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-5830">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5830">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-5831">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5831">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5832">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5832">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5833">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5833">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5835">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-5835">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5837">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5837">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5839">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-5839">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5841">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5841">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5843">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5843">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5845">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-5845">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5847">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-5847">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5849">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5849">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-5850">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5850">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5852">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5852">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5854">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-5854">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5856">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5856">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="0fc30-5857">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRGB<sup>FCS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5857">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="0fc30-5858">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-5858">Target</span></span> | <span data-ttu-id="0fc30-5859">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5859">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-5860">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5860">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-5861">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-5861">32</span></span> |
| <span data-ttu-id="0fc30-5862">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5862">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5864">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-5864">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5865">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5865">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5866">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5866">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5867">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5867">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5868">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5868">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5870">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5870">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5872">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5872">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5874">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-5874">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5876">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-5876">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5878">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5878">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5880">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5880">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5881">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5881">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5882">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5882">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-5883">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-5883">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-5884">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-5884">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5886">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-5886">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5888">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-5888">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5890">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-5890">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5892">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-5892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-5893">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-5893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-5894">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5895">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5896">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5896">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-5897">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-5897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-5898">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-5899">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-5899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-5900">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-5901">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-5901">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-5902">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-5903">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5904">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5905">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5905">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5907">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-5907">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5909">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5909">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5911">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-5911">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5913">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5913">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5915">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5915">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5917">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-5917">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5919">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-5919">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5921">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5921">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-5922">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5922">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5924">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5924">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-5926">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-5926">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5928">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="0fc30-5929">DXGI_FORMAT_B8G8R8X8 de \_ <sup>equipos</sup> sin tipo (92)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5929">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="0fc30-5930">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-5930">Target</span></span> | <span data-ttu-id="0fc30-5931">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5931">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-5932">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-5933">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-5933">32</span></span> |
| <span data-ttu-id="0fc30-5934">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5934">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5936">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-5936">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5937">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5937">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5938">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5938">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5939">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5939">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-5940">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5940">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5942">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5942">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5944">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-5944">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5946">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-5946">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5948">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-5948">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-5949">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5949">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5950">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5950">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5951">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5951">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-5952">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-5952">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-5953">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-5953">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-5954">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-5954">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5956">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-5956">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-5957">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-5957">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5958">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-5958">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5959">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-5959">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-5960">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-5960">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-5961">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5961">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5962">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5962">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-5963">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5963">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-5964">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-5964">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-5965">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5965">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-5966">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-5966">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-5967">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5967">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-5968">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-5968">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-5969">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-5969">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-5970">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5970">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5971">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-5971">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-5972">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5972">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5974">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-5974">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5975">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5975">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-5976">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-5976">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-5977">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5977">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-5978">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-5978">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-5979">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-5979">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-5980">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-5980">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5982">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5982">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-5983">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5983">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-5984">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-5984">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-5985">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-5985">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5987">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5987">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="0fc30-5988">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FCS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5988">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="0fc30-5989">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-5989">Target</span></span> | <span data-ttu-id="0fc30-5990">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-5990">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-5991">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-5991">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-5992">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-5992">32</span></span> |
| <span data-ttu-id="0fc30-5993">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-5993">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5995">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-5995">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5997">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5997">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-5999">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-5999">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6000">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6000">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6001">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6001">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6003">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6003">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6005">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6005">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6007">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-6007">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6009">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-6009">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6011">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6011">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6013">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6013">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6014">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6014">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6015">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-6015">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-6016">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-6016">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-6017">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-6017">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6019">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-6019">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6021">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-6021">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6023">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-6023">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6025">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-6025">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-6026">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-6026">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-6027">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6027">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6028">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6028">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6029">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6029">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-6030">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-6030">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-6031">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6031">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-6032">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-6032">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-6033">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6033">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-6034">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-6034">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-6035">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6035">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-6036">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6036">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6037">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6037">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6038">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6038">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6040">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-6040">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6042">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6042">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6044">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-6044">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6046">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6046">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6048">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6048">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6050">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-6050">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-6051">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-6051">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6053">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6053">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-6054">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6054">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6056">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6056">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6058">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-6058">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6060">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6060">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="0fc30-6061">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRGB<sup>FCS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6061">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="0fc30-6062">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-6062">Target</span></span> | <span data-ttu-id="0fc30-6063">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6063">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-6064">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6064">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-6065">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-6065">32</span></span> |
| <span data-ttu-id="0fc30-6066">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6066">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6068">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-6068">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6069">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6069">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6070">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6070">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6071">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6071">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6072">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6072">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6074">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6074">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6076">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6076">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6078">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-6078">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6080">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-6080">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6082">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6082">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6084">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6084">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6085">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6085">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6086">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-6086">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-6087">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-6087">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-6088">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-6088">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6090">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-6090">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6092">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-6092">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6094">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-6094">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6096">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-6096">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-6097">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-6097">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-6098">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6098">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6099">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6099">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6100">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6100">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-6101">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-6101">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-6102">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6102">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-6103">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-6103">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-6104">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6104">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-6105">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-6105">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-6106">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6106">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-6107">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6107">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6108">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6108">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6109">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6109">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6111">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-6111">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6113">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6113">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6115">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-6115">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6117">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6117">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6119">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6119">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6121">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-6121">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-6122">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-6122">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6124">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6124">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-6125">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6125">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-6126">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6126">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-6127">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-6127">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6129">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6129">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="0fc30-6130">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6130">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="0fc30-6131">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-6131">Target</span></span> | <span data-ttu-id="0fc30-6132">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6132">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-6133">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6133">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-6134">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-6134">32</span></span> |
| <span data-ttu-id="0fc30-6135">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6135">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6137">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-6137">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6138">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6138">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6139">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6139">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6140">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6140">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6141">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6141">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-6142">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6142">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6144">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6144">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-6145">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-6145">TextureCube</span></span> | \- |
| <span data-ttu-id="0fc30-6146">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-6146">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6148">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6148">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6150">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6150">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6151">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6151">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6152">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-6152">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-6153">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-6153">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-6154">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-6154">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6156">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-6156">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6158">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-6158">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6160">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-6160">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6162">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-6162">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-6163">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-6163">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-6164">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6164">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6165">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6165">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6166">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6166">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-6167">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-6167">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-6168">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6168">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-6169">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-6169">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-6170">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6170">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-6171">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-6171">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-6172">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6172">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-6173">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6173">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6174">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6174">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6175">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6175">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6177">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-6177">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6178">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6178">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6179">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-6179">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-6180">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6180">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-6181">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6181">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-6182">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-6182">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-6183">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-6183">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-6184">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6184">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6186">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6186">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6188">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6188">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6190">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-6190">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6192">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6192">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="0fc30-6193">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6193">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="0fc30-6194">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-6194">Target</span></span> | <span data-ttu-id="0fc30-6195">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6195">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-6196">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6196">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-6197">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-6197">32</span></span> |
| <span data-ttu-id="0fc30-6198">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6198">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6200">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-6200">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6201">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6201">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6202">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6202">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6203">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6203">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6204">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6204">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-6205">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6205">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6207">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6207">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-6208">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-6208">TextureCube</span></span> | \- |
| <span data-ttu-id="0fc30-6209">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-6209">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6211">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6211">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6213">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6213">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6214">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6214">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6215">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-6215">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-6216">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-6216">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-6217">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-6217">Mipmap</span></span> | \- |
| <span data-ttu-id="0fc30-6218">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-6218">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-6219">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-6219">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6220">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-6220">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6221">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-6221">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-6222">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-6222">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-6223">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6223">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6224">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6224">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6225">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6225">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-6226">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-6226">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-6227">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6227">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-6228">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-6228">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-6229">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6229">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-6230">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-6230">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-6231">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6231">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-6232">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6232">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6233">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6233">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6234">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6234">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6236">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-6236">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6237">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6237">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6238">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-6238">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-6239">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6239">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-6240">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6240">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-6241">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-6241">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-6242">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-6242">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-6243">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6243">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6245">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6245">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6247">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6247">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6249">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-6249">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6251">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6251">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="0fc30-6252">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6252">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="0fc30-6253">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-6253">Target</span></span> | <span data-ttu-id="0fc30-6254">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6254">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-6255">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6255">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-6256">64</span><span class="sxs-lookup"><span data-stu-id="0fc30-6256">64</span></span> |
| <span data-ttu-id="0fc30-6257">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6257">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6259">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-6259">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6260">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6260">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6261">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6261">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6262">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6262">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6263">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6263">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-6264">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6264">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6266">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6266">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-6267">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-6267">TextureCube</span></span> | \- |
| <span data-ttu-id="0fc30-6268">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-6268">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6270">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6270">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6272">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6272">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6273">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6273">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6274">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-6274">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-6275">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-6275">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-6276">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-6276">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6278">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-6278">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-6279">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-6279">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6280">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-6280">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6281">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-6281">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-6282">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-6282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-6283">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6284">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6285">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6285">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-6286">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-6286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-6287">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-6288">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-6288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-6289">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-6290">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-6290">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-6291">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-6292">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6293">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6294">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6294">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6296">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-6296">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6297">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6297">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6298">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-6298">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-6299">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6299">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-6300">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6300">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-6301">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-6301">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-6302">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-6302">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-6303">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6303">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6305">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6305">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6307">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6307">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6309">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-6309">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6311">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6311">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="0fc30-6312">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6312">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="0fc30-6313">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-6313">Target</span></span> | <span data-ttu-id="0fc30-6314">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6314">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-6315">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6315">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-6316">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-6316">8</span></span> |
| <span data-ttu-id="0fc30-6317">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6317">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6319">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-6319">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6320">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6320">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6321">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6321">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6322">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6322">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6323">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6323">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-6324">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6324">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6326">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6326">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-6327">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-6327">TextureCube</span></span> | \- |
| <span data-ttu-id="0fc30-6328">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-6328">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6330">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6330">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6332">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6332">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6333">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6333">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6334">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-6334">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-6335">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-6335">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-6336">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-6336">Mipmap</span></span> | \- |
| <span data-ttu-id="0fc30-6337">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-6337">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-6338">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-6338">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6340">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-6340">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6342">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-6342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-6343">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-6343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-6344">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6345">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6346">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6346">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-6347">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-6347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-6348">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-6349">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-6349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-6350">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-6351">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-6351">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-6352">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-6353">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6354">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6355">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6355">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6357">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-6357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6358">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6359">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-6359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-6360">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-6361">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6361">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-6362">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-6362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-6363">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-6363">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-6364">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6364">Video Decoder Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6366">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6366">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6368">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6368">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6370">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-6370">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6372">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6372">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="0fc30-6373">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6373">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="0fc30-6374">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-6374">Target</span></span> | <span data-ttu-id="0fc30-6375">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6375">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-6376">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6376">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-6377">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-6377">16</span></span> |
| <span data-ttu-id="0fc30-6378">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6378">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6380">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-6380">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6381">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6381">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6382">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6382">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6383">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6383">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6384">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6384">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-6385">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6385">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6387">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6387">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-6388">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-6388">TextureCube</span></span> | \- |
| <span data-ttu-id="0fc30-6389">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-6389">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6391">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6391">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6393">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6393">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6394">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6394">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6395">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-6395">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-6396">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-6396">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-6397">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-6397">Mipmap</span></span> | \- |
| <span data-ttu-id="0fc30-6398">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-6398">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-6399">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-6399">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6401">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-6401">Blendable RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6403">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-6403">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-6404">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-6404">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-6405">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6405">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6406">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6406">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6407">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6407">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-6408">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-6408">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-6409">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6409">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-6410">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-6410">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-6411">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6411">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-6412">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-6412">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-6413">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6413">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-6414">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6414">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6415">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6415">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6416">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6416">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6418">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-6418">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6419">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6419">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6420">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-6420">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-6421">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6421">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-6422">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6422">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-6423">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-6423">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-6424">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-6424">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-6425">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6425">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6427">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6427">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6429">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6429">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6431">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-6431">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6433">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6433">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="0fc30-6434">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6434">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="0fc30-6435">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-6435">Target</span></span> | <span data-ttu-id="0fc30-6436">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6436">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-6437">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6437">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-6438">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-6438">16</span></span> |
| <span data-ttu-id="0fc30-6439">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6439">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6441">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-6441">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6442">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6442">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6443">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6443">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6444">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6444">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6445">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6445">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-6446">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6446">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6448">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6448">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-6449">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-6449">TextureCube</span></span> | \- |
| <span data-ttu-id="0fc30-6450">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-6450">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6452">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6452">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6454">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6454">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6455">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6455">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6456">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-6456">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-6457">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-6457">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-6458">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-6458">Mipmap</span></span> | \- |
| <span data-ttu-id="0fc30-6459">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-6459">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-6460">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-6460">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6462">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-6462">Blendable RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6464">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-6464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-6465">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-6465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-6466">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6467">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6468">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6468">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-6469">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-6469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-6470">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-6471">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-6471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-6472">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-6473">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-6473">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-6474">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-6475">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6476">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6477">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6477">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6479">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-6479">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6480">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6480">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6481">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-6481">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-6482">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6482">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-6483">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6483">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-6484">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-6484">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-6485">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-6485">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-6486">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6486">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6488">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6488">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6490">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6490">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6492">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-6492">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6494">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6494">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="0fc30-6495">DXGI_FORMAT_420 \_ opaca<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6495">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="0fc30-6496">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-6496">Target</span></span> | <span data-ttu-id="0fc30-6497">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6497">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-6498">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6498">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-6499">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-6499">8</span></span> |
| <span data-ttu-id="0fc30-6500">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6500">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6502">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-6502">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6503">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6503">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6504">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6504">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6505">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6505">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6506">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6506">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-6507">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6507">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6509">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6509">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-6510">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-6510">TextureCube</span></span> | \- |
| <span data-ttu-id="0fc30-6511">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-6511">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-6512">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6512">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6513">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6513">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6514">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6514">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6515">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-6515">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-6516">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-6516">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-6517">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-6517">Mipmap</span></span> | \- |
| <span data-ttu-id="0fc30-6518">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-6518">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-6519">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-6519">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6520">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-6520">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6521">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-6521">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-6522">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-6522">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-6523">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6523">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6524">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6524">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6525">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6525">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-6526">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-6526">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-6527">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6527">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-6528">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-6528">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-6529">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6529">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-6530">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-6530">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-6531">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6531">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-6532">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6532">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6533">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6533">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6534">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6534">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0fc30-6535">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-6535">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6536">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6536">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6537">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-6537">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-6538">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6538">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-6539">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6539">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-6540">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-6540">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-6541">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-6541">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-6542">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6542">Video Decoder Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6544">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6544">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6546">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6546">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6548">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-6548">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6550">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6550">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="0fc30-6551">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6551">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="0fc30-6552">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-6552">Target</span></span> | <span data-ttu-id="0fc30-6553">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6553">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-6554">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6554">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-6555">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-6555">16</span></span> |
| <span data-ttu-id="0fc30-6556">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6556">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6558">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-6558">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6559">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6559">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6560">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6560">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6561">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6561">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6562">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6562">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-6563">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6563">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6565">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6565">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-6566">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-6566">TextureCube</span></span> | \- |
| <span data-ttu-id="0fc30-6567">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-6567">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6569">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6569">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6571">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6571">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6572">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6572">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6573">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-6573">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-6574">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-6574">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-6575">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-6575">Mipmap</span></span> | \- |
| <span data-ttu-id="0fc30-6576">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-6576">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-6577">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-6577">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6578">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-6578">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6579">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-6579">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-6580">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-6580">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-6581">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6581">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6582">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6582">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6583">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6583">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-6584">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-6584">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-6585">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6585">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-6586">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-6586">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-6587">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6587">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-6588">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-6588">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-6589">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6589">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-6590">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6590">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6591">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6591">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6592">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6592">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6594">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-6594">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6595">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6595">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6596">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-6596">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-6597">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6597">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-6598">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6598">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-6599">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-6599">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-6600">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-6600">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-6601">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6601">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6603">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6603">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6605">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6605">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6607">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-6607">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6609">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6609">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="0fc30-6610">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6610">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="0fc30-6611">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-6611">Target</span></span> | <span data-ttu-id="0fc30-6612">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6612">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-6613">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6613">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-6614">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-6614">32</span></span> |
| <span data-ttu-id="0fc30-6615">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6615">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6617">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-6617">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6618">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6618">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6619">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6619">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6620">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6620">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6621">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6621">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-6622">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6622">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6624">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6624">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-6625">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-6625">TextureCube</span></span> | \- |
| <span data-ttu-id="0fc30-6626">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-6626">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6628">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6628">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6630">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6630">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6631">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6631">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6632">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-6632">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-6633">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-6633">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-6634">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-6634">Mipmap</span></span> | \- |
| <span data-ttu-id="0fc30-6635">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-6635">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-6636">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-6636">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6637">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-6637">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6638">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-6638">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-6639">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-6639">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-6640">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6640">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6641">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6641">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6642">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6642">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-6643">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-6643">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-6644">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6644">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-6645">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-6645">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-6646">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6646">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-6647">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-6647">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-6648">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6648">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-6649">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6649">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6650">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6650">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6651">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6651">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6653">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-6653">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6654">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6654">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6655">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-6655">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-6656">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6656">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-6657">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6657">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-6658">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-6658">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-6659">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-6659">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-6660">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6660">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6662">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6662">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6664">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6664">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6666">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-6666">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6668">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6668">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="0fc30-6669">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6669">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="0fc30-6670">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-6670">Target</span></span> | <span data-ttu-id="0fc30-6671">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6671">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-6672">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6672">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-6673">32</span><span class="sxs-lookup"><span data-stu-id="0fc30-6673">32</span></span> |
| <span data-ttu-id="0fc30-6674">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6674">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6676">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-6676">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6677">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6677">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6678">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6678">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6679">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6679">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6680">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6680">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-6681">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6681">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6683">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6683">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-6684">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-6684">TextureCube</span></span> | \- |
| <span data-ttu-id="0fc30-6685">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-6685">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6687">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6687">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6689">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6689">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6690">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6690">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6691">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-6691">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-6692">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-6692">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-6693">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-6693">Mipmap</span></span> | \- |
| <span data-ttu-id="0fc30-6694">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-6694">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-6695">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-6695">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6696">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-6696">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6697">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-6697">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-6698">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-6698">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-6699">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6699">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6700">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6700">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6701">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6701">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-6702">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-6702">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-6703">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6703">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-6704">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-6704">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-6705">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6705">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-6706">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-6706">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-6707">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6707">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-6708">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6708">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6709">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6709">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6710">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6710">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6712">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-6712">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6713">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6713">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6714">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-6714">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-6715">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6715">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-6716">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6716">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-6717">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-6717">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-6718">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-6718">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-6719">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6719">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6721">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6721">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6723">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6723">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6725">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-6725">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6727">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6727">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="0fc30-6728">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6728">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="0fc30-6729">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-6729">Target</span></span> | <span data-ttu-id="0fc30-6730">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6730">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-6731">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6731">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-6732">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-6732">8</span></span> |
| <span data-ttu-id="0fc30-6733">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6733">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6735">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-6735">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6736">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6736">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6737">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6737">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6738">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6738">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6739">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6739">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-6740">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6740">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6742">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6742">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-6743">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-6743">TextureCube</span></span> | \- |
| <span data-ttu-id="0fc30-6744">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-6744">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6746">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6746">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6748">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6748">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6749">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6749">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6750">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-6750">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-6751">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-6751">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-6752">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-6752">Mipmap</span></span> | \- |
| <span data-ttu-id="0fc30-6753">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-6753">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-6754">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-6754">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6756">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-6756">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6758">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-6758">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-6759">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-6759">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-6760">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6760">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6761">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6761">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6762">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6762">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-6763">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-6763">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-6764">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6764">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-6765">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-6765">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-6766">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6766">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-6767">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-6767">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-6768">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6768">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-6769">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6769">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6770">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6770">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6771">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6771">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6773">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-6773">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6774">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6774">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6775">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-6775">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-6776">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6776">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-6777">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6777">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-6778">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-6778">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-6779">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-6779">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-6780">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6780">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6782">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6782">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6784">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6784">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6786">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-6786">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6788">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6788">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="0fc30-6789">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6789">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="0fc30-6790">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-6790">Target</span></span> | <span data-ttu-id="0fc30-6791">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6791">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-6792">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6792">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-6793">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-6793">8</span></span> |
| <span data-ttu-id="0fc30-6794">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6794">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6796">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-6796">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6797">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6797">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6798">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6798">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6799">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6799">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6800">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6800">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-6801">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6801">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6803">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6803">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-6804">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-6804">TextureCube</span></span> | \- |
| <span data-ttu-id="0fc30-6805">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-6805">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-6806">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6806">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6807">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6807">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6808">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6808">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6809">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-6809">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-6810">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-6810">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-6811">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-6811">Mipmap</span></span> | \- |
| <span data-ttu-id="0fc30-6812">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-6812">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-6813">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-6813">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6814">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-6814">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6815">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-6815">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-6816">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-6816">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-6817">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6817">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6818">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6818">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6819">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6819">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-6820">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-6820">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-6821">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6821">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-6822">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-6822">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-6823">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6823">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-6824">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-6824">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-6825">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6825">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-6826">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6826">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6827">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6827">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6828">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6828">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6830">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-6830">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6831">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6831">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6832">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-6832">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-6833">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6833">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-6834">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6834">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-6835">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-6835">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-6836">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-6836">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-6837">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6837">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-6838">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6838">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6840">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6840">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-6841">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-6841">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-6842">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6842">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="0fc30-6843">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6843">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="0fc30-6844">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-6844">Target</span></span> | <span data-ttu-id="0fc30-6845">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6845">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-6846">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6846">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-6847">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-6847">8</span></span> |
| <span data-ttu-id="0fc30-6848">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6848">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6850">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-6850">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6851">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6851">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6852">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6852">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6853">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6853">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6854">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6854">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-6855">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6855">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6857">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6857">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-6858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-6858">TextureCube</span></span> | \- |
| <span data-ttu-id="0fc30-6859">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-6859">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-6860">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6860">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6861">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6861">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6862">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6862">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6863">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-6863">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-6864">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-6864">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-6865">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-6865">Mipmap</span></span> | \- |
| <span data-ttu-id="0fc30-6866">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-6866">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-6867">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-6867">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6868">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-6868">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6869">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-6869">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-6870">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-6870">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-6871">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6871">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6872">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6872">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6873">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6873">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-6874">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-6874">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-6875">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6875">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-6876">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-6876">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-6877">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6877">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-6878">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-6878">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-6879">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6879">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-6880">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6880">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6881">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6881">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6882">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6882">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6884">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-6884">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6885">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6885">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6886">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-6886">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-6887">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6887">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-6888">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6888">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-6889">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-6889">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-6890">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-6890">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-6891">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6891">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-6892">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6892">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6894">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6894">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-6895">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-6895">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-6896">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6896">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="0fc30-6897">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6897">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="0fc30-6898">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-6898">Target</span></span> | <span data-ttu-id="0fc30-6899">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6899">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-6900">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6900">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-6901">8</span><span class="sxs-lookup"><span data-stu-id="0fc30-6901">8</span></span> |
| <span data-ttu-id="0fc30-6902">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6902">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6904">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-6904">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6905">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6905">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6906">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6906">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6907">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6907">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6908">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6908">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-6909">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6909">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6911">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6911">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-6912">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-6912">TextureCube</span></span> | \- |
| <span data-ttu-id="0fc30-6913">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-6913">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-6914">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6914">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6915">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6915">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6916">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6916">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6917">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-6917">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-6918">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-6918">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-6919">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-6919">Mipmap</span></span> | \- |
| <span data-ttu-id="0fc30-6920">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-6920">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-6921">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-6921">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6922">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-6922">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6923">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-6923">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-6924">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-6924">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-6925">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6925">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6926">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6926">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6927">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6927">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-6928">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-6928">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-6929">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6929">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-6930">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-6930">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-6931">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6931">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-6932">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-6932">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-6933">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6933">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-6934">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6934">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6935">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6935">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6936">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6936">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6938">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-6938">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6939">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6939">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6940">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-6940">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-6941">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6941">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-6942">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6942">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-6943">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-6943">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-6944">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-6944">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-6945">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6945">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-6946">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6946">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6948">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6948">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-6949">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-6949">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-6950">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6950">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="0fc30-6951">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6951">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="0fc30-6952">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-6952">Target</span></span> | <span data-ttu-id="0fc30-6953">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-6953">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-6954">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6954">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-6955">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-6955">16</span></span> |
| <span data-ttu-id="0fc30-6956">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6956">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-6958">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-6958">Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6959">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6959">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6960">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6960">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6961">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6961">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-6962">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6962">Texture1D</span></span> | \- |
| <span data-ttu-id="0fc30-6963">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6963">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6965">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-6965">Texture3D</span></span> | \- |
| <span data-ttu-id="0fc30-6966">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-6966">TextureCube</span></span> | \- |
| <span data-ttu-id="0fc30-6967">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-6967">Shader ld</span></span> | \- |
| <span data-ttu-id="0fc30-6968">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6968">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6969">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6969">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6970">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-6970">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-6971">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-6971">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-6972">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-6972">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-6973">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-6973">Mipmap</span></span> | \- |
| <span data-ttu-id="0fc30-6974">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-6974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0fc30-6975">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-6975">RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6976">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-6976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6977">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-6977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-6978">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-6978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-6979">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-6979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6980">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-6981">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6981">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-6982">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-6982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-6983">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-6984">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-6984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-6985">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-6986">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-6986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-6987">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-6987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-6988">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6989">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-6989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-6990">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-6990">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-6992">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-6992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6993">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0fc30-6994">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-6994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0fc30-6995">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0fc30-6996">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-6996">Multisample Load</span></span> | \- |
| <span data-ttu-id="0fc30-6997">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-6997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-6998">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-6998">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-6999">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-6999">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-7000">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-7000">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-7002">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-7002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-7003">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-7003">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-7004">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-7004">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="0fc30-7005">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="0fc30-7005">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="0fc30-7006">Destino</span><span class="sxs-lookup"><span data-stu-id="0fc30-7006">Target</span></span> | <span data-ttu-id="0fc30-7007">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0fc30-7007">Support</span></span> |
| - | - |
| <span data-ttu-id="0fc30-7008">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="0fc30-7008">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0fc30-7009">16</span><span class="sxs-lookup"><span data-stu-id="0fc30-7009">16</span></span> |
| <span data-ttu-id="0fc30-7010">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-7010">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-7012">Buffer</span><span class="sxs-lookup"><span data-stu-id="0fc30-7012">Buffer</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-7014">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-7014">Input Assembler Vertex Buffer</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-7016">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="0fc30-7016">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-7017">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="0fc30-7017">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0fc30-7018">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fc30-7018">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-7020">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fc30-7020">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-7022">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fc30-7022">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-7024">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fc30-7024">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-7026">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="0fc30-7026">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-7028">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="0fc30-7028">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-7030">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="0fc30-7030">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0fc30-7031">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="0fc30-7031">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0fc30-7032">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="0fc30-7032">Shader gather4</span></span> | \- |
| <span data-ttu-id="0fc30-7033">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0fc30-7033">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0fc30-7034">Mapa</span><span class="sxs-lookup"><span data-stu-id="0fc30-7034">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-7036">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="0fc30-7036">Mipmap Auto-Generation</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-7038">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0fc30-7038">RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-7040">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="0fc30-7040">Blendable RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-7042">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="0fc30-7042">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0fc30-7043">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="0fc30-7043">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0fc30-7044">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="0fc30-7044">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-7045">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="0fc30-7045">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0fc30-7046">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-7046">Typed UAV</span></span> | \- |
| <span data-ttu-id="0fc30-7047">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc30-7047">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0fc30-7048">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-7048">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0fc30-7049">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0fc30-7049">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0fc30-7050">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-7050">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0fc30-7051">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0fc30-7051">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0fc30-7052">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="0fc30-7052">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0fc30-7053">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-7053">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-7054">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="0fc30-7054">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0fc30-7055">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="0fc30-7055">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-7057">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="0fc30-7057">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-7059">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-7059">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-7061">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="0fc30-7061">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-7063">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc30-7063">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="0fc30-7065">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="0fc30-7065">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="0fc30-7067">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0fc30-7067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0fc30-7068">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="0fc30-7068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0fc30-7069">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-7069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0fc30-7070">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-7070">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0fc30-7071">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-7071">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0fc30-7072">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="0fc30-7072">Shared Resource</span></span> | \- |
| <span data-ttu-id="0fc30-7073">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0fc30-7073">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="0fc30-7074">Dar formato a notas</span><span class="sxs-lookup"><span data-stu-id="0fc30-7074">Format notes</span></span>

<span data-ttu-id="0fc30-7075">El propósito del formato puede cambiar de un nivel de característica de hardware a otro.</span><span class="sxs-lookup"><span data-stu-id="0fc30-7075">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="0fc30-7076"><sup>L</sup> : formato sin tipo</span><span class="sxs-lookup"><span data-stu-id="0fc30-7076"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="0fc30-7077"><sup>PC</sup> : diseño parcialmente tipado, de conversión de tipos y sencillo</span><span class="sxs-lookup"><span data-stu-id="0fc30-7077"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="0fc30-7078"><sup>FCS</sup> : diseño totalmente tipado, convertible y sencillo</span><span class="sxs-lookup"><span data-stu-id="0fc30-7078"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="0fc30-7079"><sup>FNS</sup> : diseño totalmente tipado, sin conversión y simple</span><span class="sxs-lookup"><span data-stu-id="0fc30-7079"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="0fc30-7080"><sup>PCC</sup> : diseño parcialmente tipado, convertible y complejo</span><span class="sxs-lookup"><span data-stu-id="0fc30-7080"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="0fc30-7081"><sup>FCC</sup> : diseño totalmente tipado, convertible y complejo</span><span class="sxs-lookup"><span data-stu-id="0fc30-7081"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="0fc30-7082"><sup>FNC</sup> : diseño totalmente tipado, no convertible y complejo</span><span class="sxs-lookup"><span data-stu-id="0fc30-7082"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="0fc30-7083"><sup>V</sup> : formato de vídeo</span><span class="sxs-lookup"><span data-stu-id="0fc30-7083"><sup>V</sup> : video format</span></span>
</dt> </dl>

<span data-ttu-id="0fc30-7084">Los búferes de reserva y los recorridos con el [**formato de DXGI \_ R16G16B16A16 formato \_ \_ float**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) contienen datos de gamma con valores lineales.</span><span class="sxs-lookup"><span data-stu-id="0fc30-7084">Back buffers and scan outs with the [**DXGI\_FORMAT\_R16G16B16A16\_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format contain linear-valued gamma data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0fc30-7085">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0fc30-7085">Related topics</span></span>

[<span data-ttu-id="0fc30-7086">Niveles de características de hardware de D3D12</span><span class="sxs-lookup"><span data-stu-id="0fc30-7086">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="0fc30-7087">**ID3D10Device::CheckFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="0fc30-7087">**ID3D10Device::CheckFormatSupport**</span></span>](/windows/win32/api/d3d10/nf-d3d10-id3d10device-checkformatsupport)

[<span data-ttu-id="0fc30-7088">Guía de programación para DXGI</span><span class="sxs-lookup"><span data-stu-id="0fc30-7088">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
