---
title: Atributo MS-SQL-AllowQueuedUpdatingSubscription
description: True para permitir las transacciones en cola al actualizar las suscripciones.
ms.assetid: 132c107f-8586-48db-b70c-027c619aadf7
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de MS-SQL-AllowQueuedUpdatingSubscription
- Esquema de AD de atributos de mS-SQL-AllowQueuedUpdatingSubscription
topic_type:
- apiref
api_name:
- MS-SQL-AllowQueuedUpdatingSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2056a04b6e0f155c156cde06975e96eb13f61eb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905812"
---
# <a name="ms-sql-allowqueuedupdatingsubscription-attribute"></a><span data-ttu-id="a20cb-105">Atributo MS-SQL-AllowQueuedUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="a20cb-105">MS-SQL-AllowQueuedUpdatingSubscription attribute</span></span>

<span data-ttu-id="a20cb-106">True para permitir las transacciones en cola al actualizar las suscripciones.</span><span class="sxs-lookup"><span data-stu-id="a20cb-106">True to allow queued transactions when updating subscriptions.</span></span>



| <span data-ttu-id="a20cb-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a20cb-107">Entry</span></span> | <span data-ttu-id="a20cb-108">Value</span><span class="sxs-lookup"><span data-stu-id="a20cb-108">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="a20cb-109">CN</span><span class="sxs-lookup"><span data-stu-id="a20cb-109">CN</span></span>                | <span data-ttu-id="a20cb-110">MS-SQL-AllowQueuedUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="a20cb-110">MS-SQL-AllowQueuedUpdatingSubscription</span></span> |
| <span data-ttu-id="a20cb-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="a20cb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a20cb-112">mS-SQL-AllowQueuedUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="a20cb-112">mS-SQL-AllowQueuedUpdatingSubscription</span></span> |
| <span data-ttu-id="a20cb-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a20cb-113">Size</span></span>              | <span data-ttu-id="a20cb-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="a20cb-114">4 bytes</span></span>                                |
| <span data-ttu-id="a20cb-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="a20cb-115">Update Privilege</span></span>  | <span data-ttu-id="a20cb-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="a20cb-116">This value is set by the system.</span></span>       |
| <span data-ttu-id="a20cb-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="a20cb-117">Update Frequency</span></span>  | <span data-ttu-id="a20cb-118">Cuando se configura la replicación.</span><span class="sxs-lookup"><span data-stu-id="a20cb-118">When replication is setup.</span></span>             |
| <span data-ttu-id="a20cb-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a20cb-119">Attribute-Id</span></span>      | <span data-ttu-id="a20cb-120">1.2.840.113556.1.4.1405</span><span class="sxs-lookup"><span data-stu-id="a20cb-120">1.2.840.113556.1.4.1405</span></span>                |
| <span data-ttu-id="a20cb-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a20cb-121">System-Id-Guid</span></span>    | <span data-ttu-id="a20cb-122">c458ca80-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="a20cb-122">c458ca80-d34b-11d2-999a-0000f87a57d4</span></span>   |
| <span data-ttu-id="a20cb-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a20cb-123">Syntax</span></span>            | [<span data-ttu-id="a20cb-124">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="a20cb-124">**Boolean**</span></span>](s-boolean.md)           |



## <a name="implementations"></a><span data-ttu-id="a20cb-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="a20cb-125">Implementations</span></span>

-   [<span data-ttu-id="a20cb-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a20cb-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a20cb-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a20cb-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a20cb-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a20cb-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a20cb-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a20cb-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a20cb-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a20cb-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a20cb-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a20cb-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a20cb-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a20cb-132">Windows 2000 Server</span></span>



| <span data-ttu-id="a20cb-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="a20cb-133">Entry</span></span> | <span data-ttu-id="a20cb-134">Value</span><span class="sxs-lookup"><span data-stu-id="a20cb-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a20cb-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a20cb-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a20cb-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a20cb-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a20cb-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="a20cb-137">System-Only</span></span>            | <span data-ttu-id="a20cb-138">False</span><span class="sxs-lookup"><span data-stu-id="a20cb-138">False</span></span>                                                               |
| <span data-ttu-id="a20cb-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a20cb-139">Is-Single-Valued</span></span>       | <span data-ttu-id="a20cb-140">True</span><span class="sxs-lookup"><span data-stu-id="a20cb-140">True</span></span>                                                                |
| <span data-ttu-id="a20cb-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a20cb-141">Is Indexed</span></span>             | <span data-ttu-id="a20cb-142">False</span><span class="sxs-lookup"><span data-stu-id="a20cb-142">False</span></span>                                                               |
| <span data-ttu-id="a20cb-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a20cb-143">In Global Catalog</span></span>      | <span data-ttu-id="a20cb-144">False</span><span class="sxs-lookup"><span data-stu-id="a20cb-144">False</span></span>                                                               |
| <span data-ttu-id="a20cb-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a20cb-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="a20cb-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a20cb-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a20cb-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a20cb-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a20cb-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a20cb-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a20cb-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a20cb-149">Search-Flags</span></span>           | <span data-ttu-id="a20cb-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a20cb-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="a20cb-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a20cb-151">System-Flags</span></span>           | <span data-ttu-id="a20cb-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a20cb-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="a20cb-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a20cb-153">Classes used in</span></span>        | [<span data-ttu-id="a20cb-154">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a20cb-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a20cb-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a20cb-155">Windows Server 2003</span></span>



| <span data-ttu-id="a20cb-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="a20cb-156">Entry</span></span> | <span data-ttu-id="a20cb-157">Value</span><span class="sxs-lookup"><span data-stu-id="a20cb-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a20cb-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a20cb-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a20cb-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a20cb-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a20cb-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="a20cb-160">System-Only</span></span>            | <span data-ttu-id="a20cb-161">False</span><span class="sxs-lookup"><span data-stu-id="a20cb-161">False</span></span>                                                               |
| <span data-ttu-id="a20cb-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a20cb-162">Is-Single-Valued</span></span>       | <span data-ttu-id="a20cb-163">True</span><span class="sxs-lookup"><span data-stu-id="a20cb-163">True</span></span>                                                                |
| <span data-ttu-id="a20cb-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a20cb-164">Is Indexed</span></span>             | <span data-ttu-id="a20cb-165">False</span><span class="sxs-lookup"><span data-stu-id="a20cb-165">False</span></span>                                                               |
| <span data-ttu-id="a20cb-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a20cb-166">In Global Catalog</span></span>      | <span data-ttu-id="a20cb-167">False</span><span class="sxs-lookup"><span data-stu-id="a20cb-167">False</span></span>                                                               |
| <span data-ttu-id="a20cb-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a20cb-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="a20cb-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a20cb-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a20cb-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a20cb-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a20cb-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a20cb-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a20cb-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a20cb-172">Search-Flags</span></span>           | <span data-ttu-id="a20cb-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a20cb-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="a20cb-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a20cb-174">System-Flags</span></span>           | <span data-ttu-id="a20cb-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a20cb-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="a20cb-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a20cb-176">Classes used in</span></span>        | [<span data-ttu-id="a20cb-177">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a20cb-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a20cb-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a20cb-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a20cb-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="a20cb-179">Entry</span></span> | <span data-ttu-id="a20cb-180">Value</span><span class="sxs-lookup"><span data-stu-id="a20cb-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a20cb-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a20cb-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a20cb-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a20cb-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a20cb-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="a20cb-183">System-Only</span></span>            | <span data-ttu-id="a20cb-184">False</span><span class="sxs-lookup"><span data-stu-id="a20cb-184">False</span></span>                                                               |
| <span data-ttu-id="a20cb-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a20cb-185">Is-Single-Valued</span></span>       | <span data-ttu-id="a20cb-186">True</span><span class="sxs-lookup"><span data-stu-id="a20cb-186">True</span></span>                                                                |
| <span data-ttu-id="a20cb-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a20cb-187">Is Indexed</span></span>             | <span data-ttu-id="a20cb-188">False</span><span class="sxs-lookup"><span data-stu-id="a20cb-188">False</span></span>                                                               |
| <span data-ttu-id="a20cb-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a20cb-189">In Global Catalog</span></span>      | <span data-ttu-id="a20cb-190">False</span><span class="sxs-lookup"><span data-stu-id="a20cb-190">False</span></span>                                                               |
| <span data-ttu-id="a20cb-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a20cb-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="a20cb-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a20cb-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a20cb-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a20cb-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a20cb-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a20cb-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a20cb-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a20cb-195">Search-Flags</span></span>           | <span data-ttu-id="a20cb-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a20cb-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="a20cb-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a20cb-197">System-Flags</span></span>           | <span data-ttu-id="a20cb-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a20cb-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="a20cb-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a20cb-199">Classes used in</span></span>        | [<span data-ttu-id="a20cb-200">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a20cb-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a20cb-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a20cb-201">Windows Server 2008</span></span>



| <span data-ttu-id="a20cb-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="a20cb-202">Entry</span></span> | <span data-ttu-id="a20cb-203">Value</span><span class="sxs-lookup"><span data-stu-id="a20cb-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a20cb-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a20cb-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a20cb-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a20cb-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a20cb-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="a20cb-206">System-Only</span></span>            | <span data-ttu-id="a20cb-207">False</span><span class="sxs-lookup"><span data-stu-id="a20cb-207">False</span></span>                                                               |
| <span data-ttu-id="a20cb-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a20cb-208">Is-Single-Valued</span></span>       | <span data-ttu-id="a20cb-209">True</span><span class="sxs-lookup"><span data-stu-id="a20cb-209">True</span></span>                                                                |
| <span data-ttu-id="a20cb-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a20cb-210">Is Indexed</span></span>             | <span data-ttu-id="a20cb-211">False</span><span class="sxs-lookup"><span data-stu-id="a20cb-211">False</span></span>                                                               |
| <span data-ttu-id="a20cb-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a20cb-212">In Global Catalog</span></span>      | <span data-ttu-id="a20cb-213">False</span><span class="sxs-lookup"><span data-stu-id="a20cb-213">False</span></span>                                                               |
| <span data-ttu-id="a20cb-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a20cb-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="a20cb-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a20cb-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a20cb-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a20cb-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a20cb-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a20cb-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a20cb-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a20cb-218">Search-Flags</span></span>           | <span data-ttu-id="a20cb-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a20cb-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="a20cb-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a20cb-220">System-Flags</span></span>           | <span data-ttu-id="a20cb-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a20cb-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="a20cb-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a20cb-222">Classes used in</span></span>        | [<span data-ttu-id="a20cb-223">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a20cb-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a20cb-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a20cb-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a20cb-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="a20cb-225">Entry</span></span> | <span data-ttu-id="a20cb-226">Value</span><span class="sxs-lookup"><span data-stu-id="a20cb-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a20cb-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a20cb-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a20cb-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a20cb-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a20cb-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="a20cb-229">System-Only</span></span>            | <span data-ttu-id="a20cb-230">False</span><span class="sxs-lookup"><span data-stu-id="a20cb-230">False</span></span>                                                               |
| <span data-ttu-id="a20cb-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a20cb-231">Is-Single-Valued</span></span>       | <span data-ttu-id="a20cb-232">True</span><span class="sxs-lookup"><span data-stu-id="a20cb-232">True</span></span>                                                                |
| <span data-ttu-id="a20cb-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a20cb-233">Is Indexed</span></span>             | <span data-ttu-id="a20cb-234">False</span><span class="sxs-lookup"><span data-stu-id="a20cb-234">False</span></span>                                                               |
| <span data-ttu-id="a20cb-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a20cb-235">In Global Catalog</span></span>      | <span data-ttu-id="a20cb-236">False</span><span class="sxs-lookup"><span data-stu-id="a20cb-236">False</span></span>                                                               |
| <span data-ttu-id="a20cb-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a20cb-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="a20cb-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a20cb-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a20cb-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a20cb-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a20cb-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a20cb-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a20cb-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a20cb-241">Search-Flags</span></span>           | <span data-ttu-id="a20cb-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a20cb-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="a20cb-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a20cb-243">System-Flags</span></span>           | <span data-ttu-id="a20cb-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a20cb-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="a20cb-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a20cb-245">Classes used in</span></span>        | [<span data-ttu-id="a20cb-246">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a20cb-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a20cb-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a20cb-247">Windows Server 2012</span></span>



| <span data-ttu-id="a20cb-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="a20cb-248">Entry</span></span> | <span data-ttu-id="a20cb-249">Value</span><span class="sxs-lookup"><span data-stu-id="a20cb-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a20cb-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a20cb-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a20cb-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a20cb-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a20cb-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="a20cb-252">System-Only</span></span>            | <span data-ttu-id="a20cb-253">False</span><span class="sxs-lookup"><span data-stu-id="a20cb-253">False</span></span>                                                               |
| <span data-ttu-id="a20cb-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a20cb-254">Is-Single-Valued</span></span>       | <span data-ttu-id="a20cb-255">True</span><span class="sxs-lookup"><span data-stu-id="a20cb-255">True</span></span>                                                                |
| <span data-ttu-id="a20cb-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a20cb-256">Is Indexed</span></span>             | <span data-ttu-id="a20cb-257">False</span><span class="sxs-lookup"><span data-stu-id="a20cb-257">False</span></span>                                                               |
| <span data-ttu-id="a20cb-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a20cb-258">In Global Catalog</span></span>      | <span data-ttu-id="a20cb-259">False</span><span class="sxs-lookup"><span data-stu-id="a20cb-259">False</span></span>                                                               |
| <span data-ttu-id="a20cb-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a20cb-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="a20cb-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a20cb-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a20cb-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a20cb-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a20cb-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a20cb-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a20cb-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a20cb-264">Search-Flags</span></span>           | <span data-ttu-id="a20cb-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a20cb-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="a20cb-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a20cb-266">System-Flags</span></span>           | <span data-ttu-id="a20cb-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a20cb-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="a20cb-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a20cb-268">Classes used in</span></span>        | [<span data-ttu-id="a20cb-269">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a20cb-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





