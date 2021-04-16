---
title: DNS-Property atributo)
description: Se usa para almacenar la configuración binaria (propiedades) en objetos de zona DNS.
ms.assetid: 55ea38cd-6b5b-4500-8e68-ae4d35e4b177
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de DNS-Property
- dNSProperty esquema de AD de atributos
topic_type:
- apiref
api_name:
- DNS-Property
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f8fd18f4524ec0bf61a609d21a361668ed295b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658555"
---
# <a name="dns-property-attribute"></a><span data-ttu-id="92626-105">DNS-Property atributo)</span><span class="sxs-lookup"><span data-stu-id="92626-105">DNS-Property attribute</span></span>

<span data-ttu-id="92626-106">Se usa para almacenar la configuración binaria (propiedades) en objetos de zona DNS.</span><span class="sxs-lookup"><span data-stu-id="92626-106">Used to store binary settings (properties) on DNS zone objects.</span></span>



| <span data-ttu-id="92626-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="92626-107">Entry</span></span> | <span data-ttu-id="92626-108">Value</span><span class="sxs-lookup"><span data-stu-id="92626-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="92626-109">CN</span><span class="sxs-lookup"><span data-stu-id="92626-109">CN</span></span>                | <span data-ttu-id="92626-110">DNS-Property</span><span class="sxs-lookup"><span data-stu-id="92626-110">DNS-Property</span></span>                                          |
| <span data-ttu-id="92626-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="92626-111">Ldap-Display-Name</span></span> | <span data-ttu-id="92626-112">dNSProperty</span><span class="sxs-lookup"><span data-stu-id="92626-112">dNSProperty</span></span>                                           |
| <span data-ttu-id="92626-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="92626-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="92626-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="92626-114">Update Privilege</span></span>  | <span data-ttu-id="92626-115">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="92626-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="92626-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="92626-116">Update Frequency</span></span>  | <span data-ttu-id="92626-117">Cada vez que se modifican los registros de la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="92626-117">Whenever DNS zone records change.</span></span>                     |
| <span data-ttu-id="92626-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="92626-118">Attribute-Id</span></span>      | <span data-ttu-id="92626-119">1.2.840.113556.1.4.1306</span><span class="sxs-lookup"><span data-stu-id="92626-119">1.2.840.113556.1.4.1306</span></span>                               |
| <span data-ttu-id="92626-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="92626-120">System-Id-Guid</span></span>    | <span data-ttu-id="92626-121">675a15fe-3b70-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="92626-121">675a15fe-3b70-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="92626-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92626-122">Syntax</span></span>            | [<span data-ttu-id="92626-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="92626-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="92626-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="92626-124">Implementations</span></span>

-   [<span data-ttu-id="92626-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="92626-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="92626-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="92626-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="92626-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="92626-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="92626-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="92626-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="92626-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="92626-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="92626-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="92626-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="92626-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="92626-131">Windows 2000 Server</span></span>



| <span data-ttu-id="92626-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="92626-132">Entry</span></span> | <span data-ttu-id="92626-133">Value</span><span class="sxs-lookup"><span data-stu-id="92626-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="92626-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="92626-134">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="92626-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92626-135">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="92626-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="92626-136">System-Only</span></span>            | <span data-ttu-id="92626-137">False</span><span class="sxs-lookup"><span data-stu-id="92626-137">False</span></span>                                                                             |
| <span data-ttu-id="92626-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="92626-138">Is-Single-Valued</span></span>       | <span data-ttu-id="92626-139">False</span><span class="sxs-lookup"><span data-stu-id="92626-139">False</span></span>                                                                             |
| <span data-ttu-id="92626-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="92626-140">Is Indexed</span></span>             | <span data-ttu-id="92626-141">False</span><span class="sxs-lookup"><span data-stu-id="92626-141">False</span></span>                                                                             |
| <span data-ttu-id="92626-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="92626-142">In Global Catalog</span></span>      | <span data-ttu-id="92626-143">False</span><span class="sxs-lookup"><span data-stu-id="92626-143">False</span></span>                                                                             |
| <span data-ttu-id="92626-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="92626-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="92626-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92626-145">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="92626-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92626-146">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="92626-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92626-147">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="92626-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92626-148">Search-Flags</span></span>           | <span data-ttu-id="92626-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92626-149">0x00000000</span></span>                                                                        |
| <span data-ttu-id="92626-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92626-150">System-Flags</span></span>           | <span data-ttu-id="92626-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92626-151">0x00000010</span></span>                                                                        |
| <span data-ttu-id="92626-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="92626-152">Classes used in</span></span>        | [<span data-ttu-id="92626-153">**Nodo DNS**</span><span class="sxs-lookup"><span data-stu-id="92626-153">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="92626-154">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="92626-154">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="92626-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="92626-155">Windows Server 2003</span></span>



| <span data-ttu-id="92626-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="92626-156">Entry</span></span> | <span data-ttu-id="92626-157">Value</span><span class="sxs-lookup"><span data-stu-id="92626-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="92626-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="92626-158">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="92626-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92626-159">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="92626-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="92626-160">System-Only</span></span>            | <span data-ttu-id="92626-161">False</span><span class="sxs-lookup"><span data-stu-id="92626-161">False</span></span>                                                                             |
| <span data-ttu-id="92626-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="92626-162">Is-Single-Valued</span></span>       | <span data-ttu-id="92626-163">False</span><span class="sxs-lookup"><span data-stu-id="92626-163">False</span></span>                                                                             |
| <span data-ttu-id="92626-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="92626-164">Is Indexed</span></span>             | <span data-ttu-id="92626-165">False</span><span class="sxs-lookup"><span data-stu-id="92626-165">False</span></span>                                                                             |
| <span data-ttu-id="92626-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="92626-166">In Global Catalog</span></span>      | <span data-ttu-id="92626-167">False</span><span class="sxs-lookup"><span data-stu-id="92626-167">False</span></span>                                                                             |
| <span data-ttu-id="92626-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="92626-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="92626-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92626-169">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="92626-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92626-170">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="92626-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92626-171">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="92626-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92626-172">Search-Flags</span></span>           | <span data-ttu-id="92626-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92626-173">0x00000000</span></span>                                                                        |
| <span data-ttu-id="92626-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92626-174">System-Flags</span></span>           | <span data-ttu-id="92626-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92626-175">0x00000010</span></span>                                                                        |
| <span data-ttu-id="92626-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="92626-176">Classes used in</span></span>        | [<span data-ttu-id="92626-177">**Nodo DNS**</span><span class="sxs-lookup"><span data-stu-id="92626-177">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="92626-178">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="92626-178">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="92626-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="92626-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="92626-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="92626-180">Entry</span></span> | <span data-ttu-id="92626-181">Value</span><span class="sxs-lookup"><span data-stu-id="92626-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="92626-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="92626-182">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="92626-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92626-183">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="92626-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="92626-184">System-Only</span></span>            | <span data-ttu-id="92626-185">False</span><span class="sxs-lookup"><span data-stu-id="92626-185">False</span></span>                                                                             |
| <span data-ttu-id="92626-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="92626-186">Is-Single-Valued</span></span>       | <span data-ttu-id="92626-187">False</span><span class="sxs-lookup"><span data-stu-id="92626-187">False</span></span>                                                                             |
| <span data-ttu-id="92626-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="92626-188">Is Indexed</span></span>             | <span data-ttu-id="92626-189">False</span><span class="sxs-lookup"><span data-stu-id="92626-189">False</span></span>                                                                             |
| <span data-ttu-id="92626-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="92626-190">In Global Catalog</span></span>      | <span data-ttu-id="92626-191">False</span><span class="sxs-lookup"><span data-stu-id="92626-191">False</span></span>                                                                             |
| <span data-ttu-id="92626-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="92626-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="92626-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92626-193">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="92626-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92626-194">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="92626-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92626-195">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="92626-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92626-196">Search-Flags</span></span>           | <span data-ttu-id="92626-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92626-197">0x00000000</span></span>                                                                        |
| <span data-ttu-id="92626-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92626-198">System-Flags</span></span>           | <span data-ttu-id="92626-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92626-199">0x00000010</span></span>                                                                        |
| <span data-ttu-id="92626-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="92626-200">Classes used in</span></span>        | [<span data-ttu-id="92626-201">**Nodo DNS**</span><span class="sxs-lookup"><span data-stu-id="92626-201">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="92626-202">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="92626-202">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="92626-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92626-203">Windows Server 2008</span></span>



| <span data-ttu-id="92626-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="92626-204">Entry</span></span> | <span data-ttu-id="92626-205">Value</span><span class="sxs-lookup"><span data-stu-id="92626-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="92626-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="92626-206">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="92626-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92626-207">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="92626-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="92626-208">System-Only</span></span>            | <span data-ttu-id="92626-209">False</span><span class="sxs-lookup"><span data-stu-id="92626-209">False</span></span>                                                                             |
| <span data-ttu-id="92626-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="92626-210">Is-Single-Valued</span></span>       | <span data-ttu-id="92626-211">False</span><span class="sxs-lookup"><span data-stu-id="92626-211">False</span></span>                                                                             |
| <span data-ttu-id="92626-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="92626-212">Is Indexed</span></span>             | <span data-ttu-id="92626-213">False</span><span class="sxs-lookup"><span data-stu-id="92626-213">False</span></span>                                                                             |
| <span data-ttu-id="92626-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="92626-214">In Global Catalog</span></span>      | <span data-ttu-id="92626-215">False</span><span class="sxs-lookup"><span data-stu-id="92626-215">False</span></span>                                                                             |
| <span data-ttu-id="92626-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="92626-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="92626-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92626-217">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="92626-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92626-218">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="92626-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92626-219">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="92626-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92626-220">Search-Flags</span></span>           | <span data-ttu-id="92626-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92626-221">0x00000000</span></span>                                                                        |
| <span data-ttu-id="92626-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92626-222">System-Flags</span></span>           | <span data-ttu-id="92626-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92626-223">0x00000010</span></span>                                                                        |
| <span data-ttu-id="92626-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="92626-224">Classes used in</span></span>        | [<span data-ttu-id="92626-225">**Nodo DNS**</span><span class="sxs-lookup"><span data-stu-id="92626-225">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="92626-226">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="92626-226">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="92626-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="92626-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="92626-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="92626-228">Entry</span></span> | <span data-ttu-id="92626-229">Value</span><span class="sxs-lookup"><span data-stu-id="92626-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="92626-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="92626-230">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="92626-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92626-231">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="92626-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="92626-232">System-Only</span></span>            | <span data-ttu-id="92626-233">False</span><span class="sxs-lookup"><span data-stu-id="92626-233">False</span></span>                                                                             |
| <span data-ttu-id="92626-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="92626-234">Is-Single-Valued</span></span>       | <span data-ttu-id="92626-235">False</span><span class="sxs-lookup"><span data-stu-id="92626-235">False</span></span>                                                                             |
| <span data-ttu-id="92626-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="92626-236">Is Indexed</span></span>             | <span data-ttu-id="92626-237">False</span><span class="sxs-lookup"><span data-stu-id="92626-237">False</span></span>                                                                             |
| <span data-ttu-id="92626-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="92626-238">In Global Catalog</span></span>      | <span data-ttu-id="92626-239">False</span><span class="sxs-lookup"><span data-stu-id="92626-239">False</span></span>                                                                             |
| <span data-ttu-id="92626-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="92626-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="92626-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92626-241">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="92626-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92626-242">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="92626-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92626-243">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="92626-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92626-244">Search-Flags</span></span>           | <span data-ttu-id="92626-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92626-245">0x00000000</span></span>                                                                        |
| <span data-ttu-id="92626-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92626-246">System-Flags</span></span>           | <span data-ttu-id="92626-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92626-247">0x00000010</span></span>                                                                        |
| <span data-ttu-id="92626-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="92626-248">Classes used in</span></span>        | [<span data-ttu-id="92626-249">**Nodo DNS**</span><span class="sxs-lookup"><span data-stu-id="92626-249">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="92626-250">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="92626-250">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="92626-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="92626-251">Windows Server 2012</span></span>



| <span data-ttu-id="92626-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="92626-252">Entry</span></span> | <span data-ttu-id="92626-253">Value</span><span class="sxs-lookup"><span data-stu-id="92626-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="92626-254">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="92626-254">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="92626-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92626-255">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="92626-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="92626-256">System-Only</span></span>            | <span data-ttu-id="92626-257">False</span><span class="sxs-lookup"><span data-stu-id="92626-257">False</span></span>                                                                             |
| <span data-ttu-id="92626-258">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="92626-258">Is-Single-Valued</span></span>       | <span data-ttu-id="92626-259">False</span><span class="sxs-lookup"><span data-stu-id="92626-259">False</span></span>                                                                             |
| <span data-ttu-id="92626-260">Está indexado</span><span class="sxs-lookup"><span data-stu-id="92626-260">Is Indexed</span></span>             | <span data-ttu-id="92626-261">False</span><span class="sxs-lookup"><span data-stu-id="92626-261">False</span></span>                                                                             |
| <span data-ttu-id="92626-262">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="92626-262">In Global Catalog</span></span>      | <span data-ttu-id="92626-263">False</span><span class="sxs-lookup"><span data-stu-id="92626-263">False</span></span>                                                                             |
| <span data-ttu-id="92626-264">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="92626-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="92626-265">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="92626-265">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="92626-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92626-266">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="92626-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92626-267">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="92626-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92626-268">Search-Flags</span></span>           | <span data-ttu-id="92626-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92626-269">0x00000000</span></span>                                                                        |
| <span data-ttu-id="92626-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92626-270">System-Flags</span></span>           | <span data-ttu-id="92626-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92626-271">0x00000010</span></span>                                                                        |
| <span data-ttu-id="92626-272">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="92626-272">Classes used in</span></span>        | [<span data-ttu-id="92626-273">**Nodo DNS**</span><span class="sxs-lookup"><span data-stu-id="92626-273">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="92626-274">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="92626-274">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 





