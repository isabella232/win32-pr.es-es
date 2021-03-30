---
title: 'Sistema: atributo puede contener'
description: Lista de atributos opcionales para una clase. El sistema solo puede modificar la lista de atributos.
ms.assetid: b2fbeb64-d147-4c1a-a609-4f16327609ce
ms.tgt_platform: multiple
keywords:
- 'Sistema: esquema de AD-puede contener atributo'
- systemMayContain esquema de AD de atributos
topic_type:
- apiref
api_name:
- System-May-Contain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03730e9904cbaa6ee5954662556fba261c51cd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151560"
---
# <a name="system-may-contain-attribute"></a><span data-ttu-id="86e31-106">Sistema: atributo puede contener</span><span class="sxs-lookup"><span data-stu-id="86e31-106">System-May-Contain attribute</span></span>

<span data-ttu-id="86e31-107">Lista de atributos opcionales para una clase.</span><span class="sxs-lookup"><span data-stu-id="86e31-107">The list of optional attributes for a class.</span></span> <span data-ttu-id="86e31-108">El sistema solo puede modificar la lista de atributos.</span><span class="sxs-lookup"><span data-stu-id="86e31-108">The list of attributes can only be modified by the system.</span></span>



| <span data-ttu-id="86e31-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="86e31-109">Entry</span></span> | <span data-ttu-id="86e31-110">Value</span><span class="sxs-lookup"><span data-stu-id="86e31-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="86e31-111">CN</span><span class="sxs-lookup"><span data-stu-id="86e31-111">CN</span></span>                | <span data-ttu-id="86e31-112">Sistema: puede contener</span><span class="sxs-lookup"><span data-stu-id="86e31-112">System-May-Contain</span></span>                                                           |
| <span data-ttu-id="86e31-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="86e31-113">Ldap-Display-Name</span></span> | <span data-ttu-id="86e31-114">systemMayContain</span><span class="sxs-lookup"><span data-stu-id="86e31-114">systemMayContain</span></span>                                                             |
| <span data-ttu-id="86e31-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="86e31-115">Size</span></span>              | \-                                                                           |
| <span data-ttu-id="86e31-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="86e31-116">Update Privilege</span></span>  | <span data-ttu-id="86e31-117">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="86e31-117">Schema administrator</span></span>                                                         |
| <span data-ttu-id="86e31-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="86e31-118">Update Frequency</span></span>  | <span data-ttu-id="86e31-119">Cuando se crea la clase o se agrega un nuevo atributo opcional a la clase.</span><span class="sxs-lookup"><span data-stu-id="86e31-119">When the class is created or a new optional attribute is added to the class.</span></span> |
| <span data-ttu-id="86e31-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="86e31-120">Attribute-Id</span></span>      | <span data-ttu-id="86e31-121">1.2.840.113556.1.4.196</span><span class="sxs-lookup"><span data-stu-id="86e31-121">1.2.840.113556.1.4.196</span></span>                                                       |
| <span data-ttu-id="86e31-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="86e31-122">System-Id-Guid</span></span>    | <span data-ttu-id="86e31-123">bf967a44-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="86e31-123">bf967a44-0de6-11d0-a285-00aa003049e2</span></span>                                         |
| <span data-ttu-id="86e31-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86e31-124">Syntax</span></span>            | [<span data-ttu-id="86e31-125">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="86e31-125">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)              |



## <a name="implementations"></a><span data-ttu-id="86e31-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="86e31-126">Implementations</span></span>

-   [<span data-ttu-id="86e31-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="86e31-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="86e31-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="86e31-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="86e31-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="86e31-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="86e31-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="86e31-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="86e31-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="86e31-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="86e31-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="86e31-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="86e31-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="86e31-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="86e31-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="86e31-134">Windows 2000 Server</span></span>



| <span data-ttu-id="86e31-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="86e31-135">Entry</span></span> | <span data-ttu-id="86e31-136">Value</span><span class="sxs-lookup"><span data-stu-id="86e31-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="86e31-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="86e31-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="86e31-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86e31-138">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="86e31-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="86e31-139">System-Only</span></span>            | <span data-ttu-id="86e31-140">True</span><span class="sxs-lookup"><span data-stu-id="86e31-140">True</span></span>                                             |
| <span data-ttu-id="86e31-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="86e31-141">Is-Single-Valued</span></span>       | <span data-ttu-id="86e31-142">False</span><span class="sxs-lookup"><span data-stu-id="86e31-142">False</span></span>                                            |
| <span data-ttu-id="86e31-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="86e31-143">Is Indexed</span></span>             | <span data-ttu-id="86e31-144">False</span><span class="sxs-lookup"><span data-stu-id="86e31-144">False</span></span>                                            |
| <span data-ttu-id="86e31-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="86e31-145">In Global Catalog</span></span>      | <span data-ttu-id="86e31-146">False</span><span class="sxs-lookup"><span data-stu-id="86e31-146">False</span></span>                                            |
| <span data-ttu-id="86e31-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="86e31-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="86e31-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="86e31-148">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="86e31-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86e31-149">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="86e31-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86e31-150">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="86e31-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86e31-151">Search-Flags</span></span>           | <span data-ttu-id="86e31-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86e31-152">0x00000000</span></span>                                       |
| <span data-ttu-id="86e31-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86e31-153">System-Flags</span></span>           | <span data-ttu-id="86e31-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86e31-154">0x00000010</span></span>                                       |
| <span data-ttu-id="86e31-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="86e31-155">Classes used in</span></span>        | [<span data-ttu-id="86e31-156">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="86e31-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="86e31-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="86e31-157">Windows Server 2003</span></span>



| <span data-ttu-id="86e31-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="86e31-158">Entry</span></span> | <span data-ttu-id="86e31-159">Value</span><span class="sxs-lookup"><span data-stu-id="86e31-159">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="86e31-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="86e31-160">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="86e31-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86e31-161">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="86e31-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="86e31-162">System-Only</span></span>            | <span data-ttu-id="86e31-163">True</span><span class="sxs-lookup"><span data-stu-id="86e31-163">True</span></span>                                             |
| <span data-ttu-id="86e31-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="86e31-164">Is-Single-Valued</span></span>       | <span data-ttu-id="86e31-165">False</span><span class="sxs-lookup"><span data-stu-id="86e31-165">False</span></span>                                            |
| <span data-ttu-id="86e31-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="86e31-166">Is Indexed</span></span>             | <span data-ttu-id="86e31-167">False</span><span class="sxs-lookup"><span data-stu-id="86e31-167">False</span></span>                                            |
| <span data-ttu-id="86e31-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="86e31-168">In Global Catalog</span></span>      | <span data-ttu-id="86e31-169">False</span><span class="sxs-lookup"><span data-stu-id="86e31-169">False</span></span>                                            |
| <span data-ttu-id="86e31-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="86e31-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="86e31-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="86e31-171">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="86e31-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86e31-172">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="86e31-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86e31-173">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="86e31-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86e31-174">Search-Flags</span></span>           | <span data-ttu-id="86e31-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86e31-175">0x00000000</span></span>                                       |
| <span data-ttu-id="86e31-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86e31-176">System-Flags</span></span>           | <span data-ttu-id="86e31-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86e31-177">0x00000010</span></span>                                       |
| <span data-ttu-id="86e31-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="86e31-178">Classes used in</span></span>        | [<span data-ttu-id="86e31-179">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="86e31-179">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="86e31-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="86e31-180">ADAM</span></span>



| <span data-ttu-id="86e31-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="86e31-181">Entry</span></span> | <span data-ttu-id="86e31-182">Value</span><span class="sxs-lookup"><span data-stu-id="86e31-182">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="86e31-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="86e31-183">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="86e31-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86e31-184">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="86e31-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="86e31-185">System-Only</span></span>            | <span data-ttu-id="86e31-186">True</span><span class="sxs-lookup"><span data-stu-id="86e31-186">True</span></span>                                             |
| <span data-ttu-id="86e31-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="86e31-187">Is-Single-Valued</span></span>       | <span data-ttu-id="86e31-188">False</span><span class="sxs-lookup"><span data-stu-id="86e31-188">False</span></span>                                            |
| <span data-ttu-id="86e31-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="86e31-189">Is Indexed</span></span>             | <span data-ttu-id="86e31-190">False</span><span class="sxs-lookup"><span data-stu-id="86e31-190">False</span></span>                                            |
| <span data-ttu-id="86e31-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="86e31-191">In Global Catalog</span></span>      | <span data-ttu-id="86e31-192">False</span><span class="sxs-lookup"><span data-stu-id="86e31-192">False</span></span>                                            |
| <span data-ttu-id="86e31-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="86e31-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="86e31-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="86e31-194">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="86e31-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86e31-195">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="86e31-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86e31-196">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="86e31-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86e31-197">Search-Flags</span></span>           | <span data-ttu-id="86e31-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86e31-198">0x00000000</span></span>                                       |
| <span data-ttu-id="86e31-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86e31-199">System-Flags</span></span>           | <span data-ttu-id="86e31-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86e31-200">0x00000010</span></span>                                       |
| <span data-ttu-id="86e31-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="86e31-201">Classes used in</span></span>        | [<span data-ttu-id="86e31-202">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="86e31-202">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="86e31-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="86e31-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="86e31-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="86e31-204">Entry</span></span> | <span data-ttu-id="86e31-205">Value</span><span class="sxs-lookup"><span data-stu-id="86e31-205">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="86e31-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="86e31-206">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="86e31-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86e31-207">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="86e31-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="86e31-208">System-Only</span></span>            | <span data-ttu-id="86e31-209">True</span><span class="sxs-lookup"><span data-stu-id="86e31-209">True</span></span>                                             |
| <span data-ttu-id="86e31-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="86e31-210">Is-Single-Valued</span></span>       | <span data-ttu-id="86e31-211">False</span><span class="sxs-lookup"><span data-stu-id="86e31-211">False</span></span>                                            |
| <span data-ttu-id="86e31-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="86e31-212">Is Indexed</span></span>             | <span data-ttu-id="86e31-213">False</span><span class="sxs-lookup"><span data-stu-id="86e31-213">False</span></span>                                            |
| <span data-ttu-id="86e31-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="86e31-214">In Global Catalog</span></span>      | <span data-ttu-id="86e31-215">False</span><span class="sxs-lookup"><span data-stu-id="86e31-215">False</span></span>                                            |
| <span data-ttu-id="86e31-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="86e31-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="86e31-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="86e31-217">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="86e31-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86e31-218">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="86e31-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86e31-219">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="86e31-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86e31-220">Search-Flags</span></span>           | <span data-ttu-id="86e31-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86e31-221">0x00000000</span></span>                                       |
| <span data-ttu-id="86e31-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86e31-222">System-Flags</span></span>           | <span data-ttu-id="86e31-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86e31-223">0x00000010</span></span>                                       |
| <span data-ttu-id="86e31-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="86e31-224">Classes used in</span></span>        | [<span data-ttu-id="86e31-225">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="86e31-225">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="86e31-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86e31-226">Windows Server 2008</span></span>



| <span data-ttu-id="86e31-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="86e31-227">Entry</span></span> | <span data-ttu-id="86e31-228">Value</span><span class="sxs-lookup"><span data-stu-id="86e31-228">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="86e31-229">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="86e31-229">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="86e31-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86e31-230">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="86e31-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="86e31-231">System-Only</span></span>            | <span data-ttu-id="86e31-232">True</span><span class="sxs-lookup"><span data-stu-id="86e31-232">True</span></span>                                             |
| <span data-ttu-id="86e31-233">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="86e31-233">Is-Single-Valued</span></span>       | <span data-ttu-id="86e31-234">False</span><span class="sxs-lookup"><span data-stu-id="86e31-234">False</span></span>                                            |
| <span data-ttu-id="86e31-235">Está indexado</span><span class="sxs-lookup"><span data-stu-id="86e31-235">Is Indexed</span></span>             | <span data-ttu-id="86e31-236">False</span><span class="sxs-lookup"><span data-stu-id="86e31-236">False</span></span>                                            |
| <span data-ttu-id="86e31-237">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="86e31-237">In Global Catalog</span></span>      | <span data-ttu-id="86e31-238">False</span><span class="sxs-lookup"><span data-stu-id="86e31-238">False</span></span>                                            |
| <span data-ttu-id="86e31-239">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="86e31-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="86e31-240">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="86e31-240">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="86e31-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86e31-241">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="86e31-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86e31-242">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="86e31-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86e31-243">Search-Flags</span></span>           | <span data-ttu-id="86e31-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86e31-244">0x00000000</span></span>                                       |
| <span data-ttu-id="86e31-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86e31-245">System-Flags</span></span>           | <span data-ttu-id="86e31-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86e31-246">0x00000010</span></span>                                       |
| <span data-ttu-id="86e31-247">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="86e31-247">Classes used in</span></span>        | [<span data-ttu-id="86e31-248">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="86e31-248">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="86e31-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="86e31-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="86e31-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="86e31-250">Entry</span></span> | <span data-ttu-id="86e31-251">Value</span><span class="sxs-lookup"><span data-stu-id="86e31-251">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="86e31-252">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="86e31-252">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="86e31-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86e31-253">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="86e31-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="86e31-254">System-Only</span></span>            | <span data-ttu-id="86e31-255">True</span><span class="sxs-lookup"><span data-stu-id="86e31-255">True</span></span>                                             |
| <span data-ttu-id="86e31-256">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="86e31-256">Is-Single-Valued</span></span>       | <span data-ttu-id="86e31-257">False</span><span class="sxs-lookup"><span data-stu-id="86e31-257">False</span></span>                                            |
| <span data-ttu-id="86e31-258">Está indexado</span><span class="sxs-lookup"><span data-stu-id="86e31-258">Is Indexed</span></span>             | <span data-ttu-id="86e31-259">False</span><span class="sxs-lookup"><span data-stu-id="86e31-259">False</span></span>                                            |
| <span data-ttu-id="86e31-260">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="86e31-260">In Global Catalog</span></span>      | <span data-ttu-id="86e31-261">False</span><span class="sxs-lookup"><span data-stu-id="86e31-261">False</span></span>                                            |
| <span data-ttu-id="86e31-262">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="86e31-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="86e31-263">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="86e31-263">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="86e31-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86e31-264">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="86e31-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86e31-265">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="86e31-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86e31-266">Search-Flags</span></span>           | <span data-ttu-id="86e31-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86e31-267">0x00000000</span></span>                                       |
| <span data-ttu-id="86e31-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86e31-268">System-Flags</span></span>           | <span data-ttu-id="86e31-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86e31-269">0x00000010</span></span>                                       |
| <span data-ttu-id="86e31-270">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="86e31-270">Classes used in</span></span>        | [<span data-ttu-id="86e31-271">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="86e31-271">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="86e31-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="86e31-272">Windows Server 2012</span></span>



| <span data-ttu-id="86e31-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="86e31-273">Entry</span></span> | <span data-ttu-id="86e31-274">Value</span><span class="sxs-lookup"><span data-stu-id="86e31-274">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="86e31-275">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="86e31-275">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="86e31-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86e31-276">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="86e31-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="86e31-277">System-Only</span></span>            | <span data-ttu-id="86e31-278">True</span><span class="sxs-lookup"><span data-stu-id="86e31-278">True</span></span>                                             |
| <span data-ttu-id="86e31-279">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="86e31-279">Is-Single-Valued</span></span>       | <span data-ttu-id="86e31-280">False</span><span class="sxs-lookup"><span data-stu-id="86e31-280">False</span></span>                                            |
| <span data-ttu-id="86e31-281">Está indexado</span><span class="sxs-lookup"><span data-stu-id="86e31-281">Is Indexed</span></span>             | <span data-ttu-id="86e31-282">False</span><span class="sxs-lookup"><span data-stu-id="86e31-282">False</span></span>                                            |
| <span data-ttu-id="86e31-283">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="86e31-283">In Global Catalog</span></span>      | <span data-ttu-id="86e31-284">False</span><span class="sxs-lookup"><span data-stu-id="86e31-284">False</span></span>                                            |
| <span data-ttu-id="86e31-285">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="86e31-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="86e31-286">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="86e31-286">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="86e31-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86e31-287">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="86e31-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86e31-288">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="86e31-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86e31-289">Search-Flags</span></span>           | <span data-ttu-id="86e31-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86e31-290">0x00000000</span></span>                                       |
| <span data-ttu-id="86e31-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86e31-291">System-Flags</span></span>           | <span data-ttu-id="86e31-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86e31-292">0x00000010</span></span>                                       |
| <span data-ttu-id="86e31-293">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="86e31-293">Classes used in</span></span>        | [<span data-ttu-id="86e31-294">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="86e31-294">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





