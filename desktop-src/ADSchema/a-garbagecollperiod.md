---
title: Atributo Garbage-COLLATE-period
description: Este atributo se encuentra en el servicio de directorio CN, CN Windows NT, CN Services, CN Configuration,... objeto. Representa el tiempo, en horas, entre ejecuciones de recolección de elementos no utilizados de DS.
ms.assetid: 982a75f9-04b5-489e-99b3-a9fd3fb280c8
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo Garbage-COLLATE-period
- garbageCollPeriod esquema de AD de atributos
topic_type:
- apiref
api_name:
- Garbage-Coll-Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64890df97cf4c131ad0dcdbed8cb80bf20b66a83
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658521"
---
# <a name="garbage-coll-period-attribute"></a><span data-ttu-id="f3712-106">Atributo Garbage-COLLATE-period</span><span class="sxs-lookup"><span data-stu-id="f3712-106">Garbage-Coll-Period attribute</span></span>

<span data-ttu-id="f3712-107">Este atributo se encuentra en el CN = Directory Service, CN = Windows NT, CN = Services, CN = Configuration,... objeto.</span><span class="sxs-lookup"><span data-stu-id="f3712-107">This attribute is located on the CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,... object.</span></span> <span data-ttu-id="f3712-108">Representa el tiempo, en horas, entre ejecuciones de recolección de elementos no utilizados de DS.</span><span class="sxs-lookup"><span data-stu-id="f3712-108">It represents the time, in hours, between DS garbage collection runs.</span></span>



| <span data-ttu-id="f3712-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3712-109">Entry</span></span> | <span data-ttu-id="f3712-110">Value</span><span class="sxs-lookup"><span data-stu-id="f3712-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f3712-111">CN</span><span class="sxs-lookup"><span data-stu-id="f3712-111">CN</span></span>                | <span data-ttu-id="f3712-112">Tiempo de intercalación de elementos no utilizados</span><span class="sxs-lookup"><span data-stu-id="f3712-112">Garbage-Coll-Period</span></span>                  |
| <span data-ttu-id="f3712-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="f3712-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f3712-114">garbageCollPeriod</span><span class="sxs-lookup"><span data-stu-id="f3712-114">garbageCollPeriod</span></span>                    |
| <span data-ttu-id="f3712-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f3712-115">Size</span></span>              | <span data-ttu-id="f3712-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="f3712-116">4 bytes</span></span>                              |
| <span data-ttu-id="f3712-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="f3712-117">Update Privilege</span></span>  | <span data-ttu-id="f3712-118">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="f3712-118">Domain administrator</span></span>                 |
| <span data-ttu-id="f3712-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="f3712-119">Update Frequency</span></span>  | <span data-ttu-id="f3712-120">Muy poco frecuente.</span><span class="sxs-lookup"><span data-stu-id="f3712-120">Very rare.</span></span>                           |
| <span data-ttu-id="f3712-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f3712-121">Attribute-Id</span></span>      | <span data-ttu-id="f3712-122">1.2.840.113556.1.2.301</span><span class="sxs-lookup"><span data-stu-id="f3712-122">1.2.840.113556.1.2.301</span></span>               |
| <span data-ttu-id="f3712-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f3712-123">System-Id-Guid</span></span>    | <span data-ttu-id="f3712-124">5fd424a1-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="f3712-124">5fd424a1-1262-11d0-a060-00aa006c33ed</span></span> |
| <span data-ttu-id="f3712-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3712-125">Syntax</span></span>            | [<span data-ttu-id="f3712-126">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="f3712-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="f3712-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="f3712-127">Implementations</span></span>

-   [<span data-ttu-id="f3712-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f3712-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f3712-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f3712-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f3712-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f3712-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f3712-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f3712-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f3712-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f3712-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f3712-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f3712-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f3712-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f3712-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f3712-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f3712-135">Windows 2000 Server</span></span>



| <span data-ttu-id="f3712-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3712-136">Entry</span></span> | <span data-ttu-id="f3712-137">Value</span><span class="sxs-lookup"><span data-stu-id="f3712-137">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3712-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f3712-138">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="f3712-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3712-139">MAPI-Id</span></span>                | <span data-ttu-id="f3712-140">0x80AF</span><span class="sxs-lookup"><span data-stu-id="f3712-140">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="f3712-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3712-141">System-Only</span></span>            | <span data-ttu-id="f3712-142">False</span><span class="sxs-lookup"><span data-stu-id="f3712-142">False</span></span>                                                                                                 |
| <span data-ttu-id="f3712-143">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f3712-143">Is-Single-Valued</span></span>       | <span data-ttu-id="f3712-144">True</span><span class="sxs-lookup"><span data-stu-id="f3712-144">True</span></span>                                                                                                  |
| <span data-ttu-id="f3712-145">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f3712-145">Is Indexed</span></span>             | <span data-ttu-id="f3712-146">False</span><span class="sxs-lookup"><span data-stu-id="f3712-146">False</span></span>                                                                                                 |
| <span data-ttu-id="f3712-147">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3712-147">In Global Catalog</span></span>      | <span data-ttu-id="f3712-148">False</span><span class="sxs-lookup"><span data-stu-id="f3712-148">False</span></span>                                                                                                 |
| <span data-ttu-id="f3712-149">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f3712-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3712-150">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3712-150">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="f3712-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3712-151">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="f3712-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3712-152">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="f3712-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3712-153">Search-Flags</span></span>           | <span data-ttu-id="f3712-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3712-154">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="f3712-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3712-155">System-Flags</span></span>           | <span data-ttu-id="f3712-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3712-156">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="f3712-157">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f3712-157">Classes used in</span></span>        | [<span data-ttu-id="f3712-158">**Destinatario de correo**</span><span class="sxs-lookup"><span data-stu-id="f3712-158">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="f3712-159">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="f3712-159">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f3712-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f3712-160">Windows Server 2003</span></span>



| <span data-ttu-id="f3712-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3712-161">Entry</span></span> | <span data-ttu-id="f3712-162">Value</span><span class="sxs-lookup"><span data-stu-id="f3712-162">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3712-163">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f3712-163">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="f3712-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3712-164">MAPI-Id</span></span>                | <span data-ttu-id="f3712-165">0x80AF</span><span class="sxs-lookup"><span data-stu-id="f3712-165">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="f3712-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3712-166">System-Only</span></span>            | <span data-ttu-id="f3712-167">False</span><span class="sxs-lookup"><span data-stu-id="f3712-167">False</span></span>                                                                                                 |
| <span data-ttu-id="f3712-168">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f3712-168">Is-Single-Valued</span></span>       | <span data-ttu-id="f3712-169">True</span><span class="sxs-lookup"><span data-stu-id="f3712-169">True</span></span>                                                                                                  |
| <span data-ttu-id="f3712-170">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f3712-170">Is Indexed</span></span>             | <span data-ttu-id="f3712-171">False</span><span class="sxs-lookup"><span data-stu-id="f3712-171">False</span></span>                                                                                                 |
| <span data-ttu-id="f3712-172">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3712-172">In Global Catalog</span></span>      | <span data-ttu-id="f3712-173">False</span><span class="sxs-lookup"><span data-stu-id="f3712-173">False</span></span>                                                                                                 |
| <span data-ttu-id="f3712-174">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f3712-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3712-175">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3712-175">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="f3712-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3712-176">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="f3712-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3712-177">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="f3712-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3712-178">Search-Flags</span></span>           | <span data-ttu-id="f3712-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3712-179">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="f3712-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3712-180">System-Flags</span></span>           | <span data-ttu-id="f3712-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3712-181">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="f3712-182">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f3712-182">Classes used in</span></span>        | [<span data-ttu-id="f3712-183">**Destinatario de correo**</span><span class="sxs-lookup"><span data-stu-id="f3712-183">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="f3712-184">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="f3712-184">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f3712-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="f3712-185">ADAM</span></span>



| <span data-ttu-id="f3712-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3712-186">Entry</span></span> | <span data-ttu-id="f3712-187">Value</span><span class="sxs-lookup"><span data-stu-id="f3712-187">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="f3712-188">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f3712-188">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="f3712-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3712-189">MAPI-Id</span></span>                | <span data-ttu-id="f3712-190">0x80AF</span><span class="sxs-lookup"><span data-stu-id="f3712-190">0x80AF</span></span>                                           |
| <span data-ttu-id="f3712-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3712-191">System-Only</span></span>            | <span data-ttu-id="f3712-192">False</span><span class="sxs-lookup"><span data-stu-id="f3712-192">False</span></span>                                            |
| <span data-ttu-id="f3712-193">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f3712-193">Is-Single-Valued</span></span>       | <span data-ttu-id="f3712-194">True</span><span class="sxs-lookup"><span data-stu-id="f3712-194">True</span></span>                                             |
| <span data-ttu-id="f3712-195">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f3712-195">Is Indexed</span></span>             | <span data-ttu-id="f3712-196">False</span><span class="sxs-lookup"><span data-stu-id="f3712-196">False</span></span>                                            |
| <span data-ttu-id="f3712-197">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3712-197">In Global Catalog</span></span>      | <span data-ttu-id="f3712-198">False</span><span class="sxs-lookup"><span data-stu-id="f3712-198">False</span></span>                                            |
| <span data-ttu-id="f3712-199">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f3712-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3712-200">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3712-200">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="f3712-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3712-201">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="f3712-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3712-202">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="f3712-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3712-203">Search-Flags</span></span>           | <span data-ttu-id="f3712-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3712-204">0x00000000</span></span>                                       |
| <span data-ttu-id="f3712-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3712-205">System-Flags</span></span>           | <span data-ttu-id="f3712-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3712-206">0x00000010</span></span>                                       |
| <span data-ttu-id="f3712-207">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f3712-207">Classes used in</span></span>        | [<span data-ttu-id="f3712-208">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="f3712-208">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f3712-209">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f3712-209">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f3712-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3712-210">Entry</span></span> | <span data-ttu-id="f3712-211">Value</span><span class="sxs-lookup"><span data-stu-id="f3712-211">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3712-212">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f3712-212">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="f3712-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3712-213">MAPI-Id</span></span>                | <span data-ttu-id="f3712-214">0x80AF</span><span class="sxs-lookup"><span data-stu-id="f3712-214">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="f3712-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3712-215">System-Only</span></span>            | <span data-ttu-id="f3712-216">False</span><span class="sxs-lookup"><span data-stu-id="f3712-216">False</span></span>                                                                                                 |
| <span data-ttu-id="f3712-217">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f3712-217">Is-Single-Valued</span></span>       | <span data-ttu-id="f3712-218">True</span><span class="sxs-lookup"><span data-stu-id="f3712-218">True</span></span>                                                                                                  |
| <span data-ttu-id="f3712-219">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f3712-219">Is Indexed</span></span>             | <span data-ttu-id="f3712-220">False</span><span class="sxs-lookup"><span data-stu-id="f3712-220">False</span></span>                                                                                                 |
| <span data-ttu-id="f3712-221">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3712-221">In Global Catalog</span></span>      | <span data-ttu-id="f3712-222">False</span><span class="sxs-lookup"><span data-stu-id="f3712-222">False</span></span>                                                                                                 |
| <span data-ttu-id="f3712-223">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f3712-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3712-224">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3712-224">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="f3712-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3712-225">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="f3712-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3712-226">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="f3712-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3712-227">Search-Flags</span></span>           | <span data-ttu-id="f3712-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3712-228">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="f3712-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3712-229">System-Flags</span></span>           | <span data-ttu-id="f3712-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3712-230">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="f3712-231">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f3712-231">Classes used in</span></span>        | [<span data-ttu-id="f3712-232">**Destinatario de correo**</span><span class="sxs-lookup"><span data-stu-id="f3712-232">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="f3712-233">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="f3712-233">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f3712-234">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3712-234">Windows Server 2008</span></span>



| <span data-ttu-id="f3712-235">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3712-235">Entry</span></span> | <span data-ttu-id="f3712-236">Value</span><span class="sxs-lookup"><span data-stu-id="f3712-236">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3712-237">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f3712-237">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="f3712-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3712-238">MAPI-Id</span></span>                | <span data-ttu-id="f3712-239">0x80AF</span><span class="sxs-lookup"><span data-stu-id="f3712-239">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="f3712-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3712-240">System-Only</span></span>            | <span data-ttu-id="f3712-241">False</span><span class="sxs-lookup"><span data-stu-id="f3712-241">False</span></span>                                                                                                 |
| <span data-ttu-id="f3712-242">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f3712-242">Is-Single-Valued</span></span>       | <span data-ttu-id="f3712-243">True</span><span class="sxs-lookup"><span data-stu-id="f3712-243">True</span></span>                                                                                                  |
| <span data-ttu-id="f3712-244">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f3712-244">Is Indexed</span></span>             | <span data-ttu-id="f3712-245">False</span><span class="sxs-lookup"><span data-stu-id="f3712-245">False</span></span>                                                                                                 |
| <span data-ttu-id="f3712-246">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3712-246">In Global Catalog</span></span>      | <span data-ttu-id="f3712-247">False</span><span class="sxs-lookup"><span data-stu-id="f3712-247">False</span></span>                                                                                                 |
| <span data-ttu-id="f3712-248">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f3712-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3712-249">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3712-249">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="f3712-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3712-250">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="f3712-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3712-251">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="f3712-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3712-252">Search-Flags</span></span>           | <span data-ttu-id="f3712-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3712-253">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="f3712-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3712-254">System-Flags</span></span>           | <span data-ttu-id="f3712-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3712-255">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="f3712-256">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f3712-256">Classes used in</span></span>        | [<span data-ttu-id="f3712-257">**Destinatario de correo**</span><span class="sxs-lookup"><span data-stu-id="f3712-257">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="f3712-258">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="f3712-258">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f3712-259">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f3712-259">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f3712-260">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3712-260">Entry</span></span> | <span data-ttu-id="f3712-261">Value</span><span class="sxs-lookup"><span data-stu-id="f3712-261">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3712-262">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f3712-262">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="f3712-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3712-263">MAPI-Id</span></span>                | <span data-ttu-id="f3712-264">0x80AF</span><span class="sxs-lookup"><span data-stu-id="f3712-264">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="f3712-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3712-265">System-Only</span></span>            | <span data-ttu-id="f3712-266">False</span><span class="sxs-lookup"><span data-stu-id="f3712-266">False</span></span>                                                                                                 |
| <span data-ttu-id="f3712-267">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f3712-267">Is-Single-Valued</span></span>       | <span data-ttu-id="f3712-268">True</span><span class="sxs-lookup"><span data-stu-id="f3712-268">True</span></span>                                                                                                  |
| <span data-ttu-id="f3712-269">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f3712-269">Is Indexed</span></span>             | <span data-ttu-id="f3712-270">False</span><span class="sxs-lookup"><span data-stu-id="f3712-270">False</span></span>                                                                                                 |
| <span data-ttu-id="f3712-271">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3712-271">In Global Catalog</span></span>      | <span data-ttu-id="f3712-272">False</span><span class="sxs-lookup"><span data-stu-id="f3712-272">False</span></span>                                                                                                 |
| <span data-ttu-id="f3712-273">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f3712-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3712-274">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3712-274">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="f3712-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3712-275">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="f3712-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3712-276">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="f3712-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3712-277">Search-Flags</span></span>           | <span data-ttu-id="f3712-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3712-278">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="f3712-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3712-279">System-Flags</span></span>           | <span data-ttu-id="f3712-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3712-280">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="f3712-281">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f3712-281">Classes used in</span></span>        | [<span data-ttu-id="f3712-282">**Destinatario de correo**</span><span class="sxs-lookup"><span data-stu-id="f3712-282">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="f3712-283">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="f3712-283">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f3712-284">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f3712-284">Windows Server 2012</span></span>



| <span data-ttu-id="f3712-285">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3712-285">Entry</span></span> | <span data-ttu-id="f3712-286">Value</span><span class="sxs-lookup"><span data-stu-id="f3712-286">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3712-287">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f3712-287">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="f3712-288">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3712-288">MAPI-Id</span></span>                | <span data-ttu-id="f3712-289">0x80AF</span><span class="sxs-lookup"><span data-stu-id="f3712-289">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="f3712-290">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3712-290">System-Only</span></span>            | <span data-ttu-id="f3712-291">False</span><span class="sxs-lookup"><span data-stu-id="f3712-291">False</span></span>                                                                                                 |
| <span data-ttu-id="f3712-292">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f3712-292">Is-Single-Valued</span></span>       | <span data-ttu-id="f3712-293">True</span><span class="sxs-lookup"><span data-stu-id="f3712-293">True</span></span>                                                                                                  |
| <span data-ttu-id="f3712-294">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f3712-294">Is Indexed</span></span>             | <span data-ttu-id="f3712-295">False</span><span class="sxs-lookup"><span data-stu-id="f3712-295">False</span></span>                                                                                                 |
| <span data-ttu-id="f3712-296">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3712-296">In Global Catalog</span></span>      | <span data-ttu-id="f3712-297">False</span><span class="sxs-lookup"><span data-stu-id="f3712-297">False</span></span>                                                                                                 |
| <span data-ttu-id="f3712-298">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f3712-298">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3712-299">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3712-299">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="f3712-300">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3712-300">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="f3712-301">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3712-301">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="f3712-302">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3712-302">Search-Flags</span></span>           | <span data-ttu-id="f3712-303">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3712-303">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="f3712-304">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3712-304">System-Flags</span></span>           | <span data-ttu-id="f3712-305">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3712-305">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="f3712-306">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f3712-306">Classes used in</span></span>        | [<span data-ttu-id="f3712-307">**Destinatario de correo**</span><span class="sxs-lookup"><span data-stu-id="f3712-307">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="f3712-308">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="f3712-308">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





