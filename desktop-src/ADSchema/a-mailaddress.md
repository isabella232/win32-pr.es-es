---
title: SMTP-correo-dirección (atributo)
description: Atributo de dirección de correo genérico. Se usa en el cuadro como atributo opcional de objetos de servidor, donde lo consume la replicación DS basada en correo (si los equipos están configurados).
ms.assetid: 54fd710c-d140-4d46-9db3-0c72fb5fb08c
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de dirección de correo SMTP
- Esquema de AD del atributo mailAddress
topic_type:
- apiref
api_name:
- SMTP-Mail-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e1828c59af346ab5a5741aaa03358b711484089
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151468"
---
# <a name="smtp-mail-address-attribute"></a><span data-ttu-id="82adf-106">SMTP-correo-dirección (atributo)</span><span class="sxs-lookup"><span data-stu-id="82adf-106">SMTP-Mail-Address attribute</span></span>

<span data-ttu-id="82adf-107">Atributo de dirección de correo genérico.</span><span class="sxs-lookup"><span data-stu-id="82adf-107">Generic mail address attribute.</span></span> <span data-ttu-id="82adf-108">Se usa en el cuadro como atributo opcional de objetos de servidor, donde lo consume la replicación DS basada en correo (si los equipos están configurados).</span><span class="sxs-lookup"><span data-stu-id="82adf-108">Used in the box as an optional attribute of server objects, where it is consumed by mail-based DS replication (if the computers are so configured).</span></span>



| <span data-ttu-id="82adf-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="82adf-109">Entry</span></span> | <span data-ttu-id="82adf-110">Value</span><span class="sxs-lookup"><span data-stu-id="82adf-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="82adf-111">CN</span><span class="sxs-lookup"><span data-stu-id="82adf-111">CN</span></span>                | <span data-ttu-id="82adf-112">SMTP-dirección de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="82adf-112">SMTP-Mail-Address</span></span>                           |
| <span data-ttu-id="82adf-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="82adf-113">Ldap-Display-Name</span></span> | <span data-ttu-id="82adf-114">mailAddress</span><span class="sxs-lookup"><span data-stu-id="82adf-114">mailAddress</span></span>                                 |
| <span data-ttu-id="82adf-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="82adf-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="82adf-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="82adf-116">Update Privilege</span></span>  | <span data-ttu-id="82adf-117">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="82adf-117">Domain administrator</span></span>                        |
| <span data-ttu-id="82adf-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="82adf-118">Update Frequency</span></span>  | <span data-ttu-id="82adf-119">Casi nunca</span><span class="sxs-lookup"><span data-stu-id="82adf-119">Almost never</span></span>                                |
| <span data-ttu-id="82adf-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="82adf-120">Attribute-Id</span></span>      | <span data-ttu-id="82adf-121">1.2.840.113556.1.4.786</span><span class="sxs-lookup"><span data-stu-id="82adf-121">1.2.840.113556.1.4.786</span></span>                      |
| <span data-ttu-id="82adf-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="82adf-122">System-Id-Guid</span></span>    | <span data-ttu-id="82adf-123">26d9736f-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="82adf-123">26d9736f-6070-11d1-a9c6-0000f80367c1</span></span>        |
| <span data-ttu-id="82adf-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82adf-124">Syntax</span></span>            | [<span data-ttu-id="82adf-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="82adf-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="82adf-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="82adf-126">Implementations</span></span>

-   [<span data-ttu-id="82adf-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="82adf-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="82adf-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="82adf-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="82adf-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="82adf-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="82adf-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="82adf-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="82adf-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="82adf-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="82adf-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="82adf-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="82adf-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="82adf-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="82adf-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="82adf-134">Windows 2000 Server</span></span>



| <span data-ttu-id="82adf-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="82adf-135">Entry</span></span> | <span data-ttu-id="82adf-136">Value</span><span class="sxs-lookup"><span data-stu-id="82adf-136">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="82adf-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="82adf-137">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="82adf-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82adf-138">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="82adf-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="82adf-139">System-Only</span></span>            | <span data-ttu-id="82adf-140">False</span><span class="sxs-lookup"><span data-stu-id="82adf-140">False</span></span>                                 |
| <span data-ttu-id="82adf-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="82adf-141">Is-Single-Valued</span></span>       | <span data-ttu-id="82adf-142">True</span><span class="sxs-lookup"><span data-stu-id="82adf-142">True</span></span>                                  |
| <span data-ttu-id="82adf-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="82adf-143">Is Indexed</span></span>             | <span data-ttu-id="82adf-144">False</span><span class="sxs-lookup"><span data-stu-id="82adf-144">False</span></span>                                 |
| <span data-ttu-id="82adf-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="82adf-145">In Global Catalog</span></span>      | <span data-ttu-id="82adf-146">False</span><span class="sxs-lookup"><span data-stu-id="82adf-146">False</span></span>                                 |
| <span data-ttu-id="82adf-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="82adf-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="82adf-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82adf-148">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="82adf-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82adf-149">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="82adf-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82adf-150">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="82adf-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82adf-151">Search-Flags</span></span>           | <span data-ttu-id="82adf-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82adf-152">0x00000000</span></span>                            |
| <span data-ttu-id="82adf-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82adf-153">System-Flags</span></span>           | <span data-ttu-id="82adf-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82adf-154">0x00000010</span></span>                            |
| <span data-ttu-id="82adf-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="82adf-155">Classes used in</span></span>        | [<span data-ttu-id="82adf-156">**Server**</span><span class="sxs-lookup"><span data-stu-id="82adf-156">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="82adf-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="82adf-157">Windows Server 2003</span></span>



| <span data-ttu-id="82adf-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="82adf-158">Entry</span></span> | <span data-ttu-id="82adf-159">Value</span><span class="sxs-lookup"><span data-stu-id="82adf-159">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="82adf-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="82adf-160">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="82adf-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82adf-161">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="82adf-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="82adf-162">System-Only</span></span>            | <span data-ttu-id="82adf-163">False</span><span class="sxs-lookup"><span data-stu-id="82adf-163">False</span></span>                                 |
| <span data-ttu-id="82adf-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="82adf-164">Is-Single-Valued</span></span>       | <span data-ttu-id="82adf-165">True</span><span class="sxs-lookup"><span data-stu-id="82adf-165">True</span></span>                                  |
| <span data-ttu-id="82adf-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="82adf-166">Is Indexed</span></span>             | <span data-ttu-id="82adf-167">False</span><span class="sxs-lookup"><span data-stu-id="82adf-167">False</span></span>                                 |
| <span data-ttu-id="82adf-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="82adf-168">In Global Catalog</span></span>      | <span data-ttu-id="82adf-169">False</span><span class="sxs-lookup"><span data-stu-id="82adf-169">False</span></span>                                 |
| <span data-ttu-id="82adf-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="82adf-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="82adf-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82adf-171">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="82adf-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82adf-172">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="82adf-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82adf-173">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="82adf-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82adf-174">Search-Flags</span></span>           | <span data-ttu-id="82adf-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82adf-175">0x00000000</span></span>                            |
| <span data-ttu-id="82adf-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82adf-176">System-Flags</span></span>           | <span data-ttu-id="82adf-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82adf-177">0x00000010</span></span>                            |
| <span data-ttu-id="82adf-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="82adf-178">Classes used in</span></span>        | [<span data-ttu-id="82adf-179">**Server**</span><span class="sxs-lookup"><span data-stu-id="82adf-179">**Server**</span></span>](c-server.md)<br/> |



## <a name="adam"></a><span data-ttu-id="82adf-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="82adf-180">ADAM</span></span>



| <span data-ttu-id="82adf-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="82adf-181">Entry</span></span> | <span data-ttu-id="82adf-182">Value</span><span class="sxs-lookup"><span data-stu-id="82adf-182">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="82adf-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="82adf-183">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="82adf-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82adf-184">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="82adf-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="82adf-185">System-Only</span></span>            | <span data-ttu-id="82adf-186">False</span><span class="sxs-lookup"><span data-stu-id="82adf-186">False</span></span>                                 |
| <span data-ttu-id="82adf-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="82adf-187">Is-Single-Valued</span></span>       | <span data-ttu-id="82adf-188">True</span><span class="sxs-lookup"><span data-stu-id="82adf-188">True</span></span>                                  |
| <span data-ttu-id="82adf-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="82adf-189">Is Indexed</span></span>             | <span data-ttu-id="82adf-190">False</span><span class="sxs-lookup"><span data-stu-id="82adf-190">False</span></span>                                 |
| <span data-ttu-id="82adf-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="82adf-191">In Global Catalog</span></span>      | <span data-ttu-id="82adf-192">False</span><span class="sxs-lookup"><span data-stu-id="82adf-192">False</span></span>                                 |
| <span data-ttu-id="82adf-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="82adf-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="82adf-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82adf-194">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="82adf-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82adf-195">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="82adf-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82adf-196">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="82adf-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82adf-197">Search-Flags</span></span>           | <span data-ttu-id="82adf-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82adf-198">0x00000000</span></span>                            |
| <span data-ttu-id="82adf-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82adf-199">System-Flags</span></span>           | <span data-ttu-id="82adf-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82adf-200">0x00000010</span></span>                            |
| <span data-ttu-id="82adf-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="82adf-201">Classes used in</span></span>        | [<span data-ttu-id="82adf-202">**Server**</span><span class="sxs-lookup"><span data-stu-id="82adf-202">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="82adf-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="82adf-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="82adf-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="82adf-204">Entry</span></span> | <span data-ttu-id="82adf-205">Value</span><span class="sxs-lookup"><span data-stu-id="82adf-205">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="82adf-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="82adf-206">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="82adf-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82adf-207">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="82adf-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="82adf-208">System-Only</span></span>            | <span data-ttu-id="82adf-209">False</span><span class="sxs-lookup"><span data-stu-id="82adf-209">False</span></span>                                 |
| <span data-ttu-id="82adf-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="82adf-210">Is-Single-Valued</span></span>       | <span data-ttu-id="82adf-211">True</span><span class="sxs-lookup"><span data-stu-id="82adf-211">True</span></span>                                  |
| <span data-ttu-id="82adf-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="82adf-212">Is Indexed</span></span>             | <span data-ttu-id="82adf-213">False</span><span class="sxs-lookup"><span data-stu-id="82adf-213">False</span></span>                                 |
| <span data-ttu-id="82adf-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="82adf-214">In Global Catalog</span></span>      | <span data-ttu-id="82adf-215">False</span><span class="sxs-lookup"><span data-stu-id="82adf-215">False</span></span>                                 |
| <span data-ttu-id="82adf-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="82adf-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="82adf-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82adf-217">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="82adf-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82adf-218">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="82adf-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82adf-219">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="82adf-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82adf-220">Search-Flags</span></span>           | <span data-ttu-id="82adf-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82adf-221">0x00000000</span></span>                            |
| <span data-ttu-id="82adf-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82adf-222">System-Flags</span></span>           | <span data-ttu-id="82adf-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82adf-223">0x00000010</span></span>                            |
| <span data-ttu-id="82adf-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="82adf-224">Classes used in</span></span>        | [<span data-ttu-id="82adf-225">**Server**</span><span class="sxs-lookup"><span data-stu-id="82adf-225">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="82adf-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82adf-226">Windows Server 2008</span></span>



| <span data-ttu-id="82adf-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="82adf-227">Entry</span></span> | <span data-ttu-id="82adf-228">Value</span><span class="sxs-lookup"><span data-stu-id="82adf-228">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="82adf-229">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="82adf-229">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="82adf-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82adf-230">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="82adf-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="82adf-231">System-Only</span></span>            | <span data-ttu-id="82adf-232">False</span><span class="sxs-lookup"><span data-stu-id="82adf-232">False</span></span>                                 |
| <span data-ttu-id="82adf-233">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="82adf-233">Is-Single-Valued</span></span>       | <span data-ttu-id="82adf-234">True</span><span class="sxs-lookup"><span data-stu-id="82adf-234">True</span></span>                                  |
| <span data-ttu-id="82adf-235">Está indexado</span><span class="sxs-lookup"><span data-stu-id="82adf-235">Is Indexed</span></span>             | <span data-ttu-id="82adf-236">False</span><span class="sxs-lookup"><span data-stu-id="82adf-236">False</span></span>                                 |
| <span data-ttu-id="82adf-237">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="82adf-237">In Global Catalog</span></span>      | <span data-ttu-id="82adf-238">False</span><span class="sxs-lookup"><span data-stu-id="82adf-238">False</span></span>                                 |
| <span data-ttu-id="82adf-239">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="82adf-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="82adf-240">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82adf-240">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="82adf-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82adf-241">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="82adf-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82adf-242">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="82adf-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82adf-243">Search-Flags</span></span>           | <span data-ttu-id="82adf-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82adf-244">0x00000000</span></span>                            |
| <span data-ttu-id="82adf-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82adf-245">System-Flags</span></span>           | <span data-ttu-id="82adf-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82adf-246">0x00000010</span></span>                            |
| <span data-ttu-id="82adf-247">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="82adf-247">Classes used in</span></span>        | [<span data-ttu-id="82adf-248">**Server**</span><span class="sxs-lookup"><span data-stu-id="82adf-248">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="82adf-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="82adf-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="82adf-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="82adf-250">Entry</span></span> | <span data-ttu-id="82adf-251">Value</span><span class="sxs-lookup"><span data-stu-id="82adf-251">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="82adf-252">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="82adf-252">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="82adf-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82adf-253">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="82adf-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="82adf-254">System-Only</span></span>            | <span data-ttu-id="82adf-255">False</span><span class="sxs-lookup"><span data-stu-id="82adf-255">False</span></span>                                 |
| <span data-ttu-id="82adf-256">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="82adf-256">Is-Single-Valued</span></span>       | <span data-ttu-id="82adf-257">True</span><span class="sxs-lookup"><span data-stu-id="82adf-257">True</span></span>                                  |
| <span data-ttu-id="82adf-258">Está indexado</span><span class="sxs-lookup"><span data-stu-id="82adf-258">Is Indexed</span></span>             | <span data-ttu-id="82adf-259">False</span><span class="sxs-lookup"><span data-stu-id="82adf-259">False</span></span>                                 |
| <span data-ttu-id="82adf-260">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="82adf-260">In Global Catalog</span></span>      | <span data-ttu-id="82adf-261">False</span><span class="sxs-lookup"><span data-stu-id="82adf-261">False</span></span>                                 |
| <span data-ttu-id="82adf-262">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="82adf-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="82adf-263">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82adf-263">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="82adf-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82adf-264">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="82adf-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82adf-265">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="82adf-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82adf-266">Search-Flags</span></span>           | <span data-ttu-id="82adf-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82adf-267">0x00000000</span></span>                            |
| <span data-ttu-id="82adf-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82adf-268">System-Flags</span></span>           | <span data-ttu-id="82adf-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82adf-269">0x00000010</span></span>                            |
| <span data-ttu-id="82adf-270">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="82adf-270">Classes used in</span></span>        | [<span data-ttu-id="82adf-271">**Server**</span><span class="sxs-lookup"><span data-stu-id="82adf-271">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="82adf-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="82adf-272">Windows Server 2012</span></span>



| <span data-ttu-id="82adf-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="82adf-273">Entry</span></span> | <span data-ttu-id="82adf-274">Value</span><span class="sxs-lookup"><span data-stu-id="82adf-274">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="82adf-275">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="82adf-275">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="82adf-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82adf-276">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="82adf-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="82adf-277">System-Only</span></span>            | <span data-ttu-id="82adf-278">False</span><span class="sxs-lookup"><span data-stu-id="82adf-278">False</span></span>                                 |
| <span data-ttu-id="82adf-279">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="82adf-279">Is-Single-Valued</span></span>       | <span data-ttu-id="82adf-280">True</span><span class="sxs-lookup"><span data-stu-id="82adf-280">True</span></span>                                  |
| <span data-ttu-id="82adf-281">Está indexado</span><span class="sxs-lookup"><span data-stu-id="82adf-281">Is Indexed</span></span>             | <span data-ttu-id="82adf-282">False</span><span class="sxs-lookup"><span data-stu-id="82adf-282">False</span></span>                                 |
| <span data-ttu-id="82adf-283">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="82adf-283">In Global Catalog</span></span>      | <span data-ttu-id="82adf-284">False</span><span class="sxs-lookup"><span data-stu-id="82adf-284">False</span></span>                                 |
| <span data-ttu-id="82adf-285">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="82adf-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="82adf-286">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82adf-286">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="82adf-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82adf-287">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="82adf-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82adf-288">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="82adf-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82adf-289">Search-Flags</span></span>           | <span data-ttu-id="82adf-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82adf-290">0x00000000</span></span>                            |
| <span data-ttu-id="82adf-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82adf-291">System-Flags</span></span>           | <span data-ttu-id="82adf-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82adf-292">0x00000010</span></span>                            |
| <span data-ttu-id="82adf-293">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="82adf-293">Classes used in</span></span>        | [<span data-ttu-id="82adf-294">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="82adf-294">**Server**</span></span>](c-server.md)<br/> |



 

 





