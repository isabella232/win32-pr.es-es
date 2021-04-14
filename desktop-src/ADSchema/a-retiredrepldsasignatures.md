---
title: Retiród-REPL-DSA-signaturas (atributo)
description: Realiza el seguimiento de las identidades de replicación de DS pasadas de un controlador de dominio determinado.
ms.assetid: 82e8b222-5635-41ad-b2ab-386c9e6aa280
ms.tgt_platform: multiple
keywords:
- Retiród-REPL-DSA-signaturas atributo AD Schema
- retiredReplDSASignatures esquema de AD de atributos
topic_type:
- apiref
api_name:
- Retired-Repl-DSA-Signatures
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a9a4cb4030a8d3aa24244bc2e7a2702e83686fc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104422699"
---
# <a name="retired-repl-dsa-signatures-attribute"></a><span data-ttu-id="d5b23-105">Retiród-REPL-DSA-signaturas (atributo)</span><span class="sxs-lookup"><span data-stu-id="d5b23-105">Retired-Repl-DSA-Signatures attribute</span></span>

<span data-ttu-id="d5b23-106">Realiza el seguimiento de las identidades de replicación de DS pasadas de un controlador de dominio determinado.</span><span class="sxs-lookup"><span data-stu-id="d5b23-106">Tracks the past DS replication identities of a given DC.</span></span>



| <span data-ttu-id="d5b23-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5b23-107">Entry</span></span> | <span data-ttu-id="d5b23-108">Value</span><span class="sxs-lookup"><span data-stu-id="d5b23-108">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d5b23-109">CN</span><span class="sxs-lookup"><span data-stu-id="d5b23-109">CN</span></span>                | <span data-ttu-id="d5b23-110">Retiradas-REPL-DSA-firmas</span><span class="sxs-lookup"><span data-stu-id="d5b23-110">Retired-Repl-DSA-Signatures</span></span>                                                         |
| <span data-ttu-id="d5b23-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="d5b23-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d5b23-112">retiredReplDSASignatures</span><span class="sxs-lookup"><span data-stu-id="d5b23-112">retiredReplDSASignatures</span></span>                                                            |
| <span data-ttu-id="d5b23-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="d5b23-113">Size</span></span>              | <span data-ttu-id="d5b23-114">La longitud es proporcional al número de veces que se ha restaurado el controlador de dominio desde la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d5b23-114">Length is proportional to the number of times the DC has been restored from backup.</span></span> |
| <span data-ttu-id="d5b23-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="d5b23-115">Update Privilege</span></span>  | <span data-ttu-id="d5b23-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="d5b23-116">This value is set by the system.</span></span>                                                    |
| <span data-ttu-id="d5b23-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="d5b23-117">Update Frequency</span></span>  | \-                                                                                  |
| <span data-ttu-id="d5b23-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d5b23-118">Attribute-Id</span></span>      | <span data-ttu-id="d5b23-119">1.2.840.113556.1.4.673</span><span class="sxs-lookup"><span data-stu-id="d5b23-119">1.2.840.113556.1.4.673</span></span>                                                              |
| <span data-ttu-id="d5b23-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d5b23-120">System-Id-Guid</span></span>    | <span data-ttu-id="d5b23-121">7bfdcb7f-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d5b23-121">7bfdcb7f-4807-11d1-a9c3-0000f80367c1</span></span>                                                |
| <span data-ttu-id="d5b23-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5b23-122">Syntax</span></span>            | [<span data-ttu-id="d5b23-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="d5b23-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                               |



## <a name="implementations"></a><span data-ttu-id="d5b23-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="d5b23-124">Implementations</span></span>

-   [<span data-ttu-id="d5b23-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d5b23-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d5b23-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d5b23-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d5b23-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d5b23-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d5b23-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d5b23-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d5b23-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d5b23-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d5b23-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d5b23-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d5b23-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d5b23-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d5b23-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d5b23-132">Windows 2000 Server</span></span>



| <span data-ttu-id="d5b23-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5b23-133">Entry</span></span> | <span data-ttu-id="d5b23-134">Value</span><span class="sxs-lookup"><span data-stu-id="d5b23-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="d5b23-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5b23-135">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="d5b23-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5b23-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="d5b23-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5b23-137">System-Only</span></span>            | <span data-ttu-id="d5b23-138">True</span><span class="sxs-lookup"><span data-stu-id="d5b23-138">True</span></span>                                     |
| <span data-ttu-id="d5b23-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5b23-139">Is-Single-Valued</span></span>       | <span data-ttu-id="d5b23-140">True</span><span class="sxs-lookup"><span data-stu-id="d5b23-140">True</span></span>                                     |
| <span data-ttu-id="d5b23-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5b23-141">Is Indexed</span></span>             | <span data-ttu-id="d5b23-142">False</span><span class="sxs-lookup"><span data-stu-id="d5b23-142">False</span></span>                                    |
| <span data-ttu-id="d5b23-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5b23-143">In Global Catalog</span></span>      | <span data-ttu-id="d5b23-144">False</span><span class="sxs-lookup"><span data-stu-id="d5b23-144">False</span></span>                                    |
| <span data-ttu-id="d5b23-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5b23-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5b23-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5b23-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="d5b23-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5b23-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="d5b23-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5b23-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="d5b23-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5b23-149">Search-Flags</span></span>           | <span data-ttu-id="d5b23-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5b23-150">0x00000000</span></span>                               |
| <span data-ttu-id="d5b23-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5b23-151">System-Flags</span></span>           | <span data-ttu-id="d5b23-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5b23-152">0x00000010</span></span>                               |
| <span data-ttu-id="d5b23-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5b23-153">Classes used in</span></span>        | [<span data-ttu-id="d5b23-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="d5b23-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d5b23-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d5b23-155">Windows Server 2003</span></span>



| <span data-ttu-id="d5b23-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5b23-156">Entry</span></span> | <span data-ttu-id="d5b23-157">Value</span><span class="sxs-lookup"><span data-stu-id="d5b23-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="d5b23-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5b23-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="d5b23-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5b23-159">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="d5b23-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5b23-160">System-Only</span></span>            | <span data-ttu-id="d5b23-161">True</span><span class="sxs-lookup"><span data-stu-id="d5b23-161">True</span></span>                                     |
| <span data-ttu-id="d5b23-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5b23-162">Is-Single-Valued</span></span>       | <span data-ttu-id="d5b23-163">True</span><span class="sxs-lookup"><span data-stu-id="d5b23-163">True</span></span>                                     |
| <span data-ttu-id="d5b23-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5b23-164">Is Indexed</span></span>             | <span data-ttu-id="d5b23-165">False</span><span class="sxs-lookup"><span data-stu-id="d5b23-165">False</span></span>                                    |
| <span data-ttu-id="d5b23-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5b23-166">In Global Catalog</span></span>      | <span data-ttu-id="d5b23-167">False</span><span class="sxs-lookup"><span data-stu-id="d5b23-167">False</span></span>                                    |
| <span data-ttu-id="d5b23-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5b23-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5b23-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5b23-169">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="d5b23-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5b23-170">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="d5b23-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5b23-171">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="d5b23-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5b23-172">Search-Flags</span></span>           | <span data-ttu-id="d5b23-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5b23-173">0x00000000</span></span>                               |
| <span data-ttu-id="d5b23-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5b23-174">System-Flags</span></span>           | <span data-ttu-id="d5b23-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5b23-175">0x00000010</span></span>                               |
| <span data-ttu-id="d5b23-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5b23-176">Classes used in</span></span>        | [<span data-ttu-id="d5b23-177">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="d5b23-177">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d5b23-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="d5b23-178">ADAM</span></span>



| <span data-ttu-id="d5b23-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5b23-179">Entry</span></span> | <span data-ttu-id="d5b23-180">Value</span><span class="sxs-lookup"><span data-stu-id="d5b23-180">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="d5b23-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5b23-181">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="d5b23-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5b23-182">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="d5b23-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5b23-183">System-Only</span></span>            | <span data-ttu-id="d5b23-184">True</span><span class="sxs-lookup"><span data-stu-id="d5b23-184">True</span></span>                                     |
| <span data-ttu-id="d5b23-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5b23-185">Is-Single-Valued</span></span>       | <span data-ttu-id="d5b23-186">True</span><span class="sxs-lookup"><span data-stu-id="d5b23-186">True</span></span>                                     |
| <span data-ttu-id="d5b23-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5b23-187">Is Indexed</span></span>             | <span data-ttu-id="d5b23-188">False</span><span class="sxs-lookup"><span data-stu-id="d5b23-188">False</span></span>                                    |
| <span data-ttu-id="d5b23-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5b23-189">In Global Catalog</span></span>      | <span data-ttu-id="d5b23-190">False</span><span class="sxs-lookup"><span data-stu-id="d5b23-190">False</span></span>                                    |
| <span data-ttu-id="d5b23-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5b23-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5b23-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5b23-192">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="d5b23-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5b23-193">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="d5b23-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5b23-194">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="d5b23-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5b23-195">Search-Flags</span></span>           | <span data-ttu-id="d5b23-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5b23-196">0x00000000</span></span>                               |
| <span data-ttu-id="d5b23-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5b23-197">System-Flags</span></span>           | <span data-ttu-id="d5b23-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5b23-198">0x00000010</span></span>                               |
| <span data-ttu-id="d5b23-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5b23-199">Classes used in</span></span>        | [<span data-ttu-id="d5b23-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="d5b23-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d5b23-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d5b23-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d5b23-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5b23-202">Entry</span></span> | <span data-ttu-id="d5b23-203">Value</span><span class="sxs-lookup"><span data-stu-id="d5b23-203">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="d5b23-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5b23-204">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="d5b23-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5b23-205">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="d5b23-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5b23-206">System-Only</span></span>            | <span data-ttu-id="d5b23-207">True</span><span class="sxs-lookup"><span data-stu-id="d5b23-207">True</span></span>                                     |
| <span data-ttu-id="d5b23-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5b23-208">Is-Single-Valued</span></span>       | <span data-ttu-id="d5b23-209">True</span><span class="sxs-lookup"><span data-stu-id="d5b23-209">True</span></span>                                     |
| <span data-ttu-id="d5b23-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5b23-210">Is Indexed</span></span>             | <span data-ttu-id="d5b23-211">False</span><span class="sxs-lookup"><span data-stu-id="d5b23-211">False</span></span>                                    |
| <span data-ttu-id="d5b23-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5b23-212">In Global Catalog</span></span>      | <span data-ttu-id="d5b23-213">False</span><span class="sxs-lookup"><span data-stu-id="d5b23-213">False</span></span>                                    |
| <span data-ttu-id="d5b23-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5b23-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5b23-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5b23-215">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="d5b23-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5b23-216">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="d5b23-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5b23-217">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="d5b23-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5b23-218">Search-Flags</span></span>           | <span data-ttu-id="d5b23-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5b23-219">0x00000000</span></span>                               |
| <span data-ttu-id="d5b23-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5b23-220">System-Flags</span></span>           | <span data-ttu-id="d5b23-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5b23-221">0x00000010</span></span>                               |
| <span data-ttu-id="d5b23-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5b23-222">Classes used in</span></span>        | [<span data-ttu-id="d5b23-223">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="d5b23-223">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d5b23-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5b23-224">Windows Server 2008</span></span>



| <span data-ttu-id="d5b23-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5b23-225">Entry</span></span> | <span data-ttu-id="d5b23-226">Value</span><span class="sxs-lookup"><span data-stu-id="d5b23-226">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="d5b23-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5b23-227">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="d5b23-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5b23-228">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="d5b23-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5b23-229">System-Only</span></span>            | <span data-ttu-id="d5b23-230">True</span><span class="sxs-lookup"><span data-stu-id="d5b23-230">True</span></span>                                     |
| <span data-ttu-id="d5b23-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5b23-231">Is-Single-Valued</span></span>       | <span data-ttu-id="d5b23-232">True</span><span class="sxs-lookup"><span data-stu-id="d5b23-232">True</span></span>                                     |
| <span data-ttu-id="d5b23-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5b23-233">Is Indexed</span></span>             | <span data-ttu-id="d5b23-234">False</span><span class="sxs-lookup"><span data-stu-id="d5b23-234">False</span></span>                                    |
| <span data-ttu-id="d5b23-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5b23-235">In Global Catalog</span></span>      | <span data-ttu-id="d5b23-236">False</span><span class="sxs-lookup"><span data-stu-id="d5b23-236">False</span></span>                                    |
| <span data-ttu-id="d5b23-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5b23-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5b23-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5b23-238">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="d5b23-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5b23-239">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="d5b23-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5b23-240">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="d5b23-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5b23-241">Search-Flags</span></span>           | <span data-ttu-id="d5b23-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5b23-242">0x00000000</span></span>                               |
| <span data-ttu-id="d5b23-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5b23-243">System-Flags</span></span>           | <span data-ttu-id="d5b23-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5b23-244">0x00000010</span></span>                               |
| <span data-ttu-id="d5b23-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5b23-245">Classes used in</span></span>        | [<span data-ttu-id="d5b23-246">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="d5b23-246">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d5b23-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d5b23-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d5b23-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5b23-248">Entry</span></span> | <span data-ttu-id="d5b23-249">Value</span><span class="sxs-lookup"><span data-stu-id="d5b23-249">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="d5b23-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5b23-250">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="d5b23-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5b23-251">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="d5b23-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5b23-252">System-Only</span></span>            | <span data-ttu-id="d5b23-253">True</span><span class="sxs-lookup"><span data-stu-id="d5b23-253">True</span></span>                                     |
| <span data-ttu-id="d5b23-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5b23-254">Is-Single-Valued</span></span>       | <span data-ttu-id="d5b23-255">True</span><span class="sxs-lookup"><span data-stu-id="d5b23-255">True</span></span>                                     |
| <span data-ttu-id="d5b23-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5b23-256">Is Indexed</span></span>             | <span data-ttu-id="d5b23-257">False</span><span class="sxs-lookup"><span data-stu-id="d5b23-257">False</span></span>                                    |
| <span data-ttu-id="d5b23-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5b23-258">In Global Catalog</span></span>      | <span data-ttu-id="d5b23-259">False</span><span class="sxs-lookup"><span data-stu-id="d5b23-259">False</span></span>                                    |
| <span data-ttu-id="d5b23-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5b23-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5b23-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5b23-261">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="d5b23-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5b23-262">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="d5b23-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5b23-263">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="d5b23-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5b23-264">Search-Flags</span></span>           | <span data-ttu-id="d5b23-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5b23-265">0x00000000</span></span>                               |
| <span data-ttu-id="d5b23-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5b23-266">System-Flags</span></span>           | <span data-ttu-id="d5b23-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5b23-267">0x00000010</span></span>                               |
| <span data-ttu-id="d5b23-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5b23-268">Classes used in</span></span>        | [<span data-ttu-id="d5b23-269">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="d5b23-269">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d5b23-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d5b23-270">Windows Server 2012</span></span>



| <span data-ttu-id="d5b23-271">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5b23-271">Entry</span></span> | <span data-ttu-id="d5b23-272">Value</span><span class="sxs-lookup"><span data-stu-id="d5b23-272">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="d5b23-273">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5b23-273">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="d5b23-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5b23-274">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="d5b23-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5b23-275">System-Only</span></span>            | <span data-ttu-id="d5b23-276">True</span><span class="sxs-lookup"><span data-stu-id="d5b23-276">True</span></span>                                     |
| <span data-ttu-id="d5b23-277">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5b23-277">Is-Single-Valued</span></span>       | <span data-ttu-id="d5b23-278">True</span><span class="sxs-lookup"><span data-stu-id="d5b23-278">True</span></span>                                     |
| <span data-ttu-id="d5b23-279">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5b23-279">Is Indexed</span></span>             | <span data-ttu-id="d5b23-280">False</span><span class="sxs-lookup"><span data-stu-id="d5b23-280">False</span></span>                                    |
| <span data-ttu-id="d5b23-281">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5b23-281">In Global Catalog</span></span>      | <span data-ttu-id="d5b23-282">False</span><span class="sxs-lookup"><span data-stu-id="d5b23-282">False</span></span>                                    |
| <span data-ttu-id="d5b23-283">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5b23-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5b23-284">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5b23-284">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="d5b23-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5b23-285">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="d5b23-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5b23-286">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="d5b23-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5b23-287">Search-Flags</span></span>           | <span data-ttu-id="d5b23-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5b23-288">0x00000000</span></span>                               |
| <span data-ttu-id="d5b23-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5b23-289">System-Flags</span></span>           | <span data-ttu-id="d5b23-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5b23-290">0x00000010</span></span>                               |
| <span data-ttu-id="d5b23-291">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5b23-291">Classes used in</span></span>        | [<span data-ttu-id="d5b23-292">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="d5b23-292">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





