---
title: atributo MS-DS-Members-for-AZ-role
description: Lista de grupos de aplicaciones miembro o usuarios vinculados a AZ-role.
ms.assetid: c1234443-fd25-4ed8-a8ee-9853810ebe7d
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-Members-for-AZ-role
- Esquema de AD de atributo msDS-MembersForAzRole
topic_type:
- apiref
api_name:
- ms-DS-Members-For-Az-Role
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b19203e5c44d0389e64531867444d1bb2865196
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494032"
---
# <a name="ms-ds-members-for-az-role-attribute"></a><span data-ttu-id="bfe7e-105">atributo MS-DS-Members-for-AZ-role</span><span class="sxs-lookup"><span data-stu-id="bfe7e-105">ms-DS-Members-For-Az-Role attribute</span></span>

<span data-ttu-id="bfe7e-106">Lista de grupos de aplicaciones miembro o usuarios vinculados a AZ-role.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-106">List of member application groups or users linked to Az-Role.</span></span>



| <span data-ttu-id="bfe7e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="bfe7e-107">Entry</span></span> | <span data-ttu-id="bfe7e-108">Value</span><span class="sxs-lookup"><span data-stu-id="bfe7e-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="bfe7e-109">CN</span><span class="sxs-lookup"><span data-stu-id="bfe7e-109">CN</span></span>                | <span data-ttu-id="bfe7e-110">MS-DS-Members-for-AZ-role</span><span class="sxs-lookup"><span data-stu-id="bfe7e-110">ms-DS-Members-For-Az-Role</span></span>               |
| <span data-ttu-id="bfe7e-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="bfe7e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bfe7e-112">msDS-MembersForAzRole</span><span class="sxs-lookup"><span data-stu-id="bfe7e-112">msDS-MembersForAzRole</span></span>                   |
| <span data-ttu-id="bfe7e-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="bfe7e-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="bfe7e-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="bfe7e-114">Update Privilege</span></span>  | <span data-ttu-id="bfe7e-115">Administrador de AzRoles</span><span class="sxs-lookup"><span data-stu-id="bfe7e-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="bfe7e-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="bfe7e-116">Update Frequency</span></span>  | <span data-ttu-id="bfe7e-117">Durante la inicialización o el cambio de directiva.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="bfe7e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bfe7e-118">Attribute-Id</span></span>      | <span data-ttu-id="bfe7e-119">1.2.840.113556.1.4.1806</span><span class="sxs-lookup"><span data-stu-id="bfe7e-119">1.2.840.113556.1.4.1806</span></span>                 |
| <span data-ttu-id="bfe7e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bfe7e-120">System-Id-Guid</span></span>    | <span data-ttu-id="bfe7e-121">cbf7e6cd-85a4-4314-8939-8bfe80597835</span><span class="sxs-lookup"><span data-stu-id="bfe7e-121">cbf7e6cd-85a4-4314-8939-8bfe80597835</span></span>    |
| <span data-ttu-id="bfe7e-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfe7e-122">Syntax</span></span>            | [<span data-ttu-id="bfe7e-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="bfe7e-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="bfe7e-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="bfe7e-124">Implementations</span></span>

-   [<span data-ttu-id="bfe7e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bfe7e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bfe7e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bfe7e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bfe7e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bfe7e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bfe7e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bfe7e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bfe7e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bfe7e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="bfe7e-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bfe7e-130">Windows Server 2003</span></span>



| <span data-ttu-id="bfe7e-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="bfe7e-131">Entry</span></span> | <span data-ttu-id="bfe7e-132">Value</span><span class="sxs-lookup"><span data-stu-id="bfe7e-132">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="bfe7e-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="bfe7e-133">Link-Id</span></span>                | <span data-ttu-id="bfe7e-134">2016</span><span class="sxs-lookup"><span data-stu-id="bfe7e-134">2016</span></span>                                              |
| <span data-ttu-id="bfe7e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfe7e-135">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="bfe7e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfe7e-136">System-Only</span></span>            | <span data-ttu-id="bfe7e-137">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-137">False</span></span>                                             |
| <span data-ttu-id="bfe7e-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="bfe7e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="bfe7e-139">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-139">False</span></span>                                             |
| <span data-ttu-id="bfe7e-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="bfe7e-140">Is Indexed</span></span>             | <span data-ttu-id="bfe7e-141">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-141">False</span></span>                                             |
| <span data-ttu-id="bfe7e-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="bfe7e-142">In Global Catalog</span></span>      | <span data-ttu-id="bfe7e-143">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-143">False</span></span>                                             |
| <span data-ttu-id="bfe7e-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="bfe7e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfe7e-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bfe7e-145">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="bfe7e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfe7e-146">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="bfe7e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfe7e-147">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="bfe7e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe7e-148">Search-Flags</span></span>           | <span data-ttu-id="bfe7e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfe7e-149">0x00000000</span></span>                                        |
| <span data-ttu-id="bfe7e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe7e-150">System-Flags</span></span>           | <span data-ttu-id="bfe7e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bfe7e-151">0x00000010</span></span>                                        |
| <span data-ttu-id="bfe7e-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="bfe7e-152">Classes used in</span></span>        | [<span data-ttu-id="bfe7e-153">**MS-DS-AZ-role**</span><span class="sxs-lookup"><span data-stu-id="bfe7e-153">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bfe7e-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bfe7e-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bfe7e-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="bfe7e-155">Entry</span></span> | <span data-ttu-id="bfe7e-156">Value</span><span class="sxs-lookup"><span data-stu-id="bfe7e-156">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="bfe7e-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="bfe7e-157">Link-Id</span></span>                | <span data-ttu-id="bfe7e-158">2016</span><span class="sxs-lookup"><span data-stu-id="bfe7e-158">2016</span></span>                                              |
| <span data-ttu-id="bfe7e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfe7e-159">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="bfe7e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfe7e-160">System-Only</span></span>            | <span data-ttu-id="bfe7e-161">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-161">False</span></span>                                             |
| <span data-ttu-id="bfe7e-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="bfe7e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="bfe7e-163">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-163">False</span></span>                                             |
| <span data-ttu-id="bfe7e-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="bfe7e-164">Is Indexed</span></span>             | <span data-ttu-id="bfe7e-165">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-165">False</span></span>                                             |
| <span data-ttu-id="bfe7e-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="bfe7e-166">In Global Catalog</span></span>      | <span data-ttu-id="bfe7e-167">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-167">False</span></span>                                             |
| <span data-ttu-id="bfe7e-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="bfe7e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfe7e-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bfe7e-169">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="bfe7e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfe7e-170">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="bfe7e-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfe7e-171">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="bfe7e-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe7e-172">Search-Flags</span></span>           | <span data-ttu-id="bfe7e-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfe7e-173">0x00000000</span></span>                                        |
| <span data-ttu-id="bfe7e-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe7e-174">System-Flags</span></span>           | <span data-ttu-id="bfe7e-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bfe7e-175">0x00000010</span></span>                                        |
| <span data-ttu-id="bfe7e-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="bfe7e-176">Classes used in</span></span>        | [<span data-ttu-id="bfe7e-177">**MS-DS-AZ-role**</span><span class="sxs-lookup"><span data-stu-id="bfe7e-177">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bfe7e-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bfe7e-178">Windows Server 2008</span></span>



| <span data-ttu-id="bfe7e-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="bfe7e-179">Entry</span></span> | <span data-ttu-id="bfe7e-180">Value</span><span class="sxs-lookup"><span data-stu-id="bfe7e-180">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="bfe7e-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="bfe7e-181">Link-Id</span></span>                | <span data-ttu-id="bfe7e-182">2016</span><span class="sxs-lookup"><span data-stu-id="bfe7e-182">2016</span></span>                                              |
| <span data-ttu-id="bfe7e-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfe7e-183">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="bfe7e-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfe7e-184">System-Only</span></span>            | <span data-ttu-id="bfe7e-185">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-185">False</span></span>                                             |
| <span data-ttu-id="bfe7e-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="bfe7e-186">Is-Single-Valued</span></span>       | <span data-ttu-id="bfe7e-187">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-187">False</span></span>                                             |
| <span data-ttu-id="bfe7e-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="bfe7e-188">Is Indexed</span></span>             | <span data-ttu-id="bfe7e-189">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-189">False</span></span>                                             |
| <span data-ttu-id="bfe7e-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="bfe7e-190">In Global Catalog</span></span>      | <span data-ttu-id="bfe7e-191">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-191">False</span></span>                                             |
| <span data-ttu-id="bfe7e-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="bfe7e-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfe7e-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bfe7e-193">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="bfe7e-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfe7e-194">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="bfe7e-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfe7e-195">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="bfe7e-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe7e-196">Search-Flags</span></span>           | <span data-ttu-id="bfe7e-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfe7e-197">0x00000000</span></span>                                        |
| <span data-ttu-id="bfe7e-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe7e-198">System-Flags</span></span>           | <span data-ttu-id="bfe7e-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bfe7e-199">0x00000010</span></span>                                        |
| <span data-ttu-id="bfe7e-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="bfe7e-200">Classes used in</span></span>        | [<span data-ttu-id="bfe7e-201">**MS-DS-AZ-role**</span><span class="sxs-lookup"><span data-stu-id="bfe7e-201">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bfe7e-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bfe7e-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bfe7e-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="bfe7e-203">Entry</span></span> | <span data-ttu-id="bfe7e-204">Value</span><span class="sxs-lookup"><span data-stu-id="bfe7e-204">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="bfe7e-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="bfe7e-205">Link-Id</span></span>                | <span data-ttu-id="bfe7e-206">2016</span><span class="sxs-lookup"><span data-stu-id="bfe7e-206">2016</span></span>                                              |
| <span data-ttu-id="bfe7e-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfe7e-207">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="bfe7e-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfe7e-208">System-Only</span></span>            | <span data-ttu-id="bfe7e-209">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-209">False</span></span>                                             |
| <span data-ttu-id="bfe7e-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="bfe7e-210">Is-Single-Valued</span></span>       | <span data-ttu-id="bfe7e-211">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-211">False</span></span>                                             |
| <span data-ttu-id="bfe7e-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="bfe7e-212">Is Indexed</span></span>             | <span data-ttu-id="bfe7e-213">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-213">False</span></span>                                             |
| <span data-ttu-id="bfe7e-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="bfe7e-214">In Global Catalog</span></span>      | <span data-ttu-id="bfe7e-215">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-215">False</span></span>                                             |
| <span data-ttu-id="bfe7e-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="bfe7e-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfe7e-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bfe7e-217">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="bfe7e-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfe7e-218">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="bfe7e-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfe7e-219">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="bfe7e-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe7e-220">Search-Flags</span></span>           | <span data-ttu-id="bfe7e-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfe7e-221">0x00000000</span></span>                                        |
| <span data-ttu-id="bfe7e-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe7e-222">System-Flags</span></span>           | <span data-ttu-id="bfe7e-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bfe7e-223">0x00000010</span></span>                                        |
| <span data-ttu-id="bfe7e-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="bfe7e-224">Classes used in</span></span>        | [<span data-ttu-id="bfe7e-225">**MS-DS-AZ-role**</span><span class="sxs-lookup"><span data-stu-id="bfe7e-225">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bfe7e-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bfe7e-226">Windows Server 2012</span></span>



| <span data-ttu-id="bfe7e-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="bfe7e-227">Entry</span></span> | <span data-ttu-id="bfe7e-228">Value</span><span class="sxs-lookup"><span data-stu-id="bfe7e-228">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="bfe7e-229">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="bfe7e-229">Link-Id</span></span>                | <span data-ttu-id="bfe7e-230">2016</span><span class="sxs-lookup"><span data-stu-id="bfe7e-230">2016</span></span>                                              |
| <span data-ttu-id="bfe7e-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfe7e-231">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="bfe7e-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfe7e-232">System-Only</span></span>            | <span data-ttu-id="bfe7e-233">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-233">False</span></span>                                             |
| <span data-ttu-id="bfe7e-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="bfe7e-234">Is-Single-Valued</span></span>       | <span data-ttu-id="bfe7e-235">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-235">False</span></span>                                             |
| <span data-ttu-id="bfe7e-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="bfe7e-236">Is Indexed</span></span>             | <span data-ttu-id="bfe7e-237">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-237">False</span></span>                                             |
| <span data-ttu-id="bfe7e-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="bfe7e-238">In Global Catalog</span></span>      | <span data-ttu-id="bfe7e-239">False</span><span class="sxs-lookup"><span data-stu-id="bfe7e-239">False</span></span>                                             |
| <span data-ttu-id="bfe7e-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="bfe7e-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfe7e-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bfe7e-241">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="bfe7e-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfe7e-242">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="bfe7e-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfe7e-243">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="bfe7e-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe7e-244">Search-Flags</span></span>           | <span data-ttu-id="bfe7e-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfe7e-245">0x00000000</span></span>                                        |
| <span data-ttu-id="bfe7e-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe7e-246">System-Flags</span></span>           | <span data-ttu-id="bfe7e-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bfe7e-247">0x00000010</span></span>                                        |
| <span data-ttu-id="bfe7e-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="bfe7e-248">Classes used in</span></span>        | [<span data-ttu-id="bfe7e-249">**MS-DS-AZ-role**</span><span class="sxs-lookup"><span data-stu-id="bfe7e-249">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



 

 





