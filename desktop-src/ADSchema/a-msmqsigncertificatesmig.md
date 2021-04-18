---
title: MSMQ-Sign-Certificates-atributo MIG
description: En el modo mixto de MSMQ, el atributo contiene el valor anterior de mSMQSignCertificates. MSMQ admite la migración de MSMQ 1,0 DS a Windows 2000 DS y el modo mixto especifica un estado en el que algunos de los servidores de DS no se actualizaron a Windows 2000.
ms.assetid: 0dbc5d97-39e6-4863-a386-541ea2abaadc
ms.tgt_platform: multiple
keywords:
- MSMQ-Sign-Certificates-MIG atributo AD Schema
- mSMQSignCertificatesMig esquema de AD de atributos
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates-Mig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a1916cf98d15da1bd84603a2305543e899d868
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659076"
---
# <a name="msmq-sign-certificates-mig-attribute"></a><span data-ttu-id="ddf4f-106">MSMQ-Sign-Certificates-atributo MIG</span><span class="sxs-lookup"><span data-stu-id="ddf4f-106">MSMQ-Sign-Certificates-Mig attribute</span></span>

<span data-ttu-id="ddf4f-107">En el modo mixto de MSMQ, el atributo contiene el valor anterior de mSMQSignCertificates.</span><span class="sxs-lookup"><span data-stu-id="ddf4f-107">In MSMQ mixed-mode, the attribute contains the previous value of mSMQSignCertificates.</span></span> <span data-ttu-id="ddf4f-108">MSMQ admite la migración de MSMQ 1,0 DS a Windows 2000 DS y el modo mixto especifica un estado en el que algunos de los servidores de DS no se actualizaron a Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ddf4f-108">MSMQ supports migration from the MSMQ 1.0 DS to the Windows 2000 DS, and mixed mode specifies a state in which some of the DS severs were not upgraded to Windows 2000.</span></span>



| <span data-ttu-id="ddf4f-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="ddf4f-109">Entry</span></span> | <span data-ttu-id="ddf4f-110">Value</span><span class="sxs-lookup"><span data-stu-id="ddf4f-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="ddf4f-111">CN</span><span class="sxs-lookup"><span data-stu-id="ddf4f-111">CN</span></span>                | <span data-ttu-id="ddf4f-112">MSMQ-Sign-Certificates-MIG</span><span class="sxs-lookup"><span data-stu-id="ddf4f-112">MSMQ-Sign-Certificates-Mig</span></span>                            |
| <span data-ttu-id="ddf4f-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="ddf4f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ddf4f-114">mSMQSignCertificatesMig</span><span class="sxs-lookup"><span data-stu-id="ddf4f-114">mSMQSignCertificatesMig</span></span>                               |
| <span data-ttu-id="ddf4f-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="ddf4f-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="ddf4f-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="ddf4f-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="ddf4f-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="ddf4f-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="ddf4f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ddf4f-118">Attribute-Id</span></span>      | <span data-ttu-id="ddf4f-119">1.2.840.113556.1.4.967</span><span class="sxs-lookup"><span data-stu-id="ddf4f-119">1.2.840.113556.1.4.967</span></span>                                |
| <span data-ttu-id="ddf4f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ddf4f-120">System-Id-Guid</span></span>    | <span data-ttu-id="ddf4f-121">3881b8ea-da3b-11d1-90a5-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="ddf4f-121">3881b8ea-da3b-11d1-90a5-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="ddf4f-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ddf4f-122">Syntax</span></span>            | [<span data-ttu-id="ddf4f-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="ddf4f-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="ddf4f-124">Implementations</span></span>

-   [<span data-ttu-id="ddf4f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ddf4f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ddf4f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ddf4f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ddf4f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ddf4f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ddf4f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ddf4f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ddf4f-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="ddf4f-132">Entry</span></span> | <span data-ttu-id="ddf4f-133">Value</span><span class="sxs-lookup"><span data-stu-id="ddf4f-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf4f-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ddf4f-134">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ddf4f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddf4f-135">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ddf4f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddf4f-136">System-Only</span></span>            | <span data-ttu-id="ddf4f-137">False</span><span class="sxs-lookup"><span data-stu-id="ddf4f-137">False</span></span>                                                                                         |
| <span data-ttu-id="ddf4f-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ddf4f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ddf4f-139">True</span><span class="sxs-lookup"><span data-stu-id="ddf4f-139">True</span></span>                                                                                          |
| <span data-ttu-id="ddf4f-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ddf4f-140">Is Indexed</span></span>             | <span data-ttu-id="ddf4f-141">False</span><span class="sxs-lookup"><span data-stu-id="ddf4f-141">False</span></span>                                                                                         |
| <span data-ttu-id="ddf4f-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ddf4f-142">In Global Catalog</span></span>      | <span data-ttu-id="ddf4f-143">True</span><span class="sxs-lookup"><span data-stu-id="ddf4f-143">True</span></span>                                                                                          |
| <span data-ttu-id="ddf4f-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ddf4f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddf4f-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ddf4f-145">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="ddf4f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddf4f-146">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="ddf4f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddf4f-147">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="ddf4f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf4f-148">Search-Flags</span></span>           | <span data-ttu-id="ddf4f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddf4f-149">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="ddf4f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf4f-150">System-Flags</span></span>           | <span data-ttu-id="ddf4f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddf4f-151">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="ddf4f-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ddf4f-152">Classes used in</span></span>        | [<span data-ttu-id="ddf4f-153">**MSMQ-Migrated: usuario**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-153">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="ddf4f-154">**User**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ddf4f-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ddf4f-155">Windows Server 2003</span></span>



| <span data-ttu-id="ddf4f-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="ddf4f-156">Entry</span></span> | <span data-ttu-id="ddf4f-157">Value</span><span class="sxs-lookup"><span data-stu-id="ddf4f-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf4f-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ddf4f-158">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ddf4f-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddf4f-159">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ddf4f-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddf4f-160">System-Only</span></span>            | <span data-ttu-id="ddf4f-161">False</span><span class="sxs-lookup"><span data-stu-id="ddf4f-161">False</span></span>                                                                                         |
| <span data-ttu-id="ddf4f-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ddf4f-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ddf4f-163">True</span><span class="sxs-lookup"><span data-stu-id="ddf4f-163">True</span></span>                                                                                          |
| <span data-ttu-id="ddf4f-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ddf4f-164">Is Indexed</span></span>             | <span data-ttu-id="ddf4f-165">False</span><span class="sxs-lookup"><span data-stu-id="ddf4f-165">False</span></span>                                                                                         |
| <span data-ttu-id="ddf4f-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ddf4f-166">In Global Catalog</span></span>      | <span data-ttu-id="ddf4f-167">True</span><span class="sxs-lookup"><span data-stu-id="ddf4f-167">True</span></span>                                                                                          |
| <span data-ttu-id="ddf4f-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ddf4f-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddf4f-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ddf4f-169">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="ddf4f-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddf4f-170">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="ddf4f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddf4f-171">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="ddf4f-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf4f-172">Search-Flags</span></span>           | <span data-ttu-id="ddf4f-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddf4f-173">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="ddf4f-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf4f-174">System-Flags</span></span>           | <span data-ttu-id="ddf4f-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddf4f-175">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="ddf4f-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ddf4f-176">Classes used in</span></span>        | [<span data-ttu-id="ddf4f-177">**MSMQ-Migrated: usuario**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-177">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="ddf4f-178">**User**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ddf4f-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ddf4f-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ddf4f-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="ddf4f-180">Entry</span></span> | <span data-ttu-id="ddf4f-181">Value</span><span class="sxs-lookup"><span data-stu-id="ddf4f-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf4f-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ddf4f-182">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ddf4f-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddf4f-183">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ddf4f-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddf4f-184">System-Only</span></span>            | <span data-ttu-id="ddf4f-185">False</span><span class="sxs-lookup"><span data-stu-id="ddf4f-185">False</span></span>                                                                                         |
| <span data-ttu-id="ddf4f-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ddf4f-186">Is-Single-Valued</span></span>       | <span data-ttu-id="ddf4f-187">True</span><span class="sxs-lookup"><span data-stu-id="ddf4f-187">True</span></span>                                                                                          |
| <span data-ttu-id="ddf4f-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ddf4f-188">Is Indexed</span></span>             | <span data-ttu-id="ddf4f-189">False</span><span class="sxs-lookup"><span data-stu-id="ddf4f-189">False</span></span>                                                                                         |
| <span data-ttu-id="ddf4f-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ddf4f-190">In Global Catalog</span></span>      | <span data-ttu-id="ddf4f-191">True</span><span class="sxs-lookup"><span data-stu-id="ddf4f-191">True</span></span>                                                                                          |
| <span data-ttu-id="ddf4f-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ddf4f-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddf4f-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ddf4f-193">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="ddf4f-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddf4f-194">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="ddf4f-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddf4f-195">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="ddf4f-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf4f-196">Search-Flags</span></span>           | <span data-ttu-id="ddf4f-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddf4f-197">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="ddf4f-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf4f-198">System-Flags</span></span>           | <span data-ttu-id="ddf4f-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddf4f-199">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="ddf4f-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ddf4f-200">Classes used in</span></span>        | [<span data-ttu-id="ddf4f-201">**MSMQ-Migrated: usuario**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-201">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="ddf4f-202">**User**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ddf4f-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddf4f-203">Windows Server 2008</span></span>



| <span data-ttu-id="ddf4f-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="ddf4f-204">Entry</span></span> | <span data-ttu-id="ddf4f-205">Value</span><span class="sxs-lookup"><span data-stu-id="ddf4f-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf4f-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ddf4f-206">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ddf4f-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddf4f-207">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ddf4f-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddf4f-208">System-Only</span></span>            | <span data-ttu-id="ddf4f-209">False</span><span class="sxs-lookup"><span data-stu-id="ddf4f-209">False</span></span>                                                                                         |
| <span data-ttu-id="ddf4f-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ddf4f-210">Is-Single-Valued</span></span>       | <span data-ttu-id="ddf4f-211">True</span><span class="sxs-lookup"><span data-stu-id="ddf4f-211">True</span></span>                                                                                          |
| <span data-ttu-id="ddf4f-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ddf4f-212">Is Indexed</span></span>             | <span data-ttu-id="ddf4f-213">False</span><span class="sxs-lookup"><span data-stu-id="ddf4f-213">False</span></span>                                                                                         |
| <span data-ttu-id="ddf4f-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ddf4f-214">In Global Catalog</span></span>      | <span data-ttu-id="ddf4f-215">True</span><span class="sxs-lookup"><span data-stu-id="ddf4f-215">True</span></span>                                                                                          |
| <span data-ttu-id="ddf4f-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ddf4f-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddf4f-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ddf4f-217">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="ddf4f-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddf4f-218">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="ddf4f-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddf4f-219">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="ddf4f-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf4f-220">Search-Flags</span></span>           | <span data-ttu-id="ddf4f-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddf4f-221">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="ddf4f-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf4f-222">System-Flags</span></span>           | <span data-ttu-id="ddf4f-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddf4f-223">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="ddf4f-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ddf4f-224">Classes used in</span></span>        | [<span data-ttu-id="ddf4f-225">**MSMQ-Migrated: usuario**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-225">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="ddf4f-226">**User**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ddf4f-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ddf4f-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ddf4f-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="ddf4f-228">Entry</span></span> | <span data-ttu-id="ddf4f-229">Value</span><span class="sxs-lookup"><span data-stu-id="ddf4f-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf4f-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ddf4f-230">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ddf4f-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddf4f-231">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ddf4f-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddf4f-232">System-Only</span></span>            | <span data-ttu-id="ddf4f-233">False</span><span class="sxs-lookup"><span data-stu-id="ddf4f-233">False</span></span>                                                                                         |
| <span data-ttu-id="ddf4f-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ddf4f-234">Is-Single-Valued</span></span>       | <span data-ttu-id="ddf4f-235">True</span><span class="sxs-lookup"><span data-stu-id="ddf4f-235">True</span></span>                                                                                          |
| <span data-ttu-id="ddf4f-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ddf4f-236">Is Indexed</span></span>             | <span data-ttu-id="ddf4f-237">False</span><span class="sxs-lookup"><span data-stu-id="ddf4f-237">False</span></span>                                                                                         |
| <span data-ttu-id="ddf4f-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ddf4f-238">In Global Catalog</span></span>      | <span data-ttu-id="ddf4f-239">True</span><span class="sxs-lookup"><span data-stu-id="ddf4f-239">True</span></span>                                                                                          |
| <span data-ttu-id="ddf4f-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ddf4f-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddf4f-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ddf4f-241">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="ddf4f-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddf4f-242">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="ddf4f-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddf4f-243">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="ddf4f-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf4f-244">Search-Flags</span></span>           | <span data-ttu-id="ddf4f-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddf4f-245">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="ddf4f-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf4f-246">System-Flags</span></span>           | <span data-ttu-id="ddf4f-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddf4f-247">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="ddf4f-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ddf4f-248">Classes used in</span></span>        | [<span data-ttu-id="ddf4f-249">**MSMQ-Migrated: usuario**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-249">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="ddf4f-250">**User**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-250">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ddf4f-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ddf4f-251">Windows Server 2012</span></span>



| <span data-ttu-id="ddf4f-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="ddf4f-252">Entry</span></span> | <span data-ttu-id="ddf4f-253">Value</span><span class="sxs-lookup"><span data-stu-id="ddf4f-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf4f-254">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ddf4f-254">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ddf4f-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddf4f-255">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ddf4f-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddf4f-256">System-Only</span></span>            | <span data-ttu-id="ddf4f-257">False</span><span class="sxs-lookup"><span data-stu-id="ddf4f-257">False</span></span>                                                                                         |
| <span data-ttu-id="ddf4f-258">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ddf4f-258">Is-Single-Valued</span></span>       | <span data-ttu-id="ddf4f-259">True</span><span class="sxs-lookup"><span data-stu-id="ddf4f-259">True</span></span>                                                                                          |
| <span data-ttu-id="ddf4f-260">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ddf4f-260">Is Indexed</span></span>             | <span data-ttu-id="ddf4f-261">False</span><span class="sxs-lookup"><span data-stu-id="ddf4f-261">False</span></span>                                                                                         |
| <span data-ttu-id="ddf4f-262">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ddf4f-262">In Global Catalog</span></span>      | <span data-ttu-id="ddf4f-263">True</span><span class="sxs-lookup"><span data-stu-id="ddf4f-263">True</span></span>                                                                                          |
| <span data-ttu-id="ddf4f-264">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ddf4f-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddf4f-265">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ddf4f-265">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="ddf4f-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddf4f-266">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="ddf4f-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddf4f-267">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="ddf4f-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf4f-268">Search-Flags</span></span>           | <span data-ttu-id="ddf4f-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddf4f-269">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="ddf4f-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf4f-270">System-Flags</span></span>           | <span data-ttu-id="ddf4f-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddf4f-271">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="ddf4f-272">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ddf4f-272">Classes used in</span></span>        | [<span data-ttu-id="ddf4f-273">**MSMQ-Migrated: usuario**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-273">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="ddf4f-274">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-274">**User**</span></span>](c-user.md)<br/> |



 

 





