---
title: atributo MS-DS-tiene-Domain-NC
description: Información de replicación del servicio de directorio que detalla los contextos de nomenclatura de dominio presentes en un servidor determinado.
ms.assetid: e5a7c371-5a37-466e-b56f-ee261b48e3b2
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MS-DS-tiene-Domain-NC
- Esquema de AD de atributo msDS-HasDomainNCs
topic_type:
- apiref
api_name:
- ms-DS-Has-Domain-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83b946286974cc6ba4e6d30484e7768a1daeccb6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493823"
---
# <a name="ms-ds-has-domain-ncs-attribute"></a><span data-ttu-id="92fd4-105">atributo MS-DS-tiene-Domain-NC</span><span class="sxs-lookup"><span data-stu-id="92fd4-105">ms-DS-Has-Domain-NCs attribute</span></span>

<span data-ttu-id="92fd4-106">Información de replicación del servicio de directorio que detalla los contextos de nomenclatura de dominio presentes en un servidor determinado.</span><span class="sxs-lookup"><span data-stu-id="92fd4-106">Directory service replication information that details the domain naming contexts present on a particular server.</span></span>



| <span data-ttu-id="92fd4-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="92fd4-107">Entry</span></span> | <span data-ttu-id="92fd4-108">Value</span><span class="sxs-lookup"><span data-stu-id="92fd4-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="92fd4-109">CN</span><span class="sxs-lookup"><span data-stu-id="92fd4-109">CN</span></span>                | <span data-ttu-id="92fd4-110">MS-DS-tiene-Domain-NC</span><span class="sxs-lookup"><span data-stu-id="92fd4-110">ms-DS-Has-Domain-NCs</span></span>                                |
| <span data-ttu-id="92fd4-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="92fd4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="92fd4-112">msDS-HasDomainNCs</span><span class="sxs-lookup"><span data-stu-id="92fd4-112">msDS-HasDomainNCs</span></span>                                   |
| <span data-ttu-id="92fd4-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="92fd4-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="92fd4-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="92fd4-114">Update Privilege</span></span>  | <span data-ttu-id="92fd4-115">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="92fd4-115">This value is set by the system</span></span>                     |
| <span data-ttu-id="92fd4-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="92fd4-116">Update Frequency</span></span>  | <span data-ttu-id="92fd4-117">Está establecido por DCPromo y nunca se modificó después.</span><span class="sxs-lookup"><span data-stu-id="92fd4-117">It is set by DCPromo and never modified thereafter.</span></span> |
| <span data-ttu-id="92fd4-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="92fd4-118">Attribute-Id</span></span>      | <span data-ttu-id="92fd4-119">1.2.840.113556.1.4.1820</span><span class="sxs-lookup"><span data-stu-id="92fd4-119">1.2.840.113556.1.4.1820</span></span>                             |
| <span data-ttu-id="92fd4-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="92fd4-120">System-Id-Guid</span></span>    | <span data-ttu-id="92fd4-121">6f17e347-a842-4498-b8b3-15e007da4fed</span><span class="sxs-lookup"><span data-stu-id="92fd4-121">6f17e347-a842-4498-b8b3-15e007da4fed</span></span>                |
| <span data-ttu-id="92fd4-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92fd4-122">Syntax</span></span>            | [<span data-ttu-id="92fd4-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="92fd4-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)             |



## <a name="implementations"></a><span data-ttu-id="92fd4-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="92fd4-124">Implementations</span></span>

-   [<span data-ttu-id="92fd4-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="92fd4-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="92fd4-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="92fd4-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="92fd4-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="92fd4-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="92fd4-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="92fd4-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="92fd4-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="92fd4-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="92fd4-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="92fd4-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="92fd4-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="92fd4-131">Windows Server 2003</span></span>



| <span data-ttu-id="92fd4-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="92fd4-132">Entry</span></span> | <span data-ttu-id="92fd4-133">Value</span><span class="sxs-lookup"><span data-stu-id="92fd4-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="92fd4-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="92fd4-134">Link-Id</span></span>                | <span data-ttu-id="92fd4-135">2026</span><span class="sxs-lookup"><span data-stu-id="92fd4-135">2026</span></span>                                     |
| <span data-ttu-id="92fd4-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92fd4-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="92fd4-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="92fd4-137">System-Only</span></span>            | <span data-ttu-id="92fd4-138">True</span><span class="sxs-lookup"><span data-stu-id="92fd4-138">True</span></span>                                     |
| <span data-ttu-id="92fd4-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="92fd4-139">Is-Single-Valued</span></span>       | <span data-ttu-id="92fd4-140">False</span><span class="sxs-lookup"><span data-stu-id="92fd4-140">False</span></span>                                    |
| <span data-ttu-id="92fd4-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="92fd4-141">Is Indexed</span></span>             | <span data-ttu-id="92fd4-142">False</span><span class="sxs-lookup"><span data-stu-id="92fd4-142">False</span></span>                                    |
| <span data-ttu-id="92fd4-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="92fd4-143">In Global Catalog</span></span>      | <span data-ttu-id="92fd4-144">False</span><span class="sxs-lookup"><span data-stu-id="92fd4-144">False</span></span>                                    |
| <span data-ttu-id="92fd4-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="92fd4-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="92fd4-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92fd4-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="92fd4-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92fd4-147">Range-Lower</span></span>            | <span data-ttu-id="92fd4-148">4</span><span class="sxs-lookup"><span data-stu-id="92fd4-148">4</span></span>                                        |
| <span data-ttu-id="92fd4-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92fd4-149">Range-Upper</span></span>            | <span data-ttu-id="92fd4-150">4</span><span class="sxs-lookup"><span data-stu-id="92fd4-150">4</span></span>                                        |
| <span data-ttu-id="92fd4-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92fd4-151">Search-Flags</span></span>           | <span data-ttu-id="92fd4-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92fd4-152">0x00000000</span></span>                               |
| <span data-ttu-id="92fd4-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92fd4-153">System-Flags</span></span>           | <span data-ttu-id="92fd4-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92fd4-154">0x00000010</span></span>                               |
| <span data-ttu-id="92fd4-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="92fd4-155">Classes used in</span></span>        | [<span data-ttu-id="92fd4-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="92fd4-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="92fd4-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="92fd4-157">ADAM</span></span>



| <span data-ttu-id="92fd4-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="92fd4-158">Entry</span></span> | <span data-ttu-id="92fd4-159">Value</span><span class="sxs-lookup"><span data-stu-id="92fd4-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="92fd4-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="92fd4-160">Link-Id</span></span>                | <span data-ttu-id="92fd4-161">2026</span><span class="sxs-lookup"><span data-stu-id="92fd4-161">2026</span></span>                                     |
| <span data-ttu-id="92fd4-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92fd4-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="92fd4-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="92fd4-163">System-Only</span></span>            | <span data-ttu-id="92fd4-164">True</span><span class="sxs-lookup"><span data-stu-id="92fd4-164">True</span></span>                                     |
| <span data-ttu-id="92fd4-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="92fd4-165">Is-Single-Valued</span></span>       | <span data-ttu-id="92fd4-166">False</span><span class="sxs-lookup"><span data-stu-id="92fd4-166">False</span></span>                                    |
| <span data-ttu-id="92fd4-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="92fd4-167">Is Indexed</span></span>             | <span data-ttu-id="92fd4-168">False</span><span class="sxs-lookup"><span data-stu-id="92fd4-168">False</span></span>                                    |
| <span data-ttu-id="92fd4-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="92fd4-169">In Global Catalog</span></span>      | <span data-ttu-id="92fd4-170">False</span><span class="sxs-lookup"><span data-stu-id="92fd4-170">False</span></span>                                    |
| <span data-ttu-id="92fd4-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="92fd4-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="92fd4-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92fd4-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="92fd4-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92fd4-173">Range-Lower</span></span>            | <span data-ttu-id="92fd4-174">4</span><span class="sxs-lookup"><span data-stu-id="92fd4-174">4</span></span>                                        |
| <span data-ttu-id="92fd4-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92fd4-175">Range-Upper</span></span>            | <span data-ttu-id="92fd4-176">4</span><span class="sxs-lookup"><span data-stu-id="92fd4-176">4</span></span>                                        |
| <span data-ttu-id="92fd4-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92fd4-177">Search-Flags</span></span>           | <span data-ttu-id="92fd4-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92fd4-178">0x00000000</span></span>                               |
| <span data-ttu-id="92fd4-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92fd4-179">System-Flags</span></span>           | <span data-ttu-id="92fd4-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92fd4-180">0x00000010</span></span>                               |
| <span data-ttu-id="92fd4-181">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="92fd4-181">Classes used in</span></span>        | [<span data-ttu-id="92fd4-182">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="92fd4-182">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="92fd4-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="92fd4-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="92fd4-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="92fd4-184">Entry</span></span> | <span data-ttu-id="92fd4-185">Value</span><span class="sxs-lookup"><span data-stu-id="92fd4-185">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="92fd4-186">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="92fd4-186">Link-Id</span></span>                | <span data-ttu-id="92fd4-187">2026</span><span class="sxs-lookup"><span data-stu-id="92fd4-187">2026</span></span>                                     |
| <span data-ttu-id="92fd4-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92fd4-188">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="92fd4-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="92fd4-189">System-Only</span></span>            | <span data-ttu-id="92fd4-190">True</span><span class="sxs-lookup"><span data-stu-id="92fd4-190">True</span></span>                                     |
| <span data-ttu-id="92fd4-191">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="92fd4-191">Is-Single-Valued</span></span>       | <span data-ttu-id="92fd4-192">False</span><span class="sxs-lookup"><span data-stu-id="92fd4-192">False</span></span>                                    |
| <span data-ttu-id="92fd4-193">Está indexado</span><span class="sxs-lookup"><span data-stu-id="92fd4-193">Is Indexed</span></span>             | <span data-ttu-id="92fd4-194">False</span><span class="sxs-lookup"><span data-stu-id="92fd4-194">False</span></span>                                    |
| <span data-ttu-id="92fd4-195">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="92fd4-195">In Global Catalog</span></span>      | <span data-ttu-id="92fd4-196">False</span><span class="sxs-lookup"><span data-stu-id="92fd4-196">False</span></span>                                    |
| <span data-ttu-id="92fd4-197">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="92fd4-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="92fd4-198">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92fd4-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="92fd4-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92fd4-199">Range-Lower</span></span>            | <span data-ttu-id="92fd4-200">4</span><span class="sxs-lookup"><span data-stu-id="92fd4-200">4</span></span>                                        |
| <span data-ttu-id="92fd4-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92fd4-201">Range-Upper</span></span>            | <span data-ttu-id="92fd4-202">4</span><span class="sxs-lookup"><span data-stu-id="92fd4-202">4</span></span>                                        |
| <span data-ttu-id="92fd4-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92fd4-203">Search-Flags</span></span>           | <span data-ttu-id="92fd4-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92fd4-204">0x00000000</span></span>                               |
| <span data-ttu-id="92fd4-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92fd4-205">System-Flags</span></span>           | <span data-ttu-id="92fd4-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92fd4-206">0x00000010</span></span>                               |
| <span data-ttu-id="92fd4-207">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="92fd4-207">Classes used in</span></span>        | [<span data-ttu-id="92fd4-208">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="92fd4-208">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="92fd4-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92fd4-209">Windows Server 2008</span></span>



| <span data-ttu-id="92fd4-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="92fd4-210">Entry</span></span> | <span data-ttu-id="92fd4-211">Value</span><span class="sxs-lookup"><span data-stu-id="92fd4-211">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="92fd4-212">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="92fd4-212">Link-Id</span></span>                | <span data-ttu-id="92fd4-213">2026</span><span class="sxs-lookup"><span data-stu-id="92fd4-213">2026</span></span>                                     |
| <span data-ttu-id="92fd4-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92fd4-214">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="92fd4-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="92fd4-215">System-Only</span></span>            | <span data-ttu-id="92fd4-216">True</span><span class="sxs-lookup"><span data-stu-id="92fd4-216">True</span></span>                                     |
| <span data-ttu-id="92fd4-217">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="92fd4-217">Is-Single-Valued</span></span>       | <span data-ttu-id="92fd4-218">False</span><span class="sxs-lookup"><span data-stu-id="92fd4-218">False</span></span>                                    |
| <span data-ttu-id="92fd4-219">Está indexado</span><span class="sxs-lookup"><span data-stu-id="92fd4-219">Is Indexed</span></span>             | <span data-ttu-id="92fd4-220">False</span><span class="sxs-lookup"><span data-stu-id="92fd4-220">False</span></span>                                    |
| <span data-ttu-id="92fd4-221">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="92fd4-221">In Global Catalog</span></span>      | <span data-ttu-id="92fd4-222">False</span><span class="sxs-lookup"><span data-stu-id="92fd4-222">False</span></span>                                    |
| <span data-ttu-id="92fd4-223">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="92fd4-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="92fd4-224">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92fd4-224">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="92fd4-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92fd4-225">Range-Lower</span></span>            | <span data-ttu-id="92fd4-226">4</span><span class="sxs-lookup"><span data-stu-id="92fd4-226">4</span></span>                                        |
| <span data-ttu-id="92fd4-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92fd4-227">Range-Upper</span></span>            | <span data-ttu-id="92fd4-228">4</span><span class="sxs-lookup"><span data-stu-id="92fd4-228">4</span></span>                                        |
| <span data-ttu-id="92fd4-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92fd4-229">Search-Flags</span></span>           | <span data-ttu-id="92fd4-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92fd4-230">0x00000000</span></span>                               |
| <span data-ttu-id="92fd4-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92fd4-231">System-Flags</span></span>           | <span data-ttu-id="92fd4-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92fd4-232">0x00000010</span></span>                               |
| <span data-ttu-id="92fd4-233">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="92fd4-233">Classes used in</span></span>        | [<span data-ttu-id="92fd4-234">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="92fd4-234">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="92fd4-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="92fd4-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="92fd4-236">Entrada</span><span class="sxs-lookup"><span data-stu-id="92fd4-236">Entry</span></span> | <span data-ttu-id="92fd4-237">Value</span><span class="sxs-lookup"><span data-stu-id="92fd4-237">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="92fd4-238">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="92fd4-238">Link-Id</span></span>                | <span data-ttu-id="92fd4-239">2026</span><span class="sxs-lookup"><span data-stu-id="92fd4-239">2026</span></span>                                     |
| <span data-ttu-id="92fd4-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92fd4-240">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="92fd4-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="92fd4-241">System-Only</span></span>            | <span data-ttu-id="92fd4-242">True</span><span class="sxs-lookup"><span data-stu-id="92fd4-242">True</span></span>                                     |
| <span data-ttu-id="92fd4-243">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="92fd4-243">Is-Single-Valued</span></span>       | <span data-ttu-id="92fd4-244">False</span><span class="sxs-lookup"><span data-stu-id="92fd4-244">False</span></span>                                    |
| <span data-ttu-id="92fd4-245">Está indexado</span><span class="sxs-lookup"><span data-stu-id="92fd4-245">Is Indexed</span></span>             | <span data-ttu-id="92fd4-246">False</span><span class="sxs-lookup"><span data-stu-id="92fd4-246">False</span></span>                                    |
| <span data-ttu-id="92fd4-247">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="92fd4-247">In Global Catalog</span></span>      | <span data-ttu-id="92fd4-248">False</span><span class="sxs-lookup"><span data-stu-id="92fd4-248">False</span></span>                                    |
| <span data-ttu-id="92fd4-249">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="92fd4-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="92fd4-250">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92fd4-250">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="92fd4-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92fd4-251">Range-Lower</span></span>            | <span data-ttu-id="92fd4-252">4</span><span class="sxs-lookup"><span data-stu-id="92fd4-252">4</span></span>                                        |
| <span data-ttu-id="92fd4-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92fd4-253">Range-Upper</span></span>            | <span data-ttu-id="92fd4-254">4</span><span class="sxs-lookup"><span data-stu-id="92fd4-254">4</span></span>                                        |
| <span data-ttu-id="92fd4-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92fd4-255">Search-Flags</span></span>           | <span data-ttu-id="92fd4-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92fd4-256">0x00000000</span></span>                               |
| <span data-ttu-id="92fd4-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92fd4-257">System-Flags</span></span>           | <span data-ttu-id="92fd4-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92fd4-258">0x00000010</span></span>                               |
| <span data-ttu-id="92fd4-259">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="92fd4-259">Classes used in</span></span>        | [<span data-ttu-id="92fd4-260">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="92fd4-260">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="92fd4-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="92fd4-261">Windows Server 2012</span></span>



| <span data-ttu-id="92fd4-262">Entrada</span><span class="sxs-lookup"><span data-stu-id="92fd4-262">Entry</span></span> | <span data-ttu-id="92fd4-263">Value</span><span class="sxs-lookup"><span data-stu-id="92fd4-263">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="92fd4-264">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="92fd4-264">Link-Id</span></span>                | <span data-ttu-id="92fd4-265">2026</span><span class="sxs-lookup"><span data-stu-id="92fd4-265">2026</span></span>                                     |
| <span data-ttu-id="92fd4-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92fd4-266">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="92fd4-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="92fd4-267">System-Only</span></span>            | <span data-ttu-id="92fd4-268">True</span><span class="sxs-lookup"><span data-stu-id="92fd4-268">True</span></span>                                     |
| <span data-ttu-id="92fd4-269">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="92fd4-269">Is-Single-Valued</span></span>       | <span data-ttu-id="92fd4-270">False</span><span class="sxs-lookup"><span data-stu-id="92fd4-270">False</span></span>                                    |
| <span data-ttu-id="92fd4-271">Está indexado</span><span class="sxs-lookup"><span data-stu-id="92fd4-271">Is Indexed</span></span>             | <span data-ttu-id="92fd4-272">False</span><span class="sxs-lookup"><span data-stu-id="92fd4-272">False</span></span>                                    |
| <span data-ttu-id="92fd4-273">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="92fd4-273">In Global Catalog</span></span>      | <span data-ttu-id="92fd4-274">False</span><span class="sxs-lookup"><span data-stu-id="92fd4-274">False</span></span>                                    |
| <span data-ttu-id="92fd4-275">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="92fd4-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="92fd4-276">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92fd4-276">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="92fd4-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92fd4-277">Range-Lower</span></span>            | <span data-ttu-id="92fd4-278">4</span><span class="sxs-lookup"><span data-stu-id="92fd4-278">4</span></span>                                        |
| <span data-ttu-id="92fd4-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92fd4-279">Range-Upper</span></span>            | <span data-ttu-id="92fd4-280">4</span><span class="sxs-lookup"><span data-stu-id="92fd4-280">4</span></span>                                        |
| <span data-ttu-id="92fd4-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92fd4-281">Search-Flags</span></span>           | <span data-ttu-id="92fd4-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92fd4-282">0x00000000</span></span>                               |
| <span data-ttu-id="92fd4-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92fd4-283">System-Flags</span></span>           | <span data-ttu-id="92fd4-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92fd4-284">0x00000010</span></span>                               |
| <span data-ttu-id="92fd4-285">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="92fd4-285">Classes used in</span></span>        | [<span data-ttu-id="92fd4-286">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="92fd4-286">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





