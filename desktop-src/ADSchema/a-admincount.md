---
title: Admin-Count atributo)
description: Indica que el sistema ha cambiado las ACL de un objeto dado a un valor más seguro porque era miembro de uno de los grupos administrativos (directa o transitiva).
ms.assetid: b2384ada-a792-42fa-be64-291d23e00887
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Admin-Count
- adminCount esquema de AD de atributos
topic_type:
- apiref
api_name:
- Admin-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95b953aebaa39bb3fc3e4c9cf96632f32a37850
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103805131"
---
# <a name="admin-count-attribute"></a><span data-ttu-id="1cd76-105">Admin-Count atributo)</span><span class="sxs-lookup"><span data-stu-id="1cd76-105">Admin-Count attribute</span></span>

<span data-ttu-id="1cd76-106">Indica que el sistema ha cambiado las ACL de un objeto dado a un valor más seguro porque era miembro de uno de los grupos administrativos (directa o transitiva).</span><span class="sxs-lookup"><span data-stu-id="1cd76-106">Indicates that a given object has had its ACLs changed to a more secure value by the system because it was a member of one of the administrative groups (directly or transitively).</span></span>



| <span data-ttu-id="1cd76-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="1cd76-107">Entry</span></span> | <span data-ttu-id="1cd76-108">Value</span><span class="sxs-lookup"><span data-stu-id="1cd76-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="1cd76-109">CN</span><span class="sxs-lookup"><span data-stu-id="1cd76-109">CN</span></span>                | <span data-ttu-id="1cd76-110">Admin-Count</span><span class="sxs-lookup"><span data-stu-id="1cd76-110">Admin-Count</span></span>                                         |
| <span data-ttu-id="1cd76-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="1cd76-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1cd76-112">adminCount</span><span class="sxs-lookup"><span data-stu-id="1cd76-112">adminCount</span></span>                                          |
| <span data-ttu-id="1cd76-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="1cd76-113">Size</span></span>              | <span data-ttu-id="1cd76-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="1cd76-114">4 bytes</span></span>                                             |
| <span data-ttu-id="1cd76-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="1cd76-115">Update Privilege</span></span>  | <span data-ttu-id="1cd76-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="1cd76-116">This value is set by the system.</span></span>                    |
| <span data-ttu-id="1cd76-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="1cd76-117">Update Frequency</span></span>  | <span data-ttu-id="1cd76-118">Cuando se agrega un objeto a un grupo administrativo.</span><span class="sxs-lookup"><span data-stu-id="1cd76-118">When an object is added to an administrative group.</span></span> |
| <span data-ttu-id="1cd76-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1cd76-119">Attribute-Id</span></span>      | <span data-ttu-id="1cd76-120">1.2.840.113556.1.4.150</span><span class="sxs-lookup"><span data-stu-id="1cd76-120">1.2.840.113556.1.4.150</span></span>                              |
| <span data-ttu-id="1cd76-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1cd76-121">System-Id-Guid</span></span>    | <span data-ttu-id="1cd76-122">bf967918-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1cd76-122">bf967918-0de6-11d0-a285-00aa003049e2</span></span>                |
| <span data-ttu-id="1cd76-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cd76-123">Syntax</span></span>            | [<span data-ttu-id="1cd76-124">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="1cd76-124">**Enumeration**</span></span>](s-enumeration.md)                |



## <a name="implementations"></a><span data-ttu-id="1cd76-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="1cd76-125">Implementations</span></span>

-   [<span data-ttu-id="1cd76-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1cd76-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1cd76-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1cd76-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1cd76-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1cd76-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1cd76-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1cd76-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1cd76-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1cd76-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1cd76-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1cd76-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1cd76-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1cd76-132">Windows 2000 Server</span></span>



| <span data-ttu-id="1cd76-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="1cd76-133">Entry</span></span> | <span data-ttu-id="1cd76-134">Value</span><span class="sxs-lookup"><span data-stu-id="1cd76-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="1cd76-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1cd76-135">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="1cd76-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cd76-136">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="1cd76-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cd76-137">System-Only</span></span>            | <span data-ttu-id="1cd76-138">False</span><span class="sxs-lookup"><span data-stu-id="1cd76-138">False</span></span>                                                                 |
| <span data-ttu-id="1cd76-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1cd76-139">Is-Single-Valued</span></span>       | <span data-ttu-id="1cd76-140">True</span><span class="sxs-lookup"><span data-stu-id="1cd76-140">True</span></span>                                                                  |
| <span data-ttu-id="1cd76-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1cd76-141">Is Indexed</span></span>             | <span data-ttu-id="1cd76-142">False</span><span class="sxs-lookup"><span data-stu-id="1cd76-142">False</span></span>                                                                 |
| <span data-ttu-id="1cd76-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1cd76-143">In Global Catalog</span></span>      | <span data-ttu-id="1cd76-144">False</span><span class="sxs-lookup"><span data-stu-id="1cd76-144">False</span></span>                                                                 |
| <span data-ttu-id="1cd76-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1cd76-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cd76-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1cd76-146">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="1cd76-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cd76-147">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="1cd76-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cd76-148">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="1cd76-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd76-149">Search-Flags</span></span>           | <span data-ttu-id="1cd76-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cd76-150">0x00000000</span></span>                                                            |
| <span data-ttu-id="1cd76-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd76-151">System-Flags</span></span>           | <span data-ttu-id="1cd76-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cd76-152">0x00000010</span></span>                                                            |
| <span data-ttu-id="1cd76-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1cd76-153">Classes used in</span></span>        | [<span data-ttu-id="1cd76-154">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="1cd76-154">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="1cd76-155">**User**</span><span class="sxs-lookup"><span data-stu-id="1cd76-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1cd76-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1cd76-156">Windows Server 2003</span></span>



| <span data-ttu-id="1cd76-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="1cd76-157">Entry</span></span> | <span data-ttu-id="1cd76-158">Value</span><span class="sxs-lookup"><span data-stu-id="1cd76-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="1cd76-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1cd76-159">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="1cd76-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cd76-160">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="1cd76-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cd76-161">System-Only</span></span>            | <span data-ttu-id="1cd76-162">False</span><span class="sxs-lookup"><span data-stu-id="1cd76-162">False</span></span>                                                                 |
| <span data-ttu-id="1cd76-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1cd76-163">Is-Single-Valued</span></span>       | <span data-ttu-id="1cd76-164">True</span><span class="sxs-lookup"><span data-stu-id="1cd76-164">True</span></span>                                                                  |
| <span data-ttu-id="1cd76-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1cd76-165">Is Indexed</span></span>             | <span data-ttu-id="1cd76-166">False</span><span class="sxs-lookup"><span data-stu-id="1cd76-166">False</span></span>                                                                 |
| <span data-ttu-id="1cd76-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1cd76-167">In Global Catalog</span></span>      | <span data-ttu-id="1cd76-168">False</span><span class="sxs-lookup"><span data-stu-id="1cd76-168">False</span></span>                                                                 |
| <span data-ttu-id="1cd76-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1cd76-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cd76-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1cd76-170">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="1cd76-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cd76-171">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="1cd76-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cd76-172">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="1cd76-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd76-173">Search-Flags</span></span>           | <span data-ttu-id="1cd76-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cd76-174">0x00000000</span></span>                                                            |
| <span data-ttu-id="1cd76-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd76-175">System-Flags</span></span>           | <span data-ttu-id="1cd76-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cd76-176">0x00000010</span></span>                                                            |
| <span data-ttu-id="1cd76-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1cd76-177">Classes used in</span></span>        | [<span data-ttu-id="1cd76-178">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="1cd76-178">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="1cd76-179">**User**</span><span class="sxs-lookup"><span data-stu-id="1cd76-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1cd76-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1cd76-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1cd76-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="1cd76-181">Entry</span></span> | <span data-ttu-id="1cd76-182">Value</span><span class="sxs-lookup"><span data-stu-id="1cd76-182">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="1cd76-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1cd76-183">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="1cd76-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cd76-184">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="1cd76-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cd76-185">System-Only</span></span>            | <span data-ttu-id="1cd76-186">False</span><span class="sxs-lookup"><span data-stu-id="1cd76-186">False</span></span>                                                                 |
| <span data-ttu-id="1cd76-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1cd76-187">Is-Single-Valued</span></span>       | <span data-ttu-id="1cd76-188">True</span><span class="sxs-lookup"><span data-stu-id="1cd76-188">True</span></span>                                                                  |
| <span data-ttu-id="1cd76-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1cd76-189">Is Indexed</span></span>             | <span data-ttu-id="1cd76-190">False</span><span class="sxs-lookup"><span data-stu-id="1cd76-190">False</span></span>                                                                 |
| <span data-ttu-id="1cd76-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1cd76-191">In Global Catalog</span></span>      | <span data-ttu-id="1cd76-192">False</span><span class="sxs-lookup"><span data-stu-id="1cd76-192">False</span></span>                                                                 |
| <span data-ttu-id="1cd76-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1cd76-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cd76-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1cd76-194">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="1cd76-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cd76-195">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="1cd76-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cd76-196">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="1cd76-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd76-197">Search-Flags</span></span>           | <span data-ttu-id="1cd76-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cd76-198">0x00000000</span></span>                                                            |
| <span data-ttu-id="1cd76-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd76-199">System-Flags</span></span>           | <span data-ttu-id="1cd76-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cd76-200">0x00000010</span></span>                                                            |
| <span data-ttu-id="1cd76-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1cd76-201">Classes used in</span></span>        | [<span data-ttu-id="1cd76-202">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="1cd76-202">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="1cd76-203">**User**</span><span class="sxs-lookup"><span data-stu-id="1cd76-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1cd76-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1cd76-204">Windows Server 2008</span></span>



| <span data-ttu-id="1cd76-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="1cd76-205">Entry</span></span> | <span data-ttu-id="1cd76-206">Value</span><span class="sxs-lookup"><span data-stu-id="1cd76-206">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="1cd76-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1cd76-207">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="1cd76-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cd76-208">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="1cd76-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cd76-209">System-Only</span></span>            | <span data-ttu-id="1cd76-210">False</span><span class="sxs-lookup"><span data-stu-id="1cd76-210">False</span></span>                                                                 |
| <span data-ttu-id="1cd76-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1cd76-211">Is-Single-Valued</span></span>       | <span data-ttu-id="1cd76-212">True</span><span class="sxs-lookup"><span data-stu-id="1cd76-212">True</span></span>                                                                  |
| <span data-ttu-id="1cd76-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1cd76-213">Is Indexed</span></span>             | <span data-ttu-id="1cd76-214">False</span><span class="sxs-lookup"><span data-stu-id="1cd76-214">False</span></span>                                                                 |
| <span data-ttu-id="1cd76-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1cd76-215">In Global Catalog</span></span>      | <span data-ttu-id="1cd76-216">False</span><span class="sxs-lookup"><span data-stu-id="1cd76-216">False</span></span>                                                                 |
| <span data-ttu-id="1cd76-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1cd76-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cd76-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1cd76-218">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="1cd76-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cd76-219">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="1cd76-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cd76-220">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="1cd76-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd76-221">Search-Flags</span></span>           | <span data-ttu-id="1cd76-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cd76-222">0x00000000</span></span>                                                            |
| <span data-ttu-id="1cd76-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd76-223">System-Flags</span></span>           | <span data-ttu-id="1cd76-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cd76-224">0x00000010</span></span>                                                            |
| <span data-ttu-id="1cd76-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1cd76-225">Classes used in</span></span>        | [<span data-ttu-id="1cd76-226">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="1cd76-226">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="1cd76-227">**User**</span><span class="sxs-lookup"><span data-stu-id="1cd76-227">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1cd76-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1cd76-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1cd76-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="1cd76-229">Entry</span></span> | <span data-ttu-id="1cd76-230">Value</span><span class="sxs-lookup"><span data-stu-id="1cd76-230">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="1cd76-231">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1cd76-231">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="1cd76-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cd76-232">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="1cd76-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cd76-233">System-Only</span></span>            | <span data-ttu-id="1cd76-234">False</span><span class="sxs-lookup"><span data-stu-id="1cd76-234">False</span></span>                                                                 |
| <span data-ttu-id="1cd76-235">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1cd76-235">Is-Single-Valued</span></span>       | <span data-ttu-id="1cd76-236">True</span><span class="sxs-lookup"><span data-stu-id="1cd76-236">True</span></span>                                                                  |
| <span data-ttu-id="1cd76-237">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1cd76-237">Is Indexed</span></span>             | <span data-ttu-id="1cd76-238">False</span><span class="sxs-lookup"><span data-stu-id="1cd76-238">False</span></span>                                                                 |
| <span data-ttu-id="1cd76-239">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1cd76-239">In Global Catalog</span></span>      | <span data-ttu-id="1cd76-240">False</span><span class="sxs-lookup"><span data-stu-id="1cd76-240">False</span></span>                                                                 |
| <span data-ttu-id="1cd76-241">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1cd76-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cd76-242">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1cd76-242">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="1cd76-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cd76-243">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="1cd76-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cd76-244">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="1cd76-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd76-245">Search-Flags</span></span>           | <span data-ttu-id="1cd76-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cd76-246">0x00000000</span></span>                                                            |
| <span data-ttu-id="1cd76-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd76-247">System-Flags</span></span>           | <span data-ttu-id="1cd76-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cd76-248">0x00000010</span></span>                                                            |
| <span data-ttu-id="1cd76-249">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1cd76-249">Classes used in</span></span>        | [<span data-ttu-id="1cd76-250">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="1cd76-250">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="1cd76-251">**User**</span><span class="sxs-lookup"><span data-stu-id="1cd76-251">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1cd76-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1cd76-252">Windows Server 2012</span></span>



| <span data-ttu-id="1cd76-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="1cd76-253">Entry</span></span> | <span data-ttu-id="1cd76-254">Value</span><span class="sxs-lookup"><span data-stu-id="1cd76-254">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="1cd76-255">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1cd76-255">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="1cd76-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cd76-256">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="1cd76-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cd76-257">System-Only</span></span>            | <span data-ttu-id="1cd76-258">False</span><span class="sxs-lookup"><span data-stu-id="1cd76-258">False</span></span>                                                                 |
| <span data-ttu-id="1cd76-259">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1cd76-259">Is-Single-Valued</span></span>       | <span data-ttu-id="1cd76-260">True</span><span class="sxs-lookup"><span data-stu-id="1cd76-260">True</span></span>                                                                  |
| <span data-ttu-id="1cd76-261">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1cd76-261">Is Indexed</span></span>             | <span data-ttu-id="1cd76-262">False</span><span class="sxs-lookup"><span data-stu-id="1cd76-262">False</span></span>                                                                 |
| <span data-ttu-id="1cd76-263">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1cd76-263">In Global Catalog</span></span>      | <span data-ttu-id="1cd76-264">False</span><span class="sxs-lookup"><span data-stu-id="1cd76-264">False</span></span>                                                                 |
| <span data-ttu-id="1cd76-265">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1cd76-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cd76-266">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1cd76-266">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="1cd76-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cd76-267">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="1cd76-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cd76-268">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="1cd76-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd76-269">Search-Flags</span></span>           | <span data-ttu-id="1cd76-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cd76-270">0x00000000</span></span>                                                            |
| <span data-ttu-id="1cd76-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd76-271">System-Flags</span></span>           | <span data-ttu-id="1cd76-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cd76-272">0x00000010</span></span>                                                            |
| <span data-ttu-id="1cd76-273">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1cd76-273">Classes used in</span></span>        | [<span data-ttu-id="1cd76-274">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="1cd76-274">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="1cd76-275">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="1cd76-275">**User**</span></span>](c-user.md)<br/> |



 

 





