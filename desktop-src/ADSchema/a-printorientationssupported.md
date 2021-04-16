---
title: Orientaciones de impresión-atributo compatible
description: Rotación de página para la impresión horizontal.
ms.assetid: a3e910f1-452e-4b85-8ede-50b7274475a0
ms.tgt_platform: multiple
keywords:
- Orientación de impresión-esquema de AD de atributos admitidos
- printOrientationsSupported esquema de AD de atributos
topic_type:
- apiref
api_name:
- Print-Orientations-Supported
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49888caa713de7dd12616dcb9932e52b15b2a454
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658767"
---
# <a name="print-orientations-supported-attribute"></a><span data-ttu-id="bb87d-105">Orientaciones de impresión-atributo compatible</span><span class="sxs-lookup"><span data-stu-id="bb87d-105">Print-Orientations-Supported attribute</span></span>

<span data-ttu-id="bb87d-106">Rotación de página para la impresión horizontal.</span><span class="sxs-lookup"><span data-stu-id="bb87d-106">The page rotation for landscape printing.</span></span>



| <span data-ttu-id="bb87d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb87d-107">Entry</span></span> | <span data-ttu-id="bb87d-108">Value</span><span class="sxs-lookup"><span data-stu-id="bb87d-108">Value</span></span> |
|-------------------|-------------------------------------------------------------|
| <span data-ttu-id="bb87d-109">CN</span><span class="sxs-lookup"><span data-stu-id="bb87d-109">CN</span></span>                | <span data-ttu-id="bb87d-110">Orientaciones de impresión: compatible</span><span class="sxs-lookup"><span data-stu-id="bb87d-110">Print-Orientations-Supported</span></span>                                |
| <span data-ttu-id="bb87d-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="bb87d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bb87d-112">printOrientationsSupported</span><span class="sxs-lookup"><span data-stu-id="bb87d-112">printOrientationsSupported</span></span>                                  |
| <span data-ttu-id="bb87d-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="bb87d-113">Size</span></span>              | <span data-ttu-id="bb87d-114">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="bb87d-114">4 bytes.</span></span> <span data-ttu-id="bb87d-115">Valores posibles: 0, 90, 270 y 0 = sin panorama.</span><span class="sxs-lookup"><span data-stu-id="bb87d-115">Possible values: 0, 90, 270, and 0 = no landscape.</span></span> |
| <span data-ttu-id="bb87d-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="bb87d-116">Update Privilege</span></span>  | \-                                                          |
| <span data-ttu-id="bb87d-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="bb87d-117">Update Frequency</span></span>  | \-                                                          |
| <span data-ttu-id="bb87d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bb87d-118">Attribute-Id</span></span>      | <span data-ttu-id="bb87d-119">1.2.840.113556.1.4.240</span><span class="sxs-lookup"><span data-stu-id="bb87d-119">1.2.840.113556.1.4.240</span></span>                                      |
| <span data-ttu-id="bb87d-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bb87d-120">System-Id-Guid</span></span>    | <span data-ttu-id="bb87d-121">281416d0-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="bb87d-121">281416d0-1968-11d0-a28f-00aa003049e2</span></span>                        |
| <span data-ttu-id="bb87d-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb87d-122">Syntax</span></span>            | [<span data-ttu-id="bb87d-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bb87d-123">**String(Unicode)**</span></span>](s-string-unicode.md)                 |



## <a name="implementations"></a><span data-ttu-id="bb87d-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="bb87d-124">Implementations</span></span>

-   [<span data-ttu-id="bb87d-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bb87d-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bb87d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bb87d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bb87d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bb87d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bb87d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bb87d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bb87d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bb87d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bb87d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bb87d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bb87d-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bb87d-131">Windows 2000 Server</span></span>



| <span data-ttu-id="bb87d-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb87d-132">Entry</span></span> | <span data-ttu-id="bb87d-133">Value</span><span class="sxs-lookup"><span data-stu-id="bb87d-133">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="bb87d-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="bb87d-134">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="bb87d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb87d-135">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="bb87d-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb87d-136">System-Only</span></span>            | <span data-ttu-id="bb87d-137">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-137">False</span></span>                                          |
| <span data-ttu-id="bb87d-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="bb87d-138">Is-Single-Valued</span></span>       | <span data-ttu-id="bb87d-139">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-139">False</span></span>                                          |
| <span data-ttu-id="bb87d-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="bb87d-140">Is Indexed</span></span>             | <span data-ttu-id="bb87d-141">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-141">False</span></span>                                          |
| <span data-ttu-id="bb87d-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="bb87d-142">In Global Catalog</span></span>      | <span data-ttu-id="bb87d-143">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-143">False</span></span>                                          |
| <span data-ttu-id="bb87d-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="bb87d-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb87d-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bb87d-145">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="bb87d-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb87d-146">Range-Lower</span></span>            | <span data-ttu-id="bb87d-147">1</span><span class="sxs-lookup"><span data-stu-id="bb87d-147">1</span></span>                                              |
| <span data-ttu-id="bb87d-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb87d-148">Range-Upper</span></span>            | <span data-ttu-id="bb87d-149">256</span><span class="sxs-lookup"><span data-stu-id="bb87d-149">256</span></span>                                            |
| <span data-ttu-id="bb87d-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb87d-150">Search-Flags</span></span>           | <span data-ttu-id="bb87d-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb87d-151">0x00000000</span></span>                                     |
| <span data-ttu-id="bb87d-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb87d-152">System-Flags</span></span>           | <span data-ttu-id="bb87d-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb87d-153">0x00000010</span></span>                                     |
| <span data-ttu-id="bb87d-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="bb87d-154">Classes used in</span></span>        | [<span data-ttu-id="bb87d-155">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="bb87d-155">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bb87d-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bb87d-156">Windows Server 2003</span></span>



| <span data-ttu-id="bb87d-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb87d-157">Entry</span></span> | <span data-ttu-id="bb87d-158">Value</span><span class="sxs-lookup"><span data-stu-id="bb87d-158">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="bb87d-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="bb87d-159">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="bb87d-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb87d-160">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="bb87d-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb87d-161">System-Only</span></span>            | <span data-ttu-id="bb87d-162">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-162">False</span></span>                                          |
| <span data-ttu-id="bb87d-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="bb87d-163">Is-Single-Valued</span></span>       | <span data-ttu-id="bb87d-164">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-164">False</span></span>                                          |
| <span data-ttu-id="bb87d-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="bb87d-165">Is Indexed</span></span>             | <span data-ttu-id="bb87d-166">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-166">False</span></span>                                          |
| <span data-ttu-id="bb87d-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="bb87d-167">In Global Catalog</span></span>      | <span data-ttu-id="bb87d-168">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-168">False</span></span>                                          |
| <span data-ttu-id="bb87d-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="bb87d-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb87d-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bb87d-170">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="bb87d-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb87d-171">Range-Lower</span></span>            | <span data-ttu-id="bb87d-172">1</span><span class="sxs-lookup"><span data-stu-id="bb87d-172">1</span></span>                                              |
| <span data-ttu-id="bb87d-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb87d-173">Range-Upper</span></span>            | <span data-ttu-id="bb87d-174">256</span><span class="sxs-lookup"><span data-stu-id="bb87d-174">256</span></span>                                            |
| <span data-ttu-id="bb87d-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb87d-175">Search-Flags</span></span>           | <span data-ttu-id="bb87d-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb87d-176">0x00000000</span></span>                                     |
| <span data-ttu-id="bb87d-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb87d-177">System-Flags</span></span>           | <span data-ttu-id="bb87d-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb87d-178">0x00000010</span></span>                                     |
| <span data-ttu-id="bb87d-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="bb87d-179">Classes used in</span></span>        | [<span data-ttu-id="bb87d-180">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="bb87d-180">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bb87d-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bb87d-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bb87d-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb87d-182">Entry</span></span> | <span data-ttu-id="bb87d-183">Value</span><span class="sxs-lookup"><span data-stu-id="bb87d-183">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="bb87d-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="bb87d-184">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="bb87d-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb87d-185">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="bb87d-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb87d-186">System-Only</span></span>            | <span data-ttu-id="bb87d-187">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-187">False</span></span>                                          |
| <span data-ttu-id="bb87d-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="bb87d-188">Is-Single-Valued</span></span>       | <span data-ttu-id="bb87d-189">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-189">False</span></span>                                          |
| <span data-ttu-id="bb87d-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="bb87d-190">Is Indexed</span></span>             | <span data-ttu-id="bb87d-191">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-191">False</span></span>                                          |
| <span data-ttu-id="bb87d-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="bb87d-192">In Global Catalog</span></span>      | <span data-ttu-id="bb87d-193">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-193">False</span></span>                                          |
| <span data-ttu-id="bb87d-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="bb87d-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb87d-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bb87d-195">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="bb87d-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb87d-196">Range-Lower</span></span>            | <span data-ttu-id="bb87d-197">1</span><span class="sxs-lookup"><span data-stu-id="bb87d-197">1</span></span>                                              |
| <span data-ttu-id="bb87d-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb87d-198">Range-Upper</span></span>            | <span data-ttu-id="bb87d-199">256</span><span class="sxs-lookup"><span data-stu-id="bb87d-199">256</span></span>                                            |
| <span data-ttu-id="bb87d-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb87d-200">Search-Flags</span></span>           | <span data-ttu-id="bb87d-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb87d-201">0x00000000</span></span>                                     |
| <span data-ttu-id="bb87d-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb87d-202">System-Flags</span></span>           | <span data-ttu-id="bb87d-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb87d-203">0x00000010</span></span>                                     |
| <span data-ttu-id="bb87d-204">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="bb87d-204">Classes used in</span></span>        | [<span data-ttu-id="bb87d-205">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="bb87d-205">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bb87d-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb87d-206">Windows Server 2008</span></span>



| <span data-ttu-id="bb87d-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb87d-207">Entry</span></span> | <span data-ttu-id="bb87d-208">Value</span><span class="sxs-lookup"><span data-stu-id="bb87d-208">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="bb87d-209">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="bb87d-209">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="bb87d-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb87d-210">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="bb87d-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb87d-211">System-Only</span></span>            | <span data-ttu-id="bb87d-212">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-212">False</span></span>                                          |
| <span data-ttu-id="bb87d-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="bb87d-213">Is-Single-Valued</span></span>       | <span data-ttu-id="bb87d-214">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-214">False</span></span>                                          |
| <span data-ttu-id="bb87d-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="bb87d-215">Is Indexed</span></span>             | <span data-ttu-id="bb87d-216">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-216">False</span></span>                                          |
| <span data-ttu-id="bb87d-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="bb87d-217">In Global Catalog</span></span>      | <span data-ttu-id="bb87d-218">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-218">False</span></span>                                          |
| <span data-ttu-id="bb87d-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="bb87d-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb87d-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bb87d-220">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="bb87d-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb87d-221">Range-Lower</span></span>            | <span data-ttu-id="bb87d-222">1</span><span class="sxs-lookup"><span data-stu-id="bb87d-222">1</span></span>                                              |
| <span data-ttu-id="bb87d-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb87d-223">Range-Upper</span></span>            | <span data-ttu-id="bb87d-224">256</span><span class="sxs-lookup"><span data-stu-id="bb87d-224">256</span></span>                                            |
| <span data-ttu-id="bb87d-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb87d-225">Search-Flags</span></span>           | <span data-ttu-id="bb87d-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb87d-226">0x00000000</span></span>                                     |
| <span data-ttu-id="bb87d-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb87d-227">System-Flags</span></span>           | <span data-ttu-id="bb87d-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb87d-228">0x00000010</span></span>                                     |
| <span data-ttu-id="bb87d-229">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="bb87d-229">Classes used in</span></span>        | [<span data-ttu-id="bb87d-230">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="bb87d-230">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bb87d-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bb87d-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bb87d-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb87d-232">Entry</span></span> | <span data-ttu-id="bb87d-233">Value</span><span class="sxs-lookup"><span data-stu-id="bb87d-233">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="bb87d-234">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="bb87d-234">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="bb87d-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb87d-235">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="bb87d-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb87d-236">System-Only</span></span>            | <span data-ttu-id="bb87d-237">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-237">False</span></span>                                          |
| <span data-ttu-id="bb87d-238">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="bb87d-238">Is-Single-Valued</span></span>       | <span data-ttu-id="bb87d-239">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-239">False</span></span>                                          |
| <span data-ttu-id="bb87d-240">Está indexado</span><span class="sxs-lookup"><span data-stu-id="bb87d-240">Is Indexed</span></span>             | <span data-ttu-id="bb87d-241">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-241">False</span></span>                                          |
| <span data-ttu-id="bb87d-242">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="bb87d-242">In Global Catalog</span></span>      | <span data-ttu-id="bb87d-243">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-243">False</span></span>                                          |
| <span data-ttu-id="bb87d-244">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="bb87d-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb87d-245">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bb87d-245">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="bb87d-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb87d-246">Range-Lower</span></span>            | <span data-ttu-id="bb87d-247">1</span><span class="sxs-lookup"><span data-stu-id="bb87d-247">1</span></span>                                              |
| <span data-ttu-id="bb87d-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb87d-248">Range-Upper</span></span>            | <span data-ttu-id="bb87d-249">256</span><span class="sxs-lookup"><span data-stu-id="bb87d-249">256</span></span>                                            |
| <span data-ttu-id="bb87d-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb87d-250">Search-Flags</span></span>           | <span data-ttu-id="bb87d-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb87d-251">0x00000000</span></span>                                     |
| <span data-ttu-id="bb87d-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb87d-252">System-Flags</span></span>           | <span data-ttu-id="bb87d-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb87d-253">0x00000010</span></span>                                     |
| <span data-ttu-id="bb87d-254">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="bb87d-254">Classes used in</span></span>        | [<span data-ttu-id="bb87d-255">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="bb87d-255">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bb87d-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bb87d-256">Windows Server 2012</span></span>



| <span data-ttu-id="bb87d-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb87d-257">Entry</span></span> | <span data-ttu-id="bb87d-258">Value</span><span class="sxs-lookup"><span data-stu-id="bb87d-258">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="bb87d-259">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="bb87d-259">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="bb87d-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb87d-260">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="bb87d-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb87d-261">System-Only</span></span>            | <span data-ttu-id="bb87d-262">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-262">False</span></span>                                          |
| <span data-ttu-id="bb87d-263">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="bb87d-263">Is-Single-Valued</span></span>       | <span data-ttu-id="bb87d-264">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-264">False</span></span>                                          |
| <span data-ttu-id="bb87d-265">Está indexado</span><span class="sxs-lookup"><span data-stu-id="bb87d-265">Is Indexed</span></span>             | <span data-ttu-id="bb87d-266">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-266">False</span></span>                                          |
| <span data-ttu-id="bb87d-267">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="bb87d-267">In Global Catalog</span></span>      | <span data-ttu-id="bb87d-268">False</span><span class="sxs-lookup"><span data-stu-id="bb87d-268">False</span></span>                                          |
| <span data-ttu-id="bb87d-269">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="bb87d-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb87d-270">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bb87d-270">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="bb87d-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb87d-271">Range-Lower</span></span>            | <span data-ttu-id="bb87d-272">1</span><span class="sxs-lookup"><span data-stu-id="bb87d-272">1</span></span>                                              |
| <span data-ttu-id="bb87d-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb87d-273">Range-Upper</span></span>            | <span data-ttu-id="bb87d-274">256</span><span class="sxs-lookup"><span data-stu-id="bb87d-274">256</span></span>                                            |
| <span data-ttu-id="bb87d-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb87d-275">Search-Flags</span></span>           | <span data-ttu-id="bb87d-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb87d-276">0x00000000</span></span>                                     |
| <span data-ttu-id="bb87d-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb87d-277">System-Flags</span></span>           | <span data-ttu-id="bb87d-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb87d-278">0x00000010</span></span>                                     |
| <span data-ttu-id="bb87d-279">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="bb87d-279">Classes used in</span></span>        | [<span data-ttu-id="bb87d-280">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="bb87d-280">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





