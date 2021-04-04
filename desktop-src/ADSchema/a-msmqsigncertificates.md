---
title: Atributo MSMQ-Sign-Certificates
description: Este atributo contiene una serie de certificados. Un usuario puede generar un certificado por equipo. Para cada certificado, también se mantiene un resumen.
ms.assetid: 70e182c7-3544-43d7-b27a-6e8d03bd2d47
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MSMQ-Sign-Certificates
- mSMQSignCertificates esquema de AD de atributos
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd7e81cf145ac249b78e0a3e20be657df68b4af
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905998"
---
# <a name="msmq-sign-certificates-attribute"></a><span data-ttu-id="8acd5-107">Atributo MSMQ-Sign-Certificates</span><span class="sxs-lookup"><span data-stu-id="8acd5-107">MSMQ-Sign-Certificates attribute</span></span>

<span data-ttu-id="8acd5-108">Este atributo contiene una serie de certificados.</span><span class="sxs-lookup"><span data-stu-id="8acd5-108">This attribute contains a number of certificates.</span></span> <span data-ttu-id="8acd5-109">Un usuario puede generar un certificado por equipo.</span><span class="sxs-lookup"><span data-stu-id="8acd5-109">A user can generate a certificate per computer.</span></span> <span data-ttu-id="8acd5-110">Para cada certificado, también se mantiene un resumen.</span><span class="sxs-lookup"><span data-stu-id="8acd5-110">For each certificate we also keep a digest.</span></span>



| <span data-ttu-id="8acd5-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="8acd5-111">Entry</span></span> | <span data-ttu-id="8acd5-112">Value</span><span class="sxs-lookup"><span data-stu-id="8acd5-112">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8acd5-113">CN</span><span class="sxs-lookup"><span data-stu-id="8acd5-113">CN</span></span>                | <span data-ttu-id="8acd5-114">Certificados de firma MSMQ</span><span class="sxs-lookup"><span data-stu-id="8acd5-114">MSMQ-Sign-Certificates</span></span>                                                                 |
| <span data-ttu-id="8acd5-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="8acd5-115">Ldap-Display-Name</span></span> | <span data-ttu-id="8acd5-116">mSMQSignCertificates</span><span class="sxs-lookup"><span data-stu-id="8acd5-116">mSMQSignCertificates</span></span>                                                                   |
| <span data-ttu-id="8acd5-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="8acd5-117">Size</span></span>              | <span data-ttu-id="8acd5-118">El tipo de atributo es un BLOB, el tamaño no es limitado y los datos se mantienen en nuestro propio formato.</span><span class="sxs-lookup"><span data-stu-id="8acd5-118">The attribute type is a BLOB, size is not limited, and data is kept in our own format.</span></span> |
| <span data-ttu-id="8acd5-119">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="8acd5-119">Update Privilege</span></span>  | \-                                                                                     |
| <span data-ttu-id="8acd5-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="8acd5-120">Update Frequency</span></span>  | \-                                                                                     |
| <span data-ttu-id="8acd5-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8acd5-121">Attribute-Id</span></span>      | <span data-ttu-id="8acd5-122">1.2.840.113556.1.4.947</span><span class="sxs-lookup"><span data-stu-id="8acd5-122">1.2.840.113556.1.4.947</span></span>                                                                 |
| <span data-ttu-id="8acd5-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8acd5-123">System-Id-Guid</span></span>    | <span data-ttu-id="8acd5-124">9a0dc33b-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="8acd5-124">9a0dc33b-c100-11d1-bbc5-0080c76670c0</span></span>                                                   |
| <span data-ttu-id="8acd5-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8acd5-125">Syntax</span></span>            | [<span data-ttu-id="8acd5-126">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="8acd5-126">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                  |



## <a name="implementations"></a><span data-ttu-id="8acd5-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="8acd5-127">Implementations</span></span>

-   [<span data-ttu-id="8acd5-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8acd5-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8acd5-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8acd5-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8acd5-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8acd5-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8acd5-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8acd5-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8acd5-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8acd5-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8acd5-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8acd5-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8acd5-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8acd5-134">Windows 2000 Server</span></span>



| <span data-ttu-id="8acd5-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="8acd5-135">Entry</span></span> | <span data-ttu-id="8acd5-136">Value</span><span class="sxs-lookup"><span data-stu-id="8acd5-136">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8acd5-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8acd5-137">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="8acd5-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8acd5-138">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="8acd5-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="8acd5-139">System-Only</span></span>            | <span data-ttu-id="8acd5-140">False</span><span class="sxs-lookup"><span data-stu-id="8acd5-140">False</span></span>                                                                                         |
| <span data-ttu-id="8acd5-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8acd5-141">Is-Single-Valued</span></span>       | <span data-ttu-id="8acd5-142">True</span><span class="sxs-lookup"><span data-stu-id="8acd5-142">True</span></span>                                                                                          |
| <span data-ttu-id="8acd5-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8acd5-143">Is Indexed</span></span>             | <span data-ttu-id="8acd5-144">False</span><span class="sxs-lookup"><span data-stu-id="8acd5-144">False</span></span>                                                                                         |
| <span data-ttu-id="8acd5-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8acd5-145">In Global Catalog</span></span>      | <span data-ttu-id="8acd5-146">True</span><span class="sxs-lookup"><span data-stu-id="8acd5-146">True</span></span>                                                                                          |
| <span data-ttu-id="8acd5-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8acd5-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="8acd5-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8acd5-148">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="8acd5-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8acd5-149">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="8acd5-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8acd5-150">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="8acd5-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8acd5-151">Search-Flags</span></span>           | <span data-ttu-id="8acd5-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8acd5-152">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="8acd5-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8acd5-153">System-Flags</span></span>           | <span data-ttu-id="8acd5-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8acd5-154">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="8acd5-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8acd5-155">Classes used in</span></span>        | [<span data-ttu-id="8acd5-156">**MSMQ-Migrated: usuario**</span><span class="sxs-lookup"><span data-stu-id="8acd5-156">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="8acd5-157">**User**</span><span class="sxs-lookup"><span data-stu-id="8acd5-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8acd5-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8acd5-158">Windows Server 2003</span></span>



| <span data-ttu-id="8acd5-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="8acd5-159">Entry</span></span> | <span data-ttu-id="8acd5-160">Value</span><span class="sxs-lookup"><span data-stu-id="8acd5-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8acd5-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8acd5-161">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="8acd5-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8acd5-162">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="8acd5-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="8acd5-163">System-Only</span></span>            | <span data-ttu-id="8acd5-164">False</span><span class="sxs-lookup"><span data-stu-id="8acd5-164">False</span></span>                                                                                         |
| <span data-ttu-id="8acd5-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8acd5-165">Is-Single-Valued</span></span>       | <span data-ttu-id="8acd5-166">True</span><span class="sxs-lookup"><span data-stu-id="8acd5-166">True</span></span>                                                                                          |
| <span data-ttu-id="8acd5-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8acd5-167">Is Indexed</span></span>             | <span data-ttu-id="8acd5-168">False</span><span class="sxs-lookup"><span data-stu-id="8acd5-168">False</span></span>                                                                                         |
| <span data-ttu-id="8acd5-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8acd5-169">In Global Catalog</span></span>      | <span data-ttu-id="8acd5-170">True</span><span class="sxs-lookup"><span data-stu-id="8acd5-170">True</span></span>                                                                                          |
| <span data-ttu-id="8acd5-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8acd5-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="8acd5-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8acd5-172">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="8acd5-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8acd5-173">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="8acd5-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8acd5-174">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="8acd5-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8acd5-175">Search-Flags</span></span>           | <span data-ttu-id="8acd5-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8acd5-176">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="8acd5-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8acd5-177">System-Flags</span></span>           | <span data-ttu-id="8acd5-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8acd5-178">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="8acd5-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8acd5-179">Classes used in</span></span>        | [<span data-ttu-id="8acd5-180">**MSMQ-Migrated: usuario**</span><span class="sxs-lookup"><span data-stu-id="8acd5-180">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="8acd5-181">**User**</span><span class="sxs-lookup"><span data-stu-id="8acd5-181">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8acd5-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8acd5-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8acd5-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="8acd5-183">Entry</span></span> | <span data-ttu-id="8acd5-184">Value</span><span class="sxs-lookup"><span data-stu-id="8acd5-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8acd5-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8acd5-185">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="8acd5-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8acd5-186">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="8acd5-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="8acd5-187">System-Only</span></span>            | <span data-ttu-id="8acd5-188">False</span><span class="sxs-lookup"><span data-stu-id="8acd5-188">False</span></span>                                                                                         |
| <span data-ttu-id="8acd5-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8acd5-189">Is-Single-Valued</span></span>       | <span data-ttu-id="8acd5-190">True</span><span class="sxs-lookup"><span data-stu-id="8acd5-190">True</span></span>                                                                                          |
| <span data-ttu-id="8acd5-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8acd5-191">Is Indexed</span></span>             | <span data-ttu-id="8acd5-192">False</span><span class="sxs-lookup"><span data-stu-id="8acd5-192">False</span></span>                                                                                         |
| <span data-ttu-id="8acd5-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8acd5-193">In Global Catalog</span></span>      | <span data-ttu-id="8acd5-194">True</span><span class="sxs-lookup"><span data-stu-id="8acd5-194">True</span></span>                                                                                          |
| <span data-ttu-id="8acd5-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8acd5-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="8acd5-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8acd5-196">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="8acd5-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8acd5-197">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="8acd5-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8acd5-198">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="8acd5-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8acd5-199">Search-Flags</span></span>           | <span data-ttu-id="8acd5-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8acd5-200">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="8acd5-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8acd5-201">System-Flags</span></span>           | <span data-ttu-id="8acd5-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8acd5-202">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="8acd5-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8acd5-203">Classes used in</span></span>        | [<span data-ttu-id="8acd5-204">**MSMQ-Migrated: usuario**</span><span class="sxs-lookup"><span data-stu-id="8acd5-204">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="8acd5-205">**User**</span><span class="sxs-lookup"><span data-stu-id="8acd5-205">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8acd5-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8acd5-206">Windows Server 2008</span></span>



| <span data-ttu-id="8acd5-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="8acd5-207">Entry</span></span> | <span data-ttu-id="8acd5-208">Value</span><span class="sxs-lookup"><span data-stu-id="8acd5-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8acd5-209">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8acd5-209">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="8acd5-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8acd5-210">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="8acd5-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="8acd5-211">System-Only</span></span>            | <span data-ttu-id="8acd5-212">False</span><span class="sxs-lookup"><span data-stu-id="8acd5-212">False</span></span>                                                                                         |
| <span data-ttu-id="8acd5-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8acd5-213">Is-Single-Valued</span></span>       | <span data-ttu-id="8acd5-214">True</span><span class="sxs-lookup"><span data-stu-id="8acd5-214">True</span></span>                                                                                          |
| <span data-ttu-id="8acd5-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8acd5-215">Is Indexed</span></span>             | <span data-ttu-id="8acd5-216">False</span><span class="sxs-lookup"><span data-stu-id="8acd5-216">False</span></span>                                                                                         |
| <span data-ttu-id="8acd5-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8acd5-217">In Global Catalog</span></span>      | <span data-ttu-id="8acd5-218">True</span><span class="sxs-lookup"><span data-stu-id="8acd5-218">True</span></span>                                                                                          |
| <span data-ttu-id="8acd5-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8acd5-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="8acd5-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8acd5-220">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="8acd5-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8acd5-221">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="8acd5-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8acd5-222">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="8acd5-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8acd5-223">Search-Flags</span></span>           | <span data-ttu-id="8acd5-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8acd5-224">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="8acd5-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8acd5-225">System-Flags</span></span>           | <span data-ttu-id="8acd5-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8acd5-226">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="8acd5-227">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8acd5-227">Classes used in</span></span>        | [<span data-ttu-id="8acd5-228">**MSMQ-Migrated: usuario**</span><span class="sxs-lookup"><span data-stu-id="8acd5-228">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="8acd5-229">**User**</span><span class="sxs-lookup"><span data-stu-id="8acd5-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8acd5-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8acd5-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8acd5-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="8acd5-231">Entry</span></span> | <span data-ttu-id="8acd5-232">Value</span><span class="sxs-lookup"><span data-stu-id="8acd5-232">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8acd5-233">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8acd5-233">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="8acd5-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8acd5-234">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="8acd5-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="8acd5-235">System-Only</span></span>            | <span data-ttu-id="8acd5-236">False</span><span class="sxs-lookup"><span data-stu-id="8acd5-236">False</span></span>                                                                                         |
| <span data-ttu-id="8acd5-237">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8acd5-237">Is-Single-Valued</span></span>       | <span data-ttu-id="8acd5-238">True</span><span class="sxs-lookup"><span data-stu-id="8acd5-238">True</span></span>                                                                                          |
| <span data-ttu-id="8acd5-239">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8acd5-239">Is Indexed</span></span>             | <span data-ttu-id="8acd5-240">False</span><span class="sxs-lookup"><span data-stu-id="8acd5-240">False</span></span>                                                                                         |
| <span data-ttu-id="8acd5-241">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8acd5-241">In Global Catalog</span></span>      | <span data-ttu-id="8acd5-242">True</span><span class="sxs-lookup"><span data-stu-id="8acd5-242">True</span></span>                                                                                          |
| <span data-ttu-id="8acd5-243">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8acd5-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="8acd5-244">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8acd5-244">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="8acd5-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8acd5-245">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="8acd5-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8acd5-246">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="8acd5-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8acd5-247">Search-Flags</span></span>           | <span data-ttu-id="8acd5-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8acd5-248">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="8acd5-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8acd5-249">System-Flags</span></span>           | <span data-ttu-id="8acd5-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8acd5-250">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="8acd5-251">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8acd5-251">Classes used in</span></span>        | [<span data-ttu-id="8acd5-252">**MSMQ-Migrated: usuario**</span><span class="sxs-lookup"><span data-stu-id="8acd5-252">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="8acd5-253">**User**</span><span class="sxs-lookup"><span data-stu-id="8acd5-253">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8acd5-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8acd5-254">Windows Server 2012</span></span>



| <span data-ttu-id="8acd5-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="8acd5-255">Entry</span></span> | <span data-ttu-id="8acd5-256">Value</span><span class="sxs-lookup"><span data-stu-id="8acd5-256">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8acd5-257">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8acd5-257">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="8acd5-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8acd5-258">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="8acd5-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="8acd5-259">System-Only</span></span>            | <span data-ttu-id="8acd5-260">False</span><span class="sxs-lookup"><span data-stu-id="8acd5-260">False</span></span>                                                                                         |
| <span data-ttu-id="8acd5-261">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8acd5-261">Is-Single-Valued</span></span>       | <span data-ttu-id="8acd5-262">True</span><span class="sxs-lookup"><span data-stu-id="8acd5-262">True</span></span>                                                                                          |
| <span data-ttu-id="8acd5-263">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8acd5-263">Is Indexed</span></span>             | <span data-ttu-id="8acd5-264">False</span><span class="sxs-lookup"><span data-stu-id="8acd5-264">False</span></span>                                                                                         |
| <span data-ttu-id="8acd5-265">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8acd5-265">In Global Catalog</span></span>      | <span data-ttu-id="8acd5-266">True</span><span class="sxs-lookup"><span data-stu-id="8acd5-266">True</span></span>                                                                                          |
| <span data-ttu-id="8acd5-267">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8acd5-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="8acd5-268">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8acd5-268">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="8acd5-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8acd5-269">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="8acd5-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8acd5-270">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="8acd5-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8acd5-271">Search-Flags</span></span>           | <span data-ttu-id="8acd5-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8acd5-272">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="8acd5-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8acd5-273">System-Flags</span></span>           | <span data-ttu-id="8acd5-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8acd5-274">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="8acd5-275">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8acd5-275">Classes used in</span></span>        | [<span data-ttu-id="8acd5-276">**MSMQ-Migrated: usuario**</span><span class="sxs-lookup"><span data-stu-id="8acd5-276">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="8acd5-277">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="8acd5-277">**User**</span></span>](c-user.md)<br/> |



 

 





