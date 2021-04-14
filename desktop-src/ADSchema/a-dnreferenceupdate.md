---
title: Atributo DN-Reference-Update
description: Si se cambia el nombre de un objeto, este atributo se utiliza para realizar el seguimiento de todos los nombres anteriores y actuales asignados a un objeto para que los objetos vinculados puedan encontrarlos.
ms.assetid: 28e02a38-eed8-475c-a381-145857477ec6
ms.tgt_platform: multiple
keywords:
- DN-Reference-actualizar atributo AD Schema
- dNReferenceUpdate esquema de AD de atributos
topic_type:
- apiref
api_name:
- DN-Reference-Update
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71e8360be6e7ed6697363daa0f6ff32e2ec5fb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659187"
---
# <a name="dn-reference-update-attribute"></a><span data-ttu-id="64d57-105">Atributo DN-Reference-Update</span><span class="sxs-lookup"><span data-stu-id="64d57-105">DN-Reference-Update attribute</span></span>

<span data-ttu-id="64d57-106">Si se cambia el nombre de un objeto, este atributo se utiliza para realizar el seguimiento de todos los nombres anteriores y actuales asignados a un objeto para que los objetos vinculados puedan encontrarlos.</span><span class="sxs-lookup"><span data-stu-id="64d57-106">If an object is renamed, this attribute is used to track all of the previous and current names that have been assigned to an object so that linked objects can still find it.</span></span>



| <span data-ttu-id="64d57-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="64d57-107">Entry</span></span> | <span data-ttu-id="64d57-108">Value</span><span class="sxs-lookup"><span data-stu-id="64d57-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="64d57-109">CN</span><span class="sxs-lookup"><span data-stu-id="64d57-109">CN</span></span>                | <span data-ttu-id="64d57-110">DN-Reference-actualizar</span><span class="sxs-lookup"><span data-stu-id="64d57-110">DN-Reference-Update</span></span>                     |
| <span data-ttu-id="64d57-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="64d57-111">Ldap-Display-Name</span></span> | <span data-ttu-id="64d57-112">dNReferenceUpdate</span><span class="sxs-lookup"><span data-stu-id="64d57-112">dNReferenceUpdate</span></span>                       |
| <span data-ttu-id="64d57-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="64d57-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="64d57-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="64d57-114">Update Privilege</span></span>  | <span data-ttu-id="64d57-115">Lo establece el sistema.</span><span class="sxs-lookup"><span data-stu-id="64d57-115">This is set by the system.</span></span>              |
| <span data-ttu-id="64d57-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="64d57-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="64d57-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="64d57-117">Attribute-Id</span></span>      | <span data-ttu-id="64d57-118">1.2.840.113556.1.4.1242</span><span class="sxs-lookup"><span data-stu-id="64d57-118">1.2.840.113556.1.4.1242</span></span>                 |
| <span data-ttu-id="64d57-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="64d57-119">System-Id-Guid</span></span>    | <span data-ttu-id="64d57-120">2df90d86-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="64d57-120">2df90d86-009f-11d2-aa4c-00c04fd7d83a</span></span>    |
| <span data-ttu-id="64d57-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64d57-121">Syntax</span></span>            | [<span data-ttu-id="64d57-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="64d57-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="64d57-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="64d57-123">Implementations</span></span>

-   [<span data-ttu-id="64d57-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="64d57-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="64d57-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="64d57-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="64d57-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="64d57-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="64d57-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="64d57-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="64d57-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="64d57-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="64d57-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="64d57-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="64d57-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="64d57-130">Windows 2000 Server</span></span>



| <span data-ttu-id="64d57-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="64d57-131">Entry</span></span> | <span data-ttu-id="64d57-132">Value</span><span class="sxs-lookup"><span data-stu-id="64d57-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="64d57-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="64d57-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="64d57-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64d57-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="64d57-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="64d57-135">System-Only</span></span>            | <span data-ttu-id="64d57-136">True</span><span class="sxs-lookup"><span data-stu-id="64d57-136">True</span></span>                                                               |
| <span data-ttu-id="64d57-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="64d57-137">Is-Single-Valued</span></span>       | <span data-ttu-id="64d57-138">False</span><span class="sxs-lookup"><span data-stu-id="64d57-138">False</span></span>                                                              |
| <span data-ttu-id="64d57-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="64d57-139">Is Indexed</span></span>             | <span data-ttu-id="64d57-140">False</span><span class="sxs-lookup"><span data-stu-id="64d57-140">False</span></span>                                                              |
| <span data-ttu-id="64d57-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="64d57-141">In Global Catalog</span></span>      | <span data-ttu-id="64d57-142">False</span><span class="sxs-lookup"><span data-stu-id="64d57-142">False</span></span>                                                              |
| <span data-ttu-id="64d57-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="64d57-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="64d57-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="64d57-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="64d57-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64d57-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="64d57-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64d57-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="64d57-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64d57-147">Search-Flags</span></span>           | <span data-ttu-id="64d57-148">0x00000008</span><span class="sxs-lookup"><span data-stu-id="64d57-148">0x00000008</span></span>                                                         |
| <span data-ttu-id="64d57-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64d57-149">System-Flags</span></span>           | <span data-ttu-id="64d57-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64d57-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="64d57-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="64d57-151">Classes used in</span></span>        | [<span data-ttu-id="64d57-152">**Infraestructura: actualizar**</span><span class="sxs-lookup"><span data-stu-id="64d57-152">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="64d57-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="64d57-153">Windows Server 2003</span></span>



| <span data-ttu-id="64d57-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="64d57-154">Entry</span></span> | <span data-ttu-id="64d57-155">Value</span><span class="sxs-lookup"><span data-stu-id="64d57-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="64d57-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="64d57-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="64d57-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64d57-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="64d57-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="64d57-158">System-Only</span></span>            | <span data-ttu-id="64d57-159">True</span><span class="sxs-lookup"><span data-stu-id="64d57-159">True</span></span>                                                               |
| <span data-ttu-id="64d57-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="64d57-160">Is-Single-Valued</span></span>       | <span data-ttu-id="64d57-161">False</span><span class="sxs-lookup"><span data-stu-id="64d57-161">False</span></span>                                                              |
| <span data-ttu-id="64d57-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="64d57-162">Is Indexed</span></span>             | <span data-ttu-id="64d57-163">False</span><span class="sxs-lookup"><span data-stu-id="64d57-163">False</span></span>                                                              |
| <span data-ttu-id="64d57-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="64d57-164">In Global Catalog</span></span>      | <span data-ttu-id="64d57-165">False</span><span class="sxs-lookup"><span data-stu-id="64d57-165">False</span></span>                                                              |
| <span data-ttu-id="64d57-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="64d57-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="64d57-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="64d57-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="64d57-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64d57-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="64d57-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64d57-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="64d57-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64d57-170">Search-Flags</span></span>           | <span data-ttu-id="64d57-171">0x00000008</span><span class="sxs-lookup"><span data-stu-id="64d57-171">0x00000008</span></span>                                                         |
| <span data-ttu-id="64d57-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64d57-172">System-Flags</span></span>           | <span data-ttu-id="64d57-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64d57-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="64d57-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="64d57-174">Classes used in</span></span>        | [<span data-ttu-id="64d57-175">**Infraestructura: actualizar**</span><span class="sxs-lookup"><span data-stu-id="64d57-175">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="64d57-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="64d57-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="64d57-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="64d57-177">Entry</span></span> | <span data-ttu-id="64d57-178">Value</span><span class="sxs-lookup"><span data-stu-id="64d57-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="64d57-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="64d57-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="64d57-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64d57-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="64d57-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="64d57-181">System-Only</span></span>            | <span data-ttu-id="64d57-182">True</span><span class="sxs-lookup"><span data-stu-id="64d57-182">True</span></span>                                                               |
| <span data-ttu-id="64d57-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="64d57-183">Is-Single-Valued</span></span>       | <span data-ttu-id="64d57-184">False</span><span class="sxs-lookup"><span data-stu-id="64d57-184">False</span></span>                                                              |
| <span data-ttu-id="64d57-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="64d57-185">Is Indexed</span></span>             | <span data-ttu-id="64d57-186">False</span><span class="sxs-lookup"><span data-stu-id="64d57-186">False</span></span>                                                              |
| <span data-ttu-id="64d57-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="64d57-187">In Global Catalog</span></span>      | <span data-ttu-id="64d57-188">False</span><span class="sxs-lookup"><span data-stu-id="64d57-188">False</span></span>                                                              |
| <span data-ttu-id="64d57-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="64d57-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="64d57-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="64d57-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="64d57-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64d57-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="64d57-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64d57-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="64d57-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64d57-193">Search-Flags</span></span>           | <span data-ttu-id="64d57-194">0x00000008</span><span class="sxs-lookup"><span data-stu-id="64d57-194">0x00000008</span></span>                                                         |
| <span data-ttu-id="64d57-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64d57-195">System-Flags</span></span>           | <span data-ttu-id="64d57-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64d57-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="64d57-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="64d57-197">Classes used in</span></span>        | [<span data-ttu-id="64d57-198">**Infraestructura: actualizar**</span><span class="sxs-lookup"><span data-stu-id="64d57-198">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="64d57-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64d57-199">Windows Server 2008</span></span>



| <span data-ttu-id="64d57-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="64d57-200">Entry</span></span> | <span data-ttu-id="64d57-201">Value</span><span class="sxs-lookup"><span data-stu-id="64d57-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="64d57-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="64d57-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="64d57-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64d57-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="64d57-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="64d57-204">System-Only</span></span>            | <span data-ttu-id="64d57-205">True</span><span class="sxs-lookup"><span data-stu-id="64d57-205">True</span></span>                                                               |
| <span data-ttu-id="64d57-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="64d57-206">Is-Single-Valued</span></span>       | <span data-ttu-id="64d57-207">False</span><span class="sxs-lookup"><span data-stu-id="64d57-207">False</span></span>                                                              |
| <span data-ttu-id="64d57-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="64d57-208">Is Indexed</span></span>             | <span data-ttu-id="64d57-209">False</span><span class="sxs-lookup"><span data-stu-id="64d57-209">False</span></span>                                                              |
| <span data-ttu-id="64d57-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="64d57-210">In Global Catalog</span></span>      | <span data-ttu-id="64d57-211">False</span><span class="sxs-lookup"><span data-stu-id="64d57-211">False</span></span>                                                              |
| <span data-ttu-id="64d57-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="64d57-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="64d57-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="64d57-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="64d57-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64d57-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="64d57-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64d57-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="64d57-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64d57-216">Search-Flags</span></span>           | <span data-ttu-id="64d57-217">0x00000008</span><span class="sxs-lookup"><span data-stu-id="64d57-217">0x00000008</span></span>                                                         |
| <span data-ttu-id="64d57-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64d57-218">System-Flags</span></span>           | <span data-ttu-id="64d57-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64d57-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="64d57-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="64d57-220">Classes used in</span></span>        | [<span data-ttu-id="64d57-221">**Infraestructura: actualizar**</span><span class="sxs-lookup"><span data-stu-id="64d57-221">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="64d57-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="64d57-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="64d57-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="64d57-223">Entry</span></span> | <span data-ttu-id="64d57-224">Value</span><span class="sxs-lookup"><span data-stu-id="64d57-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="64d57-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="64d57-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="64d57-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64d57-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="64d57-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="64d57-227">System-Only</span></span>            | <span data-ttu-id="64d57-228">True</span><span class="sxs-lookup"><span data-stu-id="64d57-228">True</span></span>                                                               |
| <span data-ttu-id="64d57-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="64d57-229">Is-Single-Valued</span></span>       | <span data-ttu-id="64d57-230">False</span><span class="sxs-lookup"><span data-stu-id="64d57-230">False</span></span>                                                              |
| <span data-ttu-id="64d57-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="64d57-231">Is Indexed</span></span>             | <span data-ttu-id="64d57-232">False</span><span class="sxs-lookup"><span data-stu-id="64d57-232">False</span></span>                                                              |
| <span data-ttu-id="64d57-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="64d57-233">In Global Catalog</span></span>      | <span data-ttu-id="64d57-234">False</span><span class="sxs-lookup"><span data-stu-id="64d57-234">False</span></span>                                                              |
| <span data-ttu-id="64d57-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="64d57-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="64d57-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="64d57-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="64d57-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64d57-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="64d57-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64d57-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="64d57-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64d57-239">Search-Flags</span></span>           | <span data-ttu-id="64d57-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="64d57-240">0x00000008</span></span>                                                         |
| <span data-ttu-id="64d57-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64d57-241">System-Flags</span></span>           | <span data-ttu-id="64d57-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64d57-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="64d57-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="64d57-243">Classes used in</span></span>        | [<span data-ttu-id="64d57-244">**Infraestructura: actualizar**</span><span class="sxs-lookup"><span data-stu-id="64d57-244">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="64d57-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="64d57-245">Windows Server 2012</span></span>



| <span data-ttu-id="64d57-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="64d57-246">Entry</span></span> | <span data-ttu-id="64d57-247">Value</span><span class="sxs-lookup"><span data-stu-id="64d57-247">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="64d57-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="64d57-248">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="64d57-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64d57-249">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="64d57-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="64d57-250">System-Only</span></span>            | <span data-ttu-id="64d57-251">True</span><span class="sxs-lookup"><span data-stu-id="64d57-251">True</span></span>                                                               |
| <span data-ttu-id="64d57-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="64d57-252">Is-Single-Valued</span></span>       | <span data-ttu-id="64d57-253">False</span><span class="sxs-lookup"><span data-stu-id="64d57-253">False</span></span>                                                              |
| <span data-ttu-id="64d57-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="64d57-254">Is Indexed</span></span>             | <span data-ttu-id="64d57-255">False</span><span class="sxs-lookup"><span data-stu-id="64d57-255">False</span></span>                                                              |
| <span data-ttu-id="64d57-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="64d57-256">In Global Catalog</span></span>      | <span data-ttu-id="64d57-257">False</span><span class="sxs-lookup"><span data-stu-id="64d57-257">False</span></span>                                                              |
| <span data-ttu-id="64d57-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="64d57-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="64d57-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="64d57-259">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="64d57-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64d57-260">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="64d57-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64d57-261">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="64d57-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64d57-262">Search-Flags</span></span>           | <span data-ttu-id="64d57-263">0x00000008</span><span class="sxs-lookup"><span data-stu-id="64d57-263">0x00000008</span></span>                                                         |
| <span data-ttu-id="64d57-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64d57-264">System-Flags</span></span>           | <span data-ttu-id="64d57-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64d57-265">0x00000010</span></span>                                                         |
| <span data-ttu-id="64d57-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="64d57-266">Classes used in</span></span>        | [<span data-ttu-id="64d57-267">**Infraestructura: actualizar**</span><span class="sxs-lookup"><span data-stu-id="64d57-267">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



 

 





