---
title: Atributo ALT-Security-Identities
description: Contiene las asignaciones de certificados X. 509 o cuentas de usuario de Kerberos externas a este usuario con el fin de la autenticación.
ms.assetid: 40b2af9c-fd4f-4883-8494-2b64682ee50c
ms.tgt_platform: multiple
keywords:
- Alt-Security-Identidads atributo AD Schema
- altSecurityIdentities esquema de AD de atributos
topic_type:
- apiref
api_name:
- Alt-Security-Identities
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2548e337f29778400bb173a8c15d928d7b06d988
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997316"
---
# <a name="alt-security-identities-attribute"></a><span data-ttu-id="aecbd-105">Atributo ALT-Security-Identities</span><span class="sxs-lookup"><span data-stu-id="aecbd-105">Alt-Security-Identities attribute</span></span>

<span data-ttu-id="aecbd-106">Contiene las asignaciones de certificados X. 509 o cuentas de usuario de Kerberos externas a este usuario con el fin de la autenticación.</span><span class="sxs-lookup"><span data-stu-id="aecbd-106">Contains mappings for X.509 certificates or external Kerberos user accounts to this user for the purpose of authentication.</span></span>



| <span data-ttu-id="aecbd-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="aecbd-107">Entry</span></span> | <span data-ttu-id="aecbd-108">Value</span><span class="sxs-lookup"><span data-stu-id="aecbd-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="aecbd-109">CN</span><span class="sxs-lookup"><span data-stu-id="aecbd-109">CN</span></span>                | <span data-ttu-id="aecbd-110">Alt-seguridad-identidades</span><span class="sxs-lookup"><span data-stu-id="aecbd-110">Alt-Security-Identities</span></span>                             |
| <span data-ttu-id="aecbd-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="aecbd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="aecbd-112">altSecurityIdentities</span><span class="sxs-lookup"><span data-stu-id="aecbd-112">altSecurityIdentities</span></span>                               |
| <span data-ttu-id="aecbd-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="aecbd-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="aecbd-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="aecbd-114">Update Privilege</span></span>  | <span data-ttu-id="aecbd-115">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="aecbd-115">Domain administrator</span></span>                                |
| <span data-ttu-id="aecbd-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="aecbd-116">Update Frequency</span></span>  | <span data-ttu-id="aecbd-117">Cada vez que se necesita un nuevo mecanismo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="aecbd-117">Each time a new authentication mechanism is needed.</span></span> |
| <span data-ttu-id="aecbd-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="aecbd-118">Attribute-Id</span></span>      | <span data-ttu-id="aecbd-119">1.2.840.113556.1.4.867</span><span class="sxs-lookup"><span data-stu-id="aecbd-119">1.2.840.113556.1.4.867</span></span>                              |
| <span data-ttu-id="aecbd-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="aecbd-120">System-Id-Guid</span></span>    | <span data-ttu-id="aecbd-121">00fbf30c-91fe-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="aecbd-121">00fbf30c-91fe-11d1-aebc-0000f80367c1</span></span>                |
| <span data-ttu-id="aecbd-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aecbd-122">Syntax</span></span>            | [<span data-ttu-id="aecbd-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="aecbd-123">**String(Unicode)**</span></span>](s-string-unicode.md)         |



## <a name="implementations"></a><span data-ttu-id="aecbd-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="aecbd-124">Implementations</span></span>

-   [<span data-ttu-id="aecbd-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="aecbd-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="aecbd-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="aecbd-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="aecbd-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="aecbd-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="aecbd-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="aecbd-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="aecbd-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="aecbd-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="aecbd-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="aecbd-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="aecbd-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aecbd-131">Windows 2000 Server</span></span>



| <span data-ttu-id="aecbd-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="aecbd-132">Entry</span></span> | <span data-ttu-id="aecbd-133">Value</span><span class="sxs-lookup"><span data-stu-id="aecbd-133">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="aecbd-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="aecbd-134">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="aecbd-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aecbd-135">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="aecbd-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="aecbd-136">System-Only</span></span>            | <span data-ttu-id="aecbd-137">False</span><span class="sxs-lookup"><span data-stu-id="aecbd-137">False</span></span>                                                        |
| <span data-ttu-id="aecbd-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="aecbd-138">Is-Single-Valued</span></span>       | <span data-ttu-id="aecbd-139">False</span><span class="sxs-lookup"><span data-stu-id="aecbd-139">False</span></span>                                                        |
| <span data-ttu-id="aecbd-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="aecbd-140">Is Indexed</span></span>             | <span data-ttu-id="aecbd-141">True</span><span class="sxs-lookup"><span data-stu-id="aecbd-141">True</span></span>                                                         |
| <span data-ttu-id="aecbd-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="aecbd-142">In Global Catalog</span></span>      | <span data-ttu-id="aecbd-143">True</span><span class="sxs-lookup"><span data-stu-id="aecbd-143">True</span></span>                                                         |
| <span data-ttu-id="aecbd-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="aecbd-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="aecbd-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aecbd-145">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="aecbd-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aecbd-146">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="aecbd-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aecbd-147">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="aecbd-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aecbd-148">Search-Flags</span></span>           | <span data-ttu-id="aecbd-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="aecbd-149">0x00000001</span></span>                                                   |
| <span data-ttu-id="aecbd-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aecbd-150">System-Flags</span></span>           | <span data-ttu-id="aecbd-151">0x00000012</span><span class="sxs-lookup"><span data-stu-id="aecbd-151">0x00000012</span></span>                                                   |
| <span data-ttu-id="aecbd-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="aecbd-152">Classes used in</span></span>        | [<span data-ttu-id="aecbd-153">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="aecbd-153">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="aecbd-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aecbd-154">Windows Server 2003</span></span>



| <span data-ttu-id="aecbd-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="aecbd-155">Entry</span></span> | <span data-ttu-id="aecbd-156">Value</span><span class="sxs-lookup"><span data-stu-id="aecbd-156">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="aecbd-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="aecbd-157">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="aecbd-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aecbd-158">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="aecbd-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="aecbd-159">System-Only</span></span>            | <span data-ttu-id="aecbd-160">False</span><span class="sxs-lookup"><span data-stu-id="aecbd-160">False</span></span>                                                        |
| <span data-ttu-id="aecbd-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="aecbd-161">Is-Single-Valued</span></span>       | <span data-ttu-id="aecbd-162">False</span><span class="sxs-lookup"><span data-stu-id="aecbd-162">False</span></span>                                                        |
| <span data-ttu-id="aecbd-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="aecbd-163">Is Indexed</span></span>             | <span data-ttu-id="aecbd-164">True</span><span class="sxs-lookup"><span data-stu-id="aecbd-164">True</span></span>                                                         |
| <span data-ttu-id="aecbd-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="aecbd-165">In Global Catalog</span></span>      | <span data-ttu-id="aecbd-166">True</span><span class="sxs-lookup"><span data-stu-id="aecbd-166">True</span></span>                                                         |
| <span data-ttu-id="aecbd-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="aecbd-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="aecbd-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aecbd-168">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="aecbd-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aecbd-169">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="aecbd-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aecbd-170">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="aecbd-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aecbd-171">Search-Flags</span></span>           | <span data-ttu-id="aecbd-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="aecbd-172">0x00000001</span></span>                                                   |
| <span data-ttu-id="aecbd-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aecbd-173">System-Flags</span></span>           | <span data-ttu-id="aecbd-174">0x00000012</span><span class="sxs-lookup"><span data-stu-id="aecbd-174">0x00000012</span></span>                                                   |
| <span data-ttu-id="aecbd-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="aecbd-175">Classes used in</span></span>        | [<span data-ttu-id="aecbd-176">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="aecbd-176">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="aecbd-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="aecbd-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="aecbd-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="aecbd-178">Entry</span></span> | <span data-ttu-id="aecbd-179">Value</span><span class="sxs-lookup"><span data-stu-id="aecbd-179">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="aecbd-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="aecbd-180">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="aecbd-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aecbd-181">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="aecbd-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="aecbd-182">System-Only</span></span>            | <span data-ttu-id="aecbd-183">False</span><span class="sxs-lookup"><span data-stu-id="aecbd-183">False</span></span>                                                        |
| <span data-ttu-id="aecbd-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="aecbd-184">Is-Single-Valued</span></span>       | <span data-ttu-id="aecbd-185">False</span><span class="sxs-lookup"><span data-stu-id="aecbd-185">False</span></span>                                                        |
| <span data-ttu-id="aecbd-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="aecbd-186">Is Indexed</span></span>             | <span data-ttu-id="aecbd-187">True</span><span class="sxs-lookup"><span data-stu-id="aecbd-187">True</span></span>                                                         |
| <span data-ttu-id="aecbd-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="aecbd-188">In Global Catalog</span></span>      | <span data-ttu-id="aecbd-189">True</span><span class="sxs-lookup"><span data-stu-id="aecbd-189">True</span></span>                                                         |
| <span data-ttu-id="aecbd-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="aecbd-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="aecbd-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aecbd-191">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="aecbd-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aecbd-192">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="aecbd-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aecbd-193">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="aecbd-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aecbd-194">Search-Flags</span></span>           | <span data-ttu-id="aecbd-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="aecbd-195">0x00000001</span></span>                                                   |
| <span data-ttu-id="aecbd-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aecbd-196">System-Flags</span></span>           | <span data-ttu-id="aecbd-197">0x00000012</span><span class="sxs-lookup"><span data-stu-id="aecbd-197">0x00000012</span></span>                                                   |
| <span data-ttu-id="aecbd-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="aecbd-198">Classes used in</span></span>        | [<span data-ttu-id="aecbd-199">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="aecbd-199">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="aecbd-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aecbd-200">Windows Server 2008</span></span>



| <span data-ttu-id="aecbd-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="aecbd-201">Entry</span></span> | <span data-ttu-id="aecbd-202">Value</span><span class="sxs-lookup"><span data-stu-id="aecbd-202">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="aecbd-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="aecbd-203">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="aecbd-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aecbd-204">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="aecbd-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="aecbd-205">System-Only</span></span>            | <span data-ttu-id="aecbd-206">False</span><span class="sxs-lookup"><span data-stu-id="aecbd-206">False</span></span>                                                        |
| <span data-ttu-id="aecbd-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="aecbd-207">Is-Single-Valued</span></span>       | <span data-ttu-id="aecbd-208">False</span><span class="sxs-lookup"><span data-stu-id="aecbd-208">False</span></span>                                                        |
| <span data-ttu-id="aecbd-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="aecbd-209">Is Indexed</span></span>             | <span data-ttu-id="aecbd-210">True</span><span class="sxs-lookup"><span data-stu-id="aecbd-210">True</span></span>                                                         |
| <span data-ttu-id="aecbd-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="aecbd-211">In Global Catalog</span></span>      | <span data-ttu-id="aecbd-212">True</span><span class="sxs-lookup"><span data-stu-id="aecbd-212">True</span></span>                                                         |
| <span data-ttu-id="aecbd-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="aecbd-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="aecbd-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aecbd-214">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="aecbd-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aecbd-215">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="aecbd-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aecbd-216">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="aecbd-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aecbd-217">Search-Flags</span></span>           | <span data-ttu-id="aecbd-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="aecbd-218">0x00000001</span></span>                                                   |
| <span data-ttu-id="aecbd-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aecbd-219">System-Flags</span></span>           | <span data-ttu-id="aecbd-220">0x00000012</span><span class="sxs-lookup"><span data-stu-id="aecbd-220">0x00000012</span></span>                                                   |
| <span data-ttu-id="aecbd-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="aecbd-221">Classes used in</span></span>        | [<span data-ttu-id="aecbd-222">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="aecbd-222">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="aecbd-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aecbd-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="aecbd-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="aecbd-224">Entry</span></span> | <span data-ttu-id="aecbd-225">Value</span><span class="sxs-lookup"><span data-stu-id="aecbd-225">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="aecbd-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="aecbd-226">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="aecbd-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aecbd-227">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="aecbd-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="aecbd-228">System-Only</span></span>            | <span data-ttu-id="aecbd-229">False</span><span class="sxs-lookup"><span data-stu-id="aecbd-229">False</span></span>                                                        |
| <span data-ttu-id="aecbd-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="aecbd-230">Is-Single-Valued</span></span>       | <span data-ttu-id="aecbd-231">False</span><span class="sxs-lookup"><span data-stu-id="aecbd-231">False</span></span>                                                        |
| <span data-ttu-id="aecbd-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="aecbd-232">Is Indexed</span></span>             | <span data-ttu-id="aecbd-233">True</span><span class="sxs-lookup"><span data-stu-id="aecbd-233">True</span></span>                                                         |
| <span data-ttu-id="aecbd-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="aecbd-234">In Global Catalog</span></span>      | <span data-ttu-id="aecbd-235">True</span><span class="sxs-lookup"><span data-stu-id="aecbd-235">True</span></span>                                                         |
| <span data-ttu-id="aecbd-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="aecbd-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="aecbd-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aecbd-237">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="aecbd-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aecbd-238">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="aecbd-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aecbd-239">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="aecbd-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aecbd-240">Search-Flags</span></span>           | <span data-ttu-id="aecbd-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="aecbd-241">0x00000001</span></span>                                                   |
| <span data-ttu-id="aecbd-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aecbd-242">System-Flags</span></span>           | <span data-ttu-id="aecbd-243">0x00000012</span><span class="sxs-lookup"><span data-stu-id="aecbd-243">0x00000012</span></span>                                                   |
| <span data-ttu-id="aecbd-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="aecbd-244">Classes used in</span></span>        | [<span data-ttu-id="aecbd-245">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="aecbd-245">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="aecbd-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aecbd-246">Windows Server 2012</span></span>



| <span data-ttu-id="aecbd-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="aecbd-247">Entry</span></span> | <span data-ttu-id="aecbd-248">Value</span><span class="sxs-lookup"><span data-stu-id="aecbd-248">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="aecbd-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="aecbd-249">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="aecbd-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aecbd-250">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="aecbd-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="aecbd-251">System-Only</span></span>            | <span data-ttu-id="aecbd-252">False</span><span class="sxs-lookup"><span data-stu-id="aecbd-252">False</span></span>                                                        |
| <span data-ttu-id="aecbd-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="aecbd-253">Is-Single-Valued</span></span>       | <span data-ttu-id="aecbd-254">False</span><span class="sxs-lookup"><span data-stu-id="aecbd-254">False</span></span>                                                        |
| <span data-ttu-id="aecbd-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="aecbd-255">Is Indexed</span></span>             | <span data-ttu-id="aecbd-256">True</span><span class="sxs-lookup"><span data-stu-id="aecbd-256">True</span></span>                                                         |
| <span data-ttu-id="aecbd-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="aecbd-257">In Global Catalog</span></span>      | <span data-ttu-id="aecbd-258">True</span><span class="sxs-lookup"><span data-stu-id="aecbd-258">True</span></span>                                                         |
| <span data-ttu-id="aecbd-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="aecbd-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="aecbd-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aecbd-260">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="aecbd-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aecbd-261">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="aecbd-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aecbd-262">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="aecbd-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aecbd-263">Search-Flags</span></span>           | <span data-ttu-id="aecbd-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="aecbd-264">0x00000001</span></span>                                                   |
| <span data-ttu-id="aecbd-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aecbd-265">System-Flags</span></span>           | <span data-ttu-id="aecbd-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="aecbd-266">0x00000012</span></span>                                                   |
| <span data-ttu-id="aecbd-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="aecbd-267">Classes used in</span></span>        | [<span data-ttu-id="aecbd-268">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="aecbd-268">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





