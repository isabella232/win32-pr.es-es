---
title: Atributo Can-upgrade-script
description: Este atributo almacena la lista de paquetes de aplicación que puede actualizar o que puede actualizar este paquete de aplicación.
ms.assetid: 95dea9c7-dbbd-42fb-ab32-6b89490aa5d6
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo Can-upgrade-script
- canUpgradeScript esquema de AD de atributos
topic_type:
- apiref
api_name:
- Can-Upgrade-Script
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305e5b90c45d124a8647dd5d3a0af9c4a2ca6c4f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659222"
---
# <a name="can-upgrade-script-attribute"></a><span data-ttu-id="0a53e-105">Atributo Can-upgrade-script</span><span class="sxs-lookup"><span data-stu-id="0a53e-105">Can-Upgrade-Script attribute</span></span>

<span data-ttu-id="0a53e-106">Este atributo almacena la lista de paquetes de aplicación que puede actualizar o que puede actualizar este paquete de aplicación.</span><span class="sxs-lookup"><span data-stu-id="0a53e-106">This attribute stores the list of application packages that can be upgraded by or which can upgrade this application package.</span></span>



| <span data-ttu-id="0a53e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="0a53e-107">Entry</span></span> | <span data-ttu-id="0a53e-108">Value</span><span class="sxs-lookup"><span data-stu-id="0a53e-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="0a53e-109">CN</span><span class="sxs-lookup"><span data-stu-id="0a53e-109">CN</span></span>                | <span data-ttu-id="0a53e-110">Script Can-upgrade</span><span class="sxs-lookup"><span data-stu-id="0a53e-110">Can-Upgrade-Script</span></span>                          |
| <span data-ttu-id="0a53e-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="0a53e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0a53e-112">canUpgradeScript</span><span class="sxs-lookup"><span data-stu-id="0a53e-112">canUpgradeScript</span></span>                            |
| <span data-ttu-id="0a53e-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="0a53e-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="0a53e-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="0a53e-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="0a53e-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="0a53e-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="0a53e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0a53e-116">Attribute-Id</span></span>      | <span data-ttu-id="0a53e-117">1.2.840.113556.1.4.815</span><span class="sxs-lookup"><span data-stu-id="0a53e-117">1.2.840.113556.1.4.815</span></span>                      |
| <span data-ttu-id="0a53e-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0a53e-118">System-Id-Guid</span></span>    | <span data-ttu-id="0a53e-119">d9e18314-8939-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="0a53e-119">d9e18314-8939-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="0a53e-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a53e-120">Syntax</span></span>            | [<span data-ttu-id="0a53e-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="0a53e-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="0a53e-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="0a53e-122">Implementations</span></span>

-   [<span data-ttu-id="0a53e-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0a53e-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0a53e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0a53e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0a53e-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0a53e-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0a53e-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0a53e-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0a53e-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0a53e-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0a53e-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0a53e-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0a53e-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0a53e-129">Windows 2000 Server</span></span>



| <span data-ttu-id="0a53e-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="0a53e-130">Entry</span></span> | <span data-ttu-id="0a53e-131">Value</span><span class="sxs-lookup"><span data-stu-id="0a53e-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="0a53e-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0a53e-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0a53e-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0a53e-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0a53e-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="0a53e-134">System-Only</span></span>            | <span data-ttu-id="0a53e-135">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-135">False</span></span>                                                            |
| <span data-ttu-id="0a53e-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0a53e-136">Is-Single-Valued</span></span>       | <span data-ttu-id="0a53e-137">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-137">False</span></span>                                                            |
| <span data-ttu-id="0a53e-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0a53e-138">Is Indexed</span></span>             | <span data-ttu-id="0a53e-139">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-139">False</span></span>                                                            |
| <span data-ttu-id="0a53e-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0a53e-140">In Global Catalog</span></span>      | <span data-ttu-id="0a53e-141">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-141">False</span></span>                                                            |
| <span data-ttu-id="0a53e-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0a53e-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="0a53e-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0a53e-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="0a53e-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0a53e-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="0a53e-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0a53e-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="0a53e-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0a53e-146">Search-Flags</span></span>           | <span data-ttu-id="0a53e-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0a53e-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="0a53e-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0a53e-148">System-Flags</span></span>           | <span data-ttu-id="0a53e-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a53e-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="0a53e-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0a53e-150">Classes used in</span></span>        | [<span data-ttu-id="0a53e-151">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="0a53e-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0a53e-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0a53e-152">Windows Server 2003</span></span>



| <span data-ttu-id="0a53e-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="0a53e-153">Entry</span></span> | <span data-ttu-id="0a53e-154">Value</span><span class="sxs-lookup"><span data-stu-id="0a53e-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="0a53e-155">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0a53e-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0a53e-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0a53e-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0a53e-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="0a53e-157">System-Only</span></span>            | <span data-ttu-id="0a53e-158">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-158">False</span></span>                                                            |
| <span data-ttu-id="0a53e-159">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0a53e-159">Is-Single-Valued</span></span>       | <span data-ttu-id="0a53e-160">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-160">False</span></span>                                                            |
| <span data-ttu-id="0a53e-161">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0a53e-161">Is Indexed</span></span>             | <span data-ttu-id="0a53e-162">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-162">False</span></span>                                                            |
| <span data-ttu-id="0a53e-163">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0a53e-163">In Global Catalog</span></span>      | <span data-ttu-id="0a53e-164">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-164">False</span></span>                                                            |
| <span data-ttu-id="0a53e-165">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0a53e-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="0a53e-166">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0a53e-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="0a53e-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0a53e-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="0a53e-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0a53e-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="0a53e-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0a53e-169">Search-Flags</span></span>           | <span data-ttu-id="0a53e-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0a53e-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="0a53e-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0a53e-171">System-Flags</span></span>           | <span data-ttu-id="0a53e-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a53e-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="0a53e-173">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0a53e-173">Classes used in</span></span>        | [<span data-ttu-id="0a53e-174">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="0a53e-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0a53e-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0a53e-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0a53e-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="0a53e-176">Entry</span></span> | <span data-ttu-id="0a53e-177">Value</span><span class="sxs-lookup"><span data-stu-id="0a53e-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="0a53e-178">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0a53e-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0a53e-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0a53e-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0a53e-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="0a53e-180">System-Only</span></span>            | <span data-ttu-id="0a53e-181">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-181">False</span></span>                                                            |
| <span data-ttu-id="0a53e-182">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0a53e-182">Is-Single-Valued</span></span>       | <span data-ttu-id="0a53e-183">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-183">False</span></span>                                                            |
| <span data-ttu-id="0a53e-184">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0a53e-184">Is Indexed</span></span>             | <span data-ttu-id="0a53e-185">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-185">False</span></span>                                                            |
| <span data-ttu-id="0a53e-186">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0a53e-186">In Global Catalog</span></span>      | <span data-ttu-id="0a53e-187">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-187">False</span></span>                                                            |
| <span data-ttu-id="0a53e-188">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0a53e-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="0a53e-189">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0a53e-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="0a53e-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0a53e-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="0a53e-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0a53e-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="0a53e-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0a53e-192">Search-Flags</span></span>           | <span data-ttu-id="0a53e-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0a53e-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="0a53e-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0a53e-194">System-Flags</span></span>           | <span data-ttu-id="0a53e-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a53e-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="0a53e-196">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0a53e-196">Classes used in</span></span>        | [<span data-ttu-id="0a53e-197">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="0a53e-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0a53e-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a53e-198">Windows Server 2008</span></span>



| <span data-ttu-id="0a53e-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="0a53e-199">Entry</span></span> | <span data-ttu-id="0a53e-200">Value</span><span class="sxs-lookup"><span data-stu-id="0a53e-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="0a53e-201">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0a53e-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0a53e-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0a53e-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0a53e-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="0a53e-203">System-Only</span></span>            | <span data-ttu-id="0a53e-204">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-204">False</span></span>                                                            |
| <span data-ttu-id="0a53e-205">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0a53e-205">Is-Single-Valued</span></span>       | <span data-ttu-id="0a53e-206">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-206">False</span></span>                                                            |
| <span data-ttu-id="0a53e-207">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0a53e-207">Is Indexed</span></span>             | <span data-ttu-id="0a53e-208">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-208">False</span></span>                                                            |
| <span data-ttu-id="0a53e-209">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0a53e-209">In Global Catalog</span></span>      | <span data-ttu-id="0a53e-210">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-210">False</span></span>                                                            |
| <span data-ttu-id="0a53e-211">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0a53e-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="0a53e-212">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0a53e-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="0a53e-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0a53e-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="0a53e-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0a53e-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="0a53e-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0a53e-215">Search-Flags</span></span>           | <span data-ttu-id="0a53e-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0a53e-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="0a53e-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0a53e-217">System-Flags</span></span>           | <span data-ttu-id="0a53e-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a53e-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="0a53e-219">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0a53e-219">Classes used in</span></span>        | [<span data-ttu-id="0a53e-220">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="0a53e-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0a53e-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0a53e-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0a53e-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="0a53e-222">Entry</span></span> | <span data-ttu-id="0a53e-223">Value</span><span class="sxs-lookup"><span data-stu-id="0a53e-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="0a53e-224">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0a53e-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0a53e-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0a53e-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0a53e-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="0a53e-226">System-Only</span></span>            | <span data-ttu-id="0a53e-227">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-227">False</span></span>                                                            |
| <span data-ttu-id="0a53e-228">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0a53e-228">Is-Single-Valued</span></span>       | <span data-ttu-id="0a53e-229">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-229">False</span></span>                                                            |
| <span data-ttu-id="0a53e-230">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0a53e-230">Is Indexed</span></span>             | <span data-ttu-id="0a53e-231">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-231">False</span></span>                                                            |
| <span data-ttu-id="0a53e-232">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0a53e-232">In Global Catalog</span></span>      | <span data-ttu-id="0a53e-233">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-233">False</span></span>                                                            |
| <span data-ttu-id="0a53e-234">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0a53e-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="0a53e-235">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0a53e-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="0a53e-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0a53e-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="0a53e-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0a53e-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="0a53e-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0a53e-238">Search-Flags</span></span>           | <span data-ttu-id="0a53e-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0a53e-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="0a53e-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0a53e-240">System-Flags</span></span>           | <span data-ttu-id="0a53e-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a53e-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="0a53e-242">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0a53e-242">Classes used in</span></span>        | [<span data-ttu-id="0a53e-243">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="0a53e-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0a53e-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0a53e-244">Windows Server 2012</span></span>



| <span data-ttu-id="0a53e-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="0a53e-245">Entry</span></span> | <span data-ttu-id="0a53e-246">Value</span><span class="sxs-lookup"><span data-stu-id="0a53e-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="0a53e-247">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0a53e-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0a53e-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0a53e-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0a53e-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="0a53e-249">System-Only</span></span>            | <span data-ttu-id="0a53e-250">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-250">False</span></span>                                                            |
| <span data-ttu-id="0a53e-251">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0a53e-251">Is-Single-Valued</span></span>       | <span data-ttu-id="0a53e-252">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-252">False</span></span>                                                            |
| <span data-ttu-id="0a53e-253">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0a53e-253">Is Indexed</span></span>             | <span data-ttu-id="0a53e-254">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-254">False</span></span>                                                            |
| <span data-ttu-id="0a53e-255">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0a53e-255">In Global Catalog</span></span>      | <span data-ttu-id="0a53e-256">False</span><span class="sxs-lookup"><span data-stu-id="0a53e-256">False</span></span>                                                            |
| <span data-ttu-id="0a53e-257">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0a53e-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="0a53e-258">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0a53e-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="0a53e-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0a53e-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="0a53e-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0a53e-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="0a53e-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0a53e-261">Search-Flags</span></span>           | <span data-ttu-id="0a53e-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0a53e-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="0a53e-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0a53e-263">System-Flags</span></span>           | <span data-ttu-id="0a53e-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a53e-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="0a53e-265">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0a53e-265">Classes used in</span></span>        | [<span data-ttu-id="0a53e-266">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="0a53e-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





