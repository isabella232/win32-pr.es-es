---
title: Atributo de seguimiento de vínculo-secreto
description: Este atributo almacena un vínculo a una clave secreta que permite traducir un archivo cifrado a texto sin formato.
ms.assetid: e476f4af-71a8-4bd9-a81d-f825bfbf267b
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de seguimiento de vínculo-secreto
- linkTrackSecret esquema de AD de atributos
topic_type:
- apiref
api_name:
- Link-Track-Secret
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb172ec0985acc7c93c62796881c369c7ad0b82
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658628"
---
# <a name="link-track-secret-attribute"></a><span data-ttu-id="0aa78-105">Atributo de seguimiento de vínculo-secreto</span><span class="sxs-lookup"><span data-stu-id="0aa78-105">Link-Track-Secret attribute</span></span>

<span data-ttu-id="0aa78-106">Este atributo almacena un vínculo a una clave secreta que permite traducir un archivo cifrado a texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="0aa78-106">This attribute stores a link to a secret key that allows an encrypted file to be translated to plaintext.</span></span>



| <span data-ttu-id="0aa78-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="0aa78-107">Entry</span></span> | <span data-ttu-id="0aa78-108">Value</span><span class="sxs-lookup"><span data-stu-id="0aa78-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="0aa78-109">CN</span><span class="sxs-lookup"><span data-stu-id="0aa78-109">CN</span></span>                | <span data-ttu-id="0aa78-110">Vínculo-seguimiento-secreto</span><span class="sxs-lookup"><span data-stu-id="0aa78-110">Link-Track-Secret</span></span>                                     |
| <span data-ttu-id="0aa78-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="0aa78-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0aa78-112">linkTrackSecret</span><span class="sxs-lookup"><span data-stu-id="0aa78-112">linkTrackSecret</span></span>                                       |
| <span data-ttu-id="0aa78-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="0aa78-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="0aa78-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="0aa78-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="0aa78-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="0aa78-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="0aa78-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0aa78-116">Attribute-Id</span></span>      | <span data-ttu-id="0aa78-117">1.2.840.113556.1.4.269</span><span class="sxs-lookup"><span data-stu-id="0aa78-117">1.2.840.113556.1.4.269</span></span>                                |
| <span data-ttu-id="0aa78-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0aa78-118">System-Id-Guid</span></span>    | <span data-ttu-id="0aa78-119">2ae80fe2-47b4-11d0-a1a4-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="0aa78-119">2ae80fe2-47b4-11d0-a1a4-00c04fd930c9</span></span>                  |
| <span data-ttu-id="0aa78-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0aa78-120">Syntax</span></span>            | [<span data-ttu-id="0aa78-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="0aa78-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="0aa78-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="0aa78-122">Implementations</span></span>

-   [<span data-ttu-id="0aa78-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0aa78-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0aa78-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0aa78-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0aa78-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0aa78-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0aa78-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0aa78-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0aa78-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0aa78-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0aa78-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0aa78-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0aa78-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0aa78-129">Windows 2000 Server</span></span>



| <span data-ttu-id="0aa78-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="0aa78-130">Entry</span></span> | <span data-ttu-id="0aa78-131">Value</span><span class="sxs-lookup"><span data-stu-id="0aa78-131">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="0aa78-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0aa78-132">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0aa78-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0aa78-133">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0aa78-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="0aa78-134">System-Only</span></span>            | <span data-ttu-id="0aa78-135">False</span><span class="sxs-lookup"><span data-stu-id="0aa78-135">False</span></span>                                                          |
| <span data-ttu-id="0aa78-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0aa78-136">Is-Single-Valued</span></span>       | <span data-ttu-id="0aa78-137">True</span><span class="sxs-lookup"><span data-stu-id="0aa78-137">True</span></span>                                                           |
| <span data-ttu-id="0aa78-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0aa78-138">Is Indexed</span></span>             | <span data-ttu-id="0aa78-139">False</span><span class="sxs-lookup"><span data-stu-id="0aa78-139">False</span></span>                                                          |
| <span data-ttu-id="0aa78-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0aa78-140">In Global Catalog</span></span>      | <span data-ttu-id="0aa78-141">False</span><span class="sxs-lookup"><span data-stu-id="0aa78-141">False</span></span>                                                          |
| <span data-ttu-id="0aa78-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0aa78-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="0aa78-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0aa78-143">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="0aa78-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0aa78-144">Range-Lower</span></span>            | <span data-ttu-id="0aa78-145">0</span><span class="sxs-lookup"><span data-stu-id="0aa78-145">0</span></span>                                                              |
| <span data-ttu-id="0aa78-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0aa78-146">Range-Upper</span></span>            | <span data-ttu-id="0aa78-147">16</span><span class="sxs-lookup"><span data-stu-id="0aa78-147">16</span></span>                                                             |
| <span data-ttu-id="0aa78-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0aa78-148">Search-Flags</span></span>           | <span data-ttu-id="0aa78-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0aa78-149">0x00000000</span></span>                                                     |
| <span data-ttu-id="0aa78-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0aa78-150">System-Flags</span></span>           | <span data-ttu-id="0aa78-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0aa78-151">0x00000010</span></span>                                                     |
| <span data-ttu-id="0aa78-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0aa78-152">Classes used in</span></span>        | [<span data-ttu-id="0aa78-153">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="0aa78-153">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0aa78-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0aa78-154">Windows Server 2003</span></span>



| <span data-ttu-id="0aa78-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="0aa78-155">Entry</span></span> | <span data-ttu-id="0aa78-156">Value</span><span class="sxs-lookup"><span data-stu-id="0aa78-156">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="0aa78-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0aa78-157">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0aa78-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0aa78-158">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0aa78-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="0aa78-159">System-Only</span></span>            | <span data-ttu-id="0aa78-160">False</span><span class="sxs-lookup"><span data-stu-id="0aa78-160">False</span></span>                                                          |
| <span data-ttu-id="0aa78-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0aa78-161">Is-Single-Valued</span></span>       | <span data-ttu-id="0aa78-162">True</span><span class="sxs-lookup"><span data-stu-id="0aa78-162">True</span></span>                                                           |
| <span data-ttu-id="0aa78-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0aa78-163">Is Indexed</span></span>             | <span data-ttu-id="0aa78-164">False</span><span class="sxs-lookup"><span data-stu-id="0aa78-164">False</span></span>                                                          |
| <span data-ttu-id="0aa78-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0aa78-165">In Global Catalog</span></span>      | <span data-ttu-id="0aa78-166">False</span><span class="sxs-lookup"><span data-stu-id="0aa78-166">False</span></span>                                                          |
| <span data-ttu-id="0aa78-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0aa78-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="0aa78-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0aa78-168">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="0aa78-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0aa78-169">Range-Lower</span></span>            | <span data-ttu-id="0aa78-170">0</span><span class="sxs-lookup"><span data-stu-id="0aa78-170">0</span></span>                                                              |
| <span data-ttu-id="0aa78-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0aa78-171">Range-Upper</span></span>            | <span data-ttu-id="0aa78-172">16</span><span class="sxs-lookup"><span data-stu-id="0aa78-172">16</span></span>                                                             |
| <span data-ttu-id="0aa78-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0aa78-173">Search-Flags</span></span>           | <span data-ttu-id="0aa78-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0aa78-174">0x00000000</span></span>                                                     |
| <span data-ttu-id="0aa78-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0aa78-175">System-Flags</span></span>           | <span data-ttu-id="0aa78-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0aa78-176">0x00000010</span></span>                                                     |
| <span data-ttu-id="0aa78-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0aa78-177">Classes used in</span></span>        | [<span data-ttu-id="0aa78-178">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="0aa78-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0aa78-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0aa78-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0aa78-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="0aa78-180">Entry</span></span> | <span data-ttu-id="0aa78-181">Value</span><span class="sxs-lookup"><span data-stu-id="0aa78-181">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="0aa78-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0aa78-182">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0aa78-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0aa78-183">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0aa78-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="0aa78-184">System-Only</span></span>            | <span data-ttu-id="0aa78-185">False</span><span class="sxs-lookup"><span data-stu-id="0aa78-185">False</span></span>                                                          |
| <span data-ttu-id="0aa78-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0aa78-186">Is-Single-Valued</span></span>       | <span data-ttu-id="0aa78-187">True</span><span class="sxs-lookup"><span data-stu-id="0aa78-187">True</span></span>                                                           |
| <span data-ttu-id="0aa78-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0aa78-188">Is Indexed</span></span>             | <span data-ttu-id="0aa78-189">False</span><span class="sxs-lookup"><span data-stu-id="0aa78-189">False</span></span>                                                          |
| <span data-ttu-id="0aa78-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0aa78-190">In Global Catalog</span></span>      | <span data-ttu-id="0aa78-191">False</span><span class="sxs-lookup"><span data-stu-id="0aa78-191">False</span></span>                                                          |
| <span data-ttu-id="0aa78-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0aa78-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="0aa78-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0aa78-193">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="0aa78-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0aa78-194">Range-Lower</span></span>            | <span data-ttu-id="0aa78-195">0</span><span class="sxs-lookup"><span data-stu-id="0aa78-195">0</span></span>                                                              |
| <span data-ttu-id="0aa78-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0aa78-196">Range-Upper</span></span>            | <span data-ttu-id="0aa78-197">16</span><span class="sxs-lookup"><span data-stu-id="0aa78-197">16</span></span>                                                             |
| <span data-ttu-id="0aa78-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0aa78-198">Search-Flags</span></span>           | <span data-ttu-id="0aa78-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0aa78-199">0x00000000</span></span>                                                     |
| <span data-ttu-id="0aa78-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0aa78-200">System-Flags</span></span>           | <span data-ttu-id="0aa78-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0aa78-201">0x00000010</span></span>                                                     |
| <span data-ttu-id="0aa78-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0aa78-202">Classes used in</span></span>        | [<span data-ttu-id="0aa78-203">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="0aa78-203">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0aa78-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0aa78-204">Windows Server 2008</span></span>



| <span data-ttu-id="0aa78-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="0aa78-205">Entry</span></span> | <span data-ttu-id="0aa78-206">Value</span><span class="sxs-lookup"><span data-stu-id="0aa78-206">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="0aa78-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0aa78-207">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0aa78-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0aa78-208">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0aa78-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="0aa78-209">System-Only</span></span>            | <span data-ttu-id="0aa78-210">False</span><span class="sxs-lookup"><span data-stu-id="0aa78-210">False</span></span>                                                          |
| <span data-ttu-id="0aa78-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0aa78-211">Is-Single-Valued</span></span>       | <span data-ttu-id="0aa78-212">True</span><span class="sxs-lookup"><span data-stu-id="0aa78-212">True</span></span>                                                           |
| <span data-ttu-id="0aa78-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0aa78-213">Is Indexed</span></span>             | <span data-ttu-id="0aa78-214">False</span><span class="sxs-lookup"><span data-stu-id="0aa78-214">False</span></span>                                                          |
| <span data-ttu-id="0aa78-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0aa78-215">In Global Catalog</span></span>      | <span data-ttu-id="0aa78-216">False</span><span class="sxs-lookup"><span data-stu-id="0aa78-216">False</span></span>                                                          |
| <span data-ttu-id="0aa78-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0aa78-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="0aa78-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0aa78-218">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="0aa78-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0aa78-219">Range-Lower</span></span>            | <span data-ttu-id="0aa78-220">0</span><span class="sxs-lookup"><span data-stu-id="0aa78-220">0</span></span>                                                              |
| <span data-ttu-id="0aa78-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0aa78-221">Range-Upper</span></span>            | <span data-ttu-id="0aa78-222">16</span><span class="sxs-lookup"><span data-stu-id="0aa78-222">16</span></span>                                                             |
| <span data-ttu-id="0aa78-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0aa78-223">Search-Flags</span></span>           | <span data-ttu-id="0aa78-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0aa78-224">0x00000000</span></span>                                                     |
| <span data-ttu-id="0aa78-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0aa78-225">System-Flags</span></span>           | <span data-ttu-id="0aa78-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0aa78-226">0x00000010</span></span>                                                     |
| <span data-ttu-id="0aa78-227">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0aa78-227">Classes used in</span></span>        | [<span data-ttu-id="0aa78-228">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="0aa78-228">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0aa78-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0aa78-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0aa78-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="0aa78-230">Entry</span></span> | <span data-ttu-id="0aa78-231">Value</span><span class="sxs-lookup"><span data-stu-id="0aa78-231">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="0aa78-232">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0aa78-232">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0aa78-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0aa78-233">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0aa78-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="0aa78-234">System-Only</span></span>            | <span data-ttu-id="0aa78-235">False</span><span class="sxs-lookup"><span data-stu-id="0aa78-235">False</span></span>                                                          |
| <span data-ttu-id="0aa78-236">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0aa78-236">Is-Single-Valued</span></span>       | <span data-ttu-id="0aa78-237">True</span><span class="sxs-lookup"><span data-stu-id="0aa78-237">True</span></span>                                                           |
| <span data-ttu-id="0aa78-238">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0aa78-238">Is Indexed</span></span>             | <span data-ttu-id="0aa78-239">False</span><span class="sxs-lookup"><span data-stu-id="0aa78-239">False</span></span>                                                          |
| <span data-ttu-id="0aa78-240">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0aa78-240">In Global Catalog</span></span>      | <span data-ttu-id="0aa78-241">False</span><span class="sxs-lookup"><span data-stu-id="0aa78-241">False</span></span>                                                          |
| <span data-ttu-id="0aa78-242">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0aa78-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="0aa78-243">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0aa78-243">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="0aa78-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0aa78-244">Range-Lower</span></span>            | <span data-ttu-id="0aa78-245">0</span><span class="sxs-lookup"><span data-stu-id="0aa78-245">0</span></span>                                                              |
| <span data-ttu-id="0aa78-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0aa78-246">Range-Upper</span></span>            | <span data-ttu-id="0aa78-247">16</span><span class="sxs-lookup"><span data-stu-id="0aa78-247">16</span></span>                                                             |
| <span data-ttu-id="0aa78-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0aa78-248">Search-Flags</span></span>           | <span data-ttu-id="0aa78-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0aa78-249">0x00000000</span></span>                                                     |
| <span data-ttu-id="0aa78-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0aa78-250">System-Flags</span></span>           | <span data-ttu-id="0aa78-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0aa78-251">0x00000010</span></span>                                                     |
| <span data-ttu-id="0aa78-252">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0aa78-252">Classes used in</span></span>        | [<span data-ttu-id="0aa78-253">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="0aa78-253">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0aa78-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0aa78-254">Windows Server 2012</span></span>



| <span data-ttu-id="0aa78-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="0aa78-255">Entry</span></span> | <span data-ttu-id="0aa78-256">Value</span><span class="sxs-lookup"><span data-stu-id="0aa78-256">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="0aa78-257">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0aa78-257">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0aa78-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0aa78-258">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="0aa78-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="0aa78-259">System-Only</span></span>            | <span data-ttu-id="0aa78-260">False</span><span class="sxs-lookup"><span data-stu-id="0aa78-260">False</span></span>                                                          |
| <span data-ttu-id="0aa78-261">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0aa78-261">Is-Single-Valued</span></span>       | <span data-ttu-id="0aa78-262">True</span><span class="sxs-lookup"><span data-stu-id="0aa78-262">True</span></span>                                                           |
| <span data-ttu-id="0aa78-263">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0aa78-263">Is Indexed</span></span>             | <span data-ttu-id="0aa78-264">False</span><span class="sxs-lookup"><span data-stu-id="0aa78-264">False</span></span>                                                          |
| <span data-ttu-id="0aa78-265">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0aa78-265">In Global Catalog</span></span>      | <span data-ttu-id="0aa78-266">False</span><span class="sxs-lookup"><span data-stu-id="0aa78-266">False</span></span>                                                          |
| <span data-ttu-id="0aa78-267">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0aa78-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="0aa78-268">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0aa78-268">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="0aa78-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0aa78-269">Range-Lower</span></span>            | <span data-ttu-id="0aa78-270">0</span><span class="sxs-lookup"><span data-stu-id="0aa78-270">0</span></span>                                                              |
| <span data-ttu-id="0aa78-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0aa78-271">Range-Upper</span></span>            | <span data-ttu-id="0aa78-272">16</span><span class="sxs-lookup"><span data-stu-id="0aa78-272">16</span></span>                                                             |
| <span data-ttu-id="0aa78-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0aa78-273">Search-Flags</span></span>           | <span data-ttu-id="0aa78-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0aa78-274">0x00000000</span></span>                                                     |
| <span data-ttu-id="0aa78-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0aa78-275">System-Flags</span></span>           | <span data-ttu-id="0aa78-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0aa78-276">0x00000010</span></span>                                                     |
| <span data-ttu-id="0aa78-277">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0aa78-277">Classes used in</span></span>        | [<span data-ttu-id="0aa78-278">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="0aa78-278">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





