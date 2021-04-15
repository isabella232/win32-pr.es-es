---
title: Atributo de tiempo de contraseña incorrecto
description: La última vez y la fecha en que se intentó iniciar sesión en esta cuenta con una contraseña no válida.
ms.assetid: 8e8c5b73-b42d-4a62-89af-c0ff2fe106d8
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de tiempo de contraseña incorrecto
- badPasswordTime esquema de AD de atributos
topic_type:
- apiref
api_name:
- Bad-Password-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47df09d0ff2d82a9180c43721aa09e5363884e24
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494104"
---
# <a name="bad-password-time-attribute"></a><span data-ttu-id="6a3da-105">Atributo de tiempo de contraseña incorrecto</span><span class="sxs-lookup"><span data-stu-id="6a3da-105">Bad-Password-Time attribute</span></span>

<span data-ttu-id="6a3da-106">La última vez y la fecha en que se intentó iniciar sesión en esta cuenta con una contraseña no válida.</span><span class="sxs-lookup"><span data-stu-id="6a3da-106">The last time and date that an attempt to log on to this account was made with a password that is not valid.</span></span> <span data-ttu-id="6a3da-107">Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="6a3da-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="6a3da-108">Un valor de cero significa que se desconoce la última vez que se usó una contraseña incorrecta.</span><span class="sxs-lookup"><span data-stu-id="6a3da-108">A value of zero means that the last time a incorrect password was used is unknown.</span></span>



| <span data-ttu-id="6a3da-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a3da-109">Entry</span></span> | <span data-ttu-id="6a3da-110">Value</span><span class="sxs-lookup"><span data-stu-id="6a3da-110">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="6a3da-111">CN</span><span class="sxs-lookup"><span data-stu-id="6a3da-111">CN</span></span>                | <span data-ttu-id="6a3da-112">Hora de contraseña incorrecta</span><span class="sxs-lookup"><span data-stu-id="6a3da-112">Bad-Password-Time</span></span>                         |
| <span data-ttu-id="6a3da-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="6a3da-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6a3da-114">badPasswordTime</span><span class="sxs-lookup"><span data-stu-id="6a3da-114">badPasswordTime</span></span>                           |
| <span data-ttu-id="6a3da-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="6a3da-115">Size</span></span>              | <span data-ttu-id="6a3da-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="6a3da-116">8 bytes</span></span>                                   |
| <span data-ttu-id="6a3da-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="6a3da-117">Update Privilege</span></span>  | <span data-ttu-id="6a3da-118">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="6a3da-118">This value is set by the system.</span></span>          |
| <span data-ttu-id="6a3da-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="6a3da-119">Update Frequency</span></span>  | <span data-ttu-id="6a3da-120">Cada vez que el usuario escribe una contraseña incorrecta.</span><span class="sxs-lookup"><span data-stu-id="6a3da-120">Each time the user enters a bad password.</span></span> |
| <span data-ttu-id="6a3da-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6a3da-121">Attribute-Id</span></span>      | <span data-ttu-id="6a3da-122">1.2.840.113556.1.4.49</span><span class="sxs-lookup"><span data-stu-id="6a3da-122">1.2.840.113556.1.4.49</span></span>                     |
| <span data-ttu-id="6a3da-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6a3da-123">System-Id-Guid</span></span>    | <span data-ttu-id="6a3da-124">bf96792d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6a3da-124">bf96792d-0de6-11d0-a285-00aa003049e2</span></span>      |
| <span data-ttu-id="6a3da-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a3da-125">Syntax</span></span>            | [<span data-ttu-id="6a3da-126">**Interval**</span><span class="sxs-lookup"><span data-stu-id="6a3da-126">**Interval**</span></span>](s-interval.md)            |



## <a name="implementations"></a><span data-ttu-id="6a3da-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="6a3da-127">Implementations</span></span>

-   [<span data-ttu-id="6a3da-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6a3da-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6a3da-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6a3da-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6a3da-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6a3da-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6a3da-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6a3da-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6a3da-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6a3da-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6a3da-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6a3da-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6a3da-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6a3da-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6a3da-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6a3da-135">Windows 2000 Server</span></span>



| <span data-ttu-id="6a3da-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a3da-136">Entry</span></span> | <span data-ttu-id="6a3da-137">Value</span><span class="sxs-lookup"><span data-stu-id="6a3da-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6a3da-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a3da-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6a3da-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a3da-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6a3da-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a3da-140">System-Only</span></span>            | <span data-ttu-id="6a3da-141">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-141">False</span></span>                             |
| <span data-ttu-id="6a3da-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a3da-142">Is-Single-Valued</span></span>       | <span data-ttu-id="6a3da-143">True</span><span class="sxs-lookup"><span data-stu-id="6a3da-143">True</span></span>                              |
| <span data-ttu-id="6a3da-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a3da-144">Is Indexed</span></span>             | <span data-ttu-id="6a3da-145">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-145">False</span></span>                             |
| <span data-ttu-id="6a3da-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a3da-146">In Global Catalog</span></span>      | <span data-ttu-id="6a3da-147">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-147">False</span></span>                             |
| <span data-ttu-id="6a3da-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a3da-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a3da-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a3da-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6a3da-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a3da-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6a3da-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a3da-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6a3da-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a3da-152">Search-Flags</span></span>           | <span data-ttu-id="6a3da-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a3da-153">0x00000000</span></span>                        |
| <span data-ttu-id="6a3da-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a3da-154">System-Flags</span></span>           | <span data-ttu-id="6a3da-155">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6a3da-155">0x00000011</span></span>                        |
| <span data-ttu-id="6a3da-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a3da-156">Classes used in</span></span>        | [<span data-ttu-id="6a3da-157">**User**</span><span class="sxs-lookup"><span data-stu-id="6a3da-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6a3da-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6a3da-158">Windows Server 2003</span></span>



| <span data-ttu-id="6a3da-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a3da-159">Entry</span></span> | <span data-ttu-id="6a3da-160">Value</span><span class="sxs-lookup"><span data-stu-id="6a3da-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6a3da-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a3da-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6a3da-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a3da-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6a3da-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a3da-163">System-Only</span></span>            | <span data-ttu-id="6a3da-164">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-164">False</span></span>                             |
| <span data-ttu-id="6a3da-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a3da-165">Is-Single-Valued</span></span>       | <span data-ttu-id="6a3da-166">True</span><span class="sxs-lookup"><span data-stu-id="6a3da-166">True</span></span>                              |
| <span data-ttu-id="6a3da-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a3da-167">Is Indexed</span></span>             | <span data-ttu-id="6a3da-168">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-168">False</span></span>                             |
| <span data-ttu-id="6a3da-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a3da-169">In Global Catalog</span></span>      | <span data-ttu-id="6a3da-170">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-170">False</span></span>                             |
| <span data-ttu-id="6a3da-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a3da-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a3da-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a3da-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6a3da-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a3da-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6a3da-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a3da-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6a3da-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a3da-175">Search-Flags</span></span>           | <span data-ttu-id="6a3da-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a3da-176">0x00000000</span></span>                        |
| <span data-ttu-id="6a3da-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a3da-177">System-Flags</span></span>           | <span data-ttu-id="6a3da-178">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6a3da-178">0x00000011</span></span>                        |
| <span data-ttu-id="6a3da-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a3da-179">Classes used in</span></span>        | [<span data-ttu-id="6a3da-180">**User**</span><span class="sxs-lookup"><span data-stu-id="6a3da-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6a3da-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="6a3da-181">ADAM</span></span>



| <span data-ttu-id="6a3da-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a3da-182">Entry</span></span> | <span data-ttu-id="6a3da-183">Value</span><span class="sxs-lookup"><span data-stu-id="6a3da-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="6a3da-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a3da-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6a3da-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a3da-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6a3da-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a3da-186">System-Only</span></span>            | <span data-ttu-id="6a3da-187">True</span><span class="sxs-lookup"><span data-stu-id="6a3da-187">True</span></span>                                                              |
| <span data-ttu-id="6a3da-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a3da-188">Is-Single-Valued</span></span>       | <span data-ttu-id="6a3da-189">True</span><span class="sxs-lookup"><span data-stu-id="6a3da-189">True</span></span>                                                              |
| <span data-ttu-id="6a3da-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a3da-190">Is Indexed</span></span>             | <span data-ttu-id="6a3da-191">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-191">False</span></span>                                                             |
| <span data-ttu-id="6a3da-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a3da-192">In Global Catalog</span></span>      | <span data-ttu-id="6a3da-193">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-193">False</span></span>                                                             |
| <span data-ttu-id="6a3da-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a3da-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a3da-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a3da-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="6a3da-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a3da-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="6a3da-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a3da-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="6a3da-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a3da-198">Search-Flags</span></span>           | <span data-ttu-id="6a3da-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a3da-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="6a3da-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a3da-200">System-Flags</span></span>           | <span data-ttu-id="6a3da-201">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6a3da-201">0x00000011</span></span>                                                        |
| <span data-ttu-id="6a3da-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a3da-202">Classes used in</span></span>        | [<span data-ttu-id="6a3da-203">**Objeto MS-DS-Bindable**</span><span class="sxs-lookup"><span data-stu-id="6a3da-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6a3da-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6a3da-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6a3da-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a3da-205">Entry</span></span> | <span data-ttu-id="6a3da-206">Value</span><span class="sxs-lookup"><span data-stu-id="6a3da-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6a3da-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a3da-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6a3da-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a3da-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6a3da-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a3da-209">System-Only</span></span>            | <span data-ttu-id="6a3da-210">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-210">False</span></span>                             |
| <span data-ttu-id="6a3da-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a3da-211">Is-Single-Valued</span></span>       | <span data-ttu-id="6a3da-212">True</span><span class="sxs-lookup"><span data-stu-id="6a3da-212">True</span></span>                              |
| <span data-ttu-id="6a3da-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a3da-213">Is Indexed</span></span>             | <span data-ttu-id="6a3da-214">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-214">False</span></span>                             |
| <span data-ttu-id="6a3da-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a3da-215">In Global Catalog</span></span>      | <span data-ttu-id="6a3da-216">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-216">False</span></span>                             |
| <span data-ttu-id="6a3da-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a3da-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a3da-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a3da-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6a3da-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a3da-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6a3da-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a3da-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6a3da-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a3da-221">Search-Flags</span></span>           | <span data-ttu-id="6a3da-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a3da-222">0x00000000</span></span>                        |
| <span data-ttu-id="6a3da-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a3da-223">System-Flags</span></span>           | <span data-ttu-id="6a3da-224">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6a3da-224">0x00000011</span></span>                        |
| <span data-ttu-id="6a3da-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a3da-225">Classes used in</span></span>        | [<span data-ttu-id="6a3da-226">**User**</span><span class="sxs-lookup"><span data-stu-id="6a3da-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6a3da-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a3da-227">Windows Server 2008</span></span>



| <span data-ttu-id="6a3da-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a3da-228">Entry</span></span> | <span data-ttu-id="6a3da-229">Value</span><span class="sxs-lookup"><span data-stu-id="6a3da-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6a3da-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a3da-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6a3da-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a3da-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6a3da-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a3da-232">System-Only</span></span>            | <span data-ttu-id="6a3da-233">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-233">False</span></span>                             |
| <span data-ttu-id="6a3da-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a3da-234">Is-Single-Valued</span></span>       | <span data-ttu-id="6a3da-235">True</span><span class="sxs-lookup"><span data-stu-id="6a3da-235">True</span></span>                              |
| <span data-ttu-id="6a3da-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a3da-236">Is Indexed</span></span>             | <span data-ttu-id="6a3da-237">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-237">False</span></span>                             |
| <span data-ttu-id="6a3da-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a3da-238">In Global Catalog</span></span>      | <span data-ttu-id="6a3da-239">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-239">False</span></span>                             |
| <span data-ttu-id="6a3da-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a3da-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a3da-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a3da-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6a3da-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a3da-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6a3da-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a3da-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6a3da-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a3da-244">Search-Flags</span></span>           | <span data-ttu-id="6a3da-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a3da-245">0x00000000</span></span>                        |
| <span data-ttu-id="6a3da-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a3da-246">System-Flags</span></span>           | <span data-ttu-id="6a3da-247">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6a3da-247">0x00000011</span></span>                        |
| <span data-ttu-id="6a3da-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a3da-248">Classes used in</span></span>        | [<span data-ttu-id="6a3da-249">**User**</span><span class="sxs-lookup"><span data-stu-id="6a3da-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6a3da-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6a3da-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6a3da-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a3da-251">Entry</span></span> | <span data-ttu-id="6a3da-252">Value</span><span class="sxs-lookup"><span data-stu-id="6a3da-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6a3da-253">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a3da-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6a3da-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a3da-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6a3da-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a3da-255">System-Only</span></span>            | <span data-ttu-id="6a3da-256">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-256">False</span></span>                             |
| <span data-ttu-id="6a3da-257">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a3da-257">Is-Single-Valued</span></span>       | <span data-ttu-id="6a3da-258">True</span><span class="sxs-lookup"><span data-stu-id="6a3da-258">True</span></span>                              |
| <span data-ttu-id="6a3da-259">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a3da-259">Is Indexed</span></span>             | <span data-ttu-id="6a3da-260">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-260">False</span></span>                             |
| <span data-ttu-id="6a3da-261">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a3da-261">In Global Catalog</span></span>      | <span data-ttu-id="6a3da-262">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-262">False</span></span>                             |
| <span data-ttu-id="6a3da-263">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a3da-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a3da-264">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a3da-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6a3da-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a3da-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6a3da-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a3da-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6a3da-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a3da-267">Search-Flags</span></span>           | <span data-ttu-id="6a3da-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a3da-268">0x00000000</span></span>                        |
| <span data-ttu-id="6a3da-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a3da-269">System-Flags</span></span>           | <span data-ttu-id="6a3da-270">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6a3da-270">0x00000011</span></span>                        |
| <span data-ttu-id="6a3da-271">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a3da-271">Classes used in</span></span>        | [<span data-ttu-id="6a3da-272">**User**</span><span class="sxs-lookup"><span data-stu-id="6a3da-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6a3da-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a3da-273">Windows Server 2012</span></span>



| <span data-ttu-id="6a3da-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a3da-274">Entry</span></span> | <span data-ttu-id="6a3da-275">Value</span><span class="sxs-lookup"><span data-stu-id="6a3da-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6a3da-276">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a3da-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6a3da-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a3da-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6a3da-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a3da-278">System-Only</span></span>            | <span data-ttu-id="6a3da-279">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-279">False</span></span>                             |
| <span data-ttu-id="6a3da-280">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a3da-280">Is-Single-Valued</span></span>       | <span data-ttu-id="6a3da-281">True</span><span class="sxs-lookup"><span data-stu-id="6a3da-281">True</span></span>                              |
| <span data-ttu-id="6a3da-282">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a3da-282">Is Indexed</span></span>             | <span data-ttu-id="6a3da-283">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-283">False</span></span>                             |
| <span data-ttu-id="6a3da-284">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a3da-284">In Global Catalog</span></span>      | <span data-ttu-id="6a3da-285">False</span><span class="sxs-lookup"><span data-stu-id="6a3da-285">False</span></span>                             |
| <span data-ttu-id="6a3da-286">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a3da-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a3da-287">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a3da-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6a3da-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a3da-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6a3da-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a3da-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6a3da-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a3da-290">Search-Flags</span></span>           | <span data-ttu-id="6a3da-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a3da-291">0x00000000</span></span>                        |
| <span data-ttu-id="6a3da-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a3da-292">System-Flags</span></span>           | <span data-ttu-id="6a3da-293">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6a3da-293">0x00000011</span></span>                        |
| <span data-ttu-id="6a3da-294">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a3da-294">Classes used in</span></span>        | [<span data-ttu-id="6a3da-295">**User**</span><span class="sxs-lookup"><span data-stu-id="6a3da-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="6a3da-296">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a3da-296">Remarks</span></span>

<span data-ttu-id="6a3da-297">La parte alta de este entero grande corresponde al miembro **dwHighDateTime** de la estructura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) y la parte baja corresponde al miembro **dwLowDateTime** de la estructura **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="6a3da-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="6a3da-298">Este atributo no se replica y se mantiene por separado en cada controlador de dominio del dominio.</span><span class="sxs-lookup"><span data-stu-id="6a3da-298">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="6a3da-299">Para obtener un valor exacto de la última hora de contraseña incorrecta del usuario en el dominio, se deben consultar todos los controladores de dominio del dominio.</span><span class="sxs-lookup"><span data-stu-id="6a3da-299">To get an accurate value for the user's last bad password time in the domain, each domain controller in the domain must be queried.</span></span> <span data-ttu-id="6a3da-300">El valor más grande que se obtiene representa el verdadero tiempo de contraseña incorrecto.</span><span class="sxs-lookup"><span data-stu-id="6a3da-300">The largest value that is obtained represents the true bad password time.</span></span>

 

