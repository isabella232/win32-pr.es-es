---
title: Atributo Previous-Parent-CA
description: Referencia a las entidades de certificación que emitieron el último certificado expirado para una entidad de certificación.
ms.assetid: 9772d6cb-1105-426c-9982-473b4c1bf0d8
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos anteriores-primario-CA
- previousParentCA esquema de AD de atributos
topic_type:
- apiref
api_name:
- Previous-Parent-CA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a4c89652ef7ffffdc731614cfc57572b3edcde
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104079798"
---
# <a name="previous-parent-ca-attribute"></a><span data-ttu-id="93d4c-105">Atributo Previous-Parent-CA</span><span class="sxs-lookup"><span data-stu-id="93d4c-105">Previous-Parent-CA attribute</span></span>

<span data-ttu-id="93d4c-106">Referencia a las entidades de certificación que emitieron el último certificado expirado para una entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="93d4c-106">Reference to the certification authorities that issued the last expired certificate for a certification authority.</span></span>



| <span data-ttu-id="93d4c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="93d4c-107">Entry</span></span> | <span data-ttu-id="93d4c-108">Value</span><span class="sxs-lookup"><span data-stu-id="93d4c-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="93d4c-109">CN</span><span class="sxs-lookup"><span data-stu-id="93d4c-109">CN</span></span>                | <span data-ttu-id="93d4c-110">Anterior-primario-CA</span><span class="sxs-lookup"><span data-stu-id="93d4c-110">Previous-Parent-CA</span></span>                      |
| <span data-ttu-id="93d4c-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="93d4c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="93d4c-112">previousParentCA</span><span class="sxs-lookup"><span data-stu-id="93d4c-112">previousParentCA</span></span>                        |
| <span data-ttu-id="93d4c-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="93d4c-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="93d4c-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="93d4c-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="93d4c-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="93d4c-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="93d4c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="93d4c-116">Attribute-Id</span></span>      | <span data-ttu-id="93d4c-117">1.2.840.113556.1.4.694</span><span class="sxs-lookup"><span data-stu-id="93d4c-117">1.2.840.113556.1.4.694</span></span>                  |
| <span data-ttu-id="93d4c-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="93d4c-118">System-Id-Guid</span></span>    | <span data-ttu-id="93d4c-119">963d273d-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="93d4c-119">963d273d-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="93d4c-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93d4c-120">Syntax</span></span>            | [<span data-ttu-id="93d4c-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="93d4c-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="93d4c-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="93d4c-122">Implementations</span></span>

-   [<span data-ttu-id="93d4c-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="93d4c-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="93d4c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="93d4c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="93d4c-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="93d4c-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="93d4c-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="93d4c-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="93d4c-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="93d4c-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="93d4c-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="93d4c-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="93d4c-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="93d4c-129">Windows 2000 Server</span></span>



| <span data-ttu-id="93d4c-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="93d4c-130">Entry</span></span> | <span data-ttu-id="93d4c-131">Value</span><span class="sxs-lookup"><span data-stu-id="93d4c-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="93d4c-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="93d4c-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="93d4c-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93d4c-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="93d4c-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="93d4c-134">System-Only</span></span>            | <span data-ttu-id="93d4c-135">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-135">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="93d4c-136">Is-Single-Valued</span></span>       | <span data-ttu-id="93d4c-137">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-137">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="93d4c-138">Is Indexed</span></span>             | <span data-ttu-id="93d4c-139">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-139">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="93d4c-140">In Global Catalog</span></span>      | <span data-ttu-id="93d4c-141">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-141">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="93d4c-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="93d4c-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="93d4c-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="93d4c-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93d4c-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="93d4c-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93d4c-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="93d4c-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93d4c-146">Search-Flags</span></span>           | <span data-ttu-id="93d4c-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93d4c-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="93d4c-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93d4c-148">System-Flags</span></span>           | <span data-ttu-id="93d4c-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93d4c-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="93d4c-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="93d4c-150">Classes used in</span></span>        | [<span data-ttu-id="93d4c-151">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="93d4c-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="93d4c-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="93d4c-152">Windows Server 2003</span></span>



| <span data-ttu-id="93d4c-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="93d4c-153">Entry</span></span> | <span data-ttu-id="93d4c-154">Value</span><span class="sxs-lookup"><span data-stu-id="93d4c-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="93d4c-155">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="93d4c-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="93d4c-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93d4c-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="93d4c-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="93d4c-157">System-Only</span></span>            | <span data-ttu-id="93d4c-158">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-158">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-159">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="93d4c-159">Is-Single-Valued</span></span>       | <span data-ttu-id="93d4c-160">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-160">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-161">Está indexado</span><span class="sxs-lookup"><span data-stu-id="93d4c-161">Is Indexed</span></span>             | <span data-ttu-id="93d4c-162">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-162">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-163">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="93d4c-163">In Global Catalog</span></span>      | <span data-ttu-id="93d4c-164">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-164">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-165">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="93d4c-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="93d4c-166">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="93d4c-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="93d4c-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93d4c-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="93d4c-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93d4c-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="93d4c-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93d4c-169">Search-Flags</span></span>           | <span data-ttu-id="93d4c-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93d4c-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="93d4c-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93d4c-171">System-Flags</span></span>           | <span data-ttu-id="93d4c-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93d4c-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="93d4c-173">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="93d4c-173">Classes used in</span></span>        | [<span data-ttu-id="93d4c-174">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="93d4c-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="93d4c-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="93d4c-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="93d4c-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="93d4c-176">Entry</span></span> | <span data-ttu-id="93d4c-177">Value</span><span class="sxs-lookup"><span data-stu-id="93d4c-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="93d4c-178">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="93d4c-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="93d4c-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93d4c-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="93d4c-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="93d4c-180">System-Only</span></span>            | <span data-ttu-id="93d4c-181">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-181">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-182">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="93d4c-182">Is-Single-Valued</span></span>       | <span data-ttu-id="93d4c-183">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-183">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-184">Está indexado</span><span class="sxs-lookup"><span data-stu-id="93d4c-184">Is Indexed</span></span>             | <span data-ttu-id="93d4c-185">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-185">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-186">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="93d4c-186">In Global Catalog</span></span>      | <span data-ttu-id="93d4c-187">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-187">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-188">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="93d4c-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="93d4c-189">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="93d4c-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="93d4c-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93d4c-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="93d4c-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93d4c-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="93d4c-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93d4c-192">Search-Flags</span></span>           | <span data-ttu-id="93d4c-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93d4c-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="93d4c-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93d4c-194">System-Flags</span></span>           | <span data-ttu-id="93d4c-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93d4c-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="93d4c-196">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="93d4c-196">Classes used in</span></span>        | [<span data-ttu-id="93d4c-197">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="93d4c-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="93d4c-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93d4c-198">Windows Server 2008</span></span>



| <span data-ttu-id="93d4c-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="93d4c-199">Entry</span></span> | <span data-ttu-id="93d4c-200">Value</span><span class="sxs-lookup"><span data-stu-id="93d4c-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="93d4c-201">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="93d4c-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="93d4c-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93d4c-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="93d4c-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="93d4c-203">System-Only</span></span>            | <span data-ttu-id="93d4c-204">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-204">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-205">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="93d4c-205">Is-Single-Valued</span></span>       | <span data-ttu-id="93d4c-206">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-206">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-207">Está indexado</span><span class="sxs-lookup"><span data-stu-id="93d4c-207">Is Indexed</span></span>             | <span data-ttu-id="93d4c-208">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-208">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-209">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="93d4c-209">In Global Catalog</span></span>      | <span data-ttu-id="93d4c-210">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-210">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-211">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="93d4c-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="93d4c-212">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="93d4c-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="93d4c-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93d4c-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="93d4c-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93d4c-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="93d4c-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93d4c-215">Search-Flags</span></span>           | <span data-ttu-id="93d4c-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93d4c-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="93d4c-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93d4c-217">System-Flags</span></span>           | <span data-ttu-id="93d4c-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93d4c-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="93d4c-219">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="93d4c-219">Classes used in</span></span>        | [<span data-ttu-id="93d4c-220">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="93d4c-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="93d4c-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="93d4c-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="93d4c-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="93d4c-222">Entry</span></span> | <span data-ttu-id="93d4c-223">Value</span><span class="sxs-lookup"><span data-stu-id="93d4c-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="93d4c-224">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="93d4c-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="93d4c-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93d4c-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="93d4c-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="93d4c-226">System-Only</span></span>            | <span data-ttu-id="93d4c-227">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-227">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-228">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="93d4c-228">Is-Single-Valued</span></span>       | <span data-ttu-id="93d4c-229">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-229">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-230">Está indexado</span><span class="sxs-lookup"><span data-stu-id="93d4c-230">Is Indexed</span></span>             | <span data-ttu-id="93d4c-231">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-231">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-232">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="93d4c-232">In Global Catalog</span></span>      | <span data-ttu-id="93d4c-233">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-233">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-234">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="93d4c-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="93d4c-235">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="93d4c-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="93d4c-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93d4c-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="93d4c-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93d4c-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="93d4c-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93d4c-238">Search-Flags</span></span>           | <span data-ttu-id="93d4c-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93d4c-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="93d4c-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93d4c-240">System-Flags</span></span>           | <span data-ttu-id="93d4c-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93d4c-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="93d4c-242">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="93d4c-242">Classes used in</span></span>        | [<span data-ttu-id="93d4c-243">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="93d4c-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="93d4c-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="93d4c-244">Windows Server 2012</span></span>



| <span data-ttu-id="93d4c-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="93d4c-245">Entry</span></span> | <span data-ttu-id="93d4c-246">Value</span><span class="sxs-lookup"><span data-stu-id="93d4c-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="93d4c-247">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="93d4c-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="93d4c-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93d4c-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="93d4c-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="93d4c-249">System-Only</span></span>            | <span data-ttu-id="93d4c-250">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-250">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-251">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="93d4c-251">Is-Single-Valued</span></span>       | <span data-ttu-id="93d4c-252">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-252">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-253">Está indexado</span><span class="sxs-lookup"><span data-stu-id="93d4c-253">Is Indexed</span></span>             | <span data-ttu-id="93d4c-254">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-254">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-255">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="93d4c-255">In Global Catalog</span></span>      | <span data-ttu-id="93d4c-256">False</span><span class="sxs-lookup"><span data-stu-id="93d4c-256">False</span></span>                                                                  |
| <span data-ttu-id="93d4c-257">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="93d4c-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="93d4c-258">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="93d4c-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="93d4c-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93d4c-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="93d4c-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93d4c-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="93d4c-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93d4c-261">Search-Flags</span></span>           | <span data-ttu-id="93d4c-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93d4c-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="93d4c-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93d4c-263">System-Flags</span></span>           | <span data-ttu-id="93d4c-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93d4c-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="93d4c-265">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="93d4c-265">Classes used in</span></span>        | [<span data-ttu-id="93d4c-266">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="93d4c-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





