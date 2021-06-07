---
title: Atributo ms-DFS-Link-Path-v2
description: Ruta de acceso del vínculo DFS relativa al recurso compartido de destino raíz DFS (es decir, sin los componentes de nombre de espacio de nombres DFS o servidor/dominio). Use barras diagonales (/) en lugar de barras diagonales inversas ( , para que las búsquedas LDAP se puedan realizar sin tener que \) usar escapes.
ms.assetid: 98fd6e99-0d7e-4ffa-b8ec-d26ca03ffead
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ms-DFS-Link-Path-v2
- Esquema de AD del atributo msDFS-LinkPathv2
topic_type:
- apiref
api_name:
- ms-DFS-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4659dbf00c6a53c77a23e98836ea1af4eeb4c38a
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386864"
---
# <a name="ms-dfs-link-path-v2-attribute"></a><span data-ttu-id="3b155-106">Atributo ms-DFS-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="3b155-106">ms-DFS-Link-Path-v2 attribute</span></span>

<span data-ttu-id="3b155-107">Ruta de acceso del vínculo DFS relativa al recurso compartido de destino raíz DFS (es decir, sin los componentes de nombre de espacio de nombres DFS o servidor/dominio).</span><span class="sxs-lookup"><span data-stu-id="3b155-107">DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="3b155-108">Use barras diagonales (/) en lugar de barras diagonales inversas ( ), para que las búsquedas LDAP se puedan realizar sin tener que \\ usar escapes.</span><span class="sxs-lookup"><span data-stu-id="3b155-108">Use forward slashes (/) instead of backslashes (\\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="3b155-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="3b155-109">Entry</span></span> | <span data-ttu-id="3b155-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3b155-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="3b155-111">CN</span><span class="sxs-lookup"><span data-stu-id="3b155-111">CN</span></span>                | <span data-ttu-id="3b155-112">ms-DFS-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="3b155-112">ms-DFS-Link-Path-v2</span></span>                         |
| <span data-ttu-id="3b155-113">Ldap-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3b155-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3b155-114">msDFS-LinkPathv2</span><span class="sxs-lookup"><span data-stu-id="3b155-114">msDFS-LinkPathv2</span></span>                            |
| <span data-ttu-id="3b155-115">Size</span><span class="sxs-lookup"><span data-stu-id="3b155-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="3b155-116">Actualizar privilegios</span><span class="sxs-lookup"><span data-stu-id="3b155-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="3b155-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="3b155-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="3b155-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3b155-118">Attribute-Id</span></span>      | <span data-ttu-id="3b155-119">1.2.840.113556.1.4.2039</span><span class="sxs-lookup"><span data-stu-id="3b155-119">1.2.840.113556.1.4.2039</span></span>                     |
| <span data-ttu-id="3b155-120">System-Id-Guid</span><span class="sxs-lookup"><span data-stu-id="3b155-120">System-Id-Guid</span></span>    | <span data-ttu-id="3b155-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span><span class="sxs-lookup"><span data-stu-id="3b155-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span></span>        |
| <span data-ttu-id="3b155-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b155-122">Syntax</span></span>            | [<span data-ttu-id="3b155-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3b155-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="3b155-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="3b155-124">Implementations</span></span>

-   [<span data-ttu-id="3b155-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3b155-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3b155-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3b155-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3b155-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3b155-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="3b155-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b155-128">Windows Server 2008</span></span>



| <span data-ttu-id="3b155-129">Entrada</span><span class="sxs-lookup"><span data-stu-id="3b155-129">Entry</span></span> | <span data-ttu-id="3b155-130">Valor</span><span class="sxs-lookup"><span data-stu-id="3b155-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b155-131">Id. de vínculo</span><span class="sxs-lookup"><span data-stu-id="3b155-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="3b155-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b155-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="3b155-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b155-133">System-Only</span></span>            | <span data-ttu-id="3b155-134">False</span><span class="sxs-lookup"><span data-stu-id="3b155-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="3b155-135">Es de un solo valor</span><span class="sxs-lookup"><span data-stu-id="3b155-135">Is-Single-Valued</span></span>       | <span data-ttu-id="3b155-136">True</span><span class="sxs-lookup"><span data-stu-id="3b155-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="3b155-137">Está indexado</span><span class="sxs-lookup"><span data-stu-id="3b155-137">Is Indexed</span></span>             | <span data-ttu-id="3b155-138">False</span><span class="sxs-lookup"><span data-stu-id="3b155-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="3b155-139">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3b155-139">In Global Catalog</span></span>      | <span data-ttu-id="3b155-140">False</span><span class="sxs-lookup"><span data-stu-id="3b155-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="3b155-141">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3b155-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b155-142">O:BAG:BAD:S:</span><span class="sxs-lookup"><span data-stu-id="3b155-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="3b155-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b155-143">Range-Lower</span></span>            | <span data-ttu-id="3b155-144">0</span><span class="sxs-lookup"><span data-stu-id="3b155-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="3b155-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b155-145">Range-Upper</span></span>            | <span data-ttu-id="3b155-146">32766</span><span class="sxs-lookup"><span data-stu-id="3b155-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="3b155-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b155-147">Search-Flags</span></span>           | <span data-ttu-id="3b155-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b155-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="3b155-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b155-149">System-Flags</span></span>           | <span data-ttu-id="3b155-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b155-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3b155-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="3b155-151">Classes used in</span></span>        | [<span data-ttu-id="3b155-152">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="3b155-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="3b155-153">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="3b155-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3b155-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3b155-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3b155-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="3b155-155">Entry</span></span> | <span data-ttu-id="3b155-156">Valor</span><span class="sxs-lookup"><span data-stu-id="3b155-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b155-157">Id. de vínculo</span><span class="sxs-lookup"><span data-stu-id="3b155-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="3b155-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b155-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="3b155-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b155-159">System-Only</span></span>            | <span data-ttu-id="3b155-160">False</span><span class="sxs-lookup"><span data-stu-id="3b155-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="3b155-161">Es de un solo valor</span><span class="sxs-lookup"><span data-stu-id="3b155-161">Is-Single-Valued</span></span>       | <span data-ttu-id="3b155-162">True</span><span class="sxs-lookup"><span data-stu-id="3b155-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="3b155-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="3b155-163">Is Indexed</span></span>             | <span data-ttu-id="3b155-164">False</span><span class="sxs-lookup"><span data-stu-id="3b155-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="3b155-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3b155-165">In Global Catalog</span></span>      | <span data-ttu-id="3b155-166">False</span><span class="sxs-lookup"><span data-stu-id="3b155-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="3b155-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3b155-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b155-168">O:BAG:BAD:S:</span><span class="sxs-lookup"><span data-stu-id="3b155-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="3b155-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b155-169">Range-Lower</span></span>            | <span data-ttu-id="3b155-170">0</span><span class="sxs-lookup"><span data-stu-id="3b155-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="3b155-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b155-171">Range-Upper</span></span>            | <span data-ttu-id="3b155-172">32766</span><span class="sxs-lookup"><span data-stu-id="3b155-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="3b155-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b155-173">Search-Flags</span></span>           | <span data-ttu-id="3b155-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b155-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="3b155-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b155-175">System-Flags</span></span>           | <span data-ttu-id="3b155-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b155-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3b155-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="3b155-177">Classes used in</span></span>        | [<span data-ttu-id="3b155-178">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="3b155-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="3b155-179">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="3b155-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3b155-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3b155-180">Windows Server 2012</span></span>



| <span data-ttu-id="3b155-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="3b155-181">Entry</span></span> | <span data-ttu-id="3b155-182">Valor</span><span class="sxs-lookup"><span data-stu-id="3b155-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b155-183">Id. de vínculo</span><span class="sxs-lookup"><span data-stu-id="3b155-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="3b155-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b155-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="3b155-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b155-185">System-Only</span></span>            | <span data-ttu-id="3b155-186">False</span><span class="sxs-lookup"><span data-stu-id="3b155-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="3b155-187">Es de un solo valor</span><span class="sxs-lookup"><span data-stu-id="3b155-187">Is-Single-Valued</span></span>       | <span data-ttu-id="3b155-188">True</span><span class="sxs-lookup"><span data-stu-id="3b155-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="3b155-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="3b155-189">Is Indexed</span></span>             | <span data-ttu-id="3b155-190">False</span><span class="sxs-lookup"><span data-stu-id="3b155-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="3b155-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3b155-191">In Global Catalog</span></span>      | <span data-ttu-id="3b155-192">False</span><span class="sxs-lookup"><span data-stu-id="3b155-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="3b155-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3b155-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b155-194">O:BAG:BAD:S:</span><span class="sxs-lookup"><span data-stu-id="3b155-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="3b155-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b155-195">Range-Lower</span></span>            | <span data-ttu-id="3b155-196">0</span><span class="sxs-lookup"><span data-stu-id="3b155-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="3b155-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b155-197">Range-Upper</span></span>            | <span data-ttu-id="3b155-198">32766</span><span class="sxs-lookup"><span data-stu-id="3b155-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="3b155-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b155-199">Search-Flags</span></span>           | <span data-ttu-id="3b155-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b155-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="3b155-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b155-201">System-Flags</span></span>           | <span data-ttu-id="3b155-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b155-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3b155-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="3b155-203">Classes used in</span></span>        | [<span data-ttu-id="3b155-204">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="3b155-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="3b155-205">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="3b155-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





