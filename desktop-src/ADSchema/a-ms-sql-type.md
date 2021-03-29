---
title: Atributo de tipo MS-SQL
description: El tipo de replicación utilizado por este servidor SQL Server.
ms.assetid: 8e7fa9ab-9a25-4ee3-9134-68af698a5fb8
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de tipo MS-SQL
- Esquema de AD de atributo de tipo mS-SQL
topic_type:
- apiref
api_name:
- MS-SQL-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057b85b0c522a891cc31cde699fd062897c54818
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906230"
---
# <a name="ms-sql-type-attribute"></a><span data-ttu-id="c8d32-105">Atributo de tipo MS-SQL</span><span class="sxs-lookup"><span data-stu-id="c8d32-105">MS-SQL-Type attribute</span></span>

<span data-ttu-id="c8d32-106">El tipo de replicación utilizado por este servidor SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c8d32-106">The replication type used by this SQL server.</span></span> <span data-ttu-id="c8d32-107">Los valores siguientes son los valores posibles para este atributo.</span><span class="sxs-lookup"><span data-stu-id="c8d32-107">The following values are the possible values for this attribute.</span></span>



| <span data-ttu-id="c8d32-108">Value</span><span class="sxs-lookup"><span data-stu-id="c8d32-108">Value</span></span>        | <span data-ttu-id="c8d32-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8d32-109">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="c8d32-110">0</span><span class="sxs-lookup"><span data-stu-id="c8d32-110">0</span></span><br/> | <span data-ttu-id="c8d32-111">Replicación transaccional.</span><span class="sxs-lookup"><span data-stu-id="c8d32-111">Transactional replication.</span></span><br/> |
| <span data-ttu-id="c8d32-112">1</span><span class="sxs-lookup"><span data-stu-id="c8d32-112">1</span></span><br/> | <span data-ttu-id="c8d32-113">Replicación de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="c8d32-113">Snapshot replication.</span></span><br/>      |
| <span data-ttu-id="c8d32-114">2</span><span class="sxs-lookup"><span data-stu-id="c8d32-114">2</span></span><br/> | <span data-ttu-id="c8d32-115">Replicación de mezcla.</span><span class="sxs-lookup"><span data-stu-id="c8d32-115">Merge replication.</span></span><br/>         |



 



| <span data-ttu-id="c8d32-116">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8d32-116">Entry</span></span> | <span data-ttu-id="c8d32-117">Value</span><span class="sxs-lookup"><span data-stu-id="c8d32-117">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c8d32-118">CN</span><span class="sxs-lookup"><span data-stu-id="c8d32-118">CN</span></span>                | <span data-ttu-id="c8d32-119">Tipo MS-SQL</span><span class="sxs-lookup"><span data-stu-id="c8d32-119">MS-SQL-Type</span></span>                                 |
| <span data-ttu-id="c8d32-120">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="c8d32-120">Ldap-Display-Name</span></span> | <span data-ttu-id="c8d32-121">Tipo mS-SQL</span><span class="sxs-lookup"><span data-stu-id="c8d32-121">mS-SQL-Type</span></span>                                 |
| <span data-ttu-id="c8d32-122">Tamaño</span><span class="sxs-lookup"><span data-stu-id="c8d32-122">Size</span></span>              | \-                                          |
| <span data-ttu-id="c8d32-123">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="c8d32-123">Update Privilege</span></span>  | <span data-ttu-id="c8d32-124">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="c8d32-124">Domain administrator</span></span>                        |
| <span data-ttu-id="c8d32-125">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="c8d32-125">Update Frequency</span></span>  | <span data-ttu-id="c8d32-126">Cuando la replicación está configurada.</span><span class="sxs-lookup"><span data-stu-id="c8d32-126">When replication is set up.</span></span>                 |
| <span data-ttu-id="c8d32-127">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c8d32-127">Attribute-Id</span></span>      | <span data-ttu-id="c8d32-128">1.2.840.113556.1.4.1391</span><span class="sxs-lookup"><span data-stu-id="c8d32-128">1.2.840.113556.1.4.1391</span></span>                     |
| <span data-ttu-id="c8d32-129">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c8d32-129">System-Id-Guid</span></span>    | <span data-ttu-id="c8d32-130">ca48eba8-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="c8d32-130">ca48eba8-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="c8d32-131">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8d32-131">Syntax</span></span>            | [<span data-ttu-id="c8d32-132">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c8d32-132">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c8d32-133">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="c8d32-133">Implementations</span></span>

-   [<span data-ttu-id="c8d32-134">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c8d32-134">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c8d32-135">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c8d32-135">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c8d32-136">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c8d32-136">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c8d32-137">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c8d32-137">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c8d32-138">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c8d32-138">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c8d32-139">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c8d32-139">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c8d32-140">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c8d32-140">Windows 2000 Server</span></span>



| <span data-ttu-id="c8d32-141">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8d32-141">Entry</span></span> | <span data-ttu-id="c8d32-142">Value</span><span class="sxs-lookup"><span data-stu-id="c8d32-142">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8d32-143">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c8d32-143">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-144">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8d32-144">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-145">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8d32-145">System-Only</span></span>            | <span data-ttu-id="c8d32-146">False</span><span class="sxs-lookup"><span data-stu-id="c8d32-146">False</span></span>                                                                                                                               |
| <span data-ttu-id="c8d32-147">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c8d32-147">Is-Single-Valued</span></span>       | <span data-ttu-id="c8d32-148">True</span><span class="sxs-lookup"><span data-stu-id="c8d32-148">True</span></span>                                                                                                                                |
| <span data-ttu-id="c8d32-149">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c8d32-149">Is Indexed</span></span>             | <span data-ttu-id="c8d32-150">False</span><span class="sxs-lookup"><span data-stu-id="c8d32-150">False</span></span>                                                                                                                               |
| <span data-ttu-id="c8d32-151">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c8d32-151">In Global Catalog</span></span>      | <span data-ttu-id="c8d32-152">False</span><span class="sxs-lookup"><span data-stu-id="c8d32-152">False</span></span>                                                                                                                               |
| <span data-ttu-id="c8d32-153">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c8d32-153">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8d32-154">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c8d32-154">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="c8d32-155">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8d32-155">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-156">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8d32-156">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-157">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8d32-157">Search-Flags</span></span>           | <span data-ttu-id="c8d32-158">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8d32-158">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="c8d32-159">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8d32-159">System-Flags</span></span>           | <span data-ttu-id="c8d32-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8d32-160">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="c8d32-161">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c8d32-161">Classes used in</span></span>        | [<span data-ttu-id="c8d32-162">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c8d32-162">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="c8d32-163">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="c8d32-163">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c8d32-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c8d32-164">Windows Server 2003</span></span>



| <span data-ttu-id="c8d32-165">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8d32-165">Entry</span></span> | <span data-ttu-id="c8d32-166">Value</span><span class="sxs-lookup"><span data-stu-id="c8d32-166">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8d32-167">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c8d32-167">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8d32-168">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-169">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8d32-169">System-Only</span></span>            | <span data-ttu-id="c8d32-170">False</span><span class="sxs-lookup"><span data-stu-id="c8d32-170">False</span></span>                                                                                                                               |
| <span data-ttu-id="c8d32-171">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c8d32-171">Is-Single-Valued</span></span>       | <span data-ttu-id="c8d32-172">True</span><span class="sxs-lookup"><span data-stu-id="c8d32-172">True</span></span>                                                                                                                                |
| <span data-ttu-id="c8d32-173">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c8d32-173">Is Indexed</span></span>             | <span data-ttu-id="c8d32-174">False</span><span class="sxs-lookup"><span data-stu-id="c8d32-174">False</span></span>                                                                                                                               |
| <span data-ttu-id="c8d32-175">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c8d32-175">In Global Catalog</span></span>      | <span data-ttu-id="c8d32-176">False</span><span class="sxs-lookup"><span data-stu-id="c8d32-176">False</span></span>                                                                                                                               |
| <span data-ttu-id="c8d32-177">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c8d32-177">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8d32-178">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c8d32-178">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="c8d32-179">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8d32-179">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8d32-180">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8d32-181">Search-Flags</span></span>           | <span data-ttu-id="c8d32-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8d32-182">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="c8d32-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8d32-183">System-Flags</span></span>           | <span data-ttu-id="c8d32-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8d32-184">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="c8d32-185">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c8d32-185">Classes used in</span></span>        | [<span data-ttu-id="c8d32-186">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c8d32-186">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="c8d32-187">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="c8d32-187">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c8d32-188">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c8d32-188">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c8d32-189">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8d32-189">Entry</span></span> | <span data-ttu-id="c8d32-190">Value</span><span class="sxs-lookup"><span data-stu-id="c8d32-190">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8d32-191">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c8d32-191">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8d32-192">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8d32-193">System-Only</span></span>            | <span data-ttu-id="c8d32-194">False</span><span class="sxs-lookup"><span data-stu-id="c8d32-194">False</span></span>                                                                                                                               |
| <span data-ttu-id="c8d32-195">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c8d32-195">Is-Single-Valued</span></span>       | <span data-ttu-id="c8d32-196">True</span><span class="sxs-lookup"><span data-stu-id="c8d32-196">True</span></span>                                                                                                                                |
| <span data-ttu-id="c8d32-197">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c8d32-197">Is Indexed</span></span>             | <span data-ttu-id="c8d32-198">False</span><span class="sxs-lookup"><span data-stu-id="c8d32-198">False</span></span>                                                                                                                               |
| <span data-ttu-id="c8d32-199">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c8d32-199">In Global Catalog</span></span>      | <span data-ttu-id="c8d32-200">False</span><span class="sxs-lookup"><span data-stu-id="c8d32-200">False</span></span>                                                                                                                               |
| <span data-ttu-id="c8d32-201">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c8d32-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8d32-202">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c8d32-202">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="c8d32-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8d32-203">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8d32-204">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8d32-205">Search-Flags</span></span>           | <span data-ttu-id="c8d32-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8d32-206">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="c8d32-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8d32-207">System-Flags</span></span>           | <span data-ttu-id="c8d32-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8d32-208">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="c8d32-209">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c8d32-209">Classes used in</span></span>        | [<span data-ttu-id="c8d32-210">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c8d32-210">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="c8d32-211">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="c8d32-211">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c8d32-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8d32-212">Windows Server 2008</span></span>



| <span data-ttu-id="c8d32-213">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8d32-213">Entry</span></span> | <span data-ttu-id="c8d32-214">Value</span><span class="sxs-lookup"><span data-stu-id="c8d32-214">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8d32-215">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c8d32-215">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8d32-216">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8d32-217">System-Only</span></span>            | <span data-ttu-id="c8d32-218">False</span><span class="sxs-lookup"><span data-stu-id="c8d32-218">False</span></span>                                                                                                                               |
| <span data-ttu-id="c8d32-219">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c8d32-219">Is-Single-Valued</span></span>       | <span data-ttu-id="c8d32-220">True</span><span class="sxs-lookup"><span data-stu-id="c8d32-220">True</span></span>                                                                                                                                |
| <span data-ttu-id="c8d32-221">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c8d32-221">Is Indexed</span></span>             | <span data-ttu-id="c8d32-222">False</span><span class="sxs-lookup"><span data-stu-id="c8d32-222">False</span></span>                                                                                                                               |
| <span data-ttu-id="c8d32-223">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c8d32-223">In Global Catalog</span></span>      | <span data-ttu-id="c8d32-224">False</span><span class="sxs-lookup"><span data-stu-id="c8d32-224">False</span></span>                                                                                                                               |
| <span data-ttu-id="c8d32-225">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c8d32-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8d32-226">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c8d32-226">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="c8d32-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8d32-227">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8d32-228">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8d32-229">Search-Flags</span></span>           | <span data-ttu-id="c8d32-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8d32-230">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="c8d32-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8d32-231">System-Flags</span></span>           | <span data-ttu-id="c8d32-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8d32-232">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="c8d32-233">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c8d32-233">Classes used in</span></span>        | [<span data-ttu-id="c8d32-234">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c8d32-234">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="c8d32-235">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="c8d32-235">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c8d32-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c8d32-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c8d32-237">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8d32-237">Entry</span></span> | <span data-ttu-id="c8d32-238">Value</span><span class="sxs-lookup"><span data-stu-id="c8d32-238">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8d32-239">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c8d32-239">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8d32-240">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8d32-241">System-Only</span></span>            | <span data-ttu-id="c8d32-242">False</span><span class="sxs-lookup"><span data-stu-id="c8d32-242">False</span></span>                                                                                                                               |
| <span data-ttu-id="c8d32-243">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c8d32-243">Is-Single-Valued</span></span>       | <span data-ttu-id="c8d32-244">True</span><span class="sxs-lookup"><span data-stu-id="c8d32-244">True</span></span>                                                                                                                                |
| <span data-ttu-id="c8d32-245">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c8d32-245">Is Indexed</span></span>             | <span data-ttu-id="c8d32-246">False</span><span class="sxs-lookup"><span data-stu-id="c8d32-246">False</span></span>                                                                                                                               |
| <span data-ttu-id="c8d32-247">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c8d32-247">In Global Catalog</span></span>      | <span data-ttu-id="c8d32-248">False</span><span class="sxs-lookup"><span data-stu-id="c8d32-248">False</span></span>                                                                                                                               |
| <span data-ttu-id="c8d32-249">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c8d32-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8d32-250">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c8d32-250">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="c8d32-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8d32-251">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8d32-252">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8d32-253">Search-Flags</span></span>           | <span data-ttu-id="c8d32-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8d32-254">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="c8d32-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8d32-255">System-Flags</span></span>           | <span data-ttu-id="c8d32-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8d32-256">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="c8d32-257">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c8d32-257">Classes used in</span></span>        | [<span data-ttu-id="c8d32-258">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c8d32-258">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="c8d32-259">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="c8d32-259">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c8d32-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c8d32-260">Windows Server 2012</span></span>



| <span data-ttu-id="c8d32-261">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8d32-261">Entry</span></span> | <span data-ttu-id="c8d32-262">Value</span><span class="sxs-lookup"><span data-stu-id="c8d32-262">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8d32-263">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c8d32-263">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8d32-264">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8d32-265">System-Only</span></span>            | <span data-ttu-id="c8d32-266">False</span><span class="sxs-lookup"><span data-stu-id="c8d32-266">False</span></span>                                                                                                                               |
| <span data-ttu-id="c8d32-267">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c8d32-267">Is-Single-Valued</span></span>       | <span data-ttu-id="c8d32-268">True</span><span class="sxs-lookup"><span data-stu-id="c8d32-268">True</span></span>                                                                                                                                |
| <span data-ttu-id="c8d32-269">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c8d32-269">Is Indexed</span></span>             | <span data-ttu-id="c8d32-270">False</span><span class="sxs-lookup"><span data-stu-id="c8d32-270">False</span></span>                                                                                                                               |
| <span data-ttu-id="c8d32-271">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c8d32-271">In Global Catalog</span></span>      | <span data-ttu-id="c8d32-272">False</span><span class="sxs-lookup"><span data-stu-id="c8d32-272">False</span></span>                                                                                                                               |
| <span data-ttu-id="c8d32-273">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c8d32-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8d32-274">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c8d32-274">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="c8d32-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8d32-275">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8d32-276">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="c8d32-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8d32-277">Search-Flags</span></span>           | <span data-ttu-id="c8d32-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8d32-278">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="c8d32-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8d32-279">System-Flags</span></span>           | <span data-ttu-id="c8d32-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8d32-280">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="c8d32-281">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c8d32-281">Classes used in</span></span>        | [<span data-ttu-id="c8d32-282">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c8d32-282">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="c8d32-283">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="c8d32-283">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



 

 





