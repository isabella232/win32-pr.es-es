---
title: atributo MS-DS-AZ-Generate-Audits
description: Un campo booleano que indica si es necesario activar las auditorías en tiempo de ejecución (incluir auditorías para las comprobaciones de acceso, etc.).
ms.assetid: 23578f6a-7e7f-4871-9503-73f2ce598173
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-AZ-Generate-Audits
- Esquema de AD de atributo msDS-AzGenerateAudits
topic_type:
- apiref
api_name:
- ms-DS-Az-Generate-Audits
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645bdfd2f822139072391d401ecedfedee8680b8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906208"
---
# <a name="ms-ds-az-generate-audits-attribute"></a><span data-ttu-id="fe43f-105">atributo MS-DS-AZ-Generate-Audits</span><span class="sxs-lookup"><span data-stu-id="fe43f-105">ms-DS-Az-Generate-Audits attribute</span></span>

<span data-ttu-id="fe43f-106">Un campo booleano que indica si es necesario activar las auditorías en tiempo de ejecución (incluir auditorías para las comprobaciones de acceso, etc.).</span><span class="sxs-lookup"><span data-stu-id="fe43f-106">A Boolean field that indicates whether runtime audits need to be turned on (include audits for access checks, and so on).</span></span>



| <span data-ttu-id="fe43f-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="fe43f-107">Entry</span></span> | <span data-ttu-id="fe43f-108">Value</span><span class="sxs-lookup"><span data-stu-id="fe43f-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="fe43f-109">CN</span><span class="sxs-lookup"><span data-stu-id="fe43f-109">CN</span></span>                | <span data-ttu-id="fe43f-110">MS-DS-AZ-Generate-Audits</span><span class="sxs-lookup"><span data-stu-id="fe43f-110">ms-DS-Az-Generate-Audits</span></span>                |
| <span data-ttu-id="fe43f-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="fe43f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fe43f-112">msDS-AzGenerateAudits</span><span class="sxs-lookup"><span data-stu-id="fe43f-112">msDS-AzGenerateAudits</span></span>                   |
| <span data-ttu-id="fe43f-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="fe43f-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="fe43f-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="fe43f-114">Update Privilege</span></span>  | <span data-ttu-id="fe43f-115">Administrador de AzRoles</span><span class="sxs-lookup"><span data-stu-id="fe43f-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="fe43f-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="fe43f-116">Update Frequency</span></span>  | <span data-ttu-id="fe43f-117">Durante la inicialización o el cambio de directiva.</span><span class="sxs-lookup"><span data-stu-id="fe43f-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="fe43f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fe43f-118">Attribute-Id</span></span>      | <span data-ttu-id="fe43f-119">1.2.840.113556.1.4.1805</span><span class="sxs-lookup"><span data-stu-id="fe43f-119">1.2.840.113556.1.4.1805</span></span>                 |
| <span data-ttu-id="fe43f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fe43f-120">System-Id-Guid</span></span>    | <span data-ttu-id="fe43f-121">f90abab0-186c-4418-bb85-88447c87222a</span><span class="sxs-lookup"><span data-stu-id="fe43f-121">f90abab0-186c-4418-bb85-88447c87222a</span></span>    |
| <span data-ttu-id="fe43f-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe43f-122">Syntax</span></span>            | [<span data-ttu-id="fe43f-123">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="fe43f-123">**Boolean**</span></span>](s-boolean.md)            |



## <a name="implementations"></a><span data-ttu-id="fe43f-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="fe43f-124">Implementations</span></span>

-   [<span data-ttu-id="fe43f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fe43f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fe43f-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fe43f-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fe43f-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fe43f-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fe43f-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fe43f-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fe43f-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fe43f-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="fe43f-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe43f-130">Windows Server 2003</span></span>



| <span data-ttu-id="fe43f-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="fe43f-131">Entry</span></span> | <span data-ttu-id="fe43f-132">Value</span><span class="sxs-lookup"><span data-stu-id="fe43f-132">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe43f-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fe43f-133">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe43f-134">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe43f-135">System-Only</span></span>            | <span data-ttu-id="fe43f-136">False</span><span class="sxs-lookup"><span data-stu-id="fe43f-136">False</span></span>                                                                                                                              |
| <span data-ttu-id="fe43f-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fe43f-137">Is-Single-Valued</span></span>       | <span data-ttu-id="fe43f-138">True</span><span class="sxs-lookup"><span data-stu-id="fe43f-138">True</span></span>                                                                                                                               |
| <span data-ttu-id="fe43f-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fe43f-139">Is Indexed</span></span>             | <span data-ttu-id="fe43f-140">False</span><span class="sxs-lookup"><span data-stu-id="fe43f-140">False</span></span>                                                                                                                              |
| <span data-ttu-id="fe43f-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fe43f-141">In Global Catalog</span></span>      | <span data-ttu-id="fe43f-142">False</span><span class="sxs-lookup"><span data-stu-id="fe43f-142">False</span></span>                                                                                                                              |
| <span data-ttu-id="fe43f-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fe43f-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe43f-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fe43f-144">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="fe43f-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe43f-145">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe43f-146">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe43f-147">Search-Flags</span></span>           | <span data-ttu-id="fe43f-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe43f-148">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="fe43f-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe43f-149">System-Flags</span></span>           | <span data-ttu-id="fe43f-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe43f-150">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="fe43f-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fe43f-151">Classes used in</span></span>        | [<span data-ttu-id="fe43f-152">**MS-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="fe43f-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="fe43f-153">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="fe43f-153">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fe43f-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fe43f-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fe43f-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="fe43f-155">Entry</span></span> | <span data-ttu-id="fe43f-156">Value</span><span class="sxs-lookup"><span data-stu-id="fe43f-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe43f-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fe43f-157">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe43f-158">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe43f-159">System-Only</span></span>            | <span data-ttu-id="fe43f-160">False</span><span class="sxs-lookup"><span data-stu-id="fe43f-160">False</span></span>                                                                                                                              |
| <span data-ttu-id="fe43f-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fe43f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="fe43f-162">True</span><span class="sxs-lookup"><span data-stu-id="fe43f-162">True</span></span>                                                                                                                               |
| <span data-ttu-id="fe43f-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fe43f-163">Is Indexed</span></span>             | <span data-ttu-id="fe43f-164">False</span><span class="sxs-lookup"><span data-stu-id="fe43f-164">False</span></span>                                                                                                                              |
| <span data-ttu-id="fe43f-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fe43f-165">In Global Catalog</span></span>      | <span data-ttu-id="fe43f-166">False</span><span class="sxs-lookup"><span data-stu-id="fe43f-166">False</span></span>                                                                                                                              |
| <span data-ttu-id="fe43f-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fe43f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe43f-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fe43f-168">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="fe43f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe43f-169">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe43f-170">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe43f-171">Search-Flags</span></span>           | <span data-ttu-id="fe43f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe43f-172">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="fe43f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe43f-173">System-Flags</span></span>           | <span data-ttu-id="fe43f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe43f-174">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="fe43f-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fe43f-175">Classes used in</span></span>        | [<span data-ttu-id="fe43f-176">**MS-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="fe43f-176">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="fe43f-177">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="fe43f-177">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fe43f-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe43f-178">Windows Server 2008</span></span>



| <span data-ttu-id="fe43f-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="fe43f-179">Entry</span></span> | <span data-ttu-id="fe43f-180">Value</span><span class="sxs-lookup"><span data-stu-id="fe43f-180">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe43f-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fe43f-181">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe43f-182">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe43f-183">System-Only</span></span>            | <span data-ttu-id="fe43f-184">False</span><span class="sxs-lookup"><span data-stu-id="fe43f-184">False</span></span>                                                                                                                              |
| <span data-ttu-id="fe43f-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fe43f-185">Is-Single-Valued</span></span>       | <span data-ttu-id="fe43f-186">True</span><span class="sxs-lookup"><span data-stu-id="fe43f-186">True</span></span>                                                                                                                               |
| <span data-ttu-id="fe43f-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fe43f-187">Is Indexed</span></span>             | <span data-ttu-id="fe43f-188">False</span><span class="sxs-lookup"><span data-stu-id="fe43f-188">False</span></span>                                                                                                                              |
| <span data-ttu-id="fe43f-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fe43f-189">In Global Catalog</span></span>      | <span data-ttu-id="fe43f-190">False</span><span class="sxs-lookup"><span data-stu-id="fe43f-190">False</span></span>                                                                                                                              |
| <span data-ttu-id="fe43f-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fe43f-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe43f-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fe43f-192">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="fe43f-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe43f-193">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe43f-194">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe43f-195">Search-Flags</span></span>           | <span data-ttu-id="fe43f-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe43f-196">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="fe43f-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe43f-197">System-Flags</span></span>           | <span data-ttu-id="fe43f-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe43f-198">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="fe43f-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fe43f-199">Classes used in</span></span>        | [<span data-ttu-id="fe43f-200">**MS-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="fe43f-200">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="fe43f-201">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="fe43f-201">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fe43f-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fe43f-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fe43f-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="fe43f-203">Entry</span></span> | <span data-ttu-id="fe43f-204">Value</span><span class="sxs-lookup"><span data-stu-id="fe43f-204">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe43f-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fe43f-205">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe43f-206">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe43f-207">System-Only</span></span>            | <span data-ttu-id="fe43f-208">False</span><span class="sxs-lookup"><span data-stu-id="fe43f-208">False</span></span>                                                                                                                              |
| <span data-ttu-id="fe43f-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fe43f-209">Is-Single-Valued</span></span>       | <span data-ttu-id="fe43f-210">True</span><span class="sxs-lookup"><span data-stu-id="fe43f-210">True</span></span>                                                                                                                               |
| <span data-ttu-id="fe43f-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fe43f-211">Is Indexed</span></span>             | <span data-ttu-id="fe43f-212">False</span><span class="sxs-lookup"><span data-stu-id="fe43f-212">False</span></span>                                                                                                                              |
| <span data-ttu-id="fe43f-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fe43f-213">In Global Catalog</span></span>      | <span data-ttu-id="fe43f-214">False</span><span class="sxs-lookup"><span data-stu-id="fe43f-214">False</span></span>                                                                                                                              |
| <span data-ttu-id="fe43f-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fe43f-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe43f-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fe43f-216">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="fe43f-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe43f-217">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe43f-218">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe43f-219">Search-Flags</span></span>           | <span data-ttu-id="fe43f-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe43f-220">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="fe43f-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe43f-221">System-Flags</span></span>           | <span data-ttu-id="fe43f-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe43f-222">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="fe43f-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fe43f-223">Classes used in</span></span>        | [<span data-ttu-id="fe43f-224">**MS-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="fe43f-224">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="fe43f-225">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="fe43f-225">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fe43f-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fe43f-226">Windows Server 2012</span></span>



| <span data-ttu-id="fe43f-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="fe43f-227">Entry</span></span> | <span data-ttu-id="fe43f-228">Value</span><span class="sxs-lookup"><span data-stu-id="fe43f-228">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe43f-229">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fe43f-229">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe43f-230">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe43f-231">System-Only</span></span>            | <span data-ttu-id="fe43f-232">False</span><span class="sxs-lookup"><span data-stu-id="fe43f-232">False</span></span>                                                                                                                              |
| <span data-ttu-id="fe43f-233">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fe43f-233">Is-Single-Valued</span></span>       | <span data-ttu-id="fe43f-234">True</span><span class="sxs-lookup"><span data-stu-id="fe43f-234">True</span></span>                                                                                                                               |
| <span data-ttu-id="fe43f-235">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fe43f-235">Is Indexed</span></span>             | <span data-ttu-id="fe43f-236">False</span><span class="sxs-lookup"><span data-stu-id="fe43f-236">False</span></span>                                                                                                                              |
| <span data-ttu-id="fe43f-237">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fe43f-237">In Global Catalog</span></span>      | <span data-ttu-id="fe43f-238">False</span><span class="sxs-lookup"><span data-stu-id="fe43f-238">False</span></span>                                                                                                                              |
| <span data-ttu-id="fe43f-239">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fe43f-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe43f-240">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fe43f-240">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="fe43f-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe43f-241">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe43f-242">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="fe43f-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe43f-243">Search-Flags</span></span>           | <span data-ttu-id="fe43f-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe43f-244">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="fe43f-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe43f-245">System-Flags</span></span>           | <span data-ttu-id="fe43f-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe43f-246">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="fe43f-247">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fe43f-247">Classes used in</span></span>        | [<span data-ttu-id="fe43f-248">**MS-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="fe43f-248">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="fe43f-249">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="fe43f-249">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



 

 





