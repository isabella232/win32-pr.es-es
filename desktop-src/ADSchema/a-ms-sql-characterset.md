---
title: Atributo MS-SQL-CharacterSet
description: Juego de caracteres de la instancia actual de SQL Server.
ms.assetid: 5c45058f-e883-455c-8e18-415ddae149f8
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos MS-SQL-CharacterSet
- Esquema de AD de atributos mS-SQL-CharacterSet
topic_type:
- apiref
api_name:
- MS-SQL-CharacterSet
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f2f3718c9e47393498e42c4091283ea768d5072
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906237"
---
# <a name="ms-sql-characterset-attribute"></a><span data-ttu-id="d58e9-105">Atributo MS-SQL-CharacterSet</span><span class="sxs-lookup"><span data-stu-id="d58e9-105">MS-SQL-CharacterSet attribute</span></span>

<span data-ttu-id="d58e9-106">Juego de caracteres de la instancia actual de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d58e9-106">The character set for the current instance of SQL Server.</span></span>



| <span data-ttu-id="d58e9-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d58e9-107">Entry</span></span> | <span data-ttu-id="d58e9-108">Value</span><span class="sxs-lookup"><span data-stu-id="d58e9-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d58e9-109">CN</span><span class="sxs-lookup"><span data-stu-id="d58e9-109">CN</span></span>                | <span data-ttu-id="d58e9-110">MS-SQL-CharacterSet</span><span class="sxs-lookup"><span data-stu-id="d58e9-110">MS-SQL-CharacterSet</span></span>                  |
| <span data-ttu-id="d58e9-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="d58e9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d58e9-112">mS-SQL-CharacterSet</span><span class="sxs-lookup"><span data-stu-id="d58e9-112">mS-SQL-CharacterSet</span></span>                  |
| <span data-ttu-id="d58e9-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="d58e9-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="d58e9-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="d58e9-114">Update Privilege</span></span>  | <span data-ttu-id="d58e9-115">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="d58e9-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="d58e9-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="d58e9-116">Update Frequency</span></span>  | <span data-ttu-id="d58e9-117">Al iniciar el sistema.</span><span class="sxs-lookup"><span data-stu-id="d58e9-117">At system startup.</span></span>                   |
| <span data-ttu-id="d58e9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d58e9-118">Attribute-Id</span></span>      | <span data-ttu-id="d58e9-119">1.2.840.113556.1.4.1370</span><span class="sxs-lookup"><span data-stu-id="d58e9-119">1.2.840.113556.1.4.1370</span></span>              |
| <span data-ttu-id="d58e9-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d58e9-120">System-Id-Guid</span></span>    | <span data-ttu-id="d58e9-121">696177a6-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="d58e9-121">696177a6-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="d58e9-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d58e9-122">Syntax</span></span>            | [<span data-ttu-id="d58e9-123">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="d58e9-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="d58e9-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="d58e9-124">Implementations</span></span>

-   [<span data-ttu-id="d58e9-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d58e9-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d58e9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d58e9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d58e9-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d58e9-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d58e9-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d58e9-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d58e9-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d58e9-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d58e9-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d58e9-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d58e9-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d58e9-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d58e9-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="d58e9-132">Entry</span></span> | <span data-ttu-id="d58e9-133">Value</span><span class="sxs-lookup"><span data-stu-id="d58e9-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d58e9-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d58e9-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d58e9-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d58e9-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d58e9-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d58e9-136">System-Only</span></span>            | <span data-ttu-id="d58e9-137">False</span><span class="sxs-lookup"><span data-stu-id="d58e9-137">False</span></span>                                                     |
| <span data-ttu-id="d58e9-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d58e9-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d58e9-139">True</span><span class="sxs-lookup"><span data-stu-id="d58e9-139">True</span></span>                                                      |
| <span data-ttu-id="d58e9-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d58e9-140">Is Indexed</span></span>             | <span data-ttu-id="d58e9-141">False</span><span class="sxs-lookup"><span data-stu-id="d58e9-141">False</span></span>                                                     |
| <span data-ttu-id="d58e9-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d58e9-142">In Global Catalog</span></span>      | <span data-ttu-id="d58e9-143">False</span><span class="sxs-lookup"><span data-stu-id="d58e9-143">False</span></span>                                                     |
| <span data-ttu-id="d58e9-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d58e9-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d58e9-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d58e9-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d58e9-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d58e9-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d58e9-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d58e9-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d58e9-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d58e9-148">Search-Flags</span></span>           | <span data-ttu-id="d58e9-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d58e9-149">0x00000000</span></span>                                                |
| <span data-ttu-id="d58e9-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d58e9-150">System-Flags</span></span>           | <span data-ttu-id="d58e9-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d58e9-151">0x00000010</span></span>                                                |
| <span data-ttu-id="d58e9-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d58e9-152">Classes used in</span></span>        | [<span data-ttu-id="d58e9-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="d58e9-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d58e9-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d58e9-154">Windows Server 2003</span></span>



| <span data-ttu-id="d58e9-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="d58e9-155">Entry</span></span> | <span data-ttu-id="d58e9-156">Value</span><span class="sxs-lookup"><span data-stu-id="d58e9-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d58e9-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d58e9-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d58e9-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d58e9-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d58e9-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d58e9-159">System-Only</span></span>            | <span data-ttu-id="d58e9-160">False</span><span class="sxs-lookup"><span data-stu-id="d58e9-160">False</span></span>                                                     |
| <span data-ttu-id="d58e9-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d58e9-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d58e9-162">True</span><span class="sxs-lookup"><span data-stu-id="d58e9-162">True</span></span>                                                      |
| <span data-ttu-id="d58e9-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d58e9-163">Is Indexed</span></span>             | <span data-ttu-id="d58e9-164">False</span><span class="sxs-lookup"><span data-stu-id="d58e9-164">False</span></span>                                                     |
| <span data-ttu-id="d58e9-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d58e9-165">In Global Catalog</span></span>      | <span data-ttu-id="d58e9-166">False</span><span class="sxs-lookup"><span data-stu-id="d58e9-166">False</span></span>                                                     |
| <span data-ttu-id="d58e9-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d58e9-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d58e9-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d58e9-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d58e9-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d58e9-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d58e9-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d58e9-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d58e9-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d58e9-171">Search-Flags</span></span>           | <span data-ttu-id="d58e9-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d58e9-172">0x00000000</span></span>                                                |
| <span data-ttu-id="d58e9-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d58e9-173">System-Flags</span></span>           | <span data-ttu-id="d58e9-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d58e9-174">0x00000010</span></span>                                                |
| <span data-ttu-id="d58e9-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d58e9-175">Classes used in</span></span>        | [<span data-ttu-id="d58e9-176">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="d58e9-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d58e9-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d58e9-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d58e9-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="d58e9-178">Entry</span></span> | <span data-ttu-id="d58e9-179">Value</span><span class="sxs-lookup"><span data-stu-id="d58e9-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d58e9-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d58e9-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d58e9-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d58e9-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d58e9-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="d58e9-182">System-Only</span></span>            | <span data-ttu-id="d58e9-183">False</span><span class="sxs-lookup"><span data-stu-id="d58e9-183">False</span></span>                                                     |
| <span data-ttu-id="d58e9-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d58e9-184">Is-Single-Valued</span></span>       | <span data-ttu-id="d58e9-185">True</span><span class="sxs-lookup"><span data-stu-id="d58e9-185">True</span></span>                                                      |
| <span data-ttu-id="d58e9-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d58e9-186">Is Indexed</span></span>             | <span data-ttu-id="d58e9-187">False</span><span class="sxs-lookup"><span data-stu-id="d58e9-187">False</span></span>                                                     |
| <span data-ttu-id="d58e9-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d58e9-188">In Global Catalog</span></span>      | <span data-ttu-id="d58e9-189">False</span><span class="sxs-lookup"><span data-stu-id="d58e9-189">False</span></span>                                                     |
| <span data-ttu-id="d58e9-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d58e9-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="d58e9-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d58e9-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d58e9-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d58e9-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d58e9-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d58e9-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d58e9-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d58e9-194">Search-Flags</span></span>           | <span data-ttu-id="d58e9-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d58e9-195">0x00000000</span></span>                                                |
| <span data-ttu-id="d58e9-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d58e9-196">System-Flags</span></span>           | <span data-ttu-id="d58e9-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d58e9-197">0x00000010</span></span>                                                |
| <span data-ttu-id="d58e9-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d58e9-198">Classes used in</span></span>        | [<span data-ttu-id="d58e9-199">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="d58e9-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d58e9-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d58e9-200">Windows Server 2008</span></span>



| <span data-ttu-id="d58e9-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="d58e9-201">Entry</span></span> | <span data-ttu-id="d58e9-202">Value</span><span class="sxs-lookup"><span data-stu-id="d58e9-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d58e9-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d58e9-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d58e9-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d58e9-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d58e9-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="d58e9-205">System-Only</span></span>            | <span data-ttu-id="d58e9-206">False</span><span class="sxs-lookup"><span data-stu-id="d58e9-206">False</span></span>                                                     |
| <span data-ttu-id="d58e9-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d58e9-207">Is-Single-Valued</span></span>       | <span data-ttu-id="d58e9-208">True</span><span class="sxs-lookup"><span data-stu-id="d58e9-208">True</span></span>                                                      |
| <span data-ttu-id="d58e9-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d58e9-209">Is Indexed</span></span>             | <span data-ttu-id="d58e9-210">False</span><span class="sxs-lookup"><span data-stu-id="d58e9-210">False</span></span>                                                     |
| <span data-ttu-id="d58e9-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d58e9-211">In Global Catalog</span></span>      | <span data-ttu-id="d58e9-212">False</span><span class="sxs-lookup"><span data-stu-id="d58e9-212">False</span></span>                                                     |
| <span data-ttu-id="d58e9-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d58e9-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="d58e9-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d58e9-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d58e9-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d58e9-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d58e9-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d58e9-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d58e9-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d58e9-217">Search-Flags</span></span>           | <span data-ttu-id="d58e9-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d58e9-218">0x00000000</span></span>                                                |
| <span data-ttu-id="d58e9-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d58e9-219">System-Flags</span></span>           | <span data-ttu-id="d58e9-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d58e9-220">0x00000010</span></span>                                                |
| <span data-ttu-id="d58e9-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d58e9-221">Classes used in</span></span>        | [<span data-ttu-id="d58e9-222">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="d58e9-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d58e9-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d58e9-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d58e9-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="d58e9-224">Entry</span></span> | <span data-ttu-id="d58e9-225">Value</span><span class="sxs-lookup"><span data-stu-id="d58e9-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d58e9-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d58e9-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d58e9-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d58e9-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d58e9-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d58e9-228">System-Only</span></span>            | <span data-ttu-id="d58e9-229">False</span><span class="sxs-lookup"><span data-stu-id="d58e9-229">False</span></span>                                                     |
| <span data-ttu-id="d58e9-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d58e9-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d58e9-231">True</span><span class="sxs-lookup"><span data-stu-id="d58e9-231">True</span></span>                                                      |
| <span data-ttu-id="d58e9-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d58e9-232">Is Indexed</span></span>             | <span data-ttu-id="d58e9-233">False</span><span class="sxs-lookup"><span data-stu-id="d58e9-233">False</span></span>                                                     |
| <span data-ttu-id="d58e9-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d58e9-234">In Global Catalog</span></span>      | <span data-ttu-id="d58e9-235">False</span><span class="sxs-lookup"><span data-stu-id="d58e9-235">False</span></span>                                                     |
| <span data-ttu-id="d58e9-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d58e9-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d58e9-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d58e9-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d58e9-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d58e9-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d58e9-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d58e9-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d58e9-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d58e9-240">Search-Flags</span></span>           | <span data-ttu-id="d58e9-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d58e9-241">0x00000000</span></span>                                                |
| <span data-ttu-id="d58e9-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d58e9-242">System-Flags</span></span>           | <span data-ttu-id="d58e9-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d58e9-243">0x00000010</span></span>                                                |
| <span data-ttu-id="d58e9-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d58e9-244">Classes used in</span></span>        | [<span data-ttu-id="d58e9-245">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="d58e9-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d58e9-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d58e9-246">Windows Server 2012</span></span>



| <span data-ttu-id="d58e9-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="d58e9-247">Entry</span></span> | <span data-ttu-id="d58e9-248">Value</span><span class="sxs-lookup"><span data-stu-id="d58e9-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d58e9-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d58e9-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d58e9-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d58e9-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d58e9-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="d58e9-251">System-Only</span></span>            | <span data-ttu-id="d58e9-252">False</span><span class="sxs-lookup"><span data-stu-id="d58e9-252">False</span></span>                                                     |
| <span data-ttu-id="d58e9-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d58e9-253">Is-Single-Valued</span></span>       | <span data-ttu-id="d58e9-254">True</span><span class="sxs-lookup"><span data-stu-id="d58e9-254">True</span></span>                                                      |
| <span data-ttu-id="d58e9-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d58e9-255">Is Indexed</span></span>             | <span data-ttu-id="d58e9-256">False</span><span class="sxs-lookup"><span data-stu-id="d58e9-256">False</span></span>                                                     |
| <span data-ttu-id="d58e9-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d58e9-257">In Global Catalog</span></span>      | <span data-ttu-id="d58e9-258">False</span><span class="sxs-lookup"><span data-stu-id="d58e9-258">False</span></span>                                                     |
| <span data-ttu-id="d58e9-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d58e9-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="d58e9-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d58e9-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d58e9-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d58e9-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d58e9-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d58e9-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d58e9-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d58e9-263">Search-Flags</span></span>           | <span data-ttu-id="d58e9-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d58e9-264">0x00000000</span></span>                                                |
| <span data-ttu-id="d58e9-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d58e9-265">System-Flags</span></span>           | <span data-ttu-id="d58e9-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d58e9-266">0x00000010</span></span>                                                |
| <span data-ttu-id="d58e9-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d58e9-267">Classes used in</span></span>        | [<span data-ttu-id="d58e9-268">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="d58e9-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





