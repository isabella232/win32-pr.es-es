---
title: Initial-auth-entrante (atributo)
description: Contiene información sobre una solicitud de autenticación entrante inicial de un cliente a este servidor. Este servidor envía esta solicitud al servidor de autenticación del dominio.
ms.assetid: d49d45ae-87fe-415d-8110-79b2b321f2b6
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de entrada-autenticación inicial
- initialAuthIncoming esquema de AD de atributos
topic_type:
- apiref
api_name:
- Initial-Auth-Incoming
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 973b00abd5b77b713fc03b5efb3d4cf45b97fc19
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804778"
---
# <a name="initial-auth-incoming-attribute"></a><span data-ttu-id="b1b12-106">Initial-auth-entrante (atributo)</span><span class="sxs-lookup"><span data-stu-id="b1b12-106">Initial-Auth-Incoming attribute</span></span>

<span data-ttu-id="b1b12-107">Contiene información sobre una solicitud de autenticación entrante inicial de un cliente a este servidor.</span><span class="sxs-lookup"><span data-stu-id="b1b12-107">Contains information about an initial incoming authentication request by a client to this server.</span></span> <span data-ttu-id="b1b12-108">Este servidor envía esta solicitud al servidor de autenticación del dominio.</span><span class="sxs-lookup"><span data-stu-id="b1b12-108">This request is then sent by this server to the authentication server for the domain.</span></span>



| <span data-ttu-id="b1b12-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1b12-109">Entry</span></span> | <span data-ttu-id="b1b12-110">Value</span><span class="sxs-lookup"><span data-stu-id="b1b12-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b1b12-111">CN</span><span class="sxs-lookup"><span data-stu-id="b1b12-111">CN</span></span>                | <span data-ttu-id="b1b12-112">Autenticación inicial-entrante</span><span class="sxs-lookup"><span data-stu-id="b1b12-112">Initial-Auth-Incoming</span></span>                       |
| <span data-ttu-id="b1b12-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="b1b12-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b1b12-114">initialAuthIncoming</span><span class="sxs-lookup"><span data-stu-id="b1b12-114">initialAuthIncoming</span></span>                         |
| <span data-ttu-id="b1b12-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="b1b12-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="b1b12-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="b1b12-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="b1b12-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="b1b12-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b1b12-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b1b12-118">Attribute-Id</span></span>      | <span data-ttu-id="b1b12-119">1.2.840.113556.1.4.539</span><span class="sxs-lookup"><span data-stu-id="b1b12-119">1.2.840.113556.1.4.539</span></span>                      |
| <span data-ttu-id="b1b12-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b1b12-120">System-Id-Guid</span></span>    | <span data-ttu-id="b1b12-121">52458023-ca6a-11d0-AFFF-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="b1b12-121">52458023-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="b1b12-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1b12-122">Syntax</span></span>            | [<span data-ttu-id="b1b12-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b1b12-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b1b12-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="b1b12-124">Implementations</span></span>

-   [<span data-ttu-id="b1b12-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b1b12-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b1b12-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b1b12-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b1b12-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b1b12-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b1b12-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b1b12-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b1b12-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b1b12-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b1b12-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b1b12-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b1b12-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b1b12-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b1b12-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1b12-132">Entry</span></span> | <span data-ttu-id="b1b12-133">Value</span><span class="sxs-lookup"><span data-stu-id="b1b12-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b1b12-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b1b12-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1b12-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1b12-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1b12-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1b12-136">System-Only</span></span>            | <span data-ttu-id="b1b12-137">False</span><span class="sxs-lookup"><span data-stu-id="b1b12-137">False</span></span>                                                |
| <span data-ttu-id="b1b12-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b1b12-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b1b12-139">True</span><span class="sxs-lookup"><span data-stu-id="b1b12-139">True</span></span>                                                 |
| <span data-ttu-id="b1b12-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b1b12-140">Is Indexed</span></span>             | <span data-ttu-id="b1b12-141">False</span><span class="sxs-lookup"><span data-stu-id="b1b12-141">False</span></span>                                                |
| <span data-ttu-id="b1b12-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b1b12-142">In Global Catalog</span></span>      | <span data-ttu-id="b1b12-143">False</span><span class="sxs-lookup"><span data-stu-id="b1b12-143">False</span></span>                                                |
| <span data-ttu-id="b1b12-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b1b12-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1b12-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1b12-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b1b12-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1b12-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b1b12-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1b12-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b1b12-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1b12-148">Search-Flags</span></span>           | <span data-ttu-id="b1b12-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1b12-149">0x00000000</span></span>                                           |
| <span data-ttu-id="b1b12-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1b12-150">System-Flags</span></span>           | <span data-ttu-id="b1b12-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1b12-151">0x00000010</span></span>                                           |
| <span data-ttu-id="b1b12-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b1b12-152">Classes used in</span></span>        | [<span data-ttu-id="b1b12-153">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="b1b12-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b1b12-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1b12-154">Windows Server 2003</span></span>



| <span data-ttu-id="b1b12-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1b12-155">Entry</span></span> | <span data-ttu-id="b1b12-156">Value</span><span class="sxs-lookup"><span data-stu-id="b1b12-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b1b12-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b1b12-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1b12-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1b12-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1b12-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1b12-159">System-Only</span></span>            | <span data-ttu-id="b1b12-160">False</span><span class="sxs-lookup"><span data-stu-id="b1b12-160">False</span></span>                                                |
| <span data-ttu-id="b1b12-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b1b12-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b1b12-162">True</span><span class="sxs-lookup"><span data-stu-id="b1b12-162">True</span></span>                                                 |
| <span data-ttu-id="b1b12-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b1b12-163">Is Indexed</span></span>             | <span data-ttu-id="b1b12-164">False</span><span class="sxs-lookup"><span data-stu-id="b1b12-164">False</span></span>                                                |
| <span data-ttu-id="b1b12-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b1b12-165">In Global Catalog</span></span>      | <span data-ttu-id="b1b12-166">False</span><span class="sxs-lookup"><span data-stu-id="b1b12-166">False</span></span>                                                |
| <span data-ttu-id="b1b12-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b1b12-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1b12-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1b12-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b1b12-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1b12-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b1b12-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1b12-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b1b12-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1b12-171">Search-Flags</span></span>           | <span data-ttu-id="b1b12-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1b12-172">0x00000000</span></span>                                           |
| <span data-ttu-id="b1b12-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1b12-173">System-Flags</span></span>           | <span data-ttu-id="b1b12-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1b12-174">0x00000010</span></span>                                           |
| <span data-ttu-id="b1b12-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b1b12-175">Classes used in</span></span>        | [<span data-ttu-id="b1b12-176">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="b1b12-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b1b12-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b1b12-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b1b12-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1b12-178">Entry</span></span> | <span data-ttu-id="b1b12-179">Value</span><span class="sxs-lookup"><span data-stu-id="b1b12-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b1b12-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b1b12-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1b12-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1b12-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1b12-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1b12-182">System-Only</span></span>            | <span data-ttu-id="b1b12-183">False</span><span class="sxs-lookup"><span data-stu-id="b1b12-183">False</span></span>                                                |
| <span data-ttu-id="b1b12-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b1b12-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b1b12-185">True</span><span class="sxs-lookup"><span data-stu-id="b1b12-185">True</span></span>                                                 |
| <span data-ttu-id="b1b12-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b1b12-186">Is Indexed</span></span>             | <span data-ttu-id="b1b12-187">False</span><span class="sxs-lookup"><span data-stu-id="b1b12-187">False</span></span>                                                |
| <span data-ttu-id="b1b12-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b1b12-188">In Global Catalog</span></span>      | <span data-ttu-id="b1b12-189">False</span><span class="sxs-lookup"><span data-stu-id="b1b12-189">False</span></span>                                                |
| <span data-ttu-id="b1b12-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b1b12-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1b12-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1b12-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b1b12-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1b12-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b1b12-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1b12-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b1b12-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1b12-194">Search-Flags</span></span>           | <span data-ttu-id="b1b12-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1b12-195">0x00000000</span></span>                                           |
| <span data-ttu-id="b1b12-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1b12-196">System-Flags</span></span>           | <span data-ttu-id="b1b12-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1b12-197">0x00000010</span></span>                                           |
| <span data-ttu-id="b1b12-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b1b12-198">Classes used in</span></span>        | [<span data-ttu-id="b1b12-199">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="b1b12-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b1b12-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1b12-200">Windows Server 2008</span></span>



| <span data-ttu-id="b1b12-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1b12-201">Entry</span></span> | <span data-ttu-id="b1b12-202">Value</span><span class="sxs-lookup"><span data-stu-id="b1b12-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b1b12-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b1b12-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1b12-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1b12-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1b12-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1b12-205">System-Only</span></span>            | <span data-ttu-id="b1b12-206">False</span><span class="sxs-lookup"><span data-stu-id="b1b12-206">False</span></span>                                                |
| <span data-ttu-id="b1b12-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b1b12-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b1b12-208">True</span><span class="sxs-lookup"><span data-stu-id="b1b12-208">True</span></span>                                                 |
| <span data-ttu-id="b1b12-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b1b12-209">Is Indexed</span></span>             | <span data-ttu-id="b1b12-210">False</span><span class="sxs-lookup"><span data-stu-id="b1b12-210">False</span></span>                                                |
| <span data-ttu-id="b1b12-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b1b12-211">In Global Catalog</span></span>      | <span data-ttu-id="b1b12-212">False</span><span class="sxs-lookup"><span data-stu-id="b1b12-212">False</span></span>                                                |
| <span data-ttu-id="b1b12-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b1b12-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1b12-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1b12-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b1b12-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1b12-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b1b12-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1b12-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b1b12-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1b12-217">Search-Flags</span></span>           | <span data-ttu-id="b1b12-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1b12-218">0x00000000</span></span>                                           |
| <span data-ttu-id="b1b12-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1b12-219">System-Flags</span></span>           | <span data-ttu-id="b1b12-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1b12-220">0x00000010</span></span>                                           |
| <span data-ttu-id="b1b12-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b1b12-221">Classes used in</span></span>        | [<span data-ttu-id="b1b12-222">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="b1b12-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b1b12-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b1b12-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b1b12-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1b12-224">Entry</span></span> | <span data-ttu-id="b1b12-225">Value</span><span class="sxs-lookup"><span data-stu-id="b1b12-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b1b12-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b1b12-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1b12-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1b12-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1b12-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1b12-228">System-Only</span></span>            | <span data-ttu-id="b1b12-229">False</span><span class="sxs-lookup"><span data-stu-id="b1b12-229">False</span></span>                                                |
| <span data-ttu-id="b1b12-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b1b12-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b1b12-231">True</span><span class="sxs-lookup"><span data-stu-id="b1b12-231">True</span></span>                                                 |
| <span data-ttu-id="b1b12-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b1b12-232">Is Indexed</span></span>             | <span data-ttu-id="b1b12-233">False</span><span class="sxs-lookup"><span data-stu-id="b1b12-233">False</span></span>                                                |
| <span data-ttu-id="b1b12-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b1b12-234">In Global Catalog</span></span>      | <span data-ttu-id="b1b12-235">False</span><span class="sxs-lookup"><span data-stu-id="b1b12-235">False</span></span>                                                |
| <span data-ttu-id="b1b12-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b1b12-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1b12-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1b12-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b1b12-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1b12-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b1b12-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1b12-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b1b12-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1b12-240">Search-Flags</span></span>           | <span data-ttu-id="b1b12-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1b12-241">0x00000000</span></span>                                           |
| <span data-ttu-id="b1b12-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1b12-242">System-Flags</span></span>           | <span data-ttu-id="b1b12-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1b12-243">0x00000010</span></span>                                           |
| <span data-ttu-id="b1b12-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b1b12-244">Classes used in</span></span>        | [<span data-ttu-id="b1b12-245">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="b1b12-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b1b12-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1b12-246">Windows Server 2012</span></span>



| <span data-ttu-id="b1b12-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1b12-247">Entry</span></span> | <span data-ttu-id="b1b12-248">Value</span><span class="sxs-lookup"><span data-stu-id="b1b12-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b1b12-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b1b12-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1b12-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1b12-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1b12-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1b12-251">System-Only</span></span>            | <span data-ttu-id="b1b12-252">False</span><span class="sxs-lookup"><span data-stu-id="b1b12-252">False</span></span>                                                |
| <span data-ttu-id="b1b12-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b1b12-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b1b12-254">True</span><span class="sxs-lookup"><span data-stu-id="b1b12-254">True</span></span>                                                 |
| <span data-ttu-id="b1b12-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b1b12-255">Is Indexed</span></span>             | <span data-ttu-id="b1b12-256">False</span><span class="sxs-lookup"><span data-stu-id="b1b12-256">False</span></span>                                                |
| <span data-ttu-id="b1b12-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b1b12-257">In Global Catalog</span></span>      | <span data-ttu-id="b1b12-258">False</span><span class="sxs-lookup"><span data-stu-id="b1b12-258">False</span></span>                                                |
| <span data-ttu-id="b1b12-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b1b12-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1b12-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1b12-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b1b12-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1b12-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b1b12-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1b12-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b1b12-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1b12-263">Search-Flags</span></span>           | <span data-ttu-id="b1b12-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1b12-264">0x00000000</span></span>                                           |
| <span data-ttu-id="b1b12-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1b12-265">System-Flags</span></span>           | <span data-ttu-id="b1b12-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1b12-266">0x00000010</span></span>                                           |
| <span data-ttu-id="b1b12-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b1b12-267">Classes used in</span></span>        | [<span data-ttu-id="b1b12-268">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="b1b12-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





