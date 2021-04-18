---
title: Atributo MS-SQL-TCPIP
description: El punto de conexión TCP.
ms.assetid: f61f7d54-958e-4f34-852e-222338c26de0
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de MS-SQL-TCPIP
- Esquema de AD de atributos de mS-SQL-TCPIP
topic_type:
- apiref
api_name:
- MS-SQL-TCPIP
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 098d5e7818789774b425ad9e238f8f3b3a4d5378
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659179"
---
# <a name="ms-sql-tcpip-attribute"></a><span data-ttu-id="1efa6-105">Atributo MS-SQL-TCPIP</span><span class="sxs-lookup"><span data-stu-id="1efa6-105">MS-SQL-TCPIP attribute</span></span>

<span data-ttu-id="1efa6-106">El punto de conexión TCP.</span><span class="sxs-lookup"><span data-stu-id="1efa6-106">The TCP connection point.</span></span>



| <span data-ttu-id="1efa6-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="1efa6-107">Entry</span></span> | <span data-ttu-id="1efa6-108">Value</span><span class="sxs-lookup"><span data-stu-id="1efa6-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="1efa6-109">CN</span><span class="sxs-lookup"><span data-stu-id="1efa6-109">CN</span></span>                | <span data-ttu-id="1efa6-110">MS-SQL-TCPIP</span><span class="sxs-lookup"><span data-stu-id="1efa6-110">MS-SQL-TCPIP</span></span>                                |
| <span data-ttu-id="1efa6-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="1efa6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1efa6-112">mS-SQL-TCPIP</span><span class="sxs-lookup"><span data-stu-id="1efa6-112">mS-SQL-TCPIP</span></span>                                |
| <span data-ttu-id="1efa6-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="1efa6-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="1efa6-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="1efa6-114">Update Privilege</span></span>  | <span data-ttu-id="1efa6-115">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="1efa6-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="1efa6-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="1efa6-116">Update Frequency</span></span>  | <span data-ttu-id="1efa6-117">Al iniciar el sistema.</span><span class="sxs-lookup"><span data-stu-id="1efa6-117">At system startup.</span></span>                          |
| <span data-ttu-id="1efa6-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1efa6-118">Attribute-Id</span></span>      | <span data-ttu-id="1efa6-119">1.2.840.113556.1.4.1377</span><span class="sxs-lookup"><span data-stu-id="1efa6-119">1.2.840.113556.1.4.1377</span></span>                     |
| <span data-ttu-id="1efa6-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1efa6-120">System-Id-Guid</span></span>    | <span data-ttu-id="1efa6-121">8ac263a6-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="1efa6-121">8ac263a6-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="1efa6-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1efa6-122">Syntax</span></span>            | [<span data-ttu-id="1efa6-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1efa6-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="1efa6-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="1efa6-124">Implementations</span></span>

-   [<span data-ttu-id="1efa6-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1efa6-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1efa6-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1efa6-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1efa6-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1efa6-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1efa6-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1efa6-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1efa6-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1efa6-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1efa6-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1efa6-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1efa6-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1efa6-131">Windows 2000 Server</span></span>



| <span data-ttu-id="1efa6-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="1efa6-132">Entry</span></span> | <span data-ttu-id="1efa6-133">Value</span><span class="sxs-lookup"><span data-stu-id="1efa6-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1efa6-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1efa6-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1efa6-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1efa6-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1efa6-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="1efa6-136">System-Only</span></span>            | <span data-ttu-id="1efa6-137">False</span><span class="sxs-lookup"><span data-stu-id="1efa6-137">False</span></span>                                                     |
| <span data-ttu-id="1efa6-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1efa6-138">Is-Single-Valued</span></span>       | <span data-ttu-id="1efa6-139">True</span><span class="sxs-lookup"><span data-stu-id="1efa6-139">True</span></span>                                                      |
| <span data-ttu-id="1efa6-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1efa6-140">Is Indexed</span></span>             | <span data-ttu-id="1efa6-141">False</span><span class="sxs-lookup"><span data-stu-id="1efa6-141">False</span></span>                                                     |
| <span data-ttu-id="1efa6-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1efa6-142">In Global Catalog</span></span>      | <span data-ttu-id="1efa6-143">False</span><span class="sxs-lookup"><span data-stu-id="1efa6-143">False</span></span>                                                     |
| <span data-ttu-id="1efa6-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1efa6-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="1efa6-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1efa6-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1efa6-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1efa6-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1efa6-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1efa6-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1efa6-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa6-148">Search-Flags</span></span>           | <span data-ttu-id="1efa6-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1efa6-149">0x00000000</span></span>                                                |
| <span data-ttu-id="1efa6-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa6-150">System-Flags</span></span>           | <span data-ttu-id="1efa6-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1efa6-151">0x00000010</span></span>                                                |
| <span data-ttu-id="1efa6-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1efa6-152">Classes used in</span></span>        | [<span data-ttu-id="1efa6-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="1efa6-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1efa6-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1efa6-154">Windows Server 2003</span></span>



| <span data-ttu-id="1efa6-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="1efa6-155">Entry</span></span> | <span data-ttu-id="1efa6-156">Value</span><span class="sxs-lookup"><span data-stu-id="1efa6-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1efa6-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1efa6-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1efa6-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1efa6-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1efa6-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="1efa6-159">System-Only</span></span>            | <span data-ttu-id="1efa6-160">False</span><span class="sxs-lookup"><span data-stu-id="1efa6-160">False</span></span>                                                     |
| <span data-ttu-id="1efa6-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1efa6-161">Is-Single-Valued</span></span>       | <span data-ttu-id="1efa6-162">True</span><span class="sxs-lookup"><span data-stu-id="1efa6-162">True</span></span>                                                      |
| <span data-ttu-id="1efa6-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1efa6-163">Is Indexed</span></span>             | <span data-ttu-id="1efa6-164">False</span><span class="sxs-lookup"><span data-stu-id="1efa6-164">False</span></span>                                                     |
| <span data-ttu-id="1efa6-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1efa6-165">In Global Catalog</span></span>      | <span data-ttu-id="1efa6-166">False</span><span class="sxs-lookup"><span data-stu-id="1efa6-166">False</span></span>                                                     |
| <span data-ttu-id="1efa6-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1efa6-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="1efa6-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1efa6-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1efa6-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1efa6-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1efa6-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1efa6-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1efa6-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa6-171">Search-Flags</span></span>           | <span data-ttu-id="1efa6-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1efa6-172">0x00000000</span></span>                                                |
| <span data-ttu-id="1efa6-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa6-173">System-Flags</span></span>           | <span data-ttu-id="1efa6-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1efa6-174">0x00000010</span></span>                                                |
| <span data-ttu-id="1efa6-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1efa6-175">Classes used in</span></span>        | [<span data-ttu-id="1efa6-176">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="1efa6-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1efa6-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1efa6-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1efa6-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="1efa6-178">Entry</span></span> | <span data-ttu-id="1efa6-179">Value</span><span class="sxs-lookup"><span data-stu-id="1efa6-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1efa6-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1efa6-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1efa6-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1efa6-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1efa6-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="1efa6-182">System-Only</span></span>            | <span data-ttu-id="1efa6-183">False</span><span class="sxs-lookup"><span data-stu-id="1efa6-183">False</span></span>                                                     |
| <span data-ttu-id="1efa6-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1efa6-184">Is-Single-Valued</span></span>       | <span data-ttu-id="1efa6-185">True</span><span class="sxs-lookup"><span data-stu-id="1efa6-185">True</span></span>                                                      |
| <span data-ttu-id="1efa6-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1efa6-186">Is Indexed</span></span>             | <span data-ttu-id="1efa6-187">False</span><span class="sxs-lookup"><span data-stu-id="1efa6-187">False</span></span>                                                     |
| <span data-ttu-id="1efa6-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1efa6-188">In Global Catalog</span></span>      | <span data-ttu-id="1efa6-189">False</span><span class="sxs-lookup"><span data-stu-id="1efa6-189">False</span></span>                                                     |
| <span data-ttu-id="1efa6-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1efa6-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="1efa6-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1efa6-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1efa6-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1efa6-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1efa6-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1efa6-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1efa6-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa6-194">Search-Flags</span></span>           | <span data-ttu-id="1efa6-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1efa6-195">0x00000000</span></span>                                                |
| <span data-ttu-id="1efa6-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa6-196">System-Flags</span></span>           | <span data-ttu-id="1efa6-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1efa6-197">0x00000010</span></span>                                                |
| <span data-ttu-id="1efa6-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1efa6-198">Classes used in</span></span>        | [<span data-ttu-id="1efa6-199">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="1efa6-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1efa6-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1efa6-200">Windows Server 2008</span></span>



| <span data-ttu-id="1efa6-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="1efa6-201">Entry</span></span> | <span data-ttu-id="1efa6-202">Value</span><span class="sxs-lookup"><span data-stu-id="1efa6-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1efa6-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1efa6-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1efa6-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1efa6-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1efa6-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="1efa6-205">System-Only</span></span>            | <span data-ttu-id="1efa6-206">False</span><span class="sxs-lookup"><span data-stu-id="1efa6-206">False</span></span>                                                     |
| <span data-ttu-id="1efa6-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1efa6-207">Is-Single-Valued</span></span>       | <span data-ttu-id="1efa6-208">True</span><span class="sxs-lookup"><span data-stu-id="1efa6-208">True</span></span>                                                      |
| <span data-ttu-id="1efa6-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1efa6-209">Is Indexed</span></span>             | <span data-ttu-id="1efa6-210">False</span><span class="sxs-lookup"><span data-stu-id="1efa6-210">False</span></span>                                                     |
| <span data-ttu-id="1efa6-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1efa6-211">In Global Catalog</span></span>      | <span data-ttu-id="1efa6-212">False</span><span class="sxs-lookup"><span data-stu-id="1efa6-212">False</span></span>                                                     |
| <span data-ttu-id="1efa6-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1efa6-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="1efa6-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1efa6-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1efa6-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1efa6-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1efa6-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1efa6-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1efa6-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa6-217">Search-Flags</span></span>           | <span data-ttu-id="1efa6-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1efa6-218">0x00000000</span></span>                                                |
| <span data-ttu-id="1efa6-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa6-219">System-Flags</span></span>           | <span data-ttu-id="1efa6-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1efa6-220">0x00000010</span></span>                                                |
| <span data-ttu-id="1efa6-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1efa6-221">Classes used in</span></span>        | [<span data-ttu-id="1efa6-222">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="1efa6-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1efa6-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1efa6-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1efa6-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="1efa6-224">Entry</span></span> | <span data-ttu-id="1efa6-225">Value</span><span class="sxs-lookup"><span data-stu-id="1efa6-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1efa6-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1efa6-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1efa6-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1efa6-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1efa6-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="1efa6-228">System-Only</span></span>            | <span data-ttu-id="1efa6-229">False</span><span class="sxs-lookup"><span data-stu-id="1efa6-229">False</span></span>                                                     |
| <span data-ttu-id="1efa6-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1efa6-230">Is-Single-Valued</span></span>       | <span data-ttu-id="1efa6-231">True</span><span class="sxs-lookup"><span data-stu-id="1efa6-231">True</span></span>                                                      |
| <span data-ttu-id="1efa6-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1efa6-232">Is Indexed</span></span>             | <span data-ttu-id="1efa6-233">False</span><span class="sxs-lookup"><span data-stu-id="1efa6-233">False</span></span>                                                     |
| <span data-ttu-id="1efa6-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1efa6-234">In Global Catalog</span></span>      | <span data-ttu-id="1efa6-235">False</span><span class="sxs-lookup"><span data-stu-id="1efa6-235">False</span></span>                                                     |
| <span data-ttu-id="1efa6-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1efa6-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="1efa6-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1efa6-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1efa6-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1efa6-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1efa6-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1efa6-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1efa6-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa6-240">Search-Flags</span></span>           | <span data-ttu-id="1efa6-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1efa6-241">0x00000000</span></span>                                                |
| <span data-ttu-id="1efa6-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa6-242">System-Flags</span></span>           | <span data-ttu-id="1efa6-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1efa6-243">0x00000010</span></span>                                                |
| <span data-ttu-id="1efa6-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1efa6-244">Classes used in</span></span>        | [<span data-ttu-id="1efa6-245">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="1efa6-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1efa6-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1efa6-246">Windows Server 2012</span></span>



| <span data-ttu-id="1efa6-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="1efa6-247">Entry</span></span> | <span data-ttu-id="1efa6-248">Value</span><span class="sxs-lookup"><span data-stu-id="1efa6-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1efa6-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1efa6-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1efa6-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1efa6-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1efa6-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="1efa6-251">System-Only</span></span>            | <span data-ttu-id="1efa6-252">False</span><span class="sxs-lookup"><span data-stu-id="1efa6-252">False</span></span>                                                     |
| <span data-ttu-id="1efa6-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1efa6-253">Is-Single-Valued</span></span>       | <span data-ttu-id="1efa6-254">True</span><span class="sxs-lookup"><span data-stu-id="1efa6-254">True</span></span>                                                      |
| <span data-ttu-id="1efa6-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1efa6-255">Is Indexed</span></span>             | <span data-ttu-id="1efa6-256">False</span><span class="sxs-lookup"><span data-stu-id="1efa6-256">False</span></span>                                                     |
| <span data-ttu-id="1efa6-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1efa6-257">In Global Catalog</span></span>      | <span data-ttu-id="1efa6-258">False</span><span class="sxs-lookup"><span data-stu-id="1efa6-258">False</span></span>                                                     |
| <span data-ttu-id="1efa6-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1efa6-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="1efa6-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1efa6-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1efa6-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1efa6-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1efa6-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1efa6-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1efa6-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa6-263">Search-Flags</span></span>           | <span data-ttu-id="1efa6-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1efa6-264">0x00000000</span></span>                                                |
| <span data-ttu-id="1efa6-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa6-265">System-Flags</span></span>           | <span data-ttu-id="1efa6-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1efa6-266">0x00000010</span></span>                                                |
| <span data-ttu-id="1efa6-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1efa6-267">Classes used in</span></span>        | [<span data-ttu-id="1efa6-268">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="1efa6-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





