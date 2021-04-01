---
title: LM-pwd-atributo History
description: El historial de contraseñas del usuario en el formato unidireccional (OWF) de LAN Manager (LM). LM OWF se usa para la compatibilidad con los clientes de LAN Manager 2. x, Windows 95 y Windows 98.
ms.assetid: c4cb2e74-b37d-4c76-8d21-d71bc9c19a4a
ms.tgt_platform: multiple
keywords:
- 'LM-pwd-History: esquema de AD de atributos'
- lmPwdHistory esquema de AD de atributos
topic_type:
- apiref
api_name:
- Lm-Pwd-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28f5c73b35bb0ea2cae9d01324d82e1568485541
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906073"
---
# <a name="lm-pwd-history-attribute"></a><span data-ttu-id="41cdf-106">LM-pwd-atributo History</span><span class="sxs-lookup"><span data-stu-id="41cdf-106">Lm-Pwd-History attribute</span></span>

<span data-ttu-id="41cdf-107">El historial de contraseñas del usuario en el formato unidireccional (OWF) de LAN Manager (LM).</span><span class="sxs-lookup"><span data-stu-id="41cdf-107">The password history of the user in LAN Manager (LM) one-way format (OWF).</span></span> <span data-ttu-id="41cdf-108">LM OWF se usa para la compatibilidad con LAN Manager 2. clientes *x* , Windows 95 y Windows 98.</span><span class="sxs-lookup"><span data-stu-id="41cdf-108">The LM OWF is used for compatibility with LAN Manager 2.*x* clients, Windows 95, and Windows 98.</span></span>



| <span data-ttu-id="41cdf-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="41cdf-109">Entry</span></span> | <span data-ttu-id="41cdf-110">Value</span><span class="sxs-lookup"><span data-stu-id="41cdf-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="41cdf-111">CN</span><span class="sxs-lookup"><span data-stu-id="41cdf-111">CN</span></span>                | <span data-ttu-id="41cdf-112">LM-pwd-historial</span><span class="sxs-lookup"><span data-stu-id="41cdf-112">Lm-Pwd-History</span></span>                                        |
| <span data-ttu-id="41cdf-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="41cdf-113">Ldap-Display-Name</span></span> | <span data-ttu-id="41cdf-114">lmPwdHistory</span><span class="sxs-lookup"><span data-stu-id="41cdf-114">lmPwdHistory</span></span>                                          |
| <span data-ttu-id="41cdf-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="41cdf-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="41cdf-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="41cdf-116">Update Privilege</span></span>  | <span data-ttu-id="41cdf-117">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="41cdf-117">Domain administrator</span></span>                                  |
| <span data-ttu-id="41cdf-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="41cdf-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="41cdf-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="41cdf-119">Attribute-Id</span></span>      | <span data-ttu-id="41cdf-120">1.2.840.113556.1.4.160</span><span class="sxs-lookup"><span data-stu-id="41cdf-120">1.2.840.113556.1.4.160</span></span>                                |
| <span data-ttu-id="41cdf-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="41cdf-121">System-Id-Guid</span></span>    | <span data-ttu-id="41cdf-122">bf96799d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="41cdf-122">bf96799d-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="41cdf-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41cdf-123">Syntax</span></span>            | [<span data-ttu-id="41cdf-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="41cdf-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="41cdf-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="41cdf-125">Implementations</span></span>

-   [<span data-ttu-id="41cdf-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="41cdf-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="41cdf-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="41cdf-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="41cdf-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="41cdf-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="41cdf-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="41cdf-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="41cdf-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="41cdf-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="41cdf-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="41cdf-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="41cdf-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="41cdf-132">Windows 2000 Server</span></span>



| <span data-ttu-id="41cdf-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="41cdf-133">Entry</span></span> | <span data-ttu-id="41cdf-134">Value</span><span class="sxs-lookup"><span data-stu-id="41cdf-134">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="41cdf-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="41cdf-135">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="41cdf-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="41cdf-136">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="41cdf-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="41cdf-137">System-Only</span></span>            | <span data-ttu-id="41cdf-138">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-138">False</span></span>                             |
| <span data-ttu-id="41cdf-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="41cdf-139">Is-Single-Valued</span></span>       | <span data-ttu-id="41cdf-140">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-140">False</span></span>                             |
| <span data-ttu-id="41cdf-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="41cdf-141">Is Indexed</span></span>             | <span data-ttu-id="41cdf-142">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-142">False</span></span>                             |
| <span data-ttu-id="41cdf-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="41cdf-143">In Global Catalog</span></span>      | <span data-ttu-id="41cdf-144">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-144">False</span></span>                             |
| <span data-ttu-id="41cdf-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="41cdf-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="41cdf-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="41cdf-146">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="41cdf-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="41cdf-147">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="41cdf-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="41cdf-148">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="41cdf-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="41cdf-149">Search-Flags</span></span>           | <span data-ttu-id="41cdf-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41cdf-150">0x00000000</span></span>                        |
| <span data-ttu-id="41cdf-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="41cdf-151">System-Flags</span></span>           | <span data-ttu-id="41cdf-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41cdf-152">0x00000010</span></span>                        |
| <span data-ttu-id="41cdf-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="41cdf-153">Classes used in</span></span>        | [<span data-ttu-id="41cdf-154">**User**</span><span class="sxs-lookup"><span data-stu-id="41cdf-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="41cdf-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="41cdf-155">Windows Server 2003</span></span>



| <span data-ttu-id="41cdf-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="41cdf-156">Entry</span></span> | <span data-ttu-id="41cdf-157">Value</span><span class="sxs-lookup"><span data-stu-id="41cdf-157">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="41cdf-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="41cdf-158">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="41cdf-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="41cdf-159">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="41cdf-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="41cdf-160">System-Only</span></span>            | <span data-ttu-id="41cdf-161">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-161">False</span></span>                             |
| <span data-ttu-id="41cdf-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="41cdf-162">Is-Single-Valued</span></span>       | <span data-ttu-id="41cdf-163">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-163">False</span></span>                             |
| <span data-ttu-id="41cdf-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="41cdf-164">Is Indexed</span></span>             | <span data-ttu-id="41cdf-165">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-165">False</span></span>                             |
| <span data-ttu-id="41cdf-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="41cdf-166">In Global Catalog</span></span>      | <span data-ttu-id="41cdf-167">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-167">False</span></span>                             |
| <span data-ttu-id="41cdf-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="41cdf-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="41cdf-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="41cdf-169">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="41cdf-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="41cdf-170">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="41cdf-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="41cdf-171">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="41cdf-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="41cdf-172">Search-Flags</span></span>           | <span data-ttu-id="41cdf-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41cdf-173">0x00000000</span></span>                        |
| <span data-ttu-id="41cdf-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="41cdf-174">System-Flags</span></span>           | <span data-ttu-id="41cdf-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41cdf-175">0x00000010</span></span>                        |
| <span data-ttu-id="41cdf-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="41cdf-176">Classes used in</span></span>        | [<span data-ttu-id="41cdf-177">**User**</span><span class="sxs-lookup"><span data-stu-id="41cdf-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="41cdf-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="41cdf-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="41cdf-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="41cdf-179">Entry</span></span> | <span data-ttu-id="41cdf-180">Value</span><span class="sxs-lookup"><span data-stu-id="41cdf-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="41cdf-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="41cdf-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="41cdf-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="41cdf-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="41cdf-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="41cdf-183">System-Only</span></span>            | <span data-ttu-id="41cdf-184">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-184">False</span></span>                             |
| <span data-ttu-id="41cdf-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="41cdf-185">Is-Single-Valued</span></span>       | <span data-ttu-id="41cdf-186">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-186">False</span></span>                             |
| <span data-ttu-id="41cdf-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="41cdf-187">Is Indexed</span></span>             | <span data-ttu-id="41cdf-188">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-188">False</span></span>                             |
| <span data-ttu-id="41cdf-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="41cdf-189">In Global Catalog</span></span>      | <span data-ttu-id="41cdf-190">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-190">False</span></span>                             |
| <span data-ttu-id="41cdf-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="41cdf-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="41cdf-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="41cdf-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="41cdf-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="41cdf-193">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="41cdf-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="41cdf-194">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="41cdf-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="41cdf-195">Search-Flags</span></span>           | <span data-ttu-id="41cdf-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41cdf-196">0x00000000</span></span>                        |
| <span data-ttu-id="41cdf-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="41cdf-197">System-Flags</span></span>           | <span data-ttu-id="41cdf-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41cdf-198">0x00000010</span></span>                        |
| <span data-ttu-id="41cdf-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="41cdf-199">Classes used in</span></span>        | [<span data-ttu-id="41cdf-200">**User**</span><span class="sxs-lookup"><span data-stu-id="41cdf-200">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="41cdf-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41cdf-201">Windows Server 2008</span></span>



| <span data-ttu-id="41cdf-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="41cdf-202">Entry</span></span> | <span data-ttu-id="41cdf-203">Value</span><span class="sxs-lookup"><span data-stu-id="41cdf-203">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="41cdf-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="41cdf-204">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="41cdf-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="41cdf-205">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="41cdf-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="41cdf-206">System-Only</span></span>            | <span data-ttu-id="41cdf-207">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-207">False</span></span>                             |
| <span data-ttu-id="41cdf-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="41cdf-208">Is-Single-Valued</span></span>       | <span data-ttu-id="41cdf-209">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-209">False</span></span>                             |
| <span data-ttu-id="41cdf-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="41cdf-210">Is Indexed</span></span>             | <span data-ttu-id="41cdf-211">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-211">False</span></span>                             |
| <span data-ttu-id="41cdf-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="41cdf-212">In Global Catalog</span></span>      | <span data-ttu-id="41cdf-213">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-213">False</span></span>                             |
| <span data-ttu-id="41cdf-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="41cdf-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="41cdf-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="41cdf-215">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="41cdf-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="41cdf-216">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="41cdf-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="41cdf-217">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="41cdf-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="41cdf-218">Search-Flags</span></span>           | <span data-ttu-id="41cdf-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41cdf-219">0x00000000</span></span>                        |
| <span data-ttu-id="41cdf-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="41cdf-220">System-Flags</span></span>           | <span data-ttu-id="41cdf-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41cdf-221">0x00000010</span></span>                        |
| <span data-ttu-id="41cdf-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="41cdf-222">Classes used in</span></span>        | [<span data-ttu-id="41cdf-223">**User**</span><span class="sxs-lookup"><span data-stu-id="41cdf-223">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="41cdf-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="41cdf-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="41cdf-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="41cdf-225">Entry</span></span> | <span data-ttu-id="41cdf-226">Value</span><span class="sxs-lookup"><span data-stu-id="41cdf-226">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="41cdf-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="41cdf-227">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="41cdf-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="41cdf-228">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="41cdf-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="41cdf-229">System-Only</span></span>            | <span data-ttu-id="41cdf-230">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-230">False</span></span>                             |
| <span data-ttu-id="41cdf-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="41cdf-231">Is-Single-Valued</span></span>       | <span data-ttu-id="41cdf-232">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-232">False</span></span>                             |
| <span data-ttu-id="41cdf-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="41cdf-233">Is Indexed</span></span>             | <span data-ttu-id="41cdf-234">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-234">False</span></span>                             |
| <span data-ttu-id="41cdf-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="41cdf-235">In Global Catalog</span></span>      | <span data-ttu-id="41cdf-236">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-236">False</span></span>                             |
| <span data-ttu-id="41cdf-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="41cdf-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="41cdf-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="41cdf-238">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="41cdf-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="41cdf-239">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="41cdf-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="41cdf-240">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="41cdf-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="41cdf-241">Search-Flags</span></span>           | <span data-ttu-id="41cdf-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41cdf-242">0x00000000</span></span>                        |
| <span data-ttu-id="41cdf-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="41cdf-243">System-Flags</span></span>           | <span data-ttu-id="41cdf-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41cdf-244">0x00000010</span></span>                        |
| <span data-ttu-id="41cdf-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="41cdf-245">Classes used in</span></span>        | [<span data-ttu-id="41cdf-246">**User**</span><span class="sxs-lookup"><span data-stu-id="41cdf-246">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="41cdf-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="41cdf-247">Windows Server 2012</span></span>



| <span data-ttu-id="41cdf-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="41cdf-248">Entry</span></span> | <span data-ttu-id="41cdf-249">Value</span><span class="sxs-lookup"><span data-stu-id="41cdf-249">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="41cdf-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="41cdf-250">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="41cdf-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="41cdf-251">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="41cdf-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="41cdf-252">System-Only</span></span>            | <span data-ttu-id="41cdf-253">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-253">False</span></span>                             |
| <span data-ttu-id="41cdf-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="41cdf-254">Is-Single-Valued</span></span>       | <span data-ttu-id="41cdf-255">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-255">False</span></span>                             |
| <span data-ttu-id="41cdf-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="41cdf-256">Is Indexed</span></span>             | <span data-ttu-id="41cdf-257">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-257">False</span></span>                             |
| <span data-ttu-id="41cdf-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="41cdf-258">In Global Catalog</span></span>      | <span data-ttu-id="41cdf-259">False</span><span class="sxs-lookup"><span data-stu-id="41cdf-259">False</span></span>                             |
| <span data-ttu-id="41cdf-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="41cdf-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="41cdf-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="41cdf-261">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="41cdf-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="41cdf-262">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="41cdf-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="41cdf-263">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="41cdf-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="41cdf-264">Search-Flags</span></span>           | <span data-ttu-id="41cdf-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41cdf-265">0x00000000</span></span>                        |
| <span data-ttu-id="41cdf-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="41cdf-266">System-Flags</span></span>           | <span data-ttu-id="41cdf-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41cdf-267">0x00000010</span></span>                        |
| <span data-ttu-id="41cdf-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="41cdf-268">Classes used in</span></span>        | [<span data-ttu-id="41cdf-269">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="41cdf-269">**User**</span></span>](c-user.md)<br/> |



 

 





