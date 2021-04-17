---
title: RDN (atributo)
description: Nombre distintivo relativo (RDN) de un objeto.
ms.assetid: 07fe0e81-1b18-4dbb-abca-a059a8bf993e
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos RDN
- atributo de nombre esquema de AD
topic_type:
- apiref
api_name:
- RDN
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe49bd525d0fa3f4ed95874f2020d9d2a5eb9554
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659030"
---
# <a name="rdn-attribute"></a><span data-ttu-id="e1003-105">RDN (atributo)</span><span class="sxs-lookup"><span data-stu-id="e1003-105">RDN attribute</span></span>

<span data-ttu-id="e1003-106">Nombre distintivo relativo (RDN) de un objeto.</span><span class="sxs-lookup"><span data-stu-id="e1003-106">The Relative Distinguished Name (RDN) of an object.</span></span> <span data-ttu-id="e1003-107">Un RDN es la parte relativa de un nombre distintivo (DN) que identifica de forma única un objeto LDAP.</span><span class="sxs-lookup"><span data-stu-id="e1003-107">An RDN is the relative portion of a distinguished name (DN), which uniquely identifies an LDAP object.</span></span>



| <span data-ttu-id="e1003-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="e1003-108">Entry</span></span> | <span data-ttu-id="e1003-109">Value</span><span class="sxs-lookup"><span data-stu-id="e1003-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="e1003-110">CN</span><span class="sxs-lookup"><span data-stu-id="e1003-110">CN</span></span>                | <span data-ttu-id="e1003-111">RDN</span><span class="sxs-lookup"><span data-stu-id="e1003-111">RDN</span></span>                                            |
| <span data-ttu-id="e1003-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="e1003-112">Ldap-Display-Name</span></span> | <span data-ttu-id="e1003-113">name</span><span class="sxs-lookup"><span data-stu-id="e1003-113">name</span></span>                                           |
| <span data-ttu-id="e1003-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="e1003-114">Size</span></span>              | \-                                             |
| <span data-ttu-id="e1003-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="e1003-115">Update Privilege</span></span>  | <span data-ttu-id="e1003-116">El administrador del esquema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="e1003-116">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="e1003-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="e1003-117">Update Frequency</span></span>  | \-                                             |
| <span data-ttu-id="e1003-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e1003-118">Attribute-Id</span></span>      | <span data-ttu-id="e1003-119">1.2.840.113556.1.4.1</span><span class="sxs-lookup"><span data-stu-id="e1003-119">1.2.840.113556.1.4.1</span></span>                           |
| <span data-ttu-id="e1003-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e1003-120">System-Id-Guid</span></span>    | <span data-ttu-id="e1003-121">bf967a0e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e1003-121">bf967a0e-0de6-11d0-a285-00aa003049e2</span></span>           |
| <span data-ttu-id="e1003-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1003-122">Syntax</span></span>            | [<span data-ttu-id="e1003-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e1003-123">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="e1003-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="e1003-124">Implementations</span></span>

-   [<span data-ttu-id="e1003-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e1003-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e1003-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e1003-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e1003-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e1003-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e1003-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e1003-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e1003-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e1003-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e1003-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e1003-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e1003-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e1003-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e1003-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e1003-132">Windows 2000 Server</span></span>



| <span data-ttu-id="e1003-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="e1003-133">Entry</span></span> | <span data-ttu-id="e1003-134">Value</span><span class="sxs-lookup"><span data-stu-id="e1003-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e1003-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e1003-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e1003-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1003-136">MAPI-Id</span></span>                | <span data-ttu-id="e1003-137">0x8202</span><span class="sxs-lookup"><span data-stu-id="e1003-137">0x8202</span></span>                          |
| <span data-ttu-id="e1003-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1003-138">System-Only</span></span>            | <span data-ttu-id="e1003-139">True</span><span class="sxs-lookup"><span data-stu-id="e1003-139">True</span></span>                            |
| <span data-ttu-id="e1003-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e1003-140">Is-Single-Valued</span></span>       | <span data-ttu-id="e1003-141">True</span><span class="sxs-lookup"><span data-stu-id="e1003-141">True</span></span>                            |
| <span data-ttu-id="e1003-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e1003-142">Is Indexed</span></span>             | <span data-ttu-id="e1003-143">True</span><span class="sxs-lookup"><span data-stu-id="e1003-143">True</span></span>                            |
| <span data-ttu-id="e1003-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e1003-144">In Global Catalog</span></span>      | <span data-ttu-id="e1003-145">True</span><span class="sxs-lookup"><span data-stu-id="e1003-145">True</span></span>                            |
| <span data-ttu-id="e1003-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e1003-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1003-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e1003-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e1003-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1003-148">Range-Lower</span></span>            | <span data-ttu-id="e1003-149">1</span><span class="sxs-lookup"><span data-stu-id="e1003-149">1</span></span>                               |
| <span data-ttu-id="e1003-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1003-150">Range-Upper</span></span>            | <span data-ttu-id="e1003-151">255</span><span class="sxs-lookup"><span data-stu-id="e1003-151">255</span></span>                             |
| <span data-ttu-id="e1003-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1003-152">Search-Flags</span></span>           | <span data-ttu-id="e1003-153">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="e1003-153">0x0000000D</span></span>                      |
| <span data-ttu-id="e1003-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1003-154">System-Flags</span></span>           | <span data-ttu-id="e1003-155">0x00000012</span><span class="sxs-lookup"><span data-stu-id="e1003-155">0x00000012</span></span>                      |
| <span data-ttu-id="e1003-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e1003-156">Classes used in</span></span>        | [<span data-ttu-id="e1003-157">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="e1003-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e1003-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e1003-158">Windows Server 2003</span></span>



| <span data-ttu-id="e1003-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="e1003-159">Entry</span></span> | <span data-ttu-id="e1003-160">Value</span><span class="sxs-lookup"><span data-stu-id="e1003-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e1003-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e1003-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e1003-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1003-162">MAPI-Id</span></span>                | <span data-ttu-id="e1003-163">0x8202</span><span class="sxs-lookup"><span data-stu-id="e1003-163">0x8202</span></span>                          |
| <span data-ttu-id="e1003-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1003-164">System-Only</span></span>            | <span data-ttu-id="e1003-165">True</span><span class="sxs-lookup"><span data-stu-id="e1003-165">True</span></span>                            |
| <span data-ttu-id="e1003-166">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e1003-166">Is-Single-Valued</span></span>       | <span data-ttu-id="e1003-167">True</span><span class="sxs-lookup"><span data-stu-id="e1003-167">True</span></span>                            |
| <span data-ttu-id="e1003-168">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e1003-168">Is Indexed</span></span>             | <span data-ttu-id="e1003-169">True</span><span class="sxs-lookup"><span data-stu-id="e1003-169">True</span></span>                            |
| <span data-ttu-id="e1003-170">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e1003-170">In Global Catalog</span></span>      | <span data-ttu-id="e1003-171">True</span><span class="sxs-lookup"><span data-stu-id="e1003-171">True</span></span>                            |
| <span data-ttu-id="e1003-172">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e1003-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1003-173">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e1003-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e1003-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1003-174">Range-Lower</span></span>            | <span data-ttu-id="e1003-175">1</span><span class="sxs-lookup"><span data-stu-id="e1003-175">1</span></span>                               |
| <span data-ttu-id="e1003-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1003-176">Range-Upper</span></span>            | <span data-ttu-id="e1003-177">255</span><span class="sxs-lookup"><span data-stu-id="e1003-177">255</span></span>                             |
| <span data-ttu-id="e1003-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1003-178">Search-Flags</span></span>           | <span data-ttu-id="e1003-179">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="e1003-179">0x0000000D</span></span>                      |
| <span data-ttu-id="e1003-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1003-180">System-Flags</span></span>           | <span data-ttu-id="e1003-181">0x00000012</span><span class="sxs-lookup"><span data-stu-id="e1003-181">0x00000012</span></span>                      |
| <span data-ttu-id="e1003-182">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e1003-182">Classes used in</span></span>        | [<span data-ttu-id="e1003-183">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="e1003-183">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e1003-184">ADAM</span><span class="sxs-lookup"><span data-stu-id="e1003-184">ADAM</span></span>



| <span data-ttu-id="e1003-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="e1003-185">Entry</span></span> | <span data-ttu-id="e1003-186">Value</span><span class="sxs-lookup"><span data-stu-id="e1003-186">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e1003-187">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e1003-187">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e1003-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1003-188">MAPI-Id</span></span>                | <span data-ttu-id="e1003-189">0x8202</span><span class="sxs-lookup"><span data-stu-id="e1003-189">0x8202</span></span>                          |
| <span data-ttu-id="e1003-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1003-190">System-Only</span></span>            | <span data-ttu-id="e1003-191">True</span><span class="sxs-lookup"><span data-stu-id="e1003-191">True</span></span>                            |
| <span data-ttu-id="e1003-192">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e1003-192">Is-Single-Valued</span></span>       | <span data-ttu-id="e1003-193">True</span><span class="sxs-lookup"><span data-stu-id="e1003-193">True</span></span>                            |
| <span data-ttu-id="e1003-194">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e1003-194">Is Indexed</span></span>             | <span data-ttu-id="e1003-195">True</span><span class="sxs-lookup"><span data-stu-id="e1003-195">True</span></span>                            |
| <span data-ttu-id="e1003-196">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e1003-196">In Global Catalog</span></span>      | <span data-ttu-id="e1003-197">True</span><span class="sxs-lookup"><span data-stu-id="e1003-197">True</span></span>                            |
| <span data-ttu-id="e1003-198">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e1003-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1003-199">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e1003-199">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e1003-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1003-200">Range-Lower</span></span>            | <span data-ttu-id="e1003-201">1</span><span class="sxs-lookup"><span data-stu-id="e1003-201">1</span></span>                               |
| <span data-ttu-id="e1003-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1003-202">Range-Upper</span></span>            | <span data-ttu-id="e1003-203">255</span><span class="sxs-lookup"><span data-stu-id="e1003-203">255</span></span>                             |
| <span data-ttu-id="e1003-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1003-204">Search-Flags</span></span>           | <span data-ttu-id="e1003-205">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="e1003-205">0x0000000D</span></span>                      |
| <span data-ttu-id="e1003-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1003-206">System-Flags</span></span>           | <span data-ttu-id="e1003-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="e1003-207">0x00000012</span></span>                      |
| <span data-ttu-id="e1003-208">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e1003-208">Classes used in</span></span>        | [<span data-ttu-id="e1003-209">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="e1003-209">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e1003-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e1003-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e1003-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="e1003-211">Entry</span></span> | <span data-ttu-id="e1003-212">Value</span><span class="sxs-lookup"><span data-stu-id="e1003-212">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e1003-213">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e1003-213">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e1003-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1003-214">MAPI-Id</span></span>                | <span data-ttu-id="e1003-215">0x8202</span><span class="sxs-lookup"><span data-stu-id="e1003-215">0x8202</span></span>                          |
| <span data-ttu-id="e1003-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1003-216">System-Only</span></span>            | <span data-ttu-id="e1003-217">True</span><span class="sxs-lookup"><span data-stu-id="e1003-217">True</span></span>                            |
| <span data-ttu-id="e1003-218">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e1003-218">Is-Single-Valued</span></span>       | <span data-ttu-id="e1003-219">True</span><span class="sxs-lookup"><span data-stu-id="e1003-219">True</span></span>                            |
| <span data-ttu-id="e1003-220">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e1003-220">Is Indexed</span></span>             | <span data-ttu-id="e1003-221">True</span><span class="sxs-lookup"><span data-stu-id="e1003-221">True</span></span>                            |
| <span data-ttu-id="e1003-222">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e1003-222">In Global Catalog</span></span>      | <span data-ttu-id="e1003-223">True</span><span class="sxs-lookup"><span data-stu-id="e1003-223">True</span></span>                            |
| <span data-ttu-id="e1003-224">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e1003-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1003-225">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e1003-225">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e1003-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1003-226">Range-Lower</span></span>            | <span data-ttu-id="e1003-227">1</span><span class="sxs-lookup"><span data-stu-id="e1003-227">1</span></span>                               |
| <span data-ttu-id="e1003-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1003-228">Range-Upper</span></span>            | <span data-ttu-id="e1003-229">255</span><span class="sxs-lookup"><span data-stu-id="e1003-229">255</span></span>                             |
| <span data-ttu-id="e1003-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1003-230">Search-Flags</span></span>           | <span data-ttu-id="e1003-231">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="e1003-231">0x0000000D</span></span>                      |
| <span data-ttu-id="e1003-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1003-232">System-Flags</span></span>           | <span data-ttu-id="e1003-233">0x00000012</span><span class="sxs-lookup"><span data-stu-id="e1003-233">0x00000012</span></span>                      |
| <span data-ttu-id="e1003-234">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e1003-234">Classes used in</span></span>        | [<span data-ttu-id="e1003-235">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="e1003-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e1003-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1003-236">Windows Server 2008</span></span>



| <span data-ttu-id="e1003-237">Entrada</span><span class="sxs-lookup"><span data-stu-id="e1003-237">Entry</span></span> | <span data-ttu-id="e1003-238">Value</span><span class="sxs-lookup"><span data-stu-id="e1003-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e1003-239">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e1003-239">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e1003-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1003-240">MAPI-Id</span></span>                | <span data-ttu-id="e1003-241">0x8202</span><span class="sxs-lookup"><span data-stu-id="e1003-241">0x8202</span></span>                          |
| <span data-ttu-id="e1003-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1003-242">System-Only</span></span>            | <span data-ttu-id="e1003-243">True</span><span class="sxs-lookup"><span data-stu-id="e1003-243">True</span></span>                            |
| <span data-ttu-id="e1003-244">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e1003-244">Is-Single-Valued</span></span>       | <span data-ttu-id="e1003-245">True</span><span class="sxs-lookup"><span data-stu-id="e1003-245">True</span></span>                            |
| <span data-ttu-id="e1003-246">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e1003-246">Is Indexed</span></span>             | <span data-ttu-id="e1003-247">True</span><span class="sxs-lookup"><span data-stu-id="e1003-247">True</span></span>                            |
| <span data-ttu-id="e1003-248">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e1003-248">In Global Catalog</span></span>      | <span data-ttu-id="e1003-249">True</span><span class="sxs-lookup"><span data-stu-id="e1003-249">True</span></span>                            |
| <span data-ttu-id="e1003-250">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e1003-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1003-251">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e1003-251">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e1003-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1003-252">Range-Lower</span></span>            | <span data-ttu-id="e1003-253">1</span><span class="sxs-lookup"><span data-stu-id="e1003-253">1</span></span>                               |
| <span data-ttu-id="e1003-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1003-254">Range-Upper</span></span>            | <span data-ttu-id="e1003-255">255</span><span class="sxs-lookup"><span data-stu-id="e1003-255">255</span></span>                             |
| <span data-ttu-id="e1003-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1003-256">Search-Flags</span></span>           | <span data-ttu-id="e1003-257">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="e1003-257">0x0000000D</span></span>                      |
| <span data-ttu-id="e1003-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1003-258">System-Flags</span></span>           | <span data-ttu-id="e1003-259">0x00000012</span><span class="sxs-lookup"><span data-stu-id="e1003-259">0x00000012</span></span>                      |
| <span data-ttu-id="e1003-260">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e1003-260">Classes used in</span></span>        | [<span data-ttu-id="e1003-261">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="e1003-261">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e1003-262">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e1003-262">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e1003-263">Entrada</span><span class="sxs-lookup"><span data-stu-id="e1003-263">Entry</span></span> | <span data-ttu-id="e1003-264">Value</span><span class="sxs-lookup"><span data-stu-id="e1003-264">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e1003-265">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e1003-265">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e1003-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1003-266">MAPI-Id</span></span>                | <span data-ttu-id="e1003-267">0x8202</span><span class="sxs-lookup"><span data-stu-id="e1003-267">0x8202</span></span>                          |
| <span data-ttu-id="e1003-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1003-268">System-Only</span></span>            | <span data-ttu-id="e1003-269">True</span><span class="sxs-lookup"><span data-stu-id="e1003-269">True</span></span>                            |
| <span data-ttu-id="e1003-270">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e1003-270">Is-Single-Valued</span></span>       | <span data-ttu-id="e1003-271">True</span><span class="sxs-lookup"><span data-stu-id="e1003-271">True</span></span>                            |
| <span data-ttu-id="e1003-272">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e1003-272">Is Indexed</span></span>             | <span data-ttu-id="e1003-273">True</span><span class="sxs-lookup"><span data-stu-id="e1003-273">True</span></span>                            |
| <span data-ttu-id="e1003-274">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e1003-274">In Global Catalog</span></span>      | <span data-ttu-id="e1003-275">True</span><span class="sxs-lookup"><span data-stu-id="e1003-275">True</span></span>                            |
| <span data-ttu-id="e1003-276">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e1003-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1003-277">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e1003-277">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e1003-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1003-278">Range-Lower</span></span>            | <span data-ttu-id="e1003-279">1</span><span class="sxs-lookup"><span data-stu-id="e1003-279">1</span></span>                               |
| <span data-ttu-id="e1003-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1003-280">Range-Upper</span></span>            | <span data-ttu-id="e1003-281">255</span><span class="sxs-lookup"><span data-stu-id="e1003-281">255</span></span>                             |
| <span data-ttu-id="e1003-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1003-282">Search-Flags</span></span>           | <span data-ttu-id="e1003-283">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="e1003-283">0x0000000D</span></span>                      |
| <span data-ttu-id="e1003-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1003-284">System-Flags</span></span>           | <span data-ttu-id="e1003-285">0x00000012</span><span class="sxs-lookup"><span data-stu-id="e1003-285">0x00000012</span></span>                      |
| <span data-ttu-id="e1003-286">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e1003-286">Classes used in</span></span>        | [<span data-ttu-id="e1003-287">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="e1003-287">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e1003-288">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e1003-288">Windows Server 2012</span></span>



| <span data-ttu-id="e1003-289">Entrada</span><span class="sxs-lookup"><span data-stu-id="e1003-289">Entry</span></span> | <span data-ttu-id="e1003-290">Value</span><span class="sxs-lookup"><span data-stu-id="e1003-290">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e1003-291">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e1003-291">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e1003-292">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1003-292">MAPI-Id</span></span>                | <span data-ttu-id="e1003-293">0x8202</span><span class="sxs-lookup"><span data-stu-id="e1003-293">0x8202</span></span>                          |
| <span data-ttu-id="e1003-294">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1003-294">System-Only</span></span>            | <span data-ttu-id="e1003-295">True</span><span class="sxs-lookup"><span data-stu-id="e1003-295">True</span></span>                            |
| <span data-ttu-id="e1003-296">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e1003-296">Is-Single-Valued</span></span>       | <span data-ttu-id="e1003-297">True</span><span class="sxs-lookup"><span data-stu-id="e1003-297">True</span></span>                            |
| <span data-ttu-id="e1003-298">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e1003-298">Is Indexed</span></span>             | <span data-ttu-id="e1003-299">True</span><span class="sxs-lookup"><span data-stu-id="e1003-299">True</span></span>                            |
| <span data-ttu-id="e1003-300">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e1003-300">In Global Catalog</span></span>      | <span data-ttu-id="e1003-301">True</span><span class="sxs-lookup"><span data-stu-id="e1003-301">True</span></span>                            |
| <span data-ttu-id="e1003-302">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e1003-302">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1003-303">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e1003-303">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e1003-304">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1003-304">Range-Lower</span></span>            | <span data-ttu-id="e1003-305">1</span><span class="sxs-lookup"><span data-stu-id="e1003-305">1</span></span>                               |
| <span data-ttu-id="e1003-306">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1003-306">Range-Upper</span></span>            | <span data-ttu-id="e1003-307">255</span><span class="sxs-lookup"><span data-stu-id="e1003-307">255</span></span>                             |
| <span data-ttu-id="e1003-308">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1003-308">Search-Flags</span></span>           | <span data-ttu-id="e1003-309">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="e1003-309">0x0000000D</span></span>                      |
| <span data-ttu-id="e1003-310">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1003-310">System-Flags</span></span>           | <span data-ttu-id="e1003-311">0x00000012</span><span class="sxs-lookup"><span data-stu-id="e1003-311">0x00000012</span></span>                      |
| <span data-ttu-id="e1003-312">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e1003-312">Classes used in</span></span>        | [<span data-ttu-id="e1003-313">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="e1003-313">**Top**</span></span>](c-top.md)<br/> |



 

 





