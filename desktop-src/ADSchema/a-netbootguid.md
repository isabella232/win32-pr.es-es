---
title: 'Netboot: atributo GUID'
description: 'Arranque sin disco: el GUID del equipo se inicia en el panel. Corresponde a la dirección MAC de la tarjeta de red del equipo.'
ms.assetid: 60ce0482-79a3-499a-9607-f1f496e297d0
ms.tgt_platform: multiple
keywords:
- 'Netboot: esquema de AD del atributo GUID'
- netbootGUID esquema de AD de atributos
topic_type:
- apiref
api_name:
- Netboot-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7c09d6f9139580ad329b47f13999d348abf5a87
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906151"
---
# <a name="netboot-guid-attribute"></a><span data-ttu-id="21e40-106">Netboot: atributo GUID</span><span class="sxs-lookup"><span data-stu-id="21e40-106">Netboot-GUID attribute</span></span>

<span data-ttu-id="21e40-107">Arranque sin disco: el GUID en el panel de un equipo.</span><span class="sxs-lookup"><span data-stu-id="21e40-107">Diskless boot: A computer's on-board GUID.</span></span> <span data-ttu-id="21e40-108">Corresponde a la dirección MAC de la tarjeta de red del equipo.</span><span class="sxs-lookup"><span data-stu-id="21e40-108">Corresponds to the computer's network card MAC address.</span></span>



| <span data-ttu-id="21e40-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="21e40-109">Entry</span></span> | <span data-ttu-id="21e40-110">Value</span><span class="sxs-lookup"><span data-stu-id="21e40-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="21e40-111">CN</span><span class="sxs-lookup"><span data-stu-id="21e40-111">CN</span></span>                | <span data-ttu-id="21e40-112">Netboot-GUID</span><span class="sxs-lookup"><span data-stu-id="21e40-112">Netboot-GUID</span></span>                                          |
| <span data-ttu-id="21e40-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="21e40-113">Ldap-Display-Name</span></span> | <span data-ttu-id="21e40-114">netbootGUID</span><span class="sxs-lookup"><span data-stu-id="21e40-114">netbootGUID</span></span>                                           |
| <span data-ttu-id="21e40-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="21e40-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="21e40-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="21e40-116">Update Privilege</span></span>  | <span data-ttu-id="21e40-117">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="21e40-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="21e40-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="21e40-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="21e40-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="21e40-119">Attribute-Id</span></span>      | <span data-ttu-id="21e40-120">1.2.840.113556.1.4.359</span><span class="sxs-lookup"><span data-stu-id="21e40-120">1.2.840.113556.1.4.359</span></span>                                |
| <span data-ttu-id="21e40-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="21e40-121">System-Id-Guid</span></span>    | <span data-ttu-id="21e40-122">3e978921-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="21e40-122">3e978921-8c01-11d0-afda-00c04fd930c9</span></span>                  |
| <span data-ttu-id="21e40-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21e40-123">Syntax</span></span>            | [<span data-ttu-id="21e40-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="21e40-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="21e40-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="21e40-125">Implementations</span></span>

-   [<span data-ttu-id="21e40-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="21e40-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="21e40-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="21e40-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="21e40-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="21e40-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="21e40-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="21e40-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="21e40-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="21e40-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="21e40-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="21e40-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="21e40-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="21e40-132">Windows 2000 Server</span></span>



| <span data-ttu-id="21e40-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="21e40-133">Entry</span></span> | <span data-ttu-id="21e40-134">Value</span><span class="sxs-lookup"><span data-stu-id="21e40-134">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="21e40-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="21e40-135">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="21e40-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21e40-136">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="21e40-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="21e40-137">System-Only</span></span>            | <span data-ttu-id="21e40-138">False</span><span class="sxs-lookup"><span data-stu-id="21e40-138">False</span></span>                                     |
| <span data-ttu-id="21e40-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="21e40-139">Is-Single-Valued</span></span>       | <span data-ttu-id="21e40-140">True</span><span class="sxs-lookup"><span data-stu-id="21e40-140">True</span></span>                                      |
| <span data-ttu-id="21e40-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="21e40-141">Is Indexed</span></span>             | <span data-ttu-id="21e40-142">True</span><span class="sxs-lookup"><span data-stu-id="21e40-142">True</span></span>                                      |
| <span data-ttu-id="21e40-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="21e40-143">In Global Catalog</span></span>      | <span data-ttu-id="21e40-144">True</span><span class="sxs-lookup"><span data-stu-id="21e40-144">True</span></span>                                      |
| <span data-ttu-id="21e40-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="21e40-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="21e40-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21e40-146">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="21e40-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21e40-147">Range-Lower</span></span>            | <span data-ttu-id="21e40-148">16</span><span class="sxs-lookup"><span data-stu-id="21e40-148">16</span></span>                                        |
| <span data-ttu-id="21e40-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21e40-149">Range-Upper</span></span>            | <span data-ttu-id="21e40-150">16</span><span class="sxs-lookup"><span data-stu-id="21e40-150">16</span></span>                                        |
| <span data-ttu-id="21e40-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21e40-151">Search-Flags</span></span>           | <span data-ttu-id="21e40-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21e40-152">0x00000001</span></span>                                |
| <span data-ttu-id="21e40-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21e40-153">System-Flags</span></span>           | <span data-ttu-id="21e40-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21e40-154">0x00000010</span></span>                                |
| <span data-ttu-id="21e40-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="21e40-155">Classes used in</span></span>        | [<span data-ttu-id="21e40-156">**Computer**</span><span class="sxs-lookup"><span data-stu-id="21e40-156">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="21e40-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="21e40-157">Windows Server 2003</span></span>



| <span data-ttu-id="21e40-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="21e40-158">Entry</span></span> | <span data-ttu-id="21e40-159">Value</span><span class="sxs-lookup"><span data-stu-id="21e40-159">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="21e40-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="21e40-160">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="21e40-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21e40-161">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="21e40-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="21e40-162">System-Only</span></span>            | <span data-ttu-id="21e40-163">False</span><span class="sxs-lookup"><span data-stu-id="21e40-163">False</span></span>                                     |
| <span data-ttu-id="21e40-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="21e40-164">Is-Single-Valued</span></span>       | <span data-ttu-id="21e40-165">True</span><span class="sxs-lookup"><span data-stu-id="21e40-165">True</span></span>                                      |
| <span data-ttu-id="21e40-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="21e40-166">Is Indexed</span></span>             | <span data-ttu-id="21e40-167">True</span><span class="sxs-lookup"><span data-stu-id="21e40-167">True</span></span>                                      |
| <span data-ttu-id="21e40-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="21e40-168">In Global Catalog</span></span>      | <span data-ttu-id="21e40-169">True</span><span class="sxs-lookup"><span data-stu-id="21e40-169">True</span></span>                                      |
| <span data-ttu-id="21e40-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="21e40-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="21e40-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21e40-171">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="21e40-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21e40-172">Range-Lower</span></span>            | <span data-ttu-id="21e40-173">16</span><span class="sxs-lookup"><span data-stu-id="21e40-173">16</span></span>                                        |
| <span data-ttu-id="21e40-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21e40-174">Range-Upper</span></span>            | <span data-ttu-id="21e40-175">16</span><span class="sxs-lookup"><span data-stu-id="21e40-175">16</span></span>                                        |
| <span data-ttu-id="21e40-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21e40-176">Search-Flags</span></span>           | <span data-ttu-id="21e40-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21e40-177">0x00000001</span></span>                                |
| <span data-ttu-id="21e40-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21e40-178">System-Flags</span></span>           | <span data-ttu-id="21e40-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21e40-179">0x00000010</span></span>                                |
| <span data-ttu-id="21e40-180">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="21e40-180">Classes used in</span></span>        | [<span data-ttu-id="21e40-181">**Computer**</span><span class="sxs-lookup"><span data-stu-id="21e40-181">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="21e40-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="21e40-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="21e40-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="21e40-183">Entry</span></span> | <span data-ttu-id="21e40-184">Value</span><span class="sxs-lookup"><span data-stu-id="21e40-184">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="21e40-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="21e40-185">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="21e40-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21e40-186">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="21e40-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="21e40-187">System-Only</span></span>            | <span data-ttu-id="21e40-188">False</span><span class="sxs-lookup"><span data-stu-id="21e40-188">False</span></span>                                     |
| <span data-ttu-id="21e40-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="21e40-189">Is-Single-Valued</span></span>       | <span data-ttu-id="21e40-190">True</span><span class="sxs-lookup"><span data-stu-id="21e40-190">True</span></span>                                      |
| <span data-ttu-id="21e40-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="21e40-191">Is Indexed</span></span>             | <span data-ttu-id="21e40-192">True</span><span class="sxs-lookup"><span data-stu-id="21e40-192">True</span></span>                                      |
| <span data-ttu-id="21e40-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="21e40-193">In Global Catalog</span></span>      | <span data-ttu-id="21e40-194">True</span><span class="sxs-lookup"><span data-stu-id="21e40-194">True</span></span>                                      |
| <span data-ttu-id="21e40-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="21e40-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="21e40-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21e40-196">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="21e40-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21e40-197">Range-Lower</span></span>            | <span data-ttu-id="21e40-198">16</span><span class="sxs-lookup"><span data-stu-id="21e40-198">16</span></span>                                        |
| <span data-ttu-id="21e40-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21e40-199">Range-Upper</span></span>            | <span data-ttu-id="21e40-200">16</span><span class="sxs-lookup"><span data-stu-id="21e40-200">16</span></span>                                        |
| <span data-ttu-id="21e40-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21e40-201">Search-Flags</span></span>           | <span data-ttu-id="21e40-202">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21e40-202">0x00000001</span></span>                                |
| <span data-ttu-id="21e40-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21e40-203">System-Flags</span></span>           | <span data-ttu-id="21e40-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21e40-204">0x00000010</span></span>                                |
| <span data-ttu-id="21e40-205">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="21e40-205">Classes used in</span></span>        | [<span data-ttu-id="21e40-206">**Computer**</span><span class="sxs-lookup"><span data-stu-id="21e40-206">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="21e40-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21e40-207">Windows Server 2008</span></span>



| <span data-ttu-id="21e40-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="21e40-208">Entry</span></span> | <span data-ttu-id="21e40-209">Value</span><span class="sxs-lookup"><span data-stu-id="21e40-209">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="21e40-210">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="21e40-210">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="21e40-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21e40-211">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="21e40-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="21e40-212">System-Only</span></span>            | <span data-ttu-id="21e40-213">False</span><span class="sxs-lookup"><span data-stu-id="21e40-213">False</span></span>                                     |
| <span data-ttu-id="21e40-214">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="21e40-214">Is-Single-Valued</span></span>       | <span data-ttu-id="21e40-215">True</span><span class="sxs-lookup"><span data-stu-id="21e40-215">True</span></span>                                      |
| <span data-ttu-id="21e40-216">Está indexado</span><span class="sxs-lookup"><span data-stu-id="21e40-216">Is Indexed</span></span>             | <span data-ttu-id="21e40-217">True</span><span class="sxs-lookup"><span data-stu-id="21e40-217">True</span></span>                                      |
| <span data-ttu-id="21e40-218">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="21e40-218">In Global Catalog</span></span>      | <span data-ttu-id="21e40-219">True</span><span class="sxs-lookup"><span data-stu-id="21e40-219">True</span></span>                                      |
| <span data-ttu-id="21e40-220">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="21e40-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="21e40-221">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21e40-221">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="21e40-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21e40-222">Range-Lower</span></span>            | <span data-ttu-id="21e40-223">16</span><span class="sxs-lookup"><span data-stu-id="21e40-223">16</span></span>                                        |
| <span data-ttu-id="21e40-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21e40-224">Range-Upper</span></span>            | <span data-ttu-id="21e40-225">16</span><span class="sxs-lookup"><span data-stu-id="21e40-225">16</span></span>                                        |
| <span data-ttu-id="21e40-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21e40-226">Search-Flags</span></span>           | <span data-ttu-id="21e40-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21e40-227">0x00000001</span></span>                                |
| <span data-ttu-id="21e40-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21e40-228">System-Flags</span></span>           | <span data-ttu-id="21e40-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21e40-229">0x00000010</span></span>                                |
| <span data-ttu-id="21e40-230">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="21e40-230">Classes used in</span></span>        | [<span data-ttu-id="21e40-231">**Computer**</span><span class="sxs-lookup"><span data-stu-id="21e40-231">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="21e40-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="21e40-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="21e40-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="21e40-233">Entry</span></span> | <span data-ttu-id="21e40-234">Value</span><span class="sxs-lookup"><span data-stu-id="21e40-234">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="21e40-235">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="21e40-235">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="21e40-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21e40-236">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="21e40-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="21e40-237">System-Only</span></span>            | <span data-ttu-id="21e40-238">False</span><span class="sxs-lookup"><span data-stu-id="21e40-238">False</span></span>                                     |
| <span data-ttu-id="21e40-239">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="21e40-239">Is-Single-Valued</span></span>       | <span data-ttu-id="21e40-240">True</span><span class="sxs-lookup"><span data-stu-id="21e40-240">True</span></span>                                      |
| <span data-ttu-id="21e40-241">Está indexado</span><span class="sxs-lookup"><span data-stu-id="21e40-241">Is Indexed</span></span>             | <span data-ttu-id="21e40-242">True</span><span class="sxs-lookup"><span data-stu-id="21e40-242">True</span></span>                                      |
| <span data-ttu-id="21e40-243">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="21e40-243">In Global Catalog</span></span>      | <span data-ttu-id="21e40-244">True</span><span class="sxs-lookup"><span data-stu-id="21e40-244">True</span></span>                                      |
| <span data-ttu-id="21e40-245">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="21e40-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="21e40-246">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21e40-246">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="21e40-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21e40-247">Range-Lower</span></span>            | <span data-ttu-id="21e40-248">16</span><span class="sxs-lookup"><span data-stu-id="21e40-248">16</span></span>                                        |
| <span data-ttu-id="21e40-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21e40-249">Range-Upper</span></span>            | <span data-ttu-id="21e40-250">16</span><span class="sxs-lookup"><span data-stu-id="21e40-250">16</span></span>                                        |
| <span data-ttu-id="21e40-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21e40-251">Search-Flags</span></span>           | <span data-ttu-id="21e40-252">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21e40-252">0x00000001</span></span>                                |
| <span data-ttu-id="21e40-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21e40-253">System-Flags</span></span>           | <span data-ttu-id="21e40-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21e40-254">0x00000010</span></span>                                |
| <span data-ttu-id="21e40-255">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="21e40-255">Classes used in</span></span>        | [<span data-ttu-id="21e40-256">**Computer**</span><span class="sxs-lookup"><span data-stu-id="21e40-256">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="21e40-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21e40-257">Windows Server 2012</span></span>



| <span data-ttu-id="21e40-258">Entrada</span><span class="sxs-lookup"><span data-stu-id="21e40-258">Entry</span></span> | <span data-ttu-id="21e40-259">Value</span><span class="sxs-lookup"><span data-stu-id="21e40-259">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="21e40-260">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="21e40-260">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="21e40-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21e40-261">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="21e40-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="21e40-262">System-Only</span></span>            | <span data-ttu-id="21e40-263">False</span><span class="sxs-lookup"><span data-stu-id="21e40-263">False</span></span>                                     |
| <span data-ttu-id="21e40-264">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="21e40-264">Is-Single-Valued</span></span>       | <span data-ttu-id="21e40-265">True</span><span class="sxs-lookup"><span data-stu-id="21e40-265">True</span></span>                                      |
| <span data-ttu-id="21e40-266">Está indexado</span><span class="sxs-lookup"><span data-stu-id="21e40-266">Is Indexed</span></span>             | <span data-ttu-id="21e40-267">True</span><span class="sxs-lookup"><span data-stu-id="21e40-267">True</span></span>                                      |
| <span data-ttu-id="21e40-268">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="21e40-268">In Global Catalog</span></span>      | <span data-ttu-id="21e40-269">True</span><span class="sxs-lookup"><span data-stu-id="21e40-269">True</span></span>                                      |
| <span data-ttu-id="21e40-270">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="21e40-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="21e40-271">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21e40-271">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="21e40-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21e40-272">Range-Lower</span></span>            | <span data-ttu-id="21e40-273">16</span><span class="sxs-lookup"><span data-stu-id="21e40-273">16</span></span>                                        |
| <span data-ttu-id="21e40-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21e40-274">Range-Upper</span></span>            | <span data-ttu-id="21e40-275">16</span><span class="sxs-lookup"><span data-stu-id="21e40-275">16</span></span>                                        |
| <span data-ttu-id="21e40-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21e40-276">Search-Flags</span></span>           | <span data-ttu-id="21e40-277">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21e40-277">0x00000001</span></span>                                |
| <span data-ttu-id="21e40-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21e40-278">System-Flags</span></span>           | <span data-ttu-id="21e40-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21e40-279">0x00000010</span></span>                                |
| <span data-ttu-id="21e40-280">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="21e40-280">Classes used in</span></span>        | [<span data-ttu-id="21e40-281">**Computer**</span><span class="sxs-lookup"><span data-stu-id="21e40-281">**Computer**</span></span>](c-computer.md)<br/> |



 

 





