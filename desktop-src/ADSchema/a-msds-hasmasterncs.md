---
title: atributo MS-DS-tiene-Master-NCS
description: Contiene los contextos de nomenclatura mantenidos por un controlador de dominio. Este atributo deja de ser-Master-NC.
ms.assetid: 5325db42-afd7-472c-8797-447e752a3907
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MS-DS-tiene-Master-NC
- Esquema de AD de atributo msDS-hasMasterNCs
topic_type:
- apiref
api_name:
- ms-DS-Has-Master-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24507460eaa7653cfc2c98d3772942de9936162c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906203"
---
# <a name="ms-ds-has-master-ncs-attribute"></a><span data-ttu-id="ab5be-106">atributo MS-DS-tiene-Master-NCS</span><span class="sxs-lookup"><span data-stu-id="ab5be-106">ms-DS-Has-Master-NCs attribute</span></span>

<span data-ttu-id="ab5be-107">Contiene los contextos de nomenclatura mantenidos por un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="ab5be-107">Contains the naming contexts held by a domain controller.</span></span> <span data-ttu-id="ab5be-108">Este atributo deja de ser-Master-NC.</span><span class="sxs-lookup"><span data-stu-id="ab5be-108">This attribute deprecates has-Master-NCs.</span></span>



| <span data-ttu-id="ab5be-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="ab5be-109">Entry</span></span> | <span data-ttu-id="ab5be-110">Value</span><span class="sxs-lookup"><span data-stu-id="ab5be-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="ab5be-111">CN</span><span class="sxs-lookup"><span data-stu-id="ab5be-111">CN</span></span>                | <span data-ttu-id="ab5be-112">MS-DS-tiene-Master-NC</span><span class="sxs-lookup"><span data-stu-id="ab5be-112">ms-DS-Has-Master-NCs</span></span>                    |
| <span data-ttu-id="ab5be-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="ab5be-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ab5be-114">msDS-hasMasterNCs</span><span class="sxs-lookup"><span data-stu-id="ab5be-114">msDS-hasMasterNCs</span></span>                       |
| <span data-ttu-id="ab5be-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="ab5be-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="ab5be-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="ab5be-116">Update Privilege</span></span>  | <span data-ttu-id="ab5be-117">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="ab5be-117">This value is set by the system</span></span>         |
| <span data-ttu-id="ab5be-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="ab5be-118">Update Frequency</span></span>  | <span data-ttu-id="ab5be-119">Cada vez que se crea un nuevo NC.</span><span class="sxs-lookup"><span data-stu-id="ab5be-119">Each time a new NC is created.</span></span>          |
| <span data-ttu-id="ab5be-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ab5be-120">Attribute-Id</span></span>      | <span data-ttu-id="ab5be-121">1.2.840.113556.1.4.1836</span><span class="sxs-lookup"><span data-stu-id="ab5be-121">1.2.840.113556.1.4.1836</span></span>                 |
| <span data-ttu-id="ab5be-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ab5be-122">System-Id-Guid</span></span>    | <span data-ttu-id="ab5be-123">ae2de0e2-59d7-4d47-8d47-ed4dfe4357ad</span><span class="sxs-lookup"><span data-stu-id="ab5be-123">ae2de0e2-59d7-4d47-8d47-ed4dfe4357ad</span></span>    |
| <span data-ttu-id="ab5be-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab5be-124">Syntax</span></span>            | [<span data-ttu-id="ab5be-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="ab5be-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="ab5be-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="ab5be-126">Implementations</span></span>

-   [<span data-ttu-id="ab5be-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ab5be-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ab5be-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ab5be-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ab5be-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ab5be-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ab5be-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ab5be-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ab5be-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ab5be-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ab5be-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ab5be-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ab5be-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ab5be-133">Windows Server 2003</span></span>



| <span data-ttu-id="ab5be-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="ab5be-134">Entry</span></span> | <span data-ttu-id="ab5be-135">Value</span><span class="sxs-lookup"><span data-stu-id="ab5be-135">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ab5be-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ab5be-136">Link-Id</span></span>                | <span data-ttu-id="ab5be-137">2036</span><span class="sxs-lookup"><span data-stu-id="ab5be-137">2036</span></span>                                     |
| <span data-ttu-id="ab5be-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab5be-138">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="ab5be-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab5be-139">System-Only</span></span>            | <span data-ttu-id="ab5be-140">True</span><span class="sxs-lookup"><span data-stu-id="ab5be-140">True</span></span>                                     |
| <span data-ttu-id="ab5be-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ab5be-141">Is-Single-Valued</span></span>       | <span data-ttu-id="ab5be-142">False</span><span class="sxs-lookup"><span data-stu-id="ab5be-142">False</span></span>                                    |
| <span data-ttu-id="ab5be-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ab5be-143">Is Indexed</span></span>             | <span data-ttu-id="ab5be-144">False</span><span class="sxs-lookup"><span data-stu-id="ab5be-144">False</span></span>                                    |
| <span data-ttu-id="ab5be-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ab5be-145">In Global Catalog</span></span>      | <span data-ttu-id="ab5be-146">False</span><span class="sxs-lookup"><span data-stu-id="ab5be-146">False</span></span>                                    |
| <span data-ttu-id="ab5be-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ab5be-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab5be-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab5be-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ab5be-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab5be-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ab5be-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab5be-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ab5be-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab5be-151">Search-Flags</span></span>           | <span data-ttu-id="ab5be-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab5be-152">0x00000000</span></span>                               |
| <span data-ttu-id="ab5be-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab5be-153">System-Flags</span></span>           | <span data-ttu-id="ab5be-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab5be-154">0x00000010</span></span>                               |
| <span data-ttu-id="ab5be-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ab5be-155">Classes used in</span></span>        | [<span data-ttu-id="ab5be-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ab5be-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ab5be-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="ab5be-157">ADAM</span></span>



| <span data-ttu-id="ab5be-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="ab5be-158">Entry</span></span> | <span data-ttu-id="ab5be-159">Value</span><span class="sxs-lookup"><span data-stu-id="ab5be-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ab5be-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ab5be-160">Link-Id</span></span>                | <span data-ttu-id="ab5be-161">2036</span><span class="sxs-lookup"><span data-stu-id="ab5be-161">2036</span></span>                                     |
| <span data-ttu-id="ab5be-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab5be-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="ab5be-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab5be-163">System-Only</span></span>            | <span data-ttu-id="ab5be-164">True</span><span class="sxs-lookup"><span data-stu-id="ab5be-164">True</span></span>                                     |
| <span data-ttu-id="ab5be-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ab5be-165">Is-Single-Valued</span></span>       | <span data-ttu-id="ab5be-166">False</span><span class="sxs-lookup"><span data-stu-id="ab5be-166">False</span></span>                                    |
| <span data-ttu-id="ab5be-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ab5be-167">Is Indexed</span></span>             | <span data-ttu-id="ab5be-168">False</span><span class="sxs-lookup"><span data-stu-id="ab5be-168">False</span></span>                                    |
| <span data-ttu-id="ab5be-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ab5be-169">In Global Catalog</span></span>      | <span data-ttu-id="ab5be-170">False</span><span class="sxs-lookup"><span data-stu-id="ab5be-170">False</span></span>                                    |
| <span data-ttu-id="ab5be-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ab5be-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab5be-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab5be-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ab5be-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab5be-173">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ab5be-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab5be-174">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ab5be-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab5be-175">Search-Flags</span></span>           | <span data-ttu-id="ab5be-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab5be-176">0x00000000</span></span>                               |
| <span data-ttu-id="ab5be-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab5be-177">System-Flags</span></span>           | <span data-ttu-id="ab5be-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab5be-178">0x00000010</span></span>                               |
| <span data-ttu-id="ab5be-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ab5be-179">Classes used in</span></span>        | [<span data-ttu-id="ab5be-180">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ab5be-180">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ab5be-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ab5be-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ab5be-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="ab5be-182">Entry</span></span> | <span data-ttu-id="ab5be-183">Value</span><span class="sxs-lookup"><span data-stu-id="ab5be-183">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ab5be-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ab5be-184">Link-Id</span></span>                | <span data-ttu-id="ab5be-185">2036</span><span class="sxs-lookup"><span data-stu-id="ab5be-185">2036</span></span>                                     |
| <span data-ttu-id="ab5be-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab5be-186">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="ab5be-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab5be-187">System-Only</span></span>            | <span data-ttu-id="ab5be-188">True</span><span class="sxs-lookup"><span data-stu-id="ab5be-188">True</span></span>                                     |
| <span data-ttu-id="ab5be-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ab5be-189">Is-Single-Valued</span></span>       | <span data-ttu-id="ab5be-190">False</span><span class="sxs-lookup"><span data-stu-id="ab5be-190">False</span></span>                                    |
| <span data-ttu-id="ab5be-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ab5be-191">Is Indexed</span></span>             | <span data-ttu-id="ab5be-192">False</span><span class="sxs-lookup"><span data-stu-id="ab5be-192">False</span></span>                                    |
| <span data-ttu-id="ab5be-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ab5be-193">In Global Catalog</span></span>      | <span data-ttu-id="ab5be-194">False</span><span class="sxs-lookup"><span data-stu-id="ab5be-194">False</span></span>                                    |
| <span data-ttu-id="ab5be-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ab5be-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab5be-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab5be-196">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ab5be-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab5be-197">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ab5be-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab5be-198">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ab5be-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab5be-199">Search-Flags</span></span>           | <span data-ttu-id="ab5be-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab5be-200">0x00000000</span></span>                               |
| <span data-ttu-id="ab5be-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab5be-201">System-Flags</span></span>           | <span data-ttu-id="ab5be-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab5be-202">0x00000010</span></span>                               |
| <span data-ttu-id="ab5be-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ab5be-203">Classes used in</span></span>        | [<span data-ttu-id="ab5be-204">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ab5be-204">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ab5be-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab5be-205">Windows Server 2008</span></span>



| <span data-ttu-id="ab5be-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="ab5be-206">Entry</span></span> | <span data-ttu-id="ab5be-207">Value</span><span class="sxs-lookup"><span data-stu-id="ab5be-207">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ab5be-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ab5be-208">Link-Id</span></span>                | <span data-ttu-id="ab5be-209">2036</span><span class="sxs-lookup"><span data-stu-id="ab5be-209">2036</span></span>                                     |
| <span data-ttu-id="ab5be-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab5be-210">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="ab5be-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab5be-211">System-Only</span></span>            | <span data-ttu-id="ab5be-212">True</span><span class="sxs-lookup"><span data-stu-id="ab5be-212">True</span></span>                                     |
| <span data-ttu-id="ab5be-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ab5be-213">Is-Single-Valued</span></span>       | <span data-ttu-id="ab5be-214">False</span><span class="sxs-lookup"><span data-stu-id="ab5be-214">False</span></span>                                    |
| <span data-ttu-id="ab5be-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ab5be-215">Is Indexed</span></span>             | <span data-ttu-id="ab5be-216">False</span><span class="sxs-lookup"><span data-stu-id="ab5be-216">False</span></span>                                    |
| <span data-ttu-id="ab5be-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ab5be-217">In Global Catalog</span></span>      | <span data-ttu-id="ab5be-218">False</span><span class="sxs-lookup"><span data-stu-id="ab5be-218">False</span></span>                                    |
| <span data-ttu-id="ab5be-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ab5be-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab5be-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab5be-220">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ab5be-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab5be-221">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ab5be-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab5be-222">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ab5be-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab5be-223">Search-Flags</span></span>           | <span data-ttu-id="ab5be-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab5be-224">0x00000000</span></span>                               |
| <span data-ttu-id="ab5be-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab5be-225">System-Flags</span></span>           | <span data-ttu-id="ab5be-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab5be-226">0x00000010</span></span>                               |
| <span data-ttu-id="ab5be-227">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ab5be-227">Classes used in</span></span>        | [<span data-ttu-id="ab5be-228">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ab5be-228">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ab5be-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ab5be-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ab5be-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="ab5be-230">Entry</span></span> | <span data-ttu-id="ab5be-231">Value</span><span class="sxs-lookup"><span data-stu-id="ab5be-231">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ab5be-232">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ab5be-232">Link-Id</span></span>                | <span data-ttu-id="ab5be-233">2036</span><span class="sxs-lookup"><span data-stu-id="ab5be-233">2036</span></span>                                     |
| <span data-ttu-id="ab5be-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab5be-234">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="ab5be-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab5be-235">System-Only</span></span>            | <span data-ttu-id="ab5be-236">True</span><span class="sxs-lookup"><span data-stu-id="ab5be-236">True</span></span>                                     |
| <span data-ttu-id="ab5be-237">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ab5be-237">Is-Single-Valued</span></span>       | <span data-ttu-id="ab5be-238">False</span><span class="sxs-lookup"><span data-stu-id="ab5be-238">False</span></span>                                    |
| <span data-ttu-id="ab5be-239">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ab5be-239">Is Indexed</span></span>             | <span data-ttu-id="ab5be-240">False</span><span class="sxs-lookup"><span data-stu-id="ab5be-240">False</span></span>                                    |
| <span data-ttu-id="ab5be-241">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ab5be-241">In Global Catalog</span></span>      | <span data-ttu-id="ab5be-242">False</span><span class="sxs-lookup"><span data-stu-id="ab5be-242">False</span></span>                                    |
| <span data-ttu-id="ab5be-243">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ab5be-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab5be-244">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab5be-244">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ab5be-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab5be-245">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ab5be-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab5be-246">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ab5be-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab5be-247">Search-Flags</span></span>           | <span data-ttu-id="ab5be-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab5be-248">0x00000000</span></span>                               |
| <span data-ttu-id="ab5be-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab5be-249">System-Flags</span></span>           | <span data-ttu-id="ab5be-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab5be-250">0x00000010</span></span>                               |
| <span data-ttu-id="ab5be-251">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ab5be-251">Classes used in</span></span>        | [<span data-ttu-id="ab5be-252">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ab5be-252">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ab5be-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ab5be-253">Windows Server 2012</span></span>



| <span data-ttu-id="ab5be-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="ab5be-254">Entry</span></span> | <span data-ttu-id="ab5be-255">Value</span><span class="sxs-lookup"><span data-stu-id="ab5be-255">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ab5be-256">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ab5be-256">Link-Id</span></span>                | <span data-ttu-id="ab5be-257">2036</span><span class="sxs-lookup"><span data-stu-id="ab5be-257">2036</span></span>                                     |
| <span data-ttu-id="ab5be-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab5be-258">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="ab5be-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab5be-259">System-Only</span></span>            | <span data-ttu-id="ab5be-260">True</span><span class="sxs-lookup"><span data-stu-id="ab5be-260">True</span></span>                                     |
| <span data-ttu-id="ab5be-261">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ab5be-261">Is-Single-Valued</span></span>       | <span data-ttu-id="ab5be-262">False</span><span class="sxs-lookup"><span data-stu-id="ab5be-262">False</span></span>                                    |
| <span data-ttu-id="ab5be-263">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ab5be-263">Is Indexed</span></span>             | <span data-ttu-id="ab5be-264">False</span><span class="sxs-lookup"><span data-stu-id="ab5be-264">False</span></span>                                    |
| <span data-ttu-id="ab5be-265">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ab5be-265">In Global Catalog</span></span>      | <span data-ttu-id="ab5be-266">False</span><span class="sxs-lookup"><span data-stu-id="ab5be-266">False</span></span>                                    |
| <span data-ttu-id="ab5be-267">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ab5be-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab5be-268">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab5be-268">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ab5be-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab5be-269">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ab5be-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab5be-270">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ab5be-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab5be-271">Search-Flags</span></span>           | <span data-ttu-id="ab5be-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab5be-272">0x00000000</span></span>                               |
| <span data-ttu-id="ab5be-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab5be-273">System-Flags</span></span>           | <span data-ttu-id="ab5be-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab5be-274">0x00000010</span></span>                               |
| <span data-ttu-id="ab5be-275">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ab5be-275">Classes used in</span></span>        | [<span data-ttu-id="ab5be-276">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ab5be-276">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





