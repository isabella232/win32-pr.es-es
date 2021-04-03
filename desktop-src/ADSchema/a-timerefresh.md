---
title: Time-Refresh atributo)
description: Este atributo tiene el intervalo durante el cual un registro de recursos incluido en una Active Directory zona integrada se debe actualizar para el servidor DNS. El intervalo predeterminado es de 7 días.
ms.assetid: 9e473c29-7fcf-4d6d-8a7c-2791c7822c7d
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Time-Refresh
- timeRefresh esquema de AD de atributos
topic_type:
- apiref
api_name:
- Time-Refresh
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87bc360686b1692d2dbda1ee23ad6351e69d3afe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997495"
---
# <a name="time-refresh-attribute"></a><span data-ttu-id="4d9ad-106">Time-Refresh atributo)</span><span class="sxs-lookup"><span data-stu-id="4d9ad-106">Time-Refresh attribute</span></span>

<span data-ttu-id="4d9ad-107">Este atributo tiene el intervalo durante el cual un registro de recursos incluido en una Active Directory zona integrada se debe actualizar para el servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="4d9ad-107">This attribute has the interval during which a resource record that is contained in an Active Directory integrated zone should be refreshed for the DNS server.</span></span> <span data-ttu-id="4d9ad-108">El intervalo predeterminado es de 7 días.</span><span class="sxs-lookup"><span data-stu-id="4d9ad-108">The default interval is 7 days.</span></span>



| <span data-ttu-id="4d9ad-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="4d9ad-109">Entry</span></span> | <span data-ttu-id="4d9ad-110">Value</span><span class="sxs-lookup"><span data-stu-id="4d9ad-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="4d9ad-111">CN</span><span class="sxs-lookup"><span data-stu-id="4d9ad-111">CN</span></span>                | <span data-ttu-id="4d9ad-112">Time-Refresh</span><span class="sxs-lookup"><span data-stu-id="4d9ad-112">Time-Refresh</span></span>                         |
| <span data-ttu-id="4d9ad-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="4d9ad-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4d9ad-114">timeRefresh</span><span class="sxs-lookup"><span data-stu-id="4d9ad-114">timeRefresh</span></span>                          |
| <span data-ttu-id="4d9ad-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="4d9ad-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="4d9ad-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="4d9ad-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="4d9ad-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="4d9ad-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="4d9ad-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4d9ad-118">Attribute-Id</span></span>      | <span data-ttu-id="4d9ad-119">1.2.840.113556.1.4.503</span><span class="sxs-lookup"><span data-stu-id="4d9ad-119">1.2.840.113556.1.4.503</span></span>               |
| <span data-ttu-id="4d9ad-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4d9ad-120">System-Id-Guid</span></span>    | <span data-ttu-id="4d9ad-121">ddac0cf1-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="4d9ad-121">ddac0cf1-af8f-11d0-afeb-00c04fd930c9</span></span> |
| <span data-ttu-id="4d9ad-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d9ad-122">Syntax</span></span>            | [<span data-ttu-id="4d9ad-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="4d9ad-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="4d9ad-124">Implementations</span></span>

-   [<span data-ttu-id="4d9ad-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4d9ad-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4d9ad-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4d9ad-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4d9ad-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4d9ad-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4d9ad-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4d9ad-131">Windows 2000 Server</span></span>



| <span data-ttu-id="4d9ad-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="4d9ad-132">Entry</span></span> | <span data-ttu-id="4d9ad-133">Value</span><span class="sxs-lookup"><span data-stu-id="4d9ad-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d9ad-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4d9ad-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d9ad-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d9ad-136">System-Only</span></span>            | <span data-ttu-id="4d9ad-137">False</span><span class="sxs-lookup"><span data-stu-id="4d9ad-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="4d9ad-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4d9ad-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4d9ad-139">True</span><span class="sxs-lookup"><span data-stu-id="4d9ad-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="4d9ad-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4d9ad-140">Is Indexed</span></span>             | <span data-ttu-id="4d9ad-141">False</span><span class="sxs-lookup"><span data-stu-id="4d9ad-141">False</span></span>                                                                                                                         |
| <span data-ttu-id="4d9ad-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4d9ad-142">In Global Catalog</span></span>      | <span data-ttu-id="4d9ad-143">False</span><span class="sxs-lookup"><span data-stu-id="4d9ad-143">False</span></span>                                                                                                                         |
| <span data-ttu-id="4d9ad-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4d9ad-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d9ad-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4d9ad-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="4d9ad-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d9ad-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d9ad-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d9ad-148">Search-Flags</span></span>           | <span data-ttu-id="4d9ad-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d9ad-149">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="4d9ad-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d9ad-150">System-Flags</span></span>           | <span data-ttu-id="4d9ad-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d9ad-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="4d9ad-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4d9ad-152">Classes used in</span></span>        | [<span data-ttu-id="4d9ad-153">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-153">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="4d9ad-154">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-154">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4d9ad-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4d9ad-155">Windows Server 2003</span></span>



| <span data-ttu-id="4d9ad-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="4d9ad-156">Entry</span></span> | <span data-ttu-id="4d9ad-157">Value</span><span class="sxs-lookup"><span data-stu-id="4d9ad-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d9ad-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4d9ad-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d9ad-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d9ad-160">System-Only</span></span>            | <span data-ttu-id="4d9ad-161">False</span><span class="sxs-lookup"><span data-stu-id="4d9ad-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="4d9ad-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4d9ad-162">Is-Single-Valued</span></span>       | <span data-ttu-id="4d9ad-163">True</span><span class="sxs-lookup"><span data-stu-id="4d9ad-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="4d9ad-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4d9ad-164">Is Indexed</span></span>             | <span data-ttu-id="4d9ad-165">False</span><span class="sxs-lookup"><span data-stu-id="4d9ad-165">False</span></span>                                                                                                                         |
| <span data-ttu-id="4d9ad-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4d9ad-166">In Global Catalog</span></span>      | <span data-ttu-id="4d9ad-167">False</span><span class="sxs-lookup"><span data-stu-id="4d9ad-167">False</span></span>                                                                                                                         |
| <span data-ttu-id="4d9ad-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4d9ad-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d9ad-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4d9ad-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="4d9ad-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d9ad-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d9ad-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d9ad-172">Search-Flags</span></span>           | <span data-ttu-id="4d9ad-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d9ad-173">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="4d9ad-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d9ad-174">System-Flags</span></span>           | <span data-ttu-id="4d9ad-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d9ad-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="4d9ad-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4d9ad-176">Classes used in</span></span>        | [<span data-ttu-id="4d9ad-177">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-177">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="4d9ad-178">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4d9ad-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4d9ad-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4d9ad-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="4d9ad-180">Entry</span></span> | <span data-ttu-id="4d9ad-181">Value</span><span class="sxs-lookup"><span data-stu-id="4d9ad-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d9ad-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4d9ad-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d9ad-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d9ad-184">System-Only</span></span>            | <span data-ttu-id="4d9ad-185">False</span><span class="sxs-lookup"><span data-stu-id="4d9ad-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="4d9ad-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4d9ad-186">Is-Single-Valued</span></span>       | <span data-ttu-id="4d9ad-187">True</span><span class="sxs-lookup"><span data-stu-id="4d9ad-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="4d9ad-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4d9ad-188">Is Indexed</span></span>             | <span data-ttu-id="4d9ad-189">False</span><span class="sxs-lookup"><span data-stu-id="4d9ad-189">False</span></span>                                                                                                                         |
| <span data-ttu-id="4d9ad-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4d9ad-190">In Global Catalog</span></span>      | <span data-ttu-id="4d9ad-191">False</span><span class="sxs-lookup"><span data-stu-id="4d9ad-191">False</span></span>                                                                                                                         |
| <span data-ttu-id="4d9ad-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4d9ad-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d9ad-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4d9ad-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="4d9ad-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d9ad-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d9ad-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d9ad-196">Search-Flags</span></span>           | <span data-ttu-id="4d9ad-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d9ad-197">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="4d9ad-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d9ad-198">System-Flags</span></span>           | <span data-ttu-id="4d9ad-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d9ad-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="4d9ad-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4d9ad-200">Classes used in</span></span>        | [<span data-ttu-id="4d9ad-201">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-201">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="4d9ad-202">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-202">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4d9ad-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d9ad-203">Windows Server 2008</span></span>



| <span data-ttu-id="4d9ad-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="4d9ad-204">Entry</span></span> | <span data-ttu-id="4d9ad-205">Value</span><span class="sxs-lookup"><span data-stu-id="4d9ad-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d9ad-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4d9ad-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d9ad-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d9ad-208">System-Only</span></span>            | <span data-ttu-id="4d9ad-209">False</span><span class="sxs-lookup"><span data-stu-id="4d9ad-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="4d9ad-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4d9ad-210">Is-Single-Valued</span></span>       | <span data-ttu-id="4d9ad-211">True</span><span class="sxs-lookup"><span data-stu-id="4d9ad-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="4d9ad-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4d9ad-212">Is Indexed</span></span>             | <span data-ttu-id="4d9ad-213">False</span><span class="sxs-lookup"><span data-stu-id="4d9ad-213">False</span></span>                                                                                                                         |
| <span data-ttu-id="4d9ad-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4d9ad-214">In Global Catalog</span></span>      | <span data-ttu-id="4d9ad-215">False</span><span class="sxs-lookup"><span data-stu-id="4d9ad-215">False</span></span>                                                                                                                         |
| <span data-ttu-id="4d9ad-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4d9ad-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d9ad-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4d9ad-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="4d9ad-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d9ad-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d9ad-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d9ad-220">Search-Flags</span></span>           | <span data-ttu-id="4d9ad-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d9ad-221">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="4d9ad-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d9ad-222">System-Flags</span></span>           | <span data-ttu-id="4d9ad-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d9ad-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="4d9ad-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4d9ad-224">Classes used in</span></span>        | [<span data-ttu-id="4d9ad-225">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-225">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="4d9ad-226">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-226">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4d9ad-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4d9ad-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4d9ad-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="4d9ad-228">Entry</span></span> | <span data-ttu-id="4d9ad-229">Value</span><span class="sxs-lookup"><span data-stu-id="4d9ad-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d9ad-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4d9ad-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d9ad-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d9ad-232">System-Only</span></span>            | <span data-ttu-id="4d9ad-233">False</span><span class="sxs-lookup"><span data-stu-id="4d9ad-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="4d9ad-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4d9ad-234">Is-Single-Valued</span></span>       | <span data-ttu-id="4d9ad-235">True</span><span class="sxs-lookup"><span data-stu-id="4d9ad-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="4d9ad-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4d9ad-236">Is Indexed</span></span>             | <span data-ttu-id="4d9ad-237">False</span><span class="sxs-lookup"><span data-stu-id="4d9ad-237">False</span></span>                                                                                                                         |
| <span data-ttu-id="4d9ad-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4d9ad-238">In Global Catalog</span></span>      | <span data-ttu-id="4d9ad-239">False</span><span class="sxs-lookup"><span data-stu-id="4d9ad-239">False</span></span>                                                                                                                         |
| <span data-ttu-id="4d9ad-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4d9ad-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d9ad-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4d9ad-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="4d9ad-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d9ad-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d9ad-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d9ad-244">Search-Flags</span></span>           | <span data-ttu-id="4d9ad-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d9ad-245">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="4d9ad-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d9ad-246">System-Flags</span></span>           | <span data-ttu-id="4d9ad-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d9ad-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="4d9ad-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4d9ad-248">Classes used in</span></span>        | [<span data-ttu-id="4d9ad-249">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-249">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="4d9ad-250">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-250">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4d9ad-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4d9ad-251">Windows Server 2012</span></span>



| <span data-ttu-id="4d9ad-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="4d9ad-252">Entry</span></span> | <span data-ttu-id="4d9ad-253">Value</span><span class="sxs-lookup"><span data-stu-id="4d9ad-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d9ad-254">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4d9ad-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d9ad-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d9ad-256">System-Only</span></span>            | <span data-ttu-id="4d9ad-257">False</span><span class="sxs-lookup"><span data-stu-id="4d9ad-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="4d9ad-258">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4d9ad-258">Is-Single-Valued</span></span>       | <span data-ttu-id="4d9ad-259">True</span><span class="sxs-lookup"><span data-stu-id="4d9ad-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="4d9ad-260">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4d9ad-260">Is Indexed</span></span>             | <span data-ttu-id="4d9ad-261">False</span><span class="sxs-lookup"><span data-stu-id="4d9ad-261">False</span></span>                                                                                                                         |
| <span data-ttu-id="4d9ad-262">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4d9ad-262">In Global Catalog</span></span>      | <span data-ttu-id="4d9ad-263">False</span><span class="sxs-lookup"><span data-stu-id="4d9ad-263">False</span></span>                                                                                                                         |
| <span data-ttu-id="4d9ad-264">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4d9ad-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d9ad-265">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4d9ad-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="4d9ad-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d9ad-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d9ad-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="4d9ad-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d9ad-268">Search-Flags</span></span>           | <span data-ttu-id="4d9ad-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d9ad-269">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="4d9ad-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d9ad-270">System-Flags</span></span>           | <span data-ttu-id="4d9ad-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d9ad-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="4d9ad-272">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4d9ad-272">Classes used in</span></span>        | [<span data-ttu-id="4d9ad-273">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-273">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="4d9ad-274">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="4d9ad-274">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





