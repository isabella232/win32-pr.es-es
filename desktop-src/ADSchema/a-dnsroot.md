---
title: Dns-Root atributo)
description: El nombre de dominio DNS superior asignado a una partición de dominio o directorio.
ms.assetid: 0b33daad-b5c5-4126-86fa-abd3e0006c5f
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Dns-Root
- dnsRoot esquema de AD de atributos
topic_type:
- apiref
api_name:
- Dns-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2c2fd2c39e8f0015d7641eccd27279b3478ec4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658653"
---
# <a name="dns-root-attribute"></a><span data-ttu-id="08a47-105">Dns-Root atributo)</span><span class="sxs-lookup"><span data-stu-id="08a47-105">Dns-Root attribute</span></span>

<span data-ttu-id="08a47-106">El nombre de dominio DNS superior asignado a una partición de dominio o directorio.</span><span class="sxs-lookup"><span data-stu-id="08a47-106">The uppermost DNS domain name assigned to a domain/directory partition.</span></span> <span data-ttu-id="08a47-107">Se establece en un objeto crossRef y se usa, entre otras cosas, para la generación de referencias.</span><span class="sxs-lookup"><span data-stu-id="08a47-107">This is set on a crossRef object and is used, among other things, for referral generation.</span></span> <span data-ttu-id="08a47-108">Al buscar a través de un árbol de dominios completo, se debe iniciar la búsqueda en el objeto Dns-Root.</span><span class="sxs-lookup"><span data-stu-id="08a47-108">When searching through an entire domain tree, the search must be initiated at the Dns-Root object.</span></span> <span data-ttu-id="08a47-109">Este atributo puede tener varios valores, en cuyo caso se generan varias referencias.</span><span class="sxs-lookup"><span data-stu-id="08a47-109">This attribute can be multi-valued, in which case multiple referrals are generated.</span></span>



| <span data-ttu-id="08a47-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="08a47-110">Entry</span></span> | <span data-ttu-id="08a47-111">Value</span><span class="sxs-lookup"><span data-stu-id="08a47-111">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="08a47-112">CN</span><span class="sxs-lookup"><span data-stu-id="08a47-112">CN</span></span>                | <span data-ttu-id="08a47-113">Dns-Root</span><span class="sxs-lookup"><span data-stu-id="08a47-113">Dns-Root</span></span>                                    |
| <span data-ttu-id="08a47-114">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="08a47-114">Ldap-Display-Name</span></span> | <span data-ttu-id="08a47-115">dnsRoot</span><span class="sxs-lookup"><span data-stu-id="08a47-115">dnsRoot</span></span>                                     |
| <span data-ttu-id="08a47-116">Tamaño</span><span class="sxs-lookup"><span data-stu-id="08a47-116">Size</span></span>              | \-                                          |
| <span data-ttu-id="08a47-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="08a47-117">Update Privilege</span></span>  | <span data-ttu-id="08a47-118">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="08a47-118">This value is set by the system.</span></span>            |
| <span data-ttu-id="08a47-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="08a47-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="08a47-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="08a47-120">Attribute-Id</span></span>      | <span data-ttu-id="08a47-121">1.2.840.113556.1.4.28</span><span class="sxs-lookup"><span data-stu-id="08a47-121">1.2.840.113556.1.4.28</span></span>                       |
| <span data-ttu-id="08a47-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="08a47-122">System-Id-Guid</span></span>    | <span data-ttu-id="08a47-123">bf967959-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="08a47-123">bf967959-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="08a47-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08a47-124">Syntax</span></span>            | [<span data-ttu-id="08a47-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="08a47-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="08a47-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="08a47-126">Implementations</span></span>

-   [<span data-ttu-id="08a47-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="08a47-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="08a47-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="08a47-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="08a47-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="08a47-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="08a47-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="08a47-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="08a47-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="08a47-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="08a47-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="08a47-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="08a47-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="08a47-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="08a47-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="08a47-134">Windows 2000 Server</span></span>



| <span data-ttu-id="08a47-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="08a47-135">Entry</span></span> | <span data-ttu-id="08a47-136">Value</span><span class="sxs-lookup"><span data-stu-id="08a47-136">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="08a47-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08a47-137">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="08a47-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08a47-138">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="08a47-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="08a47-139">System-Only</span></span>            | <span data-ttu-id="08a47-140">False</span><span class="sxs-lookup"><span data-stu-id="08a47-140">False</span></span>                                      |
| <span data-ttu-id="08a47-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08a47-141">Is-Single-Valued</span></span>       | <span data-ttu-id="08a47-142">False</span><span class="sxs-lookup"><span data-stu-id="08a47-142">False</span></span>                                      |
| <span data-ttu-id="08a47-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08a47-143">Is Indexed</span></span>             | <span data-ttu-id="08a47-144">True</span><span class="sxs-lookup"><span data-stu-id="08a47-144">True</span></span>                                       |
| <span data-ttu-id="08a47-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08a47-145">In Global Catalog</span></span>      | <span data-ttu-id="08a47-146">False</span><span class="sxs-lookup"><span data-stu-id="08a47-146">False</span></span>                                      |
| <span data-ttu-id="08a47-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08a47-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="08a47-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08a47-148">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="08a47-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08a47-149">Range-Lower</span></span>            | <span data-ttu-id="08a47-150">1</span><span class="sxs-lookup"><span data-stu-id="08a47-150">1</span></span>                                          |
| <span data-ttu-id="08a47-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08a47-151">Range-Upper</span></span>            | <span data-ttu-id="08a47-152">255</span><span class="sxs-lookup"><span data-stu-id="08a47-152">255</span></span>                                        |
| <span data-ttu-id="08a47-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08a47-153">Search-Flags</span></span>           | <span data-ttu-id="08a47-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="08a47-154">0x00000001</span></span>                                 |
| <span data-ttu-id="08a47-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08a47-155">System-Flags</span></span>           | <span data-ttu-id="08a47-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08a47-156">0x00000010</span></span>                                 |
| <span data-ttu-id="08a47-157">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08a47-157">Classes used in</span></span>        | [<span data-ttu-id="08a47-158">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="08a47-158">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="08a47-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="08a47-159">Windows Server 2003</span></span>



| <span data-ttu-id="08a47-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="08a47-160">Entry</span></span> | <span data-ttu-id="08a47-161">Value</span><span class="sxs-lookup"><span data-stu-id="08a47-161">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="08a47-162">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08a47-162">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="08a47-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08a47-163">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="08a47-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="08a47-164">System-Only</span></span>            | <span data-ttu-id="08a47-165">False</span><span class="sxs-lookup"><span data-stu-id="08a47-165">False</span></span>                                      |
| <span data-ttu-id="08a47-166">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08a47-166">Is-Single-Valued</span></span>       | <span data-ttu-id="08a47-167">False</span><span class="sxs-lookup"><span data-stu-id="08a47-167">False</span></span>                                      |
| <span data-ttu-id="08a47-168">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08a47-168">Is Indexed</span></span>             | <span data-ttu-id="08a47-169">True</span><span class="sxs-lookup"><span data-stu-id="08a47-169">True</span></span>                                       |
| <span data-ttu-id="08a47-170">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08a47-170">In Global Catalog</span></span>      | <span data-ttu-id="08a47-171">False</span><span class="sxs-lookup"><span data-stu-id="08a47-171">False</span></span>                                      |
| <span data-ttu-id="08a47-172">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08a47-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="08a47-173">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08a47-173">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="08a47-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08a47-174">Range-Lower</span></span>            | <span data-ttu-id="08a47-175">1</span><span class="sxs-lookup"><span data-stu-id="08a47-175">1</span></span>                                          |
| <span data-ttu-id="08a47-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08a47-176">Range-Upper</span></span>            | <span data-ttu-id="08a47-177">255</span><span class="sxs-lookup"><span data-stu-id="08a47-177">255</span></span>                                        |
| <span data-ttu-id="08a47-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08a47-178">Search-Flags</span></span>           | <span data-ttu-id="08a47-179">0x00000001</span><span class="sxs-lookup"><span data-stu-id="08a47-179">0x00000001</span></span>                                 |
| <span data-ttu-id="08a47-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08a47-180">System-Flags</span></span>           | <span data-ttu-id="08a47-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08a47-181">0x00000010</span></span>                                 |
| <span data-ttu-id="08a47-182">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08a47-182">Classes used in</span></span>        | [<span data-ttu-id="08a47-183">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="08a47-183">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="08a47-184">ADAM</span><span class="sxs-lookup"><span data-stu-id="08a47-184">ADAM</span></span>



| <span data-ttu-id="08a47-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="08a47-185">Entry</span></span> | <span data-ttu-id="08a47-186">Value</span><span class="sxs-lookup"><span data-stu-id="08a47-186">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="08a47-187">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08a47-187">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="08a47-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08a47-188">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="08a47-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="08a47-189">System-Only</span></span>            | <span data-ttu-id="08a47-190">False</span><span class="sxs-lookup"><span data-stu-id="08a47-190">False</span></span>                                      |
| <span data-ttu-id="08a47-191">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08a47-191">Is-Single-Valued</span></span>       | <span data-ttu-id="08a47-192">False</span><span class="sxs-lookup"><span data-stu-id="08a47-192">False</span></span>                                      |
| <span data-ttu-id="08a47-193">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08a47-193">Is Indexed</span></span>             | <span data-ttu-id="08a47-194">True</span><span class="sxs-lookup"><span data-stu-id="08a47-194">True</span></span>                                       |
| <span data-ttu-id="08a47-195">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08a47-195">In Global Catalog</span></span>      | <span data-ttu-id="08a47-196">False</span><span class="sxs-lookup"><span data-stu-id="08a47-196">False</span></span>                                      |
| <span data-ttu-id="08a47-197">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08a47-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="08a47-198">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08a47-198">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="08a47-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08a47-199">Range-Lower</span></span>            | <span data-ttu-id="08a47-200">1</span><span class="sxs-lookup"><span data-stu-id="08a47-200">1</span></span>                                          |
| <span data-ttu-id="08a47-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08a47-201">Range-Upper</span></span>            | <span data-ttu-id="08a47-202">255</span><span class="sxs-lookup"><span data-stu-id="08a47-202">255</span></span>                                        |
| <span data-ttu-id="08a47-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08a47-203">Search-Flags</span></span>           | <span data-ttu-id="08a47-204">0x00000001</span><span class="sxs-lookup"><span data-stu-id="08a47-204">0x00000001</span></span>                                 |
| <span data-ttu-id="08a47-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08a47-205">System-Flags</span></span>           | <span data-ttu-id="08a47-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08a47-206">0x00000010</span></span>                                 |
| <span data-ttu-id="08a47-207">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08a47-207">Classes used in</span></span>        | [<span data-ttu-id="08a47-208">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="08a47-208">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="08a47-209">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="08a47-209">Windows Server 2003 R2</span></span>



| <span data-ttu-id="08a47-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="08a47-210">Entry</span></span> | <span data-ttu-id="08a47-211">Value</span><span class="sxs-lookup"><span data-stu-id="08a47-211">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="08a47-212">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08a47-212">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="08a47-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08a47-213">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="08a47-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="08a47-214">System-Only</span></span>            | <span data-ttu-id="08a47-215">False</span><span class="sxs-lookup"><span data-stu-id="08a47-215">False</span></span>                                      |
| <span data-ttu-id="08a47-216">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08a47-216">Is-Single-Valued</span></span>       | <span data-ttu-id="08a47-217">False</span><span class="sxs-lookup"><span data-stu-id="08a47-217">False</span></span>                                      |
| <span data-ttu-id="08a47-218">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08a47-218">Is Indexed</span></span>             | <span data-ttu-id="08a47-219">True</span><span class="sxs-lookup"><span data-stu-id="08a47-219">True</span></span>                                       |
| <span data-ttu-id="08a47-220">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08a47-220">In Global Catalog</span></span>      | <span data-ttu-id="08a47-221">False</span><span class="sxs-lookup"><span data-stu-id="08a47-221">False</span></span>                                      |
| <span data-ttu-id="08a47-222">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08a47-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="08a47-223">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08a47-223">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="08a47-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08a47-224">Range-Lower</span></span>            | <span data-ttu-id="08a47-225">1</span><span class="sxs-lookup"><span data-stu-id="08a47-225">1</span></span>                                          |
| <span data-ttu-id="08a47-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08a47-226">Range-Upper</span></span>            | <span data-ttu-id="08a47-227">255</span><span class="sxs-lookup"><span data-stu-id="08a47-227">255</span></span>                                        |
| <span data-ttu-id="08a47-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08a47-228">Search-Flags</span></span>           | <span data-ttu-id="08a47-229">0x00000001</span><span class="sxs-lookup"><span data-stu-id="08a47-229">0x00000001</span></span>                                 |
| <span data-ttu-id="08a47-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08a47-230">System-Flags</span></span>           | <span data-ttu-id="08a47-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08a47-231">0x00000010</span></span>                                 |
| <span data-ttu-id="08a47-232">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08a47-232">Classes used in</span></span>        | [<span data-ttu-id="08a47-233">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="08a47-233">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="08a47-234">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08a47-234">Windows Server 2008</span></span>



| <span data-ttu-id="08a47-235">Entrada</span><span class="sxs-lookup"><span data-stu-id="08a47-235">Entry</span></span> | <span data-ttu-id="08a47-236">Value</span><span class="sxs-lookup"><span data-stu-id="08a47-236">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="08a47-237">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08a47-237">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="08a47-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08a47-238">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="08a47-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="08a47-239">System-Only</span></span>            | <span data-ttu-id="08a47-240">False</span><span class="sxs-lookup"><span data-stu-id="08a47-240">False</span></span>                                      |
| <span data-ttu-id="08a47-241">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08a47-241">Is-Single-Valued</span></span>       | <span data-ttu-id="08a47-242">False</span><span class="sxs-lookup"><span data-stu-id="08a47-242">False</span></span>                                      |
| <span data-ttu-id="08a47-243">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08a47-243">Is Indexed</span></span>             | <span data-ttu-id="08a47-244">True</span><span class="sxs-lookup"><span data-stu-id="08a47-244">True</span></span>                                       |
| <span data-ttu-id="08a47-245">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08a47-245">In Global Catalog</span></span>      | <span data-ttu-id="08a47-246">False</span><span class="sxs-lookup"><span data-stu-id="08a47-246">False</span></span>                                      |
| <span data-ttu-id="08a47-247">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08a47-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="08a47-248">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08a47-248">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="08a47-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08a47-249">Range-Lower</span></span>            | <span data-ttu-id="08a47-250">1</span><span class="sxs-lookup"><span data-stu-id="08a47-250">1</span></span>                                          |
| <span data-ttu-id="08a47-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08a47-251">Range-Upper</span></span>            | <span data-ttu-id="08a47-252">255</span><span class="sxs-lookup"><span data-stu-id="08a47-252">255</span></span>                                        |
| <span data-ttu-id="08a47-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08a47-253">Search-Flags</span></span>           | <span data-ttu-id="08a47-254">0x00000001</span><span class="sxs-lookup"><span data-stu-id="08a47-254">0x00000001</span></span>                                 |
| <span data-ttu-id="08a47-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08a47-255">System-Flags</span></span>           | <span data-ttu-id="08a47-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08a47-256">0x00000010</span></span>                                 |
| <span data-ttu-id="08a47-257">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08a47-257">Classes used in</span></span>        | [<span data-ttu-id="08a47-258">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="08a47-258">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="08a47-259">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="08a47-259">Windows Server 2008 R2</span></span>



| <span data-ttu-id="08a47-260">Entrada</span><span class="sxs-lookup"><span data-stu-id="08a47-260">Entry</span></span> | <span data-ttu-id="08a47-261">Value</span><span class="sxs-lookup"><span data-stu-id="08a47-261">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="08a47-262">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08a47-262">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="08a47-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08a47-263">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="08a47-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="08a47-264">System-Only</span></span>            | <span data-ttu-id="08a47-265">False</span><span class="sxs-lookup"><span data-stu-id="08a47-265">False</span></span>                                      |
| <span data-ttu-id="08a47-266">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08a47-266">Is-Single-Valued</span></span>       | <span data-ttu-id="08a47-267">False</span><span class="sxs-lookup"><span data-stu-id="08a47-267">False</span></span>                                      |
| <span data-ttu-id="08a47-268">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08a47-268">Is Indexed</span></span>             | <span data-ttu-id="08a47-269">True</span><span class="sxs-lookup"><span data-stu-id="08a47-269">True</span></span>                                       |
| <span data-ttu-id="08a47-270">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08a47-270">In Global Catalog</span></span>      | <span data-ttu-id="08a47-271">False</span><span class="sxs-lookup"><span data-stu-id="08a47-271">False</span></span>                                      |
| <span data-ttu-id="08a47-272">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08a47-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="08a47-273">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08a47-273">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="08a47-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08a47-274">Range-Lower</span></span>            | <span data-ttu-id="08a47-275">1</span><span class="sxs-lookup"><span data-stu-id="08a47-275">1</span></span>                                          |
| <span data-ttu-id="08a47-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08a47-276">Range-Upper</span></span>            | <span data-ttu-id="08a47-277">255</span><span class="sxs-lookup"><span data-stu-id="08a47-277">255</span></span>                                        |
| <span data-ttu-id="08a47-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08a47-278">Search-Flags</span></span>           | <span data-ttu-id="08a47-279">0x00000001</span><span class="sxs-lookup"><span data-stu-id="08a47-279">0x00000001</span></span>                                 |
| <span data-ttu-id="08a47-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08a47-280">System-Flags</span></span>           | <span data-ttu-id="08a47-281">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08a47-281">0x00000010</span></span>                                 |
| <span data-ttu-id="08a47-282">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08a47-282">Classes used in</span></span>        | [<span data-ttu-id="08a47-283">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="08a47-283">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="08a47-284">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="08a47-284">Windows Server 2012</span></span>



| <span data-ttu-id="08a47-285">Entrada</span><span class="sxs-lookup"><span data-stu-id="08a47-285">Entry</span></span> | <span data-ttu-id="08a47-286">Value</span><span class="sxs-lookup"><span data-stu-id="08a47-286">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="08a47-287">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08a47-287">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="08a47-288">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08a47-288">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="08a47-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="08a47-289">System-Only</span></span>            | <span data-ttu-id="08a47-290">False</span><span class="sxs-lookup"><span data-stu-id="08a47-290">False</span></span>                                      |
| <span data-ttu-id="08a47-291">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08a47-291">Is-Single-Valued</span></span>       | <span data-ttu-id="08a47-292">False</span><span class="sxs-lookup"><span data-stu-id="08a47-292">False</span></span>                                      |
| <span data-ttu-id="08a47-293">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08a47-293">Is Indexed</span></span>             | <span data-ttu-id="08a47-294">True</span><span class="sxs-lookup"><span data-stu-id="08a47-294">True</span></span>                                       |
| <span data-ttu-id="08a47-295">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08a47-295">In Global Catalog</span></span>      | <span data-ttu-id="08a47-296">False</span><span class="sxs-lookup"><span data-stu-id="08a47-296">False</span></span>                                      |
| <span data-ttu-id="08a47-297">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08a47-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="08a47-298">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08a47-298">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="08a47-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08a47-299">Range-Lower</span></span>            | <span data-ttu-id="08a47-300">1</span><span class="sxs-lookup"><span data-stu-id="08a47-300">1</span></span>                                          |
| <span data-ttu-id="08a47-301">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08a47-301">Range-Upper</span></span>            | <span data-ttu-id="08a47-302">255</span><span class="sxs-lookup"><span data-stu-id="08a47-302">255</span></span>                                        |
| <span data-ttu-id="08a47-303">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08a47-303">Search-Flags</span></span>           | <span data-ttu-id="08a47-304">0x00000001</span><span class="sxs-lookup"><span data-stu-id="08a47-304">0x00000001</span></span>                                 |
| <span data-ttu-id="08a47-305">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08a47-305">System-Flags</span></span>           | <span data-ttu-id="08a47-306">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08a47-306">0x00000010</span></span>                                 |
| <span data-ttu-id="08a47-307">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08a47-307">Classes used in</span></span>        | [<span data-ttu-id="08a47-308">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="08a47-308">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





