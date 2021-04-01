---
title: atributo MS-DS-site-Affinity
description: El atributo MS-DS-site-Affinity es utilizado por el administrador de cuentas de seguridad para la expansión de grupos durante la evaluación de tokens.
ms.assetid: c05df70a-adbb-48e0-bdcd-c1d83a2e43bd
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de afinidad de MS-DS-site
- msDS-site-Affinity atributo AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Site-Affinity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dd3ed17b07c73d9e7a6a2d93d93463e1dea40fc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906184"
---
# <a name="ms-ds-site-affinity-attribute"></a><span data-ttu-id="125e0-105">atributo MS-DS-site-Affinity</span><span class="sxs-lookup"><span data-stu-id="125e0-105">ms-DS-Site-Affinity attribute</span></span>

<span data-ttu-id="125e0-106">El atributo **MS-DS-site-Affinity** es utilizado por el administrador de cuentas de seguridad para la expansión de grupos durante la evaluación de tokens.</span><span class="sxs-lookup"><span data-stu-id="125e0-106">The **ms-DS-Site-Affinity** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="125e0-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="125e0-107">Entry</span></span> | <span data-ttu-id="125e0-108">Value</span><span class="sxs-lookup"><span data-stu-id="125e0-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="125e0-109">CN</span><span class="sxs-lookup"><span data-stu-id="125e0-109">CN</span></span>                | <span data-ttu-id="125e0-110">Afinidad de MS-DS-site</span><span class="sxs-lookup"><span data-stu-id="125e0-110">ms-DS-Site-Affinity</span></span>                                                                     |
| <span data-ttu-id="125e0-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="125e0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="125e0-112">msDS-site-Affinity</span><span class="sxs-lookup"><span data-stu-id="125e0-112">msDS-Site-Affinity</span></span>                                                                      |
| <span data-ttu-id="125e0-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="125e0-113">Size</span></span>              | <span data-ttu-id="125e0-114">BLOB binario de varios valores, donde cada valor es sizeof (GUID) + sizeof (entero grande \_ ).</span><span class="sxs-lookup"><span data-stu-id="125e0-114">Multiple-valued binary BLOB, where each value is sizeof(GUID) + sizeof(LARGE\_INTEGER).</span></span> |
| <span data-ttu-id="125e0-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="125e0-115">Update Privilege</span></span>  | \-                                                                                      |
| <span data-ttu-id="125e0-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="125e0-116">Update Frequency</span></span>  | <span data-ttu-id="125e0-117">De forma predeterminada, una vez cada tres meses.</span><span class="sxs-lookup"><span data-stu-id="125e0-117">By default once every three months.</span></span>                                                     |
| <span data-ttu-id="125e0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="125e0-118">Attribute-Id</span></span>      | <span data-ttu-id="125e0-119">1.2.840.113556.1.4.1443</span><span class="sxs-lookup"><span data-stu-id="125e0-119">1.2.840.113556.1.4.1443</span></span>                                                                 |
| <span data-ttu-id="125e0-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="125e0-120">System-Id-Guid</span></span>    | <span data-ttu-id="125e0-121">c17c5602-bcb7-46f0-9656-6370ca884b72</span><span class="sxs-lookup"><span data-stu-id="125e0-121">c17c5602-bcb7-46f0-9656-6370ca884b72</span></span>                                                    |
| <span data-ttu-id="125e0-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="125e0-122">Syntax</span></span>            | [<span data-ttu-id="125e0-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="125e0-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                   |



## <a name="implementations"></a><span data-ttu-id="125e0-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="125e0-124">Implementations</span></span>

-   [<span data-ttu-id="125e0-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="125e0-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="125e0-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="125e0-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="125e0-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="125e0-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="125e0-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="125e0-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="125e0-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="125e0-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="125e0-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="125e0-130">Windows Server 2003</span></span>



| <span data-ttu-id="125e0-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="125e0-131">Entry</span></span> | <span data-ttu-id="125e0-132">Value</span><span class="sxs-lookup"><span data-stu-id="125e0-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="125e0-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="125e0-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="125e0-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="125e0-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="125e0-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="125e0-135">System-Only</span></span>            | <span data-ttu-id="125e0-136">False</span><span class="sxs-lookup"><span data-stu-id="125e0-136">False</span></span>                             |
| <span data-ttu-id="125e0-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="125e0-137">Is-Single-Valued</span></span>       | <span data-ttu-id="125e0-138">False</span><span class="sxs-lookup"><span data-stu-id="125e0-138">False</span></span>                             |
| <span data-ttu-id="125e0-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="125e0-139">Is Indexed</span></span>             | <span data-ttu-id="125e0-140">True</span><span class="sxs-lookup"><span data-stu-id="125e0-140">True</span></span>                              |
| <span data-ttu-id="125e0-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="125e0-141">In Global Catalog</span></span>      | <span data-ttu-id="125e0-142">False</span><span class="sxs-lookup"><span data-stu-id="125e0-142">False</span></span>                             |
| <span data-ttu-id="125e0-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="125e0-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="125e0-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="125e0-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="125e0-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="125e0-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="125e0-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="125e0-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="125e0-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="125e0-147">Search-Flags</span></span>           | <span data-ttu-id="125e0-148">0x00000001</span><span class="sxs-lookup"><span data-stu-id="125e0-148">0x00000001</span></span>                        |
| <span data-ttu-id="125e0-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="125e0-149">System-Flags</span></span>           | <span data-ttu-id="125e0-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="125e0-150">0x00000010</span></span>                        |
| <span data-ttu-id="125e0-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="125e0-151">Classes used in</span></span>        | [<span data-ttu-id="125e0-152">**User**</span><span class="sxs-lookup"><span data-stu-id="125e0-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="125e0-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="125e0-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="125e0-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="125e0-154">Entry</span></span> | <span data-ttu-id="125e0-155">Value</span><span class="sxs-lookup"><span data-stu-id="125e0-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="125e0-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="125e0-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="125e0-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="125e0-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="125e0-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="125e0-158">System-Only</span></span>            | <span data-ttu-id="125e0-159">False</span><span class="sxs-lookup"><span data-stu-id="125e0-159">False</span></span>                             |
| <span data-ttu-id="125e0-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="125e0-160">Is-Single-Valued</span></span>       | <span data-ttu-id="125e0-161">False</span><span class="sxs-lookup"><span data-stu-id="125e0-161">False</span></span>                             |
| <span data-ttu-id="125e0-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="125e0-162">Is Indexed</span></span>             | <span data-ttu-id="125e0-163">True</span><span class="sxs-lookup"><span data-stu-id="125e0-163">True</span></span>                              |
| <span data-ttu-id="125e0-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="125e0-164">In Global Catalog</span></span>      | <span data-ttu-id="125e0-165">False</span><span class="sxs-lookup"><span data-stu-id="125e0-165">False</span></span>                             |
| <span data-ttu-id="125e0-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="125e0-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="125e0-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="125e0-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="125e0-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="125e0-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="125e0-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="125e0-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="125e0-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="125e0-170">Search-Flags</span></span>           | <span data-ttu-id="125e0-171">0x00000001</span><span class="sxs-lookup"><span data-stu-id="125e0-171">0x00000001</span></span>                        |
| <span data-ttu-id="125e0-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="125e0-172">System-Flags</span></span>           | <span data-ttu-id="125e0-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="125e0-173">0x00000010</span></span>                        |
| <span data-ttu-id="125e0-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="125e0-174">Classes used in</span></span>        | [<span data-ttu-id="125e0-175">**User**</span><span class="sxs-lookup"><span data-stu-id="125e0-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="125e0-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="125e0-176">Windows Server 2008</span></span>



| <span data-ttu-id="125e0-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="125e0-177">Entry</span></span> | <span data-ttu-id="125e0-178">Value</span><span class="sxs-lookup"><span data-stu-id="125e0-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="125e0-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="125e0-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="125e0-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="125e0-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="125e0-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="125e0-181">System-Only</span></span>            | <span data-ttu-id="125e0-182">False</span><span class="sxs-lookup"><span data-stu-id="125e0-182">False</span></span>                             |
| <span data-ttu-id="125e0-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="125e0-183">Is-Single-Valued</span></span>       | <span data-ttu-id="125e0-184">False</span><span class="sxs-lookup"><span data-stu-id="125e0-184">False</span></span>                             |
| <span data-ttu-id="125e0-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="125e0-185">Is Indexed</span></span>             | <span data-ttu-id="125e0-186">True</span><span class="sxs-lookup"><span data-stu-id="125e0-186">True</span></span>                              |
| <span data-ttu-id="125e0-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="125e0-187">In Global Catalog</span></span>      | <span data-ttu-id="125e0-188">False</span><span class="sxs-lookup"><span data-stu-id="125e0-188">False</span></span>                             |
| <span data-ttu-id="125e0-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="125e0-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="125e0-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="125e0-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="125e0-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="125e0-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="125e0-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="125e0-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="125e0-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="125e0-193">Search-Flags</span></span>           | <span data-ttu-id="125e0-194">0x00000001</span><span class="sxs-lookup"><span data-stu-id="125e0-194">0x00000001</span></span>                        |
| <span data-ttu-id="125e0-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="125e0-195">System-Flags</span></span>           | <span data-ttu-id="125e0-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="125e0-196">0x00000010</span></span>                        |
| <span data-ttu-id="125e0-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="125e0-197">Classes used in</span></span>        | [<span data-ttu-id="125e0-198">**User**</span><span class="sxs-lookup"><span data-stu-id="125e0-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="125e0-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="125e0-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="125e0-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="125e0-200">Entry</span></span> | <span data-ttu-id="125e0-201">Value</span><span class="sxs-lookup"><span data-stu-id="125e0-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="125e0-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="125e0-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="125e0-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="125e0-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="125e0-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="125e0-204">System-Only</span></span>            | <span data-ttu-id="125e0-205">False</span><span class="sxs-lookup"><span data-stu-id="125e0-205">False</span></span>                             |
| <span data-ttu-id="125e0-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="125e0-206">Is-Single-Valued</span></span>       | <span data-ttu-id="125e0-207">False</span><span class="sxs-lookup"><span data-stu-id="125e0-207">False</span></span>                             |
| <span data-ttu-id="125e0-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="125e0-208">Is Indexed</span></span>             | <span data-ttu-id="125e0-209">True</span><span class="sxs-lookup"><span data-stu-id="125e0-209">True</span></span>                              |
| <span data-ttu-id="125e0-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="125e0-210">In Global Catalog</span></span>      | <span data-ttu-id="125e0-211">False</span><span class="sxs-lookup"><span data-stu-id="125e0-211">False</span></span>                             |
| <span data-ttu-id="125e0-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="125e0-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="125e0-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="125e0-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="125e0-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="125e0-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="125e0-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="125e0-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="125e0-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="125e0-216">Search-Flags</span></span>           | <span data-ttu-id="125e0-217">0x00000001</span><span class="sxs-lookup"><span data-stu-id="125e0-217">0x00000001</span></span>                        |
| <span data-ttu-id="125e0-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="125e0-218">System-Flags</span></span>           | <span data-ttu-id="125e0-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="125e0-219">0x00000010</span></span>                        |
| <span data-ttu-id="125e0-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="125e0-220">Classes used in</span></span>        | [<span data-ttu-id="125e0-221">**User**</span><span class="sxs-lookup"><span data-stu-id="125e0-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="125e0-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="125e0-222">Windows Server 2012</span></span>



| <span data-ttu-id="125e0-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="125e0-223">Entry</span></span> | <span data-ttu-id="125e0-224">Value</span><span class="sxs-lookup"><span data-stu-id="125e0-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="125e0-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="125e0-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="125e0-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="125e0-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="125e0-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="125e0-227">System-Only</span></span>            | <span data-ttu-id="125e0-228">False</span><span class="sxs-lookup"><span data-stu-id="125e0-228">False</span></span>                             |
| <span data-ttu-id="125e0-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="125e0-229">Is-Single-Valued</span></span>       | <span data-ttu-id="125e0-230">False</span><span class="sxs-lookup"><span data-stu-id="125e0-230">False</span></span>                             |
| <span data-ttu-id="125e0-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="125e0-231">Is Indexed</span></span>             | <span data-ttu-id="125e0-232">True</span><span class="sxs-lookup"><span data-stu-id="125e0-232">True</span></span>                              |
| <span data-ttu-id="125e0-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="125e0-233">In Global Catalog</span></span>      | <span data-ttu-id="125e0-234">False</span><span class="sxs-lookup"><span data-stu-id="125e0-234">False</span></span>                             |
| <span data-ttu-id="125e0-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="125e0-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="125e0-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="125e0-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="125e0-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="125e0-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="125e0-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="125e0-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="125e0-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="125e0-239">Search-Flags</span></span>           | <span data-ttu-id="125e0-240">0x00000001</span><span class="sxs-lookup"><span data-stu-id="125e0-240">0x00000001</span></span>                        |
| <span data-ttu-id="125e0-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="125e0-241">System-Flags</span></span>           | <span data-ttu-id="125e0-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="125e0-242">0x00000010</span></span>                        |
| <span data-ttu-id="125e0-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="125e0-243">Classes used in</span></span>        | [<span data-ttu-id="125e0-244">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="125e0-244">**User**</span></span>](c-user.md)<br/> |



 

 





