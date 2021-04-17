---
title: Atributo MS-SQL-InformationDirectory
description: Directorio informativo de la instancia actual de SQL Server.
ms.assetid: fec29b94-b136-4862-8615-7190b3b45ec3
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de MS-SQL-InformationDirectory
- Esquema de AD de atributos de mS-SQL-InformationDirectory
topic_type:
- apiref
api_name:
- MS-SQL-InformationDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a5ca19d6c746e6e5874e82010fcbca367c1157
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659181"
---
# <a name="ms-sql-informationdirectory-attribute"></a><span data-ttu-id="76b71-105">Atributo MS-SQL-InformationDirectory</span><span class="sxs-lookup"><span data-stu-id="76b71-105">MS-SQL-InformationDirectory attribute</span></span>

<span data-ttu-id="76b71-106">Directorio informativo de la instancia actual de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="76b71-106">The informational directory for the current instance of SQL Server.</span></span>



| <span data-ttu-id="76b71-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="76b71-107">Entry</span></span> | <span data-ttu-id="76b71-108">Value</span><span class="sxs-lookup"><span data-stu-id="76b71-108">Value</span></span> |
|-------------------|------------------------------------------|
| <span data-ttu-id="76b71-109">CN</span><span class="sxs-lookup"><span data-stu-id="76b71-109">CN</span></span>                | <span data-ttu-id="76b71-110">MS-SQL-InformationDirectory</span><span class="sxs-lookup"><span data-stu-id="76b71-110">MS-SQL-InformationDirectory</span></span>              |
| <span data-ttu-id="76b71-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="76b71-111">Ldap-Display-Name</span></span> | <span data-ttu-id="76b71-112">mS-SQL-InformationDirectory</span><span class="sxs-lookup"><span data-stu-id="76b71-112">mS-SQL-InformationDirectory</span></span>              |
| <span data-ttu-id="76b71-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="76b71-113">Size</span></span>              | \-                                       |
| <span data-ttu-id="76b71-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="76b71-114">Update Privilege</span></span>  | <span data-ttu-id="76b71-115">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="76b71-115">Domain administrator</span></span>                     |
| <span data-ttu-id="76b71-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="76b71-116">Update Frequency</span></span>  | <span data-ttu-id="76b71-117">Al iniciar el sistema o al actualizar AD.</span><span class="sxs-lookup"><span data-stu-id="76b71-117">At system startup or when AD is updated.</span></span> |
| <span data-ttu-id="76b71-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="76b71-118">Attribute-Id</span></span>      | <span data-ttu-id="76b71-119">1.2.840.113556.1.4.1392</span><span class="sxs-lookup"><span data-stu-id="76b71-119">1.2.840.113556.1.4.1392</span></span>                  |
| <span data-ttu-id="76b71-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="76b71-120">System-Id-Guid</span></span>    | <span data-ttu-id="76b71-121">d0aedb2e-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="76b71-121">d0aedb2e-ccee-11d2-9993-0000f87a57d4</span></span>     |
| <span data-ttu-id="76b71-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76b71-122">Syntax</span></span>            | [<span data-ttu-id="76b71-123">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="76b71-123">**Boolean**</span></span>](s-boolean.md)             |



## <a name="implementations"></a><span data-ttu-id="76b71-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="76b71-124">Implementations</span></span>

-   [<span data-ttu-id="76b71-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="76b71-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="76b71-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="76b71-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="76b71-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="76b71-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="76b71-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="76b71-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="76b71-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="76b71-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="76b71-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="76b71-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="76b71-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="76b71-131">Windows 2000 Server</span></span>



| <span data-ttu-id="76b71-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="76b71-132">Entry</span></span> | <span data-ttu-id="76b71-133">Value</span><span class="sxs-lookup"><span data-stu-id="76b71-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="76b71-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="76b71-134">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="76b71-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76b71-135">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="76b71-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="76b71-136">System-Only</span></span>            | <span data-ttu-id="76b71-137">False</span><span class="sxs-lookup"><span data-stu-id="76b71-137">False</span></span>                                                             |
| <span data-ttu-id="76b71-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="76b71-138">Is-Single-Valued</span></span>       | <span data-ttu-id="76b71-139">True</span><span class="sxs-lookup"><span data-stu-id="76b71-139">True</span></span>                                                              |
| <span data-ttu-id="76b71-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="76b71-140">Is Indexed</span></span>             | <span data-ttu-id="76b71-141">False</span><span class="sxs-lookup"><span data-stu-id="76b71-141">False</span></span>                                                             |
| <span data-ttu-id="76b71-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="76b71-142">In Global Catalog</span></span>      | <span data-ttu-id="76b71-143">False</span><span class="sxs-lookup"><span data-stu-id="76b71-143">False</span></span>                                                             |
| <span data-ttu-id="76b71-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="76b71-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="76b71-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="76b71-145">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="76b71-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76b71-146">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="76b71-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76b71-147">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="76b71-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76b71-148">Search-Flags</span></span>           | <span data-ttu-id="76b71-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76b71-149">0x00000000</span></span>                                                        |
| <span data-ttu-id="76b71-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76b71-150">System-Flags</span></span>           | <span data-ttu-id="76b71-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76b71-151">0x00000010</span></span>                                                        |
| <span data-ttu-id="76b71-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="76b71-152">Classes used in</span></span>        | [<span data-ttu-id="76b71-153">**MS-SQL-SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="76b71-153">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="76b71-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="76b71-154">Windows Server 2003</span></span>



| <span data-ttu-id="76b71-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="76b71-155">Entry</span></span> | <span data-ttu-id="76b71-156">Value</span><span class="sxs-lookup"><span data-stu-id="76b71-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="76b71-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="76b71-157">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="76b71-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76b71-158">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="76b71-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="76b71-159">System-Only</span></span>            | <span data-ttu-id="76b71-160">False</span><span class="sxs-lookup"><span data-stu-id="76b71-160">False</span></span>                                                             |
| <span data-ttu-id="76b71-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="76b71-161">Is-Single-Valued</span></span>       | <span data-ttu-id="76b71-162">True</span><span class="sxs-lookup"><span data-stu-id="76b71-162">True</span></span>                                                              |
| <span data-ttu-id="76b71-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="76b71-163">Is Indexed</span></span>             | <span data-ttu-id="76b71-164">False</span><span class="sxs-lookup"><span data-stu-id="76b71-164">False</span></span>                                                             |
| <span data-ttu-id="76b71-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="76b71-165">In Global Catalog</span></span>      | <span data-ttu-id="76b71-166">False</span><span class="sxs-lookup"><span data-stu-id="76b71-166">False</span></span>                                                             |
| <span data-ttu-id="76b71-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="76b71-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="76b71-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="76b71-168">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="76b71-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76b71-169">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="76b71-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76b71-170">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="76b71-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76b71-171">Search-Flags</span></span>           | <span data-ttu-id="76b71-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76b71-172">0x00000000</span></span>                                                        |
| <span data-ttu-id="76b71-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76b71-173">System-Flags</span></span>           | <span data-ttu-id="76b71-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76b71-174">0x00000010</span></span>                                                        |
| <span data-ttu-id="76b71-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="76b71-175">Classes used in</span></span>        | [<span data-ttu-id="76b71-176">**MS-SQL-SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="76b71-176">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="76b71-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="76b71-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="76b71-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="76b71-178">Entry</span></span> | <span data-ttu-id="76b71-179">Value</span><span class="sxs-lookup"><span data-stu-id="76b71-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="76b71-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="76b71-180">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="76b71-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76b71-181">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="76b71-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="76b71-182">System-Only</span></span>            | <span data-ttu-id="76b71-183">False</span><span class="sxs-lookup"><span data-stu-id="76b71-183">False</span></span>                                                             |
| <span data-ttu-id="76b71-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="76b71-184">Is-Single-Valued</span></span>       | <span data-ttu-id="76b71-185">True</span><span class="sxs-lookup"><span data-stu-id="76b71-185">True</span></span>                                                              |
| <span data-ttu-id="76b71-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="76b71-186">Is Indexed</span></span>             | <span data-ttu-id="76b71-187">False</span><span class="sxs-lookup"><span data-stu-id="76b71-187">False</span></span>                                                             |
| <span data-ttu-id="76b71-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="76b71-188">In Global Catalog</span></span>      | <span data-ttu-id="76b71-189">False</span><span class="sxs-lookup"><span data-stu-id="76b71-189">False</span></span>                                                             |
| <span data-ttu-id="76b71-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="76b71-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="76b71-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="76b71-191">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="76b71-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76b71-192">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="76b71-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76b71-193">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="76b71-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76b71-194">Search-Flags</span></span>           | <span data-ttu-id="76b71-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76b71-195">0x00000000</span></span>                                                        |
| <span data-ttu-id="76b71-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76b71-196">System-Flags</span></span>           | <span data-ttu-id="76b71-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76b71-197">0x00000010</span></span>                                                        |
| <span data-ttu-id="76b71-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="76b71-198">Classes used in</span></span>        | [<span data-ttu-id="76b71-199">**MS-SQL-SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="76b71-199">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="76b71-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76b71-200">Windows Server 2008</span></span>



| <span data-ttu-id="76b71-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="76b71-201">Entry</span></span> | <span data-ttu-id="76b71-202">Value</span><span class="sxs-lookup"><span data-stu-id="76b71-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="76b71-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="76b71-203">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="76b71-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76b71-204">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="76b71-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="76b71-205">System-Only</span></span>            | <span data-ttu-id="76b71-206">False</span><span class="sxs-lookup"><span data-stu-id="76b71-206">False</span></span>                                                             |
| <span data-ttu-id="76b71-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="76b71-207">Is-Single-Valued</span></span>       | <span data-ttu-id="76b71-208">True</span><span class="sxs-lookup"><span data-stu-id="76b71-208">True</span></span>                                                              |
| <span data-ttu-id="76b71-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="76b71-209">Is Indexed</span></span>             | <span data-ttu-id="76b71-210">False</span><span class="sxs-lookup"><span data-stu-id="76b71-210">False</span></span>                                                             |
| <span data-ttu-id="76b71-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="76b71-211">In Global Catalog</span></span>      | <span data-ttu-id="76b71-212">False</span><span class="sxs-lookup"><span data-stu-id="76b71-212">False</span></span>                                                             |
| <span data-ttu-id="76b71-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="76b71-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="76b71-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="76b71-214">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="76b71-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76b71-215">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="76b71-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76b71-216">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="76b71-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76b71-217">Search-Flags</span></span>           | <span data-ttu-id="76b71-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76b71-218">0x00000000</span></span>                                                        |
| <span data-ttu-id="76b71-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76b71-219">System-Flags</span></span>           | <span data-ttu-id="76b71-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76b71-220">0x00000010</span></span>                                                        |
| <span data-ttu-id="76b71-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="76b71-221">Classes used in</span></span>        | [<span data-ttu-id="76b71-222">**MS-SQL-SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="76b71-222">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="76b71-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="76b71-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="76b71-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="76b71-224">Entry</span></span> | <span data-ttu-id="76b71-225">Value</span><span class="sxs-lookup"><span data-stu-id="76b71-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="76b71-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="76b71-226">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="76b71-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76b71-227">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="76b71-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="76b71-228">System-Only</span></span>            | <span data-ttu-id="76b71-229">False</span><span class="sxs-lookup"><span data-stu-id="76b71-229">False</span></span>                                                             |
| <span data-ttu-id="76b71-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="76b71-230">Is-Single-Valued</span></span>       | <span data-ttu-id="76b71-231">True</span><span class="sxs-lookup"><span data-stu-id="76b71-231">True</span></span>                                                              |
| <span data-ttu-id="76b71-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="76b71-232">Is Indexed</span></span>             | <span data-ttu-id="76b71-233">False</span><span class="sxs-lookup"><span data-stu-id="76b71-233">False</span></span>                                                             |
| <span data-ttu-id="76b71-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="76b71-234">In Global Catalog</span></span>      | <span data-ttu-id="76b71-235">False</span><span class="sxs-lookup"><span data-stu-id="76b71-235">False</span></span>                                                             |
| <span data-ttu-id="76b71-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="76b71-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="76b71-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="76b71-237">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="76b71-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76b71-238">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="76b71-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76b71-239">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="76b71-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76b71-240">Search-Flags</span></span>           | <span data-ttu-id="76b71-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76b71-241">0x00000000</span></span>                                                        |
| <span data-ttu-id="76b71-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76b71-242">System-Flags</span></span>           | <span data-ttu-id="76b71-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76b71-243">0x00000010</span></span>                                                        |
| <span data-ttu-id="76b71-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="76b71-244">Classes used in</span></span>        | [<span data-ttu-id="76b71-245">**MS-SQL-SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="76b71-245">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="76b71-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="76b71-246">Windows Server 2012</span></span>



| <span data-ttu-id="76b71-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="76b71-247">Entry</span></span> | <span data-ttu-id="76b71-248">Value</span><span class="sxs-lookup"><span data-stu-id="76b71-248">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="76b71-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="76b71-249">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="76b71-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76b71-250">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="76b71-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="76b71-251">System-Only</span></span>            | <span data-ttu-id="76b71-252">False</span><span class="sxs-lookup"><span data-stu-id="76b71-252">False</span></span>                                                             |
| <span data-ttu-id="76b71-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="76b71-253">Is-Single-Valued</span></span>       | <span data-ttu-id="76b71-254">True</span><span class="sxs-lookup"><span data-stu-id="76b71-254">True</span></span>                                                              |
| <span data-ttu-id="76b71-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="76b71-255">Is Indexed</span></span>             | <span data-ttu-id="76b71-256">False</span><span class="sxs-lookup"><span data-stu-id="76b71-256">False</span></span>                                                             |
| <span data-ttu-id="76b71-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="76b71-257">In Global Catalog</span></span>      | <span data-ttu-id="76b71-258">False</span><span class="sxs-lookup"><span data-stu-id="76b71-258">False</span></span>                                                             |
| <span data-ttu-id="76b71-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="76b71-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="76b71-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="76b71-260">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="76b71-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76b71-261">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="76b71-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76b71-262">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="76b71-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76b71-263">Search-Flags</span></span>           | <span data-ttu-id="76b71-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76b71-264">0x00000000</span></span>                                                        |
| <span data-ttu-id="76b71-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76b71-265">System-Flags</span></span>           | <span data-ttu-id="76b71-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76b71-266">0x00000010</span></span>                                                        |
| <span data-ttu-id="76b71-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="76b71-267">Classes used in</span></span>        | [<span data-ttu-id="76b71-268">**MS-SQL-SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="76b71-268">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



 

 





