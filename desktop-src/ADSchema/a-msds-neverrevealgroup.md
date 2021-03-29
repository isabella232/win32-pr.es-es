---
title: atributo MS-DS-Never-Reveal-Group
description: Se usa con RODC para definir qué usuarios, equipos y grupos no pueden almacenar en caché sus contraseñas en un RODC.
ms.assetid: 203a660b-503e-4cf1-a796-eac024629b3e
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de grupo MS-DS-Never-Reveal
- Esquema de AD de atributo msDS-NeverRevealGroup
topic_type:
- apiref
api_name:
- ms-DS-Never-Reveal-Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1308fb1bc0818601a037e66b764e607c0a32532
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658866"
---
# <a name="ms-ds-never-reveal-group-attribute"></a><span data-ttu-id="e6c5a-105">atributo MS-DS-Never-Reveal-Group</span><span class="sxs-lookup"><span data-stu-id="e6c5a-105">ms-DS-Never-Reveal-Group attribute</span></span>

<span data-ttu-id="e6c5a-106">Se usa con RODC para definir qué usuarios, equipos y grupos no pueden almacenar en caché sus contraseñas en un RODC.</span><span class="sxs-lookup"><span data-stu-id="e6c5a-106">Used with RODCs to define which users, computers, and groups are not allowed to have their passwords cached on an RODC.</span></span>



| <span data-ttu-id="e6c5a-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6c5a-107">Entry</span></span> | <span data-ttu-id="e6c5a-108">Value</span><span class="sxs-lookup"><span data-stu-id="e6c5a-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="e6c5a-109">CN</span><span class="sxs-lookup"><span data-stu-id="e6c5a-109">CN</span></span>                | <span data-ttu-id="e6c5a-110">MS-DS-Never-Reveal-Group</span><span class="sxs-lookup"><span data-stu-id="e6c5a-110">ms-DS-Never-Reveal-Group</span></span>                |
| <span data-ttu-id="e6c5a-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="e6c5a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e6c5a-112">msDS-NeverRevealGroup</span><span class="sxs-lookup"><span data-stu-id="e6c5a-112">msDS-NeverRevealGroup</span></span>                   |
| <span data-ttu-id="e6c5a-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="e6c5a-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="e6c5a-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="e6c5a-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="e6c5a-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="e6c5a-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="e6c5a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e6c5a-116">Attribute-Id</span></span>      | <span data-ttu-id="e6c5a-117">1.2.840.113556.1.4.1926</span><span class="sxs-lookup"><span data-stu-id="e6c5a-117">1.2.840.113556.1.4.1926</span></span>                 |
| <span data-ttu-id="e6c5a-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e6c5a-118">System-Id-Guid</span></span>    | <span data-ttu-id="e6c5a-119">15585999-fd49-4d66-B25D-eeb96aba8174</span><span class="sxs-lookup"><span data-stu-id="e6c5a-119">15585999-fd49-4d66-b25d-eeb96aba8174</span></span>    |
| <span data-ttu-id="e6c5a-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6c5a-120">Syntax</span></span>            | [<span data-ttu-id="e6c5a-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="e6c5a-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="e6c5a-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="e6c5a-122">Implementations</span></span>

-   [<span data-ttu-id="e6c5a-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e6c5a-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e6c5a-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e6c5a-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e6c5a-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e6c5a-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="e6c5a-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6c5a-126">Windows Server 2008</span></span>



| <span data-ttu-id="e6c5a-127">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6c5a-127">Entry</span></span> | <span data-ttu-id="e6c5a-128">Value</span><span class="sxs-lookup"><span data-stu-id="e6c5a-128">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c5a-129">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e6c5a-129">Link-Id</span></span>                | <span data-ttu-id="e6c5a-130">2106</span><span class="sxs-lookup"><span data-stu-id="e6c5a-130">2106</span></span>                                                                               |
| <span data-ttu-id="e6c5a-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6c5a-131">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="e6c5a-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6c5a-132">System-Only</span></span>            | <span data-ttu-id="e6c5a-133">False</span><span class="sxs-lookup"><span data-stu-id="e6c5a-133">False</span></span>                                                                              |
| <span data-ttu-id="e6c5a-134">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e6c5a-134">Is-Single-Valued</span></span>       | <span data-ttu-id="e6c5a-135">False</span><span class="sxs-lookup"><span data-stu-id="e6c5a-135">False</span></span>                                                                              |
| <span data-ttu-id="e6c5a-136">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e6c5a-136">Is Indexed</span></span>             | <span data-ttu-id="e6c5a-137">False</span><span class="sxs-lookup"><span data-stu-id="e6c5a-137">False</span></span>                                                                              |
| <span data-ttu-id="e6c5a-138">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e6c5a-138">In Global Catalog</span></span>      | <span data-ttu-id="e6c5a-139">False</span><span class="sxs-lookup"><span data-stu-id="e6c5a-139">False</span></span>                                                                              |
| <span data-ttu-id="e6c5a-140">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e6c5a-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6c5a-141">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6c5a-141">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="e6c5a-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6c5a-142">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="e6c5a-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6c5a-143">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="e6c5a-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6c5a-144">Search-Flags</span></span>           | <span data-ttu-id="e6c5a-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6c5a-145">0x00000000</span></span>                                                                         |
| <span data-ttu-id="e6c5a-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6c5a-146">System-Flags</span></span>           | <span data-ttu-id="e6c5a-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6c5a-147">0x00000010</span></span>                                                                         |
| <span data-ttu-id="e6c5a-148">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e6c5a-148">Classes used in</span></span>        | [<span data-ttu-id="e6c5a-149">**Computer**</span><span class="sxs-lookup"><span data-stu-id="e6c5a-149">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="e6c5a-150">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="e6c5a-150">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e6c5a-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e6c5a-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e6c5a-152">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6c5a-152">Entry</span></span> | <span data-ttu-id="e6c5a-153">Value</span><span class="sxs-lookup"><span data-stu-id="e6c5a-153">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c5a-154">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e6c5a-154">Link-Id</span></span>                | <span data-ttu-id="e6c5a-155">2106</span><span class="sxs-lookup"><span data-stu-id="e6c5a-155">2106</span></span>                                                                               |
| <span data-ttu-id="e6c5a-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6c5a-156">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="e6c5a-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6c5a-157">System-Only</span></span>            | <span data-ttu-id="e6c5a-158">False</span><span class="sxs-lookup"><span data-stu-id="e6c5a-158">False</span></span>                                                                              |
| <span data-ttu-id="e6c5a-159">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e6c5a-159">Is-Single-Valued</span></span>       | <span data-ttu-id="e6c5a-160">False</span><span class="sxs-lookup"><span data-stu-id="e6c5a-160">False</span></span>                                                                              |
| <span data-ttu-id="e6c5a-161">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e6c5a-161">Is Indexed</span></span>             | <span data-ttu-id="e6c5a-162">False</span><span class="sxs-lookup"><span data-stu-id="e6c5a-162">False</span></span>                                                                              |
| <span data-ttu-id="e6c5a-163">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e6c5a-163">In Global Catalog</span></span>      | <span data-ttu-id="e6c5a-164">False</span><span class="sxs-lookup"><span data-stu-id="e6c5a-164">False</span></span>                                                                              |
| <span data-ttu-id="e6c5a-165">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e6c5a-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6c5a-166">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6c5a-166">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="e6c5a-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6c5a-167">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="e6c5a-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6c5a-168">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="e6c5a-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6c5a-169">Search-Flags</span></span>           | <span data-ttu-id="e6c5a-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6c5a-170">0x00000000</span></span>                                                                         |
| <span data-ttu-id="e6c5a-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6c5a-171">System-Flags</span></span>           | <span data-ttu-id="e6c5a-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6c5a-172">0x00000010</span></span>                                                                         |
| <span data-ttu-id="e6c5a-173">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e6c5a-173">Classes used in</span></span>        | [<span data-ttu-id="e6c5a-174">**Computer**</span><span class="sxs-lookup"><span data-stu-id="e6c5a-174">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="e6c5a-175">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="e6c5a-175">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e6c5a-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e6c5a-176">Windows Server 2012</span></span>



| <span data-ttu-id="e6c5a-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6c5a-177">Entry</span></span> | <span data-ttu-id="e6c5a-178">Value</span><span class="sxs-lookup"><span data-stu-id="e6c5a-178">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c5a-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e6c5a-179">Link-Id</span></span>                | <span data-ttu-id="e6c5a-180">2106</span><span class="sxs-lookup"><span data-stu-id="e6c5a-180">2106</span></span>                                                                               |
| <span data-ttu-id="e6c5a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6c5a-181">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="e6c5a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6c5a-182">System-Only</span></span>            | <span data-ttu-id="e6c5a-183">False</span><span class="sxs-lookup"><span data-stu-id="e6c5a-183">False</span></span>                                                                              |
| <span data-ttu-id="e6c5a-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e6c5a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e6c5a-185">False</span><span class="sxs-lookup"><span data-stu-id="e6c5a-185">False</span></span>                                                                              |
| <span data-ttu-id="e6c5a-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e6c5a-186">Is Indexed</span></span>             | <span data-ttu-id="e6c5a-187">False</span><span class="sxs-lookup"><span data-stu-id="e6c5a-187">False</span></span>                                                                              |
| <span data-ttu-id="e6c5a-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e6c5a-188">In Global Catalog</span></span>      | <span data-ttu-id="e6c5a-189">False</span><span class="sxs-lookup"><span data-stu-id="e6c5a-189">False</span></span>                                                                              |
| <span data-ttu-id="e6c5a-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e6c5a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6c5a-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6c5a-191">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="e6c5a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6c5a-192">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="e6c5a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6c5a-193">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="e6c5a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6c5a-194">Search-Flags</span></span>           | <span data-ttu-id="e6c5a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6c5a-195">0x00000000</span></span>                                                                         |
| <span data-ttu-id="e6c5a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6c5a-196">System-Flags</span></span>           | <span data-ttu-id="e6c5a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6c5a-197">0x00000010</span></span>                                                                         |
| <span data-ttu-id="e6c5a-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e6c5a-198">Classes used in</span></span>        | [<span data-ttu-id="e6c5a-199">**Computer**</span><span class="sxs-lookup"><span data-stu-id="e6c5a-199">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="e6c5a-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="e6c5a-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





