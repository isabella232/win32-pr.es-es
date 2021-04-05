---
title: Atributo comment
description: Comentarios del usuario. Esta cadena puede ser una cadena nula.
ms.assetid: c57493b3-a42a-49ad-8f8c-0afadbb3ba09
ms.tgt_platform: multiple
keywords:
- Atributo de comentario esquema de AD
- atributo de información esquema de AD
topic_type:
- apiref
api_name:
- Comment
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd84674fce08f75c3162628b32f67a75fb8c026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804309"
---
# <a name="comment-attribute-ad-schema"></a><span data-ttu-id="f7487-106">Comment (atributo) (esquema de AD)</span><span class="sxs-lookup"><span data-stu-id="f7487-106">Comment attribute (AD Schema)</span></span>

<span data-ttu-id="f7487-107">Comentarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="f7487-107">The user's comments.</span></span> <span data-ttu-id="f7487-108">Esta cadena puede ser una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="f7487-108">This string can be a null string.</span></span>



| <span data-ttu-id="f7487-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7487-109">Entry</span></span> | <span data-ttu-id="f7487-110">Value</span><span class="sxs-lookup"><span data-stu-id="f7487-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="f7487-111">CN</span><span class="sxs-lookup"><span data-stu-id="f7487-111">CN</span></span>                | <span data-ttu-id="f7487-112">Comentario</span><span class="sxs-lookup"><span data-stu-id="f7487-112">Comment</span></span>                                                                  |
| <span data-ttu-id="f7487-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="f7487-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f7487-114">info</span><span class="sxs-lookup"><span data-stu-id="f7487-114">info</span></span>                                                                     |
| <span data-ttu-id="f7487-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f7487-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="f7487-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="f7487-116">Update Privilege</span></span>  | <span data-ttu-id="f7487-117">Administrador de dominio o propietario de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="f7487-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="f7487-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="f7487-118">Update Frequency</span></span>  | <span data-ttu-id="f7487-119">Siempre que el usuario o el administrador necesite agregar comentarios en la cuenta.</span><span class="sxs-lookup"><span data-stu-id="f7487-119">Whenever the user or administrator needs to add comments on the account.</span></span> |
| <span data-ttu-id="f7487-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f7487-120">Attribute-Id</span></span>      | <span data-ttu-id="f7487-121">1.2.840.113556.1.2.81</span><span class="sxs-lookup"><span data-stu-id="f7487-121">1.2.840.113556.1.2.81</span></span>                                                    |
| <span data-ttu-id="f7487-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f7487-122">System-Id-Guid</span></span>    | <span data-ttu-id="f7487-123">bf96793e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f7487-123">bf96793e-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="f7487-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7487-124">Syntax</span></span>            | [<span data-ttu-id="f7487-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f7487-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="f7487-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="f7487-126">Implementations</span></span>

-   [<span data-ttu-id="f7487-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f7487-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f7487-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f7487-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f7487-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f7487-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f7487-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f7487-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f7487-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f7487-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f7487-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f7487-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f7487-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f7487-133">Windows 2000 Server</span></span>



| <span data-ttu-id="f7487-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7487-134">Entry</span></span> | <span data-ttu-id="f7487-135">Value</span><span class="sxs-lookup"><span data-stu-id="f7487-135">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f7487-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f7487-136">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f7487-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7487-137">MAPI-Id</span></span>                | <span data-ttu-id="f7487-138">0x3004</span><span class="sxs-lookup"><span data-stu-id="f7487-138">0x3004</span></span>                                               |
| <span data-ttu-id="f7487-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7487-139">System-Only</span></span>            | <span data-ttu-id="f7487-140">False</span><span class="sxs-lookup"><span data-stu-id="f7487-140">False</span></span>                                                |
| <span data-ttu-id="f7487-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f7487-141">Is-Single-Valued</span></span>       | <span data-ttu-id="f7487-142">True</span><span class="sxs-lookup"><span data-stu-id="f7487-142">True</span></span>                                                 |
| <span data-ttu-id="f7487-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f7487-143">Is Indexed</span></span>             | <span data-ttu-id="f7487-144">False</span><span class="sxs-lookup"><span data-stu-id="f7487-144">False</span></span>                                                |
| <span data-ttu-id="f7487-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7487-145">In Global Catalog</span></span>      | <span data-ttu-id="f7487-146">False</span><span class="sxs-lookup"><span data-stu-id="f7487-146">False</span></span>                                                |
| <span data-ttu-id="f7487-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f7487-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7487-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7487-148">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f7487-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7487-149">Range-Lower</span></span>            | <span data-ttu-id="f7487-150">1</span><span class="sxs-lookup"><span data-stu-id="f7487-150">1</span></span>                                                    |
| <span data-ttu-id="f7487-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7487-151">Range-Upper</span></span>            | <span data-ttu-id="f7487-152">1024</span><span class="sxs-lookup"><span data-stu-id="f7487-152">1024</span></span>                                                 |
| <span data-ttu-id="f7487-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7487-153">Search-Flags</span></span>           | <span data-ttu-id="f7487-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7487-154">0x00000000</span></span>                                           |
| <span data-ttu-id="f7487-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7487-155">System-Flags</span></span>           | <span data-ttu-id="f7487-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7487-156">0x00000010</span></span>                                           |
| <span data-ttu-id="f7487-157">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f7487-157">Classes used in</span></span>        | [<span data-ttu-id="f7487-158">**Destinatario de correo**</span><span class="sxs-lookup"><span data-stu-id="f7487-158">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f7487-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f7487-159">Windows Server 2003</span></span>



| <span data-ttu-id="f7487-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7487-160">Entry</span></span> | <span data-ttu-id="f7487-161">Value</span><span class="sxs-lookup"><span data-stu-id="f7487-161">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f7487-162">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f7487-162">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f7487-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7487-163">MAPI-Id</span></span>                | <span data-ttu-id="f7487-164">0x3004</span><span class="sxs-lookup"><span data-stu-id="f7487-164">0x3004</span></span>                                               |
| <span data-ttu-id="f7487-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7487-165">System-Only</span></span>            | <span data-ttu-id="f7487-166">False</span><span class="sxs-lookup"><span data-stu-id="f7487-166">False</span></span>                                                |
| <span data-ttu-id="f7487-167">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f7487-167">Is-Single-Valued</span></span>       | <span data-ttu-id="f7487-168">True</span><span class="sxs-lookup"><span data-stu-id="f7487-168">True</span></span>                                                 |
| <span data-ttu-id="f7487-169">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f7487-169">Is Indexed</span></span>             | <span data-ttu-id="f7487-170">False</span><span class="sxs-lookup"><span data-stu-id="f7487-170">False</span></span>                                                |
| <span data-ttu-id="f7487-171">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7487-171">In Global Catalog</span></span>      | <span data-ttu-id="f7487-172">False</span><span class="sxs-lookup"><span data-stu-id="f7487-172">False</span></span>                                                |
| <span data-ttu-id="f7487-173">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f7487-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7487-174">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7487-174">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f7487-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7487-175">Range-Lower</span></span>            | <span data-ttu-id="f7487-176">1</span><span class="sxs-lookup"><span data-stu-id="f7487-176">1</span></span>                                                    |
| <span data-ttu-id="f7487-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7487-177">Range-Upper</span></span>            | <span data-ttu-id="f7487-178">1024</span><span class="sxs-lookup"><span data-stu-id="f7487-178">1024</span></span>                                                 |
| <span data-ttu-id="f7487-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7487-179">Search-Flags</span></span>           | <span data-ttu-id="f7487-180">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7487-180">0x00000000</span></span>                                           |
| <span data-ttu-id="f7487-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7487-181">System-Flags</span></span>           | <span data-ttu-id="f7487-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7487-182">0x00000010</span></span>                                           |
| <span data-ttu-id="f7487-183">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f7487-183">Classes used in</span></span>        | [<span data-ttu-id="f7487-184">**Destinatario de correo**</span><span class="sxs-lookup"><span data-stu-id="f7487-184">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f7487-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f7487-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f7487-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7487-186">Entry</span></span> | <span data-ttu-id="f7487-187">Value</span><span class="sxs-lookup"><span data-stu-id="f7487-187">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f7487-188">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f7487-188">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f7487-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7487-189">MAPI-Id</span></span>                | <span data-ttu-id="f7487-190">0x3004</span><span class="sxs-lookup"><span data-stu-id="f7487-190">0x3004</span></span>                                               |
| <span data-ttu-id="f7487-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7487-191">System-Only</span></span>            | <span data-ttu-id="f7487-192">False</span><span class="sxs-lookup"><span data-stu-id="f7487-192">False</span></span>                                                |
| <span data-ttu-id="f7487-193">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f7487-193">Is-Single-Valued</span></span>       | <span data-ttu-id="f7487-194">True</span><span class="sxs-lookup"><span data-stu-id="f7487-194">True</span></span>                                                 |
| <span data-ttu-id="f7487-195">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f7487-195">Is Indexed</span></span>             | <span data-ttu-id="f7487-196">False</span><span class="sxs-lookup"><span data-stu-id="f7487-196">False</span></span>                                                |
| <span data-ttu-id="f7487-197">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7487-197">In Global Catalog</span></span>      | <span data-ttu-id="f7487-198">False</span><span class="sxs-lookup"><span data-stu-id="f7487-198">False</span></span>                                                |
| <span data-ttu-id="f7487-199">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f7487-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7487-200">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7487-200">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f7487-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7487-201">Range-Lower</span></span>            | <span data-ttu-id="f7487-202">1</span><span class="sxs-lookup"><span data-stu-id="f7487-202">1</span></span>                                                    |
| <span data-ttu-id="f7487-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7487-203">Range-Upper</span></span>            | <span data-ttu-id="f7487-204">1024</span><span class="sxs-lookup"><span data-stu-id="f7487-204">1024</span></span>                                                 |
| <span data-ttu-id="f7487-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7487-205">Search-Flags</span></span>           | <span data-ttu-id="f7487-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7487-206">0x00000000</span></span>                                           |
| <span data-ttu-id="f7487-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7487-207">System-Flags</span></span>           | <span data-ttu-id="f7487-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7487-208">0x00000010</span></span>                                           |
| <span data-ttu-id="f7487-209">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f7487-209">Classes used in</span></span>        | [<span data-ttu-id="f7487-210">**Destinatario de correo**</span><span class="sxs-lookup"><span data-stu-id="f7487-210">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f7487-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7487-211">Windows Server 2008</span></span>



| <span data-ttu-id="f7487-212">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7487-212">Entry</span></span> | <span data-ttu-id="f7487-213">Value</span><span class="sxs-lookup"><span data-stu-id="f7487-213">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f7487-214">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f7487-214">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f7487-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7487-215">MAPI-Id</span></span>                | <span data-ttu-id="f7487-216">0x3004</span><span class="sxs-lookup"><span data-stu-id="f7487-216">0x3004</span></span>                                               |
| <span data-ttu-id="f7487-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7487-217">System-Only</span></span>            | <span data-ttu-id="f7487-218">False</span><span class="sxs-lookup"><span data-stu-id="f7487-218">False</span></span>                                                |
| <span data-ttu-id="f7487-219">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f7487-219">Is-Single-Valued</span></span>       | <span data-ttu-id="f7487-220">True</span><span class="sxs-lookup"><span data-stu-id="f7487-220">True</span></span>                                                 |
| <span data-ttu-id="f7487-221">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f7487-221">Is Indexed</span></span>             | <span data-ttu-id="f7487-222">False</span><span class="sxs-lookup"><span data-stu-id="f7487-222">False</span></span>                                                |
| <span data-ttu-id="f7487-223">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7487-223">In Global Catalog</span></span>      | <span data-ttu-id="f7487-224">False</span><span class="sxs-lookup"><span data-stu-id="f7487-224">False</span></span>                                                |
| <span data-ttu-id="f7487-225">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f7487-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7487-226">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7487-226">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f7487-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7487-227">Range-Lower</span></span>            | <span data-ttu-id="f7487-228">1</span><span class="sxs-lookup"><span data-stu-id="f7487-228">1</span></span>                                                    |
| <span data-ttu-id="f7487-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7487-229">Range-Upper</span></span>            | <span data-ttu-id="f7487-230">1024</span><span class="sxs-lookup"><span data-stu-id="f7487-230">1024</span></span>                                                 |
| <span data-ttu-id="f7487-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7487-231">Search-Flags</span></span>           | <span data-ttu-id="f7487-232">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7487-232">0x00000000</span></span>                                           |
| <span data-ttu-id="f7487-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7487-233">System-Flags</span></span>           | <span data-ttu-id="f7487-234">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7487-234">0x00000010</span></span>                                           |
| <span data-ttu-id="f7487-235">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f7487-235">Classes used in</span></span>        | [<span data-ttu-id="f7487-236">**Destinatario de correo**</span><span class="sxs-lookup"><span data-stu-id="f7487-236">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f7487-237">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f7487-237">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f7487-238">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7487-238">Entry</span></span> | <span data-ttu-id="f7487-239">Value</span><span class="sxs-lookup"><span data-stu-id="f7487-239">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f7487-240">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f7487-240">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f7487-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7487-241">MAPI-Id</span></span>                | <span data-ttu-id="f7487-242">0x3004</span><span class="sxs-lookup"><span data-stu-id="f7487-242">0x3004</span></span>                                               |
| <span data-ttu-id="f7487-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7487-243">System-Only</span></span>            | <span data-ttu-id="f7487-244">False</span><span class="sxs-lookup"><span data-stu-id="f7487-244">False</span></span>                                                |
| <span data-ttu-id="f7487-245">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f7487-245">Is-Single-Valued</span></span>       | <span data-ttu-id="f7487-246">True</span><span class="sxs-lookup"><span data-stu-id="f7487-246">True</span></span>                                                 |
| <span data-ttu-id="f7487-247">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f7487-247">Is Indexed</span></span>             | <span data-ttu-id="f7487-248">False</span><span class="sxs-lookup"><span data-stu-id="f7487-248">False</span></span>                                                |
| <span data-ttu-id="f7487-249">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7487-249">In Global Catalog</span></span>      | <span data-ttu-id="f7487-250">False</span><span class="sxs-lookup"><span data-stu-id="f7487-250">False</span></span>                                                |
| <span data-ttu-id="f7487-251">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f7487-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7487-252">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7487-252">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f7487-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7487-253">Range-Lower</span></span>            | <span data-ttu-id="f7487-254">1</span><span class="sxs-lookup"><span data-stu-id="f7487-254">1</span></span>                                                    |
| <span data-ttu-id="f7487-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7487-255">Range-Upper</span></span>            | <span data-ttu-id="f7487-256">1024</span><span class="sxs-lookup"><span data-stu-id="f7487-256">1024</span></span>                                                 |
| <span data-ttu-id="f7487-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7487-257">Search-Flags</span></span>           | <span data-ttu-id="f7487-258">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7487-258">0x00000000</span></span>                                           |
| <span data-ttu-id="f7487-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7487-259">System-Flags</span></span>           | <span data-ttu-id="f7487-260">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7487-260">0x00000010</span></span>                                           |
| <span data-ttu-id="f7487-261">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f7487-261">Classes used in</span></span>        | [<span data-ttu-id="f7487-262">**Destinatario de correo**</span><span class="sxs-lookup"><span data-stu-id="f7487-262">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f7487-263">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f7487-263">Windows Server 2012</span></span>



| <span data-ttu-id="f7487-264">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7487-264">Entry</span></span> | <span data-ttu-id="f7487-265">Value</span><span class="sxs-lookup"><span data-stu-id="f7487-265">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f7487-266">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f7487-266">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f7487-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7487-267">MAPI-Id</span></span>                | <span data-ttu-id="f7487-268">0x3004</span><span class="sxs-lookup"><span data-stu-id="f7487-268">0x3004</span></span>                                               |
| <span data-ttu-id="f7487-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7487-269">System-Only</span></span>            | <span data-ttu-id="f7487-270">False</span><span class="sxs-lookup"><span data-stu-id="f7487-270">False</span></span>                                                |
| <span data-ttu-id="f7487-271">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f7487-271">Is-Single-Valued</span></span>       | <span data-ttu-id="f7487-272">True</span><span class="sxs-lookup"><span data-stu-id="f7487-272">True</span></span>                                                 |
| <span data-ttu-id="f7487-273">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f7487-273">Is Indexed</span></span>             | <span data-ttu-id="f7487-274">False</span><span class="sxs-lookup"><span data-stu-id="f7487-274">False</span></span>                                                |
| <span data-ttu-id="f7487-275">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7487-275">In Global Catalog</span></span>      | <span data-ttu-id="f7487-276">False</span><span class="sxs-lookup"><span data-stu-id="f7487-276">False</span></span>                                                |
| <span data-ttu-id="f7487-277">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f7487-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7487-278">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7487-278">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f7487-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7487-279">Range-Lower</span></span>            | <span data-ttu-id="f7487-280">1</span><span class="sxs-lookup"><span data-stu-id="f7487-280">1</span></span>                                                    |
| <span data-ttu-id="f7487-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7487-281">Range-Upper</span></span>            | <span data-ttu-id="f7487-282">1024</span><span class="sxs-lookup"><span data-stu-id="f7487-282">1024</span></span>                                                 |
| <span data-ttu-id="f7487-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7487-283">Search-Flags</span></span>           | <span data-ttu-id="f7487-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7487-284">0x00000000</span></span>                                           |
| <span data-ttu-id="f7487-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7487-285">System-Flags</span></span>           | <span data-ttu-id="f7487-286">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7487-286">0x00000010</span></span>                                           |
| <span data-ttu-id="f7487-287">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f7487-287">Classes used in</span></span>        | [<span data-ttu-id="f7487-288">**Destinatario de correo**</span><span class="sxs-lookup"><span data-stu-id="f7487-288">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 





