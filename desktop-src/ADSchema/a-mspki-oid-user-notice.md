---
title: atributo MS-PKI-OID-User-Notice
description: Aviso de usuario para el OID de la Directiva de emisor Enterprise.
ms.assetid: b7cfc5fd-99d8-4ddd-bc8f-5e5505eb1f1b
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-PKI-OID-User-Notice
- Atributo mspki-OID-User-Notice atributo AD Schema
topic_type:
- apiref
api_name:
- ms-PKI-OID-User-Notice
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115a40f39dc9d6eb8e033435d2803a658edcaacf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659067"
---
# <a name="ms-pki-oid-user-notice-attribute"></a><span data-ttu-id="9b173-105">atributo MS-PKI-OID-User-Notice</span><span class="sxs-lookup"><span data-stu-id="9b173-105">ms-PKI-OID-User-Notice attribute</span></span>

<span data-ttu-id="9b173-106">Aviso de usuario para el OID de la Directiva de emisor Enterprise.</span><span class="sxs-lookup"><span data-stu-id="9b173-106">The user notice for the enterprise issuer policy OID.</span></span>



| <span data-ttu-id="9b173-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b173-107">Entry</span></span> | <span data-ttu-id="9b173-108">Value</span><span class="sxs-lookup"><span data-stu-id="9b173-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b173-109">CN</span><span class="sxs-lookup"><span data-stu-id="9b173-109">CN</span></span>                | <span data-ttu-id="9b173-110">MS-PKI-OID-usuario-aviso</span><span class="sxs-lookup"><span data-stu-id="9b173-110">ms-PKI-OID-User-Notice</span></span>                                                                     |
| <span data-ttu-id="9b173-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="9b173-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9b173-112">Atributo mspki-OID-usuario-aviso</span><span class="sxs-lookup"><span data-stu-id="9b173-112">msPKI-OID-User-Notice</span></span>                                                                      |
| <span data-ttu-id="9b173-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="9b173-113">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="9b173-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="9b173-114">Update Privilege</span></span>  | <span data-ttu-id="9b173-115">Administrador de empresa</span><span class="sxs-lookup"><span data-stu-id="9b173-115">Enterprise administrator</span></span>                                                                   |
| <span data-ttu-id="9b173-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="9b173-116">Update Frequency</span></span>  | <span data-ttu-id="9b173-117">Siempre que se crea una nueva plantilla o se editan los atributos de las plantillas existentes.</span><span class="sxs-lookup"><span data-stu-id="9b173-117">Whenever a new template is created, or the attributes of an existing templates are edited.</span></span> |
| <span data-ttu-id="9b173-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9b173-118">Attribute-Id</span></span>      | <span data-ttu-id="9b173-119">1.2.840.113556.1.4.1673</span><span class="sxs-lookup"><span data-stu-id="9b173-119">1.2.840.113556.1.4.1673</span></span>                                                                    |
| <span data-ttu-id="9b173-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9b173-120">System-Id-Guid</span></span>    | <span data-ttu-id="9b173-121">04c4da7a-e114-4e69-88de-e293f2d3b395</span><span class="sxs-lookup"><span data-stu-id="9b173-121">04c4da7a-e114-4e69-88de-e293f2d3b395</span></span>                                                       |
| <span data-ttu-id="9b173-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b173-122">Syntax</span></span>            | [<span data-ttu-id="9b173-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9b173-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="9b173-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="9b173-124">Implementations</span></span>

-   [<span data-ttu-id="9b173-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9b173-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9b173-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9b173-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9b173-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9b173-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9b173-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9b173-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9b173-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9b173-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9b173-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9b173-130">Windows Server 2003</span></span>



| <span data-ttu-id="9b173-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b173-131">Entry</span></span> | <span data-ttu-id="9b173-132">Value</span><span class="sxs-lookup"><span data-stu-id="9b173-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="9b173-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9b173-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="9b173-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b173-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="9b173-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b173-135">System-Only</span></span>            | <span data-ttu-id="9b173-136">False</span><span class="sxs-lookup"><span data-stu-id="9b173-136">False</span></span>                                                              |
| <span data-ttu-id="9b173-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9b173-137">Is-Single-Valued</span></span>       | <span data-ttu-id="9b173-138">False</span><span class="sxs-lookup"><span data-stu-id="9b173-138">False</span></span>                                                              |
| <span data-ttu-id="9b173-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9b173-139">Is Indexed</span></span>             | <span data-ttu-id="9b173-140">False</span><span class="sxs-lookup"><span data-stu-id="9b173-140">False</span></span>                                                              |
| <span data-ttu-id="9b173-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b173-141">In Global Catalog</span></span>      | <span data-ttu-id="9b173-142">False</span><span class="sxs-lookup"><span data-stu-id="9b173-142">False</span></span>                                                              |
| <span data-ttu-id="9b173-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9b173-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b173-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b173-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="9b173-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b173-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="9b173-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b173-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="9b173-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b173-147">Search-Flags</span></span>           | <span data-ttu-id="9b173-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b173-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="9b173-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b173-149">System-Flags</span></span>           | <span data-ttu-id="9b173-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b173-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="9b173-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9b173-151">Classes used in</span></span>        | [<span data-ttu-id="9b173-152">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="9b173-152">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9b173-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9b173-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9b173-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b173-154">Entry</span></span> | <span data-ttu-id="9b173-155">Value</span><span class="sxs-lookup"><span data-stu-id="9b173-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="9b173-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9b173-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="9b173-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b173-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="9b173-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b173-158">System-Only</span></span>            | <span data-ttu-id="9b173-159">False</span><span class="sxs-lookup"><span data-stu-id="9b173-159">False</span></span>                                                              |
| <span data-ttu-id="9b173-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9b173-160">Is-Single-Valued</span></span>       | <span data-ttu-id="9b173-161">False</span><span class="sxs-lookup"><span data-stu-id="9b173-161">False</span></span>                                                              |
| <span data-ttu-id="9b173-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9b173-162">Is Indexed</span></span>             | <span data-ttu-id="9b173-163">False</span><span class="sxs-lookup"><span data-stu-id="9b173-163">False</span></span>                                                              |
| <span data-ttu-id="9b173-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b173-164">In Global Catalog</span></span>      | <span data-ttu-id="9b173-165">False</span><span class="sxs-lookup"><span data-stu-id="9b173-165">False</span></span>                                                              |
| <span data-ttu-id="9b173-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9b173-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b173-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b173-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="9b173-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b173-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="9b173-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b173-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="9b173-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b173-170">Search-Flags</span></span>           | <span data-ttu-id="9b173-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b173-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="9b173-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b173-172">System-Flags</span></span>           | <span data-ttu-id="9b173-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b173-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="9b173-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9b173-174">Classes used in</span></span>        | [<span data-ttu-id="9b173-175">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="9b173-175">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9b173-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b173-176">Windows Server 2008</span></span>



| <span data-ttu-id="9b173-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b173-177">Entry</span></span> | <span data-ttu-id="9b173-178">Value</span><span class="sxs-lookup"><span data-stu-id="9b173-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="9b173-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9b173-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="9b173-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b173-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="9b173-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b173-181">System-Only</span></span>            | <span data-ttu-id="9b173-182">False</span><span class="sxs-lookup"><span data-stu-id="9b173-182">False</span></span>                                                              |
| <span data-ttu-id="9b173-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9b173-183">Is-Single-Valued</span></span>       | <span data-ttu-id="9b173-184">False</span><span class="sxs-lookup"><span data-stu-id="9b173-184">False</span></span>                                                              |
| <span data-ttu-id="9b173-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9b173-185">Is Indexed</span></span>             | <span data-ttu-id="9b173-186">False</span><span class="sxs-lookup"><span data-stu-id="9b173-186">False</span></span>                                                              |
| <span data-ttu-id="9b173-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b173-187">In Global Catalog</span></span>      | <span data-ttu-id="9b173-188">False</span><span class="sxs-lookup"><span data-stu-id="9b173-188">False</span></span>                                                              |
| <span data-ttu-id="9b173-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9b173-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b173-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b173-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="9b173-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b173-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="9b173-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b173-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="9b173-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b173-193">Search-Flags</span></span>           | <span data-ttu-id="9b173-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b173-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="9b173-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b173-195">System-Flags</span></span>           | <span data-ttu-id="9b173-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b173-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="9b173-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9b173-197">Classes used in</span></span>        | [<span data-ttu-id="9b173-198">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="9b173-198">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9b173-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9b173-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9b173-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b173-200">Entry</span></span> | <span data-ttu-id="9b173-201">Value</span><span class="sxs-lookup"><span data-stu-id="9b173-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="9b173-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9b173-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="9b173-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b173-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="9b173-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b173-204">System-Only</span></span>            | <span data-ttu-id="9b173-205">False</span><span class="sxs-lookup"><span data-stu-id="9b173-205">False</span></span>                                                              |
| <span data-ttu-id="9b173-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9b173-206">Is-Single-Valued</span></span>       | <span data-ttu-id="9b173-207">False</span><span class="sxs-lookup"><span data-stu-id="9b173-207">False</span></span>                                                              |
| <span data-ttu-id="9b173-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9b173-208">Is Indexed</span></span>             | <span data-ttu-id="9b173-209">False</span><span class="sxs-lookup"><span data-stu-id="9b173-209">False</span></span>                                                              |
| <span data-ttu-id="9b173-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b173-210">In Global Catalog</span></span>      | <span data-ttu-id="9b173-211">False</span><span class="sxs-lookup"><span data-stu-id="9b173-211">False</span></span>                                                              |
| <span data-ttu-id="9b173-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9b173-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b173-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b173-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="9b173-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b173-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="9b173-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b173-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="9b173-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b173-216">Search-Flags</span></span>           | <span data-ttu-id="9b173-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b173-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="9b173-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b173-218">System-Flags</span></span>           | <span data-ttu-id="9b173-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b173-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="9b173-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9b173-220">Classes used in</span></span>        | [<span data-ttu-id="9b173-221">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="9b173-221">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9b173-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9b173-222">Windows Server 2012</span></span>



| <span data-ttu-id="9b173-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b173-223">Entry</span></span> | <span data-ttu-id="9b173-224">Value</span><span class="sxs-lookup"><span data-stu-id="9b173-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="9b173-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9b173-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="9b173-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b173-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="9b173-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b173-227">System-Only</span></span>            | <span data-ttu-id="9b173-228">False</span><span class="sxs-lookup"><span data-stu-id="9b173-228">False</span></span>                                                              |
| <span data-ttu-id="9b173-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9b173-229">Is-Single-Valued</span></span>       | <span data-ttu-id="9b173-230">False</span><span class="sxs-lookup"><span data-stu-id="9b173-230">False</span></span>                                                              |
| <span data-ttu-id="9b173-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9b173-231">Is Indexed</span></span>             | <span data-ttu-id="9b173-232">False</span><span class="sxs-lookup"><span data-stu-id="9b173-232">False</span></span>                                                              |
| <span data-ttu-id="9b173-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b173-233">In Global Catalog</span></span>      | <span data-ttu-id="9b173-234">False</span><span class="sxs-lookup"><span data-stu-id="9b173-234">False</span></span>                                                              |
| <span data-ttu-id="9b173-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9b173-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b173-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b173-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="9b173-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b173-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="9b173-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b173-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="9b173-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b173-239">Search-Flags</span></span>           | <span data-ttu-id="9b173-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b173-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="9b173-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b173-241">System-Flags</span></span>           | <span data-ttu-id="9b173-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b173-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="9b173-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9b173-243">Classes used in</span></span>        | [<span data-ttu-id="9b173-244">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="9b173-244">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



 

 





