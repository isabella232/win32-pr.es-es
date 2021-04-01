---
title: atributo MS-DS-non-members
description: Este atributo tiene el mismo propósito que el atributo que no es de seguridad, pero se aplican las reglas de ámbito.
ms.assetid: 11d3d030-3643-4ed2-a52e-a57f32e9597f
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-non-members
- atributo msDS-nonmembers esquema de AD
topic_type:
- apiref
api_name:
- ms-DS-Non-Members
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca8ca19af90f2f534f974863aa7d766f6be4624b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906034"
---
# <a name="ms-ds-non-members-attribute"></a><span data-ttu-id="7cb15-105">atributo MS-DS-non-members</span><span class="sxs-lookup"><span data-stu-id="7cb15-105">ms-DS-Non-Members attribute</span></span>

<span data-ttu-id="7cb15-106">Este atributo tiene el mismo propósito que el atributo que no es de seguridad, pero se aplican las reglas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="7cb15-106">This attribute serves the same purpose as the Non-Security-Member attribute but with scoping rules applied.</span></span>



| <span data-ttu-id="7cb15-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="7cb15-107">Entry</span></span> | <span data-ttu-id="7cb15-108">Value</span><span class="sxs-lookup"><span data-stu-id="7cb15-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="7cb15-109">CN</span><span class="sxs-lookup"><span data-stu-id="7cb15-109">CN</span></span>                | <span data-ttu-id="7cb15-110">MS-DS-no miembros</span><span class="sxs-lookup"><span data-stu-id="7cb15-110">ms-DS-Non-Members</span></span>                       |
| <span data-ttu-id="7cb15-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="7cb15-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7cb15-112">msDS-no miembro</span><span class="sxs-lookup"><span data-stu-id="7cb15-112">msDS-NonMembers</span></span>                         |
| <span data-ttu-id="7cb15-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="7cb15-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="7cb15-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="7cb15-114">Update Privilege</span></span>  | <span data-ttu-id="7cb15-115">Administrador de AzRoles</span><span class="sxs-lookup"><span data-stu-id="7cb15-115">AzRoles Admin</span></span>                           |
| <span data-ttu-id="7cb15-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="7cb15-116">Update Frequency</span></span>  | <span data-ttu-id="7cb15-117">Durante la inicialización y el cambio de directiva.</span><span class="sxs-lookup"><span data-stu-id="7cb15-117">At initialization and policy change.</span></span>    |
| <span data-ttu-id="7cb15-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7cb15-118">Attribute-Id</span></span>      | <span data-ttu-id="7cb15-119">1.2.840.113556.1.4.1793</span><span class="sxs-lookup"><span data-stu-id="7cb15-119">1.2.840.113556.1.4.1793</span></span>                 |
| <span data-ttu-id="7cb15-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7cb15-120">System-Id-Guid</span></span>    | <span data-ttu-id="7cb15-121">cafcb1de-f23c-46b5-adf7-1e64957bd5db</span><span class="sxs-lookup"><span data-stu-id="7cb15-121">cafcb1de-f23c-46b5-adf7-1e64957bd5db</span></span>    |
| <span data-ttu-id="7cb15-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7cb15-122">Syntax</span></span>            | [<span data-ttu-id="7cb15-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="7cb15-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="7cb15-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="7cb15-124">Implementations</span></span>

-   [<span data-ttu-id="7cb15-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7cb15-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7cb15-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7cb15-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7cb15-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7cb15-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7cb15-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7cb15-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7cb15-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7cb15-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="7cb15-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7cb15-130">Windows Server 2003</span></span>



| <span data-ttu-id="7cb15-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="7cb15-131">Entry</span></span> | <span data-ttu-id="7cb15-132">Value</span><span class="sxs-lookup"><span data-stu-id="7cb15-132">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="7cb15-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7cb15-133">Link-Id</span></span>                | <span data-ttu-id="7cb15-134">2014</span><span class="sxs-lookup"><span data-stu-id="7cb15-134">2014</span></span>                                |
| <span data-ttu-id="7cb15-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7cb15-135">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="7cb15-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7cb15-136">System-Only</span></span>            | <span data-ttu-id="7cb15-137">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-137">False</span></span>                               |
| <span data-ttu-id="7cb15-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7cb15-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7cb15-139">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-139">False</span></span>                               |
| <span data-ttu-id="7cb15-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7cb15-140">Is Indexed</span></span>             | <span data-ttu-id="7cb15-141">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-141">False</span></span>                               |
| <span data-ttu-id="7cb15-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7cb15-142">In Global Catalog</span></span>      | <span data-ttu-id="7cb15-143">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-143">False</span></span>                               |
| <span data-ttu-id="7cb15-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7cb15-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7cb15-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7cb15-145">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="7cb15-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7cb15-146">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="7cb15-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7cb15-147">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="7cb15-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb15-148">Search-Flags</span></span>           | <span data-ttu-id="7cb15-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7cb15-149">0x00000000</span></span>                          |
| <span data-ttu-id="7cb15-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb15-150">System-Flags</span></span>           | <span data-ttu-id="7cb15-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7cb15-151">0x00000010</span></span>                          |
| <span data-ttu-id="7cb15-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7cb15-152">Classes used in</span></span>        | [<span data-ttu-id="7cb15-153">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="7cb15-153">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7cb15-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7cb15-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7cb15-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="7cb15-155">Entry</span></span> | <span data-ttu-id="7cb15-156">Value</span><span class="sxs-lookup"><span data-stu-id="7cb15-156">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="7cb15-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7cb15-157">Link-Id</span></span>                | <span data-ttu-id="7cb15-158">2014</span><span class="sxs-lookup"><span data-stu-id="7cb15-158">2014</span></span>                                |
| <span data-ttu-id="7cb15-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7cb15-159">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="7cb15-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="7cb15-160">System-Only</span></span>            | <span data-ttu-id="7cb15-161">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-161">False</span></span>                               |
| <span data-ttu-id="7cb15-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7cb15-162">Is-Single-Valued</span></span>       | <span data-ttu-id="7cb15-163">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-163">False</span></span>                               |
| <span data-ttu-id="7cb15-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7cb15-164">Is Indexed</span></span>             | <span data-ttu-id="7cb15-165">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-165">False</span></span>                               |
| <span data-ttu-id="7cb15-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7cb15-166">In Global Catalog</span></span>      | <span data-ttu-id="7cb15-167">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-167">False</span></span>                               |
| <span data-ttu-id="7cb15-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7cb15-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="7cb15-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7cb15-169">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="7cb15-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7cb15-170">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="7cb15-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7cb15-171">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="7cb15-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb15-172">Search-Flags</span></span>           | <span data-ttu-id="7cb15-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7cb15-173">0x00000000</span></span>                          |
| <span data-ttu-id="7cb15-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb15-174">System-Flags</span></span>           | <span data-ttu-id="7cb15-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7cb15-175">0x00000010</span></span>                          |
| <span data-ttu-id="7cb15-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7cb15-176">Classes used in</span></span>        | [<span data-ttu-id="7cb15-177">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="7cb15-177">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7cb15-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7cb15-178">Windows Server 2008</span></span>



| <span data-ttu-id="7cb15-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="7cb15-179">Entry</span></span> | <span data-ttu-id="7cb15-180">Value</span><span class="sxs-lookup"><span data-stu-id="7cb15-180">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="7cb15-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7cb15-181">Link-Id</span></span>                | <span data-ttu-id="7cb15-182">2014</span><span class="sxs-lookup"><span data-stu-id="7cb15-182">2014</span></span>                                |
| <span data-ttu-id="7cb15-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7cb15-183">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="7cb15-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="7cb15-184">System-Only</span></span>            | <span data-ttu-id="7cb15-185">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-185">False</span></span>                               |
| <span data-ttu-id="7cb15-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7cb15-186">Is-Single-Valued</span></span>       | <span data-ttu-id="7cb15-187">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-187">False</span></span>                               |
| <span data-ttu-id="7cb15-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7cb15-188">Is Indexed</span></span>             | <span data-ttu-id="7cb15-189">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-189">False</span></span>                               |
| <span data-ttu-id="7cb15-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7cb15-190">In Global Catalog</span></span>      | <span data-ttu-id="7cb15-191">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-191">False</span></span>                               |
| <span data-ttu-id="7cb15-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7cb15-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="7cb15-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7cb15-193">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="7cb15-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7cb15-194">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="7cb15-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7cb15-195">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="7cb15-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb15-196">Search-Flags</span></span>           | <span data-ttu-id="7cb15-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7cb15-197">0x00000000</span></span>                          |
| <span data-ttu-id="7cb15-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb15-198">System-Flags</span></span>           | <span data-ttu-id="7cb15-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7cb15-199">0x00000010</span></span>                          |
| <span data-ttu-id="7cb15-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7cb15-200">Classes used in</span></span>        | [<span data-ttu-id="7cb15-201">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="7cb15-201">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7cb15-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7cb15-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7cb15-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="7cb15-203">Entry</span></span> | <span data-ttu-id="7cb15-204">Value</span><span class="sxs-lookup"><span data-stu-id="7cb15-204">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="7cb15-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7cb15-205">Link-Id</span></span>                | <span data-ttu-id="7cb15-206">2014</span><span class="sxs-lookup"><span data-stu-id="7cb15-206">2014</span></span>                                |
| <span data-ttu-id="7cb15-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7cb15-207">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="7cb15-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="7cb15-208">System-Only</span></span>            | <span data-ttu-id="7cb15-209">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-209">False</span></span>                               |
| <span data-ttu-id="7cb15-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7cb15-210">Is-Single-Valued</span></span>       | <span data-ttu-id="7cb15-211">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-211">False</span></span>                               |
| <span data-ttu-id="7cb15-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7cb15-212">Is Indexed</span></span>             | <span data-ttu-id="7cb15-213">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-213">False</span></span>                               |
| <span data-ttu-id="7cb15-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7cb15-214">In Global Catalog</span></span>      | <span data-ttu-id="7cb15-215">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-215">False</span></span>                               |
| <span data-ttu-id="7cb15-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7cb15-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="7cb15-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7cb15-217">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="7cb15-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7cb15-218">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="7cb15-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7cb15-219">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="7cb15-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb15-220">Search-Flags</span></span>           | <span data-ttu-id="7cb15-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7cb15-221">0x00000000</span></span>                          |
| <span data-ttu-id="7cb15-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb15-222">System-Flags</span></span>           | <span data-ttu-id="7cb15-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7cb15-223">0x00000010</span></span>                          |
| <span data-ttu-id="7cb15-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7cb15-224">Classes used in</span></span>        | [<span data-ttu-id="7cb15-225">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="7cb15-225">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7cb15-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7cb15-226">Windows Server 2012</span></span>



| <span data-ttu-id="7cb15-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="7cb15-227">Entry</span></span> | <span data-ttu-id="7cb15-228">Value</span><span class="sxs-lookup"><span data-stu-id="7cb15-228">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="7cb15-229">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7cb15-229">Link-Id</span></span>                | <span data-ttu-id="7cb15-230">2014</span><span class="sxs-lookup"><span data-stu-id="7cb15-230">2014</span></span>                                |
| <span data-ttu-id="7cb15-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7cb15-231">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="7cb15-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="7cb15-232">System-Only</span></span>            | <span data-ttu-id="7cb15-233">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-233">False</span></span>                               |
| <span data-ttu-id="7cb15-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7cb15-234">Is-Single-Valued</span></span>       | <span data-ttu-id="7cb15-235">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-235">False</span></span>                               |
| <span data-ttu-id="7cb15-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7cb15-236">Is Indexed</span></span>             | <span data-ttu-id="7cb15-237">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-237">False</span></span>                               |
| <span data-ttu-id="7cb15-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7cb15-238">In Global Catalog</span></span>      | <span data-ttu-id="7cb15-239">False</span><span class="sxs-lookup"><span data-stu-id="7cb15-239">False</span></span>                               |
| <span data-ttu-id="7cb15-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7cb15-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="7cb15-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7cb15-241">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="7cb15-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7cb15-242">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="7cb15-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7cb15-243">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="7cb15-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb15-244">Search-Flags</span></span>           | <span data-ttu-id="7cb15-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7cb15-245">0x00000000</span></span>                          |
| <span data-ttu-id="7cb15-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7cb15-246">System-Flags</span></span>           | <span data-ttu-id="7cb15-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7cb15-247">0x00000010</span></span>                          |
| <span data-ttu-id="7cb15-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7cb15-248">Classes used in</span></span>        | [<span data-ttu-id="7cb15-249">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="7cb15-249">**Group**</span></span>](c-group.md)<br/> |



 

 





