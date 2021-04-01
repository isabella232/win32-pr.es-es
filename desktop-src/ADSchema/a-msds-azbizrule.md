---
title: atributo MS-DS-AZ-BIZ-Rule
description: Texto del script que implementa la regla de negocios.
ms.assetid: 884513ae-9600-49b0-a371-6f77b84b54f9
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-AZ-BIZ-Rule
- Esquema de AD de atributo msDS-AzBizRule
topic_type:
- apiref
api_name:
- ms-DS-Az-Biz-Rule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 571ab48c9742ffb93015c433685c01cb3a9666d3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151824"
---
# <a name="ms-ds-az-biz-rule-attribute"></a><span data-ttu-id="01a13-105">atributo MS-DS-AZ-BIZ-Rule</span><span class="sxs-lookup"><span data-stu-id="01a13-105">ms-DS-Az-Biz-Rule attribute</span></span>

<span data-ttu-id="01a13-106">Texto del script que implementa la regla de negocios.</span><span class="sxs-lookup"><span data-stu-id="01a13-106">Text of the script implementing the business rule.</span></span>



| <span data-ttu-id="01a13-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="01a13-107">Entry</span></span> | <span data-ttu-id="01a13-108">Value</span><span class="sxs-lookup"><span data-stu-id="01a13-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="01a13-109">CN</span><span class="sxs-lookup"><span data-stu-id="01a13-109">CN</span></span>                | <span data-ttu-id="01a13-110">MS-DS-AZ-BIZ-Rule</span><span class="sxs-lookup"><span data-stu-id="01a13-110">ms-DS-Az-Biz-Rule</span></span>                           |
| <span data-ttu-id="01a13-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="01a13-111">Ldap-Display-Name</span></span> | <span data-ttu-id="01a13-112">msDS-AzBizRule</span><span class="sxs-lookup"><span data-stu-id="01a13-112">msDS-AzBizRule</span></span>                              |
| <span data-ttu-id="01a13-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="01a13-113">Size</span></span>              | <span data-ttu-id="01a13-114">128 caracteres</span><span class="sxs-lookup"><span data-stu-id="01a13-114">128 characters</span></span>                              |
| <span data-ttu-id="01a13-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="01a13-115">Update Privilege</span></span>  | <span data-ttu-id="01a13-116">Administrador de AzRoles</span><span class="sxs-lookup"><span data-stu-id="01a13-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="01a13-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="01a13-117">Update Frequency</span></span>  | <span data-ttu-id="01a13-118">Durante la inicialización o el cambio de directiva.</span><span class="sxs-lookup"><span data-stu-id="01a13-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="01a13-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="01a13-119">Attribute-Id</span></span>      | <span data-ttu-id="01a13-120">1.2.840.113556.1.4.1801</span><span class="sxs-lookup"><span data-stu-id="01a13-120">1.2.840.113556.1.4.1801</span></span>                     |
| <span data-ttu-id="01a13-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="01a13-121">System-Id-Guid</span></span>    | <span data-ttu-id="01a13-122">33d41ea8-c0c9-4c92-9494-f104878413fd</span><span class="sxs-lookup"><span data-stu-id="01a13-122">33d41ea8-c0c9-4c92-9494-f104878413fd</span></span>        |
| <span data-ttu-id="01a13-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01a13-123">Syntax</span></span>            | [<span data-ttu-id="01a13-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="01a13-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="01a13-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="01a13-125">Implementations</span></span>

-   [<span data-ttu-id="01a13-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="01a13-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="01a13-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="01a13-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="01a13-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="01a13-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="01a13-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="01a13-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="01a13-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="01a13-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="01a13-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="01a13-131">Windows Server 2003</span></span>



| <span data-ttu-id="01a13-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="01a13-132">Entry</span></span> | <span data-ttu-id="01a13-133">Value</span><span class="sxs-lookup"><span data-stu-id="01a13-133">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="01a13-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="01a13-134">Link-Id</span></span>                | \-                                                |
| <span data-ttu-id="01a13-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01a13-135">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="01a13-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="01a13-136">System-Only</span></span>            | <span data-ttu-id="01a13-137">False</span><span class="sxs-lookup"><span data-stu-id="01a13-137">False</span></span>                                             |
| <span data-ttu-id="01a13-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="01a13-138">Is-Single-Valued</span></span>       | <span data-ttu-id="01a13-139">True</span><span class="sxs-lookup"><span data-stu-id="01a13-139">True</span></span>                                              |
| <span data-ttu-id="01a13-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="01a13-140">Is Indexed</span></span>             | <span data-ttu-id="01a13-141">False</span><span class="sxs-lookup"><span data-stu-id="01a13-141">False</span></span>                                             |
| <span data-ttu-id="01a13-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="01a13-142">In Global Catalog</span></span>      | <span data-ttu-id="01a13-143">False</span><span class="sxs-lookup"><span data-stu-id="01a13-143">False</span></span>                                             |
| <span data-ttu-id="01a13-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="01a13-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="01a13-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="01a13-145">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="01a13-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01a13-146">Range-Lower</span></span>            | <span data-ttu-id="01a13-147">0</span><span class="sxs-lookup"><span data-stu-id="01a13-147">0</span></span>                                                 |
| <span data-ttu-id="01a13-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01a13-148">Range-Upper</span></span>            | <span data-ttu-id="01a13-149">65536</span><span class="sxs-lookup"><span data-stu-id="01a13-149">65536</span></span>                                             |
| <span data-ttu-id="01a13-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01a13-150">Search-Flags</span></span>           | <span data-ttu-id="01a13-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01a13-151">0x00000000</span></span>                                        |
| <span data-ttu-id="01a13-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01a13-152">System-Flags</span></span>           | <span data-ttu-id="01a13-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01a13-153">0x00000010</span></span>                                        |
| <span data-ttu-id="01a13-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="01a13-154">Classes used in</span></span>        | [<span data-ttu-id="01a13-155">**MS-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="01a13-155">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="01a13-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="01a13-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="01a13-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="01a13-157">Entry</span></span> | <span data-ttu-id="01a13-158">Value</span><span class="sxs-lookup"><span data-stu-id="01a13-158">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="01a13-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="01a13-159">Link-Id</span></span>                | \-                                                |
| <span data-ttu-id="01a13-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01a13-160">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="01a13-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="01a13-161">System-Only</span></span>            | <span data-ttu-id="01a13-162">False</span><span class="sxs-lookup"><span data-stu-id="01a13-162">False</span></span>                                             |
| <span data-ttu-id="01a13-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="01a13-163">Is-Single-Valued</span></span>       | <span data-ttu-id="01a13-164">True</span><span class="sxs-lookup"><span data-stu-id="01a13-164">True</span></span>                                              |
| <span data-ttu-id="01a13-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="01a13-165">Is Indexed</span></span>             | <span data-ttu-id="01a13-166">False</span><span class="sxs-lookup"><span data-stu-id="01a13-166">False</span></span>                                             |
| <span data-ttu-id="01a13-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="01a13-167">In Global Catalog</span></span>      | <span data-ttu-id="01a13-168">False</span><span class="sxs-lookup"><span data-stu-id="01a13-168">False</span></span>                                             |
| <span data-ttu-id="01a13-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="01a13-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="01a13-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="01a13-170">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="01a13-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01a13-171">Range-Lower</span></span>            | <span data-ttu-id="01a13-172">0</span><span class="sxs-lookup"><span data-stu-id="01a13-172">0</span></span>                                                 |
| <span data-ttu-id="01a13-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01a13-173">Range-Upper</span></span>            | <span data-ttu-id="01a13-174">65536</span><span class="sxs-lookup"><span data-stu-id="01a13-174">65536</span></span>                                             |
| <span data-ttu-id="01a13-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01a13-175">Search-Flags</span></span>           | <span data-ttu-id="01a13-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01a13-176">0x00000000</span></span>                                        |
| <span data-ttu-id="01a13-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01a13-177">System-Flags</span></span>           | <span data-ttu-id="01a13-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01a13-178">0x00000010</span></span>                                        |
| <span data-ttu-id="01a13-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="01a13-179">Classes used in</span></span>        | [<span data-ttu-id="01a13-180">**MS-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="01a13-180">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="01a13-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01a13-181">Windows Server 2008</span></span>



| <span data-ttu-id="01a13-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="01a13-182">Entry</span></span> | <span data-ttu-id="01a13-183">Value</span><span class="sxs-lookup"><span data-stu-id="01a13-183">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01a13-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="01a13-184">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="01a13-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01a13-185">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="01a13-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="01a13-186">System-Only</span></span>            | <span data-ttu-id="01a13-187">False</span><span class="sxs-lookup"><span data-stu-id="01a13-187">False</span></span>                                                                                 |
| <span data-ttu-id="01a13-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="01a13-188">Is-Single-Valued</span></span>       | <span data-ttu-id="01a13-189">True</span><span class="sxs-lookup"><span data-stu-id="01a13-189">True</span></span>                                                                                  |
| <span data-ttu-id="01a13-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="01a13-190">Is Indexed</span></span>             | <span data-ttu-id="01a13-191">False</span><span class="sxs-lookup"><span data-stu-id="01a13-191">False</span></span>                                                                                 |
| <span data-ttu-id="01a13-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="01a13-192">In Global Catalog</span></span>      | <span data-ttu-id="01a13-193">False</span><span class="sxs-lookup"><span data-stu-id="01a13-193">False</span></span>                                                                                 |
| <span data-ttu-id="01a13-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="01a13-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="01a13-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="01a13-195">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="01a13-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01a13-196">Range-Lower</span></span>            | <span data-ttu-id="01a13-197">0</span><span class="sxs-lookup"><span data-stu-id="01a13-197">0</span></span>                                                                                     |
| <span data-ttu-id="01a13-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01a13-198">Range-Upper</span></span>            | <span data-ttu-id="01a13-199">65536</span><span class="sxs-lookup"><span data-stu-id="01a13-199">65536</span></span>                                                                                 |
| <span data-ttu-id="01a13-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01a13-200">Search-Flags</span></span>           | <span data-ttu-id="01a13-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01a13-201">0x00000000</span></span>                                                                            |
| <span data-ttu-id="01a13-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01a13-202">System-Flags</span></span>           | <span data-ttu-id="01a13-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01a13-203">0x00000010</span></span>                                                                            |
| <span data-ttu-id="01a13-204">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="01a13-204">Classes used in</span></span>        | [<span data-ttu-id="01a13-205">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="01a13-205">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="01a13-206">**MS-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="01a13-206">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="01a13-207">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="01a13-207">Windows Server 2008 R2</span></span>



| <span data-ttu-id="01a13-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="01a13-208">Entry</span></span> | <span data-ttu-id="01a13-209">Value</span><span class="sxs-lookup"><span data-stu-id="01a13-209">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01a13-210">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="01a13-210">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="01a13-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01a13-211">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="01a13-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="01a13-212">System-Only</span></span>            | <span data-ttu-id="01a13-213">False</span><span class="sxs-lookup"><span data-stu-id="01a13-213">False</span></span>                                                                                 |
| <span data-ttu-id="01a13-214">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="01a13-214">Is-Single-Valued</span></span>       | <span data-ttu-id="01a13-215">True</span><span class="sxs-lookup"><span data-stu-id="01a13-215">True</span></span>                                                                                  |
| <span data-ttu-id="01a13-216">Está indexado</span><span class="sxs-lookup"><span data-stu-id="01a13-216">Is Indexed</span></span>             | <span data-ttu-id="01a13-217">False</span><span class="sxs-lookup"><span data-stu-id="01a13-217">False</span></span>                                                                                 |
| <span data-ttu-id="01a13-218">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="01a13-218">In Global Catalog</span></span>      | <span data-ttu-id="01a13-219">False</span><span class="sxs-lookup"><span data-stu-id="01a13-219">False</span></span>                                                                                 |
| <span data-ttu-id="01a13-220">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="01a13-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="01a13-221">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="01a13-221">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="01a13-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01a13-222">Range-Lower</span></span>            | <span data-ttu-id="01a13-223">0</span><span class="sxs-lookup"><span data-stu-id="01a13-223">0</span></span>                                                                                     |
| <span data-ttu-id="01a13-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01a13-224">Range-Upper</span></span>            | <span data-ttu-id="01a13-225">65536</span><span class="sxs-lookup"><span data-stu-id="01a13-225">65536</span></span>                                                                                 |
| <span data-ttu-id="01a13-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01a13-226">Search-Flags</span></span>           | <span data-ttu-id="01a13-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01a13-227">0x00000000</span></span>                                                                            |
| <span data-ttu-id="01a13-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01a13-228">System-Flags</span></span>           | <span data-ttu-id="01a13-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01a13-229">0x00000010</span></span>                                                                            |
| <span data-ttu-id="01a13-230">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="01a13-230">Classes used in</span></span>        | [<span data-ttu-id="01a13-231">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="01a13-231">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="01a13-232">**MS-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="01a13-232">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="01a13-233">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="01a13-233">Windows Server 2012</span></span>



| <span data-ttu-id="01a13-234">Entrada</span><span class="sxs-lookup"><span data-stu-id="01a13-234">Entry</span></span> | <span data-ttu-id="01a13-235">Value</span><span class="sxs-lookup"><span data-stu-id="01a13-235">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01a13-236">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="01a13-236">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="01a13-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01a13-237">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="01a13-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="01a13-238">System-Only</span></span>            | <span data-ttu-id="01a13-239">False</span><span class="sxs-lookup"><span data-stu-id="01a13-239">False</span></span>                                                                                 |
| <span data-ttu-id="01a13-240">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="01a13-240">Is-Single-Valued</span></span>       | <span data-ttu-id="01a13-241">True</span><span class="sxs-lookup"><span data-stu-id="01a13-241">True</span></span>                                                                                  |
| <span data-ttu-id="01a13-242">Está indexado</span><span class="sxs-lookup"><span data-stu-id="01a13-242">Is Indexed</span></span>             | <span data-ttu-id="01a13-243">False</span><span class="sxs-lookup"><span data-stu-id="01a13-243">False</span></span>                                                                                 |
| <span data-ttu-id="01a13-244">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="01a13-244">In Global Catalog</span></span>      | <span data-ttu-id="01a13-245">False</span><span class="sxs-lookup"><span data-stu-id="01a13-245">False</span></span>                                                                                 |
| <span data-ttu-id="01a13-246">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="01a13-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="01a13-247">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="01a13-247">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="01a13-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01a13-248">Range-Lower</span></span>            | <span data-ttu-id="01a13-249">0</span><span class="sxs-lookup"><span data-stu-id="01a13-249">0</span></span>                                                                                     |
| <span data-ttu-id="01a13-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01a13-250">Range-Upper</span></span>            | <span data-ttu-id="01a13-251">65536</span><span class="sxs-lookup"><span data-stu-id="01a13-251">65536</span></span>                                                                                 |
| <span data-ttu-id="01a13-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01a13-252">Search-Flags</span></span>           | <span data-ttu-id="01a13-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01a13-253">0x00000000</span></span>                                                                            |
| <span data-ttu-id="01a13-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01a13-254">System-Flags</span></span>           | <span data-ttu-id="01a13-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01a13-255">0x00000010</span></span>                                                                            |
| <span data-ttu-id="01a13-256">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="01a13-256">Classes used in</span></span>        | [<span data-ttu-id="01a13-257">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="01a13-257">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="01a13-258">**MS-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="01a13-258">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



 

 





