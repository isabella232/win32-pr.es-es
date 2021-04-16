---
title: Atributo de nombre de objeto de proxy
description: Este atributo lo usa internamente Active Directory para ayudar a realizar el seguimiento de los movimientos entre dominios.
ms.assetid: 661ea322-f78c-44dc-8d64-4f28ead1a7aa
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de nombre de objeto de proxy
- proxiedObjectName esquema de AD de atributos
topic_type:
- apiref
api_name:
- Proxied-Object-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ffafbbea411c950954102a788226c29589029e1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658474"
---
# <a name="proxied-object-name-attribute"></a><span data-ttu-id="35d33-105">Atributo de nombre de objeto de proxy</span><span class="sxs-lookup"><span data-stu-id="35d33-105">Proxied-Object-Name attribute</span></span>

<span data-ttu-id="35d33-106">Este atributo lo usa internamente Active Directory para ayudar a realizar el seguimiento de los movimientos entre dominios.</span><span class="sxs-lookup"><span data-stu-id="35d33-106">This attribute is used internally by Active Directory to help track interdomain moves.</span></span>



| <span data-ttu-id="35d33-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="35d33-107">Entry</span></span> | <span data-ttu-id="35d33-108">Value</span><span class="sxs-lookup"><span data-stu-id="35d33-108">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="35d33-109">CN</span><span class="sxs-lookup"><span data-stu-id="35d33-109">CN</span></span>                | <span data-ttu-id="35d33-110">Nombre-objeto-proxy</span><span class="sxs-lookup"><span data-stu-id="35d33-110">Proxied-Object-Name</span></span>                             |
| <span data-ttu-id="35d33-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="35d33-111">Ldap-Display-Name</span></span> | <span data-ttu-id="35d33-112">proxiedObjectName</span><span class="sxs-lookup"><span data-stu-id="35d33-112">proxiedObjectName</span></span>                               |
| <span data-ttu-id="35d33-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="35d33-113">Size</span></span>              | \-                                              |
| <span data-ttu-id="35d33-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="35d33-114">Update Privilege</span></span>  | <span data-ttu-id="35d33-115">Lo utiliza el sistema.</span><span class="sxs-lookup"><span data-stu-id="35d33-115">This is used by the system.</span></span>                     |
| <span data-ttu-id="35d33-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="35d33-116">Update Frequency</span></span>  | \-                                              |
| <span data-ttu-id="35d33-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="35d33-117">Attribute-Id</span></span>      | <span data-ttu-id="35d33-118">1.2.840.113556.1.4.1249</span><span class="sxs-lookup"><span data-stu-id="35d33-118">1.2.840.113556.1.4.1249</span></span>                         |
| <span data-ttu-id="35d33-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="35d33-119">System-Id-Guid</span></span>    | <span data-ttu-id="35d33-120">e1aea402-cd5b-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="35d33-120">e1aea402-cd5b-11d0-afff-0000f80367c1</span></span>            |
| <span data-ttu-id="35d33-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35d33-121">Syntax</span></span>            | [<span data-ttu-id="35d33-122">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="35d33-122">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md) |



## <a name="implementations"></a><span data-ttu-id="35d33-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="35d33-123">Implementations</span></span>

-   [<span data-ttu-id="35d33-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="35d33-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="35d33-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="35d33-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="35d33-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="35d33-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="35d33-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="35d33-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="35d33-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="35d33-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="35d33-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="35d33-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="35d33-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="35d33-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="35d33-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="35d33-131">Windows 2000 Server</span></span>



| <span data-ttu-id="35d33-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="35d33-132">Entry</span></span> | <span data-ttu-id="35d33-133">Value</span><span class="sxs-lookup"><span data-stu-id="35d33-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="35d33-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="35d33-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="35d33-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35d33-135">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="35d33-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="35d33-136">System-Only</span></span>            | <span data-ttu-id="35d33-137">True</span><span class="sxs-lookup"><span data-stu-id="35d33-137">True</span></span>                            |
| <span data-ttu-id="35d33-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="35d33-138">Is-Single-Valued</span></span>       | <span data-ttu-id="35d33-139">True</span><span class="sxs-lookup"><span data-stu-id="35d33-139">True</span></span>                            |
| <span data-ttu-id="35d33-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="35d33-140">Is Indexed</span></span>             | <span data-ttu-id="35d33-141">False</span><span class="sxs-lookup"><span data-stu-id="35d33-141">False</span></span>                           |
| <span data-ttu-id="35d33-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="35d33-142">In Global Catalog</span></span>      | <span data-ttu-id="35d33-143">True</span><span class="sxs-lookup"><span data-stu-id="35d33-143">True</span></span>                            |
| <span data-ttu-id="35d33-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="35d33-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="35d33-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="35d33-145">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="35d33-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35d33-146">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="35d33-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35d33-147">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="35d33-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35d33-148">Search-Flags</span></span>           | <span data-ttu-id="35d33-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35d33-149">0x00000000</span></span>                      |
| <span data-ttu-id="35d33-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35d33-150">System-Flags</span></span>           | <span data-ttu-id="35d33-151">0x00000012</span><span class="sxs-lookup"><span data-stu-id="35d33-151">0x00000012</span></span>                      |
| <span data-ttu-id="35d33-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="35d33-152">Classes used in</span></span>        | [<span data-ttu-id="35d33-153">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="35d33-153">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="35d33-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="35d33-154">Windows Server 2003</span></span>



| <span data-ttu-id="35d33-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="35d33-155">Entry</span></span> | <span data-ttu-id="35d33-156">Value</span><span class="sxs-lookup"><span data-stu-id="35d33-156">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="35d33-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="35d33-157">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="35d33-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35d33-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="35d33-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="35d33-159">System-Only</span></span>            | <span data-ttu-id="35d33-160">True</span><span class="sxs-lookup"><span data-stu-id="35d33-160">True</span></span>                            |
| <span data-ttu-id="35d33-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="35d33-161">Is-Single-Valued</span></span>       | <span data-ttu-id="35d33-162">True</span><span class="sxs-lookup"><span data-stu-id="35d33-162">True</span></span>                            |
| <span data-ttu-id="35d33-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="35d33-163">Is Indexed</span></span>             | <span data-ttu-id="35d33-164">False</span><span class="sxs-lookup"><span data-stu-id="35d33-164">False</span></span>                           |
| <span data-ttu-id="35d33-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="35d33-165">In Global Catalog</span></span>      | <span data-ttu-id="35d33-166">True</span><span class="sxs-lookup"><span data-stu-id="35d33-166">True</span></span>                            |
| <span data-ttu-id="35d33-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="35d33-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="35d33-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="35d33-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="35d33-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35d33-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="35d33-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35d33-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="35d33-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35d33-171">Search-Flags</span></span>           | <span data-ttu-id="35d33-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35d33-172">0x00000000</span></span>                      |
| <span data-ttu-id="35d33-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35d33-173">System-Flags</span></span>           | <span data-ttu-id="35d33-174">0x00000012</span><span class="sxs-lookup"><span data-stu-id="35d33-174">0x00000012</span></span>                      |
| <span data-ttu-id="35d33-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="35d33-175">Classes used in</span></span>        | [<span data-ttu-id="35d33-176">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="35d33-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="35d33-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="35d33-177">ADAM</span></span>



| <span data-ttu-id="35d33-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="35d33-178">Entry</span></span> | <span data-ttu-id="35d33-179">Value</span><span class="sxs-lookup"><span data-stu-id="35d33-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="35d33-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="35d33-180">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="35d33-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35d33-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="35d33-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="35d33-182">System-Only</span></span>            | <span data-ttu-id="35d33-183">True</span><span class="sxs-lookup"><span data-stu-id="35d33-183">True</span></span>                            |
| <span data-ttu-id="35d33-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="35d33-184">Is-Single-Valued</span></span>       | <span data-ttu-id="35d33-185">True</span><span class="sxs-lookup"><span data-stu-id="35d33-185">True</span></span>                            |
| <span data-ttu-id="35d33-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="35d33-186">Is Indexed</span></span>             | <span data-ttu-id="35d33-187">False</span><span class="sxs-lookup"><span data-stu-id="35d33-187">False</span></span>                           |
| <span data-ttu-id="35d33-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="35d33-188">In Global Catalog</span></span>      | <span data-ttu-id="35d33-189">True</span><span class="sxs-lookup"><span data-stu-id="35d33-189">True</span></span>                            |
| <span data-ttu-id="35d33-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="35d33-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="35d33-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="35d33-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="35d33-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35d33-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="35d33-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35d33-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="35d33-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35d33-194">Search-Flags</span></span>           | <span data-ttu-id="35d33-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35d33-195">0x00000000</span></span>                      |
| <span data-ttu-id="35d33-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35d33-196">System-Flags</span></span>           | <span data-ttu-id="35d33-197">0x00000012</span><span class="sxs-lookup"><span data-stu-id="35d33-197">0x00000012</span></span>                      |
| <span data-ttu-id="35d33-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="35d33-198">Classes used in</span></span>        | [<span data-ttu-id="35d33-199">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="35d33-199">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="35d33-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="35d33-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="35d33-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="35d33-201">Entry</span></span> | <span data-ttu-id="35d33-202">Value</span><span class="sxs-lookup"><span data-stu-id="35d33-202">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="35d33-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="35d33-203">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="35d33-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35d33-204">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="35d33-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="35d33-205">System-Only</span></span>            | <span data-ttu-id="35d33-206">True</span><span class="sxs-lookup"><span data-stu-id="35d33-206">True</span></span>                            |
| <span data-ttu-id="35d33-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="35d33-207">Is-Single-Valued</span></span>       | <span data-ttu-id="35d33-208">True</span><span class="sxs-lookup"><span data-stu-id="35d33-208">True</span></span>                            |
| <span data-ttu-id="35d33-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="35d33-209">Is Indexed</span></span>             | <span data-ttu-id="35d33-210">False</span><span class="sxs-lookup"><span data-stu-id="35d33-210">False</span></span>                           |
| <span data-ttu-id="35d33-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="35d33-211">In Global Catalog</span></span>      | <span data-ttu-id="35d33-212">True</span><span class="sxs-lookup"><span data-stu-id="35d33-212">True</span></span>                            |
| <span data-ttu-id="35d33-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="35d33-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="35d33-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="35d33-214">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="35d33-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35d33-215">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="35d33-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35d33-216">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="35d33-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35d33-217">Search-Flags</span></span>           | <span data-ttu-id="35d33-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35d33-218">0x00000000</span></span>                      |
| <span data-ttu-id="35d33-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35d33-219">System-Flags</span></span>           | <span data-ttu-id="35d33-220">0x00000012</span><span class="sxs-lookup"><span data-stu-id="35d33-220">0x00000012</span></span>                      |
| <span data-ttu-id="35d33-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="35d33-221">Classes used in</span></span>        | [<span data-ttu-id="35d33-222">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="35d33-222">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="35d33-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35d33-223">Windows Server 2008</span></span>



| <span data-ttu-id="35d33-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="35d33-224">Entry</span></span> | <span data-ttu-id="35d33-225">Value</span><span class="sxs-lookup"><span data-stu-id="35d33-225">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="35d33-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="35d33-226">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="35d33-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35d33-227">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="35d33-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="35d33-228">System-Only</span></span>            | <span data-ttu-id="35d33-229">True</span><span class="sxs-lookup"><span data-stu-id="35d33-229">True</span></span>                            |
| <span data-ttu-id="35d33-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="35d33-230">Is-Single-Valued</span></span>       | <span data-ttu-id="35d33-231">True</span><span class="sxs-lookup"><span data-stu-id="35d33-231">True</span></span>                            |
| <span data-ttu-id="35d33-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="35d33-232">Is Indexed</span></span>             | <span data-ttu-id="35d33-233">False</span><span class="sxs-lookup"><span data-stu-id="35d33-233">False</span></span>                           |
| <span data-ttu-id="35d33-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="35d33-234">In Global Catalog</span></span>      | <span data-ttu-id="35d33-235">True</span><span class="sxs-lookup"><span data-stu-id="35d33-235">True</span></span>                            |
| <span data-ttu-id="35d33-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="35d33-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="35d33-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="35d33-237">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="35d33-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35d33-238">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="35d33-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35d33-239">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="35d33-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35d33-240">Search-Flags</span></span>           | <span data-ttu-id="35d33-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35d33-241">0x00000000</span></span>                      |
| <span data-ttu-id="35d33-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35d33-242">System-Flags</span></span>           | <span data-ttu-id="35d33-243">0x00000012</span><span class="sxs-lookup"><span data-stu-id="35d33-243">0x00000012</span></span>                      |
| <span data-ttu-id="35d33-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="35d33-244">Classes used in</span></span>        | [<span data-ttu-id="35d33-245">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="35d33-245">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="35d33-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="35d33-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="35d33-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="35d33-247">Entry</span></span> | <span data-ttu-id="35d33-248">Value</span><span class="sxs-lookup"><span data-stu-id="35d33-248">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="35d33-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="35d33-249">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="35d33-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35d33-250">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="35d33-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="35d33-251">System-Only</span></span>            | <span data-ttu-id="35d33-252">True</span><span class="sxs-lookup"><span data-stu-id="35d33-252">True</span></span>                            |
| <span data-ttu-id="35d33-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="35d33-253">Is-Single-Valued</span></span>       | <span data-ttu-id="35d33-254">True</span><span class="sxs-lookup"><span data-stu-id="35d33-254">True</span></span>                            |
| <span data-ttu-id="35d33-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="35d33-255">Is Indexed</span></span>             | <span data-ttu-id="35d33-256">False</span><span class="sxs-lookup"><span data-stu-id="35d33-256">False</span></span>                           |
| <span data-ttu-id="35d33-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="35d33-257">In Global Catalog</span></span>      | <span data-ttu-id="35d33-258">True</span><span class="sxs-lookup"><span data-stu-id="35d33-258">True</span></span>                            |
| <span data-ttu-id="35d33-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="35d33-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="35d33-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="35d33-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="35d33-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35d33-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="35d33-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35d33-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="35d33-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35d33-263">Search-Flags</span></span>           | <span data-ttu-id="35d33-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35d33-264">0x00000000</span></span>                      |
| <span data-ttu-id="35d33-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35d33-265">System-Flags</span></span>           | <span data-ttu-id="35d33-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="35d33-266">0x00000012</span></span>                      |
| <span data-ttu-id="35d33-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="35d33-267">Classes used in</span></span>        | [<span data-ttu-id="35d33-268">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="35d33-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="35d33-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="35d33-269">Windows Server 2012</span></span>



| <span data-ttu-id="35d33-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="35d33-270">Entry</span></span> | <span data-ttu-id="35d33-271">Value</span><span class="sxs-lookup"><span data-stu-id="35d33-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="35d33-272">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="35d33-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="35d33-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35d33-273">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="35d33-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="35d33-274">System-Only</span></span>            | <span data-ttu-id="35d33-275">True</span><span class="sxs-lookup"><span data-stu-id="35d33-275">True</span></span>                            |
| <span data-ttu-id="35d33-276">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="35d33-276">Is-Single-Valued</span></span>       | <span data-ttu-id="35d33-277">True</span><span class="sxs-lookup"><span data-stu-id="35d33-277">True</span></span>                            |
| <span data-ttu-id="35d33-278">Está indexado</span><span class="sxs-lookup"><span data-stu-id="35d33-278">Is Indexed</span></span>             | <span data-ttu-id="35d33-279">False</span><span class="sxs-lookup"><span data-stu-id="35d33-279">False</span></span>                           |
| <span data-ttu-id="35d33-280">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="35d33-280">In Global Catalog</span></span>      | <span data-ttu-id="35d33-281">True</span><span class="sxs-lookup"><span data-stu-id="35d33-281">True</span></span>                            |
| <span data-ttu-id="35d33-282">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="35d33-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="35d33-283">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="35d33-283">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="35d33-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35d33-284">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="35d33-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35d33-285">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="35d33-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35d33-286">Search-Flags</span></span>           | <span data-ttu-id="35d33-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35d33-287">0x00000000</span></span>                      |
| <span data-ttu-id="35d33-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35d33-288">System-Flags</span></span>           | <span data-ttu-id="35d33-289">0x00000012</span><span class="sxs-lookup"><span data-stu-id="35d33-289">0x00000012</span></span>                      |
| <span data-ttu-id="35d33-290">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="35d33-290">Classes used in</span></span>        | [<span data-ttu-id="35d33-291">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="35d33-291">**Top**</span></span>](c-top.md)<br/> |



 

 





