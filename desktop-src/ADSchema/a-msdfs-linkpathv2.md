---
title: atributo MS-DFS-Link-path-V2
description: Ruta de acceso de vínculo DFS relativa al recurso compartido de destino raíz DFS (es decir, sin los componentes servidor/dominio y nombre del espacio de nombres DFS). Utilice barras diagonales (/) en lugar de barras diagonales inversas ( \) , de modo que las búsquedas LDAP se puedan realizar sin tener que usar escapes.
ms.assetid: 98fd6e99-0d7e-4ffa-b8ec-d26ca03ffead
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DFS-Link-path-V2
- msDFS-LinkPathv2 atributo AD Schema
topic_type:
- apiref
api_name:
- ms-DFS-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 892cee6a5e6f423a0ed750858e19e1accccbe45f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151835"
---
# <a name="ms-dfs-link-path-v2-attribute"></a><span data-ttu-id="160f2-106">atributo MS-DFS-Link-path-V2</span><span class="sxs-lookup"><span data-stu-id="160f2-106">ms-DFS-Link-Path-v2 attribute</span></span>

<span data-ttu-id="160f2-107">Ruta de acceso de vínculo DFS relativa al recurso compartido de destino raíz DFS (es decir, sin los componentes servidor/dominio y nombre del espacio de nombres DFS).</span><span class="sxs-lookup"><span data-stu-id="160f2-107">DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="160f2-108">Utilice barras diagonales (/) en lugar de barras diagonales inversas ( \) , de modo que las búsquedas LDAP se puedan realizar sin tener que usar escapes.</span><span class="sxs-lookup"><span data-stu-id="160f2-108">Use forward slashes (/) instead of backslashes (\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="160f2-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="160f2-109">Entry</span></span> | <span data-ttu-id="160f2-110">Value</span><span class="sxs-lookup"><span data-stu-id="160f2-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="160f2-111">CN</span><span class="sxs-lookup"><span data-stu-id="160f2-111">CN</span></span>                | <span data-ttu-id="160f2-112">MS-DFS-Link-path-V2</span><span class="sxs-lookup"><span data-stu-id="160f2-112">ms-DFS-Link-Path-v2</span></span>                         |
| <span data-ttu-id="160f2-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="160f2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="160f2-114">msDFS-LinkPathv2</span><span class="sxs-lookup"><span data-stu-id="160f2-114">msDFS-LinkPathv2</span></span>                            |
| <span data-ttu-id="160f2-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="160f2-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="160f2-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="160f2-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="160f2-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="160f2-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="160f2-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="160f2-118">Attribute-Id</span></span>      | <span data-ttu-id="160f2-119">1.2.840.113556.1.4.2039</span><span class="sxs-lookup"><span data-stu-id="160f2-119">1.2.840.113556.1.4.2039</span></span>                     |
| <span data-ttu-id="160f2-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="160f2-120">System-Id-Guid</span></span>    | <span data-ttu-id="160f2-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span><span class="sxs-lookup"><span data-stu-id="160f2-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span></span>        |
| <span data-ttu-id="160f2-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="160f2-122">Syntax</span></span>            | [<span data-ttu-id="160f2-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="160f2-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="160f2-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="160f2-124">Implementations</span></span>

-   [<span data-ttu-id="160f2-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="160f2-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="160f2-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="160f2-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="160f2-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="160f2-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="160f2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="160f2-128">Windows Server 2008</span></span>



| <span data-ttu-id="160f2-129">Entrada</span><span class="sxs-lookup"><span data-stu-id="160f2-129">Entry</span></span> | <span data-ttu-id="160f2-130">Value</span><span class="sxs-lookup"><span data-stu-id="160f2-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="160f2-131">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="160f2-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="160f2-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="160f2-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="160f2-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="160f2-133">System-Only</span></span>            | <span data-ttu-id="160f2-134">False</span><span class="sxs-lookup"><span data-stu-id="160f2-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="160f2-135">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="160f2-135">Is-Single-Valued</span></span>       | <span data-ttu-id="160f2-136">True</span><span class="sxs-lookup"><span data-stu-id="160f2-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="160f2-137">Está indexado</span><span class="sxs-lookup"><span data-stu-id="160f2-137">Is Indexed</span></span>             | <span data-ttu-id="160f2-138">False</span><span class="sxs-lookup"><span data-stu-id="160f2-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="160f2-139">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="160f2-139">In Global Catalog</span></span>      | <span data-ttu-id="160f2-140">False</span><span class="sxs-lookup"><span data-stu-id="160f2-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="160f2-141">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="160f2-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="160f2-142">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="160f2-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="160f2-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="160f2-143">Range-Lower</span></span>            | <span data-ttu-id="160f2-144">0</span><span class="sxs-lookup"><span data-stu-id="160f2-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="160f2-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="160f2-145">Range-Upper</span></span>            | <span data-ttu-id="160f2-146">32766</span><span class="sxs-lookup"><span data-stu-id="160f2-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="160f2-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="160f2-147">Search-Flags</span></span>           | <span data-ttu-id="160f2-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="160f2-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="160f2-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="160f2-149">System-Flags</span></span>           | <span data-ttu-id="160f2-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="160f2-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="160f2-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="160f2-151">Classes used in</span></span>        | [<span data-ttu-id="160f2-152">**MS-DFS-Deleted-Link-V2**</span><span class="sxs-lookup"><span data-stu-id="160f2-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="160f2-153">**MS-DFS-Link-V2**</span><span class="sxs-lookup"><span data-stu-id="160f2-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="160f2-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="160f2-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="160f2-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="160f2-155">Entry</span></span> | <span data-ttu-id="160f2-156">Value</span><span class="sxs-lookup"><span data-stu-id="160f2-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="160f2-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="160f2-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="160f2-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="160f2-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="160f2-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="160f2-159">System-Only</span></span>            | <span data-ttu-id="160f2-160">False</span><span class="sxs-lookup"><span data-stu-id="160f2-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="160f2-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="160f2-161">Is-Single-Valued</span></span>       | <span data-ttu-id="160f2-162">True</span><span class="sxs-lookup"><span data-stu-id="160f2-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="160f2-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="160f2-163">Is Indexed</span></span>             | <span data-ttu-id="160f2-164">False</span><span class="sxs-lookup"><span data-stu-id="160f2-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="160f2-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="160f2-165">In Global Catalog</span></span>      | <span data-ttu-id="160f2-166">False</span><span class="sxs-lookup"><span data-stu-id="160f2-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="160f2-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="160f2-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="160f2-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="160f2-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="160f2-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="160f2-169">Range-Lower</span></span>            | <span data-ttu-id="160f2-170">0</span><span class="sxs-lookup"><span data-stu-id="160f2-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="160f2-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="160f2-171">Range-Upper</span></span>            | <span data-ttu-id="160f2-172">32766</span><span class="sxs-lookup"><span data-stu-id="160f2-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="160f2-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="160f2-173">Search-Flags</span></span>           | <span data-ttu-id="160f2-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="160f2-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="160f2-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="160f2-175">System-Flags</span></span>           | <span data-ttu-id="160f2-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="160f2-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="160f2-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="160f2-177">Classes used in</span></span>        | [<span data-ttu-id="160f2-178">**MS-DFS-Deleted-Link-V2**</span><span class="sxs-lookup"><span data-stu-id="160f2-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="160f2-179">**MS-DFS-Link-V2**</span><span class="sxs-lookup"><span data-stu-id="160f2-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="160f2-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="160f2-180">Windows Server 2012</span></span>



| <span data-ttu-id="160f2-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="160f2-181">Entry</span></span> | <span data-ttu-id="160f2-182">Value</span><span class="sxs-lookup"><span data-stu-id="160f2-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="160f2-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="160f2-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="160f2-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="160f2-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="160f2-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="160f2-185">System-Only</span></span>            | <span data-ttu-id="160f2-186">False</span><span class="sxs-lookup"><span data-stu-id="160f2-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="160f2-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="160f2-187">Is-Single-Valued</span></span>       | <span data-ttu-id="160f2-188">True</span><span class="sxs-lookup"><span data-stu-id="160f2-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="160f2-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="160f2-189">Is Indexed</span></span>             | <span data-ttu-id="160f2-190">False</span><span class="sxs-lookup"><span data-stu-id="160f2-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="160f2-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="160f2-191">In Global Catalog</span></span>      | <span data-ttu-id="160f2-192">False</span><span class="sxs-lookup"><span data-stu-id="160f2-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="160f2-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="160f2-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="160f2-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="160f2-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="160f2-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="160f2-195">Range-Lower</span></span>            | <span data-ttu-id="160f2-196">0</span><span class="sxs-lookup"><span data-stu-id="160f2-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="160f2-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="160f2-197">Range-Upper</span></span>            | <span data-ttu-id="160f2-198">32766</span><span class="sxs-lookup"><span data-stu-id="160f2-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="160f2-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="160f2-199">Search-Flags</span></span>           | <span data-ttu-id="160f2-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="160f2-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="160f2-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="160f2-201">System-Flags</span></span>           | <span data-ttu-id="160f2-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="160f2-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="160f2-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="160f2-203">Classes used in</span></span>        | [<span data-ttu-id="160f2-204">**MS-DFS-Deleted-Link-V2**</span><span class="sxs-lookup"><span data-stu-id="160f2-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="160f2-205">**MS-DFS-Link-V2**</span><span class="sxs-lookup"><span data-stu-id="160f2-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





