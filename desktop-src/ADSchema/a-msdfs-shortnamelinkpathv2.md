---
title: Atributo ms-DFS-Short-Name-Link-Path-v2
description: Ruta de acceso del vínculo DFS de nombre corto en relación con el recurso compartido de destino raíz DFS (es decir, sin los componentes de nombre de espacio de nombres DFS o servidor/dominio). Use barras diagonales (/) en lugar de barras diagonales inversas ( , para que las búsquedas LDAP se puedan realizar sin tener que \) usar escapes.
ms.assetid: 0589d3f5-9734-4f95-bba9-22f13bb1c9f1
ms.tgt_platform: multiple
keywords:
- ms-DFS-Short-Name-Link-Path-v2 attribute AD Schema
- Esquema de AD del atributo msDFS-ShortNameLinkPathv2
topic_type:
- apiref
api_name:
- ms-DFS-Short-Name-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 663ee1ff2dac67eff7bd9eca87aa8eacf40436ff
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386854"
---
# <a name="ms-dfs-short-name-link-path-v2-attribute"></a><span data-ttu-id="69c3d-106">Atributo ms-DFS-Short-Name-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="69c3d-106">ms-DFS-Short-Name-Link-Path-v2 attribute</span></span>

<span data-ttu-id="69c3d-107">Ruta de acceso del vínculo DFS de nombre corto en relación con el recurso compartido de destino raíz DFS (es decir, sin los componentes de nombre de espacio de nombres DFS o servidor/dominio).</span><span class="sxs-lookup"><span data-stu-id="69c3d-107">Short Name DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="69c3d-108">Use barras diagonales (/) en lugar de barras diagonales inversas ( ), para que las búsquedas LDAP se puedan realizar sin tener que \\ usar escapes.</span><span class="sxs-lookup"><span data-stu-id="69c3d-108">Use forward slashes (/) instead of backslashes (\\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="69c3d-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="69c3d-109">Entry</span></span> | <span data-ttu-id="69c3d-110">Valor</span><span class="sxs-lookup"><span data-stu-id="69c3d-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="69c3d-111">CN</span><span class="sxs-lookup"><span data-stu-id="69c3d-111">CN</span></span>                | <span data-ttu-id="69c3d-112">ms-DFS-Short-Name-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="69c3d-112">ms-DFS-Short-Name-Link-Path-v2</span></span>              |
| <span data-ttu-id="69c3d-113">Ldap-Display-Name</span><span class="sxs-lookup"><span data-stu-id="69c3d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="69c3d-114">msDFS-ShortNameLinkPathv2</span><span class="sxs-lookup"><span data-stu-id="69c3d-114">msDFS-ShortNameLinkPathv2</span></span>                   |
| <span data-ttu-id="69c3d-115">Size</span><span class="sxs-lookup"><span data-stu-id="69c3d-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="69c3d-116">Actualizar privilegios</span><span class="sxs-lookup"><span data-stu-id="69c3d-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="69c3d-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="69c3d-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="69c3d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="69c3d-118">Attribute-Id</span></span>      | <span data-ttu-id="69c3d-119">1.2.840.113556.1.4.2042</span><span class="sxs-lookup"><span data-stu-id="69c3d-119">1.2.840.113556.1.4.2042</span></span>                     |
| <span data-ttu-id="69c3d-120">System-Id-Guid</span><span class="sxs-lookup"><span data-stu-id="69c3d-120">System-Id-Guid</span></span>    | <span data-ttu-id="69c3d-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span><span class="sxs-lookup"><span data-stu-id="69c3d-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span></span>        |
| <span data-ttu-id="69c3d-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69c3d-122">Syntax</span></span>            | [<span data-ttu-id="69c3d-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="69c3d-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="69c3d-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="69c3d-124">Implementations</span></span>

-   [<span data-ttu-id="69c3d-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="69c3d-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="69c3d-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="69c3d-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="69c3d-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="69c3d-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="69c3d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69c3d-128">Windows Server 2008</span></span>



| <span data-ttu-id="69c3d-129">Entrada</span><span class="sxs-lookup"><span data-stu-id="69c3d-129">Entry</span></span> | <span data-ttu-id="69c3d-130">Valor</span><span class="sxs-lookup"><span data-stu-id="69c3d-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69c3d-131">Id. de vínculo</span><span class="sxs-lookup"><span data-stu-id="69c3d-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="69c3d-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69c3d-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="69c3d-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="69c3d-133">System-Only</span></span>            | <span data-ttu-id="69c3d-134">False</span><span class="sxs-lookup"><span data-stu-id="69c3d-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="69c3d-135">Es de un solo valor</span><span class="sxs-lookup"><span data-stu-id="69c3d-135">Is-Single-Valued</span></span>       | <span data-ttu-id="69c3d-136">True</span><span class="sxs-lookup"><span data-stu-id="69c3d-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="69c3d-137">Está indexado</span><span class="sxs-lookup"><span data-stu-id="69c3d-137">Is Indexed</span></span>             | <span data-ttu-id="69c3d-138">False</span><span class="sxs-lookup"><span data-stu-id="69c3d-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="69c3d-139">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="69c3d-139">In Global Catalog</span></span>      | <span data-ttu-id="69c3d-140">False</span><span class="sxs-lookup"><span data-stu-id="69c3d-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="69c3d-141">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69c3d-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="69c3d-142">O:BAG:BAD:S:</span><span class="sxs-lookup"><span data-stu-id="69c3d-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="69c3d-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69c3d-143">Range-Lower</span></span>            | <span data-ttu-id="69c3d-144">0</span><span class="sxs-lookup"><span data-stu-id="69c3d-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="69c3d-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69c3d-145">Range-Upper</span></span>            | <span data-ttu-id="69c3d-146">32766</span><span class="sxs-lookup"><span data-stu-id="69c3d-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="69c3d-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69c3d-147">Search-Flags</span></span>           | <span data-ttu-id="69c3d-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69c3d-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="69c3d-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69c3d-149">System-Flags</span></span>           | <span data-ttu-id="69c3d-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69c3d-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="69c3d-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="69c3d-151">Classes used in</span></span>        | [<span data-ttu-id="69c3d-152">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="69c3d-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="69c3d-153">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="69c3d-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="69c3d-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="69c3d-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="69c3d-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="69c3d-155">Entry</span></span> | <span data-ttu-id="69c3d-156">Valor</span><span class="sxs-lookup"><span data-stu-id="69c3d-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69c3d-157">Id. de vínculo</span><span class="sxs-lookup"><span data-stu-id="69c3d-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="69c3d-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69c3d-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="69c3d-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="69c3d-159">System-Only</span></span>            | <span data-ttu-id="69c3d-160">False</span><span class="sxs-lookup"><span data-stu-id="69c3d-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="69c3d-161">Es de un solo valor</span><span class="sxs-lookup"><span data-stu-id="69c3d-161">Is-Single-Valued</span></span>       | <span data-ttu-id="69c3d-162">True</span><span class="sxs-lookup"><span data-stu-id="69c3d-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="69c3d-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="69c3d-163">Is Indexed</span></span>             | <span data-ttu-id="69c3d-164">False</span><span class="sxs-lookup"><span data-stu-id="69c3d-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="69c3d-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="69c3d-165">In Global Catalog</span></span>      | <span data-ttu-id="69c3d-166">False</span><span class="sxs-lookup"><span data-stu-id="69c3d-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="69c3d-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69c3d-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="69c3d-168">O:BAG:BAD:S:</span><span class="sxs-lookup"><span data-stu-id="69c3d-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="69c3d-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69c3d-169">Range-Lower</span></span>            | <span data-ttu-id="69c3d-170">0</span><span class="sxs-lookup"><span data-stu-id="69c3d-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="69c3d-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69c3d-171">Range-Upper</span></span>            | <span data-ttu-id="69c3d-172">32766</span><span class="sxs-lookup"><span data-stu-id="69c3d-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="69c3d-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69c3d-173">Search-Flags</span></span>           | <span data-ttu-id="69c3d-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69c3d-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="69c3d-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69c3d-175">System-Flags</span></span>           | <span data-ttu-id="69c3d-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69c3d-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="69c3d-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="69c3d-177">Classes used in</span></span>        | [<span data-ttu-id="69c3d-178">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="69c3d-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="69c3d-179">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="69c3d-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="69c3d-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="69c3d-180">Windows Server 2012</span></span>



| <span data-ttu-id="69c3d-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="69c3d-181">Entry</span></span> | <span data-ttu-id="69c3d-182">Valor</span><span class="sxs-lookup"><span data-stu-id="69c3d-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69c3d-183">Id. de vínculo</span><span class="sxs-lookup"><span data-stu-id="69c3d-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="69c3d-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69c3d-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="69c3d-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="69c3d-185">System-Only</span></span>            | <span data-ttu-id="69c3d-186">False</span><span class="sxs-lookup"><span data-stu-id="69c3d-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="69c3d-187">Es de un solo valor</span><span class="sxs-lookup"><span data-stu-id="69c3d-187">Is-Single-Valued</span></span>       | <span data-ttu-id="69c3d-188">True</span><span class="sxs-lookup"><span data-stu-id="69c3d-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="69c3d-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="69c3d-189">Is Indexed</span></span>             | <span data-ttu-id="69c3d-190">False</span><span class="sxs-lookup"><span data-stu-id="69c3d-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="69c3d-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="69c3d-191">In Global Catalog</span></span>      | <span data-ttu-id="69c3d-192">False</span><span class="sxs-lookup"><span data-stu-id="69c3d-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="69c3d-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69c3d-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="69c3d-194">O:BAG:BAD:S:</span><span class="sxs-lookup"><span data-stu-id="69c3d-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="69c3d-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69c3d-195">Range-Lower</span></span>            | <span data-ttu-id="69c3d-196">0</span><span class="sxs-lookup"><span data-stu-id="69c3d-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="69c3d-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69c3d-197">Range-Upper</span></span>            | <span data-ttu-id="69c3d-198">32766</span><span class="sxs-lookup"><span data-stu-id="69c3d-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="69c3d-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69c3d-199">Search-Flags</span></span>           | <span data-ttu-id="69c3d-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69c3d-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="69c3d-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69c3d-201">System-Flags</span></span>           | <span data-ttu-id="69c3d-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69c3d-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="69c3d-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="69c3d-203">Classes used in</span></span>        | [<span data-ttu-id="69c3d-204">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="69c3d-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="69c3d-205">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="69c3d-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





