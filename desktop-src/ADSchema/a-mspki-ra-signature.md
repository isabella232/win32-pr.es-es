---
title: atributo MS-PKI-RA-Signature
description: Especifica el número de firmas de autoridad de registro de inscripción que se requieren en una solicitud de inscripción.
ms.assetid: da9d9357-6826-4511-b589-594c73114713
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-PKI-RA-Signature
- Atributo mspki-RA-Signature atributo AD Schema
topic_type:
- apiref
api_name:
- ms-PKI-RA-Signature
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 170793e46095e16a62d8e025ec16b67bf2be7131
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658824"
---
# <a name="ms-pki-ra-signature-attribute"></a><span data-ttu-id="2ce91-105">atributo MS-PKI-RA-Signature</span><span class="sxs-lookup"><span data-stu-id="2ce91-105">ms-PKI-RA-Signature attribute</span></span>

<span data-ttu-id="2ce91-106">Especifica el número de firmas de autoridad de registro de inscripción que se requieren en una solicitud de inscripción.</span><span class="sxs-lookup"><span data-stu-id="2ce91-106">Specifies the number of enrollment registration authority signatures that are required in an enrollment request.</span></span>



| <span data-ttu-id="2ce91-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="2ce91-107">Entry</span></span> | <span data-ttu-id="2ce91-108">Value</span><span class="sxs-lookup"><span data-stu-id="2ce91-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ce91-109">CN</span><span class="sxs-lookup"><span data-stu-id="2ce91-109">CN</span></span>                | <span data-ttu-id="2ce91-110">MS-PKI-RA-Signature</span><span class="sxs-lookup"><span data-stu-id="2ce91-110">ms-PKI-RA-Signature</span></span>                                                                               |
| <span data-ttu-id="2ce91-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="2ce91-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2ce91-112">Atributo mspki-RA-Signature</span><span class="sxs-lookup"><span data-stu-id="2ce91-112">msPKI-RA-Signature</span></span>                                                                                |
| <span data-ttu-id="2ce91-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="2ce91-113">Size</span></span>              | <span data-ttu-id="2ce91-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="2ce91-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="2ce91-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="2ce91-115">Update Privilege</span></span>  | <span data-ttu-id="2ce91-116">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="2ce91-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="2ce91-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="2ce91-117">Update Frequency</span></span>  | <span data-ttu-id="2ce91-118">Cuando se edita, crea o clona el objeto plantilla de certificado (MS-PKI-Certificate-template).</span><span class="sxs-lookup"><span data-stu-id="2ce91-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="2ce91-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2ce91-119">Attribute-Id</span></span>      | <span data-ttu-id="2ce91-120">1.2.840.113556.1.4.1429</span><span class="sxs-lookup"><span data-stu-id="2ce91-120">1.2.840.113556.1.4.1429</span></span>                                                                           |
| <span data-ttu-id="2ce91-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2ce91-121">System-Id-Guid</span></span>    | <span data-ttu-id="2ce91-122">fe17e04b-937d-4f7e-8e0e-9292c8d5683e</span><span class="sxs-lookup"><span data-stu-id="2ce91-122">fe17e04b-937d-4f7e-8e0e-9292c8d5683e</span></span>                                                              |
| <span data-ttu-id="2ce91-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ce91-123">Syntax</span></span>            | [<span data-ttu-id="2ce91-124">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="2ce91-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="2ce91-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="2ce91-125">Implementations</span></span>

-   [<span data-ttu-id="2ce91-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2ce91-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2ce91-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2ce91-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2ce91-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2ce91-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2ce91-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2ce91-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2ce91-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2ce91-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="2ce91-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2ce91-131">Windows Server 2003</span></span>



| <span data-ttu-id="2ce91-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="2ce91-132">Entry</span></span> | <span data-ttu-id="2ce91-133">Value</span><span class="sxs-lookup"><span data-stu-id="2ce91-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2ce91-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2ce91-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2ce91-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ce91-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2ce91-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ce91-136">System-Only</span></span>            | <span data-ttu-id="2ce91-137">False</span><span class="sxs-lookup"><span data-stu-id="2ce91-137">False</span></span>                                                                   |
| <span data-ttu-id="2ce91-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2ce91-138">Is-Single-Valued</span></span>       | <span data-ttu-id="2ce91-139">True</span><span class="sxs-lookup"><span data-stu-id="2ce91-139">True</span></span>                                                                    |
| <span data-ttu-id="2ce91-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2ce91-140">Is Indexed</span></span>             | <span data-ttu-id="2ce91-141">False</span><span class="sxs-lookup"><span data-stu-id="2ce91-141">False</span></span>                                                                   |
| <span data-ttu-id="2ce91-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2ce91-142">In Global Catalog</span></span>      | <span data-ttu-id="2ce91-143">False</span><span class="sxs-lookup"><span data-stu-id="2ce91-143">False</span></span>                                                                   |
| <span data-ttu-id="2ce91-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2ce91-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ce91-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2ce91-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2ce91-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ce91-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2ce91-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ce91-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2ce91-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ce91-148">Search-Flags</span></span>           | <span data-ttu-id="2ce91-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ce91-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="2ce91-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ce91-150">System-Flags</span></span>           | <span data-ttu-id="2ce91-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ce91-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="2ce91-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2ce91-152">Classes used in</span></span>        | [<span data-ttu-id="2ce91-153">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="2ce91-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2ce91-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2ce91-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2ce91-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="2ce91-155">Entry</span></span> | <span data-ttu-id="2ce91-156">Value</span><span class="sxs-lookup"><span data-stu-id="2ce91-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2ce91-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2ce91-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2ce91-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ce91-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2ce91-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ce91-159">System-Only</span></span>            | <span data-ttu-id="2ce91-160">False</span><span class="sxs-lookup"><span data-stu-id="2ce91-160">False</span></span>                                                                   |
| <span data-ttu-id="2ce91-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2ce91-161">Is-Single-Valued</span></span>       | <span data-ttu-id="2ce91-162">True</span><span class="sxs-lookup"><span data-stu-id="2ce91-162">True</span></span>                                                                    |
| <span data-ttu-id="2ce91-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2ce91-163">Is Indexed</span></span>             | <span data-ttu-id="2ce91-164">False</span><span class="sxs-lookup"><span data-stu-id="2ce91-164">False</span></span>                                                                   |
| <span data-ttu-id="2ce91-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2ce91-165">In Global Catalog</span></span>      | <span data-ttu-id="2ce91-166">False</span><span class="sxs-lookup"><span data-stu-id="2ce91-166">False</span></span>                                                                   |
| <span data-ttu-id="2ce91-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2ce91-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ce91-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2ce91-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2ce91-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ce91-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2ce91-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ce91-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2ce91-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ce91-171">Search-Flags</span></span>           | <span data-ttu-id="2ce91-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ce91-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="2ce91-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ce91-173">System-Flags</span></span>           | <span data-ttu-id="2ce91-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ce91-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="2ce91-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2ce91-175">Classes used in</span></span>        | [<span data-ttu-id="2ce91-176">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="2ce91-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2ce91-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ce91-177">Windows Server 2008</span></span>



| <span data-ttu-id="2ce91-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="2ce91-178">Entry</span></span> | <span data-ttu-id="2ce91-179">Value</span><span class="sxs-lookup"><span data-stu-id="2ce91-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2ce91-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2ce91-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2ce91-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ce91-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2ce91-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ce91-182">System-Only</span></span>            | <span data-ttu-id="2ce91-183">False</span><span class="sxs-lookup"><span data-stu-id="2ce91-183">False</span></span>                                                                   |
| <span data-ttu-id="2ce91-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2ce91-184">Is-Single-Valued</span></span>       | <span data-ttu-id="2ce91-185">True</span><span class="sxs-lookup"><span data-stu-id="2ce91-185">True</span></span>                                                                    |
| <span data-ttu-id="2ce91-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2ce91-186">Is Indexed</span></span>             | <span data-ttu-id="2ce91-187">False</span><span class="sxs-lookup"><span data-stu-id="2ce91-187">False</span></span>                                                                   |
| <span data-ttu-id="2ce91-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2ce91-188">In Global Catalog</span></span>      | <span data-ttu-id="2ce91-189">False</span><span class="sxs-lookup"><span data-stu-id="2ce91-189">False</span></span>                                                                   |
| <span data-ttu-id="2ce91-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2ce91-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ce91-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2ce91-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2ce91-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ce91-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2ce91-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ce91-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2ce91-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ce91-194">Search-Flags</span></span>           | <span data-ttu-id="2ce91-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ce91-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="2ce91-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ce91-196">System-Flags</span></span>           | <span data-ttu-id="2ce91-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ce91-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="2ce91-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2ce91-198">Classes used in</span></span>        | [<span data-ttu-id="2ce91-199">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="2ce91-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2ce91-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2ce91-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2ce91-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="2ce91-201">Entry</span></span> | <span data-ttu-id="2ce91-202">Value</span><span class="sxs-lookup"><span data-stu-id="2ce91-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2ce91-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2ce91-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2ce91-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ce91-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2ce91-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ce91-205">System-Only</span></span>            | <span data-ttu-id="2ce91-206">False</span><span class="sxs-lookup"><span data-stu-id="2ce91-206">False</span></span>                                                                   |
| <span data-ttu-id="2ce91-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2ce91-207">Is-Single-Valued</span></span>       | <span data-ttu-id="2ce91-208">True</span><span class="sxs-lookup"><span data-stu-id="2ce91-208">True</span></span>                                                                    |
| <span data-ttu-id="2ce91-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2ce91-209">Is Indexed</span></span>             | <span data-ttu-id="2ce91-210">False</span><span class="sxs-lookup"><span data-stu-id="2ce91-210">False</span></span>                                                                   |
| <span data-ttu-id="2ce91-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2ce91-211">In Global Catalog</span></span>      | <span data-ttu-id="2ce91-212">False</span><span class="sxs-lookup"><span data-stu-id="2ce91-212">False</span></span>                                                                   |
| <span data-ttu-id="2ce91-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2ce91-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ce91-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2ce91-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2ce91-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ce91-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2ce91-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ce91-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2ce91-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ce91-217">Search-Flags</span></span>           | <span data-ttu-id="2ce91-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ce91-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="2ce91-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ce91-219">System-Flags</span></span>           | <span data-ttu-id="2ce91-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ce91-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="2ce91-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2ce91-221">Classes used in</span></span>        | [<span data-ttu-id="2ce91-222">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="2ce91-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2ce91-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ce91-223">Windows Server 2012</span></span>



| <span data-ttu-id="2ce91-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="2ce91-224">Entry</span></span> | <span data-ttu-id="2ce91-225">Value</span><span class="sxs-lookup"><span data-stu-id="2ce91-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2ce91-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2ce91-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2ce91-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ce91-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2ce91-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ce91-228">System-Only</span></span>            | <span data-ttu-id="2ce91-229">False</span><span class="sxs-lookup"><span data-stu-id="2ce91-229">False</span></span>                                                                   |
| <span data-ttu-id="2ce91-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2ce91-230">Is-Single-Valued</span></span>       | <span data-ttu-id="2ce91-231">True</span><span class="sxs-lookup"><span data-stu-id="2ce91-231">True</span></span>                                                                    |
| <span data-ttu-id="2ce91-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2ce91-232">Is Indexed</span></span>             | <span data-ttu-id="2ce91-233">False</span><span class="sxs-lookup"><span data-stu-id="2ce91-233">False</span></span>                                                                   |
| <span data-ttu-id="2ce91-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2ce91-234">In Global Catalog</span></span>      | <span data-ttu-id="2ce91-235">False</span><span class="sxs-lookup"><span data-stu-id="2ce91-235">False</span></span>                                                                   |
| <span data-ttu-id="2ce91-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2ce91-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ce91-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2ce91-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2ce91-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ce91-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2ce91-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ce91-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2ce91-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ce91-240">Search-Flags</span></span>           | <span data-ttu-id="2ce91-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ce91-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="2ce91-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ce91-242">System-Flags</span></span>           | <span data-ttu-id="2ce91-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ce91-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="2ce91-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2ce91-244">Classes used in</span></span>        | [<span data-ttu-id="2ce91-245">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="2ce91-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





