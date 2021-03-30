---
title: USN-Source atributo)
description: Valor del atributo USN-Changed del objeto del directorio remoto que ha replicado el cambio en el servidor local.
ms.assetid: b307f84a-3ab1-4bfa-afc2-e74055f2a652
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de USN-Source
- uSNSource esquema de AD de atributos
topic_type:
- apiref
api_name:
- USN-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0998ffb73fc02511d77440550c8c669b35a98563
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104422665"
---
# <a name="usn-source-attribute"></a><span data-ttu-id="38868-105">USN-Source atributo)</span><span class="sxs-lookup"><span data-stu-id="38868-105">USN-Source attribute</span></span>

<span data-ttu-id="38868-106">Valor del atributo [**USN-Changed**](a-usnchanged.md) del objeto del directorio remoto que ha replicado el cambio en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="38868-106">Value of the [**USN-Changed**](a-usnchanged.md) attribute of the object from the remote directory that replicated the change to the local server.</span></span>



| <span data-ttu-id="38868-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="38868-107">Entry</span></span> | <span data-ttu-id="38868-108">Value</span><span class="sxs-lookup"><span data-stu-id="38868-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38868-109">CN</span><span class="sxs-lookup"><span data-stu-id="38868-109">CN</span></span>                | <span data-ttu-id="38868-110">USN-Source</span><span class="sxs-lookup"><span data-stu-id="38868-110">USN-Source</span></span>                                                                                          |
| <span data-ttu-id="38868-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="38868-111">Ldap-Display-Name</span></span> | <span data-ttu-id="38868-112">uSNSource</span><span class="sxs-lookup"><span data-stu-id="38868-112">uSNSource</span></span>                                                                                           |
| <span data-ttu-id="38868-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="38868-113">Size</span></span>              | <span data-ttu-id="38868-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="38868-114">8 bytes</span></span>                                                                                             |
| <span data-ttu-id="38868-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="38868-115">Update Privilege</span></span>  | <span data-ttu-id="38868-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="38868-116">This value is set by the system.</span></span>                                                                    |
| <span data-ttu-id="38868-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="38868-117">Update Frequency</span></span>  | <span data-ttu-id="38868-118">Cuando el objeto se cambia en un directorio remoto que replica el cambio en el directorio local.</span><span class="sxs-lookup"><span data-stu-id="38868-118">When the object is changed on a remote directory that replicated the change to the local directory.</span></span> |
| <span data-ttu-id="38868-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="38868-119">Attribute-Id</span></span>      | <span data-ttu-id="38868-120">1.2.840.113556.1.4.896</span><span class="sxs-lookup"><span data-stu-id="38868-120">1.2.840.113556.1.4.896</span></span>                                                                              |
| <span data-ttu-id="38868-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="38868-121">System-Id-Guid</span></span>    | <span data-ttu-id="38868-122">167758ad-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="38868-122">167758ad-47f3-11d1-a9c3-0000f80367c1</span></span>                                                                |
| <span data-ttu-id="38868-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38868-123">Syntax</span></span>            | [<span data-ttu-id="38868-124">**Interval**</span><span class="sxs-lookup"><span data-stu-id="38868-124">**Interval**</span></span>](s-interval.md)                                                                      |



## <a name="implementations"></a><span data-ttu-id="38868-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="38868-125">Implementations</span></span>

-   [<span data-ttu-id="38868-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="38868-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="38868-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="38868-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="38868-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="38868-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="38868-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="38868-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="38868-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="38868-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="38868-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="38868-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="38868-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="38868-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="38868-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="38868-133">Windows 2000 Server</span></span>



| <span data-ttu-id="38868-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="38868-134">Entry</span></span> | <span data-ttu-id="38868-135">Value</span><span class="sxs-lookup"><span data-stu-id="38868-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="38868-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38868-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="38868-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38868-137">MAPI-Id</span></span>                | <span data-ttu-id="38868-138">0x8157</span><span class="sxs-lookup"><span data-stu-id="38868-138">0x8157</span></span>                          |
| <span data-ttu-id="38868-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="38868-139">System-Only</span></span>            | <span data-ttu-id="38868-140">False</span><span class="sxs-lookup"><span data-stu-id="38868-140">False</span></span>                           |
| <span data-ttu-id="38868-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38868-141">Is-Single-Valued</span></span>       | <span data-ttu-id="38868-142">True</span><span class="sxs-lookup"><span data-stu-id="38868-142">True</span></span>                            |
| <span data-ttu-id="38868-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38868-143">Is Indexed</span></span>             | <span data-ttu-id="38868-144">False</span><span class="sxs-lookup"><span data-stu-id="38868-144">False</span></span>                           |
| <span data-ttu-id="38868-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38868-145">In Global Catalog</span></span>      | <span data-ttu-id="38868-146">False</span><span class="sxs-lookup"><span data-stu-id="38868-146">False</span></span>                           |
| <span data-ttu-id="38868-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38868-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="38868-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38868-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="38868-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38868-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="38868-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38868-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="38868-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38868-151">Search-Flags</span></span>           | <span data-ttu-id="38868-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38868-152">0x00000000</span></span>                      |
| <span data-ttu-id="38868-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38868-153">System-Flags</span></span>           | <span data-ttu-id="38868-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38868-154">0x00000010</span></span>                      |
| <span data-ttu-id="38868-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38868-155">Classes used in</span></span>        | [<span data-ttu-id="38868-156">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="38868-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="38868-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="38868-157">Windows Server 2003</span></span>



| <span data-ttu-id="38868-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="38868-158">Entry</span></span> | <span data-ttu-id="38868-159">Value</span><span class="sxs-lookup"><span data-stu-id="38868-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="38868-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38868-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="38868-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38868-161">MAPI-Id</span></span>                | <span data-ttu-id="38868-162">0x8157</span><span class="sxs-lookup"><span data-stu-id="38868-162">0x8157</span></span>                          |
| <span data-ttu-id="38868-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="38868-163">System-Only</span></span>            | <span data-ttu-id="38868-164">False</span><span class="sxs-lookup"><span data-stu-id="38868-164">False</span></span>                           |
| <span data-ttu-id="38868-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38868-165">Is-Single-Valued</span></span>       | <span data-ttu-id="38868-166">True</span><span class="sxs-lookup"><span data-stu-id="38868-166">True</span></span>                            |
| <span data-ttu-id="38868-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38868-167">Is Indexed</span></span>             | <span data-ttu-id="38868-168">False</span><span class="sxs-lookup"><span data-stu-id="38868-168">False</span></span>                           |
| <span data-ttu-id="38868-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38868-169">In Global Catalog</span></span>      | <span data-ttu-id="38868-170">False</span><span class="sxs-lookup"><span data-stu-id="38868-170">False</span></span>                           |
| <span data-ttu-id="38868-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38868-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="38868-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38868-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="38868-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38868-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="38868-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38868-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="38868-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38868-175">Search-Flags</span></span>           | <span data-ttu-id="38868-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38868-176">0x00000000</span></span>                      |
| <span data-ttu-id="38868-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38868-177">System-Flags</span></span>           | <span data-ttu-id="38868-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38868-178">0x00000010</span></span>                      |
| <span data-ttu-id="38868-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38868-179">Classes used in</span></span>        | [<span data-ttu-id="38868-180">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="38868-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="38868-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="38868-181">ADAM</span></span>



| <span data-ttu-id="38868-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="38868-182">Entry</span></span> | <span data-ttu-id="38868-183">Value</span><span class="sxs-lookup"><span data-stu-id="38868-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="38868-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38868-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="38868-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38868-185">MAPI-Id</span></span>                | <span data-ttu-id="38868-186">0x8157</span><span class="sxs-lookup"><span data-stu-id="38868-186">0x8157</span></span>                          |
| <span data-ttu-id="38868-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="38868-187">System-Only</span></span>            | <span data-ttu-id="38868-188">False</span><span class="sxs-lookup"><span data-stu-id="38868-188">False</span></span>                           |
| <span data-ttu-id="38868-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38868-189">Is-Single-Valued</span></span>       | <span data-ttu-id="38868-190">True</span><span class="sxs-lookup"><span data-stu-id="38868-190">True</span></span>                            |
| <span data-ttu-id="38868-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38868-191">Is Indexed</span></span>             | <span data-ttu-id="38868-192">False</span><span class="sxs-lookup"><span data-stu-id="38868-192">False</span></span>                           |
| <span data-ttu-id="38868-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38868-193">In Global Catalog</span></span>      | <span data-ttu-id="38868-194">False</span><span class="sxs-lookup"><span data-stu-id="38868-194">False</span></span>                           |
| <span data-ttu-id="38868-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38868-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="38868-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38868-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="38868-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38868-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="38868-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38868-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="38868-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38868-199">Search-Flags</span></span>           | <span data-ttu-id="38868-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38868-200">0x00000000</span></span>                      |
| <span data-ttu-id="38868-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38868-201">System-Flags</span></span>           | <span data-ttu-id="38868-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38868-202">0x00000010</span></span>                      |
| <span data-ttu-id="38868-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38868-203">Classes used in</span></span>        | [<span data-ttu-id="38868-204">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="38868-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="38868-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="38868-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="38868-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="38868-206">Entry</span></span> | <span data-ttu-id="38868-207">Value</span><span class="sxs-lookup"><span data-stu-id="38868-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="38868-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38868-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="38868-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38868-209">MAPI-Id</span></span>                | <span data-ttu-id="38868-210">0x8157</span><span class="sxs-lookup"><span data-stu-id="38868-210">0x8157</span></span>                          |
| <span data-ttu-id="38868-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="38868-211">System-Only</span></span>            | <span data-ttu-id="38868-212">False</span><span class="sxs-lookup"><span data-stu-id="38868-212">False</span></span>                           |
| <span data-ttu-id="38868-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38868-213">Is-Single-Valued</span></span>       | <span data-ttu-id="38868-214">True</span><span class="sxs-lookup"><span data-stu-id="38868-214">True</span></span>                            |
| <span data-ttu-id="38868-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38868-215">Is Indexed</span></span>             | <span data-ttu-id="38868-216">False</span><span class="sxs-lookup"><span data-stu-id="38868-216">False</span></span>                           |
| <span data-ttu-id="38868-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38868-217">In Global Catalog</span></span>      | <span data-ttu-id="38868-218">False</span><span class="sxs-lookup"><span data-stu-id="38868-218">False</span></span>                           |
| <span data-ttu-id="38868-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38868-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="38868-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38868-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="38868-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38868-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="38868-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38868-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="38868-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38868-223">Search-Flags</span></span>           | <span data-ttu-id="38868-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38868-224">0x00000000</span></span>                      |
| <span data-ttu-id="38868-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38868-225">System-Flags</span></span>           | <span data-ttu-id="38868-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38868-226">0x00000010</span></span>                      |
| <span data-ttu-id="38868-227">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38868-227">Classes used in</span></span>        | [<span data-ttu-id="38868-228">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="38868-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="38868-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38868-229">Windows Server 2008</span></span>



| <span data-ttu-id="38868-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="38868-230">Entry</span></span> | <span data-ttu-id="38868-231">Value</span><span class="sxs-lookup"><span data-stu-id="38868-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="38868-232">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38868-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="38868-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38868-233">MAPI-Id</span></span>                | <span data-ttu-id="38868-234">0x8157</span><span class="sxs-lookup"><span data-stu-id="38868-234">0x8157</span></span>                          |
| <span data-ttu-id="38868-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="38868-235">System-Only</span></span>            | <span data-ttu-id="38868-236">False</span><span class="sxs-lookup"><span data-stu-id="38868-236">False</span></span>                           |
| <span data-ttu-id="38868-237">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38868-237">Is-Single-Valued</span></span>       | <span data-ttu-id="38868-238">True</span><span class="sxs-lookup"><span data-stu-id="38868-238">True</span></span>                            |
| <span data-ttu-id="38868-239">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38868-239">Is Indexed</span></span>             | <span data-ttu-id="38868-240">False</span><span class="sxs-lookup"><span data-stu-id="38868-240">False</span></span>                           |
| <span data-ttu-id="38868-241">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38868-241">In Global Catalog</span></span>      | <span data-ttu-id="38868-242">False</span><span class="sxs-lookup"><span data-stu-id="38868-242">False</span></span>                           |
| <span data-ttu-id="38868-243">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38868-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="38868-244">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38868-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="38868-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38868-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="38868-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38868-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="38868-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38868-247">Search-Flags</span></span>           | <span data-ttu-id="38868-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38868-248">0x00000000</span></span>                      |
| <span data-ttu-id="38868-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38868-249">System-Flags</span></span>           | <span data-ttu-id="38868-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38868-250">0x00000010</span></span>                      |
| <span data-ttu-id="38868-251">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38868-251">Classes used in</span></span>        | [<span data-ttu-id="38868-252">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="38868-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="38868-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="38868-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="38868-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="38868-254">Entry</span></span> | <span data-ttu-id="38868-255">Value</span><span class="sxs-lookup"><span data-stu-id="38868-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="38868-256">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38868-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="38868-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38868-257">MAPI-Id</span></span>                | <span data-ttu-id="38868-258">0x8157</span><span class="sxs-lookup"><span data-stu-id="38868-258">0x8157</span></span>                          |
| <span data-ttu-id="38868-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="38868-259">System-Only</span></span>            | <span data-ttu-id="38868-260">False</span><span class="sxs-lookup"><span data-stu-id="38868-260">False</span></span>                           |
| <span data-ttu-id="38868-261">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38868-261">Is-Single-Valued</span></span>       | <span data-ttu-id="38868-262">True</span><span class="sxs-lookup"><span data-stu-id="38868-262">True</span></span>                            |
| <span data-ttu-id="38868-263">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38868-263">Is Indexed</span></span>             | <span data-ttu-id="38868-264">False</span><span class="sxs-lookup"><span data-stu-id="38868-264">False</span></span>                           |
| <span data-ttu-id="38868-265">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38868-265">In Global Catalog</span></span>      | <span data-ttu-id="38868-266">False</span><span class="sxs-lookup"><span data-stu-id="38868-266">False</span></span>                           |
| <span data-ttu-id="38868-267">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38868-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="38868-268">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38868-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="38868-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38868-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="38868-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38868-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="38868-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38868-271">Search-Flags</span></span>           | <span data-ttu-id="38868-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38868-272">0x00000000</span></span>                      |
| <span data-ttu-id="38868-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38868-273">System-Flags</span></span>           | <span data-ttu-id="38868-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38868-274">0x00000010</span></span>                      |
| <span data-ttu-id="38868-275">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38868-275">Classes used in</span></span>        | [<span data-ttu-id="38868-276">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="38868-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="38868-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38868-277">Windows Server 2012</span></span>



| <span data-ttu-id="38868-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="38868-278">Entry</span></span> | <span data-ttu-id="38868-279">Value</span><span class="sxs-lookup"><span data-stu-id="38868-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="38868-280">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38868-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="38868-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38868-281">MAPI-Id</span></span>                | <span data-ttu-id="38868-282">0x8157</span><span class="sxs-lookup"><span data-stu-id="38868-282">0x8157</span></span>                          |
| <span data-ttu-id="38868-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="38868-283">System-Only</span></span>            | <span data-ttu-id="38868-284">False</span><span class="sxs-lookup"><span data-stu-id="38868-284">False</span></span>                           |
| <span data-ttu-id="38868-285">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38868-285">Is-Single-Valued</span></span>       | <span data-ttu-id="38868-286">True</span><span class="sxs-lookup"><span data-stu-id="38868-286">True</span></span>                            |
| <span data-ttu-id="38868-287">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38868-287">Is Indexed</span></span>             | <span data-ttu-id="38868-288">False</span><span class="sxs-lookup"><span data-stu-id="38868-288">False</span></span>                           |
| <span data-ttu-id="38868-289">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38868-289">In Global Catalog</span></span>      | <span data-ttu-id="38868-290">False</span><span class="sxs-lookup"><span data-stu-id="38868-290">False</span></span>                           |
| <span data-ttu-id="38868-291">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38868-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="38868-292">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38868-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="38868-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38868-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="38868-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38868-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="38868-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38868-295">Search-Flags</span></span>           | <span data-ttu-id="38868-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38868-296">0x00000000</span></span>                      |
| <span data-ttu-id="38868-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38868-297">System-Flags</span></span>           | <span data-ttu-id="38868-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38868-298">0x00000010</span></span>                      |
| <span data-ttu-id="38868-299">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38868-299">Classes used in</span></span>        | [<span data-ttu-id="38868-300">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="38868-300">**Top**</span></span>](c-top.md)<br/> |



 

 





