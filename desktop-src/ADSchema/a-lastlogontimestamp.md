---
title: Last-Logon-atributo timestamp
description: Esta es la hora a la que el usuario inició sesión en el dominio por última vez.
ms.assetid: 6c94bccb-1e0a-421c-a00c-5f6e6389690f
ms.tgt_platform: multiple
keywords:
- Último inicio de sesión-esquema de marca de tiempo del atributo AD
- lastLogonTimestamp esquema de AD de atributos
topic_type:
- apiref
api_name:
- Last-Logon-Timestamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6d7668891d008e1b16b7dc148462498e9210b4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151472"
---
# <a name="last-logon-timestamp-attribute"></a><span data-ttu-id="7aed5-105">Last-Logon-atributo timestamp</span><span class="sxs-lookup"><span data-stu-id="7aed5-105">Last-Logon-Timestamp attribute</span></span>

<span data-ttu-id="7aed5-106">Esta es la hora a la que el usuario inició sesión en el dominio por última vez.</span><span class="sxs-lookup"><span data-stu-id="7aed5-106">This is the time that the user last logged into the domain.</span></span> <span data-ttu-id="7aed5-107">Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="7aed5-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="7aed5-108">Cada vez que un usuario inicia sesión, el valor de este atributo se lee desde el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="7aed5-108">Whenever a user logs on, the value of this attribute is read from the DC.</span></span> <span data-ttu-id="7aed5-109">Si el valor es anterior \[ `current_time - msDS-LogonTimeSyncInterval` \] , se actualiza el valor.</span><span class="sxs-lookup"><span data-stu-id="7aed5-109">If the value is older \[ `current_time - msDS-LogonTimeSyncInterval` \], the value is updated.</span></span> <span data-ttu-id="7aed5-110">La actualización inicial después del aumento del nivel funcional del dominio se calcula como 14 días menos el porcentaje aleatorio de 5 días.</span><span class="sxs-lookup"><span data-stu-id="7aed5-110">The initial update after the raise of the domain functional level is calculated as 14 days minus random percentage of 5 days.</span></span>



| <span data-ttu-id="7aed5-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="7aed5-111">Entry</span></span> | <span data-ttu-id="7aed5-112">Value</span><span class="sxs-lookup"><span data-stu-id="7aed5-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7aed5-113">CN</span><span class="sxs-lookup"><span data-stu-id="7aed5-113">CN</span></span>                | <span data-ttu-id="7aed5-114">Último inicio de sesión-marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="7aed5-114">Last-Logon-Timestamp</span></span>                                                                                                   |
| <span data-ttu-id="7aed5-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="7aed5-115">Ldap-Display-Name</span></span> | <span data-ttu-id="7aed5-116">lastLogonTimestamp</span><span class="sxs-lookup"><span data-stu-id="7aed5-116">lastLogonTimestamp</span></span>                                                                                                     |
| <span data-ttu-id="7aed5-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="7aed5-117">Size</span></span>              | \-                                                                                                                     |
| <span data-ttu-id="7aed5-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="7aed5-118">Update Privilege</span></span>  | <span data-ttu-id="7aed5-119">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="7aed5-119">This value is set by the system.</span></span>                                                                                       |
| <span data-ttu-id="7aed5-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="7aed5-120">Update Frequency</span></span>  | <span data-ttu-id="7aed5-121">Cuando el usuario inicia sesión, y si este valor es anterior a la hora actual menos el valor de msDS-LogonTimeSyncInterval.</span><span class="sxs-lookup"><span data-stu-id="7aed5-121">When the user logs on, and if this value is older than the current time minus the value of msDS-LogonTimeSyncInterval.</span></span> |
| <span data-ttu-id="7aed5-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7aed5-122">Attribute-Id</span></span>      | <span data-ttu-id="7aed5-123">1.2.840.113556.1.4.1696</span><span class="sxs-lookup"><span data-stu-id="7aed5-123">1.2.840.113556.1.4.1696</span></span>                                                                                                |
| <span data-ttu-id="7aed5-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7aed5-124">System-Id-Guid</span></span>    | <span data-ttu-id="7aed5-125">c0e20a04-0e5a-4ff3-9482-5efeaecd7060</span><span class="sxs-lookup"><span data-stu-id="7aed5-125">c0e20a04-0e5a-4ff3-9482-5efeaecd7060</span></span>                                                                                   |
| <span data-ttu-id="7aed5-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7aed5-126">Syntax</span></span>            | [<span data-ttu-id="7aed5-127">**Interval**</span><span class="sxs-lookup"><span data-stu-id="7aed5-127">**Interval**</span></span>](s-interval.md)                                                                                         |



## <a name="implementations"></a><span data-ttu-id="7aed5-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="7aed5-128">Implementations</span></span>

-   [<span data-ttu-id="7aed5-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7aed5-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7aed5-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7aed5-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7aed5-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7aed5-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7aed5-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7aed5-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7aed5-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7aed5-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7aed5-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7aed5-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="7aed5-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7aed5-135">Windows Server 2003</span></span>



| <span data-ttu-id="7aed5-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="7aed5-136">Entry</span></span> | <span data-ttu-id="7aed5-137">Value</span><span class="sxs-lookup"><span data-stu-id="7aed5-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7aed5-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7aed5-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7aed5-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7aed5-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7aed5-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="7aed5-140">System-Only</span></span>            | <span data-ttu-id="7aed5-141">False</span><span class="sxs-lookup"><span data-stu-id="7aed5-141">False</span></span>                             |
| <span data-ttu-id="7aed5-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7aed5-142">Is-Single-Valued</span></span>       | <span data-ttu-id="7aed5-143">True</span><span class="sxs-lookup"><span data-stu-id="7aed5-143">True</span></span>                              |
| <span data-ttu-id="7aed5-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7aed5-144">Is Indexed</span></span>             | <span data-ttu-id="7aed5-145">False</span><span class="sxs-lookup"><span data-stu-id="7aed5-145">False</span></span>                             |
| <span data-ttu-id="7aed5-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7aed5-146">In Global Catalog</span></span>      | <span data-ttu-id="7aed5-147">False</span><span class="sxs-lookup"><span data-stu-id="7aed5-147">False</span></span>                             |
| <span data-ttu-id="7aed5-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7aed5-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="7aed5-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7aed5-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7aed5-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7aed5-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7aed5-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7aed5-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7aed5-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7aed5-152">Search-Flags</span></span>           | <span data-ttu-id="7aed5-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7aed5-153">0x00000000</span></span>                        |
| <span data-ttu-id="7aed5-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7aed5-154">System-Flags</span></span>           | <span data-ttu-id="7aed5-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7aed5-155">0x00000010</span></span>                        |
| <span data-ttu-id="7aed5-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7aed5-156">Classes used in</span></span>        | [<span data-ttu-id="7aed5-157">**User**</span><span class="sxs-lookup"><span data-stu-id="7aed5-157">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7aed5-158">ADAM</span><span class="sxs-lookup"><span data-stu-id="7aed5-158">ADAM</span></span>



| <span data-ttu-id="7aed5-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="7aed5-159">Entry</span></span> | <span data-ttu-id="7aed5-160">Value</span><span class="sxs-lookup"><span data-stu-id="7aed5-160">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="7aed5-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7aed5-161">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="7aed5-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7aed5-162">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="7aed5-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="7aed5-163">System-Only</span></span>            | <span data-ttu-id="7aed5-164">True</span><span class="sxs-lookup"><span data-stu-id="7aed5-164">True</span></span>                                                              |
| <span data-ttu-id="7aed5-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7aed5-165">Is-Single-Valued</span></span>       | <span data-ttu-id="7aed5-166">True</span><span class="sxs-lookup"><span data-stu-id="7aed5-166">True</span></span>                                                              |
| <span data-ttu-id="7aed5-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7aed5-167">Is Indexed</span></span>             | <span data-ttu-id="7aed5-168">False</span><span class="sxs-lookup"><span data-stu-id="7aed5-168">False</span></span>                                                             |
| <span data-ttu-id="7aed5-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7aed5-169">In Global Catalog</span></span>      | <span data-ttu-id="7aed5-170">False</span><span class="sxs-lookup"><span data-stu-id="7aed5-170">False</span></span>                                                             |
| <span data-ttu-id="7aed5-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7aed5-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="7aed5-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7aed5-172">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="7aed5-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7aed5-173">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="7aed5-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7aed5-174">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="7aed5-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7aed5-175">Search-Flags</span></span>           | <span data-ttu-id="7aed5-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7aed5-176">0x00000000</span></span>                                                        |
| <span data-ttu-id="7aed5-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7aed5-177">System-Flags</span></span>           | <span data-ttu-id="7aed5-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7aed5-178">0x00000010</span></span>                                                        |
| <span data-ttu-id="7aed5-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7aed5-179">Classes used in</span></span>        | [<span data-ttu-id="7aed5-180">**Objeto MS-DS-Bindable**</span><span class="sxs-lookup"><span data-stu-id="7aed5-180">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7aed5-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7aed5-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7aed5-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="7aed5-182">Entry</span></span> | <span data-ttu-id="7aed5-183">Value</span><span class="sxs-lookup"><span data-stu-id="7aed5-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7aed5-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7aed5-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7aed5-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7aed5-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7aed5-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="7aed5-186">System-Only</span></span>            | <span data-ttu-id="7aed5-187">False</span><span class="sxs-lookup"><span data-stu-id="7aed5-187">False</span></span>                             |
| <span data-ttu-id="7aed5-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7aed5-188">Is-Single-Valued</span></span>       | <span data-ttu-id="7aed5-189">True</span><span class="sxs-lookup"><span data-stu-id="7aed5-189">True</span></span>                              |
| <span data-ttu-id="7aed5-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7aed5-190">Is Indexed</span></span>             | <span data-ttu-id="7aed5-191">False</span><span class="sxs-lookup"><span data-stu-id="7aed5-191">False</span></span>                             |
| <span data-ttu-id="7aed5-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7aed5-192">In Global Catalog</span></span>      | <span data-ttu-id="7aed5-193">False</span><span class="sxs-lookup"><span data-stu-id="7aed5-193">False</span></span>                             |
| <span data-ttu-id="7aed5-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7aed5-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="7aed5-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7aed5-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7aed5-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7aed5-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7aed5-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7aed5-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7aed5-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7aed5-198">Search-Flags</span></span>           | <span data-ttu-id="7aed5-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7aed5-199">0x00000000</span></span>                        |
| <span data-ttu-id="7aed5-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7aed5-200">System-Flags</span></span>           | <span data-ttu-id="7aed5-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7aed5-201">0x00000010</span></span>                        |
| <span data-ttu-id="7aed5-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7aed5-202">Classes used in</span></span>        | [<span data-ttu-id="7aed5-203">**User**</span><span class="sxs-lookup"><span data-stu-id="7aed5-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7aed5-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7aed5-204">Windows Server 2008</span></span>



| <span data-ttu-id="7aed5-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="7aed5-205">Entry</span></span> | <span data-ttu-id="7aed5-206">Value</span><span class="sxs-lookup"><span data-stu-id="7aed5-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7aed5-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7aed5-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7aed5-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7aed5-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7aed5-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="7aed5-209">System-Only</span></span>            | <span data-ttu-id="7aed5-210">False</span><span class="sxs-lookup"><span data-stu-id="7aed5-210">False</span></span>                             |
| <span data-ttu-id="7aed5-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7aed5-211">Is-Single-Valued</span></span>       | <span data-ttu-id="7aed5-212">True</span><span class="sxs-lookup"><span data-stu-id="7aed5-212">True</span></span>                              |
| <span data-ttu-id="7aed5-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7aed5-213">Is Indexed</span></span>             | <span data-ttu-id="7aed5-214">True</span><span class="sxs-lookup"><span data-stu-id="7aed5-214">True</span></span>                              |
| <span data-ttu-id="7aed5-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7aed5-215">In Global Catalog</span></span>      | <span data-ttu-id="7aed5-216">True</span><span class="sxs-lookup"><span data-stu-id="7aed5-216">True</span></span>                              |
| <span data-ttu-id="7aed5-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7aed5-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="7aed5-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7aed5-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7aed5-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7aed5-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7aed5-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7aed5-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7aed5-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7aed5-221">Search-Flags</span></span>           | <span data-ttu-id="7aed5-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7aed5-222">0x00000001</span></span>                        |
| <span data-ttu-id="7aed5-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7aed5-223">System-Flags</span></span>           | <span data-ttu-id="7aed5-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7aed5-224">0x00000010</span></span>                        |
| <span data-ttu-id="7aed5-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7aed5-225">Classes used in</span></span>        | [<span data-ttu-id="7aed5-226">**User**</span><span class="sxs-lookup"><span data-stu-id="7aed5-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7aed5-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7aed5-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7aed5-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="7aed5-228">Entry</span></span> | <span data-ttu-id="7aed5-229">Value</span><span class="sxs-lookup"><span data-stu-id="7aed5-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7aed5-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7aed5-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7aed5-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7aed5-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7aed5-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="7aed5-232">System-Only</span></span>            | <span data-ttu-id="7aed5-233">False</span><span class="sxs-lookup"><span data-stu-id="7aed5-233">False</span></span>                             |
| <span data-ttu-id="7aed5-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7aed5-234">Is-Single-Valued</span></span>       | <span data-ttu-id="7aed5-235">True</span><span class="sxs-lookup"><span data-stu-id="7aed5-235">True</span></span>                              |
| <span data-ttu-id="7aed5-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7aed5-236">Is Indexed</span></span>             | <span data-ttu-id="7aed5-237">True</span><span class="sxs-lookup"><span data-stu-id="7aed5-237">True</span></span>                              |
| <span data-ttu-id="7aed5-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7aed5-238">In Global Catalog</span></span>      | <span data-ttu-id="7aed5-239">True</span><span class="sxs-lookup"><span data-stu-id="7aed5-239">True</span></span>                              |
| <span data-ttu-id="7aed5-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7aed5-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="7aed5-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7aed5-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7aed5-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7aed5-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7aed5-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7aed5-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7aed5-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7aed5-244">Search-Flags</span></span>           | <span data-ttu-id="7aed5-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7aed5-245">0x00000001</span></span>                        |
| <span data-ttu-id="7aed5-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7aed5-246">System-Flags</span></span>           | <span data-ttu-id="7aed5-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7aed5-247">0x00000010</span></span>                        |
| <span data-ttu-id="7aed5-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7aed5-248">Classes used in</span></span>        | [<span data-ttu-id="7aed5-249">**User**</span><span class="sxs-lookup"><span data-stu-id="7aed5-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7aed5-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7aed5-250">Windows Server 2012</span></span>



| <span data-ttu-id="7aed5-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="7aed5-251">Entry</span></span> | <span data-ttu-id="7aed5-252">Value</span><span class="sxs-lookup"><span data-stu-id="7aed5-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7aed5-253">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7aed5-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7aed5-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7aed5-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7aed5-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="7aed5-255">System-Only</span></span>            | <span data-ttu-id="7aed5-256">False</span><span class="sxs-lookup"><span data-stu-id="7aed5-256">False</span></span>                             |
| <span data-ttu-id="7aed5-257">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7aed5-257">Is-Single-Valued</span></span>       | <span data-ttu-id="7aed5-258">True</span><span class="sxs-lookup"><span data-stu-id="7aed5-258">True</span></span>                              |
| <span data-ttu-id="7aed5-259">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7aed5-259">Is Indexed</span></span>             | <span data-ttu-id="7aed5-260">True</span><span class="sxs-lookup"><span data-stu-id="7aed5-260">True</span></span>                              |
| <span data-ttu-id="7aed5-261">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7aed5-261">In Global Catalog</span></span>      | <span data-ttu-id="7aed5-262">True</span><span class="sxs-lookup"><span data-stu-id="7aed5-262">True</span></span>                              |
| <span data-ttu-id="7aed5-263">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7aed5-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="7aed5-264">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7aed5-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7aed5-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7aed5-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7aed5-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7aed5-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7aed5-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7aed5-267">Search-Flags</span></span>           | <span data-ttu-id="7aed5-268">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7aed5-268">0x00000001</span></span>                        |
| <span data-ttu-id="7aed5-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7aed5-269">System-Flags</span></span>           | <span data-ttu-id="7aed5-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7aed5-270">0x00000010</span></span>                        |
| <span data-ttu-id="7aed5-271">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7aed5-271">Classes used in</span></span>        | [<span data-ttu-id="7aed5-272">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="7aed5-272">**User**</span></span>](c-user.md)<br/> |



 

 





