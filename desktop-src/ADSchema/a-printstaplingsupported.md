---
title: 'Grapado de impresión: atributo compatible'
description: TRUE si la impresora admite grapado. Proporcionado por el controlador.
ms.assetid: c0d1cbc5-7657-45a8-b154-a67f57386f52
ms.tgt_platform: multiple
keywords:
- 'Grapado de impresión: esquema de AD de atributos admitidos'
- printStaplingSupported esquema de AD de atributos
topic_type:
- apiref
api_name:
- Print-Stapling-Supported
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12303d9a18f267ec4eaef3a33dc8ec7350967aa6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658478"
---
# <a name="print-stapling-supported-attribute"></a><span data-ttu-id="f7f46-106">Grapado de impresión: atributo compatible</span><span class="sxs-lookup"><span data-stu-id="f7f46-106">Print-Stapling-Supported attribute</span></span>

<span data-ttu-id="f7f46-107">**True** si la impresora admite grapado.</span><span class="sxs-lookup"><span data-stu-id="f7f46-107">**TRUE** if the printer supports stapling.</span></span> <span data-ttu-id="f7f46-108">Proporcionado por el controlador.</span><span class="sxs-lookup"><span data-stu-id="f7f46-108">Supplied by the driver.</span></span>



| <span data-ttu-id="f7f46-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7f46-109">Entry</span></span> | <span data-ttu-id="f7f46-110">Value</span><span class="sxs-lookup"><span data-stu-id="f7f46-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f7f46-111">CN</span><span class="sxs-lookup"><span data-stu-id="f7f46-111">CN</span></span>                | <span data-ttu-id="f7f46-112">Grapado de impresión: compatible</span><span class="sxs-lookup"><span data-stu-id="f7f46-112">Print-Stapling-Supported</span></span>             |
| <span data-ttu-id="f7f46-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="f7f46-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f7f46-114">printStaplingSupported</span><span class="sxs-lookup"><span data-stu-id="f7f46-114">printStaplingSupported</span></span>               |
| <span data-ttu-id="f7f46-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f7f46-115">Size</span></span>              | <span data-ttu-id="f7f46-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="f7f46-116">4 bytes</span></span>                              |
| <span data-ttu-id="f7f46-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="f7f46-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f7f46-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="f7f46-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f7f46-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f7f46-119">Attribute-Id</span></span>      | <span data-ttu-id="f7f46-120">1.2.840.113556.1.4.281</span><span class="sxs-lookup"><span data-stu-id="f7f46-120">1.2.840.113556.1.4.281</span></span>               |
| <span data-ttu-id="f7f46-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f7f46-121">System-Id-Guid</span></span>    | <span data-ttu-id="f7f46-122">ba305f73-47e3-11d0-a1a6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="f7f46-122">ba305f73-47e3-11d0-a1a6-00c04fd930c9</span></span> |
| <span data-ttu-id="f7f46-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7f46-123">Syntax</span></span>            | [<span data-ttu-id="f7f46-124">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="f7f46-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="f7f46-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="f7f46-125">Implementations</span></span>

-   [<span data-ttu-id="f7f46-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f7f46-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f7f46-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f7f46-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f7f46-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f7f46-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f7f46-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f7f46-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f7f46-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f7f46-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f7f46-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f7f46-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f7f46-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f7f46-132">Windows 2000 Server</span></span>



| <span data-ttu-id="f7f46-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7f46-133">Entry</span></span> | <span data-ttu-id="f7f46-134">Value</span><span class="sxs-lookup"><span data-stu-id="f7f46-134">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="f7f46-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f7f46-135">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="f7f46-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7f46-136">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="f7f46-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7f46-137">System-Only</span></span>            | <span data-ttu-id="f7f46-138">False</span><span class="sxs-lookup"><span data-stu-id="f7f46-138">False</span></span>                                          |
| <span data-ttu-id="f7f46-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f7f46-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f7f46-140">True</span><span class="sxs-lookup"><span data-stu-id="f7f46-140">True</span></span>                                           |
| <span data-ttu-id="f7f46-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f7f46-141">Is Indexed</span></span>             | <span data-ttu-id="f7f46-142">False</span><span class="sxs-lookup"><span data-stu-id="f7f46-142">False</span></span>                                          |
| <span data-ttu-id="f7f46-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7f46-143">In Global Catalog</span></span>      | <span data-ttu-id="f7f46-144">True</span><span class="sxs-lookup"><span data-stu-id="f7f46-144">True</span></span>                                           |
| <span data-ttu-id="f7f46-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f7f46-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7f46-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7f46-146">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="f7f46-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7f46-147">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="f7f46-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7f46-148">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="f7f46-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f46-149">Search-Flags</span></span>           | <span data-ttu-id="f7f46-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f46-150">0x00000000</span></span>                                     |
| <span data-ttu-id="f7f46-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f46-151">System-Flags</span></span>           | <span data-ttu-id="f7f46-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7f46-152">0x00000010</span></span>                                     |
| <span data-ttu-id="f7f46-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f7f46-153">Classes used in</span></span>        | [<span data-ttu-id="f7f46-154">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="f7f46-154">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f7f46-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f7f46-155">Windows Server 2003</span></span>



| <span data-ttu-id="f7f46-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7f46-156">Entry</span></span> | <span data-ttu-id="f7f46-157">Value</span><span class="sxs-lookup"><span data-stu-id="f7f46-157">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="f7f46-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f7f46-158">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="f7f46-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7f46-159">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="f7f46-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7f46-160">System-Only</span></span>            | <span data-ttu-id="f7f46-161">False</span><span class="sxs-lookup"><span data-stu-id="f7f46-161">False</span></span>                                          |
| <span data-ttu-id="f7f46-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f7f46-162">Is-Single-Valued</span></span>       | <span data-ttu-id="f7f46-163">True</span><span class="sxs-lookup"><span data-stu-id="f7f46-163">True</span></span>                                           |
| <span data-ttu-id="f7f46-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f7f46-164">Is Indexed</span></span>             | <span data-ttu-id="f7f46-165">False</span><span class="sxs-lookup"><span data-stu-id="f7f46-165">False</span></span>                                          |
| <span data-ttu-id="f7f46-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7f46-166">In Global Catalog</span></span>      | <span data-ttu-id="f7f46-167">True</span><span class="sxs-lookup"><span data-stu-id="f7f46-167">True</span></span>                                           |
| <span data-ttu-id="f7f46-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f7f46-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7f46-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7f46-169">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="f7f46-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7f46-170">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="f7f46-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7f46-171">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="f7f46-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f46-172">Search-Flags</span></span>           | <span data-ttu-id="f7f46-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f46-173">0x00000000</span></span>                                     |
| <span data-ttu-id="f7f46-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f46-174">System-Flags</span></span>           | <span data-ttu-id="f7f46-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7f46-175">0x00000010</span></span>                                     |
| <span data-ttu-id="f7f46-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f7f46-176">Classes used in</span></span>        | [<span data-ttu-id="f7f46-177">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="f7f46-177">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f7f46-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f7f46-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f7f46-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7f46-179">Entry</span></span> | <span data-ttu-id="f7f46-180">Value</span><span class="sxs-lookup"><span data-stu-id="f7f46-180">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="f7f46-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f7f46-181">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="f7f46-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7f46-182">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="f7f46-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7f46-183">System-Only</span></span>            | <span data-ttu-id="f7f46-184">False</span><span class="sxs-lookup"><span data-stu-id="f7f46-184">False</span></span>                                          |
| <span data-ttu-id="f7f46-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f7f46-185">Is-Single-Valued</span></span>       | <span data-ttu-id="f7f46-186">True</span><span class="sxs-lookup"><span data-stu-id="f7f46-186">True</span></span>                                           |
| <span data-ttu-id="f7f46-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f7f46-187">Is Indexed</span></span>             | <span data-ttu-id="f7f46-188">False</span><span class="sxs-lookup"><span data-stu-id="f7f46-188">False</span></span>                                          |
| <span data-ttu-id="f7f46-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7f46-189">In Global Catalog</span></span>      | <span data-ttu-id="f7f46-190">True</span><span class="sxs-lookup"><span data-stu-id="f7f46-190">True</span></span>                                           |
| <span data-ttu-id="f7f46-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f7f46-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7f46-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7f46-192">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="f7f46-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7f46-193">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="f7f46-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7f46-194">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="f7f46-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f46-195">Search-Flags</span></span>           | <span data-ttu-id="f7f46-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f46-196">0x00000000</span></span>                                     |
| <span data-ttu-id="f7f46-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f46-197">System-Flags</span></span>           | <span data-ttu-id="f7f46-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7f46-198">0x00000010</span></span>                                     |
| <span data-ttu-id="f7f46-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f7f46-199">Classes used in</span></span>        | [<span data-ttu-id="f7f46-200">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="f7f46-200">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f7f46-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7f46-201">Windows Server 2008</span></span>



| <span data-ttu-id="f7f46-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7f46-202">Entry</span></span> | <span data-ttu-id="f7f46-203">Value</span><span class="sxs-lookup"><span data-stu-id="f7f46-203">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="f7f46-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f7f46-204">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="f7f46-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7f46-205">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="f7f46-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7f46-206">System-Only</span></span>            | <span data-ttu-id="f7f46-207">False</span><span class="sxs-lookup"><span data-stu-id="f7f46-207">False</span></span>                                          |
| <span data-ttu-id="f7f46-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f7f46-208">Is-Single-Valued</span></span>       | <span data-ttu-id="f7f46-209">True</span><span class="sxs-lookup"><span data-stu-id="f7f46-209">True</span></span>                                           |
| <span data-ttu-id="f7f46-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f7f46-210">Is Indexed</span></span>             | <span data-ttu-id="f7f46-211">False</span><span class="sxs-lookup"><span data-stu-id="f7f46-211">False</span></span>                                          |
| <span data-ttu-id="f7f46-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7f46-212">In Global Catalog</span></span>      | <span data-ttu-id="f7f46-213">True</span><span class="sxs-lookup"><span data-stu-id="f7f46-213">True</span></span>                                           |
| <span data-ttu-id="f7f46-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f7f46-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7f46-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7f46-215">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="f7f46-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7f46-216">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="f7f46-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7f46-217">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="f7f46-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f46-218">Search-Flags</span></span>           | <span data-ttu-id="f7f46-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f46-219">0x00000000</span></span>                                     |
| <span data-ttu-id="f7f46-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f46-220">System-Flags</span></span>           | <span data-ttu-id="f7f46-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7f46-221">0x00000010</span></span>                                     |
| <span data-ttu-id="f7f46-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f7f46-222">Classes used in</span></span>        | [<span data-ttu-id="f7f46-223">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="f7f46-223">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f7f46-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f7f46-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f7f46-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7f46-225">Entry</span></span> | <span data-ttu-id="f7f46-226">Value</span><span class="sxs-lookup"><span data-stu-id="f7f46-226">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="f7f46-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f7f46-227">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="f7f46-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7f46-228">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="f7f46-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7f46-229">System-Only</span></span>            | <span data-ttu-id="f7f46-230">False</span><span class="sxs-lookup"><span data-stu-id="f7f46-230">False</span></span>                                          |
| <span data-ttu-id="f7f46-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f7f46-231">Is-Single-Valued</span></span>       | <span data-ttu-id="f7f46-232">True</span><span class="sxs-lookup"><span data-stu-id="f7f46-232">True</span></span>                                           |
| <span data-ttu-id="f7f46-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f7f46-233">Is Indexed</span></span>             | <span data-ttu-id="f7f46-234">False</span><span class="sxs-lookup"><span data-stu-id="f7f46-234">False</span></span>                                          |
| <span data-ttu-id="f7f46-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7f46-235">In Global Catalog</span></span>      | <span data-ttu-id="f7f46-236">True</span><span class="sxs-lookup"><span data-stu-id="f7f46-236">True</span></span>                                           |
| <span data-ttu-id="f7f46-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f7f46-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7f46-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7f46-238">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="f7f46-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7f46-239">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="f7f46-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7f46-240">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="f7f46-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f46-241">Search-Flags</span></span>           | <span data-ttu-id="f7f46-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f46-242">0x00000000</span></span>                                     |
| <span data-ttu-id="f7f46-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f46-243">System-Flags</span></span>           | <span data-ttu-id="f7f46-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7f46-244">0x00000010</span></span>                                     |
| <span data-ttu-id="f7f46-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f7f46-245">Classes used in</span></span>        | [<span data-ttu-id="f7f46-246">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="f7f46-246">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f7f46-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f7f46-247">Windows Server 2012</span></span>



| <span data-ttu-id="f7f46-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7f46-248">Entry</span></span> | <span data-ttu-id="f7f46-249">Value</span><span class="sxs-lookup"><span data-stu-id="f7f46-249">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="f7f46-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f7f46-250">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="f7f46-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7f46-251">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="f7f46-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7f46-252">System-Only</span></span>            | <span data-ttu-id="f7f46-253">False</span><span class="sxs-lookup"><span data-stu-id="f7f46-253">False</span></span>                                          |
| <span data-ttu-id="f7f46-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f7f46-254">Is-Single-Valued</span></span>       | <span data-ttu-id="f7f46-255">True</span><span class="sxs-lookup"><span data-stu-id="f7f46-255">True</span></span>                                           |
| <span data-ttu-id="f7f46-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f7f46-256">Is Indexed</span></span>             | <span data-ttu-id="f7f46-257">False</span><span class="sxs-lookup"><span data-stu-id="f7f46-257">False</span></span>                                          |
| <span data-ttu-id="f7f46-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7f46-258">In Global Catalog</span></span>      | <span data-ttu-id="f7f46-259">True</span><span class="sxs-lookup"><span data-stu-id="f7f46-259">True</span></span>                                           |
| <span data-ttu-id="f7f46-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f7f46-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7f46-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7f46-261">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="f7f46-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7f46-262">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="f7f46-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7f46-263">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="f7f46-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f46-264">Search-Flags</span></span>           | <span data-ttu-id="f7f46-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7f46-265">0x00000000</span></span>                                     |
| <span data-ttu-id="f7f46-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7f46-266">System-Flags</span></span>           | <span data-ttu-id="f7f46-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7f46-267">0x00000010</span></span>                                     |
| <span data-ttu-id="f7f46-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f7f46-268">Classes used in</span></span>        | [<span data-ttu-id="f7f46-269">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="f7f46-269">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





