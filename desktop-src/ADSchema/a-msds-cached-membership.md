---
title: atributo MS-DS-Cached-Membership
description: El atributo MS-DS-Cached-Membership se usa en el administrador de cuentas de seguridad para la expansión de grupos durante la evaluación de tokens.
ms.assetid: e54c5d55-d292-4a6e-942a-3818f5d75301
ms.tgt_platform: multiple
keywords:
- 'MS-DS-Cached: esquema de AD de atributo de pertenencia'
- 'msDS-Cached: esquema de AD de atributo de pertenencia'
topic_type:
- apiref
api_name:
- ms-DS-Cached-Membership
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 936c5c21d33d19ee51dba7f1dec0b03299cee346
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536280"
---
# <a name="ms-ds-cached-membership-attribute"></a><span data-ttu-id="198ad-105">atributo MS-DS-Cached-Membership</span><span class="sxs-lookup"><span data-stu-id="198ad-105">ms-DS-Cached-Membership attribute</span></span>

<span data-ttu-id="198ad-106">El atributo **MS-DS-Cached-Membership** se usa en el administrador de cuentas de seguridad para la expansión de grupos durante la evaluación de tokens.</span><span class="sxs-lookup"><span data-stu-id="198ad-106">The **ms-DS-Cached-Membership** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="198ad-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="198ad-107">Entry</span></span> | <span data-ttu-id="198ad-108">Value</span><span class="sxs-lookup"><span data-stu-id="198ad-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="198ad-109">CN</span><span class="sxs-lookup"><span data-stu-id="198ad-109">CN</span></span>                | <span data-ttu-id="198ad-110">MS-DS-en caché-pertenencia</span><span class="sxs-lookup"><span data-stu-id="198ad-110">ms-DS-Cached-Membership</span></span>                               |
| <span data-ttu-id="198ad-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="198ad-111">Ldap-Display-Name</span></span> | <span data-ttu-id="198ad-112">msDS: pertenencia a la caché</span><span class="sxs-lookup"><span data-stu-id="198ad-112">msDS-Cached-Membership</span></span>                                |
| <span data-ttu-id="198ad-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="198ad-113">Size</span></span>              | <span data-ttu-id="198ad-114">BLOB binario de hasta 3 kilobytes.</span><span class="sxs-lookup"><span data-stu-id="198ad-114">Binary BLOB of up to 3 kilobytes.</span></span>                     |
| <span data-ttu-id="198ad-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="198ad-115">Update Privilege</span></span>  | <span data-ttu-id="198ad-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="198ad-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="198ad-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="198ad-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="198ad-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="198ad-118">Attribute-Id</span></span>      | <span data-ttu-id="198ad-119">1.2.840.113556.1.4.1441</span><span class="sxs-lookup"><span data-stu-id="198ad-119">1.2.840.113556.1.4.1441</span></span>                               |
| <span data-ttu-id="198ad-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="198ad-120">System-Id-Guid</span></span>    | <span data-ttu-id="198ad-121">69cab008-cdd4-4bc9-bab8-0ff37efe1b20</span><span class="sxs-lookup"><span data-stu-id="198ad-121">69cab008-cdd4-4bc9-bab8-0ff37efe1b20</span></span>                  |
| <span data-ttu-id="198ad-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="198ad-122">Syntax</span></span>            | [<span data-ttu-id="198ad-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="198ad-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="198ad-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="198ad-124">Implementations</span></span>

-   [<span data-ttu-id="198ad-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="198ad-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="198ad-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="198ad-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="198ad-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="198ad-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="198ad-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="198ad-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="198ad-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="198ad-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="198ad-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="198ad-130">Windows Server 2003</span></span>



| <span data-ttu-id="198ad-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="198ad-131">Entry</span></span> | <span data-ttu-id="198ad-132">Value</span><span class="sxs-lookup"><span data-stu-id="198ad-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="198ad-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="198ad-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="198ad-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="198ad-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="198ad-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="198ad-135">System-Only</span></span>            | <span data-ttu-id="198ad-136">False</span><span class="sxs-lookup"><span data-stu-id="198ad-136">False</span></span>                             |
| <span data-ttu-id="198ad-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="198ad-137">Is-Single-Valued</span></span>       | <span data-ttu-id="198ad-138">True</span><span class="sxs-lookup"><span data-stu-id="198ad-138">True</span></span>                              |
| <span data-ttu-id="198ad-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="198ad-139">Is Indexed</span></span>             | <span data-ttu-id="198ad-140">False</span><span class="sxs-lookup"><span data-stu-id="198ad-140">False</span></span>                             |
| <span data-ttu-id="198ad-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="198ad-141">In Global Catalog</span></span>      | <span data-ttu-id="198ad-142">False</span><span class="sxs-lookup"><span data-stu-id="198ad-142">False</span></span>                             |
| <span data-ttu-id="198ad-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="198ad-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="198ad-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="198ad-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="198ad-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="198ad-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="198ad-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="198ad-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="198ad-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="198ad-147">Search-Flags</span></span>           | <span data-ttu-id="198ad-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="198ad-148">0x00000000</span></span>                        |
| <span data-ttu-id="198ad-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="198ad-149">System-Flags</span></span>           | <span data-ttu-id="198ad-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="198ad-150">0x00000011</span></span>                        |
| <span data-ttu-id="198ad-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="198ad-151">Classes used in</span></span>        | [<span data-ttu-id="198ad-152">**User**</span><span class="sxs-lookup"><span data-stu-id="198ad-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="198ad-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="198ad-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="198ad-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="198ad-154">Entry</span></span> | <span data-ttu-id="198ad-155">Value</span><span class="sxs-lookup"><span data-stu-id="198ad-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="198ad-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="198ad-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="198ad-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="198ad-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="198ad-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="198ad-158">System-Only</span></span>            | <span data-ttu-id="198ad-159">False</span><span class="sxs-lookup"><span data-stu-id="198ad-159">False</span></span>                             |
| <span data-ttu-id="198ad-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="198ad-160">Is-Single-Valued</span></span>       | <span data-ttu-id="198ad-161">True</span><span class="sxs-lookup"><span data-stu-id="198ad-161">True</span></span>                              |
| <span data-ttu-id="198ad-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="198ad-162">Is Indexed</span></span>             | <span data-ttu-id="198ad-163">False</span><span class="sxs-lookup"><span data-stu-id="198ad-163">False</span></span>                             |
| <span data-ttu-id="198ad-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="198ad-164">In Global Catalog</span></span>      | <span data-ttu-id="198ad-165">False</span><span class="sxs-lookup"><span data-stu-id="198ad-165">False</span></span>                             |
| <span data-ttu-id="198ad-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="198ad-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="198ad-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="198ad-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="198ad-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="198ad-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="198ad-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="198ad-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="198ad-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="198ad-170">Search-Flags</span></span>           | <span data-ttu-id="198ad-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="198ad-171">0x00000000</span></span>                        |
| <span data-ttu-id="198ad-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="198ad-172">System-Flags</span></span>           | <span data-ttu-id="198ad-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="198ad-173">0x00000011</span></span>                        |
| <span data-ttu-id="198ad-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="198ad-174">Classes used in</span></span>        | [<span data-ttu-id="198ad-175">**User**</span><span class="sxs-lookup"><span data-stu-id="198ad-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="198ad-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="198ad-176">Windows Server 2008</span></span>



| <span data-ttu-id="198ad-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="198ad-177">Entry</span></span> | <span data-ttu-id="198ad-178">Value</span><span class="sxs-lookup"><span data-stu-id="198ad-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="198ad-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="198ad-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="198ad-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="198ad-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="198ad-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="198ad-181">System-Only</span></span>            | <span data-ttu-id="198ad-182">False</span><span class="sxs-lookup"><span data-stu-id="198ad-182">False</span></span>                             |
| <span data-ttu-id="198ad-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="198ad-183">Is-Single-Valued</span></span>       | <span data-ttu-id="198ad-184">True</span><span class="sxs-lookup"><span data-stu-id="198ad-184">True</span></span>                              |
| <span data-ttu-id="198ad-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="198ad-185">Is Indexed</span></span>             | <span data-ttu-id="198ad-186">False</span><span class="sxs-lookup"><span data-stu-id="198ad-186">False</span></span>                             |
| <span data-ttu-id="198ad-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="198ad-187">In Global Catalog</span></span>      | <span data-ttu-id="198ad-188">False</span><span class="sxs-lookup"><span data-stu-id="198ad-188">False</span></span>                             |
| <span data-ttu-id="198ad-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="198ad-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="198ad-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="198ad-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="198ad-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="198ad-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="198ad-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="198ad-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="198ad-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="198ad-193">Search-Flags</span></span>           | <span data-ttu-id="198ad-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="198ad-194">0x00000000</span></span>                        |
| <span data-ttu-id="198ad-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="198ad-195">System-Flags</span></span>           | <span data-ttu-id="198ad-196">0x00000011</span><span class="sxs-lookup"><span data-stu-id="198ad-196">0x00000011</span></span>                        |
| <span data-ttu-id="198ad-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="198ad-197">Classes used in</span></span>        | [<span data-ttu-id="198ad-198">**User**</span><span class="sxs-lookup"><span data-stu-id="198ad-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="198ad-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="198ad-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="198ad-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="198ad-200">Entry</span></span> | <span data-ttu-id="198ad-201">Value</span><span class="sxs-lookup"><span data-stu-id="198ad-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="198ad-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="198ad-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="198ad-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="198ad-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="198ad-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="198ad-204">System-Only</span></span>            | <span data-ttu-id="198ad-205">False</span><span class="sxs-lookup"><span data-stu-id="198ad-205">False</span></span>                             |
| <span data-ttu-id="198ad-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="198ad-206">Is-Single-Valued</span></span>       | <span data-ttu-id="198ad-207">True</span><span class="sxs-lookup"><span data-stu-id="198ad-207">True</span></span>                              |
| <span data-ttu-id="198ad-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="198ad-208">Is Indexed</span></span>             | <span data-ttu-id="198ad-209">False</span><span class="sxs-lookup"><span data-stu-id="198ad-209">False</span></span>                             |
| <span data-ttu-id="198ad-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="198ad-210">In Global Catalog</span></span>      | <span data-ttu-id="198ad-211">False</span><span class="sxs-lookup"><span data-stu-id="198ad-211">False</span></span>                             |
| <span data-ttu-id="198ad-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="198ad-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="198ad-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="198ad-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="198ad-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="198ad-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="198ad-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="198ad-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="198ad-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="198ad-216">Search-Flags</span></span>           | <span data-ttu-id="198ad-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="198ad-217">0x00000000</span></span>                        |
| <span data-ttu-id="198ad-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="198ad-218">System-Flags</span></span>           | <span data-ttu-id="198ad-219">0x00000011</span><span class="sxs-lookup"><span data-stu-id="198ad-219">0x00000011</span></span>                        |
| <span data-ttu-id="198ad-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="198ad-220">Classes used in</span></span>        | [<span data-ttu-id="198ad-221">**User**</span><span class="sxs-lookup"><span data-stu-id="198ad-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="198ad-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="198ad-222">Windows Server 2012</span></span>



| <span data-ttu-id="198ad-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="198ad-223">Entry</span></span> | <span data-ttu-id="198ad-224">Value</span><span class="sxs-lookup"><span data-stu-id="198ad-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="198ad-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="198ad-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="198ad-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="198ad-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="198ad-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="198ad-227">System-Only</span></span>            | <span data-ttu-id="198ad-228">False</span><span class="sxs-lookup"><span data-stu-id="198ad-228">False</span></span>                             |
| <span data-ttu-id="198ad-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="198ad-229">Is-Single-Valued</span></span>       | <span data-ttu-id="198ad-230">True</span><span class="sxs-lookup"><span data-stu-id="198ad-230">True</span></span>                              |
| <span data-ttu-id="198ad-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="198ad-231">Is Indexed</span></span>             | <span data-ttu-id="198ad-232">False</span><span class="sxs-lookup"><span data-stu-id="198ad-232">False</span></span>                             |
| <span data-ttu-id="198ad-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="198ad-233">In Global Catalog</span></span>      | <span data-ttu-id="198ad-234">False</span><span class="sxs-lookup"><span data-stu-id="198ad-234">False</span></span>                             |
| <span data-ttu-id="198ad-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="198ad-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="198ad-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="198ad-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="198ad-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="198ad-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="198ad-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="198ad-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="198ad-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="198ad-239">Search-Flags</span></span>           | <span data-ttu-id="198ad-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="198ad-240">0x00000000</span></span>                        |
| <span data-ttu-id="198ad-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="198ad-241">System-Flags</span></span>           | <span data-ttu-id="198ad-242">0x00000011</span><span class="sxs-lookup"><span data-stu-id="198ad-242">0x00000011</span></span>                        |
| <span data-ttu-id="198ad-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="198ad-243">Classes used in</span></span>        | [<span data-ttu-id="198ad-244">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="198ad-244">**User**</span></span>](c-user.md)<br/> |



 

 





