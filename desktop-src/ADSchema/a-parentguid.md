---
title: Atributo primario-GUID
description: Se trata de un atributo construido, inventado para admitir el control DirSync. Este atributo contiene el objectGuid del elemento primario de un objeto al replicar la creación, el cambio de nombre o el desplazamiento de un objeto.
ms.assetid: caf2491b-c0bf-4ea1-80ec-d44cf9307551
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo primario-GUID
- parentGUID esquema de AD de atributos
topic_type:
- apiref
api_name:
- Parent-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b01faf958f4add9c7788d630321d7c225f5026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906134"
---
# <a name="parent-guid-attribute"></a><span data-ttu-id="b5e7f-106">Atributo primario-GUID</span><span class="sxs-lookup"><span data-stu-id="b5e7f-106">Parent-GUID attribute</span></span>

<span data-ttu-id="b5e7f-107">Se trata de un atributo construido, inventado para admitir el control DirSync.</span><span class="sxs-lookup"><span data-stu-id="b5e7f-107">This is a constructed attribute, invented to support the DirSync control.</span></span> <span data-ttu-id="b5e7f-108">Este atributo contiene el objectGuid del elemento primario de un objeto al replicar la creación, el cambio de nombre o el desplazamiento de un objeto.</span><span class="sxs-lookup"><span data-stu-id="b5e7f-108">This attribute holds the objectGuid of an object's parent when replicating an object's creation, rename, or move.</span></span>



| <span data-ttu-id="b5e7f-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="b5e7f-109">Entry</span></span> | <span data-ttu-id="b5e7f-110">Value</span><span class="sxs-lookup"><span data-stu-id="b5e7f-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b5e7f-111">CN</span><span class="sxs-lookup"><span data-stu-id="b5e7f-111">CN</span></span>                | <span data-ttu-id="b5e7f-112">Primario-GUID</span><span class="sxs-lookup"><span data-stu-id="b5e7f-112">Parent-GUID</span></span>                                           |
| <span data-ttu-id="b5e7f-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="b5e7f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b5e7f-114">parentGUID</span><span class="sxs-lookup"><span data-stu-id="b5e7f-114">parentGUID</span></span>                                            |
| <span data-ttu-id="b5e7f-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="b5e7f-115">Size</span></span>              | <span data-ttu-id="b5e7f-116">16 bytes</span><span class="sxs-lookup"><span data-stu-id="b5e7f-116">16 bytes</span></span>                                              |
| <span data-ttu-id="b5e7f-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="b5e7f-117">Update Privilege</span></span>  | <span data-ttu-id="b5e7f-118">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="b5e7f-118">This value is set by the system.</span></span>                      |
| <span data-ttu-id="b5e7f-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="b5e7f-119">Update Frequency</span></span>  | <span data-ttu-id="b5e7f-120">Durante la replicación</span><span class="sxs-lookup"><span data-stu-id="b5e7f-120">During replication</span></span>                                    |
| <span data-ttu-id="b5e7f-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b5e7f-121">Attribute-Id</span></span>      | <span data-ttu-id="b5e7f-122">1.2.840.113556.1.4.1224</span><span class="sxs-lookup"><span data-stu-id="b5e7f-122">1.2.840.113556.1.4.1224</span></span>                               |
| <span data-ttu-id="b5e7f-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b5e7f-123">System-Id-Guid</span></span>    | <span data-ttu-id="b5e7f-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="b5e7f-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span></span>                  |
| <span data-ttu-id="b5e7f-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5e7f-125">Syntax</span></span>            | [<span data-ttu-id="b5e7f-126">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="b5e7f-126">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="b5e7f-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="b5e7f-127">Implementations</span></span>

-   [<span data-ttu-id="b5e7f-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b5e7f-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b5e7f-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b5e7f-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b5e7f-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b5e7f-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b5e7f-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b5e7f-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b5e7f-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b5e7f-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b5e7f-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b5e7f-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b5e7f-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b5e7f-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b5e7f-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b5e7f-135">Windows 2000 Server</span></span>



| <span data-ttu-id="b5e7f-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="b5e7f-136">Entry</span></span> | <span data-ttu-id="b5e7f-137">Value</span><span class="sxs-lookup"><span data-stu-id="b5e7f-137">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b5e7f-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b5e7f-138">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b5e7f-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5e7f-139">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b5e7f-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5e7f-140">System-Only</span></span>            | <span data-ttu-id="b5e7f-141">True</span><span class="sxs-lookup"><span data-stu-id="b5e7f-141">True</span></span>         |
| <span data-ttu-id="b5e7f-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b5e7f-142">Is-Single-Valued</span></span>       | <span data-ttu-id="b5e7f-143">True</span><span class="sxs-lookup"><span data-stu-id="b5e7f-143">True</span></span>         |
| <span data-ttu-id="b5e7f-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b5e7f-144">Is Indexed</span></span>             | <span data-ttu-id="b5e7f-145">False</span><span class="sxs-lookup"><span data-stu-id="b5e7f-145">False</span></span>        |
| <span data-ttu-id="b5e7f-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b5e7f-146">In Global Catalog</span></span>      | <span data-ttu-id="b5e7f-147">False</span><span class="sxs-lookup"><span data-stu-id="b5e7f-147">False</span></span>        |
| <span data-ttu-id="b5e7f-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b5e7f-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5e7f-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b5e7f-149">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b5e7f-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5e7f-150">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b5e7f-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5e7f-151">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b5e7f-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5e7f-152">Search-Flags</span></span>           | <span data-ttu-id="b5e7f-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5e7f-153">0x00000000</span></span>   |
| <span data-ttu-id="b5e7f-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5e7f-154">System-Flags</span></span>           | <span data-ttu-id="b5e7f-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b5e7f-155">0x08000014</span></span>   |
| <span data-ttu-id="b5e7f-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b5e7f-156">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="b5e7f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b5e7f-157">Windows Server 2003</span></span>



| <span data-ttu-id="b5e7f-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="b5e7f-158">Entry</span></span> | <span data-ttu-id="b5e7f-159">Value</span><span class="sxs-lookup"><span data-stu-id="b5e7f-159">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b5e7f-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b5e7f-160">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b5e7f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5e7f-161">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b5e7f-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5e7f-162">System-Only</span></span>            | <span data-ttu-id="b5e7f-163">True</span><span class="sxs-lookup"><span data-stu-id="b5e7f-163">True</span></span>         |
| <span data-ttu-id="b5e7f-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b5e7f-164">Is-Single-Valued</span></span>       | <span data-ttu-id="b5e7f-165">True</span><span class="sxs-lookup"><span data-stu-id="b5e7f-165">True</span></span>         |
| <span data-ttu-id="b5e7f-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b5e7f-166">Is Indexed</span></span>             | <span data-ttu-id="b5e7f-167">False</span><span class="sxs-lookup"><span data-stu-id="b5e7f-167">False</span></span>        |
| <span data-ttu-id="b5e7f-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b5e7f-168">In Global Catalog</span></span>      | <span data-ttu-id="b5e7f-169">False</span><span class="sxs-lookup"><span data-stu-id="b5e7f-169">False</span></span>        |
| <span data-ttu-id="b5e7f-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b5e7f-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5e7f-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b5e7f-171">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b5e7f-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5e7f-172">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b5e7f-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5e7f-173">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b5e7f-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5e7f-174">Search-Flags</span></span>           | <span data-ttu-id="b5e7f-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5e7f-175">0x00000000</span></span>   |
| <span data-ttu-id="b5e7f-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5e7f-176">System-Flags</span></span>           | <span data-ttu-id="b5e7f-177">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b5e7f-177">0x08000014</span></span>   |
| <span data-ttu-id="b5e7f-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b5e7f-178">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="b5e7f-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="b5e7f-179">ADAM</span></span>



| <span data-ttu-id="b5e7f-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="b5e7f-180">Entry</span></span> | <span data-ttu-id="b5e7f-181">Value</span><span class="sxs-lookup"><span data-stu-id="b5e7f-181">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b5e7f-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b5e7f-182">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b5e7f-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5e7f-183">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b5e7f-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5e7f-184">System-Only</span></span>            | <span data-ttu-id="b5e7f-185">True</span><span class="sxs-lookup"><span data-stu-id="b5e7f-185">True</span></span>         |
| <span data-ttu-id="b5e7f-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b5e7f-186">Is-Single-Valued</span></span>       | <span data-ttu-id="b5e7f-187">True</span><span class="sxs-lookup"><span data-stu-id="b5e7f-187">True</span></span>         |
| <span data-ttu-id="b5e7f-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b5e7f-188">Is Indexed</span></span>             | <span data-ttu-id="b5e7f-189">False</span><span class="sxs-lookup"><span data-stu-id="b5e7f-189">False</span></span>        |
| <span data-ttu-id="b5e7f-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b5e7f-190">In Global Catalog</span></span>      | <span data-ttu-id="b5e7f-191">False</span><span class="sxs-lookup"><span data-stu-id="b5e7f-191">False</span></span>        |
| <span data-ttu-id="b5e7f-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b5e7f-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5e7f-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b5e7f-193">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b5e7f-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5e7f-194">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b5e7f-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5e7f-195">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b5e7f-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5e7f-196">Search-Flags</span></span>           | <span data-ttu-id="b5e7f-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5e7f-197">0x00000000</span></span>   |
| <span data-ttu-id="b5e7f-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5e7f-198">System-Flags</span></span>           | <span data-ttu-id="b5e7f-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b5e7f-199">0x08000014</span></span>   |
| <span data-ttu-id="b5e7f-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b5e7f-200">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b5e7f-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b5e7f-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b5e7f-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="b5e7f-202">Entry</span></span> | <span data-ttu-id="b5e7f-203">Value</span><span class="sxs-lookup"><span data-stu-id="b5e7f-203">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b5e7f-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b5e7f-204">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b5e7f-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5e7f-205">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b5e7f-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5e7f-206">System-Only</span></span>            | <span data-ttu-id="b5e7f-207">True</span><span class="sxs-lookup"><span data-stu-id="b5e7f-207">True</span></span>         |
| <span data-ttu-id="b5e7f-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b5e7f-208">Is-Single-Valued</span></span>       | <span data-ttu-id="b5e7f-209">True</span><span class="sxs-lookup"><span data-stu-id="b5e7f-209">True</span></span>         |
| <span data-ttu-id="b5e7f-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b5e7f-210">Is Indexed</span></span>             | <span data-ttu-id="b5e7f-211">False</span><span class="sxs-lookup"><span data-stu-id="b5e7f-211">False</span></span>        |
| <span data-ttu-id="b5e7f-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b5e7f-212">In Global Catalog</span></span>      | <span data-ttu-id="b5e7f-213">False</span><span class="sxs-lookup"><span data-stu-id="b5e7f-213">False</span></span>        |
| <span data-ttu-id="b5e7f-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b5e7f-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5e7f-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b5e7f-215">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b5e7f-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5e7f-216">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b5e7f-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5e7f-217">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b5e7f-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5e7f-218">Search-Flags</span></span>           | <span data-ttu-id="b5e7f-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5e7f-219">0x00000000</span></span>   |
| <span data-ttu-id="b5e7f-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5e7f-220">System-Flags</span></span>           | <span data-ttu-id="b5e7f-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b5e7f-221">0x08000014</span></span>   |
| <span data-ttu-id="b5e7f-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b5e7f-222">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="b5e7f-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5e7f-223">Windows Server 2008</span></span>



| <span data-ttu-id="b5e7f-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="b5e7f-224">Entry</span></span> | <span data-ttu-id="b5e7f-225">Value</span><span class="sxs-lookup"><span data-stu-id="b5e7f-225">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b5e7f-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b5e7f-226">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b5e7f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5e7f-227">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b5e7f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5e7f-228">System-Only</span></span>            | <span data-ttu-id="b5e7f-229">True</span><span class="sxs-lookup"><span data-stu-id="b5e7f-229">True</span></span>         |
| <span data-ttu-id="b5e7f-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b5e7f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b5e7f-231">True</span><span class="sxs-lookup"><span data-stu-id="b5e7f-231">True</span></span>         |
| <span data-ttu-id="b5e7f-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b5e7f-232">Is Indexed</span></span>             | <span data-ttu-id="b5e7f-233">False</span><span class="sxs-lookup"><span data-stu-id="b5e7f-233">False</span></span>        |
| <span data-ttu-id="b5e7f-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b5e7f-234">In Global Catalog</span></span>      | <span data-ttu-id="b5e7f-235">False</span><span class="sxs-lookup"><span data-stu-id="b5e7f-235">False</span></span>        |
| <span data-ttu-id="b5e7f-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b5e7f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5e7f-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b5e7f-237">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b5e7f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5e7f-238">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b5e7f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5e7f-239">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b5e7f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5e7f-240">Search-Flags</span></span>           | <span data-ttu-id="b5e7f-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5e7f-241">0x00000000</span></span>   |
| <span data-ttu-id="b5e7f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5e7f-242">System-Flags</span></span>           | <span data-ttu-id="b5e7f-243">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b5e7f-243">0x08000014</span></span>   |
| <span data-ttu-id="b5e7f-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b5e7f-244">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b5e7f-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b5e7f-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b5e7f-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="b5e7f-246">Entry</span></span> | <span data-ttu-id="b5e7f-247">Value</span><span class="sxs-lookup"><span data-stu-id="b5e7f-247">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b5e7f-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b5e7f-248">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b5e7f-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5e7f-249">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b5e7f-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5e7f-250">System-Only</span></span>            | <span data-ttu-id="b5e7f-251">True</span><span class="sxs-lookup"><span data-stu-id="b5e7f-251">True</span></span>         |
| <span data-ttu-id="b5e7f-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b5e7f-252">Is-Single-Valued</span></span>       | <span data-ttu-id="b5e7f-253">True</span><span class="sxs-lookup"><span data-stu-id="b5e7f-253">True</span></span>         |
| <span data-ttu-id="b5e7f-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b5e7f-254">Is Indexed</span></span>             | <span data-ttu-id="b5e7f-255">False</span><span class="sxs-lookup"><span data-stu-id="b5e7f-255">False</span></span>        |
| <span data-ttu-id="b5e7f-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b5e7f-256">In Global Catalog</span></span>      | <span data-ttu-id="b5e7f-257">False</span><span class="sxs-lookup"><span data-stu-id="b5e7f-257">False</span></span>        |
| <span data-ttu-id="b5e7f-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b5e7f-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5e7f-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b5e7f-259">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b5e7f-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5e7f-260">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b5e7f-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5e7f-261">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b5e7f-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5e7f-262">Search-Flags</span></span>           | <span data-ttu-id="b5e7f-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5e7f-263">0x00000000</span></span>   |
| <span data-ttu-id="b5e7f-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5e7f-264">System-Flags</span></span>           | <span data-ttu-id="b5e7f-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b5e7f-265">0x08000014</span></span>   |
| <span data-ttu-id="b5e7f-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b5e7f-266">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="b5e7f-267">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b5e7f-267">Windows Server 2012</span></span>



| <span data-ttu-id="b5e7f-268">Entrada</span><span class="sxs-lookup"><span data-stu-id="b5e7f-268">Entry</span></span> | <span data-ttu-id="b5e7f-269">Value</span><span class="sxs-lookup"><span data-stu-id="b5e7f-269">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b5e7f-270">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b5e7f-270">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b5e7f-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5e7f-271">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b5e7f-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5e7f-272">System-Only</span></span>            | <span data-ttu-id="b5e7f-273">True</span><span class="sxs-lookup"><span data-stu-id="b5e7f-273">True</span></span>         |
| <span data-ttu-id="b5e7f-274">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b5e7f-274">Is-Single-Valued</span></span>       | <span data-ttu-id="b5e7f-275">True</span><span class="sxs-lookup"><span data-stu-id="b5e7f-275">True</span></span>         |
| <span data-ttu-id="b5e7f-276">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b5e7f-276">Is Indexed</span></span>             | <span data-ttu-id="b5e7f-277">False</span><span class="sxs-lookup"><span data-stu-id="b5e7f-277">False</span></span>        |
| <span data-ttu-id="b5e7f-278">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b5e7f-278">In Global Catalog</span></span>      | <span data-ttu-id="b5e7f-279">False</span><span class="sxs-lookup"><span data-stu-id="b5e7f-279">False</span></span>        |
| <span data-ttu-id="b5e7f-280">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b5e7f-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5e7f-281">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b5e7f-281">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b5e7f-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5e7f-282">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b5e7f-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5e7f-283">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b5e7f-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5e7f-284">Search-Flags</span></span>           | <span data-ttu-id="b5e7f-285">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5e7f-285">0x00000000</span></span>   |
| <span data-ttu-id="b5e7f-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5e7f-286">System-Flags</span></span>           | <span data-ttu-id="b5e7f-287">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b5e7f-287">0x08000014</span></span>   |
| <span data-ttu-id="b5e7f-288">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b5e7f-288">Classes used in</span></span>        | \-           |



 

 




