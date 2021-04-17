---
title: Atributo RDN-ATT-ID
description: El RDN para el atributo que se usa para asignar un nombre a una clase.
ms.assetid: 793199c4-6c5e-481f-8f73-bd59375ab51b
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo RDN-ATT-ID
- rDNAttID esquema de AD de atributos
topic_type:
- apiref
api_name:
- RDN-Att-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b5fb573d289b71bb459cd8595b5df5115f42bf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658760"
---
# <a name="rdn-att-id-attribute"></a><span data-ttu-id="2e8fb-105">Atributo RDN-ATT-ID</span><span class="sxs-lookup"><span data-stu-id="2e8fb-105">RDN-Att-ID attribute</span></span>

<span data-ttu-id="2e8fb-106">El RDN para el atributo que se usa para asignar un nombre a una clase.</span><span class="sxs-lookup"><span data-stu-id="2e8fb-106">The RDN for the attribute that is used to name a class.</span></span>



| <span data-ttu-id="2e8fb-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e8fb-107">Entry</span></span> | <span data-ttu-id="2e8fb-108">Value</span><span class="sxs-lookup"><span data-stu-id="2e8fb-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="2e8fb-109">CN</span><span class="sxs-lookup"><span data-stu-id="2e8fb-109">CN</span></span>                | <span data-ttu-id="2e8fb-110">RDN-ATT-ID</span><span class="sxs-lookup"><span data-stu-id="2e8fb-110">RDN-Att-ID</span></span>                                                      |
| <span data-ttu-id="2e8fb-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="2e8fb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2e8fb-112">rDNAttID</span><span class="sxs-lookup"><span data-stu-id="2e8fb-112">rDNAttID</span></span>                                                        |
| <span data-ttu-id="2e8fb-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="2e8fb-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="2e8fb-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="2e8fb-114">Update Privilege</span></span>  | <span data-ttu-id="2e8fb-115">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="2e8fb-115">Schema administrator</span></span>                                            |
| <span data-ttu-id="2e8fb-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="2e8fb-116">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="2e8fb-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2e8fb-117">Attribute-Id</span></span>      | <span data-ttu-id="2e8fb-118">1.2.840.113556.1.2.26</span><span class="sxs-lookup"><span data-stu-id="2e8fb-118">1.2.840.113556.1.2.26</span></span>                                           |
| <span data-ttu-id="2e8fb-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2e8fb-119">System-Id-Guid</span></span>    | <span data-ttu-id="2e8fb-120">bf967a0f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2e8fb-120">bf967a0f-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="2e8fb-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e8fb-121">Syntax</span></span>            | [<span data-ttu-id="2e8fb-122">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="2e8fb-122">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="2e8fb-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="2e8fb-123">Implementations</span></span>

-   [<span data-ttu-id="2e8fb-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2e8fb-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2e8fb-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2e8fb-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2e8fb-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2e8fb-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2e8fb-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2e8fb-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2e8fb-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2e8fb-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2e8fb-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2e8fb-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2e8fb-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2e8fb-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2e8fb-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e8fb-131">Windows 2000 Server</span></span>



| <span data-ttu-id="2e8fb-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e8fb-132">Entry</span></span> | <span data-ttu-id="2e8fb-133">Value</span><span class="sxs-lookup"><span data-stu-id="2e8fb-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2e8fb-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2e8fb-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e8fb-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e8fb-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e8fb-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e8fb-136">System-Only</span></span>            | <span data-ttu-id="2e8fb-137">True</span><span class="sxs-lookup"><span data-stu-id="2e8fb-137">True</span></span>                                             |
| <span data-ttu-id="2e8fb-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2e8fb-138">Is-Single-Valued</span></span>       | <span data-ttu-id="2e8fb-139">True</span><span class="sxs-lookup"><span data-stu-id="2e8fb-139">True</span></span>                                             |
| <span data-ttu-id="2e8fb-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2e8fb-140">Is Indexed</span></span>             | <span data-ttu-id="2e8fb-141">False</span><span class="sxs-lookup"><span data-stu-id="2e8fb-141">False</span></span>                                            |
| <span data-ttu-id="2e8fb-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2e8fb-142">In Global Catalog</span></span>      | <span data-ttu-id="2e8fb-143">False</span><span class="sxs-lookup"><span data-stu-id="2e8fb-143">False</span></span>                                            |
| <span data-ttu-id="2e8fb-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2e8fb-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e8fb-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e8fb-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2e8fb-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e8fb-146">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2e8fb-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e8fb-147">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2e8fb-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e8fb-148">Search-Flags</span></span>           | <span data-ttu-id="2e8fb-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e8fb-149">0x00000000</span></span>                                       |
| <span data-ttu-id="2e8fb-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e8fb-150">System-Flags</span></span>           | <span data-ttu-id="2e8fb-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e8fb-151">0x00000010</span></span>                                       |
| <span data-ttu-id="2e8fb-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2e8fb-152">Classes used in</span></span>        | [<span data-ttu-id="2e8fb-153">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="2e8fb-153">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2e8fb-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2e8fb-154">Windows Server 2003</span></span>



| <span data-ttu-id="2e8fb-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e8fb-155">Entry</span></span> | <span data-ttu-id="2e8fb-156">Value</span><span class="sxs-lookup"><span data-stu-id="2e8fb-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2e8fb-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2e8fb-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e8fb-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e8fb-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e8fb-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e8fb-159">System-Only</span></span>            | <span data-ttu-id="2e8fb-160">True</span><span class="sxs-lookup"><span data-stu-id="2e8fb-160">True</span></span>                                             |
| <span data-ttu-id="2e8fb-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2e8fb-161">Is-Single-Valued</span></span>       | <span data-ttu-id="2e8fb-162">True</span><span class="sxs-lookup"><span data-stu-id="2e8fb-162">True</span></span>                                             |
| <span data-ttu-id="2e8fb-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2e8fb-163">Is Indexed</span></span>             | <span data-ttu-id="2e8fb-164">False</span><span class="sxs-lookup"><span data-stu-id="2e8fb-164">False</span></span>                                            |
| <span data-ttu-id="2e8fb-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2e8fb-165">In Global Catalog</span></span>      | <span data-ttu-id="2e8fb-166">False</span><span class="sxs-lookup"><span data-stu-id="2e8fb-166">False</span></span>                                            |
| <span data-ttu-id="2e8fb-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2e8fb-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e8fb-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e8fb-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2e8fb-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e8fb-169">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2e8fb-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e8fb-170">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2e8fb-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e8fb-171">Search-Flags</span></span>           | <span data-ttu-id="2e8fb-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e8fb-172">0x00000000</span></span>                                       |
| <span data-ttu-id="2e8fb-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e8fb-173">System-Flags</span></span>           | <span data-ttu-id="2e8fb-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e8fb-174">0x00000010</span></span>                                       |
| <span data-ttu-id="2e8fb-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2e8fb-175">Classes used in</span></span>        | [<span data-ttu-id="2e8fb-176">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="2e8fb-176">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2e8fb-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="2e8fb-177">ADAM</span></span>



| <span data-ttu-id="2e8fb-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e8fb-178">Entry</span></span> | <span data-ttu-id="2e8fb-179">Value</span><span class="sxs-lookup"><span data-stu-id="2e8fb-179">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2e8fb-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2e8fb-180">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e8fb-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e8fb-181">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e8fb-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e8fb-182">System-Only</span></span>            | <span data-ttu-id="2e8fb-183">True</span><span class="sxs-lookup"><span data-stu-id="2e8fb-183">True</span></span>                                             |
| <span data-ttu-id="2e8fb-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2e8fb-184">Is-Single-Valued</span></span>       | <span data-ttu-id="2e8fb-185">True</span><span class="sxs-lookup"><span data-stu-id="2e8fb-185">True</span></span>                                             |
| <span data-ttu-id="2e8fb-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2e8fb-186">Is Indexed</span></span>             | <span data-ttu-id="2e8fb-187">False</span><span class="sxs-lookup"><span data-stu-id="2e8fb-187">False</span></span>                                            |
| <span data-ttu-id="2e8fb-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2e8fb-188">In Global Catalog</span></span>      | <span data-ttu-id="2e8fb-189">False</span><span class="sxs-lookup"><span data-stu-id="2e8fb-189">False</span></span>                                            |
| <span data-ttu-id="2e8fb-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2e8fb-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e8fb-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e8fb-191">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2e8fb-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e8fb-192">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2e8fb-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e8fb-193">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2e8fb-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e8fb-194">Search-Flags</span></span>           | <span data-ttu-id="2e8fb-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e8fb-195">0x00000000</span></span>                                       |
| <span data-ttu-id="2e8fb-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e8fb-196">System-Flags</span></span>           | <span data-ttu-id="2e8fb-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e8fb-197">0x00000010</span></span>                                       |
| <span data-ttu-id="2e8fb-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2e8fb-198">Classes used in</span></span>        | [<span data-ttu-id="2e8fb-199">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="2e8fb-199">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2e8fb-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2e8fb-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2e8fb-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e8fb-201">Entry</span></span> | <span data-ttu-id="2e8fb-202">Value</span><span class="sxs-lookup"><span data-stu-id="2e8fb-202">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2e8fb-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2e8fb-203">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e8fb-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e8fb-204">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e8fb-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e8fb-205">System-Only</span></span>            | <span data-ttu-id="2e8fb-206">True</span><span class="sxs-lookup"><span data-stu-id="2e8fb-206">True</span></span>                                             |
| <span data-ttu-id="2e8fb-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2e8fb-207">Is-Single-Valued</span></span>       | <span data-ttu-id="2e8fb-208">True</span><span class="sxs-lookup"><span data-stu-id="2e8fb-208">True</span></span>                                             |
| <span data-ttu-id="2e8fb-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2e8fb-209">Is Indexed</span></span>             | <span data-ttu-id="2e8fb-210">False</span><span class="sxs-lookup"><span data-stu-id="2e8fb-210">False</span></span>                                            |
| <span data-ttu-id="2e8fb-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2e8fb-211">In Global Catalog</span></span>      | <span data-ttu-id="2e8fb-212">False</span><span class="sxs-lookup"><span data-stu-id="2e8fb-212">False</span></span>                                            |
| <span data-ttu-id="2e8fb-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2e8fb-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e8fb-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e8fb-214">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2e8fb-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e8fb-215">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2e8fb-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e8fb-216">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2e8fb-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e8fb-217">Search-Flags</span></span>           | <span data-ttu-id="2e8fb-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e8fb-218">0x00000000</span></span>                                       |
| <span data-ttu-id="2e8fb-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e8fb-219">System-Flags</span></span>           | <span data-ttu-id="2e8fb-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e8fb-220">0x00000010</span></span>                                       |
| <span data-ttu-id="2e8fb-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2e8fb-221">Classes used in</span></span>        | [<span data-ttu-id="2e8fb-222">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="2e8fb-222">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2e8fb-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e8fb-223">Windows Server 2008</span></span>



| <span data-ttu-id="2e8fb-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e8fb-224">Entry</span></span> | <span data-ttu-id="2e8fb-225">Value</span><span class="sxs-lookup"><span data-stu-id="2e8fb-225">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2e8fb-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2e8fb-226">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e8fb-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e8fb-227">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e8fb-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e8fb-228">System-Only</span></span>            | <span data-ttu-id="2e8fb-229">True</span><span class="sxs-lookup"><span data-stu-id="2e8fb-229">True</span></span>                                             |
| <span data-ttu-id="2e8fb-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2e8fb-230">Is-Single-Valued</span></span>       | <span data-ttu-id="2e8fb-231">True</span><span class="sxs-lookup"><span data-stu-id="2e8fb-231">True</span></span>                                             |
| <span data-ttu-id="2e8fb-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2e8fb-232">Is Indexed</span></span>             | <span data-ttu-id="2e8fb-233">False</span><span class="sxs-lookup"><span data-stu-id="2e8fb-233">False</span></span>                                            |
| <span data-ttu-id="2e8fb-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2e8fb-234">In Global Catalog</span></span>      | <span data-ttu-id="2e8fb-235">False</span><span class="sxs-lookup"><span data-stu-id="2e8fb-235">False</span></span>                                            |
| <span data-ttu-id="2e8fb-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2e8fb-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e8fb-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e8fb-237">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2e8fb-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e8fb-238">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2e8fb-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e8fb-239">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2e8fb-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e8fb-240">Search-Flags</span></span>           | <span data-ttu-id="2e8fb-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e8fb-241">0x00000000</span></span>                                       |
| <span data-ttu-id="2e8fb-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e8fb-242">System-Flags</span></span>           | <span data-ttu-id="2e8fb-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e8fb-243">0x00000010</span></span>                                       |
| <span data-ttu-id="2e8fb-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2e8fb-244">Classes used in</span></span>        | [<span data-ttu-id="2e8fb-245">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="2e8fb-245">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2e8fb-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2e8fb-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2e8fb-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e8fb-247">Entry</span></span> | <span data-ttu-id="2e8fb-248">Value</span><span class="sxs-lookup"><span data-stu-id="2e8fb-248">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2e8fb-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2e8fb-249">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e8fb-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e8fb-250">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e8fb-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e8fb-251">System-Only</span></span>            | <span data-ttu-id="2e8fb-252">True</span><span class="sxs-lookup"><span data-stu-id="2e8fb-252">True</span></span>                                             |
| <span data-ttu-id="2e8fb-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2e8fb-253">Is-Single-Valued</span></span>       | <span data-ttu-id="2e8fb-254">True</span><span class="sxs-lookup"><span data-stu-id="2e8fb-254">True</span></span>                                             |
| <span data-ttu-id="2e8fb-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2e8fb-255">Is Indexed</span></span>             | <span data-ttu-id="2e8fb-256">False</span><span class="sxs-lookup"><span data-stu-id="2e8fb-256">False</span></span>                                            |
| <span data-ttu-id="2e8fb-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2e8fb-257">In Global Catalog</span></span>      | <span data-ttu-id="2e8fb-258">False</span><span class="sxs-lookup"><span data-stu-id="2e8fb-258">False</span></span>                                            |
| <span data-ttu-id="2e8fb-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2e8fb-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e8fb-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e8fb-260">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2e8fb-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e8fb-261">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2e8fb-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e8fb-262">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2e8fb-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e8fb-263">Search-Flags</span></span>           | <span data-ttu-id="2e8fb-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e8fb-264">0x00000000</span></span>                                       |
| <span data-ttu-id="2e8fb-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e8fb-265">System-Flags</span></span>           | <span data-ttu-id="2e8fb-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e8fb-266">0x00000010</span></span>                                       |
| <span data-ttu-id="2e8fb-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2e8fb-267">Classes used in</span></span>        | [<span data-ttu-id="2e8fb-268">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="2e8fb-268">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2e8fb-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e8fb-269">Windows Server 2012</span></span>



| <span data-ttu-id="2e8fb-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e8fb-270">Entry</span></span> | <span data-ttu-id="2e8fb-271">Value</span><span class="sxs-lookup"><span data-stu-id="2e8fb-271">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2e8fb-272">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2e8fb-272">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e8fb-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e8fb-273">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e8fb-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e8fb-274">System-Only</span></span>            | <span data-ttu-id="2e8fb-275">True</span><span class="sxs-lookup"><span data-stu-id="2e8fb-275">True</span></span>                                             |
| <span data-ttu-id="2e8fb-276">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2e8fb-276">Is-Single-Valued</span></span>       | <span data-ttu-id="2e8fb-277">True</span><span class="sxs-lookup"><span data-stu-id="2e8fb-277">True</span></span>                                             |
| <span data-ttu-id="2e8fb-278">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2e8fb-278">Is Indexed</span></span>             | <span data-ttu-id="2e8fb-279">False</span><span class="sxs-lookup"><span data-stu-id="2e8fb-279">False</span></span>                                            |
| <span data-ttu-id="2e8fb-280">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2e8fb-280">In Global Catalog</span></span>      | <span data-ttu-id="2e8fb-281">False</span><span class="sxs-lookup"><span data-stu-id="2e8fb-281">False</span></span>                                            |
| <span data-ttu-id="2e8fb-282">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2e8fb-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e8fb-283">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e8fb-283">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2e8fb-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e8fb-284">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2e8fb-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e8fb-285">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2e8fb-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e8fb-286">Search-Flags</span></span>           | <span data-ttu-id="2e8fb-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e8fb-287">0x00000000</span></span>                                       |
| <span data-ttu-id="2e8fb-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e8fb-288">System-Flags</span></span>           | <span data-ttu-id="2e8fb-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e8fb-289">0x00000010</span></span>                                       |
| <span data-ttu-id="2e8fb-290">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2e8fb-290">Classes used in</span></span>        | [<span data-ttu-id="2e8fb-291">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="2e8fb-291">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





