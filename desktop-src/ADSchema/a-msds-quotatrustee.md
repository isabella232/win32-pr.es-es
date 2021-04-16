---
title: atributo MS-DS-quota-Trustee
description: SID de la entidad de seguridad a la que se asigna la cuota.
ms.assetid: 4da8f731-0a8f-4d8a-a4e7-81ed881a30b5
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-quota-Trustee
- Esquema de AD de atributo msDS-QuotaTrustee
topic_type:
- apiref
api_name:
- ms-DS-Quota-Trustee
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7733e74c2f5d381aa6f52ea58bb03c377fab7cbe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658858"
---
# <a name="ms-ds-quota-trustee-attribute"></a><span data-ttu-id="afb1a-105">atributo MS-DS-quota-Trustee</span><span class="sxs-lookup"><span data-stu-id="afb1a-105">ms-DS-Quota-Trustee attribute</span></span>

<span data-ttu-id="afb1a-106">SID de la entidad de seguridad a la que se asigna la cuota.</span><span class="sxs-lookup"><span data-stu-id="afb1a-106">The SID of the security principal for which the quota is being assigned.</span></span>



| <span data-ttu-id="afb1a-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="afb1a-107">Entry</span></span> | <span data-ttu-id="afb1a-108">Value</span><span class="sxs-lookup"><span data-stu-id="afb1a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="afb1a-109">CN</span><span class="sxs-lookup"><span data-stu-id="afb1a-109">CN</span></span>                | <span data-ttu-id="afb1a-110">MS-DS-quota-Trustee</span><span class="sxs-lookup"><span data-stu-id="afb1a-110">ms-DS-Quota-Trustee</span></span>                  |
| <span data-ttu-id="afb1a-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="afb1a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="afb1a-112">msDS-QuotaTrustee</span><span class="sxs-lookup"><span data-stu-id="afb1a-112">msDS-QuotaTrustee</span></span>                    |
| <span data-ttu-id="afb1a-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="afb1a-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="afb1a-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="afb1a-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="afb1a-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="afb1a-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="afb1a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="afb1a-116">Attribute-Id</span></span>      | <span data-ttu-id="afb1a-117">1.2.840.113556.1.4.1844</span><span class="sxs-lookup"><span data-stu-id="afb1a-117">1.2.840.113556.1.4.1844</span></span>              |
| <span data-ttu-id="afb1a-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="afb1a-118">System-Id-Guid</span></span>    | <span data-ttu-id="afb1a-119">16378906-4ea5-49be-a8d1-bfd41dff4f65</span><span class="sxs-lookup"><span data-stu-id="afb1a-119">16378906-4ea5-49be-a8d1-bfd41dff4f65</span></span> |
| <span data-ttu-id="afb1a-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="afb1a-120">Syntax</span></span>            | [<span data-ttu-id="afb1a-121">**Cadena (SID)**</span><span class="sxs-lookup"><span data-stu-id="afb1a-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="afb1a-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="afb1a-122">Implementations</span></span>

-   [<span data-ttu-id="afb1a-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="afb1a-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="afb1a-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="afb1a-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="afb1a-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="afb1a-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="afb1a-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="afb1a-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="afb1a-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="afb1a-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="afb1a-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="afb1a-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="afb1a-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="afb1a-129">Windows Server 2003</span></span>



| <span data-ttu-id="afb1a-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="afb1a-130">Entry</span></span> | <span data-ttu-id="afb1a-131">Value</span><span class="sxs-lookup"><span data-stu-id="afb1a-131">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="afb1a-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="afb1a-132">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="afb1a-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afb1a-133">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="afb1a-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="afb1a-134">System-Only</span></span>            | <span data-ttu-id="afb1a-135">False</span><span class="sxs-lookup"><span data-stu-id="afb1a-135">False</span></span>                                                         |
| <span data-ttu-id="afb1a-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="afb1a-136">Is-Single-Valued</span></span>       | <span data-ttu-id="afb1a-137">True</span><span class="sxs-lookup"><span data-stu-id="afb1a-137">True</span></span>                                                          |
| <span data-ttu-id="afb1a-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="afb1a-138">Is Indexed</span></span>             | <span data-ttu-id="afb1a-139">False</span><span class="sxs-lookup"><span data-stu-id="afb1a-139">False</span></span>                                                         |
| <span data-ttu-id="afb1a-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="afb1a-140">In Global Catalog</span></span>      | <span data-ttu-id="afb1a-141">False</span><span class="sxs-lookup"><span data-stu-id="afb1a-141">False</span></span>                                                         |
| <span data-ttu-id="afb1a-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="afb1a-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="afb1a-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afb1a-143">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="afb1a-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afb1a-144">Range-Lower</span></span>            | <span data-ttu-id="afb1a-145">0</span><span class="sxs-lookup"><span data-stu-id="afb1a-145">0</span></span>                                                             |
| <span data-ttu-id="afb1a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afb1a-146">Range-Upper</span></span>            | <span data-ttu-id="afb1a-147">28</span><span class="sxs-lookup"><span data-stu-id="afb1a-147">28</span></span>                                                            |
| <span data-ttu-id="afb1a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afb1a-148">Search-Flags</span></span>           | <span data-ttu-id="afb1a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afb1a-149">0x00000000</span></span>                                                    |
| <span data-ttu-id="afb1a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afb1a-150">System-Flags</span></span>           | <span data-ttu-id="afb1a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afb1a-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="afb1a-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="afb1a-152">Classes used in</span></span>        | [<span data-ttu-id="afb1a-153">**Control de cuota MS-DS**</span><span class="sxs-lookup"><span data-stu-id="afb1a-153">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="adam"></a><span data-ttu-id="afb1a-154">ADAM</span><span class="sxs-lookup"><span data-stu-id="afb1a-154">ADAM</span></span>



| <span data-ttu-id="afb1a-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="afb1a-155">Entry</span></span> | <span data-ttu-id="afb1a-156">Value</span><span class="sxs-lookup"><span data-stu-id="afb1a-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="afb1a-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="afb1a-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="afb1a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afb1a-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="afb1a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="afb1a-159">System-Only</span></span>            | <span data-ttu-id="afb1a-160">False</span><span class="sxs-lookup"><span data-stu-id="afb1a-160">False</span></span>                                                         |
| <span data-ttu-id="afb1a-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="afb1a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="afb1a-162">True</span><span class="sxs-lookup"><span data-stu-id="afb1a-162">True</span></span>                                                          |
| <span data-ttu-id="afb1a-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="afb1a-163">Is Indexed</span></span>             | <span data-ttu-id="afb1a-164">False</span><span class="sxs-lookup"><span data-stu-id="afb1a-164">False</span></span>                                                         |
| <span data-ttu-id="afb1a-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="afb1a-165">In Global Catalog</span></span>      | <span data-ttu-id="afb1a-166">False</span><span class="sxs-lookup"><span data-stu-id="afb1a-166">False</span></span>                                                         |
| <span data-ttu-id="afb1a-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="afb1a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="afb1a-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afb1a-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="afb1a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afb1a-169">Range-Lower</span></span>            | <span data-ttu-id="afb1a-170">0</span><span class="sxs-lookup"><span data-stu-id="afb1a-170">0</span></span>                                                             |
| <span data-ttu-id="afb1a-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afb1a-171">Range-Upper</span></span>            | <span data-ttu-id="afb1a-172">28</span><span class="sxs-lookup"><span data-stu-id="afb1a-172">28</span></span>                                                            |
| <span data-ttu-id="afb1a-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afb1a-173">Search-Flags</span></span>           | <span data-ttu-id="afb1a-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afb1a-174">0x00000000</span></span>                                                    |
| <span data-ttu-id="afb1a-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afb1a-175">System-Flags</span></span>           | <span data-ttu-id="afb1a-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afb1a-176">0x00000010</span></span>                                                    |
| <span data-ttu-id="afb1a-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="afb1a-177">Classes used in</span></span>        | [<span data-ttu-id="afb1a-178">**Control de cuota MS-DS**</span><span class="sxs-lookup"><span data-stu-id="afb1a-178">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="afb1a-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="afb1a-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="afb1a-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="afb1a-180">Entry</span></span> | <span data-ttu-id="afb1a-181">Value</span><span class="sxs-lookup"><span data-stu-id="afb1a-181">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="afb1a-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="afb1a-182">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="afb1a-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afb1a-183">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="afb1a-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="afb1a-184">System-Only</span></span>            | <span data-ttu-id="afb1a-185">False</span><span class="sxs-lookup"><span data-stu-id="afb1a-185">False</span></span>                                                         |
| <span data-ttu-id="afb1a-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="afb1a-186">Is-Single-Valued</span></span>       | <span data-ttu-id="afb1a-187">True</span><span class="sxs-lookup"><span data-stu-id="afb1a-187">True</span></span>                                                          |
| <span data-ttu-id="afb1a-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="afb1a-188">Is Indexed</span></span>             | <span data-ttu-id="afb1a-189">False</span><span class="sxs-lookup"><span data-stu-id="afb1a-189">False</span></span>                                                         |
| <span data-ttu-id="afb1a-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="afb1a-190">In Global Catalog</span></span>      | <span data-ttu-id="afb1a-191">False</span><span class="sxs-lookup"><span data-stu-id="afb1a-191">False</span></span>                                                         |
| <span data-ttu-id="afb1a-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="afb1a-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="afb1a-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afb1a-193">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="afb1a-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afb1a-194">Range-Lower</span></span>            | <span data-ttu-id="afb1a-195">0</span><span class="sxs-lookup"><span data-stu-id="afb1a-195">0</span></span>                                                             |
| <span data-ttu-id="afb1a-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afb1a-196">Range-Upper</span></span>            | <span data-ttu-id="afb1a-197">28</span><span class="sxs-lookup"><span data-stu-id="afb1a-197">28</span></span>                                                            |
| <span data-ttu-id="afb1a-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afb1a-198">Search-Flags</span></span>           | <span data-ttu-id="afb1a-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afb1a-199">0x00000000</span></span>                                                    |
| <span data-ttu-id="afb1a-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afb1a-200">System-Flags</span></span>           | <span data-ttu-id="afb1a-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afb1a-201">0x00000010</span></span>                                                    |
| <span data-ttu-id="afb1a-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="afb1a-202">Classes used in</span></span>        | [<span data-ttu-id="afb1a-203">**Control de cuota MS-DS**</span><span class="sxs-lookup"><span data-stu-id="afb1a-203">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="afb1a-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afb1a-204">Windows Server 2008</span></span>



| <span data-ttu-id="afb1a-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="afb1a-205">Entry</span></span> | <span data-ttu-id="afb1a-206">Value</span><span class="sxs-lookup"><span data-stu-id="afb1a-206">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="afb1a-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="afb1a-207">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="afb1a-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afb1a-208">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="afb1a-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="afb1a-209">System-Only</span></span>            | <span data-ttu-id="afb1a-210">False</span><span class="sxs-lookup"><span data-stu-id="afb1a-210">False</span></span>                                                         |
| <span data-ttu-id="afb1a-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="afb1a-211">Is-Single-Valued</span></span>       | <span data-ttu-id="afb1a-212">True</span><span class="sxs-lookup"><span data-stu-id="afb1a-212">True</span></span>                                                          |
| <span data-ttu-id="afb1a-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="afb1a-213">Is Indexed</span></span>             | <span data-ttu-id="afb1a-214">False</span><span class="sxs-lookup"><span data-stu-id="afb1a-214">False</span></span>                                                         |
| <span data-ttu-id="afb1a-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="afb1a-215">In Global Catalog</span></span>      | <span data-ttu-id="afb1a-216">False</span><span class="sxs-lookup"><span data-stu-id="afb1a-216">False</span></span>                                                         |
| <span data-ttu-id="afb1a-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="afb1a-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="afb1a-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afb1a-218">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="afb1a-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afb1a-219">Range-Lower</span></span>            | <span data-ttu-id="afb1a-220">0</span><span class="sxs-lookup"><span data-stu-id="afb1a-220">0</span></span>                                                             |
| <span data-ttu-id="afb1a-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afb1a-221">Range-Upper</span></span>            | <span data-ttu-id="afb1a-222">28</span><span class="sxs-lookup"><span data-stu-id="afb1a-222">28</span></span>                                                            |
| <span data-ttu-id="afb1a-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afb1a-223">Search-Flags</span></span>           | <span data-ttu-id="afb1a-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afb1a-224">0x00000000</span></span>                                                    |
| <span data-ttu-id="afb1a-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afb1a-225">System-Flags</span></span>           | <span data-ttu-id="afb1a-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afb1a-226">0x00000010</span></span>                                                    |
| <span data-ttu-id="afb1a-227">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="afb1a-227">Classes used in</span></span>        | [<span data-ttu-id="afb1a-228">**Control de cuota MS-DS**</span><span class="sxs-lookup"><span data-stu-id="afb1a-228">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="afb1a-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="afb1a-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="afb1a-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="afb1a-230">Entry</span></span> | <span data-ttu-id="afb1a-231">Value</span><span class="sxs-lookup"><span data-stu-id="afb1a-231">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="afb1a-232">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="afb1a-232">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="afb1a-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afb1a-233">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="afb1a-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="afb1a-234">System-Only</span></span>            | <span data-ttu-id="afb1a-235">False</span><span class="sxs-lookup"><span data-stu-id="afb1a-235">False</span></span>                                                         |
| <span data-ttu-id="afb1a-236">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="afb1a-236">Is-Single-Valued</span></span>       | <span data-ttu-id="afb1a-237">True</span><span class="sxs-lookup"><span data-stu-id="afb1a-237">True</span></span>                                                          |
| <span data-ttu-id="afb1a-238">Está indexado</span><span class="sxs-lookup"><span data-stu-id="afb1a-238">Is Indexed</span></span>             | <span data-ttu-id="afb1a-239">False</span><span class="sxs-lookup"><span data-stu-id="afb1a-239">False</span></span>                                                         |
| <span data-ttu-id="afb1a-240">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="afb1a-240">In Global Catalog</span></span>      | <span data-ttu-id="afb1a-241">False</span><span class="sxs-lookup"><span data-stu-id="afb1a-241">False</span></span>                                                         |
| <span data-ttu-id="afb1a-242">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="afb1a-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="afb1a-243">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afb1a-243">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="afb1a-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afb1a-244">Range-Lower</span></span>            | <span data-ttu-id="afb1a-245">0</span><span class="sxs-lookup"><span data-stu-id="afb1a-245">0</span></span>                                                             |
| <span data-ttu-id="afb1a-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afb1a-246">Range-Upper</span></span>            | <span data-ttu-id="afb1a-247">28</span><span class="sxs-lookup"><span data-stu-id="afb1a-247">28</span></span>                                                            |
| <span data-ttu-id="afb1a-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afb1a-248">Search-Flags</span></span>           | <span data-ttu-id="afb1a-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afb1a-249">0x00000000</span></span>                                                    |
| <span data-ttu-id="afb1a-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afb1a-250">System-Flags</span></span>           | <span data-ttu-id="afb1a-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afb1a-251">0x00000010</span></span>                                                    |
| <span data-ttu-id="afb1a-252">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="afb1a-252">Classes used in</span></span>        | [<span data-ttu-id="afb1a-253">**Control de cuota MS-DS**</span><span class="sxs-lookup"><span data-stu-id="afb1a-253">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="afb1a-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="afb1a-254">Windows Server 2012</span></span>



| <span data-ttu-id="afb1a-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="afb1a-255">Entry</span></span> | <span data-ttu-id="afb1a-256">Value</span><span class="sxs-lookup"><span data-stu-id="afb1a-256">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="afb1a-257">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="afb1a-257">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="afb1a-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afb1a-258">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="afb1a-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="afb1a-259">System-Only</span></span>            | <span data-ttu-id="afb1a-260">False</span><span class="sxs-lookup"><span data-stu-id="afb1a-260">False</span></span>                                                         |
| <span data-ttu-id="afb1a-261">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="afb1a-261">Is-Single-Valued</span></span>       | <span data-ttu-id="afb1a-262">True</span><span class="sxs-lookup"><span data-stu-id="afb1a-262">True</span></span>                                                          |
| <span data-ttu-id="afb1a-263">Está indexado</span><span class="sxs-lookup"><span data-stu-id="afb1a-263">Is Indexed</span></span>             | <span data-ttu-id="afb1a-264">False</span><span class="sxs-lookup"><span data-stu-id="afb1a-264">False</span></span>                                                         |
| <span data-ttu-id="afb1a-265">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="afb1a-265">In Global Catalog</span></span>      | <span data-ttu-id="afb1a-266">False</span><span class="sxs-lookup"><span data-stu-id="afb1a-266">False</span></span>                                                         |
| <span data-ttu-id="afb1a-267">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="afb1a-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="afb1a-268">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afb1a-268">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="afb1a-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afb1a-269">Range-Lower</span></span>            | <span data-ttu-id="afb1a-270">0</span><span class="sxs-lookup"><span data-stu-id="afb1a-270">0</span></span>                                                             |
| <span data-ttu-id="afb1a-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afb1a-271">Range-Upper</span></span>            | <span data-ttu-id="afb1a-272">28</span><span class="sxs-lookup"><span data-stu-id="afb1a-272">28</span></span>                                                            |
| <span data-ttu-id="afb1a-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afb1a-273">Search-Flags</span></span>           | <span data-ttu-id="afb1a-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afb1a-274">0x00000000</span></span>                                                    |
| <span data-ttu-id="afb1a-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afb1a-275">System-Flags</span></span>           | <span data-ttu-id="afb1a-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afb1a-276">0x00000010</span></span>                                                    |
| <span data-ttu-id="afb1a-277">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="afb1a-277">Classes used in</span></span>        | [<span data-ttu-id="afb1a-278">**Control de cuota MS-DS**</span><span class="sxs-lookup"><span data-stu-id="afb1a-278">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



 

 





