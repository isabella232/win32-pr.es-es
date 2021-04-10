---
title: Atributo Initial-auth-
description: Contiene información sobre una autenticación de salida inicial enviada por el servidor de autenticación para este dominio al cliente que solicitó la autenticación.
ms.assetid: cc5ceb14-0424-4caa-bcd9-1e48988af67a
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de salida de autenticación inicial
- initialAuthOutgoing esquema de AD de atributos
topic_type:
- apiref
api_name:
- Initial-Auth-Outgoing
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84faaa443c9589e04f4998dc41d72fe870b5f2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151407"
---
# <a name="initial-auth-outgoing-attribute"></a><span data-ttu-id="ee64c-105">Atributo Initial-auth-</span><span class="sxs-lookup"><span data-stu-id="ee64c-105">Initial-Auth-Outgoing attribute</span></span>

<span data-ttu-id="ee64c-106">Contiene información sobre una autenticación de salida inicial enviada por el servidor de autenticación para este dominio al cliente que solicitó la autenticación.</span><span class="sxs-lookup"><span data-stu-id="ee64c-106">Contains information about an initial outgoing authentication sent by the authentication server for this domain to the client that requested authentication.</span></span> <span data-ttu-id="ee64c-107">El servidor que usa este atributo recibe la autorización del servidor de autenticación y la envía al cliente.</span><span class="sxs-lookup"><span data-stu-id="ee64c-107">The server that uses this attribute receives the authorization from the authentication server and sends it to the client.</span></span>



| <span data-ttu-id="ee64c-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee64c-108">Entry</span></span> | <span data-ttu-id="ee64c-109">Value</span><span class="sxs-lookup"><span data-stu-id="ee64c-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ee64c-110">CN</span><span class="sxs-lookup"><span data-stu-id="ee64c-110">CN</span></span>                | <span data-ttu-id="ee64c-111">Autenticación inicial-saliente</span><span class="sxs-lookup"><span data-stu-id="ee64c-111">Initial-Auth-Outgoing</span></span>                       |
| <span data-ttu-id="ee64c-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="ee64c-112">Ldap-Display-Name</span></span> | <span data-ttu-id="ee64c-113">initialAuthOutgoing</span><span class="sxs-lookup"><span data-stu-id="ee64c-113">initialAuthOutgoing</span></span>                         |
| <span data-ttu-id="ee64c-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="ee64c-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="ee64c-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="ee64c-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="ee64c-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="ee64c-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="ee64c-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ee64c-117">Attribute-Id</span></span>      | <span data-ttu-id="ee64c-118">1.2.840.113556.1.4.540</span><span class="sxs-lookup"><span data-stu-id="ee64c-118">1.2.840.113556.1.4.540</span></span>                      |
| <span data-ttu-id="ee64c-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ee64c-119">System-Id-Guid</span></span>    | <span data-ttu-id="ee64c-120">52458024-ca6a-11d0-AFFF-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ee64c-120">52458024-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="ee64c-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee64c-121">Syntax</span></span>            | [<span data-ttu-id="ee64c-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ee64c-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ee64c-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="ee64c-123">Implementations</span></span>

-   [<span data-ttu-id="ee64c-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ee64c-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ee64c-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ee64c-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ee64c-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ee64c-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ee64c-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ee64c-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ee64c-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ee64c-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ee64c-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ee64c-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ee64c-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ee64c-130">Windows 2000 Server</span></span>



| <span data-ttu-id="ee64c-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee64c-131">Entry</span></span> | <span data-ttu-id="ee64c-132">Value</span><span class="sxs-lookup"><span data-stu-id="ee64c-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ee64c-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ee64c-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ee64c-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee64c-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ee64c-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee64c-135">System-Only</span></span>            | <span data-ttu-id="ee64c-136">False</span><span class="sxs-lookup"><span data-stu-id="ee64c-136">False</span></span>                                                |
| <span data-ttu-id="ee64c-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ee64c-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ee64c-138">True</span><span class="sxs-lookup"><span data-stu-id="ee64c-138">True</span></span>                                                 |
| <span data-ttu-id="ee64c-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ee64c-139">Is Indexed</span></span>             | <span data-ttu-id="ee64c-140">False</span><span class="sxs-lookup"><span data-stu-id="ee64c-140">False</span></span>                                                |
| <span data-ttu-id="ee64c-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee64c-141">In Global Catalog</span></span>      | <span data-ttu-id="ee64c-142">False</span><span class="sxs-lookup"><span data-stu-id="ee64c-142">False</span></span>                                                |
| <span data-ttu-id="ee64c-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ee64c-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee64c-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ee64c-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ee64c-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee64c-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ee64c-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee64c-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ee64c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee64c-147">Search-Flags</span></span>           | <span data-ttu-id="ee64c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee64c-148">0x00000000</span></span>                                           |
| <span data-ttu-id="ee64c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee64c-149">System-Flags</span></span>           | <span data-ttu-id="ee64c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee64c-150">0x00000010</span></span>                                           |
| <span data-ttu-id="ee64c-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ee64c-151">Classes used in</span></span>        | [<span data-ttu-id="ee64c-152">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="ee64c-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ee64c-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ee64c-153">Windows Server 2003</span></span>



| <span data-ttu-id="ee64c-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee64c-154">Entry</span></span> | <span data-ttu-id="ee64c-155">Value</span><span class="sxs-lookup"><span data-stu-id="ee64c-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ee64c-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ee64c-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ee64c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee64c-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ee64c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee64c-158">System-Only</span></span>            | <span data-ttu-id="ee64c-159">False</span><span class="sxs-lookup"><span data-stu-id="ee64c-159">False</span></span>                                                |
| <span data-ttu-id="ee64c-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ee64c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="ee64c-161">True</span><span class="sxs-lookup"><span data-stu-id="ee64c-161">True</span></span>                                                 |
| <span data-ttu-id="ee64c-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ee64c-162">Is Indexed</span></span>             | <span data-ttu-id="ee64c-163">False</span><span class="sxs-lookup"><span data-stu-id="ee64c-163">False</span></span>                                                |
| <span data-ttu-id="ee64c-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee64c-164">In Global Catalog</span></span>      | <span data-ttu-id="ee64c-165">False</span><span class="sxs-lookup"><span data-stu-id="ee64c-165">False</span></span>                                                |
| <span data-ttu-id="ee64c-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ee64c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee64c-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ee64c-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ee64c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee64c-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ee64c-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee64c-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ee64c-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee64c-170">Search-Flags</span></span>           | <span data-ttu-id="ee64c-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee64c-171">0x00000000</span></span>                                           |
| <span data-ttu-id="ee64c-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee64c-172">System-Flags</span></span>           | <span data-ttu-id="ee64c-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee64c-173">0x00000010</span></span>                                           |
| <span data-ttu-id="ee64c-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ee64c-174">Classes used in</span></span>        | [<span data-ttu-id="ee64c-175">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="ee64c-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ee64c-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ee64c-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ee64c-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee64c-177">Entry</span></span> | <span data-ttu-id="ee64c-178">Value</span><span class="sxs-lookup"><span data-stu-id="ee64c-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ee64c-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ee64c-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ee64c-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee64c-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ee64c-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee64c-181">System-Only</span></span>            | <span data-ttu-id="ee64c-182">False</span><span class="sxs-lookup"><span data-stu-id="ee64c-182">False</span></span>                                                |
| <span data-ttu-id="ee64c-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ee64c-183">Is-Single-Valued</span></span>       | <span data-ttu-id="ee64c-184">True</span><span class="sxs-lookup"><span data-stu-id="ee64c-184">True</span></span>                                                 |
| <span data-ttu-id="ee64c-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ee64c-185">Is Indexed</span></span>             | <span data-ttu-id="ee64c-186">False</span><span class="sxs-lookup"><span data-stu-id="ee64c-186">False</span></span>                                                |
| <span data-ttu-id="ee64c-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee64c-187">In Global Catalog</span></span>      | <span data-ttu-id="ee64c-188">False</span><span class="sxs-lookup"><span data-stu-id="ee64c-188">False</span></span>                                                |
| <span data-ttu-id="ee64c-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ee64c-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee64c-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ee64c-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ee64c-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee64c-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ee64c-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee64c-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ee64c-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee64c-193">Search-Flags</span></span>           | <span data-ttu-id="ee64c-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee64c-194">0x00000000</span></span>                                           |
| <span data-ttu-id="ee64c-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee64c-195">System-Flags</span></span>           | <span data-ttu-id="ee64c-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee64c-196">0x00000010</span></span>                                           |
| <span data-ttu-id="ee64c-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ee64c-197">Classes used in</span></span>        | [<span data-ttu-id="ee64c-198">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="ee64c-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ee64c-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee64c-199">Windows Server 2008</span></span>



| <span data-ttu-id="ee64c-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee64c-200">Entry</span></span> | <span data-ttu-id="ee64c-201">Value</span><span class="sxs-lookup"><span data-stu-id="ee64c-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ee64c-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ee64c-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ee64c-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee64c-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ee64c-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee64c-204">System-Only</span></span>            | <span data-ttu-id="ee64c-205">False</span><span class="sxs-lookup"><span data-stu-id="ee64c-205">False</span></span>                                                |
| <span data-ttu-id="ee64c-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ee64c-206">Is-Single-Valued</span></span>       | <span data-ttu-id="ee64c-207">True</span><span class="sxs-lookup"><span data-stu-id="ee64c-207">True</span></span>                                                 |
| <span data-ttu-id="ee64c-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ee64c-208">Is Indexed</span></span>             | <span data-ttu-id="ee64c-209">False</span><span class="sxs-lookup"><span data-stu-id="ee64c-209">False</span></span>                                                |
| <span data-ttu-id="ee64c-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee64c-210">In Global Catalog</span></span>      | <span data-ttu-id="ee64c-211">False</span><span class="sxs-lookup"><span data-stu-id="ee64c-211">False</span></span>                                                |
| <span data-ttu-id="ee64c-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ee64c-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee64c-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ee64c-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ee64c-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee64c-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ee64c-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee64c-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ee64c-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee64c-216">Search-Flags</span></span>           | <span data-ttu-id="ee64c-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee64c-217">0x00000000</span></span>                                           |
| <span data-ttu-id="ee64c-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee64c-218">System-Flags</span></span>           | <span data-ttu-id="ee64c-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee64c-219">0x00000010</span></span>                                           |
| <span data-ttu-id="ee64c-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ee64c-220">Classes used in</span></span>        | [<span data-ttu-id="ee64c-221">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="ee64c-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ee64c-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ee64c-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ee64c-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee64c-223">Entry</span></span> | <span data-ttu-id="ee64c-224">Value</span><span class="sxs-lookup"><span data-stu-id="ee64c-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ee64c-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ee64c-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ee64c-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee64c-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ee64c-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee64c-227">System-Only</span></span>            | <span data-ttu-id="ee64c-228">False</span><span class="sxs-lookup"><span data-stu-id="ee64c-228">False</span></span>                                                |
| <span data-ttu-id="ee64c-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ee64c-229">Is-Single-Valued</span></span>       | <span data-ttu-id="ee64c-230">True</span><span class="sxs-lookup"><span data-stu-id="ee64c-230">True</span></span>                                                 |
| <span data-ttu-id="ee64c-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ee64c-231">Is Indexed</span></span>             | <span data-ttu-id="ee64c-232">False</span><span class="sxs-lookup"><span data-stu-id="ee64c-232">False</span></span>                                                |
| <span data-ttu-id="ee64c-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee64c-233">In Global Catalog</span></span>      | <span data-ttu-id="ee64c-234">False</span><span class="sxs-lookup"><span data-stu-id="ee64c-234">False</span></span>                                                |
| <span data-ttu-id="ee64c-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ee64c-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee64c-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ee64c-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ee64c-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee64c-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ee64c-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee64c-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ee64c-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee64c-239">Search-Flags</span></span>           | <span data-ttu-id="ee64c-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee64c-240">0x00000000</span></span>                                           |
| <span data-ttu-id="ee64c-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee64c-241">System-Flags</span></span>           | <span data-ttu-id="ee64c-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee64c-242">0x00000010</span></span>                                           |
| <span data-ttu-id="ee64c-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ee64c-243">Classes used in</span></span>        | [<span data-ttu-id="ee64c-244">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="ee64c-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ee64c-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ee64c-245">Windows Server 2012</span></span>



| <span data-ttu-id="ee64c-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee64c-246">Entry</span></span> | <span data-ttu-id="ee64c-247">Value</span><span class="sxs-lookup"><span data-stu-id="ee64c-247">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ee64c-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ee64c-248">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ee64c-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee64c-249">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ee64c-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee64c-250">System-Only</span></span>            | <span data-ttu-id="ee64c-251">False</span><span class="sxs-lookup"><span data-stu-id="ee64c-251">False</span></span>                                                |
| <span data-ttu-id="ee64c-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ee64c-252">Is-Single-Valued</span></span>       | <span data-ttu-id="ee64c-253">True</span><span class="sxs-lookup"><span data-stu-id="ee64c-253">True</span></span>                                                 |
| <span data-ttu-id="ee64c-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ee64c-254">Is Indexed</span></span>             | <span data-ttu-id="ee64c-255">False</span><span class="sxs-lookup"><span data-stu-id="ee64c-255">False</span></span>                                                |
| <span data-ttu-id="ee64c-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee64c-256">In Global Catalog</span></span>      | <span data-ttu-id="ee64c-257">False</span><span class="sxs-lookup"><span data-stu-id="ee64c-257">False</span></span>                                                |
| <span data-ttu-id="ee64c-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ee64c-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee64c-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ee64c-259">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ee64c-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee64c-260">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ee64c-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee64c-261">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ee64c-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee64c-262">Search-Flags</span></span>           | <span data-ttu-id="ee64c-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee64c-263">0x00000000</span></span>                                           |
| <span data-ttu-id="ee64c-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee64c-264">System-Flags</span></span>           | <span data-ttu-id="ee64c-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee64c-265">0x00000010</span></span>                                           |
| <span data-ttu-id="ee64c-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ee64c-266">Classes used in</span></span>        | [<span data-ttu-id="ee64c-267">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="ee64c-267">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





