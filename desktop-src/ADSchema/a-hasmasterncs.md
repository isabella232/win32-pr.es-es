---
title: Tiene el atributo-Master-NC
description: Nombre distintivo para los contextos de nomenclatura del controlador de dominio. Vínculo hacia delante del atributo de Mastered-By.
ms.assetid: 77a7e693-513f-4f76-8c4f-d2ef3240323b
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo tiene-Master-NC
- hasMasterNCs esquema de AD de atributos
topic_type:
- apiref
api_name:
- Has-Master-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34756c491c5228c58da1b95d4fd7b838c691f38
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997474"
---
# <a name="has-master-ncs-attribute"></a><span data-ttu-id="1fcc1-106">Tiene el atributo-Master-NC</span><span class="sxs-lookup"><span data-stu-id="1fcc1-106">Has-Master-NCs attribute</span></span>

<span data-ttu-id="1fcc1-107">Nombre distintivo para los contextos de nomenclatura del controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="1fcc1-107">The distinguished name for the naming contexts for the DC.</span></span> <span data-ttu-id="1fcc1-108">Vínculo hacia delante del atributo de Mastered-By.</span><span class="sxs-lookup"><span data-stu-id="1fcc1-108">Forward link for the Mastered-By attribute.</span></span>



| <span data-ttu-id="1fcc1-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="1fcc1-109">Entry</span></span> | <span data-ttu-id="1fcc1-110">Value</span><span class="sxs-lookup"><span data-stu-id="1fcc1-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="1fcc1-111">CN</span><span class="sxs-lookup"><span data-stu-id="1fcc1-111">CN</span></span>                | <span data-ttu-id="1fcc1-112">Tiene-Master-NC</span><span class="sxs-lookup"><span data-stu-id="1fcc1-112">Has-Master-NCs</span></span>                          |
| <span data-ttu-id="1fcc1-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="1fcc1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1fcc1-114">hasMasterNCs</span><span class="sxs-lookup"><span data-stu-id="1fcc1-114">hasMasterNCs</span></span>                            |
| <span data-ttu-id="1fcc1-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="1fcc1-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="1fcc1-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="1fcc1-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="1fcc1-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="1fcc1-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="1fcc1-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1fcc1-118">Attribute-Id</span></span>      | <span data-ttu-id="1fcc1-119">1.2.840.113556.1.2.14</span><span class="sxs-lookup"><span data-stu-id="1fcc1-119">1.2.840.113556.1.2.14</span></span>                   |
| <span data-ttu-id="1fcc1-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1fcc1-120">System-Id-Guid</span></span>    | <span data-ttu-id="1fcc1-121">bf967982-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1fcc1-121">bf967982-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="1fcc1-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1fcc1-122">Syntax</span></span>            | [<span data-ttu-id="1fcc1-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="1fcc1-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="1fcc1-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="1fcc1-124">Implementations</span></span>

-   [<span data-ttu-id="1fcc1-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1fcc1-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1fcc1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1fcc1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1fcc1-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1fcc1-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1fcc1-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1fcc1-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1fcc1-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1fcc1-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1fcc1-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1fcc1-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1fcc1-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1fcc1-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1fcc1-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1fcc1-132">Windows 2000 Server</span></span>



| <span data-ttu-id="1fcc1-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="1fcc1-133">Entry</span></span> | <span data-ttu-id="1fcc1-134">Value</span><span class="sxs-lookup"><span data-stu-id="1fcc1-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="1fcc1-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1fcc1-135">Link-Id</span></span>                | <span data-ttu-id="1fcc1-136">76</span><span class="sxs-lookup"><span data-stu-id="1fcc1-136">76</span></span>                                       |
| <span data-ttu-id="1fcc1-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fcc1-137">MAPI-Id</span></span>                | <span data-ttu-id="1fcc1-138">0x80B6</span><span class="sxs-lookup"><span data-stu-id="1fcc1-138">0x80B6</span></span>                                   |
| <span data-ttu-id="1fcc1-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fcc1-139">System-Only</span></span>            | <span data-ttu-id="1fcc1-140">True</span><span class="sxs-lookup"><span data-stu-id="1fcc1-140">True</span></span>                                     |
| <span data-ttu-id="1fcc1-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1fcc1-141">Is-Single-Valued</span></span>       | <span data-ttu-id="1fcc1-142">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-142">False</span></span>                                    |
| <span data-ttu-id="1fcc1-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1fcc1-143">Is Indexed</span></span>             | <span data-ttu-id="1fcc1-144">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-144">False</span></span>                                    |
| <span data-ttu-id="1fcc1-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1fcc1-145">In Global Catalog</span></span>      | <span data-ttu-id="1fcc1-146">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-146">False</span></span>                                    |
| <span data-ttu-id="1fcc1-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1fcc1-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fcc1-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1fcc1-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="1fcc1-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fcc1-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="1fcc1-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fcc1-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="1fcc1-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fcc1-151">Search-Flags</span></span>           | <span data-ttu-id="1fcc1-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fcc1-152">0x00000000</span></span>                               |
| <span data-ttu-id="1fcc1-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fcc1-153">System-Flags</span></span>           | <span data-ttu-id="1fcc1-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fcc1-154">0x00000010</span></span>                               |
| <span data-ttu-id="1fcc1-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1fcc1-155">Classes used in</span></span>        | [<span data-ttu-id="1fcc1-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="1fcc1-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1fcc1-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1fcc1-157">Windows Server 2003</span></span>



| <span data-ttu-id="1fcc1-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="1fcc1-158">Entry</span></span> | <span data-ttu-id="1fcc1-159">Value</span><span class="sxs-lookup"><span data-stu-id="1fcc1-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="1fcc1-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1fcc1-160">Link-Id</span></span>                | <span data-ttu-id="1fcc1-161">76</span><span class="sxs-lookup"><span data-stu-id="1fcc1-161">76</span></span>                                       |
| <span data-ttu-id="1fcc1-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fcc1-162">MAPI-Id</span></span>                | <span data-ttu-id="1fcc1-163">0x80B6</span><span class="sxs-lookup"><span data-stu-id="1fcc1-163">0x80B6</span></span>                                   |
| <span data-ttu-id="1fcc1-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fcc1-164">System-Only</span></span>            | <span data-ttu-id="1fcc1-165">True</span><span class="sxs-lookup"><span data-stu-id="1fcc1-165">True</span></span>                                     |
| <span data-ttu-id="1fcc1-166">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1fcc1-166">Is-Single-Valued</span></span>       | <span data-ttu-id="1fcc1-167">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-167">False</span></span>                                    |
| <span data-ttu-id="1fcc1-168">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1fcc1-168">Is Indexed</span></span>             | <span data-ttu-id="1fcc1-169">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-169">False</span></span>                                    |
| <span data-ttu-id="1fcc1-170">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1fcc1-170">In Global Catalog</span></span>      | <span data-ttu-id="1fcc1-171">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-171">False</span></span>                                    |
| <span data-ttu-id="1fcc1-172">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1fcc1-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fcc1-173">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1fcc1-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="1fcc1-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fcc1-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="1fcc1-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fcc1-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="1fcc1-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fcc1-176">Search-Flags</span></span>           | <span data-ttu-id="1fcc1-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fcc1-177">0x00000000</span></span>                               |
| <span data-ttu-id="1fcc1-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fcc1-178">System-Flags</span></span>           | <span data-ttu-id="1fcc1-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fcc1-179">0x00000010</span></span>                               |
| <span data-ttu-id="1fcc1-180">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1fcc1-180">Classes used in</span></span>        | [<span data-ttu-id="1fcc1-181">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="1fcc1-181">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1fcc1-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="1fcc1-182">ADAM</span></span>



| <span data-ttu-id="1fcc1-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="1fcc1-183">Entry</span></span> | <span data-ttu-id="1fcc1-184">Value</span><span class="sxs-lookup"><span data-stu-id="1fcc1-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="1fcc1-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1fcc1-185">Link-Id</span></span>                | <span data-ttu-id="1fcc1-186">76</span><span class="sxs-lookup"><span data-stu-id="1fcc1-186">76</span></span>                                       |
| <span data-ttu-id="1fcc1-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fcc1-187">MAPI-Id</span></span>                | <span data-ttu-id="1fcc1-188">0x80B6</span><span class="sxs-lookup"><span data-stu-id="1fcc1-188">0x80B6</span></span>                                   |
| <span data-ttu-id="1fcc1-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fcc1-189">System-Only</span></span>            | <span data-ttu-id="1fcc1-190">True</span><span class="sxs-lookup"><span data-stu-id="1fcc1-190">True</span></span>                                     |
| <span data-ttu-id="1fcc1-191">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1fcc1-191">Is-Single-Valued</span></span>       | <span data-ttu-id="1fcc1-192">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-192">False</span></span>                                    |
| <span data-ttu-id="1fcc1-193">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1fcc1-193">Is Indexed</span></span>             | <span data-ttu-id="1fcc1-194">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-194">False</span></span>                                    |
| <span data-ttu-id="1fcc1-195">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1fcc1-195">In Global Catalog</span></span>      | <span data-ttu-id="1fcc1-196">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-196">False</span></span>                                    |
| <span data-ttu-id="1fcc1-197">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1fcc1-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fcc1-198">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1fcc1-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="1fcc1-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fcc1-199">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="1fcc1-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fcc1-200">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="1fcc1-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fcc1-201">Search-Flags</span></span>           | <span data-ttu-id="1fcc1-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fcc1-202">0x00000000</span></span>                               |
| <span data-ttu-id="1fcc1-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fcc1-203">System-Flags</span></span>           | <span data-ttu-id="1fcc1-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fcc1-204">0x00000010</span></span>                               |
| <span data-ttu-id="1fcc1-205">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1fcc1-205">Classes used in</span></span>        | [<span data-ttu-id="1fcc1-206">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="1fcc1-206">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1fcc1-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1fcc1-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1fcc1-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="1fcc1-208">Entry</span></span> | <span data-ttu-id="1fcc1-209">Value</span><span class="sxs-lookup"><span data-stu-id="1fcc1-209">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="1fcc1-210">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1fcc1-210">Link-Id</span></span>                | <span data-ttu-id="1fcc1-211">76</span><span class="sxs-lookup"><span data-stu-id="1fcc1-211">76</span></span>                                       |
| <span data-ttu-id="1fcc1-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fcc1-212">MAPI-Id</span></span>                | <span data-ttu-id="1fcc1-213">0x80B6</span><span class="sxs-lookup"><span data-stu-id="1fcc1-213">0x80B6</span></span>                                   |
| <span data-ttu-id="1fcc1-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fcc1-214">System-Only</span></span>            | <span data-ttu-id="1fcc1-215">True</span><span class="sxs-lookup"><span data-stu-id="1fcc1-215">True</span></span>                                     |
| <span data-ttu-id="1fcc1-216">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1fcc1-216">Is-Single-Valued</span></span>       | <span data-ttu-id="1fcc1-217">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-217">False</span></span>                                    |
| <span data-ttu-id="1fcc1-218">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1fcc1-218">Is Indexed</span></span>             | <span data-ttu-id="1fcc1-219">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-219">False</span></span>                                    |
| <span data-ttu-id="1fcc1-220">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1fcc1-220">In Global Catalog</span></span>      | <span data-ttu-id="1fcc1-221">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-221">False</span></span>                                    |
| <span data-ttu-id="1fcc1-222">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1fcc1-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fcc1-223">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1fcc1-223">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="1fcc1-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fcc1-224">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="1fcc1-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fcc1-225">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="1fcc1-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fcc1-226">Search-Flags</span></span>           | <span data-ttu-id="1fcc1-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fcc1-227">0x00000000</span></span>                               |
| <span data-ttu-id="1fcc1-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fcc1-228">System-Flags</span></span>           | <span data-ttu-id="1fcc1-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fcc1-229">0x00000010</span></span>                               |
| <span data-ttu-id="1fcc1-230">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1fcc1-230">Classes used in</span></span>        | [<span data-ttu-id="1fcc1-231">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="1fcc1-231">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1fcc1-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fcc1-232">Windows Server 2008</span></span>



| <span data-ttu-id="1fcc1-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="1fcc1-233">Entry</span></span> | <span data-ttu-id="1fcc1-234">Value</span><span class="sxs-lookup"><span data-stu-id="1fcc1-234">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="1fcc1-235">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1fcc1-235">Link-Id</span></span>                | <span data-ttu-id="1fcc1-236">76</span><span class="sxs-lookup"><span data-stu-id="1fcc1-236">76</span></span>                                       |
| <span data-ttu-id="1fcc1-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fcc1-237">MAPI-Id</span></span>                | <span data-ttu-id="1fcc1-238">0x80B6</span><span class="sxs-lookup"><span data-stu-id="1fcc1-238">0x80B6</span></span>                                   |
| <span data-ttu-id="1fcc1-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fcc1-239">System-Only</span></span>            | <span data-ttu-id="1fcc1-240">True</span><span class="sxs-lookup"><span data-stu-id="1fcc1-240">True</span></span>                                     |
| <span data-ttu-id="1fcc1-241">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1fcc1-241">Is-Single-Valued</span></span>       | <span data-ttu-id="1fcc1-242">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-242">False</span></span>                                    |
| <span data-ttu-id="1fcc1-243">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1fcc1-243">Is Indexed</span></span>             | <span data-ttu-id="1fcc1-244">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-244">False</span></span>                                    |
| <span data-ttu-id="1fcc1-245">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1fcc1-245">In Global Catalog</span></span>      | <span data-ttu-id="1fcc1-246">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-246">False</span></span>                                    |
| <span data-ttu-id="1fcc1-247">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1fcc1-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fcc1-248">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1fcc1-248">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="1fcc1-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fcc1-249">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="1fcc1-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fcc1-250">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="1fcc1-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fcc1-251">Search-Flags</span></span>           | <span data-ttu-id="1fcc1-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fcc1-252">0x00000000</span></span>                               |
| <span data-ttu-id="1fcc1-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fcc1-253">System-Flags</span></span>           | <span data-ttu-id="1fcc1-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fcc1-254">0x00000010</span></span>                               |
| <span data-ttu-id="1fcc1-255">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1fcc1-255">Classes used in</span></span>        | [<span data-ttu-id="1fcc1-256">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="1fcc1-256">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1fcc1-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1fcc1-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1fcc1-258">Entrada</span><span class="sxs-lookup"><span data-stu-id="1fcc1-258">Entry</span></span> | <span data-ttu-id="1fcc1-259">Value</span><span class="sxs-lookup"><span data-stu-id="1fcc1-259">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="1fcc1-260">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1fcc1-260">Link-Id</span></span>                | <span data-ttu-id="1fcc1-261">76</span><span class="sxs-lookup"><span data-stu-id="1fcc1-261">76</span></span>                                       |
| <span data-ttu-id="1fcc1-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fcc1-262">MAPI-Id</span></span>                | <span data-ttu-id="1fcc1-263">0x80B6</span><span class="sxs-lookup"><span data-stu-id="1fcc1-263">0x80B6</span></span>                                   |
| <span data-ttu-id="1fcc1-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fcc1-264">System-Only</span></span>            | <span data-ttu-id="1fcc1-265">True</span><span class="sxs-lookup"><span data-stu-id="1fcc1-265">True</span></span>                                     |
| <span data-ttu-id="1fcc1-266">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1fcc1-266">Is-Single-Valued</span></span>       | <span data-ttu-id="1fcc1-267">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-267">False</span></span>                                    |
| <span data-ttu-id="1fcc1-268">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1fcc1-268">Is Indexed</span></span>             | <span data-ttu-id="1fcc1-269">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-269">False</span></span>                                    |
| <span data-ttu-id="1fcc1-270">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1fcc1-270">In Global Catalog</span></span>      | <span data-ttu-id="1fcc1-271">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-271">False</span></span>                                    |
| <span data-ttu-id="1fcc1-272">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1fcc1-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fcc1-273">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1fcc1-273">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="1fcc1-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fcc1-274">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="1fcc1-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fcc1-275">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="1fcc1-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fcc1-276">Search-Flags</span></span>           | <span data-ttu-id="1fcc1-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fcc1-277">0x00000000</span></span>                               |
| <span data-ttu-id="1fcc1-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fcc1-278">System-Flags</span></span>           | <span data-ttu-id="1fcc1-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fcc1-279">0x00000010</span></span>                               |
| <span data-ttu-id="1fcc1-280">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1fcc1-280">Classes used in</span></span>        | [<span data-ttu-id="1fcc1-281">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="1fcc1-281">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1fcc1-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1fcc1-282">Windows Server 2012</span></span>



| <span data-ttu-id="1fcc1-283">Entrada</span><span class="sxs-lookup"><span data-stu-id="1fcc1-283">Entry</span></span> | <span data-ttu-id="1fcc1-284">Value</span><span class="sxs-lookup"><span data-stu-id="1fcc1-284">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="1fcc1-285">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1fcc1-285">Link-Id</span></span>                | <span data-ttu-id="1fcc1-286">76</span><span class="sxs-lookup"><span data-stu-id="1fcc1-286">76</span></span>                                       |
| <span data-ttu-id="1fcc1-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fcc1-287">MAPI-Id</span></span>                | <span data-ttu-id="1fcc1-288">0x80B6</span><span class="sxs-lookup"><span data-stu-id="1fcc1-288">0x80B6</span></span>                                   |
| <span data-ttu-id="1fcc1-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fcc1-289">System-Only</span></span>            | <span data-ttu-id="1fcc1-290">True</span><span class="sxs-lookup"><span data-stu-id="1fcc1-290">True</span></span>                                     |
| <span data-ttu-id="1fcc1-291">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1fcc1-291">Is-Single-Valued</span></span>       | <span data-ttu-id="1fcc1-292">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-292">False</span></span>                                    |
| <span data-ttu-id="1fcc1-293">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1fcc1-293">Is Indexed</span></span>             | <span data-ttu-id="1fcc1-294">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-294">False</span></span>                                    |
| <span data-ttu-id="1fcc1-295">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1fcc1-295">In Global Catalog</span></span>      | <span data-ttu-id="1fcc1-296">False</span><span class="sxs-lookup"><span data-stu-id="1fcc1-296">False</span></span>                                    |
| <span data-ttu-id="1fcc1-297">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1fcc1-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fcc1-298">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1fcc1-298">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="1fcc1-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fcc1-299">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="1fcc1-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fcc1-300">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="1fcc1-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fcc1-301">Search-Flags</span></span>           | <span data-ttu-id="1fcc1-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fcc1-302">0x00000000</span></span>                               |
| <span data-ttu-id="1fcc1-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fcc1-303">System-Flags</span></span>           | <span data-ttu-id="1fcc1-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fcc1-304">0x00000010</span></span>                               |
| <span data-ttu-id="1fcc1-305">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1fcc1-305">Classes used in</span></span>        | [<span data-ttu-id="1fcc1-306">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="1fcc1-306">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





