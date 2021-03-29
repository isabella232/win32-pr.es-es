---
title: Mostrar atributo en la libreta de direcciones
description: Este atributo se utiliza para indicar en qué libretas de direcciones MAPI aparecerá un objeto.
ms.assetid: de00da4d-7c04-4d1d-b375-ce3b5eb2f50f
ms.tgt_platform: multiple
keywords:
- Mostrar el esquema de AD del atributo de libreta de direcciones
- showInAddressBook atributo AD Schema
topic_type:
- apiref
api_name:
- Show-In-Address-Book
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44632604c539278c67e9dd46537d8e797e2d70d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493696"
---
# <a name="show-in-address-book-attribute"></a><span data-ttu-id="e9e79-105">Mostrar atributo en la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="e9e79-105">Show-In-Address-Book attribute</span></span>

<span data-ttu-id="e9e79-106">Este atributo se utiliza para indicar en qué libretas de direcciones MAPI aparecerá un objeto.</span><span class="sxs-lookup"><span data-stu-id="e9e79-106">This attribute is used to indicate in which MAPI address books an object will appear.</span></span> <span data-ttu-id="e9e79-107">Normalmente se mantiene mediante el servicio de actualización de destinatarios de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e9e79-107">It is usually maintained by the Exchange Recipient Update Service.</span></span>



| <span data-ttu-id="e9e79-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="e9e79-108">Entry</span></span> | <span data-ttu-id="e9e79-109">Value</span><span class="sxs-lookup"><span data-stu-id="e9e79-109">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="e9e79-110">CN</span><span class="sxs-lookup"><span data-stu-id="e9e79-110">CN</span></span>                | <span data-ttu-id="e9e79-111">Mostrar en la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="e9e79-111">Show-In-Address-Book</span></span>                    |
| <span data-ttu-id="e9e79-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="e9e79-112">Ldap-Display-Name</span></span> | <span data-ttu-id="e9e79-113">showInAddressBook</span><span class="sxs-lookup"><span data-stu-id="e9e79-113">showInAddressBook</span></span>                       |
| <span data-ttu-id="e9e79-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="e9e79-114">Size</span></span>              | \-                                      |
| <span data-ttu-id="e9e79-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="e9e79-115">Update Privilege</span></span>  | <span data-ttu-id="e9e79-116">Lo utiliza el sistema.</span><span class="sxs-lookup"><span data-stu-id="e9e79-116">This is used by the system.</span></span>             |
| <span data-ttu-id="e9e79-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="e9e79-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="e9e79-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e9e79-118">Attribute-Id</span></span>      | <span data-ttu-id="e9e79-119">1.2.840.113556.1.4.644</span><span class="sxs-lookup"><span data-stu-id="e9e79-119">1.2.840.113556.1.4.644</span></span>                  |
| <span data-ttu-id="e9e79-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e9e79-120">System-Id-Guid</span></span>    | <span data-ttu-id="e9e79-121">3e74f60e-3e73-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e9e79-121">3e74f60e-3e73-11d1-a9c0-0000f80367c1</span></span>    |
| <span data-ttu-id="e9e79-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9e79-122">Syntax</span></span>            | [<span data-ttu-id="e9e79-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="e9e79-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="e9e79-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="e9e79-124">Implementations</span></span>

-   [<span data-ttu-id="e9e79-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e9e79-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e9e79-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e9e79-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e9e79-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e9e79-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e9e79-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e9e79-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e9e79-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e9e79-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e9e79-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e9e79-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e9e79-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e9e79-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e9e79-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="e9e79-132">Entry</span></span> | <span data-ttu-id="e9e79-133">Value</span><span class="sxs-lookup"><span data-stu-id="e9e79-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="e9e79-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e9e79-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e9e79-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9e79-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e9e79-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9e79-136">System-Only</span></span>            | <span data-ttu-id="e9e79-137">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-137">False</span></span>                                                |
| <span data-ttu-id="e9e79-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e9e79-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e9e79-139">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-139">False</span></span>                                                |
| <span data-ttu-id="e9e79-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e9e79-140">Is Indexed</span></span>             | <span data-ttu-id="e9e79-141">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-141">False</span></span>                                                |
| <span data-ttu-id="e9e79-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e9e79-142">In Global Catalog</span></span>      | <span data-ttu-id="e9e79-143">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-143">False</span></span>                                                |
| <span data-ttu-id="e9e79-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e9e79-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9e79-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9e79-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="e9e79-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9e79-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="e9e79-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9e79-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="e9e79-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e79-148">Search-Flags</span></span>           | <span data-ttu-id="e9e79-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9e79-149">0x00000010</span></span>                                           |
| <span data-ttu-id="e9e79-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e79-150">System-Flags</span></span>           | <span data-ttu-id="e9e79-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9e79-151">0x00000010</span></span>                                           |
| <span data-ttu-id="e9e79-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e9e79-152">Classes used in</span></span>        | [<span data-ttu-id="e9e79-153">**Destinatario de correo**</span><span class="sxs-lookup"><span data-stu-id="e9e79-153">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e9e79-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e9e79-154">Windows Server 2003</span></span>



| <span data-ttu-id="e9e79-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="e9e79-155">Entry</span></span> | <span data-ttu-id="e9e79-156">Value</span><span class="sxs-lookup"><span data-stu-id="e9e79-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="e9e79-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e9e79-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e9e79-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9e79-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e9e79-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9e79-159">System-Only</span></span>            | <span data-ttu-id="e9e79-160">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-160">False</span></span>                                                |
| <span data-ttu-id="e9e79-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e9e79-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e9e79-162">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-162">False</span></span>                                                |
| <span data-ttu-id="e9e79-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e9e79-163">Is Indexed</span></span>             | <span data-ttu-id="e9e79-164">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-164">False</span></span>                                                |
| <span data-ttu-id="e9e79-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e9e79-165">In Global Catalog</span></span>      | <span data-ttu-id="e9e79-166">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-166">False</span></span>                                                |
| <span data-ttu-id="e9e79-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e9e79-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9e79-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9e79-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="e9e79-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9e79-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="e9e79-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9e79-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="e9e79-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e79-171">Search-Flags</span></span>           | <span data-ttu-id="e9e79-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9e79-172">0x00000010</span></span>                                           |
| <span data-ttu-id="e9e79-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e79-173">System-Flags</span></span>           | <span data-ttu-id="e9e79-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9e79-174">0x00000010</span></span>                                           |
| <span data-ttu-id="e9e79-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e9e79-175">Classes used in</span></span>        | [<span data-ttu-id="e9e79-176">**Destinatario de correo**</span><span class="sxs-lookup"><span data-stu-id="e9e79-176">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e9e79-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e9e79-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e9e79-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="e9e79-178">Entry</span></span> | <span data-ttu-id="e9e79-179">Value</span><span class="sxs-lookup"><span data-stu-id="e9e79-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="e9e79-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e9e79-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e9e79-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9e79-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e9e79-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9e79-182">System-Only</span></span>            | <span data-ttu-id="e9e79-183">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-183">False</span></span>                                                |
| <span data-ttu-id="e9e79-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e9e79-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e9e79-185">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-185">False</span></span>                                                |
| <span data-ttu-id="e9e79-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e9e79-186">Is Indexed</span></span>             | <span data-ttu-id="e9e79-187">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-187">False</span></span>                                                |
| <span data-ttu-id="e9e79-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e9e79-188">In Global Catalog</span></span>      | <span data-ttu-id="e9e79-189">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-189">False</span></span>                                                |
| <span data-ttu-id="e9e79-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e9e79-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9e79-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9e79-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="e9e79-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9e79-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="e9e79-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9e79-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="e9e79-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e79-194">Search-Flags</span></span>           | <span data-ttu-id="e9e79-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9e79-195">0x00000010</span></span>                                           |
| <span data-ttu-id="e9e79-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e79-196">System-Flags</span></span>           | <span data-ttu-id="e9e79-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9e79-197">0x00000010</span></span>                                           |
| <span data-ttu-id="e9e79-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e9e79-198">Classes used in</span></span>        | [<span data-ttu-id="e9e79-199">**Destinatario de correo**</span><span class="sxs-lookup"><span data-stu-id="e9e79-199">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e9e79-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9e79-200">Windows Server 2008</span></span>



| <span data-ttu-id="e9e79-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="e9e79-201">Entry</span></span> | <span data-ttu-id="e9e79-202">Value</span><span class="sxs-lookup"><span data-stu-id="e9e79-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="e9e79-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e9e79-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e9e79-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9e79-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e9e79-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9e79-205">System-Only</span></span>            | <span data-ttu-id="e9e79-206">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-206">False</span></span>                                                |
| <span data-ttu-id="e9e79-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e9e79-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e9e79-208">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-208">False</span></span>                                                |
| <span data-ttu-id="e9e79-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e9e79-209">Is Indexed</span></span>             | <span data-ttu-id="e9e79-210">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-210">False</span></span>                                                |
| <span data-ttu-id="e9e79-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e9e79-211">In Global Catalog</span></span>      | <span data-ttu-id="e9e79-212">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-212">False</span></span>                                                |
| <span data-ttu-id="e9e79-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e9e79-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9e79-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9e79-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="e9e79-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9e79-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="e9e79-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9e79-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="e9e79-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e79-217">Search-Flags</span></span>           | <span data-ttu-id="e9e79-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9e79-218">0x00000010</span></span>                                           |
| <span data-ttu-id="e9e79-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e79-219">System-Flags</span></span>           | <span data-ttu-id="e9e79-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9e79-220">0x00000010</span></span>                                           |
| <span data-ttu-id="e9e79-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e9e79-221">Classes used in</span></span>        | [<span data-ttu-id="e9e79-222">**Destinatario de correo**</span><span class="sxs-lookup"><span data-stu-id="e9e79-222">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e9e79-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e9e79-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e9e79-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="e9e79-224">Entry</span></span> | <span data-ttu-id="e9e79-225">Value</span><span class="sxs-lookup"><span data-stu-id="e9e79-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="e9e79-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e9e79-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e9e79-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9e79-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e9e79-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9e79-228">System-Only</span></span>            | <span data-ttu-id="e9e79-229">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-229">False</span></span>                                                |
| <span data-ttu-id="e9e79-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e9e79-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e9e79-231">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-231">False</span></span>                                                |
| <span data-ttu-id="e9e79-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e9e79-232">Is Indexed</span></span>             | <span data-ttu-id="e9e79-233">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-233">False</span></span>                                                |
| <span data-ttu-id="e9e79-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e9e79-234">In Global Catalog</span></span>      | <span data-ttu-id="e9e79-235">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-235">False</span></span>                                                |
| <span data-ttu-id="e9e79-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e9e79-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9e79-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9e79-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="e9e79-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9e79-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="e9e79-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9e79-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="e9e79-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e79-240">Search-Flags</span></span>           | <span data-ttu-id="e9e79-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9e79-241">0x00000010</span></span>                                           |
| <span data-ttu-id="e9e79-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e79-242">System-Flags</span></span>           | <span data-ttu-id="e9e79-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9e79-243">0x00000010</span></span>                                           |
| <span data-ttu-id="e9e79-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e9e79-244">Classes used in</span></span>        | [<span data-ttu-id="e9e79-245">**Destinatario de correo**</span><span class="sxs-lookup"><span data-stu-id="e9e79-245">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e9e79-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9e79-246">Windows Server 2012</span></span>



| <span data-ttu-id="e9e79-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="e9e79-247">Entry</span></span> | <span data-ttu-id="e9e79-248">Value</span><span class="sxs-lookup"><span data-stu-id="e9e79-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="e9e79-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e9e79-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e9e79-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9e79-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e9e79-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9e79-251">System-Only</span></span>            | <span data-ttu-id="e9e79-252">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-252">False</span></span>                                                |
| <span data-ttu-id="e9e79-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e9e79-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e9e79-254">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-254">False</span></span>                                                |
| <span data-ttu-id="e9e79-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e9e79-255">Is Indexed</span></span>             | <span data-ttu-id="e9e79-256">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-256">False</span></span>                                                |
| <span data-ttu-id="e9e79-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e9e79-257">In Global Catalog</span></span>      | <span data-ttu-id="e9e79-258">False</span><span class="sxs-lookup"><span data-stu-id="e9e79-258">False</span></span>                                                |
| <span data-ttu-id="e9e79-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e9e79-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9e79-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9e79-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="e9e79-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9e79-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="e9e79-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9e79-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="e9e79-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e79-263">Search-Flags</span></span>           | <span data-ttu-id="e9e79-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9e79-264">0x00000010</span></span>                                           |
| <span data-ttu-id="e9e79-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e79-265">System-Flags</span></span>           | <span data-ttu-id="e9e79-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9e79-266">0x00000010</span></span>                                           |
| <span data-ttu-id="e9e79-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e9e79-267">Classes used in</span></span>        | [<span data-ttu-id="e9e79-268">**Destinatario de correo**</span><span class="sxs-lookup"><span data-stu-id="e9e79-268">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 





