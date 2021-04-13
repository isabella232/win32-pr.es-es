---
title: Schema-Info atributo)
description: Un valor binario interno que se usa para detectar los cambios de esquema entre controladores de archivos y forzar un ciclo de replicación de NC de esquema antes de replicar cualquier otro NC. Se utiliza para resolver los lazos cuando se asumi el esquema FSMO y se realiza un cambio en más de un controlador de dominio.
ms.assetid: 416cef3f-211b-439d-b177-267806c6a5d2
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Schema-Info
- schemaInfo esquema de AD de atributos
topic_type:
- apiref
api_name:
- Schema-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca55fc8ad3f53709b3819a7333e3470a1ac35cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536166"
---
# <a name="schema-info-attribute"></a><span data-ttu-id="c2164-106">Schema-Info atributo)</span><span class="sxs-lookup"><span data-stu-id="c2164-106">Schema-Info attribute</span></span>

<span data-ttu-id="c2164-107">Un valor binario interno que se usa para detectar los cambios de esquema entre controladores de archivos y forzar un ciclo de replicación de NC de esquema antes de replicar cualquier otro NC.</span><span class="sxs-lookup"><span data-stu-id="c2164-107">An internal binary value used to detect schema changes between DCs and force a schema NC replication cycle before replicating any other NC.</span></span> <span data-ttu-id="c2164-108">Se utiliza para resolver los lazos cuando se asumi el esquema FSMO y se realiza un cambio en más de un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="c2164-108">Used to resolve ties when the schema FSMO is seized and a change is made on more than one DC.</span></span>



| <span data-ttu-id="c2164-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2164-109">Entry</span></span> | <span data-ttu-id="c2164-110">Value</span><span class="sxs-lookup"><span data-stu-id="c2164-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="c2164-111">CN</span><span class="sxs-lookup"><span data-stu-id="c2164-111">CN</span></span>                | <span data-ttu-id="c2164-112">Schema-Info</span><span class="sxs-lookup"><span data-stu-id="c2164-112">Schema-Info</span></span>                                           |
| <span data-ttu-id="c2164-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="c2164-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c2164-114">schemaInfo</span><span class="sxs-lookup"><span data-stu-id="c2164-114">schemaInfo</span></span>                                            |
| <span data-ttu-id="c2164-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="c2164-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="c2164-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="c2164-116">Update Privilege</span></span>  | <span data-ttu-id="c2164-117">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="c2164-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="c2164-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="c2164-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="c2164-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c2164-119">Attribute-Id</span></span>      | <span data-ttu-id="c2164-120">1.2.840.113556.1.4.1358</span><span class="sxs-lookup"><span data-stu-id="c2164-120">1.2.840.113556.1.4.1358</span></span>                               |
| <span data-ttu-id="c2164-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c2164-121">System-Id-Guid</span></span>    | <span data-ttu-id="c2164-122">f9fb64ae-93b4-11d2-9945-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="c2164-122">f9fb64ae-93b4-11d2-9945-0000f87a57d4</span></span>                  |
| <span data-ttu-id="c2164-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2164-123">Syntax</span></span>            | [<span data-ttu-id="c2164-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="c2164-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="c2164-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="c2164-125">Implementations</span></span>

-   [<span data-ttu-id="c2164-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c2164-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c2164-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c2164-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c2164-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c2164-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c2164-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c2164-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c2164-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c2164-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c2164-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c2164-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c2164-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c2164-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c2164-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c2164-133">Windows 2000 Server</span></span>



| <span data-ttu-id="c2164-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2164-134">Entry</span></span> | <span data-ttu-id="c2164-135">Value</span><span class="sxs-lookup"><span data-stu-id="c2164-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c2164-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c2164-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c2164-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2164-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c2164-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2164-138">System-Only</span></span>            | <span data-ttu-id="c2164-139">True</span><span class="sxs-lookup"><span data-stu-id="c2164-139">True</span></span>                            |
| <span data-ttu-id="c2164-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c2164-140">Is-Single-Valued</span></span>       | <span data-ttu-id="c2164-141">False</span><span class="sxs-lookup"><span data-stu-id="c2164-141">False</span></span>                           |
| <span data-ttu-id="c2164-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c2164-142">Is Indexed</span></span>             | <span data-ttu-id="c2164-143">False</span><span class="sxs-lookup"><span data-stu-id="c2164-143">False</span></span>                           |
| <span data-ttu-id="c2164-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c2164-144">In Global Catalog</span></span>      | <span data-ttu-id="c2164-145">False</span><span class="sxs-lookup"><span data-stu-id="c2164-145">False</span></span>                           |
| <span data-ttu-id="c2164-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c2164-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2164-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c2164-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c2164-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2164-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c2164-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2164-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c2164-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2164-150">Search-Flags</span></span>           | <span data-ttu-id="c2164-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2164-151">0x00000000</span></span>                      |
| <span data-ttu-id="c2164-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2164-152">System-Flags</span></span>           | <span data-ttu-id="c2164-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2164-153">0x00000010</span></span>                      |
| <span data-ttu-id="c2164-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c2164-154">Classes used in</span></span>        | [<span data-ttu-id="c2164-155">**DMD**</span><span class="sxs-lookup"><span data-stu-id="c2164-155">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c2164-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c2164-156">Windows Server 2003</span></span>



| <span data-ttu-id="c2164-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2164-157">Entry</span></span> | <span data-ttu-id="c2164-158">Value</span><span class="sxs-lookup"><span data-stu-id="c2164-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c2164-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c2164-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c2164-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2164-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c2164-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2164-161">System-Only</span></span>            | <span data-ttu-id="c2164-162">True</span><span class="sxs-lookup"><span data-stu-id="c2164-162">True</span></span>                            |
| <span data-ttu-id="c2164-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c2164-163">Is-Single-Valued</span></span>       | <span data-ttu-id="c2164-164">False</span><span class="sxs-lookup"><span data-stu-id="c2164-164">False</span></span>                           |
| <span data-ttu-id="c2164-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c2164-165">Is Indexed</span></span>             | <span data-ttu-id="c2164-166">False</span><span class="sxs-lookup"><span data-stu-id="c2164-166">False</span></span>                           |
| <span data-ttu-id="c2164-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c2164-167">In Global Catalog</span></span>      | <span data-ttu-id="c2164-168">False</span><span class="sxs-lookup"><span data-stu-id="c2164-168">False</span></span>                           |
| <span data-ttu-id="c2164-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c2164-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2164-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c2164-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c2164-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2164-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c2164-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2164-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c2164-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2164-173">Search-Flags</span></span>           | <span data-ttu-id="c2164-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2164-174">0x00000000</span></span>                      |
| <span data-ttu-id="c2164-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2164-175">System-Flags</span></span>           | <span data-ttu-id="c2164-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2164-176">0x00000010</span></span>                      |
| <span data-ttu-id="c2164-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c2164-177">Classes used in</span></span>        | [<span data-ttu-id="c2164-178">**DMD**</span><span class="sxs-lookup"><span data-stu-id="c2164-178">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c2164-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="c2164-179">ADAM</span></span>



| <span data-ttu-id="c2164-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2164-180">Entry</span></span> | <span data-ttu-id="c2164-181">Value</span><span class="sxs-lookup"><span data-stu-id="c2164-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c2164-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c2164-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c2164-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2164-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c2164-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2164-184">System-Only</span></span>            | <span data-ttu-id="c2164-185">True</span><span class="sxs-lookup"><span data-stu-id="c2164-185">True</span></span>                            |
| <span data-ttu-id="c2164-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c2164-186">Is-Single-Valued</span></span>       | <span data-ttu-id="c2164-187">False</span><span class="sxs-lookup"><span data-stu-id="c2164-187">False</span></span>                           |
| <span data-ttu-id="c2164-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c2164-188">Is Indexed</span></span>             | <span data-ttu-id="c2164-189">False</span><span class="sxs-lookup"><span data-stu-id="c2164-189">False</span></span>                           |
| <span data-ttu-id="c2164-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c2164-190">In Global Catalog</span></span>      | <span data-ttu-id="c2164-191">False</span><span class="sxs-lookup"><span data-stu-id="c2164-191">False</span></span>                           |
| <span data-ttu-id="c2164-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c2164-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2164-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c2164-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c2164-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2164-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c2164-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2164-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c2164-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2164-196">Search-Flags</span></span>           | <span data-ttu-id="c2164-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2164-197">0x00000000</span></span>                      |
| <span data-ttu-id="c2164-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2164-198">System-Flags</span></span>           | <span data-ttu-id="c2164-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2164-199">0x00000010</span></span>                      |
| <span data-ttu-id="c2164-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c2164-200">Classes used in</span></span>        | [<span data-ttu-id="c2164-201">**DMD**</span><span class="sxs-lookup"><span data-stu-id="c2164-201">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c2164-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c2164-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c2164-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2164-203">Entry</span></span> | <span data-ttu-id="c2164-204">Value</span><span class="sxs-lookup"><span data-stu-id="c2164-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c2164-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c2164-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c2164-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2164-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c2164-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2164-207">System-Only</span></span>            | <span data-ttu-id="c2164-208">True</span><span class="sxs-lookup"><span data-stu-id="c2164-208">True</span></span>                            |
| <span data-ttu-id="c2164-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c2164-209">Is-Single-Valued</span></span>       | <span data-ttu-id="c2164-210">False</span><span class="sxs-lookup"><span data-stu-id="c2164-210">False</span></span>                           |
| <span data-ttu-id="c2164-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c2164-211">Is Indexed</span></span>             | <span data-ttu-id="c2164-212">False</span><span class="sxs-lookup"><span data-stu-id="c2164-212">False</span></span>                           |
| <span data-ttu-id="c2164-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c2164-213">In Global Catalog</span></span>      | <span data-ttu-id="c2164-214">False</span><span class="sxs-lookup"><span data-stu-id="c2164-214">False</span></span>                           |
| <span data-ttu-id="c2164-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c2164-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2164-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c2164-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c2164-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2164-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c2164-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2164-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c2164-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2164-219">Search-Flags</span></span>           | <span data-ttu-id="c2164-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2164-220">0x00000000</span></span>                      |
| <span data-ttu-id="c2164-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2164-221">System-Flags</span></span>           | <span data-ttu-id="c2164-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2164-222">0x00000010</span></span>                      |
| <span data-ttu-id="c2164-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c2164-223">Classes used in</span></span>        | [<span data-ttu-id="c2164-224">**DMD**</span><span class="sxs-lookup"><span data-stu-id="c2164-224">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c2164-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2164-225">Windows Server 2008</span></span>



| <span data-ttu-id="c2164-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2164-226">Entry</span></span> | <span data-ttu-id="c2164-227">Value</span><span class="sxs-lookup"><span data-stu-id="c2164-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c2164-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c2164-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c2164-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2164-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c2164-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2164-230">System-Only</span></span>            | <span data-ttu-id="c2164-231">True</span><span class="sxs-lookup"><span data-stu-id="c2164-231">True</span></span>                            |
| <span data-ttu-id="c2164-232">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c2164-232">Is-Single-Valued</span></span>       | <span data-ttu-id="c2164-233">False</span><span class="sxs-lookup"><span data-stu-id="c2164-233">False</span></span>                           |
| <span data-ttu-id="c2164-234">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c2164-234">Is Indexed</span></span>             | <span data-ttu-id="c2164-235">False</span><span class="sxs-lookup"><span data-stu-id="c2164-235">False</span></span>                           |
| <span data-ttu-id="c2164-236">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c2164-236">In Global Catalog</span></span>      | <span data-ttu-id="c2164-237">False</span><span class="sxs-lookup"><span data-stu-id="c2164-237">False</span></span>                           |
| <span data-ttu-id="c2164-238">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c2164-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2164-239">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c2164-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c2164-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2164-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c2164-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2164-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c2164-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2164-242">Search-Flags</span></span>           | <span data-ttu-id="c2164-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2164-243">0x00000000</span></span>                      |
| <span data-ttu-id="c2164-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2164-244">System-Flags</span></span>           | <span data-ttu-id="c2164-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2164-245">0x00000010</span></span>                      |
| <span data-ttu-id="c2164-246">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c2164-246">Classes used in</span></span>        | [<span data-ttu-id="c2164-247">**DMD**</span><span class="sxs-lookup"><span data-stu-id="c2164-247">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c2164-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2164-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c2164-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2164-249">Entry</span></span> | <span data-ttu-id="c2164-250">Value</span><span class="sxs-lookup"><span data-stu-id="c2164-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c2164-251">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c2164-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c2164-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2164-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c2164-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2164-253">System-Only</span></span>            | <span data-ttu-id="c2164-254">True</span><span class="sxs-lookup"><span data-stu-id="c2164-254">True</span></span>                            |
| <span data-ttu-id="c2164-255">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c2164-255">Is-Single-Valued</span></span>       | <span data-ttu-id="c2164-256">False</span><span class="sxs-lookup"><span data-stu-id="c2164-256">False</span></span>                           |
| <span data-ttu-id="c2164-257">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c2164-257">Is Indexed</span></span>             | <span data-ttu-id="c2164-258">False</span><span class="sxs-lookup"><span data-stu-id="c2164-258">False</span></span>                           |
| <span data-ttu-id="c2164-259">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c2164-259">In Global Catalog</span></span>      | <span data-ttu-id="c2164-260">False</span><span class="sxs-lookup"><span data-stu-id="c2164-260">False</span></span>                           |
| <span data-ttu-id="c2164-261">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c2164-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2164-262">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c2164-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c2164-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2164-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c2164-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2164-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c2164-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2164-265">Search-Flags</span></span>           | <span data-ttu-id="c2164-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2164-266">0x00000000</span></span>                      |
| <span data-ttu-id="c2164-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2164-267">System-Flags</span></span>           | <span data-ttu-id="c2164-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2164-268">0x00000010</span></span>                      |
| <span data-ttu-id="c2164-269">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c2164-269">Classes used in</span></span>        | [<span data-ttu-id="c2164-270">**DMD**</span><span class="sxs-lookup"><span data-stu-id="c2164-270">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c2164-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c2164-271">Windows Server 2012</span></span>



| <span data-ttu-id="c2164-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2164-272">Entry</span></span> | <span data-ttu-id="c2164-273">Value</span><span class="sxs-lookup"><span data-stu-id="c2164-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c2164-274">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c2164-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c2164-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2164-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c2164-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2164-276">System-Only</span></span>            | <span data-ttu-id="c2164-277">True</span><span class="sxs-lookup"><span data-stu-id="c2164-277">True</span></span>                            |
| <span data-ttu-id="c2164-278">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c2164-278">Is-Single-Valued</span></span>       | <span data-ttu-id="c2164-279">False</span><span class="sxs-lookup"><span data-stu-id="c2164-279">False</span></span>                           |
| <span data-ttu-id="c2164-280">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c2164-280">Is Indexed</span></span>             | <span data-ttu-id="c2164-281">False</span><span class="sxs-lookup"><span data-stu-id="c2164-281">False</span></span>                           |
| <span data-ttu-id="c2164-282">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c2164-282">In Global Catalog</span></span>      | <span data-ttu-id="c2164-283">False</span><span class="sxs-lookup"><span data-stu-id="c2164-283">False</span></span>                           |
| <span data-ttu-id="c2164-284">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c2164-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2164-285">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c2164-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c2164-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2164-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c2164-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2164-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c2164-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2164-288">Search-Flags</span></span>           | <span data-ttu-id="c2164-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2164-289">0x00000000</span></span>                      |
| <span data-ttu-id="c2164-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2164-290">System-Flags</span></span>           | <span data-ttu-id="c2164-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2164-291">0x00000010</span></span>                      |
| <span data-ttu-id="c2164-292">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c2164-292">Classes used in</span></span>        | [<span data-ttu-id="c2164-293">**DMD**</span><span class="sxs-lookup"><span data-stu-id="c2164-293">**DMD**</span></span>](c-dmd.md)<br/> |



 

 





