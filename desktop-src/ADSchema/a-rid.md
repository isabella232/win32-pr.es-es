---
title: Atributo RID
description: Identificador relativo de un objeto.
ms.assetid: 52110cac-033c-475c-84d7-aff631af3413
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo RID
- Esquema de AD de atributo RID
topic_type:
- apiref
api_name:
- Rid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90ab6327fccf804b21a9ba7de6881f98ea4f97be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997513"
---
# <a name="rid-attribute"></a><span data-ttu-id="df5ce-105">Atributo RID</span><span class="sxs-lookup"><span data-stu-id="df5ce-105">Rid attribute</span></span>

<span data-ttu-id="df5ce-106">Identificador relativo de un objeto.</span><span class="sxs-lookup"><span data-stu-id="df5ce-106">The relative Identifier of an object.</span></span>



| <span data-ttu-id="df5ce-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="df5ce-107">Entry</span></span> | <span data-ttu-id="df5ce-108">Value</span><span class="sxs-lookup"><span data-stu-id="df5ce-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="df5ce-109">CN</span><span class="sxs-lookup"><span data-stu-id="df5ce-109">CN</span></span>                | <span data-ttu-id="df5ce-110">Libra</span><span class="sxs-lookup"><span data-stu-id="df5ce-110">Rid</span></span>                                         |
| <span data-ttu-id="df5ce-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="df5ce-111">Ldap-Display-Name</span></span> | <span data-ttu-id="df5ce-112">rid</span><span class="sxs-lookup"><span data-stu-id="df5ce-112">rid</span></span>                                         |
| <span data-ttu-id="df5ce-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="df5ce-113">Size</span></span>              | <span data-ttu-id="df5ce-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="df5ce-114">4 bytes</span></span>                                     |
| <span data-ttu-id="df5ce-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="df5ce-115">Update Privilege</span></span>  | <span data-ttu-id="df5ce-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="df5ce-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="df5ce-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="df5ce-117">Update Frequency</span></span>  | <span data-ttu-id="df5ce-118">Cuando se crea un objeto que necesita un RID.</span><span class="sxs-lookup"><span data-stu-id="df5ce-118">When an object that needs a RID is created.</span></span> |
| <span data-ttu-id="df5ce-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="df5ce-119">Attribute-Id</span></span>      | <span data-ttu-id="df5ce-120">1.2.840.113556.1.4.153</span><span class="sxs-lookup"><span data-stu-id="df5ce-120">1.2.840.113556.1.4.153</span></span>                      |
| <span data-ttu-id="df5ce-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="df5ce-121">System-Id-Guid</span></span>    | <span data-ttu-id="df5ce-122">bf967a22-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="df5ce-122">bf967a22-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="df5ce-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df5ce-123">Syntax</span></span>            | [<span data-ttu-id="df5ce-124">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="df5ce-124">**Enumeration**</span></span>](s-enumeration.md)        |



## <a name="implementations"></a><span data-ttu-id="df5ce-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="df5ce-125">Implementations</span></span>

-   [<span data-ttu-id="df5ce-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="df5ce-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="df5ce-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="df5ce-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="df5ce-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="df5ce-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="df5ce-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="df5ce-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="df5ce-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="df5ce-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="df5ce-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="df5ce-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="df5ce-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="df5ce-132">Windows 2000 Server</span></span>



| <span data-ttu-id="df5ce-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="df5ce-133">Entry</span></span> | <span data-ttu-id="df5ce-134">Value</span><span class="sxs-lookup"><span data-stu-id="df5ce-134">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="df5ce-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="df5ce-135">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df5ce-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df5ce-136">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df5ce-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="df5ce-137">System-Only</span></span>            | <span data-ttu-id="df5ce-138">False</span><span class="sxs-lookup"><span data-stu-id="df5ce-138">False</span></span>                                                        |
| <span data-ttu-id="df5ce-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="df5ce-139">Is-Single-Valued</span></span>       | <span data-ttu-id="df5ce-140">True</span><span class="sxs-lookup"><span data-stu-id="df5ce-140">True</span></span>                                                         |
| <span data-ttu-id="df5ce-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="df5ce-141">Is Indexed</span></span>             | <span data-ttu-id="df5ce-142">False</span><span class="sxs-lookup"><span data-stu-id="df5ce-142">False</span></span>                                                        |
| <span data-ttu-id="df5ce-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="df5ce-143">In Global Catalog</span></span>      | <span data-ttu-id="df5ce-144">False</span><span class="sxs-lookup"><span data-stu-id="df5ce-144">False</span></span>                                                        |
| <span data-ttu-id="df5ce-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="df5ce-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="df5ce-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="df5ce-146">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="df5ce-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df5ce-147">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="df5ce-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df5ce-148">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="df5ce-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df5ce-149">Search-Flags</span></span>           | <span data-ttu-id="df5ce-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df5ce-150">0x00000000</span></span>                                                   |
| <span data-ttu-id="df5ce-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df5ce-151">System-Flags</span></span>           | <span data-ttu-id="df5ce-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df5ce-152">0x00000010</span></span>                                                   |
| <span data-ttu-id="df5ce-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="df5ce-153">Classes used in</span></span>        | [<span data-ttu-id="df5ce-154">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="df5ce-154">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="df5ce-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="df5ce-155">Windows Server 2003</span></span>



| <span data-ttu-id="df5ce-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="df5ce-156">Entry</span></span> | <span data-ttu-id="df5ce-157">Value</span><span class="sxs-lookup"><span data-stu-id="df5ce-157">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="df5ce-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="df5ce-158">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df5ce-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df5ce-159">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df5ce-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="df5ce-160">System-Only</span></span>            | <span data-ttu-id="df5ce-161">False</span><span class="sxs-lookup"><span data-stu-id="df5ce-161">False</span></span>                                                        |
| <span data-ttu-id="df5ce-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="df5ce-162">Is-Single-Valued</span></span>       | <span data-ttu-id="df5ce-163">True</span><span class="sxs-lookup"><span data-stu-id="df5ce-163">True</span></span>                                                         |
| <span data-ttu-id="df5ce-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="df5ce-164">Is Indexed</span></span>             | <span data-ttu-id="df5ce-165">False</span><span class="sxs-lookup"><span data-stu-id="df5ce-165">False</span></span>                                                        |
| <span data-ttu-id="df5ce-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="df5ce-166">In Global Catalog</span></span>      | <span data-ttu-id="df5ce-167">False</span><span class="sxs-lookup"><span data-stu-id="df5ce-167">False</span></span>                                                        |
| <span data-ttu-id="df5ce-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="df5ce-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="df5ce-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="df5ce-169">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="df5ce-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df5ce-170">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="df5ce-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df5ce-171">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="df5ce-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df5ce-172">Search-Flags</span></span>           | <span data-ttu-id="df5ce-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df5ce-173">0x00000000</span></span>                                                   |
| <span data-ttu-id="df5ce-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df5ce-174">System-Flags</span></span>           | <span data-ttu-id="df5ce-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df5ce-175">0x00000010</span></span>                                                   |
| <span data-ttu-id="df5ce-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="df5ce-176">Classes used in</span></span>        | [<span data-ttu-id="df5ce-177">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="df5ce-177">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="df5ce-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="df5ce-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="df5ce-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="df5ce-179">Entry</span></span> | <span data-ttu-id="df5ce-180">Value</span><span class="sxs-lookup"><span data-stu-id="df5ce-180">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="df5ce-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="df5ce-181">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df5ce-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df5ce-182">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df5ce-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="df5ce-183">System-Only</span></span>            | <span data-ttu-id="df5ce-184">False</span><span class="sxs-lookup"><span data-stu-id="df5ce-184">False</span></span>                                                        |
| <span data-ttu-id="df5ce-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="df5ce-185">Is-Single-Valued</span></span>       | <span data-ttu-id="df5ce-186">True</span><span class="sxs-lookup"><span data-stu-id="df5ce-186">True</span></span>                                                         |
| <span data-ttu-id="df5ce-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="df5ce-187">Is Indexed</span></span>             | <span data-ttu-id="df5ce-188">False</span><span class="sxs-lookup"><span data-stu-id="df5ce-188">False</span></span>                                                        |
| <span data-ttu-id="df5ce-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="df5ce-189">In Global Catalog</span></span>      | <span data-ttu-id="df5ce-190">False</span><span class="sxs-lookup"><span data-stu-id="df5ce-190">False</span></span>                                                        |
| <span data-ttu-id="df5ce-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="df5ce-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="df5ce-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="df5ce-192">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="df5ce-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df5ce-193">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="df5ce-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df5ce-194">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="df5ce-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df5ce-195">Search-Flags</span></span>           | <span data-ttu-id="df5ce-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df5ce-196">0x00000000</span></span>                                                   |
| <span data-ttu-id="df5ce-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df5ce-197">System-Flags</span></span>           | <span data-ttu-id="df5ce-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df5ce-198">0x00000010</span></span>                                                   |
| <span data-ttu-id="df5ce-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="df5ce-199">Classes used in</span></span>        | [<span data-ttu-id="df5ce-200">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="df5ce-200">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="df5ce-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df5ce-201">Windows Server 2008</span></span>



| <span data-ttu-id="df5ce-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="df5ce-202">Entry</span></span> | <span data-ttu-id="df5ce-203">Value</span><span class="sxs-lookup"><span data-stu-id="df5ce-203">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="df5ce-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="df5ce-204">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df5ce-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df5ce-205">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df5ce-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="df5ce-206">System-Only</span></span>            | <span data-ttu-id="df5ce-207">False</span><span class="sxs-lookup"><span data-stu-id="df5ce-207">False</span></span>                                                        |
| <span data-ttu-id="df5ce-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="df5ce-208">Is-Single-Valued</span></span>       | <span data-ttu-id="df5ce-209">True</span><span class="sxs-lookup"><span data-stu-id="df5ce-209">True</span></span>                                                         |
| <span data-ttu-id="df5ce-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="df5ce-210">Is Indexed</span></span>             | <span data-ttu-id="df5ce-211">False</span><span class="sxs-lookup"><span data-stu-id="df5ce-211">False</span></span>                                                        |
| <span data-ttu-id="df5ce-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="df5ce-212">In Global Catalog</span></span>      | <span data-ttu-id="df5ce-213">False</span><span class="sxs-lookup"><span data-stu-id="df5ce-213">False</span></span>                                                        |
| <span data-ttu-id="df5ce-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="df5ce-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="df5ce-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="df5ce-215">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="df5ce-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df5ce-216">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="df5ce-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df5ce-217">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="df5ce-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df5ce-218">Search-Flags</span></span>           | <span data-ttu-id="df5ce-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df5ce-219">0x00000000</span></span>                                                   |
| <span data-ttu-id="df5ce-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df5ce-220">System-Flags</span></span>           | <span data-ttu-id="df5ce-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df5ce-221">0x00000010</span></span>                                                   |
| <span data-ttu-id="df5ce-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="df5ce-222">Classes used in</span></span>        | [<span data-ttu-id="df5ce-223">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="df5ce-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="df5ce-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="df5ce-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="df5ce-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="df5ce-225">Entry</span></span> | <span data-ttu-id="df5ce-226">Value</span><span class="sxs-lookup"><span data-stu-id="df5ce-226">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="df5ce-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="df5ce-227">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df5ce-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df5ce-228">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df5ce-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="df5ce-229">System-Only</span></span>            | <span data-ttu-id="df5ce-230">False</span><span class="sxs-lookup"><span data-stu-id="df5ce-230">False</span></span>                                                        |
| <span data-ttu-id="df5ce-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="df5ce-231">Is-Single-Valued</span></span>       | <span data-ttu-id="df5ce-232">True</span><span class="sxs-lookup"><span data-stu-id="df5ce-232">True</span></span>                                                         |
| <span data-ttu-id="df5ce-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="df5ce-233">Is Indexed</span></span>             | <span data-ttu-id="df5ce-234">False</span><span class="sxs-lookup"><span data-stu-id="df5ce-234">False</span></span>                                                        |
| <span data-ttu-id="df5ce-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="df5ce-235">In Global Catalog</span></span>      | <span data-ttu-id="df5ce-236">False</span><span class="sxs-lookup"><span data-stu-id="df5ce-236">False</span></span>                                                        |
| <span data-ttu-id="df5ce-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="df5ce-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="df5ce-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="df5ce-238">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="df5ce-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df5ce-239">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="df5ce-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df5ce-240">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="df5ce-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df5ce-241">Search-Flags</span></span>           | <span data-ttu-id="df5ce-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df5ce-242">0x00000000</span></span>                                                   |
| <span data-ttu-id="df5ce-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df5ce-243">System-Flags</span></span>           | <span data-ttu-id="df5ce-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df5ce-244">0x00000010</span></span>                                                   |
| <span data-ttu-id="df5ce-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="df5ce-245">Classes used in</span></span>        | [<span data-ttu-id="df5ce-246">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="df5ce-246">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="df5ce-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="df5ce-247">Windows Server 2012</span></span>



| <span data-ttu-id="df5ce-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="df5ce-248">Entry</span></span> | <span data-ttu-id="df5ce-249">Value</span><span class="sxs-lookup"><span data-stu-id="df5ce-249">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="df5ce-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="df5ce-250">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df5ce-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df5ce-251">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df5ce-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="df5ce-252">System-Only</span></span>            | <span data-ttu-id="df5ce-253">False</span><span class="sxs-lookup"><span data-stu-id="df5ce-253">False</span></span>                                                        |
| <span data-ttu-id="df5ce-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="df5ce-254">Is-Single-Valued</span></span>       | <span data-ttu-id="df5ce-255">True</span><span class="sxs-lookup"><span data-stu-id="df5ce-255">True</span></span>                                                         |
| <span data-ttu-id="df5ce-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="df5ce-256">Is Indexed</span></span>             | <span data-ttu-id="df5ce-257">False</span><span class="sxs-lookup"><span data-stu-id="df5ce-257">False</span></span>                                                        |
| <span data-ttu-id="df5ce-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="df5ce-258">In Global Catalog</span></span>      | <span data-ttu-id="df5ce-259">False</span><span class="sxs-lookup"><span data-stu-id="df5ce-259">False</span></span>                                                        |
| <span data-ttu-id="df5ce-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="df5ce-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="df5ce-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="df5ce-261">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="df5ce-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df5ce-262">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="df5ce-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df5ce-263">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="df5ce-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df5ce-264">Search-Flags</span></span>           | <span data-ttu-id="df5ce-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df5ce-265">0x00000000</span></span>                                                   |
| <span data-ttu-id="df5ce-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df5ce-266">System-Flags</span></span>           | <span data-ttu-id="df5ce-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df5ce-267">0x00000010</span></span>                                                   |
| <span data-ttu-id="df5ce-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="df5ce-268">Classes used in</span></span>        | [<span data-ttu-id="df5ce-269">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="df5ce-269">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





