---
title: Lockout-Time atributo)
description: Fecha y hora (UTC) en que se bloqueó esta cuenta.
ms.assetid: 4a0a66a3-9f7f-48ec-9b96-a9c3e72b2b6b
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Lockout-Time
- lockoutTime esquema de AD de atributos
topic_type:
- apiref
api_name:
- Lockout-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adebe8bf76ba04fe4ba774726da7cd5c54e64ab1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658928"
---
# <a name="lockout-time-attribute"></a><span data-ttu-id="75054-105">Lockout-Time atributo)</span><span class="sxs-lookup"><span data-stu-id="75054-105">Lockout-Time attribute</span></span>

<span data-ttu-id="75054-106">Fecha y hora (UTC) en que se bloqueó esta cuenta. Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="75054-106">The date and time (UTC) that this account was locked out. This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="75054-107">Un valor de cero significa que la cuenta no está bloqueada actualmente.</span><span class="sxs-lookup"><span data-stu-id="75054-107">A value of zero means that the account is not currently locked out.</span></span>



| <span data-ttu-id="75054-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="75054-108">Entry</span></span> | <span data-ttu-id="75054-109">Value</span><span class="sxs-lookup"><span data-stu-id="75054-109">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="75054-110">CN</span><span class="sxs-lookup"><span data-stu-id="75054-110">CN</span></span>                | <span data-ttu-id="75054-111">Lockout-Time</span><span class="sxs-lookup"><span data-stu-id="75054-111">Lockout-Time</span></span>                                                                     |
| <span data-ttu-id="75054-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="75054-112">Ldap-Display-Name</span></span> | <span data-ttu-id="75054-113">lockoutTime</span><span class="sxs-lookup"><span data-stu-id="75054-113">lockoutTime</span></span>                                                                      |
| <span data-ttu-id="75054-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="75054-114">Size</span></span>              | <span data-ttu-id="75054-115">8 bytes</span><span class="sxs-lookup"><span data-stu-id="75054-115">8 bytes</span></span>                                                                          |
| <span data-ttu-id="75054-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="75054-116">Update Privilege</span></span>  | <span data-ttu-id="75054-117">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="75054-117">Domain administrator</span></span>                                                             |
| <span data-ttu-id="75054-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="75054-118">Update Frequency</span></span>  | <span data-ttu-id="75054-119">Cuando se crea el registro del usuario y cada vez que es necesario cambiar el tiempo de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="75054-119">When the user's record is created and whenever the lockout time needs to change.</span></span> |
| <span data-ttu-id="75054-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="75054-120">Attribute-Id</span></span>      | <span data-ttu-id="75054-121">1.2.840.113556.1.4.662</span><span class="sxs-lookup"><span data-stu-id="75054-121">1.2.840.113556.1.4.662</span></span>                                                           |
| <span data-ttu-id="75054-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="75054-122">System-Id-Guid</span></span>    | <span data-ttu-id="75054-123">28630ebf-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="75054-123">28630ebf-41d5-11d1-a9c1-0000f80367c1</span></span>                                             |
| <span data-ttu-id="75054-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75054-124">Syntax</span></span>            | [<span data-ttu-id="75054-125">**Interval**</span><span class="sxs-lookup"><span data-stu-id="75054-125">**Interval**</span></span>](s-interval.md)                                                   |



## <a name="implementations"></a><span data-ttu-id="75054-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="75054-126">Implementations</span></span>

-   [<span data-ttu-id="75054-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="75054-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="75054-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="75054-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="75054-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="75054-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="75054-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="75054-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="75054-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="75054-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="75054-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="75054-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="75054-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="75054-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="75054-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="75054-134">Windows 2000 Server</span></span>



| <span data-ttu-id="75054-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="75054-135">Entry</span></span> | <span data-ttu-id="75054-136">Value</span><span class="sxs-lookup"><span data-stu-id="75054-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="75054-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="75054-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="75054-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75054-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="75054-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="75054-139">System-Only</span></span>            | <span data-ttu-id="75054-140">False</span><span class="sxs-lookup"><span data-stu-id="75054-140">False</span></span>                             |
| <span data-ttu-id="75054-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="75054-141">Is-Single-Valued</span></span>       | <span data-ttu-id="75054-142">True</span><span class="sxs-lookup"><span data-stu-id="75054-142">True</span></span>                              |
| <span data-ttu-id="75054-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="75054-143">Is Indexed</span></span>             | <span data-ttu-id="75054-144">False</span><span class="sxs-lookup"><span data-stu-id="75054-144">False</span></span>                             |
| <span data-ttu-id="75054-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="75054-145">In Global Catalog</span></span>      | <span data-ttu-id="75054-146">False</span><span class="sxs-lookup"><span data-stu-id="75054-146">False</span></span>                             |
| <span data-ttu-id="75054-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="75054-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="75054-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="75054-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="75054-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75054-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="75054-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75054-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="75054-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75054-151">Search-Flags</span></span>           | <span data-ttu-id="75054-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75054-152">0x00000000</span></span>                        |
| <span data-ttu-id="75054-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75054-153">System-Flags</span></span>           | <span data-ttu-id="75054-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75054-154">0x00000010</span></span>                        |
| <span data-ttu-id="75054-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="75054-155">Classes used in</span></span>        | [<span data-ttu-id="75054-156">**User**</span><span class="sxs-lookup"><span data-stu-id="75054-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="75054-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="75054-157">Windows Server 2003</span></span>



| <span data-ttu-id="75054-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="75054-158">Entry</span></span> | <span data-ttu-id="75054-159">Value</span><span class="sxs-lookup"><span data-stu-id="75054-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="75054-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="75054-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="75054-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75054-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="75054-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="75054-162">System-Only</span></span>            | <span data-ttu-id="75054-163">False</span><span class="sxs-lookup"><span data-stu-id="75054-163">False</span></span>                             |
| <span data-ttu-id="75054-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="75054-164">Is-Single-Valued</span></span>       | <span data-ttu-id="75054-165">True</span><span class="sxs-lookup"><span data-stu-id="75054-165">True</span></span>                              |
| <span data-ttu-id="75054-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="75054-166">Is Indexed</span></span>             | <span data-ttu-id="75054-167">False</span><span class="sxs-lookup"><span data-stu-id="75054-167">False</span></span>                             |
| <span data-ttu-id="75054-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="75054-168">In Global Catalog</span></span>      | <span data-ttu-id="75054-169">False</span><span class="sxs-lookup"><span data-stu-id="75054-169">False</span></span>                             |
| <span data-ttu-id="75054-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="75054-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="75054-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="75054-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="75054-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75054-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="75054-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75054-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="75054-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75054-174">Search-Flags</span></span>           | <span data-ttu-id="75054-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75054-175">0x00000000</span></span>                        |
| <span data-ttu-id="75054-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75054-176">System-Flags</span></span>           | <span data-ttu-id="75054-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75054-177">0x00000010</span></span>                        |
| <span data-ttu-id="75054-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="75054-178">Classes used in</span></span>        | [<span data-ttu-id="75054-179">**User**</span><span class="sxs-lookup"><span data-stu-id="75054-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="75054-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="75054-180">ADAM</span></span>



| <span data-ttu-id="75054-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="75054-181">Entry</span></span> | <span data-ttu-id="75054-182">Value</span><span class="sxs-lookup"><span data-stu-id="75054-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="75054-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="75054-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="75054-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75054-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="75054-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="75054-185">System-Only</span></span>            | <span data-ttu-id="75054-186">False</span><span class="sxs-lookup"><span data-stu-id="75054-186">False</span></span>                                                             |
| <span data-ttu-id="75054-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="75054-187">Is-Single-Valued</span></span>       | <span data-ttu-id="75054-188">True</span><span class="sxs-lookup"><span data-stu-id="75054-188">True</span></span>                                                              |
| <span data-ttu-id="75054-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="75054-189">Is Indexed</span></span>             | <span data-ttu-id="75054-190">False</span><span class="sxs-lookup"><span data-stu-id="75054-190">False</span></span>                                                             |
| <span data-ttu-id="75054-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="75054-191">In Global Catalog</span></span>      | <span data-ttu-id="75054-192">False</span><span class="sxs-lookup"><span data-stu-id="75054-192">False</span></span>                                                             |
| <span data-ttu-id="75054-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="75054-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="75054-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="75054-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="75054-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75054-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="75054-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75054-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="75054-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75054-197">Search-Flags</span></span>           | <span data-ttu-id="75054-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75054-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="75054-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75054-199">System-Flags</span></span>           | <span data-ttu-id="75054-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75054-200">0x00000010</span></span>                                                        |
| <span data-ttu-id="75054-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="75054-201">Classes used in</span></span>        | [<span data-ttu-id="75054-202">**Objeto MS-DS-Bindable**</span><span class="sxs-lookup"><span data-stu-id="75054-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="75054-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="75054-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="75054-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="75054-204">Entry</span></span> | <span data-ttu-id="75054-205">Value</span><span class="sxs-lookup"><span data-stu-id="75054-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="75054-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="75054-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="75054-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75054-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="75054-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="75054-208">System-Only</span></span>            | <span data-ttu-id="75054-209">False</span><span class="sxs-lookup"><span data-stu-id="75054-209">False</span></span>                             |
| <span data-ttu-id="75054-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="75054-210">Is-Single-Valued</span></span>       | <span data-ttu-id="75054-211">True</span><span class="sxs-lookup"><span data-stu-id="75054-211">True</span></span>                              |
| <span data-ttu-id="75054-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="75054-212">Is Indexed</span></span>             | <span data-ttu-id="75054-213">False</span><span class="sxs-lookup"><span data-stu-id="75054-213">False</span></span>                             |
| <span data-ttu-id="75054-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="75054-214">In Global Catalog</span></span>      | <span data-ttu-id="75054-215">False</span><span class="sxs-lookup"><span data-stu-id="75054-215">False</span></span>                             |
| <span data-ttu-id="75054-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="75054-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="75054-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="75054-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="75054-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75054-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="75054-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75054-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="75054-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75054-220">Search-Flags</span></span>           | <span data-ttu-id="75054-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75054-221">0x00000000</span></span>                        |
| <span data-ttu-id="75054-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75054-222">System-Flags</span></span>           | <span data-ttu-id="75054-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75054-223">0x00000010</span></span>                        |
| <span data-ttu-id="75054-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="75054-224">Classes used in</span></span>        | [<span data-ttu-id="75054-225">**User**</span><span class="sxs-lookup"><span data-stu-id="75054-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="75054-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75054-226">Windows Server 2008</span></span>



| <span data-ttu-id="75054-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="75054-227">Entry</span></span> | <span data-ttu-id="75054-228">Value</span><span class="sxs-lookup"><span data-stu-id="75054-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="75054-229">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="75054-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="75054-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75054-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="75054-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="75054-231">System-Only</span></span>            | <span data-ttu-id="75054-232">False</span><span class="sxs-lookup"><span data-stu-id="75054-232">False</span></span>                             |
| <span data-ttu-id="75054-233">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="75054-233">Is-Single-Valued</span></span>       | <span data-ttu-id="75054-234">True</span><span class="sxs-lookup"><span data-stu-id="75054-234">True</span></span>                              |
| <span data-ttu-id="75054-235">Está indexado</span><span class="sxs-lookup"><span data-stu-id="75054-235">Is Indexed</span></span>             | <span data-ttu-id="75054-236">False</span><span class="sxs-lookup"><span data-stu-id="75054-236">False</span></span>                             |
| <span data-ttu-id="75054-237">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="75054-237">In Global Catalog</span></span>      | <span data-ttu-id="75054-238">False</span><span class="sxs-lookup"><span data-stu-id="75054-238">False</span></span>                             |
| <span data-ttu-id="75054-239">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="75054-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="75054-240">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="75054-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="75054-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75054-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="75054-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75054-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="75054-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75054-243">Search-Flags</span></span>           | <span data-ttu-id="75054-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75054-244">0x00000000</span></span>                        |
| <span data-ttu-id="75054-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75054-245">System-Flags</span></span>           | <span data-ttu-id="75054-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75054-246">0x00000010</span></span>                        |
| <span data-ttu-id="75054-247">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="75054-247">Classes used in</span></span>        | [<span data-ttu-id="75054-248">**User**</span><span class="sxs-lookup"><span data-stu-id="75054-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="75054-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="75054-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="75054-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="75054-250">Entry</span></span> | <span data-ttu-id="75054-251">Value</span><span class="sxs-lookup"><span data-stu-id="75054-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="75054-252">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="75054-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="75054-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75054-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="75054-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="75054-254">System-Only</span></span>            | <span data-ttu-id="75054-255">False</span><span class="sxs-lookup"><span data-stu-id="75054-255">False</span></span>                             |
| <span data-ttu-id="75054-256">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="75054-256">Is-Single-Valued</span></span>       | <span data-ttu-id="75054-257">True</span><span class="sxs-lookup"><span data-stu-id="75054-257">True</span></span>                              |
| <span data-ttu-id="75054-258">Está indexado</span><span class="sxs-lookup"><span data-stu-id="75054-258">Is Indexed</span></span>             | <span data-ttu-id="75054-259">False</span><span class="sxs-lookup"><span data-stu-id="75054-259">False</span></span>                             |
| <span data-ttu-id="75054-260">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="75054-260">In Global Catalog</span></span>      | <span data-ttu-id="75054-261">False</span><span class="sxs-lookup"><span data-stu-id="75054-261">False</span></span>                             |
| <span data-ttu-id="75054-262">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="75054-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="75054-263">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="75054-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="75054-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75054-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="75054-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75054-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="75054-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75054-266">Search-Flags</span></span>           | <span data-ttu-id="75054-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75054-267">0x00000000</span></span>                        |
| <span data-ttu-id="75054-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75054-268">System-Flags</span></span>           | <span data-ttu-id="75054-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75054-269">0x00000010</span></span>                        |
| <span data-ttu-id="75054-270">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="75054-270">Classes used in</span></span>        | [<span data-ttu-id="75054-271">**User**</span><span class="sxs-lookup"><span data-stu-id="75054-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="75054-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="75054-272">Windows Server 2012</span></span>



| <span data-ttu-id="75054-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="75054-273">Entry</span></span> | <span data-ttu-id="75054-274">Value</span><span class="sxs-lookup"><span data-stu-id="75054-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="75054-275">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="75054-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="75054-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75054-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="75054-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="75054-277">System-Only</span></span>            | <span data-ttu-id="75054-278">False</span><span class="sxs-lookup"><span data-stu-id="75054-278">False</span></span>                             |
| <span data-ttu-id="75054-279">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="75054-279">Is-Single-Valued</span></span>       | <span data-ttu-id="75054-280">True</span><span class="sxs-lookup"><span data-stu-id="75054-280">True</span></span>                              |
| <span data-ttu-id="75054-281">Está indexado</span><span class="sxs-lookup"><span data-stu-id="75054-281">Is Indexed</span></span>             | <span data-ttu-id="75054-282">False</span><span class="sxs-lookup"><span data-stu-id="75054-282">False</span></span>                             |
| <span data-ttu-id="75054-283">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="75054-283">In Global Catalog</span></span>      | <span data-ttu-id="75054-284">False</span><span class="sxs-lookup"><span data-stu-id="75054-284">False</span></span>                             |
| <span data-ttu-id="75054-285">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="75054-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="75054-286">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="75054-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="75054-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75054-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="75054-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75054-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="75054-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75054-289">Search-Flags</span></span>           | <span data-ttu-id="75054-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75054-290">0x00000000</span></span>                        |
| <span data-ttu-id="75054-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75054-291">System-Flags</span></span>           | <span data-ttu-id="75054-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75054-292">0x00000010</span></span>                        |
| <span data-ttu-id="75054-293">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="75054-293">Classes used in</span></span>        | [<span data-ttu-id="75054-294">**User**</span><span class="sxs-lookup"><span data-stu-id="75054-294">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="75054-295">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75054-295">Remarks</span></span>

<span data-ttu-id="75054-296">La parte alta de este entero grande corresponde al miembro **dwHighDateTime** de la estructura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) y la parte baja corresponde al miembro **dwLowDateTime** de la estructura **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="75054-296">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="75054-297">Este valor de atributo solo se restablece cuando la cuenta ha iniciado sesión correctamente.</span><span class="sxs-lookup"><span data-stu-id="75054-297">This attribute value is only reset when the account is logged onto successfully.</span></span> <span data-ttu-id="75054-298">Esto significa que este valor puede ser distinto de cero, pero la cuenta no está bloqueada. Para determinar con precisión si la cuenta está bloqueada, debe agregar la [**duración del bloqueo**](a-lockoutduration.md) a este momento y comparar el resultado con la hora actual, teniendo en cuenta las zonas horarias locales y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="75054-298">This means that this value may be non zero, yet the account is not locked out. To accurately determine if the account is locked out, you must add the [**Lockout-Duration**](a-lockoutduration.md) to this time and compare the result to the current time, accounting for local time zones and daylight savings time.</span></span>

## <a name="see-also"></a><span data-ttu-id="75054-299">Vea también</span><span class="sxs-lookup"><span data-stu-id="75054-299">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75054-300">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="75054-300">**FILETIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[<span data-ttu-id="75054-301">**Bloqueo: duración**</span><span class="sxs-lookup"><span data-stu-id="75054-301">**Lockout-Duration**</span></span>](a-lockoutduration.md)
</dt> </dl>

 

