---
title: Atributo MS-SQL-ThirdParty
description: Este atributo indica si los datos de la publicación proceden de un origen de datos distinto de SQL Server. Si procede de otro origen, se establece en TRUE.
ms.assetid: 84d93b9f-0acc-47da-9f1b-44d8468ad53e
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de MS-SQL-ThirdParty
- Esquema de AD de atributos de mS-SQL-ThirdParty
topic_type:
- apiref
api_name:
- MS-SQL-ThirdParty
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc2b60f9589990f6357ee3c4cd24215e8af21df
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804375"
---
# <a name="ms-sql-thirdparty-attribute"></a><span data-ttu-id="c2f75-106">Atributo MS-SQL-ThirdParty</span><span class="sxs-lookup"><span data-stu-id="c2f75-106">MS-SQL-ThirdParty attribute</span></span>

<span data-ttu-id="c2f75-107">Este atributo indica si los datos de la publicación proceden de un origen de datos distinto de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c2f75-107">This attribute indicates whether the publication data is from a data source other than SQL Server.</span></span> <span data-ttu-id="c2f75-108">Si procede de otro origen, se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="c2f75-108">If it is from another source, then it is set to **TRUE**.</span></span>



| <span data-ttu-id="c2f75-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2f75-109">Entry</span></span> | <span data-ttu-id="c2f75-110">Value</span><span class="sxs-lookup"><span data-stu-id="c2f75-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c2f75-111">CN</span><span class="sxs-lookup"><span data-stu-id="c2f75-111">CN</span></span>                | <span data-ttu-id="c2f75-112">MS-SQL-ThirdParty</span><span class="sxs-lookup"><span data-stu-id="c2f75-112">MS-SQL-ThirdParty</span></span>                    |
| <span data-ttu-id="c2f75-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="c2f75-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c2f75-114">mS-SQL-ThirdParty</span><span class="sxs-lookup"><span data-stu-id="c2f75-114">mS-SQL-ThirdParty</span></span>                    |
| <span data-ttu-id="c2f75-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="c2f75-115">Size</span></span>              | <span data-ttu-id="c2f75-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="c2f75-116">4 bytes</span></span>                              |
| <span data-ttu-id="c2f75-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="c2f75-117">Update Privilege</span></span>  | <span data-ttu-id="c2f75-118">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="c2f75-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="c2f75-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="c2f75-119">Update Frequency</span></span>  | <span data-ttu-id="c2f75-120">Cuando se configura la replicación.</span><span class="sxs-lookup"><span data-stu-id="c2f75-120">When replication is setup.</span></span>           |
| <span data-ttu-id="c2f75-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c2f75-121">Attribute-Id</span></span>      | <span data-ttu-id="c2f75-122">1.2.840.113556.1.4.1407</span><span class="sxs-lookup"><span data-stu-id="c2f75-122">1.2.840.113556.1.4.1407</span></span>              |
| <span data-ttu-id="c2f75-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c2f75-123">System-Id-Guid</span></span>    | <span data-ttu-id="c2f75-124">c4e311fc-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="c2f75-124">c4e311fc-d34b-11d2-999a-0000f87a57d4</span></span> |
| <span data-ttu-id="c2f75-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2f75-125">Syntax</span></span>            | [<span data-ttu-id="c2f75-126">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="c2f75-126">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="c2f75-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="c2f75-127">Implementations</span></span>

-   [<span data-ttu-id="c2f75-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c2f75-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c2f75-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c2f75-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c2f75-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c2f75-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c2f75-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c2f75-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c2f75-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c2f75-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c2f75-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c2f75-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c2f75-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c2f75-134">Windows 2000 Server</span></span>



| <span data-ttu-id="c2f75-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2f75-135">Entry</span></span> | <span data-ttu-id="c2f75-136">Value</span><span class="sxs-lookup"><span data-stu-id="c2f75-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c2f75-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c2f75-137">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c2f75-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2f75-138">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c2f75-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2f75-139">System-Only</span></span>            | <span data-ttu-id="c2f75-140">False</span><span class="sxs-lookup"><span data-stu-id="c2f75-140">False</span></span>                                                               |
| <span data-ttu-id="c2f75-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c2f75-141">Is-Single-Valued</span></span>       | <span data-ttu-id="c2f75-142">True</span><span class="sxs-lookup"><span data-stu-id="c2f75-142">True</span></span>                                                                |
| <span data-ttu-id="c2f75-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c2f75-143">Is Indexed</span></span>             | <span data-ttu-id="c2f75-144">False</span><span class="sxs-lookup"><span data-stu-id="c2f75-144">False</span></span>                                                               |
| <span data-ttu-id="c2f75-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c2f75-145">In Global Catalog</span></span>      | <span data-ttu-id="c2f75-146">False</span><span class="sxs-lookup"><span data-stu-id="c2f75-146">False</span></span>                                                               |
| <span data-ttu-id="c2f75-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c2f75-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2f75-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c2f75-148">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="c2f75-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2f75-149">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="c2f75-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2f75-150">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="c2f75-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2f75-151">Search-Flags</span></span>           | <span data-ttu-id="c2f75-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2f75-152">0x00000000</span></span>                                                          |
| <span data-ttu-id="c2f75-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2f75-153">System-Flags</span></span>           | <span data-ttu-id="c2f75-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2f75-154">0x00000010</span></span>                                                          |
| <span data-ttu-id="c2f75-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c2f75-155">Classes used in</span></span>        | [<span data-ttu-id="c2f75-156">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c2f75-156">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c2f75-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c2f75-157">Windows Server 2003</span></span>



| <span data-ttu-id="c2f75-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2f75-158">Entry</span></span> | <span data-ttu-id="c2f75-159">Value</span><span class="sxs-lookup"><span data-stu-id="c2f75-159">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c2f75-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c2f75-160">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c2f75-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2f75-161">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c2f75-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2f75-162">System-Only</span></span>            | <span data-ttu-id="c2f75-163">False</span><span class="sxs-lookup"><span data-stu-id="c2f75-163">False</span></span>                                                               |
| <span data-ttu-id="c2f75-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c2f75-164">Is-Single-Valued</span></span>       | <span data-ttu-id="c2f75-165">True</span><span class="sxs-lookup"><span data-stu-id="c2f75-165">True</span></span>                                                                |
| <span data-ttu-id="c2f75-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c2f75-166">Is Indexed</span></span>             | <span data-ttu-id="c2f75-167">False</span><span class="sxs-lookup"><span data-stu-id="c2f75-167">False</span></span>                                                               |
| <span data-ttu-id="c2f75-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c2f75-168">In Global Catalog</span></span>      | <span data-ttu-id="c2f75-169">False</span><span class="sxs-lookup"><span data-stu-id="c2f75-169">False</span></span>                                                               |
| <span data-ttu-id="c2f75-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c2f75-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2f75-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c2f75-171">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="c2f75-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2f75-172">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="c2f75-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2f75-173">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="c2f75-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2f75-174">Search-Flags</span></span>           | <span data-ttu-id="c2f75-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2f75-175">0x00000000</span></span>                                                          |
| <span data-ttu-id="c2f75-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2f75-176">System-Flags</span></span>           | <span data-ttu-id="c2f75-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2f75-177">0x00000010</span></span>                                                          |
| <span data-ttu-id="c2f75-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c2f75-178">Classes used in</span></span>        | [<span data-ttu-id="c2f75-179">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c2f75-179">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c2f75-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c2f75-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c2f75-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2f75-181">Entry</span></span> | <span data-ttu-id="c2f75-182">Value</span><span class="sxs-lookup"><span data-stu-id="c2f75-182">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c2f75-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c2f75-183">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c2f75-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2f75-184">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c2f75-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2f75-185">System-Only</span></span>            | <span data-ttu-id="c2f75-186">False</span><span class="sxs-lookup"><span data-stu-id="c2f75-186">False</span></span>                                                               |
| <span data-ttu-id="c2f75-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c2f75-187">Is-Single-Valued</span></span>       | <span data-ttu-id="c2f75-188">True</span><span class="sxs-lookup"><span data-stu-id="c2f75-188">True</span></span>                                                                |
| <span data-ttu-id="c2f75-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c2f75-189">Is Indexed</span></span>             | <span data-ttu-id="c2f75-190">False</span><span class="sxs-lookup"><span data-stu-id="c2f75-190">False</span></span>                                                               |
| <span data-ttu-id="c2f75-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c2f75-191">In Global Catalog</span></span>      | <span data-ttu-id="c2f75-192">False</span><span class="sxs-lookup"><span data-stu-id="c2f75-192">False</span></span>                                                               |
| <span data-ttu-id="c2f75-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c2f75-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2f75-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c2f75-194">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="c2f75-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2f75-195">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="c2f75-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2f75-196">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="c2f75-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2f75-197">Search-Flags</span></span>           | <span data-ttu-id="c2f75-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2f75-198">0x00000000</span></span>                                                          |
| <span data-ttu-id="c2f75-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2f75-199">System-Flags</span></span>           | <span data-ttu-id="c2f75-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2f75-200">0x00000010</span></span>                                                          |
| <span data-ttu-id="c2f75-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c2f75-201">Classes used in</span></span>        | [<span data-ttu-id="c2f75-202">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c2f75-202">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c2f75-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2f75-203">Windows Server 2008</span></span>



| <span data-ttu-id="c2f75-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2f75-204">Entry</span></span> | <span data-ttu-id="c2f75-205">Value</span><span class="sxs-lookup"><span data-stu-id="c2f75-205">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c2f75-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c2f75-206">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c2f75-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2f75-207">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c2f75-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2f75-208">System-Only</span></span>            | <span data-ttu-id="c2f75-209">False</span><span class="sxs-lookup"><span data-stu-id="c2f75-209">False</span></span>                                                               |
| <span data-ttu-id="c2f75-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c2f75-210">Is-Single-Valued</span></span>       | <span data-ttu-id="c2f75-211">True</span><span class="sxs-lookup"><span data-stu-id="c2f75-211">True</span></span>                                                                |
| <span data-ttu-id="c2f75-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c2f75-212">Is Indexed</span></span>             | <span data-ttu-id="c2f75-213">False</span><span class="sxs-lookup"><span data-stu-id="c2f75-213">False</span></span>                                                               |
| <span data-ttu-id="c2f75-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c2f75-214">In Global Catalog</span></span>      | <span data-ttu-id="c2f75-215">False</span><span class="sxs-lookup"><span data-stu-id="c2f75-215">False</span></span>                                                               |
| <span data-ttu-id="c2f75-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c2f75-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2f75-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c2f75-217">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="c2f75-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2f75-218">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="c2f75-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2f75-219">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="c2f75-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2f75-220">Search-Flags</span></span>           | <span data-ttu-id="c2f75-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2f75-221">0x00000000</span></span>                                                          |
| <span data-ttu-id="c2f75-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2f75-222">System-Flags</span></span>           | <span data-ttu-id="c2f75-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2f75-223">0x00000010</span></span>                                                          |
| <span data-ttu-id="c2f75-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c2f75-224">Classes used in</span></span>        | [<span data-ttu-id="c2f75-225">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c2f75-225">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c2f75-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2f75-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c2f75-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2f75-227">Entry</span></span> | <span data-ttu-id="c2f75-228">Value</span><span class="sxs-lookup"><span data-stu-id="c2f75-228">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c2f75-229">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c2f75-229">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c2f75-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2f75-230">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c2f75-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2f75-231">System-Only</span></span>            | <span data-ttu-id="c2f75-232">False</span><span class="sxs-lookup"><span data-stu-id="c2f75-232">False</span></span>                                                               |
| <span data-ttu-id="c2f75-233">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c2f75-233">Is-Single-Valued</span></span>       | <span data-ttu-id="c2f75-234">True</span><span class="sxs-lookup"><span data-stu-id="c2f75-234">True</span></span>                                                                |
| <span data-ttu-id="c2f75-235">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c2f75-235">Is Indexed</span></span>             | <span data-ttu-id="c2f75-236">False</span><span class="sxs-lookup"><span data-stu-id="c2f75-236">False</span></span>                                                               |
| <span data-ttu-id="c2f75-237">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c2f75-237">In Global Catalog</span></span>      | <span data-ttu-id="c2f75-238">False</span><span class="sxs-lookup"><span data-stu-id="c2f75-238">False</span></span>                                                               |
| <span data-ttu-id="c2f75-239">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c2f75-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2f75-240">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c2f75-240">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="c2f75-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2f75-241">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="c2f75-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2f75-242">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="c2f75-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2f75-243">Search-Flags</span></span>           | <span data-ttu-id="c2f75-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2f75-244">0x00000000</span></span>                                                          |
| <span data-ttu-id="c2f75-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2f75-245">System-Flags</span></span>           | <span data-ttu-id="c2f75-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2f75-246">0x00000010</span></span>                                                          |
| <span data-ttu-id="c2f75-247">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c2f75-247">Classes used in</span></span>        | [<span data-ttu-id="c2f75-248">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c2f75-248">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c2f75-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c2f75-249">Windows Server 2012</span></span>



| <span data-ttu-id="c2f75-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2f75-250">Entry</span></span> | <span data-ttu-id="c2f75-251">Value</span><span class="sxs-lookup"><span data-stu-id="c2f75-251">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c2f75-252">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c2f75-252">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c2f75-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2f75-253">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c2f75-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2f75-254">System-Only</span></span>            | <span data-ttu-id="c2f75-255">False</span><span class="sxs-lookup"><span data-stu-id="c2f75-255">False</span></span>                                                               |
| <span data-ttu-id="c2f75-256">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c2f75-256">Is-Single-Valued</span></span>       | <span data-ttu-id="c2f75-257">True</span><span class="sxs-lookup"><span data-stu-id="c2f75-257">True</span></span>                                                                |
| <span data-ttu-id="c2f75-258">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c2f75-258">Is Indexed</span></span>             | <span data-ttu-id="c2f75-259">False</span><span class="sxs-lookup"><span data-stu-id="c2f75-259">False</span></span>                                                               |
| <span data-ttu-id="c2f75-260">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c2f75-260">In Global Catalog</span></span>      | <span data-ttu-id="c2f75-261">False</span><span class="sxs-lookup"><span data-stu-id="c2f75-261">False</span></span>                                                               |
| <span data-ttu-id="c2f75-262">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c2f75-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2f75-263">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c2f75-263">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="c2f75-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2f75-264">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="c2f75-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2f75-265">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="c2f75-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2f75-266">Search-Flags</span></span>           | <span data-ttu-id="c2f75-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2f75-267">0x00000000</span></span>                                                          |
| <span data-ttu-id="c2f75-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2f75-268">System-Flags</span></span>           | <span data-ttu-id="c2f75-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2f75-269">0x00000010</span></span>                                                          |
| <span data-ttu-id="c2f75-270">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c2f75-270">Classes used in</span></span>        | [<span data-ttu-id="c2f75-271">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c2f75-271">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





