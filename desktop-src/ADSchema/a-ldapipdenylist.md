---
title: Atributo LDAP-IPDeny-List
description: Contiene una lista de direcciones IP binarias a las que se deniega el acceso a un servidor LDAP.
ms.assetid: 7d554d49-8934-4d71-b32f-8e59c22faf8c
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo LDAP-IPDeny-List
- lDAPIPDenyList esquema de AD de atributos
topic_type:
- apiref
api_name:
- LDAP-IPDeny-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43246b5bb5786eefafc8598e9d729d9a2f308e08
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151692"
---
# <a name="ldap-ipdeny-list-attribute"></a><span data-ttu-id="8e57a-105">Atributo LDAP-IPDeny-List</span><span class="sxs-lookup"><span data-stu-id="8e57a-105">LDAP-IPDeny-List attribute</span></span>

<span data-ttu-id="8e57a-106">Contiene una lista de direcciones IP binarias a las que se deniega el acceso a un servidor LDAP.</span><span class="sxs-lookup"><span data-stu-id="8e57a-106">Holds a list of binary IP addresses that are denied access to an LDAP server.</span></span>



| <span data-ttu-id="8e57a-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="8e57a-107">Entry</span></span> | <span data-ttu-id="8e57a-108">Value</span><span class="sxs-lookup"><span data-stu-id="8e57a-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="8e57a-109">CN</span><span class="sxs-lookup"><span data-stu-id="8e57a-109">CN</span></span>                | <span data-ttu-id="8e57a-110">LDAP-IPDeny-List</span><span class="sxs-lookup"><span data-stu-id="8e57a-110">LDAP-IPDeny-List</span></span>                                      |
| <span data-ttu-id="8e57a-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="8e57a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8e57a-112">lDAPIPDenyList</span><span class="sxs-lookup"><span data-stu-id="8e57a-112">lDAPIPDenyList</span></span>                                        |
| <span data-ttu-id="8e57a-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="8e57a-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="8e57a-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="8e57a-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="8e57a-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="8e57a-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="8e57a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8e57a-116">Attribute-Id</span></span>      | <span data-ttu-id="8e57a-117">1.2.840.113556.1.4.844</span><span class="sxs-lookup"><span data-stu-id="8e57a-117">1.2.840.113556.1.4.844</span></span>                                |
| <span data-ttu-id="8e57a-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8e57a-118">System-Id-Guid</span></span>    | <span data-ttu-id="8e57a-119">7359a353-90f7-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8e57a-119">7359a353-90f7-11d1-aebc-0000f80367c1</span></span>                  |
| <span data-ttu-id="8e57a-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e57a-120">Syntax</span></span>            | [<span data-ttu-id="8e57a-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="8e57a-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="8e57a-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="8e57a-122">Implementations</span></span>

-   [<span data-ttu-id="8e57a-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8e57a-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8e57a-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8e57a-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8e57a-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8e57a-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8e57a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8e57a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8e57a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8e57a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8e57a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8e57a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8e57a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8e57a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8e57a-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8e57a-130">Windows 2000 Server</span></span>



| <span data-ttu-id="8e57a-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="8e57a-131">Entry</span></span> | <span data-ttu-id="8e57a-132">Value</span><span class="sxs-lookup"><span data-stu-id="8e57a-132">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8e57a-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8e57a-133">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8e57a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e57a-134">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="8e57a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e57a-135">System-Only</span></span>            | <span data-ttu-id="8e57a-136">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-136">False</span></span>                                            |
| <span data-ttu-id="8e57a-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8e57a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="8e57a-138">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-138">False</span></span>                                            |
| <span data-ttu-id="8e57a-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8e57a-139">Is Indexed</span></span>             | <span data-ttu-id="8e57a-140">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-140">False</span></span>                                            |
| <span data-ttu-id="8e57a-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8e57a-141">In Global Catalog</span></span>      | <span data-ttu-id="8e57a-142">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-142">False</span></span>                                            |
| <span data-ttu-id="8e57a-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8e57a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e57a-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e57a-144">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8e57a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e57a-145">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8e57a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e57a-146">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8e57a-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e57a-147">Search-Flags</span></span>           | <span data-ttu-id="8e57a-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e57a-148">0x00000000</span></span>                                       |
| <span data-ttu-id="8e57a-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e57a-149">System-Flags</span></span>           | <span data-ttu-id="8e57a-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e57a-150">0x00000010</span></span>                                       |
| <span data-ttu-id="8e57a-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8e57a-151">Classes used in</span></span>        | [<span data-ttu-id="8e57a-152">**Directiva de consulta**</span><span class="sxs-lookup"><span data-stu-id="8e57a-152">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8e57a-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8e57a-153">Windows Server 2003</span></span>



| <span data-ttu-id="8e57a-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="8e57a-154">Entry</span></span> | <span data-ttu-id="8e57a-155">Value</span><span class="sxs-lookup"><span data-stu-id="8e57a-155">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8e57a-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8e57a-156">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8e57a-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e57a-157">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="8e57a-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e57a-158">System-Only</span></span>            | <span data-ttu-id="8e57a-159">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-159">False</span></span>                                            |
| <span data-ttu-id="8e57a-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8e57a-160">Is-Single-Valued</span></span>       | <span data-ttu-id="8e57a-161">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-161">False</span></span>                                            |
| <span data-ttu-id="8e57a-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8e57a-162">Is Indexed</span></span>             | <span data-ttu-id="8e57a-163">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-163">False</span></span>                                            |
| <span data-ttu-id="8e57a-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8e57a-164">In Global Catalog</span></span>      | <span data-ttu-id="8e57a-165">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-165">False</span></span>                                            |
| <span data-ttu-id="8e57a-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8e57a-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e57a-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e57a-167">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8e57a-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e57a-168">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8e57a-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e57a-169">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8e57a-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e57a-170">Search-Flags</span></span>           | <span data-ttu-id="8e57a-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e57a-171">0x00000000</span></span>                                       |
| <span data-ttu-id="8e57a-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e57a-172">System-Flags</span></span>           | <span data-ttu-id="8e57a-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e57a-173">0x00000010</span></span>                                       |
| <span data-ttu-id="8e57a-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8e57a-174">Classes used in</span></span>        | [<span data-ttu-id="8e57a-175">**Directiva de consulta**</span><span class="sxs-lookup"><span data-stu-id="8e57a-175">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8e57a-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="8e57a-176">ADAM</span></span>



| <span data-ttu-id="8e57a-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="8e57a-177">Entry</span></span> | <span data-ttu-id="8e57a-178">Value</span><span class="sxs-lookup"><span data-stu-id="8e57a-178">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8e57a-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8e57a-179">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8e57a-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e57a-180">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="8e57a-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e57a-181">System-Only</span></span>            | <span data-ttu-id="8e57a-182">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-182">False</span></span>                                            |
| <span data-ttu-id="8e57a-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8e57a-183">Is-Single-Valued</span></span>       | <span data-ttu-id="8e57a-184">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-184">False</span></span>                                            |
| <span data-ttu-id="8e57a-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8e57a-185">Is Indexed</span></span>             | <span data-ttu-id="8e57a-186">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-186">False</span></span>                                            |
| <span data-ttu-id="8e57a-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8e57a-187">In Global Catalog</span></span>      | <span data-ttu-id="8e57a-188">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-188">False</span></span>                                            |
| <span data-ttu-id="8e57a-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8e57a-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e57a-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e57a-190">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8e57a-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e57a-191">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8e57a-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e57a-192">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8e57a-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e57a-193">Search-Flags</span></span>           | <span data-ttu-id="8e57a-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e57a-194">0x00000000</span></span>                                       |
| <span data-ttu-id="8e57a-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e57a-195">System-Flags</span></span>           | <span data-ttu-id="8e57a-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e57a-196">0x00000010</span></span>                                       |
| <span data-ttu-id="8e57a-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8e57a-197">Classes used in</span></span>        | [<span data-ttu-id="8e57a-198">**Directiva de consulta**</span><span class="sxs-lookup"><span data-stu-id="8e57a-198">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8e57a-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8e57a-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8e57a-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="8e57a-200">Entry</span></span> | <span data-ttu-id="8e57a-201">Value</span><span class="sxs-lookup"><span data-stu-id="8e57a-201">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8e57a-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8e57a-202">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8e57a-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e57a-203">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="8e57a-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e57a-204">System-Only</span></span>            | <span data-ttu-id="8e57a-205">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-205">False</span></span>                                            |
| <span data-ttu-id="8e57a-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8e57a-206">Is-Single-Valued</span></span>       | <span data-ttu-id="8e57a-207">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-207">False</span></span>                                            |
| <span data-ttu-id="8e57a-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8e57a-208">Is Indexed</span></span>             | <span data-ttu-id="8e57a-209">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-209">False</span></span>                                            |
| <span data-ttu-id="8e57a-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8e57a-210">In Global Catalog</span></span>      | <span data-ttu-id="8e57a-211">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-211">False</span></span>                                            |
| <span data-ttu-id="8e57a-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8e57a-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e57a-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e57a-213">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8e57a-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e57a-214">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8e57a-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e57a-215">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8e57a-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e57a-216">Search-Flags</span></span>           | <span data-ttu-id="8e57a-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e57a-217">0x00000000</span></span>                                       |
| <span data-ttu-id="8e57a-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e57a-218">System-Flags</span></span>           | <span data-ttu-id="8e57a-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e57a-219">0x00000010</span></span>                                       |
| <span data-ttu-id="8e57a-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8e57a-220">Classes used in</span></span>        | [<span data-ttu-id="8e57a-221">**Directiva de consulta**</span><span class="sxs-lookup"><span data-stu-id="8e57a-221">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8e57a-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e57a-222">Windows Server 2008</span></span>



| <span data-ttu-id="8e57a-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="8e57a-223">Entry</span></span> | <span data-ttu-id="8e57a-224">Value</span><span class="sxs-lookup"><span data-stu-id="8e57a-224">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8e57a-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8e57a-225">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8e57a-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e57a-226">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="8e57a-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e57a-227">System-Only</span></span>            | <span data-ttu-id="8e57a-228">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-228">False</span></span>                                            |
| <span data-ttu-id="8e57a-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8e57a-229">Is-Single-Valued</span></span>       | <span data-ttu-id="8e57a-230">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-230">False</span></span>                                            |
| <span data-ttu-id="8e57a-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8e57a-231">Is Indexed</span></span>             | <span data-ttu-id="8e57a-232">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-232">False</span></span>                                            |
| <span data-ttu-id="8e57a-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8e57a-233">In Global Catalog</span></span>      | <span data-ttu-id="8e57a-234">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-234">False</span></span>                                            |
| <span data-ttu-id="8e57a-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8e57a-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e57a-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e57a-236">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8e57a-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e57a-237">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8e57a-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e57a-238">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8e57a-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e57a-239">Search-Flags</span></span>           | <span data-ttu-id="8e57a-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e57a-240">0x00000000</span></span>                                       |
| <span data-ttu-id="8e57a-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e57a-241">System-Flags</span></span>           | <span data-ttu-id="8e57a-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e57a-242">0x00000010</span></span>                                       |
| <span data-ttu-id="8e57a-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8e57a-243">Classes used in</span></span>        | [<span data-ttu-id="8e57a-244">**Directiva de consulta**</span><span class="sxs-lookup"><span data-stu-id="8e57a-244">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8e57a-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8e57a-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8e57a-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="8e57a-246">Entry</span></span> | <span data-ttu-id="8e57a-247">Value</span><span class="sxs-lookup"><span data-stu-id="8e57a-247">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8e57a-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8e57a-248">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8e57a-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e57a-249">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="8e57a-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e57a-250">System-Only</span></span>            | <span data-ttu-id="8e57a-251">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-251">False</span></span>                                            |
| <span data-ttu-id="8e57a-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8e57a-252">Is-Single-Valued</span></span>       | <span data-ttu-id="8e57a-253">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-253">False</span></span>                                            |
| <span data-ttu-id="8e57a-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8e57a-254">Is Indexed</span></span>             | <span data-ttu-id="8e57a-255">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-255">False</span></span>                                            |
| <span data-ttu-id="8e57a-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8e57a-256">In Global Catalog</span></span>      | <span data-ttu-id="8e57a-257">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-257">False</span></span>                                            |
| <span data-ttu-id="8e57a-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8e57a-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e57a-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e57a-259">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8e57a-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e57a-260">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8e57a-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e57a-261">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8e57a-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e57a-262">Search-Flags</span></span>           | <span data-ttu-id="8e57a-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e57a-263">0x00000000</span></span>                                       |
| <span data-ttu-id="8e57a-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e57a-264">System-Flags</span></span>           | <span data-ttu-id="8e57a-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e57a-265">0x00000010</span></span>                                       |
| <span data-ttu-id="8e57a-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8e57a-266">Classes used in</span></span>        | [<span data-ttu-id="8e57a-267">**Directiva de consulta**</span><span class="sxs-lookup"><span data-stu-id="8e57a-267">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8e57a-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8e57a-268">Windows Server 2012</span></span>



| <span data-ttu-id="8e57a-269">Entrada</span><span class="sxs-lookup"><span data-stu-id="8e57a-269">Entry</span></span> | <span data-ttu-id="8e57a-270">Value</span><span class="sxs-lookup"><span data-stu-id="8e57a-270">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8e57a-271">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8e57a-271">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8e57a-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e57a-272">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="8e57a-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e57a-273">System-Only</span></span>            | <span data-ttu-id="8e57a-274">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-274">False</span></span>                                            |
| <span data-ttu-id="8e57a-275">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8e57a-275">Is-Single-Valued</span></span>       | <span data-ttu-id="8e57a-276">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-276">False</span></span>                                            |
| <span data-ttu-id="8e57a-277">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8e57a-277">Is Indexed</span></span>             | <span data-ttu-id="8e57a-278">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-278">False</span></span>                                            |
| <span data-ttu-id="8e57a-279">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8e57a-279">In Global Catalog</span></span>      | <span data-ttu-id="8e57a-280">False</span><span class="sxs-lookup"><span data-stu-id="8e57a-280">False</span></span>                                            |
| <span data-ttu-id="8e57a-281">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8e57a-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e57a-282">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e57a-282">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8e57a-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e57a-283">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8e57a-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e57a-284">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8e57a-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e57a-285">Search-Flags</span></span>           | <span data-ttu-id="8e57a-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e57a-286">0x00000000</span></span>                                       |
| <span data-ttu-id="8e57a-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e57a-287">System-Flags</span></span>           | <span data-ttu-id="8e57a-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e57a-288">0x00000010</span></span>                                       |
| <span data-ttu-id="8e57a-289">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8e57a-289">Classes used in</span></span>        | [<span data-ttu-id="8e57a-290">**Directiva de consulta**</span><span class="sxs-lookup"><span data-stu-id="8e57a-290">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



 

 





