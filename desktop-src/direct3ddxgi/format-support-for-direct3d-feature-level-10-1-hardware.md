---
description: En esta sección se especifican los formatos ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que se admiten en el hardware de nivel de característica de Direct3D 10,1.
ms.assetid: 2C7E16D7-EEF0-4EA7-A819-5274C9105F68
title: Compatibilidad con el formato de hardware de la característica de nivel 10.1 de Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edb5c81ef0a99bc14031a9a7a505736e91e13d8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494723"
---
# <a name="format-support-for-direct3d-feature-level-101-hardware"></a><span data-ttu-id="ad36b-103">Compatibilidad con el formato de hardware de la característica de nivel 10.1 de Direct3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-103">Format support for Direct3D Feature Level 10.1 hardware</span></span>

<span data-ttu-id="ad36b-104">En esta sección se especifican los formatos ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que se admiten en el hardware de nivel de característica de Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="ad36b-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 10.1 hardware.</span></span>

<span data-ttu-id="ad36b-105">En la tabla se resume la compatibilidad de las características con la siguiente clave.</span><span class="sxs-lookup"><span data-stu-id="ad36b-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="ad36b-106">Símbolo</span><span class="sxs-lookup"><span data-stu-id="ad36b-106">Symbol</span></span>                            | <span data-ttu-id="ad36b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad36b-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="ad36b-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="ad36b-108">_ *-*\*</span></span>                             | <span data-ttu-id="ad36b-109">No permitido o no disponible.</span><span class="sxs-lookup"><span data-stu-id="ad36b-109">Disallowed or not available.</span></span>                                                  |
| ![requerido](images/letter-r.jpg)  | <span data-ttu-id="ad36b-111">Se requiere compatibilidad con hardware.</span><span class="sxs-lookup"><span data-stu-id="ad36b-111">Hardware support is required.</span></span>                                                 |
| ![opcional](images/letter-o.jpg)  | <span data-ttu-id="ad36b-113">Compatibilidad de hardware opcional, el formato puede ser o no acelerado por hardware.</span><span class="sxs-lookup"><span data-stu-id="ad36b-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dependientes](images/letter-d.jpg) | <span data-ttu-id="ad36b-115">Requerido si se admite la característica opcional relacionada.</span><span class="sxs-lookup"><span data-stu-id="ad36b-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="ad36b-116">Este tema contiene una sección por formato.</span><span class="sxs-lookup"><span data-stu-id="ad36b-116">This topic contains a section per format.</span></span> <span data-ttu-id="ad36b-117">Un *destino* de formato (las tablas contienen una fila por destino) puede ser un tipo de recurso, una función intrínseca de HLSL o una funcionalidad determinada que depende de un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="ad36b-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="ad36b-118">Para comprobar mediante programación la compatibilidad de formato en D3D11 y D3D12, consulte Comprobación de la compatibilidad de las [características de hardware](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="ad36b-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="ad36b-119">Los números de los formatos son principalmente, pero no todos, en orden numérico ascendente; &mdash; algunos están fuera del orden numérico y se enumeran junto con otros formatos relevantes.</span><span class="sxs-lookup"><span data-stu-id="ad36b-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="ad36b-120">Tenga en cuenta también que los *tipos sin tipo* en un nombre de formato pueden significar un tipo *parcial* y no tienen un tipo estricto (consulte la sección [notas de formato](#format-notes) al final del tema).</span><span class="sxs-lookup"><span data-stu-id="ad36b-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="ad36b-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="ad36b-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="ad36b-122">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-122">Target</span></span> | <span data-ttu-id="ad36b-123">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-123">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-124">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-125">0</span><span class="sxs-lookup"><span data-stu-id="ad36b-125">0</span></span> |
| <span data-ttu-id="ad36b-126">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-126">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-128">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-128">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-130">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-131">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-132">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-133">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-134">Texture2D</span></span> | \- |
| <span data-ttu-id="ad36b-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-135">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-136">TextureCube</span></span> | \- |
| <span data-ttu-id="ad36b-137">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-137">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-138">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-139">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-139">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-140">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-140">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-141">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-142">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-142">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-143">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-143">Mipmap</span></span> | \- |
| <span data-ttu-id="ad36b-144">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-146">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-147">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-148">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-149">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-150">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-151">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-151">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-152">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-153">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-154">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-155">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-156">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-157">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-158">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-159">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-160">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-160">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-162">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-163">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-164">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-165">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-166">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-166">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-167">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-168">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-168">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-169">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-170">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-171">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-172">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-172">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-173">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="ad36b-174">DXGI_FORMAT_R32G32B32A32 de \_ <sup>equipos</sup> sin tipo (1)</span><span class="sxs-lookup"><span data-stu-id="ad36b-174">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="ad36b-175">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-175">Target</span></span> | <span data-ttu-id="ad36b-176">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-176">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-177">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-178">128</span><span class="sxs-lookup"><span data-stu-id="ad36b-178">128</span></span> |
| <span data-ttu-id="ad36b-179">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-179">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-181">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-181">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-182">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-182">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-183">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-183">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-184">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-184">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-185">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-185">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-187">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-189">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-189">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-191">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-191">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-193">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-193">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-194">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-194">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-195">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-195">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-196">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-196">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-197">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-197">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-198">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-198">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-199">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-199">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-201">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-201">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-202">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-202">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-203">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-203">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-204">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-204">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-205">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-206">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-207">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-208">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-208">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-209">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-209">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-210">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-210">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-211">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-211">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-212">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-212">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-213">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-213">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-214">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-214">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-215">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-215">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-216">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-216">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-217">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-217">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-219">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-219">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-220">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-220">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-221">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-221">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-222">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-222">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-223">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-223">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-224">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-224">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-225">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-225">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-227">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-227">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-228">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-228">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-229">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-229">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-230">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-230">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-232">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-232">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="ad36b-233">DXGI_FORMAT_R32G32B32A32 \_ float<sup>FCS</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="ad36b-233">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="ad36b-234">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-234">Target</span></span> | <span data-ttu-id="ad36b-235">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-235">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-236">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-236">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-237">128</span><span class="sxs-lookup"><span data-stu-id="ad36b-237">128</span></span> |
| <span data-ttu-id="ad36b-238">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-238">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-240">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-240">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-242">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-242">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-244">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-244">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-245">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-245">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-247">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-249">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-249">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-251">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-253">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-253">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-255">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-255">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-257">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-257">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-259">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-260">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-261">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-261">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-262">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-263">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-263">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-265">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-265">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-267">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-267">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-269">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-269">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-271">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-272">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-273">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-274">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-275">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-275">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-276">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-276">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-277">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-277">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-278">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-278">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-279">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-279">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-280">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-280">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-281">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-281">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-282">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-282">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-283">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-283">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-284">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-284">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-286">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-286">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-288">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-288">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-290">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-290">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-292">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-292">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-294">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-294">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-296">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-296">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-297">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-297">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-299">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-299">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-300">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-300">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-301">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-301">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-302">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-302">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-304">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-304">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="ad36b-305">DXGI_FORMAT_R32G32B32A32 \_ uint<sup>FCS</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="ad36b-305">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="ad36b-306">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-306">Target</span></span> | <span data-ttu-id="ad36b-307">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-307">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-308">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-308">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-309">128</span><span class="sxs-lookup"><span data-stu-id="ad36b-309">128</span></span> |
| <span data-ttu-id="ad36b-310">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-310">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-312">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-312">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-314">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-314">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-316">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-316">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-317">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-317">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-319">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-319">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-321">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-321">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-323">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-323">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-325">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-325">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-327">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-327">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-329">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-329">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-330">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-330">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-331">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-331">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-332">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-332">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-333">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-333">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-334">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-334">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-336">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-336">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-337">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-337">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-339">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-339">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-340">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-340">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-342">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-342">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-343">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-343">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-344">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-344">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-345">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-345">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-346">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-346">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-347">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-347">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-348">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-348">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-349">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-349">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-350">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-350">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-351">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-351">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-352">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-352">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-353">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-353">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-354">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-354">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-356">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-356">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-358">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-358">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-360">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-360">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-362">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-362">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-363">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-363">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-365">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-365">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-366">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-366">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-368">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-369">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-370">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-371">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-371">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-373">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-373">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="ad36b-374">DXGI_FORMAT_R32G32B32A32 \_ San<sup>FCS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="ad36b-374">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="ad36b-375">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-375">Target</span></span> | <span data-ttu-id="ad36b-376">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-376">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-377">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-377">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-378">128</span><span class="sxs-lookup"><span data-stu-id="ad36b-378">128</span></span> |
| <span data-ttu-id="ad36b-379">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-379">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-381">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-381">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-383">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-383">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-385">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-385">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-386">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-386">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-388">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-388">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-390">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-390">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-392">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-392">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-394">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-396">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-396">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-398">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-399">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-400">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-401">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-401">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-402">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-403">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-403">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-405">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-406">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-406">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-408">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-409">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-410">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-411">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-412">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-413">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-414">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-415">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-416">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-417">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-419">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-420">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-421">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-422">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-422">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-424">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-424">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-426">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-426">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-428">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-428">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-430">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-430">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-431">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-431">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-433">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-434">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-434">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-436">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-437">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-438">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-439">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-439">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-441">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="ad36b-442">DXGI_FORMAT_R32G32B32 de \_ <sup>equipos</sup> sin tipo (5)</span><span class="sxs-lookup"><span data-stu-id="ad36b-442">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="ad36b-443">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-443">Target</span></span> | <span data-ttu-id="ad36b-444">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-444">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-445">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-446">96</span><span class="sxs-lookup"><span data-stu-id="ad36b-446">96</span></span> |
| <span data-ttu-id="ad36b-447">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-447">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-449">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-449">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-450">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-451">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-452">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-453">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-455">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-455">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-457">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-459">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-459">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-461">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-461">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-462">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-462">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-463">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-463">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-464">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-464">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-465">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-465">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-466">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-466">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-467">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-467">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-469">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-470">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-471">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-472">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-473">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-474">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-475">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-476">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-476">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-477">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-478">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-479">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-480">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-481">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-481">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-482">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-483">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-484">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-485">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-485">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-487">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-487">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-488">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-488">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-489">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-489">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-490">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-490">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-491">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-491">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-492">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-492">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-493">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-493">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-495">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-496">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-497">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-498">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-498">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-499">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="ad36b-500">DXGI_FORMAT_R32G32B32 \_ float<sup>FCS</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="ad36b-500">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="ad36b-501">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-501">Target</span></span> | <span data-ttu-id="ad36b-502">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-502">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-503">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-504">96</span><span class="sxs-lookup"><span data-stu-id="ad36b-504">96</span></span> |
| <span data-ttu-id="ad36b-505">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-505">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-507">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-507">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-509">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-509">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-511">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-511">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-512">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-512">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-514">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-514">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-516">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-518">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-520">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-522">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-522">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-524">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-524">Shader sample (any filter)</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-526">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-526">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-527">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-527">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-528">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-528">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-529">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-529">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-530">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-530">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-532">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-532">Mipmap Auto-Generation</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-534">RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-536">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-536">Blendable RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="ad36b-538">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-538">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-539">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-539">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-540">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-540">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-541">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-541">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-542">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-542">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-543">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-543">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-544">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-544">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-545">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-545">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-546">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-546">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-547">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-547">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-548">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-548">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-549">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-549">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-550">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-550">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-551">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-551">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-553">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-553">4x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="ad36b-555">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-555">8x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="ad36b-557">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-557">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-559">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-559">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-561">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-561">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-563">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-563">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-564">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-564">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-566">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-566">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-567">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-567">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-568">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-568">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-569">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-569">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-570">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-570">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="ad36b-571">DXGI_FORMAT_R32G32B32 \_ uint<sup>FCS</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="ad36b-571">DXGI_FORMAT_R32G32B32\_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="ad36b-572">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-572">Target</span></span> | <span data-ttu-id="ad36b-573">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-573">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-574">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-574">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-575">96</span><span class="sxs-lookup"><span data-stu-id="ad36b-575">96</span></span> |
| <span data-ttu-id="ad36b-576">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-576">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-578">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-578">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-580">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-580">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-582">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-583">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-583">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-585">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-587">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-589">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-591">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-591">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-593">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-593">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-595">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-595">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-596">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-596">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-597">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-597">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-598">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-598">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-599">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-600">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-600">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-602">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-602">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-603">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-603">RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-605">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-606">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-606">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-608">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-608">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-609">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-609">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-610">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-610">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-611">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-611">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-612">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-612">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-613">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-613">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-614">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-614">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-615">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-615">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-616">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-616">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-617">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-617">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-618">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-618">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-619">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-619">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-620">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-620">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-622">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-622">4x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="ad36b-624">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-624">8x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="ad36b-626">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-626">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-628">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-628">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-629">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-629">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-631">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-631">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-632">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-632">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-634">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-634">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-635">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-635">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-636">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-636">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-637">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-637">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-638">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-638">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="ad36b-639">DXGI_FORMAT_R32G32B32 \_ San<sup>FCS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="ad36b-639">DXGI_FORMAT_R32G32B32\_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="ad36b-640">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-640">Target</span></span> | <span data-ttu-id="ad36b-641">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-641">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-642">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-642">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-643">96</span><span class="sxs-lookup"><span data-stu-id="ad36b-643">96</span></span> |
| <span data-ttu-id="ad36b-644">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-644">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-646">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-646">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-648">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-648">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-650">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-650">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-651">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-651">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-653">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-655">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-657">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-659">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-661">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-661">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-663">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-664">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-665">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-666">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-666">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-667">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-668">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-668">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-670">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-670">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-671">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-671">RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-673">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-673">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-674">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-675">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-676">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-677">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-678">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-678">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-679">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-680">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-681">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-682">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-683">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-683">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-684">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-685">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-686">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-687">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-687">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-689">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-689">4x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="ad36b-691">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-691">8x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="ad36b-693">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-693">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-695">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-696">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-696">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-698">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-698">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-699">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-699">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-701">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-701">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-702">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-702">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-703">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-703">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-704">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-704">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-705">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-705">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="ad36b-706">DXGI_FORMAT_R16G16B16A16 de \_ <sup>equipos</sup> sin tipo (9)</span><span class="sxs-lookup"><span data-stu-id="ad36b-706">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="ad36b-707">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-707">Target</span></span> | <span data-ttu-id="ad36b-708">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-708">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-709">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-709">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-710">64</span><span class="sxs-lookup"><span data-stu-id="ad36b-710">64</span></span> |
| <span data-ttu-id="ad36b-711">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-711">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-713">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-713">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-714">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-714">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-715">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-715">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-716">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-716">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-717">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-717">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-719">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-719">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-721">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-721">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-723">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-723">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-725">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-725">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-726">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-726">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-727">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-727">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-728">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-728">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-729">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-729">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-730">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-730">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-731">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-731">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-733">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-733">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-734">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-734">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-735">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-735">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-736">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-736">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-737">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-738">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-739">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-740">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-740">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-741">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-741">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-742">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-742">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-743">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-743">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-744">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-744">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-745">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-745">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-746">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-746">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-747">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-747">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-748">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-748">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-749">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-749">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-751">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-751">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-752">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-752">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-753">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-753">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-754">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-754">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-755">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-755">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-756">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-756">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-757">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-757">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-759">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-759">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-760">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-760">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-761">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-761">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-762">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-762">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-764">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-764">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="ad36b-765">DXGI_FORMAT_R16G16B16A16 \_ de<sup>FCS</sup> Float (10)</span><span class="sxs-lookup"><span data-stu-id="ad36b-765">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="ad36b-766">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-766">Target</span></span> | <span data-ttu-id="ad36b-767">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-767">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-768">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-768">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-769">64</span><span class="sxs-lookup"><span data-stu-id="ad36b-769">64</span></span> |
| <span data-ttu-id="ad36b-770">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-770">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-772">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-772">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-774">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-774">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-776">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-776">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-777">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-777">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-778">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-778">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-780">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-780">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-782">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-782">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-784">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-786">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-786">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-788">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-788">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-790">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-790">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-791">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-791">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-792">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-792">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-793">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-793">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-794">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-794">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-796">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-796">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-798">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-798">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-800">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-800">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-802">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-802">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-803">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-803">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-804">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-804">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-805">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-805">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-806">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-806">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-807">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-807">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-808">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-808">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-809">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-809">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-810">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-810">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-811">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-811">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-812">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-812">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-813">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-813">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-814">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-814">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-815">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-815">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-817">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-817">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-819">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-819">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-821">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-821">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-823">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-823">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-825">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-825">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-827">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-827">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-829">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-829">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-831">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-831">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-832">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-832">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-834">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-834">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-836">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-836">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-838">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-838">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="ad36b-839">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FCS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="ad36b-839">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="ad36b-840">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-840">Target</span></span> | <span data-ttu-id="ad36b-841">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-841">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-842">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-842">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-843">64</span><span class="sxs-lookup"><span data-stu-id="ad36b-843">64</span></span> |
| <span data-ttu-id="ad36b-844">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-844">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-846">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-846">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-848">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-848">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-850">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-850">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-851">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-851">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-852">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-852">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-854">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-854">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-856">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-856">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-858">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-860">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-860">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-862">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-862">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-864">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-864">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-865">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-865">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-866">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-866">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-867">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-867">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-868">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-868">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-870">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-870">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-872">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-872">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-874">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-874">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-876">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-877">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-878">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-879">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-880">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-880">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-881">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-882">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-883">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-884">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-885">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-886">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-887">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-888">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-889">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-889">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-891">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-891">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-893">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-893">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-895">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-895">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-897">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-897">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-899">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-899">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-901">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-901">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-902">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-902">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-904">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-905">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-906">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-907">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-907">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-909">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-909">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="ad36b-910">DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FCS</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="ad36b-910">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="ad36b-911">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-911">Target</span></span> | <span data-ttu-id="ad36b-912">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-912">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-913">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-913">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-914">64</span><span class="sxs-lookup"><span data-stu-id="ad36b-914">64</span></span> |
| <span data-ttu-id="ad36b-915">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-915">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-917">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-917">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-919">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-919">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-921">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-921">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-922">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-922">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-923">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-923">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-925">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-927">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-929">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-929">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-931">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-931">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-933">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-934">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-935">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-936">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-936">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-937">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-938">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-938">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-940">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-940">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-941">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-941">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-943">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-943">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-944">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-944">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-946">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-946">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-947">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-947">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-948">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-948">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-949">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-949">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-950">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-950">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-951">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-951">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-952">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-952">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-953">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-953">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-954">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-954">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-955">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-955">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-956">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-956">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-957">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-957">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-958">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-958">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-960">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-960">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-962">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-962">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-964">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-964">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-966">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-966">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-967">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-967">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-969">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-969">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-970">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-970">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-972">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-972">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-973">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-973">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-974">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-974">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-975">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-975">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-977">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-977">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="ad36b-978">DXGI_FORMAT_R16G16B16A16 \_ SNORM<sup>FCS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="ad36b-978">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="ad36b-979">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-979">Target</span></span> | <span data-ttu-id="ad36b-980">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-980">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-981">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-981">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-982">64</span><span class="sxs-lookup"><span data-stu-id="ad36b-982">64</span></span> |
| <span data-ttu-id="ad36b-983">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-983">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-985">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-985">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-987">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-987">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-989">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-990">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-991">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-993">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-993">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-995">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-995">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-997">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-997">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-999">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-999">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1001">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1001">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1003">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1003">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1004">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1004">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1005">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-1005">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-1006">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-1006">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-1007">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-1007">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1009">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-1009">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-1011">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1013">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-1013">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1015">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-1015">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-1016">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-1016">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-1017">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1017">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1018">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1018">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1019">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1019">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-1020">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-1020">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-1021">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1021">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-1022">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-1022">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-1023">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1023">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-1024">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-1024">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-1025">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1025">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-1026">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1026">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1027">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1027">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1028">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1028">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1030">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-1030">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1032">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1032">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1034">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-1034">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1036">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1036">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1038">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1038">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1040">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-1040">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-1041">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-1041">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1043">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1043">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-1044">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1044">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-1045">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1045">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-1046">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-1046">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1048">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1048">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="ad36b-1049">DXGI_FORMAT_R16G16B16A16 \_ San<sup>FCS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1049">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="ad36b-1050">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-1050">Target</span></span> | <span data-ttu-id="ad36b-1051">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1051">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-1052">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1052">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-1053">64</span><span class="sxs-lookup"><span data-stu-id="ad36b-1053">64</span></span> |
| <span data-ttu-id="ad36b-1054">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1054">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1056">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-1056">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1058">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1058">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1060">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1060">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1061">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1061">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1062">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1062">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1064">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1064">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1066">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1066">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1068">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-1068">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1070">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-1070">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1072">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1072">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1073">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1073">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1074">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1074">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1075">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-1075">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-1076">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-1076">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-1077">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-1077">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1079">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-1079">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-1080">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-1080">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1082">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-1082">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1083">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-1083">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-1084">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-1084">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-1085">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1085">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1086">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1086">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1087">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1087">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-1088">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-1088">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-1089">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1089">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-1090">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-1090">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-1091">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1091">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-1092">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-1092">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-1093">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1093">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-1094">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1094">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1095">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1095">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1096">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1096">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1098">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-1098">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1100">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1100">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1102">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-1102">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1104">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1104">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-1105">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1105">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1107">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-1107">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-1108">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-1108">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1110">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-1111">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-1112">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-1113">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-1113">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1115">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1115">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="ad36b-1116">DXGI_FORMAT_R32G32 de \_ <sup>equipos</sup> sin tipo (15)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1116">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="ad36b-1117">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-1117">Target</span></span> | <span data-ttu-id="ad36b-1118">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1118">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-1119">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1119">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-1120">64</span><span class="sxs-lookup"><span data-stu-id="ad36b-1120">64</span></span> |
| <span data-ttu-id="ad36b-1121">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1121">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1123">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-1123">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1124">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1124">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1125">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1125">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1126">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1126">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1127">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1127">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1129">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1129">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1131">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1131">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1133">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-1133">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1135">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-1135">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-1136">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1137">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1138">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1139">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-1139">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-1140">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-1140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-1141">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-1141">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1143">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-1143">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-1144">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-1144">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1145">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-1145">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1146">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-1146">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-1147">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-1147">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-1148">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1148">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1149">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1149">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1150">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1150">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-1151">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-1151">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-1152">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1152">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-1153">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-1153">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-1154">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1154">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-1155">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-1155">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-1156">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1156">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-1157">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1157">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1158">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1158">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1159">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1159">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1161">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-1161">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1162">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1162">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1163">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-1163">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-1164">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1164">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-1165">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1165">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-1166">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-1166">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-1167">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-1167">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1169">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-1170">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-1171">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-1172">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-1172">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-1173">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="ad36b-1174">DXGI_FORMAT_R32G32 \_ float<sup>FCS</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1174">DXGI_FORMAT_R32G32\_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="ad36b-1175">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-1175">Target</span></span> | <span data-ttu-id="ad36b-1176">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1176">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-1177">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-1178">64</span><span class="sxs-lookup"><span data-stu-id="ad36b-1178">64</span></span> |
| <span data-ttu-id="ad36b-1179">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1179">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1181">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-1181">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1183">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1183">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1185">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1185">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1186">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1186">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1188">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1188">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1190">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1190">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1192">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1192">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1194">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-1194">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1196">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-1196">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1198">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1198">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1200">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1200">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1201">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1201">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1202">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-1202">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-1203">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-1203">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-1204">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-1204">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1206">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-1206">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1208">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-1208">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1210">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-1210">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1212">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-1212">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-1213">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-1213">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-1214">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1214">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1215">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1215">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1216">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1216">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-1217">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-1217">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-1218">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1218">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-1219">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-1219">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-1220">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1220">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-1221">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-1221">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-1222">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1222">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-1223">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1223">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1224">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1224">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1225">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1225">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1227">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-1227">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1229">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1229">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1231">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-1231">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1233">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1233">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1235">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1235">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1237">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-1237">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-1238">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-1238">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1240">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1240">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-1241">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1241">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-1242">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1242">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-1243">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-1243">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-1244">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1244">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="ad36b-1245">DXGI_FORMAT_R32G32 \_ uint<sup>FCS</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1245">DXGI_FORMAT_R32G32\_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="ad36b-1246">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-1246">Target</span></span> | <span data-ttu-id="ad36b-1247">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1247">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-1248">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1248">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-1249">64</span><span class="sxs-lookup"><span data-stu-id="ad36b-1249">64</span></span> |
| <span data-ttu-id="ad36b-1250">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1250">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1252">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-1252">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1254">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1254">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1256">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1256">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1257">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1257">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1259">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1259">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1261">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1261">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1263">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1263">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1265">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-1265">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1267">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-1267">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1269">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1269">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1270">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1270">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1271">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1271">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1272">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-1272">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-1273">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-1273">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-1274">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-1274">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1276">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-1276">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-1277">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-1277">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1279">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-1279">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1280">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-1280">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1282">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-1282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-1283">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1284">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1285">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1285">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-1286">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-1286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-1287">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-1288">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-1288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-1289">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-1290">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-1290">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-1291">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-1292">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1293">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1294">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1294">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1296">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-1296">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1298">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1298">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1300">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-1300">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1302">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1302">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-1303">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1303">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1305">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-1305">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-1306">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-1306">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1308">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1308">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-1309">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1309">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-1310">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1310">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-1311">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-1311">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-1312">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1312">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="ad36b-1313">DXGI_FORMAT_R32G32 \_ San<sup>FCS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1313">DXGI_FORMAT_R32G32\_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="ad36b-1314">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-1314">Target</span></span> | <span data-ttu-id="ad36b-1315">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1315">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-1316">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1316">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-1317">64</span><span class="sxs-lookup"><span data-stu-id="ad36b-1317">64</span></span> |
| <span data-ttu-id="ad36b-1318">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1318">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1320">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-1320">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1322">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1322">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1324">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1324">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1325">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1325">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1327">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1327">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1329">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1329">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1331">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1331">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1333">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-1333">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1335">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-1335">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1337">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1337">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1338">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1338">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1339">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1339">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1340">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-1340">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-1341">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-1341">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-1342">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-1342">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1344">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-1344">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-1345">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-1345">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1347">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-1347">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1348">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-1348">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-1349">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-1349">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-1350">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1350">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1351">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1351">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1352">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1352">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-1353">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-1353">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-1354">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1354">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-1355">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-1355">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-1356">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1356">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-1357">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-1357">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-1358">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1358">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-1359">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1359">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1360">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1360">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1361">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1361">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1363">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-1363">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1365">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1365">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1367">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-1367">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1369">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-1370">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1370">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1372">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-1372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-1373">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-1373">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1375">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1375">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-1376">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1376">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-1377">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1377">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-1378">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-1378">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-1379">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1379">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="ad36b-1380">DXGI_FORMAT_R32G8X24 de \_ <sup>equipos</sup> sin tipo (19)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1380">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="ad36b-1381">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-1381">Target</span></span> | <span data-ttu-id="ad36b-1382">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1382">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-1383">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1383">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-1384">64</span><span class="sxs-lookup"><span data-stu-id="ad36b-1384">64</span></span> |
| <span data-ttu-id="ad36b-1385">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1385">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1387">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-1387">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1388">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1388">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1389">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1390">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1391">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1393">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1393">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1395">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1395">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-1396">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-1396">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1398">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-1398">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-1399">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1399">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1400">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1400">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1401">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1401">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1402">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-1402">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-1403">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-1403">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-1404">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-1404">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1406">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-1406">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-1407">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-1407">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1408">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-1408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1409">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-1409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-1410">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-1410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-1411">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1412">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1413">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1413">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-1414">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-1414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-1415">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-1416">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-1416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-1417">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-1418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-1418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-1419">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-1420">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1421">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1422">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1422">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1424">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-1424">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1425">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1425">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1426">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-1426">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-1427">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1427">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-1428">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1428">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-1429">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-1429">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-1430">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-1430">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1432">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1432">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-1433">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1433">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-1434">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1434">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-1435">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-1435">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-1436">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1436">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfcssup-20"></a><span data-ttu-id="ad36b-1437">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FCS</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1437">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FCS</sup> (20)</span></span>
| <span data-ttu-id="ad36b-1438">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-1438">Target</span></span> | <span data-ttu-id="ad36b-1439">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1439">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-1440">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1440">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-1441">64</span><span class="sxs-lookup"><span data-stu-id="ad36b-1441">64</span></span> |
| <span data-ttu-id="ad36b-1442">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1442">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1444">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-1444">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1445">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1445">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1446">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1446">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1447">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1447">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1448">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1448">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1450">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1450">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1452">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1452">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-1453">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-1453">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1455">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-1455">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-1456">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1456">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1457">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1457">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1458">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1458">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1459">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-1459">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-1460">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-1460">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-1461">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-1461">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1463">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-1463">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-1464">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-1464">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1465">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-1465">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1466">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-1466">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-1467">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-1467">Depth/Stencil Target</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1469">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1469">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1470">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1470">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1471">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1471">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-1472">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-1472">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-1473">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1473">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-1474">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-1474">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-1475">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1475">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-1476">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-1476">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-1477">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1477">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-1478">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1478">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1479">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1479">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1480">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1480">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1482">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-1482">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1484">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1484">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1486">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-1486">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1488">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1488">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-1489">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1489">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-1490">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-1490">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-1491">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-1491">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1493">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1493">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-1494">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1494">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-1495">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1495">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-1496">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-1496">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-1497">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1497">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfcssup-21"></a><span data-ttu-id="ad36b-1498">DXGI_FORMAT_R32 \_ \_ X8X24 Float \_ sin tipo,<sup>FCS</sup> (21)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1498">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FCS</sup> (21)</span></span>
| <span data-ttu-id="ad36b-1499">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-1499">Target</span></span> | <span data-ttu-id="ad36b-1500">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1500">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-1501">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1501">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-1502">64</span><span class="sxs-lookup"><span data-stu-id="ad36b-1502">64</span></span> |
| <span data-ttu-id="ad36b-1503">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1503">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1505">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-1505">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1506">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1506">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1507">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1507">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1508">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1508">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1509">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1509">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1511">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1511">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1513">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1513">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-1514">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-1514">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1516">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-1516">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1518">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1518">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1520">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1520">Shader sample\_c (comparison filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1522">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1522">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1523">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-1523">Shader gather4</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1525">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-1525">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-1526">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-1526">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1528">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-1528">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-1529">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-1529">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1530">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-1530">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1531">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-1531">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-1532">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-1532">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-1533">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1533">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1534">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1534">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1535">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1535">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-1536">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-1536">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-1537">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1537">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-1538">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-1538">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-1539">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1539">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-1540">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-1540">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-1541">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1541">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-1542">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1542">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1543">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1543">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1544">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1544">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1546">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-1546">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1547">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1547">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1548">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-1548">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-1549">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1549">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-1550">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1550">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1552">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-1552">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-1553">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-1553">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1555">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1555">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-1556">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1556">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-1557">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1557">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-1558">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-1558">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-1559">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1559">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfcssup-22"></a><span data-ttu-id="ad36b-1560">DXGI_FORMAT_X32 \_ \_ G8X24 \_ uint<sup>FC FCS</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1560">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FCS</sup> (22)</span></span>
| <span data-ttu-id="ad36b-1561">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-1561">Target</span></span> | <span data-ttu-id="ad36b-1562">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1562">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-1563">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1563">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-1564">64</span><span class="sxs-lookup"><span data-stu-id="ad36b-1564">64</span></span> |
| <span data-ttu-id="ad36b-1565">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1565">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1567">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-1567">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1568">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1568">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1569">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1569">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1570">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1570">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1571">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1571">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1573">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1573">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1575">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1575">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-1576">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-1576">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1578">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-1578">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1580">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1580">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1581">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1581">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1582">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1582">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1583">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-1583">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-1584">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-1584">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-1585">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-1585">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1587">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-1587">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-1588">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-1588">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1589">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-1589">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1590">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-1590">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-1591">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-1591">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-1592">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1592">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1593">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1593">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1594">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1594">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-1595">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-1595">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-1596">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1596">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-1597">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-1597">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-1598">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1598">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-1599">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-1599">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-1600">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1600">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-1601">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1601">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1602">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1602">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1603">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1603">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1605">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-1605">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1606">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1606">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1607">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-1607">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-1608">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1608">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-1609">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1609">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1611">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-1611">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-1612">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-1612">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1614">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1614">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-1615">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1615">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-1616">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1616">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-1617">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-1617">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-1618">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1618">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="ad36b-1619">DXGI_FORMAT_R10G10B10A2 de \_ <sup>equipos</sup> sin tipo (23)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1619">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="ad36b-1620">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-1620">Target</span></span> | <span data-ttu-id="ad36b-1621">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1621">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-1622">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1622">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-1623">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-1623">32</span></span> |
| <span data-ttu-id="ad36b-1624">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1624">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1626">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-1626">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1627">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1627">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1628">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1628">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1629">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1629">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1630">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1630">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1632">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1632">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1634">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1634">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1636">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-1636">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1638">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-1638">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-1639">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1639">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1640">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1640">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1641">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1641">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1642">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-1642">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-1643">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-1643">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-1644">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-1644">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1646">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-1646">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-1647">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-1647">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1648">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-1648">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1649">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-1649">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-1650">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-1650">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-1651">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1651">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1652">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1652">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1653">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1653">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-1654">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-1654">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-1655">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1655">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-1656">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-1656">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-1657">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1657">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-1658">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-1658">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-1659">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1659">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-1660">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1660">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1661">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1661">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1662">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1662">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1664">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-1664">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1665">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1665">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1666">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-1666">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-1667">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1667">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-1668">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1668">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-1669">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-1669">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-1670">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-1670">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1672">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1672">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-1673">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1673">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-1674">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1674">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-1675">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-1675">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1677">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1677">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="ad36b-1678">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FCS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1678">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="ad36b-1679">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-1679">Target</span></span> | <span data-ttu-id="ad36b-1680">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1680">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-1681">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1681">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-1682">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-1682">32</span></span> |
| <span data-ttu-id="ad36b-1683">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1683">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1685">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-1685">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1687">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1687">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1689">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1689">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1690">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1690">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1691">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1691">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1693">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1693">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1695">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1695">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1697">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-1697">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1699">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-1699">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1701">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1701">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1703">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1703">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1704">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1704">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1705">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-1705">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-1706">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-1706">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-1707">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-1707">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1709">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-1709">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1711">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-1711">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1713">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-1713">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1715">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-1715">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-1716">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-1716">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-1717">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1717">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1718">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1718">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1719">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1719">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-1720">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-1720">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-1721">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1721">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-1722">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-1722">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-1723">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1723">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-1724">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-1724">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-1725">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1725">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-1726">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1726">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1727">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1727">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1728">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1728">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1730">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-1730">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1732">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1732">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1734">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-1734">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1736">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1736">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1738">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1738">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1740">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-1740">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1742">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-1742">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1744">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1744">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-1745">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1745">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1747">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1747">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1749">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-1749">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1751">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1751">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="ad36b-1752">DXGI_FORMAT_R10G10B10A2 \_ uint<sup>FCS</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1752">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="ad36b-1753">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-1753">Target</span></span> | <span data-ttu-id="ad36b-1754">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1754">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-1755">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1755">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-1756">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-1756">32</span></span> |
| <span data-ttu-id="ad36b-1757">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1757">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1759">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-1759">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1761">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1761">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1763">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1763">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1764">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1764">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1765">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1765">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1767">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1767">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1769">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1769">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1771">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-1771">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1773">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-1773">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1775">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1775">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1776">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1776">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1777">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1777">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1778">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-1778">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-1779">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-1779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-1780">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-1780">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1782">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-1782">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-1783">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-1783">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1785">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-1785">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1786">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-1786">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1788">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-1788">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-1789">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1789">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1790">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1790">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1791">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1791">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-1792">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-1792">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-1793">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1793">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-1794">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-1794">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-1795">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1795">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-1796">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-1796">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-1797">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1797">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-1798">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1798">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1799">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1799">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1800">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1800">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1802">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-1802">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1804">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1804">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1806">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-1806">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1808">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1808">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-1809">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1809">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1811">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-1811">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-1812">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-1812">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1814">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1814">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-1815">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1815">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-1816">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1816">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-1817">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-1817">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1819">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1819">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="ad36b-1820">DXGI_FORMAT_R10G10B10 \_ la \_ inclinación de XR \_ a2 \_ UNORM<sup>FCS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1820">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="ad36b-1821">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-1821">Target</span></span> | <span data-ttu-id="ad36b-1822">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1822">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-1823">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1823">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-1824">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-1824">32</span></span> |
| <span data-ttu-id="ad36b-1825">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1825">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1827">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-1827">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1828">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1828">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1829">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1829">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1830">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1830">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1831">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1831">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-1832">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1832">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1834">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1834">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-1835">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-1835">TextureCube</span></span> | \- |
| <span data-ttu-id="ad36b-1836">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-1836">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-1837">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1837">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1838">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1838">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1839">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1839">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1840">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-1840">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-1841">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-1841">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-1842">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-1842">Mipmap</span></span> | \- |
| <span data-ttu-id="ad36b-1843">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-1843">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-1844">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-1844">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1845">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-1845">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1846">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-1846">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-1847">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-1847">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-1848">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1848">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1849">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1849">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1850">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1850">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-1851">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-1851">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-1852">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1852">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-1853">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-1853">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-1854">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1854">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-1855">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-1855">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-1856">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1856">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-1857">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1857">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1858">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1858">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1859">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1859">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1861">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-1861">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1862">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1862">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1863">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-1863">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-1864">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1864">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-1865">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1865">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-1866">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-1866">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1868">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-1868">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1870">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1870">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-1871">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1871">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1873">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1873">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1875">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-1875">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1877">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1877">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="ad36b-1878">DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1878">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="ad36b-1879">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-1879">Target</span></span> | <span data-ttu-id="ad36b-1880">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1880">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-1881">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1881">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-1882">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-1882">32</span></span> |
| <span data-ttu-id="ad36b-1883">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1883">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1885">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-1885">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1887">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1887">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1889">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1889">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1890">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1890">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1891">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1891">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1893">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1893">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1895">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1895">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1897">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-1897">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1899">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-1899">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1901">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1901">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1903">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1903">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1904">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1904">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1905">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-1905">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-1906">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-1906">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-1907">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-1907">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1909">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-1909">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1911">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-1911">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1913">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-1913">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1915">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-1915">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-1916">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-1916">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-1917">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1917">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1918">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1918">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1919">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1919">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-1920">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-1920">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-1921">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1921">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-1922">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-1922">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-1923">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1923">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-1924">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-1924">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-1925">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1925">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-1926">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1926">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1927">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1927">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1928">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1928">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1930">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-1930">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1932">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1932">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1934">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-1934">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-1936">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1936">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1938">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1938">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1940">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-1940">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-1941">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-1941">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-1942">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1942">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-1943">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1943">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-1944">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1944">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-1945">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-1945">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-1946">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="ad36b-1947">DXGI_FORMAT_R8G8B8A8 de \_ <sup>equipos</sup> sin tipo (27)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1947">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="ad36b-1948">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-1948">Target</span></span> | <span data-ttu-id="ad36b-1949">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-1949">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-1950">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-1951">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-1951">32</span></span> |
| <span data-ttu-id="ad36b-1952">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1952">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1954">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-1954">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1955">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1955">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1956">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1956">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1957">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1957">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-1958">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1958">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1960">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1960">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1962">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-1962">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1964">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-1964">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1966">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-1966">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-1967">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1967">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1968">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1968">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1969">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-1969">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-1970">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-1970">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-1971">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-1971">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-1972">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-1972">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1974">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-1974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-1975">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-1975">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1976">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-1976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1977">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-1977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-1978">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-1978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-1979">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-1979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1980">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-1981">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1981">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-1982">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-1982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-1983">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-1984">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-1984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-1985">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-1986">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-1986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-1987">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-1987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-1988">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1989">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-1989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-1990">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-1990">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-1992">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-1992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1993">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-1994">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-1994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-1995">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-1995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-1996">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-1996">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-1997">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-1997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-1998">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-1998">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2000">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2000">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-2001">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2001">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-2002">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-2003">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-2003">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2005">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2005">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="ad36b-2006">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FCS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2006">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="ad36b-2007">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-2007">Target</span></span> | <span data-ttu-id="ad36b-2008">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2008">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-2009">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2009">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-2010">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-2010">32</span></span> |
| <span data-ttu-id="ad36b-2011">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2011">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2013">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-2013">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2015">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2015">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2017">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2017">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2018">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2018">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2019">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2019">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2021">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2023">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-2025">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2027">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-2027">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2029">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2029">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2031">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2032">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2033">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-2033">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-2034">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-2034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-2035">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-2035">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2037">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-2037">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2039">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-2039">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2041">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-2041">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2043">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-2043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-2044">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-2044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-2045">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2046">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2047">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2047">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-2048">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-2048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-2049">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-2050">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-2050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-2051">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-2052">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-2052">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-2053">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-2054">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2055">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2056">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2056">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2058">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-2058">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2060">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2060">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2062">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-2062">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2064">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2064">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2066">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2066">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2068">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-2068">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2070">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-2070">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2072">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2072">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-2073">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2073">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2075">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2075">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2077">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-2077">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2079">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2079">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="ad36b-2080">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRGB<sup>FCS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2080">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="ad36b-2081">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-2081">Target</span></span> | <span data-ttu-id="ad36b-2082">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2082">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-2083">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2083">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-2084">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-2084">32</span></span> |
| <span data-ttu-id="ad36b-2085">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2085">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2087">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-2087">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2088">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2088">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2089">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2089">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2090">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2090">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2091">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2091">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2093">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2093">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2095">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2095">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2097">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-2097">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2099">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-2099">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2101">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2101">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2103">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2103">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2104">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2104">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2105">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-2105">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-2106">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-2106">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-2107">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-2107">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2109">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-2109">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2111">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-2111">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2113">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-2113">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2115">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-2115">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-2116">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-2116">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-2117">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2117">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2118">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2118">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2119">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2119">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-2120">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-2120">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-2121">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2121">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-2122">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-2122">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-2123">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2123">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-2124">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-2124">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-2125">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2125">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-2126">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2126">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2127">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2127">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2128">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2128">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2130">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-2130">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2132">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2132">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2134">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-2134">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2136">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2136">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2138">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2138">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2140">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-2140">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2142">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-2142">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2144">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2144">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-2145">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2145">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2147">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2147">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2149">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-2149">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2151">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2151">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="ad36b-2152">DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FCS</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2152">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="ad36b-2153">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-2153">Target</span></span> | <span data-ttu-id="ad36b-2154">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2154">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-2155">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2155">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-2156">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-2156">32</span></span> |
| <span data-ttu-id="ad36b-2157">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2157">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2159">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-2159">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2161">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2161">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2163">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2163">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2164">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2164">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2165">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2165">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2167">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2167">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2169">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2169">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2171">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-2171">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2173">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-2173">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2175">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2175">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2176">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2176">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2177">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2177">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2178">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-2178">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-2179">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-2179">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-2180">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-2180">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2182">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-2182">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-2183">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-2183">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2185">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-2185">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-2186">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-2186">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2188">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-2188">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-2189">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2189">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2190">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2190">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2191">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2191">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-2192">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-2192">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-2193">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2193">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-2194">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-2194">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-2195">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2195">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-2196">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-2196">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-2197">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2197">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-2198">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2198">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2199">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2199">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2200">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2200">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2202">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-2202">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2204">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2204">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2206">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-2206">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2208">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2208">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-2209">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2209">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2211">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-2211">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-2212">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-2212">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2214">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2214">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-2215">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2215">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-2216">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2216">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-2217">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-2217">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2219">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2219">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="ad36b-2220">DXGI_FORMAT_R8G8B8A8 \_ SNORM<sup>FCS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2220">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="ad36b-2221">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-2221">Target</span></span> | <span data-ttu-id="ad36b-2222">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2222">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-2223">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2223">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-2224">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-2224">32</span></span> |
| <span data-ttu-id="ad36b-2225">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2225">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2227">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-2227">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2229">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2229">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2231">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2232">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2233">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2235">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2235">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2237">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2237">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-2239">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2241">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-2241">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2243">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2243">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2245">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2245">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2246">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2246">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2247">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-2247">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-2248">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-2248">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-2249">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-2249">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2251">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-2251">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2253">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-2253">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2255">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-2255">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2257">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-2257">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-2258">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-2258">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-2259">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2259">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2260">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2260">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2261">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2261">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-2262">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-2262">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-2263">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2263">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-2264">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-2264">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-2265">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2265">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-2266">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-2266">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-2267">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2267">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-2268">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2268">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2269">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2269">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2270">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2270">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2272">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-2272">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2274">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2274">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2276">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-2276">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2278">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2278">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2280">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2280">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2282">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-2282">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-2283">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-2283">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2285">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2285">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-2286">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2286">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-2287">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2287">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-2288">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-2288">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2290">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2290">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="ad36b-2291">DXGI_FORMAT_R8G8B8A8 \_ San<sup>FCS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2291">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="ad36b-2292">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-2292">Target</span></span> | <span data-ttu-id="ad36b-2293">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2293">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-2294">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2294">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-2295">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-2295">32</span></span> |
| <span data-ttu-id="ad36b-2296">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2296">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2298">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-2298">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2300">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2300">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2302">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2302">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2303">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2303">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2304">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2304">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2306">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2306">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2308">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2308">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2310">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-2310">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2312">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-2312">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2314">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2314">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2315">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2315">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2316">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2316">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2317">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-2317">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-2318">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-2318">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-2319">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-2319">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2321">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-2321">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-2322">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-2322">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2324">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-2324">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-2325">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-2325">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-2326">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-2326">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-2327">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2327">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2328">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2328">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2329">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2329">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-2330">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-2330">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-2331">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2331">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-2332">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-2332">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-2333">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2333">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-2334">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-2334">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-2335">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2335">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-2336">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2336">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2337">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2337">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2338">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2338">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2340">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-2340">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2342">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2342">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2344">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-2344">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2346">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2346">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-2347">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2347">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2349">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-2349">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-2350">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-2350">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2352">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2352">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-2353">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2353">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-2354">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2354">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-2355">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-2355">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2357">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2357">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="ad36b-2358">DXGI_FORMAT_R16G16 de \_ <sup>equipos</sup> sin tipo (33)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2358">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="ad36b-2359">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-2359">Target</span></span> | <span data-ttu-id="ad36b-2360">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2360">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-2361">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2361">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-2362">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-2362">32</span></span> |
| <span data-ttu-id="ad36b-2363">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2363">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2365">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-2365">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2366">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2366">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2367">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2367">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2368">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2368">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2369">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2369">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2371">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2371">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2373">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2373">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2375">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-2375">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2377">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-2377">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-2378">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2378">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2379">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2379">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2380">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2380">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2381">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-2381">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-2382">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-2382">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-2383">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-2383">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2385">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-2385">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-2386">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-2386">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-2387">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-2387">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-2388">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-2388">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-2389">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-2389">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-2390">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2390">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2391">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2391">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2392">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2392">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-2393">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-2393">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-2394">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2394">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-2395">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-2395">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-2396">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2396">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-2397">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-2397">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-2398">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2398">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-2399">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2399">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2400">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2400">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2401">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2401">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2403">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-2403">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-2404">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2404">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-2405">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-2405">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-2406">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2406">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-2407">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2407">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-2408">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-2408">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-2409">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-2409">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2411">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2411">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-2412">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2412">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-2413">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2413">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-2414">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-2414">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-2415">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2415">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="ad36b-2416">DXGI_FORMAT_R16G16 \_ float<sup>FCS</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2416">DXGI_FORMAT_R16G16\_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="ad36b-2417">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-2417">Target</span></span> | <span data-ttu-id="ad36b-2418">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2418">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-2419">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2419">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-2420">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-2420">32</span></span> |
| <span data-ttu-id="ad36b-2421">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2421">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2423">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-2423">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2425">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2425">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2427">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2427">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2428">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2428">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2429">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2429">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2431">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2431">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2433">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2433">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2435">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-2435">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2437">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-2437">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2439">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2439">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2441">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2442">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2443">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-2443">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-2444">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-2444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-2445">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-2445">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2447">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-2447">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2449">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-2449">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2451">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-2451">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2453">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-2453">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-2454">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-2454">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-2455">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2455">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2456">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2456">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2457">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2457">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-2458">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-2458">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-2459">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2459">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-2460">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-2460">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-2461">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2461">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-2462">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-2462">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-2463">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2463">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-2464">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2464">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2465">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2465">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2466">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2466">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2468">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-2468">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2470">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2470">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2472">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-2472">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2474">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2474">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2476">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2476">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2478">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-2478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-2479">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-2479">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2481">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-2482">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-2483">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-2484">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-2484">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-2485">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2485">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="ad36b-2486">DXGI_FORMAT_R16G16 \_ UNORM<sup>FCS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2486">DXGI_FORMAT_R16G16\_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="ad36b-2487">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-2487">Target</span></span> | <span data-ttu-id="ad36b-2488">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2488">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-2489">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2489">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-2490">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-2490">32</span></span> |
| <span data-ttu-id="ad36b-2491">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2491">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2493">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-2493">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2495">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2495">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2497">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2497">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2498">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2498">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2499">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2499">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2501">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2503">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2503">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-2505">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2507">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-2507">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2509">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2509">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2511">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2511">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2512">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2512">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2513">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-2513">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-2514">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-2514">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-2515">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-2515">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2517">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-2517">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2519">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-2519">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2521">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-2521">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2523">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-2523">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-2524">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-2524">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-2525">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2525">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2526">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2526">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2527">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2527">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-2528">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-2528">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-2529">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2529">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-2530">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-2530">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-2531">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2531">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-2532">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-2532">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-2533">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2533">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-2534">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2534">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2535">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2535">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2536">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2536">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2538">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-2538">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2540">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2540">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2542">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-2542">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2544">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2544">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2546">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2546">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2548">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-2548">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-2549">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-2549">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2551">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2551">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-2552">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2552">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-2553">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2553">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-2554">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-2554">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-2555">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2555">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="ad36b-2556">DXGI_FORMAT_R16G16 \_ uint<sup>FCS</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2556">DXGI_FORMAT_R16G16\_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="ad36b-2557">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-2557">Target</span></span> | <span data-ttu-id="ad36b-2558">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2558">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-2559">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2559">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-2560">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-2560">32</span></span> |
| <span data-ttu-id="ad36b-2561">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2561">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2563">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-2563">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2565">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2565">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2567">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2567">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2568">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2568">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2569">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2569">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2571">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2571">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2573">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2573">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2575">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-2575">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2577">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-2577">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2579">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2579">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2580">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2580">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2581">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2581">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2582">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-2582">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-2583">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-2583">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-2584">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-2584">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2586">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-2586">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-2587">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-2587">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2589">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-2589">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-2590">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-2590">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2592">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-2592">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-2593">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2593">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2594">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2594">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2595">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2595">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-2596">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-2596">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-2597">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2597">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-2598">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-2598">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-2599">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2599">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-2600">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-2600">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-2601">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2601">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-2602">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2602">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2603">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2603">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2604">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2604">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2606">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-2606">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2608">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2608">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2610">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-2610">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2612">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2612">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-2613">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2613">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2615">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-2615">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-2616">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-2616">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2618">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2618">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-2619">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2619">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-2620">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2620">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-2621">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-2621">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-2622">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2622">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="ad36b-2623">DXGI_FORMAT_R16G16 \_ SNORM<sup>FCS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2623">DXGI_FORMAT_R16G16\_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="ad36b-2624">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-2624">Target</span></span> | <span data-ttu-id="ad36b-2625">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2625">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-2626">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2626">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-2627">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-2627">32</span></span> |
| <span data-ttu-id="ad36b-2628">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2628">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2630">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-2630">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2632">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2632">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2634">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2634">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2635">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2635">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2636">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2636">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2638">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2638">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2640">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2640">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2642">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-2642">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2644">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-2644">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2646">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2646">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2648">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2648">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2649">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2649">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2650">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-2650">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-2651">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-2651">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-2652">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-2652">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2654">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-2654">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2656">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-2656">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2658">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-2658">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2660">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-2660">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-2661">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-2661">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-2662">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2662">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2663">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2663">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2664">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2664">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-2665">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-2665">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-2666">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2666">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-2667">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-2667">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-2668">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2668">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-2669">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-2669">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-2670">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2670">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-2671">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2671">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2672">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2672">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2673">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2673">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2675">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-2675">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2677">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2677">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2679">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-2679">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2681">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2681">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2683">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2683">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2685">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-2685">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-2686">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-2686">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2688">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2688">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-2689">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2689">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-2690">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2690">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-2691">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-2691">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-2692">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2692">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="ad36b-2693">DXGI_FORMAT_R16G16 \_ San<sup>FCS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2693">DXGI_FORMAT_R16G16\_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="ad36b-2694">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-2694">Target</span></span> | <span data-ttu-id="ad36b-2695">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2695">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-2696">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2696">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-2697">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-2697">32</span></span> |
| <span data-ttu-id="ad36b-2698">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2698">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2700">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-2700">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2702">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2702">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2704">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2704">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2705">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2705">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2706">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2706">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2708">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2708">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2710">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2710">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2712">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-2712">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2714">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-2714">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2716">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2716">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2717">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2717">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2718">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2718">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2719">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-2719">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-2720">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-2720">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-2721">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-2721">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2723">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-2723">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-2724">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-2724">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2726">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-2726">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-2727">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-2727">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-2728">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-2728">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-2729">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2729">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2730">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2730">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2731">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2731">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-2732">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-2732">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-2733">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2733">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-2734">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-2734">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-2735">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2735">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-2736">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-2736">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-2737">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2737">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-2738">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2738">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2739">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2739">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2740">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2740">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2742">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-2742">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2744">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2744">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2746">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-2746">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2748">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2748">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-2749">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2749">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2751">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-2751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-2752">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-2752">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2754">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2754">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-2755">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2755">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-2756">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-2757">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-2757">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-2758">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2758">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="ad36b-2759">DXGI_FORMAT_R32 de \_ <sup>equipos</sup> sin tipo (39)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2759">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="ad36b-2760">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-2760">Target</span></span> | <span data-ttu-id="ad36b-2761">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2761">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-2762">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-2763">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-2763">32</span></span> |
| <span data-ttu-id="ad36b-2764">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2764">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2766">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-2766">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2767">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2767">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2768">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2768">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2769">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2769">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2770">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2770">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2772">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2772">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2774">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2776">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-2776">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2778">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-2778">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-2779">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2779">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2780">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2780">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2781">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2781">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2782">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-2782">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-2783">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-2783">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-2784">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-2784">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2786">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-2786">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-2787">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-2787">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-2788">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-2788">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-2789">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-2789">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-2790">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-2790">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-2791">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2791">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2792">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2792">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2793">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2793">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-2794">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-2794">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-2795">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2795">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-2796">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-2796">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-2797">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2797">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-2798">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-2798">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-2799">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2799">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-2800">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2800">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2801">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2801">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2802">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2802">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2804">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-2804">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-2805">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2805">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-2806">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-2806">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-2807">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2807">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-2808">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2808">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-2809">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-2809">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-2810">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-2810">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2812">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2812">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-2813">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2813">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-2814">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2814">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-2815">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-2815">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2817">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2817">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="ad36b-2818">DXGI_FORMAT_D32 \_ float<sup>FCS</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2818">DXGI_FORMAT_D32\_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="ad36b-2819">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-2819">Target</span></span> | <span data-ttu-id="ad36b-2820">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2820">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-2821">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2821">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-2822">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-2822">32</span></span> |
| <span data-ttu-id="ad36b-2823">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2823">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2825">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-2825">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2826">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2826">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2827">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2827">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2828">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2828">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2829">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2829">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2831">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2831">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2833">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2833">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-2834">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-2834">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2836">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-2836">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-2837">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2837">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2838">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2838">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2839">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2839">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2840">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-2840">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-2841">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-2841">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-2842">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-2842">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2844">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-2844">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-2845">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-2845">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-2846">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-2846">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-2847">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-2847">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-2848">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-2848">Depth/Stencil Target</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2850">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2850">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2851">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2851">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2852">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2852">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-2853">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-2853">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-2854">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2854">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-2855">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-2855">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-2856">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2856">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-2857">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-2857">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-2858">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2858">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-2859">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2859">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2860">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2860">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2861">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2861">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2863">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-2863">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2865">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2865">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2867">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-2867">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2869">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2869">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-2870">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2870">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-2871">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-2871">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-2872">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-2872">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2874">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2874">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-2875">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2875">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-2876">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2876">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-2877">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-2877">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2879">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2879">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="ad36b-2880">DXGI_FORMAT_R32 \_ float<sup>FCS</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2880">DXGI_FORMAT_R32\_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="ad36b-2881">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-2881">Target</span></span> | <span data-ttu-id="ad36b-2882">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2882">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-2883">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2883">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-2884">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-2884">32</span></span> |
| <span data-ttu-id="ad36b-2885">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2885">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2887">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-2887">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2889">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2889">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2891">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2891">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-2892">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2892">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2894">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2894">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2896">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2896">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2898">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2898">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2900">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-2900">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2902">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-2902">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2904">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2904">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2906">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2906">Shader sample\_c (comparison filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2908">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2908">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2909">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-2909">Shader gather4</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2911">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-2911">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-2912">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-2912">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2914">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-2914">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2916">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-2916">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2918">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-2918">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2920">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-2920">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-2921">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-2921">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-2922">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2922">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2923">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2923">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2924">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2924">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-2925">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-2925">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-2926">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2926">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-2927">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-2927">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-2928">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2928">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-2929">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-2929">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-2930">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2930">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-2931">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2931">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2932">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-2932">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-2933">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2933">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2935">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-2935">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2937">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2937">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2939">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-2939">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2941">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2941">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2943">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-2943">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2945">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-2945">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-2946">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-2946">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2948">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2948">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-2949">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2949">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-2950">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2950">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-2951">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-2951">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2953">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2953">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="ad36b-2954">DXGI_FORMAT_R32 \_ uint<sup>FCS</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2954">DXGI_FORMAT_R32\_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="ad36b-2955">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-2955">Target</span></span> | <span data-ttu-id="ad36b-2956">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-2956">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-2957">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2957">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-2958">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-2958">32</span></span> |
| <span data-ttu-id="ad36b-2959">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2959">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2961">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-2961">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2963">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2963">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2965">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-2965">Input Assembler Index Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2967">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2967">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2969">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2969">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2971">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2971">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2973">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-2973">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2975">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-2975">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2977">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-2977">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2979">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2979">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2980">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2980">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2981">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-2981">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-2982">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-2982">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-2983">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-2983">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-2984">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-2984">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2986">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-2986">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-2987">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-2987">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-2989">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-2989">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-2990">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-2990">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-2992">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-2992">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-2993">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-2993">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2994">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2994">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-2995">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-2995">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-2996">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-2996">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-2997">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2997">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-2998">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-2998">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-2999">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-2999">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-3000">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-3000">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-3001">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3001">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-3002">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3002">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3003">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3003">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3004">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3004">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3006">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-3006">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3008">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3008">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3010">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-3010">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3012">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3012">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-3013">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3013">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3015">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-3015">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-3016">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-3016">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3018">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3018">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-3019">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3019">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-3020">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3020">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-3021">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-3021">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3023">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3023">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="ad36b-3024">DXGI_FORMAT_R32 \_ San<sup>FCS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3024">DXGI_FORMAT_R32\_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="ad36b-3025">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-3025">Target</span></span> | <span data-ttu-id="ad36b-3026">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3026">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-3027">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3027">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-3028">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-3028">32</span></span> |
| <span data-ttu-id="ad36b-3029">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3029">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3031">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-3031">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3033">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3033">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3035">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3035">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3036">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3036">Stream Output Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3038">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3038">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3040">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3040">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3042">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3042">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3044">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-3044">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3046">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-3046">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3048">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3048">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3049">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3049">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3050">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3050">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3051">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-3051">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-3052">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-3052">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-3053">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-3053">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3055">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-3055">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-3056">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-3056">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3058">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-3058">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3059">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-3059">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-3060">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-3060">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-3061">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3061">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3062">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3062">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3063">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3063">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-3064">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-3064">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-3065">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3065">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-3066">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-3066">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-3067">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3067">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-3068">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-3068">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-3069">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3069">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-3070">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3070">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3071">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3071">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3072">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3072">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3074">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-3074">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3076">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3076">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3078">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-3078">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3080">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-3081">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3081">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3083">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-3083">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-3084">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-3084">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3086">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3086">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-3087">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3087">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-3088">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3088">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-3089">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-3089">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3091">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3091">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="ad36b-3092">DXGI_FORMAT_R24G8 de \_ <sup>equipos</sup> sin tipo (44)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3092">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="ad36b-3093">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-3093">Target</span></span> | <span data-ttu-id="ad36b-3094">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3094">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-3095">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3095">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-3096">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-3096">32</span></span> |
| <span data-ttu-id="ad36b-3097">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3097">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3099">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-3099">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3100">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3100">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3101">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3101">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3102">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3102">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3103">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3103">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3105">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3105">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3107">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3107">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-3108">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-3108">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3110">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-3110">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-3111">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3111">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3112">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3112">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3113">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3113">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3114">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-3114">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-3115">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-3115">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-3116">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-3116">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3118">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-3118">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-3119">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-3119">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3120">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-3120">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3121">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-3121">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-3122">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-3122">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-3123">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3123">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3124">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3124">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3125">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3125">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-3126">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-3126">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-3127">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3127">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-3128">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-3128">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-3129">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3129">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-3130">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-3130">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-3131">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3131">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-3132">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3132">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3133">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3133">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3134">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3134">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3136">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-3136">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3137">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3137">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3138">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-3138">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-3139">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3139">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-3140">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3140">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-3141">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-3141">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-3142">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-3142">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3144">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3144">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-3145">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3145">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-3146">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3146">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-3147">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-3147">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-3148">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3148">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfcssup-45"></a><span data-ttu-id="ad36b-3149">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FCS</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3149">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FCS</sup> (45)</span></span>
| <span data-ttu-id="ad36b-3150">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-3150">Target</span></span> | <span data-ttu-id="ad36b-3151">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3151">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-3152">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3152">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-3153">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-3153">32</span></span> |
| <span data-ttu-id="ad36b-3154">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3154">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3156">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-3156">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3157">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3157">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3158">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3158">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3159">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3159">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3160">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3160">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3162">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3162">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3164">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3164">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-3165">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-3165">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3167">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-3167">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-3168">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3168">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3169">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3169">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3170">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3170">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3171">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-3171">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-3172">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-3172">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-3173">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-3173">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3175">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-3175">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-3176">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-3176">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3177">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-3177">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3178">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-3178">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-3179">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-3179">Depth/Stencil Target</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3181">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3181">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3182">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3182">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3183">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3183">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-3184">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-3184">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-3185">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3185">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-3186">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-3186">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-3187">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3187">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-3188">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-3188">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-3189">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3189">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-3190">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3190">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3191">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3191">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3192">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3192">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3194">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-3194">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3196">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3196">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3198">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-3198">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3200">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3200">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-3201">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3201">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-3202">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-3202">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-3203">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-3203">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3205">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3205">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-3206">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3206">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-3207">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3207">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-3208">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-3208">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-3209">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3209">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfcssup-46"></a><span data-ttu-id="ad36b-3210">DXGI_FORMAT_R24 \_ UNORM \_ X8 \_ sin tipo de<sup>FCS</sup> (46)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3210">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FCS</sup> (46)</span></span>
| <span data-ttu-id="ad36b-3211">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-3211">Target</span></span> | <span data-ttu-id="ad36b-3212">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3212">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-3213">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3213">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-3214">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-3214">32</span></span> |
| <span data-ttu-id="ad36b-3215">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3215">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3217">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-3217">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3218">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3218">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3219">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3219">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3220">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3220">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3221">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3221">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3223">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3223">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3225">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3225">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-3226">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-3226">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3228">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-3228">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3230">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3230">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3232">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3232">Shader sample\_c (comparison filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3234">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3234">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3235">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-3235">Shader gather4</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3237">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-3237">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-3238">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-3238">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3240">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-3240">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-3241">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-3241">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3242">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-3242">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3243">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-3243">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-3244">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-3244">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-3245">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3245">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3246">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3246">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3247">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3247">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-3248">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-3248">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-3249">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3249">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-3250">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-3250">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-3251">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3251">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-3252">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-3252">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-3253">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3253">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-3254">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3254">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3255">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3255">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3256">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3256">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3258">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-3258">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3259">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3259">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3260">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-3260">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-3261">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3261">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-3262">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3262">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3264">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-3264">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-3265">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-3265">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3267">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3267">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-3268">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3268">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-3269">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3269">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-3270">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-3270">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-3271">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3271">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfcssup-47"></a><span data-ttu-id="ad36b-3272">DXGI_FORMAT_X24 de \_ G8 no typeless \_ \_ (47)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="ad36b-3272">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FCS</sup> (47)</span></span>
| <span data-ttu-id="ad36b-3273">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-3273">Target</span></span> | <span data-ttu-id="ad36b-3274">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3274">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-3275">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3275">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-3276">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-3276">32</span></span> |
| <span data-ttu-id="ad36b-3277">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3277">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3279">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-3279">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3280">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3281">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3282">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3283">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3285">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3285">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3287">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3287">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-3288">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-3288">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3290">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-3290">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3292">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3292">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3293">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3293">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3294">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3294">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3295">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-3295">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-3296">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-3296">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-3297">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-3297">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3299">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-3299">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-3300">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-3300">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3301">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-3301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3302">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-3302">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-3303">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-3303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-3304">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3305">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3306">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3306">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-3307">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-3307">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-3308">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3308">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-3309">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-3309">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-3310">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3310">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-3311">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-3311">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-3312">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3312">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-3313">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3313">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3314">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3314">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3315">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3315">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3317">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-3317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3318">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3319">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-3319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-3320">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-3321">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3321">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3323">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-3323">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-3324">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-3324">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3326">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3326">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-3327">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3327">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-3328">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3328">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-3329">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-3329">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-3330">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3330">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="ad36b-3331">DXGI_FORMAT_R8G8 de \_ <sup>equipos</sup> sin tipo (48)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3331">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="ad36b-3332">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-3332">Target</span></span> | <span data-ttu-id="ad36b-3333">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3333">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-3334">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3334">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-3335">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-3335">16</span></span> |
| <span data-ttu-id="ad36b-3336">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3336">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3338">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-3338">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3339">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3339">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3340">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3340">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3341">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3341">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3342">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3342">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3344">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3344">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3346">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3346">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-3348">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3350">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-3350">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-3351">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3351">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3352">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3352">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3353">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3353">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3354">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-3354">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-3355">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-3355">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-3356">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-3356">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3358">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-3358">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-3359">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-3359">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3360">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-3360">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3361">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-3361">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-3362">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-3362">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-3363">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3363">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3364">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3364">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3365">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3365">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-3366">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-3366">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-3367">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3367">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-3368">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-3368">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-3369">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3369">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-3370">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-3370">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-3371">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3371">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-3372">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3372">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3373">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3373">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3374">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3374">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3376">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-3376">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3377">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3377">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3378">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-3378">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-3379">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3379">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-3380">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3380">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-3381">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-3381">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-3382">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-3382">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3384">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-3385">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-3386">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-3387">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-3387">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-3388">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3388">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="ad36b-3389">DXGI_FORMAT_R8G8 \_ UNORM<sup>FCS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3389">DXGI_FORMAT_R8G8\_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="ad36b-3390">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-3390">Target</span></span> | <span data-ttu-id="ad36b-3391">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3391">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-3392">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3392">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-3393">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-3393">16</span></span> |
| <span data-ttu-id="ad36b-3394">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3394">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3396">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-3396">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3398">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3398">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3400">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3400">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3401">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3401">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3402">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3402">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3404">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3406">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3406">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3408">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-3408">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3410">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-3410">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3412">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3412">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3414">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3415">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3416">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-3416">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-3417">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-3417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-3418">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-3418">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3420">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-3420">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-3422">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3424">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-3424">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3426">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-3426">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-3427">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-3427">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-3428">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3428">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3429">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3429">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3430">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3430">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-3431">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-3431">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-3432">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3432">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-3433">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-3433">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-3434">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3434">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-3435">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-3435">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-3436">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3436">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-3437">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3437">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3438">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3438">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3439">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3439">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3441">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-3441">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3443">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3443">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3445">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-3445">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3447">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3447">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3449">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3449">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3451">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-3451">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-3452">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-3452">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3454">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3454">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-3455">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3455">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-3456">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3456">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-3457">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-3457">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3459">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3459">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="ad36b-3460">DXGI_FORMAT_R8G8 \_ uint<sup>FCS</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3460">DXGI_FORMAT_R8G8\_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="ad36b-3461">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-3461">Target</span></span> | <span data-ttu-id="ad36b-3462">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3462">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-3463">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3463">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-3464">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-3464">16</span></span> |
| <span data-ttu-id="ad36b-3465">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3465">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3467">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-3467">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3469">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3469">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3471">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3471">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3472">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3472">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3473">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3473">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3475">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3475">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3477">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3477">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3479">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-3479">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3481">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-3481">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3483">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3483">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3484">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3484">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3485">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3485">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3486">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-3486">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-3487">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-3487">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-3488">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-3488">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3490">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-3490">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-3491">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-3491">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3493">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-3493">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3494">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-3494">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3496">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-3496">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-3497">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3497">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3498">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3498">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3499">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3499">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-3500">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-3500">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-3501">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3501">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-3502">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-3502">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-3503">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3503">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-3504">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-3504">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-3505">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3505">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-3506">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3506">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3507">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3507">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3508">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3508">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3510">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-3510">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3512">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3512">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3514">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-3514">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3516">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3516">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-3517">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3517">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3519">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-3519">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-3520">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-3520">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3522">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3522">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-3523">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3523">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-3524">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3524">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-3525">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-3525">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-3526">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3526">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="ad36b-3527">DXGI_FORMAT_R8G8 \_ SNORM<sup>FCS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3527">DXGI_FORMAT_R8G8\_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="ad36b-3528">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-3528">Target</span></span> | <span data-ttu-id="ad36b-3529">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3529">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-3530">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3530">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-3531">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-3531">16</span></span> |
| <span data-ttu-id="ad36b-3532">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3532">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3534">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-3534">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3536">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3536">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3538">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3538">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3539">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3539">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3540">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3540">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3542">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3542">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3544">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3544">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3546">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-3546">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3548">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-3548">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3550">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3550">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3552">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3552">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3553">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3553">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3554">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-3554">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-3555">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-3555">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-3556">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-3556">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3558">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-3558">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3560">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-3560">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3562">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-3562">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3564">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-3564">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-3565">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-3565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-3566">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3567">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3568">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3568">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-3569">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-3569">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-3570">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3570">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-3571">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-3571">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-3572">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3572">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-3573">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-3573">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-3574">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3574">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-3575">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3575">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3576">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3576">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3577">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3577">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3579">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-3579">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3581">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3581">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3583">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-3583">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3585">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3585">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3587">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3587">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3589">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-3589">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-3590">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-3590">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3592">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3592">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-3593">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3593">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-3594">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3594">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-3595">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-3595">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-3596">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3596">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="ad36b-3597">DXGI_FORMAT_R8G8 \_ San<sup>FCS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3597">DXGI_FORMAT_R8G8\_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="ad36b-3598">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-3598">Target</span></span> | <span data-ttu-id="ad36b-3599">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3599">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-3600">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3600">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-3601">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-3601">16</span></span> |
| <span data-ttu-id="ad36b-3602">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3602">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3604">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-3604">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3606">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3606">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3608">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3608">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3609">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3609">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3610">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3610">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3612">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3612">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3614">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3614">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3616">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-3616">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3618">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-3618">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3620">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3620">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3621">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3621">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3622">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3622">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3623">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-3623">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-3624">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-3624">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-3625">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-3625">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3627">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-3627">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-3628">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-3628">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3630">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-3630">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3631">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-3631">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-3632">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-3632">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-3633">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3633">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3634">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3634">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3635">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3635">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-3636">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-3636">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-3637">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3637">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-3638">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-3638">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-3639">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3639">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-3640">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-3640">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-3641">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3641">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-3642">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3642">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3643">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3643">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3644">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3644">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3646">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-3646">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3648">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3648">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3650">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-3650">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3652">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-3653">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3653">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3655">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-3655">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-3656">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-3656">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3658">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3658">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-3659">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3659">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-3660">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3660">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-3661">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-3661">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-3662">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3662">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="ad36b-3663">DXGI_FORMAT_R16 de \_ <sup>equipos</sup> sin tipo (53)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3663">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="ad36b-3664">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-3664">Target</span></span> | <span data-ttu-id="ad36b-3665">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3665">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-3666">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3666">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-3667">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-3667">16</span></span> |
| <span data-ttu-id="ad36b-3668">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3668">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3670">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-3670">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3671">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3671">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3672">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3672">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3673">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3673">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3674">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3674">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3676">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3676">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3678">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3678">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3680">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-3680">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3682">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-3682">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-3683">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3683">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3684">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3684">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3685">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3685">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3686">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-3686">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-3687">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-3687">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-3688">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-3688">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3690">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-3690">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-3691">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-3691">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3692">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-3692">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3693">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-3693">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-3694">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-3694">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-3695">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3695">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3696">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3696">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3697">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3697">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-3698">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-3698">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-3699">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3699">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-3700">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-3700">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-3701">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3701">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-3702">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-3702">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-3703">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3703">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-3704">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3704">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3705">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3705">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3706">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3706">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3708">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-3708">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3709">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3709">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3710">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-3710">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-3711">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3711">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-3712">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3712">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-3713">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-3713">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-3714">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-3714">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3716">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3716">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-3717">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3717">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-3718">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3718">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-3719">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-3719">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3721">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3721">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="ad36b-3722">DXGI_FORMAT_R16 \_ float<sup>FCS</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3722">DXGI_FORMAT_R16\_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="ad36b-3723">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-3723">Target</span></span> | <span data-ttu-id="ad36b-3724">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3724">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-3725">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3725">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-3726">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-3726">16</span></span> |
| <span data-ttu-id="ad36b-3727">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3727">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3729">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-3729">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3731">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3731">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3733">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3733">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3734">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3734">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3735">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3735">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3737">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3737">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3739">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3739">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3741">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-3741">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3743">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-3743">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3745">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3745">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3747">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3747">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3748">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3748">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3749">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-3749">Shader gather4</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3751">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-3751">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-3752">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-3752">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3754">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-3754">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3756">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-3756">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3758">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-3758">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3760">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-3760">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-3761">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-3761">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-3762">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3762">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3763">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3763">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3764">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3764">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-3765">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-3765">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-3766">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3766">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-3767">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-3767">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-3768">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3768">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-3769">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-3769">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-3770">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3770">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-3771">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3771">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3772">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3772">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3773">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3773">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3775">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-3775">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3777">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3777">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3779">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-3779">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3781">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3781">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3783">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3783">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3785">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-3785">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-3786">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-3786">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3788">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3788">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-3789">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3789">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-3790">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3790">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-3791">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-3791">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3793">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3793">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="ad36b-3794">DXGI_FORMAT_D16 \_ UNORM<sup>FCS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3794">DXGI_FORMAT_D16\_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="ad36b-3795">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-3795">Target</span></span> | <span data-ttu-id="ad36b-3796">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3796">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-3797">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3797">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-3798">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-3798">16</span></span> |
| <span data-ttu-id="ad36b-3799">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3799">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3801">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-3801">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3802">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3802">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3803">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3803">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3804">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3804">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3805">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3805">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3807">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3807">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3809">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3809">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-3810">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-3810">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3812">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-3812">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-3813">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3813">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3814">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3814">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3815">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3815">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3816">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-3816">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-3817">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-3817">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-3818">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-3818">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3820">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-3820">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-3821">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-3821">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3822">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-3822">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3823">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-3823">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-3824">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-3824">Depth/Stencil Target</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3826">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3826">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3827">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3827">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3828">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3828">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-3829">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-3829">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-3830">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3830">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-3831">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-3831">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-3832">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3832">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-3833">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-3833">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-3834">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3834">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-3835">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3835">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3836">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3836">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3837">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3837">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3839">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-3839">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3841">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3841">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3843">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-3843">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3845">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3845">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-3846">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3846">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-3847">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-3847">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-3848">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-3848">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3850">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3850">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-3851">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3851">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-3852">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3852">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-3853">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-3853">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3855">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3855">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="ad36b-3856">DXGI_FORMAT_R16 \_ UNORM<sup>FCS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3856">DXGI_FORMAT_R16\_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="ad36b-3857">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-3857">Target</span></span> | <span data-ttu-id="ad36b-3858">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3858">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-3859">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3859">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-3860">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-3860">16</span></span> |
| <span data-ttu-id="ad36b-3861">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3861">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3863">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-3863">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3865">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3865">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3867">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3867">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3868">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3868">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3869">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3869">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3871">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3871">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3873">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3873">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3875">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-3875">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3877">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-3877">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3879">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3879">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3881">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3881">Shader sample\_c (comparison filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3883">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3883">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3884">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-3884">Shader gather4</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3886">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-3886">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-3887">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-3887">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3889">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-3889">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3891">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-3891">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3893">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-3893">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3895">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-3895">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-3896">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-3896">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-3897">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3897">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3898">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3898">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3899">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3899">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-3900">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-3900">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-3901">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3901">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-3902">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-3902">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-3903">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3903">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-3904">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-3904">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-3905">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3905">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-3906">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3906">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3907">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3907">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3908">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3908">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3910">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-3910">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3912">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3912">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3914">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-3914">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3916">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3916">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3918">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3918">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3920">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-3920">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-3921">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-3921">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3923">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3923">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-3924">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3924">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-3925">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3925">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-3926">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-3926">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3928">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="ad36b-3929">DXGI_FORMAT_R16 \_ uint<sup>FCS</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3929">DXGI_FORMAT_R16\_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="ad36b-3930">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-3930">Target</span></span> | <span data-ttu-id="ad36b-3931">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3931">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-3932">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-3933">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-3933">16</span></span> |
| <span data-ttu-id="ad36b-3934">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3934">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3936">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-3936">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3938">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3938">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3940">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3940">Input Assembler Index Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3942">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3942">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-3943">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3943">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3945">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3945">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3947">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-3947">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3949">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-3949">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3951">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-3951">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3953">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3953">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3954">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3954">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3955">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3955">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-3956">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-3956">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-3957">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-3957">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-3958">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-3958">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3960">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-3960">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-3961">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-3961">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3963">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-3963">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-3964">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-3964">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3966">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-3966">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-3967">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-3967">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3968">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3968">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-3969">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3969">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-3970">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-3970">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-3971">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3971">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-3972">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-3972">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-3973">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3973">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-3974">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-3974">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-3975">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-3975">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-3976">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3976">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3977">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-3977">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-3978">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-3978">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3980">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-3980">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3982">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3982">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3984">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-3984">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-3986">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3986">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-3987">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-3987">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3989">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-3989">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-3990">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-3990">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3992">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3992">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-3993">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3993">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-3994">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-3994">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-3995">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-3995">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-3997">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-3997">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="ad36b-3998">DXGI_FORMAT_R16 \_ SNORM<sup>FCS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="ad36b-3998">DXGI_FORMAT_R16\_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="ad36b-3999">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-3999">Target</span></span> | <span data-ttu-id="ad36b-4000">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4000">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-4001">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4001">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-4002">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-4002">16</span></span> |
| <span data-ttu-id="ad36b-4003">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4003">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4005">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-4005">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4007">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4007">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4009">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4009">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4010">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4010">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4011">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4011">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4013">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4013">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4015">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4015">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4017">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-4017">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4019">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-4019">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4021">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4021">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4023">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4023">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4024">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4024">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4025">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4025">Shader gather4</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4027">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-4027">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-4028">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-4028">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4030">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-4030">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4032">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-4032">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4034">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-4034">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4036">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-4036">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-4037">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-4037">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-4038">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4038">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4039">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4039">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4040">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4040">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-4041">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-4041">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-4042">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4042">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-4043">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-4043">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-4044">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4044">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-4045">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-4045">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-4046">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4046">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-4047">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4047">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4048">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4048">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4049">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4049">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4051">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-4051">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4053">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4053">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-4055">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-4055">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-4057">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4057">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4059">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4059">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4061">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-4061">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-4062">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-4062">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4064">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4064">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-4065">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4065">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-4066">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4066">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-4067">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-4067">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4069">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4069">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="ad36b-4070">DXGI_FORMAT_R16 \_ San<sup>FCS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4070">DXGI_FORMAT_R16\_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="ad36b-4071">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-4071">Target</span></span> | <span data-ttu-id="ad36b-4072">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4072">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-4073">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4073">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-4074">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-4074">16</span></span> |
| <span data-ttu-id="ad36b-4075">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4075">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4077">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-4077">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4079">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4079">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4081">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4081">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4082">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4082">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4083">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4083">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4085">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4085">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4087">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4087">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4089">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-4089">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4091">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-4091">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4093">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4093">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4094">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4094">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4095">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4095">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4096">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4096">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-4097">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-4097">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-4098">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-4098">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4100">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-4100">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-4101">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-4101">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4103">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-4103">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4104">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-4104">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-4105">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-4105">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-4106">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4106">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4107">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4107">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4108">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4108">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-4109">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-4109">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-4110">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4110">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-4111">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-4111">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-4112">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4112">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-4113">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-4113">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-4114">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4114">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-4115">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4115">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4116">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4116">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4117">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4117">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4119">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-4119">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4121">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4121">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-4123">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-4123">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-4125">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4125">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-4126">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4126">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4128">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-4128">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-4129">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-4129">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4131">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4131">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-4132">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4132">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-4133">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4133">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-4134">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-4134">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4136">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4136">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="ad36b-4137">DXGI_FORMAT_R8 de \_ <sup>equipos</sup> sin tipo (60)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4137">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="ad36b-4138">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-4138">Target</span></span> | <span data-ttu-id="ad36b-4139">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4139">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-4140">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4140">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-4141">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-4141">8</span></span> |
| <span data-ttu-id="ad36b-4142">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4142">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4144">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-4144">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4145">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4145">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4146">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4146">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4147">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4147">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4148">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4148">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4150">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4150">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4152">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4152">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4154">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-4154">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4156">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-4156">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-4157">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4157">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4158">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4158">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4159">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4159">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4160">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4160">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-4161">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-4161">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-4162">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-4162">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4164">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-4164">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-4165">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-4165">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4166">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-4166">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4167">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-4167">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-4168">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-4168">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-4169">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4169">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4170">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4170">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4171">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4171">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-4172">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-4172">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-4173">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4173">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-4174">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-4174">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-4175">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4175">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-4176">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-4176">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-4177">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4177">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-4178">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4178">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4179">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4179">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4180">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4180">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4182">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-4182">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4183">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4183">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4184">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-4184">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-4185">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4185">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-4186">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4186">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-4187">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-4187">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-4188">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-4188">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4190">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4190">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-4191">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4191">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-4192">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4192">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-4193">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-4193">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4195">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4195">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="ad36b-4196">DXGI_FORMAT_R8 \_ UNORM<sup>FCS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4196">DXGI_FORMAT_R8\_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="ad36b-4197">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-4197">Target</span></span> | <span data-ttu-id="ad36b-4198">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4198">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-4199">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4199">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-4200">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-4200">8</span></span> |
| <span data-ttu-id="ad36b-4201">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4201">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4203">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-4203">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4205">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4205">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4207">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4207">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4208">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4208">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4209">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4209">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4211">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4211">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4213">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4213">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4215">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-4215">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4217">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-4217">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4219">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4219">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4221">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4221">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4222">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4222">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4223">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4223">Shader gather4</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4225">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-4225">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-4226">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-4226">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4228">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-4228">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4230">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-4230">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4232">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-4232">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4234">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-4234">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-4235">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-4235">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-4236">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4236">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4237">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4237">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4238">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4238">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-4239">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-4239">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-4240">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4240">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-4241">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-4241">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-4242">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4242">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-4243">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-4243">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-4244">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4244">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-4245">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4245">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4246">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4246">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4247">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4247">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4249">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-4249">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4251">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4251">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-4253">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-4253">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-4255">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4255">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4257">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4257">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4259">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-4259">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-4260">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-4260">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4262">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4262">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-4263">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4263">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-4264">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4264">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-4265">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-4265">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4267">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4267">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="ad36b-4268">DXGI_FORMAT_R8 \_ uint<sup>FCS</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4268">DXGI_FORMAT_R8\_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="ad36b-4269">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-4269">Target</span></span> | <span data-ttu-id="ad36b-4270">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4270">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-4271">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4271">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-4272">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-4272">8</span></span> |
| <span data-ttu-id="ad36b-4273">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4273">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4275">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-4275">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4277">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4277">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4279">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4279">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4280">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4280">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4281">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4281">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4283">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4283">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4285">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4285">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4287">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-4287">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4289">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-4289">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4291">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4291">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4292">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4293">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4294">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4294">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-4295">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-4295">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-4296">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-4296">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4298">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-4298">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-4299">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-4299">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4301">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-4301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4302">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-4302">Output Merger Logic Op</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-4304">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-4304">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-4305">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4305">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4306">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4306">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4307">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4307">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-4308">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-4308">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-4309">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4309">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-4310">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-4310">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-4311">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4311">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-4312">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-4312">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-4313">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4313">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-4314">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4314">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4315">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4315">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4316">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4316">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4318">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-4318">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4320">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4320">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-4322">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-4322">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-4324">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4324">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-4325">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4325">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4327">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-4327">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-4328">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-4328">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4330">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4330">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-4331">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4331">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-4332">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4332">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-4333">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-4333">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4335">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4335">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="ad36b-4336">DXGI_FORMAT_R8 \_ SNORM<sup>FCS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4336">DXGI_FORMAT_R8\_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="ad36b-4337">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-4337">Target</span></span> | <span data-ttu-id="ad36b-4338">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4338">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-4339">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4339">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-4340">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-4340">8</span></span> |
| <span data-ttu-id="ad36b-4341">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4341">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4343">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-4343">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4345">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4345">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4347">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4347">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4348">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4348">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4349">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4349">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4351">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4351">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4353">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4353">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4355">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-4355">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4357">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-4357">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4359">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4359">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4361">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4361">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4362">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4362">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4363">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4363">Shader gather4</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4365">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-4365">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-4366">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-4366">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4368">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-4368">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4370">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-4370">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4372">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-4372">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4374">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-4374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-4375">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-4375">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-4376">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4376">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4377">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4377">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4378">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4378">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-4379">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-4379">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-4380">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4380">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-4381">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-4381">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-4382">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4382">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-4383">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-4383">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-4384">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4384">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-4385">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4385">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4386">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4386">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4387">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4387">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4389">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-4389">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4391">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4391">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-4393">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-4393">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-4395">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4395">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4397">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4397">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4399">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-4399">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-4400">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-4400">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4402">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4402">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-4403">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4403">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-4404">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4404">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-4405">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-4405">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4407">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4407">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="ad36b-4408">DXGI_FORMAT_R8 \_ San<sup>FCS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4408">DXGI_FORMAT_R8\_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="ad36b-4409">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-4409">Target</span></span> | <span data-ttu-id="ad36b-4410">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4410">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-4411">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4411">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-4412">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-4412">8</span></span> |
| <span data-ttu-id="ad36b-4413">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4413">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4415">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-4415">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4417">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4417">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4419">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4419">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4420">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4420">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4421">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4421">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4423">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4423">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4425">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4425">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4427">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-4427">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4429">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-4429">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4431">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4431">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4432">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4432">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4433">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4433">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4434">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4434">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-4435">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-4435">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-4436">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-4436">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4438">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-4438">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-4439">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-4439">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4441">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-4441">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4442">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-4442">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-4443">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-4443">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-4444">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4444">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4445">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4445">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4446">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4446">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-4447">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-4447">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-4448">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4448">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-4449">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-4449">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-4450">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4450">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-4451">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-4451">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-4452">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4452">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-4453">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4453">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4454">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4454">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4455">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4455">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4457">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-4457">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4459">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4459">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-4461">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-4461">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-4463">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4463">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-4464">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4464">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4466">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-4466">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-4467">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-4467">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4469">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4469">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-4470">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4470">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-4471">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4471">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-4472">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-4472">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4474">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4474">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="ad36b-4475">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4475">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="ad36b-4476">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-4476">Target</span></span> | <span data-ttu-id="ad36b-4477">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4477">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-4478">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4478">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-4479">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-4479">8</span></span> |
| <span data-ttu-id="ad36b-4480">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4480">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4482">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-4482">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4483">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4483">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4484">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4484">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4485">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4485">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4486">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4486">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4488">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4488">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4490">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4490">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4492">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-4492">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4494">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-4494">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4496">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4496">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4498">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4498">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4499">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4499">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4500">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4500">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-4501">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-4501">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-4502">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-4502">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4504">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-4504">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4506">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-4506">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4508">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-4508">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4510">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-4510">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-4511">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-4511">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-4512">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4512">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4513">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4513">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4514">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4514">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-4515">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-4515">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-4516">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4516">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-4517">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-4517">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-4518">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4518">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-4519">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-4519">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-4520">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4520">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-4521">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4521">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4522">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4522">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4523">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4523">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4525">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-4525">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4527">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4527">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-4529">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-4529">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-4531">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4531">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4533">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4533">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4535">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-4535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-4536">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-4536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-4537">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-4538">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-4539">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-4540">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-4540">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4542">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4542">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="ad36b-4543">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4543">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="ad36b-4544">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-4544">Target</span></span> | <span data-ttu-id="ad36b-4545">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4545">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-4546">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4546">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-4547">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-4547">32</span></span> |
| <span data-ttu-id="ad36b-4548">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4548">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4550">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-4550">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4551">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4551">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4552">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4552">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4553">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4553">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4554">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4554">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4556">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4556">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4558">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4558">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4560">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-4560">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4562">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-4562">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4564">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4564">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4566">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4566">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4567">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4567">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4568">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4568">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-4569">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-4569">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-4570">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-4570">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4572">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-4572">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-4573">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-4573">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4574">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-4574">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4575">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-4575">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-4576">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-4576">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-4577">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4577">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4578">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4578">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4579">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4579">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-4580">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-4580">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-4581">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4581">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-4582">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-4582">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-4583">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4583">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-4584">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-4584">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-4585">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4585">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-4586">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4586">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4587">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4587">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4588">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4588">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4590">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-4590">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4591">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4591">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4592">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-4592">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-4593">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4593">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-4594">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4594">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-4595">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-4595">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-4596">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-4596">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-4597">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4597">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-4598">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4598">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-4599">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4599">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-4600">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-4600">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-4601">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4601">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="ad36b-4602">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4602">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="ad36b-4603">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-4603">Target</span></span> | <span data-ttu-id="ad36b-4604">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4604">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-4605">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4605">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-4606">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-4606">16</span></span> |
| <span data-ttu-id="ad36b-4607">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4607">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4609">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-4609">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4610">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4610">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4611">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4611">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4612">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4612">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4613">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4613">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4615">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4615">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4617">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4617">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4619">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-4619">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4621">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-4621">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4623">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4623">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4625">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4625">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4626">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4626">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4627">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4627">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-4628">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-4628">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-4629">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-4629">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4631">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-4631">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-4632">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-4632">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4633">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-4633">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4634">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-4634">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-4635">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-4635">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-4636">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4636">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4637">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4637">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4638">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4638">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-4639">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-4639">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-4640">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4640">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-4641">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-4641">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-4642">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4642">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-4643">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-4643">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-4644">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4644">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-4645">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4645">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4646">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4646">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4647">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4647">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4649">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-4649">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4650">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4650">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4651">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-4651">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-4652">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-4653">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4653">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-4654">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-4654">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-4655">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-4655">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-4656">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4656">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-4657">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4657">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-4658">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4658">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-4659">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-4659">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-4660">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4660">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="ad36b-4661">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4661">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="ad36b-4662">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-4662">Target</span></span> | <span data-ttu-id="ad36b-4663">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4663">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-4664">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4664">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-4665">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-4665">16</span></span> |
| <span data-ttu-id="ad36b-4666">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4666">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4668">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-4668">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4669">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4669">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4670">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4670">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4671">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4671">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4672">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4672">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4674">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4674">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4676">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4676">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4678">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-4678">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4680">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-4680">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4682">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4682">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4684">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4684">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4685">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4685">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4686">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4686">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-4687">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-4687">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-4688">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-4688">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4690">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-4690">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-4691">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-4691">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4692">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-4692">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4693">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-4693">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-4694">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-4694">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-4695">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4695">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4696">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4696">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4697">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4697">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-4698">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-4698">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-4699">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4699">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-4700">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-4700">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-4701">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4701">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-4702">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-4702">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-4703">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4703">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-4704">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4704">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4705">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4705">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4706">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4706">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4708">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-4708">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4709">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4709">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4710">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-4710">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-4711">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4711">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-4712">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4712">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-4713">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-4713">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-4714">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-4714">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-4715">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4715">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-4716">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4716">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-4717">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4717">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-4718">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-4718">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-4719">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4719">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="ad36b-4720">DXGI_FORMAT_BC1 \_ <sup>PCC</sup> sin tipo (70)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4720">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="ad36b-4721">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-4721">Target</span></span> | <span data-ttu-id="ad36b-4722">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4722">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-4723">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4723">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-4724">4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4724">4</span></span> |
| <span data-ttu-id="ad36b-4725">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4725">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4727">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-4727">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4728">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4728">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4729">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4729">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4730">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4730">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4731">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4731">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-4732">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4732">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4734">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4734">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4736">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-4736">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4738">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-4738">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-4739">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4739">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4740">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4740">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4741">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4741">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4742">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4742">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-4743">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-4743">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-4744">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-4744">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4746">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-4746">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-4747">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-4747">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4748">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-4748">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4749">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-4749">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-4750">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-4750">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-4751">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4751">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4752">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4752">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4753">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4753">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-4754">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-4754">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-4755">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4755">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-4756">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-4756">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-4757">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4757">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-4758">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-4758">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-4759">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4759">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-4760">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4760">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4761">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4761">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4762">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4762">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4764">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-4764">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4765">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4765">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4766">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-4766">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-4767">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4767">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-4768">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4768">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-4769">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-4769">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-4770">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-4770">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4772">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4772">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-4773">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4773">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-4774">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4774">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-4775">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-4775">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4777">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4777">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfccsup-71"></a><span data-ttu-id="ad36b-4778">DXGI_FORMAT_BC1 \_ UNORM<sup>FCC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4778">DXGI_FORMAT_BC1\_UNORM<sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="ad36b-4779">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-4779">Target</span></span> | <span data-ttu-id="ad36b-4780">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4780">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-4781">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4781">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-4782">4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4782">4</span></span> |
| <span data-ttu-id="ad36b-4783">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4783">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4785">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-4785">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4786">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4786">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4787">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4787">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4788">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4788">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4789">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4789">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-4790">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4790">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4792">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4792">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4794">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-4794">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4796">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-4796">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4798">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4798">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4800">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4800">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4801">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4801">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4802">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4802">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-4803">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-4803">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-4804">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-4804">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4806">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-4806">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-4807">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-4807">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4808">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-4808">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4809">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-4809">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-4810">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-4810">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-4811">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4811">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4812">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4812">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4813">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4813">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-4814">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-4814">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-4815">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4815">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-4816">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-4816">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-4817">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4817">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-4818">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-4818">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-4819">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4819">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-4820">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4820">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4821">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4821">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4822">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4822">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4824">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-4824">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4825">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4825">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4826">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-4826">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-4827">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4827">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-4828">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4828">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-4829">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-4829">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-4830">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-4830">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4832">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4832">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-4833">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4833">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-4834">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4834">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-4835">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-4835">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4837">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4837">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfccsup-72"></a><span data-ttu-id="ad36b-4838">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FCC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4838">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="ad36b-4839">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-4839">Target</span></span> | <span data-ttu-id="ad36b-4840">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4840">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-4841">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4841">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-4842">4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4842">4</span></span> |
| <span data-ttu-id="ad36b-4843">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4843">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4845">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-4845">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4846">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4846">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4847">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4847">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4848">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4848">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4849">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4849">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-4850">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4850">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4852">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4852">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4854">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-4854">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4856">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-4856">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4858">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4858">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4860">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4860">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4861">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4861">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4862">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4862">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-4863">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-4863">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-4864">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-4864">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4866">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-4866">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-4867">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-4867">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4868">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-4868">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4869">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-4869">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-4870">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-4870">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-4871">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4871">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4872">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4872">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4873">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4873">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-4874">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-4874">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-4875">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4875">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-4876">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-4876">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-4877">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4877">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-4878">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-4878">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-4879">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4879">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-4880">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4880">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4881">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4881">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4882">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4882">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4884">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-4884">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4885">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4885">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4886">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-4886">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-4887">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4887">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-4888">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4888">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-4889">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-4889">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-4890">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-4890">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4892">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4892">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-4893">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4893">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-4894">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4894">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-4895">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-4895">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4897">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4897">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="ad36b-4898">DXGI_FORMAT_BC2 \_ <sup>PCC</sup> sin tipo (73)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4898">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="ad36b-4899">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-4899">Target</span></span> | <span data-ttu-id="ad36b-4900">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4900">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-4901">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4901">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-4902">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-4902">8</span></span> |
| <span data-ttu-id="ad36b-4903">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4903">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4905">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-4905">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4906">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4906">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4907">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4907">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4908">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4908">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4909">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4909">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-4910">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4910">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4912">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4912">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4914">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-4914">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4916">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-4916">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-4917">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4917">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4918">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4918">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4919">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4919">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4920">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4920">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-4921">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-4921">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-4922">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-4922">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4924">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-4924">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-4925">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-4925">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4926">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-4926">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4927">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-4927">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-4928">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-4928">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-4929">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4929">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4930">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4930">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4931">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4931">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-4932">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-4932">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-4933">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4933">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-4934">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-4934">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-4935">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4935">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-4936">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-4936">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-4937">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4937">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-4938">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4938">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4939">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4939">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4940">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4940">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4942">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-4942">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4943">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4943">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4944">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-4944">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-4945">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4945">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-4946">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-4946">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-4947">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-4947">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-4948">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-4948">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4950">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4950">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-4951">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4951">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-4952">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4952">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-4953">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-4953">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4955">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4955">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfccsup-74"></a><span data-ttu-id="ad36b-4956">DXGI_FORMAT_BC2 \_ UNORM<sup>FCC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4956">DXGI_FORMAT_BC2\_UNORM<sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="ad36b-4957">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-4957">Target</span></span> | <span data-ttu-id="ad36b-4958">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-4958">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-4959">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4959">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-4960">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-4960">8</span></span> |
| <span data-ttu-id="ad36b-4961">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4961">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4963">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-4963">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4964">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4964">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4965">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-4965">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4966">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4966">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-4967">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4967">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-4968">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4968">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4970">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-4970">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4972">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-4972">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4974">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-4974">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4976">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4976">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4978">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4978">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4979">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-4979">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-4980">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-4980">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-4981">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-4981">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-4982">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-4982">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-4984">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-4984">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-4985">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-4985">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4986">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-4986">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-4987">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-4987">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-4988">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-4988">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-4989">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-4989">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4990">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4990">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-4991">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-4991">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-4992">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-4992">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-4993">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4993">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-4994">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-4994">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-4995">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4995">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-4996">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-4996">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-4997">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-4997">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-4998">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4998">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-4999">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-4999">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5000">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5000">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5002">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-5002">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5003">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5003">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5004">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-5004">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-5005">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5005">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-5006">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5006">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-5007">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-5007">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-5008">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-5008">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5010">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5010">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-5011">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5011">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-5012">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5012">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-5013">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-5013">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5015">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5015">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfccsup-75"></a><span data-ttu-id="ad36b-5016">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FCC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5016">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="ad36b-5017">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-5017">Target</span></span> | <span data-ttu-id="ad36b-5018">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5018">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-5019">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5019">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-5020">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-5020">8</span></span> |
| <span data-ttu-id="ad36b-5021">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5021">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5023">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-5023">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5024">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5024">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5025">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5025">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5026">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5026">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5027">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5027">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-5028">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5028">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5030">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5030">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5032">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-5032">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5034">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-5034">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5036">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5036">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5038">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5038">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5039">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5039">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5040">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5040">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-5041">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-5041">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-5042">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-5042">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5044">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-5044">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-5045">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-5045">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5046">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-5046">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5047">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-5047">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-5048">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-5048">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-5049">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5049">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5050">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5050">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5051">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5051">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-5052">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-5052">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-5053">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5053">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-5054">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-5054">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-5055">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5055">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-5056">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-5056">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-5057">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5057">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-5058">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5058">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5059">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5059">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5060">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5060">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5062">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-5062">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5063">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5063">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5064">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-5064">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-5065">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5065">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-5066">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5066">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-5067">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-5067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-5068">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-5068">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5070">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5070">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-5071">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5071">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-5072">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5072">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-5073">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-5073">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5075">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5075">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="ad36b-5076">DXGI_FORMAT_BC3 \_ <sup>PCC</sup> sin tipo (76)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5076">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="ad36b-5077">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-5077">Target</span></span> | <span data-ttu-id="ad36b-5078">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5078">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-5079">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5079">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-5080">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-5080">8</span></span> |
| <span data-ttu-id="ad36b-5081">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5081">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5083">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-5083">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5084">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5085">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5086">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5087">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-5088">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5088">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5090">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5090">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5092">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-5092">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5094">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-5094">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-5095">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5095">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5096">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5096">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5097">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5097">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5098">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5098">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-5099">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-5099">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-5100">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-5100">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5102">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-5102">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-5103">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-5103">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5104">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-5104">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5105">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-5105">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-5106">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-5106">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-5107">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5107">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5108">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5108">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5109">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5109">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-5110">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-5110">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-5111">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5111">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-5112">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-5112">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-5113">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5113">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-5114">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-5114">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-5115">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5115">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-5116">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5116">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5117">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5117">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5118">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5118">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5120">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-5120">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5121">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5121">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5122">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-5122">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-5123">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5123">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-5124">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5124">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-5125">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-5125">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-5126">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-5126">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5128">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5128">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-5129">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5129">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-5130">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5130">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-5131">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-5131">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5133">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5133">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfccsup-77"></a><span data-ttu-id="ad36b-5134">DXGI_FORMAT_BC3 \_ UNORM<sup>FCC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5134">DXGI_FORMAT_BC3\_UNORM<sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="ad36b-5135">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-5135">Target</span></span> | <span data-ttu-id="ad36b-5136">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5136">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-5137">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5137">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-5138">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-5138">8</span></span> |
| <span data-ttu-id="ad36b-5139">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5139">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5141">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-5141">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5142">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5142">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5143">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5143">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5144">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5144">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5145">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5145">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-5146">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5146">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5148">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5148">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5150">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-5150">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5152">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-5152">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5154">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5154">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5156">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5156">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5157">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5157">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5158">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5158">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-5159">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-5159">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-5160">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-5160">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5162">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-5162">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-5163">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-5163">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5164">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-5164">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5165">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-5165">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-5166">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-5166">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-5167">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5167">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5168">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5168">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5169">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5169">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-5170">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-5170">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-5171">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-5172">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-5172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-5173">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-5174">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-5174">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-5175">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-5176">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5176">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5177">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5177">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5178">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5178">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5180">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-5180">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5181">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5181">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5182">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-5182">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-5183">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5183">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-5184">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5184">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-5185">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-5185">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-5186">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-5186">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5188">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5188">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-5189">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5189">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-5190">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5190">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-5191">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-5191">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5193">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5193">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfccsup-78"></a><span data-ttu-id="ad36b-5194">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FCC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5194">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="ad36b-5195">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-5195">Target</span></span> | <span data-ttu-id="ad36b-5196">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5196">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-5197">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5197">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-5198">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-5198">8</span></span> |
| <span data-ttu-id="ad36b-5199">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5199">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5201">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-5201">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5202">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5202">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5203">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5203">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5204">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5204">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5205">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5205">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-5206">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5206">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5208">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5208">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5210">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-5210">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5212">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-5212">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5214">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5214">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5216">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5216">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5217">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5217">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5218">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5218">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-5219">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-5219">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-5220">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-5220">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5222">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-5222">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-5223">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-5223">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5224">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-5224">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5225">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-5225">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-5226">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-5226">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-5227">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5227">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5228">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5228">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5229">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5229">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-5230">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-5230">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-5231">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5231">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-5232">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-5232">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-5233">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5233">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-5234">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-5234">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-5235">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5235">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-5236">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5236">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5237">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5237">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5238">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5238">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5240">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-5240">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5241">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5241">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5242">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-5242">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-5243">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5243">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-5244">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5244">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-5245">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-5245">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-5246">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-5246">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5248">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5248">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-5249">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5249">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-5250">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5250">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-5251">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-5251">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5253">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5253">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="ad36b-5254">DXGI_FORMAT_BC4 \_ <sup>PCC</sup> sin tipo (79)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5254">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="ad36b-5255">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-5255">Target</span></span> | <span data-ttu-id="ad36b-5256">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5256">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-5257">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5257">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-5258">4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5258">4</span></span> |
| <span data-ttu-id="ad36b-5259">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5259">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5261">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-5261">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5262">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5262">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5263">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5263">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5264">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5264">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5265">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5265">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-5266">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5266">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5268">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5268">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5270">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-5270">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5272">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-5272">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-5273">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5273">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5274">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5274">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5275">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5275">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5276">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5276">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-5277">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-5277">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-5278">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-5278">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5280">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-5280">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-5281">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-5281">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5282">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-5282">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5283">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-5283">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-5284">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-5284">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-5285">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5285">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5286">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5286">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5287">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5287">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-5288">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-5288">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-5289">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5289">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-5290">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-5290">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-5291">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5291">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-5292">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-5292">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-5293">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5293">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-5294">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5294">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5295">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5295">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5296">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5296">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5298">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-5298">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5299">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5299">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5300">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-5300">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-5301">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5301">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-5302">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5302">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-5303">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-5303">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-5304">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-5304">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5306">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5306">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-5307">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5307">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-5308">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5308">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-5309">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-5309">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-5310">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5310">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfccsup-80"></a><span data-ttu-id="ad36b-5311">DXGI_FORMAT_BC4 \_ UNORM<sup>FCC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5311">DXGI_FORMAT_BC4\_UNORM<sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="ad36b-5312">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-5312">Target</span></span> | <span data-ttu-id="ad36b-5313">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5313">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-5314">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5314">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-5315">4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5315">4</span></span> |
| <span data-ttu-id="ad36b-5316">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5316">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5318">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-5318">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5319">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5319">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5320">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5321">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5321">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5322">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5322">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-5323">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5323">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5325">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5325">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5327">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-5327">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5329">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-5329">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5331">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5331">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5333">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5333">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5334">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5334">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5335">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5335">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-5336">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-5336">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-5337">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-5337">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5339">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-5339">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-5340">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-5340">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5341">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-5341">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5342">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-5342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-5343">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-5343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-5344">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5345">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5346">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5346">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-5347">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-5347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-5348">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-5349">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-5349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-5350">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-5351">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-5351">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-5352">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-5353">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5354">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5355">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5355">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5357">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-5357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5358">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5359">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-5359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-5360">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-5361">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5361">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-5362">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-5362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-5363">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-5363">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5365">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5365">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-5366">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5366">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-5367">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5367">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-5368">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-5368">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-5369">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5369">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfccsup-81"></a><span data-ttu-id="ad36b-5370">DXGI_FORMAT_BC4 \_ SNORM<sup>FCC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5370">DXGI_FORMAT_BC4\_SNORM<sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="ad36b-5371">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-5371">Target</span></span> | <span data-ttu-id="ad36b-5372">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5372">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-5373">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5373">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-5374">4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5374">4</span></span> |
| <span data-ttu-id="ad36b-5375">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5375">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5377">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-5377">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5378">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5378">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5379">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5379">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5380">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5380">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5381">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5381">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-5382">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5382">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5384">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5384">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5386">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-5386">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5388">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-5388">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5390">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5390">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5392">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5392">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5393">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5393">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5394">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5394">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-5395">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-5395">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-5396">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-5396">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5398">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-5398">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-5399">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-5399">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5400">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-5400">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5401">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-5401">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-5402">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-5402">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-5403">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5403">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5404">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5404">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5405">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5405">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-5406">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-5406">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-5407">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5407">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-5408">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-5408">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-5409">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5409">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-5410">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-5410">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-5411">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5411">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-5412">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5412">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5413">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5413">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5414">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5414">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5416">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-5416">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5417">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5417">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5418">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-5418">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-5419">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5419">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-5420">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5420">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-5421">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-5421">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-5422">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-5422">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5424">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5424">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-5425">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5425">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-5426">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5426">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-5427">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-5427">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-5428">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5428">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="ad36b-5429">DXGI_FORMAT_BC5 \_ <sup>PCC</sup> sin tipo (82)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5429">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="ad36b-5430">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-5430">Target</span></span> | <span data-ttu-id="ad36b-5431">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5431">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-5432">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5432">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-5433">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-5433">8</span></span> |
| <span data-ttu-id="ad36b-5434">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5434">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5436">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-5436">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5437">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5437">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5438">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5438">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5439">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5439">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5440">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5440">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-5441">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5441">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5443">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5443">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5445">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-5445">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5447">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-5447">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-5448">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5448">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5449">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5449">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5450">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5450">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5451">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5451">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-5452">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-5452">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-5453">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-5453">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5455">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-5455">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-5456">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-5456">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5457">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-5457">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5458">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-5458">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-5459">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-5459">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-5460">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5460">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5461">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5461">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5462">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5462">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-5463">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-5463">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-5464">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5464">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-5465">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-5465">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-5466">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5466">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-5467">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-5467">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-5468">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5468">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-5469">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5469">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5470">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5470">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5471">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5471">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5473">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-5473">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5474">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5474">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5475">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-5475">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-5476">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5476">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-5477">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5477">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-5478">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-5478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-5479">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-5479">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5481">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-5482">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-5483">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-5484">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-5484">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-5485">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5485">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfccsup-83"></a><span data-ttu-id="ad36b-5486">DXGI_FORMAT_BC5 \_ UNORM<sup>FCC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5486">DXGI_FORMAT_BC5\_UNORM<sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="ad36b-5487">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-5487">Target</span></span> | <span data-ttu-id="ad36b-5488">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5488">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-5489">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5489">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-5490">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-5490">8</span></span> |
| <span data-ttu-id="ad36b-5491">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5491">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5493">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-5493">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5494">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5494">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5495">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5495">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5496">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5496">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5497">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5497">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-5498">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5498">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5500">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5500">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5502">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-5502">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5504">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-5504">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5506">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5506">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5508">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5509">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5510">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5510">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-5511">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-5511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-5512">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-5512">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5514">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-5514">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-5515">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-5515">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5516">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-5516">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5517">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-5517">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-5518">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-5518">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-5519">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5519">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5520">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5520">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5521">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5521">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-5522">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-5522">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-5523">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5523">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-5524">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-5524">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-5525">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5525">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-5526">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-5526">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-5527">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5527">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-5528">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5528">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5529">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5529">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5530">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5530">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5532">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-5532">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5533">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5533">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5534">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-5534">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-5535">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5535">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-5536">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5536">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-5537">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-5537">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-5538">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-5538">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5540">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5540">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-5541">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5541">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-5542">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5542">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-5543">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-5543">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-5544">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5544">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfccsup-84"></a><span data-ttu-id="ad36b-5545">DXGI_FORMAT_BC5 \_ SNORM<sup>FCC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5545">DXGI_FORMAT_BC5\_SNORM<sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="ad36b-5546">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-5546">Target</span></span> | <span data-ttu-id="ad36b-5547">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5547">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-5548">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5548">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-5549">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-5549">8</span></span> |
| <span data-ttu-id="ad36b-5550">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5550">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5552">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-5552">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5553">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5553">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5554">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5554">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5555">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5555">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5556">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5556">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-5557">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5557">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5559">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5559">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5561">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-5561">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5563">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-5563">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5565">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5565">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5567">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5567">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5568">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5568">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5569">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5569">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-5570">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-5570">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-5571">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-5571">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5573">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-5573">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-5574">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-5574">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5575">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-5575">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5576">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-5576">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-5577">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-5577">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-5578">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5578">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5579">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5579">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5580">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5580">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-5581">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-5581">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-5582">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5582">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-5583">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-5583">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-5584">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5584">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-5585">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-5585">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-5586">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5586">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-5587">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5587">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5588">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5588">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5589">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5589">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5591">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-5591">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5592">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5592">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5593">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-5593">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-5594">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5594">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-5595">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5595">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-5596">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-5596">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-5597">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-5597">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5599">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5599">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-5600">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5600">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-5601">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5601">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-5602">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-5602">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-5603">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5603">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="ad36b-5604">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5604">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="ad36b-5605">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-5605">Target</span></span> | <span data-ttu-id="ad36b-5606">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5606">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-5607">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5607">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-5608">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-5608">16</span></span> |
| <span data-ttu-id="ad36b-5609">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5609">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5611">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-5611">Buffer</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5613">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5613">Input Assembler Vertex Buffer</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5615">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5615">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5616">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5616">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5617">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5617">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5619">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5619">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5621">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5621">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5623">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-5623">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5625">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-5625">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5627">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5627">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5629">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5629">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5630">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5630">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5631">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5631">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-5632">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-5632">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-5633">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-5633">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5635">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-5635">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5637">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-5637">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5639">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-5639">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5641">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-5641">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-5642">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-5642">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-5643">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5643">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5644">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5644">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5645">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5645">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-5646">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-5646">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-5647">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5647">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-5648">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-5648">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-5649">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5649">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-5650">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-5650">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-5651">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5651">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-5652">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5652">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5653">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5653">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5654">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5654">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5656">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-5656">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5658">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5658">8x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5660">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-5660">Other Multisample Count RT</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5662">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5662">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5664">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5664">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5666">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-5666">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-5667">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-5667">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-5668">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5668">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-5669">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5669">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-5670">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5670">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-5671">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-5671">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-5672">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5672">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="ad36b-5673">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5673">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="ad36b-5674">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-5674">Target</span></span> | <span data-ttu-id="ad36b-5675">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5675">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-5676">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5676">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-5677">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-5677">16</span></span> |
| <span data-ttu-id="ad36b-5678">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5678">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5680">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-5680">Buffer</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5682">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5682">Input Assembler Vertex Buffer</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5684">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5684">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5685">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5685">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5686">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5686">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5688">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5688">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5690">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5690">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5692">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-5692">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5694">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-5694">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5696">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5696">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5698">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5698">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5699">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5699">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5700">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5700">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-5701">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-5701">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-5702">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-5702">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5704">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-5704">Mipmap Auto-Generation</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5706">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-5706">RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5708">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-5708">Blendable RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5710">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-5710">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-5711">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-5711">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-5712">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5712">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5713">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5713">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5714">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5714">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-5715">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-5715">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-5716">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5716">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-5717">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-5717">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-5718">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5718">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-5719">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-5719">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-5720">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5720">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-5721">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5721">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5722">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5722">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5723">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5723">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5725">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-5725">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5727">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5727">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5729">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-5729">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5731">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5731">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5733">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5733">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5735">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-5735">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-5736">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-5736">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-5737">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5737">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-5738">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5738">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-5739">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5739">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-5740">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-5740">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-5741">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5741">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="ad36b-5742">DXGI_FORMAT_B8G8R8A8 de \_ <sup>equipos</sup> sin tipo (90)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5742">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="ad36b-5743">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-5743">Target</span></span> | <span data-ttu-id="ad36b-5744">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5744">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-5745">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5745">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-5746">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-5746">32</span></span> |
| <span data-ttu-id="ad36b-5747">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5747">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5749">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-5749">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5750">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5750">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5751">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5751">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5752">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5752">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5753">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5753">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5755">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5755">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5757">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5759">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-5759">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5761">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-5761">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-5762">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5762">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5763">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5763">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5764">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5764">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5765">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5765">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-5766">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-5766">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-5767">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-5767">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5769">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-5769">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-5770">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-5770">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5771">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-5771">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5772">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-5772">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-5773">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-5773">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-5774">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5774">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5775">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5775">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5776">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5776">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-5777">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-5777">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-5778">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5778">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-5779">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-5779">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-5780">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5780">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-5781">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-5781">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-5782">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5782">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-5783">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5783">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5784">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5784">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5785">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5785">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5787">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-5787">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5788">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5788">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5789">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-5789">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-5790">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5790">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-5791">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5791">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-5792">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-5792">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-5793">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-5793">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5795">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5795">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-5796">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5796">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-5797">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5797">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-5798">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-5798">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5800">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5800">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="ad36b-5801">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FCS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5801">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="ad36b-5802">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-5802">Target</span></span> | <span data-ttu-id="ad36b-5803">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5803">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-5804">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5804">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-5805">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-5805">32</span></span> |
| <span data-ttu-id="ad36b-5806">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5806">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5808">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-5808">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5810">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5810">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5812">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5812">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5813">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5813">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5814">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5814">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5816">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5816">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5818">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5818">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5820">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-5820">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5822">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-5822">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5824">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5824">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5826">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5826">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5827">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5827">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5828">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5828">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-5829">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-5829">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-5830">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-5830">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5832">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-5832">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5834">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-5834">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5836">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-5836">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5838">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-5838">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-5839">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-5839">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-5840">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5840">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5841">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5841">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5842">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5842">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-5843">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-5843">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-5844">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5844">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-5845">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-5845">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-5846">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5846">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-5847">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-5847">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-5848">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5848">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-5849">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5849">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5850">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5850">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5851">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5851">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5853">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-5853">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5855">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5855">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5857">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-5857">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5859">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5859">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5861">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5861">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5863">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-5863">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5865">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-5865">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5867">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5867">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-5868">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5868">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5870">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5870">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5872">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-5872">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5874">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5874">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="ad36b-5875">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRGB<sup>FCS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5875">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="ad36b-5876">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-5876">Target</span></span> | <span data-ttu-id="ad36b-5877">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5877">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-5878">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5878">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-5879">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-5879">32</span></span> |
| <span data-ttu-id="ad36b-5880">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5880">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5882">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-5882">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5883">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5883">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5884">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5884">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5885">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5885">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5886">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5886">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5888">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5888">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5890">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5890">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-5892">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5894">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-5894">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5896">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5896">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5898">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5898">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5899">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5899">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5900">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5900">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-5901">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-5901">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-5902">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-5902">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5904">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-5904">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5906">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-5906">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5908">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-5908">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5910">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-5910">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-5911">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-5911">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-5912">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5912">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5913">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5913">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5914">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5914">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-5915">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-5915">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-5916">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5916">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-5917">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-5917">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-5918">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5918">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-5919">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-5919">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-5920">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5920">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-5921">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5921">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5922">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5922">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5923">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5923">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5925">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-5925">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5927">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5927">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5929">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-5929">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5931">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5931">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5933">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5933">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5935">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-5935">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5937">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-5937">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5939">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5939">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-5940">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5940">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5942">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5942">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-5944">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-5944">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5946">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="ad36b-5947">DXGI_FORMAT_B8G8R8X8 de \_ <sup>equipos</sup> sin tipo (92)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5947">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="ad36b-5948">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-5948">Target</span></span> | <span data-ttu-id="ad36b-5949">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-5949">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-5950">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-5951">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-5951">32</span></span> |
| <span data-ttu-id="ad36b-5952">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5952">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5954">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-5954">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5955">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5955">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5956">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5956">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5957">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5957">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-5958">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5958">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5960">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5960">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5962">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-5962">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5964">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-5964">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5966">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-5966">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-5967">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5967">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5968">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5968">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5969">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-5969">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-5970">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-5970">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-5971">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-5971">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-5972">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-5972">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5974">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-5974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-5975">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-5975">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5976">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-5976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5977">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-5977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-5978">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-5978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-5979">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-5979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5980">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-5981">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5981">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-5982">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-5982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-5983">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-5984">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-5984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-5985">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-5986">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-5986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-5987">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-5987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-5988">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5989">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-5989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-5990">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-5990">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-5992">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-5992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5993">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-5994">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-5994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-5995">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-5995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-5996">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-5996">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-5997">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-5997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-5998">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-5998">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6000">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6000">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-6001">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6001">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-6002">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-6003">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-6003">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6005">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6005">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="ad36b-6006">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FCS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6006">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="ad36b-6007">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-6007">Target</span></span> | <span data-ttu-id="ad36b-6008">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6008">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-6009">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6009">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-6010">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-6010">32</span></span> |
| <span data-ttu-id="ad36b-6011">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6011">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6013">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-6013">Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6015">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6015">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6017">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6017">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6018">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6018">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6019">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6019">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6021">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6023">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-6025">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6027">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-6027">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6029">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6029">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6031">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6032">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6033">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-6033">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-6034">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-6034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-6035">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-6035">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6037">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-6037">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6039">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-6039">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6041">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-6041">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6043">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-6043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-6044">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-6044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-6045">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6046">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6047">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6047">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-6048">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-6048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-6049">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-6050">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-6050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-6051">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-6052">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-6052">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-6053">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-6054">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6055">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6056">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6056">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6058">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-6058">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6060">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6060">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6062">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-6062">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6064">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6064">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6066">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6066">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6068">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-6068">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-6069">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-6069">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6071">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6071">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-6072">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6072">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6074">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6074">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6076">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-6076">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6078">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6078">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="ad36b-6079">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRGB<sup>FCS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6079">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="ad36b-6080">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-6080">Target</span></span> | <span data-ttu-id="ad36b-6081">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6081">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-6082">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6082">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-6083">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-6083">32</span></span> |
| <span data-ttu-id="ad36b-6084">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6084">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6086">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-6086">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6087">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6087">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6088">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6088">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6089">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6089">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6090">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6090">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6092">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6092">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6094">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6094">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6096">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-6096">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6098">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-6098">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6100">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6100">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6102">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6102">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6103">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6103">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6104">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-6104">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-6105">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-6105">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-6106">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-6106">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6108">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-6108">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6110">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-6110">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6112">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-6112">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6114">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-6114">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-6115">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-6115">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-6116">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6116">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6117">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6117">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6118">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6118">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-6119">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-6119">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-6120">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6120">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-6121">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-6121">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-6122">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6122">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-6123">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-6123">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-6124">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6124">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-6125">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6125">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6126">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6126">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6127">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6127">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6129">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-6129">4x Multisample RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6131">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6131">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6133">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-6133">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6135">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6135">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6137">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6137">Multisample Load</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6139">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-6139">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-6140">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-6140">Cast Within Bit Layout</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6142">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6142">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-6143">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6143">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-6144">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6144">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-6145">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-6145">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6147">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="ad36b-6148">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6148">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="ad36b-6149">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-6149">Target</span></span> | <span data-ttu-id="ad36b-6150">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6150">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-6151">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-6152">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-6152">32</span></span> |
| <span data-ttu-id="ad36b-6153">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6153">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6155">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-6155">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6156">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6156">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6157">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6157">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6158">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6158">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6159">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6159">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-6160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6160">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6162">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6162">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-6163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-6163">TextureCube</span></span> | \- |
| <span data-ttu-id="ad36b-6164">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-6164">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6166">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6166">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6168">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6168">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6169">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6169">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6170">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-6170">Shader gather4</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6172">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-6172">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-6173">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-6173">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6175">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-6175">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6177">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-6177">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6179">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-6179">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6181">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-6181">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-6182">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-6182">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-6183">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6183">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6184">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6184">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6185">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6185">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-6186">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-6186">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-6187">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6187">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-6188">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-6188">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-6189">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6189">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-6190">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-6190">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-6191">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6191">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-6192">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6192">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6193">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6193">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6194">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6194">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6196">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-6196">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6197">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6197">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6198">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-6198">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-6199">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6199">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-6200">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6200">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-6201">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-6201">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-6202">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-6202">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-6203">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6203">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6205">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6205">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6207">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6207">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6209">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-6209">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6211">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6211">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="ad36b-6212">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6212">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="ad36b-6213">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-6213">Target</span></span> | <span data-ttu-id="ad36b-6214">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6214">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-6215">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6215">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-6216">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-6216">32</span></span> |
| <span data-ttu-id="ad36b-6217">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6217">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6219">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-6219">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6220">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6220">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6221">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6221">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6222">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6222">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6223">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6223">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-6224">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6224">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6226">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6226">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-6227">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-6227">TextureCube</span></span> | \- |
| <span data-ttu-id="ad36b-6228">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-6228">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6230">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6230">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6232">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6232">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6233">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6233">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6234">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-6234">Shader gather4</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6236">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-6236">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-6237">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-6237">Mipmap</span></span> | \- |
| <span data-ttu-id="ad36b-6238">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-6238">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-6239">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-6239">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6240">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-6240">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6241">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-6241">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-6242">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-6242">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-6243">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6243">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6244">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6244">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6245">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6245">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-6246">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-6246">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-6247">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6247">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-6248">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-6248">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-6249">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6249">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-6250">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-6250">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-6251">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6251">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-6252">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6252">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6253">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6253">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6254">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6254">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6256">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-6256">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6257">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6257">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6258">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-6258">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-6259">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6259">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-6260">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6260">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-6261">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-6261">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-6262">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-6262">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-6263">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6263">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6265">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6265">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6267">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6267">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6269">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-6269">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6271">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6271">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="ad36b-6272">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6272">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="ad36b-6273">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-6273">Target</span></span> | <span data-ttu-id="ad36b-6274">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6274">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-6275">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6275">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-6276">64</span><span class="sxs-lookup"><span data-stu-id="ad36b-6276">64</span></span> |
| <span data-ttu-id="ad36b-6277">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6277">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6279">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-6279">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6280">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6281">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6282">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6283">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-6284">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6284">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6286">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6286">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-6287">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-6287">TextureCube</span></span> | \- |
| <span data-ttu-id="ad36b-6288">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-6288">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6290">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6290">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6292">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6293">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6294">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-6294">Shader gather4</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6296">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-6296">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-6297">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-6297">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6299">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-6299">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-6300">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-6300">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6301">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-6301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6302">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-6302">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-6303">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-6303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-6304">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6305">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6306">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6306">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-6307">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-6307">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-6308">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6308">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-6309">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-6309">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-6310">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6310">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-6311">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-6311">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-6312">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6312">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-6313">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6313">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6314">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6314">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6315">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6315">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6317">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-6317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6318">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6319">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-6319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-6320">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-6321">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6321">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-6322">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-6322">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-6323">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-6323">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-6324">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6324">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6326">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6326">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6328">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6328">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6330">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-6330">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6332">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6332">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="ad36b-6333">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6333">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="ad36b-6334">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-6334">Target</span></span> | <span data-ttu-id="ad36b-6335">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6335">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-6336">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6336">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-6337">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-6337">8</span></span> |
| <span data-ttu-id="ad36b-6338">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6338">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6340">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-6340">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6341">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6341">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6342">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6342">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6343">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6343">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6344">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6344">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-6345">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6345">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6347">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6347">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-6348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-6348">TextureCube</span></span> | \- |
| <span data-ttu-id="ad36b-6349">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-6349">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6351">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6351">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6353">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6353">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6354">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6354">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6355">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-6355">Shader gather4</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6357">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-6357">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-6358">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-6358">Mipmap</span></span> | \- |
| <span data-ttu-id="ad36b-6359">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-6359">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-6360">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-6360">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6362">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-6362">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6364">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-6364">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-6365">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-6365">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-6366">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6366">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6367">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6367">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6368">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6368">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-6369">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-6369">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-6370">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6370">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-6371">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-6371">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-6372">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6372">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-6373">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-6373">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-6374">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6374">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-6375">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6375">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6376">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6376">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6377">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6377">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6379">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-6379">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6380">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6380">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6381">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-6381">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-6382">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6382">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-6383">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6383">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-6384">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-6384">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-6385">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-6385">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-6386">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6386">Video Decoder Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6388">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6388">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6390">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6390">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6392">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-6392">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6394">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6394">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="ad36b-6395">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6395">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="ad36b-6396">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-6396">Target</span></span> | <span data-ttu-id="ad36b-6397">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6397">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-6398">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6398">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-6399">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-6399">16</span></span> |
| <span data-ttu-id="ad36b-6400">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6400">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6402">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-6402">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6403">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6403">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6404">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6404">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6405">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6405">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6406">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6406">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-6407">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6407">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6409">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6409">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-6410">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-6410">TextureCube</span></span> | \- |
| <span data-ttu-id="ad36b-6411">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-6411">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6413">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6413">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6415">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6415">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6416">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6416">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6417">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-6417">Shader gather4</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6419">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-6419">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-6420">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-6420">Mipmap</span></span> | \- |
| <span data-ttu-id="ad36b-6421">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-6421">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-6422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-6422">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6424">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-6424">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6426">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-6426">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-6427">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-6427">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-6428">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6428">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6429">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6429">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6430">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6430">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-6431">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-6431">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-6432">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6432">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-6433">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-6433">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-6434">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6434">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-6435">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-6435">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-6436">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6436">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-6437">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6437">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6438">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6438">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6439">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6439">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6441">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-6441">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6442">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6442">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6443">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-6443">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-6444">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6444">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-6445">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6445">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-6446">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-6446">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-6447">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-6447">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-6448">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6448">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6450">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6450">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6452">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6452">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6454">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-6454">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6456">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6456">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="ad36b-6457">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6457">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="ad36b-6458">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-6458">Target</span></span> | <span data-ttu-id="ad36b-6459">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6459">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-6460">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6460">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-6461">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-6461">16</span></span> |
| <span data-ttu-id="ad36b-6462">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6462">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6464">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-6464">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6465">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6465">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6466">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6466">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6467">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6467">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6468">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6468">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-6469">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6469">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6471">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6471">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-6472">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-6472">TextureCube</span></span> | \- |
| <span data-ttu-id="ad36b-6473">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-6473">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6475">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6475">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6477">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6477">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6478">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6478">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6479">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-6479">Shader gather4</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6481">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-6481">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-6482">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-6482">Mipmap</span></span> | \- |
| <span data-ttu-id="ad36b-6483">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-6483">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-6484">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-6484">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6486">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-6486">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6488">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-6488">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-6489">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-6489">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-6490">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6490">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6491">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6491">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6492">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6492">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-6493">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-6493">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-6494">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6494">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-6495">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-6495">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-6496">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6496">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-6497">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-6497">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-6498">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6498">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-6499">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6499">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6500">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6500">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6501">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6501">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6503">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-6503">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6504">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6504">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6505">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-6505">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-6506">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6506">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-6507">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6507">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-6508">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-6508">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-6509">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-6509">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-6510">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6510">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6512">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6512">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6514">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6514">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6516">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-6516">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6518">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6518">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="ad36b-6519">DXGI_FORMAT_420 \_ opaca<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6519">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="ad36b-6520">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-6520">Target</span></span> | <span data-ttu-id="ad36b-6521">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6521">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-6522">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6522">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-6523">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-6523">8</span></span> |
| <span data-ttu-id="ad36b-6524">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6524">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6526">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-6526">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6527">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6527">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6528">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6528">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6529">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6529">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6530">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6530">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-6531">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6531">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6533">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6533">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-6534">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-6534">TextureCube</span></span> | \- |
| <span data-ttu-id="ad36b-6535">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-6535">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-6536">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6536">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6537">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6537">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6538">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6538">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6539">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-6539">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-6540">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-6540">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-6541">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-6541">Mipmap</span></span> | \- |
| <span data-ttu-id="ad36b-6542">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-6542">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-6543">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-6543">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6544">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-6544">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6545">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-6545">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-6546">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-6546">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-6547">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6547">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6548">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6548">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6549">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6549">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-6550">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-6550">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-6551">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6551">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-6552">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-6552">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-6553">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6553">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-6554">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-6554">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-6555">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6555">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-6556">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6556">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6557">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6557">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6558">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6558">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ad36b-6559">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-6559">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6560">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6560">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6561">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-6561">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-6562">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6562">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-6563">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6563">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-6564">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-6564">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-6565">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-6565">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-6566">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6566">Video Decoder Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6568">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6568">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6570">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6570">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6572">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-6572">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6574">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6574">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="ad36b-6575">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6575">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="ad36b-6576">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-6576">Target</span></span> | <span data-ttu-id="ad36b-6577">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6577">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-6578">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6578">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-6579">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-6579">16</span></span> |
| <span data-ttu-id="ad36b-6580">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6580">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6582">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-6582">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6583">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6583">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6584">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6584">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6585">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6585">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6586">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6586">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-6587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6587">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6589">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-6590">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-6590">TextureCube</span></span> | \- |
| <span data-ttu-id="ad36b-6591">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-6591">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6593">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6593">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6595">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6595">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6596">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6596">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6597">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-6597">Shader gather4</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6599">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-6599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-6600">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-6600">Mipmap</span></span> | \- |
| <span data-ttu-id="ad36b-6601">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-6601">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-6602">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-6602">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6603">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-6603">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6604">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-6604">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-6605">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-6605">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-6606">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6606">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6607">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6607">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6608">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6608">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-6609">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-6609">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-6610">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6610">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-6611">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-6611">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-6612">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6612">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-6613">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-6613">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-6614">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6614">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-6615">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6615">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6616">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6616">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6617">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6617">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6619">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-6619">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6620">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6620">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6621">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-6621">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-6622">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6622">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-6623">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6623">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-6624">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-6624">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-6625">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-6625">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-6626">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6626">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6628">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6628">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6630">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6630">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6632">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-6632">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6634">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6634">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="ad36b-6635">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6635">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="ad36b-6636">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-6636">Target</span></span> | <span data-ttu-id="ad36b-6637">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6637">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-6638">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6638">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-6639">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-6639">32</span></span> |
| <span data-ttu-id="ad36b-6640">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6640">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6642">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-6642">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6643">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6643">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6644">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6644">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6645">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6645">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6646">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6646">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-6647">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6647">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6649">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6649">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-6650">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-6650">TextureCube</span></span> | \- |
| <span data-ttu-id="ad36b-6651">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-6651">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6653">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6653">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6655">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6655">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6656">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6656">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6657">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-6657">Shader gather4</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6659">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-6659">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-6660">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-6660">Mipmap</span></span> | \- |
| <span data-ttu-id="ad36b-6661">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-6661">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-6662">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-6662">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6663">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-6663">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6664">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-6664">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-6665">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-6665">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-6666">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6666">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6667">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6667">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6668">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6668">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-6669">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-6669">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-6670">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6670">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-6671">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-6671">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-6672">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6672">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-6673">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-6673">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-6674">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6674">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-6675">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6675">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6676">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6676">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6677">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6677">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6679">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-6679">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6680">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6680">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6681">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-6681">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-6682">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6682">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-6683">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6683">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-6684">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-6684">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-6685">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-6685">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-6686">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6686">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6688">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6688">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6690">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6690">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6692">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-6692">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6694">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6694">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="ad36b-6695">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6695">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="ad36b-6696">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-6696">Target</span></span> | <span data-ttu-id="ad36b-6697">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6697">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-6698">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6698">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-6699">32</span><span class="sxs-lookup"><span data-stu-id="ad36b-6699">32</span></span> |
| <span data-ttu-id="ad36b-6700">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6700">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6702">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-6702">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6703">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6703">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6704">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6704">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6705">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6705">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6706">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6706">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-6707">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6707">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6709">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6709">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-6710">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-6710">TextureCube</span></span> | \- |
| <span data-ttu-id="ad36b-6711">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-6711">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6713">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6713">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6715">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6715">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6716">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6716">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6717">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-6717">Shader gather4</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6719">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-6719">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-6720">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-6720">Mipmap</span></span> | \- |
| <span data-ttu-id="ad36b-6721">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-6721">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-6722">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-6722">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6723">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-6723">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6724">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-6724">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-6725">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-6725">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-6726">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6726">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6727">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6727">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6728">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6728">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-6729">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-6729">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-6730">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6730">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-6731">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-6731">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-6732">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6732">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-6733">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-6733">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-6734">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6734">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-6735">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6735">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6736">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6736">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6737">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6737">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6739">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-6739">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6740">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6740">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6741">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-6741">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-6742">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-6743">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6743">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-6744">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-6744">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-6745">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-6745">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-6746">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6746">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6748">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6748">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6750">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6750">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6752">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-6752">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6754">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6754">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="ad36b-6755">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6755">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="ad36b-6756">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-6756">Target</span></span> | <span data-ttu-id="ad36b-6757">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6757">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-6758">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6758">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-6759">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-6759">8</span></span> |
| <span data-ttu-id="ad36b-6760">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6760">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6762">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-6762">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6763">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6763">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6764">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6764">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6765">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6765">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6766">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6766">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-6767">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6767">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6769">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6769">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-6770">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-6770">TextureCube</span></span> | \- |
| <span data-ttu-id="ad36b-6771">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-6771">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6773">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6773">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6775">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6775">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6776">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6776">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6777">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-6777">Shader gather4</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6779">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-6779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-6780">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-6780">Mipmap</span></span> | \- |
| <span data-ttu-id="ad36b-6781">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-6781">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-6782">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-6782">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6784">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-6784">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6786">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-6786">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-6787">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-6787">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-6788">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6788">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6789">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6789">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6790">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6790">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-6791">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-6791">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-6792">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6792">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-6793">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-6793">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-6794">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6794">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-6795">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-6795">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-6796">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6796">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-6797">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6797">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6798">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6798">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6799">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6799">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6801">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-6801">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6802">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6802">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6803">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-6803">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-6804">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6804">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-6805">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6805">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-6806">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-6806">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-6807">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-6807">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-6808">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6808">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6810">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6810">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6812">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6812">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6814">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-6814">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6816">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6816">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="ad36b-6817">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6817">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="ad36b-6818">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-6818">Target</span></span> | <span data-ttu-id="ad36b-6819">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6819">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-6820">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6820">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-6821">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-6821">8</span></span> |
| <span data-ttu-id="ad36b-6822">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6822">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6824">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-6824">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6825">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6825">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6826">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6826">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6827">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6827">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6828">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6828">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-6829">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6829">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6831">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6831">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-6832">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-6832">TextureCube</span></span> | \- |
| <span data-ttu-id="ad36b-6833">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-6833">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-6834">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6834">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6835">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6835">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6836">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6836">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6837">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-6837">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-6838">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-6838">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-6839">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-6839">Mipmap</span></span> | \- |
| <span data-ttu-id="ad36b-6840">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-6840">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-6841">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-6841">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6842">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-6842">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6843">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-6843">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-6844">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-6844">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-6845">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6845">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6846">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6846">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6847">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6847">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-6848">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-6848">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-6849">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6849">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-6850">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-6850">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-6851">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6851">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-6852">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-6852">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-6853">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6853">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-6854">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6854">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6855">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6855">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6856">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6856">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6858">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-6858">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6859">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6859">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6860">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-6860">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-6861">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6861">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-6862">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6862">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-6863">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-6863">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-6864">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-6864">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-6865">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6865">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-6866">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6866">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6868">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6868">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-6869">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-6869">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-6870">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6870">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="ad36b-6871">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6871">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="ad36b-6872">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-6872">Target</span></span> | <span data-ttu-id="ad36b-6873">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6873">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-6874">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6874">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-6875">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-6875">8</span></span> |
| <span data-ttu-id="ad36b-6876">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6876">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6878">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-6878">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6879">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6879">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6880">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6880">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6881">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6881">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6882">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6882">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-6883">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6883">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6885">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6885">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-6886">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-6886">TextureCube</span></span> | \- |
| <span data-ttu-id="ad36b-6887">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-6887">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-6888">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6888">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6889">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6889">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6890">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6890">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6891">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-6891">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-6892">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-6892">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-6893">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-6893">Mipmap</span></span> | \- |
| <span data-ttu-id="ad36b-6894">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-6894">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-6895">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-6895">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6896">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-6896">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6897">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-6897">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-6898">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-6898">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-6899">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6899">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6900">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6900">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6901">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6901">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-6902">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-6902">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-6903">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6903">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-6904">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-6904">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-6905">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6905">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-6906">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-6906">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-6907">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6907">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-6908">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6908">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6909">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6909">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6910">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6910">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6912">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-6912">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6913">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6913">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6914">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-6914">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-6915">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6915">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-6916">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6916">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-6917">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-6917">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-6918">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-6918">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-6919">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6919">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-6920">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6920">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6922">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6922">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-6923">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-6923">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-6924">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6924">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="ad36b-6925">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6925">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="ad36b-6926">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-6926">Target</span></span> | <span data-ttu-id="ad36b-6927">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6927">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-6928">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6928">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-6929">8</span><span class="sxs-lookup"><span data-stu-id="ad36b-6929">8</span></span> |
| <span data-ttu-id="ad36b-6930">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6930">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6932">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-6932">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6933">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6933">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6934">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6934">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6935">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6935">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6936">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6936">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-6937">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6937">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6939">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6939">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-6940">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-6940">TextureCube</span></span> | \- |
| <span data-ttu-id="ad36b-6941">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-6941">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-6942">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6942">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6943">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6943">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6944">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6944">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6945">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-6945">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-6946">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-6946">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-6947">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-6947">Mipmap</span></span> | \- |
| <span data-ttu-id="ad36b-6948">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-6948">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-6949">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-6949">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6950">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-6950">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6951">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-6951">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-6952">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-6952">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-6953">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6953">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6954">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6954">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-6955">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6955">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-6956">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-6956">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-6957">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6957">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-6958">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-6958">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-6959">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6959">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-6960">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-6960">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-6961">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-6961">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-6962">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6962">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6963">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-6963">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-6964">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6964">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6966">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-6966">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6967">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6967">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-6968">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-6968">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-6969">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6969">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-6970">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-6970">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-6971">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-6971">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-6972">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-6972">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-6973">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6973">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-6974">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6974">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6976">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-6977">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-6977">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-6978">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6978">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="ad36b-6979">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6979">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="ad36b-6980">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-6980">Target</span></span> | <span data-ttu-id="ad36b-6981">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-6981">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-6982">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6982">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-6983">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-6983">16</span></span> |
| <span data-ttu-id="ad36b-6984">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-6984">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-6986">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-6986">Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6987">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6987">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6988">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-6988">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6989">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-6989">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-6990">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6990">Texture1D</span></span> | \- |
| <span data-ttu-id="ad36b-6991">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6991">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-6993">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-6993">Texture3D</span></span> | \- |
| <span data-ttu-id="ad36b-6994">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-6994">TextureCube</span></span> | \- |
| <span data-ttu-id="ad36b-6995">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-6995">Shader ld</span></span> | \- |
| <span data-ttu-id="ad36b-6996">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6996">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6997">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6997">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6998">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-6998">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-6999">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-6999">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-7000">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-7000">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-7001">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-7001">Mipmap</span></span> | \- |
| <span data-ttu-id="ad36b-7002">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-7002">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ad36b-7003">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-7003">RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-7004">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-7004">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-7005">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-7005">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-7006">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-7006">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-7007">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-7007">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-7008">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-7008">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-7009">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-7009">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-7010">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-7010">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-7011">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-7011">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-7012">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-7012">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-7013">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-7013">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-7014">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-7014">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-7015">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-7015">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-7016">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-7016">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-7017">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-7017">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-7018">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-7018">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-7020">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-7020">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-7021">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-7021">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ad36b-7022">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-7022">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ad36b-7023">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-7023">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ad36b-7024">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-7024">Multisample Load</span></span> | \- |
| <span data-ttu-id="ad36b-7025">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-7025">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-7026">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-7026">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-7027">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-7027">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-7028">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-7028">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-7030">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-7030">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-7031">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-7031">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-7032">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-7032">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="ad36b-7033">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="ad36b-7033">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="ad36b-7034">Destino</span><span class="sxs-lookup"><span data-stu-id="ad36b-7034">Target</span></span> | <span data-ttu-id="ad36b-7035">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="ad36b-7035">Support</span></span> |
| - | - |
| <span data-ttu-id="ad36b-7036">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="ad36b-7036">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ad36b-7037">16</span><span class="sxs-lookup"><span data-stu-id="ad36b-7037">16</span></span> |
| <span data-ttu-id="ad36b-7038">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-7038">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-7040">Buffer</span><span class="sxs-lookup"><span data-stu-id="ad36b-7040">Buffer</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-7042">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-7042">Input Assembler Vertex Buffer</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-7044">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="ad36b-7044">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-7045">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="ad36b-7045">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ad36b-7046">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad36b-7046">Texture1D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-7048">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad36b-7048">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-7050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad36b-7050">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-7052">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad36b-7052">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-7054">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="ad36b-7054">Shader ld</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-7056">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="ad36b-7056">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-7058">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="ad36b-7058">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ad36b-7059">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="ad36b-7059">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ad36b-7060">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="ad36b-7060">Shader gather4</span></span> | \- |
| <span data-ttu-id="ad36b-7061">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ad36b-7061">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ad36b-7062">Mapa</span><span class="sxs-lookup"><span data-stu-id="ad36b-7062">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-7064">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="ad36b-7064">Mipmap Auto-Generation</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-7066">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ad36b-7066">RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-7068">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="ad36b-7068">Blendable RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-7070">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="ad36b-7070">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ad36b-7071">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="ad36b-7071">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ad36b-7072">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="ad36b-7072">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-7073">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="ad36b-7073">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ad36b-7074">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-7074">Typed UAV</span></span> | \- |
| <span data-ttu-id="ad36b-7075">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="ad36b-7075">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ad36b-7076">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-7076">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ad36b-7077">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="ad36b-7077">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ad36b-7078">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-7078">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ad36b-7079">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="ad36b-7079">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ad36b-7080">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="ad36b-7080">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ad36b-7081">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-7081">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-7082">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="ad36b-7082">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ad36b-7083">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="ad36b-7083">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-7085">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="ad36b-7085">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-7087">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-7087">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-7089">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="ad36b-7089">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-7091">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="ad36b-7091">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="ad36b-7093">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="ad36b-7093">Multisample Load</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="ad36b-7095">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ad36b-7095">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ad36b-7096">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="ad36b-7096">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ad36b-7097">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-7097">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ad36b-7098">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-7098">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ad36b-7099">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-7099">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ad36b-7100">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="ad36b-7100">Shared Resource</span></span> | \- |
| <span data-ttu-id="ad36b-7101">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="ad36b-7101">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="ad36b-7102">Dar formato a notas</span><span class="sxs-lookup"><span data-stu-id="ad36b-7102">Format notes</span></span>

<span data-ttu-id="ad36b-7103">El propósito del formato puede cambiar de un nivel de característica de hardware a otro.</span><span class="sxs-lookup"><span data-stu-id="ad36b-7103">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="ad36b-7104"><sup>L</sup> : formato sin tipo</span><span class="sxs-lookup"><span data-stu-id="ad36b-7104"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="ad36b-7105"><sup>PC</sup> : diseño parcialmente tipado, de conversión de tipos y sencillo</span><span class="sxs-lookup"><span data-stu-id="ad36b-7105"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="ad36b-7106"><sup>FCS</sup> : diseño totalmente tipado, convertible y sencillo</span><span class="sxs-lookup"><span data-stu-id="ad36b-7106"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="ad36b-7107"><sup>FNS</sup> : diseño totalmente tipado, sin conversión y simple</span><span class="sxs-lookup"><span data-stu-id="ad36b-7107"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="ad36b-7108"><sup>PCC</sup> : diseño parcialmente tipado, convertible y complejo</span><span class="sxs-lookup"><span data-stu-id="ad36b-7108"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="ad36b-7109"><sup>FCC</sup> : diseño totalmente tipado, convertible y complejo</span><span class="sxs-lookup"><span data-stu-id="ad36b-7109"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="ad36b-7110"><sup>FNC</sup> : diseño totalmente tipado, no convertible y complejo</span><span class="sxs-lookup"><span data-stu-id="ad36b-7110"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="ad36b-7111"><sup>V</sup> : formato de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad36b-7111"><sup>V</sup> : video format</span></span>
</dt> </dl>

<span data-ttu-id="ad36b-7112">Los búferes de reserva y los recorridos con el [**formato de DXGI \_ R16G16B16A16 formato \_ \_ float**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) contienen datos de gamma con valores lineales.</span><span class="sxs-lookup"><span data-stu-id="ad36b-7112">Back buffers and scan outs with the [**DXGI\_FORMAT\_R16G16B16A16\_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format contain linear-valued gamma data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad36b-7113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad36b-7113">Related topics</span></span>

[<span data-ttu-id="ad36b-7114">Niveles de características de hardware de D3D12</span><span class="sxs-lookup"><span data-stu-id="ad36b-7114">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="ad36b-7115">**ID3D10Device::CheckFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="ad36b-7115">**ID3D10Device::CheckFormatSupport**</span></span>](/windows/win32/api/d3d10/nf-d3d10-id3d10device-checkformatsupport)

[<span data-ttu-id="ad36b-7116">Guía de programación para DXGI</span><span class="sxs-lookup"><span data-stu-id="ad36b-7116">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
