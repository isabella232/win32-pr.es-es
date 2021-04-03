---
title: atributo MS-DS-AZ-Domain-timeout
description: Tiempo, en milisegundos, después de que se detecte que un dominio es inaccesible y antes de que se vuelva a intentar el controlador de dominio.
ms.assetid: b2523faa-7cf1-4325-a3fa-70c5f568adaa
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-AZ-Domain-timeout
- Esquema de AD de atributo msDS-AzDomainTimeout
topic_type:
- apiref
api_name:
- ms-DS-Az-Domain-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce6f457977de1124438fa4b54e4a84d1cb6d54e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906046"
---
# <a name="ms-ds-az-domain-timeout-attribute"></a><span data-ttu-id="913a4-105">atributo MS-DS-AZ-Domain-timeout</span><span class="sxs-lookup"><span data-stu-id="913a4-105">ms-DS-Az-Domain-Timeout attribute</span></span>

<span data-ttu-id="913a4-106">Tiempo, en milisegundos, después de que se detecte que un dominio es inaccesible y antes de que se vuelva a intentar el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="913a4-106">Time, in milliseconds, after a domain is detected to be unreachable and before the DC is tried again.</span></span>



| <span data-ttu-id="913a4-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="913a4-107">Entry</span></span> | <span data-ttu-id="913a4-108">Value</span><span class="sxs-lookup"><span data-stu-id="913a4-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="913a4-109">CN</span><span class="sxs-lookup"><span data-stu-id="913a4-109">CN</span></span>                | <span data-ttu-id="913a4-110">MS-DS-AZ-Domain-timeout</span><span class="sxs-lookup"><span data-stu-id="913a4-110">ms-DS-Az-Domain-Timeout</span></span>                 |
| <span data-ttu-id="913a4-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="913a4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="913a4-112">msDS-AzDomainTimeout</span><span class="sxs-lookup"><span data-stu-id="913a4-112">msDS-AzDomainTimeout</span></span>                    |
| <span data-ttu-id="913a4-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="913a4-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="913a4-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="913a4-114">Update Privilege</span></span>  | <span data-ttu-id="913a4-115">Administrador de AzRoles</span><span class="sxs-lookup"><span data-stu-id="913a4-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="913a4-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="913a4-116">Update Frequency</span></span>  | <span data-ttu-id="913a4-117">Durante la inicialización o el cambio de directiva.</span><span class="sxs-lookup"><span data-stu-id="913a4-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="913a4-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="913a4-118">Attribute-Id</span></span>      | <span data-ttu-id="913a4-119">1.2.840.113556.1.4.1795</span><span class="sxs-lookup"><span data-stu-id="913a4-119">1.2.840.113556.1.4.1795</span></span>                 |
| <span data-ttu-id="913a4-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="913a4-120">System-Id-Guid</span></span>    | <span data-ttu-id="913a4-121">6448f56a-ca70-4e2e-b0af-d20e4ce653d0</span><span class="sxs-lookup"><span data-stu-id="913a4-121">6448f56a-ca70-4e2e-b0af-d20e4ce653d0</span></span>    |
| <span data-ttu-id="913a4-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="913a4-122">Syntax</span></span>            | [<span data-ttu-id="913a4-123">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="913a4-123">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="913a4-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="913a4-124">Implementations</span></span>

-   [<span data-ttu-id="913a4-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="913a4-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="913a4-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="913a4-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="913a4-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="913a4-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="913a4-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="913a4-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="913a4-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="913a4-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="913a4-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="913a4-130">Windows Server 2003</span></span>



| <span data-ttu-id="913a4-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="913a4-131">Entry</span></span> | <span data-ttu-id="913a4-132">Value</span><span class="sxs-lookup"><span data-stu-id="913a4-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="913a4-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="913a4-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="913a4-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="913a4-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="913a4-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="913a4-135">System-Only</span></span>            | <span data-ttu-id="913a4-136">False</span><span class="sxs-lookup"><span data-stu-id="913a4-136">False</span></span>                                                              |
| <span data-ttu-id="913a4-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="913a4-137">Is-Single-Valued</span></span>       | <span data-ttu-id="913a4-138">True</span><span class="sxs-lookup"><span data-stu-id="913a4-138">True</span></span>                                                               |
| <span data-ttu-id="913a4-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="913a4-139">Is Indexed</span></span>             | <span data-ttu-id="913a4-140">False</span><span class="sxs-lookup"><span data-stu-id="913a4-140">False</span></span>                                                              |
| <span data-ttu-id="913a4-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="913a4-141">In Global Catalog</span></span>      | <span data-ttu-id="913a4-142">False</span><span class="sxs-lookup"><span data-stu-id="913a4-142">False</span></span>                                                              |
| <span data-ttu-id="913a4-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="913a4-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="913a4-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="913a4-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="913a4-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="913a4-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="913a4-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="913a4-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="913a4-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="913a4-147">Search-Flags</span></span>           | <span data-ttu-id="913a4-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="913a4-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="913a4-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="913a4-149">System-Flags</span></span>           | <span data-ttu-id="913a4-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="913a4-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="913a4-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="913a4-151">Classes used in</span></span>        | [<span data-ttu-id="913a4-152">**MS-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="913a4-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="913a4-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="913a4-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="913a4-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="913a4-154">Entry</span></span> | <span data-ttu-id="913a4-155">Value</span><span class="sxs-lookup"><span data-stu-id="913a4-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="913a4-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="913a4-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="913a4-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="913a4-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="913a4-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="913a4-158">System-Only</span></span>            | <span data-ttu-id="913a4-159">False</span><span class="sxs-lookup"><span data-stu-id="913a4-159">False</span></span>                                                              |
| <span data-ttu-id="913a4-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="913a4-160">Is-Single-Valued</span></span>       | <span data-ttu-id="913a4-161">True</span><span class="sxs-lookup"><span data-stu-id="913a4-161">True</span></span>                                                               |
| <span data-ttu-id="913a4-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="913a4-162">Is Indexed</span></span>             | <span data-ttu-id="913a4-163">False</span><span class="sxs-lookup"><span data-stu-id="913a4-163">False</span></span>                                                              |
| <span data-ttu-id="913a4-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="913a4-164">In Global Catalog</span></span>      | <span data-ttu-id="913a4-165">False</span><span class="sxs-lookup"><span data-stu-id="913a4-165">False</span></span>                                                              |
| <span data-ttu-id="913a4-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="913a4-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="913a4-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="913a4-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="913a4-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="913a4-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="913a4-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="913a4-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="913a4-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="913a4-170">Search-Flags</span></span>           | <span data-ttu-id="913a4-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="913a4-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="913a4-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="913a4-172">System-Flags</span></span>           | <span data-ttu-id="913a4-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="913a4-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="913a4-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="913a4-174">Classes used in</span></span>        | [<span data-ttu-id="913a4-175">**MS-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="913a4-175">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="913a4-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="913a4-176">Windows Server 2008</span></span>



| <span data-ttu-id="913a4-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="913a4-177">Entry</span></span> | <span data-ttu-id="913a4-178">Value</span><span class="sxs-lookup"><span data-stu-id="913a4-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="913a4-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="913a4-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="913a4-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="913a4-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="913a4-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="913a4-181">System-Only</span></span>            | <span data-ttu-id="913a4-182">False</span><span class="sxs-lookup"><span data-stu-id="913a4-182">False</span></span>                                                              |
| <span data-ttu-id="913a4-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="913a4-183">Is-Single-Valued</span></span>       | <span data-ttu-id="913a4-184">True</span><span class="sxs-lookup"><span data-stu-id="913a4-184">True</span></span>                                                               |
| <span data-ttu-id="913a4-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="913a4-185">Is Indexed</span></span>             | <span data-ttu-id="913a4-186">False</span><span class="sxs-lookup"><span data-stu-id="913a4-186">False</span></span>                                                              |
| <span data-ttu-id="913a4-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="913a4-187">In Global Catalog</span></span>      | <span data-ttu-id="913a4-188">False</span><span class="sxs-lookup"><span data-stu-id="913a4-188">False</span></span>                                                              |
| <span data-ttu-id="913a4-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="913a4-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="913a4-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="913a4-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="913a4-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="913a4-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="913a4-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="913a4-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="913a4-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="913a4-193">Search-Flags</span></span>           | <span data-ttu-id="913a4-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="913a4-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="913a4-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="913a4-195">System-Flags</span></span>           | <span data-ttu-id="913a4-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="913a4-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="913a4-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="913a4-197">Classes used in</span></span>        | [<span data-ttu-id="913a4-198">**MS-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="913a4-198">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="913a4-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="913a4-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="913a4-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="913a4-200">Entry</span></span> | <span data-ttu-id="913a4-201">Value</span><span class="sxs-lookup"><span data-stu-id="913a4-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="913a4-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="913a4-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="913a4-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="913a4-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="913a4-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="913a4-204">System-Only</span></span>            | <span data-ttu-id="913a4-205">False</span><span class="sxs-lookup"><span data-stu-id="913a4-205">False</span></span>                                                              |
| <span data-ttu-id="913a4-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="913a4-206">Is-Single-Valued</span></span>       | <span data-ttu-id="913a4-207">True</span><span class="sxs-lookup"><span data-stu-id="913a4-207">True</span></span>                                                               |
| <span data-ttu-id="913a4-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="913a4-208">Is Indexed</span></span>             | <span data-ttu-id="913a4-209">False</span><span class="sxs-lookup"><span data-stu-id="913a4-209">False</span></span>                                                              |
| <span data-ttu-id="913a4-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="913a4-210">In Global Catalog</span></span>      | <span data-ttu-id="913a4-211">False</span><span class="sxs-lookup"><span data-stu-id="913a4-211">False</span></span>                                                              |
| <span data-ttu-id="913a4-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="913a4-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="913a4-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="913a4-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="913a4-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="913a4-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="913a4-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="913a4-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="913a4-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="913a4-216">Search-Flags</span></span>           | <span data-ttu-id="913a4-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="913a4-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="913a4-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="913a4-218">System-Flags</span></span>           | <span data-ttu-id="913a4-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="913a4-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="913a4-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="913a4-220">Classes used in</span></span>        | [<span data-ttu-id="913a4-221">**MS-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="913a4-221">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="913a4-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="913a4-222">Windows Server 2012</span></span>



| <span data-ttu-id="913a4-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="913a4-223">Entry</span></span> | <span data-ttu-id="913a4-224">Value</span><span class="sxs-lookup"><span data-stu-id="913a4-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="913a4-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="913a4-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="913a4-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="913a4-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="913a4-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="913a4-227">System-Only</span></span>            | <span data-ttu-id="913a4-228">False</span><span class="sxs-lookup"><span data-stu-id="913a4-228">False</span></span>                                                              |
| <span data-ttu-id="913a4-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="913a4-229">Is-Single-Valued</span></span>       | <span data-ttu-id="913a4-230">True</span><span class="sxs-lookup"><span data-stu-id="913a4-230">True</span></span>                                                               |
| <span data-ttu-id="913a4-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="913a4-231">Is Indexed</span></span>             | <span data-ttu-id="913a4-232">False</span><span class="sxs-lookup"><span data-stu-id="913a4-232">False</span></span>                                                              |
| <span data-ttu-id="913a4-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="913a4-233">In Global Catalog</span></span>      | <span data-ttu-id="913a4-234">False</span><span class="sxs-lookup"><span data-stu-id="913a4-234">False</span></span>                                                              |
| <span data-ttu-id="913a4-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="913a4-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="913a4-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="913a4-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="913a4-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="913a4-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="913a4-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="913a4-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="913a4-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="913a4-239">Search-Flags</span></span>           | <span data-ttu-id="913a4-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="913a4-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="913a4-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="913a4-241">System-Flags</span></span>           | <span data-ttu-id="913a4-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="913a4-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="913a4-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="913a4-243">Classes used in</span></span>        | [<span data-ttu-id="913a4-244">**MS-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="913a4-244">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



 

 





