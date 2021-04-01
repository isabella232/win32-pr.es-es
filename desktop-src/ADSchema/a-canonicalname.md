---
title: Canonical-Name atributo)
description: Nombre del objeto en formato canónico.
ms.assetid: f217e5fa-f70b-4f4d-afa6-53e4f7e8a0e1
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Canonical-Name
- canonicalName esquema de AD de atributos
topic_type:
- apiref
api_name:
- Canonical-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 487476271456fa0465e8d47791f5376f33617eb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906248"
---
# <a name="canonical-name-attribute"></a><span data-ttu-id="70224-105">Canonical-Name atributo)</span><span class="sxs-lookup"><span data-stu-id="70224-105">Canonical-Name attribute</span></span>

<span data-ttu-id="70224-106">Nombre del objeto en formato canónico.</span><span class="sxs-lookup"><span data-stu-id="70224-106">The name of the object in canonical format.</span></span> <span data-ttu-id="70224-107">myserver2.fabrikam.com/users/jeffsmith es un ejemplo de un nombre distintivo en formato canónico.</span><span class="sxs-lookup"><span data-stu-id="70224-107">myserver2.fabrikam.com/users/jeffsmith is an example of a distinguished name in canonical format.</span></span> <span data-ttu-id="70224-108">Este es un atributo construido.</span><span class="sxs-lookup"><span data-stu-id="70224-108">This is a constructed attribute.</span></span> <span data-ttu-id="70224-109">Los resultados devueltos son idénticos a los devueltos por la siguiente función de Active Directory: DsCrackNames (NULL, marca de nombre de DS \_ \_ \_ \_ solo sintáctica, \_ nombre de dominio completo de DS \_ 1779, nombre canónico de \_ DS \_ \_ ,...).</span><span class="sxs-lookup"><span data-stu-id="70224-109">The results returned are identical to those returned by the following Active Directory function: DsCrackNames(NULL, DS\_NAME\_FLAG\_SYNTACTICAL\_ONLY, DS\_FQDN\_1779\_NAME, DS\_CANONICAL\_NAME, ...).</span></span>

<span data-ttu-id="70224-110">Para obtener más información sobre los formatos de nombre, vea [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).</span><span class="sxs-lookup"><span data-stu-id="70224-110">For more information about name formats, see [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).</span></span>



| <span data-ttu-id="70224-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="70224-111">Entry</span></span> | <span data-ttu-id="70224-112">Value</span><span class="sxs-lookup"><span data-stu-id="70224-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="70224-113">CN</span><span class="sxs-lookup"><span data-stu-id="70224-113">CN</span></span>                | <span data-ttu-id="70224-114">Canonical-Name</span><span class="sxs-lookup"><span data-stu-id="70224-114">Canonical-Name</span></span>                              |
| <span data-ttu-id="70224-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="70224-115">Ldap-Display-Name</span></span> | <span data-ttu-id="70224-116">canonicalName</span><span class="sxs-lookup"><span data-stu-id="70224-116">canonicalName</span></span>                               |
| <span data-ttu-id="70224-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="70224-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="70224-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="70224-118">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="70224-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="70224-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="70224-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="70224-120">Attribute-Id</span></span>      | <span data-ttu-id="70224-121">1.2.840.113556.1.4.916</span><span class="sxs-lookup"><span data-stu-id="70224-121">1.2.840.113556.1.4.916</span></span>                      |
| <span data-ttu-id="70224-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="70224-122">System-Id-Guid</span></span>    | <span data-ttu-id="70224-123">9a7ad945-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="70224-123">9a7ad945-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="70224-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70224-124">Syntax</span></span>            | [<span data-ttu-id="70224-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="70224-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="70224-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="70224-126">Implementations</span></span>

-   [<span data-ttu-id="70224-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="70224-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="70224-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="70224-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="70224-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="70224-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="70224-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="70224-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="70224-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="70224-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="70224-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="70224-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="70224-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="70224-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="70224-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="70224-134">Windows 2000 Server</span></span>



| <span data-ttu-id="70224-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="70224-135">Entry</span></span> | <span data-ttu-id="70224-136">Value</span><span class="sxs-lookup"><span data-stu-id="70224-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="70224-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="70224-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="70224-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70224-138">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="70224-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="70224-139">System-Only</span></span>            | <span data-ttu-id="70224-140">True</span><span class="sxs-lookup"><span data-stu-id="70224-140">True</span></span>                            |
| <span data-ttu-id="70224-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="70224-141">Is-Single-Valued</span></span>       | <span data-ttu-id="70224-142">False</span><span class="sxs-lookup"><span data-stu-id="70224-142">False</span></span>                           |
| <span data-ttu-id="70224-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="70224-143">Is Indexed</span></span>             | <span data-ttu-id="70224-144">False</span><span class="sxs-lookup"><span data-stu-id="70224-144">False</span></span>                           |
| <span data-ttu-id="70224-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="70224-145">In Global Catalog</span></span>      | <span data-ttu-id="70224-146">False</span><span class="sxs-lookup"><span data-stu-id="70224-146">False</span></span>                           |
| <span data-ttu-id="70224-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="70224-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="70224-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="70224-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="70224-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70224-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="70224-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70224-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="70224-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70224-151">Search-Flags</span></span>           | <span data-ttu-id="70224-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70224-152">0x00000000</span></span>                      |
| <span data-ttu-id="70224-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70224-153">System-Flags</span></span>           | <span data-ttu-id="70224-154">0x08000014</span><span class="sxs-lookup"><span data-stu-id="70224-154">0x08000014</span></span>                      |
| <span data-ttu-id="70224-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="70224-155">Classes used in</span></span>        | [<span data-ttu-id="70224-156">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="70224-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="70224-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="70224-157">Windows Server 2003</span></span>



| <span data-ttu-id="70224-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="70224-158">Entry</span></span> | <span data-ttu-id="70224-159">Value</span><span class="sxs-lookup"><span data-stu-id="70224-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="70224-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="70224-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="70224-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70224-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="70224-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="70224-162">System-Only</span></span>            | <span data-ttu-id="70224-163">True</span><span class="sxs-lookup"><span data-stu-id="70224-163">True</span></span>                            |
| <span data-ttu-id="70224-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="70224-164">Is-Single-Valued</span></span>       | <span data-ttu-id="70224-165">False</span><span class="sxs-lookup"><span data-stu-id="70224-165">False</span></span>                           |
| <span data-ttu-id="70224-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="70224-166">Is Indexed</span></span>             | <span data-ttu-id="70224-167">False</span><span class="sxs-lookup"><span data-stu-id="70224-167">False</span></span>                           |
| <span data-ttu-id="70224-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="70224-168">In Global Catalog</span></span>      | <span data-ttu-id="70224-169">False</span><span class="sxs-lookup"><span data-stu-id="70224-169">False</span></span>                           |
| <span data-ttu-id="70224-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="70224-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="70224-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="70224-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="70224-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70224-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="70224-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70224-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="70224-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70224-174">Search-Flags</span></span>           | <span data-ttu-id="70224-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70224-175">0x00000000</span></span>                      |
| <span data-ttu-id="70224-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70224-176">System-Flags</span></span>           | <span data-ttu-id="70224-177">0x08000014</span><span class="sxs-lookup"><span data-stu-id="70224-177">0x08000014</span></span>                      |
| <span data-ttu-id="70224-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="70224-178">Classes used in</span></span>        | [<span data-ttu-id="70224-179">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="70224-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="70224-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="70224-180">ADAM</span></span>



| <span data-ttu-id="70224-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="70224-181">Entry</span></span> | <span data-ttu-id="70224-182">Value</span><span class="sxs-lookup"><span data-stu-id="70224-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="70224-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="70224-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="70224-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70224-184">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="70224-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="70224-185">System-Only</span></span>            | <span data-ttu-id="70224-186">True</span><span class="sxs-lookup"><span data-stu-id="70224-186">True</span></span>                            |
| <span data-ttu-id="70224-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="70224-187">Is-Single-Valued</span></span>       | <span data-ttu-id="70224-188">False</span><span class="sxs-lookup"><span data-stu-id="70224-188">False</span></span>                           |
| <span data-ttu-id="70224-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="70224-189">Is Indexed</span></span>             | <span data-ttu-id="70224-190">False</span><span class="sxs-lookup"><span data-stu-id="70224-190">False</span></span>                           |
| <span data-ttu-id="70224-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="70224-191">In Global Catalog</span></span>      | <span data-ttu-id="70224-192">False</span><span class="sxs-lookup"><span data-stu-id="70224-192">False</span></span>                           |
| <span data-ttu-id="70224-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="70224-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="70224-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="70224-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="70224-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70224-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="70224-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70224-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="70224-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70224-197">Search-Flags</span></span>           | <span data-ttu-id="70224-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70224-198">0x00000000</span></span>                      |
| <span data-ttu-id="70224-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70224-199">System-Flags</span></span>           | <span data-ttu-id="70224-200">0x08000014</span><span class="sxs-lookup"><span data-stu-id="70224-200">0x08000014</span></span>                      |
| <span data-ttu-id="70224-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="70224-201">Classes used in</span></span>        | [<span data-ttu-id="70224-202">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="70224-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="70224-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="70224-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="70224-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="70224-204">Entry</span></span> | <span data-ttu-id="70224-205">Value</span><span class="sxs-lookup"><span data-stu-id="70224-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="70224-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="70224-206">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="70224-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70224-207">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="70224-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="70224-208">System-Only</span></span>            | <span data-ttu-id="70224-209">True</span><span class="sxs-lookup"><span data-stu-id="70224-209">True</span></span>                            |
| <span data-ttu-id="70224-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="70224-210">Is-Single-Valued</span></span>       | <span data-ttu-id="70224-211">False</span><span class="sxs-lookup"><span data-stu-id="70224-211">False</span></span>                           |
| <span data-ttu-id="70224-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="70224-212">Is Indexed</span></span>             | <span data-ttu-id="70224-213">False</span><span class="sxs-lookup"><span data-stu-id="70224-213">False</span></span>                           |
| <span data-ttu-id="70224-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="70224-214">In Global Catalog</span></span>      | <span data-ttu-id="70224-215">False</span><span class="sxs-lookup"><span data-stu-id="70224-215">False</span></span>                           |
| <span data-ttu-id="70224-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="70224-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="70224-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="70224-217">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="70224-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70224-218">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="70224-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70224-219">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="70224-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70224-220">Search-Flags</span></span>           | <span data-ttu-id="70224-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70224-221">0x00000000</span></span>                      |
| <span data-ttu-id="70224-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70224-222">System-Flags</span></span>           | <span data-ttu-id="70224-223">0x08000014</span><span class="sxs-lookup"><span data-stu-id="70224-223">0x08000014</span></span>                      |
| <span data-ttu-id="70224-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="70224-224">Classes used in</span></span>        | [<span data-ttu-id="70224-225">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="70224-225">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="70224-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70224-226">Windows Server 2008</span></span>



| <span data-ttu-id="70224-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="70224-227">Entry</span></span> | <span data-ttu-id="70224-228">Value</span><span class="sxs-lookup"><span data-stu-id="70224-228">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="70224-229">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="70224-229">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="70224-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70224-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="70224-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="70224-231">System-Only</span></span>            | <span data-ttu-id="70224-232">True</span><span class="sxs-lookup"><span data-stu-id="70224-232">True</span></span>                            |
| <span data-ttu-id="70224-233">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="70224-233">Is-Single-Valued</span></span>       | <span data-ttu-id="70224-234">False</span><span class="sxs-lookup"><span data-stu-id="70224-234">False</span></span>                           |
| <span data-ttu-id="70224-235">Está indexado</span><span class="sxs-lookup"><span data-stu-id="70224-235">Is Indexed</span></span>             | <span data-ttu-id="70224-236">False</span><span class="sxs-lookup"><span data-stu-id="70224-236">False</span></span>                           |
| <span data-ttu-id="70224-237">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="70224-237">In Global Catalog</span></span>      | <span data-ttu-id="70224-238">False</span><span class="sxs-lookup"><span data-stu-id="70224-238">False</span></span>                           |
| <span data-ttu-id="70224-239">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="70224-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="70224-240">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="70224-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="70224-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70224-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="70224-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70224-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="70224-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70224-243">Search-Flags</span></span>           | <span data-ttu-id="70224-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70224-244">0x00000000</span></span>                      |
| <span data-ttu-id="70224-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70224-245">System-Flags</span></span>           | <span data-ttu-id="70224-246">0x08000014</span><span class="sxs-lookup"><span data-stu-id="70224-246">0x08000014</span></span>                      |
| <span data-ttu-id="70224-247">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="70224-247">Classes used in</span></span>        | [<span data-ttu-id="70224-248">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="70224-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="70224-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="70224-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="70224-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="70224-250">Entry</span></span> | <span data-ttu-id="70224-251">Value</span><span class="sxs-lookup"><span data-stu-id="70224-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="70224-252">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="70224-252">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="70224-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70224-253">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="70224-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="70224-254">System-Only</span></span>            | <span data-ttu-id="70224-255">True</span><span class="sxs-lookup"><span data-stu-id="70224-255">True</span></span>                            |
| <span data-ttu-id="70224-256">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="70224-256">Is-Single-Valued</span></span>       | <span data-ttu-id="70224-257">False</span><span class="sxs-lookup"><span data-stu-id="70224-257">False</span></span>                           |
| <span data-ttu-id="70224-258">Está indexado</span><span class="sxs-lookup"><span data-stu-id="70224-258">Is Indexed</span></span>             | <span data-ttu-id="70224-259">False</span><span class="sxs-lookup"><span data-stu-id="70224-259">False</span></span>                           |
| <span data-ttu-id="70224-260">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="70224-260">In Global Catalog</span></span>      | <span data-ttu-id="70224-261">False</span><span class="sxs-lookup"><span data-stu-id="70224-261">False</span></span>                           |
| <span data-ttu-id="70224-262">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="70224-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="70224-263">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="70224-263">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="70224-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70224-264">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="70224-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70224-265">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="70224-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70224-266">Search-Flags</span></span>           | <span data-ttu-id="70224-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70224-267">0x00000000</span></span>                      |
| <span data-ttu-id="70224-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70224-268">System-Flags</span></span>           | <span data-ttu-id="70224-269">0x08000014</span><span class="sxs-lookup"><span data-stu-id="70224-269">0x08000014</span></span>                      |
| <span data-ttu-id="70224-270">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="70224-270">Classes used in</span></span>        | [<span data-ttu-id="70224-271">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="70224-271">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="70224-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="70224-272">Windows Server 2012</span></span>



| <span data-ttu-id="70224-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="70224-273">Entry</span></span> | <span data-ttu-id="70224-274">Value</span><span class="sxs-lookup"><span data-stu-id="70224-274">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="70224-275">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="70224-275">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="70224-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70224-276">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="70224-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="70224-277">System-Only</span></span>            | <span data-ttu-id="70224-278">True</span><span class="sxs-lookup"><span data-stu-id="70224-278">True</span></span>                            |
| <span data-ttu-id="70224-279">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="70224-279">Is-Single-Valued</span></span>       | <span data-ttu-id="70224-280">False</span><span class="sxs-lookup"><span data-stu-id="70224-280">False</span></span>                           |
| <span data-ttu-id="70224-281">Está indexado</span><span class="sxs-lookup"><span data-stu-id="70224-281">Is Indexed</span></span>             | <span data-ttu-id="70224-282">False</span><span class="sxs-lookup"><span data-stu-id="70224-282">False</span></span>                           |
| <span data-ttu-id="70224-283">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="70224-283">In Global Catalog</span></span>      | <span data-ttu-id="70224-284">False</span><span class="sxs-lookup"><span data-stu-id="70224-284">False</span></span>                           |
| <span data-ttu-id="70224-285">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="70224-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="70224-286">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="70224-286">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="70224-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70224-287">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="70224-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70224-288">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="70224-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70224-289">Search-Flags</span></span>           | <span data-ttu-id="70224-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70224-290">0x00000000</span></span>                      |
| <span data-ttu-id="70224-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70224-291">System-Flags</span></span>           | <span data-ttu-id="70224-292">0x08000014</span><span class="sxs-lookup"><span data-stu-id="70224-292">0x08000014</span></span>                      |
| <span data-ttu-id="70224-293">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="70224-293">Classes used in</span></span>        | [<span data-ttu-id="70224-294">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="70224-294">**Top**</span></span>](c-top.md)<br/> |



 

