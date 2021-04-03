---
title: Atributo MS-SQL-LastBackupDate
description: Última fecha en la que se realizó la copia de seguridad de la base de datos.
ms.assetid: 09bd6c2a-85fe-46af-8569-5bc3cbc8411d
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de MS-SQL-LastBackupDate
- Esquema de AD de atributos de mS-SQL-LastBackupDate
topic_type:
- apiref
api_name:
- MS-SQL-LastBackupDate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d91cadf953ab51185882c73d4d999a5ccb3fed9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997584"
---
# <a name="ms-sql-lastbackupdate-attribute"></a><span data-ttu-id="cb4d3-105">Atributo MS-SQL-LastBackupDate</span><span class="sxs-lookup"><span data-stu-id="cb4d3-105">MS-SQL-LastBackupDate attribute</span></span>

<span data-ttu-id="cb4d3-106">Última fecha en la que se realizó la copia de seguridad de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="cb4d3-106">The last date that the database was backed up.</span></span>



| <span data-ttu-id="cb4d3-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb4d3-107">Entry</span></span> | <span data-ttu-id="cb4d3-108">Value</span><span class="sxs-lookup"><span data-stu-id="cb4d3-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="cb4d3-109">CN</span><span class="sxs-lookup"><span data-stu-id="cb4d3-109">CN</span></span>                | <span data-ttu-id="cb4d3-110">MS-SQL-LastBackupDate</span><span class="sxs-lookup"><span data-stu-id="cb4d3-110">MS-SQL-LastBackupDate</span></span>                       |
| <span data-ttu-id="cb4d3-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="cb4d3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cb4d3-112">mS-SQL-LastBackupDate</span><span class="sxs-lookup"><span data-stu-id="cb4d3-112">mS-SQL-LastBackupDate</span></span>                       |
| <span data-ttu-id="cb4d3-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="cb4d3-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="cb4d3-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="cb4d3-114">Update Privilege</span></span>  | <span data-ttu-id="cb4d3-115">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="cb4d3-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="cb4d3-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="cb4d3-116">Update Frequency</span></span>  | <span data-ttu-id="cb4d3-117">Cuando se realiza una copia de seguridad de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="cb4d3-117">When the database is backed up.</span></span>             |
| <span data-ttu-id="cb4d3-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cb4d3-118">Attribute-Id</span></span>      | <span data-ttu-id="cb4d3-119">1.2.840.113556.1.4.1398</span><span class="sxs-lookup"><span data-stu-id="cb4d3-119">1.2.840.113556.1.4.1398</span></span>                     |
| <span data-ttu-id="cb4d3-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cb4d3-120">System-Id-Guid</span></span>    | <span data-ttu-id="cb4d3-121">f2b6abca-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="cb4d3-121">f2b6abca-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="cb4d3-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb4d3-122">Syntax</span></span>            | [<span data-ttu-id="cb4d3-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="cb4d3-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="cb4d3-124">Implementations</span></span>

-   [<span data-ttu-id="cb4d3-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cb4d3-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cb4d3-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cb4d3-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cb4d3-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cb4d3-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cb4d3-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cb4d3-131">Windows 2000 Server</span></span>



| <span data-ttu-id="cb4d3-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb4d3-132">Entry</span></span> | <span data-ttu-id="cb4d3-133">Value</span><span class="sxs-lookup"><span data-stu-id="cb4d3-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4d3-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cb4d3-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb4d3-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb4d3-136">System-Only</span></span>            | <span data-ttu-id="cb4d3-137">False</span><span class="sxs-lookup"><span data-stu-id="cb4d3-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="cb4d3-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cb4d3-138">Is-Single-Valued</span></span>       | <span data-ttu-id="cb4d3-139">True</span><span class="sxs-lookup"><span data-stu-id="cb4d3-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="cb4d3-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cb4d3-140">Is Indexed</span></span>             | <span data-ttu-id="cb4d3-141">False</span><span class="sxs-lookup"><span data-stu-id="cb4d3-141">False</span></span>                                                                                                                         |
| <span data-ttu-id="cb4d3-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb4d3-142">In Global Catalog</span></span>      | <span data-ttu-id="cb4d3-143">False</span><span class="sxs-lookup"><span data-stu-id="cb4d3-143">False</span></span>                                                                                                                         |
| <span data-ttu-id="cb4d3-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cb4d3-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb4d3-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cb4d3-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="cb4d3-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb4d3-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb4d3-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb4d3-148">Search-Flags</span></span>           | <span data-ttu-id="cb4d3-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb4d3-149">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="cb4d3-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb4d3-150">System-Flags</span></span>           | <span data-ttu-id="cb4d3-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb4d3-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="cb4d3-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cb4d3-152">Classes used in</span></span>        | [<span data-ttu-id="cb4d3-153">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="cb4d3-154">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-154">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cb4d3-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cb4d3-155">Windows Server 2003</span></span>



| <span data-ttu-id="cb4d3-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb4d3-156">Entry</span></span> | <span data-ttu-id="cb4d3-157">Value</span><span class="sxs-lookup"><span data-stu-id="cb4d3-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4d3-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cb4d3-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb4d3-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb4d3-160">System-Only</span></span>            | <span data-ttu-id="cb4d3-161">False</span><span class="sxs-lookup"><span data-stu-id="cb4d3-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="cb4d3-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cb4d3-162">Is-Single-Valued</span></span>       | <span data-ttu-id="cb4d3-163">True</span><span class="sxs-lookup"><span data-stu-id="cb4d3-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="cb4d3-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cb4d3-164">Is Indexed</span></span>             | <span data-ttu-id="cb4d3-165">False</span><span class="sxs-lookup"><span data-stu-id="cb4d3-165">False</span></span>                                                                                                                         |
| <span data-ttu-id="cb4d3-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb4d3-166">In Global Catalog</span></span>      | <span data-ttu-id="cb4d3-167">False</span><span class="sxs-lookup"><span data-stu-id="cb4d3-167">False</span></span>                                                                                                                         |
| <span data-ttu-id="cb4d3-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cb4d3-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb4d3-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cb4d3-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="cb4d3-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb4d3-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb4d3-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb4d3-172">Search-Flags</span></span>           | <span data-ttu-id="cb4d3-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb4d3-173">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="cb4d3-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb4d3-174">System-Flags</span></span>           | <span data-ttu-id="cb4d3-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb4d3-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="cb4d3-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cb4d3-176">Classes used in</span></span>        | [<span data-ttu-id="cb4d3-177">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-177">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="cb4d3-178">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-178">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cb4d3-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cb4d3-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cb4d3-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb4d3-180">Entry</span></span> | <span data-ttu-id="cb4d3-181">Value</span><span class="sxs-lookup"><span data-stu-id="cb4d3-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4d3-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cb4d3-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb4d3-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb4d3-184">System-Only</span></span>            | <span data-ttu-id="cb4d3-185">False</span><span class="sxs-lookup"><span data-stu-id="cb4d3-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="cb4d3-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cb4d3-186">Is-Single-Valued</span></span>       | <span data-ttu-id="cb4d3-187">True</span><span class="sxs-lookup"><span data-stu-id="cb4d3-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="cb4d3-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cb4d3-188">Is Indexed</span></span>             | <span data-ttu-id="cb4d3-189">False</span><span class="sxs-lookup"><span data-stu-id="cb4d3-189">False</span></span>                                                                                                                         |
| <span data-ttu-id="cb4d3-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb4d3-190">In Global Catalog</span></span>      | <span data-ttu-id="cb4d3-191">False</span><span class="sxs-lookup"><span data-stu-id="cb4d3-191">False</span></span>                                                                                                                         |
| <span data-ttu-id="cb4d3-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cb4d3-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb4d3-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cb4d3-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="cb4d3-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb4d3-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb4d3-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb4d3-196">Search-Flags</span></span>           | <span data-ttu-id="cb4d3-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb4d3-197">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="cb4d3-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb4d3-198">System-Flags</span></span>           | <span data-ttu-id="cb4d3-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb4d3-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="cb4d3-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cb4d3-200">Classes used in</span></span>        | [<span data-ttu-id="cb4d3-201">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-201">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="cb4d3-202">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-202">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cb4d3-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb4d3-203">Windows Server 2008</span></span>



| <span data-ttu-id="cb4d3-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb4d3-204">Entry</span></span> | <span data-ttu-id="cb4d3-205">Value</span><span class="sxs-lookup"><span data-stu-id="cb4d3-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4d3-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cb4d3-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb4d3-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb4d3-208">System-Only</span></span>            | <span data-ttu-id="cb4d3-209">False</span><span class="sxs-lookup"><span data-stu-id="cb4d3-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="cb4d3-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cb4d3-210">Is-Single-Valued</span></span>       | <span data-ttu-id="cb4d3-211">True</span><span class="sxs-lookup"><span data-stu-id="cb4d3-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="cb4d3-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cb4d3-212">Is Indexed</span></span>             | <span data-ttu-id="cb4d3-213">False</span><span class="sxs-lookup"><span data-stu-id="cb4d3-213">False</span></span>                                                                                                                         |
| <span data-ttu-id="cb4d3-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb4d3-214">In Global Catalog</span></span>      | <span data-ttu-id="cb4d3-215">False</span><span class="sxs-lookup"><span data-stu-id="cb4d3-215">False</span></span>                                                                                                                         |
| <span data-ttu-id="cb4d3-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cb4d3-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb4d3-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cb4d3-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="cb4d3-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb4d3-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb4d3-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb4d3-220">Search-Flags</span></span>           | <span data-ttu-id="cb4d3-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb4d3-221">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="cb4d3-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb4d3-222">System-Flags</span></span>           | <span data-ttu-id="cb4d3-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb4d3-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="cb4d3-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cb4d3-224">Classes used in</span></span>        | [<span data-ttu-id="cb4d3-225">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-225">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="cb4d3-226">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-226">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cb4d3-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cb4d3-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cb4d3-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb4d3-228">Entry</span></span> | <span data-ttu-id="cb4d3-229">Value</span><span class="sxs-lookup"><span data-stu-id="cb4d3-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4d3-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cb4d3-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb4d3-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb4d3-232">System-Only</span></span>            | <span data-ttu-id="cb4d3-233">False</span><span class="sxs-lookup"><span data-stu-id="cb4d3-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="cb4d3-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cb4d3-234">Is-Single-Valued</span></span>       | <span data-ttu-id="cb4d3-235">True</span><span class="sxs-lookup"><span data-stu-id="cb4d3-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="cb4d3-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cb4d3-236">Is Indexed</span></span>             | <span data-ttu-id="cb4d3-237">False</span><span class="sxs-lookup"><span data-stu-id="cb4d3-237">False</span></span>                                                                                                                         |
| <span data-ttu-id="cb4d3-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb4d3-238">In Global Catalog</span></span>      | <span data-ttu-id="cb4d3-239">False</span><span class="sxs-lookup"><span data-stu-id="cb4d3-239">False</span></span>                                                                                                                         |
| <span data-ttu-id="cb4d3-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cb4d3-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb4d3-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cb4d3-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="cb4d3-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb4d3-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb4d3-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb4d3-244">Search-Flags</span></span>           | <span data-ttu-id="cb4d3-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb4d3-245">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="cb4d3-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb4d3-246">System-Flags</span></span>           | <span data-ttu-id="cb4d3-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb4d3-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="cb4d3-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cb4d3-248">Classes used in</span></span>        | [<span data-ttu-id="cb4d3-249">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-249">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="cb4d3-250">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-250">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cb4d3-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cb4d3-251">Windows Server 2012</span></span>



| <span data-ttu-id="cb4d3-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb4d3-252">Entry</span></span> | <span data-ttu-id="cb4d3-253">Value</span><span class="sxs-lookup"><span data-stu-id="cb4d3-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4d3-254">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cb4d3-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb4d3-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb4d3-256">System-Only</span></span>            | <span data-ttu-id="cb4d3-257">False</span><span class="sxs-lookup"><span data-stu-id="cb4d3-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="cb4d3-258">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cb4d3-258">Is-Single-Valued</span></span>       | <span data-ttu-id="cb4d3-259">True</span><span class="sxs-lookup"><span data-stu-id="cb4d3-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="cb4d3-260">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cb4d3-260">Is Indexed</span></span>             | <span data-ttu-id="cb4d3-261">False</span><span class="sxs-lookup"><span data-stu-id="cb4d3-261">False</span></span>                                                                                                                         |
| <span data-ttu-id="cb4d3-262">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb4d3-262">In Global Catalog</span></span>      | <span data-ttu-id="cb4d3-263">False</span><span class="sxs-lookup"><span data-stu-id="cb4d3-263">False</span></span>                                                                                                                         |
| <span data-ttu-id="cb4d3-264">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cb4d3-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb4d3-265">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cb4d3-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="cb4d3-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb4d3-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb4d3-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cb4d3-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb4d3-268">Search-Flags</span></span>           | <span data-ttu-id="cb4d3-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb4d3-269">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="cb4d3-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb4d3-270">System-Flags</span></span>           | <span data-ttu-id="cb4d3-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb4d3-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="cb4d3-272">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cb4d3-272">Classes used in</span></span>        | [<span data-ttu-id="cb4d3-273">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-273">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="cb4d3-274">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="cb4d3-274">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



 

 





