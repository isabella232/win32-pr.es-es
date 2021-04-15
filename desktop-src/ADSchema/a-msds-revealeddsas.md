---
title: atributo MS-DS-Revelód-DSA
description: Vínculo hacia atrás para MS-DS-revelado-usuarios. Identifica qué RODC contiene el secreto de los usuarios.
ms.assetid: cd84db75-d961-4290-8aa7-2805febbd842
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MS-DS-Revelóted-DSA
- Esquema de AD de atributo msDS-RevealedDSAs
topic_type:
- apiref
api_name:
- ms-DS-Revealed-DSAs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e77dfd69fafffc3286f0ff9419965d7ae9daaa0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493804"
---
# <a name="ms-ds-revealed-dsas-attribute"></a><span data-ttu-id="1de4f-106">atributo MS-DS-Revelód-DSA</span><span class="sxs-lookup"><span data-stu-id="1de4f-106">ms-DS-Revealed-DSAs attribute</span></span>

<span data-ttu-id="1de4f-107">Vínculo hacia atrás para [**MS-DS-revelado-usuarios**](a-msds-revealedusers.md).</span><span class="sxs-lookup"><span data-stu-id="1de4f-107">Backward link for [**ms-DS-Revealed-Users**](a-msds-revealedusers.md).</span></span> <span data-ttu-id="1de4f-108">Identifica qué RODC contiene el secreto del usuario.</span><span class="sxs-lookup"><span data-stu-id="1de4f-108">Identifies which RODC holds that user's secret.</span></span>



| <span data-ttu-id="1de4f-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="1de4f-109">Entry</span></span> | <span data-ttu-id="1de4f-110">Value</span><span class="sxs-lookup"><span data-stu-id="1de4f-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="1de4f-111">CN</span><span class="sxs-lookup"><span data-stu-id="1de4f-111">CN</span></span>                | <span data-ttu-id="1de4f-112">MS-DS-Revelód-DSA</span><span class="sxs-lookup"><span data-stu-id="1de4f-112">ms-DS-Revealed-DSAs</span></span>                     |
| <span data-ttu-id="1de4f-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="1de4f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1de4f-114">msDS-RevealedDSAs</span><span class="sxs-lookup"><span data-stu-id="1de4f-114">msDS-RevealedDSAs</span></span>                       |
| <span data-ttu-id="1de4f-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="1de4f-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="1de4f-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="1de4f-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="1de4f-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="1de4f-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="1de4f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1de4f-118">Attribute-Id</span></span>      | <span data-ttu-id="1de4f-119">1.2.840.113556.1.4.1930</span><span class="sxs-lookup"><span data-stu-id="1de4f-119">1.2.840.113556.1.4.1930</span></span>                 |
| <span data-ttu-id="1de4f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1de4f-120">System-Id-Guid</span></span>    | <span data-ttu-id="1de4f-121">94f6f2ac-c76d-4b5e-b71f-f332c3e93c22</span><span class="sxs-lookup"><span data-stu-id="1de4f-121">94f6f2ac-c76d-4b5e-b71f-f332c3e93c22</span></span>    |
| <span data-ttu-id="1de4f-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1de4f-122">Syntax</span></span>            | [<span data-ttu-id="1de4f-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="1de4f-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="1de4f-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="1de4f-124">Implementations</span></span>

-   [<span data-ttu-id="1de4f-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1de4f-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1de4f-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1de4f-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1de4f-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1de4f-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="1de4f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1de4f-128">Windows Server 2008</span></span>



| <span data-ttu-id="1de4f-129">Entrada</span><span class="sxs-lookup"><span data-stu-id="1de4f-129">Entry</span></span> | <span data-ttu-id="1de4f-130">Value</span><span class="sxs-lookup"><span data-stu-id="1de4f-130">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1de4f-131">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1de4f-131">Link-Id</span></span>                | <span data-ttu-id="1de4f-132">2103</span><span class="sxs-lookup"><span data-stu-id="1de4f-132">2103</span></span>                            |
| <span data-ttu-id="1de4f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1de4f-133">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1de4f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="1de4f-134">System-Only</span></span>            | <span data-ttu-id="1de4f-135">True</span><span class="sxs-lookup"><span data-stu-id="1de4f-135">True</span></span>                            |
| <span data-ttu-id="1de4f-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1de4f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="1de4f-137">False</span><span class="sxs-lookup"><span data-stu-id="1de4f-137">False</span></span>                           |
| <span data-ttu-id="1de4f-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1de4f-138">Is Indexed</span></span>             | <span data-ttu-id="1de4f-139">False</span><span class="sxs-lookup"><span data-stu-id="1de4f-139">False</span></span>                           |
| <span data-ttu-id="1de4f-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1de4f-140">In Global Catalog</span></span>      | <span data-ttu-id="1de4f-141">False</span><span class="sxs-lookup"><span data-stu-id="1de4f-141">False</span></span>                           |
| <span data-ttu-id="1de4f-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1de4f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="1de4f-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1de4f-143">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1de4f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1de4f-144">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1de4f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1de4f-145">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1de4f-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1de4f-146">Search-Flags</span></span>           | <span data-ttu-id="1de4f-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1de4f-147">0x00000000</span></span>                      |
| <span data-ttu-id="1de4f-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1de4f-148">System-Flags</span></span>           | <span data-ttu-id="1de4f-149">0x00000011</span><span class="sxs-lookup"><span data-stu-id="1de4f-149">0x00000011</span></span>                      |
| <span data-ttu-id="1de4f-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1de4f-150">Classes used in</span></span>        | [<span data-ttu-id="1de4f-151">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1de4f-151">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1de4f-152">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1de4f-152">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1de4f-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="1de4f-153">Entry</span></span> | <span data-ttu-id="1de4f-154">Value</span><span class="sxs-lookup"><span data-stu-id="1de4f-154">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1de4f-155">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1de4f-155">Link-Id</span></span>                | <span data-ttu-id="1de4f-156">2103</span><span class="sxs-lookup"><span data-stu-id="1de4f-156">2103</span></span>                            |
| <span data-ttu-id="1de4f-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1de4f-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1de4f-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="1de4f-158">System-Only</span></span>            | <span data-ttu-id="1de4f-159">True</span><span class="sxs-lookup"><span data-stu-id="1de4f-159">True</span></span>                            |
| <span data-ttu-id="1de4f-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1de4f-160">Is-Single-Valued</span></span>       | <span data-ttu-id="1de4f-161">False</span><span class="sxs-lookup"><span data-stu-id="1de4f-161">False</span></span>                           |
| <span data-ttu-id="1de4f-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1de4f-162">Is Indexed</span></span>             | <span data-ttu-id="1de4f-163">False</span><span class="sxs-lookup"><span data-stu-id="1de4f-163">False</span></span>                           |
| <span data-ttu-id="1de4f-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1de4f-164">In Global Catalog</span></span>      | <span data-ttu-id="1de4f-165">False</span><span class="sxs-lookup"><span data-stu-id="1de4f-165">False</span></span>                           |
| <span data-ttu-id="1de4f-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1de4f-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="1de4f-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1de4f-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1de4f-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1de4f-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1de4f-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1de4f-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1de4f-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1de4f-170">Search-Flags</span></span>           | <span data-ttu-id="1de4f-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1de4f-171">0x00000000</span></span>                      |
| <span data-ttu-id="1de4f-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1de4f-172">System-Flags</span></span>           | <span data-ttu-id="1de4f-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="1de4f-173">0x00000011</span></span>                      |
| <span data-ttu-id="1de4f-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1de4f-174">Classes used in</span></span>        | [<span data-ttu-id="1de4f-175">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1de4f-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1de4f-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1de4f-176">Windows Server 2012</span></span>



| <span data-ttu-id="1de4f-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="1de4f-177">Entry</span></span> | <span data-ttu-id="1de4f-178">Value</span><span class="sxs-lookup"><span data-stu-id="1de4f-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1de4f-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1de4f-179">Link-Id</span></span>                | <span data-ttu-id="1de4f-180">2103</span><span class="sxs-lookup"><span data-stu-id="1de4f-180">2103</span></span>                            |
| <span data-ttu-id="1de4f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1de4f-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1de4f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="1de4f-182">System-Only</span></span>            | <span data-ttu-id="1de4f-183">True</span><span class="sxs-lookup"><span data-stu-id="1de4f-183">True</span></span>                            |
| <span data-ttu-id="1de4f-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1de4f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="1de4f-185">False</span><span class="sxs-lookup"><span data-stu-id="1de4f-185">False</span></span>                           |
| <span data-ttu-id="1de4f-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1de4f-186">Is Indexed</span></span>             | <span data-ttu-id="1de4f-187">False</span><span class="sxs-lookup"><span data-stu-id="1de4f-187">False</span></span>                           |
| <span data-ttu-id="1de4f-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1de4f-188">In Global Catalog</span></span>      | <span data-ttu-id="1de4f-189">False</span><span class="sxs-lookup"><span data-stu-id="1de4f-189">False</span></span>                           |
| <span data-ttu-id="1de4f-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1de4f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="1de4f-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1de4f-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1de4f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1de4f-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1de4f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1de4f-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1de4f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1de4f-194">Search-Flags</span></span>           | <span data-ttu-id="1de4f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1de4f-195">0x00000000</span></span>                      |
| <span data-ttu-id="1de4f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1de4f-196">System-Flags</span></span>           | <span data-ttu-id="1de4f-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="1de4f-197">0x00000011</span></span>                      |
| <span data-ttu-id="1de4f-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1de4f-198">Classes used in</span></span>        | [<span data-ttu-id="1de4f-199">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1de4f-199">**Top**</span></span>](c-top.md)<br/> |



 

 





