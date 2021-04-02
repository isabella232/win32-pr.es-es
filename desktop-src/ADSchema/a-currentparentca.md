---
title: Atributo Current-Parent-CA
description: Referencia a las entidades de certificación que emitieron los certificados actuales para una entidad de certificación.
ms.assetid: 9b851a7f-4a69-46f2-b7e2-6ee0b2d8eec1
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo Current-Parent-CA
- currentParentCA esquema de AD de atributos
topic_type:
- apiref
api_name:
- Current-Parent-CA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b26be2ccda41d998ed2b2b2c5dcddb1fcd2dcb2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997310"
---
# <a name="current-parent-ca-attribute"></a><span data-ttu-id="0bb5e-105">Atributo Current-Parent-CA</span><span class="sxs-lookup"><span data-stu-id="0bb5e-105">Current-Parent-CA attribute</span></span>

<span data-ttu-id="0bb5e-106">Referencia a las entidades de certificación que emitieron los certificados actuales para una entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="0bb5e-106">Reference to the certification authorities that issued the current certificates for a certification authority.</span></span>



| <span data-ttu-id="0bb5e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="0bb5e-107">Entry</span></span> | <span data-ttu-id="0bb5e-108">Value</span><span class="sxs-lookup"><span data-stu-id="0bb5e-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="0bb5e-109">CN</span><span class="sxs-lookup"><span data-stu-id="0bb5e-109">CN</span></span>                | <span data-ttu-id="0bb5e-110">Actual-primario-CA</span><span class="sxs-lookup"><span data-stu-id="0bb5e-110">Current-Parent-CA</span></span>                       |
| <span data-ttu-id="0bb5e-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="0bb5e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0bb5e-112">currentParentCA</span><span class="sxs-lookup"><span data-stu-id="0bb5e-112">currentParentCA</span></span>                         |
| <span data-ttu-id="0bb5e-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="0bb5e-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="0bb5e-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="0bb5e-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="0bb5e-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="0bb5e-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="0bb5e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0bb5e-116">Attribute-Id</span></span>      | <span data-ttu-id="0bb5e-117">1.2.840.113556.1.4.696</span><span class="sxs-lookup"><span data-stu-id="0bb5e-117">1.2.840.113556.1.4.696</span></span>                  |
| <span data-ttu-id="0bb5e-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0bb5e-118">System-Id-Guid</span></span>    | <span data-ttu-id="0bb5e-119">963d273f-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="0bb5e-119">963d273f-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="0bb5e-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0bb5e-120">Syntax</span></span>            | [<span data-ttu-id="0bb5e-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="0bb5e-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="0bb5e-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="0bb5e-122">Implementations</span></span>

-   [<span data-ttu-id="0bb5e-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0bb5e-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0bb5e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0bb5e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0bb5e-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0bb5e-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0bb5e-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0bb5e-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0bb5e-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0bb5e-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0bb5e-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0bb5e-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0bb5e-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0bb5e-129">Windows 2000 Server</span></span>



| <span data-ttu-id="0bb5e-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="0bb5e-130">Entry</span></span> | <span data-ttu-id="0bb5e-131">Value</span><span class="sxs-lookup"><span data-stu-id="0bb5e-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="0bb5e-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0bb5e-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0bb5e-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bb5e-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0bb5e-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bb5e-134">System-Only</span></span>            | <span data-ttu-id="0bb5e-135">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-135">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0bb5e-136">Is-Single-Valued</span></span>       | <span data-ttu-id="0bb5e-137">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-137">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0bb5e-138">Is Indexed</span></span>             | <span data-ttu-id="0bb5e-139">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-139">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0bb5e-140">In Global Catalog</span></span>      | <span data-ttu-id="0bb5e-141">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-141">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0bb5e-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bb5e-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0bb5e-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="0bb5e-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bb5e-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="0bb5e-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bb5e-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="0bb5e-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bb5e-146">Search-Flags</span></span>           | <span data-ttu-id="0bb5e-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bb5e-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="0bb5e-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bb5e-148">System-Flags</span></span>           | <span data-ttu-id="0bb5e-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bb5e-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="0bb5e-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0bb5e-150">Classes used in</span></span>        | [<span data-ttu-id="0bb5e-151">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="0bb5e-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0bb5e-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0bb5e-152">Windows Server 2003</span></span>



| <span data-ttu-id="0bb5e-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="0bb5e-153">Entry</span></span> | <span data-ttu-id="0bb5e-154">Value</span><span class="sxs-lookup"><span data-stu-id="0bb5e-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="0bb5e-155">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0bb5e-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0bb5e-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bb5e-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0bb5e-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bb5e-157">System-Only</span></span>            | <span data-ttu-id="0bb5e-158">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-158">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-159">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0bb5e-159">Is-Single-Valued</span></span>       | <span data-ttu-id="0bb5e-160">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-160">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-161">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0bb5e-161">Is Indexed</span></span>             | <span data-ttu-id="0bb5e-162">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-162">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-163">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0bb5e-163">In Global Catalog</span></span>      | <span data-ttu-id="0bb5e-164">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-164">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-165">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0bb5e-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bb5e-166">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0bb5e-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="0bb5e-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bb5e-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="0bb5e-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bb5e-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="0bb5e-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bb5e-169">Search-Flags</span></span>           | <span data-ttu-id="0bb5e-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bb5e-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="0bb5e-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bb5e-171">System-Flags</span></span>           | <span data-ttu-id="0bb5e-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bb5e-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="0bb5e-173">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0bb5e-173">Classes used in</span></span>        | [<span data-ttu-id="0bb5e-174">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="0bb5e-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0bb5e-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0bb5e-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0bb5e-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="0bb5e-176">Entry</span></span> | <span data-ttu-id="0bb5e-177">Value</span><span class="sxs-lookup"><span data-stu-id="0bb5e-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="0bb5e-178">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0bb5e-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0bb5e-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bb5e-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0bb5e-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bb5e-180">System-Only</span></span>            | <span data-ttu-id="0bb5e-181">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-181">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-182">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0bb5e-182">Is-Single-Valued</span></span>       | <span data-ttu-id="0bb5e-183">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-183">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-184">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0bb5e-184">Is Indexed</span></span>             | <span data-ttu-id="0bb5e-185">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-185">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-186">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0bb5e-186">In Global Catalog</span></span>      | <span data-ttu-id="0bb5e-187">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-187">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-188">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0bb5e-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bb5e-189">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0bb5e-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="0bb5e-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bb5e-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="0bb5e-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bb5e-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="0bb5e-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bb5e-192">Search-Flags</span></span>           | <span data-ttu-id="0bb5e-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bb5e-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="0bb5e-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bb5e-194">System-Flags</span></span>           | <span data-ttu-id="0bb5e-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bb5e-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="0bb5e-196">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0bb5e-196">Classes used in</span></span>        | [<span data-ttu-id="0bb5e-197">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="0bb5e-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0bb5e-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0bb5e-198">Windows Server 2008</span></span>



| <span data-ttu-id="0bb5e-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="0bb5e-199">Entry</span></span> | <span data-ttu-id="0bb5e-200">Value</span><span class="sxs-lookup"><span data-stu-id="0bb5e-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="0bb5e-201">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0bb5e-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0bb5e-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bb5e-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0bb5e-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bb5e-203">System-Only</span></span>            | <span data-ttu-id="0bb5e-204">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-204">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-205">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0bb5e-205">Is-Single-Valued</span></span>       | <span data-ttu-id="0bb5e-206">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-206">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-207">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0bb5e-207">Is Indexed</span></span>             | <span data-ttu-id="0bb5e-208">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-208">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-209">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0bb5e-209">In Global Catalog</span></span>      | <span data-ttu-id="0bb5e-210">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-210">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-211">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0bb5e-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bb5e-212">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0bb5e-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="0bb5e-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bb5e-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="0bb5e-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bb5e-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="0bb5e-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bb5e-215">Search-Flags</span></span>           | <span data-ttu-id="0bb5e-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bb5e-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="0bb5e-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bb5e-217">System-Flags</span></span>           | <span data-ttu-id="0bb5e-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bb5e-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="0bb5e-219">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0bb5e-219">Classes used in</span></span>        | [<span data-ttu-id="0bb5e-220">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="0bb5e-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0bb5e-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0bb5e-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0bb5e-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="0bb5e-222">Entry</span></span> | <span data-ttu-id="0bb5e-223">Value</span><span class="sxs-lookup"><span data-stu-id="0bb5e-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="0bb5e-224">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0bb5e-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0bb5e-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bb5e-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0bb5e-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bb5e-226">System-Only</span></span>            | <span data-ttu-id="0bb5e-227">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-227">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-228">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0bb5e-228">Is-Single-Valued</span></span>       | <span data-ttu-id="0bb5e-229">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-229">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-230">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0bb5e-230">Is Indexed</span></span>             | <span data-ttu-id="0bb5e-231">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-231">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-232">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0bb5e-232">In Global Catalog</span></span>      | <span data-ttu-id="0bb5e-233">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-233">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-234">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0bb5e-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bb5e-235">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0bb5e-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="0bb5e-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bb5e-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="0bb5e-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bb5e-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="0bb5e-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bb5e-238">Search-Flags</span></span>           | <span data-ttu-id="0bb5e-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bb5e-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="0bb5e-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bb5e-240">System-Flags</span></span>           | <span data-ttu-id="0bb5e-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bb5e-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="0bb5e-242">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0bb5e-242">Classes used in</span></span>        | [<span data-ttu-id="0bb5e-243">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="0bb5e-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0bb5e-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0bb5e-244">Windows Server 2012</span></span>



| <span data-ttu-id="0bb5e-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="0bb5e-245">Entry</span></span> | <span data-ttu-id="0bb5e-246">Value</span><span class="sxs-lookup"><span data-stu-id="0bb5e-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="0bb5e-247">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0bb5e-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0bb5e-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bb5e-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0bb5e-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bb5e-249">System-Only</span></span>            | <span data-ttu-id="0bb5e-250">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-250">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-251">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0bb5e-251">Is-Single-Valued</span></span>       | <span data-ttu-id="0bb5e-252">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-252">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-253">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0bb5e-253">Is Indexed</span></span>             | <span data-ttu-id="0bb5e-254">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-254">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-255">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0bb5e-255">In Global Catalog</span></span>      | <span data-ttu-id="0bb5e-256">False</span><span class="sxs-lookup"><span data-stu-id="0bb5e-256">False</span></span>                                                                  |
| <span data-ttu-id="0bb5e-257">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0bb5e-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bb5e-258">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0bb5e-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="0bb5e-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bb5e-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="0bb5e-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bb5e-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="0bb5e-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bb5e-261">Search-Flags</span></span>           | <span data-ttu-id="0bb5e-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bb5e-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="0bb5e-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bb5e-263">System-Flags</span></span>           | <span data-ttu-id="0bb5e-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bb5e-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="0bb5e-265">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0bb5e-265">Classes used in</span></span>        | [<span data-ttu-id="0bb5e-266">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="0bb5e-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





