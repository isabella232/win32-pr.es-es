---
title: Teléfono-IP-otro atributo
description: La lista de direcciones TCP/IP alternativas para el teléfono. Utilizado por telefonía.
ms.assetid: 3689c561-6dc1-4d73-adec-01c4ebdb5e47
ms.tgt_platform: multiple
keywords:
- Teléfono-IP-otro esquema de AD de atributos
- otherIpPhone esquema de AD de atributos
topic_type:
- apiref
api_name:
- Phone-Ip-Other
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7955b4fb80d46c19e5536517b53eb419e6de9ec6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659007"
---
# <a name="phone-ip-other-attribute"></a><span data-ttu-id="2a7cc-106">Teléfono-IP-otro atributo</span><span class="sxs-lookup"><span data-stu-id="2a7cc-106">Phone-Ip-Other attribute</span></span>

<span data-ttu-id="2a7cc-107">La lista de direcciones TCP/IP alternativas para el teléfono.</span><span class="sxs-lookup"><span data-stu-id="2a7cc-107">The list of alternate TCP/IP addresses for the phone.</span></span> <span data-ttu-id="2a7cc-108">Utilizado por telefonía.</span><span class="sxs-lookup"><span data-stu-id="2a7cc-108">Used by Telephony.</span></span>



| <span data-ttu-id="2a7cc-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="2a7cc-109">Entry</span></span> | <span data-ttu-id="2a7cc-110">Value</span><span class="sxs-lookup"><span data-stu-id="2a7cc-110">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2a7cc-111">CN</span><span class="sxs-lookup"><span data-stu-id="2a7cc-111">CN</span></span>                | <span data-ttu-id="2a7cc-112">Teléfono-IP-otro</span><span class="sxs-lookup"><span data-stu-id="2a7cc-112">Phone-Ip-Other</span></span>                                                                   |
| <span data-ttu-id="2a7cc-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="2a7cc-113">Ldap-Display-Name</span></span> | <span data-ttu-id="2a7cc-114">otherIpPhone</span><span class="sxs-lookup"><span data-stu-id="2a7cc-114">otherIpPhone</span></span>                                                                     |
| <span data-ttu-id="2a7cc-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="2a7cc-115">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="2a7cc-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="2a7cc-116">Update Privilege</span></span>  | <span data-ttu-id="2a7cc-117">Administrador de dominio o propietario de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="2a7cc-117">Domain administrator or account owner.</span></span>                                           |
| <span data-ttu-id="2a7cc-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="2a7cc-118">Update Frequency</span></span>  | <span data-ttu-id="2a7cc-119">Cuando se crea el registro del usuario y cada vez que es necesario cambiar el número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="2a7cc-119">When the user's record is created and whenever the phone number needs to change.</span></span> |
| <span data-ttu-id="2a7cc-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2a7cc-120">Attribute-Id</span></span>      | <span data-ttu-id="2a7cc-121">1.2.840.113556.1.4.722</span><span class="sxs-lookup"><span data-stu-id="2a7cc-121">1.2.840.113556.1.4.722</span></span>                                                           |
| <span data-ttu-id="2a7cc-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2a7cc-122">System-Id-Guid</span></span>    | <span data-ttu-id="2a7cc-123">4d146e4b-48d4-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="2a7cc-123">4d146e4b-48d4-11d1-a9c3-0000f80367c1</span></span>                                             |
| <span data-ttu-id="2a7cc-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a7cc-124">Syntax</span></span>            | [<span data-ttu-id="2a7cc-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="2a7cc-125">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="2a7cc-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="2a7cc-126">Implementations</span></span>

-   [<span data-ttu-id="2a7cc-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2a7cc-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2a7cc-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2a7cc-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2a7cc-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2a7cc-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2a7cc-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2a7cc-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2a7cc-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2a7cc-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2a7cc-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2a7cc-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2a7cc-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2a7cc-133">Windows 2000 Server</span></span>



| <span data-ttu-id="2a7cc-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="2a7cc-134">Entry</span></span> | <span data-ttu-id="2a7cc-135">Value</span><span class="sxs-lookup"><span data-stu-id="2a7cc-135">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="2a7cc-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2a7cc-136">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2a7cc-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a7cc-137">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2a7cc-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a7cc-138">System-Only</span></span>            | <span data-ttu-id="2a7cc-139">False</span><span class="sxs-lookup"><span data-stu-id="2a7cc-139">False</span></span>                                                              |
| <span data-ttu-id="2a7cc-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2a7cc-140">Is-Single-Valued</span></span>       | <span data-ttu-id="2a7cc-141">False</span><span class="sxs-lookup"><span data-stu-id="2a7cc-141">False</span></span>                                                              |
| <span data-ttu-id="2a7cc-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2a7cc-142">Is Indexed</span></span>             | <span data-ttu-id="2a7cc-143">False</span><span class="sxs-lookup"><span data-stu-id="2a7cc-143">False</span></span>                                                              |
| <span data-ttu-id="2a7cc-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2a7cc-144">In Global Catalog</span></span>      | <span data-ttu-id="2a7cc-145">True</span><span class="sxs-lookup"><span data-stu-id="2a7cc-145">True</span></span>                                                               |
| <span data-ttu-id="2a7cc-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2a7cc-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a7cc-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2a7cc-147">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="2a7cc-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a7cc-148">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="2a7cc-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a7cc-149">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="2a7cc-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a7cc-150">Search-Flags</span></span>           | <span data-ttu-id="2a7cc-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a7cc-151">0x00000000</span></span>                                                         |
| <span data-ttu-id="2a7cc-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a7cc-152">System-Flags</span></span>           | <span data-ttu-id="2a7cc-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a7cc-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="2a7cc-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2a7cc-154">Classes used in</span></span>        | [<span data-ttu-id="2a7cc-155">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="2a7cc-155">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2a7cc-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2a7cc-156">Windows Server 2003</span></span>



| <span data-ttu-id="2a7cc-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="2a7cc-157">Entry</span></span> | <span data-ttu-id="2a7cc-158">Value</span><span class="sxs-lookup"><span data-stu-id="2a7cc-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="2a7cc-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2a7cc-159">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2a7cc-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a7cc-160">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2a7cc-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a7cc-161">System-Only</span></span>            | <span data-ttu-id="2a7cc-162">False</span><span class="sxs-lookup"><span data-stu-id="2a7cc-162">False</span></span>                                                              |
| <span data-ttu-id="2a7cc-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2a7cc-163">Is-Single-Valued</span></span>       | <span data-ttu-id="2a7cc-164">False</span><span class="sxs-lookup"><span data-stu-id="2a7cc-164">False</span></span>                                                              |
| <span data-ttu-id="2a7cc-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2a7cc-165">Is Indexed</span></span>             | <span data-ttu-id="2a7cc-166">False</span><span class="sxs-lookup"><span data-stu-id="2a7cc-166">False</span></span>                                                              |
| <span data-ttu-id="2a7cc-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2a7cc-167">In Global Catalog</span></span>      | <span data-ttu-id="2a7cc-168">True</span><span class="sxs-lookup"><span data-stu-id="2a7cc-168">True</span></span>                                                               |
| <span data-ttu-id="2a7cc-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2a7cc-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a7cc-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2a7cc-170">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="2a7cc-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a7cc-171">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="2a7cc-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a7cc-172">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="2a7cc-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a7cc-173">Search-Flags</span></span>           | <span data-ttu-id="2a7cc-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a7cc-174">0x00000000</span></span>                                                         |
| <span data-ttu-id="2a7cc-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a7cc-175">System-Flags</span></span>           | <span data-ttu-id="2a7cc-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a7cc-176">0x00000010</span></span>                                                         |
| <span data-ttu-id="2a7cc-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2a7cc-177">Classes used in</span></span>        | [<span data-ttu-id="2a7cc-178">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="2a7cc-178">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2a7cc-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2a7cc-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2a7cc-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="2a7cc-180">Entry</span></span> | <span data-ttu-id="2a7cc-181">Value</span><span class="sxs-lookup"><span data-stu-id="2a7cc-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="2a7cc-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2a7cc-182">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2a7cc-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a7cc-183">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2a7cc-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a7cc-184">System-Only</span></span>            | <span data-ttu-id="2a7cc-185">False</span><span class="sxs-lookup"><span data-stu-id="2a7cc-185">False</span></span>                                                              |
| <span data-ttu-id="2a7cc-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2a7cc-186">Is-Single-Valued</span></span>       | <span data-ttu-id="2a7cc-187">False</span><span class="sxs-lookup"><span data-stu-id="2a7cc-187">False</span></span>                                                              |
| <span data-ttu-id="2a7cc-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2a7cc-188">Is Indexed</span></span>             | <span data-ttu-id="2a7cc-189">False</span><span class="sxs-lookup"><span data-stu-id="2a7cc-189">False</span></span>                                                              |
| <span data-ttu-id="2a7cc-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2a7cc-190">In Global Catalog</span></span>      | <span data-ttu-id="2a7cc-191">True</span><span class="sxs-lookup"><span data-stu-id="2a7cc-191">True</span></span>                                                               |
| <span data-ttu-id="2a7cc-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2a7cc-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a7cc-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2a7cc-193">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="2a7cc-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a7cc-194">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="2a7cc-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a7cc-195">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="2a7cc-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a7cc-196">Search-Flags</span></span>           | <span data-ttu-id="2a7cc-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a7cc-197">0x00000000</span></span>                                                         |
| <span data-ttu-id="2a7cc-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a7cc-198">System-Flags</span></span>           | <span data-ttu-id="2a7cc-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a7cc-199">0x00000010</span></span>                                                         |
| <span data-ttu-id="2a7cc-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2a7cc-200">Classes used in</span></span>        | [<span data-ttu-id="2a7cc-201">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="2a7cc-201">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2a7cc-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a7cc-202">Windows Server 2008</span></span>



| <span data-ttu-id="2a7cc-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="2a7cc-203">Entry</span></span> | <span data-ttu-id="2a7cc-204">Value</span><span class="sxs-lookup"><span data-stu-id="2a7cc-204">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="2a7cc-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2a7cc-205">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2a7cc-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a7cc-206">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2a7cc-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a7cc-207">System-Only</span></span>            | <span data-ttu-id="2a7cc-208">False</span><span class="sxs-lookup"><span data-stu-id="2a7cc-208">False</span></span>                                                              |
| <span data-ttu-id="2a7cc-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2a7cc-209">Is-Single-Valued</span></span>       | <span data-ttu-id="2a7cc-210">False</span><span class="sxs-lookup"><span data-stu-id="2a7cc-210">False</span></span>                                                              |
| <span data-ttu-id="2a7cc-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2a7cc-211">Is Indexed</span></span>             | <span data-ttu-id="2a7cc-212">False</span><span class="sxs-lookup"><span data-stu-id="2a7cc-212">False</span></span>                                                              |
| <span data-ttu-id="2a7cc-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2a7cc-213">In Global Catalog</span></span>      | <span data-ttu-id="2a7cc-214">True</span><span class="sxs-lookup"><span data-stu-id="2a7cc-214">True</span></span>                                                               |
| <span data-ttu-id="2a7cc-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2a7cc-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a7cc-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2a7cc-216">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="2a7cc-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a7cc-217">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="2a7cc-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a7cc-218">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="2a7cc-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a7cc-219">Search-Flags</span></span>           | <span data-ttu-id="2a7cc-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a7cc-220">0x00000000</span></span>                                                         |
| <span data-ttu-id="2a7cc-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a7cc-221">System-Flags</span></span>           | <span data-ttu-id="2a7cc-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a7cc-222">0x00000010</span></span>                                                         |
| <span data-ttu-id="2a7cc-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2a7cc-223">Classes used in</span></span>        | [<span data-ttu-id="2a7cc-224">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="2a7cc-224">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2a7cc-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2a7cc-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2a7cc-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="2a7cc-226">Entry</span></span> | <span data-ttu-id="2a7cc-227">Value</span><span class="sxs-lookup"><span data-stu-id="2a7cc-227">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="2a7cc-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2a7cc-228">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2a7cc-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a7cc-229">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2a7cc-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a7cc-230">System-Only</span></span>            | <span data-ttu-id="2a7cc-231">False</span><span class="sxs-lookup"><span data-stu-id="2a7cc-231">False</span></span>                                                              |
| <span data-ttu-id="2a7cc-232">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2a7cc-232">Is-Single-Valued</span></span>       | <span data-ttu-id="2a7cc-233">False</span><span class="sxs-lookup"><span data-stu-id="2a7cc-233">False</span></span>                                                              |
| <span data-ttu-id="2a7cc-234">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2a7cc-234">Is Indexed</span></span>             | <span data-ttu-id="2a7cc-235">False</span><span class="sxs-lookup"><span data-stu-id="2a7cc-235">False</span></span>                                                              |
| <span data-ttu-id="2a7cc-236">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2a7cc-236">In Global Catalog</span></span>      | <span data-ttu-id="2a7cc-237">True</span><span class="sxs-lookup"><span data-stu-id="2a7cc-237">True</span></span>                                                               |
| <span data-ttu-id="2a7cc-238">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2a7cc-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a7cc-239">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2a7cc-239">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="2a7cc-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a7cc-240">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="2a7cc-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a7cc-241">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="2a7cc-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a7cc-242">Search-Flags</span></span>           | <span data-ttu-id="2a7cc-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a7cc-243">0x00000000</span></span>                                                         |
| <span data-ttu-id="2a7cc-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a7cc-244">System-Flags</span></span>           | <span data-ttu-id="2a7cc-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a7cc-245">0x00000010</span></span>                                                         |
| <span data-ttu-id="2a7cc-246">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2a7cc-246">Classes used in</span></span>        | [<span data-ttu-id="2a7cc-247">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="2a7cc-247">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2a7cc-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2a7cc-248">Windows Server 2012</span></span>



| <span data-ttu-id="2a7cc-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="2a7cc-249">Entry</span></span> | <span data-ttu-id="2a7cc-250">Value</span><span class="sxs-lookup"><span data-stu-id="2a7cc-250">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="2a7cc-251">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2a7cc-251">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2a7cc-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a7cc-252">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2a7cc-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a7cc-253">System-Only</span></span>            | <span data-ttu-id="2a7cc-254">False</span><span class="sxs-lookup"><span data-stu-id="2a7cc-254">False</span></span>                                                              |
| <span data-ttu-id="2a7cc-255">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2a7cc-255">Is-Single-Valued</span></span>       | <span data-ttu-id="2a7cc-256">False</span><span class="sxs-lookup"><span data-stu-id="2a7cc-256">False</span></span>                                                              |
| <span data-ttu-id="2a7cc-257">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2a7cc-257">Is Indexed</span></span>             | <span data-ttu-id="2a7cc-258">False</span><span class="sxs-lookup"><span data-stu-id="2a7cc-258">False</span></span>                                                              |
| <span data-ttu-id="2a7cc-259">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2a7cc-259">In Global Catalog</span></span>      | <span data-ttu-id="2a7cc-260">True</span><span class="sxs-lookup"><span data-stu-id="2a7cc-260">True</span></span>                                                               |
| <span data-ttu-id="2a7cc-261">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2a7cc-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a7cc-262">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2a7cc-262">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="2a7cc-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a7cc-263">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="2a7cc-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a7cc-264">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="2a7cc-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a7cc-265">Search-Flags</span></span>           | <span data-ttu-id="2a7cc-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a7cc-266">0x00000000</span></span>                                                         |
| <span data-ttu-id="2a7cc-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a7cc-267">System-Flags</span></span>           | <span data-ttu-id="2a7cc-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a7cc-268">0x00000010</span></span>                                                         |
| <span data-ttu-id="2a7cc-269">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2a7cc-269">Classes used in</span></span>        | [<span data-ttu-id="2a7cc-270">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="2a7cc-270">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





