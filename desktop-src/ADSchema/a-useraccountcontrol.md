---
title: Atributo User-Account-control
description: Marcas que controlan el comportamiento de la cuenta de usuario.
ms.assetid: fc81a16a-f537-44cc-957c-5d7ca66b9755
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de control de cuentas de usuario
- atributo de userAccountControl esquema de AD
topic_type:
- apiref
api_name:
- User-Account-Control
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f60297d22aad76b229c691a667ac22a87271402c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151707"
---
# <a name="user-account-control-attribute"></a><span data-ttu-id="eb3e9-105">Atributo User-Account-control</span><span class="sxs-lookup"><span data-stu-id="eb3e9-105">User-Account-Control attribute</span></span>

<span data-ttu-id="eb3e9-106">Marcas que controlan el comportamiento de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-106">Flags that control the behavior of the user account.</span></span>



| <span data-ttu-id="eb3e9-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb3e9-107">Entry</span></span> | <span data-ttu-id="eb3e9-108">Value</span><span class="sxs-lookup"><span data-stu-id="eb3e9-108">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="eb3e9-109">CN</span><span class="sxs-lookup"><span data-stu-id="eb3e9-109">CN</span></span>                | <span data-ttu-id="eb3e9-110">Control de cuentas de usuario</span><span class="sxs-lookup"><span data-stu-id="eb3e9-110">User-Account-Control</span></span>                  |
| <span data-ttu-id="eb3e9-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="eb3e9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="eb3e9-112">userAccountControl</span><span class="sxs-lookup"><span data-stu-id="eb3e9-112">userAccountControl</span></span>                    |
| <span data-ttu-id="eb3e9-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="eb3e9-113">Size</span></span>              | <span data-ttu-id="eb3e9-114">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-114">4 bytes.</span></span>                              |
| <span data-ttu-id="eb3e9-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="eb3e9-115">Update Privilege</span></span>  | <span data-ttu-id="eb3e9-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-116">This value is set by the system.</span></span>      |
| <span data-ttu-id="eb3e9-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="eb3e9-117">Update Frequency</span></span>  | <span data-ttu-id="eb3e9-118">Cada vez que cambia la Directiva de cuenta.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-118">Each time the account policy changes.</span></span> |
| <span data-ttu-id="eb3e9-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="eb3e9-119">Attribute-Id</span></span>      | <span data-ttu-id="eb3e9-120">1.2.840.113556.1.4.8</span><span class="sxs-lookup"><span data-stu-id="eb3e9-120">1.2.840.113556.1.4.8</span></span>                  |
| <span data-ttu-id="eb3e9-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="eb3e9-121">System-Id-Guid</span></span>    | <span data-ttu-id="eb3e9-122">bf967a68-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="eb3e9-122">bf967a68-0de6-11d0-a285-00aa003049e2</span></span>  |
| <span data-ttu-id="eb3e9-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb3e9-123">Syntax</span></span>            | [<span data-ttu-id="eb3e9-124">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="eb3e9-124">**Enumeration**</span></span>](s-enumeration.md)  |



## <a name="implementations"></a><span data-ttu-id="eb3e9-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="eb3e9-125">Implementations</span></span>

-   [<span data-ttu-id="eb3e9-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="eb3e9-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="eb3e9-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="eb3e9-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="eb3e9-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="eb3e9-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="eb3e9-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="eb3e9-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="eb3e9-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="eb3e9-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="eb3e9-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="eb3e9-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="eb3e9-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eb3e9-132">Windows 2000 Server</span></span>



| <span data-ttu-id="eb3e9-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb3e9-133">Entry</span></span> | <span data-ttu-id="eb3e9-134">Value</span><span class="sxs-lookup"><span data-stu-id="eb3e9-134">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="eb3e9-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="eb3e9-135">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="eb3e9-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb3e9-136">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="eb3e9-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb3e9-137">System-Only</span></span>            | <span data-ttu-id="eb3e9-138">False</span><span class="sxs-lookup"><span data-stu-id="eb3e9-138">False</span></span>                             |
| <span data-ttu-id="eb3e9-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="eb3e9-139">Is-Single-Valued</span></span>       | <span data-ttu-id="eb3e9-140">True</span><span class="sxs-lookup"><span data-stu-id="eb3e9-140">True</span></span>                              |
| <span data-ttu-id="eb3e9-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="eb3e9-141">Is Indexed</span></span>             | <span data-ttu-id="eb3e9-142">True</span><span class="sxs-lookup"><span data-stu-id="eb3e9-142">True</span></span>                              |
| <span data-ttu-id="eb3e9-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="eb3e9-143">In Global Catalog</span></span>      | <span data-ttu-id="eb3e9-144">True</span><span class="sxs-lookup"><span data-stu-id="eb3e9-144">True</span></span>                              |
| <span data-ttu-id="eb3e9-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="eb3e9-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb3e9-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb3e9-146">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="eb3e9-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb3e9-147">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="eb3e9-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb3e9-148">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="eb3e9-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb3e9-149">Search-Flags</span></span>           | <span data-ttu-id="eb3e9-150">0x00000019</span><span class="sxs-lookup"><span data-stu-id="eb3e9-150">0x00000019</span></span>                        |
| <span data-ttu-id="eb3e9-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb3e9-151">System-Flags</span></span>           | <span data-ttu-id="eb3e9-152">0x00000012</span><span class="sxs-lookup"><span data-stu-id="eb3e9-152">0x00000012</span></span>                        |
| <span data-ttu-id="eb3e9-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="eb3e9-153">Classes used in</span></span>        | [<span data-ttu-id="eb3e9-154">**User**</span><span class="sxs-lookup"><span data-stu-id="eb3e9-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="eb3e9-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eb3e9-155">Windows Server 2003</span></span>



| <span data-ttu-id="eb3e9-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb3e9-156">Entry</span></span> | <span data-ttu-id="eb3e9-157">Value</span><span class="sxs-lookup"><span data-stu-id="eb3e9-157">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="eb3e9-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="eb3e9-158">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="eb3e9-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb3e9-159">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="eb3e9-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb3e9-160">System-Only</span></span>            | <span data-ttu-id="eb3e9-161">False</span><span class="sxs-lookup"><span data-stu-id="eb3e9-161">False</span></span>                             |
| <span data-ttu-id="eb3e9-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="eb3e9-162">Is-Single-Valued</span></span>       | <span data-ttu-id="eb3e9-163">True</span><span class="sxs-lookup"><span data-stu-id="eb3e9-163">True</span></span>                              |
| <span data-ttu-id="eb3e9-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="eb3e9-164">Is Indexed</span></span>             | <span data-ttu-id="eb3e9-165">True</span><span class="sxs-lookup"><span data-stu-id="eb3e9-165">True</span></span>                              |
| <span data-ttu-id="eb3e9-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="eb3e9-166">In Global Catalog</span></span>      | <span data-ttu-id="eb3e9-167">True</span><span class="sxs-lookup"><span data-stu-id="eb3e9-167">True</span></span>                              |
| <span data-ttu-id="eb3e9-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="eb3e9-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb3e9-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb3e9-169">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="eb3e9-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb3e9-170">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="eb3e9-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb3e9-171">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="eb3e9-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb3e9-172">Search-Flags</span></span>           | <span data-ttu-id="eb3e9-173">0x00000019</span><span class="sxs-lookup"><span data-stu-id="eb3e9-173">0x00000019</span></span>                        |
| <span data-ttu-id="eb3e9-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb3e9-174">System-Flags</span></span>           | <span data-ttu-id="eb3e9-175">0x00000012</span><span class="sxs-lookup"><span data-stu-id="eb3e9-175">0x00000012</span></span>                        |
| <span data-ttu-id="eb3e9-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="eb3e9-176">Classes used in</span></span>        | [<span data-ttu-id="eb3e9-177">**User**</span><span class="sxs-lookup"><span data-stu-id="eb3e9-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="eb3e9-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="eb3e9-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="eb3e9-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb3e9-179">Entry</span></span> | <span data-ttu-id="eb3e9-180">Value</span><span class="sxs-lookup"><span data-stu-id="eb3e9-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="eb3e9-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="eb3e9-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="eb3e9-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb3e9-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="eb3e9-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb3e9-183">System-Only</span></span>            | <span data-ttu-id="eb3e9-184">False</span><span class="sxs-lookup"><span data-stu-id="eb3e9-184">False</span></span>                             |
| <span data-ttu-id="eb3e9-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="eb3e9-185">Is-Single-Valued</span></span>       | <span data-ttu-id="eb3e9-186">True</span><span class="sxs-lookup"><span data-stu-id="eb3e9-186">True</span></span>                              |
| <span data-ttu-id="eb3e9-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="eb3e9-187">Is Indexed</span></span>             | <span data-ttu-id="eb3e9-188">True</span><span class="sxs-lookup"><span data-stu-id="eb3e9-188">True</span></span>                              |
| <span data-ttu-id="eb3e9-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="eb3e9-189">In Global Catalog</span></span>      | <span data-ttu-id="eb3e9-190">True</span><span class="sxs-lookup"><span data-stu-id="eb3e9-190">True</span></span>                              |
| <span data-ttu-id="eb3e9-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="eb3e9-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb3e9-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb3e9-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="eb3e9-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb3e9-193">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="eb3e9-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb3e9-194">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="eb3e9-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb3e9-195">Search-Flags</span></span>           | <span data-ttu-id="eb3e9-196">0x00000019</span><span class="sxs-lookup"><span data-stu-id="eb3e9-196">0x00000019</span></span>                        |
| <span data-ttu-id="eb3e9-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb3e9-197">System-Flags</span></span>           | <span data-ttu-id="eb3e9-198">0x00000012</span><span class="sxs-lookup"><span data-stu-id="eb3e9-198">0x00000012</span></span>                        |
| <span data-ttu-id="eb3e9-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="eb3e9-199">Classes used in</span></span>        | [<span data-ttu-id="eb3e9-200">**User**</span><span class="sxs-lookup"><span data-stu-id="eb3e9-200">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="eb3e9-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb3e9-201">Windows Server 2008</span></span>



| <span data-ttu-id="eb3e9-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb3e9-202">Entry</span></span> | <span data-ttu-id="eb3e9-203">Value</span><span class="sxs-lookup"><span data-stu-id="eb3e9-203">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="eb3e9-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="eb3e9-204">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="eb3e9-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb3e9-205">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="eb3e9-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb3e9-206">System-Only</span></span>            | <span data-ttu-id="eb3e9-207">False</span><span class="sxs-lookup"><span data-stu-id="eb3e9-207">False</span></span>                             |
| <span data-ttu-id="eb3e9-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="eb3e9-208">Is-Single-Valued</span></span>       | <span data-ttu-id="eb3e9-209">True</span><span class="sxs-lookup"><span data-stu-id="eb3e9-209">True</span></span>                              |
| <span data-ttu-id="eb3e9-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="eb3e9-210">Is Indexed</span></span>             | <span data-ttu-id="eb3e9-211">True</span><span class="sxs-lookup"><span data-stu-id="eb3e9-211">True</span></span>                              |
| <span data-ttu-id="eb3e9-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="eb3e9-212">In Global Catalog</span></span>      | <span data-ttu-id="eb3e9-213">True</span><span class="sxs-lookup"><span data-stu-id="eb3e9-213">True</span></span>                              |
| <span data-ttu-id="eb3e9-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="eb3e9-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb3e9-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb3e9-215">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="eb3e9-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb3e9-216">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="eb3e9-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb3e9-217">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="eb3e9-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb3e9-218">Search-Flags</span></span>           | <span data-ttu-id="eb3e9-219">0x00000019</span><span class="sxs-lookup"><span data-stu-id="eb3e9-219">0x00000019</span></span>                        |
| <span data-ttu-id="eb3e9-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb3e9-220">System-Flags</span></span>           | <span data-ttu-id="eb3e9-221">0x00000012</span><span class="sxs-lookup"><span data-stu-id="eb3e9-221">0x00000012</span></span>                        |
| <span data-ttu-id="eb3e9-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="eb3e9-222">Classes used in</span></span>        | [<span data-ttu-id="eb3e9-223">**User**</span><span class="sxs-lookup"><span data-stu-id="eb3e9-223">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="eb3e9-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eb3e9-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="eb3e9-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb3e9-225">Entry</span></span> | <span data-ttu-id="eb3e9-226">Value</span><span class="sxs-lookup"><span data-stu-id="eb3e9-226">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="eb3e9-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="eb3e9-227">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="eb3e9-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb3e9-228">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="eb3e9-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb3e9-229">System-Only</span></span>            | <span data-ttu-id="eb3e9-230">False</span><span class="sxs-lookup"><span data-stu-id="eb3e9-230">False</span></span>                             |
| <span data-ttu-id="eb3e9-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="eb3e9-231">Is-Single-Valued</span></span>       | <span data-ttu-id="eb3e9-232">True</span><span class="sxs-lookup"><span data-stu-id="eb3e9-232">True</span></span>                              |
| <span data-ttu-id="eb3e9-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="eb3e9-233">Is Indexed</span></span>             | <span data-ttu-id="eb3e9-234">True</span><span class="sxs-lookup"><span data-stu-id="eb3e9-234">True</span></span>                              |
| <span data-ttu-id="eb3e9-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="eb3e9-235">In Global Catalog</span></span>      | <span data-ttu-id="eb3e9-236">True</span><span class="sxs-lookup"><span data-stu-id="eb3e9-236">True</span></span>                              |
| <span data-ttu-id="eb3e9-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="eb3e9-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb3e9-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb3e9-238">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="eb3e9-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb3e9-239">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="eb3e9-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb3e9-240">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="eb3e9-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb3e9-241">Search-Flags</span></span>           | <span data-ttu-id="eb3e9-242">0x00000019</span><span class="sxs-lookup"><span data-stu-id="eb3e9-242">0x00000019</span></span>                        |
| <span data-ttu-id="eb3e9-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb3e9-243">System-Flags</span></span>           | <span data-ttu-id="eb3e9-244">0x00000012</span><span class="sxs-lookup"><span data-stu-id="eb3e9-244">0x00000012</span></span>                        |
| <span data-ttu-id="eb3e9-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="eb3e9-245">Classes used in</span></span>        | [<span data-ttu-id="eb3e9-246">**User**</span><span class="sxs-lookup"><span data-stu-id="eb3e9-246">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="eb3e9-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eb3e9-247">Windows Server 2012</span></span>



| <span data-ttu-id="eb3e9-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb3e9-248">Entry</span></span> | <span data-ttu-id="eb3e9-249">Value</span><span class="sxs-lookup"><span data-stu-id="eb3e9-249">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="eb3e9-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="eb3e9-250">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="eb3e9-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb3e9-251">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="eb3e9-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb3e9-252">System-Only</span></span>            | <span data-ttu-id="eb3e9-253">False</span><span class="sxs-lookup"><span data-stu-id="eb3e9-253">False</span></span>                             |
| <span data-ttu-id="eb3e9-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="eb3e9-254">Is-Single-Valued</span></span>       | <span data-ttu-id="eb3e9-255">True</span><span class="sxs-lookup"><span data-stu-id="eb3e9-255">True</span></span>                              |
| <span data-ttu-id="eb3e9-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="eb3e9-256">Is Indexed</span></span>             | <span data-ttu-id="eb3e9-257">True</span><span class="sxs-lookup"><span data-stu-id="eb3e9-257">True</span></span>                              |
| <span data-ttu-id="eb3e9-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="eb3e9-258">In Global Catalog</span></span>      | <span data-ttu-id="eb3e9-259">True</span><span class="sxs-lookup"><span data-stu-id="eb3e9-259">True</span></span>                              |
| <span data-ttu-id="eb3e9-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="eb3e9-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb3e9-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb3e9-261">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="eb3e9-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb3e9-262">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="eb3e9-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb3e9-263">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="eb3e9-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb3e9-264">Search-Flags</span></span>           | <span data-ttu-id="eb3e9-265">0x00000019</span><span class="sxs-lookup"><span data-stu-id="eb3e9-265">0x00000019</span></span>                        |
| <span data-ttu-id="eb3e9-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb3e9-266">System-Flags</span></span>           | <span data-ttu-id="eb3e9-267">0x00000012</span><span class="sxs-lookup"><span data-stu-id="eb3e9-267">0x00000012</span></span>                        |
| <span data-ttu-id="eb3e9-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="eb3e9-268">Classes used in</span></span>        | [<span data-ttu-id="eb3e9-269">**User**</span><span class="sxs-lookup"><span data-stu-id="eb3e9-269">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="eb3e9-270">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb3e9-270">Remarks</span></span>

<span data-ttu-id="eb3e9-271">Este valor de atributo puede ser cero o una combinación de uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-271">This attribute value can be zero or a combination of one or more of the following values.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb3e9-272">Valor hexadecimal</span><span class="sxs-lookup"><span data-stu-id="eb3e9-272">Hexadecimal value</span></span></th>
<th><span data-ttu-id="eb3e9-273">Identifier (definido en iAds. h)</span><span class="sxs-lookup"><span data-stu-id="eb3e9-273">Identifier (defined in iads.h)</span></span></th>
<th><span data-ttu-id="eb3e9-274">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb3e9-274">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eb3e9-275">0x00000001</span><span class="sxs-lookup"><span data-stu-id="eb3e9-275">0x00000001</span></span></td>
<td><span data-ttu-id="eb3e9-276"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-276"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-277">Se ejecuta el script de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-277">The logon script is executed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb3e9-278">0x00000002</span><span class="sxs-lookup"><span data-stu-id="eb3e9-278">0x00000002</span></span></td>
<td><span data-ttu-id="eb3e9-279"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-279"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-280">La cuenta de usuario está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-280">The user account is disabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb3e9-281">0x00000008</span><span class="sxs-lookup"><span data-stu-id="eb3e9-281">0x00000008</span></span></td>
<td><span data-ttu-id="eb3e9-282"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-282"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-283">El directorio particular es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-283">The home directory is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb3e9-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eb3e9-284">0x00000010</span></span></td>
<td><span data-ttu-id="eb3e9-285"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-285"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-286">La cuenta está bloqueada actualmente.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-286">The account is currently locked out.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb3e9-287">0x00000020</span><span class="sxs-lookup"><span data-stu-id="eb3e9-287">0x00000020</span></span></td>
<td><span data-ttu-id="eb3e9-288"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-288"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-289">No se requiere una contraseña.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-289">No password is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb3e9-290">0x00000040</span><span class="sxs-lookup"><span data-stu-id="eb3e9-290">0x00000040</span></span></td>
<td><span data-ttu-id="eb3e9-291"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-291"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-292">El usuario no puede cambiar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-292">The user cannot change the password.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="eb3e9-293">No se puede asignar la configuración de permisos de PASSWD_CANT_CHANGE modificando directamente el atributo UserAccountControl.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-293">You cannot assign the permission settings of PASSWD_CANT_CHANGE by directly modifying the UserAccountControl attribute.</span></span> <span data-ttu-id="eb3e9-294">Para obtener más información y un ejemplo de código que muestra cómo evitar que un usuario cambie la contraseña, consulte el <a href="/windows/desktop/ADSI/user-cannot-change-password">usuario no puede cambiar la contraseña</a>.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-294">For more information and a code example that shows how to prevent a user from changing the password, see <a href="/windows/desktop/ADSI/user-cannot-change-password">User Cannot Change Password</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="eb3e9-295">:</span><span class="sxs-lookup"><span data-stu-id="eb3e9-295">:</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb3e9-296">0x00000080</span><span class="sxs-lookup"><span data-stu-id="eb3e9-296">0x00000080</span></span></td>
<td><span data-ttu-id="eb3e9-297"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-297"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-298">El usuario puede enviar una contraseña cifrada.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-298">The user can send an encrypted password.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb3e9-299">0x00000100</span><span class="sxs-lookup"><span data-stu-id="eb3e9-299">0x00000100</span></span></td>
<td><span data-ttu-id="eb3e9-300"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-300"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-301">Se trata de una cuenta para usuarios cuya cuenta principal se encuentra en otro dominio.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-301">This is an account for users whose primary account is in another domain.</span></span> <span data-ttu-id="eb3e9-302">Esta cuenta proporciona acceso de usuario a este dominio, pero no a ningún dominio que confíe en este dominio.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-302">This account provides user access to this domain, but not to any domain that trusts this domain.</span></span> <span data-ttu-id="eb3e9-303">También se conoce como cuenta de usuario local.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-303">Also known as a local user account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb3e9-304">0x00000200</span><span class="sxs-lookup"><span data-stu-id="eb3e9-304">0x00000200</span></span></td>
<td><span data-ttu-id="eb3e9-305"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-305"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-306">Se trata de un tipo de cuenta predeterminado que representa a un usuario típico.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-306">This is a default account type that represents a typical user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb3e9-307">0x00000800</span><span class="sxs-lookup"><span data-stu-id="eb3e9-307">0x00000800</span></span></td>
<td><span data-ttu-id="eb3e9-308"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-308"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-309">Se trata de un permiso para confiar en la cuenta de un dominio del sistema que confía en otros dominios.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-309">This is a permit to trust account for a system domain that trusts other domains.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb3e9-310">0x00001000</span><span class="sxs-lookup"><span data-stu-id="eb3e9-310">0x00001000</span></span></td>
<td><span data-ttu-id="eb3e9-311"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-311"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-312">Se trata de una cuenta de equipo para un equipo que es miembro de este dominio.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-312">This is a computer account for a computer that is a member of this domain.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb3e9-313">0x00002000</span><span class="sxs-lookup"><span data-stu-id="eb3e9-313">0x00002000</span></span></td>
<td><span data-ttu-id="eb3e9-314"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-314"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-315">Se trata de una cuenta de equipo para un controlador de dominio de copia de seguridad del sistema que es miembro de este dominio.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-315">This is a computer account for a system backup domain controller that is a member of this domain.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb3e9-316">0x00004000</span><span class="sxs-lookup"><span data-stu-id="eb3e9-316">0x00004000</span></span></td>
<td><span data-ttu-id="eb3e9-317">N/D</span><span class="sxs-lookup"><span data-stu-id="eb3e9-317">N/A</span></span></td>
<td><span data-ttu-id="eb3e9-318">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-318">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb3e9-319">0x00008000</span><span class="sxs-lookup"><span data-stu-id="eb3e9-319">0x00008000</span></span></td>
<td><span data-ttu-id="eb3e9-320">N/D</span><span class="sxs-lookup"><span data-stu-id="eb3e9-320">N/A</span></span></td>
<td><span data-ttu-id="eb3e9-321">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-321">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb3e9-322">0x00010000</span><span class="sxs-lookup"><span data-stu-id="eb3e9-322">0x00010000</span></span></td>
<td><span data-ttu-id="eb3e9-323"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-323"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-324">La contraseña de esta cuenta nunca expirará.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-324">The password for this account will never expire.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb3e9-325">0x00020000</span><span class="sxs-lookup"><span data-stu-id="eb3e9-325">0x00020000</span></span></td>
<td><span data-ttu-id="eb3e9-326"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-326"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-327">Se trata de una cuenta de inicio de sesión de MNS.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-327">This is an MNS logon account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb3e9-328">0x00040000</span><span class="sxs-lookup"><span data-stu-id="eb3e9-328">0x00040000</span></span></td>
<td><span data-ttu-id="eb3e9-329"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-329"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-330">El usuario debe iniciar sesión con una tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-330">The user must log on using a smart card.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb3e9-331">0x00080000</span><span class="sxs-lookup"><span data-stu-id="eb3e9-331">0x00080000</span></span></td>
<td><span data-ttu-id="eb3e9-332"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-332"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-333">La cuenta de servicio (cuenta de usuario o de equipo), en la que se ejecuta un servicio, es de confianza para la delegación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-333">The service account (user or computer account), under which a service runs, is trusted for Kerberos delegation.</span></span> <span data-ttu-id="eb3e9-334">Cualquier servicio de este tipo puede suplantar a un cliente que solicite el servicio.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-334">Any such service can impersonate a client requesting the service.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb3e9-335">0x00100000</span><span class="sxs-lookup"><span data-stu-id="eb3e9-335">0x00100000</span></span></td>
<td><span data-ttu-id="eb3e9-336"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-336"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-337">El contexto de seguridad del usuario no se delegará a un servicio, incluso si la cuenta de servicio está establecida como de confianza para la delegación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-337">The security context of the user will not be delegated to a service even if the service account is set as trusted for Kerberos delegation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb3e9-338">0x00200000</span><span class="sxs-lookup"><span data-stu-id="eb3e9-338">0x00200000</span></span></td>
<td><span data-ttu-id="eb3e9-339"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-339"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-340">Restrinja esta entidad de seguridad para usar solo los tipos de cifrado estándar de cifrado de datos (DES) para las claves.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-340">Restrict this principal to use only Data Encryption Standard (DES) encryption types for keys.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb3e9-341">0x00400000</span><span class="sxs-lookup"><span data-stu-id="eb3e9-341">0x00400000</span></span></td>
<td><span data-ttu-id="eb3e9-342"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-342"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-343">Esta cuenta no requiere la autenticación previa de Kerberos para el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-343">This account does not require Kerberos pre-authentication for logon.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb3e9-344">0x00800000</span><span class="sxs-lookup"><span data-stu-id="eb3e9-344">0x00800000</span></span></td>
<td><span data-ttu-id="eb3e9-345"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-345"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-346">La contraseña de usuario ha expirado.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-346">The user password has expired.</span></span> <span data-ttu-id="eb3e9-347">El sistema crea esta marca utilizando los datos del atributo <a href="a-pwdlastset.md"><strong>pwd-Last-Set</strong></a> y la Directiva de dominio.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-347">This flag is created by the system using data from the <a href="a-pwdlastset.md"><strong>Pwd-Last-Set</strong></a> attribute and the domain policy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb3e9-348">0x01000000</span><span class="sxs-lookup"><span data-stu-id="eb3e9-348">0x01000000</span></span></td>
<td><span data-ttu-id="eb3e9-349"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb3e9-349"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a></span></span></td>
<td><span data-ttu-id="eb3e9-350">La cuenta está habilitada para la delegación.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-350">The account is enabled for delegation.</span></span> <span data-ttu-id="eb3e9-351">Se trata de una configuración que depende de la seguridad; las cuentas con esta opción habilitada deben controlarse estrictamente.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-351">This is a security-sensitive setting; accounts with this option enabled should be strictly controlled.</span></span> <span data-ttu-id="eb3e9-352">Esta configuración permite que un servicio que se ejecuta en la cuenta asuma una identidad de cliente y se autentique como ese usuario en otros servidores remotos de la red.</span><span class="sxs-lookup"><span data-stu-id="eb3e9-352">This setting enables a service running under the account to assume a client identity and authenticate as that user to other remote servers on the network.</span></span></td>
</tr>
</tbody>
</table>



 

