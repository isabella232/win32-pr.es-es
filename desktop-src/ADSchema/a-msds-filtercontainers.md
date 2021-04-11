---
title: atributo MS-DS-Filter-containers
description: Una cadena de varios valores que contiene los nombres de las clases utilizadas para determinar qué tipos de contenedor deben mostrarse en el complemento usuarios y equipos de Active Directory al filtrar.
ms.assetid: 765ac0e1-59d2-44a9-a01e-9cdf7d040c93
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-Filter-containers
- Esquema de AD de atributo msDS-FilterContainers
topic_type:
- apiref
api_name:
- ms-DS-Filter-Containers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8156b1baa2fe86ec0322a9161ce5231a7e23f32e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151815"
---
# <a name="ms-ds-filter-containers-attribute"></a><span data-ttu-id="c4d5e-105">atributo MS-DS-Filter-containers</span><span class="sxs-lookup"><span data-stu-id="c4d5e-105">ms-DS-Filter-Containers attribute</span></span>

<span data-ttu-id="c4d5e-106">Una cadena de varios valores que contiene los nombres de las clases utilizadas para determinar qué tipos de contenedor deben mostrarse en el complemento usuarios y equipos de Active Directory al filtrar.</span><span class="sxs-lookup"><span data-stu-id="c4d5e-106">A multiple-valued string that contains the names of classes used to determine which container types should be shown by the Active Directory Users and Computers snap-in when filtering.</span></span>



| <span data-ttu-id="c4d5e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4d5e-107">Entry</span></span> | <span data-ttu-id="c4d5e-108">Value</span><span class="sxs-lookup"><span data-stu-id="c4d5e-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c4d5e-109">CN</span><span class="sxs-lookup"><span data-stu-id="c4d5e-109">CN</span></span>                | <span data-ttu-id="c4d5e-110">MS-DS-Filter-containers</span><span class="sxs-lookup"><span data-stu-id="c4d5e-110">ms-DS-Filter-Containers</span></span>                     |
| <span data-ttu-id="c4d5e-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="c4d5e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c4d5e-112">msDS-FilterContainers</span><span class="sxs-lookup"><span data-stu-id="c4d5e-112">msDS-FilterContainers</span></span>                       |
| <span data-ttu-id="c4d5e-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="c4d5e-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="c4d5e-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="c4d5e-114">Update Privilege</span></span>  | <span data-ttu-id="c4d5e-115">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="c4d5e-115">Domain administrator</span></span>                        |
| <span data-ttu-id="c4d5e-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="c4d5e-116">Update Frequency</span></span>  | <span data-ttu-id="c4d5e-117">Cuando cambia la lista de tipos de contenedor.</span><span class="sxs-lookup"><span data-stu-id="c4d5e-117">When the list of container types changes.</span></span>   |
| <span data-ttu-id="c4d5e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c4d5e-118">Attribute-Id</span></span>      | <span data-ttu-id="c4d5e-119">1.2.840.113556.1.4.1703</span><span class="sxs-lookup"><span data-stu-id="c4d5e-119">1.2.840.113556.1.4.1703</span></span>                     |
| <span data-ttu-id="c4d5e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c4d5e-120">System-Id-Guid</span></span>    | <span data-ttu-id="c4d5e-121">fb00dcdf-ac37-483a-9c12-ac53a6603033</span><span class="sxs-lookup"><span data-stu-id="c4d5e-121">fb00dcdf-ac37-483a-9c12-ac53a6603033</span></span>        |
| <span data-ttu-id="c4d5e-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4d5e-122">Syntax</span></span>            | [<span data-ttu-id="c4d5e-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c4d5e-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c4d5e-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="c4d5e-124">Implementations</span></span>

-   [<span data-ttu-id="c4d5e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c4d5e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c4d5e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c4d5e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c4d5e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c4d5e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c4d5e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c4d5e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c4d5e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c4d5e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c4d5e-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c4d5e-130">Windows Server 2003</span></span>



| <span data-ttu-id="c4d5e-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4d5e-131">Entry</span></span> | <span data-ttu-id="c4d5e-132">Value</span><span class="sxs-lookup"><span data-stu-id="c4d5e-132">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="c4d5e-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c4d5e-133">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c4d5e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4d5e-134">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c4d5e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4d5e-135">System-Only</span></span>            | <span data-ttu-id="c4d5e-136">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-136">False</span></span>                                               |
| <span data-ttu-id="c4d5e-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c4d5e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c4d5e-138">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-138">False</span></span>                                               |
| <span data-ttu-id="c4d5e-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c4d5e-139">Is Indexed</span></span>             | <span data-ttu-id="c4d5e-140">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-140">False</span></span>                                               |
| <span data-ttu-id="c4d5e-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c4d5e-141">In Global Catalog</span></span>      | <span data-ttu-id="c4d5e-142">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-142">False</span></span>                                               |
| <span data-ttu-id="c4d5e-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c4d5e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4d5e-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c4d5e-144">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="c4d5e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4d5e-145">Range-Lower</span></span>            | <span data-ttu-id="c4d5e-146">1</span><span class="sxs-lookup"><span data-stu-id="c4d5e-146">1</span></span>                                                   |
| <span data-ttu-id="c4d5e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4d5e-147">Range-Upper</span></span>            | <span data-ttu-id="c4d5e-148">64</span><span class="sxs-lookup"><span data-stu-id="c4d5e-148">64</span></span>                                                  |
| <span data-ttu-id="c4d5e-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4d5e-149">Search-Flags</span></span>           | <span data-ttu-id="c4d5e-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4d5e-150">0x00000000</span></span>                                          |
| <span data-ttu-id="c4d5e-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4d5e-151">System-Flags</span></span>           | <span data-ttu-id="c4d5e-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4d5e-152">0x00000010</span></span>                                          |
| <span data-ttu-id="c4d5e-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c4d5e-153">Classes used in</span></span>        | [<span data-ttu-id="c4d5e-154">**DS-UI-configuración**</span><span class="sxs-lookup"><span data-stu-id="c4d5e-154">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c4d5e-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c4d5e-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c4d5e-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4d5e-156">Entry</span></span> | <span data-ttu-id="c4d5e-157">Value</span><span class="sxs-lookup"><span data-stu-id="c4d5e-157">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="c4d5e-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c4d5e-158">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c4d5e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4d5e-159">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c4d5e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4d5e-160">System-Only</span></span>            | <span data-ttu-id="c4d5e-161">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-161">False</span></span>                                               |
| <span data-ttu-id="c4d5e-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c4d5e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="c4d5e-163">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-163">False</span></span>                                               |
| <span data-ttu-id="c4d5e-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c4d5e-164">Is Indexed</span></span>             | <span data-ttu-id="c4d5e-165">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-165">False</span></span>                                               |
| <span data-ttu-id="c4d5e-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c4d5e-166">In Global Catalog</span></span>      | <span data-ttu-id="c4d5e-167">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-167">False</span></span>                                               |
| <span data-ttu-id="c4d5e-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c4d5e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4d5e-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c4d5e-169">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="c4d5e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4d5e-170">Range-Lower</span></span>            | <span data-ttu-id="c4d5e-171">1</span><span class="sxs-lookup"><span data-stu-id="c4d5e-171">1</span></span>                                                   |
| <span data-ttu-id="c4d5e-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4d5e-172">Range-Upper</span></span>            | <span data-ttu-id="c4d5e-173">64</span><span class="sxs-lookup"><span data-stu-id="c4d5e-173">64</span></span>                                                  |
| <span data-ttu-id="c4d5e-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4d5e-174">Search-Flags</span></span>           | <span data-ttu-id="c4d5e-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4d5e-175">0x00000000</span></span>                                          |
| <span data-ttu-id="c4d5e-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4d5e-176">System-Flags</span></span>           | <span data-ttu-id="c4d5e-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4d5e-177">0x00000010</span></span>                                          |
| <span data-ttu-id="c4d5e-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c4d5e-178">Classes used in</span></span>        | [<span data-ttu-id="c4d5e-179">**DS-UI-configuración**</span><span class="sxs-lookup"><span data-stu-id="c4d5e-179">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c4d5e-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4d5e-180">Windows Server 2008</span></span>



| <span data-ttu-id="c4d5e-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4d5e-181">Entry</span></span> | <span data-ttu-id="c4d5e-182">Value</span><span class="sxs-lookup"><span data-stu-id="c4d5e-182">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="c4d5e-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c4d5e-183">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c4d5e-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4d5e-184">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c4d5e-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4d5e-185">System-Only</span></span>            | <span data-ttu-id="c4d5e-186">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-186">False</span></span>                                               |
| <span data-ttu-id="c4d5e-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c4d5e-187">Is-Single-Valued</span></span>       | <span data-ttu-id="c4d5e-188">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-188">False</span></span>                                               |
| <span data-ttu-id="c4d5e-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c4d5e-189">Is Indexed</span></span>             | <span data-ttu-id="c4d5e-190">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-190">False</span></span>                                               |
| <span data-ttu-id="c4d5e-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c4d5e-191">In Global Catalog</span></span>      | <span data-ttu-id="c4d5e-192">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-192">False</span></span>                                               |
| <span data-ttu-id="c4d5e-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c4d5e-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4d5e-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c4d5e-194">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="c4d5e-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4d5e-195">Range-Lower</span></span>            | <span data-ttu-id="c4d5e-196">1</span><span class="sxs-lookup"><span data-stu-id="c4d5e-196">1</span></span>                                                   |
| <span data-ttu-id="c4d5e-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4d5e-197">Range-Upper</span></span>            | <span data-ttu-id="c4d5e-198">64</span><span class="sxs-lookup"><span data-stu-id="c4d5e-198">64</span></span>                                                  |
| <span data-ttu-id="c4d5e-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4d5e-199">Search-Flags</span></span>           | <span data-ttu-id="c4d5e-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4d5e-200">0x00000000</span></span>                                          |
| <span data-ttu-id="c4d5e-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4d5e-201">System-Flags</span></span>           | <span data-ttu-id="c4d5e-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4d5e-202">0x00000010</span></span>                                          |
| <span data-ttu-id="c4d5e-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c4d5e-203">Classes used in</span></span>        | [<span data-ttu-id="c4d5e-204">**DS-UI-configuración**</span><span class="sxs-lookup"><span data-stu-id="c4d5e-204">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c4d5e-205">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c4d5e-205">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c4d5e-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4d5e-206">Entry</span></span> | <span data-ttu-id="c4d5e-207">Value</span><span class="sxs-lookup"><span data-stu-id="c4d5e-207">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="c4d5e-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c4d5e-208">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c4d5e-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4d5e-209">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c4d5e-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4d5e-210">System-Only</span></span>            | <span data-ttu-id="c4d5e-211">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-211">False</span></span>                                               |
| <span data-ttu-id="c4d5e-212">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c4d5e-212">Is-Single-Valued</span></span>       | <span data-ttu-id="c4d5e-213">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-213">False</span></span>                                               |
| <span data-ttu-id="c4d5e-214">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c4d5e-214">Is Indexed</span></span>             | <span data-ttu-id="c4d5e-215">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-215">False</span></span>                                               |
| <span data-ttu-id="c4d5e-216">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c4d5e-216">In Global Catalog</span></span>      | <span data-ttu-id="c4d5e-217">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-217">False</span></span>                                               |
| <span data-ttu-id="c4d5e-218">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c4d5e-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4d5e-219">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c4d5e-219">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="c4d5e-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4d5e-220">Range-Lower</span></span>            | <span data-ttu-id="c4d5e-221">1</span><span class="sxs-lookup"><span data-stu-id="c4d5e-221">1</span></span>                                                   |
| <span data-ttu-id="c4d5e-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4d5e-222">Range-Upper</span></span>            | <span data-ttu-id="c4d5e-223">64</span><span class="sxs-lookup"><span data-stu-id="c4d5e-223">64</span></span>                                                  |
| <span data-ttu-id="c4d5e-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4d5e-224">Search-Flags</span></span>           | <span data-ttu-id="c4d5e-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4d5e-225">0x00000000</span></span>                                          |
| <span data-ttu-id="c4d5e-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4d5e-226">System-Flags</span></span>           | <span data-ttu-id="c4d5e-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4d5e-227">0x00000010</span></span>                                          |
| <span data-ttu-id="c4d5e-228">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c4d5e-228">Classes used in</span></span>        | [<span data-ttu-id="c4d5e-229">**DS-UI-configuración**</span><span class="sxs-lookup"><span data-stu-id="c4d5e-229">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c4d5e-230">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c4d5e-230">Windows Server 2012</span></span>



| <span data-ttu-id="c4d5e-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4d5e-231">Entry</span></span> | <span data-ttu-id="c4d5e-232">Value</span><span class="sxs-lookup"><span data-stu-id="c4d5e-232">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="c4d5e-233">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c4d5e-233">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c4d5e-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4d5e-234">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c4d5e-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4d5e-235">System-Only</span></span>            | <span data-ttu-id="c4d5e-236">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-236">False</span></span>                                               |
| <span data-ttu-id="c4d5e-237">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c4d5e-237">Is-Single-Valued</span></span>       | <span data-ttu-id="c4d5e-238">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-238">False</span></span>                                               |
| <span data-ttu-id="c4d5e-239">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c4d5e-239">Is Indexed</span></span>             | <span data-ttu-id="c4d5e-240">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-240">False</span></span>                                               |
| <span data-ttu-id="c4d5e-241">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c4d5e-241">In Global Catalog</span></span>      | <span data-ttu-id="c4d5e-242">False</span><span class="sxs-lookup"><span data-stu-id="c4d5e-242">False</span></span>                                               |
| <span data-ttu-id="c4d5e-243">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c4d5e-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4d5e-244">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c4d5e-244">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="c4d5e-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4d5e-245">Range-Lower</span></span>            | <span data-ttu-id="c4d5e-246">1</span><span class="sxs-lookup"><span data-stu-id="c4d5e-246">1</span></span>                                                   |
| <span data-ttu-id="c4d5e-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4d5e-247">Range-Upper</span></span>            | <span data-ttu-id="c4d5e-248">64</span><span class="sxs-lookup"><span data-stu-id="c4d5e-248">64</span></span>                                                  |
| <span data-ttu-id="c4d5e-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4d5e-249">Search-Flags</span></span>           | <span data-ttu-id="c4d5e-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4d5e-250">0x00000000</span></span>                                          |
| <span data-ttu-id="c4d5e-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4d5e-251">System-Flags</span></span>           | <span data-ttu-id="c4d5e-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4d5e-252">0x00000010</span></span>                                          |
| <span data-ttu-id="c4d5e-253">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c4d5e-253">Classes used in</span></span>        | [<span data-ttu-id="c4d5e-254">**DS-UI-configuración**</span><span class="sxs-lookup"><span data-stu-id="c4d5e-254">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



 

 





