---
title: atributo de tipo DHCP
description: El tipo de servidor DHCP.
ms.assetid: 46ab7db7-a752-45aa-a10b-1195b5cf6f80
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de tipo DHCP
- dhcpType esquema de AD de atributos
topic_type:
- apiref
api_name:
- dhcp-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5a5a331ff7298854f4ca070799a05e2a3497f2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997275"
---
# <a name="dhcp-type-attribute"></a><span data-ttu-id="e90f2-105">atributo de tipo DHCP</span><span class="sxs-lookup"><span data-stu-id="e90f2-105">dhcp-Type attribute</span></span>

<span data-ttu-id="e90f2-106">El tipo de servidor DHCP.</span><span class="sxs-lookup"><span data-stu-id="e90f2-106">The type of DHCP server.</span></span> <span data-ttu-id="e90f2-107">Este atributo se establece en todos los objetos de objectClass [**dHCPClass**](c-dhcpclass.md).</span><span class="sxs-lookup"><span data-stu-id="e90f2-107">This attribute is set on all objects of objectClass [**dHCPClass**](c-dhcpclass.md).</span></span> <span data-ttu-id="e90f2-108">Su valor define el tipo de objeto:</span><span class="sxs-lookup"><span data-stu-id="e90f2-108">Its value defines the type of object:</span></span>

``` syntax
  0 - DHCP Root Object
  1 - DHCP Server
```



| <span data-ttu-id="e90f2-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="e90f2-109">Entry</span></span> | <span data-ttu-id="e90f2-110">Value</span><span class="sxs-lookup"><span data-stu-id="e90f2-110">Value</span></span> |
|-------------------|--------------------------------------------------------|
| <span data-ttu-id="e90f2-111">CN</span><span class="sxs-lookup"><span data-stu-id="e90f2-111">CN</span></span>                | <span data-ttu-id="e90f2-112">Tipo DHCP</span><span class="sxs-lookup"><span data-stu-id="e90f2-112">dhcp-Type</span></span>                                              |
| <span data-ttu-id="e90f2-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="e90f2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e90f2-114">dhcpType</span><span class="sxs-lookup"><span data-stu-id="e90f2-114">dhcpType</span></span>                                               |
| <span data-ttu-id="e90f2-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="e90f2-115">Size</span></span>              | <span data-ttu-id="e90f2-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="e90f2-116">4 bytes</span></span>                                                |
| <span data-ttu-id="e90f2-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="e90f2-117">Update Privilege</span></span>  | <span data-ttu-id="e90f2-118">Administrador de dominio.</span><span class="sxs-lookup"><span data-stu-id="e90f2-118">Domain administrator.</span></span>                                  |
| <span data-ttu-id="e90f2-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="e90f2-119">Update Frequency</span></span>  | <span data-ttu-id="e90f2-120">Cuando se agrega o se quita un nuevo servidor del bosque.</span><span class="sxs-lookup"><span data-stu-id="e90f2-120">When a new server is added or removed from the forest.</span></span> |
| <span data-ttu-id="e90f2-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e90f2-121">Attribute-Id</span></span>      | <span data-ttu-id="e90f2-122">1.2.840.113556.1.4.699</span><span class="sxs-lookup"><span data-stu-id="e90f2-122">1.2.840.113556.1.4.699</span></span>                                 |
| <span data-ttu-id="e90f2-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e90f2-123">System-Id-Guid</span></span>    | <span data-ttu-id="e90f2-124">963d273b-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e90f2-124">963d273b-48be-11d1-a9c3-0000f80367c1</span></span>                   |
| <span data-ttu-id="e90f2-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e90f2-125">Syntax</span></span>            | [<span data-ttu-id="e90f2-126">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="e90f2-126">**Enumeration**</span></span>](s-enumeration.md)                   |



## <a name="implementations"></a><span data-ttu-id="e90f2-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="e90f2-127">Implementations</span></span>

-   [<span data-ttu-id="e90f2-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e90f2-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e90f2-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e90f2-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e90f2-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e90f2-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e90f2-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e90f2-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e90f2-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e90f2-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e90f2-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e90f2-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e90f2-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e90f2-134">Windows 2000 Server</span></span>



| <span data-ttu-id="e90f2-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="e90f2-135">Entry</span></span> | <span data-ttu-id="e90f2-136">Value</span><span class="sxs-lookup"><span data-stu-id="e90f2-136">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e90f2-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e90f2-137">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e90f2-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e90f2-138">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e90f2-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="e90f2-139">System-Only</span></span>            | <span data-ttu-id="e90f2-140">False</span><span class="sxs-lookup"><span data-stu-id="e90f2-140">False</span></span>                                        |
| <span data-ttu-id="e90f2-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e90f2-141">Is-Single-Valued</span></span>       | <span data-ttu-id="e90f2-142">True</span><span class="sxs-lookup"><span data-stu-id="e90f2-142">True</span></span>                                         |
| <span data-ttu-id="e90f2-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e90f2-143">Is Indexed</span></span>             | <span data-ttu-id="e90f2-144">True</span><span class="sxs-lookup"><span data-stu-id="e90f2-144">True</span></span>                                         |
| <span data-ttu-id="e90f2-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e90f2-145">In Global Catalog</span></span>      | <span data-ttu-id="e90f2-146">False</span><span class="sxs-lookup"><span data-stu-id="e90f2-146">False</span></span>                                        |
| <span data-ttu-id="e90f2-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e90f2-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="e90f2-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e90f2-148">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e90f2-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e90f2-149">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e90f2-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e90f2-150">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e90f2-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e90f2-151">Search-Flags</span></span>           | <span data-ttu-id="e90f2-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e90f2-152">0x00000001</span></span>                                   |
| <span data-ttu-id="e90f2-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e90f2-153">System-Flags</span></span>           | <span data-ttu-id="e90f2-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e90f2-154">0x00000010</span></span>                                   |
| <span data-ttu-id="e90f2-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e90f2-155">Classes used in</span></span>        | [<span data-ttu-id="e90f2-156">**Clase de DHCP**</span><span class="sxs-lookup"><span data-stu-id="e90f2-156">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e90f2-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e90f2-157">Windows Server 2003</span></span>



| <span data-ttu-id="e90f2-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="e90f2-158">Entry</span></span> | <span data-ttu-id="e90f2-159">Value</span><span class="sxs-lookup"><span data-stu-id="e90f2-159">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e90f2-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e90f2-160">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e90f2-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e90f2-161">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e90f2-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="e90f2-162">System-Only</span></span>            | <span data-ttu-id="e90f2-163">False</span><span class="sxs-lookup"><span data-stu-id="e90f2-163">False</span></span>                                        |
| <span data-ttu-id="e90f2-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e90f2-164">Is-Single-Valued</span></span>       | <span data-ttu-id="e90f2-165">True</span><span class="sxs-lookup"><span data-stu-id="e90f2-165">True</span></span>                                         |
| <span data-ttu-id="e90f2-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e90f2-166">Is Indexed</span></span>             | <span data-ttu-id="e90f2-167">True</span><span class="sxs-lookup"><span data-stu-id="e90f2-167">True</span></span>                                         |
| <span data-ttu-id="e90f2-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e90f2-168">In Global Catalog</span></span>      | <span data-ttu-id="e90f2-169">False</span><span class="sxs-lookup"><span data-stu-id="e90f2-169">False</span></span>                                        |
| <span data-ttu-id="e90f2-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e90f2-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="e90f2-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e90f2-171">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e90f2-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e90f2-172">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e90f2-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e90f2-173">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e90f2-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e90f2-174">Search-Flags</span></span>           | <span data-ttu-id="e90f2-175">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e90f2-175">0x00000001</span></span>                                   |
| <span data-ttu-id="e90f2-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e90f2-176">System-Flags</span></span>           | <span data-ttu-id="e90f2-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e90f2-177">0x00000010</span></span>                                   |
| <span data-ttu-id="e90f2-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e90f2-178">Classes used in</span></span>        | [<span data-ttu-id="e90f2-179">**Clase de DHCP**</span><span class="sxs-lookup"><span data-stu-id="e90f2-179">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e90f2-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e90f2-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e90f2-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="e90f2-181">Entry</span></span> | <span data-ttu-id="e90f2-182">Value</span><span class="sxs-lookup"><span data-stu-id="e90f2-182">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e90f2-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e90f2-183">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e90f2-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e90f2-184">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e90f2-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="e90f2-185">System-Only</span></span>            | <span data-ttu-id="e90f2-186">False</span><span class="sxs-lookup"><span data-stu-id="e90f2-186">False</span></span>                                        |
| <span data-ttu-id="e90f2-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e90f2-187">Is-Single-Valued</span></span>       | <span data-ttu-id="e90f2-188">True</span><span class="sxs-lookup"><span data-stu-id="e90f2-188">True</span></span>                                         |
| <span data-ttu-id="e90f2-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e90f2-189">Is Indexed</span></span>             | <span data-ttu-id="e90f2-190">True</span><span class="sxs-lookup"><span data-stu-id="e90f2-190">True</span></span>                                         |
| <span data-ttu-id="e90f2-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e90f2-191">In Global Catalog</span></span>      | <span data-ttu-id="e90f2-192">False</span><span class="sxs-lookup"><span data-stu-id="e90f2-192">False</span></span>                                        |
| <span data-ttu-id="e90f2-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e90f2-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="e90f2-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e90f2-194">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e90f2-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e90f2-195">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e90f2-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e90f2-196">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e90f2-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e90f2-197">Search-Flags</span></span>           | <span data-ttu-id="e90f2-198">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e90f2-198">0x00000001</span></span>                                   |
| <span data-ttu-id="e90f2-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e90f2-199">System-Flags</span></span>           | <span data-ttu-id="e90f2-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e90f2-200">0x00000010</span></span>                                   |
| <span data-ttu-id="e90f2-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e90f2-201">Classes used in</span></span>        | [<span data-ttu-id="e90f2-202">**Clase de DHCP**</span><span class="sxs-lookup"><span data-stu-id="e90f2-202">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e90f2-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e90f2-203">Windows Server 2008</span></span>



| <span data-ttu-id="e90f2-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="e90f2-204">Entry</span></span> | <span data-ttu-id="e90f2-205">Value</span><span class="sxs-lookup"><span data-stu-id="e90f2-205">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e90f2-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e90f2-206">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e90f2-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e90f2-207">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e90f2-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="e90f2-208">System-Only</span></span>            | <span data-ttu-id="e90f2-209">False</span><span class="sxs-lookup"><span data-stu-id="e90f2-209">False</span></span>                                        |
| <span data-ttu-id="e90f2-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e90f2-210">Is-Single-Valued</span></span>       | <span data-ttu-id="e90f2-211">True</span><span class="sxs-lookup"><span data-stu-id="e90f2-211">True</span></span>                                         |
| <span data-ttu-id="e90f2-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e90f2-212">Is Indexed</span></span>             | <span data-ttu-id="e90f2-213">True</span><span class="sxs-lookup"><span data-stu-id="e90f2-213">True</span></span>                                         |
| <span data-ttu-id="e90f2-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e90f2-214">In Global Catalog</span></span>      | <span data-ttu-id="e90f2-215">False</span><span class="sxs-lookup"><span data-stu-id="e90f2-215">False</span></span>                                        |
| <span data-ttu-id="e90f2-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e90f2-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="e90f2-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e90f2-217">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e90f2-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e90f2-218">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e90f2-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e90f2-219">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e90f2-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e90f2-220">Search-Flags</span></span>           | <span data-ttu-id="e90f2-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e90f2-221">0x00000001</span></span>                                   |
| <span data-ttu-id="e90f2-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e90f2-222">System-Flags</span></span>           | <span data-ttu-id="e90f2-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e90f2-223">0x00000010</span></span>                                   |
| <span data-ttu-id="e90f2-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e90f2-224">Classes used in</span></span>        | [<span data-ttu-id="e90f2-225">**Clase de DHCP**</span><span class="sxs-lookup"><span data-stu-id="e90f2-225">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e90f2-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e90f2-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e90f2-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="e90f2-227">Entry</span></span> | <span data-ttu-id="e90f2-228">Value</span><span class="sxs-lookup"><span data-stu-id="e90f2-228">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e90f2-229">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e90f2-229">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e90f2-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e90f2-230">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e90f2-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="e90f2-231">System-Only</span></span>            | <span data-ttu-id="e90f2-232">False</span><span class="sxs-lookup"><span data-stu-id="e90f2-232">False</span></span>                                        |
| <span data-ttu-id="e90f2-233">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e90f2-233">Is-Single-Valued</span></span>       | <span data-ttu-id="e90f2-234">True</span><span class="sxs-lookup"><span data-stu-id="e90f2-234">True</span></span>                                         |
| <span data-ttu-id="e90f2-235">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e90f2-235">Is Indexed</span></span>             | <span data-ttu-id="e90f2-236">True</span><span class="sxs-lookup"><span data-stu-id="e90f2-236">True</span></span>                                         |
| <span data-ttu-id="e90f2-237">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e90f2-237">In Global Catalog</span></span>      | <span data-ttu-id="e90f2-238">False</span><span class="sxs-lookup"><span data-stu-id="e90f2-238">False</span></span>                                        |
| <span data-ttu-id="e90f2-239">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e90f2-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="e90f2-240">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e90f2-240">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e90f2-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e90f2-241">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e90f2-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e90f2-242">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e90f2-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e90f2-243">Search-Flags</span></span>           | <span data-ttu-id="e90f2-244">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e90f2-244">0x00000001</span></span>                                   |
| <span data-ttu-id="e90f2-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e90f2-245">System-Flags</span></span>           | <span data-ttu-id="e90f2-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e90f2-246">0x00000010</span></span>                                   |
| <span data-ttu-id="e90f2-247">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e90f2-247">Classes used in</span></span>        | [<span data-ttu-id="e90f2-248">**Clase de DHCP**</span><span class="sxs-lookup"><span data-stu-id="e90f2-248">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e90f2-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e90f2-249">Windows Server 2012</span></span>



| <span data-ttu-id="e90f2-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="e90f2-250">Entry</span></span> | <span data-ttu-id="e90f2-251">Value</span><span class="sxs-lookup"><span data-stu-id="e90f2-251">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e90f2-252">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e90f2-252">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e90f2-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e90f2-253">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e90f2-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="e90f2-254">System-Only</span></span>            | <span data-ttu-id="e90f2-255">False</span><span class="sxs-lookup"><span data-stu-id="e90f2-255">False</span></span>                                        |
| <span data-ttu-id="e90f2-256">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e90f2-256">Is-Single-Valued</span></span>       | <span data-ttu-id="e90f2-257">True</span><span class="sxs-lookup"><span data-stu-id="e90f2-257">True</span></span>                                         |
| <span data-ttu-id="e90f2-258">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e90f2-258">Is Indexed</span></span>             | <span data-ttu-id="e90f2-259">True</span><span class="sxs-lookup"><span data-stu-id="e90f2-259">True</span></span>                                         |
| <span data-ttu-id="e90f2-260">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e90f2-260">In Global Catalog</span></span>      | <span data-ttu-id="e90f2-261">False</span><span class="sxs-lookup"><span data-stu-id="e90f2-261">False</span></span>                                        |
| <span data-ttu-id="e90f2-262">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e90f2-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="e90f2-263">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e90f2-263">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e90f2-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e90f2-264">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e90f2-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e90f2-265">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e90f2-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e90f2-266">Search-Flags</span></span>           | <span data-ttu-id="e90f2-267">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e90f2-267">0x00000001</span></span>                                   |
| <span data-ttu-id="e90f2-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e90f2-268">System-Flags</span></span>           | <span data-ttu-id="e90f2-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e90f2-269">0x00000010</span></span>                                   |
| <span data-ttu-id="e90f2-270">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e90f2-270">Classes used in</span></span>        | [<span data-ttu-id="e90f2-271">**Clase de DHCP**</span><span class="sxs-lookup"><span data-stu-id="e90f2-271">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



 

 





