---
title: Atributo de miembro
description: La lista de usuarios que pertenecen al grupo.
ms.assetid: 0f5e249e-1fa1-4191-90e6-94c0b657b7fc
ms.tgt_platform: multiple
keywords:
- Atributo de miembro esquema de AD
- atributo de miembro esquema de AD
topic_type:
- apiref
api_name:
- Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c237c7cb7b41ae73bcbdff5a13f6cb34f546449b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658598"
---
# <a name="member-attribute"></a><span data-ttu-id="2f5ee-105">Atributo de miembro</span><span class="sxs-lookup"><span data-stu-id="2f5ee-105">Member attribute</span></span>

<span data-ttu-id="2f5ee-106">La lista de usuarios que pertenecen al grupo.</span><span class="sxs-lookup"><span data-stu-id="2f5ee-106">The list of users that belong to the group.</span></span>



| <span data-ttu-id="2f5ee-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="2f5ee-107">Entry</span></span> | <span data-ttu-id="2f5ee-108">Value</span><span class="sxs-lookup"><span data-stu-id="2f5ee-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="2f5ee-109">CN</span><span class="sxs-lookup"><span data-stu-id="2f5ee-109">CN</span></span>                | <span data-ttu-id="2f5ee-110">Miembro</span><span class="sxs-lookup"><span data-stu-id="2f5ee-110">Member</span></span>                                                |
| <span data-ttu-id="2f5ee-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="2f5ee-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2f5ee-112">miembro</span><span class="sxs-lookup"><span data-stu-id="2f5ee-112">member</span></span>                                                |
| <span data-ttu-id="2f5ee-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="2f5ee-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="2f5ee-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="2f5ee-114">Update Privilege</span></span>  | <span data-ttu-id="2f5ee-115">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="2f5ee-115">Domain administrator</span></span>                                  |
| <span data-ttu-id="2f5ee-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="2f5ee-116">Update Frequency</span></span>  | <span data-ttu-id="2f5ee-117">Cada vez que se agrega o se quita un usuario de un grupo.</span><span class="sxs-lookup"><span data-stu-id="2f5ee-117">Each time a user is added to or removed from a group.</span></span> |
| <span data-ttu-id="2f5ee-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2f5ee-118">Attribute-Id</span></span>      | <span data-ttu-id="2f5ee-119">2.5.4.31</span><span class="sxs-lookup"><span data-stu-id="2f5ee-119">2.5.4.31</span></span>                                              |
| <span data-ttu-id="2f5ee-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2f5ee-120">System-Id-Guid</span></span>    | <span data-ttu-id="2f5ee-121">bf9679c0-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2f5ee-121">bf9679c0-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="2f5ee-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f5ee-122">Syntax</span></span>            | [<span data-ttu-id="2f5ee-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)               |



## <a name="implementations"></a><span data-ttu-id="2f5ee-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="2f5ee-124">Implementations</span></span>

-   [<span data-ttu-id="2f5ee-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2f5ee-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2f5ee-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2f5ee-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2f5ee-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2f5ee-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2f5ee-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2f5ee-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2f5ee-132">Windows 2000 Server</span></span>



| <span data-ttu-id="2f5ee-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="2f5ee-133">Entry</span></span> | <span data-ttu-id="2f5ee-134">Value</span><span class="sxs-lookup"><span data-stu-id="2f5ee-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f5ee-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2f5ee-135">Link-Id</span></span>                | <span data-ttu-id="2f5ee-136">2</span><span class="sxs-lookup"><span data-stu-id="2f5ee-136">2</span></span>                                                                                       |
| <span data-ttu-id="2f5ee-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f5ee-137">MAPI-Id</span></span>                | <span data-ttu-id="2f5ee-138">0x8009</span><span class="sxs-lookup"><span data-stu-id="2f5ee-138">0x8009</span></span>                                                                                  |
| <span data-ttu-id="2f5ee-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f5ee-139">System-Only</span></span>            | <span data-ttu-id="2f5ee-140">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-140">False</span></span>                                                                                   |
| <span data-ttu-id="2f5ee-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2f5ee-141">Is-Single-Valued</span></span>       | <span data-ttu-id="2f5ee-142">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-142">False</span></span>                                                                                   |
| <span data-ttu-id="2f5ee-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2f5ee-143">Is Indexed</span></span>             | <span data-ttu-id="2f5ee-144">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-144">False</span></span>                                                                                   |
| <span data-ttu-id="2f5ee-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2f5ee-145">In Global Catalog</span></span>      | <span data-ttu-id="2f5ee-146">True</span><span class="sxs-lookup"><span data-stu-id="2f5ee-146">True</span></span>                                                                                    |
| <span data-ttu-id="2f5ee-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2f5ee-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f5ee-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2f5ee-148">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="2f5ee-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f5ee-149">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="2f5ee-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f5ee-150">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="2f5ee-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f5ee-151">Search-Flags</span></span>           | <span data-ttu-id="2f5ee-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f5ee-152">0x00000000</span></span>                                                                              |
| <span data-ttu-id="2f5ee-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f5ee-153">System-Flags</span></span>           | <span data-ttu-id="2f5ee-154">0x00000012</span><span class="sxs-lookup"><span data-stu-id="2f5ee-154">0x00000012</span></span>                                                                              |
| <span data-ttu-id="2f5ee-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2f5ee-155">Classes used in</span></span>        | [<span data-ttu-id="2f5ee-156">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-156">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="2f5ee-157">**Grupo de nombres**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-157">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2f5ee-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2f5ee-158">Windows Server 2003</span></span>



| <span data-ttu-id="2f5ee-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="2f5ee-159">Entry</span></span> | <span data-ttu-id="2f5ee-160">Value</span><span class="sxs-lookup"><span data-stu-id="2f5ee-160">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f5ee-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2f5ee-161">Link-Id</span></span>                | <span data-ttu-id="2f5ee-162">2</span><span class="sxs-lookup"><span data-stu-id="2f5ee-162">2</span></span>                                                                                                                                     |
| <span data-ttu-id="2f5ee-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f5ee-163">MAPI-Id</span></span>                | <span data-ttu-id="2f5ee-164">0x8009</span><span class="sxs-lookup"><span data-stu-id="2f5ee-164">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="2f5ee-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f5ee-165">System-Only</span></span>            | <span data-ttu-id="2f5ee-166">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-166">False</span></span>                                                                                                                                 |
| <span data-ttu-id="2f5ee-167">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2f5ee-167">Is-Single-Valued</span></span>       | <span data-ttu-id="2f5ee-168">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-168">False</span></span>                                                                                                                                 |
| <span data-ttu-id="2f5ee-169">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2f5ee-169">Is Indexed</span></span>             | <span data-ttu-id="2f5ee-170">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-170">False</span></span>                                                                                                                                 |
| <span data-ttu-id="2f5ee-171">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2f5ee-171">In Global Catalog</span></span>      | <span data-ttu-id="2f5ee-172">True</span><span class="sxs-lookup"><span data-stu-id="2f5ee-172">True</span></span>                                                                                                                                  |
| <span data-ttu-id="2f5ee-173">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2f5ee-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f5ee-174">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2f5ee-174">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="2f5ee-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f5ee-175">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="2f5ee-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f5ee-176">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="2f5ee-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f5ee-177">Search-Flags</span></span>           | <span data-ttu-id="2f5ee-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f5ee-178">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="2f5ee-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f5ee-179">System-Flags</span></span>           | <span data-ttu-id="2f5ee-180">0x00000012</span><span class="sxs-lookup"><span data-stu-id="2f5ee-180">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="2f5ee-181">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2f5ee-181">Classes used in</span></span>        | [<span data-ttu-id="2f5ee-182">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-182">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="2f5ee-183">**Grupo de nombres**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-183">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="2f5ee-184">**MSMQ: Grupo**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-184">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2f5ee-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="2f5ee-185">ADAM</span></span>



| <span data-ttu-id="2f5ee-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="2f5ee-186">Entry</span></span> | <span data-ttu-id="2f5ee-187">Value</span><span class="sxs-lookup"><span data-stu-id="2f5ee-187">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="2f5ee-188">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2f5ee-188">Link-Id</span></span>                | <span data-ttu-id="2f5ee-189">2</span><span class="sxs-lookup"><span data-stu-id="2f5ee-189">2</span></span>                                   |
| <span data-ttu-id="2f5ee-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f5ee-190">MAPI-Id</span></span>                | <span data-ttu-id="2f5ee-191">0x8009</span><span class="sxs-lookup"><span data-stu-id="2f5ee-191">0x8009</span></span>                              |
| <span data-ttu-id="2f5ee-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f5ee-192">System-Only</span></span>            | <span data-ttu-id="2f5ee-193">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-193">False</span></span>                               |
| <span data-ttu-id="2f5ee-194">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2f5ee-194">Is-Single-Valued</span></span>       | <span data-ttu-id="2f5ee-195">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-195">False</span></span>                               |
| <span data-ttu-id="2f5ee-196">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2f5ee-196">Is Indexed</span></span>             | <span data-ttu-id="2f5ee-197">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-197">False</span></span>                               |
| <span data-ttu-id="2f5ee-198">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2f5ee-198">In Global Catalog</span></span>      | <span data-ttu-id="2f5ee-199">True</span><span class="sxs-lookup"><span data-stu-id="2f5ee-199">True</span></span>                                |
| <span data-ttu-id="2f5ee-200">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2f5ee-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f5ee-201">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2f5ee-201">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="2f5ee-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f5ee-202">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="2f5ee-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f5ee-203">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="2f5ee-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f5ee-204">Search-Flags</span></span>           | <span data-ttu-id="2f5ee-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f5ee-205">0x00000000</span></span>                          |
| <span data-ttu-id="2f5ee-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f5ee-206">System-Flags</span></span>           | <span data-ttu-id="2f5ee-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="2f5ee-207">0x00000012</span></span>                          |
| <span data-ttu-id="2f5ee-208">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2f5ee-208">Classes used in</span></span>        | [<span data-ttu-id="2f5ee-209">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-209">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2f5ee-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2f5ee-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2f5ee-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="2f5ee-211">Entry</span></span> | <span data-ttu-id="2f5ee-212">Value</span><span class="sxs-lookup"><span data-stu-id="2f5ee-212">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f5ee-213">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2f5ee-213">Link-Id</span></span>                | <span data-ttu-id="2f5ee-214">2</span><span class="sxs-lookup"><span data-stu-id="2f5ee-214">2</span></span>                                                                                                                                     |
| <span data-ttu-id="2f5ee-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f5ee-215">MAPI-Id</span></span>                | <span data-ttu-id="2f5ee-216">0x8009</span><span class="sxs-lookup"><span data-stu-id="2f5ee-216">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="2f5ee-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f5ee-217">System-Only</span></span>            | <span data-ttu-id="2f5ee-218">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-218">False</span></span>                                                                                                                                 |
| <span data-ttu-id="2f5ee-219">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2f5ee-219">Is-Single-Valued</span></span>       | <span data-ttu-id="2f5ee-220">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-220">False</span></span>                                                                                                                                 |
| <span data-ttu-id="2f5ee-221">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2f5ee-221">Is Indexed</span></span>             | <span data-ttu-id="2f5ee-222">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-222">False</span></span>                                                                                                                                 |
| <span data-ttu-id="2f5ee-223">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2f5ee-223">In Global Catalog</span></span>      | <span data-ttu-id="2f5ee-224">True</span><span class="sxs-lookup"><span data-stu-id="2f5ee-224">True</span></span>                                                                                                                                  |
| <span data-ttu-id="2f5ee-225">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2f5ee-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f5ee-226">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2f5ee-226">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="2f5ee-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f5ee-227">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="2f5ee-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f5ee-228">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="2f5ee-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f5ee-229">Search-Flags</span></span>           | <span data-ttu-id="2f5ee-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f5ee-230">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="2f5ee-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f5ee-231">System-Flags</span></span>           | <span data-ttu-id="2f5ee-232">0x00000012</span><span class="sxs-lookup"><span data-stu-id="2f5ee-232">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="2f5ee-233">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2f5ee-233">Classes used in</span></span>        | [<span data-ttu-id="2f5ee-234">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-234">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="2f5ee-235">**Grupo de nombres**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-235">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="2f5ee-236">**MSMQ: Grupo**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-236">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2f5ee-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f5ee-237">Windows Server 2008</span></span>



| <span data-ttu-id="2f5ee-238">Entrada</span><span class="sxs-lookup"><span data-stu-id="2f5ee-238">Entry</span></span> | <span data-ttu-id="2f5ee-239">Value</span><span class="sxs-lookup"><span data-stu-id="2f5ee-239">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f5ee-240">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2f5ee-240">Link-Id</span></span>                | <span data-ttu-id="2f5ee-241">2</span><span class="sxs-lookup"><span data-stu-id="2f5ee-241">2</span></span>                                                                                                                                     |
| <span data-ttu-id="2f5ee-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f5ee-242">MAPI-Id</span></span>                | <span data-ttu-id="2f5ee-243">0x8009</span><span class="sxs-lookup"><span data-stu-id="2f5ee-243">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="2f5ee-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f5ee-244">System-Only</span></span>            | <span data-ttu-id="2f5ee-245">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-245">False</span></span>                                                                                                                                 |
| <span data-ttu-id="2f5ee-246">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2f5ee-246">Is-Single-Valued</span></span>       | <span data-ttu-id="2f5ee-247">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-247">False</span></span>                                                                                                                                 |
| <span data-ttu-id="2f5ee-248">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2f5ee-248">Is Indexed</span></span>             | <span data-ttu-id="2f5ee-249">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-249">False</span></span>                                                                                                                                 |
| <span data-ttu-id="2f5ee-250">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2f5ee-250">In Global Catalog</span></span>      | <span data-ttu-id="2f5ee-251">True</span><span class="sxs-lookup"><span data-stu-id="2f5ee-251">True</span></span>                                                                                                                                  |
| <span data-ttu-id="2f5ee-252">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2f5ee-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f5ee-253">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2f5ee-253">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="2f5ee-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f5ee-254">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="2f5ee-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f5ee-255">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="2f5ee-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f5ee-256">Search-Flags</span></span>           | <span data-ttu-id="2f5ee-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f5ee-257">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="2f5ee-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f5ee-258">System-Flags</span></span>           | <span data-ttu-id="2f5ee-259">0x00000012</span><span class="sxs-lookup"><span data-stu-id="2f5ee-259">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="2f5ee-260">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2f5ee-260">Classes used in</span></span>        | [<span data-ttu-id="2f5ee-261">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-261">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="2f5ee-262">**Grupo de nombres**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-262">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="2f5ee-263">**MSMQ: Grupo**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-263">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2f5ee-264">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2f5ee-264">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2f5ee-265">Entrada</span><span class="sxs-lookup"><span data-stu-id="2f5ee-265">Entry</span></span> | <span data-ttu-id="2f5ee-266">Value</span><span class="sxs-lookup"><span data-stu-id="2f5ee-266">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f5ee-267">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2f5ee-267">Link-Id</span></span>                | <span data-ttu-id="2f5ee-268">2</span><span class="sxs-lookup"><span data-stu-id="2f5ee-268">2</span></span>                                                                                                                                     |
| <span data-ttu-id="2f5ee-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f5ee-269">MAPI-Id</span></span>                | <span data-ttu-id="2f5ee-270">0x8009</span><span class="sxs-lookup"><span data-stu-id="2f5ee-270">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="2f5ee-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f5ee-271">System-Only</span></span>            | <span data-ttu-id="2f5ee-272">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-272">False</span></span>                                                                                                                                 |
| <span data-ttu-id="2f5ee-273">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2f5ee-273">Is-Single-Valued</span></span>       | <span data-ttu-id="2f5ee-274">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-274">False</span></span>                                                                                                                                 |
| <span data-ttu-id="2f5ee-275">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2f5ee-275">Is Indexed</span></span>             | <span data-ttu-id="2f5ee-276">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-276">False</span></span>                                                                                                                                 |
| <span data-ttu-id="2f5ee-277">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2f5ee-277">In Global Catalog</span></span>      | <span data-ttu-id="2f5ee-278">True</span><span class="sxs-lookup"><span data-stu-id="2f5ee-278">True</span></span>                                                                                                                                  |
| <span data-ttu-id="2f5ee-279">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2f5ee-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f5ee-280">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2f5ee-280">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="2f5ee-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f5ee-281">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="2f5ee-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f5ee-282">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="2f5ee-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f5ee-283">Search-Flags</span></span>           | <span data-ttu-id="2f5ee-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f5ee-284">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="2f5ee-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f5ee-285">System-Flags</span></span>           | <span data-ttu-id="2f5ee-286">0x00000012</span><span class="sxs-lookup"><span data-stu-id="2f5ee-286">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="2f5ee-287">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2f5ee-287">Classes used in</span></span>        | [<span data-ttu-id="2f5ee-288">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-288">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="2f5ee-289">**Grupo de nombres**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-289">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="2f5ee-290">**MSMQ: Grupo**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-290">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2f5ee-291">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2f5ee-291">Windows Server 2012</span></span>



| <span data-ttu-id="2f5ee-292">Entrada</span><span class="sxs-lookup"><span data-stu-id="2f5ee-292">Entry</span></span> | <span data-ttu-id="2f5ee-293">Value</span><span class="sxs-lookup"><span data-stu-id="2f5ee-293">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f5ee-294">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2f5ee-294">Link-Id</span></span>                | <span data-ttu-id="2f5ee-295">2</span><span class="sxs-lookup"><span data-stu-id="2f5ee-295">2</span></span>                                                                                                                                     |
| <span data-ttu-id="2f5ee-296">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f5ee-296">MAPI-Id</span></span>                | <span data-ttu-id="2f5ee-297">0x8009</span><span class="sxs-lookup"><span data-stu-id="2f5ee-297">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="2f5ee-298">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f5ee-298">System-Only</span></span>            | <span data-ttu-id="2f5ee-299">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-299">False</span></span>                                                                                                                                 |
| <span data-ttu-id="2f5ee-300">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2f5ee-300">Is-Single-Valued</span></span>       | <span data-ttu-id="2f5ee-301">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-301">False</span></span>                                                                                                                                 |
| <span data-ttu-id="2f5ee-302">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2f5ee-302">Is Indexed</span></span>             | <span data-ttu-id="2f5ee-303">False</span><span class="sxs-lookup"><span data-stu-id="2f5ee-303">False</span></span>                                                                                                                                 |
| <span data-ttu-id="2f5ee-304">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2f5ee-304">In Global Catalog</span></span>      | <span data-ttu-id="2f5ee-305">True</span><span class="sxs-lookup"><span data-stu-id="2f5ee-305">True</span></span>                                                                                                                                  |
| <span data-ttu-id="2f5ee-306">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2f5ee-306">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f5ee-307">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2f5ee-307">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="2f5ee-308">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f5ee-308">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="2f5ee-309">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f5ee-309">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="2f5ee-310">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f5ee-310">Search-Flags</span></span>           | <span data-ttu-id="2f5ee-311">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f5ee-311">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="2f5ee-312">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f5ee-312">System-Flags</span></span>           | <span data-ttu-id="2f5ee-313">0x00000012</span><span class="sxs-lookup"><span data-stu-id="2f5ee-313">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="2f5ee-314">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2f5ee-314">Classes used in</span></span>        | [<span data-ttu-id="2f5ee-315">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-315">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="2f5ee-316">**Grupo de nombres**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-316">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="2f5ee-317">**MSMQ: Grupo**</span><span class="sxs-lookup"><span data-stu-id="2f5ee-317">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



 

 





