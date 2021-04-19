---
title: atributo MS-DS-Logon-Time-Sync-Interval
description: Este atributo controla la granularidad, en días, con la que la hora del último inicio de sesión de un usuario o equipo, registrada en el atributo lastLogonTimestamp, se replica en todos los controladores de dominio de un dominio.
ms.assetid: f1f9f1f8-df60-44b5-965d-631c4dd4ef84
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MS-DS-Logon-Time-Sync-Interval
- Esquema de AD de atributo msDS-LogonTimeSyncInterval
topic_type:
- apiref
api_name:
- ms-DS-Logon-Time-Sync-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dbf23ca77bda9dac76f02986be1c05c80559199
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536274"
---
# <a name="ms-ds-logon-time-sync-interval-attribute"></a><span data-ttu-id="15618-105">atributo MS-DS-Logon-Time-Sync-Interval</span><span class="sxs-lookup"><span data-stu-id="15618-105">ms-DS-Logon-Time-Sync-Interval attribute</span></span>

<span data-ttu-id="15618-106">Este atributo controla la granularidad, en días, con la que la hora del último inicio de sesión de un usuario o equipo, registrada en el atributo lastLogonTimestamp, se replica en todos los controladores de dominio de un dominio.</span><span class="sxs-lookup"><span data-stu-id="15618-106">This attribute controls the granularity, in days, with which the last logon time for a user or computer, recorded in the lastLogonTimestamp attribute, is replicated to all DCs in a domain.</span></span>



| <span data-ttu-id="15618-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="15618-107">Entry</span></span> | <span data-ttu-id="15618-108">Value</span><span class="sxs-lookup"><span data-stu-id="15618-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15618-109">CN</span><span class="sxs-lookup"><span data-stu-id="15618-109">CN</span></span>                | <span data-ttu-id="15618-110">MS-DS-Logon-Time-Sync-Interval</span><span class="sxs-lookup"><span data-stu-id="15618-110">ms-DS-Logon-Time-Sync-Interval</span></span>                                                                             |
| <span data-ttu-id="15618-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="15618-111">Ldap-Display-Name</span></span> | <span data-ttu-id="15618-112">msDS-LogonTimeSyncInterval</span><span class="sxs-lookup"><span data-stu-id="15618-112">msDS-LogonTimeSyncInterval</span></span>                                                                                 |
| <span data-ttu-id="15618-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="15618-113">Size</span></span>              | <span data-ttu-id="15618-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="15618-114">4 bytes</span></span>                                                                                                    |
| <span data-ttu-id="15618-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="15618-115">Update Privilege</span></span>  | <span data-ttu-id="15618-116">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="15618-116">Domain administrator</span></span>                                                                                       |
| <span data-ttu-id="15618-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="15618-117">Update Frequency</span></span>  | <span data-ttu-id="15618-118">Rara vez, puesto que se trata de una configuración de Directiva, solo se actualiza cuando se desea un cambio en la Directiva de todo el dominio.</span><span class="sxs-lookup"><span data-stu-id="15618-118">Rarely, since this is a policy setting, it is updated only when a change in domain-wide policy is desired.</span></span> |
| <span data-ttu-id="15618-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="15618-119">Attribute-Id</span></span>      | <span data-ttu-id="15618-120">1.2.840.113556.1.4.1784</span><span class="sxs-lookup"><span data-stu-id="15618-120">1.2.840.113556.1.4.1784</span></span>                                                                                    |
| <span data-ttu-id="15618-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="15618-121">System-Id-Guid</span></span>    | <span data-ttu-id="15618-122">ad7940f8-e43a-4a42-83bc-d688e59ea605</span><span class="sxs-lookup"><span data-stu-id="15618-122">ad7940f8-e43a-4a42-83bc-d688e59ea605</span></span>                                                                       |
| <span data-ttu-id="15618-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15618-123">Syntax</span></span>            | [<span data-ttu-id="15618-124">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="15618-124">**Enumeration**</span></span>](s-enumeration.md)                                                                       |



## <a name="implementations"></a><span data-ttu-id="15618-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="15618-125">Implementations</span></span>

-   [<span data-ttu-id="15618-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="15618-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="15618-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="15618-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="15618-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="15618-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="15618-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="15618-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="15618-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="15618-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="15618-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="15618-131">Windows Server 2003</span></span>



| <span data-ttu-id="15618-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="15618-132">Entry</span></span> | <span data-ttu-id="15618-133">Value</span><span class="sxs-lookup"><span data-stu-id="15618-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="15618-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="15618-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="15618-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15618-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="15618-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="15618-136">System-Only</span></span>            | <span data-ttu-id="15618-137">False</span><span class="sxs-lookup"><span data-stu-id="15618-137">False</span></span>                                        |
| <span data-ttu-id="15618-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="15618-138">Is-Single-Valued</span></span>       | <span data-ttu-id="15618-139">True</span><span class="sxs-lookup"><span data-stu-id="15618-139">True</span></span>                                         |
| <span data-ttu-id="15618-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="15618-140">Is Indexed</span></span>             | <span data-ttu-id="15618-141">False</span><span class="sxs-lookup"><span data-stu-id="15618-141">False</span></span>                                        |
| <span data-ttu-id="15618-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="15618-142">In Global Catalog</span></span>      | <span data-ttu-id="15618-143">False</span><span class="sxs-lookup"><span data-stu-id="15618-143">False</span></span>                                        |
| <span data-ttu-id="15618-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="15618-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="15618-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15618-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="15618-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15618-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="15618-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15618-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="15618-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15618-148">Search-Flags</span></span>           | <span data-ttu-id="15618-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15618-149">0x00000000</span></span>                                   |
| <span data-ttu-id="15618-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15618-150">System-Flags</span></span>           | <span data-ttu-id="15618-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15618-151">0x00000010</span></span>                                   |
| <span data-ttu-id="15618-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="15618-152">Classes used in</span></span>        | [<span data-ttu-id="15618-153">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="15618-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="15618-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="15618-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="15618-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="15618-155">Entry</span></span> | <span data-ttu-id="15618-156">Value</span><span class="sxs-lookup"><span data-stu-id="15618-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="15618-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="15618-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="15618-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15618-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="15618-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="15618-159">System-Only</span></span>            | <span data-ttu-id="15618-160">False</span><span class="sxs-lookup"><span data-stu-id="15618-160">False</span></span>                                        |
| <span data-ttu-id="15618-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="15618-161">Is-Single-Valued</span></span>       | <span data-ttu-id="15618-162">True</span><span class="sxs-lookup"><span data-stu-id="15618-162">True</span></span>                                         |
| <span data-ttu-id="15618-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="15618-163">Is Indexed</span></span>             | <span data-ttu-id="15618-164">False</span><span class="sxs-lookup"><span data-stu-id="15618-164">False</span></span>                                        |
| <span data-ttu-id="15618-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="15618-165">In Global Catalog</span></span>      | <span data-ttu-id="15618-166">False</span><span class="sxs-lookup"><span data-stu-id="15618-166">False</span></span>                                        |
| <span data-ttu-id="15618-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="15618-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="15618-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15618-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="15618-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15618-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="15618-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15618-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="15618-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15618-171">Search-Flags</span></span>           | <span data-ttu-id="15618-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15618-172">0x00000000</span></span>                                   |
| <span data-ttu-id="15618-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15618-173">System-Flags</span></span>           | <span data-ttu-id="15618-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15618-174">0x00000010</span></span>                                   |
| <span data-ttu-id="15618-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="15618-175">Classes used in</span></span>        | [<span data-ttu-id="15618-176">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="15618-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="15618-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15618-177">Windows Server 2008</span></span>



| <span data-ttu-id="15618-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="15618-178">Entry</span></span> | <span data-ttu-id="15618-179">Value</span><span class="sxs-lookup"><span data-stu-id="15618-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="15618-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="15618-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="15618-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15618-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="15618-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="15618-182">System-Only</span></span>            | <span data-ttu-id="15618-183">False</span><span class="sxs-lookup"><span data-stu-id="15618-183">False</span></span>                                        |
| <span data-ttu-id="15618-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="15618-184">Is-Single-Valued</span></span>       | <span data-ttu-id="15618-185">True</span><span class="sxs-lookup"><span data-stu-id="15618-185">True</span></span>                                         |
| <span data-ttu-id="15618-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="15618-186">Is Indexed</span></span>             | <span data-ttu-id="15618-187">False</span><span class="sxs-lookup"><span data-stu-id="15618-187">False</span></span>                                        |
| <span data-ttu-id="15618-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="15618-188">In Global Catalog</span></span>      | <span data-ttu-id="15618-189">False</span><span class="sxs-lookup"><span data-stu-id="15618-189">False</span></span>                                        |
| <span data-ttu-id="15618-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="15618-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="15618-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15618-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="15618-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15618-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="15618-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15618-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="15618-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15618-194">Search-Flags</span></span>           | <span data-ttu-id="15618-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15618-195">0x00000000</span></span>                                   |
| <span data-ttu-id="15618-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15618-196">System-Flags</span></span>           | <span data-ttu-id="15618-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15618-197">0x00000010</span></span>                                   |
| <span data-ttu-id="15618-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="15618-198">Classes used in</span></span>        | [<span data-ttu-id="15618-199">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="15618-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="15618-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="15618-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="15618-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="15618-201">Entry</span></span> | <span data-ttu-id="15618-202">Value</span><span class="sxs-lookup"><span data-stu-id="15618-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="15618-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="15618-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="15618-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15618-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="15618-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="15618-205">System-Only</span></span>            | <span data-ttu-id="15618-206">False</span><span class="sxs-lookup"><span data-stu-id="15618-206">False</span></span>                                        |
| <span data-ttu-id="15618-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="15618-207">Is-Single-Valued</span></span>       | <span data-ttu-id="15618-208">True</span><span class="sxs-lookup"><span data-stu-id="15618-208">True</span></span>                                         |
| <span data-ttu-id="15618-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="15618-209">Is Indexed</span></span>             | <span data-ttu-id="15618-210">False</span><span class="sxs-lookup"><span data-stu-id="15618-210">False</span></span>                                        |
| <span data-ttu-id="15618-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="15618-211">In Global Catalog</span></span>      | <span data-ttu-id="15618-212">False</span><span class="sxs-lookup"><span data-stu-id="15618-212">False</span></span>                                        |
| <span data-ttu-id="15618-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="15618-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="15618-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15618-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="15618-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15618-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="15618-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15618-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="15618-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15618-217">Search-Flags</span></span>           | <span data-ttu-id="15618-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15618-218">0x00000000</span></span>                                   |
| <span data-ttu-id="15618-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15618-219">System-Flags</span></span>           | <span data-ttu-id="15618-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15618-220">0x00000010</span></span>                                   |
| <span data-ttu-id="15618-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="15618-221">Classes used in</span></span>        | [<span data-ttu-id="15618-222">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="15618-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="15618-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="15618-223">Windows Server 2012</span></span>



| <span data-ttu-id="15618-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="15618-224">Entry</span></span> | <span data-ttu-id="15618-225">Value</span><span class="sxs-lookup"><span data-stu-id="15618-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="15618-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="15618-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="15618-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15618-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="15618-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="15618-228">System-Only</span></span>            | <span data-ttu-id="15618-229">False</span><span class="sxs-lookup"><span data-stu-id="15618-229">False</span></span>                                        |
| <span data-ttu-id="15618-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="15618-230">Is-Single-Valued</span></span>       | <span data-ttu-id="15618-231">True</span><span class="sxs-lookup"><span data-stu-id="15618-231">True</span></span>                                         |
| <span data-ttu-id="15618-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="15618-232">Is Indexed</span></span>             | <span data-ttu-id="15618-233">False</span><span class="sxs-lookup"><span data-stu-id="15618-233">False</span></span>                                        |
| <span data-ttu-id="15618-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="15618-234">In Global Catalog</span></span>      | <span data-ttu-id="15618-235">False</span><span class="sxs-lookup"><span data-stu-id="15618-235">False</span></span>                                        |
| <span data-ttu-id="15618-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="15618-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="15618-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15618-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="15618-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15618-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="15618-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15618-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="15618-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15618-240">Search-Flags</span></span>           | <span data-ttu-id="15618-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15618-241">0x00000000</span></span>                                   |
| <span data-ttu-id="15618-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15618-242">System-Flags</span></span>           | <span data-ttu-id="15618-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15618-243">0x00000010</span></span>                                   |
| <span data-ttu-id="15618-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="15618-244">Classes used in</span></span>        | [<span data-ttu-id="15618-245">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="15618-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





