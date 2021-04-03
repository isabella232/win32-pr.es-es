---
title: Tombstone-Lifetime atributo)
description: El número de días antes de que se quite un objeto eliminado de los servicios de directorio.
ms.assetid: 58898097-912b-4fe6-b6ea-91f49aaa2b1b
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Tombstone-Lifetime
- tombstoneLifetime (atributo) esquema de AD
topic_type:
- apiref
api_name:
- Tombstone-Lifetime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb2bd0b7b970270c626437ee65288fd07bf48272
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906097"
---
# <a name="tombstone-lifetime-attribute"></a><span data-ttu-id="4bb14-105">Tombstone-Lifetime atributo)</span><span class="sxs-lookup"><span data-stu-id="4bb14-105">Tombstone-Lifetime attribute</span></span>

<span data-ttu-id="4bb14-106">El número de días antes de que se quite un objeto eliminado de los servicios de directorio.</span><span class="sxs-lookup"><span data-stu-id="4bb14-106">The number of days before a deleted object is removed from the directory services.</span></span> <span data-ttu-id="4bb14-107">Esto ayuda a quitar objetos de los servidores replicados y evitar que las restauraciones representen un objeto eliminado.</span><span class="sxs-lookup"><span data-stu-id="4bb14-107">This assists in removing objects from replicated servers and preventing restores from reintroducing a deleted object.</span></span> <span data-ttu-id="4bb14-108">Este valor se encuentra en el objeto de servicio de directorio en la NIC de configuración.</span><span class="sxs-lookup"><span data-stu-id="4bb14-108">This value is in the Directory Service object in the configuration NIC.</span></span>



| <span data-ttu-id="4bb14-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="4bb14-109">Entry</span></span> | <span data-ttu-id="4bb14-110">Value</span><span class="sxs-lookup"><span data-stu-id="4bb14-110">Value</span></span> |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="4bb14-111">CN</span><span class="sxs-lookup"><span data-stu-id="4bb14-111">CN</span></span>                | <span data-ttu-id="4bb14-112">Tombstone-Lifetime</span><span class="sxs-lookup"><span data-stu-id="4bb14-112">Tombstone-Lifetime</span></span>                                        |
| <span data-ttu-id="4bb14-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="4bb14-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4bb14-114">tombstoneLifetime</span><span class="sxs-lookup"><span data-stu-id="4bb14-114">tombstoneLifetime</span></span>                                         |
| <span data-ttu-id="4bb14-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="4bb14-115">Size</span></span>              | <span data-ttu-id="4bb14-116">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="4bb14-116">4 bytes.</span></span> <span data-ttu-id="4bb14-117">El valor predeterminado es 60 días cuando no se especifica ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4bb14-117">The default is 60 days when no value is entered.</span></span> |
| <span data-ttu-id="4bb14-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="4bb14-118">Update Privilege</span></span>  | \-                                                        |
| <span data-ttu-id="4bb14-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="4bb14-119">Update Frequency</span></span>  | \-                                                        |
| <span data-ttu-id="4bb14-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4bb14-120">Attribute-Id</span></span>      | <span data-ttu-id="4bb14-121">1.2.840.113556.1.2.54</span><span class="sxs-lookup"><span data-stu-id="4bb14-121">1.2.840.113556.1.2.54</span></span>                                     |
| <span data-ttu-id="4bb14-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4bb14-122">System-Id-Guid</span></span>    | <span data-ttu-id="4bb14-123">16c3a860-1273-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="4bb14-123">16c3a860-1273-11d0-a060-00aa006c33ed</span></span>                      |
| <span data-ttu-id="4bb14-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4bb14-124">Syntax</span></span>            | [<span data-ttu-id="4bb14-125">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="4bb14-125">**Enumeration**</span></span>](s-enumeration.md)                      |



## <a name="implementations"></a><span data-ttu-id="4bb14-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="4bb14-126">Implementations</span></span>

-   [<span data-ttu-id="4bb14-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4bb14-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4bb14-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4bb14-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4bb14-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="4bb14-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4bb14-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4bb14-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4bb14-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4bb14-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4bb14-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4bb14-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4bb14-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4bb14-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4bb14-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4bb14-134">Windows 2000 Server</span></span>



| <span data-ttu-id="4bb14-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="4bb14-135">Entry</span></span> | <span data-ttu-id="4bb14-136">Value</span><span class="sxs-lookup"><span data-stu-id="4bb14-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4bb14-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4bb14-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4bb14-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bb14-138">MAPI-Id</span></span>                | <span data-ttu-id="4bb14-139">0x8145</span><span class="sxs-lookup"><span data-stu-id="4bb14-139">0x8145</span></span>                                           |
| <span data-ttu-id="4bb14-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bb14-140">System-Only</span></span>            | <span data-ttu-id="4bb14-141">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-141">False</span></span>                                            |
| <span data-ttu-id="4bb14-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4bb14-142">Is-Single-Valued</span></span>       | <span data-ttu-id="4bb14-143">True</span><span class="sxs-lookup"><span data-stu-id="4bb14-143">True</span></span>                                             |
| <span data-ttu-id="4bb14-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4bb14-144">Is Indexed</span></span>             | <span data-ttu-id="4bb14-145">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-145">False</span></span>                                            |
| <span data-ttu-id="4bb14-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4bb14-146">In Global Catalog</span></span>      | <span data-ttu-id="4bb14-147">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-147">False</span></span>                                            |
| <span data-ttu-id="4bb14-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4bb14-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bb14-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4bb14-149">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4bb14-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bb14-150">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="4bb14-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bb14-151">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="4bb14-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bb14-152">Search-Flags</span></span>           | <span data-ttu-id="4bb14-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bb14-153">0x00000000</span></span>                                       |
| <span data-ttu-id="4bb14-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bb14-154">System-Flags</span></span>           | <span data-ttu-id="4bb14-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bb14-155">0x00000010</span></span>                                       |
| <span data-ttu-id="4bb14-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4bb14-156">Classes used in</span></span>        | [<span data-ttu-id="4bb14-157">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="4bb14-157">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4bb14-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4bb14-158">Windows Server 2003</span></span>



| <span data-ttu-id="4bb14-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="4bb14-159">Entry</span></span> | <span data-ttu-id="4bb14-160">Value</span><span class="sxs-lookup"><span data-stu-id="4bb14-160">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4bb14-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4bb14-161">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4bb14-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bb14-162">MAPI-Id</span></span>                | <span data-ttu-id="4bb14-163">0x8145</span><span class="sxs-lookup"><span data-stu-id="4bb14-163">0x8145</span></span>                                           |
| <span data-ttu-id="4bb14-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bb14-164">System-Only</span></span>            | <span data-ttu-id="4bb14-165">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-165">False</span></span>                                            |
| <span data-ttu-id="4bb14-166">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4bb14-166">Is-Single-Valued</span></span>       | <span data-ttu-id="4bb14-167">True</span><span class="sxs-lookup"><span data-stu-id="4bb14-167">True</span></span>                                             |
| <span data-ttu-id="4bb14-168">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4bb14-168">Is Indexed</span></span>             | <span data-ttu-id="4bb14-169">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-169">False</span></span>                                            |
| <span data-ttu-id="4bb14-170">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4bb14-170">In Global Catalog</span></span>      | <span data-ttu-id="4bb14-171">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-171">False</span></span>                                            |
| <span data-ttu-id="4bb14-172">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4bb14-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bb14-173">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4bb14-173">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4bb14-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bb14-174">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="4bb14-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bb14-175">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="4bb14-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bb14-176">Search-Flags</span></span>           | <span data-ttu-id="4bb14-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bb14-177">0x00000000</span></span>                                       |
| <span data-ttu-id="4bb14-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bb14-178">System-Flags</span></span>           | <span data-ttu-id="4bb14-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bb14-179">0x00000010</span></span>                                       |
| <span data-ttu-id="4bb14-180">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4bb14-180">Classes used in</span></span>        | [<span data-ttu-id="4bb14-181">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="4bb14-181">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4bb14-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="4bb14-182">ADAM</span></span>



| <span data-ttu-id="4bb14-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="4bb14-183">Entry</span></span> | <span data-ttu-id="4bb14-184">Value</span><span class="sxs-lookup"><span data-stu-id="4bb14-184">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4bb14-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4bb14-185">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4bb14-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bb14-186">MAPI-Id</span></span>                | <span data-ttu-id="4bb14-187">0x8145</span><span class="sxs-lookup"><span data-stu-id="4bb14-187">0x8145</span></span>                                           |
| <span data-ttu-id="4bb14-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bb14-188">System-Only</span></span>            | <span data-ttu-id="4bb14-189">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-189">False</span></span>                                            |
| <span data-ttu-id="4bb14-190">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4bb14-190">Is-Single-Valued</span></span>       | <span data-ttu-id="4bb14-191">True</span><span class="sxs-lookup"><span data-stu-id="4bb14-191">True</span></span>                                             |
| <span data-ttu-id="4bb14-192">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4bb14-192">Is Indexed</span></span>             | <span data-ttu-id="4bb14-193">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-193">False</span></span>                                            |
| <span data-ttu-id="4bb14-194">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4bb14-194">In Global Catalog</span></span>      | <span data-ttu-id="4bb14-195">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-195">False</span></span>                                            |
| <span data-ttu-id="4bb14-196">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4bb14-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bb14-197">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4bb14-197">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4bb14-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bb14-198">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="4bb14-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bb14-199">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="4bb14-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bb14-200">Search-Flags</span></span>           | <span data-ttu-id="4bb14-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bb14-201">0x00000000</span></span>                                       |
| <span data-ttu-id="4bb14-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bb14-202">System-Flags</span></span>           | <span data-ttu-id="4bb14-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bb14-203">0x00000010</span></span>                                       |
| <span data-ttu-id="4bb14-204">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4bb14-204">Classes used in</span></span>        | [<span data-ttu-id="4bb14-205">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="4bb14-205">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4bb14-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4bb14-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4bb14-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="4bb14-207">Entry</span></span> | <span data-ttu-id="4bb14-208">Value</span><span class="sxs-lookup"><span data-stu-id="4bb14-208">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4bb14-209">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4bb14-209">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4bb14-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bb14-210">MAPI-Id</span></span>                | <span data-ttu-id="4bb14-211">0x8145</span><span class="sxs-lookup"><span data-stu-id="4bb14-211">0x8145</span></span>                                           |
| <span data-ttu-id="4bb14-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bb14-212">System-Only</span></span>            | <span data-ttu-id="4bb14-213">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-213">False</span></span>                                            |
| <span data-ttu-id="4bb14-214">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4bb14-214">Is-Single-Valued</span></span>       | <span data-ttu-id="4bb14-215">True</span><span class="sxs-lookup"><span data-stu-id="4bb14-215">True</span></span>                                             |
| <span data-ttu-id="4bb14-216">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4bb14-216">Is Indexed</span></span>             | <span data-ttu-id="4bb14-217">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-217">False</span></span>                                            |
| <span data-ttu-id="4bb14-218">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4bb14-218">In Global Catalog</span></span>      | <span data-ttu-id="4bb14-219">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-219">False</span></span>                                            |
| <span data-ttu-id="4bb14-220">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4bb14-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bb14-221">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4bb14-221">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4bb14-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bb14-222">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="4bb14-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bb14-223">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="4bb14-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bb14-224">Search-Flags</span></span>           | <span data-ttu-id="4bb14-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bb14-225">0x00000000</span></span>                                       |
| <span data-ttu-id="4bb14-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bb14-226">System-Flags</span></span>           | <span data-ttu-id="4bb14-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bb14-227">0x00000010</span></span>                                       |
| <span data-ttu-id="4bb14-228">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4bb14-228">Classes used in</span></span>        | [<span data-ttu-id="4bb14-229">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="4bb14-229">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4bb14-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4bb14-230">Windows Server 2008</span></span>



| <span data-ttu-id="4bb14-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="4bb14-231">Entry</span></span> | <span data-ttu-id="4bb14-232">Value</span><span class="sxs-lookup"><span data-stu-id="4bb14-232">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4bb14-233">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4bb14-233">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4bb14-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bb14-234">MAPI-Id</span></span>                | <span data-ttu-id="4bb14-235">0x8145</span><span class="sxs-lookup"><span data-stu-id="4bb14-235">0x8145</span></span>                                           |
| <span data-ttu-id="4bb14-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bb14-236">System-Only</span></span>            | <span data-ttu-id="4bb14-237">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-237">False</span></span>                                            |
| <span data-ttu-id="4bb14-238">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4bb14-238">Is-Single-Valued</span></span>       | <span data-ttu-id="4bb14-239">True</span><span class="sxs-lookup"><span data-stu-id="4bb14-239">True</span></span>                                             |
| <span data-ttu-id="4bb14-240">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4bb14-240">Is Indexed</span></span>             | <span data-ttu-id="4bb14-241">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-241">False</span></span>                                            |
| <span data-ttu-id="4bb14-242">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4bb14-242">In Global Catalog</span></span>      | <span data-ttu-id="4bb14-243">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-243">False</span></span>                                            |
| <span data-ttu-id="4bb14-244">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4bb14-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bb14-245">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4bb14-245">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4bb14-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bb14-246">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="4bb14-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bb14-247">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="4bb14-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bb14-248">Search-Flags</span></span>           | <span data-ttu-id="4bb14-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bb14-249">0x00000000</span></span>                                       |
| <span data-ttu-id="4bb14-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bb14-250">System-Flags</span></span>           | <span data-ttu-id="4bb14-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bb14-251">0x00000010</span></span>                                       |
| <span data-ttu-id="4bb14-252">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4bb14-252">Classes used in</span></span>        | [<span data-ttu-id="4bb14-253">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="4bb14-253">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4bb14-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4bb14-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4bb14-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="4bb14-255">Entry</span></span> | <span data-ttu-id="4bb14-256">Value</span><span class="sxs-lookup"><span data-stu-id="4bb14-256">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4bb14-257">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4bb14-257">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4bb14-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bb14-258">MAPI-Id</span></span>                | <span data-ttu-id="4bb14-259">0x8145</span><span class="sxs-lookup"><span data-stu-id="4bb14-259">0x8145</span></span>                                           |
| <span data-ttu-id="4bb14-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bb14-260">System-Only</span></span>            | <span data-ttu-id="4bb14-261">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-261">False</span></span>                                            |
| <span data-ttu-id="4bb14-262">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4bb14-262">Is-Single-Valued</span></span>       | <span data-ttu-id="4bb14-263">True</span><span class="sxs-lookup"><span data-stu-id="4bb14-263">True</span></span>                                             |
| <span data-ttu-id="4bb14-264">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4bb14-264">Is Indexed</span></span>             | <span data-ttu-id="4bb14-265">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-265">False</span></span>                                            |
| <span data-ttu-id="4bb14-266">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4bb14-266">In Global Catalog</span></span>      | <span data-ttu-id="4bb14-267">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-267">False</span></span>                                            |
| <span data-ttu-id="4bb14-268">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4bb14-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bb14-269">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4bb14-269">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4bb14-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bb14-270">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="4bb14-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bb14-271">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="4bb14-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bb14-272">Search-Flags</span></span>           | <span data-ttu-id="4bb14-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bb14-273">0x00000000</span></span>                                       |
| <span data-ttu-id="4bb14-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bb14-274">System-Flags</span></span>           | <span data-ttu-id="4bb14-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bb14-275">0x00000010</span></span>                                       |
| <span data-ttu-id="4bb14-276">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4bb14-276">Classes used in</span></span>        | [<span data-ttu-id="4bb14-277">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="4bb14-277">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4bb14-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4bb14-278">Windows Server 2012</span></span>



| <span data-ttu-id="4bb14-279">Entrada</span><span class="sxs-lookup"><span data-stu-id="4bb14-279">Entry</span></span> | <span data-ttu-id="4bb14-280">Value</span><span class="sxs-lookup"><span data-stu-id="4bb14-280">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4bb14-281">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4bb14-281">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4bb14-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bb14-282">MAPI-Id</span></span>                | <span data-ttu-id="4bb14-283">0x8145</span><span class="sxs-lookup"><span data-stu-id="4bb14-283">0x8145</span></span>                                           |
| <span data-ttu-id="4bb14-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bb14-284">System-Only</span></span>            | <span data-ttu-id="4bb14-285">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-285">False</span></span>                                            |
| <span data-ttu-id="4bb14-286">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4bb14-286">Is-Single-Valued</span></span>       | <span data-ttu-id="4bb14-287">True</span><span class="sxs-lookup"><span data-stu-id="4bb14-287">True</span></span>                                             |
| <span data-ttu-id="4bb14-288">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4bb14-288">Is Indexed</span></span>             | <span data-ttu-id="4bb14-289">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-289">False</span></span>                                            |
| <span data-ttu-id="4bb14-290">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4bb14-290">In Global Catalog</span></span>      | <span data-ttu-id="4bb14-291">False</span><span class="sxs-lookup"><span data-stu-id="4bb14-291">False</span></span>                                            |
| <span data-ttu-id="4bb14-292">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4bb14-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bb14-293">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4bb14-293">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4bb14-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bb14-294">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="4bb14-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bb14-295">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="4bb14-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bb14-296">Search-Flags</span></span>           | <span data-ttu-id="4bb14-297">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bb14-297">0x00000000</span></span>                                       |
| <span data-ttu-id="4bb14-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bb14-298">System-Flags</span></span>           | <span data-ttu-id="4bb14-299">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bb14-299">0x00000010</span></span>                                       |
| <span data-ttu-id="4bb14-300">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4bb14-300">Classes used in</span></span>        | [<span data-ttu-id="4bb14-301">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="4bb14-301">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





