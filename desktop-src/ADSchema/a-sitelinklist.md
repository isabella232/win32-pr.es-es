---
title: Atributo site-Link-List
description: Lista de vínculos a sitios asociados a este puente.
ms.assetid: 79ec0ae2-ceb3-4321-8b6d-ce5c3bda667a
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de lista de vínculos de sitio
- siteLinkList esquema de AD de atributos
topic_type:
- apiref
api_name:
- Site-Link-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e71284e4650a3cb146b1656c846483e33a6dd66
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104422695"
---
# <a name="site-link-list-attribute"></a><span data-ttu-id="e1e52-105">Atributo site-Link-List</span><span class="sxs-lookup"><span data-stu-id="e1e52-105">Site-Link-List attribute</span></span>

<span data-ttu-id="e1e52-106">Lista de vínculos a sitios asociados a este puente.</span><span class="sxs-lookup"><span data-stu-id="e1e52-106">List of site links that are associated with this bridge.</span></span>



| <span data-ttu-id="e1e52-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e1e52-107">Entry</span></span> | <span data-ttu-id="e1e52-108">Value</span><span class="sxs-lookup"><span data-stu-id="e1e52-108">Value</span></span> |
|-------------------|--------------------------------------------------------------|
| <span data-ttu-id="e1e52-109">CN</span><span class="sxs-lookup"><span data-stu-id="e1e52-109">CN</span></span>                | <span data-ttu-id="e1e52-110">Site-Link-List</span><span class="sxs-lookup"><span data-stu-id="e1e52-110">Site-Link-List</span></span>                                               |
| <span data-ttu-id="e1e52-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="e1e52-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e1e52-112">siteLinkList</span><span class="sxs-lookup"><span data-stu-id="e1e52-112">siteLinkList</span></span>                                                 |
| <span data-ttu-id="e1e52-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="e1e52-113">Size</span></span>              | \-                                                           |
| <span data-ttu-id="e1e52-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="e1e52-114">Update Privilege</span></span>  | <span data-ttu-id="e1e52-115">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="e1e52-115">Domain administrator</span></span>                                         |
| <span data-ttu-id="e1e52-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="e1e52-116">Update Frequency</span></span>  | <span data-ttu-id="e1e52-117">Cada vez que se agrega o se quita un vínculo de sitio del puente.</span><span class="sxs-lookup"><span data-stu-id="e1e52-117">Whenever a site link is added to or removed from the bridge.</span></span> |
| <span data-ttu-id="e1e52-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e1e52-118">Attribute-Id</span></span>      | <span data-ttu-id="e1e52-119">1.2.840.113556.1.4.822</span><span class="sxs-lookup"><span data-stu-id="e1e52-119">1.2.840.113556.1.4.822</span></span>                                       |
| <span data-ttu-id="e1e52-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e1e52-120">System-Id-Guid</span></span>    | <span data-ttu-id="e1e52-121">d50c2cdd-8951-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e1e52-121">d50c2cdd-8951-11d1-aebc-0000f80367c1</span></span>                         |
| <span data-ttu-id="e1e52-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1e52-122">Syntax</span></span>            | [<span data-ttu-id="e1e52-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="e1e52-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                      |



## <a name="implementations"></a><span data-ttu-id="e1e52-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="e1e52-124">Implementations</span></span>

-   [<span data-ttu-id="e1e52-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e1e52-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e1e52-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e1e52-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e1e52-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e1e52-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e1e52-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e1e52-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e1e52-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e1e52-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e1e52-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e1e52-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e1e52-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e1e52-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e1e52-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e1e52-132">Windows 2000 Server</span></span>



| <span data-ttu-id="e1e52-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="e1e52-133">Entry</span></span> | <span data-ttu-id="e1e52-134">Value</span><span class="sxs-lookup"><span data-stu-id="e1e52-134">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="e1e52-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e1e52-135">Link-Id</span></span>                | <span data-ttu-id="e1e52-136">142</span><span class="sxs-lookup"><span data-stu-id="e1e52-136">142</span></span>                                                     |
| <span data-ttu-id="e1e52-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1e52-137">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="e1e52-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1e52-138">System-Only</span></span>            | <span data-ttu-id="e1e52-139">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-139">False</span></span>                                                   |
| <span data-ttu-id="e1e52-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e1e52-140">Is-Single-Valued</span></span>       | <span data-ttu-id="e1e52-141">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-141">False</span></span>                                                   |
| <span data-ttu-id="e1e52-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e1e52-142">Is Indexed</span></span>             | <span data-ttu-id="e1e52-143">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-143">False</span></span>                                                   |
| <span data-ttu-id="e1e52-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e1e52-144">In Global Catalog</span></span>      | <span data-ttu-id="e1e52-145">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-145">False</span></span>                                                   |
| <span data-ttu-id="e1e52-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e1e52-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1e52-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e1e52-147">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="e1e52-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1e52-148">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="e1e52-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1e52-149">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="e1e52-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1e52-150">Search-Flags</span></span>           | <span data-ttu-id="e1e52-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e1e52-151">0x00000000</span></span>                                              |
| <span data-ttu-id="e1e52-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1e52-152">System-Flags</span></span>           | <span data-ttu-id="e1e52-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1e52-153">0x00000010</span></span>                                              |
| <span data-ttu-id="e1e52-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e1e52-154">Classes used in</span></span>        | [<span data-ttu-id="e1e52-155">**Puente de vínculo de sitio**</span><span class="sxs-lookup"><span data-stu-id="e1e52-155">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e1e52-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e1e52-156">Windows Server 2003</span></span>



| <span data-ttu-id="e1e52-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="e1e52-157">Entry</span></span> | <span data-ttu-id="e1e52-158">Value</span><span class="sxs-lookup"><span data-stu-id="e1e52-158">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="e1e52-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e1e52-159">Link-Id</span></span>                | <span data-ttu-id="e1e52-160">142</span><span class="sxs-lookup"><span data-stu-id="e1e52-160">142</span></span>                                                     |
| <span data-ttu-id="e1e52-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1e52-161">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="e1e52-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1e52-162">System-Only</span></span>            | <span data-ttu-id="e1e52-163">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-163">False</span></span>                                                   |
| <span data-ttu-id="e1e52-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e1e52-164">Is-Single-Valued</span></span>       | <span data-ttu-id="e1e52-165">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-165">False</span></span>                                                   |
| <span data-ttu-id="e1e52-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e1e52-166">Is Indexed</span></span>             | <span data-ttu-id="e1e52-167">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-167">False</span></span>                                                   |
| <span data-ttu-id="e1e52-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e1e52-168">In Global Catalog</span></span>      | <span data-ttu-id="e1e52-169">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-169">False</span></span>                                                   |
| <span data-ttu-id="e1e52-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e1e52-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1e52-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e1e52-171">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="e1e52-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1e52-172">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="e1e52-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1e52-173">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="e1e52-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1e52-174">Search-Flags</span></span>           | <span data-ttu-id="e1e52-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e1e52-175">0x00000000</span></span>                                              |
| <span data-ttu-id="e1e52-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1e52-176">System-Flags</span></span>           | <span data-ttu-id="e1e52-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1e52-177">0x00000010</span></span>                                              |
| <span data-ttu-id="e1e52-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e1e52-178">Classes used in</span></span>        | [<span data-ttu-id="e1e52-179">**Puente de vínculo de sitio**</span><span class="sxs-lookup"><span data-stu-id="e1e52-179">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e1e52-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="e1e52-180">ADAM</span></span>



| <span data-ttu-id="e1e52-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="e1e52-181">Entry</span></span> | <span data-ttu-id="e1e52-182">Value</span><span class="sxs-lookup"><span data-stu-id="e1e52-182">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="e1e52-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e1e52-183">Link-Id</span></span>                | <span data-ttu-id="e1e52-184">142</span><span class="sxs-lookup"><span data-stu-id="e1e52-184">142</span></span>                                                     |
| <span data-ttu-id="e1e52-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1e52-185">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="e1e52-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1e52-186">System-Only</span></span>            | <span data-ttu-id="e1e52-187">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-187">False</span></span>                                                   |
| <span data-ttu-id="e1e52-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e1e52-188">Is-Single-Valued</span></span>       | <span data-ttu-id="e1e52-189">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-189">False</span></span>                                                   |
| <span data-ttu-id="e1e52-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e1e52-190">Is Indexed</span></span>             | <span data-ttu-id="e1e52-191">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-191">False</span></span>                                                   |
| <span data-ttu-id="e1e52-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e1e52-192">In Global Catalog</span></span>      | <span data-ttu-id="e1e52-193">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-193">False</span></span>                                                   |
| <span data-ttu-id="e1e52-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e1e52-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1e52-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e1e52-195">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="e1e52-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1e52-196">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="e1e52-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1e52-197">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="e1e52-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1e52-198">Search-Flags</span></span>           | <span data-ttu-id="e1e52-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e1e52-199">0x00000000</span></span>                                              |
| <span data-ttu-id="e1e52-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1e52-200">System-Flags</span></span>           | <span data-ttu-id="e1e52-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1e52-201">0x00000010</span></span>                                              |
| <span data-ttu-id="e1e52-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e1e52-202">Classes used in</span></span>        | [<span data-ttu-id="e1e52-203">**Puente de vínculo de sitio**</span><span class="sxs-lookup"><span data-stu-id="e1e52-203">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e1e52-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e1e52-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e1e52-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="e1e52-205">Entry</span></span> | <span data-ttu-id="e1e52-206">Value</span><span class="sxs-lookup"><span data-stu-id="e1e52-206">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="e1e52-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e1e52-207">Link-Id</span></span>                | <span data-ttu-id="e1e52-208">142</span><span class="sxs-lookup"><span data-stu-id="e1e52-208">142</span></span>                                                     |
| <span data-ttu-id="e1e52-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1e52-209">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="e1e52-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1e52-210">System-Only</span></span>            | <span data-ttu-id="e1e52-211">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-211">False</span></span>                                                   |
| <span data-ttu-id="e1e52-212">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e1e52-212">Is-Single-Valued</span></span>       | <span data-ttu-id="e1e52-213">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-213">False</span></span>                                                   |
| <span data-ttu-id="e1e52-214">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e1e52-214">Is Indexed</span></span>             | <span data-ttu-id="e1e52-215">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-215">False</span></span>                                                   |
| <span data-ttu-id="e1e52-216">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e1e52-216">In Global Catalog</span></span>      | <span data-ttu-id="e1e52-217">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-217">False</span></span>                                                   |
| <span data-ttu-id="e1e52-218">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e1e52-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1e52-219">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e1e52-219">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="e1e52-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1e52-220">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="e1e52-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1e52-221">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="e1e52-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1e52-222">Search-Flags</span></span>           | <span data-ttu-id="e1e52-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e1e52-223">0x00000000</span></span>                                              |
| <span data-ttu-id="e1e52-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1e52-224">System-Flags</span></span>           | <span data-ttu-id="e1e52-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1e52-225">0x00000010</span></span>                                              |
| <span data-ttu-id="e1e52-226">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e1e52-226">Classes used in</span></span>        | [<span data-ttu-id="e1e52-227">**Puente de vínculo de sitio**</span><span class="sxs-lookup"><span data-stu-id="e1e52-227">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e1e52-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1e52-228">Windows Server 2008</span></span>



| <span data-ttu-id="e1e52-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="e1e52-229">Entry</span></span> | <span data-ttu-id="e1e52-230">Value</span><span class="sxs-lookup"><span data-stu-id="e1e52-230">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="e1e52-231">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e1e52-231">Link-Id</span></span>                | <span data-ttu-id="e1e52-232">142</span><span class="sxs-lookup"><span data-stu-id="e1e52-232">142</span></span>                                                     |
| <span data-ttu-id="e1e52-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1e52-233">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="e1e52-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1e52-234">System-Only</span></span>            | <span data-ttu-id="e1e52-235">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-235">False</span></span>                                                   |
| <span data-ttu-id="e1e52-236">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e1e52-236">Is-Single-Valued</span></span>       | <span data-ttu-id="e1e52-237">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-237">False</span></span>                                                   |
| <span data-ttu-id="e1e52-238">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e1e52-238">Is Indexed</span></span>             | <span data-ttu-id="e1e52-239">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-239">False</span></span>                                                   |
| <span data-ttu-id="e1e52-240">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e1e52-240">In Global Catalog</span></span>      | <span data-ttu-id="e1e52-241">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-241">False</span></span>                                                   |
| <span data-ttu-id="e1e52-242">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e1e52-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1e52-243">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e1e52-243">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="e1e52-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1e52-244">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="e1e52-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1e52-245">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="e1e52-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1e52-246">Search-Flags</span></span>           | <span data-ttu-id="e1e52-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e1e52-247">0x00000000</span></span>                                              |
| <span data-ttu-id="e1e52-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1e52-248">System-Flags</span></span>           | <span data-ttu-id="e1e52-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1e52-249">0x00000010</span></span>                                              |
| <span data-ttu-id="e1e52-250">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e1e52-250">Classes used in</span></span>        | [<span data-ttu-id="e1e52-251">**Puente de vínculo de sitio**</span><span class="sxs-lookup"><span data-stu-id="e1e52-251">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e1e52-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e1e52-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e1e52-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="e1e52-253">Entry</span></span> | <span data-ttu-id="e1e52-254">Value</span><span class="sxs-lookup"><span data-stu-id="e1e52-254">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="e1e52-255">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e1e52-255">Link-Id</span></span>                | <span data-ttu-id="e1e52-256">142</span><span class="sxs-lookup"><span data-stu-id="e1e52-256">142</span></span>                                                     |
| <span data-ttu-id="e1e52-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1e52-257">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="e1e52-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1e52-258">System-Only</span></span>            | <span data-ttu-id="e1e52-259">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-259">False</span></span>                                                   |
| <span data-ttu-id="e1e52-260">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e1e52-260">Is-Single-Valued</span></span>       | <span data-ttu-id="e1e52-261">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-261">False</span></span>                                                   |
| <span data-ttu-id="e1e52-262">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e1e52-262">Is Indexed</span></span>             | <span data-ttu-id="e1e52-263">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-263">False</span></span>                                                   |
| <span data-ttu-id="e1e52-264">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e1e52-264">In Global Catalog</span></span>      | <span data-ttu-id="e1e52-265">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-265">False</span></span>                                                   |
| <span data-ttu-id="e1e52-266">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e1e52-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1e52-267">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e1e52-267">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="e1e52-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1e52-268">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="e1e52-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1e52-269">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="e1e52-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1e52-270">Search-Flags</span></span>           | <span data-ttu-id="e1e52-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e1e52-271">0x00000000</span></span>                                              |
| <span data-ttu-id="e1e52-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1e52-272">System-Flags</span></span>           | <span data-ttu-id="e1e52-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1e52-273">0x00000010</span></span>                                              |
| <span data-ttu-id="e1e52-274">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e1e52-274">Classes used in</span></span>        | [<span data-ttu-id="e1e52-275">**Puente de vínculo de sitio**</span><span class="sxs-lookup"><span data-stu-id="e1e52-275">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e1e52-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e1e52-276">Windows Server 2012</span></span>



| <span data-ttu-id="e1e52-277">Entrada</span><span class="sxs-lookup"><span data-stu-id="e1e52-277">Entry</span></span> | <span data-ttu-id="e1e52-278">Value</span><span class="sxs-lookup"><span data-stu-id="e1e52-278">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="e1e52-279">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e1e52-279">Link-Id</span></span>                | <span data-ttu-id="e1e52-280">142</span><span class="sxs-lookup"><span data-stu-id="e1e52-280">142</span></span>                                                     |
| <span data-ttu-id="e1e52-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1e52-281">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="e1e52-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1e52-282">System-Only</span></span>            | <span data-ttu-id="e1e52-283">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-283">False</span></span>                                                   |
| <span data-ttu-id="e1e52-284">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e1e52-284">Is-Single-Valued</span></span>       | <span data-ttu-id="e1e52-285">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-285">False</span></span>                                                   |
| <span data-ttu-id="e1e52-286">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e1e52-286">Is Indexed</span></span>             | <span data-ttu-id="e1e52-287">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-287">False</span></span>                                                   |
| <span data-ttu-id="e1e52-288">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e1e52-288">In Global Catalog</span></span>      | <span data-ttu-id="e1e52-289">False</span><span class="sxs-lookup"><span data-stu-id="e1e52-289">False</span></span>                                                   |
| <span data-ttu-id="e1e52-290">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e1e52-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1e52-291">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e1e52-291">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="e1e52-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1e52-292">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="e1e52-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1e52-293">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="e1e52-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1e52-294">Search-Flags</span></span>           | <span data-ttu-id="e1e52-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e1e52-295">0x00000000</span></span>                                              |
| <span data-ttu-id="e1e52-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1e52-296">System-Flags</span></span>           | <span data-ttu-id="e1e52-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1e52-297">0x00000010</span></span>                                              |
| <span data-ttu-id="e1e52-298">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e1e52-298">Classes used in</span></span>        | [<span data-ttu-id="e1e52-299">**Puente de vínculo de sitio**</span><span class="sxs-lookup"><span data-stu-id="e1e52-299">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



 

 





