---
title: Atributo Primary-Group-ID
description: Contiene el identificador relativo (RID) para el grupo principal del usuario. De forma predeterminada, este es el RID del grupo usuarios del dominio.
ms.assetid: 80803734-f7dd-4348-a110-ca6b8bccb60b
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de ID. de grupo principal
- primaryGroupID esquema de AD de atributos
topic_type:
- apiref
api_name:
- Primary-Group-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2b6237ff6e49a01da3b960b58103ae10dca7b2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804868"
---
# <a name="primary-group-id-attribute"></a><span data-ttu-id="115c4-106">Atributo Primary-Group-ID</span><span class="sxs-lookup"><span data-stu-id="115c4-106">Primary-Group-ID attribute</span></span>

<span data-ttu-id="115c4-107">Contiene el identificador relativo (RID) para el grupo principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="115c4-107">Contains the relative identifier (RID) for the primary group of the user.</span></span> <span data-ttu-id="115c4-108">De forma predeterminada, este es el RID del grupo usuarios del dominio.</span><span class="sxs-lookup"><span data-stu-id="115c4-108">By default, this is the RID for the Domain Users group.</span></span>



| <span data-ttu-id="115c4-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="115c4-109">Entry</span></span> | <span data-ttu-id="115c4-110">Value</span><span class="sxs-lookup"><span data-stu-id="115c4-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="115c4-111">CN</span><span class="sxs-lookup"><span data-stu-id="115c4-111">CN</span></span>                | <span data-ttu-id="115c4-112">IDENTIFICADOR de grupo principal</span><span class="sxs-lookup"><span data-stu-id="115c4-112">Primary-Group-ID</span></span>                     |
| <span data-ttu-id="115c4-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="115c4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="115c4-114">primaryGroupID</span><span class="sxs-lookup"><span data-stu-id="115c4-114">primaryGroupID</span></span>                       |
| <span data-ttu-id="115c4-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="115c4-115">Size</span></span>              | <span data-ttu-id="115c4-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="115c4-116">4 bytes</span></span>                              |
| <span data-ttu-id="115c4-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="115c4-117">Update Privilege</span></span>  | <span data-ttu-id="115c4-118">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="115c4-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="115c4-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="115c4-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="115c4-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="115c4-120">Attribute-Id</span></span>      | <span data-ttu-id="115c4-121">1.2.840.113556.1.4.98</span><span class="sxs-lookup"><span data-stu-id="115c4-121">1.2.840.113556.1.4.98</span></span>                |
| <span data-ttu-id="115c4-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="115c4-122">System-Id-Guid</span></span>    | <span data-ttu-id="115c4-123">bf967a00-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="115c4-123">bf967a00-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="115c4-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="115c4-124">Syntax</span></span>            | [<span data-ttu-id="115c4-125">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="115c4-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="115c4-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="115c4-126">Implementations</span></span>

-   [<span data-ttu-id="115c4-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="115c4-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="115c4-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="115c4-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="115c4-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="115c4-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="115c4-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="115c4-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="115c4-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="115c4-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="115c4-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="115c4-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="115c4-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="115c4-133">Windows 2000 Server</span></span>



| <span data-ttu-id="115c4-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="115c4-134">Entry</span></span> | <span data-ttu-id="115c4-135">Value</span><span class="sxs-lookup"><span data-stu-id="115c4-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="115c4-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="115c4-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="115c4-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="115c4-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="115c4-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="115c4-138">System-Only</span></span>            | <span data-ttu-id="115c4-139">False</span><span class="sxs-lookup"><span data-stu-id="115c4-139">False</span></span>                             |
| <span data-ttu-id="115c4-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="115c4-140">Is-Single-Valued</span></span>       | <span data-ttu-id="115c4-141">True</span><span class="sxs-lookup"><span data-stu-id="115c4-141">True</span></span>                              |
| <span data-ttu-id="115c4-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="115c4-142">Is Indexed</span></span>             | <span data-ttu-id="115c4-143">True</span><span class="sxs-lookup"><span data-stu-id="115c4-143">True</span></span>                              |
| <span data-ttu-id="115c4-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="115c4-144">In Global Catalog</span></span>      | <span data-ttu-id="115c4-145">True</span><span class="sxs-lookup"><span data-stu-id="115c4-145">True</span></span>                              |
| <span data-ttu-id="115c4-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="115c4-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="115c4-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="115c4-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="115c4-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="115c4-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="115c4-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="115c4-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="115c4-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="115c4-150">Search-Flags</span></span>           | <span data-ttu-id="115c4-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="115c4-151">0x00000011</span></span>                        |
| <span data-ttu-id="115c4-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="115c4-152">System-Flags</span></span>           | <span data-ttu-id="115c4-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="115c4-153">0x00000012</span></span>                        |
| <span data-ttu-id="115c4-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="115c4-154">Classes used in</span></span>        | [<span data-ttu-id="115c4-155">**User**</span><span class="sxs-lookup"><span data-stu-id="115c4-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="115c4-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="115c4-156">Windows Server 2003</span></span>



| <span data-ttu-id="115c4-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="115c4-157">Entry</span></span> | <span data-ttu-id="115c4-158">Value</span><span class="sxs-lookup"><span data-stu-id="115c4-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="115c4-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="115c4-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="115c4-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="115c4-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="115c4-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="115c4-161">System-Only</span></span>            | <span data-ttu-id="115c4-162">False</span><span class="sxs-lookup"><span data-stu-id="115c4-162">False</span></span>                             |
| <span data-ttu-id="115c4-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="115c4-163">Is-Single-Valued</span></span>       | <span data-ttu-id="115c4-164">True</span><span class="sxs-lookup"><span data-stu-id="115c4-164">True</span></span>                              |
| <span data-ttu-id="115c4-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="115c4-165">Is Indexed</span></span>             | <span data-ttu-id="115c4-166">True</span><span class="sxs-lookup"><span data-stu-id="115c4-166">True</span></span>                              |
| <span data-ttu-id="115c4-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="115c4-167">In Global Catalog</span></span>      | <span data-ttu-id="115c4-168">True</span><span class="sxs-lookup"><span data-stu-id="115c4-168">True</span></span>                              |
| <span data-ttu-id="115c4-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="115c4-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="115c4-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="115c4-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="115c4-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="115c4-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="115c4-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="115c4-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="115c4-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="115c4-173">Search-Flags</span></span>           | <span data-ttu-id="115c4-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="115c4-174">0x00000011</span></span>                        |
| <span data-ttu-id="115c4-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="115c4-175">System-Flags</span></span>           | <span data-ttu-id="115c4-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="115c4-176">0x00000012</span></span>                        |
| <span data-ttu-id="115c4-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="115c4-177">Classes used in</span></span>        | [<span data-ttu-id="115c4-178">**User**</span><span class="sxs-lookup"><span data-stu-id="115c4-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="115c4-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="115c4-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="115c4-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="115c4-180">Entry</span></span> | <span data-ttu-id="115c4-181">Value</span><span class="sxs-lookup"><span data-stu-id="115c4-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="115c4-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="115c4-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="115c4-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="115c4-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="115c4-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="115c4-184">System-Only</span></span>            | <span data-ttu-id="115c4-185">False</span><span class="sxs-lookup"><span data-stu-id="115c4-185">False</span></span>                             |
| <span data-ttu-id="115c4-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="115c4-186">Is-Single-Valued</span></span>       | <span data-ttu-id="115c4-187">True</span><span class="sxs-lookup"><span data-stu-id="115c4-187">True</span></span>                              |
| <span data-ttu-id="115c4-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="115c4-188">Is Indexed</span></span>             | <span data-ttu-id="115c4-189">True</span><span class="sxs-lookup"><span data-stu-id="115c4-189">True</span></span>                              |
| <span data-ttu-id="115c4-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="115c4-190">In Global Catalog</span></span>      | <span data-ttu-id="115c4-191">True</span><span class="sxs-lookup"><span data-stu-id="115c4-191">True</span></span>                              |
| <span data-ttu-id="115c4-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="115c4-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="115c4-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="115c4-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="115c4-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="115c4-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="115c4-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="115c4-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="115c4-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="115c4-196">Search-Flags</span></span>           | <span data-ttu-id="115c4-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="115c4-197">0x00000011</span></span>                        |
| <span data-ttu-id="115c4-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="115c4-198">System-Flags</span></span>           | <span data-ttu-id="115c4-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="115c4-199">0x00000012</span></span>                        |
| <span data-ttu-id="115c4-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="115c4-200">Classes used in</span></span>        | [<span data-ttu-id="115c4-201">**User**</span><span class="sxs-lookup"><span data-stu-id="115c4-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="115c4-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="115c4-202">Windows Server 2008</span></span>



| <span data-ttu-id="115c4-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="115c4-203">Entry</span></span> | <span data-ttu-id="115c4-204">Value</span><span class="sxs-lookup"><span data-stu-id="115c4-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="115c4-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="115c4-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="115c4-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="115c4-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="115c4-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="115c4-207">System-Only</span></span>            | <span data-ttu-id="115c4-208">False</span><span class="sxs-lookup"><span data-stu-id="115c4-208">False</span></span>                             |
| <span data-ttu-id="115c4-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="115c4-209">Is-Single-Valued</span></span>       | <span data-ttu-id="115c4-210">True</span><span class="sxs-lookup"><span data-stu-id="115c4-210">True</span></span>                              |
| <span data-ttu-id="115c4-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="115c4-211">Is Indexed</span></span>             | <span data-ttu-id="115c4-212">True</span><span class="sxs-lookup"><span data-stu-id="115c4-212">True</span></span>                              |
| <span data-ttu-id="115c4-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="115c4-213">In Global Catalog</span></span>      | <span data-ttu-id="115c4-214">True</span><span class="sxs-lookup"><span data-stu-id="115c4-214">True</span></span>                              |
| <span data-ttu-id="115c4-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="115c4-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="115c4-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="115c4-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="115c4-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="115c4-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="115c4-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="115c4-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="115c4-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="115c4-219">Search-Flags</span></span>           | <span data-ttu-id="115c4-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="115c4-220">0x00000011</span></span>                        |
| <span data-ttu-id="115c4-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="115c4-221">System-Flags</span></span>           | <span data-ttu-id="115c4-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="115c4-222">0x00000012</span></span>                        |
| <span data-ttu-id="115c4-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="115c4-223">Classes used in</span></span>        | [<span data-ttu-id="115c4-224">**User**</span><span class="sxs-lookup"><span data-stu-id="115c4-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="115c4-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="115c4-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="115c4-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="115c4-226">Entry</span></span> | <span data-ttu-id="115c4-227">Value</span><span class="sxs-lookup"><span data-stu-id="115c4-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="115c4-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="115c4-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="115c4-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="115c4-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="115c4-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="115c4-230">System-Only</span></span>            | <span data-ttu-id="115c4-231">False</span><span class="sxs-lookup"><span data-stu-id="115c4-231">False</span></span>                             |
| <span data-ttu-id="115c4-232">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="115c4-232">Is-Single-Valued</span></span>       | <span data-ttu-id="115c4-233">True</span><span class="sxs-lookup"><span data-stu-id="115c4-233">True</span></span>                              |
| <span data-ttu-id="115c4-234">Está indexado</span><span class="sxs-lookup"><span data-stu-id="115c4-234">Is Indexed</span></span>             | <span data-ttu-id="115c4-235">True</span><span class="sxs-lookup"><span data-stu-id="115c4-235">True</span></span>                              |
| <span data-ttu-id="115c4-236">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="115c4-236">In Global Catalog</span></span>      | <span data-ttu-id="115c4-237">True</span><span class="sxs-lookup"><span data-stu-id="115c4-237">True</span></span>                              |
| <span data-ttu-id="115c4-238">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="115c4-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="115c4-239">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="115c4-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="115c4-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="115c4-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="115c4-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="115c4-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="115c4-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="115c4-242">Search-Flags</span></span>           | <span data-ttu-id="115c4-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="115c4-243">0x00000011</span></span>                        |
| <span data-ttu-id="115c4-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="115c4-244">System-Flags</span></span>           | <span data-ttu-id="115c4-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="115c4-245">0x00000012</span></span>                        |
| <span data-ttu-id="115c4-246">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="115c4-246">Classes used in</span></span>        | [<span data-ttu-id="115c4-247">**User**</span><span class="sxs-lookup"><span data-stu-id="115c4-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="115c4-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="115c4-248">Windows Server 2012</span></span>



| <span data-ttu-id="115c4-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="115c4-249">Entry</span></span> | <span data-ttu-id="115c4-250">Value</span><span class="sxs-lookup"><span data-stu-id="115c4-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="115c4-251">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="115c4-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="115c4-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="115c4-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="115c4-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="115c4-253">System-Only</span></span>            | <span data-ttu-id="115c4-254">False</span><span class="sxs-lookup"><span data-stu-id="115c4-254">False</span></span>                             |
| <span data-ttu-id="115c4-255">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="115c4-255">Is-Single-Valued</span></span>       | <span data-ttu-id="115c4-256">True</span><span class="sxs-lookup"><span data-stu-id="115c4-256">True</span></span>                              |
| <span data-ttu-id="115c4-257">Está indexado</span><span class="sxs-lookup"><span data-stu-id="115c4-257">Is Indexed</span></span>             | <span data-ttu-id="115c4-258">True</span><span class="sxs-lookup"><span data-stu-id="115c4-258">True</span></span>                              |
| <span data-ttu-id="115c4-259">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="115c4-259">In Global Catalog</span></span>      | <span data-ttu-id="115c4-260">True</span><span class="sxs-lookup"><span data-stu-id="115c4-260">True</span></span>                              |
| <span data-ttu-id="115c4-261">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="115c4-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="115c4-262">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="115c4-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="115c4-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="115c4-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="115c4-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="115c4-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="115c4-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="115c4-265">Search-Flags</span></span>           | <span data-ttu-id="115c4-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="115c4-266">0x00000011</span></span>                        |
| <span data-ttu-id="115c4-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="115c4-267">System-Flags</span></span>           | <span data-ttu-id="115c4-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="115c4-268">0x00000012</span></span>                        |
| <span data-ttu-id="115c4-269">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="115c4-269">Classes used in</span></span>        | [<span data-ttu-id="115c4-270">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="115c4-270">**User**</span></span>](c-user.md)<br/> |



 

 





