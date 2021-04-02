---
title: Atributo MSMQ-recipient-FormatName
description: Se utiliza como nombre de formato de destinatario en la clase MSMQ-Custom-Recipient.
ms.assetid: 26ee4cec-4e69-412e-914b-437f2f4cd88e
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MSMQ-recipient-FormatName
- Esquema de AD del atributo msMQ-recipient-FormatName
topic_type:
- apiref
api_name:
- MSMQ-Recipient-FormatName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57fbeee49ddf0c734212bc91926e5c848a9e8d1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151795"
---
# <a name="msmq-recipient-formatname-attribute"></a><span data-ttu-id="20a72-105">Atributo MSMQ-recipient-FormatName</span><span class="sxs-lookup"><span data-stu-id="20a72-105">MSMQ-Recipient-FormatName attribute</span></span>

<span data-ttu-id="20a72-106">Se utiliza como nombre de formato de destinatario en la clase MSMQ-Custom-Recipient.</span><span class="sxs-lookup"><span data-stu-id="20a72-106">Used as the recipient format name in the MSMQ-Custom-Recipient class.</span></span>



| <span data-ttu-id="20a72-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="20a72-107">Entry</span></span> | <span data-ttu-id="20a72-108">Value</span><span class="sxs-lookup"><span data-stu-id="20a72-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="20a72-109">CN</span><span class="sxs-lookup"><span data-stu-id="20a72-109">CN</span></span>                | <span data-ttu-id="20a72-110">MSMQ-recipient-FormatName</span><span class="sxs-lookup"><span data-stu-id="20a72-110">MSMQ-Recipient-FormatName</span></span>                   |
| <span data-ttu-id="20a72-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="20a72-111">Ldap-Display-Name</span></span> | <span data-ttu-id="20a72-112">msMQ-recipient-FormatName</span><span class="sxs-lookup"><span data-stu-id="20a72-112">msMQ-Recipient-FormatName</span></span>                   |
| <span data-ttu-id="20a72-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="20a72-113">Size</span></span>              | <span data-ttu-id="20a72-114">1 a 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="20a72-114">1 to 255 characters.</span></span>                        |
| <span data-ttu-id="20a72-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="20a72-115">Update Privilege</span></span>  | <span data-ttu-id="20a72-116">Propietario de la cola.</span><span class="sxs-lookup"><span data-stu-id="20a72-116">The queue owner.</span></span>                            |
| <span data-ttu-id="20a72-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="20a72-117">Update Frequency</span></span>  | <span data-ttu-id="20a72-118">Solo después de que se moviera la cola externa.</span><span class="sxs-lookup"><span data-stu-id="20a72-118">Only after the external queue was moved.</span></span>    |
| <span data-ttu-id="20a72-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="20a72-119">Attribute-Id</span></span>      | <span data-ttu-id="20a72-120">1.2.840.113556.1.4.1695</span><span class="sxs-lookup"><span data-stu-id="20a72-120">1.2.840.113556.1.4.1695</span></span>                     |
| <span data-ttu-id="20a72-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="20a72-121">System-Id-Guid</span></span>    | <span data-ttu-id="20a72-122">3bfe6748-b544-485a-b067-1b310c4334bf</span><span class="sxs-lookup"><span data-stu-id="20a72-122">3bfe6748-b544-485a-b067-1b310c4334bf</span></span>        |
| <span data-ttu-id="20a72-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20a72-123">Syntax</span></span>            | [<span data-ttu-id="20a72-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="20a72-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="20a72-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="20a72-125">Implementations</span></span>

-   [<span data-ttu-id="20a72-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="20a72-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="20a72-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="20a72-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="20a72-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="20a72-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="20a72-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="20a72-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="20a72-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="20a72-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="20a72-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="20a72-131">Windows Server 2003</span></span>



| <span data-ttu-id="20a72-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="20a72-132">Entry</span></span> | <span data-ttu-id="20a72-133">Value</span><span class="sxs-lookup"><span data-stu-id="20a72-133">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="20a72-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="20a72-134">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="20a72-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="20a72-135">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="20a72-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="20a72-136">System-Only</span></span>            | <span data-ttu-id="20a72-137">False</span><span class="sxs-lookup"><span data-stu-id="20a72-137">False</span></span>                                                               |
| <span data-ttu-id="20a72-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="20a72-138">Is-Single-Valued</span></span>       | <span data-ttu-id="20a72-139">True</span><span class="sxs-lookup"><span data-stu-id="20a72-139">True</span></span>                                                                |
| <span data-ttu-id="20a72-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="20a72-140">Is Indexed</span></span>             | <span data-ttu-id="20a72-141">False</span><span class="sxs-lookup"><span data-stu-id="20a72-141">False</span></span>                                                               |
| <span data-ttu-id="20a72-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="20a72-142">In Global Catalog</span></span>      | <span data-ttu-id="20a72-143">False</span><span class="sxs-lookup"><span data-stu-id="20a72-143">False</span></span>                                                               |
| <span data-ttu-id="20a72-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="20a72-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="20a72-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="20a72-145">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="20a72-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="20a72-146">Range-Lower</span></span>            | <span data-ttu-id="20a72-147">1</span><span class="sxs-lookup"><span data-stu-id="20a72-147">1</span></span>                                                                   |
| <span data-ttu-id="20a72-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="20a72-148">Range-Upper</span></span>            | <span data-ttu-id="20a72-149">255</span><span class="sxs-lookup"><span data-stu-id="20a72-149">255</span></span>                                                                 |
| <span data-ttu-id="20a72-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="20a72-150">Search-Flags</span></span>           | <span data-ttu-id="20a72-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="20a72-151">0x00000000</span></span>                                                          |
| <span data-ttu-id="20a72-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="20a72-152">System-Flags</span></span>           | <span data-ttu-id="20a72-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="20a72-153">0x00000010</span></span>                                                          |
| <span data-ttu-id="20a72-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="20a72-154">Classes used in</span></span>        | [<span data-ttu-id="20a72-155">**MSMQ-Custom-recipient**</span><span class="sxs-lookup"><span data-stu-id="20a72-155">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="20a72-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="20a72-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="20a72-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="20a72-157">Entry</span></span> | <span data-ttu-id="20a72-158">Value</span><span class="sxs-lookup"><span data-stu-id="20a72-158">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="20a72-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="20a72-159">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="20a72-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="20a72-160">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="20a72-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="20a72-161">System-Only</span></span>            | <span data-ttu-id="20a72-162">False</span><span class="sxs-lookup"><span data-stu-id="20a72-162">False</span></span>                                                               |
| <span data-ttu-id="20a72-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="20a72-163">Is-Single-Valued</span></span>       | <span data-ttu-id="20a72-164">True</span><span class="sxs-lookup"><span data-stu-id="20a72-164">True</span></span>                                                                |
| <span data-ttu-id="20a72-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="20a72-165">Is Indexed</span></span>             | <span data-ttu-id="20a72-166">False</span><span class="sxs-lookup"><span data-stu-id="20a72-166">False</span></span>                                                               |
| <span data-ttu-id="20a72-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="20a72-167">In Global Catalog</span></span>      | <span data-ttu-id="20a72-168">False</span><span class="sxs-lookup"><span data-stu-id="20a72-168">False</span></span>                                                               |
| <span data-ttu-id="20a72-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="20a72-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="20a72-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="20a72-170">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="20a72-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="20a72-171">Range-Lower</span></span>            | <span data-ttu-id="20a72-172">1</span><span class="sxs-lookup"><span data-stu-id="20a72-172">1</span></span>                                                                   |
| <span data-ttu-id="20a72-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="20a72-173">Range-Upper</span></span>            | <span data-ttu-id="20a72-174">255</span><span class="sxs-lookup"><span data-stu-id="20a72-174">255</span></span>                                                                 |
| <span data-ttu-id="20a72-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="20a72-175">Search-Flags</span></span>           | <span data-ttu-id="20a72-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="20a72-176">0x00000000</span></span>                                                          |
| <span data-ttu-id="20a72-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="20a72-177">System-Flags</span></span>           | <span data-ttu-id="20a72-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="20a72-178">0x00000010</span></span>                                                          |
| <span data-ttu-id="20a72-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="20a72-179">Classes used in</span></span>        | [<span data-ttu-id="20a72-180">**MSMQ-Custom-recipient**</span><span class="sxs-lookup"><span data-stu-id="20a72-180">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="20a72-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20a72-181">Windows Server 2008</span></span>



| <span data-ttu-id="20a72-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="20a72-182">Entry</span></span> | <span data-ttu-id="20a72-183">Value</span><span class="sxs-lookup"><span data-stu-id="20a72-183">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="20a72-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="20a72-184">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="20a72-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="20a72-185">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="20a72-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="20a72-186">System-Only</span></span>            | <span data-ttu-id="20a72-187">False</span><span class="sxs-lookup"><span data-stu-id="20a72-187">False</span></span>                                                               |
| <span data-ttu-id="20a72-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="20a72-188">Is-Single-Valued</span></span>       | <span data-ttu-id="20a72-189">True</span><span class="sxs-lookup"><span data-stu-id="20a72-189">True</span></span>                                                                |
| <span data-ttu-id="20a72-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="20a72-190">Is Indexed</span></span>             | <span data-ttu-id="20a72-191">False</span><span class="sxs-lookup"><span data-stu-id="20a72-191">False</span></span>                                                               |
| <span data-ttu-id="20a72-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="20a72-192">In Global Catalog</span></span>      | <span data-ttu-id="20a72-193">False</span><span class="sxs-lookup"><span data-stu-id="20a72-193">False</span></span>                                                               |
| <span data-ttu-id="20a72-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="20a72-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="20a72-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="20a72-195">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="20a72-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="20a72-196">Range-Lower</span></span>            | <span data-ttu-id="20a72-197">1</span><span class="sxs-lookup"><span data-stu-id="20a72-197">1</span></span>                                                                   |
| <span data-ttu-id="20a72-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="20a72-198">Range-Upper</span></span>            | <span data-ttu-id="20a72-199">255</span><span class="sxs-lookup"><span data-stu-id="20a72-199">255</span></span>                                                                 |
| <span data-ttu-id="20a72-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="20a72-200">Search-Flags</span></span>           | <span data-ttu-id="20a72-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="20a72-201">0x00000000</span></span>                                                          |
| <span data-ttu-id="20a72-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="20a72-202">System-Flags</span></span>           | <span data-ttu-id="20a72-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="20a72-203">0x00000010</span></span>                                                          |
| <span data-ttu-id="20a72-204">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="20a72-204">Classes used in</span></span>        | [<span data-ttu-id="20a72-205">**MSMQ-Custom-recipient**</span><span class="sxs-lookup"><span data-stu-id="20a72-205">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="20a72-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="20a72-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="20a72-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="20a72-207">Entry</span></span> | <span data-ttu-id="20a72-208">Value</span><span class="sxs-lookup"><span data-stu-id="20a72-208">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="20a72-209">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="20a72-209">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="20a72-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="20a72-210">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="20a72-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="20a72-211">System-Only</span></span>            | <span data-ttu-id="20a72-212">False</span><span class="sxs-lookup"><span data-stu-id="20a72-212">False</span></span>                                                               |
| <span data-ttu-id="20a72-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="20a72-213">Is-Single-Valued</span></span>       | <span data-ttu-id="20a72-214">True</span><span class="sxs-lookup"><span data-stu-id="20a72-214">True</span></span>                                                                |
| <span data-ttu-id="20a72-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="20a72-215">Is Indexed</span></span>             | <span data-ttu-id="20a72-216">False</span><span class="sxs-lookup"><span data-stu-id="20a72-216">False</span></span>                                                               |
| <span data-ttu-id="20a72-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="20a72-217">In Global Catalog</span></span>      | <span data-ttu-id="20a72-218">False</span><span class="sxs-lookup"><span data-stu-id="20a72-218">False</span></span>                                                               |
| <span data-ttu-id="20a72-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="20a72-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="20a72-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="20a72-220">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="20a72-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="20a72-221">Range-Lower</span></span>            | <span data-ttu-id="20a72-222">1</span><span class="sxs-lookup"><span data-stu-id="20a72-222">1</span></span>                                                                   |
| <span data-ttu-id="20a72-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="20a72-223">Range-Upper</span></span>            | <span data-ttu-id="20a72-224">255</span><span class="sxs-lookup"><span data-stu-id="20a72-224">255</span></span>                                                                 |
| <span data-ttu-id="20a72-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="20a72-225">Search-Flags</span></span>           | <span data-ttu-id="20a72-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="20a72-226">0x00000000</span></span>                                                          |
| <span data-ttu-id="20a72-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="20a72-227">System-Flags</span></span>           | <span data-ttu-id="20a72-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="20a72-228">0x00000010</span></span>                                                          |
| <span data-ttu-id="20a72-229">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="20a72-229">Classes used in</span></span>        | [<span data-ttu-id="20a72-230">**MSMQ-Custom-recipient**</span><span class="sxs-lookup"><span data-stu-id="20a72-230">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="20a72-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="20a72-231">Windows Server 2012</span></span>



| <span data-ttu-id="20a72-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="20a72-232">Entry</span></span> | <span data-ttu-id="20a72-233">Value</span><span class="sxs-lookup"><span data-stu-id="20a72-233">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="20a72-234">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="20a72-234">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="20a72-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="20a72-235">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="20a72-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="20a72-236">System-Only</span></span>            | <span data-ttu-id="20a72-237">False</span><span class="sxs-lookup"><span data-stu-id="20a72-237">False</span></span>                                                               |
| <span data-ttu-id="20a72-238">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="20a72-238">Is-Single-Valued</span></span>       | <span data-ttu-id="20a72-239">True</span><span class="sxs-lookup"><span data-stu-id="20a72-239">True</span></span>                                                                |
| <span data-ttu-id="20a72-240">Está indexado</span><span class="sxs-lookup"><span data-stu-id="20a72-240">Is Indexed</span></span>             | <span data-ttu-id="20a72-241">False</span><span class="sxs-lookup"><span data-stu-id="20a72-241">False</span></span>                                                               |
| <span data-ttu-id="20a72-242">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="20a72-242">In Global Catalog</span></span>      | <span data-ttu-id="20a72-243">False</span><span class="sxs-lookup"><span data-stu-id="20a72-243">False</span></span>                                                               |
| <span data-ttu-id="20a72-244">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="20a72-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="20a72-245">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="20a72-245">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="20a72-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="20a72-246">Range-Lower</span></span>            | <span data-ttu-id="20a72-247">1</span><span class="sxs-lookup"><span data-stu-id="20a72-247">1</span></span>                                                                   |
| <span data-ttu-id="20a72-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="20a72-248">Range-Upper</span></span>            | <span data-ttu-id="20a72-249">255</span><span class="sxs-lookup"><span data-stu-id="20a72-249">255</span></span>                                                                 |
| <span data-ttu-id="20a72-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="20a72-250">Search-Flags</span></span>           | <span data-ttu-id="20a72-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="20a72-251">0x00000000</span></span>                                                          |
| <span data-ttu-id="20a72-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="20a72-252">System-Flags</span></span>           | <span data-ttu-id="20a72-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="20a72-253">0x00000010</span></span>                                                          |
| <span data-ttu-id="20a72-254">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="20a72-254">Classes used in</span></span>        | [<span data-ttu-id="20a72-255">**MSMQ-Custom-recipient**</span><span class="sxs-lookup"><span data-stu-id="20a72-255">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



 

 





