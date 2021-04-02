---
title: Atributo MS-DS-Creator-SID
description: IDENTIFICADOR de seguridad del creador del objeto que contiene este atributo.
ms.assetid: 5e643c56-bfe9-4489-89a9-5ce56f90f288
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-Creator-SID
- Esquema de AD del atributo mS-DS-CreatorSID
topic_type:
- apiref
api_name:
- MS-DS-Creator-SID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b5b5635773271c4864ac2c8ec1898edcc9a9f9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997294"
---
# <a name="ms-ds-creator-sid-attribute"></a><span data-ttu-id="d5eaa-105">Atributo MS-DS-Creator-SID</span><span class="sxs-lookup"><span data-stu-id="d5eaa-105">MS-DS-Creator-SID attribute</span></span>

<span data-ttu-id="d5eaa-106">IDENTIFICADOR de seguridad del creador del objeto que contiene este atributo.</span><span class="sxs-lookup"><span data-stu-id="d5eaa-106">The security ID of the creator of the object that contains this attribute.</span></span>



| <span data-ttu-id="d5eaa-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5eaa-107">Entry</span></span> | <span data-ttu-id="d5eaa-108">Value</span><span class="sxs-lookup"><span data-stu-id="d5eaa-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d5eaa-109">CN</span><span class="sxs-lookup"><span data-stu-id="d5eaa-109">CN</span></span>                | <span data-ttu-id="d5eaa-110">MS-DS-Creator-SID</span><span class="sxs-lookup"><span data-stu-id="d5eaa-110">MS-DS-Creator-SID</span></span>                    |
| <span data-ttu-id="d5eaa-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="d5eaa-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d5eaa-112">mS-DS-CreatorSID</span><span class="sxs-lookup"><span data-stu-id="d5eaa-112">mS-DS-CreatorSID</span></span>                     |
| <span data-ttu-id="d5eaa-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="d5eaa-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="d5eaa-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="d5eaa-114">Update Privilege</span></span>  | <span data-ttu-id="d5eaa-115">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="d5eaa-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="d5eaa-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="d5eaa-116">Update Frequency</span></span>  | <span data-ttu-id="d5eaa-117">Cada vez que se crea un nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="d5eaa-117">Whenever a new object is created.</span></span>    |
| <span data-ttu-id="d5eaa-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d5eaa-118">Attribute-Id</span></span>      | <span data-ttu-id="d5eaa-119">1.2.840.113556.1.4.1410</span><span class="sxs-lookup"><span data-stu-id="d5eaa-119">1.2.840.113556.1.4.1410</span></span>              |
| <span data-ttu-id="d5eaa-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d5eaa-120">System-Id-Guid</span></span>    | <span data-ttu-id="d5eaa-121">c5e60132-1480-11d3-91c1-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="d5eaa-121">c5e60132-1480-11d3-91c1-0000f87a57d4</span></span> |
| <span data-ttu-id="d5eaa-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5eaa-122">Syntax</span></span>            | [<span data-ttu-id="d5eaa-123">**Cadena (SID)**</span><span class="sxs-lookup"><span data-stu-id="d5eaa-123">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="d5eaa-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="d5eaa-124">Implementations</span></span>

-   [<span data-ttu-id="d5eaa-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d5eaa-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d5eaa-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d5eaa-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d5eaa-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d5eaa-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d5eaa-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d5eaa-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d5eaa-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d5eaa-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d5eaa-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d5eaa-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d5eaa-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d5eaa-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d5eaa-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5eaa-132">Entry</span></span> | <span data-ttu-id="d5eaa-133">Value</span><span class="sxs-lookup"><span data-stu-id="d5eaa-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d5eaa-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5eaa-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d5eaa-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5eaa-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d5eaa-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5eaa-136">System-Only</span></span>            | <span data-ttu-id="d5eaa-137">True</span><span class="sxs-lookup"><span data-stu-id="d5eaa-137">True</span></span>                              |
| <span data-ttu-id="d5eaa-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5eaa-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d5eaa-139">True</span><span class="sxs-lookup"><span data-stu-id="d5eaa-139">True</span></span>                              |
| <span data-ttu-id="d5eaa-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5eaa-140">Is Indexed</span></span>             | <span data-ttu-id="d5eaa-141">True</span><span class="sxs-lookup"><span data-stu-id="d5eaa-141">True</span></span>                              |
| <span data-ttu-id="d5eaa-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5eaa-142">In Global Catalog</span></span>      | <span data-ttu-id="d5eaa-143">False</span><span class="sxs-lookup"><span data-stu-id="d5eaa-143">False</span></span>                             |
| <span data-ttu-id="d5eaa-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5eaa-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5eaa-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5eaa-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d5eaa-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5eaa-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d5eaa-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5eaa-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d5eaa-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5eaa-148">Search-Flags</span></span>           | <span data-ttu-id="d5eaa-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d5eaa-149">0x00000001</span></span>                        |
| <span data-ttu-id="d5eaa-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5eaa-150">System-Flags</span></span>           | <span data-ttu-id="d5eaa-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5eaa-151">0x00000010</span></span>                        |
| <span data-ttu-id="d5eaa-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5eaa-152">Classes used in</span></span>        | [<span data-ttu-id="d5eaa-153">**User**</span><span class="sxs-lookup"><span data-stu-id="d5eaa-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d5eaa-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d5eaa-154">Windows Server 2003</span></span>



| <span data-ttu-id="d5eaa-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5eaa-155">Entry</span></span> | <span data-ttu-id="d5eaa-156">Value</span><span class="sxs-lookup"><span data-stu-id="d5eaa-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d5eaa-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5eaa-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d5eaa-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5eaa-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d5eaa-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5eaa-159">System-Only</span></span>            | <span data-ttu-id="d5eaa-160">True</span><span class="sxs-lookup"><span data-stu-id="d5eaa-160">True</span></span>                              |
| <span data-ttu-id="d5eaa-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5eaa-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d5eaa-162">True</span><span class="sxs-lookup"><span data-stu-id="d5eaa-162">True</span></span>                              |
| <span data-ttu-id="d5eaa-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5eaa-163">Is Indexed</span></span>             | <span data-ttu-id="d5eaa-164">True</span><span class="sxs-lookup"><span data-stu-id="d5eaa-164">True</span></span>                              |
| <span data-ttu-id="d5eaa-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5eaa-165">In Global Catalog</span></span>      | <span data-ttu-id="d5eaa-166">False</span><span class="sxs-lookup"><span data-stu-id="d5eaa-166">False</span></span>                             |
| <span data-ttu-id="d5eaa-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5eaa-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5eaa-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5eaa-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d5eaa-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5eaa-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d5eaa-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5eaa-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d5eaa-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5eaa-171">Search-Flags</span></span>           | <span data-ttu-id="d5eaa-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d5eaa-172">0x00000001</span></span>                        |
| <span data-ttu-id="d5eaa-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5eaa-173">System-Flags</span></span>           | <span data-ttu-id="d5eaa-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5eaa-174">0x00000010</span></span>                        |
| <span data-ttu-id="d5eaa-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5eaa-175">Classes used in</span></span>        | [<span data-ttu-id="d5eaa-176">**User**</span><span class="sxs-lookup"><span data-stu-id="d5eaa-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d5eaa-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d5eaa-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d5eaa-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5eaa-178">Entry</span></span> | <span data-ttu-id="d5eaa-179">Value</span><span class="sxs-lookup"><span data-stu-id="d5eaa-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d5eaa-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5eaa-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d5eaa-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5eaa-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d5eaa-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5eaa-182">System-Only</span></span>            | <span data-ttu-id="d5eaa-183">True</span><span class="sxs-lookup"><span data-stu-id="d5eaa-183">True</span></span>                              |
| <span data-ttu-id="d5eaa-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5eaa-184">Is-Single-Valued</span></span>       | <span data-ttu-id="d5eaa-185">True</span><span class="sxs-lookup"><span data-stu-id="d5eaa-185">True</span></span>                              |
| <span data-ttu-id="d5eaa-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5eaa-186">Is Indexed</span></span>             | <span data-ttu-id="d5eaa-187">True</span><span class="sxs-lookup"><span data-stu-id="d5eaa-187">True</span></span>                              |
| <span data-ttu-id="d5eaa-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5eaa-188">In Global Catalog</span></span>      | <span data-ttu-id="d5eaa-189">False</span><span class="sxs-lookup"><span data-stu-id="d5eaa-189">False</span></span>                             |
| <span data-ttu-id="d5eaa-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5eaa-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5eaa-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5eaa-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d5eaa-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5eaa-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d5eaa-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5eaa-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d5eaa-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5eaa-194">Search-Flags</span></span>           | <span data-ttu-id="d5eaa-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d5eaa-195">0x00000001</span></span>                        |
| <span data-ttu-id="d5eaa-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5eaa-196">System-Flags</span></span>           | <span data-ttu-id="d5eaa-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5eaa-197">0x00000010</span></span>                        |
| <span data-ttu-id="d5eaa-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5eaa-198">Classes used in</span></span>        | [<span data-ttu-id="d5eaa-199">**User**</span><span class="sxs-lookup"><span data-stu-id="d5eaa-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d5eaa-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5eaa-200">Windows Server 2008</span></span>



| <span data-ttu-id="d5eaa-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5eaa-201">Entry</span></span> | <span data-ttu-id="d5eaa-202">Value</span><span class="sxs-lookup"><span data-stu-id="d5eaa-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d5eaa-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5eaa-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d5eaa-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5eaa-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d5eaa-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5eaa-205">System-Only</span></span>            | <span data-ttu-id="d5eaa-206">True</span><span class="sxs-lookup"><span data-stu-id="d5eaa-206">True</span></span>                              |
| <span data-ttu-id="d5eaa-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5eaa-207">Is-Single-Valued</span></span>       | <span data-ttu-id="d5eaa-208">True</span><span class="sxs-lookup"><span data-stu-id="d5eaa-208">True</span></span>                              |
| <span data-ttu-id="d5eaa-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5eaa-209">Is Indexed</span></span>             | <span data-ttu-id="d5eaa-210">True</span><span class="sxs-lookup"><span data-stu-id="d5eaa-210">True</span></span>                              |
| <span data-ttu-id="d5eaa-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5eaa-211">In Global Catalog</span></span>      | <span data-ttu-id="d5eaa-212">False</span><span class="sxs-lookup"><span data-stu-id="d5eaa-212">False</span></span>                             |
| <span data-ttu-id="d5eaa-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5eaa-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5eaa-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5eaa-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d5eaa-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5eaa-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d5eaa-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5eaa-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d5eaa-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5eaa-217">Search-Flags</span></span>           | <span data-ttu-id="d5eaa-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d5eaa-218">0x00000001</span></span>                        |
| <span data-ttu-id="d5eaa-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5eaa-219">System-Flags</span></span>           | <span data-ttu-id="d5eaa-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5eaa-220">0x00000010</span></span>                        |
| <span data-ttu-id="d5eaa-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5eaa-221">Classes used in</span></span>        | [<span data-ttu-id="d5eaa-222">**User**</span><span class="sxs-lookup"><span data-stu-id="d5eaa-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d5eaa-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d5eaa-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d5eaa-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5eaa-224">Entry</span></span> | <span data-ttu-id="d5eaa-225">Value</span><span class="sxs-lookup"><span data-stu-id="d5eaa-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d5eaa-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5eaa-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d5eaa-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5eaa-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d5eaa-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5eaa-228">System-Only</span></span>            | <span data-ttu-id="d5eaa-229">True</span><span class="sxs-lookup"><span data-stu-id="d5eaa-229">True</span></span>                              |
| <span data-ttu-id="d5eaa-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5eaa-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d5eaa-231">True</span><span class="sxs-lookup"><span data-stu-id="d5eaa-231">True</span></span>                              |
| <span data-ttu-id="d5eaa-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5eaa-232">Is Indexed</span></span>             | <span data-ttu-id="d5eaa-233">True</span><span class="sxs-lookup"><span data-stu-id="d5eaa-233">True</span></span>                              |
| <span data-ttu-id="d5eaa-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5eaa-234">In Global Catalog</span></span>      | <span data-ttu-id="d5eaa-235">False</span><span class="sxs-lookup"><span data-stu-id="d5eaa-235">False</span></span>                             |
| <span data-ttu-id="d5eaa-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5eaa-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5eaa-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5eaa-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d5eaa-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5eaa-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d5eaa-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5eaa-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d5eaa-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5eaa-240">Search-Flags</span></span>           | <span data-ttu-id="d5eaa-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d5eaa-241">0x00000001</span></span>                        |
| <span data-ttu-id="d5eaa-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5eaa-242">System-Flags</span></span>           | <span data-ttu-id="d5eaa-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5eaa-243">0x00000010</span></span>                        |
| <span data-ttu-id="d5eaa-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5eaa-244">Classes used in</span></span>        | [<span data-ttu-id="d5eaa-245">**User**</span><span class="sxs-lookup"><span data-stu-id="d5eaa-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d5eaa-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d5eaa-246">Windows Server 2012</span></span>



| <span data-ttu-id="d5eaa-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5eaa-247">Entry</span></span> | <span data-ttu-id="d5eaa-248">Value</span><span class="sxs-lookup"><span data-stu-id="d5eaa-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d5eaa-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5eaa-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d5eaa-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5eaa-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d5eaa-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5eaa-251">System-Only</span></span>            | <span data-ttu-id="d5eaa-252">True</span><span class="sxs-lookup"><span data-stu-id="d5eaa-252">True</span></span>                              |
| <span data-ttu-id="d5eaa-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5eaa-253">Is-Single-Valued</span></span>       | <span data-ttu-id="d5eaa-254">True</span><span class="sxs-lookup"><span data-stu-id="d5eaa-254">True</span></span>                              |
| <span data-ttu-id="d5eaa-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5eaa-255">Is Indexed</span></span>             | <span data-ttu-id="d5eaa-256">True</span><span class="sxs-lookup"><span data-stu-id="d5eaa-256">True</span></span>                              |
| <span data-ttu-id="d5eaa-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5eaa-257">In Global Catalog</span></span>      | <span data-ttu-id="d5eaa-258">False</span><span class="sxs-lookup"><span data-stu-id="d5eaa-258">False</span></span>                             |
| <span data-ttu-id="d5eaa-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5eaa-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5eaa-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5eaa-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d5eaa-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5eaa-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d5eaa-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5eaa-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d5eaa-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5eaa-263">Search-Flags</span></span>           | <span data-ttu-id="d5eaa-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d5eaa-264">0x00000001</span></span>                        |
| <span data-ttu-id="d5eaa-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5eaa-265">System-Flags</span></span>           | <span data-ttu-id="d5eaa-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5eaa-266">0x00000010</span></span>                        |
| <span data-ttu-id="d5eaa-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5eaa-267">Classes used in</span></span>        | [<span data-ttu-id="d5eaa-268">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="d5eaa-268">**User**</span></span>](c-user.md)<br/> |



 

 





