---
title: Atributo Vol-Table-GUID
description: Identificador único de una entrada de la tabla de seguimiento de vínculos.
ms.assetid: 3a63406a-e751-4234-a601-8f5a57f0a3b7
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo Vol-Table-GUID
- volTableGUID esquema de AD de atributos
topic_type:
- apiref
api_name:
- Vol-Table-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a23bcd088304b4a683ce3ff0f203d3c82fecf8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493655"
---
# <a name="vol-table-guid-attribute"></a><span data-ttu-id="03128-105">Atributo Vol-Table-GUID</span><span class="sxs-lookup"><span data-stu-id="03128-105">Vol-Table-GUID attribute</span></span>

<span data-ttu-id="03128-106">Identificador único de una entrada de la tabla de seguimiento de vínculos.</span><span class="sxs-lookup"><span data-stu-id="03128-106">The unique identifier for a Link-Track-Volume table entry.</span></span>



| <span data-ttu-id="03128-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="03128-107">Entry</span></span> | <span data-ttu-id="03128-108">Value</span><span class="sxs-lookup"><span data-stu-id="03128-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="03128-109">CN</span><span class="sxs-lookup"><span data-stu-id="03128-109">CN</span></span>                | <span data-ttu-id="03128-110">Vol-Table-GUID</span><span class="sxs-lookup"><span data-stu-id="03128-110">Vol-Table-GUID</span></span>                                        |
| <span data-ttu-id="03128-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="03128-111">Ldap-Display-Name</span></span> | <span data-ttu-id="03128-112">volTableGUID</span><span class="sxs-lookup"><span data-stu-id="03128-112">volTableGUID</span></span>                                          |
| <span data-ttu-id="03128-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="03128-113">Size</span></span>              | <span data-ttu-id="03128-114">16 bytes</span><span class="sxs-lookup"><span data-stu-id="03128-114">16 bytes</span></span>                                              |
| <span data-ttu-id="03128-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="03128-115">Update Privilege</span></span>  | <span data-ttu-id="03128-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="03128-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="03128-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="03128-117">Update Frequency</span></span>  | <span data-ttu-id="03128-118">Siempre que se crea un nuevo vínculo a un archivo.</span><span class="sxs-lookup"><span data-stu-id="03128-118">Whenever a new link to a file is created.</span></span>             |
| <span data-ttu-id="03128-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="03128-119">Attribute-Id</span></span>      | <span data-ttu-id="03128-120">1.2.840.113556.1.4.336</span><span class="sxs-lookup"><span data-stu-id="03128-120">1.2.840.113556.1.4.336</span></span>                                |
| <span data-ttu-id="03128-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="03128-121">System-Id-Guid</span></span>    | <span data-ttu-id="03128-122">1f0075fd-7e40-11d0-afd6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="03128-122">1f0075fd-7e40-11d0-afd6-00c04fd930c9</span></span>                  |
| <span data-ttu-id="03128-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03128-123">Syntax</span></span>            | [<span data-ttu-id="03128-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="03128-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="03128-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="03128-125">Implementations</span></span>

-   [<span data-ttu-id="03128-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="03128-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="03128-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="03128-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="03128-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="03128-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="03128-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="03128-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="03128-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="03128-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="03128-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="03128-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="03128-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="03128-132">Windows 2000 Server</span></span>



| <span data-ttu-id="03128-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="03128-133">Entry</span></span> | <span data-ttu-id="03128-134">Value</span><span class="sxs-lookup"><span data-stu-id="03128-134">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="03128-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="03128-135">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="03128-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03128-136">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="03128-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="03128-137">System-Only</span></span>            | <span data-ttu-id="03128-138">False</span><span class="sxs-lookup"><span data-stu-id="03128-138">False</span></span>                                                          |
| <span data-ttu-id="03128-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="03128-139">Is-Single-Valued</span></span>       | <span data-ttu-id="03128-140">True</span><span class="sxs-lookup"><span data-stu-id="03128-140">True</span></span>                                                           |
| <span data-ttu-id="03128-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="03128-141">Is Indexed</span></span>             | <span data-ttu-id="03128-142">False</span><span class="sxs-lookup"><span data-stu-id="03128-142">False</span></span>                                                          |
| <span data-ttu-id="03128-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="03128-143">In Global Catalog</span></span>      | <span data-ttu-id="03128-144">False</span><span class="sxs-lookup"><span data-stu-id="03128-144">False</span></span>                                                          |
| <span data-ttu-id="03128-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="03128-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="03128-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="03128-146">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="03128-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03128-147">Range-Lower</span></span>            | <span data-ttu-id="03128-148">0</span><span class="sxs-lookup"><span data-stu-id="03128-148">0</span></span>                                                              |
| <span data-ttu-id="03128-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03128-149">Range-Upper</span></span>            | <span data-ttu-id="03128-150">16</span><span class="sxs-lookup"><span data-stu-id="03128-150">16</span></span>                                                             |
| <span data-ttu-id="03128-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03128-151">Search-Flags</span></span>           | <span data-ttu-id="03128-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03128-152">0x00000000</span></span>                                                     |
| <span data-ttu-id="03128-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03128-153">System-Flags</span></span>           | <span data-ttu-id="03128-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03128-154">0x00000010</span></span>                                                     |
| <span data-ttu-id="03128-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="03128-155">Classes used in</span></span>        | [<span data-ttu-id="03128-156">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="03128-156">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="03128-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="03128-157">Windows Server 2003</span></span>



| <span data-ttu-id="03128-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="03128-158">Entry</span></span> | <span data-ttu-id="03128-159">Value</span><span class="sxs-lookup"><span data-stu-id="03128-159">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="03128-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="03128-160">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="03128-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03128-161">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="03128-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="03128-162">System-Only</span></span>            | <span data-ttu-id="03128-163">False</span><span class="sxs-lookup"><span data-stu-id="03128-163">False</span></span>                                                          |
| <span data-ttu-id="03128-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="03128-164">Is-Single-Valued</span></span>       | <span data-ttu-id="03128-165">True</span><span class="sxs-lookup"><span data-stu-id="03128-165">True</span></span>                                                           |
| <span data-ttu-id="03128-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="03128-166">Is Indexed</span></span>             | <span data-ttu-id="03128-167">False</span><span class="sxs-lookup"><span data-stu-id="03128-167">False</span></span>                                                          |
| <span data-ttu-id="03128-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="03128-168">In Global Catalog</span></span>      | <span data-ttu-id="03128-169">False</span><span class="sxs-lookup"><span data-stu-id="03128-169">False</span></span>                                                          |
| <span data-ttu-id="03128-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="03128-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="03128-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="03128-171">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="03128-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03128-172">Range-Lower</span></span>            | <span data-ttu-id="03128-173">0</span><span class="sxs-lookup"><span data-stu-id="03128-173">0</span></span>                                                              |
| <span data-ttu-id="03128-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03128-174">Range-Upper</span></span>            | <span data-ttu-id="03128-175">16</span><span class="sxs-lookup"><span data-stu-id="03128-175">16</span></span>                                                             |
| <span data-ttu-id="03128-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03128-176">Search-Flags</span></span>           | <span data-ttu-id="03128-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03128-177">0x00000000</span></span>                                                     |
| <span data-ttu-id="03128-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03128-178">System-Flags</span></span>           | <span data-ttu-id="03128-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03128-179">0x00000010</span></span>                                                     |
| <span data-ttu-id="03128-180">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="03128-180">Classes used in</span></span>        | [<span data-ttu-id="03128-181">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="03128-181">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="03128-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="03128-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="03128-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="03128-183">Entry</span></span> | <span data-ttu-id="03128-184">Value</span><span class="sxs-lookup"><span data-stu-id="03128-184">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="03128-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="03128-185">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="03128-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03128-186">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="03128-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="03128-187">System-Only</span></span>            | <span data-ttu-id="03128-188">False</span><span class="sxs-lookup"><span data-stu-id="03128-188">False</span></span>                                                          |
| <span data-ttu-id="03128-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="03128-189">Is-Single-Valued</span></span>       | <span data-ttu-id="03128-190">True</span><span class="sxs-lookup"><span data-stu-id="03128-190">True</span></span>                                                           |
| <span data-ttu-id="03128-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="03128-191">Is Indexed</span></span>             | <span data-ttu-id="03128-192">False</span><span class="sxs-lookup"><span data-stu-id="03128-192">False</span></span>                                                          |
| <span data-ttu-id="03128-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="03128-193">In Global Catalog</span></span>      | <span data-ttu-id="03128-194">False</span><span class="sxs-lookup"><span data-stu-id="03128-194">False</span></span>                                                          |
| <span data-ttu-id="03128-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="03128-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="03128-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="03128-196">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="03128-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03128-197">Range-Lower</span></span>            | <span data-ttu-id="03128-198">0</span><span class="sxs-lookup"><span data-stu-id="03128-198">0</span></span>                                                              |
| <span data-ttu-id="03128-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03128-199">Range-Upper</span></span>            | <span data-ttu-id="03128-200">16</span><span class="sxs-lookup"><span data-stu-id="03128-200">16</span></span>                                                             |
| <span data-ttu-id="03128-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03128-201">Search-Flags</span></span>           | <span data-ttu-id="03128-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03128-202">0x00000000</span></span>                                                     |
| <span data-ttu-id="03128-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03128-203">System-Flags</span></span>           | <span data-ttu-id="03128-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03128-204">0x00000010</span></span>                                                     |
| <span data-ttu-id="03128-205">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="03128-205">Classes used in</span></span>        | [<span data-ttu-id="03128-206">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="03128-206">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="03128-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03128-207">Windows Server 2008</span></span>



| <span data-ttu-id="03128-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="03128-208">Entry</span></span> | <span data-ttu-id="03128-209">Value</span><span class="sxs-lookup"><span data-stu-id="03128-209">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="03128-210">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="03128-210">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="03128-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03128-211">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="03128-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="03128-212">System-Only</span></span>            | <span data-ttu-id="03128-213">False</span><span class="sxs-lookup"><span data-stu-id="03128-213">False</span></span>                                                          |
| <span data-ttu-id="03128-214">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="03128-214">Is-Single-Valued</span></span>       | <span data-ttu-id="03128-215">True</span><span class="sxs-lookup"><span data-stu-id="03128-215">True</span></span>                                                           |
| <span data-ttu-id="03128-216">Está indexado</span><span class="sxs-lookup"><span data-stu-id="03128-216">Is Indexed</span></span>             | <span data-ttu-id="03128-217">False</span><span class="sxs-lookup"><span data-stu-id="03128-217">False</span></span>                                                          |
| <span data-ttu-id="03128-218">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="03128-218">In Global Catalog</span></span>      | <span data-ttu-id="03128-219">False</span><span class="sxs-lookup"><span data-stu-id="03128-219">False</span></span>                                                          |
| <span data-ttu-id="03128-220">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="03128-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="03128-221">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="03128-221">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="03128-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03128-222">Range-Lower</span></span>            | <span data-ttu-id="03128-223">0</span><span class="sxs-lookup"><span data-stu-id="03128-223">0</span></span>                                                              |
| <span data-ttu-id="03128-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03128-224">Range-Upper</span></span>            | <span data-ttu-id="03128-225">16</span><span class="sxs-lookup"><span data-stu-id="03128-225">16</span></span>                                                             |
| <span data-ttu-id="03128-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03128-226">Search-Flags</span></span>           | <span data-ttu-id="03128-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03128-227">0x00000000</span></span>                                                     |
| <span data-ttu-id="03128-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03128-228">System-Flags</span></span>           | <span data-ttu-id="03128-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03128-229">0x00000010</span></span>                                                     |
| <span data-ttu-id="03128-230">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="03128-230">Classes used in</span></span>        | [<span data-ttu-id="03128-231">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="03128-231">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="03128-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="03128-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="03128-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="03128-233">Entry</span></span> | <span data-ttu-id="03128-234">Value</span><span class="sxs-lookup"><span data-stu-id="03128-234">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="03128-235">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="03128-235">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="03128-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03128-236">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="03128-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="03128-237">System-Only</span></span>            | <span data-ttu-id="03128-238">False</span><span class="sxs-lookup"><span data-stu-id="03128-238">False</span></span>                                                          |
| <span data-ttu-id="03128-239">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="03128-239">Is-Single-Valued</span></span>       | <span data-ttu-id="03128-240">True</span><span class="sxs-lookup"><span data-stu-id="03128-240">True</span></span>                                                           |
| <span data-ttu-id="03128-241">Está indexado</span><span class="sxs-lookup"><span data-stu-id="03128-241">Is Indexed</span></span>             | <span data-ttu-id="03128-242">False</span><span class="sxs-lookup"><span data-stu-id="03128-242">False</span></span>                                                          |
| <span data-ttu-id="03128-243">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="03128-243">In Global Catalog</span></span>      | <span data-ttu-id="03128-244">False</span><span class="sxs-lookup"><span data-stu-id="03128-244">False</span></span>                                                          |
| <span data-ttu-id="03128-245">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="03128-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="03128-246">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="03128-246">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="03128-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03128-247">Range-Lower</span></span>            | <span data-ttu-id="03128-248">0</span><span class="sxs-lookup"><span data-stu-id="03128-248">0</span></span>                                                              |
| <span data-ttu-id="03128-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03128-249">Range-Upper</span></span>            | <span data-ttu-id="03128-250">16</span><span class="sxs-lookup"><span data-stu-id="03128-250">16</span></span>                                                             |
| <span data-ttu-id="03128-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03128-251">Search-Flags</span></span>           | <span data-ttu-id="03128-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03128-252">0x00000000</span></span>                                                     |
| <span data-ttu-id="03128-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03128-253">System-Flags</span></span>           | <span data-ttu-id="03128-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03128-254">0x00000010</span></span>                                                     |
| <span data-ttu-id="03128-255">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="03128-255">Classes used in</span></span>        | [<span data-ttu-id="03128-256">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="03128-256">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="03128-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="03128-257">Windows Server 2012</span></span>



| <span data-ttu-id="03128-258">Entrada</span><span class="sxs-lookup"><span data-stu-id="03128-258">Entry</span></span> | <span data-ttu-id="03128-259">Value</span><span class="sxs-lookup"><span data-stu-id="03128-259">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="03128-260">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="03128-260">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="03128-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03128-261">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="03128-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="03128-262">System-Only</span></span>            | <span data-ttu-id="03128-263">False</span><span class="sxs-lookup"><span data-stu-id="03128-263">False</span></span>                                                          |
| <span data-ttu-id="03128-264">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="03128-264">Is-Single-Valued</span></span>       | <span data-ttu-id="03128-265">True</span><span class="sxs-lookup"><span data-stu-id="03128-265">True</span></span>                                                           |
| <span data-ttu-id="03128-266">Está indexado</span><span class="sxs-lookup"><span data-stu-id="03128-266">Is Indexed</span></span>             | <span data-ttu-id="03128-267">False</span><span class="sxs-lookup"><span data-stu-id="03128-267">False</span></span>                                                          |
| <span data-ttu-id="03128-268">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="03128-268">In Global Catalog</span></span>      | <span data-ttu-id="03128-269">False</span><span class="sxs-lookup"><span data-stu-id="03128-269">False</span></span>                                                          |
| <span data-ttu-id="03128-270">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="03128-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="03128-271">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="03128-271">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="03128-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03128-272">Range-Lower</span></span>            | <span data-ttu-id="03128-273">0</span><span class="sxs-lookup"><span data-stu-id="03128-273">0</span></span>                                                              |
| <span data-ttu-id="03128-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03128-274">Range-Upper</span></span>            | <span data-ttu-id="03128-275">16</span><span class="sxs-lookup"><span data-stu-id="03128-275">16</span></span>                                                             |
| <span data-ttu-id="03128-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03128-276">Search-Flags</span></span>           | <span data-ttu-id="03128-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03128-277">0x00000000</span></span>                                                     |
| <span data-ttu-id="03128-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03128-278">System-Flags</span></span>           | <span data-ttu-id="03128-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03128-279">0x00000010</span></span>                                                     |
| <span data-ttu-id="03128-280">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="03128-280">Classes used in</span></span>        | [<span data-ttu-id="03128-281">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="03128-281">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





