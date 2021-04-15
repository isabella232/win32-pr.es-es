---
title: Supplemental-Credentials atributo)
description: Credenciales almacenadas para su uso en la autenticación. La versión cifrada de la contraseña del usuario. Este atributo no es legible ni modificable.
ms.assetid: 642aa699-094e-40ed-a2f8-ec7219c85de2
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Supplemental-Credentials
- supplementalCredentials esquema de AD de atributos
topic_type:
- apiref
api_name:
- Supplemental-Credentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e19a73b3ae3cf19745fc995a59c336b72d264e78
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535890"
---
# <a name="supplemental-credentials-attribute"></a><span data-ttu-id="7e5aa-107">Supplemental-Credentials atributo)</span><span class="sxs-lookup"><span data-stu-id="7e5aa-107">Supplemental-Credentials attribute</span></span>

<span data-ttu-id="7e5aa-108">Credenciales almacenadas para su uso en la autenticación.</span><span class="sxs-lookup"><span data-stu-id="7e5aa-108">Stored credentials for use in authenticating.</span></span> <span data-ttu-id="7e5aa-109">La versión cifrada de la contraseña del usuario.</span><span class="sxs-lookup"><span data-stu-id="7e5aa-109">The encrypted version of the user's password.</span></span> <span data-ttu-id="7e5aa-110">Este atributo no es legible ni modificable.</span><span class="sxs-lookup"><span data-stu-id="7e5aa-110">This attribute is neither readable nor writable.</span></span>



| <span data-ttu-id="7e5aa-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e5aa-111">Entry</span></span> | <span data-ttu-id="7e5aa-112">Value</span><span class="sxs-lookup"><span data-stu-id="7e5aa-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="7e5aa-113">CN</span><span class="sxs-lookup"><span data-stu-id="7e5aa-113">CN</span></span>                | <span data-ttu-id="7e5aa-114">Supplemental-Credentials</span><span class="sxs-lookup"><span data-stu-id="7e5aa-114">Supplemental-Credentials</span></span>                              |
| <span data-ttu-id="7e5aa-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="7e5aa-115">Ldap-Display-Name</span></span> | <span data-ttu-id="7e5aa-116">supplementalCredentials</span><span class="sxs-lookup"><span data-stu-id="7e5aa-116">supplementalCredentials</span></span>                               |
| <span data-ttu-id="7e5aa-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="7e5aa-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="7e5aa-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="7e5aa-118">Update Privilege</span></span>  | <span data-ttu-id="7e5aa-119">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="7e5aa-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="7e5aa-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="7e5aa-120">Update Frequency</span></span>  | <span data-ttu-id="7e5aa-121">Cuando cambia la contraseña del usuario.</span><span class="sxs-lookup"><span data-stu-id="7e5aa-121">When the user's password changes.</span></span>                     |
| <span data-ttu-id="7e5aa-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7e5aa-122">Attribute-Id</span></span>      | <span data-ttu-id="7e5aa-123">1.2.840.113556.1.4.125</span><span class="sxs-lookup"><span data-stu-id="7e5aa-123">1.2.840.113556.1.4.125</span></span>                                |
| <span data-ttu-id="7e5aa-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7e5aa-124">System-Id-Guid</span></span>    | <span data-ttu-id="7e5aa-125">bf967a3f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7e5aa-125">bf967a3f-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="7e5aa-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e5aa-126">Syntax</span></span>            | [<span data-ttu-id="7e5aa-127">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="7e5aa-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="7e5aa-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="7e5aa-128">Implementations</span></span>

-   [<span data-ttu-id="7e5aa-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7e5aa-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7e5aa-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7e5aa-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7e5aa-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7e5aa-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7e5aa-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7e5aa-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7e5aa-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7e5aa-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7e5aa-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7e5aa-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7e5aa-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7e5aa-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7e5aa-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7e5aa-136">Windows 2000 Server</span></span>



| <span data-ttu-id="7e5aa-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e5aa-137">Entry</span></span> | <span data-ttu-id="7e5aa-138">Value</span><span class="sxs-lookup"><span data-stu-id="7e5aa-138">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7e5aa-139">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e5aa-139">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e5aa-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e5aa-140">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e5aa-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e5aa-141">System-Only</span></span>            | <span data-ttu-id="7e5aa-142">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-142">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-143">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e5aa-143">Is-Single-Valued</span></span>       | <span data-ttu-id="7e5aa-144">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-144">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-145">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e5aa-145">Is Indexed</span></span>             | <span data-ttu-id="7e5aa-146">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-146">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-147">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e5aa-147">In Global Catalog</span></span>      | <span data-ttu-id="7e5aa-148">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-148">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-149">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e5aa-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e5aa-150">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e5aa-150">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7e5aa-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e5aa-151">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="7e5aa-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e5aa-152">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="7e5aa-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e5aa-153">Search-Flags</span></span>           | <span data-ttu-id="7e5aa-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e5aa-154">0x00000000</span></span>                                                   |
| <span data-ttu-id="7e5aa-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e5aa-155">System-Flags</span></span>           | <span data-ttu-id="7e5aa-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e5aa-156">0x00000010</span></span>                                                   |
| <span data-ttu-id="7e5aa-157">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e5aa-157">Classes used in</span></span>        | [<span data-ttu-id="7e5aa-158">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="7e5aa-158">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7e5aa-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7e5aa-159">Windows Server 2003</span></span>



| <span data-ttu-id="7e5aa-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e5aa-160">Entry</span></span> | <span data-ttu-id="7e5aa-161">Value</span><span class="sxs-lookup"><span data-stu-id="7e5aa-161">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7e5aa-162">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e5aa-162">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e5aa-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e5aa-163">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e5aa-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e5aa-164">System-Only</span></span>            | <span data-ttu-id="7e5aa-165">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-165">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-166">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e5aa-166">Is-Single-Valued</span></span>       | <span data-ttu-id="7e5aa-167">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-167">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-168">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e5aa-168">Is Indexed</span></span>             | <span data-ttu-id="7e5aa-169">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-169">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-170">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e5aa-170">In Global Catalog</span></span>      | <span data-ttu-id="7e5aa-171">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-171">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-172">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e5aa-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e5aa-173">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e5aa-173">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7e5aa-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e5aa-174">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="7e5aa-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e5aa-175">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="7e5aa-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e5aa-176">Search-Flags</span></span>           | <span data-ttu-id="7e5aa-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e5aa-177">0x00000000</span></span>                                                   |
| <span data-ttu-id="7e5aa-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e5aa-178">System-Flags</span></span>           | <span data-ttu-id="7e5aa-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e5aa-179">0x00000010</span></span>                                                   |
| <span data-ttu-id="7e5aa-180">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e5aa-180">Classes used in</span></span>        | [<span data-ttu-id="7e5aa-181">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="7e5aa-181">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7e5aa-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="7e5aa-182">ADAM</span></span>



| <span data-ttu-id="7e5aa-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e5aa-183">Entry</span></span> | <span data-ttu-id="7e5aa-184">Value</span><span class="sxs-lookup"><span data-stu-id="7e5aa-184">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7e5aa-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e5aa-185">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e5aa-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e5aa-186">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e5aa-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e5aa-187">System-Only</span></span>            | <span data-ttu-id="7e5aa-188">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-188">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e5aa-189">Is-Single-Valued</span></span>       | <span data-ttu-id="7e5aa-190">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-190">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e5aa-191">Is Indexed</span></span>             | <span data-ttu-id="7e5aa-192">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-192">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e5aa-193">In Global Catalog</span></span>      | <span data-ttu-id="7e5aa-194">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-194">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e5aa-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e5aa-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e5aa-196">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7e5aa-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e5aa-197">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="7e5aa-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e5aa-198">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="7e5aa-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e5aa-199">Search-Flags</span></span>           | <span data-ttu-id="7e5aa-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e5aa-200">0x00000000</span></span>                                                   |
| <span data-ttu-id="7e5aa-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e5aa-201">System-Flags</span></span>           | <span data-ttu-id="7e5aa-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e5aa-202">0x00000010</span></span>                                                   |
| <span data-ttu-id="7e5aa-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e5aa-203">Classes used in</span></span>        | [<span data-ttu-id="7e5aa-204">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="7e5aa-204">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7e5aa-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7e5aa-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7e5aa-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e5aa-206">Entry</span></span> | <span data-ttu-id="7e5aa-207">Value</span><span class="sxs-lookup"><span data-stu-id="7e5aa-207">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7e5aa-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e5aa-208">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e5aa-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e5aa-209">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e5aa-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e5aa-210">System-Only</span></span>            | <span data-ttu-id="7e5aa-211">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-211">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-212">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e5aa-212">Is-Single-Valued</span></span>       | <span data-ttu-id="7e5aa-213">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-213">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-214">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e5aa-214">Is Indexed</span></span>             | <span data-ttu-id="7e5aa-215">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-215">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-216">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e5aa-216">In Global Catalog</span></span>      | <span data-ttu-id="7e5aa-217">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-217">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-218">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e5aa-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e5aa-219">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e5aa-219">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7e5aa-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e5aa-220">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="7e5aa-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e5aa-221">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="7e5aa-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e5aa-222">Search-Flags</span></span>           | <span data-ttu-id="7e5aa-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e5aa-223">0x00000000</span></span>                                                   |
| <span data-ttu-id="7e5aa-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e5aa-224">System-Flags</span></span>           | <span data-ttu-id="7e5aa-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e5aa-225">0x00000010</span></span>                                                   |
| <span data-ttu-id="7e5aa-226">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e5aa-226">Classes used in</span></span>        | [<span data-ttu-id="7e5aa-227">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="7e5aa-227">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7e5aa-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e5aa-228">Windows Server 2008</span></span>



| <span data-ttu-id="7e5aa-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e5aa-229">Entry</span></span> | <span data-ttu-id="7e5aa-230">Value</span><span class="sxs-lookup"><span data-stu-id="7e5aa-230">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7e5aa-231">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e5aa-231">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e5aa-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e5aa-232">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e5aa-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e5aa-233">System-Only</span></span>            | <span data-ttu-id="7e5aa-234">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-234">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-235">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e5aa-235">Is-Single-Valued</span></span>       | <span data-ttu-id="7e5aa-236">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-236">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-237">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e5aa-237">Is Indexed</span></span>             | <span data-ttu-id="7e5aa-238">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-238">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-239">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e5aa-239">In Global Catalog</span></span>      | <span data-ttu-id="7e5aa-240">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-240">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-241">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e5aa-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e5aa-242">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e5aa-242">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7e5aa-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e5aa-243">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="7e5aa-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e5aa-244">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="7e5aa-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e5aa-245">Search-Flags</span></span>           | <span data-ttu-id="7e5aa-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e5aa-246">0x00000000</span></span>                                                   |
| <span data-ttu-id="7e5aa-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e5aa-247">System-Flags</span></span>           | <span data-ttu-id="7e5aa-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e5aa-248">0x00000010</span></span>                                                   |
| <span data-ttu-id="7e5aa-249">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e5aa-249">Classes used in</span></span>        | [<span data-ttu-id="7e5aa-250">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="7e5aa-250">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7e5aa-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7e5aa-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7e5aa-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e5aa-252">Entry</span></span> | <span data-ttu-id="7e5aa-253">Value</span><span class="sxs-lookup"><span data-stu-id="7e5aa-253">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7e5aa-254">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e5aa-254">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e5aa-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e5aa-255">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e5aa-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e5aa-256">System-Only</span></span>            | <span data-ttu-id="7e5aa-257">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-257">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-258">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e5aa-258">Is-Single-Valued</span></span>       | <span data-ttu-id="7e5aa-259">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-259">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-260">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e5aa-260">Is Indexed</span></span>             | <span data-ttu-id="7e5aa-261">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-261">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-262">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e5aa-262">In Global Catalog</span></span>      | <span data-ttu-id="7e5aa-263">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-263">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-264">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e5aa-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e5aa-265">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e5aa-265">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7e5aa-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e5aa-266">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="7e5aa-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e5aa-267">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="7e5aa-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e5aa-268">Search-Flags</span></span>           | <span data-ttu-id="7e5aa-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e5aa-269">0x00000000</span></span>                                                   |
| <span data-ttu-id="7e5aa-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e5aa-270">System-Flags</span></span>           | <span data-ttu-id="7e5aa-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e5aa-271">0x00000010</span></span>                                                   |
| <span data-ttu-id="7e5aa-272">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e5aa-272">Classes used in</span></span>        | [<span data-ttu-id="7e5aa-273">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="7e5aa-273">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7e5aa-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7e5aa-274">Windows Server 2012</span></span>



| <span data-ttu-id="7e5aa-275">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e5aa-275">Entry</span></span> | <span data-ttu-id="7e5aa-276">Value</span><span class="sxs-lookup"><span data-stu-id="7e5aa-276">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7e5aa-277">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e5aa-277">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e5aa-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e5aa-278">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e5aa-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e5aa-279">System-Only</span></span>            | <span data-ttu-id="7e5aa-280">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-280">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-281">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e5aa-281">Is-Single-Valued</span></span>       | <span data-ttu-id="7e5aa-282">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-282">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-283">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e5aa-283">Is Indexed</span></span>             | <span data-ttu-id="7e5aa-284">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-284">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-285">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e5aa-285">In Global Catalog</span></span>      | <span data-ttu-id="7e5aa-286">False</span><span class="sxs-lookup"><span data-stu-id="7e5aa-286">False</span></span>                                                        |
| <span data-ttu-id="7e5aa-287">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e5aa-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e5aa-288">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e5aa-288">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7e5aa-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e5aa-289">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="7e5aa-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e5aa-290">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="7e5aa-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e5aa-291">Search-Flags</span></span>           | <span data-ttu-id="7e5aa-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e5aa-292">0x00000000</span></span>                                                   |
| <span data-ttu-id="7e5aa-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e5aa-293">System-Flags</span></span>           | <span data-ttu-id="7e5aa-294">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e5aa-294">0x00000010</span></span>                                                   |
| <span data-ttu-id="7e5aa-295">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e5aa-295">Classes used in</span></span>        | [<span data-ttu-id="7e5aa-296">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="7e5aa-296">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





