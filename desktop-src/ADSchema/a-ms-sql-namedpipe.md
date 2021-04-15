---
title: Atributo MS-SQL-NamedPipe
description: Conexión de canalización con nombre.
ms.assetid: d18c911d-06ed-4d08-b584-7b2748620770
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de MS-SQL-NamedPipe
- Esquema de AD de atributos de mS-SQL-NamedPipe
topic_type:
- apiref
api_name:
- MS-SQL-NamedPipe
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33e231be0561ae8c0e885911cb92954d6ff0d20d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104422651"
---
# <a name="ms-sql-namedpipe-attribute"></a><span data-ttu-id="13f8e-105">Atributo MS-SQL-NamedPipe</span><span class="sxs-lookup"><span data-stu-id="13f8e-105">MS-SQL-NamedPipe attribute</span></span>

<span data-ttu-id="13f8e-106">Conexión de canalización con nombre.</span><span class="sxs-lookup"><span data-stu-id="13f8e-106">The named pipe connection.</span></span>



| <span data-ttu-id="13f8e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="13f8e-107">Entry</span></span> | <span data-ttu-id="13f8e-108">Value</span><span class="sxs-lookup"><span data-stu-id="13f8e-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="13f8e-109">CN</span><span class="sxs-lookup"><span data-stu-id="13f8e-109">CN</span></span>                | <span data-ttu-id="13f8e-110">MS-SQL-NamedPipe</span><span class="sxs-lookup"><span data-stu-id="13f8e-110">MS-SQL-NamedPipe</span></span>                            |
| <span data-ttu-id="13f8e-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="13f8e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="13f8e-112">mS-SQL-NamedPipe</span><span class="sxs-lookup"><span data-stu-id="13f8e-112">mS-SQL-NamedPipe</span></span>                            |
| <span data-ttu-id="13f8e-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="13f8e-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="13f8e-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="13f8e-114">Update Privilege</span></span>  | <span data-ttu-id="13f8e-115">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="13f8e-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="13f8e-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="13f8e-116">Update Frequency</span></span>  | <span data-ttu-id="13f8e-117">Al iniciar el sistema.</span><span class="sxs-lookup"><span data-stu-id="13f8e-117">At system startup.</span></span>                          |
| <span data-ttu-id="13f8e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="13f8e-118">Attribute-Id</span></span>      | <span data-ttu-id="13f8e-119">1.2.840.113556.1.4.1374</span><span class="sxs-lookup"><span data-stu-id="13f8e-119">1.2.840.113556.1.4.1374</span></span>                     |
| <span data-ttu-id="13f8e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="13f8e-120">System-Id-Guid</span></span>    | <span data-ttu-id="13f8e-121">7b91c840-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="13f8e-121">7b91c840-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="13f8e-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13f8e-122">Syntax</span></span>            | [<span data-ttu-id="13f8e-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="13f8e-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="13f8e-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="13f8e-124">Implementations</span></span>

-   [<span data-ttu-id="13f8e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="13f8e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="13f8e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="13f8e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="13f8e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="13f8e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="13f8e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="13f8e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="13f8e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="13f8e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="13f8e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="13f8e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="13f8e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="13f8e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="13f8e-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="13f8e-132">Entry</span></span> | <span data-ttu-id="13f8e-133">Value</span><span class="sxs-lookup"><span data-stu-id="13f8e-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="13f8e-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="13f8e-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="13f8e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13f8e-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="13f8e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="13f8e-136">System-Only</span></span>            | <span data-ttu-id="13f8e-137">False</span><span class="sxs-lookup"><span data-stu-id="13f8e-137">False</span></span>                                                     |
| <span data-ttu-id="13f8e-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="13f8e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="13f8e-139">True</span><span class="sxs-lookup"><span data-stu-id="13f8e-139">True</span></span>                                                      |
| <span data-ttu-id="13f8e-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="13f8e-140">Is Indexed</span></span>             | <span data-ttu-id="13f8e-141">False</span><span class="sxs-lookup"><span data-stu-id="13f8e-141">False</span></span>                                                     |
| <span data-ttu-id="13f8e-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="13f8e-142">In Global Catalog</span></span>      | <span data-ttu-id="13f8e-143">False</span><span class="sxs-lookup"><span data-stu-id="13f8e-143">False</span></span>                                                     |
| <span data-ttu-id="13f8e-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="13f8e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="13f8e-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13f8e-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="13f8e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13f8e-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="13f8e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13f8e-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="13f8e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13f8e-148">Search-Flags</span></span>           | <span data-ttu-id="13f8e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13f8e-149">0x00000000</span></span>                                                |
| <span data-ttu-id="13f8e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13f8e-150">System-Flags</span></span>           | <span data-ttu-id="13f8e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13f8e-151">0x00000010</span></span>                                                |
| <span data-ttu-id="13f8e-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="13f8e-152">Classes used in</span></span>        | [<span data-ttu-id="13f8e-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="13f8e-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="13f8e-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="13f8e-154">Windows Server 2003</span></span>



| <span data-ttu-id="13f8e-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="13f8e-155">Entry</span></span> | <span data-ttu-id="13f8e-156">Value</span><span class="sxs-lookup"><span data-stu-id="13f8e-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="13f8e-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="13f8e-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="13f8e-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13f8e-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="13f8e-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="13f8e-159">System-Only</span></span>            | <span data-ttu-id="13f8e-160">False</span><span class="sxs-lookup"><span data-stu-id="13f8e-160">False</span></span>                                                     |
| <span data-ttu-id="13f8e-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="13f8e-161">Is-Single-Valued</span></span>       | <span data-ttu-id="13f8e-162">True</span><span class="sxs-lookup"><span data-stu-id="13f8e-162">True</span></span>                                                      |
| <span data-ttu-id="13f8e-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="13f8e-163">Is Indexed</span></span>             | <span data-ttu-id="13f8e-164">False</span><span class="sxs-lookup"><span data-stu-id="13f8e-164">False</span></span>                                                     |
| <span data-ttu-id="13f8e-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="13f8e-165">In Global Catalog</span></span>      | <span data-ttu-id="13f8e-166">False</span><span class="sxs-lookup"><span data-stu-id="13f8e-166">False</span></span>                                                     |
| <span data-ttu-id="13f8e-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="13f8e-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="13f8e-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13f8e-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="13f8e-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13f8e-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="13f8e-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13f8e-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="13f8e-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13f8e-171">Search-Flags</span></span>           | <span data-ttu-id="13f8e-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13f8e-172">0x00000000</span></span>                                                |
| <span data-ttu-id="13f8e-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13f8e-173">System-Flags</span></span>           | <span data-ttu-id="13f8e-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13f8e-174">0x00000010</span></span>                                                |
| <span data-ttu-id="13f8e-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="13f8e-175">Classes used in</span></span>        | [<span data-ttu-id="13f8e-176">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="13f8e-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="13f8e-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="13f8e-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="13f8e-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="13f8e-178">Entry</span></span> | <span data-ttu-id="13f8e-179">Value</span><span class="sxs-lookup"><span data-stu-id="13f8e-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="13f8e-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="13f8e-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="13f8e-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13f8e-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="13f8e-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="13f8e-182">System-Only</span></span>            | <span data-ttu-id="13f8e-183">False</span><span class="sxs-lookup"><span data-stu-id="13f8e-183">False</span></span>                                                     |
| <span data-ttu-id="13f8e-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="13f8e-184">Is-Single-Valued</span></span>       | <span data-ttu-id="13f8e-185">True</span><span class="sxs-lookup"><span data-stu-id="13f8e-185">True</span></span>                                                      |
| <span data-ttu-id="13f8e-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="13f8e-186">Is Indexed</span></span>             | <span data-ttu-id="13f8e-187">False</span><span class="sxs-lookup"><span data-stu-id="13f8e-187">False</span></span>                                                     |
| <span data-ttu-id="13f8e-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="13f8e-188">In Global Catalog</span></span>      | <span data-ttu-id="13f8e-189">False</span><span class="sxs-lookup"><span data-stu-id="13f8e-189">False</span></span>                                                     |
| <span data-ttu-id="13f8e-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="13f8e-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="13f8e-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13f8e-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="13f8e-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13f8e-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="13f8e-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13f8e-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="13f8e-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13f8e-194">Search-Flags</span></span>           | <span data-ttu-id="13f8e-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13f8e-195">0x00000000</span></span>                                                |
| <span data-ttu-id="13f8e-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13f8e-196">System-Flags</span></span>           | <span data-ttu-id="13f8e-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13f8e-197">0x00000010</span></span>                                                |
| <span data-ttu-id="13f8e-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="13f8e-198">Classes used in</span></span>        | [<span data-ttu-id="13f8e-199">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="13f8e-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="13f8e-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13f8e-200">Windows Server 2008</span></span>



| <span data-ttu-id="13f8e-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="13f8e-201">Entry</span></span> | <span data-ttu-id="13f8e-202">Value</span><span class="sxs-lookup"><span data-stu-id="13f8e-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="13f8e-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="13f8e-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="13f8e-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13f8e-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="13f8e-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="13f8e-205">System-Only</span></span>            | <span data-ttu-id="13f8e-206">False</span><span class="sxs-lookup"><span data-stu-id="13f8e-206">False</span></span>                                                     |
| <span data-ttu-id="13f8e-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="13f8e-207">Is-Single-Valued</span></span>       | <span data-ttu-id="13f8e-208">True</span><span class="sxs-lookup"><span data-stu-id="13f8e-208">True</span></span>                                                      |
| <span data-ttu-id="13f8e-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="13f8e-209">Is Indexed</span></span>             | <span data-ttu-id="13f8e-210">False</span><span class="sxs-lookup"><span data-stu-id="13f8e-210">False</span></span>                                                     |
| <span data-ttu-id="13f8e-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="13f8e-211">In Global Catalog</span></span>      | <span data-ttu-id="13f8e-212">False</span><span class="sxs-lookup"><span data-stu-id="13f8e-212">False</span></span>                                                     |
| <span data-ttu-id="13f8e-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="13f8e-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="13f8e-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13f8e-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="13f8e-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13f8e-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="13f8e-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13f8e-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="13f8e-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13f8e-217">Search-Flags</span></span>           | <span data-ttu-id="13f8e-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13f8e-218">0x00000000</span></span>                                                |
| <span data-ttu-id="13f8e-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13f8e-219">System-Flags</span></span>           | <span data-ttu-id="13f8e-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13f8e-220">0x00000010</span></span>                                                |
| <span data-ttu-id="13f8e-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="13f8e-221">Classes used in</span></span>        | [<span data-ttu-id="13f8e-222">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="13f8e-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="13f8e-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13f8e-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="13f8e-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="13f8e-224">Entry</span></span> | <span data-ttu-id="13f8e-225">Value</span><span class="sxs-lookup"><span data-stu-id="13f8e-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="13f8e-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="13f8e-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="13f8e-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13f8e-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="13f8e-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="13f8e-228">System-Only</span></span>            | <span data-ttu-id="13f8e-229">False</span><span class="sxs-lookup"><span data-stu-id="13f8e-229">False</span></span>                                                     |
| <span data-ttu-id="13f8e-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="13f8e-230">Is-Single-Valued</span></span>       | <span data-ttu-id="13f8e-231">True</span><span class="sxs-lookup"><span data-stu-id="13f8e-231">True</span></span>                                                      |
| <span data-ttu-id="13f8e-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="13f8e-232">Is Indexed</span></span>             | <span data-ttu-id="13f8e-233">False</span><span class="sxs-lookup"><span data-stu-id="13f8e-233">False</span></span>                                                     |
| <span data-ttu-id="13f8e-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="13f8e-234">In Global Catalog</span></span>      | <span data-ttu-id="13f8e-235">False</span><span class="sxs-lookup"><span data-stu-id="13f8e-235">False</span></span>                                                     |
| <span data-ttu-id="13f8e-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="13f8e-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="13f8e-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13f8e-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="13f8e-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13f8e-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="13f8e-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13f8e-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="13f8e-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13f8e-240">Search-Flags</span></span>           | <span data-ttu-id="13f8e-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13f8e-241">0x00000000</span></span>                                                |
| <span data-ttu-id="13f8e-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13f8e-242">System-Flags</span></span>           | <span data-ttu-id="13f8e-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13f8e-243">0x00000010</span></span>                                                |
| <span data-ttu-id="13f8e-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="13f8e-244">Classes used in</span></span>        | [<span data-ttu-id="13f8e-245">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="13f8e-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="13f8e-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13f8e-246">Windows Server 2012</span></span>



| <span data-ttu-id="13f8e-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="13f8e-247">Entry</span></span> | <span data-ttu-id="13f8e-248">Value</span><span class="sxs-lookup"><span data-stu-id="13f8e-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="13f8e-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="13f8e-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="13f8e-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13f8e-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="13f8e-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="13f8e-251">System-Only</span></span>            | <span data-ttu-id="13f8e-252">False</span><span class="sxs-lookup"><span data-stu-id="13f8e-252">False</span></span>                                                     |
| <span data-ttu-id="13f8e-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="13f8e-253">Is-Single-Valued</span></span>       | <span data-ttu-id="13f8e-254">True</span><span class="sxs-lookup"><span data-stu-id="13f8e-254">True</span></span>                                                      |
| <span data-ttu-id="13f8e-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="13f8e-255">Is Indexed</span></span>             | <span data-ttu-id="13f8e-256">False</span><span class="sxs-lookup"><span data-stu-id="13f8e-256">False</span></span>                                                     |
| <span data-ttu-id="13f8e-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="13f8e-257">In Global Catalog</span></span>      | <span data-ttu-id="13f8e-258">False</span><span class="sxs-lookup"><span data-stu-id="13f8e-258">False</span></span>                                                     |
| <span data-ttu-id="13f8e-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="13f8e-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="13f8e-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="13f8e-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="13f8e-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13f8e-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="13f8e-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13f8e-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="13f8e-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13f8e-263">Search-Flags</span></span>           | <span data-ttu-id="13f8e-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13f8e-264">0x00000000</span></span>                                                |
| <span data-ttu-id="13f8e-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13f8e-265">System-Flags</span></span>           | <span data-ttu-id="13f8e-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13f8e-266">0x00000010</span></span>                                                |
| <span data-ttu-id="13f8e-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="13f8e-267">Classes used in</span></span>        | [<span data-ttu-id="13f8e-268">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="13f8e-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





