---
title: Atributo LDAP-Display-Name
description: Nombre utilizado por los clientes LDAP, como el proveedor LDAP de ADSI, para leer y escribir el atributo mediante el protocolo LDAP.
ms.assetid: 9cb0b2f0-16cf-4fc6-85b2-d21ff71bc477
ms.tgt_platform: multiple
keywords:
- LDAP-Display-Name atributo AD Schema
- Esquema de AD de atributo lDAPDisplayName
topic_type:
- apiref
api_name:
- LDAP-Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ffa25777ec4b5139a41ba9e56d8d5f0a9a3d92
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104274567"
---
# <a name="ldap-display-name-attribute"></a><span data-ttu-id="b0a2d-105">Atributo LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b0a2d-105">LDAP-Display-Name attribute</span></span>

<span data-ttu-id="b0a2d-106">Nombre utilizado por los clientes LDAP, como el proveedor LDAP de ADSI, para leer y escribir el atributo mediante el protocolo LDAP.</span><span class="sxs-lookup"><span data-stu-id="b0a2d-106">The name used by LDAP clients, such as the ADSI LDAP provider, to read and write the attribute by using the LDAP protocol.</span></span>



| <span data-ttu-id="b0a2d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="b0a2d-107">Entry</span></span> | <span data-ttu-id="b0a2d-108">Value</span><span class="sxs-lookup"><span data-stu-id="b0a2d-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b0a2d-109">CN</span><span class="sxs-lookup"><span data-stu-id="b0a2d-109">CN</span></span>                | <span data-ttu-id="b0a2d-110">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="b0a2d-110">LDAP-Display-Name</span></span>                           |
| <span data-ttu-id="b0a2d-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="b0a2d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b0a2d-112">lDAPDisplayName</span><span class="sxs-lookup"><span data-stu-id="b0a2d-112">lDAPDisplayName</span></span>                             |
| <span data-ttu-id="b0a2d-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="b0a2d-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="b0a2d-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="b0a2d-114">Update Privilege</span></span>  | <span data-ttu-id="b0a2d-115">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="b0a2d-115">Schema administrator</span></span>                        |
| <span data-ttu-id="b0a2d-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="b0a2d-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b0a2d-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b0a2d-117">Attribute-Id</span></span>      | <span data-ttu-id="b0a2d-118">1.2.840.113556.1.2.460</span><span class="sxs-lookup"><span data-stu-id="b0a2d-118">1.2.840.113556.1.2.460</span></span>                      |
| <span data-ttu-id="b0a2d-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b0a2d-119">System-Id-Guid</span></span>    | <span data-ttu-id="b0a2d-120">bf96799a-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b0a2d-120">bf96799a-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="b0a2d-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0a2d-121">Syntax</span></span>            | [<span data-ttu-id="b0a2d-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b0a2d-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="b0a2d-123">Implementations</span></span>

-   [<span data-ttu-id="b0a2d-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b0a2d-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b0a2d-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b0a2d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b0a2d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b0a2d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b0a2d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b0a2d-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b0a2d-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b0a2d-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="b0a2d-132">Entry</span></span> | <span data-ttu-id="b0a2d-133">Value</span><span class="sxs-lookup"><span data-stu-id="b0a2d-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a2d-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b0a2d-134">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b0a2d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0a2d-135">MAPI-Id</span></span>                | <span data-ttu-id="b0a2d-136">0x8171</span><span class="sxs-lookup"><span data-stu-id="b0a2d-136">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="b0a2d-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0a2d-137">System-Only</span></span>            | <span data-ttu-id="b0a2d-138">False</span><span class="sxs-lookup"><span data-stu-id="b0a2d-138">False</span></span>                                                                                                     |
| <span data-ttu-id="b0a2d-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b0a2d-139">Is-Single-Valued</span></span>       | <span data-ttu-id="b0a2d-140">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-140">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b0a2d-141">Is Indexed</span></span>             | <span data-ttu-id="b0a2d-142">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-142">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b0a2d-143">In Global Catalog</span></span>      | <span data-ttu-id="b0a2d-144">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-144">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b0a2d-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0a2d-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b0a2d-146">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="b0a2d-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0a2d-147">Range-Lower</span></span>            | <span data-ttu-id="b0a2d-148">1</span><span class="sxs-lookup"><span data-stu-id="b0a2d-148">1</span></span>                                                                                                         |
| <span data-ttu-id="b0a2d-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0a2d-149">Range-Upper</span></span>            | <span data-ttu-id="b0a2d-150">256</span><span class="sxs-lookup"><span data-stu-id="b0a2d-150">256</span></span>                                                                                                       |
| <span data-ttu-id="b0a2d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0a2d-151">Search-Flags</span></span>           | <span data-ttu-id="b0a2d-152">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b0a2d-152">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="b0a2d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0a2d-153">System-Flags</span></span>           | <span data-ttu-id="b0a2d-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0a2d-154">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="b0a2d-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b0a2d-155">Classes used in</span></span>        | [<span data-ttu-id="b0a2d-156">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-156">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="b0a2d-157">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-157">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b0a2d-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b0a2d-158">Windows Server 2003</span></span>



| <span data-ttu-id="b0a2d-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="b0a2d-159">Entry</span></span> | <span data-ttu-id="b0a2d-160">Value</span><span class="sxs-lookup"><span data-stu-id="b0a2d-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a2d-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b0a2d-161">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b0a2d-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0a2d-162">MAPI-Id</span></span>                | <span data-ttu-id="b0a2d-163">0x8171</span><span class="sxs-lookup"><span data-stu-id="b0a2d-163">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="b0a2d-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0a2d-164">System-Only</span></span>            | <span data-ttu-id="b0a2d-165">False</span><span class="sxs-lookup"><span data-stu-id="b0a2d-165">False</span></span>                                                                                                     |
| <span data-ttu-id="b0a2d-166">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b0a2d-166">Is-Single-Valued</span></span>       | <span data-ttu-id="b0a2d-167">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-167">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-168">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b0a2d-168">Is Indexed</span></span>             | <span data-ttu-id="b0a2d-169">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-169">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-170">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b0a2d-170">In Global Catalog</span></span>      | <span data-ttu-id="b0a2d-171">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-171">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-172">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b0a2d-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0a2d-173">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b0a2d-173">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="b0a2d-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0a2d-174">Range-Lower</span></span>            | <span data-ttu-id="b0a2d-175">1</span><span class="sxs-lookup"><span data-stu-id="b0a2d-175">1</span></span>                                                                                                         |
| <span data-ttu-id="b0a2d-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0a2d-176">Range-Upper</span></span>            | <span data-ttu-id="b0a2d-177">256</span><span class="sxs-lookup"><span data-stu-id="b0a2d-177">256</span></span>                                                                                                       |
| <span data-ttu-id="b0a2d-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0a2d-178">Search-Flags</span></span>           | <span data-ttu-id="b0a2d-179">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b0a2d-179">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="b0a2d-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0a2d-180">System-Flags</span></span>           | <span data-ttu-id="b0a2d-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0a2d-181">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="b0a2d-182">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b0a2d-182">Classes used in</span></span>        | [<span data-ttu-id="b0a2d-183">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-183">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="b0a2d-184">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-184">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b0a2d-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="b0a2d-185">ADAM</span></span>



| <span data-ttu-id="b0a2d-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="b0a2d-186">Entry</span></span> | <span data-ttu-id="b0a2d-187">Value</span><span class="sxs-lookup"><span data-stu-id="b0a2d-187">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a2d-188">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b0a2d-188">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b0a2d-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0a2d-189">MAPI-Id</span></span>                | <span data-ttu-id="b0a2d-190">0x8171</span><span class="sxs-lookup"><span data-stu-id="b0a2d-190">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="b0a2d-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0a2d-191">System-Only</span></span>            | <span data-ttu-id="b0a2d-192">False</span><span class="sxs-lookup"><span data-stu-id="b0a2d-192">False</span></span>                                                                                                     |
| <span data-ttu-id="b0a2d-193">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b0a2d-193">Is-Single-Valued</span></span>       | <span data-ttu-id="b0a2d-194">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-194">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-195">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b0a2d-195">Is Indexed</span></span>             | <span data-ttu-id="b0a2d-196">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-196">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-197">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b0a2d-197">In Global Catalog</span></span>      | <span data-ttu-id="b0a2d-198">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-198">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-199">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b0a2d-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0a2d-200">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b0a2d-200">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="b0a2d-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0a2d-201">Range-Lower</span></span>            | <span data-ttu-id="b0a2d-202">1</span><span class="sxs-lookup"><span data-stu-id="b0a2d-202">1</span></span>                                                                                                         |
| <span data-ttu-id="b0a2d-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0a2d-203">Range-Upper</span></span>            | <span data-ttu-id="b0a2d-204">256</span><span class="sxs-lookup"><span data-stu-id="b0a2d-204">256</span></span>                                                                                                       |
| <span data-ttu-id="b0a2d-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0a2d-205">Search-Flags</span></span>           | <span data-ttu-id="b0a2d-206">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b0a2d-206">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="b0a2d-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0a2d-207">System-Flags</span></span>           | <span data-ttu-id="b0a2d-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0a2d-208">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="b0a2d-209">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b0a2d-209">Classes used in</span></span>        | [<span data-ttu-id="b0a2d-210">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-210">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="b0a2d-211">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-211">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b0a2d-212">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b0a2d-212">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b0a2d-213">Entrada</span><span class="sxs-lookup"><span data-stu-id="b0a2d-213">Entry</span></span> | <span data-ttu-id="b0a2d-214">Value</span><span class="sxs-lookup"><span data-stu-id="b0a2d-214">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a2d-215">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b0a2d-215">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b0a2d-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0a2d-216">MAPI-Id</span></span>                | <span data-ttu-id="b0a2d-217">0x8171</span><span class="sxs-lookup"><span data-stu-id="b0a2d-217">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="b0a2d-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0a2d-218">System-Only</span></span>            | <span data-ttu-id="b0a2d-219">False</span><span class="sxs-lookup"><span data-stu-id="b0a2d-219">False</span></span>                                                                                                     |
| <span data-ttu-id="b0a2d-220">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b0a2d-220">Is-Single-Valued</span></span>       | <span data-ttu-id="b0a2d-221">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-221">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-222">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b0a2d-222">Is Indexed</span></span>             | <span data-ttu-id="b0a2d-223">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-223">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-224">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b0a2d-224">In Global Catalog</span></span>      | <span data-ttu-id="b0a2d-225">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-225">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-226">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b0a2d-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0a2d-227">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b0a2d-227">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="b0a2d-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0a2d-228">Range-Lower</span></span>            | <span data-ttu-id="b0a2d-229">1</span><span class="sxs-lookup"><span data-stu-id="b0a2d-229">1</span></span>                                                                                                         |
| <span data-ttu-id="b0a2d-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0a2d-230">Range-Upper</span></span>            | <span data-ttu-id="b0a2d-231">256</span><span class="sxs-lookup"><span data-stu-id="b0a2d-231">256</span></span>                                                                                                       |
| <span data-ttu-id="b0a2d-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0a2d-232">Search-Flags</span></span>           | <span data-ttu-id="b0a2d-233">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b0a2d-233">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="b0a2d-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0a2d-234">System-Flags</span></span>           | <span data-ttu-id="b0a2d-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0a2d-235">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="b0a2d-236">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b0a2d-236">Classes used in</span></span>        | [<span data-ttu-id="b0a2d-237">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-237">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="b0a2d-238">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-238">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b0a2d-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0a2d-239">Windows Server 2008</span></span>



| <span data-ttu-id="b0a2d-240">Entrada</span><span class="sxs-lookup"><span data-stu-id="b0a2d-240">Entry</span></span> | <span data-ttu-id="b0a2d-241">Value</span><span class="sxs-lookup"><span data-stu-id="b0a2d-241">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a2d-242">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b0a2d-242">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b0a2d-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0a2d-243">MAPI-Id</span></span>                | <span data-ttu-id="b0a2d-244">0x8171</span><span class="sxs-lookup"><span data-stu-id="b0a2d-244">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="b0a2d-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0a2d-245">System-Only</span></span>            | <span data-ttu-id="b0a2d-246">False</span><span class="sxs-lookup"><span data-stu-id="b0a2d-246">False</span></span>                                                                                                     |
| <span data-ttu-id="b0a2d-247">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b0a2d-247">Is-Single-Valued</span></span>       | <span data-ttu-id="b0a2d-248">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-248">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-249">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b0a2d-249">Is Indexed</span></span>             | <span data-ttu-id="b0a2d-250">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-250">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-251">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b0a2d-251">In Global Catalog</span></span>      | <span data-ttu-id="b0a2d-252">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-252">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-253">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b0a2d-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0a2d-254">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b0a2d-254">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="b0a2d-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0a2d-255">Range-Lower</span></span>            | <span data-ttu-id="b0a2d-256">1</span><span class="sxs-lookup"><span data-stu-id="b0a2d-256">1</span></span>                                                                                                         |
| <span data-ttu-id="b0a2d-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0a2d-257">Range-Upper</span></span>            | <span data-ttu-id="b0a2d-258">256</span><span class="sxs-lookup"><span data-stu-id="b0a2d-258">256</span></span>                                                                                                       |
| <span data-ttu-id="b0a2d-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0a2d-259">Search-Flags</span></span>           | <span data-ttu-id="b0a2d-260">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b0a2d-260">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="b0a2d-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0a2d-261">System-Flags</span></span>           | <span data-ttu-id="b0a2d-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0a2d-262">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="b0a2d-263">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b0a2d-263">Classes used in</span></span>        | [<span data-ttu-id="b0a2d-264">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-264">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="b0a2d-265">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-265">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b0a2d-266">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b0a2d-266">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b0a2d-267">Entrada</span><span class="sxs-lookup"><span data-stu-id="b0a2d-267">Entry</span></span> | <span data-ttu-id="b0a2d-268">Value</span><span class="sxs-lookup"><span data-stu-id="b0a2d-268">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a2d-269">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b0a2d-269">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b0a2d-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0a2d-270">MAPI-Id</span></span>                | <span data-ttu-id="b0a2d-271">0x8171</span><span class="sxs-lookup"><span data-stu-id="b0a2d-271">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="b0a2d-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0a2d-272">System-Only</span></span>            | <span data-ttu-id="b0a2d-273">False</span><span class="sxs-lookup"><span data-stu-id="b0a2d-273">False</span></span>                                                                                                     |
| <span data-ttu-id="b0a2d-274">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b0a2d-274">Is-Single-Valued</span></span>       | <span data-ttu-id="b0a2d-275">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-275">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-276">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b0a2d-276">Is Indexed</span></span>             | <span data-ttu-id="b0a2d-277">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-277">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-278">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b0a2d-278">In Global Catalog</span></span>      | <span data-ttu-id="b0a2d-279">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-279">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-280">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b0a2d-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0a2d-281">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b0a2d-281">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="b0a2d-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0a2d-282">Range-Lower</span></span>            | <span data-ttu-id="b0a2d-283">1</span><span class="sxs-lookup"><span data-stu-id="b0a2d-283">1</span></span>                                                                                                         |
| <span data-ttu-id="b0a2d-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0a2d-284">Range-Upper</span></span>            | <span data-ttu-id="b0a2d-285">256</span><span class="sxs-lookup"><span data-stu-id="b0a2d-285">256</span></span>                                                                                                       |
| <span data-ttu-id="b0a2d-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0a2d-286">Search-Flags</span></span>           | <span data-ttu-id="b0a2d-287">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b0a2d-287">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="b0a2d-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0a2d-288">System-Flags</span></span>           | <span data-ttu-id="b0a2d-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0a2d-289">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="b0a2d-290">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b0a2d-290">Classes used in</span></span>        | [<span data-ttu-id="b0a2d-291">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-291">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="b0a2d-292">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-292">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b0a2d-293">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b0a2d-293">Windows Server 2012</span></span>



| <span data-ttu-id="b0a2d-294">Entrada</span><span class="sxs-lookup"><span data-stu-id="b0a2d-294">Entry</span></span> | <span data-ttu-id="b0a2d-295">Value</span><span class="sxs-lookup"><span data-stu-id="b0a2d-295">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a2d-296">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b0a2d-296">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="b0a2d-297">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0a2d-297">MAPI-Id</span></span>                | <span data-ttu-id="b0a2d-298">0x8171</span><span class="sxs-lookup"><span data-stu-id="b0a2d-298">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="b0a2d-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0a2d-299">System-Only</span></span>            | <span data-ttu-id="b0a2d-300">False</span><span class="sxs-lookup"><span data-stu-id="b0a2d-300">False</span></span>                                                                                                     |
| <span data-ttu-id="b0a2d-301">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b0a2d-301">Is-Single-Valued</span></span>       | <span data-ttu-id="b0a2d-302">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-302">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-303">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b0a2d-303">Is Indexed</span></span>             | <span data-ttu-id="b0a2d-304">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-304">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-305">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b0a2d-305">In Global Catalog</span></span>      | <span data-ttu-id="b0a2d-306">True</span><span class="sxs-lookup"><span data-stu-id="b0a2d-306">True</span></span>                                                                                                      |
| <span data-ttu-id="b0a2d-307">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b0a2d-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0a2d-308">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b0a2d-308">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="b0a2d-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0a2d-309">Range-Lower</span></span>            | <span data-ttu-id="b0a2d-310">1</span><span class="sxs-lookup"><span data-stu-id="b0a2d-310">1</span></span>                                                                                                         |
| <span data-ttu-id="b0a2d-311">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0a2d-311">Range-Upper</span></span>            | <span data-ttu-id="b0a2d-312">256</span><span class="sxs-lookup"><span data-stu-id="b0a2d-312">256</span></span>                                                                                                       |
| <span data-ttu-id="b0a2d-313">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0a2d-313">Search-Flags</span></span>           | <span data-ttu-id="b0a2d-314">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b0a2d-314">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="b0a2d-315">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0a2d-315">System-Flags</span></span>           | <span data-ttu-id="b0a2d-316">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0a2d-316">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="b0a2d-317">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b0a2d-317">Classes used in</span></span>        | [<span data-ttu-id="b0a2d-318">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-318">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="b0a2d-319">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="b0a2d-319">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





