---
title: 'DHCP: atributo servers'
description: Contiene una lista de servidores que están autorizados en la empresa.
ms.assetid: f712b2d2-ff9c-4ee2-aede-b68023e3e6b6
ms.tgt_platform: multiple
keywords:
- DHCP-atributos de servidor esquema de AD
- dhcpServers esquema de AD de atributos
topic_type:
- apiref
api_name:
- dhcp-Servers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e43018c91e5bb495ee39476f07f40756cfcf097
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997277"
---
# <a name="dhcp-servers-attribute"></a><span data-ttu-id="4b136-105">DHCP: atributo servers</span><span class="sxs-lookup"><span data-stu-id="4b136-105">dhcp-Servers attribute</span></span>

<span data-ttu-id="4b136-106">Contiene una lista de servidores que están autorizados en la empresa.</span><span class="sxs-lookup"><span data-stu-id="4b136-106">Contains a list of servers that are authorized in the enterprise.</span></span>



| <span data-ttu-id="4b136-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="4b136-107">Entry</span></span> | <span data-ttu-id="4b136-108">Value</span><span class="sxs-lookup"><span data-stu-id="4b136-108">Value</span></span> |
|-------------------|--------------------------------------------------------|
| <span data-ttu-id="4b136-109">CN</span><span class="sxs-lookup"><span data-stu-id="4b136-109">CN</span></span>                | <span data-ttu-id="4b136-110">DHCP-servidores</span><span class="sxs-lookup"><span data-stu-id="4b136-110">dhcp-Servers</span></span>                                           |
| <span data-ttu-id="4b136-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="4b136-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4b136-112">dhcpServers</span><span class="sxs-lookup"><span data-stu-id="4b136-112">dhcpServers</span></span>                                            |
| <span data-ttu-id="4b136-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="4b136-113">Size</span></span>              | \-                                                     |
| <span data-ttu-id="4b136-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="4b136-114">Update Privilege</span></span>  | <span data-ttu-id="4b136-115">Administrador de dominio.</span><span class="sxs-lookup"><span data-stu-id="4b136-115">Domain administrator.</span></span>                                  |
| <span data-ttu-id="4b136-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="4b136-116">Update Frequency</span></span>  | <span data-ttu-id="4b136-117">Cuando se agrega o se quita un nuevo servidor del bosque.</span><span class="sxs-lookup"><span data-stu-id="4b136-117">When a new server is added or removed from the forest.</span></span> |
| <span data-ttu-id="4b136-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4b136-118">Attribute-Id</span></span>      | <span data-ttu-id="4b136-119">1.2.840.113556.1.4.704</span><span class="sxs-lookup"><span data-stu-id="4b136-119">1.2.840.113556.1.4.704</span></span>                                 |
| <span data-ttu-id="4b136-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4b136-120">System-Id-Guid</span></span>    | <span data-ttu-id="4b136-121">963d2745-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="4b136-121">963d2745-48be-11d1-a9c3-0000f80367c1</span></span>                   |
| <span data-ttu-id="4b136-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b136-122">Syntax</span></span>            | [<span data-ttu-id="4b136-123">**String(IA5)**</span><span class="sxs-lookup"><span data-stu-id="4b136-123">**String(IA5)**</span></span>](s-string-ia5.md)                    |



## <a name="implementations"></a><span data-ttu-id="4b136-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="4b136-124">Implementations</span></span>

-   [<span data-ttu-id="4b136-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4b136-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4b136-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4b136-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4b136-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4b136-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4b136-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4b136-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4b136-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4b136-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4b136-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4b136-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4b136-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4b136-131">Windows 2000 Server</span></span>



| <span data-ttu-id="4b136-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="4b136-132">Entry</span></span> | <span data-ttu-id="4b136-133">Value</span><span class="sxs-lookup"><span data-stu-id="4b136-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b136-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4b136-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b136-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b136-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b136-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b136-136">System-Only</span></span>            | <span data-ttu-id="4b136-137">False</span><span class="sxs-lookup"><span data-stu-id="4b136-137">False</span></span>                                        |
| <span data-ttu-id="4b136-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4b136-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4b136-139">False</span><span class="sxs-lookup"><span data-stu-id="4b136-139">False</span></span>                                        |
| <span data-ttu-id="4b136-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4b136-140">Is Indexed</span></span>             | <span data-ttu-id="4b136-141">False</span><span class="sxs-lookup"><span data-stu-id="4b136-141">False</span></span>                                        |
| <span data-ttu-id="4b136-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4b136-142">In Global Catalog</span></span>      | <span data-ttu-id="4b136-143">False</span><span class="sxs-lookup"><span data-stu-id="4b136-143">False</span></span>                                        |
| <span data-ttu-id="4b136-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4b136-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b136-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b136-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b136-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b136-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b136-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b136-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b136-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b136-148">Search-Flags</span></span>           | <span data-ttu-id="4b136-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b136-149">0x00000000</span></span>                                   |
| <span data-ttu-id="4b136-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b136-150">System-Flags</span></span>           | <span data-ttu-id="4b136-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b136-151">0x00000010</span></span>                                   |
| <span data-ttu-id="4b136-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4b136-152">Classes used in</span></span>        | [<span data-ttu-id="4b136-153">**Clase de DHCP**</span><span class="sxs-lookup"><span data-stu-id="4b136-153">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4b136-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4b136-154">Windows Server 2003</span></span>



| <span data-ttu-id="4b136-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="4b136-155">Entry</span></span> | <span data-ttu-id="4b136-156">Value</span><span class="sxs-lookup"><span data-stu-id="4b136-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b136-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4b136-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b136-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b136-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b136-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b136-159">System-Only</span></span>            | <span data-ttu-id="4b136-160">False</span><span class="sxs-lookup"><span data-stu-id="4b136-160">False</span></span>                                        |
| <span data-ttu-id="4b136-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4b136-161">Is-Single-Valued</span></span>       | <span data-ttu-id="4b136-162">False</span><span class="sxs-lookup"><span data-stu-id="4b136-162">False</span></span>                                        |
| <span data-ttu-id="4b136-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4b136-163">Is Indexed</span></span>             | <span data-ttu-id="4b136-164">False</span><span class="sxs-lookup"><span data-stu-id="4b136-164">False</span></span>                                        |
| <span data-ttu-id="4b136-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4b136-165">In Global Catalog</span></span>      | <span data-ttu-id="4b136-166">False</span><span class="sxs-lookup"><span data-stu-id="4b136-166">False</span></span>                                        |
| <span data-ttu-id="4b136-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4b136-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b136-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b136-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b136-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b136-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b136-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b136-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b136-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b136-171">Search-Flags</span></span>           | <span data-ttu-id="4b136-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b136-172">0x00000000</span></span>                                   |
| <span data-ttu-id="4b136-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b136-173">System-Flags</span></span>           | <span data-ttu-id="4b136-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b136-174">0x00000010</span></span>                                   |
| <span data-ttu-id="4b136-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4b136-175">Classes used in</span></span>        | [<span data-ttu-id="4b136-176">**Clase de DHCP**</span><span class="sxs-lookup"><span data-stu-id="4b136-176">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4b136-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4b136-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4b136-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="4b136-178">Entry</span></span> | <span data-ttu-id="4b136-179">Value</span><span class="sxs-lookup"><span data-stu-id="4b136-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b136-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4b136-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b136-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b136-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b136-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b136-182">System-Only</span></span>            | <span data-ttu-id="4b136-183">False</span><span class="sxs-lookup"><span data-stu-id="4b136-183">False</span></span>                                        |
| <span data-ttu-id="4b136-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4b136-184">Is-Single-Valued</span></span>       | <span data-ttu-id="4b136-185">False</span><span class="sxs-lookup"><span data-stu-id="4b136-185">False</span></span>                                        |
| <span data-ttu-id="4b136-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4b136-186">Is Indexed</span></span>             | <span data-ttu-id="4b136-187">False</span><span class="sxs-lookup"><span data-stu-id="4b136-187">False</span></span>                                        |
| <span data-ttu-id="4b136-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4b136-188">In Global Catalog</span></span>      | <span data-ttu-id="4b136-189">False</span><span class="sxs-lookup"><span data-stu-id="4b136-189">False</span></span>                                        |
| <span data-ttu-id="4b136-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4b136-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b136-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b136-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b136-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b136-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b136-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b136-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b136-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b136-194">Search-Flags</span></span>           | <span data-ttu-id="4b136-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b136-195">0x00000000</span></span>                                   |
| <span data-ttu-id="4b136-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b136-196">System-Flags</span></span>           | <span data-ttu-id="4b136-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b136-197">0x00000010</span></span>                                   |
| <span data-ttu-id="4b136-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4b136-198">Classes used in</span></span>        | [<span data-ttu-id="4b136-199">**Clase de DHCP**</span><span class="sxs-lookup"><span data-stu-id="4b136-199">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4b136-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b136-200">Windows Server 2008</span></span>



| <span data-ttu-id="4b136-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="4b136-201">Entry</span></span> | <span data-ttu-id="4b136-202">Value</span><span class="sxs-lookup"><span data-stu-id="4b136-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b136-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4b136-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b136-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b136-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b136-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b136-205">System-Only</span></span>            | <span data-ttu-id="4b136-206">False</span><span class="sxs-lookup"><span data-stu-id="4b136-206">False</span></span>                                        |
| <span data-ttu-id="4b136-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4b136-207">Is-Single-Valued</span></span>       | <span data-ttu-id="4b136-208">False</span><span class="sxs-lookup"><span data-stu-id="4b136-208">False</span></span>                                        |
| <span data-ttu-id="4b136-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4b136-209">Is Indexed</span></span>             | <span data-ttu-id="4b136-210">False</span><span class="sxs-lookup"><span data-stu-id="4b136-210">False</span></span>                                        |
| <span data-ttu-id="4b136-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4b136-211">In Global Catalog</span></span>      | <span data-ttu-id="4b136-212">False</span><span class="sxs-lookup"><span data-stu-id="4b136-212">False</span></span>                                        |
| <span data-ttu-id="4b136-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4b136-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b136-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b136-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b136-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b136-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b136-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b136-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b136-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b136-217">Search-Flags</span></span>           | <span data-ttu-id="4b136-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b136-218">0x00000000</span></span>                                   |
| <span data-ttu-id="4b136-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b136-219">System-Flags</span></span>           | <span data-ttu-id="4b136-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b136-220">0x00000010</span></span>                                   |
| <span data-ttu-id="4b136-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4b136-221">Classes used in</span></span>        | [<span data-ttu-id="4b136-222">**Clase de DHCP**</span><span class="sxs-lookup"><span data-stu-id="4b136-222">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4b136-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4b136-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4b136-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="4b136-224">Entry</span></span> | <span data-ttu-id="4b136-225">Value</span><span class="sxs-lookup"><span data-stu-id="4b136-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b136-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4b136-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b136-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b136-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b136-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b136-228">System-Only</span></span>            | <span data-ttu-id="4b136-229">False</span><span class="sxs-lookup"><span data-stu-id="4b136-229">False</span></span>                                        |
| <span data-ttu-id="4b136-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4b136-230">Is-Single-Valued</span></span>       | <span data-ttu-id="4b136-231">False</span><span class="sxs-lookup"><span data-stu-id="4b136-231">False</span></span>                                        |
| <span data-ttu-id="4b136-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4b136-232">Is Indexed</span></span>             | <span data-ttu-id="4b136-233">False</span><span class="sxs-lookup"><span data-stu-id="4b136-233">False</span></span>                                        |
| <span data-ttu-id="4b136-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4b136-234">In Global Catalog</span></span>      | <span data-ttu-id="4b136-235">False</span><span class="sxs-lookup"><span data-stu-id="4b136-235">False</span></span>                                        |
| <span data-ttu-id="4b136-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4b136-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b136-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b136-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b136-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b136-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b136-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b136-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b136-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b136-240">Search-Flags</span></span>           | <span data-ttu-id="4b136-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b136-241">0x00000000</span></span>                                   |
| <span data-ttu-id="4b136-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b136-242">System-Flags</span></span>           | <span data-ttu-id="4b136-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b136-243">0x00000010</span></span>                                   |
| <span data-ttu-id="4b136-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4b136-244">Classes used in</span></span>        | [<span data-ttu-id="4b136-245">**Clase de DHCP**</span><span class="sxs-lookup"><span data-stu-id="4b136-245">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4b136-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4b136-246">Windows Server 2012</span></span>



| <span data-ttu-id="4b136-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="4b136-247">Entry</span></span> | <span data-ttu-id="4b136-248">Value</span><span class="sxs-lookup"><span data-stu-id="4b136-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b136-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4b136-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b136-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b136-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b136-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b136-251">System-Only</span></span>            | <span data-ttu-id="4b136-252">False</span><span class="sxs-lookup"><span data-stu-id="4b136-252">False</span></span>                                        |
| <span data-ttu-id="4b136-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4b136-253">Is-Single-Valued</span></span>       | <span data-ttu-id="4b136-254">False</span><span class="sxs-lookup"><span data-stu-id="4b136-254">False</span></span>                                        |
| <span data-ttu-id="4b136-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4b136-255">Is Indexed</span></span>             | <span data-ttu-id="4b136-256">False</span><span class="sxs-lookup"><span data-stu-id="4b136-256">False</span></span>                                        |
| <span data-ttu-id="4b136-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4b136-257">In Global Catalog</span></span>      | <span data-ttu-id="4b136-258">False</span><span class="sxs-lookup"><span data-stu-id="4b136-258">False</span></span>                                        |
| <span data-ttu-id="4b136-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4b136-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b136-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b136-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b136-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b136-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b136-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b136-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b136-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b136-263">Search-Flags</span></span>           | <span data-ttu-id="4b136-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b136-264">0x00000000</span></span>                                   |
| <span data-ttu-id="4b136-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b136-265">System-Flags</span></span>           | <span data-ttu-id="4b136-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b136-266">0x00000010</span></span>                                   |
| <span data-ttu-id="4b136-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4b136-267">Classes used in</span></span>        | [<span data-ttu-id="4b136-268">**Clase de DHCP**</span><span class="sxs-lookup"><span data-stu-id="4b136-268">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



 

 





