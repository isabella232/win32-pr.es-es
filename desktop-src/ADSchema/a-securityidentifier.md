---
title: Security-Identifier atributo)
description: Un valor único de longitud variable que se usa para identificar una cuenta de usuario, una cuenta de grupo o una sesión de inicio de sesión a la que se aplica una ACE.
ms.assetid: bb6a16f6-d2c1-48f1-af9a-40fe2a59f281
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Security-Identifier
- atributo securityIdentifier esquema de AD
topic_type:
- apiref
api_name:
- Security-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd921d0bcba08c2174475007476add8e8787456
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804549"
---
# <a name="security-identifier-attribute"></a><span data-ttu-id="134bf-105">Security-Identifier atributo)</span><span class="sxs-lookup"><span data-stu-id="134bf-105">Security-Identifier attribute</span></span>

<span data-ttu-id="134bf-106">Un valor único de longitud variable que se usa para identificar una cuenta de usuario, una cuenta de grupo o una sesión de inicio de sesión a la que se aplica una ACE.</span><span class="sxs-lookup"><span data-stu-id="134bf-106">A unique value of variable length used to identify a user account, group account, or logon session to which an ACE applies.</span></span>



| <span data-ttu-id="134bf-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="134bf-107">Entry</span></span> | <span data-ttu-id="134bf-108">Value</span><span class="sxs-lookup"><span data-stu-id="134bf-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="134bf-109">CN</span><span class="sxs-lookup"><span data-stu-id="134bf-109">CN</span></span>                | <span data-ttu-id="134bf-110">Security-Identifier</span><span class="sxs-lookup"><span data-stu-id="134bf-110">Security-Identifier</span></span>                  |
| <span data-ttu-id="134bf-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="134bf-111">Ldap-Display-Name</span></span> | <span data-ttu-id="134bf-112">securityIdentifier</span><span class="sxs-lookup"><span data-stu-id="134bf-112">securityIdentifier</span></span>                   |
| <span data-ttu-id="134bf-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="134bf-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="134bf-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="134bf-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="134bf-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="134bf-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="134bf-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="134bf-116">Attribute-Id</span></span>      | <span data-ttu-id="134bf-117">1.2.840.113556.1.4.121</span><span class="sxs-lookup"><span data-stu-id="134bf-117">1.2.840.113556.1.4.121</span></span>               |
| <span data-ttu-id="134bf-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="134bf-118">System-Id-Guid</span></span>    | <span data-ttu-id="134bf-119">bf967a2f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="134bf-119">bf967a2f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="134bf-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="134bf-120">Syntax</span></span>            | [<span data-ttu-id="134bf-121">**Cadena (SID)**</span><span class="sxs-lookup"><span data-stu-id="134bf-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="134bf-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="134bf-122">Implementations</span></span>

-   [<span data-ttu-id="134bf-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="134bf-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="134bf-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="134bf-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="134bf-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="134bf-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="134bf-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="134bf-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="134bf-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="134bf-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="134bf-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="134bf-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="134bf-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="134bf-129">Windows 2000 Server</span></span>



| <span data-ttu-id="134bf-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="134bf-130">Entry</span></span> | <span data-ttu-id="134bf-131">Value</span><span class="sxs-lookup"><span data-stu-id="134bf-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="134bf-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="134bf-132">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="134bf-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="134bf-133">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="134bf-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="134bf-134">System-Only</span></span>            | <span data-ttu-id="134bf-135">False</span><span class="sxs-lookup"><span data-stu-id="134bf-135">False</span></span>                                                                                                             |
| <span data-ttu-id="134bf-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="134bf-136">Is-Single-Valued</span></span>       | <span data-ttu-id="134bf-137">True</span><span class="sxs-lookup"><span data-stu-id="134bf-137">True</span></span>                                                                                                              |
| <span data-ttu-id="134bf-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="134bf-138">Is Indexed</span></span>             | <span data-ttu-id="134bf-139">False</span><span class="sxs-lookup"><span data-stu-id="134bf-139">False</span></span>                                                                                                             |
| <span data-ttu-id="134bf-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="134bf-140">In Global Catalog</span></span>      | <span data-ttu-id="134bf-141">False</span><span class="sxs-lookup"><span data-stu-id="134bf-141">False</span></span>                                                                                                             |
| <span data-ttu-id="134bf-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="134bf-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="134bf-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="134bf-143">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="134bf-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="134bf-144">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="134bf-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="134bf-145">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="134bf-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="134bf-146">Search-Flags</span></span>           | <span data-ttu-id="134bf-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="134bf-147">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="134bf-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="134bf-148">System-Flags</span></span>           | <span data-ttu-id="134bf-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="134bf-149">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="134bf-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="134bf-150">Classes used in</span></span>        | [<span data-ttu-id="134bf-151">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="134bf-151">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="134bf-152">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="134bf-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="134bf-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="134bf-153">Windows Server 2003</span></span>



| <span data-ttu-id="134bf-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="134bf-154">Entry</span></span> | <span data-ttu-id="134bf-155">Value</span><span class="sxs-lookup"><span data-stu-id="134bf-155">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="134bf-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="134bf-156">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="134bf-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="134bf-157">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="134bf-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="134bf-158">System-Only</span></span>            | <span data-ttu-id="134bf-159">False</span><span class="sxs-lookup"><span data-stu-id="134bf-159">False</span></span>                                                                                                             |
| <span data-ttu-id="134bf-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="134bf-160">Is-Single-Valued</span></span>       | <span data-ttu-id="134bf-161">True</span><span class="sxs-lookup"><span data-stu-id="134bf-161">True</span></span>                                                                                                              |
| <span data-ttu-id="134bf-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="134bf-162">Is Indexed</span></span>             | <span data-ttu-id="134bf-163">False</span><span class="sxs-lookup"><span data-stu-id="134bf-163">False</span></span>                                                                                                             |
| <span data-ttu-id="134bf-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="134bf-164">In Global Catalog</span></span>      | <span data-ttu-id="134bf-165">True</span><span class="sxs-lookup"><span data-stu-id="134bf-165">True</span></span>                                                                                                              |
| <span data-ttu-id="134bf-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="134bf-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="134bf-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="134bf-167">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="134bf-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="134bf-168">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="134bf-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="134bf-169">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="134bf-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="134bf-170">Search-Flags</span></span>           | <span data-ttu-id="134bf-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="134bf-171">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="134bf-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="134bf-172">System-Flags</span></span>           | <span data-ttu-id="134bf-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="134bf-173">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="134bf-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="134bf-174">Classes used in</span></span>        | [<span data-ttu-id="134bf-175">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="134bf-175">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="134bf-176">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="134bf-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="134bf-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="134bf-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="134bf-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="134bf-178">Entry</span></span> | <span data-ttu-id="134bf-179">Value</span><span class="sxs-lookup"><span data-stu-id="134bf-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="134bf-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="134bf-180">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="134bf-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="134bf-181">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="134bf-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="134bf-182">System-Only</span></span>            | <span data-ttu-id="134bf-183">False</span><span class="sxs-lookup"><span data-stu-id="134bf-183">False</span></span>                                                                                                             |
| <span data-ttu-id="134bf-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="134bf-184">Is-Single-Valued</span></span>       | <span data-ttu-id="134bf-185">True</span><span class="sxs-lookup"><span data-stu-id="134bf-185">True</span></span>                                                                                                              |
| <span data-ttu-id="134bf-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="134bf-186">Is Indexed</span></span>             | <span data-ttu-id="134bf-187">False</span><span class="sxs-lookup"><span data-stu-id="134bf-187">False</span></span>                                                                                                             |
| <span data-ttu-id="134bf-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="134bf-188">In Global Catalog</span></span>      | <span data-ttu-id="134bf-189">True</span><span class="sxs-lookup"><span data-stu-id="134bf-189">True</span></span>                                                                                                              |
| <span data-ttu-id="134bf-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="134bf-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="134bf-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="134bf-191">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="134bf-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="134bf-192">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="134bf-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="134bf-193">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="134bf-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="134bf-194">Search-Flags</span></span>           | <span data-ttu-id="134bf-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="134bf-195">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="134bf-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="134bf-196">System-Flags</span></span>           | <span data-ttu-id="134bf-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="134bf-197">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="134bf-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="134bf-198">Classes used in</span></span>        | [<span data-ttu-id="134bf-199">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="134bf-199">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="134bf-200">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="134bf-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="134bf-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="134bf-201">Windows Server 2008</span></span>



| <span data-ttu-id="134bf-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="134bf-202">Entry</span></span> | <span data-ttu-id="134bf-203">Value</span><span class="sxs-lookup"><span data-stu-id="134bf-203">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="134bf-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="134bf-204">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="134bf-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="134bf-205">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="134bf-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="134bf-206">System-Only</span></span>            | <span data-ttu-id="134bf-207">False</span><span class="sxs-lookup"><span data-stu-id="134bf-207">False</span></span>                                                                                                             |
| <span data-ttu-id="134bf-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="134bf-208">Is-Single-Valued</span></span>       | <span data-ttu-id="134bf-209">True</span><span class="sxs-lookup"><span data-stu-id="134bf-209">True</span></span>                                                                                                              |
| <span data-ttu-id="134bf-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="134bf-210">Is Indexed</span></span>             | <span data-ttu-id="134bf-211">False</span><span class="sxs-lookup"><span data-stu-id="134bf-211">False</span></span>                                                                                                             |
| <span data-ttu-id="134bf-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="134bf-212">In Global Catalog</span></span>      | <span data-ttu-id="134bf-213">True</span><span class="sxs-lookup"><span data-stu-id="134bf-213">True</span></span>                                                                                                              |
| <span data-ttu-id="134bf-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="134bf-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="134bf-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="134bf-215">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="134bf-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="134bf-216">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="134bf-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="134bf-217">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="134bf-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="134bf-218">Search-Flags</span></span>           | <span data-ttu-id="134bf-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="134bf-219">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="134bf-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="134bf-220">System-Flags</span></span>           | <span data-ttu-id="134bf-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="134bf-221">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="134bf-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="134bf-222">Classes used in</span></span>        | [<span data-ttu-id="134bf-223">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="134bf-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="134bf-224">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="134bf-224">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="134bf-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="134bf-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="134bf-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="134bf-226">Entry</span></span> | <span data-ttu-id="134bf-227">Value</span><span class="sxs-lookup"><span data-stu-id="134bf-227">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="134bf-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="134bf-228">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="134bf-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="134bf-229">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="134bf-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="134bf-230">System-Only</span></span>            | <span data-ttu-id="134bf-231">False</span><span class="sxs-lookup"><span data-stu-id="134bf-231">False</span></span>                                                                                                             |
| <span data-ttu-id="134bf-232">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="134bf-232">Is-Single-Valued</span></span>       | <span data-ttu-id="134bf-233">True</span><span class="sxs-lookup"><span data-stu-id="134bf-233">True</span></span>                                                                                                              |
| <span data-ttu-id="134bf-234">Está indexado</span><span class="sxs-lookup"><span data-stu-id="134bf-234">Is Indexed</span></span>             | <span data-ttu-id="134bf-235">False</span><span class="sxs-lookup"><span data-stu-id="134bf-235">False</span></span>                                                                                                             |
| <span data-ttu-id="134bf-236">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="134bf-236">In Global Catalog</span></span>      | <span data-ttu-id="134bf-237">True</span><span class="sxs-lookup"><span data-stu-id="134bf-237">True</span></span>                                                                                                              |
| <span data-ttu-id="134bf-238">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="134bf-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="134bf-239">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="134bf-239">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="134bf-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="134bf-240">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="134bf-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="134bf-241">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="134bf-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="134bf-242">Search-Flags</span></span>           | <span data-ttu-id="134bf-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="134bf-243">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="134bf-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="134bf-244">System-Flags</span></span>           | <span data-ttu-id="134bf-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="134bf-245">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="134bf-246">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="134bf-246">Classes used in</span></span>        | [<span data-ttu-id="134bf-247">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="134bf-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="134bf-248">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="134bf-248">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="134bf-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="134bf-249">Windows Server 2012</span></span>



| <span data-ttu-id="134bf-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="134bf-250">Entry</span></span> | <span data-ttu-id="134bf-251">Value</span><span class="sxs-lookup"><span data-stu-id="134bf-251">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="134bf-252">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="134bf-252">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="134bf-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="134bf-253">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="134bf-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="134bf-254">System-Only</span></span>            | <span data-ttu-id="134bf-255">False</span><span class="sxs-lookup"><span data-stu-id="134bf-255">False</span></span>                                                                                                             |
| <span data-ttu-id="134bf-256">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="134bf-256">Is-Single-Valued</span></span>       | <span data-ttu-id="134bf-257">True</span><span class="sxs-lookup"><span data-stu-id="134bf-257">True</span></span>                                                                                                              |
| <span data-ttu-id="134bf-258">Está indexado</span><span class="sxs-lookup"><span data-stu-id="134bf-258">Is Indexed</span></span>             | <span data-ttu-id="134bf-259">False</span><span class="sxs-lookup"><span data-stu-id="134bf-259">False</span></span>                                                                                                             |
| <span data-ttu-id="134bf-260">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="134bf-260">In Global Catalog</span></span>      | <span data-ttu-id="134bf-261">True</span><span class="sxs-lookup"><span data-stu-id="134bf-261">True</span></span>                                                                                                              |
| <span data-ttu-id="134bf-262">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="134bf-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="134bf-263">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="134bf-263">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="134bf-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="134bf-264">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="134bf-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="134bf-265">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="134bf-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="134bf-266">Search-Flags</span></span>           | <span data-ttu-id="134bf-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="134bf-267">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="134bf-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="134bf-268">System-Flags</span></span>           | <span data-ttu-id="134bf-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="134bf-269">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="134bf-270">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="134bf-270">Classes used in</span></span>        | [<span data-ttu-id="134bf-271">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="134bf-271">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="134bf-272">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="134bf-272">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





