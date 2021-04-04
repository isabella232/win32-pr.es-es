---
description: En esta sección se especifican los formatos ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que se admiten en el hardware de 10Level9 9,1 de la característica Direct3D.
ms.assetid: 770A5396-C5D9-442B-99FE-3D220C54E8EB
title: Compatibilidad con el formato de hardware de la característica de nivel 9.1 de Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56653fd2fb504e3f23cfac13b432530ebaa7219b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906479"
---
# <a name="format-support-for-direct3d-feature-10level9-91-hardware"></a><span data-ttu-id="3b079-103">Compatibilidad con el formato de hardware de la característica de nivel 9.1 de Direct3D</span><span class="sxs-lookup"><span data-stu-id="3b079-103">Format support for Direct3D Feature 10Level9 9.1 hardware</span></span>

<span data-ttu-id="3b079-104">En esta sección se especifican los formatos ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que se admiten en el hardware de 10Level9 9,1 de la característica Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3b079-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature 10Level9 9.1 hardware.</span></span>

<span data-ttu-id="3b079-105">En la tabla se resume la compatibilidad de las características con la siguiente clave.</span><span class="sxs-lookup"><span data-stu-id="3b079-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="3b079-106">Símbolo</span><span class="sxs-lookup"><span data-stu-id="3b079-106">Symbol</span></span>                            | <span data-ttu-id="3b079-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b079-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="3b079-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="3b079-108">_ *-*\*</span></span>                             | <span data-ttu-id="3b079-109">No permitido o no disponible.</span><span class="sxs-lookup"><span data-stu-id="3b079-109">Disallowed or not available.</span></span>                                                  |
| ![requerido](images/letter-r.jpg)  | <span data-ttu-id="3b079-111">Se requiere compatibilidad con hardware.</span><span class="sxs-lookup"><span data-stu-id="3b079-111">Hardware support is required.</span></span>                                                 |
| ![opcional](images/letter-o.jpg)  | <span data-ttu-id="3b079-113">Compatibilidad de hardware opcional, el formato puede ser o no acelerado por hardware.</span><span class="sxs-lookup"><span data-stu-id="3b079-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dependientes](images/letter-d.jpg) | <span data-ttu-id="3b079-115">Requerido si se admite la característica opcional relacionada.</span><span class="sxs-lookup"><span data-stu-id="3b079-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="3b079-116">Este tema contiene una sección por formato.</span><span class="sxs-lookup"><span data-stu-id="3b079-116">This topic contains a section per format.</span></span> <span data-ttu-id="3b079-117">Un *destino* de formato (las tablas contienen una fila por destino) puede ser un tipo de recurso, una función intrínseca de HLSL o una funcionalidad determinada que depende de un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="3b079-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="3b079-118">Para comprobar mediante programación la compatibilidad de formato en D3D11 y D3D12, consulte Comprobación de la compatibilidad de las [características de hardware](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="3b079-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="3b079-119">Los números de los formatos son principalmente, pero no todos, en orden numérico ascendente; &mdash; algunos están fuera del orden numérico y se enumeran junto con otros formatos relevantes.</span><span class="sxs-lookup"><span data-stu-id="3b079-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="3b079-120">Tenga en cuenta también que los *tipos sin tipo* en un nombre de formato pueden significar un tipo *parcial* y no tienen un tipo estricto (consulte la sección [notas de formato](#format-notes) al final del tema).</span><span class="sxs-lookup"><span data-stu-id="3b079-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

// 

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="3b079-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="3b079-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="3b079-122">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-122">Target</span></span> | <span data-ttu-id="3b079-123">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-123">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-124">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-125">0</span><span class="sxs-lookup"><span data-stu-id="3b079-125">0</span></span> |
| <span data-ttu-id="3b079-126">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-126">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-127">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-127">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-128">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-128">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-129">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-129">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-130">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-130">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-131">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-131">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-132">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-132">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-133">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-134">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-135">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-135">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-136">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-137">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-138">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-139">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-139">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-140">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-141">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-141">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-142">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-143">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-144">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-145">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-146">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-147">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-148">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-149">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-149">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-150">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-151">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-152">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-153">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-154">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-154">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-155">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-156">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-157">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-158">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-158">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-159">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-159">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-160">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-160">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-161">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-161">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-162">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-163">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-163">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-164">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-165">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-166">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-167">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-168">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-169">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-169">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-170">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="3b079-171">DXGI_FORMAT_R32G32B32A32 de \_ <sup>equipos</sup> sin tipo (1)</span><span class="sxs-lookup"><span data-stu-id="3b079-171">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="3b079-172">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-172">Target</span></span> | <span data-ttu-id="3b079-173">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-173">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-174">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-175">128</span><span class="sxs-lookup"><span data-stu-id="3b079-175">128</span></span> |
| <span data-ttu-id="3b079-176">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-176">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-177">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-177">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-178">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-178">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-179">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-179">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-180">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-180">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-181">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-181">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-182">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-182">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-183">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-184">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-185">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-185">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-186">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-186">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-187">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-187">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-188">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-188">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-189">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-189">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-190">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-190">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-191">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-191">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-192">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-192">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-193">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-193">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-194">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-194">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-195">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-195">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-196">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-196">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-197">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-197">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-198">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-198">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-199">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-199">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-200">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-200">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-201">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-201">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-202">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-202">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-203">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-203">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-204">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-204">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-205">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-205">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-206">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-206">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-207">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-207">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-208">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-208">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-209">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-209">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-210">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-210">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-211">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-211">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-212">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-212">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-213">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-213">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-214">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-214">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-215">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-215">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-216">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-216">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-217">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-217">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-218">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-218">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-219">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-219">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-220">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-220">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a><span data-ttu-id="3b079-221">DXGI_FORMAT_R32G32B32A32 \_ float<sup>FNS</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="3b079-221">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FNS</sup> (2)</span></span>
| <span data-ttu-id="3b079-222">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-222">Target</span></span> | <span data-ttu-id="3b079-223">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-223">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-224">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-224">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-225">128</span><span class="sxs-lookup"><span data-stu-id="3b079-225">128</span></span> |
| <span data-ttu-id="3b079-226">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-226">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-228">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-228">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-229">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-229">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-231">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-232">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-233">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-234">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-234">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-235">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-235">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-236">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-236">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-237">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-237">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-238">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-238">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-239">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-239">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-240">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-240">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-241">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-241">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-242">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-242">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-243">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-243">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-244">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-244">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-245">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-245">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-246">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-246">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-247">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-247">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-248">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-248">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-249">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-249">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-250">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-250">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-251">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-251">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-252">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-252">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-253">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-253">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-254">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-254">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-255">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-255">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-256">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-256">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-257">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-257">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-258">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-258">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-259">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-259">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-260">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-260">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-261">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-261">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-262">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-262">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-263">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-263">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-264">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-264">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-265">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-265">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-266">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-266">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-267">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-267">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-268">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-268">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-269">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-269">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-270">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-270">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-271">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-271">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-272">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-272">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a><span data-ttu-id="3b079-273">DXGI_FORMAT_R32G32B32A32 \_ uint<sup>FNS</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="3b079-273">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FNS</sup> (3)</span></span>
| <span data-ttu-id="3b079-274">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-274">Target</span></span> | <span data-ttu-id="3b079-275">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-275">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-276">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-276">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-277">128</span><span class="sxs-lookup"><span data-stu-id="3b079-277">128</span></span> |
| <span data-ttu-id="3b079-278">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-278">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-279">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-279">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-280">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-281">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-282">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-283">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-284">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-284">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-285">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-285">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-286">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-286">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-287">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-287">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-288">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-288">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-289">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-289">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-290">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-290">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-291">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-291">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-292">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-292">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-293">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-293">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-294">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-294">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-295">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-295">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-296">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-296">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-297">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-297">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-298">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-298">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-299">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-299">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-300">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-300">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-301">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-301">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-302">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-302">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-303">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-303">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-304">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-304">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-305">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-305">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-306">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-306">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-307">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-307">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-308">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-308">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-309">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-309">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-310">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-310">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-311">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-311">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-312">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-312">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-313">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-313">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-314">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-314">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-315">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-315">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-316">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-316">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-317">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-317">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-318">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-318">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-319">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-319">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-320">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-320">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-321">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-321">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-322">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-322">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a><span data-ttu-id="3b079-323">DXGI_FORMAT_R32G32B32A32 \_ San<sup>FNS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="3b079-323">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FNS</sup> (4)</span></span>
| <span data-ttu-id="3b079-324">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-324">Target</span></span> | <span data-ttu-id="3b079-325">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-325">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-326">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-326">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-327">128</span><span class="sxs-lookup"><span data-stu-id="3b079-327">128</span></span> |
| <span data-ttu-id="3b079-328">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-328">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-329">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-329">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-330">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-330">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-331">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-331">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-332">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-332">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-333">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-333">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-334">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-335">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-335">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-336">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-336">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-337">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-337">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-338">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-338">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-339">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-339">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-340">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-340">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-341">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-341">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-342">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-342">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-343">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-343">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-344">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-344">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-345">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-345">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-346">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-346">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-347">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-347">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-348">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-348">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-349">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-349">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-350">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-350">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-351">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-351">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-352">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-352">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-353">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-353">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-354">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-354">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-355">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-355">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-356">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-356">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-357">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-357">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-358">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-358">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-359">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-359">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-360">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-360">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-361">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-361">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-362">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-362">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-363">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-363">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-364">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-364">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-365">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-365">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-366">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-366">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-367">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-367">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-368">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-369">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-370">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-371">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-371">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-372">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-372">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="3b079-373">DXGI_FORMAT_R32G32B32 de \_ <sup>equipos</sup> sin tipo (5)</span><span class="sxs-lookup"><span data-stu-id="3b079-373">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="3b079-374">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-374">Target</span></span> | <span data-ttu-id="3b079-375">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-375">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-376">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-376">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-377">96</span><span class="sxs-lookup"><span data-stu-id="3b079-377">96</span></span> |
| <span data-ttu-id="3b079-378">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-378">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-379">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-379">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-380">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-380">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-381">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-381">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-382">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-382">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-383">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-383">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-384">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-384">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-385">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-385">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-386">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-386">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-387">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-387">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-388">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-388">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-389">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-389">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-390">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-390">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-391">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-391">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-392">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-392">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-393">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-393">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-394">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-394">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-395">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-395">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-396">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-396">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-397">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-397">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-398">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-398">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-399">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-399">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-400">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-400">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-401">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-401">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-402">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-402">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-403">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-403">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-404">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-404">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-405">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-405">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-406">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-406">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-407">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-407">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-408">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-408">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-409">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-409">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-410">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-410">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-411">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-411">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-412">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-412">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-413">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-413">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-414">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-414">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-415">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-415">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-416">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-416">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-417">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-417">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-418">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-418">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-419">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-419">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-420">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-420">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-421">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-421">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-422">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-422">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a><span data-ttu-id="3b079-423">DXGI_FORMAT_R32G32B32 \_ float<sup>FNS</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="3b079-423">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FNS</sup> (6)</span></span>
| <span data-ttu-id="3b079-424">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-424">Target</span></span> | <span data-ttu-id="3b079-425">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-425">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-426">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-426">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-427">96</span><span class="sxs-lookup"><span data-stu-id="3b079-427">96</span></span> |
| <span data-ttu-id="3b079-428">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-428">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-430">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-430">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-431">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-431">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-433">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-433">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-434">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-434">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-435">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-435">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-436">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-436">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-437">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-437">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-438">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-438">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-439">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-439">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-440">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-441">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-442">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-443">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-443">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-444">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-445">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-445">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-446">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-446">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-447">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-447">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-448">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-448">Blendable RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="3b079-450">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-450">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-451">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-451">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-452">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-452">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-453">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-453">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-454">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-454">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-455">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-455">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-456">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-456">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-457">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-457">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-458">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-458">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-459">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-459">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-460">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-460">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-461">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-461">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-462">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-462">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-463">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-463">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-464">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-464">4x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="3b079-466">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-466">8x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="3b079-468">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-468">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-469">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-469">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-470">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-470">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-471">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-471">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-472">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-472">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-473">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-473">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-474">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-474">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-475">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-475">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-476">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-476">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-477">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-477">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a><span data-ttu-id="3b079-478">DXGI_FORMAT_R32G32B32 \_ uint<sup>FNS</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="3b079-478">DXGI_FORMAT_R32G32B32\_UINT<sup>FNS</sup> (7)</span></span>
| <span data-ttu-id="3b079-479">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-479">Target</span></span> | <span data-ttu-id="3b079-480">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-480">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-481">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-481">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-482">96</span><span class="sxs-lookup"><span data-stu-id="3b079-482">96</span></span> |
| <span data-ttu-id="3b079-483">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-483">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-484">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-484">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-485">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-485">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-486">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-486">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-487">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-487">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-488">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-488">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-489">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-489">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-490">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-490">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-491">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-491">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-492">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-492">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-493">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-493">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-494">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-494">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-495">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-495">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-496">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-496">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-497">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-497">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-498">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-498">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-499">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-499">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-500">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-500">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-501">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-501">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-502">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-502">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-503">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-503">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-504">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-504">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-505">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-505">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-506">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-506">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-507">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-507">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-508">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-508">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-509">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-509">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-510">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-510">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-511">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-511">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-512">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-512">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-513">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-513">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-514">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-514">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-515">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-515">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-516">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-516">4x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="3b079-518">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-518">8x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="3b079-520">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-520">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-521">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-521">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-522">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-522">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-523">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-523">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-524">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-524">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-525">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-525">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-526">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-526">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-527">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-527">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-528">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-528">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-529">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-529">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a><span data-ttu-id="3b079-530">DXGI_FORMAT_R32G32B32 \_ San<sup>FNS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="3b079-530">DXGI_FORMAT_R32G32B32\_SINT<sup>FNS</sup> (8)</span></span>
| <span data-ttu-id="3b079-531">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-531">Target</span></span> | <span data-ttu-id="3b079-532">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-532">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-533">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-533">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-534">96</span><span class="sxs-lookup"><span data-stu-id="3b079-534">96</span></span> |
| <span data-ttu-id="3b079-535">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-535">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-536">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-536">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-537">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-537">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-538">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-538">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-539">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-539">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-540">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-540">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-541">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-541">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-542">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-542">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-543">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-543">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-544">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-544">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-545">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-545">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-546">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-546">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-547">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-547">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-548">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-548">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-549">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-549">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-550">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-550">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-551">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-551">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-552">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-552">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-553">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-553">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-554">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-554">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-555">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-555">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-556">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-556">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-557">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-557">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-558">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-558">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-559">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-559">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-560">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-560">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-561">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-561">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-562">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-562">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-563">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-563">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-564">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-564">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-565">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-565">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-566">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-566">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-567">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-567">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-568">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-568">4x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="3b079-570">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-570">8x Multisample RenderTarget</span></span> | ![dependientes](images/letter-d.jpg) |
| <span data-ttu-id="3b079-572">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-572">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-573">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-573">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-574">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-574">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-575">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-575">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-576">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-576">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-577">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-577">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-578">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-578">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-579">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-579">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-580">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-580">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-581">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-581">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="3b079-582">DXGI_FORMAT_R16G16B16A16 de \_ <sup>equipos</sup> sin tipo (9)</span><span class="sxs-lookup"><span data-stu-id="3b079-582">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="3b079-583">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-583">Target</span></span> | <span data-ttu-id="3b079-584">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-584">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-585">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-585">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-586">64</span><span class="sxs-lookup"><span data-stu-id="3b079-586">64</span></span> |
| <span data-ttu-id="3b079-587">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-587">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-588">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-588">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-589">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-589">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-590">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-590">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-591">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-591">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-592">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-592">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-593">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-593">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-594">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-594">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-595">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-595">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-596">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-596">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-597">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-597">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-598">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-598">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-599">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-599">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-600">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-600">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-601">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-601">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-602">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-602">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-603">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-603">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-604">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-604">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-605">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-606">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-606">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-607">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-607">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-608">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-608">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-609">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-609">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-610">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-610">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-611">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-611">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-612">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-612">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-613">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-613">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-614">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-614">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-615">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-615">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-616">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-616">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-617">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-617">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-618">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-618">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-619">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-619">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-620">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-620">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-621">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-621">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-622">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-622">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-623">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-623">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-624">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-624">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-625">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-625">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-626">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-626">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-627">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-627">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-628">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-628">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-629">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-629">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-630">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-630">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-631">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-631">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a><span data-ttu-id="3b079-632">DXGI_FORMAT_R16G16B16A16 \_ float<sup>FNS</sup> (10)</span><span class="sxs-lookup"><span data-stu-id="3b079-632">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FNS</sup> (10)</span></span>
| <span data-ttu-id="3b079-633">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-633">Target</span></span> | <span data-ttu-id="3b079-634">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-634">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-635">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-635">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-636">64</span><span class="sxs-lookup"><span data-stu-id="3b079-636">64</span></span> |
| <span data-ttu-id="3b079-637">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-637">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-638">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-638">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-639">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-639">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-640">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-640">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-641">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-641">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-642">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-642">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-643">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-643">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-644">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-644">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-645">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-645">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-646">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-646">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-647">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-647">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-648">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-648">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-649">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-649">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-650">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-650">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-651">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-651">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-652">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-652">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-653">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-653">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-654">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-654">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-655">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-655">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-656">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-656">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-657">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-657">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-658">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-658">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-659">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-659">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-660">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-660">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-661">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-661">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-662">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-662">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-663">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-663">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-664">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-664">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-665">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-665">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-666">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-666">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-667">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-667">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-668">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-668">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-669">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-669">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-670">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-670">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-671">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-671">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-672">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-672">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-673">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-673">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-674">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-674">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-675">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-675">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-676">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-676">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-677">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-677">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-678">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-678">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-679">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-679">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-680">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-680">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-682">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-682">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a><span data-ttu-id="3b079-683">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FNS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="3b079-683">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FNS</sup> (11)</span></span>
| <span data-ttu-id="3b079-684">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-684">Target</span></span> | <span data-ttu-id="3b079-685">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-685">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-686">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-686">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-687">64</span><span class="sxs-lookup"><span data-stu-id="3b079-687">64</span></span> |
| <span data-ttu-id="3b079-688">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-688">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-689">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-689">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-690">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-690">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-691">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-691">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-692">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-692">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-693">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-693">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-694">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-694">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-695">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-695">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-696">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-696">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-697">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-697">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-698">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-698">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-699">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-699">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-700">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-700">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-701">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-701">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-702">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-702">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-703">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-703">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-704">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-704">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-705">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-705">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-706">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-706">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-707">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-707">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-708">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-708">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-709">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-709">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-710">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-710">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-711">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-711">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-712">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-712">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-713">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-713">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-714">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-714">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-715">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-715">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-716">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-716">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-717">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-717">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-718">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-718">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-719">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-719">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-720">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-720">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-721">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-721">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-722">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-722">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-723">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-723">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-724">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-724">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-725">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-725">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-726">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-726">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-727">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-727">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-728">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-728">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-729">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-729">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-730">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-730">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-731">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-731">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-732">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-732">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a><span data-ttu-id="3b079-733">DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FNS</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="3b079-733">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FNS</sup> (12)</span></span>
| <span data-ttu-id="3b079-734">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-734">Target</span></span> | <span data-ttu-id="3b079-735">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-735">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-736">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-736">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-737">64</span><span class="sxs-lookup"><span data-stu-id="3b079-737">64</span></span> |
| <span data-ttu-id="3b079-738">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-738">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-739">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-739">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-740">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-740">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-741">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-741">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-742">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-742">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-743">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-743">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-744">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-744">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-745">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-745">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-746">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-746">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-747">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-747">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-748">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-748">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-749">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-749">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-750">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-750">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-751">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-751">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-752">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-752">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-753">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-753">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-754">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-754">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-755">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-755">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-756">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-756">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-757">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-757">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-758">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-758">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-759">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-759">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-760">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-760">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-761">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-761">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-762">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-762">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-763">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-763">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-764">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-764">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-765">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-765">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-766">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-766">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-767">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-767">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-768">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-768">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-769">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-769">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-770">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-770">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-771">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-771">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-772">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-772">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-773">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-773">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-774">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-774">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-775">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-775">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-776">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-776">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-777">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-777">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-778">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-778">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-779">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-779">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-780">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-780">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-781">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-781">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-782">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a><span data-ttu-id="3b079-783">DXGI_FORMAT_R16G16B16A16 \_ SNORM<sup>FNS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="3b079-783">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FNS</sup> (13)</span></span>
| <span data-ttu-id="3b079-784">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-784">Target</span></span> | <span data-ttu-id="3b079-785">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-785">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-786">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-787">64</span><span class="sxs-lookup"><span data-stu-id="3b079-787">64</span></span> |
| <span data-ttu-id="3b079-788">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-788">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-790">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-790">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-791">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-791">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-793">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-793">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-794">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-794">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-795">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-795">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-796">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-796">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-797">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-798">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-798">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-799">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-799">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-800">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-800">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-801">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-801">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-802">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-802">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-803">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-803">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-804">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-804">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-805">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-805">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-806">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-806">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-807">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-807">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-808">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-808">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-809">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-809">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-810">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-810">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-811">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-811">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-812">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-812">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-813">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-813">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-814">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-814">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-815">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-815">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-816">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-816">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-817">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-817">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-818">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-818">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-819">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-819">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-820">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-820">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-821">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-821">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-822">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-822">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-823">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-823">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-824">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-824">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-825">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-825">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-826">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-826">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-827">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-827">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-828">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-828">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-829">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-829">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-830">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-830">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-831">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-831">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-832">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-832">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-833">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-833">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-834">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-834">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a><span data-ttu-id="3b079-835">DXGI_FORMAT_R16G16B16A16 \_ San<sup>FNS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="3b079-835">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FNS</sup> (14)</span></span>
| <span data-ttu-id="3b079-836">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-836">Target</span></span> | <span data-ttu-id="3b079-837">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-837">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-838">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-838">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-839">64</span><span class="sxs-lookup"><span data-stu-id="3b079-839">64</span></span> |
| <span data-ttu-id="3b079-840">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-840">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-842">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-842">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-843">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-843">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-845">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-845">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-846">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-846">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-847">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-847">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-848">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-848">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-849">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-849">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-850">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-850">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-851">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-851">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-852">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-852">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-853">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-853">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-854">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-854">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-855">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-855">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-856">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-856">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-857">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-857">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-858">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-858">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-859">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-859">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-860">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-860">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-861">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-861">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-862">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-862">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-863">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-863">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-864">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-864">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-865">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-865">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-866">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-866">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-867">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-867">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-868">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-868">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-869">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-869">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-870">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-870">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-871">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-871">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-872">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-872">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-873">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-873">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-874">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-874">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-875">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-875">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-876">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-876">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-877">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-877">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-878">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-878">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-879">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-879">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-880">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-880">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-881">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-881">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-882">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-882">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-883">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-883">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-884">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-884">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-885">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-885">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-886">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-886">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="3b079-887">DXGI_FORMAT_R32G32 de \_ <sup>equipos</sup> sin tipo (15)</span><span class="sxs-lookup"><span data-stu-id="3b079-887">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="3b079-888">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-888">Target</span></span> | <span data-ttu-id="3b079-889">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-889">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-890">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-890">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-891">64</span><span class="sxs-lookup"><span data-stu-id="3b079-891">64</span></span> |
| <span data-ttu-id="3b079-892">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-892">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-893">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-893">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-894">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-894">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-895">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-895">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-896">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-896">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-897">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-897">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-898">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-898">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-899">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-899">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-900">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-900">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-901">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-901">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-902">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-902">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-903">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-903">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-904">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-904">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-905">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-905">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-906">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-906">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-907">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-907">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-908">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-908">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-909">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-909">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-910">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-910">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-911">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-912">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-913">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-914">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-915">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-915">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-916">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-916">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-917">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-917">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-918">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-918">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-919">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-919">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-920">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-920">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-921">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-921">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-922">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-922">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-923">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-923">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-924">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-924">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-925">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-925">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-926">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-926">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-927">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-927">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-928">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-928">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-929">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-929">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-930">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-930">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-931">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-931">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-932">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-932">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-933">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-933">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-934">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-934">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-935">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-935">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-936">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-936">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a><span data-ttu-id="3b079-937">DXGI_FORMAT_R32G32 \_ float<sup>FNS</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="3b079-937">DXGI_FORMAT_R32G32\_FLOAT<sup>FNS</sup> (16)</span></span>
| <span data-ttu-id="3b079-938">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-938">Target</span></span> | <span data-ttu-id="3b079-939">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-939">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-940">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-940">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-941">64</span><span class="sxs-lookup"><span data-stu-id="3b079-941">64</span></span> |
| <span data-ttu-id="3b079-942">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-942">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-944">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-944">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-945">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-945">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-947">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-947">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-948">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-948">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-949">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-949">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-950">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-950">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-951">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-951">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-952">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-952">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-953">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-953">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-954">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-954">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-955">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-955">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-956">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-956">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-957">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-957">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-958">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-958">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-959">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-959">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-960">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-960">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-961">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-961">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-962">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-962">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-963">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-963">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-964">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-964">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-965">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-965">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-966">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-966">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-967">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-967">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-968">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-968">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-969">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-969">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-970">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-970">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-971">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-971">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-972">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-972">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-973">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-973">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-974">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-974">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-975">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-975">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-976">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-976">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-977">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-977">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-978">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-978">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-979">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-979">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-980">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-980">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-981">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-981">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-982">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-982">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-983">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-983">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-984">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-984">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-985">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-985">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-986">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-986">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-987">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-987">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-988">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-988">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a><span data-ttu-id="3b079-989">DXGI_FORMAT_R32G32 \_ uint<sup>FNS</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="3b079-989">DXGI_FORMAT_R32G32\_UINT<sup>FNS</sup> (17)</span></span>
| <span data-ttu-id="3b079-990">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-990">Target</span></span> | <span data-ttu-id="3b079-991">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-991">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-992">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-992">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-993">64</span><span class="sxs-lookup"><span data-stu-id="3b079-993">64</span></span> |
| <span data-ttu-id="3b079-994">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-994">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-995">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-995">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-996">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-996">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-997">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-997">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-998">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-998">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-999">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-999">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1000">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1000">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-1001">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1001">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-1002">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1002">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-1003">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1003">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-1004">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1004">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-1005">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1005">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1006">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1006">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1007">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1007">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1008">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1008">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1009">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1009">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-1010">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1010">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1011">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1012">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1012">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1013">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1013">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1014">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1014">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1015">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1015">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1016">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1016">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1017">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1017">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1018">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1018">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1019">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1019">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1020">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1020">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1021">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1021">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1022">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1022">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1023">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1023">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1024">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1024">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1025">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1025">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1026">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1026">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-1027">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1027">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1028">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1028">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1029">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1029">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-1030">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1030">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-1031">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1031">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1032">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1032">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-1033">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1033">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1034">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1034">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1035">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1035">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-1036">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1036">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-1037">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1037">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-1038">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1038">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a><span data-ttu-id="3b079-1039">DXGI_FORMAT_R32G32 \_ San<sup>FNS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="3b079-1039">DXGI_FORMAT_R32G32\_SINT<sup>FNS</sup> (18)</span></span>
| <span data-ttu-id="3b079-1040">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1040">Target</span></span> | <span data-ttu-id="3b079-1041">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1041">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1042">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1042">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1043">64</span><span class="sxs-lookup"><span data-stu-id="3b079-1043">64</span></span> |
| <span data-ttu-id="3b079-1044">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1044">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-1045">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1045">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1046">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1046">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1047">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1047">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1048">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1048">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1049">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1049">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1050">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1050">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-1051">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1051">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-1052">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1052">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-1053">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1053">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-1054">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1054">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-1055">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1055">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1056">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1056">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1057">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1057">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1058">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1058">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1059">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1059">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-1060">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1060">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-1061">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1061">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1062">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1062">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1063">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1063">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1064">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1064">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1065">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1065">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1066">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1066">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1067">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1067">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1068">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1068">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1069">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1069">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1070">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1070">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1071">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1071">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1072">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1072">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1073">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1073">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1074">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1074">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1075">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1075">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1076">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1076">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-1077">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1077">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1078">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1078">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1079">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1079">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-1080">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-1081">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1081">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1082">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1082">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-1083">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1083">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1084">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1084">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1085">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1085">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-1086">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1086">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-1087">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1087">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-1088">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1088">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="3b079-1089">DXGI_FORMAT_R32G8X24 de \_ <sup>equipos</sup> sin tipo (19)</span><span class="sxs-lookup"><span data-stu-id="3b079-1089">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="3b079-1090">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1090">Target</span></span> | <span data-ttu-id="3b079-1091">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1091">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1092">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1092">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1093">64</span><span class="sxs-lookup"><span data-stu-id="3b079-1093">64</span></span> |
| <span data-ttu-id="3b079-1094">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1094">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-1095">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1095">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1096">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1096">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1097">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1097">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1098">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1098">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1099">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1099">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1100">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1100">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-1101">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1101">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-1102">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1102">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-1103">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1103">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-1104">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1104">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-1105">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1105">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1106">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1106">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1107">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1107">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1108">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1108">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1109">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1109">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-1110">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1110">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-1111">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1111">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1112">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1112">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1113">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1113">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1114">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1114">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1115">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1115">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1116">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1116">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1117">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1117">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1118">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1118">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1119">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1119">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1120">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1120">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1121">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1121">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1122">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1122">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1123">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1123">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1124">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1124">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1125">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1125">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1126">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1126">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-1127">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1127">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1128">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1128">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1129">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1129">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-1130">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1130">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-1131">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1131">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1132">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1132">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-1133">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1133">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1134">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1134">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1135">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1135">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-1136">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1136">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-1137">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1137">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-1138">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1138">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a><span data-ttu-id="3b079-1139">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FNS</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="3b079-1139">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FNS</sup> (20)</span></span>
| <span data-ttu-id="3b079-1140">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1140">Target</span></span> | <span data-ttu-id="3b079-1141">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1141">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1142">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1142">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1143">64</span><span class="sxs-lookup"><span data-stu-id="3b079-1143">64</span></span> |
| <span data-ttu-id="3b079-1144">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1144">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-1145">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1145">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1146">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1146">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1147">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1147">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1148">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1148">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1149">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1149">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1150">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1150">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-1151">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1151">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-1152">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1152">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-1153">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1153">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-1154">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1154">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-1155">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1155">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1156">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1156">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1157">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1157">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1158">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1158">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1159">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1159">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-1160">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1160">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-1161">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1161">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1162">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1162">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1163">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1163">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1164">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1164">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1165">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1165">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1166">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1166">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1167">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1167">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1168">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1168">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1169">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1169">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1170">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1170">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1171">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1171">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1172">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1172">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1173">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1173">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1174">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1174">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1175">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1175">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1176">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1176">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-1177">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1177">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1178">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1178">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1179">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1179">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-1180">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1180">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-1181">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1181">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1182">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1182">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-1183">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1183">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1184">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1184">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1185">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1185">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-1186">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1186">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-1187">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1187">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-1188">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1188">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a><span data-ttu-id="3b079-1189">DXGI_FORMAT_R32 \_ float \_ \_ <sup>FNS</sup> typeless X8X24 (21)</span><span class="sxs-lookup"><span data-stu-id="3b079-1189">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FNS</sup> (21)</span></span>
| <span data-ttu-id="3b079-1190">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1190">Target</span></span> | <span data-ttu-id="3b079-1191">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1191">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1192">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1192">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1193">64</span><span class="sxs-lookup"><span data-stu-id="3b079-1193">64</span></span> |
| <span data-ttu-id="3b079-1194">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1194">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-1195">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1195">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1196">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1196">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1197">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1197">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1198">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1198">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1199">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1199">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1200">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1200">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-1201">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1201">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-1202">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1202">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-1203">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1203">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-1204">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1204">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-1205">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1205">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1206">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1206">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1207">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1207">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1208">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1208">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1209">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1209">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-1210">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1210">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-1211">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1211">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1212">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1212">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1213">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1213">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1214">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1214">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1215">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1215">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1216">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1216">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1217">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1217">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1218">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1218">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1219">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1219">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1220">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1220">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1221">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1221">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1222">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1222">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1223">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1223">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1224">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1224">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1225">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1225">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1226">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1226">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-1227">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1227">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1228">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1228">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1229">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1229">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-1230">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1230">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-1231">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1231">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1232">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1232">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-1233">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1233">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1234">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1234">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1235">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1235">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-1236">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1236">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-1237">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1237">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-1238">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1238">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a><span data-ttu-id="3b079-1239">DXGI_FORMAT_X32 \_ \_ G8X24 \_ uint<sup>FNS</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="3b079-1239">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FNS</sup> (22)</span></span>
| <span data-ttu-id="3b079-1240">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1240">Target</span></span> | <span data-ttu-id="3b079-1241">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1241">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1242">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1242">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1243">64</span><span class="sxs-lookup"><span data-stu-id="3b079-1243">64</span></span> |
| <span data-ttu-id="3b079-1244">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1244">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-1245">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1245">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1246">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1246">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1247">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1247">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1248">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1248">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1249">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1249">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1250">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1250">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-1251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1251">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-1252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1252">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-1253">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1253">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-1254">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1254">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-1255">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1255">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1256">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1256">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1257">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1257">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1258">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1258">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1259">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1259">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-1260">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1260">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-1261">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1261">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1262">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1262">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1263">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1263">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1264">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1264">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1265">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1265">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1266">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1266">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1267">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1267">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1268">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1268">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1269">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1269">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1270">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1270">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1271">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1271">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1272">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1272">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1273">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1273">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1274">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1274">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1275">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1275">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1276">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1276">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-1277">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1277">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1278">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1278">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1279">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1279">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-1280">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1280">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-1281">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1281">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1282">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1282">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-1283">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1283">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1284">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1284">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1285">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1285">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-1286">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1286">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-1287">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1287">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-1288">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1288">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="3b079-1289">DXGI_FORMAT_R10G10B10A2 de \_ <sup>equipos</sup> sin tipo (23)</span><span class="sxs-lookup"><span data-stu-id="3b079-1289">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="3b079-1290">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1290">Target</span></span> | <span data-ttu-id="3b079-1291">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1291">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1292">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1292">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1293">32</span><span class="sxs-lookup"><span data-stu-id="3b079-1293">32</span></span> |
| <span data-ttu-id="3b079-1294">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1294">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-1295">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1295">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1296">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1296">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1297">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1297">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1298">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1298">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1299">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1299">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1300">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1300">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-1301">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1301">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-1302">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1302">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-1303">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1303">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-1304">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1304">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-1305">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1305">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1306">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1306">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1307">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1307">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1308">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1308">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1309">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1309">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-1310">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1310">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-1311">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1311">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1312">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1312">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1313">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1313">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1314">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1314">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1315">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1315">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1316">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1316">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1317">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1317">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1318">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1318">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1319">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1319">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1320">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1320">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1321">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1321">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1322">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1322">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1323">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1323">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1324">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1324">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1325">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1325">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1326">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1326">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-1327">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1327">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1328">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1328">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1329">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1329">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-1330">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1330">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-1331">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1331">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1332">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1332">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-1333">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1333">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1334">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1334">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1335">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1335">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-1336">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1336">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-1337">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1337">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-1338">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1338">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a><span data-ttu-id="3b079-1339">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FNS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="3b079-1339">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FNS</sup> (24)</span></span>
| <span data-ttu-id="3b079-1340">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1340">Target</span></span> | <span data-ttu-id="3b079-1341">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1341">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1342">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1342">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1343">32</span><span class="sxs-lookup"><span data-stu-id="3b079-1343">32</span></span> |
| <span data-ttu-id="3b079-1344">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1344">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-1345">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1345">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1346">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1346">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1347">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1347">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1348">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1348">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1349">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1349">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1350">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1350">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-1351">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1351">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-1352">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1352">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-1353">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1353">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-1354">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1354">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-1355">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1355">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1356">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1356">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1357">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1357">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1358">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1358">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1359">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1359">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-1360">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1360">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-1361">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1361">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1362">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1362">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1363">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1363">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1364">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1364">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1365">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1365">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1366">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1366">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1367">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1367">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1368">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1368">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1369">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1369">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1370">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1370">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1371">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1371">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1372">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1372">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1373">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1373">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1374">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1374">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1375">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1375">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1376">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1376">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-1377">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1377">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1378">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1378">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1379">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1379">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-1380">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1380">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-1381">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1381">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1382">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1382">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-1383">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1383">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1384">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1385">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-1386">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-1387">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1387">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1389">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1389">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a><span data-ttu-id="3b079-1390">DXGI_FORMAT_R10G10B10A2 \_ uint<sup>FNS</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="3b079-1390">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FNS</sup> (25)</span></span>
| <span data-ttu-id="3b079-1391">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1391">Target</span></span> | <span data-ttu-id="3b079-1392">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1392">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1393">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1394">32</span><span class="sxs-lookup"><span data-stu-id="3b079-1394">32</span></span> |
| <span data-ttu-id="3b079-1395">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1395">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-1396">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1396">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1397">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1397">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1398">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1398">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1399">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1399">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1400">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1400">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1401">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1401">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-1402">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1402">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-1403">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1403">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-1404">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1404">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-1405">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1405">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-1406">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1406">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1407">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1407">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1408">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1408">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1409">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1409">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1410">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1410">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-1411">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1411">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-1412">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1412">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1413">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1413">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1414">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1414">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1415">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1415">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1416">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1416">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1417">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1417">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1418">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1418">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1419">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1419">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1420">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1420">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1421">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1421">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1422">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1422">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1423">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1423">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1424">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1424">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1425">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1425">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1426">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1426">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1427">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1427">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-1428">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1428">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1429">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1429">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1430">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1430">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-1431">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1431">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-1432">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1432">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1433">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-1434">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1434">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1435">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1435">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1436">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1436">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-1437">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1437">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-1438">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1438">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-1439">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1439">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a><span data-ttu-id="3b079-1440">DXGI_FORMAT_R10G10B10 \_ la \_ inclinación de XR \_ a2 \_ UNORM<sup>FNS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="3b079-1440">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FNS</sup> (89)</span></span>
| <span data-ttu-id="3b079-1441">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1441">Target</span></span> | <span data-ttu-id="3b079-1442">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1442">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1443">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1443">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1444">32</span><span class="sxs-lookup"><span data-stu-id="3b079-1444">32</span></span> |
| <span data-ttu-id="3b079-1445">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1445">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-1446">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1446">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1447">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1447">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1448">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1448">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1449">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1449">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1450">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1450">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1451">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1451">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-1452">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1452">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-1453">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1453">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-1454">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1454">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-1455">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1455">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-1456">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1456">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1457">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1457">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1458">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1458">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1459">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1459">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1460">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1460">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-1461">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1461">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-1462">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1462">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1463">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1463">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1464">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1465">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1466">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1467">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1468">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1468">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1469">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1470">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1471">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1472">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1473">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1473">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1474">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1475">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1476">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1477">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1477">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-1478">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1478">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1479">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1479">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1480">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1480">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-1481">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1481">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-1482">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1482">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1483">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1483">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-1484">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1484">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1485">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1485">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1486">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1486">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-1487">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1487">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-1488">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1488">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-1489">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1489">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="3b079-1490">DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="3b079-1490">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="3b079-1491">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1491">Target</span></span> | <span data-ttu-id="3b079-1492">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1492">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1493">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1493">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1494">32</span><span class="sxs-lookup"><span data-stu-id="3b079-1494">32</span></span> |
| <span data-ttu-id="3b079-1495">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1495">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-1496">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1496">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1497">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1498">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1499">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1500">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1501">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-1502">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1502">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-1503">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1503">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-1504">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1504">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-1505">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1505">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-1506">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1507">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1508">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1508">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1509">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1510">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1510">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-1511">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1511">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-1512">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1512">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1513">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1513">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1514">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1514">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1515">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1515">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1516">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1516">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1517">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1517">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1518">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1518">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1519">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1519">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1520">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1520">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1521">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1521">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1522">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1522">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1523">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1523">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1524">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1524">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1525">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1525">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1526">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1526">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1527">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1527">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-1528">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1528">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1529">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1529">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1530">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1530">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-1531">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1531">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-1532">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1532">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1533">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1533">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-1534">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1534">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1535">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1535">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1536">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1536">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-1537">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1537">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-1538">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1538">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-1539">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1539">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="3b079-1540">DXGI_FORMAT_R8G8B8A8 de \_ <sup>equipos</sup> sin tipo (27)</span><span class="sxs-lookup"><span data-stu-id="3b079-1540">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="3b079-1541">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1541">Target</span></span> | <span data-ttu-id="3b079-1542">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1542">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1543">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1543">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1544">32</span><span class="sxs-lookup"><span data-stu-id="3b079-1544">32</span></span> |
| <span data-ttu-id="3b079-1545">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1545">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-1546">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1546">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1547">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1547">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1548">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1548">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1549">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1549">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1550">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1550">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1551">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1551">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-1552">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1552">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-1553">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1553">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-1554">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1554">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-1555">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1555">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-1556">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1556">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1557">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1557">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1558">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1558">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1559">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1559">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1560">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1560">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-1561">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1561">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-1562">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1562">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1563">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1563">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1564">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1564">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1565">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1566">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1567">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1568">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1568">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1569">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1569">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1570">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1570">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1571">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1571">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1572">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1572">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1573">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1573">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1574">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1574">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1575">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1575">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1576">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1576">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1577">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1577">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-1578">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1578">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1579">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1579">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1580">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1580">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-1581">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1581">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-1582">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1582">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1583">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1583">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-1584">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1584">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1585">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1585">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1586">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1586">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-1587">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1587">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-1588">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1588">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-1589">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1589">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a><span data-ttu-id="3b079-1590">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FNS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="3b079-1590">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FNS</sup> (28)</span></span>
| <span data-ttu-id="3b079-1591">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1591">Target</span></span> | <span data-ttu-id="3b079-1592">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1592">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1593">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1593">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1594">32</span><span class="sxs-lookup"><span data-stu-id="3b079-1594">32</span></span> |
| <span data-ttu-id="3b079-1595">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1595">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1597">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1597">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1598">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1598">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1600">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1601">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1602">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1603">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1605">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1605">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1607">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1607">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1609">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1609">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1611">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1611">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1613">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1614">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1615">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1615">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1616">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1617">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1617">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1619">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1619">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1621">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1621">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1623">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1623">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1625">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1625">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1626">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1626">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1627">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1627">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1628">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1628">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1629">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1629">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1630">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1630">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1631">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1631">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1632">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1632">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1633">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1633">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1634">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1634">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1635">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1635">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1636">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1636">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1637">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1637">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1638">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1638">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1640">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1640">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-1642">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1642">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-1644">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1644">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-1646">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1646">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1648">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1648">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1649">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1649">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1651">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1651">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1652">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1652">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1653">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1653">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-1655">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1655">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1657">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1657">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1659">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1659">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a><span data-ttu-id="3b079-1660">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRGB<sup>FNS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="3b079-1660">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FNS</sup> (29)</span></span>
| <span data-ttu-id="3b079-1661">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1661">Target</span></span> | <span data-ttu-id="3b079-1662">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1662">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1663">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1663">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1664">32</span><span class="sxs-lookup"><span data-stu-id="3b079-1664">32</span></span> |
| <span data-ttu-id="3b079-1665">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1665">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1667">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1667">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1668">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1668">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1669">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1669">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1670">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1670">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1671">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1671">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1672">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1672">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1674">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1674">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1676">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1676">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1678">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1678">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1680">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1680">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1682">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1682">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1683">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1683">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1684">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1684">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1685">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1685">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1686">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1686">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1688">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1688">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1690">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1690">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1692">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1692">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1694">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1694">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1695">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1695">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1696">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1696">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1697">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1697">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1698">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1698">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1699">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1699">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1700">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1700">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1701">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1701">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1702">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1702">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1703">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1703">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1704">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1704">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1705">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1705">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1706">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1706">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1707">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1707">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1709">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1709">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-1711">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1711">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-1713">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1713">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-1715">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1715">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1717">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1717">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1718">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1718">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1720">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1720">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1721">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1721">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1722">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1722">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-1724">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1724">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1726">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1726">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1728">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1728">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a><span data-ttu-id="3b079-1729">DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FNS</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="3b079-1729">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FNS</sup> (30)</span></span>
| <span data-ttu-id="3b079-1730">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1730">Target</span></span> | <span data-ttu-id="3b079-1731">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1731">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1732">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1732">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1733">32</span><span class="sxs-lookup"><span data-stu-id="3b079-1733">32</span></span> |
| <span data-ttu-id="3b079-1734">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1734">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1736">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1736">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1737">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1737">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1739">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1739">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1740">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1740">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1741">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1741">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1742">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1742">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-1743">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1743">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-1744">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1744">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-1745">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1745">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-1746">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1746">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-1747">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1747">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1748">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1748">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1749">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1749">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1750">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1750">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1751">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1751">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-1752">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1752">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-1753">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1753">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1754">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1754">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1755">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1755">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1756">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1756">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1757">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1757">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1758">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1758">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1759">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1759">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1760">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1760">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1761">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1761">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1762">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1762">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1763">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1763">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1764">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1764">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1765">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1765">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1766">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1766">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1767">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1767">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1768">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1768">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-1769">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1769">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1770">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1770">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1771">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1771">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-1772">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1772">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-1773">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1773">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1774">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1774">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-1775">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1775">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1776">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1776">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1777">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1777">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-1778">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1778">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-1779">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1779">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-1780">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1780">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a><span data-ttu-id="3b079-1781">DXGI_FORMAT_R8G8B8A8 \_ SNORM<sup>FNS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="3b079-1781">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FNS</sup> (31)</span></span>
| <span data-ttu-id="3b079-1782">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1782">Target</span></span> | <span data-ttu-id="3b079-1783">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1783">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1784">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1784">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1785">32</span><span class="sxs-lookup"><span data-stu-id="3b079-1785">32</span></span> |
| <span data-ttu-id="3b079-1786">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1786">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1788">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1788">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1789">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1789">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1790">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1790">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1791">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1791">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1792">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1792">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1793">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1793">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1795">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1795">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-1796">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1796">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1798">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1798">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1800">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1800">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1802">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1802">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1803">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1803">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1804">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1804">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1805">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1805">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1806">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1806">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1808">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1808">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-1809">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1809">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1810">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1810">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1811">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1812">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1812">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1813">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1813">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1814">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1814">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1815">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1815">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1816">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1816">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1817">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1817">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1818">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1818">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1819">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1819">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1820">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1820">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1821">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1821">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1822">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1822">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1823">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1823">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1824">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1824">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-1826">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1826">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1827">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1827">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1828">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1828">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-1829">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1829">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-1830">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1830">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1831">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1831">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-1832">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1832">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1833">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1833">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1834">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1834">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-1835">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1835">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-1836">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1836">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-1837">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1837">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a><span data-ttu-id="3b079-1838">DXGI_FORMAT_R8G8B8A8 \_ Sint<sup>FNS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="3b079-1838">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FNS</sup> (32)</span></span>
| <span data-ttu-id="3b079-1839">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1839">Target</span></span> | <span data-ttu-id="3b079-1840">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1840">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1841">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1841">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1842">32</span><span class="sxs-lookup"><span data-stu-id="3b079-1842">32</span></span> |
| <span data-ttu-id="3b079-1843">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1843">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-1844">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1844">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1845">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1845">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1846">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1846">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1847">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1847">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1848">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1848">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1849">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1849">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-1850">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1850">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-1851">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1851">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-1852">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1852">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-1853">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1853">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-1854">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1854">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1855">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1855">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1856">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1856">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1857">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1857">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1858">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1858">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-1859">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1859">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-1860">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1860">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1861">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1861">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1862">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1862">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1863">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1863">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1864">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1864">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1865">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1865">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1866">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1866">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1867">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1867">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1868">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1868">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1869">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1869">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1870">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1870">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1871">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1871">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1872">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1872">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1873">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1873">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1874">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1874">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1875">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1875">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-1876">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1876">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1877">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1877">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1878">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1878">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-1879">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1879">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-1880">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1880">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1881">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1881">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-1882">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1882">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1883">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1883">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1884">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1884">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-1885">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1885">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-1886">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1886">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-1887">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1887">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="3b079-1888">DXGI_FORMAT_R16G16 de \_ <sup>equipos</sup> sin tipo (33)</span><span class="sxs-lookup"><span data-stu-id="3b079-1888">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="3b079-1889">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1889">Target</span></span> | <span data-ttu-id="3b079-1890">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1890">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1891">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1891">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1892">32</span><span class="sxs-lookup"><span data-stu-id="3b079-1892">32</span></span> |
| <span data-ttu-id="3b079-1893">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1893">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-1894">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1894">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1895">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1895">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1896">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1896">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1897">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1897">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1898">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1898">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1899">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1899">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-1900">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1900">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-1901">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1901">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-1902">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1902">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-1903">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1903">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-1904">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1904">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1905">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1905">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1906">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1906">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1907">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1907">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1908">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1908">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-1909">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1909">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-1910">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1910">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1911">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1911">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1912">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1912">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1913">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1913">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1914">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1914">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1915">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1915">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1916">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1916">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1917">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1917">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1918">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1918">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1919">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1919">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1920">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1920">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1921">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1921">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1922">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1922">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1923">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1923">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1924">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1924">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1925">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1925">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-1926">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1926">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1927">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1927">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1928">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1928">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-1929">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1929">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-1930">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1930">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1931">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1931">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-1932">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1932">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1933">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1933">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1934">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1934">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-1935">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1935">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-1936">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1936">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-1937">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1937">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a><span data-ttu-id="3b079-1938">DXGI_FORMAT_R16G16 \_ float<sup>FNS</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="3b079-1938">DXGI_FORMAT_R16G16\_FLOAT<sup>FNS</sup> (34)</span></span>
| <span data-ttu-id="3b079-1939">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1939">Target</span></span> | <span data-ttu-id="3b079-1940">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1940">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1941">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1941">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1942">32</span><span class="sxs-lookup"><span data-stu-id="3b079-1942">32</span></span> |
| <span data-ttu-id="3b079-1943">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1943">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-1944">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1944">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1945">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1945">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1946">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1946">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1947">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1947">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1948">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1948">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1949">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1949">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-1950">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-1950">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-1951">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-1951">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-1952">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-1952">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-1953">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-1953">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-1954">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-1954">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-1955">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-1955">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-1956">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-1956">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-1957">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-1957">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-1958">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-1958">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-1959">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-1959">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-1960">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-1960">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1961">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-1961">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1962">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-1962">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-1963">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-1963">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-1964">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1964">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1965">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-1965">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-1966">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-1966">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-1967">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-1967">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-1968">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1968">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-1969">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-1969">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-1970">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1970">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-1971">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-1971">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-1972">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-1972">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-1973">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1973">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1974">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-1974">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-1975">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-1975">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-1976">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-1976">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1977">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1977">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-1978">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-1978">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-1979">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-1979">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-1980">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-1980">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-1981">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-1981">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-1982">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-1982">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-1983">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1983">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-1984">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1984">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-1985">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-1985">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-1986">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-1986">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-1987">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-1987">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a><span data-ttu-id="3b079-1988">DXGI_FORMAT_R16G16 \_ UNORM<sup>FNS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="3b079-1988">DXGI_FORMAT_R16G16\_UNORM<sup>FNS</sup> (35)</span></span>
| <span data-ttu-id="3b079-1989">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-1989">Target</span></span> | <span data-ttu-id="3b079-1990">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-1990">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-1991">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-1991">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-1992">32</span><span class="sxs-lookup"><span data-stu-id="3b079-1992">32</span></span> |
| <span data-ttu-id="3b079-1993">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-1993">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-1994">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-1994">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1995">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1995">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1996">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-1996">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1997">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-1997">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-1998">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-1998">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-1999">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-1999">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-2000">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2000">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2001">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2001">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2002">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2002">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-2003">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2003">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-2004">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2004">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2005">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2005">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2006">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2006">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2007">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2007">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2008">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2008">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-2009">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2009">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2010">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2010">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2011">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2011">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2012">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2012">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2013">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2013">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2014">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2014">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2015">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2015">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2016">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2016">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2017">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2017">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2018">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2018">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2019">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2019">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2020">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2020">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2021">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2021">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2022">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2022">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2023">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2023">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2024">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2024">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2025">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2025">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-2026">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2026">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2027">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2027">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2028">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2028">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-2029">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2029">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2030">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2030">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2031">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2031">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2032">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2032">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2033">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2033">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2034">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2034">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2035">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2035">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2036">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2036">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-2037">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2037">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a><span data-ttu-id="3b079-2038">DXGI_FORMAT_R16G16 \_ uint<sup>FNS</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="3b079-2038">DXGI_FORMAT_R16G16\_UINT<sup>FNS</sup> (36)</span></span>
| <span data-ttu-id="3b079-2039">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2039">Target</span></span> | <span data-ttu-id="3b079-2040">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2040">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2041">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2041">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2042">32</span><span class="sxs-lookup"><span data-stu-id="3b079-2042">32</span></span> |
| <span data-ttu-id="3b079-2043">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2043">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-2044">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2044">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2045">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2045">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2046">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2046">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2047">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2047">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2048">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2048">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2049">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2049">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-2050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2050">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2051">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2051">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2052">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2052">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-2053">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2053">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-2054">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2054">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2055">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2055">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2056">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2056">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2057">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2057">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2058">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2058">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-2059">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2059">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2060">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2060">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2061">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2061">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2062">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2062">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2063">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2063">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2064">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2064">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2065">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2065">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2066">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2066">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2067">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2067">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2068">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2068">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2069">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2069">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2070">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2070">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2071">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2071">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2072">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2072">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2073">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2073">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2074">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2074">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2075">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2075">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-2076">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2076">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2077">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2077">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2078">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2078">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-2079">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2079">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2080">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2080">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2081">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2081">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2082">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2082">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2083">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2083">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2084">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2084">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2085">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2085">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2086">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2086">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-2087">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2087">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a><span data-ttu-id="3b079-2088">DXGI_FORMAT_R16G16 \_ SNORM<sup>FNS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="3b079-2088">DXGI_FORMAT_R16G16\_SNORM<sup>FNS</sup> (37)</span></span>
| <span data-ttu-id="3b079-2089">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2089">Target</span></span> | <span data-ttu-id="3b079-2090">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2090">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2091">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2091">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2092">32</span><span class="sxs-lookup"><span data-stu-id="3b079-2092">32</span></span> |
| <span data-ttu-id="3b079-2093">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2093">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2095">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2095">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2096">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2096">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2098">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2098">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2099">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2099">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2100">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2100">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2101">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2101">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2103">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2103">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2104">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2104">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2105">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2105">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2107">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2107">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-2108">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2108">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2109">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2109">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2110">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2110">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2111">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2111">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2112">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2112">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2114">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2114">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2115">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2115">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2116">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2116">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2117">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2117">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2118">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2118">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2119">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2119">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2120">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2120">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2121">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2121">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2122">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2122">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2123">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2123">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2124">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2124">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2125">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2125">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2126">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2126">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2127">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2127">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2128">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2128">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2129">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2129">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2130">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2130">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2132">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2132">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2133">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2133">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2134">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2134">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-2135">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2135">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2136">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2136">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2137">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2137">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2138">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2138">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2139">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2139">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2140">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2140">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2141">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2141">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2142">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2142">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-2143">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2143">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a><span data-ttu-id="3b079-2144">DXGI_FORMAT_R16G16 \_ Sint<sup>FNS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="3b079-2144">DXGI_FORMAT_R16G16\_SINT<sup>FNS</sup> (38)</span></span>
| <span data-ttu-id="3b079-2145">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2145">Target</span></span> | <span data-ttu-id="3b079-2146">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2146">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2147">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2147">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2148">32</span><span class="sxs-lookup"><span data-stu-id="3b079-2148">32</span></span> |
| <span data-ttu-id="3b079-2149">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2149">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2151">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2151">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2152">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2152">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2154">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2154">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2155">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2155">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2156">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2156">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2157">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2157">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-2158">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2158">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2159">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2159">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2160">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2160">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-2161">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2161">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-2162">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2162">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2163">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2163">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2164">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2164">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2165">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2165">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2166">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2166">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-2167">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2167">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2168">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2168">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2169">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2169">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2170">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2170">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2171">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2171">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2172">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2172">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2173">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2173">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2174">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2174">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2175">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2175">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2176">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2176">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2177">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2177">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2178">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2178">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2179">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2179">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2180">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2180">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2181">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2181">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2182">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2182">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2183">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2183">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-2184">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2184">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2185">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2185">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2186">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2186">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-2187">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2187">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2188">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2188">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2189">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2189">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2190">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2190">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2191">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2191">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2192">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2192">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2193">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2193">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2194">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2194">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-2195">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2195">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="3b079-2196">DXGI_FORMAT_R32 de \_ <sup>equipos</sup> sin tipo (39)</span><span class="sxs-lookup"><span data-stu-id="3b079-2196">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="3b079-2197">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2197">Target</span></span> | <span data-ttu-id="3b079-2198">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2198">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2199">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2199">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2200">32</span><span class="sxs-lookup"><span data-stu-id="3b079-2200">32</span></span> |
| <span data-ttu-id="3b079-2201">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2201">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-2202">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2202">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2203">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2203">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2204">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2204">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2205">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2205">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2206">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2206">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2207">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2207">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-2208">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2208">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2209">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2209">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2210">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2210">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-2211">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2211">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-2212">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2212">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2213">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2213">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2214">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2214">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2215">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2215">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2216">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2216">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-2217">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2217">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2218">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2218">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2219">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2219">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2220">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2220">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2221">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2221">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2222">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2222">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2223">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2223">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2224">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2224">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2225">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2225">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2226">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2226">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2227">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2227">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2228">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2228">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2229">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2229">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2230">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2230">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2231">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2231">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2232">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2232">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2233">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2233">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-2234">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2234">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2235">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2235">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2236">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2236">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-2237">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2237">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2238">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2238">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2239">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2239">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2240">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2240">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2241">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2241">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2242">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2242">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2243">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2243">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2244">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2244">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-2245">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2245">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a><span data-ttu-id="3b079-2246">DXGI_FORMAT_D32 \_ float<sup>FNS</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="3b079-2246">DXGI_FORMAT_D32\_FLOAT<sup>FNS</sup> (40)</span></span>
| <span data-ttu-id="3b079-2247">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2247">Target</span></span> | <span data-ttu-id="3b079-2248">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2248">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2249">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2249">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2250">32</span><span class="sxs-lookup"><span data-stu-id="3b079-2250">32</span></span> |
| <span data-ttu-id="3b079-2251">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2251">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-2252">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2252">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2253">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2253">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2254">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2254">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2255">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2255">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2256">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2256">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2257">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2257">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-2258">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2258">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2259">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2259">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2260">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2260">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-2261">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2261">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-2262">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2262">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2263">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2263">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2264">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2264">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2265">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2265">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2266">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2266">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-2267">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2267">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2268">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2268">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2269">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2269">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2270">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2270">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2271">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2271">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2272">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2272">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2273">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2273">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2274">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2274">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2275">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2275">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2276">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2276">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2277">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2277">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2278">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2278">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2279">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2279">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2280">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2280">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2281">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2281">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2282">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2282">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2283">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2283">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-2284">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2284">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2285">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2285">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2286">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2286">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-2287">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2287">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2288">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2288">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2289">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2289">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2290">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2290">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2291">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2291">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2292">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2292">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2293">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2293">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2294">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2294">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-2295">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2295">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a><span data-ttu-id="3b079-2296">DXGI_FORMAT_R32 \_ float<sup>FNS</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="3b079-2296">DXGI_FORMAT_R32\_FLOAT<sup>FNS</sup> (41)</span></span>
| <span data-ttu-id="3b079-2297">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2297">Target</span></span> | <span data-ttu-id="3b079-2298">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2298">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2299">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2299">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2300">32</span><span class="sxs-lookup"><span data-stu-id="3b079-2300">32</span></span> |
| <span data-ttu-id="3b079-2301">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2301">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2303">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2303">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2304">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2304">Input Assembler Vertex Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2306">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2306">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2307">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2307">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2308">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2308">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2309">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2309">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-2310">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2310">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2311">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2311">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2312">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2312">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-2313">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2313">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-2314">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2314">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2315">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2315">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2316">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2316">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2317">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2317">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2318">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2318">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-2319">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2319">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2320">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2320">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2321">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2321">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2322">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2322">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2323">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2323">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2324">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2324">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2325">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2325">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2326">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2326">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2327">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2327">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2328">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2328">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2329">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2329">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2330">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2330">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2331">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2331">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2332">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2332">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2333">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2333">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2334">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2334">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2335">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2335">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-2336">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2336">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2337">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2337">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2338">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2338">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-2339">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2339">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2340">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2340">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2341">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2341">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2342">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2342">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2343">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2343">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2344">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2344">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2345">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2345">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2346">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2346">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-2347">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2347">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a><span data-ttu-id="3b079-2348">DXGI_FORMAT_R32 \_ uint<sup>FNS</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="3b079-2348">DXGI_FORMAT_R32\_UINT<sup>FNS</sup> (42)</span></span>
| <span data-ttu-id="3b079-2349">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2349">Target</span></span> | <span data-ttu-id="3b079-2350">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2350">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2351">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2351">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2352">32</span><span class="sxs-lookup"><span data-stu-id="3b079-2352">32</span></span> |
| <span data-ttu-id="3b079-2353">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2353">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-2354">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2354">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2355">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2355">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2356">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2356">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2357">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2357">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2358">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2358">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2359">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2359">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-2360">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2360">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2361">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2361">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2362">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2362">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-2363">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2363">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-2364">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2364">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2365">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2365">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2366">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2366">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2367">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2367">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2368">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2368">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-2369">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2369">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2370">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2370">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2371">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2371">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2372">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2372">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2373">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2373">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2374">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2374">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2375">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2375">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2376">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2376">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2377">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2377">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2378">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2378">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2379">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2379">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2380">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2380">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2381">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2381">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2382">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2382">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2383">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2383">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2384">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2384">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2385">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2385">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-2386">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2386">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2387">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2387">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2388">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2388">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-2389">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2389">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2390">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2390">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2391">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2391">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2392">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2392">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2393">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2393">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2394">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2394">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2395">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2395">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2396">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2396">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-2397">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2397">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a><span data-ttu-id="3b079-2398">DXGI_FORMAT_R32 \_ Sint<sup>FNS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="3b079-2398">DXGI_FORMAT_R32\_SINT<sup>FNS</sup> (43)</span></span>
| <span data-ttu-id="3b079-2399">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2399">Target</span></span> | <span data-ttu-id="3b079-2400">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2400">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2401">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2401">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2402">32</span><span class="sxs-lookup"><span data-stu-id="3b079-2402">32</span></span> |
| <span data-ttu-id="3b079-2403">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2403">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-2404">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2404">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2405">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2405">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2406">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2406">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2407">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2407">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2408">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2408">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2409">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2409">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-2410">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2410">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2411">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2411">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2412">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2412">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-2413">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2413">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-2414">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2415">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2416">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2416">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2417">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2418">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2418">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-2419">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2419">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2420">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2420">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2421">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2421">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2422">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2422">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2423">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2423">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2424">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2424">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2425">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2425">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2426">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2426">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2427">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2427">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2428">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2428">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2429">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2429">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2430">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2430">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2431">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2431">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2432">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2432">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2433">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2433">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2434">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2434">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2435">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2435">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-2436">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2436">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2437">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2437">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2438">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2438">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-2439">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2439">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2440">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2440">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2441">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2442">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2442">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2443">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2443">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2444">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2444">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2445">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2445">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2446">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2446">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-2447">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2447">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="3b079-2448">DXGI_FORMAT_R24G8 de \_ <sup>equipos</sup> sin tipo (44)</span><span class="sxs-lookup"><span data-stu-id="3b079-2448">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="3b079-2449">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2449">Target</span></span> | <span data-ttu-id="3b079-2450">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2450">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2451">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2451">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2452">32</span><span class="sxs-lookup"><span data-stu-id="3b079-2452">32</span></span> |
| <span data-ttu-id="3b079-2453">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2453">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-2454">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2454">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2455">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2455">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2456">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2456">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2457">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2457">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2458">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2458">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2459">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2459">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-2460">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2460">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2461">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2461">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2462">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2462">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-2463">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2463">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-2464">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2464">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2465">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2465">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2466">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2466">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2467">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2467">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2468">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2468">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-2469">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2470">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2471">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2472">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2473">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2474">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2475">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2476">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2476">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2477">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2478">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2479">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2480">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2481">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2481">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2482">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2483">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2484">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2485">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2485">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-2486">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2486">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2487">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2487">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2488">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2488">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-2489">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2489">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2490">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2490">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2491">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2491">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2492">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2492">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2493">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2493">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2494">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2494">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2495">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2495">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2496">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2496">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-2497">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2497">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a><span data-ttu-id="3b079-2498">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FNS</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="3b079-2498">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FNS</sup> (45)</span></span>
| <span data-ttu-id="3b079-2499">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2499">Target</span></span> | <span data-ttu-id="3b079-2500">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2500">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2501">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2501">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2502">32</span><span class="sxs-lookup"><span data-stu-id="3b079-2502">32</span></span> |
| <span data-ttu-id="3b079-2503">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2503">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2505">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2505">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2506">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2506">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2507">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2507">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2508">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2508">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2509">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2509">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2510">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2510">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2512">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2513">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2514">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2514">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-2515">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2515">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-2516">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2516">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2517">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2517">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2518">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2518">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2519">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2519">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2520">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2520">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-2521">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2521">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2522">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2522">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2523">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2523">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2524">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2524">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2525">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2525">Depth/Stencil Target</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2527">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2527">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2528">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2528">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2529">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2529">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2530">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2530">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2531">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2531">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2532">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2532">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2533">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2533">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2534">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2534">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2535">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2535">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2536">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2536">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2537">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2537">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2538">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2538">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-2539">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2539">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-2541">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2541">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-2543">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2543">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-2545">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2545">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2546">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2546">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2547">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2547">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2548">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2548">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2549">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2549">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2550">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2550">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2551">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2551">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2552">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2552">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-2553">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2553">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a><span data-ttu-id="3b079-2554">DXGI_FORMAT_R24 \_ UNORM \_ X8 \_ <sup>FNS</sup> sin tipo (46)</span><span class="sxs-lookup"><span data-stu-id="3b079-2554">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FNS</sup> (46)</span></span>
| <span data-ttu-id="3b079-2555">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2555">Target</span></span> | <span data-ttu-id="3b079-2556">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2556">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2557">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2557">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2558">32</span><span class="sxs-lookup"><span data-stu-id="3b079-2558">32</span></span> |
| <span data-ttu-id="3b079-2559">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2559">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-2560">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2560">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2561">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2561">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2562">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2562">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2563">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2563">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2564">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2564">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2565">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2565">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-2566">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2566">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2567">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2567">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2568">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2568">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-2569">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2569">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-2570">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2570">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2571">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2571">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2572">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2572">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2573">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2573">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2574">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2574">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-2575">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2575">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2576">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2576">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2577">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2577">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2578">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2578">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2579">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2579">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2580">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2580">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2581">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2581">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2582">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2582">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2583">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2583">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2584">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2584">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2585">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2585">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2586">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2586">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2587">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2587">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2588">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2588">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2589">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2589">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2590">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2590">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2591">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2591">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-2592">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2592">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2593">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2593">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2594">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2594">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-2595">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2595">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2596">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2596">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2597">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2597">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2598">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2598">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2599">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2599">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2600">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2600">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2601">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2601">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2602">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2602">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-2603">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2603">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a><span data-ttu-id="3b079-2604">DXGI_FORMAT_X24 \_ tipos de \_ G8 \_ <sup>FNS</sup> (47)</span><span class="sxs-lookup"><span data-stu-id="3b079-2604">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FNS</sup> (47)</span></span>
| <span data-ttu-id="3b079-2605">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2605">Target</span></span> | <span data-ttu-id="3b079-2606">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2606">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2607">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2607">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2608">32</span><span class="sxs-lookup"><span data-stu-id="3b079-2608">32</span></span> |
| <span data-ttu-id="3b079-2609">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2609">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-2610">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2610">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2611">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2611">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2612">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2612">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2613">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2613">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2614">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2614">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2615">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2615">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-2616">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2616">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2617">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2617">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2618">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2618">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-2619">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2619">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-2620">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2620">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2621">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2621">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2622">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2622">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2623">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2623">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2624">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2624">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-2625">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2625">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2626">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2626">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2627">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2627">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2628">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2628">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2629">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2629">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2630">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2630">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2631">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2631">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2632">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2632">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2633">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2633">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2634">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2634">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2635">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2635">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2636">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2636">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2637">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2637">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2638">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2638">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2639">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2639">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2640">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2640">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2641">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2641">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-2642">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2642">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2643">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2643">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2644">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2644">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-2645">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2645">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2646">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2646">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2647">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2647">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2648">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2648">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2649">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2649">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2650">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2650">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2651">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2651">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2652">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2652">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-2653">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2653">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="3b079-2654">DXGI_FORMAT_R8G8 de \_ <sup>equipos</sup> sin tipo (48)</span><span class="sxs-lookup"><span data-stu-id="3b079-2654">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="3b079-2655">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2655">Target</span></span> | <span data-ttu-id="3b079-2656">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2656">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2657">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2657">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2658">16</span><span class="sxs-lookup"><span data-stu-id="3b079-2658">16</span></span> |
| <span data-ttu-id="3b079-2659">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2659">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-2660">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2660">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2661">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2661">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2662">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2662">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2663">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2663">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2664">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2664">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2665">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2665">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-2666">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2666">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2667">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2667">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2668">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2668">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-2669">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2669">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-2670">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2670">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2671">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2671">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2672">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2672">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2673">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2673">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2674">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2674">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-2675">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2675">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2676">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2676">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2677">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2677">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2678">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2678">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2679">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2679">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2680">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2680">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2681">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2681">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2682">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2682">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2683">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2683">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2684">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2684">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2685">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2685">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2686">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2686">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2687">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2687">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2688">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2688">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2689">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2689">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2690">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2690">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2691">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2691">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-2692">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2692">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2693">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2693">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2694">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2694">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-2695">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2696">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2696">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2697">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2697">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2698">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2698">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2699">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2699">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2700">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2700">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2701">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2701">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2702">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2702">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-2703">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2703">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a><span data-ttu-id="3b079-2704">DXGI_FORMAT_R8G8 \_ UNORM<sup>FNS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="3b079-2704">DXGI_FORMAT_R8G8\_UNORM<sup>FNS</sup> (49)</span></span>
| <span data-ttu-id="3b079-2705">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2705">Target</span></span> | <span data-ttu-id="3b079-2706">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2706">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2707">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2707">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2708">16</span><span class="sxs-lookup"><span data-stu-id="3b079-2708">16</span></span> |
| <span data-ttu-id="3b079-2709">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2709">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2711">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2711">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2712">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2712">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2713">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2713">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2714">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2714">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2715">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2715">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2716">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2716">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2718">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2718">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2719">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2719">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2720">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2720">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2722">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2722">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2724">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2724">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2725">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2725">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2726">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2726">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2727">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2727">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2728">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2728">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-2729">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2729">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2730">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2730">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2732">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2732">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2734">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2734">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2735">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2735">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2736">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2736">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2737">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2737">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2738">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2738">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2739">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2739">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2740">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2740">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2741">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2741">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2742">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2742">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2743">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2743">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2744">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2744">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2745">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2745">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2746">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2746">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2747">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2747">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2749">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2749">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2750">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2750">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2751">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2751">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-2752">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2752">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2753">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2753">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2754">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2754">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2755">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2755">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2756">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2756">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2757">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2757">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2758">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2758">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2759">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2759">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2761">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2761">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a><span data-ttu-id="3b079-2762">DXGI_FORMAT_R8G8 \_ uint<sup>FNS</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="3b079-2762">DXGI_FORMAT_R8G8\_UINT<sup>FNS</sup> (50)</span></span>
| <span data-ttu-id="3b079-2763">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2763">Target</span></span> | <span data-ttu-id="3b079-2764">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2764">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2765">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2765">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2766">16</span><span class="sxs-lookup"><span data-stu-id="3b079-2766">16</span></span> |
| <span data-ttu-id="3b079-2767">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2767">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-2768">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2768">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2769">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2769">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2770">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2770">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2771">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2771">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2772">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2772">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2773">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2773">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-2774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2774">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2775">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2775">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2776">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2776">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-2777">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2777">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-2778">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2778">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2779">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2779">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2780">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2780">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2781">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2781">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2782">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2782">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-2783">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2783">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2784">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2784">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2785">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2785">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2786">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2786">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2787">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2787">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2788">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2788">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2789">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2789">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2790">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2790">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2791">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2791">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2792">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2792">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2793">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2793">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2794">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2794">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2795">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2795">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2796">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2796">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2797">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2797">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2798">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2798">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2799">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2799">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-2800">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2800">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2801">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2801">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2802">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2802">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-2803">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2803">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2804">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2804">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2805">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2805">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2806">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2806">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2807">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2807">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2808">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2808">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2809">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2809">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2810">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2810">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-2811">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a><span data-ttu-id="3b079-2812">DXGI_FORMAT_R8G8 \_ SNORM<sup>FNS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="3b079-2812">DXGI_FORMAT_R8G8\_SNORM<sup>FNS</sup> (51)</span></span>
| <span data-ttu-id="3b079-2813">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2813">Target</span></span> | <span data-ttu-id="3b079-2814">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2814">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2815">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2816">16</span><span class="sxs-lookup"><span data-stu-id="3b079-2816">16</span></span> |
| <span data-ttu-id="3b079-2817">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2817">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2819">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2819">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2820">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2821">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2822">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2823">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2824">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2824">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2826">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2826">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2827">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2828">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2828">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2830">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2830">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2832">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2832">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2833">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2833">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2834">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2834">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2835">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2835">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2836">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2836">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2838">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2838">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2839">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2839">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2840">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2841">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2842">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2842">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2843">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2843">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2844">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2844">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2845">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2845">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2846">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2846">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2847">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2847">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2848">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2848">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2849">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2849">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2850">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2850">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2851">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2851">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2852">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2852">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2853">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2853">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2854">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2854">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-2856">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2856">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2857">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2857">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2858">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2858">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-2859">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2859">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2860">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2860">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2861">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2861">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2862">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2862">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2863">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2863">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2864">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2864">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2865">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2865">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2866">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2866">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-2867">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2867">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a><span data-ttu-id="3b079-2868">DXGI_FORMAT_R8G8 \_ Sint<sup>FNS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="3b079-2868">DXGI_FORMAT_R8G8\_SINT<sup>FNS</sup> (52)</span></span>
| <span data-ttu-id="3b079-2869">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2869">Target</span></span> | <span data-ttu-id="3b079-2870">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2870">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2871">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2871">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2872">16</span><span class="sxs-lookup"><span data-stu-id="3b079-2872">16</span></span> |
| <span data-ttu-id="3b079-2873">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2873">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-2874">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2874">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2875">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2875">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2876">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2876">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2877">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2877">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2878">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2878">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2879">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2879">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-2880">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2880">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2881">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2881">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2882">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2882">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-2883">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2883">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-2884">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2884">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2885">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2885">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2886">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2886">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2887">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2887">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2888">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2888">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-2889">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2889">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2890">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2890">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2891">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2891">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2892">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2893">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2894">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2895">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2896">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2896">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2897">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2898">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2899">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2900">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2901">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2901">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2902">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2903">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2904">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2905">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2905">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-2906">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2906">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2907">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2907">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2908">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2908">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-2909">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2909">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2910">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2910">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2911">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2911">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2912">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2912">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2913">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2913">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2914">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2914">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2915">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2915">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2916">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2916">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-2917">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2917">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="3b079-2918">DXGI_FORMAT_R16 de \_ <sup>equipos</sup> sin tipo (53)</span><span class="sxs-lookup"><span data-stu-id="3b079-2918">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="3b079-2919">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2919">Target</span></span> | <span data-ttu-id="3b079-2920">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2920">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2921">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2921">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2922">16</span><span class="sxs-lookup"><span data-stu-id="3b079-2922">16</span></span> |
| <span data-ttu-id="3b079-2923">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2923">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-2924">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2924">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2925">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2925">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2926">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2926">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2927">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2927">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2928">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2928">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2929">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2929">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-2930">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2930">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2931">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2931">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2932">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2932">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-2933">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-2934">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2935">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2936">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2936">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2937">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2938">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2938">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-2939">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2939">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2940">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2940">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2941">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2941">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2942">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2942">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2943">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2943">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2944">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2944">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2945">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2945">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2946">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2946">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2947">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2947">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2948">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2948">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2949">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2949">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-2950">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2950">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-2951">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-2951">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-2952">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2952">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-2953">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2953">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2954">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-2954">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-2955">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-2955">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-2956">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-2956">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2957">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2957">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2958">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-2958">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-2959">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-2959">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-2960">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-2960">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-2961">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-2961">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-2962">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-2962">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-2963">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2963">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-2964">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2964">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-2965">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-2965">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-2966">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-2966">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-2967">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-2967">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a><span data-ttu-id="3b079-2968">DXGI_FORMAT_R16 \_ float<sup>FNS</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="3b079-2968">DXGI_FORMAT_R16\_FLOAT<sup>FNS</sup> (54)</span></span>
| <span data-ttu-id="3b079-2969">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-2969">Target</span></span> | <span data-ttu-id="3b079-2970">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-2970">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-2971">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-2971">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-2972">16</span><span class="sxs-lookup"><span data-stu-id="3b079-2972">16</span></span> |
| <span data-ttu-id="3b079-2973">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2973">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-2974">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-2974">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2975">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2975">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2976">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-2976">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2977">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-2977">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-2978">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-2978">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-2979">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-2979">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-2980">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-2980">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-2981">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-2981">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-2982">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-2982">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-2983">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-2983">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-2984">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-2984">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-2985">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-2985">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-2986">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-2986">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-2987">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-2987">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-2988">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-2988">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-2989">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-2989">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-2990">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-2990">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2991">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-2991">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-2992">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-2992">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-2993">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-2993">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-2994">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-2994">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2995">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-2995">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-2996">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-2996">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-2997">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-2997">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-2998">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-2998">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-2999">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-2999">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3000">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3000">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3001">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3001">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3002">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3002">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3003">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3003">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3004">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3004">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3005">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3005">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-3006">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3006">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3007">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3007">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3008">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3008">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-3009">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3010">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3010">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3011">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3011">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3012">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3012">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3013">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3013">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3014">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3014">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3015">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3015">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3016">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3016">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-3017">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3017">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a><span data-ttu-id="3b079-3018">DXGI_FORMAT_D16 \_ UNORM<sup>FNS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="3b079-3018">DXGI_FORMAT_D16\_UNORM<sup>FNS</sup> (55)</span></span>
| <span data-ttu-id="3b079-3019">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3019">Target</span></span> | <span data-ttu-id="3b079-3020">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3020">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3021">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3021">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3022">16</span><span class="sxs-lookup"><span data-stu-id="3b079-3022">16</span></span> |
| <span data-ttu-id="3b079-3023">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3023">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3025">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3025">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3026">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3026">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3027">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3027">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3028">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3028">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3029">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3029">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3030">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3030">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3032">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3032">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-3033">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3033">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-3034">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3034">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-3035">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3035">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-3036">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3036">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3037">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3037">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3038">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3038">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3039">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3039">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3040">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3040">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-3041">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3041">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3042">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3042">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3043">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3043">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3044">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3044">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3045">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3045">Depth/Stencil Target</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3047">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3047">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3048">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3048">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3049">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3049">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3050">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3050">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3051">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3051">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3052">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3052">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3053">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3053">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3054">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3054">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3055">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3055">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3056">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3056">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3057">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3057">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3058">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3058">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-3059">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3059">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-3061">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3061">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-3063">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3063">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-3065">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3065">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3066">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3066">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3067">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3068">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3069">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3070">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3070">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3071">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3071">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3072">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3072">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-3073">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3073">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a><span data-ttu-id="3b079-3074">DXGI_FORMAT_R16 \_ UNORM<sup>FNS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="3b079-3074">DXGI_FORMAT_R16\_UNORM<sup>FNS</sup> (56)</span></span>
| <span data-ttu-id="3b079-3075">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3075">Target</span></span> | <span data-ttu-id="3b079-3076">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3076">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3077">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3077">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3078">16</span><span class="sxs-lookup"><span data-stu-id="3b079-3078">16</span></span> |
| <span data-ttu-id="3b079-3079">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3079">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-3080">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3080">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3081">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3081">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3082">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3082">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3083">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3083">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3084">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3084">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3085">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3085">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-3086">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3086">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-3087">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3087">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-3088">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3088">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-3089">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3089">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-3090">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3090">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3091">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3091">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3092">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3092">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3093">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3093">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3094">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3094">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-3095">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3095">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3096">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3096">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3097">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3097">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3098">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3099">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-3100">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3101">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3102">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3102">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3103">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3103">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3104">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3104">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3105">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3105">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3106">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3106">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3107">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3107">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3108">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3108">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3109">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3109">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3110">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3110">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3111">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3111">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-3112">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3112">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3113">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3113">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3114">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3114">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-3115">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3115">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3116">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3116">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3117">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3117">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3118">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3118">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3119">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3119">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3120">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3120">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3121">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3121">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3122">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3122">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-3123">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3123">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a><span data-ttu-id="3b079-3124">DXGI_FORMAT_R16 \_ uint<sup>FNS</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="3b079-3124">DXGI_FORMAT_R16\_UINT<sup>FNS</sup> (57)</span></span>
| <span data-ttu-id="3b079-3125">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3125">Target</span></span> | <span data-ttu-id="3b079-3126">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3126">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3127">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3127">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3128">16</span><span class="sxs-lookup"><span data-stu-id="3b079-3128">16</span></span> |
| <span data-ttu-id="3b079-3129">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3129">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3131">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3131">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3132">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3132">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3133">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3133">Input Assembler Index Buffer</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3135">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3135">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3136">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3136">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3137">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3137">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-3138">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3138">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-3139">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3139">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-3140">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3140">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-3141">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3141">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-3142">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3142">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3143">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3143">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3144">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3144">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3145">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3145">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3146">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3146">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-3147">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3147">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3148">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3148">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3149">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3149">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3150">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3150">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3151">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3151">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-3152">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3152">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3153">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3153">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3154">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3154">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3155">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3155">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3156">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3156">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3157">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3157">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3158">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3158">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3159">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3159">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3160">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3160">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3161">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3161">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3162">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3162">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3163">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3163">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-3164">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3164">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3165">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3165">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3166">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3166">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-3167">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3167">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3168">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3168">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3169">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3169">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3170">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3170">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3171">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3171">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3172">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3172">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3173">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3173">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3174">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3174">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-3175">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3175">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a><span data-ttu-id="3b079-3176">DXGI_FORMAT_R16 \_ SNORM<sup>FNS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="3b079-3176">DXGI_FORMAT_R16\_SNORM<sup>FNS</sup> (58)</span></span>
| <span data-ttu-id="3b079-3177">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3177">Target</span></span> | <span data-ttu-id="3b079-3178">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3178">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3179">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3179">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3180">16</span><span class="sxs-lookup"><span data-stu-id="3b079-3180">16</span></span> |
| <span data-ttu-id="3b079-3181">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3181">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-3182">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3182">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3183">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3183">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3184">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3184">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3185">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3185">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3186">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3186">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3187">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-3188">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3188">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-3189">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3189">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-3190">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3190">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-3191">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3191">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-3192">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3192">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3193">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3193">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3194">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3194">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3195">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3195">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3196">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3196">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-3197">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3197">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3198">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3198">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3199">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3199">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3200">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3200">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3201">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3201">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-3202">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3202">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3203">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3203">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3204">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3204">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3205">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3205">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3206">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3206">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3207">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3207">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3208">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3208">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3209">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3209">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3210">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3210">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3211">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3211">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3212">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3212">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3213">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3213">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-3214">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3214">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3215">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3215">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3216">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3216">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-3217">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3217">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3218">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3218">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3219">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3219">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3220">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3220">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3221">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3221">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3222">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3222">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3223">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3223">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3224">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3224">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-3225">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3225">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a><span data-ttu-id="3b079-3226">DXGI_FORMAT_R16 \_ Sint<sup>FNS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="3b079-3226">DXGI_FORMAT_R16\_SINT<sup>FNS</sup> (59)</span></span>
| <span data-ttu-id="3b079-3227">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3227">Target</span></span> | <span data-ttu-id="3b079-3228">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3228">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3229">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3229">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3230">16</span><span class="sxs-lookup"><span data-stu-id="3b079-3230">16</span></span> |
| <span data-ttu-id="3b079-3231">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3231">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-3232">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3232">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3233">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3233">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3234">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3234">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3235">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3235">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3236">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3236">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3237">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3237">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-3238">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3238">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-3239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3239">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-3240">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3240">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-3241">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3241">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-3242">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3242">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3243">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3243">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3244">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3244">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3245">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3245">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3246">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3246">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-3247">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3247">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3248">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3248">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3249">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3249">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3250">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3250">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3251">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3251">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-3252">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3252">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3253">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3253">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3254">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3254">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3255">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3255">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3256">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3256">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3257">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3257">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3258">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3258">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3259">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3259">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3260">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3260">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3261">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3261">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3262">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3262">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3263">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3263">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-3264">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3264">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3265">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3265">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3266">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3266">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-3267">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3267">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3268">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3268">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3269">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3269">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3270">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3270">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3271">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3271">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3272">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3272">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3273">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3273">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3274">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3274">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-3275">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3275">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="3b079-3276">DXGI_FORMAT_R8 de \_ <sup>equipos</sup> sin tipo (60)</span><span class="sxs-lookup"><span data-stu-id="3b079-3276">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="3b079-3277">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3277">Target</span></span> | <span data-ttu-id="3b079-3278">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3278">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3279">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3279">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3280">8</span><span class="sxs-lookup"><span data-stu-id="3b079-3280">8</span></span> |
| <span data-ttu-id="3b079-3281">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3281">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-3282">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3282">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3283">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3283">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3284">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3284">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3285">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3285">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3286">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3286">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3287">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3287">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-3288">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3288">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-3289">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3289">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-3290">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3290">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-3291">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3291">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-3292">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3293">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3294">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3294">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3295">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3295">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3296">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3296">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-3297">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3297">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3298">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3298">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3299">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3299">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3300">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3300">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3301">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3301">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-3302">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3302">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3303">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3303">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3304">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3304">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3305">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3305">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3306">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3306">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3307">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3307">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3308">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3308">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3309">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3309">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3310">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3310">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3311">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3311">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3312">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3312">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3313">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3313">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-3314">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3314">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3315">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3315">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3316">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3316">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-3317">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3317">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3318">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3318">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3319">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3319">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3320">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3320">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3321">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3321">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3322">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3322">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3323">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3323">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3324">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3324">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-3325">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3325">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a><span data-ttu-id="3b079-3326">DXGI_FORMAT_R8 \_ UNORM<sup>FNS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="3b079-3326">DXGI_FORMAT_R8\_UNORM<sup>FNS</sup> (61)</span></span>
| <span data-ttu-id="3b079-3327">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3327">Target</span></span> | <span data-ttu-id="3b079-3328">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3328">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3329">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3329">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3330">8</span><span class="sxs-lookup"><span data-stu-id="3b079-3330">8</span></span> |
| <span data-ttu-id="3b079-3331">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3331">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3333">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3333">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3334">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3334">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3335">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3335">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3336">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3336">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3337">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3337">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3338">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3338">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3340">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3340">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3342">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3342">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3344">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3344">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3346">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3346">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3348">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3348">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3349">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3349">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3350">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3350">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3351">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3351">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3352">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3352">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3354">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3354">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3355">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3355">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3357">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3357">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3359">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3359">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3360">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3360">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-3361">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3361">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3362">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3362">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3363">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3363">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3364">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3364">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3365">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3365">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3366">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3366">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3367">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3367">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3368">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3368">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3369">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3369">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3370">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3370">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3371">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3371">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3372">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3372">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3374">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3374">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3375">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3375">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3376">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3376">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-3377">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3377">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3378">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3378">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3379">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3379">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3380">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3380">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3381">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3381">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3382">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3382">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3383">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3383">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3384">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3384">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3386">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3386">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a><span data-ttu-id="3b079-3387">DXGI_FORMAT_R8 \_ uint<sup>FNS</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="3b079-3387">DXGI_FORMAT_R8\_UINT<sup>FNS</sup> (62)</span></span>
| <span data-ttu-id="3b079-3388">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3388">Target</span></span> | <span data-ttu-id="3b079-3389">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3389">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3390">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3390">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3391">8</span><span class="sxs-lookup"><span data-stu-id="3b079-3391">8</span></span> |
| <span data-ttu-id="3b079-3392">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3392">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-3393">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3393">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3394">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3394">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3395">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3395">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3396">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3396">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3397">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3397">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3398">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3398">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-3399">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3399">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-3400">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3400">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-3401">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3401">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-3402">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3402">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-3403">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3403">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3404">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3404">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3405">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3405">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3406">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3406">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3407">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3407">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-3408">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3408">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3409">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3409">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3410">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3410">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3411">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3411">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3412">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3412">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-3413">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3413">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3414">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3414">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3415">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3415">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3416">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3416">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3417">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3417">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3418">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3418">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3419">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3419">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3420">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3420">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3421">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3421">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3422">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3422">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3423">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3423">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3424">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3424">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-3425">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3425">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3426">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3426">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3427">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3427">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-3428">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3428">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3429">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3429">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3430">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3430">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3431">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3431">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3432">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3432">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3433">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3433">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3434">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3434">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3435">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3435">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-3436">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3436">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a><span data-ttu-id="3b079-3437">DXGI_FORMAT_R8 \_ SNORM<sup>FNS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="3b079-3437">DXGI_FORMAT_R8\_SNORM<sup>FNS</sup> (63)</span></span>
| <span data-ttu-id="3b079-3438">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3438">Target</span></span> | <span data-ttu-id="3b079-3439">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3439">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3440">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3440">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3441">8</span><span class="sxs-lookup"><span data-stu-id="3b079-3441">8</span></span> |
| <span data-ttu-id="3b079-3442">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3442">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-3443">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3443">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3444">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3444">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3445">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3446">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3447">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3448">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-3449">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3449">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-3450">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3450">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-3451">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3451">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-3452">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3452">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-3453">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3454">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3455">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3455">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3456">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3457">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3457">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-3458">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3458">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3459">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3459">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3460">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3460">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3461">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3461">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3462">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3462">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-3463">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3463">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3464">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3464">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3465">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3465">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3466">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3466">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3467">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3467">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3468">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3468">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3469">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3469">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3470">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3470">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3471">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3471">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3472">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3472">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3473">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3473">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3474">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3474">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-3475">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3475">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3476">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3476">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3477">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3477">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-3478">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3478">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3479">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3479">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3480">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3480">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3481">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3481">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3482">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3482">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3483">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3483">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3484">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3484">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3485">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3485">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-3486">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3486">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a><span data-ttu-id="3b079-3487">DXGI_FORMAT_R8 \_ Sint<sup>FNS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="3b079-3487">DXGI_FORMAT_R8\_SINT<sup>FNS</sup> (64)</span></span>
| <span data-ttu-id="3b079-3488">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3488">Target</span></span> | <span data-ttu-id="3b079-3489">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3489">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3490">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3490">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3491">8</span><span class="sxs-lookup"><span data-stu-id="3b079-3491">8</span></span> |
| <span data-ttu-id="3b079-3492">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3492">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-3493">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3493">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3494">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3494">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3495">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3495">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3496">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3496">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3497">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3497">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3498">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3498">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-3499">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3499">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-3500">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3500">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-3501">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3501">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-3502">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3502">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-3503">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3503">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3504">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3504">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3505">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3505">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3506">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3506">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3507">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3507">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-3508">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3508">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3509">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3509">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3510">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3510">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3511">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3511">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3512">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3512">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-3513">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3513">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3514">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3514">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3515">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3515">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3516">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3516">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3517">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3517">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3518">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3518">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3519">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3519">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3520">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3520">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3521">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3521">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3522">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3522">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3523">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3523">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3524">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3524">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-3525">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3525">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3526">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3526">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3527">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3527">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-3528">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3528">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3529">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3529">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3530">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3530">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3531">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3531">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3532">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3532">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3533">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3533">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3534">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3534">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3535">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3535">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-3536">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3536">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="3b079-3537">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="3b079-3537">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="3b079-3538">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3538">Target</span></span> | <span data-ttu-id="3b079-3539">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3539">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3540">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3540">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3541">8</span><span class="sxs-lookup"><span data-stu-id="3b079-3541">8</span></span> |
| <span data-ttu-id="3b079-3542">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3542">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3544">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3544">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3545">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3545">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3546">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3546">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3547">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3547">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3548">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3548">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3549">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3549">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3551">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3551">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-3552">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3552">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-3553">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3553">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3555">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3555">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3557">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3557">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3558">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3558">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3559">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3559">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3560">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3560">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3561">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3561">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-3562">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3562">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3563">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3563">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3565">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3565">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3567">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3567">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3568">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3568">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-3569">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3569">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3570">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3570">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3571">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3571">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3572">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3572">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3573">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3573">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3574">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3574">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3575">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3575">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3576">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3576">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3577">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3577">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3578">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3578">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3579">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3579">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3580">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3580">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3582">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3582">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3583">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3583">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3584">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3584">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-3585">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3585">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3586">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3586">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3587">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3587">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3588">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3588">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3589">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3590">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3591">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3592">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3592">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3594">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="3b079-3595">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="3b079-3595">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="3b079-3596">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3596">Target</span></span> | <span data-ttu-id="3b079-3597">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3597">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3598">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3599">32</span><span class="sxs-lookup"><span data-stu-id="3b079-3599">32</span></span> |
| <span data-ttu-id="3b079-3600">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3600">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-3601">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3601">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3602">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3602">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3603">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3603">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3604">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3604">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3605">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3605">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3606">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3606">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-3607">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3607">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-3608">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3608">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-3609">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3609">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-3610">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3610">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-3611">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3611">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3612">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3612">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3613">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3613">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3614">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3614">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3615">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3615">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-3616">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3616">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3617">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3617">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3618">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3618">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3619">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3619">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3620">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3620">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-3621">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3621">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3622">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3622">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3623">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3623">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3624">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3624">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3625">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3625">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3626">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3626">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3627">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3627">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3628">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3628">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3629">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3629">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3630">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3630">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3631">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3631">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3632">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3632">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-3633">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3633">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3634">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3634">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3635">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3635">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-3636">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3636">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3637">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3637">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3638">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3638">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3639">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3639">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3640">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3640">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3641">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3641">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3642">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3642">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3643">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3643">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-3644">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3644">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="3b079-3645">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="3b079-3645">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="3b079-3646">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3646">Target</span></span> | <span data-ttu-id="3b079-3647">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3647">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3648">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3648">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3649">16</span><span class="sxs-lookup"><span data-stu-id="3b079-3649">16</span></span> |
| <span data-ttu-id="3b079-3650">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3650">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-3651">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3651">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3652">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3652">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3653">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3653">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3654">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3654">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3655">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3655">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3656">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3656">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-3657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3657">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-3658">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3658">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-3659">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3659">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-3660">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3660">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-3661">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3661">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3662">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3662">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3663">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3663">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3664">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3664">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3665">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3665">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-3666">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3666">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3667">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3667">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3668">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3668">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3669">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3669">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3670">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3670">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-3671">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3671">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3672">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3672">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3673">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3673">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3674">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3674">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3675">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3675">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3676">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3676">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3677">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3677">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3678">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3678">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3679">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3679">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3680">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3680">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3681">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3681">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3682">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3682">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-3683">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3683">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3684">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3684">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3685">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3685">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-3686">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3686">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3687">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3687">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3688">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3688">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3689">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3689">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3690">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3690">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3691">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3691">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3692">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3692">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3693">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3693">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-3694">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3694">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="3b079-3695">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="3b079-3695">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="3b079-3696">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3696">Target</span></span> | <span data-ttu-id="3b079-3697">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3697">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3698">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3698">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3699">16</span><span class="sxs-lookup"><span data-stu-id="3b079-3699">16</span></span> |
| <span data-ttu-id="3b079-3700">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3700">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-3701">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3701">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3702">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3702">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3703">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3703">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3704">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3704">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3705">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3705">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3706">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3706">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-3707">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3707">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-3708">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3708">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-3709">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3709">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-3710">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3710">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-3711">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3711">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3712">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3712">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3713">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3713">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3714">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3714">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3715">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3715">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-3716">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3716">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3717">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3717">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3718">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3718">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3719">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3719">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3720">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3720">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-3721">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3721">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3722">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3722">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3723">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3723">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3724">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3724">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3725">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3725">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3726">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3726">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3727">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3727">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3728">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3728">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3729">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3729">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3730">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3730">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3731">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3731">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3732">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3732">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-3733">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3733">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3734">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3734">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3735">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3735">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-3736">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3736">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3737">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3737">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3738">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3738">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3739">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3739">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3740">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3740">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3741">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3741">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3742">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3742">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3743">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3743">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-3744">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3744">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="3b079-3745">DXGI_FORMAT_BC1 \_ <sup>PCC</sup> sin tipo (70)</span><span class="sxs-lookup"><span data-stu-id="3b079-3745">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="3b079-3746">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3746">Target</span></span> | <span data-ttu-id="3b079-3747">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3747">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3748">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3748">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3749">4</span><span class="sxs-lookup"><span data-stu-id="3b079-3749">4</span></span> |
| <span data-ttu-id="3b079-3750">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3750">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-3751">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3751">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3752">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3752">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3753">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3753">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3754">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3754">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3755">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3755">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3756">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3756">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-3757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3757">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-3758">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3758">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-3759">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3759">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-3760">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3760">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-3761">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3761">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3762">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3762">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3763">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3763">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3764">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3764">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3765">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3765">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-3766">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3766">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3767">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3767">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3768">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3768">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3769">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3769">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3770">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3770">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-3771">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3771">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3772">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3772">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3773">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3773">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3774">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3774">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3775">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3775">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3776">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3776">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3777">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3777">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3778">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3778">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3779">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3779">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3780">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3780">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3781">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3781">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3782">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3782">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-3783">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3783">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3784">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3784">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3785">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3785">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-3786">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3786">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3787">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3787">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3788">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3788">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3789">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3789">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3790">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3790">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3791">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3791">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3792">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3792">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3793">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3793">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-3794">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3794">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a><span data-ttu-id="3b079-3795">DXGI_FORMAT_BC1 \_ UNORM<sup>FNC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="3b079-3795">DXGI_FORMAT_BC1\_UNORM<sup>FNC</sup> (71)</span></span>
| <span data-ttu-id="3b079-3796">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3796">Target</span></span> | <span data-ttu-id="3b079-3797">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3797">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3798">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3798">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3799">4</span><span class="sxs-lookup"><span data-stu-id="3b079-3799">4</span></span> |
| <span data-ttu-id="3b079-3800">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3800">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3802">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3802">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3803">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3803">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3804">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3804">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3805">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3805">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3806">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3806">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3807">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3807">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3809">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3809">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-3810">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3810">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3812">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3812">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3814">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3814">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3816">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3816">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3817">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3817">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3818">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3818">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3819">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3819">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3820">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3820">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3822">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3822">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3823">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3823">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3824">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3824">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3825">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3825">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3826">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3826">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-3827">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3827">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3828">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3828">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3829">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3829">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3830">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3830">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3831">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3831">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3832">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3832">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3833">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3833">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3834">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3834">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3835">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3835">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3836">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3836">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3837">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3837">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3838">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3838">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3840">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3840">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3841">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3841">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3842">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3842">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-3843">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3843">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3844">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3844">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3845">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3845">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3846">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3846">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3847">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3847">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3848">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3848">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3849">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3849">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3850">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3850">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3852">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3852">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a><span data-ttu-id="3b079-3853">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FNC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="3b079-3853">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FNC</sup> (72)</span></span>
| <span data-ttu-id="3b079-3854">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3854">Target</span></span> | <span data-ttu-id="3b079-3855">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3855">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3856">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3856">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3857">4</span><span class="sxs-lookup"><span data-stu-id="3b079-3857">4</span></span> |
| <span data-ttu-id="3b079-3858">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3858">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3860">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3860">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3861">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3861">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3862">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3862">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3863">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3863">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3864">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3864">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3865">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3865">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3867">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3867">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-3868">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3868">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3870">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3870">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3872">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3872">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3874">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3874">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3875">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3875">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3876">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3876">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3877">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3877">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3878">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3878">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3880">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3880">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3881">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3881">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3882">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3883">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3884">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-3885">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3886">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3887">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3887">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3888">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3888">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3889">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3889">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3890">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3890">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3891">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3891">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3892">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3892">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3893">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3893">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3894">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3894">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3895">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3895">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3896">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3896">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3898">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3898">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3899">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3899">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3900">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3900">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-3901">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3901">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3902">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3902">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3903">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3903">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3904">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3904">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3905">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3905">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3906">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3906">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3907">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3907">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3908">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3908">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3910">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3910">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="3b079-3911">DXGI_FORMAT_BC2 \_ <sup>PCC</sup> sin tipo (73)</span><span class="sxs-lookup"><span data-stu-id="3b079-3911">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="3b079-3912">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3912">Target</span></span> | <span data-ttu-id="3b079-3913">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3913">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3914">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3914">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3915">8</span><span class="sxs-lookup"><span data-stu-id="3b079-3915">8</span></span> |
| <span data-ttu-id="3b079-3916">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3916">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-3917">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3917">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3918">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3918">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3919">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3919">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3920">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3920">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3921">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3921">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3922">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3922">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-3923">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3923">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-3924">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3924">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-3925">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3925">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-3926">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3926">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-3927">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3927">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3928">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3928">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3929">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3929">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3930">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3930">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3931">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3931">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-3932">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3932">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3933">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3933">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3934">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3934">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3935">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3935">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3936">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3936">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-3937">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3937">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3938">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3938">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3939">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3939">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3940">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3940">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3941">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3941">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3942">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3942">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3943">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3943">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-3944">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-3944">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-3945">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3945">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-3946">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3946">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3947">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-3947">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-3948">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-3948">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-3949">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-3949">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3950">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3950">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3951">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-3951">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-3952">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-3952">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-3953">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-3953">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-3954">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-3954">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-3955">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-3955">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-3956">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3956">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-3957">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3957">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-3958">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-3958">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-3959">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-3959">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-3960">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-3960">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a><span data-ttu-id="3b079-3961">DXGI_FORMAT_BC2 \_ UNORM<sup>FNC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="3b079-3961">DXGI_FORMAT_BC2\_UNORM<sup>FNC</sup> (74)</span></span>
| <span data-ttu-id="3b079-3962">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-3962">Target</span></span> | <span data-ttu-id="3b079-3963">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-3963">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-3964">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-3964">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-3965">8</span><span class="sxs-lookup"><span data-stu-id="3b079-3965">8</span></span> |
| <span data-ttu-id="3b079-3966">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3966">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3968">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-3968">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3969">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3969">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3970">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-3970">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3971">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-3971">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-3972">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-3972">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-3973">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-3973">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3975">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-3975">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-3976">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-3976">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3978">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-3978">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3980">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-3980">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3982">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-3982">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-3983">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-3983">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-3984">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-3984">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-3985">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-3985">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-3986">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-3986">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-3988">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-3988">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-3989">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-3989">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3990">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-3990">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-3991">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-3991">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-3992">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-3992">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-3993">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-3993">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3994">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-3994">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-3995">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-3995">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-3996">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-3996">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-3997">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3997">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-3998">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-3998">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-3999">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-3999">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-4000">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-4000">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-4001">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4001">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-4002">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4002">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4003">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4003">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4004">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-4004">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4006">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-4006">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4007">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4007">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4008">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-4008">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-4009">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-4009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-4010">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4010">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-4011">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-4011">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-4012">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-4012">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-4013">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4013">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-4014">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4014">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-4015">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4015">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-4016">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-4016">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4018">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-4018">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a><span data-ttu-id="3b079-4019">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FNC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="3b079-4019">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FNC</sup> (75)</span></span>
| <span data-ttu-id="3b079-4020">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-4020">Target</span></span> | <span data-ttu-id="3b079-4021">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-4021">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-4022">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-4022">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-4023">8</span><span class="sxs-lookup"><span data-stu-id="3b079-4023">8</span></span> |
| <span data-ttu-id="3b079-4024">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4024">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4026">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-4026">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4027">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4027">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4028">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4028">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4029">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-4029">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4030">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-4030">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-4031">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-4031">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4033">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-4033">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-4034">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-4034">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4036">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-4036">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4038">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-4038">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4040">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-4040">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-4041">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-4041">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-4042">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-4042">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-4043">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-4043">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-4044">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-4044">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4046">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-4046">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-4047">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-4047">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4048">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-4048">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4049">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-4049">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-4050">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-4050">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-4051">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4051">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4052">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-4052">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4053">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-4053">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-4054">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-4054">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-4055">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4055">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-4056">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-4056">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-4057">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4057">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-4058">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-4058">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-4059">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4059">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-4060">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4060">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4061">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4061">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4062">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-4062">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4064">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-4064">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4065">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4065">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4066">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-4066">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-4067">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-4067">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-4068">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4068">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-4069">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-4069">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-4070">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-4070">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-4071">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4071">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-4072">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4072">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-4073">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4073">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-4074">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-4074">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4076">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-4076">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="3b079-4077">DXGI_FORMAT_BC3 \_ <sup>PCC</sup> sin tipo (76)</span><span class="sxs-lookup"><span data-stu-id="3b079-4077">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="3b079-4078">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-4078">Target</span></span> | <span data-ttu-id="3b079-4079">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-4079">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-4080">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-4080">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-4081">8</span><span class="sxs-lookup"><span data-stu-id="3b079-4081">8</span></span> |
| <span data-ttu-id="3b079-4082">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4082">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-4083">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-4083">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4084">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4085">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4086">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-4086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-4087">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-4088">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-4088">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-4089">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-4089">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-4090">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-4090">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-4091">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-4091">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-4092">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-4092">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-4093">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-4093">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-4094">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-4094">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-4095">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-4095">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-4096">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-4096">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-4097">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-4097">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-4098">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-4098">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-4099">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-4099">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4100">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-4100">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4101">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-4101">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-4102">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-4102">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-4103">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4103">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4104">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-4104">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4105">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-4105">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-4106">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-4106">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-4107">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4107">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-4108">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-4108">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-4109">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4109">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-4110">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-4110">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-4111">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4111">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-4112">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4112">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4113">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4113">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4114">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-4114">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-4115">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-4115">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4116">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4116">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4117">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-4117">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-4118">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-4118">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-4119">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4119">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-4120">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-4120">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-4121">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-4121">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-4122">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4122">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-4123">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4123">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-4124">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4124">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-4125">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-4125">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-4126">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-4126">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a><span data-ttu-id="3b079-4127">DXGI_FORMAT_BC3 \_ UNORM<sup>FNC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="3b079-4127">DXGI_FORMAT_BC3\_UNORM<sup>FNC</sup> (77)</span></span>
| <span data-ttu-id="3b079-4128">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-4128">Target</span></span> | <span data-ttu-id="3b079-4129">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-4129">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-4130">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-4130">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-4131">8</span><span class="sxs-lookup"><span data-stu-id="3b079-4131">8</span></span> |
| <span data-ttu-id="3b079-4132">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4132">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4134">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-4134">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4135">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4135">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4136">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4136">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4137">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-4137">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-4138">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-4139">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-4139">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-4141">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-4142">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-4142">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4144">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-4144">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4146">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-4146">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4148">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-4148">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-4149">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-4149">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-4150">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-4150">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-4151">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-4151">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-4152">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-4152">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4154">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-4154">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-4155">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-4155">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4156">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-4156">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4157">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-4157">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-4158">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-4158">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-4159">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4159">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4160">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-4160">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4161">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-4161">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-4162">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-4162">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-4163">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4163">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-4164">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-4164">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-4165">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4165">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-4166">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-4166">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-4167">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4167">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-4168">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4168">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4169">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4169">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4170">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-4170">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4172">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-4172">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4173">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4173">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4174">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-4174">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-4175">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-4175">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-4176">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4176">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-4177">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-4177">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-4178">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-4178">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-4179">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4179">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-4180">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4180">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-4181">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4181">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-4182">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-4182">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4184">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-4184">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a><span data-ttu-id="3b079-4185">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FNC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="3b079-4185">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FNC</sup> (78)</span></span>
| <span data-ttu-id="3b079-4186">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-4186">Target</span></span> | <span data-ttu-id="3b079-4187">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-4187">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-4188">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-4188">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-4189">8</span><span class="sxs-lookup"><span data-stu-id="3b079-4189">8</span></span> |
| <span data-ttu-id="3b079-4190">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4190">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4192">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-4192">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4193">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4193">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4194">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4194">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4195">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-4195">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4196">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-4196">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-4197">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-4197">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4199">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-4199">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-4200">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-4200">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4202">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-4202">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4204">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-4204">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4206">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-4206">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-4207">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-4207">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-4208">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-4208">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-4209">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-4209">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-4210">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-4210">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4212">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-4212">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-4213">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-4213">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4214">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-4214">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4215">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-4215">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-4216">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-4216">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-4217">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4217">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4218">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-4218">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4219">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-4219">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-4220">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-4220">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-4221">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4221">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-4222">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-4222">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-4223">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4223">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-4224">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-4224">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-4225">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4225">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-4226">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4226">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4227">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4227">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4228">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-4228">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4230">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-4230">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4231">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4231">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4232">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-4232">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-4233">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-4233">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-4234">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4234">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-4235">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-4235">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-4236">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-4236">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-4237">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4237">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-4238">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4238">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-4239">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4239">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-4240">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-4240">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4242">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-4242">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="3b079-4243">DXGI_FORMAT_BC4 \_ <sup>PCC</sup> sin tipo (79)</span><span class="sxs-lookup"><span data-stu-id="3b079-4243">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="3b079-4244">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-4244">Target</span></span> | <span data-ttu-id="3b079-4245">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-4245">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-4246">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-4246">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-4247">4</span><span class="sxs-lookup"><span data-stu-id="3b079-4247">4</span></span> |
| <span data-ttu-id="3b079-4248">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4248">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-4249">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-4249">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4250">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4250">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4251">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4251">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4252">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-4252">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4253">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-4253">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-4254">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-4254">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-4255">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-4255">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-4256">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-4256">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-4257">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-4257">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-4258">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-4258">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-4259">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-4259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-4260">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-4260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-4261">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-4261">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-4262">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-4262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-4263">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-4263">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-4264">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-4264">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-4265">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-4265">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4266">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-4266">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4267">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-4267">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-4268">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-4268">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-4269">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4269">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4270">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-4270">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4271">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-4271">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-4272">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-4272">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-4273">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4273">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-4274">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-4274">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-4275">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4275">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-4276">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-4276">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-4277">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4277">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-4278">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4278">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4279">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4279">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4280">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-4280">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-4281">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-4281">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4282">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4282">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4283">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-4283">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-4284">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-4284">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-4285">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4285">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-4286">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-4286">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-4287">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-4287">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-4288">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4288">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-4289">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4289">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-4290">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4290">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-4291">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-4291">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-4292">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-4292">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a><span data-ttu-id="3b079-4293">DXGI_FORMAT_BC4 \_ UNORM<sup>FNC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="3b079-4293">DXGI_FORMAT_BC4\_UNORM<sup>FNC</sup> (80)</span></span>
| <span data-ttu-id="3b079-4294">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-4294">Target</span></span> | <span data-ttu-id="3b079-4295">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-4295">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-4296">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-4296">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-4297">4</span><span class="sxs-lookup"><span data-stu-id="3b079-4297">4</span></span> |
| <span data-ttu-id="3b079-4298">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4298">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-4299">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-4299">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4300">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4300">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4301">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4301">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4302">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-4302">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4303">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-4303">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-4304">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-4304">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-4305">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-4305">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-4306">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-4306">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-4307">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-4307">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-4308">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-4308">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-4309">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-4309">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-4310">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-4310">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-4311">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-4311">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-4312">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-4312">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-4313">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-4313">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-4314">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-4314">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-4315">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-4315">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4316">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-4316">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4317">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-4317">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-4318">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-4318">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-4319">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4319">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4320">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-4320">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4321">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-4321">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-4322">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-4322">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-4323">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4323">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-4324">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-4324">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-4325">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4325">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-4326">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-4326">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-4327">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4327">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-4328">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4328">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4329">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4329">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4330">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-4330">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-4331">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-4331">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4332">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4332">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4333">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-4333">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-4334">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-4334">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-4335">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4335">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-4336">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-4336">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-4337">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-4337">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-4338">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4338">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-4339">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4339">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-4340">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4340">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-4341">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-4341">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-4342">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-4342">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a><span data-ttu-id="3b079-4343">DXGI_FORMAT_BC4 \_ SNORM<sup>FNC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="3b079-4343">DXGI_FORMAT_BC4\_SNORM<sup>FNC</sup> (81)</span></span>
| <span data-ttu-id="3b079-4344">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-4344">Target</span></span> | <span data-ttu-id="3b079-4345">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-4345">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-4346">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-4346">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-4347">4</span><span class="sxs-lookup"><span data-stu-id="3b079-4347">4</span></span> |
| <span data-ttu-id="3b079-4348">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4348">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-4349">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-4349">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4350">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4350">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4351">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4351">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4352">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-4352">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4353">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-4353">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-4354">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-4354">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-4355">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-4355">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-4356">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-4356">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-4357">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-4357">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-4358">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-4358">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-4359">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-4359">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-4360">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-4360">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-4361">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-4361">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-4362">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-4362">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-4363">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-4363">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-4364">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-4364">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-4365">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-4365">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4366">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-4366">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4367">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-4367">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-4368">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-4368">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-4369">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4369">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4370">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-4370">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4371">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-4371">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-4372">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-4372">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-4373">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4373">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-4374">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-4374">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-4375">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4375">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-4376">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-4376">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-4377">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4377">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-4378">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4378">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4379">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4379">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4380">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-4380">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-4381">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-4381">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4382">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4382">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4383">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-4383">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-4384">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-4384">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-4385">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4385">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-4386">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-4386">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-4387">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-4387">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-4388">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4388">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-4389">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4389">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-4390">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4390">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-4391">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-4391">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-4392">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-4392">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="3b079-4393">DXGI_FORMAT_BC5 \_ <sup>PCC</sup> sin tipo (82)</span><span class="sxs-lookup"><span data-stu-id="3b079-4393">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="3b079-4394">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-4394">Target</span></span> | <span data-ttu-id="3b079-4395">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-4395">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-4396">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-4396">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-4397">8</span><span class="sxs-lookup"><span data-stu-id="3b079-4397">8</span></span> |
| <span data-ttu-id="3b079-4398">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4398">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-4399">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-4399">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4400">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4400">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4401">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4402">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-4402">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4403">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-4403">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-4404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-4404">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-4405">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-4405">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-4406">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-4406">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-4407">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-4407">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-4408">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-4408">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-4409">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-4409">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-4410">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-4410">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-4411">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-4411">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-4412">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-4412">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-4413">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-4413">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-4414">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-4414">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-4415">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-4415">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4416">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-4416">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4417">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-4417">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-4418">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-4418">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-4419">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4419">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4420">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-4420">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4421">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-4421">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-4422">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-4422">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-4423">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4423">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-4424">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-4424">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-4425">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4425">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-4426">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-4426">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-4427">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4427">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-4428">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4428">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4429">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4429">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4430">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-4430">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-4431">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-4431">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4432">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4432">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4433">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-4433">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-4434">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-4434">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-4435">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4435">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-4436">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-4436">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-4437">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-4437">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-4438">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4438">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-4439">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4439">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-4440">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4440">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-4441">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-4441">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-4442">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-4442">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a><span data-ttu-id="3b079-4443">DXGI_FORMAT_BC5 \_ UNORM<sup>FNC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="3b079-4443">DXGI_FORMAT_BC5\_UNORM<sup>FNC</sup> (83)</span></span>
| <span data-ttu-id="3b079-4444">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-4444">Target</span></span> | <span data-ttu-id="3b079-4445">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-4445">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-4446">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-4446">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-4447">8</span><span class="sxs-lookup"><span data-stu-id="3b079-4447">8</span></span> |
| <span data-ttu-id="3b079-4448">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4448">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-4449">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-4449">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4450">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4451">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4452">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-4452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-4453">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-4454">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-4454">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-4455">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-4455">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-4456">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-4456">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-4457">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-4457">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-4458">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-4458">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-4459">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-4459">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-4460">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-4460">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-4461">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-4461">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-4462">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-4462">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-4463">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-4463">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-4464">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-4464">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-4465">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-4465">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4466">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-4466">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4467">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-4467">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-4468">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-4468">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-4469">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4469">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4470">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-4470">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4471">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-4471">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-4472">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-4472">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-4473">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4473">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-4474">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-4474">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-4475">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4475">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-4476">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-4476">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-4477">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4477">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-4478">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4478">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4479">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4479">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4480">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-4480">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-4481">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-4481">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4482">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4482">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4483">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-4483">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-4484">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-4484">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-4485">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4485">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-4486">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-4486">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-4487">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-4487">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-4488">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4488">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-4489">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4489">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-4490">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4490">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-4491">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-4491">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-4492">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-4492">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a><span data-ttu-id="3b079-4493">DXGI_FORMAT_BC5 \_ SNORM<sup>FNC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="3b079-4493">DXGI_FORMAT_BC5\_SNORM<sup>FNC</sup> (84)</span></span>
| <span data-ttu-id="3b079-4494">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-4494">Target</span></span> | <span data-ttu-id="3b079-4495">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-4495">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-4496">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-4496">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-4497">8</span><span class="sxs-lookup"><span data-stu-id="3b079-4497">8</span></span> |
| <span data-ttu-id="3b079-4498">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4498">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-4499">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-4499">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4500">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4500">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4501">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4501">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4502">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-4502">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4503">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-4503">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-4504">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-4504">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-4505">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-4505">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-4506">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-4506">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-4507">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-4507">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-4508">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-4508">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-4509">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-4509">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-4510">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-4510">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-4511">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-4511">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-4512">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-4512">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-4513">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-4513">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-4514">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-4514">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-4515">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-4515">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4516">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-4516">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4517">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-4517">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-4518">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-4518">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-4519">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4519">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4520">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-4520">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4521">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-4521">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-4522">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-4522">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-4523">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4523">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-4524">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-4524">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-4525">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4525">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-4526">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-4526">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-4527">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4527">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-4528">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4528">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4529">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4529">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4530">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-4530">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-4531">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-4531">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4532">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4532">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4533">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-4533">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-4534">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-4534">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-4535">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4535">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-4536">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-4536">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-4537">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-4537">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-4538">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4538">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-4539">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4539">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-4540">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4540">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-4541">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-4541">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-4542">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-4542">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="3b079-4543">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="3b079-4543">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="3b079-4544">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-4544">Target</span></span> | <span data-ttu-id="3b079-4545">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-4545">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-4546">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-4546">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-4547">16</span><span class="sxs-lookup"><span data-stu-id="3b079-4547">16</span></span> |
| <span data-ttu-id="3b079-4548">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4548">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4550">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-4550">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4551">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4551">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4552">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4552">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4553">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-4553">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4554">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-4554">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-4555">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-4555">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4557">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-4557">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-4558">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-4558">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4560">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-4560">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4562">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-4562">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4564">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-4564">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-4565">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-4565">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-4566">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-4566">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-4567">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-4567">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-4568">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-4568">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4570">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-4570">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4572">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-4572">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4574">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-4574">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4576">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-4576">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-4577">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-4577">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-4578">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4578">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4579">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-4579">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4580">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-4580">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-4581">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-4581">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-4582">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4582">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-4583">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-4583">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-4584">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4584">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-4585">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-4585">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-4586">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4586">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-4587">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4587">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4588">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4588">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4589">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-4589">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4591">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-4591">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-4593">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4593">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-4595">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-4595">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-4597">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-4597">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4599">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4599">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-4600">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-4600">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-4601">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-4601">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-4602">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4602">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-4603">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4603">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-4604">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4604">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-4605">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-4605">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-4606">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-4606">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="3b079-4607">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="3b079-4607">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="3b079-4608">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-4608">Target</span></span> | <span data-ttu-id="3b079-4609">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-4609">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-4610">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-4610">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-4611">16</span><span class="sxs-lookup"><span data-stu-id="3b079-4611">16</span></span> |
| <span data-ttu-id="3b079-4612">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4612">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4614">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-4614">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4615">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4615">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4616">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4616">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4617">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-4617">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4618">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-4618">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-4619">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-4619">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4621">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-4621">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-4622">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-4622">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4624">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-4624">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4626">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-4626">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4628">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-4628">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-4629">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-4629">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-4630">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-4630">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-4631">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-4631">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-4632">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-4632">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4634">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-4634">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-4635">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-4635">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4636">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-4636">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4637">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-4637">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-4638">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-4638">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-4639">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4639">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4640">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-4640">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4641">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-4641">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-4642">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-4642">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-4643">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4643">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-4644">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-4644">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-4645">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4645">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-4646">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-4646">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-4647">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4647">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-4648">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4648">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4649">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4649">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4650">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-4650">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4652">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-4652">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4653">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4653">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4654">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-4654">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-4655">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-4655">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-4656">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4656">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-4657">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-4657">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-4658">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-4658">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-4659">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4659">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-4660">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4660">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-4661">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4661">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-4662">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-4662">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-4663">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-4663">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="3b079-4664">DXGI_FORMAT_B8G8R8A8 de \_ <sup>equipos</sup> sin tipo (90)</span><span class="sxs-lookup"><span data-stu-id="3b079-4664">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="3b079-4665">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-4665">Target</span></span> | <span data-ttu-id="3b079-4666">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-4666">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-4667">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-4667">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-4668">32</span><span class="sxs-lookup"><span data-stu-id="3b079-4668">32</span></span> |
| <span data-ttu-id="3b079-4669">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4669">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-4670">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-4670">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4671">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4671">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4672">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4672">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4673">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-4673">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4674">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-4674">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-4675">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-4675">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-4676">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-4676">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-4677">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-4677">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-4678">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-4678">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-4679">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-4679">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-4680">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-4680">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-4681">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-4681">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-4682">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-4682">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-4683">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-4683">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-4684">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-4684">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-4685">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-4685">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-4686">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-4686">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4687">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-4687">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4688">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-4688">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-4689">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-4689">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-4690">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4690">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4691">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-4691">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4692">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-4692">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-4693">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-4693">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-4694">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4694">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-4695">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-4695">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-4696">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4696">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-4697">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-4697">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-4698">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4698">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-4699">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4699">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4700">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4700">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4701">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-4701">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-4702">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-4702">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4703">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4703">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4704">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-4704">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-4705">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-4705">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-4706">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4706">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-4707">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-4707">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-4708">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-4708">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-4709">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4709">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-4710">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4710">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-4711">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4711">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-4712">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-4712">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-4713">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-4713">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a><span data-ttu-id="3b079-4714">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FNS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="3b079-4714">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FNS</sup> (87)</span></span>
| <span data-ttu-id="3b079-4715">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-4715">Target</span></span> | <span data-ttu-id="3b079-4716">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-4716">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-4717">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-4717">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-4718">32</span><span class="sxs-lookup"><span data-stu-id="3b079-4718">32</span></span> |
| <span data-ttu-id="3b079-4719">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4719">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4721">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-4721">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4722">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4722">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4723">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4723">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4724">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-4724">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4725">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-4725">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-4726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-4726">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-4728">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4730">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-4730">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4732">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-4732">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4734">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-4734">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4736">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-4736">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-4737">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-4737">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-4738">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-4738">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-4739">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-4739">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-4740">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-4740">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4742">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-4742">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4744">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-4744">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4746">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-4746">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4748">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-4748">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-4749">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-4749">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-4750">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4750">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4751">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-4751">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4752">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-4752">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-4753">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-4753">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-4754">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4754">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-4755">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-4755">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-4756">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4756">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-4757">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-4757">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-4758">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4758">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-4759">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4759">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4760">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4760">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4761">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-4761">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4763">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-4763">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-4765">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4765">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-4767">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-4767">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-4769">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-4769">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4771">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4771">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-4772">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-4772">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4774">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-4774">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-4775">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4775">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-4776">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4776">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-4778">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4778">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4780">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-4780">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4782">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-4782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a><span data-ttu-id="3b079-4783">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRGB<sup>FNS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="3b079-4783">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FNS</sup> (91)</span></span>
| <span data-ttu-id="3b079-4784">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-4784">Target</span></span> | <span data-ttu-id="3b079-4785">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-4785">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-4786">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-4786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-4787">32</span><span class="sxs-lookup"><span data-stu-id="3b079-4787">32</span></span> |
| <span data-ttu-id="3b079-4788">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4788">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4790">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-4790">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4791">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4791">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4792">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4792">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4793">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-4793">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4794">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-4794">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-4795">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-4795">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-4797">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4799">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-4799">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4801">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-4801">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4803">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-4803">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4805">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-4805">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-4806">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-4806">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-4807">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-4807">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-4808">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-4808">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-4809">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-4809">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4811">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-4811">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4813">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-4813">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4815">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-4815">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4817">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-4817">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-4818">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-4818">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-4819">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4819">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4820">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-4820">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4821">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-4821">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-4822">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-4822">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-4823">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4823">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-4824">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-4824">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-4825">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4825">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-4826">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-4826">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-4827">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4827">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-4828">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4828">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4829">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4829">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4830">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-4830">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4832">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-4832">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-4834">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4834">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-4836">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-4836">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-4838">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-4838">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4840">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4840">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-4841">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-4841">Display Scan-Out</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4843">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-4843">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-4844">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4844">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-4845">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4845">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-4847">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4847">Video Processor Output</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4849">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-4849">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4851">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-4851">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="3b079-4852">DXGI_FORMAT_B8G8R8X8 de \_ <sup>equipos</sup> sin tipo (92)</span><span class="sxs-lookup"><span data-stu-id="3b079-4852">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="3b079-4853">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-4853">Target</span></span> | <span data-ttu-id="3b079-4854">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-4854">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-4855">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-4855">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-4856">32</span><span class="sxs-lookup"><span data-stu-id="3b079-4856">32</span></span> |
| <span data-ttu-id="3b079-4857">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4857">Format Support</span></span> | \- |
| <span data-ttu-id="3b079-4858">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-4858">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4859">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4859">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4860">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4861">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-4861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-4862">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-4863">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-4863">Texture2D</span></span> | \- |
| <span data-ttu-id="3b079-4864">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-4864">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-4865">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-4865">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-4866">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-4866">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-4867">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-4867">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-4868">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-4868">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-4869">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-4869">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-4870">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-4870">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-4871">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-4871">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-4872">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-4872">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-4873">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-4873">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-4874">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-4874">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4875">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-4875">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4876">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-4876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-4877">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-4877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-4878">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4879">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-4879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4880">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-4880">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-4881">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-4881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-4882">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-4883">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-4883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-4884">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-4885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-4885">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-4886">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-4887">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4888">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4889">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-4889">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-4890">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-4890">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4891">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4891">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-4892">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-4892">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-4893">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-4893">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-4894">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4894">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-4895">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-4895">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-4896">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-4896">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-4897">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4897">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-4898">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4898">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-4899">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4899">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-4900">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-4900">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-4901">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-4901">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a><span data-ttu-id="3b079-4902">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FNS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="3b079-4902">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FNS</sup> (88)</span></span>
| <span data-ttu-id="3b079-4903">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-4903">Target</span></span> | <span data-ttu-id="3b079-4904">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-4904">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-4905">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-4905">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-4906">32</span><span class="sxs-lookup"><span data-stu-id="3b079-4906">32</span></span> |
| <span data-ttu-id="3b079-4907">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4907">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4909">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-4909">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4910">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4910">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4911">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4911">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4912">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-4912">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4913">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-4913">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-4914">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-4914">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4916">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-4916">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4918">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-4918">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4920">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-4920">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4922">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-4922">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4924">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-4924">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-4925">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-4925">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-4926">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-4926">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-4927">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-4927">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-4928">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-4928">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4930">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-4930">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4932">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-4932">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4934">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-4934">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4936">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-4936">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-4937">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-4937">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-4938">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4938">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4939">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-4939">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-4940">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-4940">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-4941">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-4941">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-4942">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4942">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-4943">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-4943">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-4944">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4944">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-4945">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-4945">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-4946">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-4946">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-4947">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4947">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4948">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-4948">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-4949">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-4949">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4951">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-4951">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-4953">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4953">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-4955">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-4955">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-4957">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-4957">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4959">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-4959">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-4960">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-4960">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-4961">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-4961">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-4962">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4962">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-4963">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4963">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-4965">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-4965">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-4967">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-4967">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4969">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-4969">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a><span data-ttu-id="3b079-4970">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRGB<sup>FNS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="3b079-4970">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FNS</sup> (93)</span></span>
| <span data-ttu-id="3b079-4971">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-4971">Target</span></span> | <span data-ttu-id="3b079-4972">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-4972">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-4973">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-4973">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-4974">32</span><span class="sxs-lookup"><span data-stu-id="3b079-4974">32</span></span> |
| <span data-ttu-id="3b079-4975">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-4975">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4977">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-4977">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4978">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4978">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4979">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-4979">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4980">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-4980">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-4981">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-4981">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-4982">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-4982">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4984">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-4984">Texture3D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4986">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-4986">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4988">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-4988">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4990">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-4990">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4992">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-4992">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-4993">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-4993">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-4994">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-4994">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-4995">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-4995">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-4996">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-4996">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-4998">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-4998">Mipmap Auto-Generation</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5000">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-5000">RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5002">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-5002">Blendable RenderTarget</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5004">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-5004">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-5005">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-5005">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-5006">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5006">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5007">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-5007">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5008">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-5008">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-5009">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-5009">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-5010">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5010">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-5011">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-5011">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-5012">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5012">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-5013">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-5013">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-5014">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5014">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-5015">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5015">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5016">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5016">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5017">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-5017">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5019">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-5019">4x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5021">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5021">8x Multisample RenderTarget</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5023">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-5023">Other Multisample Count RT</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5025">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-5025">Multisample Resolve</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5027">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5027">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-5028">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-5028">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-5029">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-5029">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-5030">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5030">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-5031">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5031">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-5032">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5032">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-5033">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-5033">Shared Resource</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5035">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-5035">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="3b079-5036">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="3b079-5036">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="3b079-5037">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-5037">Target</span></span> | <span data-ttu-id="3b079-5038">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-5038">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-5039">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-5039">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-5040">32</span><span class="sxs-lookup"><span data-stu-id="3b079-5040">32</span></span> |
| <span data-ttu-id="3b079-5041">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5041">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5043">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-5043">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5044">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5044">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5045">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5045">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5046">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-5046">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5047">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-5047">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-5048">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-5048">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-5050">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-5051">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-5051">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-5052">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-5052">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-5053">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-5053">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-5054">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-5054">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-5055">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-5055">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-5056">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-5056">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-5057">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-5057">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-5058">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-5058">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-5059">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-5059">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-5060">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-5060">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5061">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-5061">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5062">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-5062">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-5063">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-5063">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-5064">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5064">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5065">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-5065">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5066">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-5066">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-5067">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-5067">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-5068">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5068">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-5069">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-5069">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-5070">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5070">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-5071">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-5071">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-5072">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5072">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-5073">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5073">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5074">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5074">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5075">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-5075">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5077">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-5077">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5078">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5078">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5079">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-5079">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-5080">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-5080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-5081">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5081">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-5082">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-5082">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-5083">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-5083">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-5084">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5084">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5086">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5086">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5088">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5088">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5090">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-5090">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-5091">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-5091">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="3b079-5092">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="3b079-5092">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="3b079-5093">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-5093">Target</span></span> | <span data-ttu-id="3b079-5094">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-5094">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-5095">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-5095">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-5096">32</span><span class="sxs-lookup"><span data-stu-id="3b079-5096">32</span></span> |
| <span data-ttu-id="3b079-5097">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5097">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5099">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-5099">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5100">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5100">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5101">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5101">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5102">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-5102">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5103">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-5103">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-5104">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-5104">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5106">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-5106">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-5107">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-5107">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-5108">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-5108">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-5109">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-5109">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-5110">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-5110">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-5111">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-5111">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-5112">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-5112">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-5113">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-5113">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-5114">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-5114">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-5115">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-5115">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-5116">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-5116">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5117">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-5117">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5118">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-5118">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-5119">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-5119">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-5120">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5120">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5121">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-5121">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5122">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-5122">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-5123">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-5123">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-5124">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5124">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-5125">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-5125">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-5126">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5126">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-5127">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-5127">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-5128">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5128">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-5129">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5129">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5130">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5130">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5131">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-5131">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5133">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-5133">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5134">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5134">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5135">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-5135">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-5136">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-5136">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-5137">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5137">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-5138">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-5138">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-5139">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-5139">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-5140">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5140">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5142">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5142">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5144">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5144">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5146">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-5146">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-5147">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-5147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="3b079-5148">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="3b079-5148">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="3b079-5149">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-5149">Target</span></span> | <span data-ttu-id="3b079-5150">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-5150">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-5151">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-5151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-5152">64</span><span class="sxs-lookup"><span data-stu-id="3b079-5152">64</span></span> |
| <span data-ttu-id="3b079-5153">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5153">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5155">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-5155">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5156">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5156">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5157">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5157">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5158">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-5158">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5159">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-5159">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-5160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-5160">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5162">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-5162">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-5163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-5163">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-5164">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-5164">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-5165">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-5165">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-5166">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-5166">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-5167">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-5167">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-5168">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-5168">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-5169">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-5169">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-5170">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-5170">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-5171">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-5171">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-5172">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-5172">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5173">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-5173">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5174">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-5174">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-5175">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-5175">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-5176">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5176">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5177">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-5177">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5178">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-5178">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-5179">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-5179">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-5180">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5180">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-5181">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-5181">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-5182">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5182">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-5183">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-5183">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-5184">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5184">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-5185">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5185">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5186">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5186">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5187">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-5187">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5189">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-5189">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5190">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5190">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5191">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-5191">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-5192">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-5192">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-5193">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5193">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-5194">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-5194">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-5195">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-5195">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-5196">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5196">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5198">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5198">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5200">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5200">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5202">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-5202">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-5203">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-5203">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="3b079-5204">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="3b079-5204">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="3b079-5205">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-5205">Target</span></span> | <span data-ttu-id="3b079-5206">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-5206">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-5207">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-5207">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-5208">8</span><span class="sxs-lookup"><span data-stu-id="3b079-5208">8</span></span> |
| <span data-ttu-id="3b079-5209">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5209">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5211">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-5211">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5212">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5212">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5213">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5213">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5214">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-5214">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5215">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-5215">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-5216">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-5216">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5218">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-5218">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-5219">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-5219">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-5220">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-5220">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-5221">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-5221">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-5222">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-5222">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-5223">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-5223">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-5224">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-5224">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-5225">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-5225">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-5226">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-5226">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-5227">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-5227">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-5228">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-5228">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5229">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-5229">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5230">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-5230">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-5231">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-5231">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-5232">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5232">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5233">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-5233">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5234">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-5234">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-5235">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-5235">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-5236">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5236">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-5237">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-5237">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-5238">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5238">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-5239">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-5239">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-5240">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5240">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-5241">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5241">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5242">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5242">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5243">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-5243">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5245">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-5245">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5246">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5246">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5247">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-5247">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-5248">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-5248">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-5249">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5249">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-5250">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-5250">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-5251">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-5251">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-5252">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5252">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5254">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5254">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5256">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5256">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5258">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-5258">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-5259">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-5259">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="3b079-5260">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="3b079-5260">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="3b079-5261">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-5261">Target</span></span> | <span data-ttu-id="3b079-5262">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-5262">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-5263">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-5263">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-5264">16</span><span class="sxs-lookup"><span data-stu-id="3b079-5264">16</span></span> |
| <span data-ttu-id="3b079-5265">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5265">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5267">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-5267">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5268">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5268">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5269">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5269">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5270">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-5270">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5271">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-5271">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-5272">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-5272">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5274">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-5274">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-5275">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-5275">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-5276">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-5276">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-5277">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-5277">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-5278">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-5278">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-5279">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-5279">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-5280">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-5280">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-5281">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-5281">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-5282">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-5282">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-5283">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-5283">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-5284">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-5284">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5285">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-5285">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5286">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-5286">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-5287">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-5287">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-5288">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5288">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5289">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-5289">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5290">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-5290">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-5291">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-5291">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-5292">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5292">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-5293">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-5293">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-5294">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5294">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-5295">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-5295">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-5296">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5296">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-5297">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5297">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5298">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5298">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5299">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-5299">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5301">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-5301">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5302">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5302">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5303">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-5303">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-5304">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-5304">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-5305">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5305">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-5306">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-5306">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-5307">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-5307">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-5308">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5308">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5310">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5310">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5312">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5312">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5314">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-5314">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-5315">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-5315">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="3b079-5316">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="3b079-5316">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="3b079-5317">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-5317">Target</span></span> | <span data-ttu-id="3b079-5318">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-5318">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-5319">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-5319">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-5320">16</span><span class="sxs-lookup"><span data-stu-id="3b079-5320">16</span></span> |
| <span data-ttu-id="3b079-5321">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5321">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5323">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-5323">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5324">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5324">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5325">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5325">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5326">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-5326">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5327">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-5327">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-5328">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-5328">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5330">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-5330">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-5331">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-5331">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-5332">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-5332">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-5333">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-5333">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-5334">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-5334">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-5335">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-5335">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-5336">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-5336">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-5337">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-5337">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-5338">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-5338">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-5339">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-5339">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-5340">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-5340">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5341">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-5341">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5342">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-5342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-5343">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-5343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-5344">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5345">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-5345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5346">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-5346">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-5347">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-5347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-5348">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-5349">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-5349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-5350">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-5351">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-5351">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-5352">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-5353">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5354">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5355">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-5355">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5357">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-5357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5358">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5359">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-5359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-5360">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-5360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-5361">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5361">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-5362">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-5362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-5363">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-5363">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-5364">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5364">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5366">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5366">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5368">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5368">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5370">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-5370">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-5371">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-5371">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="3b079-5372">DXGI_FORMAT_420 \_ opaca<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="3b079-5372">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="3b079-5373">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-5373">Target</span></span> | <span data-ttu-id="3b079-5374">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-5374">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-5375">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-5375">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-5376">8</span><span class="sxs-lookup"><span data-stu-id="3b079-5376">8</span></span> |
| <span data-ttu-id="3b079-5377">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5377">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5379">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-5379">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5380">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5380">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5381">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5381">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5382">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-5382">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5383">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-5383">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-5384">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-5384">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5386">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-5386">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-5387">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-5387">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-5388">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-5388">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-5389">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-5389">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-5390">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-5390">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-5391">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-5391">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-5392">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-5392">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-5393">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-5393">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-5394">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-5394">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-5395">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-5395">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-5396">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-5396">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5397">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-5397">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5398">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-5398">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-5399">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-5399">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-5400">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5400">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5401">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-5401">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5402">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-5402">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-5403">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-5403">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-5404">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5404">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-5405">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-5405">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-5406">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5406">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-5407">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-5407">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-5408">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5408">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-5409">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5409">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5410">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5410">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5411">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-5411">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3b079-5412">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-5412">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5413">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5413">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5414">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-5414">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-5415">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-5415">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-5416">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5416">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-5417">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-5417">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-5418">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-5418">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-5419">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5419">Video Decoder Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5421">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5421">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5423">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5423">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5425">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-5425">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-5426">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-5426">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="3b079-5427">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="3b079-5427">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="3b079-5428">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-5428">Target</span></span> | <span data-ttu-id="3b079-5429">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-5429">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-5430">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-5430">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-5431">16</span><span class="sxs-lookup"><span data-stu-id="3b079-5431">16</span></span> |
| <span data-ttu-id="3b079-5432">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5432">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5434">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-5434">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5435">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5435">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5436">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5436">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5437">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-5437">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5438">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-5438">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-5439">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-5439">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5441">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-5441">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-5442">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-5442">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-5443">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-5443">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-5444">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-5444">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-5445">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-5445">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-5446">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-5446">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-5447">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-5447">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-5448">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-5448">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-5449">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-5449">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-5450">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-5450">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-5451">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-5451">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5452">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-5452">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5453">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-5453">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-5454">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-5454">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-5455">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5455">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5456">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-5456">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5457">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-5457">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-5458">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-5458">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-5459">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5459">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-5460">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-5460">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-5461">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5461">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-5462">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-5462">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-5463">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5463">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-5464">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5464">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5465">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5465">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5466">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-5466">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5468">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-5468">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5469">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5469">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5470">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-5470">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-5471">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-5471">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-5472">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5472">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-5473">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-5473">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-5474">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-5474">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-5475">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5475">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5477">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5477">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5479">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5479">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5481">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-5481">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-5482">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-5482">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="3b079-5483">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="3b079-5483">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="3b079-5484">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-5484">Target</span></span> | <span data-ttu-id="3b079-5485">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-5485">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-5486">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-5486">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-5487">32</span><span class="sxs-lookup"><span data-stu-id="3b079-5487">32</span></span> |
| <span data-ttu-id="3b079-5488">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5488">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5490">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-5490">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5491">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5491">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5492">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5492">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5493">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-5493">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5494">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-5494">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-5495">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-5495">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5497">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-5497">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-5498">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-5498">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-5499">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-5499">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-5500">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-5500">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-5501">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-5501">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-5502">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-5502">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-5503">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-5503">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-5504">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-5504">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-5505">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-5505">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-5506">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-5506">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-5507">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-5507">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5508">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-5508">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5509">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-5509">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-5510">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-5510">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-5511">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5511">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5512">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-5512">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5513">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-5513">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-5514">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-5514">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-5515">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5515">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-5516">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-5516">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-5517">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5517">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-5518">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-5518">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-5519">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5519">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-5520">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5520">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5521">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5521">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5522">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-5522">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5524">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-5524">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5525">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5525">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5526">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-5526">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-5527">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-5527">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-5528">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5528">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-5529">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-5529">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-5530">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-5530">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-5531">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5531">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5533">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5533">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5535">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5535">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5537">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-5537">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-5538">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-5538">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="3b079-5539">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="3b079-5539">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="3b079-5540">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-5540">Target</span></span> | <span data-ttu-id="3b079-5541">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-5541">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-5542">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-5542">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-5543">32</span><span class="sxs-lookup"><span data-stu-id="3b079-5543">32</span></span> |
| <span data-ttu-id="3b079-5544">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5544">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5546">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-5546">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5547">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5547">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5548">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5548">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5549">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-5549">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5550">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-5550">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-5551">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-5551">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5553">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-5553">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-5554">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-5554">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-5555">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-5555">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-5556">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-5556">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-5557">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-5557">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-5558">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-5558">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-5559">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-5559">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-5560">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-5560">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-5561">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-5561">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-5562">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-5562">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-5563">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-5563">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5564">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-5564">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5565">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-5565">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-5566">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-5566">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-5567">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5567">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5568">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-5568">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5569">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-5569">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-5570">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-5570">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-5571">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5571">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-5572">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-5572">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-5573">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5573">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-5574">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-5574">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-5575">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5575">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-5576">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5576">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5577">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5577">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5578">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-5578">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5580">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-5580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5581">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5582">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-5582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-5583">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-5583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-5584">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5584">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-5585">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-5585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-5586">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-5586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-5587">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5587">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5589">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5589">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5591">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5591">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5593">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-5593">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-5594">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-5594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="3b079-5595">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="3b079-5595">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="3b079-5596">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-5596">Target</span></span> | <span data-ttu-id="3b079-5597">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-5597">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-5598">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-5598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-5599">8</span><span class="sxs-lookup"><span data-stu-id="3b079-5599">8</span></span> |
| <span data-ttu-id="3b079-5600">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5600">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5602">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-5602">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5603">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5603">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5604">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5604">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5605">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-5605">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5606">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-5606">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-5607">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-5607">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5609">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-5609">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-5610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-5610">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-5611">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-5611">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-5612">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-5612">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-5613">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-5613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-5614">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-5614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-5615">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-5615">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-5616">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-5616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-5617">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-5617">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-5618">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-5618">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-5619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-5619">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5620">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-5620">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5621">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-5621">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-5622">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-5622">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-5623">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5623">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5624">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-5624">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5625">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-5625">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-5626">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-5626">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-5627">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5627">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-5628">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-5628">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-5629">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5629">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-5630">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-5630">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-5631">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5631">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-5632">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5632">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5633">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5633">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5634">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-5634">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5636">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-5636">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5637">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5637">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5638">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-5638">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-5639">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-5639">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-5640">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5640">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-5641">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-5641">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-5642">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-5642">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-5643">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5643">Video Decoder Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5645">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5645">Video Processor Input</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5647">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5647">Video Processor Output</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5649">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-5649">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-5650">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-5650">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="3b079-5651">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="3b079-5651">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="3b079-5652">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-5652">Target</span></span> | <span data-ttu-id="3b079-5653">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-5653">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-5654">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-5654">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-5655">8</span><span class="sxs-lookup"><span data-stu-id="3b079-5655">8</span></span> |
| <span data-ttu-id="3b079-5656">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5656">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5658">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-5658">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5659">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5659">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5660">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5660">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5661">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-5661">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5662">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-5662">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-5663">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-5663">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5665">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-5665">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-5666">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-5666">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-5667">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-5667">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-5668">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-5668">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-5669">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-5669">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-5670">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-5670">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-5671">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-5671">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-5672">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-5672">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-5673">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-5673">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-5674">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-5674">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-5675">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-5675">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5676">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-5676">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5677">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-5677">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-5678">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-5678">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-5679">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5679">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5680">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-5680">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5681">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-5681">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-5682">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-5682">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-5683">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5683">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-5684">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-5684">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-5685">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5685">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-5686">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-5686">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-5687">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5687">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-5688">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5688">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5689">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5689">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5690">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-5690">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5692">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-5692">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5693">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5693">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5694">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-5694">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-5695">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-5695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-5696">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5696">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-5697">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-5697">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-5698">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-5698">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-5699">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5699">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-5700">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5700">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5702">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5702">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-5703">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-5703">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-5704">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-5704">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="3b079-5705">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="3b079-5705">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="3b079-5706">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-5706">Target</span></span> | <span data-ttu-id="3b079-5707">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-5707">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-5708">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-5708">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-5709">8</span><span class="sxs-lookup"><span data-stu-id="3b079-5709">8</span></span> |
| <span data-ttu-id="3b079-5710">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5710">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5712">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-5712">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5713">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5713">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5714">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5714">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5715">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-5715">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5716">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-5716">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-5717">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-5717">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5719">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-5719">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-5720">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-5720">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-5721">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-5721">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-5722">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-5722">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-5723">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-5723">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-5724">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-5724">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-5725">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-5725">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-5726">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-5726">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-5727">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-5727">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-5728">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-5728">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-5729">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-5729">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5730">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-5730">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5731">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-5731">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-5732">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-5732">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-5733">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5733">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5734">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-5734">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5735">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-5735">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-5736">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-5736">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-5737">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5737">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-5738">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-5738">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-5739">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5739">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-5740">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-5740">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-5741">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5741">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-5742">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5742">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5743">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5743">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5744">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-5744">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5746">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-5746">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5747">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5747">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5748">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-5748">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-5749">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-5749">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-5750">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5750">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-5751">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-5751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-5752">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-5752">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-5753">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5753">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-5754">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5754">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5756">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-5757">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-5757">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-5758">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-5758">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="3b079-5759">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="3b079-5759">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="3b079-5760">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-5760">Target</span></span> | <span data-ttu-id="3b079-5761">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-5761">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-5762">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-5762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-5763">8</span><span class="sxs-lookup"><span data-stu-id="3b079-5763">8</span></span> |
| <span data-ttu-id="3b079-5764">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5764">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5766">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-5766">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5767">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5767">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5768">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5768">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5769">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-5769">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5770">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-5770">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-5771">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-5771">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5773">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-5773">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-5774">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-5774">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-5775">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-5775">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-5776">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-5776">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-5777">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-5777">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-5778">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-5778">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-5779">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-5779">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-5780">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-5780">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-5781">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-5781">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-5782">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-5782">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-5783">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-5783">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5784">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-5784">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5785">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-5785">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-5786">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-5786">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-5787">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5787">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5788">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-5788">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5789">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-5789">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-5790">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-5790">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-5791">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5791">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-5792">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-5792">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-5793">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5793">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-5794">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-5794">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-5795">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5795">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-5796">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5796">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5797">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5797">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5798">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-5798">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5800">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-5800">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5801">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5801">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5802">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-5802">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-5803">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-5803">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-5804">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5804">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-5805">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-5805">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-5806">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-5806">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-5807">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5807">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-5808">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5808">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5810">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5810">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-5811">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-5811">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-5812">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-5812">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="3b079-5813">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="3b079-5813">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="3b079-5814">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-5814">Target</span></span> | <span data-ttu-id="3b079-5815">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-5815">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-5816">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-5816">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-5817">16</span><span class="sxs-lookup"><span data-stu-id="3b079-5817">16</span></span> |
| <span data-ttu-id="3b079-5818">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5818">Format Support</span></span> | ![opcional](images/letter-o.jpg) |
| <span data-ttu-id="3b079-5820">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-5820">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5821">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5821">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5822">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5822">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5823">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-5823">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5824">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-5824">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-5825">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-5825">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5827">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-5827">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-5828">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-5828">TextureCube</span></span> | \- |
| <span data-ttu-id="3b079-5829">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-5829">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3b079-5830">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-5830">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3b079-5831">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-5831">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-5832">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-5832">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-5833">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-5833">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-5834">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-5834">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-5835">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-5835">Mipmap</span></span> | \- |
| <span data-ttu-id="3b079-5836">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-5836">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-5837">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-5837">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5838">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-5838">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5839">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-5839">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-5840">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-5840">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-5841">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5841">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5842">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-5842">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5843">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-5843">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-5844">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-5844">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-5845">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5845">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-5846">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-5846">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-5847">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5847">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-5848">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-5848">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-5849">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5849">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-5850">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5850">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5851">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5851">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5852">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-5852">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5854">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-5854">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5855">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5855">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5856">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-5856">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-5857">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-5857">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-5858">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5858">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-5859">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-5859">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-5860">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-5860">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-5861">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5861">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-5862">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5862">Video Processor Input</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5864">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5864">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-5865">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-5865">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-5866">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-5866">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="3b079-5867">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="3b079-5867">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="3b079-5868">Destino</span><span class="sxs-lookup"><span data-stu-id="3b079-5868">Target</span></span> | <span data-ttu-id="3b079-5869">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="3b079-5869">Support</span></span> |
| - | - |
| <span data-ttu-id="3b079-5870">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="3b079-5870">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3b079-5871">16</span><span class="sxs-lookup"><span data-stu-id="3b079-5871">16</span></span> |
| <span data-ttu-id="3b079-5872">Compatibilidad con formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5872">Format Support</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5874">Buffer</span><span class="sxs-lookup"><span data-stu-id="3b079-5874">Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5875">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5875">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5876">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="3b079-5876">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5877">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3b079-5877">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3b079-5878">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b079-5878">Texture1D</span></span> | \- |
| <span data-ttu-id="3b079-5879">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b079-5879">Texture2D</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5881">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b079-5881">Texture3D</span></span> | \- |
| <span data-ttu-id="3b079-5882">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b079-5882">TextureCube</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5884">Ejemplo de sombreador (solo ejemplo de punto)</span><span class="sxs-lookup"><span data-stu-id="3b079-5884">Shader sample (point sample only)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5886">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="3b079-5886">Shader sample (any filter)</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5888">Ejemplo de sombreador \_ c (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="3b079-5888">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3b079-5889">Ejemplo de sombreador (filtro de 1 bit mono)</span><span class="sxs-lookup"><span data-stu-id="3b079-5889">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3b079-5890">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="3b079-5890">Shader gather4</span></span> | \- |
| <span data-ttu-id="3b079-5891">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3b079-5891">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3b079-5892">Mapa</span><span class="sxs-lookup"><span data-stu-id="3b079-5892">Mipmap</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5894">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="3b079-5894">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3b079-5895">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="3b079-5895">RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5896">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="3b079-5896">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5897">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="3b079-5897">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3b079-5898">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="3b079-5898">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3b079-5899">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="3b079-5899">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5900">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="3b079-5900">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3b079-5901">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-5901">Typed UAV</span></span> | \- |
| <span data-ttu-id="3b079-5902">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="3b079-5902">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3b079-5903">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5903">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3b079-5904">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="3b079-5904">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3b079-5905">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5905">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3b079-5906">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="3b079-5906">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3b079-5907">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="3b079-5907">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3b079-5908">UAV Atomic con signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5908">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5909">UAV Atomic sin signo mín. o máx.</span><span class="sxs-lookup"><span data-stu-id="3b079-5909">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3b079-5910">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="3b079-5910">CPU Lockable</span></span> | ![requerido](images/letter-r.jpg) |
| <span data-ttu-id="3b079-5912">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="3b079-5912">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5913">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5913">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3b079-5914">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="3b079-5914">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3b079-5915">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="3b079-5915">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3b079-5916">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="3b079-5916">Multisample Load</span></span> | \- |
| <span data-ttu-id="3b079-5917">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3b079-5917">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3b079-5918">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="3b079-5918">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3b079-5919">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5919">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3b079-5920">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5920">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3b079-5921">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5921">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3b079-5922">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="3b079-5922">Shared Resource</span></span> | \- |
| <span data-ttu-id="3b079-5923">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b079-5923">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="3b079-5924">Dar formato a notas</span><span class="sxs-lookup"><span data-stu-id="3b079-5924">Format notes</span></span>

<span data-ttu-id="3b079-5925">El propósito del formato puede cambiar de un nivel de característica de hardware a otro.</span><span class="sxs-lookup"><span data-stu-id="3b079-5925">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="3b079-5926"><sup>L</sup> : formato sin tipo</span><span class="sxs-lookup"><span data-stu-id="3b079-5926"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="3b079-5927"><sup>PC</sup> : diseño parcialmente tipado, de conversión de tipos y sencillo</span><span class="sxs-lookup"><span data-stu-id="3b079-5927"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="3b079-5928"><sup>FCS</sup> : diseño totalmente tipado, convertible y sencillo</span><span class="sxs-lookup"><span data-stu-id="3b079-5928"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="3b079-5929"><sup>FNS</sup> : diseño totalmente tipado, sin conversión y simple</span><span class="sxs-lookup"><span data-stu-id="3b079-5929"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="3b079-5930"><sup>PCC</sup> : diseño parcialmente tipado, convertible y complejo</span><span class="sxs-lookup"><span data-stu-id="3b079-5930"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="3b079-5931"><sup>FCC</sup> : diseño totalmente tipado, convertible y complejo</span><span class="sxs-lookup"><span data-stu-id="3b079-5931"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="3b079-5932"><sup>FNC</sup> : diseño totalmente tipado, no convertible y complejo</span><span class="sxs-lookup"><span data-stu-id="3b079-5932"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="3b079-5933"><sup>V</sup> : formato de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b079-5933"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="3b079-5934">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b079-5934">Related topics</span></span>

[<span data-ttu-id="3b079-5935">Niveles de características de hardware de D3D12</span><span class="sxs-lookup"><span data-stu-id="3b079-5935">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

<span data-ttu-id="3b079-5936">[Implementación de búferes de sombra para el nivel de característica 9 de Direct3D](/previous-versions/windows/apps/jj262110(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="3b079-5936">[Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10))</span></span>

[<span data-ttu-id="3b079-5937">Asignar formatos heredados</span><span class="sxs-lookup"><span data-stu-id="3b079-5937">Mapping Legacy Formats</span></span>](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[<span data-ttu-id="3b079-5938">Guía de programación para DXGI</span><span class="sxs-lookup"><span data-stu-id="3b079-5938">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
