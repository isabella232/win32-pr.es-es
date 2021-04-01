---
title: Atributo MS-SQL-Database
description: Nombre de la base de datos de SQL Server implicada en la replicación.
ms.assetid: 624705d9-df3f-458e-98f4-fb8da073efd6
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de base de datos de MS-SQL
- Esquema de AD de atributos de base de datos de mS-SQL
topic_type:
- apiref
api_name:
- MS-SQL-Database
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae6c448213bee18fede3cc8a77cabf607c3b2ee3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905809"
---
# <a name="ms-sql-database-attribute"></a><span data-ttu-id="88c9e-105">Atributo MS-SQL-Database</span><span class="sxs-lookup"><span data-stu-id="88c9e-105">MS-SQL-Database attribute</span></span>

<span data-ttu-id="88c9e-106">Nombre de la base de datos de SQL Server implicada en la replicación.</span><span class="sxs-lookup"><span data-stu-id="88c9e-106">The name of the SQL Server database involved in replication.</span></span>



| <span data-ttu-id="88c9e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="88c9e-107">Entry</span></span> | <span data-ttu-id="88c9e-108">Value</span><span class="sxs-lookup"><span data-stu-id="88c9e-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="88c9e-109">CN</span><span class="sxs-lookup"><span data-stu-id="88c9e-109">CN</span></span>                | <span data-ttu-id="88c9e-110">MS-SQL-base de datos</span><span class="sxs-lookup"><span data-stu-id="88c9e-110">MS-SQL-Database</span></span>                             |
| <span data-ttu-id="88c9e-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="88c9e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="88c9e-112">mS-SQL-base de datos</span><span class="sxs-lookup"><span data-stu-id="88c9e-112">mS-SQL-Database</span></span>                             |
| <span data-ttu-id="88c9e-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="88c9e-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="88c9e-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="88c9e-114">Update Privilege</span></span>  | <span data-ttu-id="88c9e-115">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="88c9e-115">Domain administrator</span></span>                        |
| <span data-ttu-id="88c9e-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="88c9e-116">Update Frequency</span></span>  | <span data-ttu-id="88c9e-117">Cuando se configura la replicación.</span><span class="sxs-lookup"><span data-stu-id="88c9e-117">When replication is setup.</span></span>                  |
| <span data-ttu-id="88c9e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="88c9e-118">Attribute-Id</span></span>      | <span data-ttu-id="88c9e-119">1.2.840.113556.1.4.1393</span><span class="sxs-lookup"><span data-stu-id="88c9e-119">1.2.840.113556.1.4.1393</span></span>                     |
| <span data-ttu-id="88c9e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="88c9e-120">System-Id-Guid</span></span>    | <span data-ttu-id="88c9e-121">d5a0dbdc-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="88c9e-121">d5a0dbdc-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="88c9e-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88c9e-122">Syntax</span></span>            | [<span data-ttu-id="88c9e-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="88c9e-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="88c9e-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="88c9e-124">Implementations</span></span>

-   [<span data-ttu-id="88c9e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="88c9e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="88c9e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="88c9e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="88c9e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="88c9e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="88c9e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="88c9e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="88c9e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="88c9e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="88c9e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="88c9e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="88c9e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="88c9e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="88c9e-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="88c9e-132">Entry</span></span> | <span data-ttu-id="88c9e-133">Value</span><span class="sxs-lookup"><span data-stu-id="88c9e-133">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="88c9e-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="88c9e-134">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88c9e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c9e-135">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88c9e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c9e-136">System-Only</span></span>            | <span data-ttu-id="88c9e-137">False</span><span class="sxs-lookup"><span data-stu-id="88c9e-137">False</span></span>                                                               |
| <span data-ttu-id="88c9e-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="88c9e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="88c9e-139">True</span><span class="sxs-lookup"><span data-stu-id="88c9e-139">True</span></span>                                                                |
| <span data-ttu-id="88c9e-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="88c9e-140">Is Indexed</span></span>             | <span data-ttu-id="88c9e-141">True</span><span class="sxs-lookup"><span data-stu-id="88c9e-141">True</span></span>                                                                |
| <span data-ttu-id="88c9e-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="88c9e-142">In Global Catalog</span></span>      | <span data-ttu-id="88c9e-143">True</span><span class="sxs-lookup"><span data-stu-id="88c9e-143">True</span></span>                                                                |
| <span data-ttu-id="88c9e-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="88c9e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c9e-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="88c9e-145">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="88c9e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c9e-146">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="88c9e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c9e-147">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="88c9e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c9e-148">Search-Flags</span></span>           | <span data-ttu-id="88c9e-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="88c9e-149">0x00000001</span></span>                                                          |
| <span data-ttu-id="88c9e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c9e-150">System-Flags</span></span>           | <span data-ttu-id="88c9e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88c9e-151">0x00000010</span></span>                                                          |
| <span data-ttu-id="88c9e-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="88c9e-152">Classes used in</span></span>        | [<span data-ttu-id="88c9e-153">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="88c9e-153">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="88c9e-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="88c9e-154">Windows Server 2003</span></span>



| <span data-ttu-id="88c9e-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="88c9e-155">Entry</span></span> | <span data-ttu-id="88c9e-156">Value</span><span class="sxs-lookup"><span data-stu-id="88c9e-156">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="88c9e-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="88c9e-157">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88c9e-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c9e-158">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88c9e-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c9e-159">System-Only</span></span>            | <span data-ttu-id="88c9e-160">False</span><span class="sxs-lookup"><span data-stu-id="88c9e-160">False</span></span>                                                               |
| <span data-ttu-id="88c9e-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="88c9e-161">Is-Single-Valued</span></span>       | <span data-ttu-id="88c9e-162">True</span><span class="sxs-lookup"><span data-stu-id="88c9e-162">True</span></span>                                                                |
| <span data-ttu-id="88c9e-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="88c9e-163">Is Indexed</span></span>             | <span data-ttu-id="88c9e-164">True</span><span class="sxs-lookup"><span data-stu-id="88c9e-164">True</span></span>                                                                |
| <span data-ttu-id="88c9e-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="88c9e-165">In Global Catalog</span></span>      | <span data-ttu-id="88c9e-166">True</span><span class="sxs-lookup"><span data-stu-id="88c9e-166">True</span></span>                                                                |
| <span data-ttu-id="88c9e-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="88c9e-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c9e-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="88c9e-168">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="88c9e-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c9e-169">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="88c9e-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c9e-170">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="88c9e-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c9e-171">Search-Flags</span></span>           | <span data-ttu-id="88c9e-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="88c9e-172">0x00000001</span></span>                                                          |
| <span data-ttu-id="88c9e-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c9e-173">System-Flags</span></span>           | <span data-ttu-id="88c9e-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88c9e-174">0x00000010</span></span>                                                          |
| <span data-ttu-id="88c9e-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="88c9e-175">Classes used in</span></span>        | [<span data-ttu-id="88c9e-176">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="88c9e-176">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="88c9e-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="88c9e-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="88c9e-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="88c9e-178">Entry</span></span> | <span data-ttu-id="88c9e-179">Value</span><span class="sxs-lookup"><span data-stu-id="88c9e-179">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="88c9e-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="88c9e-180">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88c9e-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c9e-181">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88c9e-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c9e-182">System-Only</span></span>            | <span data-ttu-id="88c9e-183">False</span><span class="sxs-lookup"><span data-stu-id="88c9e-183">False</span></span>                                                               |
| <span data-ttu-id="88c9e-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="88c9e-184">Is-Single-Valued</span></span>       | <span data-ttu-id="88c9e-185">True</span><span class="sxs-lookup"><span data-stu-id="88c9e-185">True</span></span>                                                                |
| <span data-ttu-id="88c9e-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="88c9e-186">Is Indexed</span></span>             | <span data-ttu-id="88c9e-187">True</span><span class="sxs-lookup"><span data-stu-id="88c9e-187">True</span></span>                                                                |
| <span data-ttu-id="88c9e-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="88c9e-188">In Global Catalog</span></span>      | <span data-ttu-id="88c9e-189">True</span><span class="sxs-lookup"><span data-stu-id="88c9e-189">True</span></span>                                                                |
| <span data-ttu-id="88c9e-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="88c9e-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c9e-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="88c9e-191">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="88c9e-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c9e-192">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="88c9e-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c9e-193">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="88c9e-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c9e-194">Search-Flags</span></span>           | <span data-ttu-id="88c9e-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="88c9e-195">0x00000001</span></span>                                                          |
| <span data-ttu-id="88c9e-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c9e-196">System-Flags</span></span>           | <span data-ttu-id="88c9e-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88c9e-197">0x00000010</span></span>                                                          |
| <span data-ttu-id="88c9e-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="88c9e-198">Classes used in</span></span>        | [<span data-ttu-id="88c9e-199">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="88c9e-199">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="88c9e-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88c9e-200">Windows Server 2008</span></span>



| <span data-ttu-id="88c9e-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="88c9e-201">Entry</span></span> | <span data-ttu-id="88c9e-202">Value</span><span class="sxs-lookup"><span data-stu-id="88c9e-202">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="88c9e-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="88c9e-203">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88c9e-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c9e-204">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88c9e-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c9e-205">System-Only</span></span>            | <span data-ttu-id="88c9e-206">False</span><span class="sxs-lookup"><span data-stu-id="88c9e-206">False</span></span>                                                               |
| <span data-ttu-id="88c9e-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="88c9e-207">Is-Single-Valued</span></span>       | <span data-ttu-id="88c9e-208">True</span><span class="sxs-lookup"><span data-stu-id="88c9e-208">True</span></span>                                                                |
| <span data-ttu-id="88c9e-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="88c9e-209">Is Indexed</span></span>             | <span data-ttu-id="88c9e-210">True</span><span class="sxs-lookup"><span data-stu-id="88c9e-210">True</span></span>                                                                |
| <span data-ttu-id="88c9e-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="88c9e-211">In Global Catalog</span></span>      | <span data-ttu-id="88c9e-212">True</span><span class="sxs-lookup"><span data-stu-id="88c9e-212">True</span></span>                                                                |
| <span data-ttu-id="88c9e-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="88c9e-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c9e-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="88c9e-214">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="88c9e-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c9e-215">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="88c9e-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c9e-216">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="88c9e-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c9e-217">Search-Flags</span></span>           | <span data-ttu-id="88c9e-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="88c9e-218">0x00000001</span></span>                                                          |
| <span data-ttu-id="88c9e-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c9e-219">System-Flags</span></span>           | <span data-ttu-id="88c9e-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88c9e-220">0x00000010</span></span>                                                          |
| <span data-ttu-id="88c9e-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="88c9e-221">Classes used in</span></span>        | [<span data-ttu-id="88c9e-222">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="88c9e-222">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="88c9e-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="88c9e-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="88c9e-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="88c9e-224">Entry</span></span> | <span data-ttu-id="88c9e-225">Value</span><span class="sxs-lookup"><span data-stu-id="88c9e-225">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="88c9e-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="88c9e-226">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88c9e-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c9e-227">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88c9e-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c9e-228">System-Only</span></span>            | <span data-ttu-id="88c9e-229">False</span><span class="sxs-lookup"><span data-stu-id="88c9e-229">False</span></span>                                                               |
| <span data-ttu-id="88c9e-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="88c9e-230">Is-Single-Valued</span></span>       | <span data-ttu-id="88c9e-231">True</span><span class="sxs-lookup"><span data-stu-id="88c9e-231">True</span></span>                                                                |
| <span data-ttu-id="88c9e-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="88c9e-232">Is Indexed</span></span>             | <span data-ttu-id="88c9e-233">True</span><span class="sxs-lookup"><span data-stu-id="88c9e-233">True</span></span>                                                                |
| <span data-ttu-id="88c9e-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="88c9e-234">In Global Catalog</span></span>      | <span data-ttu-id="88c9e-235">True</span><span class="sxs-lookup"><span data-stu-id="88c9e-235">True</span></span>                                                                |
| <span data-ttu-id="88c9e-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="88c9e-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c9e-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="88c9e-237">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="88c9e-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c9e-238">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="88c9e-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c9e-239">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="88c9e-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c9e-240">Search-Flags</span></span>           | <span data-ttu-id="88c9e-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="88c9e-241">0x00000001</span></span>                                                          |
| <span data-ttu-id="88c9e-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c9e-242">System-Flags</span></span>           | <span data-ttu-id="88c9e-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88c9e-243">0x00000010</span></span>                                                          |
| <span data-ttu-id="88c9e-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="88c9e-244">Classes used in</span></span>        | [<span data-ttu-id="88c9e-245">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="88c9e-245">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="88c9e-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88c9e-246">Windows Server 2012</span></span>



| <span data-ttu-id="88c9e-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="88c9e-247">Entry</span></span> | <span data-ttu-id="88c9e-248">Value</span><span class="sxs-lookup"><span data-stu-id="88c9e-248">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="88c9e-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="88c9e-249">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88c9e-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c9e-250">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88c9e-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c9e-251">System-Only</span></span>            | <span data-ttu-id="88c9e-252">False</span><span class="sxs-lookup"><span data-stu-id="88c9e-252">False</span></span>                                                               |
| <span data-ttu-id="88c9e-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="88c9e-253">Is-Single-Valued</span></span>       | <span data-ttu-id="88c9e-254">True</span><span class="sxs-lookup"><span data-stu-id="88c9e-254">True</span></span>                                                                |
| <span data-ttu-id="88c9e-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="88c9e-255">Is Indexed</span></span>             | <span data-ttu-id="88c9e-256">True</span><span class="sxs-lookup"><span data-stu-id="88c9e-256">True</span></span>                                                                |
| <span data-ttu-id="88c9e-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="88c9e-257">In Global Catalog</span></span>      | <span data-ttu-id="88c9e-258">True</span><span class="sxs-lookup"><span data-stu-id="88c9e-258">True</span></span>                                                                |
| <span data-ttu-id="88c9e-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="88c9e-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c9e-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="88c9e-260">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="88c9e-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c9e-261">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="88c9e-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c9e-262">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="88c9e-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c9e-263">Search-Flags</span></span>           | <span data-ttu-id="88c9e-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="88c9e-264">0x00000001</span></span>                                                          |
| <span data-ttu-id="88c9e-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c9e-265">System-Flags</span></span>           | <span data-ttu-id="88c9e-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88c9e-266">0x00000010</span></span>                                                          |
| <span data-ttu-id="88c9e-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="88c9e-267">Classes used in</span></span>        | [<span data-ttu-id="88c9e-268">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="88c9e-268">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





