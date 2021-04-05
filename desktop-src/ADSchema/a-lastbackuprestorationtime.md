---
title: 'Último: atributo de tiempo de restauración de copia de seguridad'
description: Cuándo se produjo la última restauración del sistema.
ms.assetid: 44850c16-3f17-4883-9a54-3e82ca7d63da
ms.tgt_platform: multiple
keywords:
- 'Último: atributo de tiempo de restauración de copia de seguridad, esquema de AD AD'
- lastBackupRestorationTime esquema de AD de atributos
topic_type:
- apiref
api_name:
- Last-Backup-Restoration-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9220d06a4cdd562599611d2ad19cf09fa279ef3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104079800"
---
# <a name="last-backup-restoration-time-attribute"></a><span data-ttu-id="7e911-105">Último: atributo de tiempo de restauración de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="7e911-105">Last-Backup-Restoration-Time attribute</span></span>

<span data-ttu-id="7e911-106">Cuándo se produjo la última restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="7e911-106">When the last system restore occurred.</span></span>



| <span data-ttu-id="7e911-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e911-107">Entry</span></span> | <span data-ttu-id="7e911-108">Value</span><span class="sxs-lookup"><span data-stu-id="7e911-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7e911-109">CN</span><span class="sxs-lookup"><span data-stu-id="7e911-109">CN</span></span>                | <span data-ttu-id="7e911-110">Última copia de seguridad-tiempo de restauración</span><span class="sxs-lookup"><span data-stu-id="7e911-110">Last-Backup-Restoration-Time</span></span>         |
| <span data-ttu-id="7e911-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="7e911-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7e911-112">lastBackupRestorationTime</span><span class="sxs-lookup"><span data-stu-id="7e911-112">lastBackupRestorationTime</span></span>            |
| <span data-ttu-id="7e911-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="7e911-113">Size</span></span>              | <span data-ttu-id="7e911-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="7e911-114">8 bytes</span></span>                              |
| <span data-ttu-id="7e911-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="7e911-115">Update Privilege</span></span>  | <span data-ttu-id="7e911-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="7e911-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="7e911-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="7e911-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7e911-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7e911-118">Attribute-Id</span></span>      | <span data-ttu-id="7e911-119">1.2.840.113556.1.4.519</span><span class="sxs-lookup"><span data-stu-id="7e911-119">1.2.840.113556.1.4.519</span></span>               |
| <span data-ttu-id="7e911-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7e911-120">System-Id-Guid</span></span>    | <span data-ttu-id="7e911-121">1fbb0be8-ba63-11d0-afef-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="7e911-121">1fbb0be8-ba63-11d0-afef-0000f80367c1</span></span> |
| <span data-ttu-id="7e911-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e911-122">Syntax</span></span>            | [<span data-ttu-id="7e911-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="7e911-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="7e911-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="7e911-124">Implementations</span></span>

-   [<span data-ttu-id="7e911-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7e911-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7e911-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7e911-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7e911-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7e911-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7e911-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7e911-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7e911-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7e911-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7e911-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7e911-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7e911-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7e911-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7e911-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7e911-132">Windows 2000 Server</span></span>



| <span data-ttu-id="7e911-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e911-133">Entry</span></span> | <span data-ttu-id="7e911-134">Value</span><span class="sxs-lookup"><span data-stu-id="7e911-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7e911-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e911-135">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e911-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e911-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e911-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e911-137">System-Only</span></span>            | <span data-ttu-id="7e911-138">False</span><span class="sxs-lookup"><span data-stu-id="7e911-138">False</span></span>                                    |
| <span data-ttu-id="7e911-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e911-139">Is-Single-Valued</span></span>       | <span data-ttu-id="7e911-140">True</span><span class="sxs-lookup"><span data-stu-id="7e911-140">True</span></span>                                     |
| <span data-ttu-id="7e911-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e911-141">Is Indexed</span></span>             | <span data-ttu-id="7e911-142">False</span><span class="sxs-lookup"><span data-stu-id="7e911-142">False</span></span>                                    |
| <span data-ttu-id="7e911-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e911-143">In Global Catalog</span></span>      | <span data-ttu-id="7e911-144">False</span><span class="sxs-lookup"><span data-stu-id="7e911-144">False</span></span>                                    |
| <span data-ttu-id="7e911-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e911-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e911-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e911-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7e911-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e911-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7e911-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e911-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7e911-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e911-149">Search-Flags</span></span>           | <span data-ttu-id="7e911-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e911-150">0x00000000</span></span>                               |
| <span data-ttu-id="7e911-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e911-151">System-Flags</span></span>           | <span data-ttu-id="7e911-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e911-152">0x00000010</span></span>                               |
| <span data-ttu-id="7e911-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e911-153">Classes used in</span></span>        | [<span data-ttu-id="7e911-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="7e911-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7e911-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7e911-155">Windows Server 2003</span></span>



| <span data-ttu-id="7e911-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e911-156">Entry</span></span> | <span data-ttu-id="7e911-157">Value</span><span class="sxs-lookup"><span data-stu-id="7e911-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7e911-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e911-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e911-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e911-159">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e911-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e911-160">System-Only</span></span>            | <span data-ttu-id="7e911-161">False</span><span class="sxs-lookup"><span data-stu-id="7e911-161">False</span></span>                                    |
| <span data-ttu-id="7e911-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e911-162">Is-Single-Valued</span></span>       | <span data-ttu-id="7e911-163">True</span><span class="sxs-lookup"><span data-stu-id="7e911-163">True</span></span>                                     |
| <span data-ttu-id="7e911-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e911-164">Is Indexed</span></span>             | <span data-ttu-id="7e911-165">False</span><span class="sxs-lookup"><span data-stu-id="7e911-165">False</span></span>                                    |
| <span data-ttu-id="7e911-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e911-166">In Global Catalog</span></span>      | <span data-ttu-id="7e911-167">False</span><span class="sxs-lookup"><span data-stu-id="7e911-167">False</span></span>                                    |
| <span data-ttu-id="7e911-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e911-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e911-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e911-169">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7e911-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e911-170">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7e911-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e911-171">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7e911-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e911-172">Search-Flags</span></span>           | <span data-ttu-id="7e911-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e911-173">0x00000000</span></span>                               |
| <span data-ttu-id="7e911-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e911-174">System-Flags</span></span>           | <span data-ttu-id="7e911-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e911-175">0x00000010</span></span>                               |
| <span data-ttu-id="7e911-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e911-176">Classes used in</span></span>        | [<span data-ttu-id="7e911-177">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="7e911-177">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7e911-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="7e911-178">ADAM</span></span>



| <span data-ttu-id="7e911-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e911-179">Entry</span></span> | <span data-ttu-id="7e911-180">Value</span><span class="sxs-lookup"><span data-stu-id="7e911-180">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7e911-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e911-181">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e911-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e911-182">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e911-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e911-183">System-Only</span></span>            | <span data-ttu-id="7e911-184">False</span><span class="sxs-lookup"><span data-stu-id="7e911-184">False</span></span>                                    |
| <span data-ttu-id="7e911-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e911-185">Is-Single-Valued</span></span>       | <span data-ttu-id="7e911-186">True</span><span class="sxs-lookup"><span data-stu-id="7e911-186">True</span></span>                                     |
| <span data-ttu-id="7e911-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e911-187">Is Indexed</span></span>             | <span data-ttu-id="7e911-188">False</span><span class="sxs-lookup"><span data-stu-id="7e911-188">False</span></span>                                    |
| <span data-ttu-id="7e911-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e911-189">In Global Catalog</span></span>      | <span data-ttu-id="7e911-190">False</span><span class="sxs-lookup"><span data-stu-id="7e911-190">False</span></span>                                    |
| <span data-ttu-id="7e911-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e911-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e911-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e911-192">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7e911-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e911-193">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7e911-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e911-194">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7e911-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e911-195">Search-Flags</span></span>           | <span data-ttu-id="7e911-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e911-196">0x00000000</span></span>                               |
| <span data-ttu-id="7e911-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e911-197">System-Flags</span></span>           | <span data-ttu-id="7e911-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e911-198">0x00000010</span></span>                               |
| <span data-ttu-id="7e911-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e911-199">Classes used in</span></span>        | [<span data-ttu-id="7e911-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="7e911-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7e911-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7e911-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7e911-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e911-202">Entry</span></span> | <span data-ttu-id="7e911-203">Value</span><span class="sxs-lookup"><span data-stu-id="7e911-203">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7e911-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e911-204">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e911-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e911-205">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e911-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e911-206">System-Only</span></span>            | <span data-ttu-id="7e911-207">False</span><span class="sxs-lookup"><span data-stu-id="7e911-207">False</span></span>                                    |
| <span data-ttu-id="7e911-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e911-208">Is-Single-Valued</span></span>       | <span data-ttu-id="7e911-209">True</span><span class="sxs-lookup"><span data-stu-id="7e911-209">True</span></span>                                     |
| <span data-ttu-id="7e911-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e911-210">Is Indexed</span></span>             | <span data-ttu-id="7e911-211">False</span><span class="sxs-lookup"><span data-stu-id="7e911-211">False</span></span>                                    |
| <span data-ttu-id="7e911-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e911-212">In Global Catalog</span></span>      | <span data-ttu-id="7e911-213">False</span><span class="sxs-lookup"><span data-stu-id="7e911-213">False</span></span>                                    |
| <span data-ttu-id="7e911-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e911-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e911-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e911-215">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7e911-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e911-216">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7e911-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e911-217">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7e911-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e911-218">Search-Flags</span></span>           | <span data-ttu-id="7e911-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e911-219">0x00000000</span></span>                               |
| <span data-ttu-id="7e911-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e911-220">System-Flags</span></span>           | <span data-ttu-id="7e911-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e911-221">0x00000010</span></span>                               |
| <span data-ttu-id="7e911-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e911-222">Classes used in</span></span>        | [<span data-ttu-id="7e911-223">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="7e911-223">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7e911-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e911-224">Windows Server 2008</span></span>



| <span data-ttu-id="7e911-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e911-225">Entry</span></span> | <span data-ttu-id="7e911-226">Value</span><span class="sxs-lookup"><span data-stu-id="7e911-226">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7e911-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e911-227">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e911-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e911-228">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e911-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e911-229">System-Only</span></span>            | <span data-ttu-id="7e911-230">False</span><span class="sxs-lookup"><span data-stu-id="7e911-230">False</span></span>                                    |
| <span data-ttu-id="7e911-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e911-231">Is-Single-Valued</span></span>       | <span data-ttu-id="7e911-232">True</span><span class="sxs-lookup"><span data-stu-id="7e911-232">True</span></span>                                     |
| <span data-ttu-id="7e911-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e911-233">Is Indexed</span></span>             | <span data-ttu-id="7e911-234">False</span><span class="sxs-lookup"><span data-stu-id="7e911-234">False</span></span>                                    |
| <span data-ttu-id="7e911-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e911-235">In Global Catalog</span></span>      | <span data-ttu-id="7e911-236">False</span><span class="sxs-lookup"><span data-stu-id="7e911-236">False</span></span>                                    |
| <span data-ttu-id="7e911-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e911-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e911-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e911-238">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7e911-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e911-239">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7e911-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e911-240">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7e911-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e911-241">Search-Flags</span></span>           | <span data-ttu-id="7e911-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e911-242">0x00000000</span></span>                               |
| <span data-ttu-id="7e911-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e911-243">System-Flags</span></span>           | <span data-ttu-id="7e911-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e911-244">0x00000010</span></span>                               |
| <span data-ttu-id="7e911-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e911-245">Classes used in</span></span>        | [<span data-ttu-id="7e911-246">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="7e911-246">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7e911-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7e911-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7e911-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e911-248">Entry</span></span> | <span data-ttu-id="7e911-249">Value</span><span class="sxs-lookup"><span data-stu-id="7e911-249">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7e911-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e911-250">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e911-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e911-251">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e911-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e911-252">System-Only</span></span>            | <span data-ttu-id="7e911-253">False</span><span class="sxs-lookup"><span data-stu-id="7e911-253">False</span></span>                                    |
| <span data-ttu-id="7e911-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e911-254">Is-Single-Valued</span></span>       | <span data-ttu-id="7e911-255">True</span><span class="sxs-lookup"><span data-stu-id="7e911-255">True</span></span>                                     |
| <span data-ttu-id="7e911-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e911-256">Is Indexed</span></span>             | <span data-ttu-id="7e911-257">False</span><span class="sxs-lookup"><span data-stu-id="7e911-257">False</span></span>                                    |
| <span data-ttu-id="7e911-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e911-258">In Global Catalog</span></span>      | <span data-ttu-id="7e911-259">False</span><span class="sxs-lookup"><span data-stu-id="7e911-259">False</span></span>                                    |
| <span data-ttu-id="7e911-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e911-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e911-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e911-261">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7e911-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e911-262">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7e911-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e911-263">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7e911-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e911-264">Search-Flags</span></span>           | <span data-ttu-id="7e911-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e911-265">0x00000000</span></span>                               |
| <span data-ttu-id="7e911-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e911-266">System-Flags</span></span>           | <span data-ttu-id="7e911-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e911-267">0x00000010</span></span>                               |
| <span data-ttu-id="7e911-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e911-268">Classes used in</span></span>        | [<span data-ttu-id="7e911-269">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="7e911-269">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7e911-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7e911-270">Windows Server 2012</span></span>



| <span data-ttu-id="7e911-271">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e911-271">Entry</span></span> | <span data-ttu-id="7e911-272">Value</span><span class="sxs-lookup"><span data-stu-id="7e911-272">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7e911-273">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e911-273">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e911-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e911-274">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e911-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e911-275">System-Only</span></span>            | <span data-ttu-id="7e911-276">False</span><span class="sxs-lookup"><span data-stu-id="7e911-276">False</span></span>                                    |
| <span data-ttu-id="7e911-277">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e911-277">Is-Single-Valued</span></span>       | <span data-ttu-id="7e911-278">True</span><span class="sxs-lookup"><span data-stu-id="7e911-278">True</span></span>                                     |
| <span data-ttu-id="7e911-279">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e911-279">Is Indexed</span></span>             | <span data-ttu-id="7e911-280">False</span><span class="sxs-lookup"><span data-stu-id="7e911-280">False</span></span>                                    |
| <span data-ttu-id="7e911-281">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e911-281">In Global Catalog</span></span>      | <span data-ttu-id="7e911-282">False</span><span class="sxs-lookup"><span data-stu-id="7e911-282">False</span></span>                                    |
| <span data-ttu-id="7e911-283">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e911-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e911-284">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e911-284">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7e911-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e911-285">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7e911-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e911-286">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7e911-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e911-287">Search-Flags</span></span>           | <span data-ttu-id="7e911-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e911-288">0x00000000</span></span>                               |
| <span data-ttu-id="7e911-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e911-289">System-Flags</span></span>           | <span data-ttu-id="7e911-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e911-290">0x00000010</span></span>                               |
| <span data-ttu-id="7e911-291">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e911-291">Classes used in</span></span>        | [<span data-ttu-id="7e911-292">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="7e911-292">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





