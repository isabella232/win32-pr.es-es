---
title: atributo MS-PKI-Certificate-Policy
description: Contiene la lista de OID de directiva y sus CSP opcionales en el certificado emitido.
ms.assetid: bc84c5ff-9cb1-406c-825c-97fa479d52eb
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-PKI-Certificate-Policy
- Atributo mspki-Certificate-Policy atributo AD Schema
topic_type:
- apiref
api_name:
- ms-PKI-Certificate-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2d6857b6035cc72271c7276b679b8a497aaab9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905991"
---
# <a name="ms-pki-certificate-policy-attribute"></a><span data-ttu-id="fcf22-105">atributo MS-PKI-Certificate-Policy</span><span class="sxs-lookup"><span data-stu-id="fcf22-105">ms-PKI-Certificate-Policy attribute</span></span>

<span data-ttu-id="fcf22-106">Contiene la lista de OID de directiva y sus CSP opcionales en el certificado emitido.</span><span class="sxs-lookup"><span data-stu-id="fcf22-106">Contains the list of policy OIDs and their optional CSPs in the issued certificate.</span></span>



| <span data-ttu-id="fcf22-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="fcf22-107">Entry</span></span> | <span data-ttu-id="fcf22-108">Value</span><span class="sxs-lookup"><span data-stu-id="fcf22-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcf22-109">CN</span><span class="sxs-lookup"><span data-stu-id="fcf22-109">CN</span></span>                | <span data-ttu-id="fcf22-110">MS-PKI-Certificate-Policy</span><span class="sxs-lookup"><span data-stu-id="fcf22-110">ms-PKI-Certificate-Policy</span></span>                                                                         |
| <span data-ttu-id="fcf22-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="fcf22-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fcf22-112">Atributo mspki-Certificate-Policy</span><span class="sxs-lookup"><span data-stu-id="fcf22-112">msPKI-Certificate-Policy</span></span>                                                                          |
| <span data-ttu-id="fcf22-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="fcf22-113">Size</span></span>              | <span data-ttu-id="fcf22-114">64 bytes veces el número de entradas.</span><span class="sxs-lookup"><span data-stu-id="fcf22-114">64 bytes times the number of entries.</span></span>                                                             |
| <span data-ttu-id="fcf22-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="fcf22-115">Update Privilege</span></span>  | <span data-ttu-id="fcf22-116">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="fcf22-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="fcf22-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="fcf22-117">Update Frequency</span></span>  | <span data-ttu-id="fcf22-118">Cuando se edita, crea o clona el objeto plantilla de certificado (MS-PKI-Certificate-template).</span><span class="sxs-lookup"><span data-stu-id="fcf22-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="fcf22-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fcf22-119">Attribute-Id</span></span>      | <span data-ttu-id="fcf22-120">1.2.840.113556.1.4.1439</span><span class="sxs-lookup"><span data-stu-id="fcf22-120">1.2.840.113556.1.4.1439</span></span>                                                                           |
| <span data-ttu-id="fcf22-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fcf22-121">System-Id-Guid</span></span>    | <span data-ttu-id="fcf22-122">38942346-cc5b-424b-a7d8-6ffd12029c5f</span><span class="sxs-lookup"><span data-stu-id="fcf22-122">38942346-cc5b-424b-a7d8-6ffd12029c5f</span></span>                                                              |
| <span data-ttu-id="fcf22-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fcf22-123">Syntax</span></span>            | [<span data-ttu-id="fcf22-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="fcf22-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="fcf22-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="fcf22-125">Implementations</span></span>

-   [<span data-ttu-id="fcf22-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fcf22-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fcf22-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fcf22-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fcf22-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fcf22-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fcf22-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fcf22-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fcf22-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fcf22-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="fcf22-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fcf22-131">Windows Server 2003</span></span>



| <span data-ttu-id="fcf22-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="fcf22-132">Entry</span></span> | <span data-ttu-id="fcf22-133">Value</span><span class="sxs-lookup"><span data-stu-id="fcf22-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fcf22-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fcf22-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fcf22-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fcf22-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fcf22-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="fcf22-136">System-Only</span></span>            | <span data-ttu-id="fcf22-137">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-137">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fcf22-138">Is-Single-Valued</span></span>       | <span data-ttu-id="fcf22-139">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-139">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fcf22-140">Is Indexed</span></span>             | <span data-ttu-id="fcf22-141">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-141">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fcf22-142">In Global Catalog</span></span>      | <span data-ttu-id="fcf22-143">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-143">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fcf22-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="fcf22-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fcf22-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="fcf22-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fcf22-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="fcf22-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fcf22-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="fcf22-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fcf22-148">Search-Flags</span></span>           | <span data-ttu-id="fcf22-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcf22-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="fcf22-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fcf22-150">System-Flags</span></span>           | <span data-ttu-id="fcf22-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fcf22-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="fcf22-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fcf22-152">Classes used in</span></span>        | [<span data-ttu-id="fcf22-153">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="fcf22-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fcf22-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fcf22-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fcf22-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="fcf22-155">Entry</span></span> | <span data-ttu-id="fcf22-156">Value</span><span class="sxs-lookup"><span data-stu-id="fcf22-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fcf22-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fcf22-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fcf22-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fcf22-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fcf22-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="fcf22-159">System-Only</span></span>            | <span data-ttu-id="fcf22-160">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-160">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fcf22-161">Is-Single-Valued</span></span>       | <span data-ttu-id="fcf22-162">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-162">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fcf22-163">Is Indexed</span></span>             | <span data-ttu-id="fcf22-164">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-164">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fcf22-165">In Global Catalog</span></span>      | <span data-ttu-id="fcf22-166">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-166">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fcf22-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="fcf22-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fcf22-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="fcf22-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fcf22-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="fcf22-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fcf22-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="fcf22-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fcf22-171">Search-Flags</span></span>           | <span data-ttu-id="fcf22-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcf22-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="fcf22-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fcf22-173">System-Flags</span></span>           | <span data-ttu-id="fcf22-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fcf22-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="fcf22-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fcf22-175">Classes used in</span></span>        | [<span data-ttu-id="fcf22-176">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="fcf22-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fcf22-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fcf22-177">Windows Server 2008</span></span>



| <span data-ttu-id="fcf22-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="fcf22-178">Entry</span></span> | <span data-ttu-id="fcf22-179">Value</span><span class="sxs-lookup"><span data-stu-id="fcf22-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fcf22-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fcf22-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fcf22-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fcf22-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fcf22-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="fcf22-182">System-Only</span></span>            | <span data-ttu-id="fcf22-183">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-183">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fcf22-184">Is-Single-Valued</span></span>       | <span data-ttu-id="fcf22-185">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-185">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fcf22-186">Is Indexed</span></span>             | <span data-ttu-id="fcf22-187">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-187">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fcf22-188">In Global Catalog</span></span>      | <span data-ttu-id="fcf22-189">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-189">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fcf22-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="fcf22-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fcf22-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="fcf22-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fcf22-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="fcf22-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fcf22-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="fcf22-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fcf22-194">Search-Flags</span></span>           | <span data-ttu-id="fcf22-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcf22-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="fcf22-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fcf22-196">System-Flags</span></span>           | <span data-ttu-id="fcf22-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fcf22-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="fcf22-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fcf22-198">Classes used in</span></span>        | [<span data-ttu-id="fcf22-199">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="fcf22-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fcf22-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fcf22-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fcf22-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="fcf22-201">Entry</span></span> | <span data-ttu-id="fcf22-202">Value</span><span class="sxs-lookup"><span data-stu-id="fcf22-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fcf22-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fcf22-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fcf22-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fcf22-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fcf22-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="fcf22-205">System-Only</span></span>            | <span data-ttu-id="fcf22-206">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-206">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fcf22-207">Is-Single-Valued</span></span>       | <span data-ttu-id="fcf22-208">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-208">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fcf22-209">Is Indexed</span></span>             | <span data-ttu-id="fcf22-210">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-210">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fcf22-211">In Global Catalog</span></span>      | <span data-ttu-id="fcf22-212">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-212">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fcf22-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="fcf22-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fcf22-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="fcf22-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fcf22-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="fcf22-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fcf22-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="fcf22-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fcf22-217">Search-Flags</span></span>           | <span data-ttu-id="fcf22-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcf22-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="fcf22-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fcf22-219">System-Flags</span></span>           | <span data-ttu-id="fcf22-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fcf22-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="fcf22-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fcf22-221">Classes used in</span></span>        | [<span data-ttu-id="fcf22-222">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="fcf22-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fcf22-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fcf22-223">Windows Server 2012</span></span>



| <span data-ttu-id="fcf22-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="fcf22-224">Entry</span></span> | <span data-ttu-id="fcf22-225">Value</span><span class="sxs-lookup"><span data-stu-id="fcf22-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fcf22-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fcf22-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fcf22-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fcf22-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fcf22-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="fcf22-228">System-Only</span></span>            | <span data-ttu-id="fcf22-229">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-229">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fcf22-230">Is-Single-Valued</span></span>       | <span data-ttu-id="fcf22-231">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-231">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fcf22-232">Is Indexed</span></span>             | <span data-ttu-id="fcf22-233">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-233">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fcf22-234">In Global Catalog</span></span>      | <span data-ttu-id="fcf22-235">False</span><span class="sxs-lookup"><span data-stu-id="fcf22-235">False</span></span>                                                                   |
| <span data-ttu-id="fcf22-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fcf22-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="fcf22-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fcf22-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="fcf22-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fcf22-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="fcf22-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fcf22-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="fcf22-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fcf22-240">Search-Flags</span></span>           | <span data-ttu-id="fcf22-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcf22-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="fcf22-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fcf22-242">System-Flags</span></span>           | <span data-ttu-id="fcf22-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fcf22-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="fcf22-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fcf22-244">Classes used in</span></span>        | [<span data-ttu-id="fcf22-245">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="fcf22-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





