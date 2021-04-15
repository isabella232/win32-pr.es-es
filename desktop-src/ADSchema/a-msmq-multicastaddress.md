---
title: Atributo MSMQ-Multicast-Address
description: Esto forma parte de un objeto MSMQ, se establece mediante una llamada a la API a MQCreateQueue o MQSetProperties. Controla si MSMQ aceptará mensajes de una dirección de multidifusión.
ms.assetid: 65622cc9-81d9-42c6-b208-cac703f32244
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de dirección de multidifusión de MSMQ
- Esquema de AD de atributo de MSMQ-MulticastAddress
topic_type:
- apiref
api_name:
- MSMQ-Multicast-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b90543c40e22d8dd5fdc2b3e5195bd9382357
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535979"
---
# <a name="msmq-multicast-address-attribute"></a><span data-ttu-id="6d637-106">Atributo MSMQ-Multicast-Address</span><span class="sxs-lookup"><span data-stu-id="6d637-106">MSMQ-Multicast-Address attribute</span></span>

<span data-ttu-id="6d637-107">Esto forma parte de un objeto MSMQ, se establece mediante una llamada a la API a MQCreateQueue o MQSetProperties.</span><span class="sxs-lookup"><span data-stu-id="6d637-107">This is part of an MSMQ object, it is set by calling API to MQCreateQueue or MQSetProperties.</span></span> <span data-ttu-id="6d637-108">Controla si MSMQ aceptará mensajes de una dirección de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="6d637-108">It controls whether MSMQ will accept messages from a multicast address.</span></span>



| <span data-ttu-id="6d637-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d637-109">Entry</span></span> | <span data-ttu-id="6d637-110">Value</span><span class="sxs-lookup"><span data-stu-id="6d637-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6d637-111">CN</span><span class="sxs-lookup"><span data-stu-id="6d637-111">CN</span></span>                | <span data-ttu-id="6d637-112">MSMQ-multidifusión-dirección</span><span class="sxs-lookup"><span data-stu-id="6d637-112">MSMQ-Multicast-Address</span></span>                      |
| <span data-ttu-id="6d637-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="6d637-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6d637-114">MSMQ-MulticastAddress</span><span class="sxs-lookup"><span data-stu-id="6d637-114">MSMQ-MulticastAddress</span></span>                       |
| <span data-ttu-id="6d637-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="6d637-115">Size</span></span>              | <span data-ttu-id="6d637-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="6d637-116">4 bytes</span></span>                                     |
| <span data-ttu-id="6d637-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="6d637-117">Update Privilege</span></span>  | <span data-ttu-id="6d637-118">Propietario de la cola.</span><span class="sxs-lookup"><span data-stu-id="6d637-118">The queue owner.</span></span>                            |
| <span data-ttu-id="6d637-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="6d637-119">Update Frequency</span></span>  | <span data-ttu-id="6d637-120">Cuando se crea una cola.</span><span class="sxs-lookup"><span data-stu-id="6d637-120">When a queue is created.</span></span>                    |
| <span data-ttu-id="6d637-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6d637-121">Attribute-Id</span></span>      | <span data-ttu-id="6d637-122">1.2.840.113556.1.4.1714</span><span class="sxs-lookup"><span data-stu-id="6d637-122">1.2.840.113556.1.4.1714</span></span>                     |
| <span data-ttu-id="6d637-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6d637-123">System-Id-Guid</span></span>    | <span data-ttu-id="6d637-124">1d2f4412-f10d-4337-9b48-6e5b125cd265</span><span class="sxs-lookup"><span data-stu-id="6d637-124">1d2f4412-f10d-4337-9b48-6e5b125cd265</span></span>        |
| <span data-ttu-id="6d637-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d637-125">Syntax</span></span>            | [<span data-ttu-id="6d637-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6d637-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6d637-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="6d637-127">Implementations</span></span>

-   [<span data-ttu-id="6d637-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6d637-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6d637-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6d637-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6d637-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6d637-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6d637-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6d637-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6d637-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6d637-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="6d637-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6d637-133">Windows Server 2003</span></span>



| <span data-ttu-id="6d637-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d637-134">Entry</span></span> | <span data-ttu-id="6d637-135">Value</span><span class="sxs-lookup"><span data-stu-id="6d637-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6d637-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6d637-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d637-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d637-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d637-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d637-138">System-Only</span></span>            | <span data-ttu-id="6d637-139">False</span><span class="sxs-lookup"><span data-stu-id="6d637-139">False</span></span>                                        |
| <span data-ttu-id="6d637-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6d637-140">Is-Single-Valued</span></span>       | <span data-ttu-id="6d637-141">True</span><span class="sxs-lookup"><span data-stu-id="6d637-141">True</span></span>                                         |
| <span data-ttu-id="6d637-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6d637-142">Is Indexed</span></span>             | <span data-ttu-id="6d637-143">False</span><span class="sxs-lookup"><span data-stu-id="6d637-143">False</span></span>                                        |
| <span data-ttu-id="6d637-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6d637-144">In Global Catalog</span></span>      | <span data-ttu-id="6d637-145">True</span><span class="sxs-lookup"><span data-stu-id="6d637-145">True</span></span>                                         |
| <span data-ttu-id="6d637-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6d637-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d637-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d637-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6d637-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d637-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6d637-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d637-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6d637-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d637-150">Search-Flags</span></span>           | <span data-ttu-id="6d637-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d637-151">0x00000000</span></span>                                   |
| <span data-ttu-id="6d637-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d637-152">System-Flags</span></span>           | <span data-ttu-id="6d637-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d637-153">0x00000010</span></span>                                   |
| <span data-ttu-id="6d637-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6d637-154">Classes used in</span></span>        | [<span data-ttu-id="6d637-155">**MSMQ-cola**</span><span class="sxs-lookup"><span data-stu-id="6d637-155">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6d637-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6d637-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6d637-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d637-157">Entry</span></span> | <span data-ttu-id="6d637-158">Value</span><span class="sxs-lookup"><span data-stu-id="6d637-158">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6d637-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6d637-159">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d637-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d637-160">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d637-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d637-161">System-Only</span></span>            | <span data-ttu-id="6d637-162">False</span><span class="sxs-lookup"><span data-stu-id="6d637-162">False</span></span>                                        |
| <span data-ttu-id="6d637-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6d637-163">Is-Single-Valued</span></span>       | <span data-ttu-id="6d637-164">True</span><span class="sxs-lookup"><span data-stu-id="6d637-164">True</span></span>                                         |
| <span data-ttu-id="6d637-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6d637-165">Is Indexed</span></span>             | <span data-ttu-id="6d637-166">False</span><span class="sxs-lookup"><span data-stu-id="6d637-166">False</span></span>                                        |
| <span data-ttu-id="6d637-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6d637-167">In Global Catalog</span></span>      | <span data-ttu-id="6d637-168">True</span><span class="sxs-lookup"><span data-stu-id="6d637-168">True</span></span>                                         |
| <span data-ttu-id="6d637-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6d637-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d637-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d637-170">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6d637-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d637-171">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6d637-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d637-172">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6d637-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d637-173">Search-Flags</span></span>           | <span data-ttu-id="6d637-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d637-174">0x00000000</span></span>                                   |
| <span data-ttu-id="6d637-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d637-175">System-Flags</span></span>           | <span data-ttu-id="6d637-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d637-176">0x00000010</span></span>                                   |
| <span data-ttu-id="6d637-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6d637-177">Classes used in</span></span>        | [<span data-ttu-id="6d637-178">**MSMQ-cola**</span><span class="sxs-lookup"><span data-stu-id="6d637-178">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6d637-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d637-179">Windows Server 2008</span></span>



| <span data-ttu-id="6d637-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d637-180">Entry</span></span> | <span data-ttu-id="6d637-181">Value</span><span class="sxs-lookup"><span data-stu-id="6d637-181">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6d637-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6d637-182">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d637-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d637-183">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d637-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d637-184">System-Only</span></span>            | <span data-ttu-id="6d637-185">False</span><span class="sxs-lookup"><span data-stu-id="6d637-185">False</span></span>                                        |
| <span data-ttu-id="6d637-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6d637-186">Is-Single-Valued</span></span>       | <span data-ttu-id="6d637-187">True</span><span class="sxs-lookup"><span data-stu-id="6d637-187">True</span></span>                                         |
| <span data-ttu-id="6d637-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6d637-188">Is Indexed</span></span>             | <span data-ttu-id="6d637-189">False</span><span class="sxs-lookup"><span data-stu-id="6d637-189">False</span></span>                                        |
| <span data-ttu-id="6d637-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6d637-190">In Global Catalog</span></span>      | <span data-ttu-id="6d637-191">True</span><span class="sxs-lookup"><span data-stu-id="6d637-191">True</span></span>                                         |
| <span data-ttu-id="6d637-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6d637-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d637-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d637-193">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6d637-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d637-194">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6d637-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d637-195">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6d637-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d637-196">Search-Flags</span></span>           | <span data-ttu-id="6d637-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d637-197">0x00000000</span></span>                                   |
| <span data-ttu-id="6d637-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d637-198">System-Flags</span></span>           | <span data-ttu-id="6d637-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d637-199">0x00000010</span></span>                                   |
| <span data-ttu-id="6d637-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6d637-200">Classes used in</span></span>        | [<span data-ttu-id="6d637-201">**MSMQ-cola**</span><span class="sxs-lookup"><span data-stu-id="6d637-201">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6d637-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6d637-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6d637-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d637-203">Entry</span></span> | <span data-ttu-id="6d637-204">Value</span><span class="sxs-lookup"><span data-stu-id="6d637-204">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6d637-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6d637-205">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d637-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d637-206">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d637-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d637-207">System-Only</span></span>            | <span data-ttu-id="6d637-208">False</span><span class="sxs-lookup"><span data-stu-id="6d637-208">False</span></span>                                        |
| <span data-ttu-id="6d637-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6d637-209">Is-Single-Valued</span></span>       | <span data-ttu-id="6d637-210">True</span><span class="sxs-lookup"><span data-stu-id="6d637-210">True</span></span>                                         |
| <span data-ttu-id="6d637-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6d637-211">Is Indexed</span></span>             | <span data-ttu-id="6d637-212">False</span><span class="sxs-lookup"><span data-stu-id="6d637-212">False</span></span>                                        |
| <span data-ttu-id="6d637-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6d637-213">In Global Catalog</span></span>      | <span data-ttu-id="6d637-214">True</span><span class="sxs-lookup"><span data-stu-id="6d637-214">True</span></span>                                         |
| <span data-ttu-id="6d637-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6d637-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d637-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d637-216">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6d637-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d637-217">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6d637-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d637-218">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6d637-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d637-219">Search-Flags</span></span>           | <span data-ttu-id="6d637-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d637-220">0x00000000</span></span>                                   |
| <span data-ttu-id="6d637-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d637-221">System-Flags</span></span>           | <span data-ttu-id="6d637-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d637-222">0x00000010</span></span>                                   |
| <span data-ttu-id="6d637-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6d637-223">Classes used in</span></span>        | [<span data-ttu-id="6d637-224">**MSMQ-cola**</span><span class="sxs-lookup"><span data-stu-id="6d637-224">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6d637-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6d637-225">Windows Server 2012</span></span>



| <span data-ttu-id="6d637-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d637-226">Entry</span></span> | <span data-ttu-id="6d637-227">Value</span><span class="sxs-lookup"><span data-stu-id="6d637-227">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6d637-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6d637-228">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d637-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d637-229">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d637-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d637-230">System-Only</span></span>            | <span data-ttu-id="6d637-231">False</span><span class="sxs-lookup"><span data-stu-id="6d637-231">False</span></span>                                        |
| <span data-ttu-id="6d637-232">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6d637-232">Is-Single-Valued</span></span>       | <span data-ttu-id="6d637-233">True</span><span class="sxs-lookup"><span data-stu-id="6d637-233">True</span></span>                                         |
| <span data-ttu-id="6d637-234">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6d637-234">Is Indexed</span></span>             | <span data-ttu-id="6d637-235">False</span><span class="sxs-lookup"><span data-stu-id="6d637-235">False</span></span>                                        |
| <span data-ttu-id="6d637-236">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6d637-236">In Global Catalog</span></span>      | <span data-ttu-id="6d637-237">True</span><span class="sxs-lookup"><span data-stu-id="6d637-237">True</span></span>                                         |
| <span data-ttu-id="6d637-238">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6d637-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d637-239">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d637-239">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6d637-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d637-240">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6d637-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d637-241">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6d637-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d637-242">Search-Flags</span></span>           | <span data-ttu-id="6d637-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d637-243">0x00000000</span></span>                                   |
| <span data-ttu-id="6d637-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d637-244">System-Flags</span></span>           | <span data-ttu-id="6d637-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d637-245">0x00000010</span></span>                                   |
| <span data-ttu-id="6d637-246">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6d637-246">Classes used in</span></span>        | [<span data-ttu-id="6d637-247">**MSMQ-cola**</span><span class="sxs-lookup"><span data-stu-id="6d637-247">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





