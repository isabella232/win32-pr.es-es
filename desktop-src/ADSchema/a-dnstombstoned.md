---
title: DNS-Tombstoned atributo)
description: True si este objeto se ha desechado. Este atributo existe para facilitar y agilizar la búsqueda de registros de marcadores de exclusión. Los objetos de desecho son objetos que se han eliminado pero que todavía no se han quitado del directorio.
ms.assetid: d876a6d7-d5bc-4fe2-af03-1fff3381708f
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de DNS-Tombstoned
- dNSTombstoned esquema de AD de atributos
topic_type:
- apiref
api_name:
- DNS-Tombstoned
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dba61706861b808f28d7f6874a9bfd93d4152c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905840"
---
# <a name="dns-tombstoned-attribute"></a><span data-ttu-id="af62c-107">DNS-Tombstoned atributo)</span><span class="sxs-lookup"><span data-stu-id="af62c-107">DNS-Tombstoned attribute</span></span>

<span data-ttu-id="af62c-108">True si este objeto se ha desechado.</span><span class="sxs-lookup"><span data-stu-id="af62c-108">True if this object has been tombstoned.</span></span> <span data-ttu-id="af62c-109">Este atributo existe para facilitar y agilizar la búsqueda de registros de marcadores de exclusión.</span><span class="sxs-lookup"><span data-stu-id="af62c-109">This attribute exists to make searching for tombstoned records easier and faster.</span></span> <span data-ttu-id="af62c-110">Los objetos de desecho son objetos que se han eliminado pero que todavía no se han quitado del directorio.</span><span class="sxs-lookup"><span data-stu-id="af62c-110">Tombstoned objects are objects that have been deleted but not yet removed from the directory.</span></span>



| <span data-ttu-id="af62c-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="af62c-111">Entry</span></span> | <span data-ttu-id="af62c-112">Value</span><span class="sxs-lookup"><span data-stu-id="af62c-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="af62c-113">CN</span><span class="sxs-lookup"><span data-stu-id="af62c-113">CN</span></span>                | <span data-ttu-id="af62c-114">DNS-Tombstoned</span><span class="sxs-lookup"><span data-stu-id="af62c-114">DNS-Tombstoned</span></span>                       |
| <span data-ttu-id="af62c-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="af62c-115">Ldap-Display-Name</span></span> | <span data-ttu-id="af62c-116">dNSTombstoned</span><span class="sxs-lookup"><span data-stu-id="af62c-116">dNSTombstoned</span></span>                        |
| <span data-ttu-id="af62c-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="af62c-117">Size</span></span>              | <span data-ttu-id="af62c-118">4 bytes</span><span class="sxs-lookup"><span data-stu-id="af62c-118">4 bytes</span></span>                              |
| <span data-ttu-id="af62c-119">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="af62c-119">Update Privilege</span></span>  | <span data-ttu-id="af62c-120">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="af62c-120">This value is set by the system.</span></span>     |
| <span data-ttu-id="af62c-121">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="af62c-121">Update Frequency</span></span>  | <span data-ttu-id="af62c-122">Cada vez que se elimina un objeto.</span><span class="sxs-lookup"><span data-stu-id="af62c-122">Whenever an object is deleted.</span></span>       |
| <span data-ttu-id="af62c-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="af62c-123">Attribute-Id</span></span>      | <span data-ttu-id="af62c-124">1.2.840.113556.1.4.1414</span><span class="sxs-lookup"><span data-stu-id="af62c-124">1.2.840.113556.1.4.1414</span></span>              |
| <span data-ttu-id="af62c-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="af62c-125">System-Id-Guid</span></span>    | <span data-ttu-id="af62c-126">d5eb2eb7-be4e-463b-a214-634a44d7392e</span><span class="sxs-lookup"><span data-stu-id="af62c-126">d5eb2eb7-be4e-463b-a214-634a44d7392e</span></span> |
| <span data-ttu-id="af62c-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af62c-127">Syntax</span></span>            | [<span data-ttu-id="af62c-128">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="af62c-128">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="af62c-129">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="af62c-129">Implementations</span></span>

-   [<span data-ttu-id="af62c-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="af62c-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="af62c-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="af62c-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="af62c-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="af62c-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="af62c-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="af62c-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="af62c-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="af62c-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="af62c-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="af62c-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="af62c-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="af62c-136">Windows 2000 Server</span></span>



| <span data-ttu-id="af62c-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="af62c-137">Entry</span></span> | <span data-ttu-id="af62c-138">Value</span><span class="sxs-lookup"><span data-stu-id="af62c-138">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="af62c-139">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="af62c-139">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="af62c-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af62c-140">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="af62c-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="af62c-141">System-Only</span></span>            | <span data-ttu-id="af62c-142">False</span><span class="sxs-lookup"><span data-stu-id="af62c-142">False</span></span>                                    |
| <span data-ttu-id="af62c-143">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="af62c-143">Is-Single-Valued</span></span>       | <span data-ttu-id="af62c-144">True</span><span class="sxs-lookup"><span data-stu-id="af62c-144">True</span></span>                                     |
| <span data-ttu-id="af62c-145">Está indexado</span><span class="sxs-lookup"><span data-stu-id="af62c-145">Is Indexed</span></span>             | <span data-ttu-id="af62c-146">True</span><span class="sxs-lookup"><span data-stu-id="af62c-146">True</span></span>                                     |
| <span data-ttu-id="af62c-147">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="af62c-147">In Global Catalog</span></span>      | <span data-ttu-id="af62c-148">False</span><span class="sxs-lookup"><span data-stu-id="af62c-148">False</span></span>                                    |
| <span data-ttu-id="af62c-149">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="af62c-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="af62c-150">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af62c-150">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="af62c-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af62c-151">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="af62c-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af62c-152">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="af62c-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af62c-153">Search-Flags</span></span>           | <span data-ttu-id="af62c-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="af62c-154">0x00000001</span></span>                               |
| <span data-ttu-id="af62c-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af62c-155">System-Flags</span></span>           | <span data-ttu-id="af62c-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af62c-156">0x00000010</span></span>                               |
| <span data-ttu-id="af62c-157">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="af62c-157">Classes used in</span></span>        | [<span data-ttu-id="af62c-158">**Nodo DNS**</span><span class="sxs-lookup"><span data-stu-id="af62c-158">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="af62c-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="af62c-159">Windows Server 2003</span></span>



| <span data-ttu-id="af62c-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="af62c-160">Entry</span></span> | <span data-ttu-id="af62c-161">Value</span><span class="sxs-lookup"><span data-stu-id="af62c-161">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="af62c-162">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="af62c-162">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="af62c-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af62c-163">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="af62c-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="af62c-164">System-Only</span></span>            | <span data-ttu-id="af62c-165">False</span><span class="sxs-lookup"><span data-stu-id="af62c-165">False</span></span>                                    |
| <span data-ttu-id="af62c-166">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="af62c-166">Is-Single-Valued</span></span>       | <span data-ttu-id="af62c-167">True</span><span class="sxs-lookup"><span data-stu-id="af62c-167">True</span></span>                                     |
| <span data-ttu-id="af62c-168">Está indexado</span><span class="sxs-lookup"><span data-stu-id="af62c-168">Is Indexed</span></span>             | <span data-ttu-id="af62c-169">True</span><span class="sxs-lookup"><span data-stu-id="af62c-169">True</span></span>                                     |
| <span data-ttu-id="af62c-170">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="af62c-170">In Global Catalog</span></span>      | <span data-ttu-id="af62c-171">False</span><span class="sxs-lookup"><span data-stu-id="af62c-171">False</span></span>                                    |
| <span data-ttu-id="af62c-172">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="af62c-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="af62c-173">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af62c-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="af62c-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af62c-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="af62c-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af62c-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="af62c-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af62c-176">Search-Flags</span></span>           | <span data-ttu-id="af62c-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="af62c-177">0x00000001</span></span>                               |
| <span data-ttu-id="af62c-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af62c-178">System-Flags</span></span>           | <span data-ttu-id="af62c-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af62c-179">0x00000010</span></span>                               |
| <span data-ttu-id="af62c-180">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="af62c-180">Classes used in</span></span>        | [<span data-ttu-id="af62c-181">**Nodo DNS**</span><span class="sxs-lookup"><span data-stu-id="af62c-181">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="af62c-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="af62c-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="af62c-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="af62c-183">Entry</span></span> | <span data-ttu-id="af62c-184">Value</span><span class="sxs-lookup"><span data-stu-id="af62c-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="af62c-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="af62c-185">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="af62c-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af62c-186">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="af62c-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="af62c-187">System-Only</span></span>            | <span data-ttu-id="af62c-188">False</span><span class="sxs-lookup"><span data-stu-id="af62c-188">False</span></span>                                    |
| <span data-ttu-id="af62c-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="af62c-189">Is-Single-Valued</span></span>       | <span data-ttu-id="af62c-190">True</span><span class="sxs-lookup"><span data-stu-id="af62c-190">True</span></span>                                     |
| <span data-ttu-id="af62c-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="af62c-191">Is Indexed</span></span>             | <span data-ttu-id="af62c-192">True</span><span class="sxs-lookup"><span data-stu-id="af62c-192">True</span></span>                                     |
| <span data-ttu-id="af62c-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="af62c-193">In Global Catalog</span></span>      | <span data-ttu-id="af62c-194">False</span><span class="sxs-lookup"><span data-stu-id="af62c-194">False</span></span>                                    |
| <span data-ttu-id="af62c-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="af62c-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="af62c-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af62c-196">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="af62c-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af62c-197">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="af62c-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af62c-198">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="af62c-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af62c-199">Search-Flags</span></span>           | <span data-ttu-id="af62c-200">0x00000001</span><span class="sxs-lookup"><span data-stu-id="af62c-200">0x00000001</span></span>                               |
| <span data-ttu-id="af62c-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af62c-201">System-Flags</span></span>           | <span data-ttu-id="af62c-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af62c-202">0x00000010</span></span>                               |
| <span data-ttu-id="af62c-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="af62c-203">Classes used in</span></span>        | [<span data-ttu-id="af62c-204">**Nodo DNS**</span><span class="sxs-lookup"><span data-stu-id="af62c-204">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="af62c-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af62c-205">Windows Server 2008</span></span>



| <span data-ttu-id="af62c-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="af62c-206">Entry</span></span> | <span data-ttu-id="af62c-207">Value</span><span class="sxs-lookup"><span data-stu-id="af62c-207">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="af62c-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="af62c-208">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="af62c-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af62c-209">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="af62c-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="af62c-210">System-Only</span></span>            | <span data-ttu-id="af62c-211">False</span><span class="sxs-lookup"><span data-stu-id="af62c-211">False</span></span>                                    |
| <span data-ttu-id="af62c-212">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="af62c-212">Is-Single-Valued</span></span>       | <span data-ttu-id="af62c-213">True</span><span class="sxs-lookup"><span data-stu-id="af62c-213">True</span></span>                                     |
| <span data-ttu-id="af62c-214">Está indexado</span><span class="sxs-lookup"><span data-stu-id="af62c-214">Is Indexed</span></span>             | <span data-ttu-id="af62c-215">True</span><span class="sxs-lookup"><span data-stu-id="af62c-215">True</span></span>                                     |
| <span data-ttu-id="af62c-216">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="af62c-216">In Global Catalog</span></span>      | <span data-ttu-id="af62c-217">False</span><span class="sxs-lookup"><span data-stu-id="af62c-217">False</span></span>                                    |
| <span data-ttu-id="af62c-218">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="af62c-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="af62c-219">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af62c-219">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="af62c-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af62c-220">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="af62c-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af62c-221">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="af62c-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af62c-222">Search-Flags</span></span>           | <span data-ttu-id="af62c-223">0x00000001</span><span class="sxs-lookup"><span data-stu-id="af62c-223">0x00000001</span></span>                               |
| <span data-ttu-id="af62c-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af62c-224">System-Flags</span></span>           | <span data-ttu-id="af62c-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af62c-225">0x00000010</span></span>                               |
| <span data-ttu-id="af62c-226">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="af62c-226">Classes used in</span></span>        | [<span data-ttu-id="af62c-227">**Nodo DNS**</span><span class="sxs-lookup"><span data-stu-id="af62c-227">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="af62c-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="af62c-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="af62c-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="af62c-229">Entry</span></span> | <span data-ttu-id="af62c-230">Value</span><span class="sxs-lookup"><span data-stu-id="af62c-230">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="af62c-231">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="af62c-231">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="af62c-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af62c-232">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="af62c-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="af62c-233">System-Only</span></span>            | <span data-ttu-id="af62c-234">False</span><span class="sxs-lookup"><span data-stu-id="af62c-234">False</span></span>                                    |
| <span data-ttu-id="af62c-235">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="af62c-235">Is-Single-Valued</span></span>       | <span data-ttu-id="af62c-236">True</span><span class="sxs-lookup"><span data-stu-id="af62c-236">True</span></span>                                     |
| <span data-ttu-id="af62c-237">Está indexado</span><span class="sxs-lookup"><span data-stu-id="af62c-237">Is Indexed</span></span>             | <span data-ttu-id="af62c-238">True</span><span class="sxs-lookup"><span data-stu-id="af62c-238">True</span></span>                                     |
| <span data-ttu-id="af62c-239">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="af62c-239">In Global Catalog</span></span>      | <span data-ttu-id="af62c-240">False</span><span class="sxs-lookup"><span data-stu-id="af62c-240">False</span></span>                                    |
| <span data-ttu-id="af62c-241">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="af62c-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="af62c-242">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af62c-242">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="af62c-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af62c-243">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="af62c-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af62c-244">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="af62c-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af62c-245">Search-Flags</span></span>           | <span data-ttu-id="af62c-246">0x00000001</span><span class="sxs-lookup"><span data-stu-id="af62c-246">0x00000001</span></span>                               |
| <span data-ttu-id="af62c-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af62c-247">System-Flags</span></span>           | <span data-ttu-id="af62c-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af62c-248">0x00000010</span></span>                               |
| <span data-ttu-id="af62c-249">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="af62c-249">Classes used in</span></span>        | [<span data-ttu-id="af62c-250">**Nodo DNS**</span><span class="sxs-lookup"><span data-stu-id="af62c-250">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="af62c-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="af62c-251">Windows Server 2012</span></span>



| <span data-ttu-id="af62c-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="af62c-252">Entry</span></span> | <span data-ttu-id="af62c-253">Value</span><span class="sxs-lookup"><span data-stu-id="af62c-253">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="af62c-254">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="af62c-254">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="af62c-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af62c-255">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="af62c-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="af62c-256">System-Only</span></span>            | <span data-ttu-id="af62c-257">False</span><span class="sxs-lookup"><span data-stu-id="af62c-257">False</span></span>                                    |
| <span data-ttu-id="af62c-258">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="af62c-258">Is-Single-Valued</span></span>       | <span data-ttu-id="af62c-259">True</span><span class="sxs-lookup"><span data-stu-id="af62c-259">True</span></span>                                     |
| <span data-ttu-id="af62c-260">Está indexado</span><span class="sxs-lookup"><span data-stu-id="af62c-260">Is Indexed</span></span>             | <span data-ttu-id="af62c-261">True</span><span class="sxs-lookup"><span data-stu-id="af62c-261">True</span></span>                                     |
| <span data-ttu-id="af62c-262">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="af62c-262">In Global Catalog</span></span>      | <span data-ttu-id="af62c-263">False</span><span class="sxs-lookup"><span data-stu-id="af62c-263">False</span></span>                                    |
| <span data-ttu-id="af62c-264">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="af62c-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="af62c-265">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af62c-265">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="af62c-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af62c-266">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="af62c-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af62c-267">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="af62c-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af62c-268">Search-Flags</span></span>           | <span data-ttu-id="af62c-269">0x00000001</span><span class="sxs-lookup"><span data-stu-id="af62c-269">0x00000001</span></span>                               |
| <span data-ttu-id="af62c-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af62c-270">System-Flags</span></span>           | <span data-ttu-id="af62c-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af62c-271">0x00000010</span></span>                               |
| <span data-ttu-id="af62c-272">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="af62c-272">Classes used in</span></span>        | [<span data-ttu-id="af62c-273">**Nodo DNS**</span><span class="sxs-lookup"><span data-stu-id="af62c-273">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



 

 





