---
title: Short-Server-Name (atributo)
description: Nombre de servidor compatible con versiones anteriores a Windows 2000 para los servidores de impresión.
ms.assetid: 639704f4-e2b6-43e1-9b1b-6afffe8f0f6a
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de nombre de servidor corto
- shortServerName esquema de AD de atributos
topic_type:
- apiref
api_name:
- Short-Server-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e71b7cf5687b530bf76c673187d5152089d885d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997502"
---
# <a name="short-server-name-attribute"></a><span data-ttu-id="62c41-105">Short-Server-Name (atributo)</span><span class="sxs-lookup"><span data-stu-id="62c41-105">Short-Server-Name attribute</span></span>

<span data-ttu-id="62c41-106">Nombre de servidor compatible con versiones anteriores a Windows 2000 para los servidores de impresión.</span><span class="sxs-lookup"><span data-stu-id="62c41-106">Pre-Windows 2000 compatible server name for print servers.</span></span>



| <span data-ttu-id="62c41-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="62c41-107">Entry</span></span> | <span data-ttu-id="62c41-108">Value</span><span class="sxs-lookup"><span data-stu-id="62c41-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="62c41-109">CN</span><span class="sxs-lookup"><span data-stu-id="62c41-109">CN</span></span>                | <span data-ttu-id="62c41-110">Short-Server-Name</span><span class="sxs-lookup"><span data-stu-id="62c41-110">Short-Server-Name</span></span>                           |
| <span data-ttu-id="62c41-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="62c41-111">Ldap-Display-Name</span></span> | <span data-ttu-id="62c41-112">shortServerName</span><span class="sxs-lookup"><span data-stu-id="62c41-112">shortServerName</span></span>                             |
| <span data-ttu-id="62c41-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="62c41-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="62c41-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="62c41-114">Update Privilege</span></span>  | <span data-ttu-id="62c41-115">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="62c41-115">Domain administrator</span></span>                        |
| <span data-ttu-id="62c41-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="62c41-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="62c41-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="62c41-117">Attribute-Id</span></span>      | <span data-ttu-id="62c41-118">1.2.840.113556.1.4.1209</span><span class="sxs-lookup"><span data-stu-id="62c41-118">1.2.840.113556.1.4.1209</span></span>                     |
| <span data-ttu-id="62c41-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="62c41-119">System-Id-Guid</span></span>    | <span data-ttu-id="62c41-120">45b01501-c419-11d1-bbc9-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="62c41-120">45b01501-c419-11d1-bbc9-0080c76670c0</span></span>        |
| <span data-ttu-id="62c41-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62c41-121">Syntax</span></span>            | [<span data-ttu-id="62c41-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="62c41-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="62c41-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="62c41-123">Implementations</span></span>

-   [<span data-ttu-id="62c41-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="62c41-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="62c41-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="62c41-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="62c41-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="62c41-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="62c41-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="62c41-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="62c41-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="62c41-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="62c41-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="62c41-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="62c41-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="62c41-130">Windows 2000 Server</span></span>



| <span data-ttu-id="62c41-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="62c41-131">Entry</span></span> | <span data-ttu-id="62c41-132">Value</span><span class="sxs-lookup"><span data-stu-id="62c41-132">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="62c41-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="62c41-133">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="62c41-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62c41-134">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="62c41-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="62c41-135">System-Only</span></span>            | <span data-ttu-id="62c41-136">False</span><span class="sxs-lookup"><span data-stu-id="62c41-136">False</span></span>                                          |
| <span data-ttu-id="62c41-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="62c41-137">Is-Single-Valued</span></span>       | <span data-ttu-id="62c41-138">True</span><span class="sxs-lookup"><span data-stu-id="62c41-138">True</span></span>                                           |
| <span data-ttu-id="62c41-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="62c41-139">Is Indexed</span></span>             | <span data-ttu-id="62c41-140">False</span><span class="sxs-lookup"><span data-stu-id="62c41-140">False</span></span>                                          |
| <span data-ttu-id="62c41-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="62c41-141">In Global Catalog</span></span>      | <span data-ttu-id="62c41-142">True</span><span class="sxs-lookup"><span data-stu-id="62c41-142">True</span></span>                                           |
| <span data-ttu-id="62c41-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="62c41-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="62c41-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="62c41-144">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="62c41-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62c41-145">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="62c41-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62c41-146">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="62c41-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62c41-147">Search-Flags</span></span>           | <span data-ttu-id="62c41-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62c41-148">0x00000000</span></span>                                     |
| <span data-ttu-id="62c41-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62c41-149">System-Flags</span></span>           | <span data-ttu-id="62c41-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62c41-150">0x00000010</span></span>                                     |
| <span data-ttu-id="62c41-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="62c41-151">Classes used in</span></span>        | [<span data-ttu-id="62c41-152">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="62c41-152">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="62c41-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="62c41-153">Windows Server 2003</span></span>



| <span data-ttu-id="62c41-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="62c41-154">Entry</span></span> | <span data-ttu-id="62c41-155">Value</span><span class="sxs-lookup"><span data-stu-id="62c41-155">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="62c41-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="62c41-156">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="62c41-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62c41-157">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="62c41-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="62c41-158">System-Only</span></span>            | <span data-ttu-id="62c41-159">False</span><span class="sxs-lookup"><span data-stu-id="62c41-159">False</span></span>                                          |
| <span data-ttu-id="62c41-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="62c41-160">Is-Single-Valued</span></span>       | <span data-ttu-id="62c41-161">True</span><span class="sxs-lookup"><span data-stu-id="62c41-161">True</span></span>                                           |
| <span data-ttu-id="62c41-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="62c41-162">Is Indexed</span></span>             | <span data-ttu-id="62c41-163">False</span><span class="sxs-lookup"><span data-stu-id="62c41-163">False</span></span>                                          |
| <span data-ttu-id="62c41-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="62c41-164">In Global Catalog</span></span>      | <span data-ttu-id="62c41-165">True</span><span class="sxs-lookup"><span data-stu-id="62c41-165">True</span></span>                                           |
| <span data-ttu-id="62c41-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="62c41-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="62c41-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="62c41-167">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="62c41-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62c41-168">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="62c41-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62c41-169">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="62c41-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62c41-170">Search-Flags</span></span>           | <span data-ttu-id="62c41-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62c41-171">0x00000000</span></span>                                     |
| <span data-ttu-id="62c41-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62c41-172">System-Flags</span></span>           | <span data-ttu-id="62c41-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62c41-173">0x00000010</span></span>                                     |
| <span data-ttu-id="62c41-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="62c41-174">Classes used in</span></span>        | [<span data-ttu-id="62c41-175">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="62c41-175">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="62c41-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="62c41-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="62c41-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="62c41-177">Entry</span></span> | <span data-ttu-id="62c41-178">Value</span><span class="sxs-lookup"><span data-stu-id="62c41-178">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="62c41-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="62c41-179">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="62c41-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62c41-180">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="62c41-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="62c41-181">System-Only</span></span>            | <span data-ttu-id="62c41-182">False</span><span class="sxs-lookup"><span data-stu-id="62c41-182">False</span></span>                                          |
| <span data-ttu-id="62c41-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="62c41-183">Is-Single-Valued</span></span>       | <span data-ttu-id="62c41-184">True</span><span class="sxs-lookup"><span data-stu-id="62c41-184">True</span></span>                                           |
| <span data-ttu-id="62c41-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="62c41-185">Is Indexed</span></span>             | <span data-ttu-id="62c41-186">False</span><span class="sxs-lookup"><span data-stu-id="62c41-186">False</span></span>                                          |
| <span data-ttu-id="62c41-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="62c41-187">In Global Catalog</span></span>      | <span data-ttu-id="62c41-188">True</span><span class="sxs-lookup"><span data-stu-id="62c41-188">True</span></span>                                           |
| <span data-ttu-id="62c41-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="62c41-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="62c41-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="62c41-190">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="62c41-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62c41-191">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="62c41-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62c41-192">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="62c41-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62c41-193">Search-Flags</span></span>           | <span data-ttu-id="62c41-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62c41-194">0x00000000</span></span>                                     |
| <span data-ttu-id="62c41-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62c41-195">System-Flags</span></span>           | <span data-ttu-id="62c41-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62c41-196">0x00000010</span></span>                                     |
| <span data-ttu-id="62c41-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="62c41-197">Classes used in</span></span>        | [<span data-ttu-id="62c41-198">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="62c41-198">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="62c41-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62c41-199">Windows Server 2008</span></span>



| <span data-ttu-id="62c41-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="62c41-200">Entry</span></span> | <span data-ttu-id="62c41-201">Value</span><span class="sxs-lookup"><span data-stu-id="62c41-201">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="62c41-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="62c41-202">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="62c41-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62c41-203">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="62c41-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="62c41-204">System-Only</span></span>            | <span data-ttu-id="62c41-205">False</span><span class="sxs-lookup"><span data-stu-id="62c41-205">False</span></span>                                          |
| <span data-ttu-id="62c41-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="62c41-206">Is-Single-Valued</span></span>       | <span data-ttu-id="62c41-207">True</span><span class="sxs-lookup"><span data-stu-id="62c41-207">True</span></span>                                           |
| <span data-ttu-id="62c41-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="62c41-208">Is Indexed</span></span>             | <span data-ttu-id="62c41-209">False</span><span class="sxs-lookup"><span data-stu-id="62c41-209">False</span></span>                                          |
| <span data-ttu-id="62c41-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="62c41-210">In Global Catalog</span></span>      | <span data-ttu-id="62c41-211">True</span><span class="sxs-lookup"><span data-stu-id="62c41-211">True</span></span>                                           |
| <span data-ttu-id="62c41-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="62c41-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="62c41-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="62c41-213">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="62c41-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62c41-214">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="62c41-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62c41-215">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="62c41-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62c41-216">Search-Flags</span></span>           | <span data-ttu-id="62c41-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62c41-217">0x00000000</span></span>                                     |
| <span data-ttu-id="62c41-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62c41-218">System-Flags</span></span>           | <span data-ttu-id="62c41-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62c41-219">0x00000010</span></span>                                     |
| <span data-ttu-id="62c41-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="62c41-220">Classes used in</span></span>        | [<span data-ttu-id="62c41-221">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="62c41-221">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="62c41-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="62c41-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="62c41-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="62c41-223">Entry</span></span> | <span data-ttu-id="62c41-224">Value</span><span class="sxs-lookup"><span data-stu-id="62c41-224">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="62c41-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="62c41-225">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="62c41-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62c41-226">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="62c41-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="62c41-227">System-Only</span></span>            | <span data-ttu-id="62c41-228">False</span><span class="sxs-lookup"><span data-stu-id="62c41-228">False</span></span>                                          |
| <span data-ttu-id="62c41-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="62c41-229">Is-Single-Valued</span></span>       | <span data-ttu-id="62c41-230">True</span><span class="sxs-lookup"><span data-stu-id="62c41-230">True</span></span>                                           |
| <span data-ttu-id="62c41-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="62c41-231">Is Indexed</span></span>             | <span data-ttu-id="62c41-232">False</span><span class="sxs-lookup"><span data-stu-id="62c41-232">False</span></span>                                          |
| <span data-ttu-id="62c41-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="62c41-233">In Global Catalog</span></span>      | <span data-ttu-id="62c41-234">True</span><span class="sxs-lookup"><span data-stu-id="62c41-234">True</span></span>                                           |
| <span data-ttu-id="62c41-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="62c41-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="62c41-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="62c41-236">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="62c41-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62c41-237">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="62c41-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62c41-238">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="62c41-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62c41-239">Search-Flags</span></span>           | <span data-ttu-id="62c41-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62c41-240">0x00000000</span></span>                                     |
| <span data-ttu-id="62c41-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62c41-241">System-Flags</span></span>           | <span data-ttu-id="62c41-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62c41-242">0x00000010</span></span>                                     |
| <span data-ttu-id="62c41-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="62c41-243">Classes used in</span></span>        | [<span data-ttu-id="62c41-244">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="62c41-244">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="62c41-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="62c41-245">Windows Server 2012</span></span>



| <span data-ttu-id="62c41-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="62c41-246">Entry</span></span> | <span data-ttu-id="62c41-247">Value</span><span class="sxs-lookup"><span data-stu-id="62c41-247">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="62c41-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="62c41-248">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="62c41-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62c41-249">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="62c41-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="62c41-250">System-Only</span></span>            | <span data-ttu-id="62c41-251">False</span><span class="sxs-lookup"><span data-stu-id="62c41-251">False</span></span>                                          |
| <span data-ttu-id="62c41-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="62c41-252">Is-Single-Valued</span></span>       | <span data-ttu-id="62c41-253">True</span><span class="sxs-lookup"><span data-stu-id="62c41-253">True</span></span>                                           |
| <span data-ttu-id="62c41-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="62c41-254">Is Indexed</span></span>             | <span data-ttu-id="62c41-255">False</span><span class="sxs-lookup"><span data-stu-id="62c41-255">False</span></span>                                          |
| <span data-ttu-id="62c41-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="62c41-256">In Global Catalog</span></span>      | <span data-ttu-id="62c41-257">True</span><span class="sxs-lookup"><span data-stu-id="62c41-257">True</span></span>                                           |
| <span data-ttu-id="62c41-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="62c41-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="62c41-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="62c41-259">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="62c41-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62c41-260">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="62c41-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62c41-261">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="62c41-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62c41-262">Search-Flags</span></span>           | <span data-ttu-id="62c41-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62c41-263">0x00000000</span></span>                                     |
| <span data-ttu-id="62c41-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62c41-264">System-Flags</span></span>           | <span data-ttu-id="62c41-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62c41-265">0x00000010</span></span>                                     |
| <span data-ttu-id="62c41-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="62c41-266">Classes used in</span></span>        | [<span data-ttu-id="62c41-267">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="62c41-267">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





