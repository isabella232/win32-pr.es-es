---
title: MSMQ-Digests atributo)
description: Una matriz de resúmenes de los certificados correspondientes en el atributo mSMQ-Sign-Certificates. Se usan para asignar una síntesis a un certificado.
ms.assetid: a9b03edd-1506-4f2d-afe1-7d953977f6fa
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de MSMQ-Digests
- mSMQDigests esquema de AD de atributos
topic_type:
- apiref
api_name:
- MSMQ-Digests
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d51c607b1d99af0aed46f259513f4bcf790844
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659084"
---
# <a name="msmq-digests-attribute"></a><span data-ttu-id="48bd1-106">MSMQ-Digests atributo)</span><span class="sxs-lookup"><span data-stu-id="48bd1-106">MSMQ-Digests attribute</span></span>

<span data-ttu-id="48bd1-107">Una matriz de resúmenes de los certificados correspondientes en el atributo mSMQ-Sign-Certificates.</span><span class="sxs-lookup"><span data-stu-id="48bd1-107">An array of digests of the corresponding certificates in attribute mSMQ-Sign-Certificates.</span></span> <span data-ttu-id="48bd1-108">Se usan para asignar una síntesis a un certificado.</span><span class="sxs-lookup"><span data-stu-id="48bd1-108">They are used for mapping a digest into a certificate.</span></span>



| <span data-ttu-id="48bd1-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="48bd1-109">Entry</span></span> | <span data-ttu-id="48bd1-110">Value</span><span class="sxs-lookup"><span data-stu-id="48bd1-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="48bd1-111">CN</span><span class="sxs-lookup"><span data-stu-id="48bd1-111">CN</span></span>                | <span data-ttu-id="48bd1-112">MSMQ-Digests</span><span class="sxs-lookup"><span data-stu-id="48bd1-112">MSMQ-Digests</span></span>                                          |
| <span data-ttu-id="48bd1-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="48bd1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="48bd1-114">mSMQDigests</span><span class="sxs-lookup"><span data-stu-id="48bd1-114">mSMQDigests</span></span>                                           |
| <span data-ttu-id="48bd1-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="48bd1-115">Size</span></span>              | <span data-ttu-id="48bd1-116">Cada síntesis es de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="48bd1-116">Each digest is 16 bytes.</span></span>                              |
| <span data-ttu-id="48bd1-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="48bd1-117">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="48bd1-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="48bd1-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="48bd1-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="48bd1-119">Attribute-Id</span></span>      | <span data-ttu-id="48bd1-120">1.2.840.113556.1.4.948</span><span class="sxs-lookup"><span data-stu-id="48bd1-120">1.2.840.113556.1.4.948</span></span>                                |
| <span data-ttu-id="48bd1-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="48bd1-121">System-Id-Guid</span></span>    | <span data-ttu-id="48bd1-122">9a0dc33c-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="48bd1-122">9a0dc33c-c100-11d1-bbc5-0080c76670c0</span></span>                  |
| <span data-ttu-id="48bd1-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48bd1-123">Syntax</span></span>            | [<span data-ttu-id="48bd1-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="48bd1-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="48bd1-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="48bd1-125">Implementations</span></span>

-   [<span data-ttu-id="48bd1-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="48bd1-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="48bd1-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="48bd1-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="48bd1-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="48bd1-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="48bd1-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="48bd1-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="48bd1-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="48bd1-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="48bd1-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="48bd1-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="48bd1-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="48bd1-132">Windows 2000 Server</span></span>



| <span data-ttu-id="48bd1-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="48bd1-133">Entry</span></span> | <span data-ttu-id="48bd1-134">Value</span><span class="sxs-lookup"><span data-stu-id="48bd1-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="48bd1-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="48bd1-135">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="48bd1-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48bd1-136">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="48bd1-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="48bd1-137">System-Only</span></span>            | <span data-ttu-id="48bd1-138">False</span><span class="sxs-lookup"><span data-stu-id="48bd1-138">False</span></span>                                                                                         |
| <span data-ttu-id="48bd1-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="48bd1-139">Is-Single-Valued</span></span>       | <span data-ttu-id="48bd1-140">False</span><span class="sxs-lookup"><span data-stu-id="48bd1-140">False</span></span>                                                                                         |
| <span data-ttu-id="48bd1-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="48bd1-141">Is Indexed</span></span>             | <span data-ttu-id="48bd1-142">True</span><span class="sxs-lookup"><span data-stu-id="48bd1-142">True</span></span>                                                                                          |
| <span data-ttu-id="48bd1-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="48bd1-143">In Global Catalog</span></span>      | <span data-ttu-id="48bd1-144">True</span><span class="sxs-lookup"><span data-stu-id="48bd1-144">True</span></span>                                                                                          |
| <span data-ttu-id="48bd1-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="48bd1-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="48bd1-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="48bd1-146">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="48bd1-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48bd1-147">Range-Lower</span></span>            | <span data-ttu-id="48bd1-148">16</span><span class="sxs-lookup"><span data-stu-id="48bd1-148">16</span></span>                                                                                            |
| <span data-ttu-id="48bd1-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48bd1-149">Range-Upper</span></span>            | <span data-ttu-id="48bd1-150">16</span><span class="sxs-lookup"><span data-stu-id="48bd1-150">16</span></span>                                                                                            |
| <span data-ttu-id="48bd1-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48bd1-151">Search-Flags</span></span>           | <span data-ttu-id="48bd1-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="48bd1-152">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="48bd1-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48bd1-153">System-Flags</span></span>           | <span data-ttu-id="48bd1-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48bd1-154">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="48bd1-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="48bd1-155">Classes used in</span></span>        | [<span data-ttu-id="48bd1-156">**MSMQ-Migrated: usuario**</span><span class="sxs-lookup"><span data-stu-id="48bd1-156">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="48bd1-157">**User**</span><span class="sxs-lookup"><span data-stu-id="48bd1-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="48bd1-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="48bd1-158">Windows Server 2003</span></span>



| <span data-ttu-id="48bd1-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="48bd1-159">Entry</span></span> | <span data-ttu-id="48bd1-160">Value</span><span class="sxs-lookup"><span data-stu-id="48bd1-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="48bd1-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="48bd1-161">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="48bd1-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48bd1-162">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="48bd1-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="48bd1-163">System-Only</span></span>            | <span data-ttu-id="48bd1-164">False</span><span class="sxs-lookup"><span data-stu-id="48bd1-164">False</span></span>                                                                                         |
| <span data-ttu-id="48bd1-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="48bd1-165">Is-Single-Valued</span></span>       | <span data-ttu-id="48bd1-166">False</span><span class="sxs-lookup"><span data-stu-id="48bd1-166">False</span></span>                                                                                         |
| <span data-ttu-id="48bd1-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="48bd1-167">Is Indexed</span></span>             | <span data-ttu-id="48bd1-168">True</span><span class="sxs-lookup"><span data-stu-id="48bd1-168">True</span></span>                                                                                          |
| <span data-ttu-id="48bd1-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="48bd1-169">In Global Catalog</span></span>      | <span data-ttu-id="48bd1-170">True</span><span class="sxs-lookup"><span data-stu-id="48bd1-170">True</span></span>                                                                                          |
| <span data-ttu-id="48bd1-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="48bd1-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="48bd1-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="48bd1-172">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="48bd1-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48bd1-173">Range-Lower</span></span>            | <span data-ttu-id="48bd1-174">16</span><span class="sxs-lookup"><span data-stu-id="48bd1-174">16</span></span>                                                                                            |
| <span data-ttu-id="48bd1-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48bd1-175">Range-Upper</span></span>            | <span data-ttu-id="48bd1-176">16</span><span class="sxs-lookup"><span data-stu-id="48bd1-176">16</span></span>                                                                                            |
| <span data-ttu-id="48bd1-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48bd1-177">Search-Flags</span></span>           | <span data-ttu-id="48bd1-178">0x00000001</span><span class="sxs-lookup"><span data-stu-id="48bd1-178">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="48bd1-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48bd1-179">System-Flags</span></span>           | <span data-ttu-id="48bd1-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48bd1-180">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="48bd1-181">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="48bd1-181">Classes used in</span></span>        | [<span data-ttu-id="48bd1-182">**MSMQ-Migrated: usuario**</span><span class="sxs-lookup"><span data-stu-id="48bd1-182">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="48bd1-183">**User**</span><span class="sxs-lookup"><span data-stu-id="48bd1-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="48bd1-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="48bd1-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="48bd1-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="48bd1-185">Entry</span></span> | <span data-ttu-id="48bd1-186">Value</span><span class="sxs-lookup"><span data-stu-id="48bd1-186">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="48bd1-187">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="48bd1-187">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="48bd1-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48bd1-188">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="48bd1-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="48bd1-189">System-Only</span></span>            | <span data-ttu-id="48bd1-190">False</span><span class="sxs-lookup"><span data-stu-id="48bd1-190">False</span></span>                                                                                         |
| <span data-ttu-id="48bd1-191">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="48bd1-191">Is-Single-Valued</span></span>       | <span data-ttu-id="48bd1-192">False</span><span class="sxs-lookup"><span data-stu-id="48bd1-192">False</span></span>                                                                                         |
| <span data-ttu-id="48bd1-193">Está indexado</span><span class="sxs-lookup"><span data-stu-id="48bd1-193">Is Indexed</span></span>             | <span data-ttu-id="48bd1-194">True</span><span class="sxs-lookup"><span data-stu-id="48bd1-194">True</span></span>                                                                                          |
| <span data-ttu-id="48bd1-195">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="48bd1-195">In Global Catalog</span></span>      | <span data-ttu-id="48bd1-196">True</span><span class="sxs-lookup"><span data-stu-id="48bd1-196">True</span></span>                                                                                          |
| <span data-ttu-id="48bd1-197">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="48bd1-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="48bd1-198">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="48bd1-198">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="48bd1-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48bd1-199">Range-Lower</span></span>            | <span data-ttu-id="48bd1-200">16</span><span class="sxs-lookup"><span data-stu-id="48bd1-200">16</span></span>                                                                                            |
| <span data-ttu-id="48bd1-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48bd1-201">Range-Upper</span></span>            | <span data-ttu-id="48bd1-202">16</span><span class="sxs-lookup"><span data-stu-id="48bd1-202">16</span></span>                                                                                            |
| <span data-ttu-id="48bd1-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48bd1-203">Search-Flags</span></span>           | <span data-ttu-id="48bd1-204">0x00000001</span><span class="sxs-lookup"><span data-stu-id="48bd1-204">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="48bd1-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48bd1-205">System-Flags</span></span>           | <span data-ttu-id="48bd1-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48bd1-206">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="48bd1-207">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="48bd1-207">Classes used in</span></span>        | [<span data-ttu-id="48bd1-208">**MSMQ-Migrated: usuario**</span><span class="sxs-lookup"><span data-stu-id="48bd1-208">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="48bd1-209">**User**</span><span class="sxs-lookup"><span data-stu-id="48bd1-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="48bd1-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48bd1-210">Windows Server 2008</span></span>



| <span data-ttu-id="48bd1-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="48bd1-211">Entry</span></span> | <span data-ttu-id="48bd1-212">Value</span><span class="sxs-lookup"><span data-stu-id="48bd1-212">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="48bd1-213">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="48bd1-213">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="48bd1-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48bd1-214">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="48bd1-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="48bd1-215">System-Only</span></span>            | <span data-ttu-id="48bd1-216">False</span><span class="sxs-lookup"><span data-stu-id="48bd1-216">False</span></span>                                                                                         |
| <span data-ttu-id="48bd1-217">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="48bd1-217">Is-Single-Valued</span></span>       | <span data-ttu-id="48bd1-218">False</span><span class="sxs-lookup"><span data-stu-id="48bd1-218">False</span></span>                                                                                         |
| <span data-ttu-id="48bd1-219">Está indexado</span><span class="sxs-lookup"><span data-stu-id="48bd1-219">Is Indexed</span></span>             | <span data-ttu-id="48bd1-220">True</span><span class="sxs-lookup"><span data-stu-id="48bd1-220">True</span></span>                                                                                          |
| <span data-ttu-id="48bd1-221">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="48bd1-221">In Global Catalog</span></span>      | <span data-ttu-id="48bd1-222">True</span><span class="sxs-lookup"><span data-stu-id="48bd1-222">True</span></span>                                                                                          |
| <span data-ttu-id="48bd1-223">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="48bd1-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="48bd1-224">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="48bd1-224">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="48bd1-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48bd1-225">Range-Lower</span></span>            | <span data-ttu-id="48bd1-226">16</span><span class="sxs-lookup"><span data-stu-id="48bd1-226">16</span></span>                                                                                            |
| <span data-ttu-id="48bd1-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48bd1-227">Range-Upper</span></span>            | <span data-ttu-id="48bd1-228">16</span><span class="sxs-lookup"><span data-stu-id="48bd1-228">16</span></span>                                                                                            |
| <span data-ttu-id="48bd1-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48bd1-229">Search-Flags</span></span>           | <span data-ttu-id="48bd1-230">0x00000001</span><span class="sxs-lookup"><span data-stu-id="48bd1-230">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="48bd1-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48bd1-231">System-Flags</span></span>           | <span data-ttu-id="48bd1-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48bd1-232">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="48bd1-233">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="48bd1-233">Classes used in</span></span>        | [<span data-ttu-id="48bd1-234">**MSMQ-Migrated: usuario**</span><span class="sxs-lookup"><span data-stu-id="48bd1-234">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="48bd1-235">**User**</span><span class="sxs-lookup"><span data-stu-id="48bd1-235">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="48bd1-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="48bd1-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="48bd1-237">Entrada</span><span class="sxs-lookup"><span data-stu-id="48bd1-237">Entry</span></span> | <span data-ttu-id="48bd1-238">Value</span><span class="sxs-lookup"><span data-stu-id="48bd1-238">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="48bd1-239">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="48bd1-239">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="48bd1-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48bd1-240">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="48bd1-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="48bd1-241">System-Only</span></span>            | <span data-ttu-id="48bd1-242">False</span><span class="sxs-lookup"><span data-stu-id="48bd1-242">False</span></span>                                                                                         |
| <span data-ttu-id="48bd1-243">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="48bd1-243">Is-Single-Valued</span></span>       | <span data-ttu-id="48bd1-244">False</span><span class="sxs-lookup"><span data-stu-id="48bd1-244">False</span></span>                                                                                         |
| <span data-ttu-id="48bd1-245">Está indexado</span><span class="sxs-lookup"><span data-stu-id="48bd1-245">Is Indexed</span></span>             | <span data-ttu-id="48bd1-246">True</span><span class="sxs-lookup"><span data-stu-id="48bd1-246">True</span></span>                                                                                          |
| <span data-ttu-id="48bd1-247">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="48bd1-247">In Global Catalog</span></span>      | <span data-ttu-id="48bd1-248">True</span><span class="sxs-lookup"><span data-stu-id="48bd1-248">True</span></span>                                                                                          |
| <span data-ttu-id="48bd1-249">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="48bd1-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="48bd1-250">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="48bd1-250">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="48bd1-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48bd1-251">Range-Lower</span></span>            | <span data-ttu-id="48bd1-252">16</span><span class="sxs-lookup"><span data-stu-id="48bd1-252">16</span></span>                                                                                            |
| <span data-ttu-id="48bd1-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48bd1-253">Range-Upper</span></span>            | <span data-ttu-id="48bd1-254">16</span><span class="sxs-lookup"><span data-stu-id="48bd1-254">16</span></span>                                                                                            |
| <span data-ttu-id="48bd1-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48bd1-255">Search-Flags</span></span>           | <span data-ttu-id="48bd1-256">0x00000001</span><span class="sxs-lookup"><span data-stu-id="48bd1-256">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="48bd1-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48bd1-257">System-Flags</span></span>           | <span data-ttu-id="48bd1-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48bd1-258">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="48bd1-259">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="48bd1-259">Classes used in</span></span>        | [<span data-ttu-id="48bd1-260">**MSMQ-Migrated: usuario**</span><span class="sxs-lookup"><span data-stu-id="48bd1-260">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="48bd1-261">**User**</span><span class="sxs-lookup"><span data-stu-id="48bd1-261">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="48bd1-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="48bd1-262">Windows Server 2012</span></span>



| <span data-ttu-id="48bd1-263">Entrada</span><span class="sxs-lookup"><span data-stu-id="48bd1-263">Entry</span></span> | <span data-ttu-id="48bd1-264">Value</span><span class="sxs-lookup"><span data-stu-id="48bd1-264">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="48bd1-265">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="48bd1-265">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="48bd1-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48bd1-266">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="48bd1-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="48bd1-267">System-Only</span></span>            | <span data-ttu-id="48bd1-268">False</span><span class="sxs-lookup"><span data-stu-id="48bd1-268">False</span></span>                                                                                         |
| <span data-ttu-id="48bd1-269">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="48bd1-269">Is-Single-Valued</span></span>       | <span data-ttu-id="48bd1-270">False</span><span class="sxs-lookup"><span data-stu-id="48bd1-270">False</span></span>                                                                                         |
| <span data-ttu-id="48bd1-271">Está indexado</span><span class="sxs-lookup"><span data-stu-id="48bd1-271">Is Indexed</span></span>             | <span data-ttu-id="48bd1-272">True</span><span class="sxs-lookup"><span data-stu-id="48bd1-272">True</span></span>                                                                                          |
| <span data-ttu-id="48bd1-273">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="48bd1-273">In Global Catalog</span></span>      | <span data-ttu-id="48bd1-274">True</span><span class="sxs-lookup"><span data-stu-id="48bd1-274">True</span></span>                                                                                          |
| <span data-ttu-id="48bd1-275">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="48bd1-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="48bd1-276">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="48bd1-276">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="48bd1-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48bd1-277">Range-Lower</span></span>            | <span data-ttu-id="48bd1-278">16</span><span class="sxs-lookup"><span data-stu-id="48bd1-278">16</span></span>                                                                                            |
| <span data-ttu-id="48bd1-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48bd1-279">Range-Upper</span></span>            | <span data-ttu-id="48bd1-280">16</span><span class="sxs-lookup"><span data-stu-id="48bd1-280">16</span></span>                                                                                            |
| <span data-ttu-id="48bd1-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48bd1-281">Search-Flags</span></span>           | <span data-ttu-id="48bd1-282">0x00000001</span><span class="sxs-lookup"><span data-stu-id="48bd1-282">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="48bd1-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48bd1-283">System-Flags</span></span>           | <span data-ttu-id="48bd1-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48bd1-284">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="48bd1-285">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="48bd1-285">Classes used in</span></span>        | [<span data-ttu-id="48bd1-286">**MSMQ-Migrated: usuario**</span><span class="sxs-lookup"><span data-stu-id="48bd1-286">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="48bd1-287">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="48bd1-287">**User**</span></span>](c-user.md)<br/> |



 

 





