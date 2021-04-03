---
title: atributo MS-DS-AuthenticatedAt-DC
description: Vínculo hacia delante de MS-DS-AuthenticatedTo-Accountlist. Identifica el controlador de dominio al que se ha autenticado un usuario.
ms.assetid: 91d6f022-e48b-4e2a-9294-cbac3590760f
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-AuthenticatedAt-DC
- Esquema de AD de atributo msDS-AuthenticatedAtDC
topic_type:
- apiref
api_name:
- ms-DS-AuthenticatedAt-DC
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2f41be139f3676beb154a923552b4d794de6d3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997445"
---
# <a name="ms-ds-authenticatedat-dc-attribute"></a><span data-ttu-id="38373-106">atributo MS-DS-AuthenticatedAt-DC</span><span class="sxs-lookup"><span data-stu-id="38373-106">ms-DS-AuthenticatedAt-DC attribute</span></span>

<span data-ttu-id="38373-107">Vínculo hacia delante de [**MS-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md).</span><span class="sxs-lookup"><span data-stu-id="38373-107">Forward link for [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md).</span></span> <span data-ttu-id="38373-108">Identifica el controlador de dominio al que se ha autenticado un usuario.</span><span class="sxs-lookup"><span data-stu-id="38373-108">Identifies which DC a user has authenticated to.</span></span>



| <span data-ttu-id="38373-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="38373-109">Entry</span></span> | <span data-ttu-id="38373-110">Value</span><span class="sxs-lookup"><span data-stu-id="38373-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="38373-111">CN</span><span class="sxs-lookup"><span data-stu-id="38373-111">CN</span></span>                | <span data-ttu-id="38373-112">MS-DS-AuthenticatedAt-DC</span><span class="sxs-lookup"><span data-stu-id="38373-112">ms-DS-AuthenticatedAt-DC</span></span>                |
| <span data-ttu-id="38373-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="38373-113">Ldap-Display-Name</span></span> | <span data-ttu-id="38373-114">msDS-AuthenticatedAtDC</span><span class="sxs-lookup"><span data-stu-id="38373-114">msDS-AuthenticatedAtDC</span></span>                  |
| <span data-ttu-id="38373-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="38373-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="38373-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="38373-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="38373-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="38373-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="38373-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="38373-118">Attribute-Id</span></span>      | <span data-ttu-id="38373-119">1.2.840.113556.1.4.1958</span><span class="sxs-lookup"><span data-stu-id="38373-119">1.2.840.113556.1.4.1958</span></span>                 |
| <span data-ttu-id="38373-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="38373-120">System-Id-Guid</span></span>    | <span data-ttu-id="38373-121">3e1ee99c-6604-4489-89d9-84798a89515a</span><span class="sxs-lookup"><span data-stu-id="38373-121">3e1ee99c-6604-4489-89d9-84798a89515a</span></span>    |
| <span data-ttu-id="38373-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38373-122">Syntax</span></span>            | [<span data-ttu-id="38373-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="38373-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="38373-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="38373-124">Implementations</span></span>

-   [<span data-ttu-id="38373-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="38373-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="38373-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="38373-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="38373-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="38373-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="38373-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38373-128">Windows Server 2008</span></span>



| <span data-ttu-id="38373-129">Entrada</span><span class="sxs-lookup"><span data-stu-id="38373-129">Entry</span></span> | <span data-ttu-id="38373-130">Value</span><span class="sxs-lookup"><span data-stu-id="38373-130">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="38373-131">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38373-131">Link-Id</span></span>                | <span data-ttu-id="38373-132">2112</span><span class="sxs-lookup"><span data-stu-id="38373-132">2112</span></span>                                                                        |
| <span data-ttu-id="38373-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38373-133">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="38373-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="38373-134">System-Only</span></span>            | <span data-ttu-id="38373-135">False</span><span class="sxs-lookup"><span data-stu-id="38373-135">False</span></span>                                                                       |
| <span data-ttu-id="38373-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38373-136">Is-Single-Valued</span></span>       | <span data-ttu-id="38373-137">False</span><span class="sxs-lookup"><span data-stu-id="38373-137">False</span></span>                                                                       |
| <span data-ttu-id="38373-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38373-138">Is Indexed</span></span>             | <span data-ttu-id="38373-139">False</span><span class="sxs-lookup"><span data-stu-id="38373-139">False</span></span>                                                                       |
| <span data-ttu-id="38373-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38373-140">In Global Catalog</span></span>      | <span data-ttu-id="38373-141">False</span><span class="sxs-lookup"><span data-stu-id="38373-141">False</span></span>                                                                       |
| <span data-ttu-id="38373-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38373-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="38373-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38373-143">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="38373-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38373-144">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="38373-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38373-145">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="38373-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38373-146">Search-Flags</span></span>           | <span data-ttu-id="38373-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38373-147">0x00000000</span></span>                                                                  |
| <span data-ttu-id="38373-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38373-148">System-Flags</span></span>           | <span data-ttu-id="38373-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38373-149">0x00000010</span></span>                                                                  |
| <span data-ttu-id="38373-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38373-150">Classes used in</span></span>        | [<span data-ttu-id="38373-151">**Computer**</span><span class="sxs-lookup"><span data-stu-id="38373-151">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="38373-152">**User**</span><span class="sxs-lookup"><span data-stu-id="38373-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="38373-153">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="38373-153">Windows Server 2008 R2</span></span>



| <span data-ttu-id="38373-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="38373-154">Entry</span></span> | <span data-ttu-id="38373-155">Value</span><span class="sxs-lookup"><span data-stu-id="38373-155">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="38373-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38373-156">Link-Id</span></span>                | <span data-ttu-id="38373-157">2112</span><span class="sxs-lookup"><span data-stu-id="38373-157">2112</span></span>                                                                        |
| <span data-ttu-id="38373-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38373-158">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="38373-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="38373-159">System-Only</span></span>            | <span data-ttu-id="38373-160">False</span><span class="sxs-lookup"><span data-stu-id="38373-160">False</span></span>                                                                       |
| <span data-ttu-id="38373-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38373-161">Is-Single-Valued</span></span>       | <span data-ttu-id="38373-162">False</span><span class="sxs-lookup"><span data-stu-id="38373-162">False</span></span>                                                                       |
| <span data-ttu-id="38373-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38373-163">Is Indexed</span></span>             | <span data-ttu-id="38373-164">False</span><span class="sxs-lookup"><span data-stu-id="38373-164">False</span></span>                                                                       |
| <span data-ttu-id="38373-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38373-165">In Global Catalog</span></span>      | <span data-ttu-id="38373-166">False</span><span class="sxs-lookup"><span data-stu-id="38373-166">False</span></span>                                                                       |
| <span data-ttu-id="38373-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38373-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="38373-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38373-168">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="38373-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38373-169">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="38373-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38373-170">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="38373-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38373-171">Search-Flags</span></span>           | <span data-ttu-id="38373-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38373-172">0x00000000</span></span>                                                                  |
| <span data-ttu-id="38373-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38373-173">System-Flags</span></span>           | <span data-ttu-id="38373-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38373-174">0x00000010</span></span>                                                                  |
| <span data-ttu-id="38373-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38373-175">Classes used in</span></span>        | [<span data-ttu-id="38373-176">**Computer**</span><span class="sxs-lookup"><span data-stu-id="38373-176">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="38373-177">**User**</span><span class="sxs-lookup"><span data-stu-id="38373-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="38373-178">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38373-178">Windows Server 2012</span></span>



| <span data-ttu-id="38373-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="38373-179">Entry</span></span> | <span data-ttu-id="38373-180">Value</span><span class="sxs-lookup"><span data-stu-id="38373-180">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="38373-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38373-181">Link-Id</span></span>                | <span data-ttu-id="38373-182">2112</span><span class="sxs-lookup"><span data-stu-id="38373-182">2112</span></span>                                                                        |
| <span data-ttu-id="38373-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38373-183">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="38373-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="38373-184">System-Only</span></span>            | <span data-ttu-id="38373-185">False</span><span class="sxs-lookup"><span data-stu-id="38373-185">False</span></span>                                                                       |
| <span data-ttu-id="38373-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38373-186">Is-Single-Valued</span></span>       | <span data-ttu-id="38373-187">False</span><span class="sxs-lookup"><span data-stu-id="38373-187">False</span></span>                                                                       |
| <span data-ttu-id="38373-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38373-188">Is Indexed</span></span>             | <span data-ttu-id="38373-189">False</span><span class="sxs-lookup"><span data-stu-id="38373-189">False</span></span>                                                                       |
| <span data-ttu-id="38373-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38373-190">In Global Catalog</span></span>      | <span data-ttu-id="38373-191">False</span><span class="sxs-lookup"><span data-stu-id="38373-191">False</span></span>                                                                       |
| <span data-ttu-id="38373-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38373-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="38373-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38373-193">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="38373-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38373-194">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="38373-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38373-195">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="38373-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38373-196">Search-Flags</span></span>           | <span data-ttu-id="38373-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38373-197">0x00000000</span></span>                                                                  |
| <span data-ttu-id="38373-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38373-198">System-Flags</span></span>           | <span data-ttu-id="38373-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38373-199">0x00000010</span></span>                                                                  |
| <span data-ttu-id="38373-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38373-200">Classes used in</span></span>        | [<span data-ttu-id="38373-201">**Computer**</span><span class="sxs-lookup"><span data-stu-id="38373-201">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="38373-202">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="38373-202">**User**</span></span>](c-user.md)<br/> |



 

 





