---
title: Atributo FRS-File-Filter
description: Una lista de extensiones de nombre de archivo excluidas de la replicación de archivos.
ms.assetid: 094a393a-9e1a-4da8-a38a-161102f164fd
ms.tgt_platform: multiple
keywords:
- El esquema de AD de atributos de filtro de archivos de FRS
- fRSFileFilter esquema de AD de atributos
topic_type:
- apiref
api_name:
- FRS-File-Filter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234cf7d6e56e84c2ed9578fc56036e581a2f0ad2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658534"
---
# <a name="frs-file-filter-attribute"></a><span data-ttu-id="f4537-105">Atributo FRS-File-Filter</span><span class="sxs-lookup"><span data-stu-id="f4537-105">FRS-File-Filter attribute</span></span>

<span data-ttu-id="f4537-106">Una lista de extensiones de nombre de archivo excluidas de la replicación de archivos.</span><span class="sxs-lookup"><span data-stu-id="f4537-106">A list of file name extensions excluded from file replication.</span></span>



| <span data-ttu-id="f4537-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f4537-107">Entry</span></span> | <span data-ttu-id="f4537-108">Value</span><span class="sxs-lookup"><span data-stu-id="f4537-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f4537-109">CN</span><span class="sxs-lookup"><span data-stu-id="f4537-109">CN</span></span>                | <span data-ttu-id="f4537-110">Filtro de archivos de FRS</span><span class="sxs-lookup"><span data-stu-id="f4537-110">FRS-File-Filter</span></span>                             |
| <span data-ttu-id="f4537-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="f4537-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f4537-112">fRSFileFilter</span><span class="sxs-lookup"><span data-stu-id="f4537-112">fRSFileFilter</span></span>                               |
| <span data-ttu-id="f4537-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f4537-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="f4537-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="f4537-114">Update Privilege</span></span>  | <span data-ttu-id="f4537-115">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="f4537-115">Domain administrator</span></span>                        |
| <span data-ttu-id="f4537-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="f4537-116">Update Frequency</span></span>  | <span data-ttu-id="f4537-117">Cuando se configura la replicación.</span><span class="sxs-lookup"><span data-stu-id="f4537-117">When replication is setup.</span></span>                  |
| <span data-ttu-id="f4537-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f4537-118">Attribute-Id</span></span>      | <span data-ttu-id="f4537-119">1.2.840.113556.1.4.483</span><span class="sxs-lookup"><span data-stu-id="f4537-119">1.2.840.113556.1.4.483</span></span>                      |
| <span data-ttu-id="f4537-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f4537-120">System-Id-Guid</span></span>    | <span data-ttu-id="f4537-121">1be8f170-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="f4537-121">1be8f170-a9ff-11d0-afe2-00c04fd930c9</span></span>        |
| <span data-ttu-id="f4537-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4537-122">Syntax</span></span>            | [<span data-ttu-id="f4537-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f4537-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f4537-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="f4537-124">Implementations</span></span>

-   [<span data-ttu-id="f4537-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f4537-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f4537-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f4537-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f4537-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f4537-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f4537-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f4537-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f4537-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f4537-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f4537-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f4537-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f4537-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f4537-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f4537-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="f4537-132">Entry</span></span> | <span data-ttu-id="f4537-133">Value</span><span class="sxs-lookup"><span data-stu-id="f4537-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f4537-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f4537-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f4537-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4537-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f4537-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4537-136">System-Only</span></span>            | <span data-ttu-id="f4537-137">False</span><span class="sxs-lookup"><span data-stu-id="f4537-137">False</span></span>                                                     |
| <span data-ttu-id="f4537-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f4537-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f4537-139">True</span><span class="sxs-lookup"><span data-stu-id="f4537-139">True</span></span>                                                      |
| <span data-ttu-id="f4537-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f4537-140">Is Indexed</span></span>             | <span data-ttu-id="f4537-141">False</span><span class="sxs-lookup"><span data-stu-id="f4537-141">False</span></span>                                                     |
| <span data-ttu-id="f4537-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f4537-142">In Global Catalog</span></span>      | <span data-ttu-id="f4537-143">False</span><span class="sxs-lookup"><span data-stu-id="f4537-143">False</span></span>                                                     |
| <span data-ttu-id="f4537-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f4537-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4537-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f4537-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f4537-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4537-146">Range-Lower</span></span>            | <span data-ttu-id="f4537-147">0</span><span class="sxs-lookup"><span data-stu-id="f4537-147">0</span></span>                                                         |
| <span data-ttu-id="f4537-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4537-148">Range-Upper</span></span>            | <span data-ttu-id="f4537-149">2048</span><span class="sxs-lookup"><span data-stu-id="f4537-149">2048</span></span>                                                      |
| <span data-ttu-id="f4537-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4537-150">Search-Flags</span></span>           | <span data-ttu-id="f4537-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4537-151">0x00000000</span></span>                                                |
| <span data-ttu-id="f4537-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4537-152">System-Flags</span></span>           | <span data-ttu-id="f4537-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4537-153">0x00000010</span></span>                                                |
| <span data-ttu-id="f4537-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f4537-154">Classes used in</span></span>        | [<span data-ttu-id="f4537-155">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="f4537-155">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f4537-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f4537-156">Windows Server 2003</span></span>



| <span data-ttu-id="f4537-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="f4537-157">Entry</span></span> | <span data-ttu-id="f4537-158">Value</span><span class="sxs-lookup"><span data-stu-id="f4537-158">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f4537-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f4537-159">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f4537-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4537-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f4537-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4537-161">System-Only</span></span>            | <span data-ttu-id="f4537-162">False</span><span class="sxs-lookup"><span data-stu-id="f4537-162">False</span></span>                                                     |
| <span data-ttu-id="f4537-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f4537-163">Is-Single-Valued</span></span>       | <span data-ttu-id="f4537-164">True</span><span class="sxs-lookup"><span data-stu-id="f4537-164">True</span></span>                                                      |
| <span data-ttu-id="f4537-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f4537-165">Is Indexed</span></span>             | <span data-ttu-id="f4537-166">False</span><span class="sxs-lookup"><span data-stu-id="f4537-166">False</span></span>                                                     |
| <span data-ttu-id="f4537-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f4537-167">In Global Catalog</span></span>      | <span data-ttu-id="f4537-168">False</span><span class="sxs-lookup"><span data-stu-id="f4537-168">False</span></span>                                                     |
| <span data-ttu-id="f4537-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f4537-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4537-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f4537-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f4537-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4537-171">Range-Lower</span></span>            | <span data-ttu-id="f4537-172">0</span><span class="sxs-lookup"><span data-stu-id="f4537-172">0</span></span>                                                         |
| <span data-ttu-id="f4537-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4537-173">Range-Upper</span></span>            | <span data-ttu-id="f4537-174">2048</span><span class="sxs-lookup"><span data-stu-id="f4537-174">2048</span></span>                                                      |
| <span data-ttu-id="f4537-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4537-175">Search-Flags</span></span>           | <span data-ttu-id="f4537-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4537-176">0x00000000</span></span>                                                |
| <span data-ttu-id="f4537-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4537-177">System-Flags</span></span>           | <span data-ttu-id="f4537-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4537-178">0x00000010</span></span>                                                |
| <span data-ttu-id="f4537-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f4537-179">Classes used in</span></span>        | [<span data-ttu-id="f4537-180">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="f4537-180">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f4537-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f4537-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f4537-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="f4537-182">Entry</span></span> | <span data-ttu-id="f4537-183">Value</span><span class="sxs-lookup"><span data-stu-id="f4537-183">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f4537-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f4537-184">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f4537-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4537-185">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f4537-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4537-186">System-Only</span></span>            | <span data-ttu-id="f4537-187">False</span><span class="sxs-lookup"><span data-stu-id="f4537-187">False</span></span>                                                     |
| <span data-ttu-id="f4537-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f4537-188">Is-Single-Valued</span></span>       | <span data-ttu-id="f4537-189">True</span><span class="sxs-lookup"><span data-stu-id="f4537-189">True</span></span>                                                      |
| <span data-ttu-id="f4537-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f4537-190">Is Indexed</span></span>             | <span data-ttu-id="f4537-191">False</span><span class="sxs-lookup"><span data-stu-id="f4537-191">False</span></span>                                                     |
| <span data-ttu-id="f4537-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f4537-192">In Global Catalog</span></span>      | <span data-ttu-id="f4537-193">False</span><span class="sxs-lookup"><span data-stu-id="f4537-193">False</span></span>                                                     |
| <span data-ttu-id="f4537-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f4537-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4537-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f4537-195">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f4537-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4537-196">Range-Lower</span></span>            | <span data-ttu-id="f4537-197">0</span><span class="sxs-lookup"><span data-stu-id="f4537-197">0</span></span>                                                         |
| <span data-ttu-id="f4537-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4537-198">Range-Upper</span></span>            | <span data-ttu-id="f4537-199">2048</span><span class="sxs-lookup"><span data-stu-id="f4537-199">2048</span></span>                                                      |
| <span data-ttu-id="f4537-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4537-200">Search-Flags</span></span>           | <span data-ttu-id="f4537-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4537-201">0x00000000</span></span>                                                |
| <span data-ttu-id="f4537-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4537-202">System-Flags</span></span>           | <span data-ttu-id="f4537-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4537-203">0x00000010</span></span>                                                |
| <span data-ttu-id="f4537-204">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f4537-204">Classes used in</span></span>        | [<span data-ttu-id="f4537-205">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="f4537-205">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f4537-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4537-206">Windows Server 2008</span></span>



| <span data-ttu-id="f4537-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="f4537-207">Entry</span></span> | <span data-ttu-id="f4537-208">Value</span><span class="sxs-lookup"><span data-stu-id="f4537-208">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f4537-209">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f4537-209">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f4537-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4537-210">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f4537-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4537-211">System-Only</span></span>            | <span data-ttu-id="f4537-212">False</span><span class="sxs-lookup"><span data-stu-id="f4537-212">False</span></span>                                                     |
| <span data-ttu-id="f4537-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f4537-213">Is-Single-Valued</span></span>       | <span data-ttu-id="f4537-214">True</span><span class="sxs-lookup"><span data-stu-id="f4537-214">True</span></span>                                                      |
| <span data-ttu-id="f4537-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f4537-215">Is Indexed</span></span>             | <span data-ttu-id="f4537-216">False</span><span class="sxs-lookup"><span data-stu-id="f4537-216">False</span></span>                                                     |
| <span data-ttu-id="f4537-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f4537-217">In Global Catalog</span></span>      | <span data-ttu-id="f4537-218">False</span><span class="sxs-lookup"><span data-stu-id="f4537-218">False</span></span>                                                     |
| <span data-ttu-id="f4537-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f4537-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4537-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f4537-220">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f4537-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4537-221">Range-Lower</span></span>            | <span data-ttu-id="f4537-222">0</span><span class="sxs-lookup"><span data-stu-id="f4537-222">0</span></span>                                                         |
| <span data-ttu-id="f4537-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4537-223">Range-Upper</span></span>            | <span data-ttu-id="f4537-224">2048</span><span class="sxs-lookup"><span data-stu-id="f4537-224">2048</span></span>                                                      |
| <span data-ttu-id="f4537-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4537-225">Search-Flags</span></span>           | <span data-ttu-id="f4537-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4537-226">0x00000000</span></span>                                                |
| <span data-ttu-id="f4537-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4537-227">System-Flags</span></span>           | <span data-ttu-id="f4537-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4537-228">0x00000010</span></span>                                                |
| <span data-ttu-id="f4537-229">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f4537-229">Classes used in</span></span>        | [<span data-ttu-id="f4537-230">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="f4537-230">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f4537-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f4537-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f4537-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="f4537-232">Entry</span></span> | <span data-ttu-id="f4537-233">Value</span><span class="sxs-lookup"><span data-stu-id="f4537-233">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f4537-234">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f4537-234">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f4537-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4537-235">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f4537-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4537-236">System-Only</span></span>            | <span data-ttu-id="f4537-237">False</span><span class="sxs-lookup"><span data-stu-id="f4537-237">False</span></span>                                                     |
| <span data-ttu-id="f4537-238">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f4537-238">Is-Single-Valued</span></span>       | <span data-ttu-id="f4537-239">True</span><span class="sxs-lookup"><span data-stu-id="f4537-239">True</span></span>                                                      |
| <span data-ttu-id="f4537-240">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f4537-240">Is Indexed</span></span>             | <span data-ttu-id="f4537-241">False</span><span class="sxs-lookup"><span data-stu-id="f4537-241">False</span></span>                                                     |
| <span data-ttu-id="f4537-242">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f4537-242">In Global Catalog</span></span>      | <span data-ttu-id="f4537-243">False</span><span class="sxs-lookup"><span data-stu-id="f4537-243">False</span></span>                                                     |
| <span data-ttu-id="f4537-244">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f4537-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4537-245">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f4537-245">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f4537-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4537-246">Range-Lower</span></span>            | <span data-ttu-id="f4537-247">0</span><span class="sxs-lookup"><span data-stu-id="f4537-247">0</span></span>                                                         |
| <span data-ttu-id="f4537-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4537-248">Range-Upper</span></span>            | <span data-ttu-id="f4537-249">2048</span><span class="sxs-lookup"><span data-stu-id="f4537-249">2048</span></span>                                                      |
| <span data-ttu-id="f4537-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4537-250">Search-Flags</span></span>           | <span data-ttu-id="f4537-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4537-251">0x00000000</span></span>                                                |
| <span data-ttu-id="f4537-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4537-252">System-Flags</span></span>           | <span data-ttu-id="f4537-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4537-253">0x00000010</span></span>                                                |
| <span data-ttu-id="f4537-254">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f4537-254">Classes used in</span></span>        | [<span data-ttu-id="f4537-255">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="f4537-255">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f4537-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4537-256">Windows Server 2012</span></span>



| <span data-ttu-id="f4537-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="f4537-257">Entry</span></span> | <span data-ttu-id="f4537-258">Value</span><span class="sxs-lookup"><span data-stu-id="f4537-258">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f4537-259">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f4537-259">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f4537-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4537-260">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f4537-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4537-261">System-Only</span></span>            | <span data-ttu-id="f4537-262">False</span><span class="sxs-lookup"><span data-stu-id="f4537-262">False</span></span>                                                     |
| <span data-ttu-id="f4537-263">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f4537-263">Is-Single-Valued</span></span>       | <span data-ttu-id="f4537-264">True</span><span class="sxs-lookup"><span data-stu-id="f4537-264">True</span></span>                                                      |
| <span data-ttu-id="f4537-265">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f4537-265">Is Indexed</span></span>             | <span data-ttu-id="f4537-266">False</span><span class="sxs-lookup"><span data-stu-id="f4537-266">False</span></span>                                                     |
| <span data-ttu-id="f4537-267">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f4537-267">In Global Catalog</span></span>      | <span data-ttu-id="f4537-268">False</span><span class="sxs-lookup"><span data-stu-id="f4537-268">False</span></span>                                                     |
| <span data-ttu-id="f4537-269">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f4537-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4537-270">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f4537-270">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f4537-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4537-271">Range-Lower</span></span>            | <span data-ttu-id="f4537-272">0</span><span class="sxs-lookup"><span data-stu-id="f4537-272">0</span></span>                                                         |
| <span data-ttu-id="f4537-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4537-273">Range-Upper</span></span>            | <span data-ttu-id="f4537-274">2048</span><span class="sxs-lookup"><span data-stu-id="f4537-274">2048</span></span>                                                      |
| <span data-ttu-id="f4537-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4537-275">Search-Flags</span></span>           | <span data-ttu-id="f4537-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4537-276">0x00000000</span></span>                                                |
| <span data-ttu-id="f4537-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4537-277">System-Flags</span></span>           | <span data-ttu-id="f4537-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4537-278">0x00000010</span></span>                                                |
| <span data-ttu-id="f4537-279">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f4537-279">Classes used in</span></span>        | [<span data-ttu-id="f4537-280">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="f4537-280">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





