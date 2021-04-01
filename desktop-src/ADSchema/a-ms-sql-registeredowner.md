---
title: Atributo MS-SQL-RegisteredOwner
description: Propietario registrado de la instancia actual de SQL Server.
ms.assetid: d07712e8-021d-40db-91ba-0fef7e89bb0f
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de MS-SQL-RegisteredOwner
- Esquema de AD de atributos de mS-SQL-RegisteredOwner
topic_type:
- apiref
api_name:
- MS-SQL-RegisteredOwner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e201494afffdfea59b75bc1901a474469871351
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103805053"
---
# <a name="ms-sql-registeredowner-attribute"></a><span data-ttu-id="ff86a-105">Atributo MS-SQL-RegisteredOwner</span><span class="sxs-lookup"><span data-stu-id="ff86a-105">MS-SQL-RegisteredOwner attribute</span></span>

<span data-ttu-id="ff86a-106">Propietario registrado de la instancia actual de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ff86a-106">The registered owner for the current instance of SQL Server.</span></span>



| <span data-ttu-id="ff86a-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff86a-107">Entry</span></span> | <span data-ttu-id="ff86a-108">Value</span><span class="sxs-lookup"><span data-stu-id="ff86a-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ff86a-109">CN</span><span class="sxs-lookup"><span data-stu-id="ff86a-109">CN</span></span>                | <span data-ttu-id="ff86a-110">MS-SQL-RegisteredOwner</span><span class="sxs-lookup"><span data-stu-id="ff86a-110">MS-SQL-RegisteredOwner</span></span>                      |
| <span data-ttu-id="ff86a-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="ff86a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ff86a-112">mS-SQL-RegisteredOwner</span><span class="sxs-lookup"><span data-stu-id="ff86a-112">mS-SQL-RegisteredOwner</span></span>                      |
| <span data-ttu-id="ff86a-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="ff86a-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="ff86a-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="ff86a-114">Update Privilege</span></span>  | <span data-ttu-id="ff86a-115">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="ff86a-115">Domain administrator</span></span>                        |
| <span data-ttu-id="ff86a-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="ff86a-116">Update Frequency</span></span>  | <span data-ttu-id="ff86a-117">En el programa de instalación del sistema.</span><span class="sxs-lookup"><span data-stu-id="ff86a-117">At system setup.</span></span>                            |
| <span data-ttu-id="ff86a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ff86a-118">Attribute-Id</span></span>      | <span data-ttu-id="ff86a-119">1.2.840.113556.1.4.1364</span><span class="sxs-lookup"><span data-stu-id="ff86a-119">1.2.840.113556.1.4.1364</span></span>                     |
| <span data-ttu-id="ff86a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ff86a-120">System-Id-Guid</span></span>    | <span data-ttu-id="ff86a-121">48fd44ea-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="ff86a-121">48fd44ea-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="ff86a-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff86a-122">Syntax</span></span>            | [<span data-ttu-id="ff86a-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ff86a-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ff86a-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="ff86a-124">Implementations</span></span>

-   [<span data-ttu-id="ff86a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ff86a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ff86a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ff86a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ff86a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ff86a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ff86a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ff86a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ff86a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ff86a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ff86a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ff86a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ff86a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ff86a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ff86a-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff86a-132">Entry</span></span> | <span data-ttu-id="ff86a-133">Value</span><span class="sxs-lookup"><span data-stu-id="ff86a-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff86a-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ff86a-134">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="ff86a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff86a-135">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="ff86a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff86a-136">System-Only</span></span>            | <span data-ttu-id="ff86a-137">False</span><span class="sxs-lookup"><span data-stu-id="ff86a-137">False</span></span>                                                                                                                 |
| <span data-ttu-id="ff86a-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ff86a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ff86a-139">True</span><span class="sxs-lookup"><span data-stu-id="ff86a-139">True</span></span>                                                                                                                  |
| <span data-ttu-id="ff86a-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ff86a-140">Is Indexed</span></span>             | <span data-ttu-id="ff86a-141">False</span><span class="sxs-lookup"><span data-stu-id="ff86a-141">False</span></span>                                                                                                                 |
| <span data-ttu-id="ff86a-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff86a-142">In Global Catalog</span></span>      | <span data-ttu-id="ff86a-143">False</span><span class="sxs-lookup"><span data-stu-id="ff86a-143">False</span></span>                                                                                                                 |
| <span data-ttu-id="ff86a-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ff86a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff86a-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff86a-145">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="ff86a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff86a-146">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="ff86a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff86a-147">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="ff86a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff86a-148">Search-Flags</span></span>           | <span data-ttu-id="ff86a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff86a-149">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="ff86a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff86a-150">System-Flags</span></span>           | <span data-ttu-id="ff86a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff86a-151">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="ff86a-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ff86a-152">Classes used in</span></span>        | [<span data-ttu-id="ff86a-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="ff86a-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="ff86a-154">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="ff86a-154">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ff86a-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ff86a-155">Windows Server 2003</span></span>



| <span data-ttu-id="ff86a-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff86a-156">Entry</span></span> | <span data-ttu-id="ff86a-157">Value</span><span class="sxs-lookup"><span data-stu-id="ff86a-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff86a-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ff86a-158">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="ff86a-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff86a-159">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="ff86a-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff86a-160">System-Only</span></span>            | <span data-ttu-id="ff86a-161">False</span><span class="sxs-lookup"><span data-stu-id="ff86a-161">False</span></span>                                                                                                                 |
| <span data-ttu-id="ff86a-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ff86a-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ff86a-163">True</span><span class="sxs-lookup"><span data-stu-id="ff86a-163">True</span></span>                                                                                                                  |
| <span data-ttu-id="ff86a-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ff86a-164">Is Indexed</span></span>             | <span data-ttu-id="ff86a-165">False</span><span class="sxs-lookup"><span data-stu-id="ff86a-165">False</span></span>                                                                                                                 |
| <span data-ttu-id="ff86a-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff86a-166">In Global Catalog</span></span>      | <span data-ttu-id="ff86a-167">False</span><span class="sxs-lookup"><span data-stu-id="ff86a-167">False</span></span>                                                                                                                 |
| <span data-ttu-id="ff86a-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ff86a-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff86a-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff86a-169">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="ff86a-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff86a-170">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="ff86a-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff86a-171">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="ff86a-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff86a-172">Search-Flags</span></span>           | <span data-ttu-id="ff86a-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff86a-173">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="ff86a-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff86a-174">System-Flags</span></span>           | <span data-ttu-id="ff86a-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff86a-175">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="ff86a-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ff86a-176">Classes used in</span></span>        | [<span data-ttu-id="ff86a-177">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="ff86a-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="ff86a-178">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="ff86a-178">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ff86a-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ff86a-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ff86a-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff86a-180">Entry</span></span> | <span data-ttu-id="ff86a-181">Value</span><span class="sxs-lookup"><span data-stu-id="ff86a-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff86a-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ff86a-182">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="ff86a-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff86a-183">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="ff86a-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff86a-184">System-Only</span></span>            | <span data-ttu-id="ff86a-185">False</span><span class="sxs-lookup"><span data-stu-id="ff86a-185">False</span></span>                                                                                                                 |
| <span data-ttu-id="ff86a-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ff86a-186">Is-Single-Valued</span></span>       | <span data-ttu-id="ff86a-187">True</span><span class="sxs-lookup"><span data-stu-id="ff86a-187">True</span></span>                                                                                                                  |
| <span data-ttu-id="ff86a-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ff86a-188">Is Indexed</span></span>             | <span data-ttu-id="ff86a-189">False</span><span class="sxs-lookup"><span data-stu-id="ff86a-189">False</span></span>                                                                                                                 |
| <span data-ttu-id="ff86a-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff86a-190">In Global Catalog</span></span>      | <span data-ttu-id="ff86a-191">False</span><span class="sxs-lookup"><span data-stu-id="ff86a-191">False</span></span>                                                                                                                 |
| <span data-ttu-id="ff86a-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ff86a-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff86a-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff86a-193">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="ff86a-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff86a-194">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="ff86a-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff86a-195">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="ff86a-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff86a-196">Search-Flags</span></span>           | <span data-ttu-id="ff86a-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff86a-197">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="ff86a-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff86a-198">System-Flags</span></span>           | <span data-ttu-id="ff86a-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff86a-199">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="ff86a-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ff86a-200">Classes used in</span></span>        | [<span data-ttu-id="ff86a-201">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="ff86a-201">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="ff86a-202">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="ff86a-202">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ff86a-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff86a-203">Windows Server 2008</span></span>



| <span data-ttu-id="ff86a-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff86a-204">Entry</span></span> | <span data-ttu-id="ff86a-205">Value</span><span class="sxs-lookup"><span data-stu-id="ff86a-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff86a-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ff86a-206">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="ff86a-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff86a-207">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="ff86a-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff86a-208">System-Only</span></span>            | <span data-ttu-id="ff86a-209">False</span><span class="sxs-lookup"><span data-stu-id="ff86a-209">False</span></span>                                                                                                                 |
| <span data-ttu-id="ff86a-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ff86a-210">Is-Single-Valued</span></span>       | <span data-ttu-id="ff86a-211">True</span><span class="sxs-lookup"><span data-stu-id="ff86a-211">True</span></span>                                                                                                                  |
| <span data-ttu-id="ff86a-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ff86a-212">Is Indexed</span></span>             | <span data-ttu-id="ff86a-213">False</span><span class="sxs-lookup"><span data-stu-id="ff86a-213">False</span></span>                                                                                                                 |
| <span data-ttu-id="ff86a-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff86a-214">In Global Catalog</span></span>      | <span data-ttu-id="ff86a-215">False</span><span class="sxs-lookup"><span data-stu-id="ff86a-215">False</span></span>                                                                                                                 |
| <span data-ttu-id="ff86a-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ff86a-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff86a-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff86a-217">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="ff86a-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff86a-218">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="ff86a-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff86a-219">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="ff86a-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff86a-220">Search-Flags</span></span>           | <span data-ttu-id="ff86a-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff86a-221">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="ff86a-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff86a-222">System-Flags</span></span>           | <span data-ttu-id="ff86a-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff86a-223">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="ff86a-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ff86a-224">Classes used in</span></span>        | [<span data-ttu-id="ff86a-225">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="ff86a-225">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="ff86a-226">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="ff86a-226">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ff86a-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ff86a-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ff86a-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff86a-228">Entry</span></span> | <span data-ttu-id="ff86a-229">Value</span><span class="sxs-lookup"><span data-stu-id="ff86a-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff86a-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ff86a-230">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="ff86a-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff86a-231">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="ff86a-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff86a-232">System-Only</span></span>            | <span data-ttu-id="ff86a-233">False</span><span class="sxs-lookup"><span data-stu-id="ff86a-233">False</span></span>                                                                                                                 |
| <span data-ttu-id="ff86a-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ff86a-234">Is-Single-Valued</span></span>       | <span data-ttu-id="ff86a-235">True</span><span class="sxs-lookup"><span data-stu-id="ff86a-235">True</span></span>                                                                                                                  |
| <span data-ttu-id="ff86a-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ff86a-236">Is Indexed</span></span>             | <span data-ttu-id="ff86a-237">False</span><span class="sxs-lookup"><span data-stu-id="ff86a-237">False</span></span>                                                                                                                 |
| <span data-ttu-id="ff86a-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff86a-238">In Global Catalog</span></span>      | <span data-ttu-id="ff86a-239">False</span><span class="sxs-lookup"><span data-stu-id="ff86a-239">False</span></span>                                                                                                                 |
| <span data-ttu-id="ff86a-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ff86a-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff86a-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff86a-241">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="ff86a-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff86a-242">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="ff86a-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff86a-243">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="ff86a-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff86a-244">Search-Flags</span></span>           | <span data-ttu-id="ff86a-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff86a-245">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="ff86a-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff86a-246">System-Flags</span></span>           | <span data-ttu-id="ff86a-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff86a-247">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="ff86a-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ff86a-248">Classes used in</span></span>        | [<span data-ttu-id="ff86a-249">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="ff86a-249">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="ff86a-250">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="ff86a-250">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ff86a-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ff86a-251">Windows Server 2012</span></span>



| <span data-ttu-id="ff86a-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff86a-252">Entry</span></span> | <span data-ttu-id="ff86a-253">Value</span><span class="sxs-lookup"><span data-stu-id="ff86a-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff86a-254">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ff86a-254">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="ff86a-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff86a-255">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="ff86a-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff86a-256">System-Only</span></span>            | <span data-ttu-id="ff86a-257">False</span><span class="sxs-lookup"><span data-stu-id="ff86a-257">False</span></span>                                                                                                                 |
| <span data-ttu-id="ff86a-258">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ff86a-258">Is-Single-Valued</span></span>       | <span data-ttu-id="ff86a-259">True</span><span class="sxs-lookup"><span data-stu-id="ff86a-259">True</span></span>                                                                                                                  |
| <span data-ttu-id="ff86a-260">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ff86a-260">Is Indexed</span></span>             | <span data-ttu-id="ff86a-261">False</span><span class="sxs-lookup"><span data-stu-id="ff86a-261">False</span></span>                                                                                                                 |
| <span data-ttu-id="ff86a-262">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff86a-262">In Global Catalog</span></span>      | <span data-ttu-id="ff86a-263">False</span><span class="sxs-lookup"><span data-stu-id="ff86a-263">False</span></span>                                                                                                                 |
| <span data-ttu-id="ff86a-264">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ff86a-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff86a-265">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff86a-265">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="ff86a-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff86a-266">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="ff86a-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff86a-267">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="ff86a-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff86a-268">Search-Flags</span></span>           | <span data-ttu-id="ff86a-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff86a-269">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="ff86a-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff86a-270">System-Flags</span></span>           | <span data-ttu-id="ff86a-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff86a-271">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="ff86a-272">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ff86a-272">Classes used in</span></span>        | [<span data-ttu-id="ff86a-273">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="ff86a-273">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="ff86a-274">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="ff86a-274">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



 

 





