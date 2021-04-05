---
title: Trust-POSIX-atributo offset
description: El desplazamiento de la interfaz del sistema operativo portátil (POSIX) del dominio de confianza.
ms.assetid: a1263f9f-1577-44b8-b7cc-317a8ecb37f1
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo Trust-POSIX-offset
- trustPosixOffset esquema de AD de atributos
topic_type:
- apiref
api_name:
- Trust-Posix-Offset
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de8f3dca090d44ea545dcc290b04d99131d50dc7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104079844"
---
# <a name="trust-posix-offset-attribute"></a><span data-ttu-id="8934e-105">Trust-POSIX-atributo offset</span><span class="sxs-lookup"><span data-stu-id="8934e-105">Trust-Posix-Offset attribute</span></span>

<span data-ttu-id="8934e-106">El desplazamiento de la interfaz del sistema operativo portátil (POSIX) del dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="8934e-106">The Portable Operating System Interface (POSIX) offset for the trusted domain.</span></span>



| <span data-ttu-id="8934e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="8934e-107">Entry</span></span> | <span data-ttu-id="8934e-108">Value</span><span class="sxs-lookup"><span data-stu-id="8934e-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8934e-109">CN</span><span class="sxs-lookup"><span data-stu-id="8934e-109">CN</span></span>                | <span data-ttu-id="8934e-110">Trust-POSIX-desplazamiento</span><span class="sxs-lookup"><span data-stu-id="8934e-110">Trust-Posix-Offset</span></span>                   |
| <span data-ttu-id="8934e-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="8934e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8934e-112">trustPosixOffset</span><span class="sxs-lookup"><span data-stu-id="8934e-112">trustPosixOffset</span></span>                     |
| <span data-ttu-id="8934e-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="8934e-113">Size</span></span>              | <span data-ttu-id="8934e-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="8934e-114">4 bytes</span></span>                              |
| <span data-ttu-id="8934e-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="8934e-115">Update Privilege</span></span>  | <span data-ttu-id="8934e-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="8934e-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="8934e-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="8934e-117">Update Frequency</span></span>  | <span data-ttu-id="8934e-118">Cuando se crea una nueva confianza.</span><span class="sxs-lookup"><span data-stu-id="8934e-118">When a new trust is created.</span></span>         |
| <span data-ttu-id="8934e-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8934e-119">Attribute-Id</span></span>      | <span data-ttu-id="8934e-120">1.2.840.113556.1.4.134</span><span class="sxs-lookup"><span data-stu-id="8934e-120">1.2.840.113556.1.4.134</span></span>               |
| <span data-ttu-id="8934e-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8934e-121">System-Id-Guid</span></span>    | <span data-ttu-id="8934e-122">bf967a5e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8934e-122">bf967a5e-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="8934e-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8934e-123">Syntax</span></span>            | [<span data-ttu-id="8934e-124">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="8934e-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="8934e-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="8934e-125">Implementations</span></span>

-   [<span data-ttu-id="8934e-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8934e-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8934e-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8934e-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8934e-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8934e-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8934e-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8934e-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8934e-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8934e-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8934e-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8934e-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8934e-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8934e-132">Windows 2000 Server</span></span>



| <span data-ttu-id="8934e-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="8934e-133">Entry</span></span> | <span data-ttu-id="8934e-134">Value</span><span class="sxs-lookup"><span data-stu-id="8934e-134">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="8934e-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8934e-135">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="8934e-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8934e-136">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="8934e-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="8934e-137">System-Only</span></span>            | <span data-ttu-id="8934e-138">False</span><span class="sxs-lookup"><span data-stu-id="8934e-138">False</span></span>                                                |
| <span data-ttu-id="8934e-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8934e-139">Is-Single-Valued</span></span>       | <span data-ttu-id="8934e-140">True</span><span class="sxs-lookup"><span data-stu-id="8934e-140">True</span></span>                                                 |
| <span data-ttu-id="8934e-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8934e-141">Is Indexed</span></span>             | <span data-ttu-id="8934e-142">False</span><span class="sxs-lookup"><span data-stu-id="8934e-142">False</span></span>                                                |
| <span data-ttu-id="8934e-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8934e-143">In Global Catalog</span></span>      | <span data-ttu-id="8934e-144">False</span><span class="sxs-lookup"><span data-stu-id="8934e-144">False</span></span>                                                |
| <span data-ttu-id="8934e-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8934e-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="8934e-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8934e-146">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="8934e-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8934e-147">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="8934e-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8934e-148">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="8934e-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8934e-149">Search-Flags</span></span>           | <span data-ttu-id="8934e-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8934e-150">0x00000000</span></span>                                           |
| <span data-ttu-id="8934e-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8934e-151">System-Flags</span></span>           | <span data-ttu-id="8934e-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8934e-152">0x00000010</span></span>                                           |
| <span data-ttu-id="8934e-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8934e-153">Classes used in</span></span>        | [<span data-ttu-id="8934e-154">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="8934e-154">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8934e-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8934e-155">Windows Server 2003</span></span>



| <span data-ttu-id="8934e-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="8934e-156">Entry</span></span> | <span data-ttu-id="8934e-157">Value</span><span class="sxs-lookup"><span data-stu-id="8934e-157">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="8934e-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8934e-158">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="8934e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8934e-159">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="8934e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="8934e-160">System-Only</span></span>            | <span data-ttu-id="8934e-161">False</span><span class="sxs-lookup"><span data-stu-id="8934e-161">False</span></span>                                                |
| <span data-ttu-id="8934e-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8934e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="8934e-163">True</span><span class="sxs-lookup"><span data-stu-id="8934e-163">True</span></span>                                                 |
| <span data-ttu-id="8934e-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8934e-164">Is Indexed</span></span>             | <span data-ttu-id="8934e-165">False</span><span class="sxs-lookup"><span data-stu-id="8934e-165">False</span></span>                                                |
| <span data-ttu-id="8934e-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8934e-166">In Global Catalog</span></span>      | <span data-ttu-id="8934e-167">False</span><span class="sxs-lookup"><span data-stu-id="8934e-167">False</span></span>                                                |
| <span data-ttu-id="8934e-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8934e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="8934e-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8934e-169">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="8934e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8934e-170">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="8934e-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8934e-171">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="8934e-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8934e-172">Search-Flags</span></span>           | <span data-ttu-id="8934e-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8934e-173">0x00000000</span></span>                                           |
| <span data-ttu-id="8934e-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8934e-174">System-Flags</span></span>           | <span data-ttu-id="8934e-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8934e-175">0x00000010</span></span>                                           |
| <span data-ttu-id="8934e-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8934e-176">Classes used in</span></span>        | [<span data-ttu-id="8934e-177">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="8934e-177">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8934e-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8934e-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8934e-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="8934e-179">Entry</span></span> | <span data-ttu-id="8934e-180">Value</span><span class="sxs-lookup"><span data-stu-id="8934e-180">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="8934e-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8934e-181">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="8934e-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8934e-182">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="8934e-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="8934e-183">System-Only</span></span>            | <span data-ttu-id="8934e-184">False</span><span class="sxs-lookup"><span data-stu-id="8934e-184">False</span></span>                                                |
| <span data-ttu-id="8934e-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8934e-185">Is-Single-Valued</span></span>       | <span data-ttu-id="8934e-186">True</span><span class="sxs-lookup"><span data-stu-id="8934e-186">True</span></span>                                                 |
| <span data-ttu-id="8934e-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8934e-187">Is Indexed</span></span>             | <span data-ttu-id="8934e-188">False</span><span class="sxs-lookup"><span data-stu-id="8934e-188">False</span></span>                                                |
| <span data-ttu-id="8934e-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8934e-189">In Global Catalog</span></span>      | <span data-ttu-id="8934e-190">False</span><span class="sxs-lookup"><span data-stu-id="8934e-190">False</span></span>                                                |
| <span data-ttu-id="8934e-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8934e-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="8934e-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8934e-192">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="8934e-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8934e-193">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="8934e-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8934e-194">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="8934e-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8934e-195">Search-Flags</span></span>           | <span data-ttu-id="8934e-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8934e-196">0x00000000</span></span>                                           |
| <span data-ttu-id="8934e-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8934e-197">System-Flags</span></span>           | <span data-ttu-id="8934e-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8934e-198">0x00000010</span></span>                                           |
| <span data-ttu-id="8934e-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8934e-199">Classes used in</span></span>        | [<span data-ttu-id="8934e-200">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="8934e-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8934e-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8934e-201">Windows Server 2008</span></span>



| <span data-ttu-id="8934e-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="8934e-202">Entry</span></span> | <span data-ttu-id="8934e-203">Value</span><span class="sxs-lookup"><span data-stu-id="8934e-203">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="8934e-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8934e-204">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="8934e-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8934e-205">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="8934e-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="8934e-206">System-Only</span></span>            | <span data-ttu-id="8934e-207">False</span><span class="sxs-lookup"><span data-stu-id="8934e-207">False</span></span>                                                |
| <span data-ttu-id="8934e-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8934e-208">Is-Single-Valued</span></span>       | <span data-ttu-id="8934e-209">True</span><span class="sxs-lookup"><span data-stu-id="8934e-209">True</span></span>                                                 |
| <span data-ttu-id="8934e-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8934e-210">Is Indexed</span></span>             | <span data-ttu-id="8934e-211">False</span><span class="sxs-lookup"><span data-stu-id="8934e-211">False</span></span>                                                |
| <span data-ttu-id="8934e-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8934e-212">In Global Catalog</span></span>      | <span data-ttu-id="8934e-213">False</span><span class="sxs-lookup"><span data-stu-id="8934e-213">False</span></span>                                                |
| <span data-ttu-id="8934e-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8934e-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="8934e-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8934e-215">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="8934e-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8934e-216">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="8934e-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8934e-217">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="8934e-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8934e-218">Search-Flags</span></span>           | <span data-ttu-id="8934e-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8934e-219">0x00000000</span></span>                                           |
| <span data-ttu-id="8934e-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8934e-220">System-Flags</span></span>           | <span data-ttu-id="8934e-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8934e-221">0x00000010</span></span>                                           |
| <span data-ttu-id="8934e-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8934e-222">Classes used in</span></span>        | [<span data-ttu-id="8934e-223">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="8934e-223">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8934e-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8934e-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8934e-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="8934e-225">Entry</span></span> | <span data-ttu-id="8934e-226">Value</span><span class="sxs-lookup"><span data-stu-id="8934e-226">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="8934e-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8934e-227">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="8934e-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8934e-228">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="8934e-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="8934e-229">System-Only</span></span>            | <span data-ttu-id="8934e-230">False</span><span class="sxs-lookup"><span data-stu-id="8934e-230">False</span></span>                                                |
| <span data-ttu-id="8934e-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8934e-231">Is-Single-Valued</span></span>       | <span data-ttu-id="8934e-232">True</span><span class="sxs-lookup"><span data-stu-id="8934e-232">True</span></span>                                                 |
| <span data-ttu-id="8934e-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8934e-233">Is Indexed</span></span>             | <span data-ttu-id="8934e-234">False</span><span class="sxs-lookup"><span data-stu-id="8934e-234">False</span></span>                                                |
| <span data-ttu-id="8934e-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8934e-235">In Global Catalog</span></span>      | <span data-ttu-id="8934e-236">False</span><span class="sxs-lookup"><span data-stu-id="8934e-236">False</span></span>                                                |
| <span data-ttu-id="8934e-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8934e-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="8934e-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8934e-238">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="8934e-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8934e-239">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="8934e-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8934e-240">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="8934e-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8934e-241">Search-Flags</span></span>           | <span data-ttu-id="8934e-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8934e-242">0x00000000</span></span>                                           |
| <span data-ttu-id="8934e-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8934e-243">System-Flags</span></span>           | <span data-ttu-id="8934e-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8934e-244">0x00000010</span></span>                                           |
| <span data-ttu-id="8934e-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8934e-245">Classes used in</span></span>        | [<span data-ttu-id="8934e-246">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="8934e-246">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8934e-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8934e-247">Windows Server 2012</span></span>



| <span data-ttu-id="8934e-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="8934e-248">Entry</span></span> | <span data-ttu-id="8934e-249">Value</span><span class="sxs-lookup"><span data-stu-id="8934e-249">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="8934e-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8934e-250">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="8934e-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8934e-251">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="8934e-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="8934e-252">System-Only</span></span>            | <span data-ttu-id="8934e-253">False</span><span class="sxs-lookup"><span data-stu-id="8934e-253">False</span></span>                                                |
| <span data-ttu-id="8934e-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8934e-254">Is-Single-Valued</span></span>       | <span data-ttu-id="8934e-255">True</span><span class="sxs-lookup"><span data-stu-id="8934e-255">True</span></span>                                                 |
| <span data-ttu-id="8934e-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8934e-256">Is Indexed</span></span>             | <span data-ttu-id="8934e-257">False</span><span class="sxs-lookup"><span data-stu-id="8934e-257">False</span></span>                                                |
| <span data-ttu-id="8934e-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8934e-258">In Global Catalog</span></span>      | <span data-ttu-id="8934e-259">False</span><span class="sxs-lookup"><span data-stu-id="8934e-259">False</span></span>                                                |
| <span data-ttu-id="8934e-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8934e-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="8934e-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8934e-261">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="8934e-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8934e-262">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="8934e-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8934e-263">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="8934e-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8934e-264">Search-Flags</span></span>           | <span data-ttu-id="8934e-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8934e-265">0x00000000</span></span>                                           |
| <span data-ttu-id="8934e-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8934e-266">System-Flags</span></span>           | <span data-ttu-id="8934e-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8934e-267">0x00000010</span></span>                                           |
| <span data-ttu-id="8934e-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8934e-268">Classes used in</span></span>        | [<span data-ttu-id="8934e-269">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="8934e-269">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





