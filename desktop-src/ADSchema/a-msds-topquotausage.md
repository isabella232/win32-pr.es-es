---
title: atributo de uso de cuota de MS-DS-Top
description: La lista de usuarios de cuota superior actualmente en la base de datos de directorio, ordenada por el uso de cuota decreciente.
ms.assetid: c52db8c8-233c-495f-b3fe-edbe1d723677
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-Top-quota-Usage
- Esquema de AD de atributo msDS-TopQuotaUsage
topic_type:
- apiref
api_name:
- ms-DS-Top-Quota-Usage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db787c0360eff64c726ec680c9fd2a18da1e8d1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659102"
---
# <a name="ms-ds-top-quota-usage-attribute"></a><span data-ttu-id="1d45d-105">atributo de uso de cuota de MS-DS-Top</span><span class="sxs-lookup"><span data-stu-id="1d45d-105">ms-DS-Top-Quota-Usage attribute</span></span>

<span data-ttu-id="1d45d-106">La lista de usuarios de cuota superior actualmente en la base de datos de directorio, ordenada por el uso de cuota decreciente.</span><span class="sxs-lookup"><span data-stu-id="1d45d-106">The list of top quota users currently in the directory database, ordered by decreasing quota usage.</span></span>



| <span data-ttu-id="1d45d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d45d-107">Entry</span></span> | <span data-ttu-id="1d45d-108">Value</span><span class="sxs-lookup"><span data-stu-id="1d45d-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="1d45d-109">CN</span><span class="sxs-lookup"><span data-stu-id="1d45d-109">CN</span></span>                | <span data-ttu-id="1d45d-110">MS-DS-Top-quota-uso</span><span class="sxs-lookup"><span data-stu-id="1d45d-110">ms-DS-Top-Quota-Usage</span></span>                       |
| <span data-ttu-id="1d45d-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="1d45d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1d45d-112">msDS-TopQuotaUsage</span><span class="sxs-lookup"><span data-stu-id="1d45d-112">msDS-TopQuotaUsage</span></span>                          |
| <span data-ttu-id="1d45d-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="1d45d-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="1d45d-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="1d45d-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="1d45d-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="1d45d-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="1d45d-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1d45d-116">Attribute-Id</span></span>      | <span data-ttu-id="1d45d-117">1.2.840.113556.1.4.1850</span><span class="sxs-lookup"><span data-stu-id="1d45d-117">1.2.840.113556.1.4.1850</span></span>                     |
| <span data-ttu-id="1d45d-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1d45d-118">System-Id-Guid</span></span>    | <span data-ttu-id="1d45d-119">7b7cce4f-f1f5-4bb6-b7eb-23504af19e75</span><span class="sxs-lookup"><span data-stu-id="1d45d-119">7b7cce4f-f1f5-4bb6-b7eb-23504af19e75</span></span>        |
| <span data-ttu-id="1d45d-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d45d-120">Syntax</span></span>            | [<span data-ttu-id="1d45d-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1d45d-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="1d45d-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="1d45d-122">Implementations</span></span>

-   [<span data-ttu-id="1d45d-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1d45d-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1d45d-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1d45d-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1d45d-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1d45d-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1d45d-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1d45d-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1d45d-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1d45d-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1d45d-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1d45d-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="1d45d-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1d45d-129">Windows Server 2003</span></span>



| <span data-ttu-id="1d45d-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d45d-130">Entry</span></span> | <span data-ttu-id="1d45d-131">Value</span><span class="sxs-lookup"><span data-stu-id="1d45d-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="1d45d-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1d45d-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="1d45d-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d45d-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="1d45d-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d45d-134">System-Only</span></span>            | <span data-ttu-id="1d45d-135">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-135">False</span></span>                                                             |
| <span data-ttu-id="1d45d-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1d45d-136">Is-Single-Valued</span></span>       | <span data-ttu-id="1d45d-137">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-137">False</span></span>                                                             |
| <span data-ttu-id="1d45d-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1d45d-138">Is Indexed</span></span>             | <span data-ttu-id="1d45d-139">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-139">False</span></span>                                                             |
| <span data-ttu-id="1d45d-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d45d-140">In Global Catalog</span></span>      | <span data-ttu-id="1d45d-141">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-141">False</span></span>                                                             |
| <span data-ttu-id="1d45d-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1d45d-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d45d-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d45d-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="1d45d-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d45d-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="1d45d-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d45d-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="1d45d-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45d-146">Search-Flags</span></span>           | <span data-ttu-id="1d45d-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d45d-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="1d45d-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45d-148">System-Flags</span></span>           | <span data-ttu-id="1d45d-149">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1d45d-149">0x00000014</span></span>                                                        |
| <span data-ttu-id="1d45d-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1d45d-150">Classes used in</span></span>        | [<span data-ttu-id="1d45d-151">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="1d45d-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1d45d-152">ADAM</span><span class="sxs-lookup"><span data-stu-id="1d45d-152">ADAM</span></span>



| <span data-ttu-id="1d45d-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d45d-153">Entry</span></span> | <span data-ttu-id="1d45d-154">Value</span><span class="sxs-lookup"><span data-stu-id="1d45d-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="1d45d-155">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1d45d-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="1d45d-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d45d-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="1d45d-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d45d-157">System-Only</span></span>            | <span data-ttu-id="1d45d-158">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-158">False</span></span>                                                             |
| <span data-ttu-id="1d45d-159">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1d45d-159">Is-Single-Valued</span></span>       | <span data-ttu-id="1d45d-160">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-160">False</span></span>                                                             |
| <span data-ttu-id="1d45d-161">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1d45d-161">Is Indexed</span></span>             | <span data-ttu-id="1d45d-162">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-162">False</span></span>                                                             |
| <span data-ttu-id="1d45d-163">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d45d-163">In Global Catalog</span></span>      | <span data-ttu-id="1d45d-164">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-164">False</span></span>                                                             |
| <span data-ttu-id="1d45d-165">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1d45d-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d45d-166">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d45d-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="1d45d-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d45d-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="1d45d-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d45d-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="1d45d-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45d-169">Search-Flags</span></span>           | <span data-ttu-id="1d45d-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d45d-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="1d45d-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45d-171">System-Flags</span></span>           | <span data-ttu-id="1d45d-172">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1d45d-172">0x00000014</span></span>                                                        |
| <span data-ttu-id="1d45d-173">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1d45d-173">Classes used in</span></span>        | [<span data-ttu-id="1d45d-174">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="1d45d-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1d45d-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1d45d-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1d45d-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d45d-176">Entry</span></span> | <span data-ttu-id="1d45d-177">Value</span><span class="sxs-lookup"><span data-stu-id="1d45d-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="1d45d-178">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1d45d-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="1d45d-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d45d-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="1d45d-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d45d-180">System-Only</span></span>            | <span data-ttu-id="1d45d-181">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-181">False</span></span>                                                             |
| <span data-ttu-id="1d45d-182">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1d45d-182">Is-Single-Valued</span></span>       | <span data-ttu-id="1d45d-183">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-183">False</span></span>                                                             |
| <span data-ttu-id="1d45d-184">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1d45d-184">Is Indexed</span></span>             | <span data-ttu-id="1d45d-185">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-185">False</span></span>                                                             |
| <span data-ttu-id="1d45d-186">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d45d-186">In Global Catalog</span></span>      | <span data-ttu-id="1d45d-187">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-187">False</span></span>                                                             |
| <span data-ttu-id="1d45d-188">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1d45d-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d45d-189">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d45d-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="1d45d-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d45d-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="1d45d-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d45d-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="1d45d-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45d-192">Search-Flags</span></span>           | <span data-ttu-id="1d45d-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d45d-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="1d45d-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45d-194">System-Flags</span></span>           | <span data-ttu-id="1d45d-195">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1d45d-195">0x00000014</span></span>                                                        |
| <span data-ttu-id="1d45d-196">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1d45d-196">Classes used in</span></span>        | [<span data-ttu-id="1d45d-197">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="1d45d-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1d45d-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d45d-198">Windows Server 2008</span></span>



| <span data-ttu-id="1d45d-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d45d-199">Entry</span></span> | <span data-ttu-id="1d45d-200">Value</span><span class="sxs-lookup"><span data-stu-id="1d45d-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="1d45d-201">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1d45d-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="1d45d-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d45d-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="1d45d-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d45d-203">System-Only</span></span>            | <span data-ttu-id="1d45d-204">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-204">False</span></span>                                                             |
| <span data-ttu-id="1d45d-205">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1d45d-205">Is-Single-Valued</span></span>       | <span data-ttu-id="1d45d-206">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-206">False</span></span>                                                             |
| <span data-ttu-id="1d45d-207">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1d45d-207">Is Indexed</span></span>             | <span data-ttu-id="1d45d-208">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-208">False</span></span>                                                             |
| <span data-ttu-id="1d45d-209">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d45d-209">In Global Catalog</span></span>      | <span data-ttu-id="1d45d-210">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-210">False</span></span>                                                             |
| <span data-ttu-id="1d45d-211">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1d45d-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d45d-212">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d45d-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="1d45d-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d45d-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="1d45d-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d45d-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="1d45d-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45d-215">Search-Flags</span></span>           | <span data-ttu-id="1d45d-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d45d-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="1d45d-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45d-217">System-Flags</span></span>           | <span data-ttu-id="1d45d-218">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1d45d-218">0x00000014</span></span>                                                        |
| <span data-ttu-id="1d45d-219">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1d45d-219">Classes used in</span></span>        | [<span data-ttu-id="1d45d-220">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="1d45d-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1d45d-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1d45d-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1d45d-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d45d-222">Entry</span></span> | <span data-ttu-id="1d45d-223">Value</span><span class="sxs-lookup"><span data-stu-id="1d45d-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="1d45d-224">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1d45d-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="1d45d-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d45d-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="1d45d-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d45d-226">System-Only</span></span>            | <span data-ttu-id="1d45d-227">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-227">False</span></span>                                                             |
| <span data-ttu-id="1d45d-228">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1d45d-228">Is-Single-Valued</span></span>       | <span data-ttu-id="1d45d-229">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-229">False</span></span>                                                             |
| <span data-ttu-id="1d45d-230">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1d45d-230">Is Indexed</span></span>             | <span data-ttu-id="1d45d-231">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-231">False</span></span>                                                             |
| <span data-ttu-id="1d45d-232">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d45d-232">In Global Catalog</span></span>      | <span data-ttu-id="1d45d-233">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-233">False</span></span>                                                             |
| <span data-ttu-id="1d45d-234">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1d45d-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d45d-235">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d45d-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="1d45d-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d45d-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="1d45d-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d45d-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="1d45d-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45d-238">Search-Flags</span></span>           | <span data-ttu-id="1d45d-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d45d-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="1d45d-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45d-240">System-Flags</span></span>           | <span data-ttu-id="1d45d-241">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1d45d-241">0x00000014</span></span>                                                        |
| <span data-ttu-id="1d45d-242">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1d45d-242">Classes used in</span></span>        | [<span data-ttu-id="1d45d-243">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="1d45d-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1d45d-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1d45d-244">Windows Server 2012</span></span>



| <span data-ttu-id="1d45d-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d45d-245">Entry</span></span> | <span data-ttu-id="1d45d-246">Value</span><span class="sxs-lookup"><span data-stu-id="1d45d-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="1d45d-247">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1d45d-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="1d45d-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d45d-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="1d45d-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d45d-249">System-Only</span></span>            | <span data-ttu-id="1d45d-250">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-250">False</span></span>                                                             |
| <span data-ttu-id="1d45d-251">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1d45d-251">Is-Single-Valued</span></span>       | <span data-ttu-id="1d45d-252">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-252">False</span></span>                                                             |
| <span data-ttu-id="1d45d-253">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1d45d-253">Is Indexed</span></span>             | <span data-ttu-id="1d45d-254">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-254">False</span></span>                                                             |
| <span data-ttu-id="1d45d-255">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d45d-255">In Global Catalog</span></span>      | <span data-ttu-id="1d45d-256">False</span><span class="sxs-lookup"><span data-stu-id="1d45d-256">False</span></span>                                                             |
| <span data-ttu-id="1d45d-257">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1d45d-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d45d-258">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d45d-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="1d45d-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d45d-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="1d45d-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d45d-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="1d45d-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45d-261">Search-Flags</span></span>           | <span data-ttu-id="1d45d-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d45d-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="1d45d-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45d-263">System-Flags</span></span>           | <span data-ttu-id="1d45d-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1d45d-264">0x00000014</span></span>                                                        |
| <span data-ttu-id="1d45d-265">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1d45d-265">Classes used in</span></span>        | [<span data-ttu-id="1d45d-266">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="1d45d-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





