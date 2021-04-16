---
title: Atributo de clúster de MS-SQL
description: True si el servidor está en clúster.
ms.assetid: 066609a4-fdf1-422b-9b26-445f617c99d4
ms.tgt_platform: multiple
keywords:
- MS-SQL-esquema de AD de atributo en clúster
- mS-SQL-esquema de AD de atributo en clúster
topic_type:
- apiref
api_name:
- MS-SQL-Clustered
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4ba701168f3dff5b3809818a6df987855a08e3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658595"
---
# <a name="ms-sql-clustered-attribute"></a><span data-ttu-id="38a19-105">Atributo de clúster de MS-SQL</span><span class="sxs-lookup"><span data-stu-id="38a19-105">MS-SQL-Clustered attribute</span></span>

<span data-ttu-id="38a19-106">True si el servidor está en clúster.</span><span class="sxs-lookup"><span data-stu-id="38a19-106">True if the server is clustered.</span></span>



| <span data-ttu-id="38a19-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="38a19-107">Entry</span></span> | <span data-ttu-id="38a19-108">Value</span><span class="sxs-lookup"><span data-stu-id="38a19-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="38a19-109">CN</span><span class="sxs-lookup"><span data-stu-id="38a19-109">CN</span></span>                | <span data-ttu-id="38a19-110">En clúster de MS-SQL</span><span class="sxs-lookup"><span data-stu-id="38a19-110">MS-SQL-Clustered</span></span>                     |
| <span data-ttu-id="38a19-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="38a19-111">Ldap-Display-Name</span></span> | <span data-ttu-id="38a19-112">en clúster de mS-SQL</span><span class="sxs-lookup"><span data-stu-id="38a19-112">mS-SQL-Clustered</span></span>                     |
| <span data-ttu-id="38a19-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="38a19-113">Size</span></span>              | <span data-ttu-id="38a19-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="38a19-114">4 bytes</span></span>                              |
| <span data-ttu-id="38a19-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="38a19-115">Update Privilege</span></span>  | <span data-ttu-id="38a19-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="38a19-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="38a19-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="38a19-117">Update Frequency</span></span>  | <span data-ttu-id="38a19-118">Al iniciar el sistema.</span><span class="sxs-lookup"><span data-stu-id="38a19-118">At system startup.</span></span>                   |
| <span data-ttu-id="38a19-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="38a19-119">Attribute-Id</span></span>      | <span data-ttu-id="38a19-120">1.2.840.113556.1.4.1373</span><span class="sxs-lookup"><span data-stu-id="38a19-120">1.2.840.113556.1.4.1373</span></span>              |
| <span data-ttu-id="38a19-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="38a19-121">System-Id-Guid</span></span>    | <span data-ttu-id="38a19-122">7778bd90-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="38a19-122">7778bd90-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="38a19-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38a19-123">Syntax</span></span>            | [<span data-ttu-id="38a19-124">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="38a19-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="38a19-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="38a19-125">Implementations</span></span>

-   [<span data-ttu-id="38a19-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="38a19-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="38a19-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="38a19-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="38a19-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="38a19-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="38a19-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="38a19-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="38a19-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="38a19-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="38a19-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="38a19-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="38a19-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="38a19-132">Windows 2000 Server</span></span>



| <span data-ttu-id="38a19-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="38a19-133">Entry</span></span> | <span data-ttu-id="38a19-134">Value</span><span class="sxs-lookup"><span data-stu-id="38a19-134">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="38a19-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38a19-135">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38a19-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38a19-136">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38a19-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="38a19-137">System-Only</span></span>            | <span data-ttu-id="38a19-138">False</span><span class="sxs-lookup"><span data-stu-id="38a19-138">False</span></span>                                                     |
| <span data-ttu-id="38a19-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38a19-139">Is-Single-Valued</span></span>       | <span data-ttu-id="38a19-140">True</span><span class="sxs-lookup"><span data-stu-id="38a19-140">True</span></span>                                                      |
| <span data-ttu-id="38a19-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38a19-141">Is Indexed</span></span>             | <span data-ttu-id="38a19-142">False</span><span class="sxs-lookup"><span data-stu-id="38a19-142">False</span></span>                                                     |
| <span data-ttu-id="38a19-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38a19-143">In Global Catalog</span></span>      | <span data-ttu-id="38a19-144">False</span><span class="sxs-lookup"><span data-stu-id="38a19-144">False</span></span>                                                     |
| <span data-ttu-id="38a19-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38a19-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="38a19-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38a19-146">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="38a19-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38a19-147">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="38a19-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38a19-148">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="38a19-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38a19-149">Search-Flags</span></span>           | <span data-ttu-id="38a19-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38a19-150">0x00000000</span></span>                                                |
| <span data-ttu-id="38a19-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38a19-151">System-Flags</span></span>           | <span data-ttu-id="38a19-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38a19-152">0x00000010</span></span>                                                |
| <span data-ttu-id="38a19-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38a19-153">Classes used in</span></span>        | [<span data-ttu-id="38a19-154">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="38a19-154">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="38a19-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="38a19-155">Windows Server 2003</span></span>



| <span data-ttu-id="38a19-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="38a19-156">Entry</span></span> | <span data-ttu-id="38a19-157">Value</span><span class="sxs-lookup"><span data-stu-id="38a19-157">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="38a19-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38a19-158">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38a19-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38a19-159">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38a19-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="38a19-160">System-Only</span></span>            | <span data-ttu-id="38a19-161">False</span><span class="sxs-lookup"><span data-stu-id="38a19-161">False</span></span>                                                     |
| <span data-ttu-id="38a19-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38a19-162">Is-Single-Valued</span></span>       | <span data-ttu-id="38a19-163">True</span><span class="sxs-lookup"><span data-stu-id="38a19-163">True</span></span>                                                      |
| <span data-ttu-id="38a19-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38a19-164">Is Indexed</span></span>             | <span data-ttu-id="38a19-165">False</span><span class="sxs-lookup"><span data-stu-id="38a19-165">False</span></span>                                                     |
| <span data-ttu-id="38a19-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38a19-166">In Global Catalog</span></span>      | <span data-ttu-id="38a19-167">False</span><span class="sxs-lookup"><span data-stu-id="38a19-167">False</span></span>                                                     |
| <span data-ttu-id="38a19-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38a19-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="38a19-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38a19-169">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="38a19-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38a19-170">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="38a19-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38a19-171">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="38a19-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38a19-172">Search-Flags</span></span>           | <span data-ttu-id="38a19-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38a19-173">0x00000000</span></span>                                                |
| <span data-ttu-id="38a19-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38a19-174">System-Flags</span></span>           | <span data-ttu-id="38a19-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38a19-175">0x00000010</span></span>                                                |
| <span data-ttu-id="38a19-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38a19-176">Classes used in</span></span>        | [<span data-ttu-id="38a19-177">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="38a19-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="38a19-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="38a19-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="38a19-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="38a19-179">Entry</span></span> | <span data-ttu-id="38a19-180">Value</span><span class="sxs-lookup"><span data-stu-id="38a19-180">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="38a19-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38a19-181">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38a19-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38a19-182">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38a19-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="38a19-183">System-Only</span></span>            | <span data-ttu-id="38a19-184">False</span><span class="sxs-lookup"><span data-stu-id="38a19-184">False</span></span>                                                     |
| <span data-ttu-id="38a19-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38a19-185">Is-Single-Valued</span></span>       | <span data-ttu-id="38a19-186">True</span><span class="sxs-lookup"><span data-stu-id="38a19-186">True</span></span>                                                      |
| <span data-ttu-id="38a19-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38a19-187">Is Indexed</span></span>             | <span data-ttu-id="38a19-188">False</span><span class="sxs-lookup"><span data-stu-id="38a19-188">False</span></span>                                                     |
| <span data-ttu-id="38a19-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38a19-189">In Global Catalog</span></span>      | <span data-ttu-id="38a19-190">False</span><span class="sxs-lookup"><span data-stu-id="38a19-190">False</span></span>                                                     |
| <span data-ttu-id="38a19-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38a19-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="38a19-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38a19-192">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="38a19-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38a19-193">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="38a19-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38a19-194">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="38a19-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38a19-195">Search-Flags</span></span>           | <span data-ttu-id="38a19-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38a19-196">0x00000000</span></span>                                                |
| <span data-ttu-id="38a19-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38a19-197">System-Flags</span></span>           | <span data-ttu-id="38a19-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38a19-198">0x00000010</span></span>                                                |
| <span data-ttu-id="38a19-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38a19-199">Classes used in</span></span>        | [<span data-ttu-id="38a19-200">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="38a19-200">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="38a19-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38a19-201">Windows Server 2008</span></span>



| <span data-ttu-id="38a19-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="38a19-202">Entry</span></span> | <span data-ttu-id="38a19-203">Value</span><span class="sxs-lookup"><span data-stu-id="38a19-203">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="38a19-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38a19-204">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38a19-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38a19-205">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38a19-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="38a19-206">System-Only</span></span>            | <span data-ttu-id="38a19-207">False</span><span class="sxs-lookup"><span data-stu-id="38a19-207">False</span></span>                                                     |
| <span data-ttu-id="38a19-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38a19-208">Is-Single-Valued</span></span>       | <span data-ttu-id="38a19-209">True</span><span class="sxs-lookup"><span data-stu-id="38a19-209">True</span></span>                                                      |
| <span data-ttu-id="38a19-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38a19-210">Is Indexed</span></span>             | <span data-ttu-id="38a19-211">False</span><span class="sxs-lookup"><span data-stu-id="38a19-211">False</span></span>                                                     |
| <span data-ttu-id="38a19-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38a19-212">In Global Catalog</span></span>      | <span data-ttu-id="38a19-213">False</span><span class="sxs-lookup"><span data-stu-id="38a19-213">False</span></span>                                                     |
| <span data-ttu-id="38a19-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38a19-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="38a19-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38a19-215">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="38a19-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38a19-216">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="38a19-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38a19-217">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="38a19-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38a19-218">Search-Flags</span></span>           | <span data-ttu-id="38a19-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38a19-219">0x00000000</span></span>                                                |
| <span data-ttu-id="38a19-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38a19-220">System-Flags</span></span>           | <span data-ttu-id="38a19-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38a19-221">0x00000010</span></span>                                                |
| <span data-ttu-id="38a19-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38a19-222">Classes used in</span></span>        | [<span data-ttu-id="38a19-223">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="38a19-223">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="38a19-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="38a19-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="38a19-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="38a19-225">Entry</span></span> | <span data-ttu-id="38a19-226">Value</span><span class="sxs-lookup"><span data-stu-id="38a19-226">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="38a19-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38a19-227">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38a19-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38a19-228">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38a19-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="38a19-229">System-Only</span></span>            | <span data-ttu-id="38a19-230">False</span><span class="sxs-lookup"><span data-stu-id="38a19-230">False</span></span>                                                     |
| <span data-ttu-id="38a19-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38a19-231">Is-Single-Valued</span></span>       | <span data-ttu-id="38a19-232">True</span><span class="sxs-lookup"><span data-stu-id="38a19-232">True</span></span>                                                      |
| <span data-ttu-id="38a19-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38a19-233">Is Indexed</span></span>             | <span data-ttu-id="38a19-234">False</span><span class="sxs-lookup"><span data-stu-id="38a19-234">False</span></span>                                                     |
| <span data-ttu-id="38a19-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38a19-235">In Global Catalog</span></span>      | <span data-ttu-id="38a19-236">False</span><span class="sxs-lookup"><span data-stu-id="38a19-236">False</span></span>                                                     |
| <span data-ttu-id="38a19-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38a19-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="38a19-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38a19-238">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="38a19-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38a19-239">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="38a19-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38a19-240">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="38a19-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38a19-241">Search-Flags</span></span>           | <span data-ttu-id="38a19-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38a19-242">0x00000000</span></span>                                                |
| <span data-ttu-id="38a19-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38a19-243">System-Flags</span></span>           | <span data-ttu-id="38a19-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38a19-244">0x00000010</span></span>                                                |
| <span data-ttu-id="38a19-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38a19-245">Classes used in</span></span>        | [<span data-ttu-id="38a19-246">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="38a19-246">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="38a19-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38a19-247">Windows Server 2012</span></span>



| <span data-ttu-id="38a19-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="38a19-248">Entry</span></span> | <span data-ttu-id="38a19-249">Value</span><span class="sxs-lookup"><span data-stu-id="38a19-249">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="38a19-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38a19-250">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38a19-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38a19-251">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38a19-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="38a19-252">System-Only</span></span>            | <span data-ttu-id="38a19-253">False</span><span class="sxs-lookup"><span data-stu-id="38a19-253">False</span></span>                                                     |
| <span data-ttu-id="38a19-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38a19-254">Is-Single-Valued</span></span>       | <span data-ttu-id="38a19-255">True</span><span class="sxs-lookup"><span data-stu-id="38a19-255">True</span></span>                                                      |
| <span data-ttu-id="38a19-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38a19-256">Is Indexed</span></span>             | <span data-ttu-id="38a19-257">False</span><span class="sxs-lookup"><span data-stu-id="38a19-257">False</span></span>                                                     |
| <span data-ttu-id="38a19-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38a19-258">In Global Catalog</span></span>      | <span data-ttu-id="38a19-259">False</span><span class="sxs-lookup"><span data-stu-id="38a19-259">False</span></span>                                                     |
| <span data-ttu-id="38a19-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38a19-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="38a19-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38a19-261">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="38a19-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38a19-262">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="38a19-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38a19-263">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="38a19-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38a19-264">Search-Flags</span></span>           | <span data-ttu-id="38a19-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38a19-265">0x00000000</span></span>                                                |
| <span data-ttu-id="38a19-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38a19-266">System-Flags</span></span>           | <span data-ttu-id="38a19-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38a19-267">0x00000010</span></span>                                                |
| <span data-ttu-id="38a19-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38a19-268">Classes used in</span></span>        | [<span data-ttu-id="38a19-269">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="38a19-269">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





