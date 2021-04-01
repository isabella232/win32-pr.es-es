---
title: Atributo MS-SQL-AllowKnownPullSubscription
description: True si la publicación permite que los suscriptores registrados se suscriban.
ms.assetid: be3b618e-bdf5-4bb4-ac4d-51dc97e73408
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de MS-SQL-AllowKnownPullSubscription
- Esquema de AD de atributos de mS-SQL-AllowKnownPullSubscription
topic_type:
- apiref
api_name:
- MS-SQL-AllowKnownPullSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d07789bf68f470db69219765628ebc82b2014428
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906238"
---
# <a name="ms-sql-allowknownpullsubscription-attribute"></a><span data-ttu-id="00dc3-105">Atributo MS-SQL-AllowKnownPullSubscription</span><span class="sxs-lookup"><span data-stu-id="00dc3-105">MS-SQL-AllowKnownPullSubscription attribute</span></span>

<span data-ttu-id="00dc3-106">True si la publicación permite que los suscriptores registrados se suscriban.</span><span class="sxs-lookup"><span data-stu-id="00dc3-106">True if the publication allows registered subscribers to subscribe.</span></span>



| <span data-ttu-id="00dc3-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="00dc3-107">Entry</span></span> | <span data-ttu-id="00dc3-108">Value</span><span class="sxs-lookup"><span data-stu-id="00dc3-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="00dc3-109">CN</span><span class="sxs-lookup"><span data-stu-id="00dc3-109">CN</span></span>                | <span data-ttu-id="00dc3-110">MS-SQL-AllowKnownPullSubscription</span><span class="sxs-lookup"><span data-stu-id="00dc3-110">MS-SQL-AllowKnownPullSubscription</span></span>    |
| <span data-ttu-id="00dc3-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="00dc3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="00dc3-112">mS-SQL-AllowKnownPullSubscription</span><span class="sxs-lookup"><span data-stu-id="00dc3-112">mS-SQL-AllowKnownPullSubscription</span></span>    |
| <span data-ttu-id="00dc3-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="00dc3-113">Size</span></span>              | <span data-ttu-id="00dc3-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="00dc3-114">4 bytes</span></span>                              |
| <span data-ttu-id="00dc3-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="00dc3-115">Update Privilege</span></span>  | <span data-ttu-id="00dc3-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="00dc3-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="00dc3-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="00dc3-117">Update Frequency</span></span>  | <span data-ttu-id="00dc3-118">Cuando se configura la replicación.</span><span class="sxs-lookup"><span data-stu-id="00dc3-118">When replication is setup.</span></span>           |
| <span data-ttu-id="00dc3-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="00dc3-119">Attribute-Id</span></span>      | <span data-ttu-id="00dc3-120">1.2.840.113556.1.4.1403</span><span class="sxs-lookup"><span data-stu-id="00dc3-120">1.2.840.113556.1.4.1403</span></span>              |
| <span data-ttu-id="00dc3-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="00dc3-121">System-Id-Guid</span></span>    | <span data-ttu-id="00dc3-122">c3bb7054-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="00dc3-122">c3bb7054-d34b-11d2-999a-0000f87a57d4</span></span> |
| <span data-ttu-id="00dc3-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00dc3-123">Syntax</span></span>            | [<span data-ttu-id="00dc3-124">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="00dc3-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="00dc3-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="00dc3-125">Implementations</span></span>

-   [<span data-ttu-id="00dc3-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="00dc3-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="00dc3-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="00dc3-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="00dc3-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="00dc3-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="00dc3-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="00dc3-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="00dc3-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="00dc3-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="00dc3-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="00dc3-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="00dc3-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="00dc3-132">Windows 2000 Server</span></span>



| <span data-ttu-id="00dc3-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="00dc3-133">Entry</span></span> | <span data-ttu-id="00dc3-134">Value</span><span class="sxs-lookup"><span data-stu-id="00dc3-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="00dc3-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="00dc3-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="00dc3-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00dc3-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="00dc3-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="00dc3-137">System-Only</span></span>            | <span data-ttu-id="00dc3-138">False</span><span class="sxs-lookup"><span data-stu-id="00dc3-138">False</span></span>                                                               |
| <span data-ttu-id="00dc3-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="00dc3-139">Is-Single-Valued</span></span>       | <span data-ttu-id="00dc3-140">True</span><span class="sxs-lookup"><span data-stu-id="00dc3-140">True</span></span>                                                                |
| <span data-ttu-id="00dc3-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="00dc3-141">Is Indexed</span></span>             | <span data-ttu-id="00dc3-142">False</span><span class="sxs-lookup"><span data-stu-id="00dc3-142">False</span></span>                                                               |
| <span data-ttu-id="00dc3-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="00dc3-143">In Global Catalog</span></span>      | <span data-ttu-id="00dc3-144">False</span><span class="sxs-lookup"><span data-stu-id="00dc3-144">False</span></span>                                                               |
| <span data-ttu-id="00dc3-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="00dc3-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="00dc3-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="00dc3-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="00dc3-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00dc3-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="00dc3-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00dc3-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="00dc3-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00dc3-149">Search-Flags</span></span>           | <span data-ttu-id="00dc3-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00dc3-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="00dc3-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00dc3-151">System-Flags</span></span>           | <span data-ttu-id="00dc3-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00dc3-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="00dc3-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="00dc3-153">Classes used in</span></span>        | [<span data-ttu-id="00dc3-154">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="00dc3-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="00dc3-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00dc3-155">Windows Server 2003</span></span>



| <span data-ttu-id="00dc3-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="00dc3-156">Entry</span></span> | <span data-ttu-id="00dc3-157">Value</span><span class="sxs-lookup"><span data-stu-id="00dc3-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="00dc3-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="00dc3-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="00dc3-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00dc3-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="00dc3-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="00dc3-160">System-Only</span></span>            | <span data-ttu-id="00dc3-161">False</span><span class="sxs-lookup"><span data-stu-id="00dc3-161">False</span></span>                                                               |
| <span data-ttu-id="00dc3-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="00dc3-162">Is-Single-Valued</span></span>       | <span data-ttu-id="00dc3-163">True</span><span class="sxs-lookup"><span data-stu-id="00dc3-163">True</span></span>                                                                |
| <span data-ttu-id="00dc3-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="00dc3-164">Is Indexed</span></span>             | <span data-ttu-id="00dc3-165">False</span><span class="sxs-lookup"><span data-stu-id="00dc3-165">False</span></span>                                                               |
| <span data-ttu-id="00dc3-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="00dc3-166">In Global Catalog</span></span>      | <span data-ttu-id="00dc3-167">False</span><span class="sxs-lookup"><span data-stu-id="00dc3-167">False</span></span>                                                               |
| <span data-ttu-id="00dc3-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="00dc3-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="00dc3-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="00dc3-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="00dc3-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00dc3-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="00dc3-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00dc3-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="00dc3-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00dc3-172">Search-Flags</span></span>           | <span data-ttu-id="00dc3-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00dc3-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="00dc3-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00dc3-174">System-Flags</span></span>           | <span data-ttu-id="00dc3-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00dc3-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="00dc3-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="00dc3-176">Classes used in</span></span>        | [<span data-ttu-id="00dc3-177">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="00dc3-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="00dc3-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="00dc3-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="00dc3-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="00dc3-179">Entry</span></span> | <span data-ttu-id="00dc3-180">Value</span><span class="sxs-lookup"><span data-stu-id="00dc3-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="00dc3-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="00dc3-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="00dc3-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00dc3-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="00dc3-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="00dc3-183">System-Only</span></span>            | <span data-ttu-id="00dc3-184">False</span><span class="sxs-lookup"><span data-stu-id="00dc3-184">False</span></span>                                                               |
| <span data-ttu-id="00dc3-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="00dc3-185">Is-Single-Valued</span></span>       | <span data-ttu-id="00dc3-186">True</span><span class="sxs-lookup"><span data-stu-id="00dc3-186">True</span></span>                                                                |
| <span data-ttu-id="00dc3-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="00dc3-187">Is Indexed</span></span>             | <span data-ttu-id="00dc3-188">False</span><span class="sxs-lookup"><span data-stu-id="00dc3-188">False</span></span>                                                               |
| <span data-ttu-id="00dc3-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="00dc3-189">In Global Catalog</span></span>      | <span data-ttu-id="00dc3-190">False</span><span class="sxs-lookup"><span data-stu-id="00dc3-190">False</span></span>                                                               |
| <span data-ttu-id="00dc3-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="00dc3-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="00dc3-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="00dc3-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="00dc3-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00dc3-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="00dc3-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00dc3-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="00dc3-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00dc3-195">Search-Flags</span></span>           | <span data-ttu-id="00dc3-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00dc3-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="00dc3-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00dc3-197">System-Flags</span></span>           | <span data-ttu-id="00dc3-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00dc3-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="00dc3-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="00dc3-199">Classes used in</span></span>        | [<span data-ttu-id="00dc3-200">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="00dc3-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="00dc3-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00dc3-201">Windows Server 2008</span></span>



| <span data-ttu-id="00dc3-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="00dc3-202">Entry</span></span> | <span data-ttu-id="00dc3-203">Value</span><span class="sxs-lookup"><span data-stu-id="00dc3-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="00dc3-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="00dc3-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="00dc3-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00dc3-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="00dc3-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="00dc3-206">System-Only</span></span>            | <span data-ttu-id="00dc3-207">False</span><span class="sxs-lookup"><span data-stu-id="00dc3-207">False</span></span>                                                               |
| <span data-ttu-id="00dc3-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="00dc3-208">Is-Single-Valued</span></span>       | <span data-ttu-id="00dc3-209">True</span><span class="sxs-lookup"><span data-stu-id="00dc3-209">True</span></span>                                                                |
| <span data-ttu-id="00dc3-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="00dc3-210">Is Indexed</span></span>             | <span data-ttu-id="00dc3-211">False</span><span class="sxs-lookup"><span data-stu-id="00dc3-211">False</span></span>                                                               |
| <span data-ttu-id="00dc3-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="00dc3-212">In Global Catalog</span></span>      | <span data-ttu-id="00dc3-213">False</span><span class="sxs-lookup"><span data-stu-id="00dc3-213">False</span></span>                                                               |
| <span data-ttu-id="00dc3-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="00dc3-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="00dc3-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="00dc3-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="00dc3-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00dc3-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="00dc3-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00dc3-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="00dc3-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00dc3-218">Search-Flags</span></span>           | <span data-ttu-id="00dc3-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00dc3-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="00dc3-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00dc3-220">System-Flags</span></span>           | <span data-ttu-id="00dc3-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00dc3-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="00dc3-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="00dc3-222">Classes used in</span></span>        | [<span data-ttu-id="00dc3-223">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="00dc3-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="00dc3-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="00dc3-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="00dc3-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="00dc3-225">Entry</span></span> | <span data-ttu-id="00dc3-226">Value</span><span class="sxs-lookup"><span data-stu-id="00dc3-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="00dc3-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="00dc3-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="00dc3-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00dc3-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="00dc3-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="00dc3-229">System-Only</span></span>            | <span data-ttu-id="00dc3-230">False</span><span class="sxs-lookup"><span data-stu-id="00dc3-230">False</span></span>                                                               |
| <span data-ttu-id="00dc3-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="00dc3-231">Is-Single-Valued</span></span>       | <span data-ttu-id="00dc3-232">True</span><span class="sxs-lookup"><span data-stu-id="00dc3-232">True</span></span>                                                                |
| <span data-ttu-id="00dc3-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="00dc3-233">Is Indexed</span></span>             | <span data-ttu-id="00dc3-234">False</span><span class="sxs-lookup"><span data-stu-id="00dc3-234">False</span></span>                                                               |
| <span data-ttu-id="00dc3-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="00dc3-235">In Global Catalog</span></span>      | <span data-ttu-id="00dc3-236">False</span><span class="sxs-lookup"><span data-stu-id="00dc3-236">False</span></span>                                                               |
| <span data-ttu-id="00dc3-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="00dc3-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="00dc3-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="00dc3-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="00dc3-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00dc3-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="00dc3-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00dc3-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="00dc3-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00dc3-241">Search-Flags</span></span>           | <span data-ttu-id="00dc3-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00dc3-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="00dc3-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00dc3-243">System-Flags</span></span>           | <span data-ttu-id="00dc3-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00dc3-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="00dc3-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="00dc3-245">Classes used in</span></span>        | [<span data-ttu-id="00dc3-246">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="00dc3-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="00dc3-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="00dc3-247">Windows Server 2012</span></span>



| <span data-ttu-id="00dc3-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="00dc3-248">Entry</span></span> | <span data-ttu-id="00dc3-249">Value</span><span class="sxs-lookup"><span data-stu-id="00dc3-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="00dc3-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="00dc3-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="00dc3-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00dc3-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="00dc3-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="00dc3-252">System-Only</span></span>            | <span data-ttu-id="00dc3-253">False</span><span class="sxs-lookup"><span data-stu-id="00dc3-253">False</span></span>                                                               |
| <span data-ttu-id="00dc3-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="00dc3-254">Is-Single-Valued</span></span>       | <span data-ttu-id="00dc3-255">True</span><span class="sxs-lookup"><span data-stu-id="00dc3-255">True</span></span>                                                                |
| <span data-ttu-id="00dc3-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="00dc3-256">Is Indexed</span></span>             | <span data-ttu-id="00dc3-257">False</span><span class="sxs-lookup"><span data-stu-id="00dc3-257">False</span></span>                                                               |
| <span data-ttu-id="00dc3-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="00dc3-258">In Global Catalog</span></span>      | <span data-ttu-id="00dc3-259">False</span><span class="sxs-lookup"><span data-stu-id="00dc3-259">False</span></span>                                                               |
| <span data-ttu-id="00dc3-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="00dc3-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="00dc3-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="00dc3-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="00dc3-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00dc3-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="00dc3-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00dc3-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="00dc3-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00dc3-264">Search-Flags</span></span>           | <span data-ttu-id="00dc3-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00dc3-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="00dc3-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00dc3-266">System-Flags</span></span>           | <span data-ttu-id="00dc3-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00dc3-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="00dc3-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="00dc3-268">Classes used in</span></span>        | [<span data-ttu-id="00dc3-269">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="00dc3-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





