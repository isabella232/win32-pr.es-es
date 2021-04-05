---
title: Atributo de miembro no de seguridad
description: Miembros que no son de seguridad de un grupo. Se usa para listas de distribución de Exchange.
ms.assetid: 0db135e4-dcba-4afb-a174-3c7b2b40688e
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo que no es de seguridad
- nonSecurityMember esquema de AD de atributos
topic_type:
- apiref
api_name:
- Non-Security-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a04919d9d538ff4da97d73e79d14e9a2706032b8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997525"
---
# <a name="non-security-member-attribute"></a><span data-ttu-id="f62df-106">Atributo de miembro no de seguridad</span><span class="sxs-lookup"><span data-stu-id="f62df-106">Non-Security-Member attribute</span></span>

<span data-ttu-id="f62df-107">Miembros que no son de seguridad de un grupo.</span><span class="sxs-lookup"><span data-stu-id="f62df-107">Nonsecurity members of a group.</span></span> <span data-ttu-id="f62df-108">Se usa para listas de distribución de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f62df-108">Used for Exchange distribution lists.</span></span>



| <span data-ttu-id="f62df-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="f62df-109">Entry</span></span> | <span data-ttu-id="f62df-110">Value</span><span class="sxs-lookup"><span data-stu-id="f62df-110">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="f62df-111">CN</span><span class="sxs-lookup"><span data-stu-id="f62df-111">CN</span></span>                | <span data-ttu-id="f62df-112">Miembro que no es de seguridad</span><span class="sxs-lookup"><span data-stu-id="f62df-112">Non-Security-Member</span></span>                              |
| <span data-ttu-id="f62df-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="f62df-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f62df-114">nonSecurityMember</span><span class="sxs-lookup"><span data-stu-id="f62df-114">nonSecurityMember</span></span>                                |
| <span data-ttu-id="f62df-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f62df-115">Size</span></span>              | \-                                               |
| <span data-ttu-id="f62df-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="f62df-116">Update Privilege</span></span>  | <span data-ttu-id="f62df-117">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="f62df-117">Domain administrator</span></span>                             |
| <span data-ttu-id="f62df-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="f62df-118">Update Frequency</span></span>  | <span data-ttu-id="f62df-119">Siempre que se agrega o se quita un usuario de la DL.</span><span class="sxs-lookup"><span data-stu-id="f62df-119">Whenever a user is added or removed from the DL.</span></span> |
| <span data-ttu-id="f62df-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f62df-120">Attribute-Id</span></span>      | <span data-ttu-id="f62df-121">1.2.840.113556.1.4.530</span><span class="sxs-lookup"><span data-stu-id="f62df-121">1.2.840.113556.1.4.530</span></span>                           |
| <span data-ttu-id="f62df-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f62df-122">System-Id-Guid</span></span>    | <span data-ttu-id="f62df-123">52458018-ca6a-11d0-AFFF-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="f62df-123">52458018-ca6a-11d0-afff-0000f80367c1</span></span>             |
| <span data-ttu-id="f62df-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f62df-124">Syntax</span></span>            | [<span data-ttu-id="f62df-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="f62df-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)          |



## <a name="implementations"></a><span data-ttu-id="f62df-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="f62df-126">Implementations</span></span>

-   [<span data-ttu-id="f62df-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f62df-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f62df-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f62df-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f62df-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f62df-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f62df-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f62df-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f62df-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f62df-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f62df-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f62df-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f62df-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f62df-133">Windows 2000 Server</span></span>



| <span data-ttu-id="f62df-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="f62df-134">Entry</span></span> | <span data-ttu-id="f62df-135">Value</span><span class="sxs-lookup"><span data-stu-id="f62df-135">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="f62df-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f62df-136">Link-Id</span></span>                | <span data-ttu-id="f62df-137">50</span><span class="sxs-lookup"><span data-stu-id="f62df-137">50</span></span>                                  |
| <span data-ttu-id="f62df-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f62df-138">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="f62df-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="f62df-139">System-Only</span></span>            | <span data-ttu-id="f62df-140">False</span><span class="sxs-lookup"><span data-stu-id="f62df-140">False</span></span>                               |
| <span data-ttu-id="f62df-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f62df-141">Is-Single-Valued</span></span>       | <span data-ttu-id="f62df-142">False</span><span class="sxs-lookup"><span data-stu-id="f62df-142">False</span></span>                               |
| <span data-ttu-id="f62df-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f62df-143">Is Indexed</span></span>             | <span data-ttu-id="f62df-144">False</span><span class="sxs-lookup"><span data-stu-id="f62df-144">False</span></span>                               |
| <span data-ttu-id="f62df-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f62df-145">In Global Catalog</span></span>      | <span data-ttu-id="f62df-146">False</span><span class="sxs-lookup"><span data-stu-id="f62df-146">False</span></span>                               |
| <span data-ttu-id="f62df-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f62df-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="f62df-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f62df-148">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="f62df-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f62df-149">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="f62df-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f62df-150">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="f62df-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f62df-151">Search-Flags</span></span>           | <span data-ttu-id="f62df-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f62df-152">0x00000000</span></span>                          |
| <span data-ttu-id="f62df-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f62df-153">System-Flags</span></span>           | <span data-ttu-id="f62df-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f62df-154">0x00000010</span></span>                          |
| <span data-ttu-id="f62df-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f62df-155">Classes used in</span></span>        | [<span data-ttu-id="f62df-156">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="f62df-156">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f62df-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f62df-157">Windows Server 2003</span></span>



| <span data-ttu-id="f62df-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="f62df-158">Entry</span></span> | <span data-ttu-id="f62df-159">Value</span><span class="sxs-lookup"><span data-stu-id="f62df-159">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="f62df-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f62df-160">Link-Id</span></span>                | <span data-ttu-id="f62df-161">50</span><span class="sxs-lookup"><span data-stu-id="f62df-161">50</span></span>                                  |
| <span data-ttu-id="f62df-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f62df-162">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="f62df-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="f62df-163">System-Only</span></span>            | <span data-ttu-id="f62df-164">False</span><span class="sxs-lookup"><span data-stu-id="f62df-164">False</span></span>                               |
| <span data-ttu-id="f62df-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f62df-165">Is-Single-Valued</span></span>       | <span data-ttu-id="f62df-166">False</span><span class="sxs-lookup"><span data-stu-id="f62df-166">False</span></span>                               |
| <span data-ttu-id="f62df-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f62df-167">Is Indexed</span></span>             | <span data-ttu-id="f62df-168">False</span><span class="sxs-lookup"><span data-stu-id="f62df-168">False</span></span>                               |
| <span data-ttu-id="f62df-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f62df-169">In Global Catalog</span></span>      | <span data-ttu-id="f62df-170">False</span><span class="sxs-lookup"><span data-stu-id="f62df-170">False</span></span>                               |
| <span data-ttu-id="f62df-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f62df-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="f62df-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f62df-172">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="f62df-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f62df-173">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="f62df-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f62df-174">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="f62df-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f62df-175">Search-Flags</span></span>           | <span data-ttu-id="f62df-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f62df-176">0x00000000</span></span>                          |
| <span data-ttu-id="f62df-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f62df-177">System-Flags</span></span>           | <span data-ttu-id="f62df-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f62df-178">0x00000010</span></span>                          |
| <span data-ttu-id="f62df-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f62df-179">Classes used in</span></span>        | [<span data-ttu-id="f62df-180">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="f62df-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f62df-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f62df-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f62df-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="f62df-182">Entry</span></span> | <span data-ttu-id="f62df-183">Value</span><span class="sxs-lookup"><span data-stu-id="f62df-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="f62df-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f62df-184">Link-Id</span></span>                | <span data-ttu-id="f62df-185">50</span><span class="sxs-lookup"><span data-stu-id="f62df-185">50</span></span>                                  |
| <span data-ttu-id="f62df-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f62df-186">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="f62df-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="f62df-187">System-Only</span></span>            | <span data-ttu-id="f62df-188">False</span><span class="sxs-lookup"><span data-stu-id="f62df-188">False</span></span>                               |
| <span data-ttu-id="f62df-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f62df-189">Is-Single-Valued</span></span>       | <span data-ttu-id="f62df-190">False</span><span class="sxs-lookup"><span data-stu-id="f62df-190">False</span></span>                               |
| <span data-ttu-id="f62df-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f62df-191">Is Indexed</span></span>             | <span data-ttu-id="f62df-192">False</span><span class="sxs-lookup"><span data-stu-id="f62df-192">False</span></span>                               |
| <span data-ttu-id="f62df-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f62df-193">In Global Catalog</span></span>      | <span data-ttu-id="f62df-194">False</span><span class="sxs-lookup"><span data-stu-id="f62df-194">False</span></span>                               |
| <span data-ttu-id="f62df-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f62df-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="f62df-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f62df-196">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="f62df-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f62df-197">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="f62df-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f62df-198">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="f62df-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f62df-199">Search-Flags</span></span>           | <span data-ttu-id="f62df-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f62df-200">0x00000000</span></span>                          |
| <span data-ttu-id="f62df-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f62df-201">System-Flags</span></span>           | <span data-ttu-id="f62df-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f62df-202">0x00000010</span></span>                          |
| <span data-ttu-id="f62df-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f62df-203">Classes used in</span></span>        | [<span data-ttu-id="f62df-204">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="f62df-204">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f62df-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f62df-205">Windows Server 2008</span></span>



| <span data-ttu-id="f62df-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="f62df-206">Entry</span></span> | <span data-ttu-id="f62df-207">Value</span><span class="sxs-lookup"><span data-stu-id="f62df-207">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="f62df-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f62df-208">Link-Id</span></span>                | <span data-ttu-id="f62df-209">50</span><span class="sxs-lookup"><span data-stu-id="f62df-209">50</span></span>                                  |
| <span data-ttu-id="f62df-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f62df-210">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="f62df-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="f62df-211">System-Only</span></span>            | <span data-ttu-id="f62df-212">False</span><span class="sxs-lookup"><span data-stu-id="f62df-212">False</span></span>                               |
| <span data-ttu-id="f62df-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f62df-213">Is-Single-Valued</span></span>       | <span data-ttu-id="f62df-214">False</span><span class="sxs-lookup"><span data-stu-id="f62df-214">False</span></span>                               |
| <span data-ttu-id="f62df-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f62df-215">Is Indexed</span></span>             | <span data-ttu-id="f62df-216">False</span><span class="sxs-lookup"><span data-stu-id="f62df-216">False</span></span>                               |
| <span data-ttu-id="f62df-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f62df-217">In Global Catalog</span></span>      | <span data-ttu-id="f62df-218">False</span><span class="sxs-lookup"><span data-stu-id="f62df-218">False</span></span>                               |
| <span data-ttu-id="f62df-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f62df-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="f62df-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f62df-220">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="f62df-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f62df-221">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="f62df-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f62df-222">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="f62df-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f62df-223">Search-Flags</span></span>           | <span data-ttu-id="f62df-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f62df-224">0x00000000</span></span>                          |
| <span data-ttu-id="f62df-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f62df-225">System-Flags</span></span>           | <span data-ttu-id="f62df-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f62df-226">0x00000010</span></span>                          |
| <span data-ttu-id="f62df-227">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f62df-227">Classes used in</span></span>        | [<span data-ttu-id="f62df-228">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="f62df-228">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f62df-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f62df-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f62df-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="f62df-230">Entry</span></span> | <span data-ttu-id="f62df-231">Value</span><span class="sxs-lookup"><span data-stu-id="f62df-231">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="f62df-232">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f62df-232">Link-Id</span></span>                | <span data-ttu-id="f62df-233">50</span><span class="sxs-lookup"><span data-stu-id="f62df-233">50</span></span>                                  |
| <span data-ttu-id="f62df-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f62df-234">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="f62df-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="f62df-235">System-Only</span></span>            | <span data-ttu-id="f62df-236">False</span><span class="sxs-lookup"><span data-stu-id="f62df-236">False</span></span>                               |
| <span data-ttu-id="f62df-237">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f62df-237">Is-Single-Valued</span></span>       | <span data-ttu-id="f62df-238">False</span><span class="sxs-lookup"><span data-stu-id="f62df-238">False</span></span>                               |
| <span data-ttu-id="f62df-239">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f62df-239">Is Indexed</span></span>             | <span data-ttu-id="f62df-240">False</span><span class="sxs-lookup"><span data-stu-id="f62df-240">False</span></span>                               |
| <span data-ttu-id="f62df-241">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f62df-241">In Global Catalog</span></span>      | <span data-ttu-id="f62df-242">False</span><span class="sxs-lookup"><span data-stu-id="f62df-242">False</span></span>                               |
| <span data-ttu-id="f62df-243">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f62df-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="f62df-244">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f62df-244">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="f62df-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f62df-245">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="f62df-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f62df-246">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="f62df-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f62df-247">Search-Flags</span></span>           | <span data-ttu-id="f62df-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f62df-248">0x00000000</span></span>                          |
| <span data-ttu-id="f62df-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f62df-249">System-Flags</span></span>           | <span data-ttu-id="f62df-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f62df-250">0x00000010</span></span>                          |
| <span data-ttu-id="f62df-251">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f62df-251">Classes used in</span></span>        | [<span data-ttu-id="f62df-252">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="f62df-252">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f62df-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f62df-253">Windows Server 2012</span></span>



| <span data-ttu-id="f62df-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="f62df-254">Entry</span></span> | <span data-ttu-id="f62df-255">Value</span><span class="sxs-lookup"><span data-stu-id="f62df-255">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="f62df-256">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f62df-256">Link-Id</span></span>                | <span data-ttu-id="f62df-257">50</span><span class="sxs-lookup"><span data-stu-id="f62df-257">50</span></span>                                  |
| <span data-ttu-id="f62df-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f62df-258">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="f62df-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="f62df-259">System-Only</span></span>            | <span data-ttu-id="f62df-260">False</span><span class="sxs-lookup"><span data-stu-id="f62df-260">False</span></span>                               |
| <span data-ttu-id="f62df-261">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f62df-261">Is-Single-Valued</span></span>       | <span data-ttu-id="f62df-262">False</span><span class="sxs-lookup"><span data-stu-id="f62df-262">False</span></span>                               |
| <span data-ttu-id="f62df-263">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f62df-263">Is Indexed</span></span>             | <span data-ttu-id="f62df-264">False</span><span class="sxs-lookup"><span data-stu-id="f62df-264">False</span></span>                               |
| <span data-ttu-id="f62df-265">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f62df-265">In Global Catalog</span></span>      | <span data-ttu-id="f62df-266">False</span><span class="sxs-lookup"><span data-stu-id="f62df-266">False</span></span>                               |
| <span data-ttu-id="f62df-267">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f62df-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="f62df-268">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f62df-268">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="f62df-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f62df-269">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="f62df-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f62df-270">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="f62df-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f62df-271">Search-Flags</span></span>           | <span data-ttu-id="f62df-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f62df-272">0x00000000</span></span>                          |
| <span data-ttu-id="f62df-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f62df-273">System-Flags</span></span>           | <span data-ttu-id="f62df-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f62df-274">0x00000010</span></span>                          |
| <span data-ttu-id="f62df-275">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f62df-275">Classes used in</span></span>        | [<span data-ttu-id="f62df-276">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="f62df-276">**Group**</span></span>](c-group.md)<br/> |



 

 





