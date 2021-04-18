---
title: 'PWD: atributo Last-set'
description: Fecha y hora en que se cambió por última vez la contraseña de esta cuenta.
ms.assetid: 06ca5cd5-a285-488a-9db0-c698b82a847d
ms.tgt_platform: multiple
keywords:
- Pwd-último atributo de conjunto de esquemas de AD
- pwdLastSet esquema de AD de atributos
topic_type:
- apiref
api_name:
- Pwd-Last-Set
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc49fbbf768d2ca873f6f35f61022cc9182830b1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658992"
---
# <a name="pwd-last-set-attribute"></a><span data-ttu-id="0412b-105">PWD: atributo Last-set</span><span class="sxs-lookup"><span data-stu-id="0412b-105">Pwd-Last-Set attribute</span></span>

<span data-ttu-id="0412b-106">Fecha y hora en que se cambió por última vez la contraseña de esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="0412b-106">The date and time that the password for this account was last changed.</span></span> <span data-ttu-id="0412b-107">Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="0412b-107">This value is stored as a large integer that represents the number of 100 nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="0412b-108">Si este valor se establece en 0 y el atributo [**User-Account-Control**](a-useraccountcontrol.md) no contiene la marca de la **\_ \_ \_ passwd no expire** , el usuario debe establecer la contraseña en el siguiente inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="0412b-108">If this value is set to 0 and the [**User-Account-Control**](a-useraccountcontrol.md) attribute does not contain the **UF\_DONT\_EXPIRE\_PASSWD** flag, then the user must set the password at the next logon.</span></span>



| <span data-ttu-id="0412b-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="0412b-109">Entry</span></span> | <span data-ttu-id="0412b-110">Value</span><span class="sxs-lookup"><span data-stu-id="0412b-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0412b-111">CN</span><span class="sxs-lookup"><span data-stu-id="0412b-111">CN</span></span>                | <span data-ttu-id="0412b-112">PWD: último conjunto</span><span class="sxs-lookup"><span data-stu-id="0412b-112">Pwd-Last-Set</span></span>                         |
| <span data-ttu-id="0412b-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="0412b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="0412b-114">pwdLastSet</span><span class="sxs-lookup"><span data-stu-id="0412b-114">pwdLastSet</span></span>                           |
| <span data-ttu-id="0412b-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="0412b-115">Size</span></span>              | <span data-ttu-id="0412b-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="0412b-116">8 bytes</span></span>                              |
| <span data-ttu-id="0412b-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="0412b-117">Update Privilege</span></span>  | <span data-ttu-id="0412b-118">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="0412b-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="0412b-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="0412b-119">Update Frequency</span></span>  | <span data-ttu-id="0412b-120">Cada vez que se cambia la contraseña.</span><span class="sxs-lookup"><span data-stu-id="0412b-120">Each time the password is changed.</span></span>   |
| <span data-ttu-id="0412b-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0412b-121">Attribute-Id</span></span>      | <span data-ttu-id="0412b-122">1.2.840.113556.1.4.96</span><span class="sxs-lookup"><span data-stu-id="0412b-122">1.2.840.113556.1.4.96</span></span>                |
| <span data-ttu-id="0412b-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0412b-123">System-Id-Guid</span></span>    | <span data-ttu-id="0412b-124">bf967a0a-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0412b-124">bf967a0a-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="0412b-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0412b-125">Syntax</span></span>            | [<span data-ttu-id="0412b-126">**Interval**</span><span class="sxs-lookup"><span data-stu-id="0412b-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="0412b-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="0412b-127">Implementations</span></span>

-   [<span data-ttu-id="0412b-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0412b-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0412b-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0412b-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0412b-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="0412b-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0412b-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0412b-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0412b-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0412b-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0412b-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0412b-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0412b-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0412b-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0412b-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0412b-135">Windows 2000 Server</span></span>



| <span data-ttu-id="0412b-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="0412b-136">Entry</span></span> | <span data-ttu-id="0412b-137">Value</span><span class="sxs-lookup"><span data-stu-id="0412b-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0412b-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0412b-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0412b-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0412b-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0412b-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="0412b-140">System-Only</span></span>            | <span data-ttu-id="0412b-141">False</span><span class="sxs-lookup"><span data-stu-id="0412b-141">False</span></span>                             |
| <span data-ttu-id="0412b-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0412b-142">Is-Single-Valued</span></span>       | <span data-ttu-id="0412b-143">True</span><span class="sxs-lookup"><span data-stu-id="0412b-143">True</span></span>                              |
| <span data-ttu-id="0412b-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0412b-144">Is Indexed</span></span>             | <span data-ttu-id="0412b-145">False</span><span class="sxs-lookup"><span data-stu-id="0412b-145">False</span></span>                             |
| <span data-ttu-id="0412b-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0412b-146">In Global Catalog</span></span>      | <span data-ttu-id="0412b-147">False</span><span class="sxs-lookup"><span data-stu-id="0412b-147">False</span></span>                             |
| <span data-ttu-id="0412b-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0412b-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="0412b-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0412b-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0412b-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0412b-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0412b-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0412b-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0412b-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0412b-152">Search-Flags</span></span>           | <span data-ttu-id="0412b-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0412b-153">0x00000000</span></span>                        |
| <span data-ttu-id="0412b-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0412b-154">System-Flags</span></span>           | <span data-ttu-id="0412b-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0412b-155">0x00000010</span></span>                        |
| <span data-ttu-id="0412b-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0412b-156">Classes used in</span></span>        | [<span data-ttu-id="0412b-157">**User**</span><span class="sxs-lookup"><span data-stu-id="0412b-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0412b-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0412b-158">Windows Server 2003</span></span>



| <span data-ttu-id="0412b-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="0412b-159">Entry</span></span> | <span data-ttu-id="0412b-160">Value</span><span class="sxs-lookup"><span data-stu-id="0412b-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0412b-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0412b-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0412b-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0412b-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0412b-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="0412b-163">System-Only</span></span>            | <span data-ttu-id="0412b-164">False</span><span class="sxs-lookup"><span data-stu-id="0412b-164">False</span></span>                             |
| <span data-ttu-id="0412b-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0412b-165">Is-Single-Valued</span></span>       | <span data-ttu-id="0412b-166">True</span><span class="sxs-lookup"><span data-stu-id="0412b-166">True</span></span>                              |
| <span data-ttu-id="0412b-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0412b-167">Is Indexed</span></span>             | <span data-ttu-id="0412b-168">False</span><span class="sxs-lookup"><span data-stu-id="0412b-168">False</span></span>                             |
| <span data-ttu-id="0412b-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0412b-169">In Global Catalog</span></span>      | <span data-ttu-id="0412b-170">False</span><span class="sxs-lookup"><span data-stu-id="0412b-170">False</span></span>                             |
| <span data-ttu-id="0412b-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0412b-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="0412b-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0412b-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0412b-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0412b-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0412b-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0412b-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0412b-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0412b-175">Search-Flags</span></span>           | <span data-ttu-id="0412b-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0412b-176">0x00000000</span></span>                        |
| <span data-ttu-id="0412b-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0412b-177">System-Flags</span></span>           | <span data-ttu-id="0412b-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0412b-178">0x00000010</span></span>                        |
| <span data-ttu-id="0412b-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0412b-179">Classes used in</span></span>        | [<span data-ttu-id="0412b-180">**User**</span><span class="sxs-lookup"><span data-stu-id="0412b-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0412b-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="0412b-181">ADAM</span></span>



| <span data-ttu-id="0412b-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="0412b-182">Entry</span></span> | <span data-ttu-id="0412b-183">Value</span><span class="sxs-lookup"><span data-stu-id="0412b-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="0412b-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0412b-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="0412b-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0412b-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="0412b-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="0412b-186">System-Only</span></span>            | <span data-ttu-id="0412b-187">False</span><span class="sxs-lookup"><span data-stu-id="0412b-187">False</span></span>                                                             |
| <span data-ttu-id="0412b-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0412b-188">Is-Single-Valued</span></span>       | <span data-ttu-id="0412b-189">True</span><span class="sxs-lookup"><span data-stu-id="0412b-189">True</span></span>                                                              |
| <span data-ttu-id="0412b-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0412b-190">Is Indexed</span></span>             | <span data-ttu-id="0412b-191">False</span><span class="sxs-lookup"><span data-stu-id="0412b-191">False</span></span>                                                             |
| <span data-ttu-id="0412b-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0412b-192">In Global Catalog</span></span>      | <span data-ttu-id="0412b-193">False</span><span class="sxs-lookup"><span data-stu-id="0412b-193">False</span></span>                                                             |
| <span data-ttu-id="0412b-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0412b-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="0412b-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0412b-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="0412b-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0412b-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="0412b-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0412b-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="0412b-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0412b-198">Search-Flags</span></span>           | <span data-ttu-id="0412b-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0412b-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="0412b-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0412b-200">System-Flags</span></span>           | <span data-ttu-id="0412b-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0412b-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="0412b-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0412b-202">Classes used in</span></span>        | [<span data-ttu-id="0412b-203">**Objeto MS-DS-Bindable**</span><span class="sxs-lookup"><span data-stu-id="0412b-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0412b-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0412b-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0412b-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="0412b-205">Entry</span></span> | <span data-ttu-id="0412b-206">Value</span><span class="sxs-lookup"><span data-stu-id="0412b-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0412b-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0412b-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0412b-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0412b-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0412b-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="0412b-209">System-Only</span></span>            | <span data-ttu-id="0412b-210">False</span><span class="sxs-lookup"><span data-stu-id="0412b-210">False</span></span>                             |
| <span data-ttu-id="0412b-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0412b-211">Is-Single-Valued</span></span>       | <span data-ttu-id="0412b-212">True</span><span class="sxs-lookup"><span data-stu-id="0412b-212">True</span></span>                              |
| <span data-ttu-id="0412b-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0412b-213">Is Indexed</span></span>             | <span data-ttu-id="0412b-214">False</span><span class="sxs-lookup"><span data-stu-id="0412b-214">False</span></span>                             |
| <span data-ttu-id="0412b-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0412b-215">In Global Catalog</span></span>      | <span data-ttu-id="0412b-216">False</span><span class="sxs-lookup"><span data-stu-id="0412b-216">False</span></span>                             |
| <span data-ttu-id="0412b-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0412b-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="0412b-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0412b-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0412b-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0412b-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0412b-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0412b-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0412b-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0412b-221">Search-Flags</span></span>           | <span data-ttu-id="0412b-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0412b-222">0x00000000</span></span>                        |
| <span data-ttu-id="0412b-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0412b-223">System-Flags</span></span>           | <span data-ttu-id="0412b-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0412b-224">0x00000010</span></span>                        |
| <span data-ttu-id="0412b-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0412b-225">Classes used in</span></span>        | [<span data-ttu-id="0412b-226">**User**</span><span class="sxs-lookup"><span data-stu-id="0412b-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0412b-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0412b-227">Windows Server 2008</span></span>



| <span data-ttu-id="0412b-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="0412b-228">Entry</span></span> | <span data-ttu-id="0412b-229">Value</span><span class="sxs-lookup"><span data-stu-id="0412b-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0412b-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0412b-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0412b-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0412b-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0412b-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="0412b-232">System-Only</span></span>            | <span data-ttu-id="0412b-233">False</span><span class="sxs-lookup"><span data-stu-id="0412b-233">False</span></span>                             |
| <span data-ttu-id="0412b-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0412b-234">Is-Single-Valued</span></span>       | <span data-ttu-id="0412b-235">True</span><span class="sxs-lookup"><span data-stu-id="0412b-235">True</span></span>                              |
| <span data-ttu-id="0412b-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0412b-236">Is Indexed</span></span>             | <span data-ttu-id="0412b-237">False</span><span class="sxs-lookup"><span data-stu-id="0412b-237">False</span></span>                             |
| <span data-ttu-id="0412b-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0412b-238">In Global Catalog</span></span>      | <span data-ttu-id="0412b-239">False</span><span class="sxs-lookup"><span data-stu-id="0412b-239">False</span></span>                             |
| <span data-ttu-id="0412b-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0412b-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="0412b-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0412b-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0412b-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0412b-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0412b-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0412b-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0412b-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0412b-244">Search-Flags</span></span>           | <span data-ttu-id="0412b-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0412b-245">0x00000000</span></span>                        |
| <span data-ttu-id="0412b-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0412b-246">System-Flags</span></span>           | <span data-ttu-id="0412b-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0412b-247">0x00000010</span></span>                        |
| <span data-ttu-id="0412b-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0412b-248">Classes used in</span></span>        | [<span data-ttu-id="0412b-249">**User**</span><span class="sxs-lookup"><span data-stu-id="0412b-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0412b-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0412b-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0412b-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="0412b-251">Entry</span></span> | <span data-ttu-id="0412b-252">Value</span><span class="sxs-lookup"><span data-stu-id="0412b-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0412b-253">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0412b-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0412b-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0412b-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0412b-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="0412b-255">System-Only</span></span>            | <span data-ttu-id="0412b-256">False</span><span class="sxs-lookup"><span data-stu-id="0412b-256">False</span></span>                             |
| <span data-ttu-id="0412b-257">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0412b-257">Is-Single-Valued</span></span>       | <span data-ttu-id="0412b-258">True</span><span class="sxs-lookup"><span data-stu-id="0412b-258">True</span></span>                              |
| <span data-ttu-id="0412b-259">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0412b-259">Is Indexed</span></span>             | <span data-ttu-id="0412b-260">False</span><span class="sxs-lookup"><span data-stu-id="0412b-260">False</span></span>                             |
| <span data-ttu-id="0412b-261">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0412b-261">In Global Catalog</span></span>      | <span data-ttu-id="0412b-262">False</span><span class="sxs-lookup"><span data-stu-id="0412b-262">False</span></span>                             |
| <span data-ttu-id="0412b-263">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0412b-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="0412b-264">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0412b-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0412b-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0412b-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0412b-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0412b-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0412b-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0412b-267">Search-Flags</span></span>           | <span data-ttu-id="0412b-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0412b-268">0x00000000</span></span>                        |
| <span data-ttu-id="0412b-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0412b-269">System-Flags</span></span>           | <span data-ttu-id="0412b-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0412b-270">0x00000010</span></span>                        |
| <span data-ttu-id="0412b-271">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0412b-271">Classes used in</span></span>        | [<span data-ttu-id="0412b-272">**User**</span><span class="sxs-lookup"><span data-stu-id="0412b-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0412b-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0412b-273">Windows Server 2012</span></span>



| <span data-ttu-id="0412b-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="0412b-274">Entry</span></span> | <span data-ttu-id="0412b-275">Value</span><span class="sxs-lookup"><span data-stu-id="0412b-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0412b-276">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0412b-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0412b-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0412b-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0412b-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="0412b-278">System-Only</span></span>            | <span data-ttu-id="0412b-279">False</span><span class="sxs-lookup"><span data-stu-id="0412b-279">False</span></span>                             |
| <span data-ttu-id="0412b-280">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0412b-280">Is-Single-Valued</span></span>       | <span data-ttu-id="0412b-281">True</span><span class="sxs-lookup"><span data-stu-id="0412b-281">True</span></span>                              |
| <span data-ttu-id="0412b-282">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0412b-282">Is Indexed</span></span>             | <span data-ttu-id="0412b-283">False</span><span class="sxs-lookup"><span data-stu-id="0412b-283">False</span></span>                             |
| <span data-ttu-id="0412b-284">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0412b-284">In Global Catalog</span></span>      | <span data-ttu-id="0412b-285">False</span><span class="sxs-lookup"><span data-stu-id="0412b-285">False</span></span>                             |
| <span data-ttu-id="0412b-286">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0412b-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="0412b-287">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0412b-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0412b-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0412b-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0412b-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0412b-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0412b-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0412b-290">Search-Flags</span></span>           | <span data-ttu-id="0412b-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0412b-291">0x00000000</span></span>                        |
| <span data-ttu-id="0412b-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0412b-292">System-Flags</span></span>           | <span data-ttu-id="0412b-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0412b-293">0x00000010</span></span>                        |
| <span data-ttu-id="0412b-294">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0412b-294">Classes used in</span></span>        | [<span data-ttu-id="0412b-295">**User**</span><span class="sxs-lookup"><span data-stu-id="0412b-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="0412b-296">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0412b-296">Remarks</span></span>

<span data-ttu-id="0412b-297">La parte alta de este entero grande corresponde al miembro **dwHighDateTime** de la estructura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) y la parte baja corresponde al miembro **dwLowDateTime** de la estructura **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="0412b-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

## <a name="see-also"></a><span data-ttu-id="0412b-298">Vea también</span><span class="sxs-lookup"><span data-stu-id="0412b-298">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0412b-299">**Control de cuentas de usuario**</span><span class="sxs-lookup"><span data-stu-id="0412b-299">**User-Account-Control**</span></span>](a-useraccountcontrol.md)
</dt> </dl>

 

