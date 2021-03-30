---
title: Atributo MS-SQL-LastDiagnosticDate
description: Última fecha en que se ejecutó DBCC CHECKDB.
ms.assetid: 7060e111-e4cb-4c5a-bce1-32712cbea00e
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de MS-SQL-LastDiagnosticDate
- Esquema de AD de atributos de mS-SQL-LastDiagnosticDate
topic_type:
- apiref
api_name:
- MS-SQL-LastDiagnosticDate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f25b8322a9f83b96c0ab4883478e6c0ffa2f3b49
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804388"
---
# <a name="ms-sql-lastdiagnosticdate-attribute"></a><span data-ttu-id="c8e56-105">Atributo MS-SQL-LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="c8e56-105">MS-SQL-LastDiagnosticDate attribute</span></span>

<span data-ttu-id="c8e56-106">Última fecha en que se ejecutó DBCC CHECKDB.</span><span class="sxs-lookup"><span data-stu-id="c8e56-106">The last date that DBCC checkdb was run.</span></span>



| <span data-ttu-id="c8e56-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8e56-107">Entry</span></span> | <span data-ttu-id="c8e56-108">Value</span><span class="sxs-lookup"><span data-stu-id="c8e56-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c8e56-109">CN</span><span class="sxs-lookup"><span data-stu-id="c8e56-109">CN</span></span>                | <span data-ttu-id="c8e56-110">MS-SQL-LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="c8e56-110">MS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="c8e56-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="c8e56-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c8e56-112">mS-SQL-LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="c8e56-112">mS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="c8e56-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="c8e56-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="c8e56-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="c8e56-114">Update Privilege</span></span>  | <span data-ttu-id="c8e56-115">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="c8e56-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="c8e56-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="c8e56-116">Update Frequency</span></span>  | <span data-ttu-id="c8e56-117">Cuando se ejecuta DBCC CHECKDB.</span><span class="sxs-lookup"><span data-stu-id="c8e56-117">When DBCC checkdb is run.</span></span>                   |
| <span data-ttu-id="c8e56-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c8e56-118">Attribute-Id</span></span>      | <span data-ttu-id="c8e56-119">1.2.840.113556.1.4.1399</span><span class="sxs-lookup"><span data-stu-id="c8e56-119">1.2.840.113556.1.4.1399</span></span>                     |
| <span data-ttu-id="c8e56-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c8e56-120">System-Id-Guid</span></span>    | <span data-ttu-id="c8e56-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="c8e56-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="c8e56-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8e56-122">Syntax</span></span>            | [<span data-ttu-id="c8e56-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c8e56-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c8e56-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="c8e56-124">Implementations</span></span>

-   [<span data-ttu-id="c8e56-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c8e56-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c8e56-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c8e56-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c8e56-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c8e56-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c8e56-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c8e56-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c8e56-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c8e56-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c8e56-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c8e56-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c8e56-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c8e56-131">Windows 2000 Server</span></span>



| <span data-ttu-id="c8e56-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8e56-132">Entry</span></span> | <span data-ttu-id="c8e56-133">Value</span><span class="sxs-lookup"><span data-stu-id="c8e56-133">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c8e56-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c8e56-134">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c8e56-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8e56-135">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c8e56-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8e56-136">System-Only</span></span>            | <span data-ttu-id="c8e56-137">False</span><span class="sxs-lookup"><span data-stu-id="c8e56-137">False</span></span>                                                         |
| <span data-ttu-id="c8e56-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c8e56-138">Is-Single-Valued</span></span>       | <span data-ttu-id="c8e56-139">True</span><span class="sxs-lookup"><span data-stu-id="c8e56-139">True</span></span>                                                          |
| <span data-ttu-id="c8e56-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c8e56-140">Is Indexed</span></span>             | <span data-ttu-id="c8e56-141">False</span><span class="sxs-lookup"><span data-stu-id="c8e56-141">False</span></span>                                                         |
| <span data-ttu-id="c8e56-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c8e56-142">In Global Catalog</span></span>      | <span data-ttu-id="c8e56-143">False</span><span class="sxs-lookup"><span data-stu-id="c8e56-143">False</span></span>                                                         |
| <span data-ttu-id="c8e56-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c8e56-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8e56-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c8e56-145">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c8e56-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8e56-146">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c8e56-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8e56-147">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c8e56-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8e56-148">Search-Flags</span></span>           | <span data-ttu-id="c8e56-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8e56-149">0x00000000</span></span>                                                    |
| <span data-ttu-id="c8e56-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8e56-150">System-Flags</span></span>           | <span data-ttu-id="c8e56-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8e56-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="c8e56-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c8e56-152">Classes used in</span></span>        | [<span data-ttu-id="c8e56-153">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="c8e56-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c8e56-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c8e56-154">Windows Server 2003</span></span>



| <span data-ttu-id="c8e56-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8e56-155">Entry</span></span> | <span data-ttu-id="c8e56-156">Value</span><span class="sxs-lookup"><span data-stu-id="c8e56-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c8e56-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c8e56-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c8e56-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8e56-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c8e56-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8e56-159">System-Only</span></span>            | <span data-ttu-id="c8e56-160">False</span><span class="sxs-lookup"><span data-stu-id="c8e56-160">False</span></span>                                                         |
| <span data-ttu-id="c8e56-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c8e56-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c8e56-162">True</span><span class="sxs-lookup"><span data-stu-id="c8e56-162">True</span></span>                                                          |
| <span data-ttu-id="c8e56-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c8e56-163">Is Indexed</span></span>             | <span data-ttu-id="c8e56-164">False</span><span class="sxs-lookup"><span data-stu-id="c8e56-164">False</span></span>                                                         |
| <span data-ttu-id="c8e56-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c8e56-165">In Global Catalog</span></span>      | <span data-ttu-id="c8e56-166">False</span><span class="sxs-lookup"><span data-stu-id="c8e56-166">False</span></span>                                                         |
| <span data-ttu-id="c8e56-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c8e56-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8e56-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c8e56-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c8e56-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8e56-169">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c8e56-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8e56-170">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c8e56-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8e56-171">Search-Flags</span></span>           | <span data-ttu-id="c8e56-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8e56-172">0x00000000</span></span>                                                    |
| <span data-ttu-id="c8e56-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8e56-173">System-Flags</span></span>           | <span data-ttu-id="c8e56-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8e56-174">0x00000010</span></span>                                                    |
| <span data-ttu-id="c8e56-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c8e56-175">Classes used in</span></span>        | [<span data-ttu-id="c8e56-176">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="c8e56-176">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c8e56-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c8e56-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c8e56-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8e56-178">Entry</span></span> | <span data-ttu-id="c8e56-179">Value</span><span class="sxs-lookup"><span data-stu-id="c8e56-179">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c8e56-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c8e56-180">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c8e56-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8e56-181">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c8e56-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8e56-182">System-Only</span></span>            | <span data-ttu-id="c8e56-183">False</span><span class="sxs-lookup"><span data-stu-id="c8e56-183">False</span></span>                                                         |
| <span data-ttu-id="c8e56-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c8e56-184">Is-Single-Valued</span></span>       | <span data-ttu-id="c8e56-185">True</span><span class="sxs-lookup"><span data-stu-id="c8e56-185">True</span></span>                                                          |
| <span data-ttu-id="c8e56-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c8e56-186">Is Indexed</span></span>             | <span data-ttu-id="c8e56-187">False</span><span class="sxs-lookup"><span data-stu-id="c8e56-187">False</span></span>                                                         |
| <span data-ttu-id="c8e56-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c8e56-188">In Global Catalog</span></span>      | <span data-ttu-id="c8e56-189">False</span><span class="sxs-lookup"><span data-stu-id="c8e56-189">False</span></span>                                                         |
| <span data-ttu-id="c8e56-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c8e56-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8e56-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c8e56-191">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c8e56-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8e56-192">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c8e56-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8e56-193">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c8e56-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8e56-194">Search-Flags</span></span>           | <span data-ttu-id="c8e56-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8e56-195">0x00000000</span></span>                                                    |
| <span data-ttu-id="c8e56-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8e56-196">System-Flags</span></span>           | <span data-ttu-id="c8e56-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8e56-197">0x00000010</span></span>                                                    |
| <span data-ttu-id="c8e56-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c8e56-198">Classes used in</span></span>        | [<span data-ttu-id="c8e56-199">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="c8e56-199">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c8e56-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8e56-200">Windows Server 2008</span></span>



| <span data-ttu-id="c8e56-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8e56-201">Entry</span></span> | <span data-ttu-id="c8e56-202">Value</span><span class="sxs-lookup"><span data-stu-id="c8e56-202">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c8e56-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c8e56-203">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c8e56-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8e56-204">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c8e56-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8e56-205">System-Only</span></span>            | <span data-ttu-id="c8e56-206">False</span><span class="sxs-lookup"><span data-stu-id="c8e56-206">False</span></span>                                                         |
| <span data-ttu-id="c8e56-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c8e56-207">Is-Single-Valued</span></span>       | <span data-ttu-id="c8e56-208">True</span><span class="sxs-lookup"><span data-stu-id="c8e56-208">True</span></span>                                                          |
| <span data-ttu-id="c8e56-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c8e56-209">Is Indexed</span></span>             | <span data-ttu-id="c8e56-210">False</span><span class="sxs-lookup"><span data-stu-id="c8e56-210">False</span></span>                                                         |
| <span data-ttu-id="c8e56-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c8e56-211">In Global Catalog</span></span>      | <span data-ttu-id="c8e56-212">False</span><span class="sxs-lookup"><span data-stu-id="c8e56-212">False</span></span>                                                         |
| <span data-ttu-id="c8e56-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c8e56-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8e56-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c8e56-214">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c8e56-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8e56-215">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c8e56-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8e56-216">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c8e56-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8e56-217">Search-Flags</span></span>           | <span data-ttu-id="c8e56-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8e56-218">0x00000000</span></span>                                                    |
| <span data-ttu-id="c8e56-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8e56-219">System-Flags</span></span>           | <span data-ttu-id="c8e56-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8e56-220">0x00000010</span></span>                                                    |
| <span data-ttu-id="c8e56-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c8e56-221">Classes used in</span></span>        | [<span data-ttu-id="c8e56-222">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="c8e56-222">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c8e56-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c8e56-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c8e56-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8e56-224">Entry</span></span> | <span data-ttu-id="c8e56-225">Value</span><span class="sxs-lookup"><span data-stu-id="c8e56-225">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c8e56-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c8e56-226">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c8e56-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8e56-227">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c8e56-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8e56-228">System-Only</span></span>            | <span data-ttu-id="c8e56-229">False</span><span class="sxs-lookup"><span data-stu-id="c8e56-229">False</span></span>                                                         |
| <span data-ttu-id="c8e56-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c8e56-230">Is-Single-Valued</span></span>       | <span data-ttu-id="c8e56-231">True</span><span class="sxs-lookup"><span data-stu-id="c8e56-231">True</span></span>                                                          |
| <span data-ttu-id="c8e56-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c8e56-232">Is Indexed</span></span>             | <span data-ttu-id="c8e56-233">False</span><span class="sxs-lookup"><span data-stu-id="c8e56-233">False</span></span>                                                         |
| <span data-ttu-id="c8e56-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c8e56-234">In Global Catalog</span></span>      | <span data-ttu-id="c8e56-235">False</span><span class="sxs-lookup"><span data-stu-id="c8e56-235">False</span></span>                                                         |
| <span data-ttu-id="c8e56-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c8e56-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8e56-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c8e56-237">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c8e56-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8e56-238">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c8e56-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8e56-239">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c8e56-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8e56-240">Search-Flags</span></span>           | <span data-ttu-id="c8e56-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8e56-241">0x00000000</span></span>                                                    |
| <span data-ttu-id="c8e56-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8e56-242">System-Flags</span></span>           | <span data-ttu-id="c8e56-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8e56-243">0x00000010</span></span>                                                    |
| <span data-ttu-id="c8e56-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c8e56-244">Classes used in</span></span>        | [<span data-ttu-id="c8e56-245">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="c8e56-245">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c8e56-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c8e56-246">Windows Server 2012</span></span>



| <span data-ttu-id="c8e56-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8e56-247">Entry</span></span> | <span data-ttu-id="c8e56-248">Value</span><span class="sxs-lookup"><span data-stu-id="c8e56-248">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c8e56-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c8e56-249">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c8e56-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8e56-250">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c8e56-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8e56-251">System-Only</span></span>            | <span data-ttu-id="c8e56-252">False</span><span class="sxs-lookup"><span data-stu-id="c8e56-252">False</span></span>                                                         |
| <span data-ttu-id="c8e56-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c8e56-253">Is-Single-Valued</span></span>       | <span data-ttu-id="c8e56-254">True</span><span class="sxs-lookup"><span data-stu-id="c8e56-254">True</span></span>                                                          |
| <span data-ttu-id="c8e56-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c8e56-255">Is Indexed</span></span>             | <span data-ttu-id="c8e56-256">False</span><span class="sxs-lookup"><span data-stu-id="c8e56-256">False</span></span>                                                         |
| <span data-ttu-id="c8e56-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c8e56-257">In Global Catalog</span></span>      | <span data-ttu-id="c8e56-258">False</span><span class="sxs-lookup"><span data-stu-id="c8e56-258">False</span></span>                                                         |
| <span data-ttu-id="c8e56-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c8e56-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8e56-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c8e56-260">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c8e56-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8e56-261">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c8e56-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8e56-262">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c8e56-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8e56-263">Search-Flags</span></span>           | <span data-ttu-id="c8e56-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8e56-264">0x00000000</span></span>                                                    |
| <span data-ttu-id="c8e56-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8e56-265">System-Flags</span></span>           | <span data-ttu-id="c8e56-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8e56-266">0x00000010</span></span>                                                    |
| <span data-ttu-id="c8e56-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c8e56-267">Classes used in</span></span>        | [<span data-ttu-id="c8e56-268">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="c8e56-268">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



 

 





