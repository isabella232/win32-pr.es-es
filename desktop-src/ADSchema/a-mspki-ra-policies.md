---
title: atributo MS-PKI-RA-Policies
description: Contiene la lista de OID de directiva necesarios de las entidades de registro que firman la solicitud de inscripción.
ms.assetid: ebbdf95e-05c8-4b54-b7a5-4bb81d425225
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-PKI-RA-Policies
- Atributo mspki-RA-esquema de AD de atributos de directivas
topic_type:
- apiref
api_name:
- ms-PKI-RA-Policies
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b948dac7a95ae8b46972ace4d1ab46260b476da
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997540"
---
# <a name="ms-pki-ra-policies-attribute"></a><span data-ttu-id="adbad-105">atributo MS-PKI-RA-Policies</span><span class="sxs-lookup"><span data-stu-id="adbad-105">ms-PKI-RA-Policies attribute</span></span>

<span data-ttu-id="adbad-106">Contiene la lista de OID de directiva necesarios de las entidades de registro que firman la solicitud de inscripción.</span><span class="sxs-lookup"><span data-stu-id="adbad-106">Contains the list of required policy OIDs from registration authorities who sign the enrollment request.</span></span>



| <span data-ttu-id="adbad-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="adbad-107">Entry</span></span> | <span data-ttu-id="adbad-108">Value</span><span class="sxs-lookup"><span data-stu-id="adbad-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adbad-109">CN</span><span class="sxs-lookup"><span data-stu-id="adbad-109">CN</span></span>                | <span data-ttu-id="adbad-110">MS-PKI-RA-Policies</span><span class="sxs-lookup"><span data-stu-id="adbad-110">ms-PKI-RA-Policies</span></span>                                                                                |
| <span data-ttu-id="adbad-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="adbad-111">Ldap-Display-Name</span></span> | <span data-ttu-id="adbad-112">Atributo mspki-RA-directivas</span><span class="sxs-lookup"><span data-stu-id="adbad-112">msPKI-RA-Policies</span></span>                                                                                 |
| <span data-ttu-id="adbad-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="adbad-113">Size</span></span>              | <span data-ttu-id="adbad-114">64 bytes veces el número de entradas.</span><span class="sxs-lookup"><span data-stu-id="adbad-114">64 bytes times the number of entries.</span></span>                                                             |
| <span data-ttu-id="adbad-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="adbad-115">Update Privilege</span></span>  | <span data-ttu-id="adbad-116">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="adbad-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="adbad-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="adbad-117">Update Frequency</span></span>  | <span data-ttu-id="adbad-118">Cuando se edita, crea o clona el objeto plantilla de certificado (MS-PKI-Certificate-template).</span><span class="sxs-lookup"><span data-stu-id="adbad-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="adbad-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="adbad-119">Attribute-Id</span></span>      | <span data-ttu-id="adbad-120">1.2.840.113556.1.4.1438</span><span class="sxs-lookup"><span data-stu-id="adbad-120">1.2.840.113556.1.4.1438</span></span>                                                                           |
| <span data-ttu-id="adbad-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="adbad-121">System-Id-Guid</span></span>    | <span data-ttu-id="adbad-122">d546ae22-0951-4d47-817e-1c9f96faad46</span><span class="sxs-lookup"><span data-stu-id="adbad-122">d546ae22-0951-4d47-817e-1c9f96faad46</span></span>                                                              |
| <span data-ttu-id="adbad-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="adbad-123">Syntax</span></span>            | [<span data-ttu-id="adbad-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="adbad-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="adbad-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="adbad-125">Implementations</span></span>

-   [<span data-ttu-id="adbad-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="adbad-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="adbad-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="adbad-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="adbad-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="adbad-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="adbad-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="adbad-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="adbad-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="adbad-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="adbad-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="adbad-131">Windows Server 2003</span></span>



| <span data-ttu-id="adbad-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="adbad-132">Entry</span></span> | <span data-ttu-id="adbad-133">Value</span><span class="sxs-lookup"><span data-stu-id="adbad-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="adbad-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="adbad-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="adbad-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="adbad-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="adbad-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="adbad-136">System-Only</span></span>            | <span data-ttu-id="adbad-137">False</span><span class="sxs-lookup"><span data-stu-id="adbad-137">False</span></span>                                                                   |
| <span data-ttu-id="adbad-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="adbad-138">Is-Single-Valued</span></span>       | <span data-ttu-id="adbad-139">False</span><span class="sxs-lookup"><span data-stu-id="adbad-139">False</span></span>                                                                   |
| <span data-ttu-id="adbad-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="adbad-140">Is Indexed</span></span>             | <span data-ttu-id="adbad-141">False</span><span class="sxs-lookup"><span data-stu-id="adbad-141">False</span></span>                                                                   |
| <span data-ttu-id="adbad-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="adbad-142">In Global Catalog</span></span>      | <span data-ttu-id="adbad-143">False</span><span class="sxs-lookup"><span data-stu-id="adbad-143">False</span></span>                                                                   |
| <span data-ttu-id="adbad-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="adbad-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="adbad-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="adbad-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="adbad-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="adbad-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="adbad-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="adbad-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="adbad-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="adbad-148">Search-Flags</span></span>           | <span data-ttu-id="adbad-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adbad-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="adbad-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="adbad-150">System-Flags</span></span>           | <span data-ttu-id="adbad-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="adbad-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="adbad-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="adbad-152">Classes used in</span></span>        | [<span data-ttu-id="adbad-153">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="adbad-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="adbad-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="adbad-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="adbad-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="adbad-155">Entry</span></span> | <span data-ttu-id="adbad-156">Value</span><span class="sxs-lookup"><span data-stu-id="adbad-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="adbad-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="adbad-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="adbad-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="adbad-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="adbad-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="adbad-159">System-Only</span></span>            | <span data-ttu-id="adbad-160">False</span><span class="sxs-lookup"><span data-stu-id="adbad-160">False</span></span>                                                                   |
| <span data-ttu-id="adbad-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="adbad-161">Is-Single-Valued</span></span>       | <span data-ttu-id="adbad-162">False</span><span class="sxs-lookup"><span data-stu-id="adbad-162">False</span></span>                                                                   |
| <span data-ttu-id="adbad-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="adbad-163">Is Indexed</span></span>             | <span data-ttu-id="adbad-164">False</span><span class="sxs-lookup"><span data-stu-id="adbad-164">False</span></span>                                                                   |
| <span data-ttu-id="adbad-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="adbad-165">In Global Catalog</span></span>      | <span data-ttu-id="adbad-166">False</span><span class="sxs-lookup"><span data-stu-id="adbad-166">False</span></span>                                                                   |
| <span data-ttu-id="adbad-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="adbad-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="adbad-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="adbad-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="adbad-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="adbad-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="adbad-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="adbad-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="adbad-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="adbad-171">Search-Flags</span></span>           | <span data-ttu-id="adbad-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adbad-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="adbad-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="adbad-173">System-Flags</span></span>           | <span data-ttu-id="adbad-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="adbad-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="adbad-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="adbad-175">Classes used in</span></span>        | [<span data-ttu-id="adbad-176">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="adbad-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="adbad-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="adbad-177">Windows Server 2008</span></span>



| <span data-ttu-id="adbad-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="adbad-178">Entry</span></span> | <span data-ttu-id="adbad-179">Value</span><span class="sxs-lookup"><span data-stu-id="adbad-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="adbad-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="adbad-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="adbad-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="adbad-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="adbad-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="adbad-182">System-Only</span></span>            | <span data-ttu-id="adbad-183">False</span><span class="sxs-lookup"><span data-stu-id="adbad-183">False</span></span>                                                                   |
| <span data-ttu-id="adbad-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="adbad-184">Is-Single-Valued</span></span>       | <span data-ttu-id="adbad-185">False</span><span class="sxs-lookup"><span data-stu-id="adbad-185">False</span></span>                                                                   |
| <span data-ttu-id="adbad-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="adbad-186">Is Indexed</span></span>             | <span data-ttu-id="adbad-187">False</span><span class="sxs-lookup"><span data-stu-id="adbad-187">False</span></span>                                                                   |
| <span data-ttu-id="adbad-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="adbad-188">In Global Catalog</span></span>      | <span data-ttu-id="adbad-189">False</span><span class="sxs-lookup"><span data-stu-id="adbad-189">False</span></span>                                                                   |
| <span data-ttu-id="adbad-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="adbad-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="adbad-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="adbad-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="adbad-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="adbad-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="adbad-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="adbad-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="adbad-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="adbad-194">Search-Flags</span></span>           | <span data-ttu-id="adbad-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adbad-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="adbad-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="adbad-196">System-Flags</span></span>           | <span data-ttu-id="adbad-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="adbad-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="adbad-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="adbad-198">Classes used in</span></span>        | [<span data-ttu-id="adbad-199">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="adbad-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="adbad-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="adbad-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="adbad-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="adbad-201">Entry</span></span> | <span data-ttu-id="adbad-202">Value</span><span class="sxs-lookup"><span data-stu-id="adbad-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="adbad-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="adbad-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="adbad-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="adbad-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="adbad-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="adbad-205">System-Only</span></span>            | <span data-ttu-id="adbad-206">False</span><span class="sxs-lookup"><span data-stu-id="adbad-206">False</span></span>                                                                   |
| <span data-ttu-id="adbad-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="adbad-207">Is-Single-Valued</span></span>       | <span data-ttu-id="adbad-208">False</span><span class="sxs-lookup"><span data-stu-id="adbad-208">False</span></span>                                                                   |
| <span data-ttu-id="adbad-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="adbad-209">Is Indexed</span></span>             | <span data-ttu-id="adbad-210">False</span><span class="sxs-lookup"><span data-stu-id="adbad-210">False</span></span>                                                                   |
| <span data-ttu-id="adbad-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="adbad-211">In Global Catalog</span></span>      | <span data-ttu-id="adbad-212">False</span><span class="sxs-lookup"><span data-stu-id="adbad-212">False</span></span>                                                                   |
| <span data-ttu-id="adbad-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="adbad-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="adbad-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="adbad-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="adbad-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="adbad-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="adbad-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="adbad-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="adbad-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="adbad-217">Search-Flags</span></span>           | <span data-ttu-id="adbad-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adbad-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="adbad-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="adbad-219">System-Flags</span></span>           | <span data-ttu-id="adbad-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="adbad-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="adbad-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="adbad-221">Classes used in</span></span>        | [<span data-ttu-id="adbad-222">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="adbad-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="adbad-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="adbad-223">Windows Server 2012</span></span>



| <span data-ttu-id="adbad-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="adbad-224">Entry</span></span> | <span data-ttu-id="adbad-225">Value</span><span class="sxs-lookup"><span data-stu-id="adbad-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="adbad-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="adbad-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="adbad-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="adbad-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="adbad-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="adbad-228">System-Only</span></span>            | <span data-ttu-id="adbad-229">False</span><span class="sxs-lookup"><span data-stu-id="adbad-229">False</span></span>                                                                   |
| <span data-ttu-id="adbad-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="adbad-230">Is-Single-Valued</span></span>       | <span data-ttu-id="adbad-231">False</span><span class="sxs-lookup"><span data-stu-id="adbad-231">False</span></span>                                                                   |
| <span data-ttu-id="adbad-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="adbad-232">Is Indexed</span></span>             | <span data-ttu-id="adbad-233">False</span><span class="sxs-lookup"><span data-stu-id="adbad-233">False</span></span>                                                                   |
| <span data-ttu-id="adbad-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="adbad-234">In Global Catalog</span></span>      | <span data-ttu-id="adbad-235">False</span><span class="sxs-lookup"><span data-stu-id="adbad-235">False</span></span>                                                                   |
| <span data-ttu-id="adbad-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="adbad-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="adbad-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="adbad-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="adbad-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="adbad-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="adbad-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="adbad-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="adbad-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="adbad-240">Search-Flags</span></span>           | <span data-ttu-id="adbad-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adbad-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="adbad-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="adbad-242">System-Flags</span></span>           | <span data-ttu-id="adbad-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="adbad-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="adbad-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="adbad-244">Classes used in</span></span>        | [<span data-ttu-id="adbad-245">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="adbad-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





