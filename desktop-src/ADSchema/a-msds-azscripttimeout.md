---
title: atributo MS-DS-AZ-script-timeout
description: Tiempo máximo, en milisegundos, que se esperará a que un script termine de auditar una directiva específica.
ms.assetid: 166d87a3-8768-42d9-9041-21f272059fbf
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-AZ-script-timeout
- Esquema de AD de atributo msDS-AzScriptTimeout
topic_type:
- apiref
api_name:
- ms-DS-Az-Script-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67de4230c3f4710a3eefe6edab896d4fcadcb91
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104422714"
---
# <a name="ms-ds-az-script-timeout-attribute"></a><span data-ttu-id="955ed-105">atributo MS-DS-AZ-script-timeout</span><span class="sxs-lookup"><span data-stu-id="955ed-105">ms-DS-Az-Script-Timeout attribute</span></span>

<span data-ttu-id="955ed-106">Tiempo máximo, en milisegundos, que se esperará a que un script termine de auditar una directiva específica.</span><span class="sxs-lookup"><span data-stu-id="955ed-106">The maximum time, in milliseconds, to wait for a script to finish auditing a specific policy.</span></span>



| <span data-ttu-id="955ed-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="955ed-107">Entry</span></span> | <span data-ttu-id="955ed-108">Value</span><span class="sxs-lookup"><span data-stu-id="955ed-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="955ed-109">CN</span><span class="sxs-lookup"><span data-stu-id="955ed-109">CN</span></span>                | <span data-ttu-id="955ed-110">MS-DS-AZ-script-timeout</span><span class="sxs-lookup"><span data-stu-id="955ed-110">ms-DS-Az-Script-Timeout</span></span>                 |
| <span data-ttu-id="955ed-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="955ed-111">Ldap-Display-Name</span></span> | <span data-ttu-id="955ed-112">msDS-AzScriptTimeout</span><span class="sxs-lookup"><span data-stu-id="955ed-112">msDS-AzScriptTimeout</span></span>                    |
| <span data-ttu-id="955ed-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="955ed-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="955ed-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="955ed-114">Update Privilege</span></span>  | <span data-ttu-id="955ed-115">Administrador de AzRoles</span><span class="sxs-lookup"><span data-stu-id="955ed-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="955ed-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="955ed-116">Update Frequency</span></span>  | <span data-ttu-id="955ed-117">Durante la inicialización o el cambio de directiva.</span><span class="sxs-lookup"><span data-stu-id="955ed-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="955ed-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="955ed-118">Attribute-Id</span></span>      | <span data-ttu-id="955ed-119">1.2.840.113556.1.4.1797</span><span class="sxs-lookup"><span data-stu-id="955ed-119">1.2.840.113556.1.4.1797</span></span>                 |
| <span data-ttu-id="955ed-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="955ed-120">System-Id-Guid</span></span>    | <span data-ttu-id="955ed-121">87d0fb41-2c8b-41f6-b972-11fdfd50d6b0</span><span class="sxs-lookup"><span data-stu-id="955ed-121">87d0fb41-2c8b-41f6-b972-11fdfd50d6b0</span></span>    |
| <span data-ttu-id="955ed-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="955ed-122">Syntax</span></span>            | [<span data-ttu-id="955ed-123">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="955ed-123">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="955ed-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="955ed-124">Implementations</span></span>

-   [<span data-ttu-id="955ed-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="955ed-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="955ed-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="955ed-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="955ed-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="955ed-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="955ed-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="955ed-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="955ed-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="955ed-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="955ed-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="955ed-130">Windows Server 2003</span></span>



| <span data-ttu-id="955ed-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="955ed-131">Entry</span></span> | <span data-ttu-id="955ed-132">Value</span><span class="sxs-lookup"><span data-stu-id="955ed-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="955ed-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="955ed-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="955ed-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="955ed-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="955ed-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="955ed-135">System-Only</span></span>            | <span data-ttu-id="955ed-136">False</span><span class="sxs-lookup"><span data-stu-id="955ed-136">False</span></span>                                                              |
| <span data-ttu-id="955ed-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="955ed-137">Is-Single-Valued</span></span>       | <span data-ttu-id="955ed-138">True</span><span class="sxs-lookup"><span data-stu-id="955ed-138">True</span></span>                                                               |
| <span data-ttu-id="955ed-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="955ed-139">Is Indexed</span></span>             | <span data-ttu-id="955ed-140">False</span><span class="sxs-lookup"><span data-stu-id="955ed-140">False</span></span>                                                              |
| <span data-ttu-id="955ed-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="955ed-141">In Global Catalog</span></span>      | <span data-ttu-id="955ed-142">False</span><span class="sxs-lookup"><span data-stu-id="955ed-142">False</span></span>                                                              |
| <span data-ttu-id="955ed-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="955ed-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="955ed-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="955ed-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="955ed-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="955ed-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="955ed-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="955ed-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="955ed-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="955ed-147">Search-Flags</span></span>           | <span data-ttu-id="955ed-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="955ed-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="955ed-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="955ed-149">System-Flags</span></span>           | <span data-ttu-id="955ed-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="955ed-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="955ed-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="955ed-151">Classes used in</span></span>        | [<span data-ttu-id="955ed-152">**MS-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="955ed-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="955ed-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="955ed-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="955ed-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="955ed-154">Entry</span></span> | <span data-ttu-id="955ed-155">Value</span><span class="sxs-lookup"><span data-stu-id="955ed-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="955ed-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="955ed-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="955ed-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="955ed-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="955ed-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="955ed-158">System-Only</span></span>            | <span data-ttu-id="955ed-159">False</span><span class="sxs-lookup"><span data-stu-id="955ed-159">False</span></span>                                                              |
| <span data-ttu-id="955ed-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="955ed-160">Is-Single-Valued</span></span>       | <span data-ttu-id="955ed-161">True</span><span class="sxs-lookup"><span data-stu-id="955ed-161">True</span></span>                                                               |
| <span data-ttu-id="955ed-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="955ed-162">Is Indexed</span></span>             | <span data-ttu-id="955ed-163">False</span><span class="sxs-lookup"><span data-stu-id="955ed-163">False</span></span>                                                              |
| <span data-ttu-id="955ed-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="955ed-164">In Global Catalog</span></span>      | <span data-ttu-id="955ed-165">False</span><span class="sxs-lookup"><span data-stu-id="955ed-165">False</span></span>                                                              |
| <span data-ttu-id="955ed-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="955ed-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="955ed-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="955ed-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="955ed-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="955ed-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="955ed-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="955ed-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="955ed-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="955ed-170">Search-Flags</span></span>           | <span data-ttu-id="955ed-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="955ed-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="955ed-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="955ed-172">System-Flags</span></span>           | <span data-ttu-id="955ed-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="955ed-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="955ed-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="955ed-174">Classes used in</span></span>        | [<span data-ttu-id="955ed-175">**MS-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="955ed-175">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="955ed-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="955ed-176">Windows Server 2008</span></span>



| <span data-ttu-id="955ed-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="955ed-177">Entry</span></span> | <span data-ttu-id="955ed-178">Value</span><span class="sxs-lookup"><span data-stu-id="955ed-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="955ed-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="955ed-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="955ed-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="955ed-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="955ed-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="955ed-181">System-Only</span></span>            | <span data-ttu-id="955ed-182">False</span><span class="sxs-lookup"><span data-stu-id="955ed-182">False</span></span>                                                              |
| <span data-ttu-id="955ed-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="955ed-183">Is-Single-Valued</span></span>       | <span data-ttu-id="955ed-184">True</span><span class="sxs-lookup"><span data-stu-id="955ed-184">True</span></span>                                                               |
| <span data-ttu-id="955ed-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="955ed-185">Is Indexed</span></span>             | <span data-ttu-id="955ed-186">False</span><span class="sxs-lookup"><span data-stu-id="955ed-186">False</span></span>                                                              |
| <span data-ttu-id="955ed-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="955ed-187">In Global Catalog</span></span>      | <span data-ttu-id="955ed-188">False</span><span class="sxs-lookup"><span data-stu-id="955ed-188">False</span></span>                                                              |
| <span data-ttu-id="955ed-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="955ed-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="955ed-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="955ed-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="955ed-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="955ed-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="955ed-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="955ed-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="955ed-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="955ed-193">Search-Flags</span></span>           | <span data-ttu-id="955ed-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="955ed-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="955ed-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="955ed-195">System-Flags</span></span>           | <span data-ttu-id="955ed-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="955ed-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="955ed-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="955ed-197">Classes used in</span></span>        | [<span data-ttu-id="955ed-198">**MS-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="955ed-198">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="955ed-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="955ed-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="955ed-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="955ed-200">Entry</span></span> | <span data-ttu-id="955ed-201">Value</span><span class="sxs-lookup"><span data-stu-id="955ed-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="955ed-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="955ed-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="955ed-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="955ed-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="955ed-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="955ed-204">System-Only</span></span>            | <span data-ttu-id="955ed-205">False</span><span class="sxs-lookup"><span data-stu-id="955ed-205">False</span></span>                                                              |
| <span data-ttu-id="955ed-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="955ed-206">Is-Single-Valued</span></span>       | <span data-ttu-id="955ed-207">True</span><span class="sxs-lookup"><span data-stu-id="955ed-207">True</span></span>                                                               |
| <span data-ttu-id="955ed-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="955ed-208">Is Indexed</span></span>             | <span data-ttu-id="955ed-209">False</span><span class="sxs-lookup"><span data-stu-id="955ed-209">False</span></span>                                                              |
| <span data-ttu-id="955ed-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="955ed-210">In Global Catalog</span></span>      | <span data-ttu-id="955ed-211">False</span><span class="sxs-lookup"><span data-stu-id="955ed-211">False</span></span>                                                              |
| <span data-ttu-id="955ed-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="955ed-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="955ed-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="955ed-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="955ed-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="955ed-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="955ed-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="955ed-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="955ed-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="955ed-216">Search-Flags</span></span>           | <span data-ttu-id="955ed-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="955ed-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="955ed-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="955ed-218">System-Flags</span></span>           | <span data-ttu-id="955ed-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="955ed-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="955ed-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="955ed-220">Classes used in</span></span>        | [<span data-ttu-id="955ed-221">**MS-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="955ed-221">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="955ed-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="955ed-222">Windows Server 2012</span></span>



| <span data-ttu-id="955ed-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="955ed-223">Entry</span></span> | <span data-ttu-id="955ed-224">Value</span><span class="sxs-lookup"><span data-stu-id="955ed-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="955ed-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="955ed-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="955ed-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="955ed-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="955ed-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="955ed-227">System-Only</span></span>            | <span data-ttu-id="955ed-228">False</span><span class="sxs-lookup"><span data-stu-id="955ed-228">False</span></span>                                                              |
| <span data-ttu-id="955ed-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="955ed-229">Is-Single-Valued</span></span>       | <span data-ttu-id="955ed-230">True</span><span class="sxs-lookup"><span data-stu-id="955ed-230">True</span></span>                                                               |
| <span data-ttu-id="955ed-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="955ed-231">Is Indexed</span></span>             | <span data-ttu-id="955ed-232">False</span><span class="sxs-lookup"><span data-stu-id="955ed-232">False</span></span>                                                              |
| <span data-ttu-id="955ed-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="955ed-233">In Global Catalog</span></span>      | <span data-ttu-id="955ed-234">False</span><span class="sxs-lookup"><span data-stu-id="955ed-234">False</span></span>                                                              |
| <span data-ttu-id="955ed-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="955ed-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="955ed-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="955ed-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="955ed-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="955ed-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="955ed-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="955ed-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="955ed-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="955ed-239">Search-Flags</span></span>           | <span data-ttu-id="955ed-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="955ed-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="955ed-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="955ed-241">System-Flags</span></span>           | <span data-ttu-id="955ed-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="955ed-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="955ed-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="955ed-243">Classes used in</span></span>        | [<span data-ttu-id="955ed-244">**MS-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="955ed-244">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



 

 





