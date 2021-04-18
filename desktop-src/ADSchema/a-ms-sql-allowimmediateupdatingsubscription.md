---
title: Atributo MS-SQL-AllowImmediateUpdatingSubscription
description: True si la publicación permite suscripciones de actualización de transacciones sincronizadas.
ms.assetid: 7efa4b8f-77ad-4f68-9852-7dac9f922d95
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de MS-SQL-AllowImmediateUpdatingSubscription
- Esquema de AD de atributos de mS-SQL-AllowImmediateUpdatingSubscription
topic_type:
- apiref
api_name:
- MS-SQL-AllowImmediateUpdatingSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fed7970aa4b4f26a7221ea9a0c3d4e279ddc5db1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535787"
---
# <a name="ms-sql-allowimmediateupdatingsubscription-attribute"></a><span data-ttu-id="322ad-105">Atributo MS-SQL-AllowImmediateUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="322ad-105">MS-SQL-AllowImmediateUpdatingSubscription attribute</span></span>

<span data-ttu-id="322ad-106">True si la publicación permite suscripciones de actualización de transacciones sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="322ad-106">True if the publication allows synchronized transaction updating subscriptions.</span></span>



| <span data-ttu-id="322ad-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="322ad-107">Entry</span></span> | <span data-ttu-id="322ad-108">Value</span><span class="sxs-lookup"><span data-stu-id="322ad-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="322ad-109">CN</span><span class="sxs-lookup"><span data-stu-id="322ad-109">CN</span></span>                | <span data-ttu-id="322ad-110">MS-SQL-AllowImmediateUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="322ad-110">MS-SQL-AllowImmediateUpdatingSubscription</span></span> |
| <span data-ttu-id="322ad-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="322ad-111">Ldap-Display-Name</span></span> | <span data-ttu-id="322ad-112">mS-SQL-AllowImmediateUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="322ad-112">mS-SQL-AllowImmediateUpdatingSubscription</span></span> |
| <span data-ttu-id="322ad-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="322ad-113">Size</span></span>              | <span data-ttu-id="322ad-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="322ad-114">4 bytes</span></span>                                   |
| <span data-ttu-id="322ad-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="322ad-115">Update Privilege</span></span>  | <span data-ttu-id="322ad-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="322ad-116">This value is set by the system.</span></span>          |
| <span data-ttu-id="322ad-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="322ad-117">Update Frequency</span></span>  | <span data-ttu-id="322ad-118">Cuando se configura la replicación.</span><span class="sxs-lookup"><span data-stu-id="322ad-118">When replication is setup.</span></span>                |
| <span data-ttu-id="322ad-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="322ad-119">Attribute-Id</span></span>      | <span data-ttu-id="322ad-120">1.2.840.113556.1.4.1404</span><span class="sxs-lookup"><span data-stu-id="322ad-120">1.2.840.113556.1.4.1404</span></span>                   |
| <span data-ttu-id="322ad-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="322ad-121">System-Id-Guid</span></span>    | <span data-ttu-id="322ad-122">c4186b6e-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="322ad-122">c4186b6e-d34b-11d2-999a-0000f87a57d4</span></span>      |
| <span data-ttu-id="322ad-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="322ad-123">Syntax</span></span>            | [<span data-ttu-id="322ad-124">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="322ad-124">**Boolean**</span></span>](s-boolean.md)              |



## <a name="implementations"></a><span data-ttu-id="322ad-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="322ad-125">Implementations</span></span>

-   [<span data-ttu-id="322ad-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="322ad-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="322ad-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="322ad-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="322ad-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="322ad-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="322ad-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="322ad-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="322ad-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="322ad-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="322ad-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="322ad-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="322ad-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="322ad-132">Windows 2000 Server</span></span>



| <span data-ttu-id="322ad-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="322ad-133">Entry</span></span> | <span data-ttu-id="322ad-134">Value</span><span class="sxs-lookup"><span data-stu-id="322ad-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="322ad-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="322ad-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="322ad-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="322ad-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="322ad-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="322ad-137">System-Only</span></span>            | <span data-ttu-id="322ad-138">False</span><span class="sxs-lookup"><span data-stu-id="322ad-138">False</span></span>                                                               |
| <span data-ttu-id="322ad-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="322ad-139">Is-Single-Valued</span></span>       | <span data-ttu-id="322ad-140">True</span><span class="sxs-lookup"><span data-stu-id="322ad-140">True</span></span>                                                                |
| <span data-ttu-id="322ad-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="322ad-141">Is Indexed</span></span>             | <span data-ttu-id="322ad-142">False</span><span class="sxs-lookup"><span data-stu-id="322ad-142">False</span></span>                                                               |
| <span data-ttu-id="322ad-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="322ad-143">In Global Catalog</span></span>      | <span data-ttu-id="322ad-144">False</span><span class="sxs-lookup"><span data-stu-id="322ad-144">False</span></span>                                                               |
| <span data-ttu-id="322ad-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="322ad-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="322ad-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="322ad-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="322ad-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="322ad-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="322ad-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="322ad-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="322ad-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="322ad-149">Search-Flags</span></span>           | <span data-ttu-id="322ad-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="322ad-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="322ad-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="322ad-151">System-Flags</span></span>           | <span data-ttu-id="322ad-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="322ad-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="322ad-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="322ad-153">Classes used in</span></span>        | [<span data-ttu-id="322ad-154">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="322ad-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="322ad-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="322ad-155">Windows Server 2003</span></span>



| <span data-ttu-id="322ad-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="322ad-156">Entry</span></span> | <span data-ttu-id="322ad-157">Value</span><span class="sxs-lookup"><span data-stu-id="322ad-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="322ad-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="322ad-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="322ad-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="322ad-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="322ad-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="322ad-160">System-Only</span></span>            | <span data-ttu-id="322ad-161">False</span><span class="sxs-lookup"><span data-stu-id="322ad-161">False</span></span>                                                               |
| <span data-ttu-id="322ad-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="322ad-162">Is-Single-Valued</span></span>       | <span data-ttu-id="322ad-163">True</span><span class="sxs-lookup"><span data-stu-id="322ad-163">True</span></span>                                                                |
| <span data-ttu-id="322ad-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="322ad-164">Is Indexed</span></span>             | <span data-ttu-id="322ad-165">False</span><span class="sxs-lookup"><span data-stu-id="322ad-165">False</span></span>                                                               |
| <span data-ttu-id="322ad-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="322ad-166">In Global Catalog</span></span>      | <span data-ttu-id="322ad-167">False</span><span class="sxs-lookup"><span data-stu-id="322ad-167">False</span></span>                                                               |
| <span data-ttu-id="322ad-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="322ad-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="322ad-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="322ad-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="322ad-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="322ad-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="322ad-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="322ad-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="322ad-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="322ad-172">Search-Flags</span></span>           | <span data-ttu-id="322ad-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="322ad-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="322ad-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="322ad-174">System-Flags</span></span>           | <span data-ttu-id="322ad-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="322ad-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="322ad-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="322ad-176">Classes used in</span></span>        | [<span data-ttu-id="322ad-177">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="322ad-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="322ad-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="322ad-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="322ad-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="322ad-179">Entry</span></span> | <span data-ttu-id="322ad-180">Value</span><span class="sxs-lookup"><span data-stu-id="322ad-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="322ad-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="322ad-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="322ad-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="322ad-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="322ad-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="322ad-183">System-Only</span></span>            | <span data-ttu-id="322ad-184">False</span><span class="sxs-lookup"><span data-stu-id="322ad-184">False</span></span>                                                               |
| <span data-ttu-id="322ad-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="322ad-185">Is-Single-Valued</span></span>       | <span data-ttu-id="322ad-186">True</span><span class="sxs-lookup"><span data-stu-id="322ad-186">True</span></span>                                                                |
| <span data-ttu-id="322ad-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="322ad-187">Is Indexed</span></span>             | <span data-ttu-id="322ad-188">False</span><span class="sxs-lookup"><span data-stu-id="322ad-188">False</span></span>                                                               |
| <span data-ttu-id="322ad-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="322ad-189">In Global Catalog</span></span>      | <span data-ttu-id="322ad-190">False</span><span class="sxs-lookup"><span data-stu-id="322ad-190">False</span></span>                                                               |
| <span data-ttu-id="322ad-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="322ad-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="322ad-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="322ad-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="322ad-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="322ad-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="322ad-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="322ad-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="322ad-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="322ad-195">Search-Flags</span></span>           | <span data-ttu-id="322ad-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="322ad-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="322ad-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="322ad-197">System-Flags</span></span>           | <span data-ttu-id="322ad-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="322ad-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="322ad-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="322ad-199">Classes used in</span></span>        | [<span data-ttu-id="322ad-200">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="322ad-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="322ad-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="322ad-201">Windows Server 2008</span></span>



| <span data-ttu-id="322ad-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="322ad-202">Entry</span></span> | <span data-ttu-id="322ad-203">Value</span><span class="sxs-lookup"><span data-stu-id="322ad-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="322ad-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="322ad-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="322ad-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="322ad-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="322ad-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="322ad-206">System-Only</span></span>            | <span data-ttu-id="322ad-207">False</span><span class="sxs-lookup"><span data-stu-id="322ad-207">False</span></span>                                                               |
| <span data-ttu-id="322ad-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="322ad-208">Is-Single-Valued</span></span>       | <span data-ttu-id="322ad-209">True</span><span class="sxs-lookup"><span data-stu-id="322ad-209">True</span></span>                                                                |
| <span data-ttu-id="322ad-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="322ad-210">Is Indexed</span></span>             | <span data-ttu-id="322ad-211">False</span><span class="sxs-lookup"><span data-stu-id="322ad-211">False</span></span>                                                               |
| <span data-ttu-id="322ad-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="322ad-212">In Global Catalog</span></span>      | <span data-ttu-id="322ad-213">False</span><span class="sxs-lookup"><span data-stu-id="322ad-213">False</span></span>                                                               |
| <span data-ttu-id="322ad-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="322ad-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="322ad-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="322ad-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="322ad-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="322ad-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="322ad-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="322ad-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="322ad-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="322ad-218">Search-Flags</span></span>           | <span data-ttu-id="322ad-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="322ad-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="322ad-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="322ad-220">System-Flags</span></span>           | <span data-ttu-id="322ad-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="322ad-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="322ad-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="322ad-222">Classes used in</span></span>        | [<span data-ttu-id="322ad-223">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="322ad-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="322ad-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="322ad-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="322ad-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="322ad-225">Entry</span></span> | <span data-ttu-id="322ad-226">Value</span><span class="sxs-lookup"><span data-stu-id="322ad-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="322ad-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="322ad-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="322ad-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="322ad-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="322ad-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="322ad-229">System-Only</span></span>            | <span data-ttu-id="322ad-230">False</span><span class="sxs-lookup"><span data-stu-id="322ad-230">False</span></span>                                                               |
| <span data-ttu-id="322ad-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="322ad-231">Is-Single-Valued</span></span>       | <span data-ttu-id="322ad-232">True</span><span class="sxs-lookup"><span data-stu-id="322ad-232">True</span></span>                                                                |
| <span data-ttu-id="322ad-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="322ad-233">Is Indexed</span></span>             | <span data-ttu-id="322ad-234">False</span><span class="sxs-lookup"><span data-stu-id="322ad-234">False</span></span>                                                               |
| <span data-ttu-id="322ad-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="322ad-235">In Global Catalog</span></span>      | <span data-ttu-id="322ad-236">False</span><span class="sxs-lookup"><span data-stu-id="322ad-236">False</span></span>                                                               |
| <span data-ttu-id="322ad-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="322ad-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="322ad-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="322ad-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="322ad-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="322ad-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="322ad-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="322ad-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="322ad-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="322ad-241">Search-Flags</span></span>           | <span data-ttu-id="322ad-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="322ad-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="322ad-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="322ad-243">System-Flags</span></span>           | <span data-ttu-id="322ad-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="322ad-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="322ad-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="322ad-245">Classes used in</span></span>        | [<span data-ttu-id="322ad-246">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="322ad-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="322ad-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="322ad-247">Windows Server 2012</span></span>



| <span data-ttu-id="322ad-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="322ad-248">Entry</span></span> | <span data-ttu-id="322ad-249">Value</span><span class="sxs-lookup"><span data-stu-id="322ad-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="322ad-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="322ad-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="322ad-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="322ad-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="322ad-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="322ad-252">System-Only</span></span>            | <span data-ttu-id="322ad-253">False</span><span class="sxs-lookup"><span data-stu-id="322ad-253">False</span></span>                                                               |
| <span data-ttu-id="322ad-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="322ad-254">Is-Single-Valued</span></span>       | <span data-ttu-id="322ad-255">True</span><span class="sxs-lookup"><span data-stu-id="322ad-255">True</span></span>                                                                |
| <span data-ttu-id="322ad-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="322ad-256">Is Indexed</span></span>             | <span data-ttu-id="322ad-257">False</span><span class="sxs-lookup"><span data-stu-id="322ad-257">False</span></span>                                                               |
| <span data-ttu-id="322ad-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="322ad-258">In Global Catalog</span></span>      | <span data-ttu-id="322ad-259">False</span><span class="sxs-lookup"><span data-stu-id="322ad-259">False</span></span>                                                               |
| <span data-ttu-id="322ad-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="322ad-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="322ad-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="322ad-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="322ad-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="322ad-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="322ad-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="322ad-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="322ad-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="322ad-264">Search-Flags</span></span>           | <span data-ttu-id="322ad-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="322ad-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="322ad-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="322ad-266">System-Flags</span></span>           | <span data-ttu-id="322ad-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="322ad-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="322ad-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="322ad-268">Classes used in</span></span>        | [<span data-ttu-id="322ad-269">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="322ad-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





