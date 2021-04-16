---
title: MS-DS-Cached-pertenencia-atributo de marca de tiempo
description: El administrador de cuentas de seguridad usa el atributo MS-DS-Cached-Membership-Stamp para la expansión del grupo durante la evaluación de tokens.
ms.assetid: cb096f79-a57b-4001-b197-e75522904734
ms.tgt_platform: multiple
keywords:
- 'MS-DS-Cached-Membership: esquema de AD de atributos de marca de tiempo'
- msDS-Cached-Membership-esquema de AD de atributo de marca de tiempo
topic_type:
- apiref
api_name:
- ms-DS-Cached-Membership-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 403e87288d906587a11f2a140a9f447ce8236aca
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658891"
---
# <a name="ms-ds-cached-membership-time-stamp-attribute"></a><span data-ttu-id="a679e-105">MS-DS-Cached-pertenencia-atributo de marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="a679e-105">ms-DS-Cached-Membership-Time-Stamp attribute</span></span>

<span data-ttu-id="a679e-106">El administrador de cuentas de seguridad usa el atributo **MS-DS-Cached-Membership-Stamp** para la expansión del grupo durante la evaluación de tokens.</span><span class="sxs-lookup"><span data-stu-id="a679e-106">The **ms-DS-Cached-Membership-Time-Stamp** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="a679e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a679e-107">Entry</span></span> | <span data-ttu-id="a679e-108">Value</span><span class="sxs-lookup"><span data-stu-id="a679e-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a679e-109">CN</span><span class="sxs-lookup"><span data-stu-id="a679e-109">CN</span></span>                | <span data-ttu-id="a679e-110">MS-DS-Cached-Membership-marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="a679e-110">ms-DS-Cached-Membership-Time-Stamp</span></span>   |
| <span data-ttu-id="a679e-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="a679e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a679e-112">msDS-Cached-Membership-marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="a679e-112">msDS-Cached-Membership-Time-Stamp</span></span>    |
| <span data-ttu-id="a679e-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a679e-113">Size</span></span>              | <span data-ttu-id="a679e-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="a679e-114">8 bytes</span></span>                              |
| <span data-ttu-id="a679e-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="a679e-115">Update Privilege</span></span>  | <span data-ttu-id="a679e-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="a679e-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="a679e-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="a679e-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a679e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a679e-118">Attribute-Id</span></span>      | <span data-ttu-id="a679e-119">1.2.840.113556.1.4.1442</span><span class="sxs-lookup"><span data-stu-id="a679e-119">1.2.840.113556.1.4.1442</span></span>              |
| <span data-ttu-id="a679e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a679e-120">System-Id-Guid</span></span>    | <span data-ttu-id="a679e-121">3566bf1f-beee-4dcb-8abe-ef89fcfec6c1</span><span class="sxs-lookup"><span data-stu-id="a679e-121">3566bf1f-beee-4dcb-8abe-ef89fcfec6c1</span></span> |
| <span data-ttu-id="a679e-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a679e-122">Syntax</span></span>            | [<span data-ttu-id="a679e-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="a679e-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="a679e-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="a679e-124">Implementations</span></span>

-   [<span data-ttu-id="a679e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a679e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a679e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a679e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a679e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a679e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a679e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a679e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a679e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a679e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a679e-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a679e-130">Windows Server 2003</span></span>



| <span data-ttu-id="a679e-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="a679e-131">Entry</span></span> | <span data-ttu-id="a679e-132">Value</span><span class="sxs-lookup"><span data-stu-id="a679e-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a679e-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a679e-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a679e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a679e-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a679e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="a679e-135">System-Only</span></span>            | <span data-ttu-id="a679e-136">False</span><span class="sxs-lookup"><span data-stu-id="a679e-136">False</span></span>                             |
| <span data-ttu-id="a679e-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a679e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="a679e-138">True</span><span class="sxs-lookup"><span data-stu-id="a679e-138">True</span></span>                              |
| <span data-ttu-id="a679e-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a679e-139">Is Indexed</span></span>             | <span data-ttu-id="a679e-140">True</span><span class="sxs-lookup"><span data-stu-id="a679e-140">True</span></span>                              |
| <span data-ttu-id="a679e-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a679e-141">In Global Catalog</span></span>      | <span data-ttu-id="a679e-142">False</span><span class="sxs-lookup"><span data-stu-id="a679e-142">False</span></span>                             |
| <span data-ttu-id="a679e-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a679e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="a679e-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a679e-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a679e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a679e-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a679e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a679e-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a679e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a679e-147">Search-Flags</span></span>           | <span data-ttu-id="a679e-148">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a679e-148">0x00000001</span></span>                        |
| <span data-ttu-id="a679e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a679e-149">System-Flags</span></span>           | <span data-ttu-id="a679e-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="a679e-150">0x00000011</span></span>                        |
| <span data-ttu-id="a679e-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a679e-151">Classes used in</span></span>        | [<span data-ttu-id="a679e-152">**User**</span><span class="sxs-lookup"><span data-stu-id="a679e-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a679e-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a679e-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a679e-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="a679e-154">Entry</span></span> | <span data-ttu-id="a679e-155">Value</span><span class="sxs-lookup"><span data-stu-id="a679e-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a679e-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a679e-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a679e-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a679e-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a679e-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="a679e-158">System-Only</span></span>            | <span data-ttu-id="a679e-159">False</span><span class="sxs-lookup"><span data-stu-id="a679e-159">False</span></span>                             |
| <span data-ttu-id="a679e-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a679e-160">Is-Single-Valued</span></span>       | <span data-ttu-id="a679e-161">True</span><span class="sxs-lookup"><span data-stu-id="a679e-161">True</span></span>                              |
| <span data-ttu-id="a679e-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a679e-162">Is Indexed</span></span>             | <span data-ttu-id="a679e-163">True</span><span class="sxs-lookup"><span data-stu-id="a679e-163">True</span></span>                              |
| <span data-ttu-id="a679e-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a679e-164">In Global Catalog</span></span>      | <span data-ttu-id="a679e-165">False</span><span class="sxs-lookup"><span data-stu-id="a679e-165">False</span></span>                             |
| <span data-ttu-id="a679e-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a679e-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="a679e-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a679e-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a679e-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a679e-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a679e-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a679e-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a679e-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a679e-170">Search-Flags</span></span>           | <span data-ttu-id="a679e-171">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a679e-171">0x00000001</span></span>                        |
| <span data-ttu-id="a679e-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a679e-172">System-Flags</span></span>           | <span data-ttu-id="a679e-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="a679e-173">0x00000011</span></span>                        |
| <span data-ttu-id="a679e-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a679e-174">Classes used in</span></span>        | [<span data-ttu-id="a679e-175">**User**</span><span class="sxs-lookup"><span data-stu-id="a679e-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a679e-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a679e-176">Windows Server 2008</span></span>



| <span data-ttu-id="a679e-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="a679e-177">Entry</span></span> | <span data-ttu-id="a679e-178">Value</span><span class="sxs-lookup"><span data-stu-id="a679e-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a679e-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a679e-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a679e-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a679e-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a679e-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="a679e-181">System-Only</span></span>            | <span data-ttu-id="a679e-182">False</span><span class="sxs-lookup"><span data-stu-id="a679e-182">False</span></span>                             |
| <span data-ttu-id="a679e-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a679e-183">Is-Single-Valued</span></span>       | <span data-ttu-id="a679e-184">True</span><span class="sxs-lookup"><span data-stu-id="a679e-184">True</span></span>                              |
| <span data-ttu-id="a679e-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a679e-185">Is Indexed</span></span>             | <span data-ttu-id="a679e-186">True</span><span class="sxs-lookup"><span data-stu-id="a679e-186">True</span></span>                              |
| <span data-ttu-id="a679e-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a679e-187">In Global Catalog</span></span>      | <span data-ttu-id="a679e-188">False</span><span class="sxs-lookup"><span data-stu-id="a679e-188">False</span></span>                             |
| <span data-ttu-id="a679e-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a679e-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="a679e-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a679e-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a679e-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a679e-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a679e-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a679e-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a679e-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a679e-193">Search-Flags</span></span>           | <span data-ttu-id="a679e-194">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a679e-194">0x00000001</span></span>                        |
| <span data-ttu-id="a679e-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a679e-195">System-Flags</span></span>           | <span data-ttu-id="a679e-196">0x00000011</span><span class="sxs-lookup"><span data-stu-id="a679e-196">0x00000011</span></span>                        |
| <span data-ttu-id="a679e-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a679e-197">Classes used in</span></span>        | [<span data-ttu-id="a679e-198">**User**</span><span class="sxs-lookup"><span data-stu-id="a679e-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a679e-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a679e-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a679e-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="a679e-200">Entry</span></span> | <span data-ttu-id="a679e-201">Value</span><span class="sxs-lookup"><span data-stu-id="a679e-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a679e-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a679e-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a679e-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a679e-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a679e-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="a679e-204">System-Only</span></span>            | <span data-ttu-id="a679e-205">False</span><span class="sxs-lookup"><span data-stu-id="a679e-205">False</span></span>                             |
| <span data-ttu-id="a679e-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a679e-206">Is-Single-Valued</span></span>       | <span data-ttu-id="a679e-207">True</span><span class="sxs-lookup"><span data-stu-id="a679e-207">True</span></span>                              |
| <span data-ttu-id="a679e-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a679e-208">Is Indexed</span></span>             | <span data-ttu-id="a679e-209">True</span><span class="sxs-lookup"><span data-stu-id="a679e-209">True</span></span>                              |
| <span data-ttu-id="a679e-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a679e-210">In Global Catalog</span></span>      | <span data-ttu-id="a679e-211">False</span><span class="sxs-lookup"><span data-stu-id="a679e-211">False</span></span>                             |
| <span data-ttu-id="a679e-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a679e-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="a679e-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a679e-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a679e-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a679e-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a679e-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a679e-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a679e-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a679e-216">Search-Flags</span></span>           | <span data-ttu-id="a679e-217">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a679e-217">0x00000001</span></span>                        |
| <span data-ttu-id="a679e-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a679e-218">System-Flags</span></span>           | <span data-ttu-id="a679e-219">0x00000011</span><span class="sxs-lookup"><span data-stu-id="a679e-219">0x00000011</span></span>                        |
| <span data-ttu-id="a679e-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a679e-220">Classes used in</span></span>        | [<span data-ttu-id="a679e-221">**User**</span><span class="sxs-lookup"><span data-stu-id="a679e-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a679e-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a679e-222">Windows Server 2012</span></span>



| <span data-ttu-id="a679e-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="a679e-223">Entry</span></span> | <span data-ttu-id="a679e-224">Value</span><span class="sxs-lookup"><span data-stu-id="a679e-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a679e-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a679e-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a679e-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a679e-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a679e-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="a679e-227">System-Only</span></span>            | <span data-ttu-id="a679e-228">False</span><span class="sxs-lookup"><span data-stu-id="a679e-228">False</span></span>                             |
| <span data-ttu-id="a679e-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a679e-229">Is-Single-Valued</span></span>       | <span data-ttu-id="a679e-230">True</span><span class="sxs-lookup"><span data-stu-id="a679e-230">True</span></span>                              |
| <span data-ttu-id="a679e-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a679e-231">Is Indexed</span></span>             | <span data-ttu-id="a679e-232">True</span><span class="sxs-lookup"><span data-stu-id="a679e-232">True</span></span>                              |
| <span data-ttu-id="a679e-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a679e-233">In Global Catalog</span></span>      | <span data-ttu-id="a679e-234">False</span><span class="sxs-lookup"><span data-stu-id="a679e-234">False</span></span>                             |
| <span data-ttu-id="a679e-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a679e-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="a679e-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a679e-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a679e-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a679e-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a679e-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a679e-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a679e-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a679e-239">Search-Flags</span></span>           | <span data-ttu-id="a679e-240">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a679e-240">0x00000001</span></span>                        |
| <span data-ttu-id="a679e-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a679e-241">System-Flags</span></span>           | <span data-ttu-id="a679e-242">0x00000011</span><span class="sxs-lookup"><span data-stu-id="a679e-242">0x00000011</span></span>                        |
| <span data-ttu-id="a679e-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a679e-243">Classes used in</span></span>        | [<span data-ttu-id="a679e-244">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="a679e-244">**User**</span></span>](c-user.md)<br/> |



 

 





