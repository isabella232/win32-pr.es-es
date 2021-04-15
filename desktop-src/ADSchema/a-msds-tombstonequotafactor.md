---
title: atributo de factor de cuota MS-DS-Extinguite
description: El factor de porcentaje por el que se debe reducir el recuento de objetos de marcadores de exclusión con el fin de tener en cuenta la cuota.
ms.assetid: 602c2fe0-d3b7-45e8-8ce8-35a7163f7b25
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de factor de cuota de MS-DS-Extinguite
- Esquema de AD de atributo msDS-TombstoneQuotaFactor
topic_type:
- apiref
api_name:
- ms-DS-Tombstone-Quota-Factor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a44dd7f648754c2ded7334c9b221022d936ebfb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535998"
---
# <a name="ms-ds-tombstone-quota-factor-attribute"></a><span data-ttu-id="19d80-105">atributo de factor de cuota MS-DS-Extinguite</span><span class="sxs-lookup"><span data-stu-id="19d80-105">ms-DS-Tombstone-Quota-Factor attribute</span></span>

<span data-ttu-id="19d80-106">El factor de porcentaje por el que se debe reducir el recuento de objetos de marcadores de exclusión con el fin de tener en cuenta la cuota.</span><span class="sxs-lookup"><span data-stu-id="19d80-106">The percentage factor by which the tombstone object count should be reduced for the purpose of quota accounting.</span></span>



| <span data-ttu-id="19d80-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="19d80-107">Entry</span></span> | <span data-ttu-id="19d80-108">Value</span><span class="sxs-lookup"><span data-stu-id="19d80-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="19d80-109">CN</span><span class="sxs-lookup"><span data-stu-id="19d80-109">CN</span></span>                | <span data-ttu-id="19d80-110">MS-DS-desecho-factor de cuota</span><span class="sxs-lookup"><span data-stu-id="19d80-110">ms-DS-Tombstone-Quota-Factor</span></span>         |
| <span data-ttu-id="19d80-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="19d80-111">Ldap-Display-Name</span></span> | <span data-ttu-id="19d80-112">msDS-TombstoneQuotaFactor</span><span class="sxs-lookup"><span data-stu-id="19d80-112">msDS-TombstoneQuotaFactor</span></span>            |
| <span data-ttu-id="19d80-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="19d80-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="19d80-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="19d80-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="19d80-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="19d80-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="19d80-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="19d80-116">Attribute-Id</span></span>      | <span data-ttu-id="19d80-117">1.2.840.113556.1.4.1847</span><span class="sxs-lookup"><span data-stu-id="19d80-117">1.2.840.113556.1.4.1847</span></span>              |
| <span data-ttu-id="19d80-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="19d80-118">System-Id-Guid</span></span>    | <span data-ttu-id="19d80-119">461744d7-f3b6-45ba-8753-fb9552a5df32</span><span class="sxs-lookup"><span data-stu-id="19d80-119">461744d7-f3b6-45ba-8753-fb9552a5df32</span></span> |
| <span data-ttu-id="19d80-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19d80-120">Syntax</span></span>            | [<span data-ttu-id="19d80-121">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="19d80-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="19d80-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="19d80-122">Implementations</span></span>

-   [<span data-ttu-id="19d80-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="19d80-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="19d80-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="19d80-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="19d80-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="19d80-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="19d80-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="19d80-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="19d80-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="19d80-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="19d80-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="19d80-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="19d80-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="19d80-129">Windows Server 2003</span></span>



| <span data-ttu-id="19d80-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="19d80-130">Entry</span></span> | <span data-ttu-id="19d80-131">Value</span><span class="sxs-lookup"><span data-stu-id="19d80-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="19d80-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="19d80-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="19d80-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19d80-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="19d80-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="19d80-134">System-Only</span></span>            | <span data-ttu-id="19d80-135">False</span><span class="sxs-lookup"><span data-stu-id="19d80-135">False</span></span>                                                             |
| <span data-ttu-id="19d80-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="19d80-136">Is-Single-Valued</span></span>       | <span data-ttu-id="19d80-137">True</span><span class="sxs-lookup"><span data-stu-id="19d80-137">True</span></span>                                                              |
| <span data-ttu-id="19d80-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="19d80-138">Is Indexed</span></span>             | <span data-ttu-id="19d80-139">False</span><span class="sxs-lookup"><span data-stu-id="19d80-139">False</span></span>                                                             |
| <span data-ttu-id="19d80-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="19d80-140">In Global Catalog</span></span>      | <span data-ttu-id="19d80-141">False</span><span class="sxs-lookup"><span data-stu-id="19d80-141">False</span></span>                                                             |
| <span data-ttu-id="19d80-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="19d80-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="19d80-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19d80-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="19d80-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19d80-144">Range-Lower</span></span>            | <span data-ttu-id="19d80-145">0</span><span class="sxs-lookup"><span data-stu-id="19d80-145">0</span></span>                                                                 |
| <span data-ttu-id="19d80-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19d80-146">Range-Upper</span></span>            | <span data-ttu-id="19d80-147">100</span><span class="sxs-lookup"><span data-stu-id="19d80-147">100</span></span>                                                               |
| <span data-ttu-id="19d80-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19d80-148">Search-Flags</span></span>           | <span data-ttu-id="19d80-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19d80-149">0x00000000</span></span>                                                        |
| <span data-ttu-id="19d80-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19d80-150">System-Flags</span></span>           | <span data-ttu-id="19d80-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19d80-151">0x00000010</span></span>                                                        |
| <span data-ttu-id="19d80-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="19d80-152">Classes used in</span></span>        | [<span data-ttu-id="19d80-153">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="19d80-153">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="19d80-154">ADAM</span><span class="sxs-lookup"><span data-stu-id="19d80-154">ADAM</span></span>



| <span data-ttu-id="19d80-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="19d80-155">Entry</span></span> | <span data-ttu-id="19d80-156">Value</span><span class="sxs-lookup"><span data-stu-id="19d80-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="19d80-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="19d80-157">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="19d80-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19d80-158">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="19d80-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="19d80-159">System-Only</span></span>            | <span data-ttu-id="19d80-160">False</span><span class="sxs-lookup"><span data-stu-id="19d80-160">False</span></span>                                                             |
| <span data-ttu-id="19d80-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="19d80-161">Is-Single-Valued</span></span>       | <span data-ttu-id="19d80-162">True</span><span class="sxs-lookup"><span data-stu-id="19d80-162">True</span></span>                                                              |
| <span data-ttu-id="19d80-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="19d80-163">Is Indexed</span></span>             | <span data-ttu-id="19d80-164">False</span><span class="sxs-lookup"><span data-stu-id="19d80-164">False</span></span>                                                             |
| <span data-ttu-id="19d80-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="19d80-165">In Global Catalog</span></span>      | <span data-ttu-id="19d80-166">False</span><span class="sxs-lookup"><span data-stu-id="19d80-166">False</span></span>                                                             |
| <span data-ttu-id="19d80-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="19d80-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="19d80-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19d80-168">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="19d80-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19d80-169">Range-Lower</span></span>            | <span data-ttu-id="19d80-170">0</span><span class="sxs-lookup"><span data-stu-id="19d80-170">0</span></span>                                                                 |
| <span data-ttu-id="19d80-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19d80-171">Range-Upper</span></span>            | <span data-ttu-id="19d80-172">100</span><span class="sxs-lookup"><span data-stu-id="19d80-172">100</span></span>                                                               |
| <span data-ttu-id="19d80-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19d80-173">Search-Flags</span></span>           | <span data-ttu-id="19d80-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19d80-174">0x00000000</span></span>                                                        |
| <span data-ttu-id="19d80-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19d80-175">System-Flags</span></span>           | <span data-ttu-id="19d80-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19d80-176">0x00000010</span></span>                                                        |
| <span data-ttu-id="19d80-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="19d80-177">Classes used in</span></span>        | [<span data-ttu-id="19d80-178">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="19d80-178">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="19d80-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="19d80-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="19d80-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="19d80-180">Entry</span></span> | <span data-ttu-id="19d80-181">Value</span><span class="sxs-lookup"><span data-stu-id="19d80-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="19d80-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="19d80-182">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="19d80-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19d80-183">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="19d80-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="19d80-184">System-Only</span></span>            | <span data-ttu-id="19d80-185">False</span><span class="sxs-lookup"><span data-stu-id="19d80-185">False</span></span>                                                             |
| <span data-ttu-id="19d80-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="19d80-186">Is-Single-Valued</span></span>       | <span data-ttu-id="19d80-187">True</span><span class="sxs-lookup"><span data-stu-id="19d80-187">True</span></span>                                                              |
| <span data-ttu-id="19d80-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="19d80-188">Is Indexed</span></span>             | <span data-ttu-id="19d80-189">False</span><span class="sxs-lookup"><span data-stu-id="19d80-189">False</span></span>                                                             |
| <span data-ttu-id="19d80-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="19d80-190">In Global Catalog</span></span>      | <span data-ttu-id="19d80-191">False</span><span class="sxs-lookup"><span data-stu-id="19d80-191">False</span></span>                                                             |
| <span data-ttu-id="19d80-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="19d80-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="19d80-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19d80-193">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="19d80-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19d80-194">Range-Lower</span></span>            | <span data-ttu-id="19d80-195">0</span><span class="sxs-lookup"><span data-stu-id="19d80-195">0</span></span>                                                                 |
| <span data-ttu-id="19d80-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19d80-196">Range-Upper</span></span>            | <span data-ttu-id="19d80-197">100</span><span class="sxs-lookup"><span data-stu-id="19d80-197">100</span></span>                                                               |
| <span data-ttu-id="19d80-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19d80-198">Search-Flags</span></span>           | <span data-ttu-id="19d80-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19d80-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="19d80-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19d80-200">System-Flags</span></span>           | <span data-ttu-id="19d80-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19d80-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="19d80-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="19d80-202">Classes used in</span></span>        | [<span data-ttu-id="19d80-203">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="19d80-203">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="19d80-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19d80-204">Windows Server 2008</span></span>



| <span data-ttu-id="19d80-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="19d80-205">Entry</span></span> | <span data-ttu-id="19d80-206">Value</span><span class="sxs-lookup"><span data-stu-id="19d80-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="19d80-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="19d80-207">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="19d80-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19d80-208">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="19d80-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="19d80-209">System-Only</span></span>            | <span data-ttu-id="19d80-210">False</span><span class="sxs-lookup"><span data-stu-id="19d80-210">False</span></span>                                                             |
| <span data-ttu-id="19d80-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="19d80-211">Is-Single-Valued</span></span>       | <span data-ttu-id="19d80-212">True</span><span class="sxs-lookup"><span data-stu-id="19d80-212">True</span></span>                                                              |
| <span data-ttu-id="19d80-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="19d80-213">Is Indexed</span></span>             | <span data-ttu-id="19d80-214">False</span><span class="sxs-lookup"><span data-stu-id="19d80-214">False</span></span>                                                             |
| <span data-ttu-id="19d80-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="19d80-215">In Global Catalog</span></span>      | <span data-ttu-id="19d80-216">False</span><span class="sxs-lookup"><span data-stu-id="19d80-216">False</span></span>                                                             |
| <span data-ttu-id="19d80-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="19d80-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="19d80-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19d80-218">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="19d80-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19d80-219">Range-Lower</span></span>            | <span data-ttu-id="19d80-220">0</span><span class="sxs-lookup"><span data-stu-id="19d80-220">0</span></span>                                                                 |
| <span data-ttu-id="19d80-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19d80-221">Range-Upper</span></span>            | <span data-ttu-id="19d80-222">100</span><span class="sxs-lookup"><span data-stu-id="19d80-222">100</span></span>                                                               |
| <span data-ttu-id="19d80-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19d80-223">Search-Flags</span></span>           | <span data-ttu-id="19d80-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19d80-224">0x00000000</span></span>                                                        |
| <span data-ttu-id="19d80-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19d80-225">System-Flags</span></span>           | <span data-ttu-id="19d80-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19d80-226">0x00000010</span></span>                                                        |
| <span data-ttu-id="19d80-227">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="19d80-227">Classes used in</span></span>        | [<span data-ttu-id="19d80-228">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="19d80-228">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="19d80-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="19d80-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="19d80-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="19d80-230">Entry</span></span> | <span data-ttu-id="19d80-231">Value</span><span class="sxs-lookup"><span data-stu-id="19d80-231">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="19d80-232">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="19d80-232">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="19d80-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19d80-233">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="19d80-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="19d80-234">System-Only</span></span>            | <span data-ttu-id="19d80-235">False</span><span class="sxs-lookup"><span data-stu-id="19d80-235">False</span></span>                                                             |
| <span data-ttu-id="19d80-236">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="19d80-236">Is-Single-Valued</span></span>       | <span data-ttu-id="19d80-237">True</span><span class="sxs-lookup"><span data-stu-id="19d80-237">True</span></span>                                                              |
| <span data-ttu-id="19d80-238">Está indexado</span><span class="sxs-lookup"><span data-stu-id="19d80-238">Is Indexed</span></span>             | <span data-ttu-id="19d80-239">False</span><span class="sxs-lookup"><span data-stu-id="19d80-239">False</span></span>                                                             |
| <span data-ttu-id="19d80-240">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="19d80-240">In Global Catalog</span></span>      | <span data-ttu-id="19d80-241">False</span><span class="sxs-lookup"><span data-stu-id="19d80-241">False</span></span>                                                             |
| <span data-ttu-id="19d80-242">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="19d80-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="19d80-243">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19d80-243">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="19d80-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19d80-244">Range-Lower</span></span>            | <span data-ttu-id="19d80-245">0</span><span class="sxs-lookup"><span data-stu-id="19d80-245">0</span></span>                                                                 |
| <span data-ttu-id="19d80-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19d80-246">Range-Upper</span></span>            | <span data-ttu-id="19d80-247">100</span><span class="sxs-lookup"><span data-stu-id="19d80-247">100</span></span>                                                               |
| <span data-ttu-id="19d80-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19d80-248">Search-Flags</span></span>           | <span data-ttu-id="19d80-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19d80-249">0x00000000</span></span>                                                        |
| <span data-ttu-id="19d80-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19d80-250">System-Flags</span></span>           | <span data-ttu-id="19d80-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19d80-251">0x00000010</span></span>                                                        |
| <span data-ttu-id="19d80-252">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="19d80-252">Classes used in</span></span>        | [<span data-ttu-id="19d80-253">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="19d80-253">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="19d80-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="19d80-254">Windows Server 2012</span></span>



| <span data-ttu-id="19d80-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="19d80-255">Entry</span></span> | <span data-ttu-id="19d80-256">Value</span><span class="sxs-lookup"><span data-stu-id="19d80-256">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="19d80-257">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="19d80-257">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="19d80-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19d80-258">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="19d80-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="19d80-259">System-Only</span></span>            | <span data-ttu-id="19d80-260">False</span><span class="sxs-lookup"><span data-stu-id="19d80-260">False</span></span>                                                             |
| <span data-ttu-id="19d80-261">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="19d80-261">Is-Single-Valued</span></span>       | <span data-ttu-id="19d80-262">True</span><span class="sxs-lookup"><span data-stu-id="19d80-262">True</span></span>                                                              |
| <span data-ttu-id="19d80-263">Está indexado</span><span class="sxs-lookup"><span data-stu-id="19d80-263">Is Indexed</span></span>             | <span data-ttu-id="19d80-264">False</span><span class="sxs-lookup"><span data-stu-id="19d80-264">False</span></span>                                                             |
| <span data-ttu-id="19d80-265">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="19d80-265">In Global Catalog</span></span>      | <span data-ttu-id="19d80-266">False</span><span class="sxs-lookup"><span data-stu-id="19d80-266">False</span></span>                                                             |
| <span data-ttu-id="19d80-267">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="19d80-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="19d80-268">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19d80-268">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="19d80-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19d80-269">Range-Lower</span></span>            | <span data-ttu-id="19d80-270">0</span><span class="sxs-lookup"><span data-stu-id="19d80-270">0</span></span>                                                                 |
| <span data-ttu-id="19d80-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19d80-271">Range-Upper</span></span>            | <span data-ttu-id="19d80-272">100</span><span class="sxs-lookup"><span data-stu-id="19d80-272">100</span></span>                                                               |
| <span data-ttu-id="19d80-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19d80-273">Search-Flags</span></span>           | <span data-ttu-id="19d80-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19d80-274">0x00000000</span></span>                                                        |
| <span data-ttu-id="19d80-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19d80-275">System-Flags</span></span>           | <span data-ttu-id="19d80-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19d80-276">0x00000010</span></span>                                                        |
| <span data-ttu-id="19d80-277">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="19d80-277">Classes used in</span></span>        | [<span data-ttu-id="19d80-278">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="19d80-278">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





