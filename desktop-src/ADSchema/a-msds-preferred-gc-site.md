---
title: atributo MS-DS-Preferred-GC-site
description: El atributo MS-DS-Preferred-GC-site lo utiliza el administrador de cuentas de seguridad para la expansión de grupos durante la evaluación de tokens.
ms.assetid: f42d3787-4063-4804-a7b5-4798516ad47e
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-Preferred-GC-site
- msDS-preferido-GC-esquema de AD de atributo de sitio
topic_type:
- apiref
api_name:
- ms-DS-Preferred-GC-Site
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172e12758ba0b365fa195cb4e1384c161cea3d14
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104274577"
---
# <a name="ms-ds-preferred-gc-site-attribute"></a><span data-ttu-id="82de9-105">atributo MS-DS-Preferred-GC-site</span><span class="sxs-lookup"><span data-stu-id="82de9-105">ms-DS-Preferred-GC-Site attribute</span></span>

<span data-ttu-id="82de9-106">El atributo **MS-DS-Preferred-GC-site** lo utiliza el administrador de cuentas de seguridad para la expansión de grupos durante la evaluación de tokens.</span><span class="sxs-lookup"><span data-stu-id="82de9-106">The **ms-DS-Preferred-GC-Site** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="82de9-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="82de9-107">Entry</span></span> | <span data-ttu-id="82de9-108">Value</span><span class="sxs-lookup"><span data-stu-id="82de9-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="82de9-109">CN</span><span class="sxs-lookup"><span data-stu-id="82de9-109">CN</span></span>                | <span data-ttu-id="82de9-110">MS-DS-preferido-GC-sitio</span><span class="sxs-lookup"><span data-stu-id="82de9-110">ms-DS-Preferred-GC-Site</span></span>                 |
| <span data-ttu-id="82de9-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="82de9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="82de9-112">msDS-preferido-GC-sitio</span><span class="sxs-lookup"><span data-stu-id="82de9-112">msDS-Preferred-GC-Site</span></span>                  |
| <span data-ttu-id="82de9-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="82de9-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="82de9-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="82de9-114">Update Privilege</span></span>  | <span data-ttu-id="82de9-115">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="82de9-115">Domain administrator</span></span>                    |
| <span data-ttu-id="82de9-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="82de9-116">Update Frequency</span></span>  | <span data-ttu-id="82de9-117">A discreción del administrador.</span><span class="sxs-lookup"><span data-stu-id="82de9-117">At the administrator's discretion.</span></span>      |
| <span data-ttu-id="82de9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="82de9-118">Attribute-Id</span></span>      | <span data-ttu-id="82de9-119">1.2.840.113556.1.4.1444</span><span class="sxs-lookup"><span data-stu-id="82de9-119">1.2.840.113556.1.4.1444</span></span>                 |
| <span data-ttu-id="82de9-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="82de9-120">System-Id-Guid</span></span>    | <span data-ttu-id="82de9-121">d921b50a-0ab2-42cd-87f6-09cf83a91854</span><span class="sxs-lookup"><span data-stu-id="82de9-121">d921b50a-0ab2-42cd-87f6-09cf83a91854</span></span>    |
| <span data-ttu-id="82de9-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82de9-122">Syntax</span></span>            | [<span data-ttu-id="82de9-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="82de9-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="82de9-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="82de9-124">Implementations</span></span>

-   [<span data-ttu-id="82de9-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="82de9-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="82de9-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="82de9-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="82de9-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="82de9-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="82de9-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="82de9-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="82de9-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="82de9-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="82de9-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="82de9-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="82de9-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="82de9-131">Windows Server 2003</span></span>



| <span data-ttu-id="82de9-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="82de9-132">Entry</span></span> | <span data-ttu-id="82de9-133">Value</span><span class="sxs-lookup"><span data-stu-id="82de9-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="82de9-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="82de9-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="82de9-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82de9-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="82de9-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="82de9-136">System-Only</span></span>            | <span data-ttu-id="82de9-137">False</span><span class="sxs-lookup"><span data-stu-id="82de9-137">False</span></span>                                                       |
| <span data-ttu-id="82de9-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="82de9-138">Is-Single-Valued</span></span>       | <span data-ttu-id="82de9-139">True</span><span class="sxs-lookup"><span data-stu-id="82de9-139">True</span></span>                                                        |
| <span data-ttu-id="82de9-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="82de9-140">Is Indexed</span></span>             | <span data-ttu-id="82de9-141">False</span><span class="sxs-lookup"><span data-stu-id="82de9-141">False</span></span>                                                       |
| <span data-ttu-id="82de9-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="82de9-142">In Global Catalog</span></span>      | <span data-ttu-id="82de9-143">False</span><span class="sxs-lookup"><span data-stu-id="82de9-143">False</span></span>                                                       |
| <span data-ttu-id="82de9-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="82de9-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="82de9-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82de9-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="82de9-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82de9-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="82de9-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82de9-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="82de9-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82de9-148">Search-Flags</span></span>           | <span data-ttu-id="82de9-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82de9-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="82de9-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82de9-150">System-Flags</span></span>           | <span data-ttu-id="82de9-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82de9-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="82de9-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="82de9-152">Classes used in</span></span>        | [<span data-ttu-id="82de9-153">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="82de9-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="82de9-154">ADAM</span><span class="sxs-lookup"><span data-stu-id="82de9-154">ADAM</span></span>



| <span data-ttu-id="82de9-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="82de9-155">Entry</span></span> | <span data-ttu-id="82de9-156">Value</span><span class="sxs-lookup"><span data-stu-id="82de9-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="82de9-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="82de9-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="82de9-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82de9-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="82de9-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="82de9-159">System-Only</span></span>            | <span data-ttu-id="82de9-160">False</span><span class="sxs-lookup"><span data-stu-id="82de9-160">False</span></span>                                                       |
| <span data-ttu-id="82de9-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="82de9-161">Is-Single-Valued</span></span>       | <span data-ttu-id="82de9-162">True</span><span class="sxs-lookup"><span data-stu-id="82de9-162">True</span></span>                                                        |
| <span data-ttu-id="82de9-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="82de9-163">Is Indexed</span></span>             | <span data-ttu-id="82de9-164">False</span><span class="sxs-lookup"><span data-stu-id="82de9-164">False</span></span>                                                       |
| <span data-ttu-id="82de9-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="82de9-165">In Global Catalog</span></span>      | <span data-ttu-id="82de9-166">False</span><span class="sxs-lookup"><span data-stu-id="82de9-166">False</span></span>                                                       |
| <span data-ttu-id="82de9-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="82de9-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="82de9-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82de9-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="82de9-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82de9-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="82de9-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82de9-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="82de9-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82de9-171">Search-Flags</span></span>           | <span data-ttu-id="82de9-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82de9-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="82de9-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82de9-173">System-Flags</span></span>           | <span data-ttu-id="82de9-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82de9-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="82de9-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="82de9-175">Classes used in</span></span>        | [<span data-ttu-id="82de9-176">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="82de9-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="82de9-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="82de9-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="82de9-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="82de9-178">Entry</span></span> | <span data-ttu-id="82de9-179">Value</span><span class="sxs-lookup"><span data-stu-id="82de9-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="82de9-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="82de9-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="82de9-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82de9-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="82de9-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="82de9-182">System-Only</span></span>            | <span data-ttu-id="82de9-183">False</span><span class="sxs-lookup"><span data-stu-id="82de9-183">False</span></span>                                                       |
| <span data-ttu-id="82de9-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="82de9-184">Is-Single-Valued</span></span>       | <span data-ttu-id="82de9-185">True</span><span class="sxs-lookup"><span data-stu-id="82de9-185">True</span></span>                                                        |
| <span data-ttu-id="82de9-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="82de9-186">Is Indexed</span></span>             | <span data-ttu-id="82de9-187">False</span><span class="sxs-lookup"><span data-stu-id="82de9-187">False</span></span>                                                       |
| <span data-ttu-id="82de9-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="82de9-188">In Global Catalog</span></span>      | <span data-ttu-id="82de9-189">False</span><span class="sxs-lookup"><span data-stu-id="82de9-189">False</span></span>                                                       |
| <span data-ttu-id="82de9-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="82de9-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="82de9-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82de9-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="82de9-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82de9-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="82de9-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82de9-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="82de9-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82de9-194">Search-Flags</span></span>           | <span data-ttu-id="82de9-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82de9-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="82de9-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82de9-196">System-Flags</span></span>           | <span data-ttu-id="82de9-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82de9-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="82de9-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="82de9-198">Classes used in</span></span>        | [<span data-ttu-id="82de9-199">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="82de9-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="82de9-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82de9-200">Windows Server 2008</span></span>



| <span data-ttu-id="82de9-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="82de9-201">Entry</span></span> | <span data-ttu-id="82de9-202">Value</span><span class="sxs-lookup"><span data-stu-id="82de9-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="82de9-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="82de9-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="82de9-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82de9-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="82de9-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="82de9-205">System-Only</span></span>            | <span data-ttu-id="82de9-206">False</span><span class="sxs-lookup"><span data-stu-id="82de9-206">False</span></span>                                                       |
| <span data-ttu-id="82de9-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="82de9-207">Is-Single-Valued</span></span>       | <span data-ttu-id="82de9-208">True</span><span class="sxs-lookup"><span data-stu-id="82de9-208">True</span></span>                                                        |
| <span data-ttu-id="82de9-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="82de9-209">Is Indexed</span></span>             | <span data-ttu-id="82de9-210">False</span><span class="sxs-lookup"><span data-stu-id="82de9-210">False</span></span>                                                       |
| <span data-ttu-id="82de9-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="82de9-211">In Global Catalog</span></span>      | <span data-ttu-id="82de9-212">False</span><span class="sxs-lookup"><span data-stu-id="82de9-212">False</span></span>                                                       |
| <span data-ttu-id="82de9-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="82de9-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="82de9-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82de9-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="82de9-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82de9-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="82de9-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82de9-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="82de9-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82de9-217">Search-Flags</span></span>           | <span data-ttu-id="82de9-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82de9-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="82de9-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82de9-219">System-Flags</span></span>           | <span data-ttu-id="82de9-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82de9-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="82de9-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="82de9-221">Classes used in</span></span>        | [<span data-ttu-id="82de9-222">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="82de9-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="82de9-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="82de9-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="82de9-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="82de9-224">Entry</span></span> | <span data-ttu-id="82de9-225">Value</span><span class="sxs-lookup"><span data-stu-id="82de9-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="82de9-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="82de9-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="82de9-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82de9-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="82de9-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="82de9-228">System-Only</span></span>            | <span data-ttu-id="82de9-229">False</span><span class="sxs-lookup"><span data-stu-id="82de9-229">False</span></span>                                                       |
| <span data-ttu-id="82de9-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="82de9-230">Is-Single-Valued</span></span>       | <span data-ttu-id="82de9-231">True</span><span class="sxs-lookup"><span data-stu-id="82de9-231">True</span></span>                                                        |
| <span data-ttu-id="82de9-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="82de9-232">Is Indexed</span></span>             | <span data-ttu-id="82de9-233">False</span><span class="sxs-lookup"><span data-stu-id="82de9-233">False</span></span>                                                       |
| <span data-ttu-id="82de9-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="82de9-234">In Global Catalog</span></span>      | <span data-ttu-id="82de9-235">False</span><span class="sxs-lookup"><span data-stu-id="82de9-235">False</span></span>                                                       |
| <span data-ttu-id="82de9-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="82de9-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="82de9-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82de9-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="82de9-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82de9-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="82de9-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82de9-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="82de9-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82de9-240">Search-Flags</span></span>           | <span data-ttu-id="82de9-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82de9-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="82de9-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82de9-242">System-Flags</span></span>           | <span data-ttu-id="82de9-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82de9-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="82de9-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="82de9-244">Classes used in</span></span>        | [<span data-ttu-id="82de9-245">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="82de9-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="82de9-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="82de9-246">Windows Server 2012</span></span>



| <span data-ttu-id="82de9-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="82de9-247">Entry</span></span> | <span data-ttu-id="82de9-248">Value</span><span class="sxs-lookup"><span data-stu-id="82de9-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="82de9-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="82de9-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="82de9-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82de9-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="82de9-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="82de9-251">System-Only</span></span>            | <span data-ttu-id="82de9-252">False</span><span class="sxs-lookup"><span data-stu-id="82de9-252">False</span></span>                                                       |
| <span data-ttu-id="82de9-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="82de9-253">Is-Single-Valued</span></span>       | <span data-ttu-id="82de9-254">True</span><span class="sxs-lookup"><span data-stu-id="82de9-254">True</span></span>                                                        |
| <span data-ttu-id="82de9-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="82de9-255">Is Indexed</span></span>             | <span data-ttu-id="82de9-256">False</span><span class="sxs-lookup"><span data-stu-id="82de9-256">False</span></span>                                                       |
| <span data-ttu-id="82de9-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="82de9-257">In Global Catalog</span></span>      | <span data-ttu-id="82de9-258">False</span><span class="sxs-lookup"><span data-stu-id="82de9-258">False</span></span>                                                       |
| <span data-ttu-id="82de9-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="82de9-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="82de9-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82de9-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="82de9-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82de9-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="82de9-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82de9-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="82de9-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82de9-263">Search-Flags</span></span>           | <span data-ttu-id="82de9-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82de9-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="82de9-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82de9-265">System-Flags</span></span>           | <span data-ttu-id="82de9-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82de9-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="82de9-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="82de9-267">Classes used in</span></span>        | [<span data-ttu-id="82de9-268">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="82de9-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





