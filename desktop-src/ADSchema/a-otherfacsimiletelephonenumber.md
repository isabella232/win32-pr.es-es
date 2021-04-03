---
title: Teléfono-fax-otro atributo
description: Una lista de números de facsímil alternativos.
ms.assetid: b5e4ef38-ce91-4943-bad5-c299f83387d3
ms.tgt_platform: multiple
keywords:
- Teléfono-fax-otro atributo esquema de AD
- otherFacsimileTelephoneNumber esquema de AD de atributos
topic_type:
- apiref
api_name:
- Phone-Fax-Other
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12e765ce2c3f9b74b894714b99ae87deadd760d6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906139"
---
# <a name="phone-fax-other-attribute"></a><span data-ttu-id="df91d-105">Teléfono-fax-otro atributo</span><span class="sxs-lookup"><span data-stu-id="df91d-105">Phone-Fax-Other attribute</span></span>

<span data-ttu-id="df91d-106">Una lista de números de facsímil alternativos.</span><span class="sxs-lookup"><span data-stu-id="df91d-106">A list of alternate facsimile numbers.</span></span>



| <span data-ttu-id="df91d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="df91d-107">Entry</span></span> | <span data-ttu-id="df91d-108">Value</span><span class="sxs-lookup"><span data-stu-id="df91d-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="df91d-109">CN</span><span class="sxs-lookup"><span data-stu-id="df91d-109">CN</span></span>                | <span data-ttu-id="df91d-110">Teléfono-fax-otro</span><span class="sxs-lookup"><span data-stu-id="df91d-110">Phone-Fax-Other</span></span>                                                                  |
| <span data-ttu-id="df91d-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="df91d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="df91d-112">otherFacsimileTelephoneNumber</span><span class="sxs-lookup"><span data-stu-id="df91d-112">otherFacsimileTelephoneNumber</span></span>                                                    |
| <span data-ttu-id="df91d-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="df91d-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="df91d-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="df91d-114">Update Privilege</span></span>  | <span data-ttu-id="df91d-115">Administrador de dominio o propietario de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="df91d-115">Domain administrator or account owner.</span></span>                                           |
| <span data-ttu-id="df91d-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="df91d-116">Update Frequency</span></span>  | <span data-ttu-id="df91d-117">Cuando se crea el registro del usuario y cada vez que es necesario cambiar el número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="df91d-117">When the user's record is created and whenever the phone number needs to change.</span></span> |
| <span data-ttu-id="df91d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="df91d-118">Attribute-Id</span></span>      | <span data-ttu-id="df91d-119">1.2.840.113556.1.4.646</span><span class="sxs-lookup"><span data-stu-id="df91d-119">1.2.840.113556.1.4.646</span></span>                                                           |
| <span data-ttu-id="df91d-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="df91d-120">System-Id-Guid</span></span>    | <span data-ttu-id="df91d-121">0296c11d-40da-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="df91d-121">0296c11d-40da-11d1-a9c0-0000f80367c1</span></span>                                             |
| <span data-ttu-id="df91d-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df91d-122">Syntax</span></span>            | [<span data-ttu-id="df91d-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="df91d-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="df91d-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="df91d-124">Implementations</span></span>

-   [<span data-ttu-id="df91d-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="df91d-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="df91d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="df91d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="df91d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="df91d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="df91d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="df91d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="df91d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="df91d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="df91d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="df91d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="df91d-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="df91d-131">Windows 2000 Server</span></span>



| <span data-ttu-id="df91d-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="df91d-132">Entry</span></span> | <span data-ttu-id="df91d-133">Value</span><span class="sxs-lookup"><span data-stu-id="df91d-133">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="df91d-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="df91d-134">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="df91d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df91d-135">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="df91d-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="df91d-136">System-Only</span></span>            | <span data-ttu-id="df91d-137">False</span><span class="sxs-lookup"><span data-stu-id="df91d-137">False</span></span>                                                              |
| <span data-ttu-id="df91d-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="df91d-138">Is-Single-Valued</span></span>       | <span data-ttu-id="df91d-139">False</span><span class="sxs-lookup"><span data-stu-id="df91d-139">False</span></span>                                                              |
| <span data-ttu-id="df91d-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="df91d-140">Is Indexed</span></span>             | <span data-ttu-id="df91d-141">False</span><span class="sxs-lookup"><span data-stu-id="df91d-141">False</span></span>                                                              |
| <span data-ttu-id="df91d-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="df91d-142">In Global Catalog</span></span>      | <span data-ttu-id="df91d-143">False</span><span class="sxs-lookup"><span data-stu-id="df91d-143">False</span></span>                                                              |
| <span data-ttu-id="df91d-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="df91d-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="df91d-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="df91d-145">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="df91d-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df91d-146">Range-Lower</span></span>            | <span data-ttu-id="df91d-147">1</span><span class="sxs-lookup"><span data-stu-id="df91d-147">1</span></span>                                                                  |
| <span data-ttu-id="df91d-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df91d-148">Range-Upper</span></span>            | <span data-ttu-id="df91d-149">64</span><span class="sxs-lookup"><span data-stu-id="df91d-149">64</span></span>                                                                 |
| <span data-ttu-id="df91d-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df91d-150">Search-Flags</span></span>           | <span data-ttu-id="df91d-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df91d-151">0x00000000</span></span>                                                         |
| <span data-ttu-id="df91d-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df91d-152">System-Flags</span></span>           | <span data-ttu-id="df91d-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df91d-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="df91d-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="df91d-154">Classes used in</span></span>        | [<span data-ttu-id="df91d-155">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="df91d-155">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="df91d-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="df91d-156">Windows Server 2003</span></span>



| <span data-ttu-id="df91d-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="df91d-157">Entry</span></span> | <span data-ttu-id="df91d-158">Value</span><span class="sxs-lookup"><span data-stu-id="df91d-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="df91d-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="df91d-159">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="df91d-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df91d-160">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="df91d-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="df91d-161">System-Only</span></span>            | <span data-ttu-id="df91d-162">False</span><span class="sxs-lookup"><span data-stu-id="df91d-162">False</span></span>                                                              |
| <span data-ttu-id="df91d-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="df91d-163">Is-Single-Valued</span></span>       | <span data-ttu-id="df91d-164">False</span><span class="sxs-lookup"><span data-stu-id="df91d-164">False</span></span>                                                              |
| <span data-ttu-id="df91d-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="df91d-165">Is Indexed</span></span>             | <span data-ttu-id="df91d-166">False</span><span class="sxs-lookup"><span data-stu-id="df91d-166">False</span></span>                                                              |
| <span data-ttu-id="df91d-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="df91d-167">In Global Catalog</span></span>      | <span data-ttu-id="df91d-168">False</span><span class="sxs-lookup"><span data-stu-id="df91d-168">False</span></span>                                                              |
| <span data-ttu-id="df91d-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="df91d-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="df91d-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="df91d-170">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="df91d-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df91d-171">Range-Lower</span></span>            | <span data-ttu-id="df91d-172">1</span><span class="sxs-lookup"><span data-stu-id="df91d-172">1</span></span>                                                                  |
| <span data-ttu-id="df91d-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df91d-173">Range-Upper</span></span>            | <span data-ttu-id="df91d-174">64</span><span class="sxs-lookup"><span data-stu-id="df91d-174">64</span></span>                                                                 |
| <span data-ttu-id="df91d-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df91d-175">Search-Flags</span></span>           | <span data-ttu-id="df91d-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df91d-176">0x00000000</span></span>                                                         |
| <span data-ttu-id="df91d-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df91d-177">System-Flags</span></span>           | <span data-ttu-id="df91d-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df91d-178">0x00000010</span></span>                                                         |
| <span data-ttu-id="df91d-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="df91d-179">Classes used in</span></span>        | [<span data-ttu-id="df91d-180">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="df91d-180">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="df91d-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="df91d-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="df91d-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="df91d-182">Entry</span></span> | <span data-ttu-id="df91d-183">Value</span><span class="sxs-lookup"><span data-stu-id="df91d-183">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="df91d-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="df91d-184">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="df91d-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df91d-185">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="df91d-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="df91d-186">System-Only</span></span>            | <span data-ttu-id="df91d-187">False</span><span class="sxs-lookup"><span data-stu-id="df91d-187">False</span></span>                                                              |
| <span data-ttu-id="df91d-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="df91d-188">Is-Single-Valued</span></span>       | <span data-ttu-id="df91d-189">False</span><span class="sxs-lookup"><span data-stu-id="df91d-189">False</span></span>                                                              |
| <span data-ttu-id="df91d-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="df91d-190">Is Indexed</span></span>             | <span data-ttu-id="df91d-191">False</span><span class="sxs-lookup"><span data-stu-id="df91d-191">False</span></span>                                                              |
| <span data-ttu-id="df91d-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="df91d-192">In Global Catalog</span></span>      | <span data-ttu-id="df91d-193">False</span><span class="sxs-lookup"><span data-stu-id="df91d-193">False</span></span>                                                              |
| <span data-ttu-id="df91d-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="df91d-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="df91d-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="df91d-195">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="df91d-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df91d-196">Range-Lower</span></span>            | <span data-ttu-id="df91d-197">1</span><span class="sxs-lookup"><span data-stu-id="df91d-197">1</span></span>                                                                  |
| <span data-ttu-id="df91d-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df91d-198">Range-Upper</span></span>            | <span data-ttu-id="df91d-199">64</span><span class="sxs-lookup"><span data-stu-id="df91d-199">64</span></span>                                                                 |
| <span data-ttu-id="df91d-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df91d-200">Search-Flags</span></span>           | <span data-ttu-id="df91d-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df91d-201">0x00000000</span></span>                                                         |
| <span data-ttu-id="df91d-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df91d-202">System-Flags</span></span>           | <span data-ttu-id="df91d-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df91d-203">0x00000010</span></span>                                                         |
| <span data-ttu-id="df91d-204">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="df91d-204">Classes used in</span></span>        | [<span data-ttu-id="df91d-205">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="df91d-205">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="df91d-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df91d-206">Windows Server 2008</span></span>



| <span data-ttu-id="df91d-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="df91d-207">Entry</span></span> | <span data-ttu-id="df91d-208">Value</span><span class="sxs-lookup"><span data-stu-id="df91d-208">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="df91d-209">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="df91d-209">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="df91d-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df91d-210">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="df91d-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="df91d-211">System-Only</span></span>            | <span data-ttu-id="df91d-212">False</span><span class="sxs-lookup"><span data-stu-id="df91d-212">False</span></span>                                                              |
| <span data-ttu-id="df91d-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="df91d-213">Is-Single-Valued</span></span>       | <span data-ttu-id="df91d-214">False</span><span class="sxs-lookup"><span data-stu-id="df91d-214">False</span></span>                                                              |
| <span data-ttu-id="df91d-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="df91d-215">Is Indexed</span></span>             | <span data-ttu-id="df91d-216">False</span><span class="sxs-lookup"><span data-stu-id="df91d-216">False</span></span>                                                              |
| <span data-ttu-id="df91d-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="df91d-217">In Global Catalog</span></span>      | <span data-ttu-id="df91d-218">False</span><span class="sxs-lookup"><span data-stu-id="df91d-218">False</span></span>                                                              |
| <span data-ttu-id="df91d-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="df91d-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="df91d-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="df91d-220">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="df91d-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df91d-221">Range-Lower</span></span>            | <span data-ttu-id="df91d-222">1</span><span class="sxs-lookup"><span data-stu-id="df91d-222">1</span></span>                                                                  |
| <span data-ttu-id="df91d-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df91d-223">Range-Upper</span></span>            | <span data-ttu-id="df91d-224">64</span><span class="sxs-lookup"><span data-stu-id="df91d-224">64</span></span>                                                                 |
| <span data-ttu-id="df91d-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df91d-225">Search-Flags</span></span>           | <span data-ttu-id="df91d-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df91d-226">0x00000000</span></span>                                                         |
| <span data-ttu-id="df91d-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df91d-227">System-Flags</span></span>           | <span data-ttu-id="df91d-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df91d-228">0x00000010</span></span>                                                         |
| <span data-ttu-id="df91d-229">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="df91d-229">Classes used in</span></span>        | [<span data-ttu-id="df91d-230">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="df91d-230">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="df91d-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="df91d-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="df91d-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="df91d-232">Entry</span></span> | <span data-ttu-id="df91d-233">Value</span><span class="sxs-lookup"><span data-stu-id="df91d-233">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="df91d-234">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="df91d-234">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="df91d-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df91d-235">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="df91d-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="df91d-236">System-Only</span></span>            | <span data-ttu-id="df91d-237">False</span><span class="sxs-lookup"><span data-stu-id="df91d-237">False</span></span>                                                              |
| <span data-ttu-id="df91d-238">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="df91d-238">Is-Single-Valued</span></span>       | <span data-ttu-id="df91d-239">False</span><span class="sxs-lookup"><span data-stu-id="df91d-239">False</span></span>                                                              |
| <span data-ttu-id="df91d-240">Está indexado</span><span class="sxs-lookup"><span data-stu-id="df91d-240">Is Indexed</span></span>             | <span data-ttu-id="df91d-241">False</span><span class="sxs-lookup"><span data-stu-id="df91d-241">False</span></span>                                                              |
| <span data-ttu-id="df91d-242">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="df91d-242">In Global Catalog</span></span>      | <span data-ttu-id="df91d-243">False</span><span class="sxs-lookup"><span data-stu-id="df91d-243">False</span></span>                                                              |
| <span data-ttu-id="df91d-244">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="df91d-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="df91d-245">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="df91d-245">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="df91d-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df91d-246">Range-Lower</span></span>            | <span data-ttu-id="df91d-247">1</span><span class="sxs-lookup"><span data-stu-id="df91d-247">1</span></span>                                                                  |
| <span data-ttu-id="df91d-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df91d-248">Range-Upper</span></span>            | <span data-ttu-id="df91d-249">64</span><span class="sxs-lookup"><span data-stu-id="df91d-249">64</span></span>                                                                 |
| <span data-ttu-id="df91d-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df91d-250">Search-Flags</span></span>           | <span data-ttu-id="df91d-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df91d-251">0x00000000</span></span>                                                         |
| <span data-ttu-id="df91d-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df91d-252">System-Flags</span></span>           | <span data-ttu-id="df91d-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df91d-253">0x00000010</span></span>                                                         |
| <span data-ttu-id="df91d-254">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="df91d-254">Classes used in</span></span>        | [<span data-ttu-id="df91d-255">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="df91d-255">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="df91d-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="df91d-256">Windows Server 2012</span></span>



| <span data-ttu-id="df91d-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="df91d-257">Entry</span></span> | <span data-ttu-id="df91d-258">Value</span><span class="sxs-lookup"><span data-stu-id="df91d-258">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="df91d-259">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="df91d-259">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="df91d-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df91d-260">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="df91d-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="df91d-261">System-Only</span></span>            | <span data-ttu-id="df91d-262">False</span><span class="sxs-lookup"><span data-stu-id="df91d-262">False</span></span>                                                              |
| <span data-ttu-id="df91d-263">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="df91d-263">Is-Single-Valued</span></span>       | <span data-ttu-id="df91d-264">False</span><span class="sxs-lookup"><span data-stu-id="df91d-264">False</span></span>                                                              |
| <span data-ttu-id="df91d-265">Está indexado</span><span class="sxs-lookup"><span data-stu-id="df91d-265">Is Indexed</span></span>             | <span data-ttu-id="df91d-266">False</span><span class="sxs-lookup"><span data-stu-id="df91d-266">False</span></span>                                                              |
| <span data-ttu-id="df91d-267">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="df91d-267">In Global Catalog</span></span>      | <span data-ttu-id="df91d-268">False</span><span class="sxs-lookup"><span data-stu-id="df91d-268">False</span></span>                                                              |
| <span data-ttu-id="df91d-269">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="df91d-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="df91d-270">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="df91d-270">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="df91d-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df91d-271">Range-Lower</span></span>            | <span data-ttu-id="df91d-272">1</span><span class="sxs-lookup"><span data-stu-id="df91d-272">1</span></span>                                                                  |
| <span data-ttu-id="df91d-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df91d-273">Range-Upper</span></span>            | <span data-ttu-id="df91d-274">64</span><span class="sxs-lookup"><span data-stu-id="df91d-274">64</span></span>                                                                 |
| <span data-ttu-id="df91d-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df91d-275">Search-Flags</span></span>           | <span data-ttu-id="df91d-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df91d-276">0x00000000</span></span>                                                         |
| <span data-ttu-id="df91d-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df91d-277">System-Flags</span></span>           | <span data-ttu-id="df91d-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df91d-278">0x00000010</span></span>                                                         |
| <span data-ttu-id="df91d-279">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="df91d-279">Classes used in</span></span>        | [<span data-ttu-id="df91d-280">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="df91d-280">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





