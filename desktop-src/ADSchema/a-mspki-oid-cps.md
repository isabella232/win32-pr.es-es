---
title: atributo MS-PKI-OID-CPS
description: La CPS (declaración de directiva de certificados) para el OID de la Directiva de emisor Enterprise.
ms.assetid: 94c5115e-a8d2-49d1-9fd2-f362e95550dc
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MS-PKI-OID-CPS
- Atributo mspki-OID-esquema de AD de atributos de CPS
topic_type:
- apiref
api_name:
- ms-PKI-OID-CPS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 218fc0eabe7311f46dba769f84b972a495138d3a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905990"
---
# <a name="ms-pki-oid-cps-attribute"></a><span data-ttu-id="134d3-105">atributo MS-PKI-OID-CPS</span><span class="sxs-lookup"><span data-stu-id="134d3-105">ms-PKI-OID-CPS attribute</span></span>

<span data-ttu-id="134d3-106">La CPS (declaración de directiva de certificados) para el OID de la Directiva de emisor Enterprise.</span><span class="sxs-lookup"><span data-stu-id="134d3-106">The CPS (Certificate Policy Statement) for the enterprise issuer policy OID.</span></span>



| <span data-ttu-id="134d3-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="134d3-107">Entry</span></span> | <span data-ttu-id="134d3-108">Value</span><span class="sxs-lookup"><span data-stu-id="134d3-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="134d3-109">CN</span><span class="sxs-lookup"><span data-stu-id="134d3-109">CN</span></span>                | <span data-ttu-id="134d3-110">MS-PKI-OID-CPS</span><span class="sxs-lookup"><span data-stu-id="134d3-110">ms-PKI-OID-CPS</span></span>                                                                             |
| <span data-ttu-id="134d3-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="134d3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="134d3-112">Atributo mspki-OID-CPS</span><span class="sxs-lookup"><span data-stu-id="134d3-112">msPKI-OID-CPS</span></span>                                                                              |
| <span data-ttu-id="134d3-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="134d3-113">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="134d3-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="134d3-114">Update Privilege</span></span>  | <span data-ttu-id="134d3-115">Administrador de empresa</span><span class="sxs-lookup"><span data-stu-id="134d3-115">Enterprise administrator</span></span>                                                                   |
| <span data-ttu-id="134d3-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="134d3-116">Update Frequency</span></span>  | <span data-ttu-id="134d3-117">Siempre que se crea una nueva plantilla o se editan los atributos de las plantillas existentes.</span><span class="sxs-lookup"><span data-stu-id="134d3-117">Whenever a new template is created, or the attributes of an existing templates are edited.</span></span> |
| <span data-ttu-id="134d3-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="134d3-118">Attribute-Id</span></span>      | <span data-ttu-id="134d3-119">1.2.840.113556.1.4.1672</span><span class="sxs-lookup"><span data-stu-id="134d3-119">1.2.840.113556.1.4.1672</span></span>                                                                    |
| <span data-ttu-id="134d3-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="134d3-120">System-Id-Guid</span></span>    | <span data-ttu-id="134d3-121">5f49940e-a79f-4a51-bb6f-3d446a54dc6b</span><span class="sxs-lookup"><span data-stu-id="134d3-121">5f49940e-a79f-4a51-bb6f-3d446a54dc6b</span></span>                                                       |
| <span data-ttu-id="134d3-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="134d3-122">Syntax</span></span>            | [<span data-ttu-id="134d3-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="134d3-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="134d3-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="134d3-124">Implementations</span></span>

-   [<span data-ttu-id="134d3-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="134d3-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="134d3-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="134d3-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="134d3-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="134d3-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="134d3-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="134d3-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="134d3-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="134d3-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="134d3-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="134d3-130">Windows Server 2003</span></span>



| <span data-ttu-id="134d3-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="134d3-131">Entry</span></span> | <span data-ttu-id="134d3-132">Value</span><span class="sxs-lookup"><span data-stu-id="134d3-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="134d3-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="134d3-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="134d3-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="134d3-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="134d3-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="134d3-135">System-Only</span></span>            | <span data-ttu-id="134d3-136">False</span><span class="sxs-lookup"><span data-stu-id="134d3-136">False</span></span>                                                              |
| <span data-ttu-id="134d3-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="134d3-137">Is-Single-Valued</span></span>       | <span data-ttu-id="134d3-138">False</span><span class="sxs-lookup"><span data-stu-id="134d3-138">False</span></span>                                                              |
| <span data-ttu-id="134d3-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="134d3-139">Is Indexed</span></span>             | <span data-ttu-id="134d3-140">False</span><span class="sxs-lookup"><span data-stu-id="134d3-140">False</span></span>                                                              |
| <span data-ttu-id="134d3-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="134d3-141">In Global Catalog</span></span>      | <span data-ttu-id="134d3-142">False</span><span class="sxs-lookup"><span data-stu-id="134d3-142">False</span></span>                                                              |
| <span data-ttu-id="134d3-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="134d3-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="134d3-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="134d3-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="134d3-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="134d3-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="134d3-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="134d3-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="134d3-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="134d3-147">Search-Flags</span></span>           | <span data-ttu-id="134d3-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="134d3-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="134d3-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="134d3-149">System-Flags</span></span>           | <span data-ttu-id="134d3-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="134d3-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="134d3-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="134d3-151">Classes used in</span></span>        | [<span data-ttu-id="134d3-152">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="134d3-152">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="134d3-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="134d3-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="134d3-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="134d3-154">Entry</span></span> | <span data-ttu-id="134d3-155">Value</span><span class="sxs-lookup"><span data-stu-id="134d3-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="134d3-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="134d3-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="134d3-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="134d3-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="134d3-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="134d3-158">System-Only</span></span>            | <span data-ttu-id="134d3-159">False</span><span class="sxs-lookup"><span data-stu-id="134d3-159">False</span></span>                                                              |
| <span data-ttu-id="134d3-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="134d3-160">Is-Single-Valued</span></span>       | <span data-ttu-id="134d3-161">False</span><span class="sxs-lookup"><span data-stu-id="134d3-161">False</span></span>                                                              |
| <span data-ttu-id="134d3-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="134d3-162">Is Indexed</span></span>             | <span data-ttu-id="134d3-163">False</span><span class="sxs-lookup"><span data-stu-id="134d3-163">False</span></span>                                                              |
| <span data-ttu-id="134d3-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="134d3-164">In Global Catalog</span></span>      | <span data-ttu-id="134d3-165">False</span><span class="sxs-lookup"><span data-stu-id="134d3-165">False</span></span>                                                              |
| <span data-ttu-id="134d3-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="134d3-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="134d3-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="134d3-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="134d3-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="134d3-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="134d3-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="134d3-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="134d3-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="134d3-170">Search-Flags</span></span>           | <span data-ttu-id="134d3-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="134d3-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="134d3-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="134d3-172">System-Flags</span></span>           | <span data-ttu-id="134d3-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="134d3-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="134d3-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="134d3-174">Classes used in</span></span>        | [<span data-ttu-id="134d3-175">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="134d3-175">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="134d3-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="134d3-176">Windows Server 2008</span></span>



| <span data-ttu-id="134d3-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="134d3-177">Entry</span></span> | <span data-ttu-id="134d3-178">Value</span><span class="sxs-lookup"><span data-stu-id="134d3-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="134d3-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="134d3-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="134d3-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="134d3-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="134d3-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="134d3-181">System-Only</span></span>            | <span data-ttu-id="134d3-182">False</span><span class="sxs-lookup"><span data-stu-id="134d3-182">False</span></span>                                                              |
| <span data-ttu-id="134d3-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="134d3-183">Is-Single-Valued</span></span>       | <span data-ttu-id="134d3-184">False</span><span class="sxs-lookup"><span data-stu-id="134d3-184">False</span></span>                                                              |
| <span data-ttu-id="134d3-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="134d3-185">Is Indexed</span></span>             | <span data-ttu-id="134d3-186">False</span><span class="sxs-lookup"><span data-stu-id="134d3-186">False</span></span>                                                              |
| <span data-ttu-id="134d3-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="134d3-187">In Global Catalog</span></span>      | <span data-ttu-id="134d3-188">False</span><span class="sxs-lookup"><span data-stu-id="134d3-188">False</span></span>                                                              |
| <span data-ttu-id="134d3-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="134d3-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="134d3-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="134d3-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="134d3-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="134d3-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="134d3-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="134d3-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="134d3-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="134d3-193">Search-Flags</span></span>           | <span data-ttu-id="134d3-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="134d3-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="134d3-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="134d3-195">System-Flags</span></span>           | <span data-ttu-id="134d3-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="134d3-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="134d3-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="134d3-197">Classes used in</span></span>        | [<span data-ttu-id="134d3-198">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="134d3-198">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="134d3-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="134d3-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="134d3-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="134d3-200">Entry</span></span> | <span data-ttu-id="134d3-201">Value</span><span class="sxs-lookup"><span data-stu-id="134d3-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="134d3-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="134d3-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="134d3-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="134d3-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="134d3-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="134d3-204">System-Only</span></span>            | <span data-ttu-id="134d3-205">False</span><span class="sxs-lookup"><span data-stu-id="134d3-205">False</span></span>                                                              |
| <span data-ttu-id="134d3-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="134d3-206">Is-Single-Valued</span></span>       | <span data-ttu-id="134d3-207">False</span><span class="sxs-lookup"><span data-stu-id="134d3-207">False</span></span>                                                              |
| <span data-ttu-id="134d3-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="134d3-208">Is Indexed</span></span>             | <span data-ttu-id="134d3-209">False</span><span class="sxs-lookup"><span data-stu-id="134d3-209">False</span></span>                                                              |
| <span data-ttu-id="134d3-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="134d3-210">In Global Catalog</span></span>      | <span data-ttu-id="134d3-211">False</span><span class="sxs-lookup"><span data-stu-id="134d3-211">False</span></span>                                                              |
| <span data-ttu-id="134d3-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="134d3-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="134d3-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="134d3-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="134d3-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="134d3-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="134d3-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="134d3-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="134d3-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="134d3-216">Search-Flags</span></span>           | <span data-ttu-id="134d3-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="134d3-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="134d3-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="134d3-218">System-Flags</span></span>           | <span data-ttu-id="134d3-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="134d3-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="134d3-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="134d3-220">Classes used in</span></span>        | [<span data-ttu-id="134d3-221">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="134d3-221">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="134d3-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="134d3-222">Windows Server 2012</span></span>



| <span data-ttu-id="134d3-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="134d3-223">Entry</span></span> | <span data-ttu-id="134d3-224">Value</span><span class="sxs-lookup"><span data-stu-id="134d3-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="134d3-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="134d3-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="134d3-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="134d3-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="134d3-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="134d3-227">System-Only</span></span>            | <span data-ttu-id="134d3-228">False</span><span class="sxs-lookup"><span data-stu-id="134d3-228">False</span></span>                                                              |
| <span data-ttu-id="134d3-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="134d3-229">Is-Single-Valued</span></span>       | <span data-ttu-id="134d3-230">False</span><span class="sxs-lookup"><span data-stu-id="134d3-230">False</span></span>                                                              |
| <span data-ttu-id="134d3-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="134d3-231">Is Indexed</span></span>             | <span data-ttu-id="134d3-232">False</span><span class="sxs-lookup"><span data-stu-id="134d3-232">False</span></span>                                                              |
| <span data-ttu-id="134d3-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="134d3-233">In Global Catalog</span></span>      | <span data-ttu-id="134d3-234">False</span><span class="sxs-lookup"><span data-stu-id="134d3-234">False</span></span>                                                              |
| <span data-ttu-id="134d3-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="134d3-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="134d3-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="134d3-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="134d3-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="134d3-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="134d3-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="134d3-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="134d3-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="134d3-239">Search-Flags</span></span>           | <span data-ttu-id="134d3-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="134d3-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="134d3-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="134d3-241">System-Flags</span></span>           | <span data-ttu-id="134d3-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="134d3-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="134d3-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="134d3-243">Classes used in</span></span>        | [<span data-ttu-id="134d3-244">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="134d3-244">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



 

 





