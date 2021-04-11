---
title: Rights-Guid atributo)
description: GUID que se usa para representar un derecho extendido dentro de una entrada de control de acceso.
ms.assetid: 6f3a654e-fead-41e7-8383-6dade1a2747e
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Rights-Guid
- rightsGuid esquema de AD de atributos
topic_type:
- apiref
api_name:
- Rights-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4da47ec8e4736dd13b6ba39da0208aed505aa8a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151726"
---
# <a name="rights-guid-attribute"></a><span data-ttu-id="40ce7-105">Rights-Guid atributo)</span><span class="sxs-lookup"><span data-stu-id="40ce7-105">Rights-Guid attribute</span></span>

<span data-ttu-id="40ce7-106">GUID que se usa para representar un derecho extendido dentro de una entrada de control de acceso.</span><span class="sxs-lookup"><span data-stu-id="40ce7-106">The GUID used to represent an extended right within an access control entry.</span></span>



| <span data-ttu-id="40ce7-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="40ce7-107">Entry</span></span> | <span data-ttu-id="40ce7-108">Value</span><span class="sxs-lookup"><span data-stu-id="40ce7-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="40ce7-109">CN</span><span class="sxs-lookup"><span data-stu-id="40ce7-109">CN</span></span>                | <span data-ttu-id="40ce7-110">Rights-Guid</span><span class="sxs-lookup"><span data-stu-id="40ce7-110">Rights-Guid</span></span>                                 |
| <span data-ttu-id="40ce7-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="40ce7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="40ce7-112">rightsGuid</span><span class="sxs-lookup"><span data-stu-id="40ce7-112">rightsGuid</span></span>                                  |
| <span data-ttu-id="40ce7-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="40ce7-113">Size</span></span>              | <span data-ttu-id="40ce7-114">16 bytes</span><span class="sxs-lookup"><span data-stu-id="40ce7-114">16 bytes</span></span>                                    |
| <span data-ttu-id="40ce7-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="40ce7-115">Update Privilege</span></span>  | <span data-ttu-id="40ce7-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="40ce7-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="40ce7-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="40ce7-117">Update Frequency</span></span>  | <span data-ttu-id="40ce7-118">Cuando se crea un derecho extendido nuevo.</span><span class="sxs-lookup"><span data-stu-id="40ce7-118">When a new extended right is created.</span></span>       |
| <span data-ttu-id="40ce7-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="40ce7-119">Attribute-Id</span></span>      | <span data-ttu-id="40ce7-120">1.2.840.113556.1.4.340</span><span class="sxs-lookup"><span data-stu-id="40ce7-120">1.2.840.113556.1.4.340</span></span>                      |
| <span data-ttu-id="40ce7-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="40ce7-121">System-Id-Guid</span></span>    | <span data-ttu-id="40ce7-122">8297931c-86d3-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="40ce7-122">8297931c-86d3-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="40ce7-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40ce7-123">Syntax</span></span>            | [<span data-ttu-id="40ce7-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="40ce7-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="40ce7-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="40ce7-125">Implementations</span></span>

-   [<span data-ttu-id="40ce7-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="40ce7-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="40ce7-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="40ce7-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="40ce7-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="40ce7-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="40ce7-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="40ce7-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="40ce7-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="40ce7-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="40ce7-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="40ce7-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="40ce7-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="40ce7-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="40ce7-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="40ce7-133">Windows 2000 Server</span></span>



| <span data-ttu-id="40ce7-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="40ce7-134">Entry</span></span> | <span data-ttu-id="40ce7-135">Value</span><span class="sxs-lookup"><span data-stu-id="40ce7-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="40ce7-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="40ce7-136">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="40ce7-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40ce7-137">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="40ce7-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="40ce7-138">System-Only</span></span>            | <span data-ttu-id="40ce7-139">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-139">False</span></span>                                                           |
| <span data-ttu-id="40ce7-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="40ce7-140">Is-Single-Valued</span></span>       | <span data-ttu-id="40ce7-141">True</span><span class="sxs-lookup"><span data-stu-id="40ce7-141">True</span></span>                                                            |
| <span data-ttu-id="40ce7-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="40ce7-142">Is Indexed</span></span>             | <span data-ttu-id="40ce7-143">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-143">False</span></span>                                                           |
| <span data-ttu-id="40ce7-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="40ce7-144">In Global Catalog</span></span>      | <span data-ttu-id="40ce7-145">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-145">False</span></span>                                                           |
| <span data-ttu-id="40ce7-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="40ce7-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="40ce7-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="40ce7-147">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="40ce7-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40ce7-148">Range-Lower</span></span>            | <span data-ttu-id="40ce7-149">36</span><span class="sxs-lookup"><span data-stu-id="40ce7-149">36</span></span>                                                              |
| <span data-ttu-id="40ce7-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40ce7-150">Range-Upper</span></span>            | <span data-ttu-id="40ce7-151">36</span><span class="sxs-lookup"><span data-stu-id="40ce7-151">36</span></span>                                                              |
| <span data-ttu-id="40ce7-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40ce7-152">Search-Flags</span></span>           | <span data-ttu-id="40ce7-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40ce7-153">0x00000000</span></span>                                                      |
| <span data-ttu-id="40ce7-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40ce7-154">System-Flags</span></span>           | <span data-ttu-id="40ce7-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40ce7-155">0x00000010</span></span>                                                      |
| <span data-ttu-id="40ce7-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="40ce7-156">Classes used in</span></span>        | [<span data-ttu-id="40ce7-157">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="40ce7-157">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="40ce7-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="40ce7-158">Windows Server 2003</span></span>



| <span data-ttu-id="40ce7-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="40ce7-159">Entry</span></span> | <span data-ttu-id="40ce7-160">Value</span><span class="sxs-lookup"><span data-stu-id="40ce7-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="40ce7-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="40ce7-161">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="40ce7-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40ce7-162">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="40ce7-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="40ce7-163">System-Only</span></span>            | <span data-ttu-id="40ce7-164">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-164">False</span></span>                                                           |
| <span data-ttu-id="40ce7-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="40ce7-165">Is-Single-Valued</span></span>       | <span data-ttu-id="40ce7-166">True</span><span class="sxs-lookup"><span data-stu-id="40ce7-166">True</span></span>                                                            |
| <span data-ttu-id="40ce7-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="40ce7-167">Is Indexed</span></span>             | <span data-ttu-id="40ce7-168">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-168">False</span></span>                                                           |
| <span data-ttu-id="40ce7-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="40ce7-169">In Global Catalog</span></span>      | <span data-ttu-id="40ce7-170">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-170">False</span></span>                                                           |
| <span data-ttu-id="40ce7-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="40ce7-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="40ce7-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="40ce7-172">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="40ce7-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40ce7-173">Range-Lower</span></span>            | <span data-ttu-id="40ce7-174">36</span><span class="sxs-lookup"><span data-stu-id="40ce7-174">36</span></span>                                                              |
| <span data-ttu-id="40ce7-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40ce7-175">Range-Upper</span></span>            | <span data-ttu-id="40ce7-176">36</span><span class="sxs-lookup"><span data-stu-id="40ce7-176">36</span></span>                                                              |
| <span data-ttu-id="40ce7-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40ce7-177">Search-Flags</span></span>           | <span data-ttu-id="40ce7-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40ce7-178">0x00000000</span></span>                                                      |
| <span data-ttu-id="40ce7-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40ce7-179">System-Flags</span></span>           | <span data-ttu-id="40ce7-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40ce7-180">0x00000010</span></span>                                                      |
| <span data-ttu-id="40ce7-181">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="40ce7-181">Classes used in</span></span>        | [<span data-ttu-id="40ce7-182">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="40ce7-182">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="40ce7-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="40ce7-183">ADAM</span></span>



| <span data-ttu-id="40ce7-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="40ce7-184">Entry</span></span> | <span data-ttu-id="40ce7-185">Value</span><span class="sxs-lookup"><span data-stu-id="40ce7-185">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="40ce7-186">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="40ce7-186">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="40ce7-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40ce7-187">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="40ce7-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="40ce7-188">System-Only</span></span>            | <span data-ttu-id="40ce7-189">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-189">False</span></span>                                                           |
| <span data-ttu-id="40ce7-190">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="40ce7-190">Is-Single-Valued</span></span>       | <span data-ttu-id="40ce7-191">True</span><span class="sxs-lookup"><span data-stu-id="40ce7-191">True</span></span>                                                            |
| <span data-ttu-id="40ce7-192">Está indexado</span><span class="sxs-lookup"><span data-stu-id="40ce7-192">Is Indexed</span></span>             | <span data-ttu-id="40ce7-193">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-193">False</span></span>                                                           |
| <span data-ttu-id="40ce7-194">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="40ce7-194">In Global Catalog</span></span>      | <span data-ttu-id="40ce7-195">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-195">False</span></span>                                                           |
| <span data-ttu-id="40ce7-196">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="40ce7-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="40ce7-197">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="40ce7-197">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="40ce7-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40ce7-198">Range-Lower</span></span>            | <span data-ttu-id="40ce7-199">36</span><span class="sxs-lookup"><span data-stu-id="40ce7-199">36</span></span>                                                              |
| <span data-ttu-id="40ce7-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40ce7-200">Range-Upper</span></span>            | <span data-ttu-id="40ce7-201">36</span><span class="sxs-lookup"><span data-stu-id="40ce7-201">36</span></span>                                                              |
| <span data-ttu-id="40ce7-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40ce7-202">Search-Flags</span></span>           | <span data-ttu-id="40ce7-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40ce7-203">0x00000000</span></span>                                                      |
| <span data-ttu-id="40ce7-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40ce7-204">System-Flags</span></span>           | <span data-ttu-id="40ce7-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40ce7-205">0x00000010</span></span>                                                      |
| <span data-ttu-id="40ce7-206">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="40ce7-206">Classes used in</span></span>        | [<span data-ttu-id="40ce7-207">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="40ce7-207">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="40ce7-208">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="40ce7-208">Windows Server 2003 R2</span></span>



| <span data-ttu-id="40ce7-209">Entrada</span><span class="sxs-lookup"><span data-stu-id="40ce7-209">Entry</span></span> | <span data-ttu-id="40ce7-210">Value</span><span class="sxs-lookup"><span data-stu-id="40ce7-210">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="40ce7-211">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="40ce7-211">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="40ce7-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40ce7-212">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="40ce7-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="40ce7-213">System-Only</span></span>            | <span data-ttu-id="40ce7-214">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-214">False</span></span>                                                           |
| <span data-ttu-id="40ce7-215">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="40ce7-215">Is-Single-Valued</span></span>       | <span data-ttu-id="40ce7-216">True</span><span class="sxs-lookup"><span data-stu-id="40ce7-216">True</span></span>                                                            |
| <span data-ttu-id="40ce7-217">Está indexado</span><span class="sxs-lookup"><span data-stu-id="40ce7-217">Is Indexed</span></span>             | <span data-ttu-id="40ce7-218">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-218">False</span></span>                                                           |
| <span data-ttu-id="40ce7-219">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="40ce7-219">In Global Catalog</span></span>      | <span data-ttu-id="40ce7-220">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-220">False</span></span>                                                           |
| <span data-ttu-id="40ce7-221">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="40ce7-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="40ce7-222">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="40ce7-222">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="40ce7-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40ce7-223">Range-Lower</span></span>            | <span data-ttu-id="40ce7-224">36</span><span class="sxs-lookup"><span data-stu-id="40ce7-224">36</span></span>                                                              |
| <span data-ttu-id="40ce7-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40ce7-225">Range-Upper</span></span>            | <span data-ttu-id="40ce7-226">36</span><span class="sxs-lookup"><span data-stu-id="40ce7-226">36</span></span>                                                              |
| <span data-ttu-id="40ce7-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40ce7-227">Search-Flags</span></span>           | <span data-ttu-id="40ce7-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40ce7-228">0x00000000</span></span>                                                      |
| <span data-ttu-id="40ce7-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40ce7-229">System-Flags</span></span>           | <span data-ttu-id="40ce7-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40ce7-230">0x00000010</span></span>                                                      |
| <span data-ttu-id="40ce7-231">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="40ce7-231">Classes used in</span></span>        | [<span data-ttu-id="40ce7-232">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="40ce7-232">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="40ce7-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40ce7-233">Windows Server 2008</span></span>



| <span data-ttu-id="40ce7-234">Entrada</span><span class="sxs-lookup"><span data-stu-id="40ce7-234">Entry</span></span> | <span data-ttu-id="40ce7-235">Value</span><span class="sxs-lookup"><span data-stu-id="40ce7-235">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="40ce7-236">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="40ce7-236">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="40ce7-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40ce7-237">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="40ce7-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="40ce7-238">System-Only</span></span>            | <span data-ttu-id="40ce7-239">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-239">False</span></span>                                                           |
| <span data-ttu-id="40ce7-240">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="40ce7-240">Is-Single-Valued</span></span>       | <span data-ttu-id="40ce7-241">True</span><span class="sxs-lookup"><span data-stu-id="40ce7-241">True</span></span>                                                            |
| <span data-ttu-id="40ce7-242">Está indexado</span><span class="sxs-lookup"><span data-stu-id="40ce7-242">Is Indexed</span></span>             | <span data-ttu-id="40ce7-243">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-243">False</span></span>                                                           |
| <span data-ttu-id="40ce7-244">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="40ce7-244">In Global Catalog</span></span>      | <span data-ttu-id="40ce7-245">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-245">False</span></span>                                                           |
| <span data-ttu-id="40ce7-246">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="40ce7-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="40ce7-247">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="40ce7-247">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="40ce7-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40ce7-248">Range-Lower</span></span>            | <span data-ttu-id="40ce7-249">36</span><span class="sxs-lookup"><span data-stu-id="40ce7-249">36</span></span>                                                              |
| <span data-ttu-id="40ce7-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40ce7-250">Range-Upper</span></span>            | <span data-ttu-id="40ce7-251">36</span><span class="sxs-lookup"><span data-stu-id="40ce7-251">36</span></span>                                                              |
| <span data-ttu-id="40ce7-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40ce7-252">Search-Flags</span></span>           | <span data-ttu-id="40ce7-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40ce7-253">0x00000000</span></span>                                                      |
| <span data-ttu-id="40ce7-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40ce7-254">System-Flags</span></span>           | <span data-ttu-id="40ce7-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40ce7-255">0x00000010</span></span>                                                      |
| <span data-ttu-id="40ce7-256">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="40ce7-256">Classes used in</span></span>        | [<span data-ttu-id="40ce7-257">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="40ce7-257">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="40ce7-258">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="40ce7-258">Windows Server 2008 R2</span></span>



| <span data-ttu-id="40ce7-259">Entrada</span><span class="sxs-lookup"><span data-stu-id="40ce7-259">Entry</span></span> | <span data-ttu-id="40ce7-260">Value</span><span class="sxs-lookup"><span data-stu-id="40ce7-260">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="40ce7-261">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="40ce7-261">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="40ce7-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40ce7-262">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="40ce7-263">System-Only</span><span class="sxs-lookup"><span data-stu-id="40ce7-263">System-Only</span></span>            | <span data-ttu-id="40ce7-264">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-264">False</span></span>                                                           |
| <span data-ttu-id="40ce7-265">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="40ce7-265">Is-Single-Valued</span></span>       | <span data-ttu-id="40ce7-266">True</span><span class="sxs-lookup"><span data-stu-id="40ce7-266">True</span></span>                                                            |
| <span data-ttu-id="40ce7-267">Está indexado</span><span class="sxs-lookup"><span data-stu-id="40ce7-267">Is Indexed</span></span>             | <span data-ttu-id="40ce7-268">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-268">False</span></span>                                                           |
| <span data-ttu-id="40ce7-269">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="40ce7-269">In Global Catalog</span></span>      | <span data-ttu-id="40ce7-270">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-270">False</span></span>                                                           |
| <span data-ttu-id="40ce7-271">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="40ce7-271">NT-Security-Descriptor</span></span> | <span data-ttu-id="40ce7-272">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="40ce7-272">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="40ce7-273">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40ce7-273">Range-Lower</span></span>            | <span data-ttu-id="40ce7-274">36</span><span class="sxs-lookup"><span data-stu-id="40ce7-274">36</span></span>                                                              |
| <span data-ttu-id="40ce7-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40ce7-275">Range-Upper</span></span>            | <span data-ttu-id="40ce7-276">36</span><span class="sxs-lookup"><span data-stu-id="40ce7-276">36</span></span>                                                              |
| <span data-ttu-id="40ce7-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40ce7-277">Search-Flags</span></span>           | <span data-ttu-id="40ce7-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40ce7-278">0x00000000</span></span>                                                      |
| <span data-ttu-id="40ce7-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40ce7-279">System-Flags</span></span>           | <span data-ttu-id="40ce7-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40ce7-280">0x00000010</span></span>                                                      |
| <span data-ttu-id="40ce7-281">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="40ce7-281">Classes used in</span></span>        | [<span data-ttu-id="40ce7-282">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="40ce7-282">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="40ce7-283">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="40ce7-283">Windows Server 2012</span></span>



| <span data-ttu-id="40ce7-284">Entrada</span><span class="sxs-lookup"><span data-stu-id="40ce7-284">Entry</span></span> | <span data-ttu-id="40ce7-285">Value</span><span class="sxs-lookup"><span data-stu-id="40ce7-285">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="40ce7-286">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="40ce7-286">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="40ce7-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40ce7-287">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="40ce7-288">System-Only</span><span class="sxs-lookup"><span data-stu-id="40ce7-288">System-Only</span></span>            | <span data-ttu-id="40ce7-289">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-289">False</span></span>                                                           |
| <span data-ttu-id="40ce7-290">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="40ce7-290">Is-Single-Valued</span></span>       | <span data-ttu-id="40ce7-291">True</span><span class="sxs-lookup"><span data-stu-id="40ce7-291">True</span></span>                                                            |
| <span data-ttu-id="40ce7-292">Está indexado</span><span class="sxs-lookup"><span data-stu-id="40ce7-292">Is Indexed</span></span>             | <span data-ttu-id="40ce7-293">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-293">False</span></span>                                                           |
| <span data-ttu-id="40ce7-294">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="40ce7-294">In Global Catalog</span></span>      | <span data-ttu-id="40ce7-295">False</span><span class="sxs-lookup"><span data-stu-id="40ce7-295">False</span></span>                                                           |
| <span data-ttu-id="40ce7-296">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="40ce7-296">NT-Security-Descriptor</span></span> | <span data-ttu-id="40ce7-297">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="40ce7-297">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="40ce7-298">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40ce7-298">Range-Lower</span></span>            | <span data-ttu-id="40ce7-299">36</span><span class="sxs-lookup"><span data-stu-id="40ce7-299">36</span></span>                                                              |
| <span data-ttu-id="40ce7-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40ce7-300">Range-Upper</span></span>            | <span data-ttu-id="40ce7-301">36</span><span class="sxs-lookup"><span data-stu-id="40ce7-301">36</span></span>                                                              |
| <span data-ttu-id="40ce7-302">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40ce7-302">Search-Flags</span></span>           | <span data-ttu-id="40ce7-303">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40ce7-303">0x00000000</span></span>                                                      |
| <span data-ttu-id="40ce7-304">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40ce7-304">System-Flags</span></span>           | <span data-ttu-id="40ce7-305">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40ce7-305">0x00000010</span></span>                                                      |
| <span data-ttu-id="40ce7-306">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="40ce7-306">Classes used in</span></span>        | [<span data-ttu-id="40ce7-307">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="40ce7-307">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





