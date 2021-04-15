---
title: atributo de MS-DS-quotable
description: La cuota efectiva para una entidad de seguridad calculada a partir de las cuotas asignadas para una partición de directorio.
ms.assetid: 22422499-9b56-4d74-a30e-63917abacdd1
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos efectivos de MS-DS-quota
- Esquema de AD de atributo msDS-QuotaEffective
topic_type:
- apiref
api_name:
- ms-DS-Quota-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fe610c87c356431883cecded5eda3e0a9c42297
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494021"
---
# <a name="ms-ds-quota-effective-attribute"></a><span data-ttu-id="69095-105">atributo de MS-DS-quotable</span><span class="sxs-lookup"><span data-stu-id="69095-105">ms-DS-Quota-Effective attribute</span></span>

<span data-ttu-id="69095-106">La cuota efectiva para una entidad de seguridad calculada a partir de las cuotas asignadas para una partición de directorio.</span><span class="sxs-lookup"><span data-stu-id="69095-106">The effective quota for a security principal computed from the assigned quotas for a directory partition.</span></span>



| <span data-ttu-id="69095-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="69095-107">Entry</span></span> | <span data-ttu-id="69095-108">Value</span><span class="sxs-lookup"><span data-stu-id="69095-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="69095-109">CN</span><span class="sxs-lookup"><span data-stu-id="69095-109">CN</span></span>                | <span data-ttu-id="69095-110">MS-DS-quota-efectiva</span><span class="sxs-lookup"><span data-stu-id="69095-110">ms-DS-Quota-Effective</span></span>                |
| <span data-ttu-id="69095-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="69095-111">Ldap-Display-Name</span></span> | <span data-ttu-id="69095-112">msDS-QuotaEffective</span><span class="sxs-lookup"><span data-stu-id="69095-112">msDS-QuotaEffective</span></span>                  |
| <span data-ttu-id="69095-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="69095-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="69095-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="69095-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="69095-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="69095-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="69095-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="69095-116">Attribute-Id</span></span>      | <span data-ttu-id="69095-117">1.2.840.113556.1.4.1848</span><span class="sxs-lookup"><span data-stu-id="69095-117">1.2.840.113556.1.4.1848</span></span>              |
| <span data-ttu-id="69095-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="69095-118">System-Id-Guid</span></span>    | <span data-ttu-id="69095-119">6655b152-101c-48b4-b347-e1fcebc60157</span><span class="sxs-lookup"><span data-stu-id="69095-119">6655b152-101c-48b4-b347-e1fcebc60157</span></span> |
| <span data-ttu-id="69095-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69095-120">Syntax</span></span>            | [<span data-ttu-id="69095-121">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="69095-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="69095-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="69095-122">Implementations</span></span>

-   [<span data-ttu-id="69095-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="69095-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="69095-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="69095-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="69095-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="69095-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="69095-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="69095-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="69095-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="69095-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="69095-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="69095-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="69095-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="69095-129">Windows Server 2003</span></span>



| <span data-ttu-id="69095-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="69095-130">Entry</span></span> | <span data-ttu-id="69095-131">Value</span><span class="sxs-lookup"><span data-stu-id="69095-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="69095-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="69095-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="69095-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69095-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="69095-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="69095-134">System-Only</span></span>            | <span data-ttu-id="69095-135">False</span><span class="sxs-lookup"><span data-stu-id="69095-135">False</span></span>                                                             |
| <span data-ttu-id="69095-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="69095-136">Is-Single-Valued</span></span>       | <span data-ttu-id="69095-137">True</span><span class="sxs-lookup"><span data-stu-id="69095-137">True</span></span>                                                              |
| <span data-ttu-id="69095-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="69095-138">Is Indexed</span></span>             | <span data-ttu-id="69095-139">False</span><span class="sxs-lookup"><span data-stu-id="69095-139">False</span></span>                                                             |
| <span data-ttu-id="69095-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="69095-140">In Global Catalog</span></span>      | <span data-ttu-id="69095-141">False</span><span class="sxs-lookup"><span data-stu-id="69095-141">False</span></span>                                                             |
| <span data-ttu-id="69095-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="69095-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="69095-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69095-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="69095-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69095-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="69095-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69095-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="69095-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69095-146">Search-Flags</span></span>           | <span data-ttu-id="69095-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69095-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="69095-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69095-148">System-Flags</span></span>           | <span data-ttu-id="69095-149">0x00000014</span><span class="sxs-lookup"><span data-stu-id="69095-149">0x00000014</span></span>                                                        |
| <span data-ttu-id="69095-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="69095-150">Classes used in</span></span>        | [<span data-ttu-id="69095-151">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="69095-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="69095-152">ADAM</span><span class="sxs-lookup"><span data-stu-id="69095-152">ADAM</span></span>



| <span data-ttu-id="69095-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="69095-153">Entry</span></span> | <span data-ttu-id="69095-154">Value</span><span class="sxs-lookup"><span data-stu-id="69095-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="69095-155">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="69095-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="69095-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69095-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="69095-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="69095-157">System-Only</span></span>            | <span data-ttu-id="69095-158">False</span><span class="sxs-lookup"><span data-stu-id="69095-158">False</span></span>                                                             |
| <span data-ttu-id="69095-159">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="69095-159">Is-Single-Valued</span></span>       | <span data-ttu-id="69095-160">True</span><span class="sxs-lookup"><span data-stu-id="69095-160">True</span></span>                                                              |
| <span data-ttu-id="69095-161">Está indexado</span><span class="sxs-lookup"><span data-stu-id="69095-161">Is Indexed</span></span>             | <span data-ttu-id="69095-162">False</span><span class="sxs-lookup"><span data-stu-id="69095-162">False</span></span>                                                             |
| <span data-ttu-id="69095-163">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="69095-163">In Global Catalog</span></span>      | <span data-ttu-id="69095-164">False</span><span class="sxs-lookup"><span data-stu-id="69095-164">False</span></span>                                                             |
| <span data-ttu-id="69095-165">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="69095-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="69095-166">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69095-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="69095-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69095-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="69095-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69095-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="69095-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69095-169">Search-Flags</span></span>           | <span data-ttu-id="69095-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69095-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="69095-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69095-171">System-Flags</span></span>           | <span data-ttu-id="69095-172">0x00000014</span><span class="sxs-lookup"><span data-stu-id="69095-172">0x00000014</span></span>                                                        |
| <span data-ttu-id="69095-173">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="69095-173">Classes used in</span></span>        | [<span data-ttu-id="69095-174">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="69095-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="69095-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="69095-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="69095-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="69095-176">Entry</span></span> | <span data-ttu-id="69095-177">Value</span><span class="sxs-lookup"><span data-stu-id="69095-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="69095-178">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="69095-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="69095-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69095-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="69095-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="69095-180">System-Only</span></span>            | <span data-ttu-id="69095-181">False</span><span class="sxs-lookup"><span data-stu-id="69095-181">False</span></span>                                                             |
| <span data-ttu-id="69095-182">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="69095-182">Is-Single-Valued</span></span>       | <span data-ttu-id="69095-183">True</span><span class="sxs-lookup"><span data-stu-id="69095-183">True</span></span>                                                              |
| <span data-ttu-id="69095-184">Está indexado</span><span class="sxs-lookup"><span data-stu-id="69095-184">Is Indexed</span></span>             | <span data-ttu-id="69095-185">False</span><span class="sxs-lookup"><span data-stu-id="69095-185">False</span></span>                                                             |
| <span data-ttu-id="69095-186">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="69095-186">In Global Catalog</span></span>      | <span data-ttu-id="69095-187">False</span><span class="sxs-lookup"><span data-stu-id="69095-187">False</span></span>                                                             |
| <span data-ttu-id="69095-188">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="69095-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="69095-189">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69095-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="69095-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69095-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="69095-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69095-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="69095-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69095-192">Search-Flags</span></span>           | <span data-ttu-id="69095-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69095-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="69095-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69095-194">System-Flags</span></span>           | <span data-ttu-id="69095-195">0x00000014</span><span class="sxs-lookup"><span data-stu-id="69095-195">0x00000014</span></span>                                                        |
| <span data-ttu-id="69095-196">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="69095-196">Classes used in</span></span>        | [<span data-ttu-id="69095-197">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="69095-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="69095-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69095-198">Windows Server 2008</span></span>



| <span data-ttu-id="69095-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="69095-199">Entry</span></span> | <span data-ttu-id="69095-200">Value</span><span class="sxs-lookup"><span data-stu-id="69095-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="69095-201">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="69095-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="69095-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69095-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="69095-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="69095-203">System-Only</span></span>            | <span data-ttu-id="69095-204">False</span><span class="sxs-lookup"><span data-stu-id="69095-204">False</span></span>                                                             |
| <span data-ttu-id="69095-205">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="69095-205">Is-Single-Valued</span></span>       | <span data-ttu-id="69095-206">True</span><span class="sxs-lookup"><span data-stu-id="69095-206">True</span></span>                                                              |
| <span data-ttu-id="69095-207">Está indexado</span><span class="sxs-lookup"><span data-stu-id="69095-207">Is Indexed</span></span>             | <span data-ttu-id="69095-208">False</span><span class="sxs-lookup"><span data-stu-id="69095-208">False</span></span>                                                             |
| <span data-ttu-id="69095-209">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="69095-209">In Global Catalog</span></span>      | <span data-ttu-id="69095-210">False</span><span class="sxs-lookup"><span data-stu-id="69095-210">False</span></span>                                                             |
| <span data-ttu-id="69095-211">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="69095-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="69095-212">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69095-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="69095-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69095-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="69095-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69095-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="69095-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69095-215">Search-Flags</span></span>           | <span data-ttu-id="69095-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69095-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="69095-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69095-217">System-Flags</span></span>           | <span data-ttu-id="69095-218">0x00000014</span><span class="sxs-lookup"><span data-stu-id="69095-218">0x00000014</span></span>                                                        |
| <span data-ttu-id="69095-219">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="69095-219">Classes used in</span></span>        | [<span data-ttu-id="69095-220">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="69095-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="69095-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="69095-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="69095-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="69095-222">Entry</span></span> | <span data-ttu-id="69095-223">Value</span><span class="sxs-lookup"><span data-stu-id="69095-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="69095-224">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="69095-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="69095-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69095-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="69095-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="69095-226">System-Only</span></span>            | <span data-ttu-id="69095-227">False</span><span class="sxs-lookup"><span data-stu-id="69095-227">False</span></span>                                                             |
| <span data-ttu-id="69095-228">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="69095-228">Is-Single-Valued</span></span>       | <span data-ttu-id="69095-229">True</span><span class="sxs-lookup"><span data-stu-id="69095-229">True</span></span>                                                              |
| <span data-ttu-id="69095-230">Está indexado</span><span class="sxs-lookup"><span data-stu-id="69095-230">Is Indexed</span></span>             | <span data-ttu-id="69095-231">False</span><span class="sxs-lookup"><span data-stu-id="69095-231">False</span></span>                                                             |
| <span data-ttu-id="69095-232">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="69095-232">In Global Catalog</span></span>      | <span data-ttu-id="69095-233">False</span><span class="sxs-lookup"><span data-stu-id="69095-233">False</span></span>                                                             |
| <span data-ttu-id="69095-234">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="69095-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="69095-235">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69095-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="69095-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69095-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="69095-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69095-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="69095-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69095-238">Search-Flags</span></span>           | <span data-ttu-id="69095-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69095-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="69095-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69095-240">System-Flags</span></span>           | <span data-ttu-id="69095-241">0x00000014</span><span class="sxs-lookup"><span data-stu-id="69095-241">0x00000014</span></span>                                                        |
| <span data-ttu-id="69095-242">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="69095-242">Classes used in</span></span>        | [<span data-ttu-id="69095-243">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="69095-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="69095-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="69095-244">Windows Server 2012</span></span>



| <span data-ttu-id="69095-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="69095-245">Entry</span></span> | <span data-ttu-id="69095-246">Value</span><span class="sxs-lookup"><span data-stu-id="69095-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="69095-247">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="69095-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="69095-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69095-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="69095-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="69095-249">System-Only</span></span>            | <span data-ttu-id="69095-250">False</span><span class="sxs-lookup"><span data-stu-id="69095-250">False</span></span>                                                             |
| <span data-ttu-id="69095-251">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="69095-251">Is-Single-Valued</span></span>       | <span data-ttu-id="69095-252">True</span><span class="sxs-lookup"><span data-stu-id="69095-252">True</span></span>                                                              |
| <span data-ttu-id="69095-253">Está indexado</span><span class="sxs-lookup"><span data-stu-id="69095-253">Is Indexed</span></span>             | <span data-ttu-id="69095-254">False</span><span class="sxs-lookup"><span data-stu-id="69095-254">False</span></span>                                                             |
| <span data-ttu-id="69095-255">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="69095-255">In Global Catalog</span></span>      | <span data-ttu-id="69095-256">False</span><span class="sxs-lookup"><span data-stu-id="69095-256">False</span></span>                                                             |
| <span data-ttu-id="69095-257">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="69095-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="69095-258">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="69095-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="69095-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69095-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="69095-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69095-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="69095-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69095-261">Search-Flags</span></span>           | <span data-ttu-id="69095-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69095-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="69095-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69095-263">System-Flags</span></span>           | <span data-ttu-id="69095-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="69095-264">0x00000014</span></span>                                                        |
| <span data-ttu-id="69095-265">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="69095-265">Classes used in</span></span>        | [<span data-ttu-id="69095-266">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="69095-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





