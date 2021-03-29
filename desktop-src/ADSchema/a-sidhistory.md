---
title: SID-History atributo)
description: Contiene los SID anteriores usados para el objeto si el objeto se ha despasado de otro dominio.
ms.assetid: d738002b-fc05-4c60-aaf9-b83be61ed5a9
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de SID-History
- sIDHistory atributo AD Schema
topic_type:
- apiref
api_name:
- SID-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16474a6463fc99e7ed2c1d2b1a2cdbf6ea9b6614
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493691"
---
# <a name="sid-history-attribute"></a><span data-ttu-id="53560-105">SID-History atributo)</span><span class="sxs-lookup"><span data-stu-id="53560-105">SID-History attribute</span></span>

<span data-ttu-id="53560-106">Contiene los SID anteriores usados para el objeto si el objeto se ha despasado de otro dominio.</span><span class="sxs-lookup"><span data-stu-id="53560-106">Contains previous SIDs used for the object if the object was moved from another domain.</span></span> <span data-ttu-id="53560-107">Cada vez que un objeto se mueve de un dominio a otro, se crea un nuevo SID y ese nuevo SID se convierte en el objectSID.</span><span class="sxs-lookup"><span data-stu-id="53560-107">Whenever an object is moved from one domain to another, a new SID is created and that new SID becomes the objectSID.</span></span> <span data-ttu-id="53560-108">El SID anterior se agrega a la propiedad sIDHistory.</span><span class="sxs-lookup"><span data-stu-id="53560-108">The previous SID is added to the sIDHistory property.</span></span>



| <span data-ttu-id="53560-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="53560-109">Entry</span></span> | <span data-ttu-id="53560-110">Value</span><span class="sxs-lookup"><span data-stu-id="53560-110">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="53560-111">CN</span><span class="sxs-lookup"><span data-stu-id="53560-111">CN</span></span>                | <span data-ttu-id="53560-112">SID-History</span><span class="sxs-lookup"><span data-stu-id="53560-112">SID-History</span></span>                                    |
| <span data-ttu-id="53560-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="53560-113">Ldap-Display-Name</span></span> | <span data-ttu-id="53560-114">Correspondientes</span><span class="sxs-lookup"><span data-stu-id="53560-114">sIDHistory</span></span>                                     |
| <span data-ttu-id="53560-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="53560-115">Size</span></span>              | \-                                             |
| <span data-ttu-id="53560-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="53560-116">Update Privilege</span></span>  | <span data-ttu-id="53560-117">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="53560-117">This value is set by the system.</span></span>               |
| <span data-ttu-id="53560-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="53560-118">Update Frequency</span></span>  | <span data-ttu-id="53560-119">Cada vez que el objeto se mueve a un nuevo dominio.</span><span class="sxs-lookup"><span data-stu-id="53560-119">Each time the object is moved to a new domain.</span></span> |
| <span data-ttu-id="53560-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="53560-120">Attribute-Id</span></span>      | <span data-ttu-id="53560-121">1.2.840.113556.1.4.609</span><span class="sxs-lookup"><span data-stu-id="53560-121">1.2.840.113556.1.4.609</span></span>                         |
| <span data-ttu-id="53560-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="53560-122">System-Id-Guid</span></span>    | <span data-ttu-id="53560-123">17eb4278-d167-11d0-b002-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="53560-123">17eb4278-d167-11d0-b002-0000f80367c1</span></span>           |
| <span data-ttu-id="53560-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53560-124">Syntax</span></span>            | [<span data-ttu-id="53560-125">**Cadena (SID)**</span><span class="sxs-lookup"><span data-stu-id="53560-125">**String(Sid)**</span></span>](s-string-sid.md)            |



## <a name="implementations"></a><span data-ttu-id="53560-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="53560-126">Implementations</span></span>

-   [<span data-ttu-id="53560-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="53560-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="53560-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="53560-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="53560-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="53560-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="53560-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="53560-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="53560-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="53560-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="53560-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="53560-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="53560-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="53560-133">Windows 2000 Server</span></span>



| <span data-ttu-id="53560-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="53560-134">Entry</span></span> | <span data-ttu-id="53560-135">Value</span><span class="sxs-lookup"><span data-stu-id="53560-135">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="53560-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="53560-136">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="53560-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53560-137">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="53560-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="53560-138">System-Only</span></span>            | <span data-ttu-id="53560-139">True</span><span class="sxs-lookup"><span data-stu-id="53560-139">True</span></span>                                                         |
| <span data-ttu-id="53560-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="53560-140">Is-Single-Valued</span></span>       | <span data-ttu-id="53560-141">False</span><span class="sxs-lookup"><span data-stu-id="53560-141">False</span></span>                                                        |
| <span data-ttu-id="53560-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="53560-142">Is Indexed</span></span>             | <span data-ttu-id="53560-143">True</span><span class="sxs-lookup"><span data-stu-id="53560-143">True</span></span>                                                         |
| <span data-ttu-id="53560-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="53560-144">In Global Catalog</span></span>      | <span data-ttu-id="53560-145">True</span><span class="sxs-lookup"><span data-stu-id="53560-145">True</span></span>                                                         |
| <span data-ttu-id="53560-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="53560-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="53560-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="53560-147">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="53560-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53560-148">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="53560-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53560-149">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="53560-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53560-150">Search-Flags</span></span>           | <span data-ttu-id="53560-151">0x00000001</span><span class="sxs-lookup"><span data-stu-id="53560-151">0x00000001</span></span>                                                   |
| <span data-ttu-id="53560-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53560-152">System-Flags</span></span>           | <span data-ttu-id="53560-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="53560-153">0x00000012</span></span>                                                   |
| <span data-ttu-id="53560-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="53560-154">Classes used in</span></span>        | [<span data-ttu-id="53560-155">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="53560-155">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="53560-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="53560-156">Windows Server 2003</span></span>



| <span data-ttu-id="53560-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="53560-157">Entry</span></span> | <span data-ttu-id="53560-158">Value</span><span class="sxs-lookup"><span data-stu-id="53560-158">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="53560-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="53560-159">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="53560-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53560-160">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="53560-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="53560-161">System-Only</span></span>            | <span data-ttu-id="53560-162">False</span><span class="sxs-lookup"><span data-stu-id="53560-162">False</span></span>                                                        |
| <span data-ttu-id="53560-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="53560-163">Is-Single-Valued</span></span>       | <span data-ttu-id="53560-164">False</span><span class="sxs-lookup"><span data-stu-id="53560-164">False</span></span>                                                        |
| <span data-ttu-id="53560-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="53560-165">Is Indexed</span></span>             | <span data-ttu-id="53560-166">True</span><span class="sxs-lookup"><span data-stu-id="53560-166">True</span></span>                                                         |
| <span data-ttu-id="53560-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="53560-167">In Global Catalog</span></span>      | <span data-ttu-id="53560-168">True</span><span class="sxs-lookup"><span data-stu-id="53560-168">True</span></span>                                                         |
| <span data-ttu-id="53560-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="53560-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="53560-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="53560-170">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="53560-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53560-171">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="53560-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53560-172">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="53560-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53560-173">Search-Flags</span></span>           | <span data-ttu-id="53560-174">0x00000001</span><span class="sxs-lookup"><span data-stu-id="53560-174">0x00000001</span></span>                                                   |
| <span data-ttu-id="53560-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53560-175">System-Flags</span></span>           | <span data-ttu-id="53560-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="53560-176">0x00000012</span></span>                                                   |
| <span data-ttu-id="53560-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="53560-177">Classes used in</span></span>        | [<span data-ttu-id="53560-178">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="53560-178">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="53560-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="53560-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="53560-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="53560-180">Entry</span></span> | <span data-ttu-id="53560-181">Value</span><span class="sxs-lookup"><span data-stu-id="53560-181">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="53560-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="53560-182">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="53560-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53560-183">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="53560-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="53560-184">System-Only</span></span>            | <span data-ttu-id="53560-185">False</span><span class="sxs-lookup"><span data-stu-id="53560-185">False</span></span>                                                        |
| <span data-ttu-id="53560-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="53560-186">Is-Single-Valued</span></span>       | <span data-ttu-id="53560-187">False</span><span class="sxs-lookup"><span data-stu-id="53560-187">False</span></span>                                                        |
| <span data-ttu-id="53560-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="53560-188">Is Indexed</span></span>             | <span data-ttu-id="53560-189">True</span><span class="sxs-lookup"><span data-stu-id="53560-189">True</span></span>                                                         |
| <span data-ttu-id="53560-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="53560-190">In Global Catalog</span></span>      | <span data-ttu-id="53560-191">True</span><span class="sxs-lookup"><span data-stu-id="53560-191">True</span></span>                                                         |
| <span data-ttu-id="53560-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="53560-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="53560-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="53560-193">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="53560-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53560-194">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="53560-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53560-195">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="53560-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53560-196">Search-Flags</span></span>           | <span data-ttu-id="53560-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="53560-197">0x00000001</span></span>                                                   |
| <span data-ttu-id="53560-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53560-198">System-Flags</span></span>           | <span data-ttu-id="53560-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="53560-199">0x00000012</span></span>                                                   |
| <span data-ttu-id="53560-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="53560-200">Classes used in</span></span>        | [<span data-ttu-id="53560-201">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="53560-201">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="53560-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53560-202">Windows Server 2008</span></span>



| <span data-ttu-id="53560-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="53560-203">Entry</span></span> | <span data-ttu-id="53560-204">Value</span><span class="sxs-lookup"><span data-stu-id="53560-204">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="53560-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="53560-205">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="53560-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53560-206">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="53560-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="53560-207">System-Only</span></span>            | <span data-ttu-id="53560-208">False</span><span class="sxs-lookup"><span data-stu-id="53560-208">False</span></span>                                                        |
| <span data-ttu-id="53560-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="53560-209">Is-Single-Valued</span></span>       | <span data-ttu-id="53560-210">False</span><span class="sxs-lookup"><span data-stu-id="53560-210">False</span></span>                                                        |
| <span data-ttu-id="53560-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="53560-211">Is Indexed</span></span>             | <span data-ttu-id="53560-212">True</span><span class="sxs-lookup"><span data-stu-id="53560-212">True</span></span>                                                         |
| <span data-ttu-id="53560-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="53560-213">In Global Catalog</span></span>      | <span data-ttu-id="53560-214">True</span><span class="sxs-lookup"><span data-stu-id="53560-214">True</span></span>                                                         |
| <span data-ttu-id="53560-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="53560-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="53560-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="53560-216">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="53560-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53560-217">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="53560-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53560-218">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="53560-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53560-219">Search-Flags</span></span>           | <span data-ttu-id="53560-220">0x00000001</span><span class="sxs-lookup"><span data-stu-id="53560-220">0x00000001</span></span>                                                   |
| <span data-ttu-id="53560-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53560-221">System-Flags</span></span>           | <span data-ttu-id="53560-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="53560-222">0x00000012</span></span>                                                   |
| <span data-ttu-id="53560-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="53560-223">Classes used in</span></span>        | [<span data-ttu-id="53560-224">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="53560-224">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="53560-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="53560-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="53560-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="53560-226">Entry</span></span> | <span data-ttu-id="53560-227">Value</span><span class="sxs-lookup"><span data-stu-id="53560-227">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="53560-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="53560-228">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="53560-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53560-229">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="53560-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="53560-230">System-Only</span></span>            | <span data-ttu-id="53560-231">False</span><span class="sxs-lookup"><span data-stu-id="53560-231">False</span></span>                                                        |
| <span data-ttu-id="53560-232">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="53560-232">Is-Single-Valued</span></span>       | <span data-ttu-id="53560-233">False</span><span class="sxs-lookup"><span data-stu-id="53560-233">False</span></span>                                                        |
| <span data-ttu-id="53560-234">Está indexado</span><span class="sxs-lookup"><span data-stu-id="53560-234">Is Indexed</span></span>             | <span data-ttu-id="53560-235">True</span><span class="sxs-lookup"><span data-stu-id="53560-235">True</span></span>                                                         |
| <span data-ttu-id="53560-236">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="53560-236">In Global Catalog</span></span>      | <span data-ttu-id="53560-237">True</span><span class="sxs-lookup"><span data-stu-id="53560-237">True</span></span>                                                         |
| <span data-ttu-id="53560-238">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="53560-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="53560-239">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="53560-239">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="53560-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53560-240">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="53560-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53560-241">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="53560-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53560-242">Search-Flags</span></span>           | <span data-ttu-id="53560-243">0x00000001</span><span class="sxs-lookup"><span data-stu-id="53560-243">0x00000001</span></span>                                                   |
| <span data-ttu-id="53560-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53560-244">System-Flags</span></span>           | <span data-ttu-id="53560-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="53560-245">0x00000012</span></span>                                                   |
| <span data-ttu-id="53560-246">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="53560-246">Classes used in</span></span>        | [<span data-ttu-id="53560-247">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="53560-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="53560-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53560-248">Windows Server 2012</span></span>



| <span data-ttu-id="53560-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="53560-249">Entry</span></span> | <span data-ttu-id="53560-250">Value</span><span class="sxs-lookup"><span data-stu-id="53560-250">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="53560-251">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="53560-251">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="53560-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53560-252">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="53560-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="53560-253">System-Only</span></span>            | <span data-ttu-id="53560-254">False</span><span class="sxs-lookup"><span data-stu-id="53560-254">False</span></span>                                                        |
| <span data-ttu-id="53560-255">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="53560-255">Is-Single-Valued</span></span>       | <span data-ttu-id="53560-256">False</span><span class="sxs-lookup"><span data-stu-id="53560-256">False</span></span>                                                        |
| <span data-ttu-id="53560-257">Está indexado</span><span class="sxs-lookup"><span data-stu-id="53560-257">Is Indexed</span></span>             | <span data-ttu-id="53560-258">True</span><span class="sxs-lookup"><span data-stu-id="53560-258">True</span></span>                                                         |
| <span data-ttu-id="53560-259">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="53560-259">In Global Catalog</span></span>      | <span data-ttu-id="53560-260">True</span><span class="sxs-lookup"><span data-stu-id="53560-260">True</span></span>                                                         |
| <span data-ttu-id="53560-261">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="53560-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="53560-262">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="53560-262">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="53560-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53560-263">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="53560-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53560-264">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="53560-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53560-265">Search-Flags</span></span>           | <span data-ttu-id="53560-266">0x00000001</span><span class="sxs-lookup"><span data-stu-id="53560-266">0x00000001</span></span>                                                   |
| <span data-ttu-id="53560-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53560-267">System-Flags</span></span>           | <span data-ttu-id="53560-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="53560-268">0x00000012</span></span>                                                   |
| <span data-ttu-id="53560-269">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="53560-269">Classes used in</span></span>        | [<span data-ttu-id="53560-270">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="53560-270">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





