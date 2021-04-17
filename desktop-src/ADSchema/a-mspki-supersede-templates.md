---
title: atributo MS-PKI-reemplazó-templates
description: Especifica los nombres de las plantillas de certificado que se sustituyen por la plantilla actual.
ms.assetid: 4e247932-1c50-4bfb-b723-52b7c36a8571
ms.tgt_platform: multiple
keywords:
- atributo MS-PKI-reemplazó-templates AD Schema
- Atributo mspki-reemplazó-esquema de AD de atributos de plantillas
topic_type:
- apiref
api_name:
- ms-PKI-Supersede-Templates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd11ac2b96846912b0c6b1e8d01c6fd558f5f6db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535968"
---
# <a name="ms-pki-supersede-templates-attribute"></a><span data-ttu-id="5ef36-105">atributo MS-PKI-reemplazó-templates</span><span class="sxs-lookup"><span data-stu-id="5ef36-105">ms-PKI-Supersede-Templates attribute</span></span>

<span data-ttu-id="5ef36-106">Especifica los nombres de las plantillas de certificado que se sustituyen por la plantilla actual.</span><span class="sxs-lookup"><span data-stu-id="5ef36-106">Specifies the names of the certificate templates that are superseded by the current template.</span></span>



| <span data-ttu-id="5ef36-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ef36-107">Entry</span></span> | <span data-ttu-id="5ef36-108">Value</span><span class="sxs-lookup"><span data-stu-id="5ef36-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef36-109">CN</span><span class="sxs-lookup"><span data-stu-id="5ef36-109">CN</span></span>                | <span data-ttu-id="5ef36-110">MS-PKI-reemplazó-plantillas</span><span class="sxs-lookup"><span data-stu-id="5ef36-110">ms-PKI-Supersede-Templates</span></span>                                                                        |
| <span data-ttu-id="5ef36-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="5ef36-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5ef36-112">Atributo mspki-reemplazó-plantillas</span><span class="sxs-lookup"><span data-stu-id="5ef36-112">msPKI-Supersede-Templates</span></span>                                                                         |
| <span data-ttu-id="5ef36-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="5ef36-113">Size</span></span>              | <span data-ttu-id="5ef36-114">64 bytes</span><span class="sxs-lookup"><span data-stu-id="5ef36-114">64 bytes</span></span>                                                                                          |
| <span data-ttu-id="5ef36-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="5ef36-115">Update Privilege</span></span>  | <span data-ttu-id="5ef36-116">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="5ef36-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="5ef36-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="5ef36-117">Update Frequency</span></span>  | <span data-ttu-id="5ef36-118">Cuando se edita, crea o clona el objeto plantilla de certificado (MS-PKI-Certificate-template).</span><span class="sxs-lookup"><span data-stu-id="5ef36-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="5ef36-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5ef36-119">Attribute-Id</span></span>      | <span data-ttu-id="5ef36-120">1.2.840.113556.1.4.1437</span><span class="sxs-lookup"><span data-stu-id="5ef36-120">1.2.840.113556.1.4.1437</span></span>                                                                           |
| <span data-ttu-id="5ef36-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5ef36-121">System-Id-Guid</span></span>    | <span data-ttu-id="5ef36-122">9de8ae7d-7a5b-421d-b5e4-061f79dfd5d7</span><span class="sxs-lookup"><span data-stu-id="5ef36-122">9de8ae7d-7a5b-421d-b5e4-061f79dfd5d7</span></span>                                                              |
| <span data-ttu-id="5ef36-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ef36-123">Syntax</span></span>            | [<span data-ttu-id="5ef36-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5ef36-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="5ef36-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="5ef36-125">Implementations</span></span>

-   [<span data-ttu-id="5ef36-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5ef36-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5ef36-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5ef36-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5ef36-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5ef36-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5ef36-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5ef36-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5ef36-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5ef36-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="5ef36-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5ef36-131">Windows Server 2003</span></span>



| <span data-ttu-id="5ef36-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ef36-132">Entry</span></span> | <span data-ttu-id="5ef36-133">Value</span><span class="sxs-lookup"><span data-stu-id="5ef36-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="5ef36-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5ef36-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5ef36-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ef36-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5ef36-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ef36-136">System-Only</span></span>            | <span data-ttu-id="5ef36-137">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-137">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5ef36-138">Is-Single-Valued</span></span>       | <span data-ttu-id="5ef36-139">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-139">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5ef36-140">Is Indexed</span></span>             | <span data-ttu-id="5ef36-141">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-141">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5ef36-142">In Global Catalog</span></span>      | <span data-ttu-id="5ef36-143">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-143">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5ef36-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ef36-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5ef36-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="5ef36-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ef36-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="5ef36-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ef36-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="5ef36-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ef36-148">Search-Flags</span></span>           | <span data-ttu-id="5ef36-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ef36-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="5ef36-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ef36-150">System-Flags</span></span>           | <span data-ttu-id="5ef36-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5ef36-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="5ef36-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5ef36-152">Classes used in</span></span>        | [<span data-ttu-id="5ef36-153">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="5ef36-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5ef36-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5ef36-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5ef36-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ef36-155">Entry</span></span> | <span data-ttu-id="5ef36-156">Value</span><span class="sxs-lookup"><span data-stu-id="5ef36-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="5ef36-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5ef36-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5ef36-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ef36-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5ef36-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ef36-159">System-Only</span></span>            | <span data-ttu-id="5ef36-160">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-160">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5ef36-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5ef36-162">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-162">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5ef36-163">Is Indexed</span></span>             | <span data-ttu-id="5ef36-164">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-164">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5ef36-165">In Global Catalog</span></span>      | <span data-ttu-id="5ef36-166">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-166">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5ef36-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ef36-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5ef36-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="5ef36-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ef36-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="5ef36-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ef36-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="5ef36-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ef36-171">Search-Flags</span></span>           | <span data-ttu-id="5ef36-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ef36-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="5ef36-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ef36-173">System-Flags</span></span>           | <span data-ttu-id="5ef36-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5ef36-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="5ef36-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5ef36-175">Classes used in</span></span>        | [<span data-ttu-id="5ef36-176">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="5ef36-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5ef36-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ef36-177">Windows Server 2008</span></span>



| <span data-ttu-id="5ef36-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ef36-178">Entry</span></span> | <span data-ttu-id="5ef36-179">Value</span><span class="sxs-lookup"><span data-stu-id="5ef36-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="5ef36-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5ef36-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5ef36-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ef36-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5ef36-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ef36-182">System-Only</span></span>            | <span data-ttu-id="5ef36-183">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-183">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5ef36-184">Is-Single-Valued</span></span>       | <span data-ttu-id="5ef36-185">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-185">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5ef36-186">Is Indexed</span></span>             | <span data-ttu-id="5ef36-187">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-187">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5ef36-188">In Global Catalog</span></span>      | <span data-ttu-id="5ef36-189">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-189">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5ef36-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ef36-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5ef36-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="5ef36-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ef36-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="5ef36-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ef36-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="5ef36-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ef36-194">Search-Flags</span></span>           | <span data-ttu-id="5ef36-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ef36-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="5ef36-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ef36-196">System-Flags</span></span>           | <span data-ttu-id="5ef36-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5ef36-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="5ef36-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5ef36-198">Classes used in</span></span>        | [<span data-ttu-id="5ef36-199">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="5ef36-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5ef36-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5ef36-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5ef36-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ef36-201">Entry</span></span> | <span data-ttu-id="5ef36-202">Value</span><span class="sxs-lookup"><span data-stu-id="5ef36-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="5ef36-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5ef36-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5ef36-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ef36-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5ef36-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ef36-205">System-Only</span></span>            | <span data-ttu-id="5ef36-206">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-206">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5ef36-207">Is-Single-Valued</span></span>       | <span data-ttu-id="5ef36-208">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-208">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5ef36-209">Is Indexed</span></span>             | <span data-ttu-id="5ef36-210">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-210">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5ef36-211">In Global Catalog</span></span>      | <span data-ttu-id="5ef36-212">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-212">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5ef36-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ef36-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5ef36-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="5ef36-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ef36-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="5ef36-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ef36-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="5ef36-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ef36-217">Search-Flags</span></span>           | <span data-ttu-id="5ef36-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ef36-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="5ef36-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ef36-219">System-Flags</span></span>           | <span data-ttu-id="5ef36-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5ef36-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="5ef36-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5ef36-221">Classes used in</span></span>        | [<span data-ttu-id="5ef36-222">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="5ef36-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5ef36-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ef36-223">Windows Server 2012</span></span>



| <span data-ttu-id="5ef36-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ef36-224">Entry</span></span> | <span data-ttu-id="5ef36-225">Value</span><span class="sxs-lookup"><span data-stu-id="5ef36-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="5ef36-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5ef36-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5ef36-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ef36-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5ef36-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ef36-228">System-Only</span></span>            | <span data-ttu-id="5ef36-229">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-229">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5ef36-230">Is-Single-Valued</span></span>       | <span data-ttu-id="5ef36-231">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-231">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5ef36-232">Is Indexed</span></span>             | <span data-ttu-id="5ef36-233">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-233">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5ef36-234">In Global Catalog</span></span>      | <span data-ttu-id="5ef36-235">False</span><span class="sxs-lookup"><span data-stu-id="5ef36-235">False</span></span>                                                                   |
| <span data-ttu-id="5ef36-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5ef36-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ef36-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5ef36-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="5ef36-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ef36-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="5ef36-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ef36-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="5ef36-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ef36-240">Search-Flags</span></span>           | <span data-ttu-id="5ef36-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ef36-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="5ef36-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ef36-242">System-Flags</span></span>           | <span data-ttu-id="5ef36-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5ef36-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="5ef36-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5ef36-244">Classes used in</span></span>        | [<span data-ttu-id="5ef36-245">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="5ef36-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





