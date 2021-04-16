---
title: Atributo global-Address-List
description: Este atributo se usa en un contenedor de Microsoft Exchange para almacenar el nombre distintivo de una lista global de direcciones (GAL) recién creada.
ms.assetid: 0da2bafe-ecdf-4b75-9461-08a35151b85c
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de lista global de direcciones
- atributo globalAddressList esquema de AD
topic_type:
- apiref
api_name:
- Global-Address-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28178dfd6621593ee60e6e07043be544445cb6e7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658517"
---
# <a name="global-address-list-attribute"></a><span data-ttu-id="65527-105">Atributo global-Address-List</span><span class="sxs-lookup"><span data-stu-id="65527-105">Global-Address-List attribute</span></span>

<span data-ttu-id="65527-106">Este atributo se usa en un contenedor de Microsoft Exchange para almacenar el nombre distintivo de una lista global de direcciones (GAL) recién creada.</span><span class="sxs-lookup"><span data-stu-id="65527-106">This attribute is used on a Microsoft Exchange container to store the distinguished name of a newly created global address list (GAL).</span></span> <span data-ttu-id="65527-107">Este atributo debe tener una entrada antes de poder habilitar los clientes de la interfaz de programación de aplicaciones (MAPI) de mensajería para usar una GAL.</span><span class="sxs-lookup"><span data-stu-id="65527-107">This attribute must have an entry before you can enable Messaging Application Programming Interface (MAPI) clients to use a GAL.</span></span>



| <span data-ttu-id="65527-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="65527-108">Entry</span></span> | <span data-ttu-id="65527-109">Value</span><span class="sxs-lookup"><span data-stu-id="65527-109">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="65527-110">CN</span><span class="sxs-lookup"><span data-stu-id="65527-110">CN</span></span>                | <span data-ttu-id="65527-111">Lista global de direcciones</span><span class="sxs-lookup"><span data-stu-id="65527-111">Global-Address-List</span></span>                     |
| <span data-ttu-id="65527-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="65527-112">Ldap-Display-Name</span></span> | <span data-ttu-id="65527-113">globalAddressList</span><span class="sxs-lookup"><span data-stu-id="65527-113">globalAddressList</span></span>                       |
| <span data-ttu-id="65527-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="65527-114">Size</span></span>              | \-                                      |
| <span data-ttu-id="65527-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="65527-115">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="65527-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="65527-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="65527-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="65527-117">Attribute-Id</span></span>      | <span data-ttu-id="65527-118">1.2.840.113556.1.4.1245</span><span class="sxs-lookup"><span data-stu-id="65527-118">1.2.840.113556.1.4.1245</span></span>                 |
| <span data-ttu-id="65527-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="65527-119">System-Id-Guid</span></span>    | <span data-ttu-id="65527-120">f754c748-06f4-11d2-aa53-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="65527-120">f754c748-06f4-11d2-aa53-00c04fd7d83a</span></span>    |
| <span data-ttu-id="65527-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65527-121">Syntax</span></span>            | [<span data-ttu-id="65527-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="65527-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="65527-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="65527-123">Implementations</span></span>

-   [<span data-ttu-id="65527-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="65527-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="65527-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="65527-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="65527-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="65527-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="65527-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="65527-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="65527-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="65527-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="65527-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="65527-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="65527-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="65527-130">Windows 2000 Server</span></span>



| <span data-ttu-id="65527-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="65527-131">Entry</span></span> | <span data-ttu-id="65527-132">Value</span><span class="sxs-lookup"><span data-stu-id="65527-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="65527-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="65527-133">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="65527-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65527-134">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="65527-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="65527-135">System-Only</span></span>            | <span data-ttu-id="65527-136">False</span><span class="sxs-lookup"><span data-stu-id="65527-136">False</span></span>                                                                                |
| <span data-ttu-id="65527-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="65527-137">Is-Single-Valued</span></span>       | <span data-ttu-id="65527-138">False</span><span class="sxs-lookup"><span data-stu-id="65527-138">False</span></span>                                                                                |
| <span data-ttu-id="65527-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="65527-139">Is Indexed</span></span>             | <span data-ttu-id="65527-140">False</span><span class="sxs-lookup"><span data-stu-id="65527-140">False</span></span>                                                                                |
| <span data-ttu-id="65527-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="65527-141">In Global Catalog</span></span>      | <span data-ttu-id="65527-142">False</span><span class="sxs-lookup"><span data-stu-id="65527-142">False</span></span>                                                                                |
| <span data-ttu-id="65527-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="65527-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="65527-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65527-144">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="65527-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65527-145">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="65527-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65527-146">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="65527-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65527-147">Search-Flags</span></span>           | <span data-ttu-id="65527-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65527-148">0x00000000</span></span>                                                                           |
| <span data-ttu-id="65527-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65527-149">System-Flags</span></span>           | <span data-ttu-id="65527-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65527-150">0x00000010</span></span>                                                                           |
| <span data-ttu-id="65527-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="65527-151">Classes used in</span></span>        | [<span data-ttu-id="65527-152">**MS-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="65527-152">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="65527-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="65527-153">Windows Server 2003</span></span>



| <span data-ttu-id="65527-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="65527-154">Entry</span></span> | <span data-ttu-id="65527-155">Value</span><span class="sxs-lookup"><span data-stu-id="65527-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="65527-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="65527-156">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="65527-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65527-157">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="65527-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="65527-158">System-Only</span></span>            | <span data-ttu-id="65527-159">False</span><span class="sxs-lookup"><span data-stu-id="65527-159">False</span></span>                                                                                |
| <span data-ttu-id="65527-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="65527-160">Is-Single-Valued</span></span>       | <span data-ttu-id="65527-161">False</span><span class="sxs-lookup"><span data-stu-id="65527-161">False</span></span>                                                                                |
| <span data-ttu-id="65527-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="65527-162">Is Indexed</span></span>             | <span data-ttu-id="65527-163">False</span><span class="sxs-lookup"><span data-stu-id="65527-163">False</span></span>                                                                                |
| <span data-ttu-id="65527-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="65527-164">In Global Catalog</span></span>      | <span data-ttu-id="65527-165">False</span><span class="sxs-lookup"><span data-stu-id="65527-165">False</span></span>                                                                                |
| <span data-ttu-id="65527-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="65527-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="65527-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65527-167">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="65527-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65527-168">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="65527-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65527-169">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="65527-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65527-170">Search-Flags</span></span>           | <span data-ttu-id="65527-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65527-171">0x00000000</span></span>                                                                           |
| <span data-ttu-id="65527-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65527-172">System-Flags</span></span>           | <span data-ttu-id="65527-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65527-173">0x00000010</span></span>                                                                           |
| <span data-ttu-id="65527-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="65527-174">Classes used in</span></span>        | [<span data-ttu-id="65527-175">**MS-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="65527-175">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="65527-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="65527-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="65527-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="65527-177">Entry</span></span> | <span data-ttu-id="65527-178">Value</span><span class="sxs-lookup"><span data-stu-id="65527-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="65527-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="65527-179">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="65527-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65527-180">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="65527-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="65527-181">System-Only</span></span>            | <span data-ttu-id="65527-182">False</span><span class="sxs-lookup"><span data-stu-id="65527-182">False</span></span>                                                                                |
| <span data-ttu-id="65527-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="65527-183">Is-Single-Valued</span></span>       | <span data-ttu-id="65527-184">False</span><span class="sxs-lookup"><span data-stu-id="65527-184">False</span></span>                                                                                |
| <span data-ttu-id="65527-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="65527-185">Is Indexed</span></span>             | <span data-ttu-id="65527-186">False</span><span class="sxs-lookup"><span data-stu-id="65527-186">False</span></span>                                                                                |
| <span data-ttu-id="65527-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="65527-187">In Global Catalog</span></span>      | <span data-ttu-id="65527-188">False</span><span class="sxs-lookup"><span data-stu-id="65527-188">False</span></span>                                                                                |
| <span data-ttu-id="65527-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="65527-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="65527-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65527-190">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="65527-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65527-191">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="65527-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65527-192">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="65527-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65527-193">Search-Flags</span></span>           | <span data-ttu-id="65527-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65527-194">0x00000000</span></span>                                                                           |
| <span data-ttu-id="65527-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65527-195">System-Flags</span></span>           | <span data-ttu-id="65527-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65527-196">0x00000010</span></span>                                                                           |
| <span data-ttu-id="65527-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="65527-197">Classes used in</span></span>        | [<span data-ttu-id="65527-198">**MS-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="65527-198">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="65527-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65527-199">Windows Server 2008</span></span>



| <span data-ttu-id="65527-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="65527-200">Entry</span></span> | <span data-ttu-id="65527-201">Value</span><span class="sxs-lookup"><span data-stu-id="65527-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="65527-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="65527-202">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="65527-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65527-203">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="65527-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="65527-204">System-Only</span></span>            | <span data-ttu-id="65527-205">False</span><span class="sxs-lookup"><span data-stu-id="65527-205">False</span></span>                                                                                |
| <span data-ttu-id="65527-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="65527-206">Is-Single-Valued</span></span>       | <span data-ttu-id="65527-207">False</span><span class="sxs-lookup"><span data-stu-id="65527-207">False</span></span>                                                                                |
| <span data-ttu-id="65527-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="65527-208">Is Indexed</span></span>             | <span data-ttu-id="65527-209">False</span><span class="sxs-lookup"><span data-stu-id="65527-209">False</span></span>                                                                                |
| <span data-ttu-id="65527-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="65527-210">In Global Catalog</span></span>      | <span data-ttu-id="65527-211">False</span><span class="sxs-lookup"><span data-stu-id="65527-211">False</span></span>                                                                                |
| <span data-ttu-id="65527-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="65527-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="65527-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65527-213">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="65527-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65527-214">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="65527-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65527-215">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="65527-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65527-216">Search-Flags</span></span>           | <span data-ttu-id="65527-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65527-217">0x00000000</span></span>                                                                           |
| <span data-ttu-id="65527-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65527-218">System-Flags</span></span>           | <span data-ttu-id="65527-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65527-219">0x00000010</span></span>                                                                           |
| <span data-ttu-id="65527-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="65527-220">Classes used in</span></span>        | [<span data-ttu-id="65527-221">**MS-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="65527-221">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="65527-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="65527-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="65527-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="65527-223">Entry</span></span> | <span data-ttu-id="65527-224">Value</span><span class="sxs-lookup"><span data-stu-id="65527-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="65527-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="65527-225">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="65527-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65527-226">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="65527-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="65527-227">System-Only</span></span>            | <span data-ttu-id="65527-228">False</span><span class="sxs-lookup"><span data-stu-id="65527-228">False</span></span>                                                                                |
| <span data-ttu-id="65527-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="65527-229">Is-Single-Valued</span></span>       | <span data-ttu-id="65527-230">False</span><span class="sxs-lookup"><span data-stu-id="65527-230">False</span></span>                                                                                |
| <span data-ttu-id="65527-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="65527-231">Is Indexed</span></span>             | <span data-ttu-id="65527-232">False</span><span class="sxs-lookup"><span data-stu-id="65527-232">False</span></span>                                                                                |
| <span data-ttu-id="65527-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="65527-233">In Global Catalog</span></span>      | <span data-ttu-id="65527-234">False</span><span class="sxs-lookup"><span data-stu-id="65527-234">False</span></span>                                                                                |
| <span data-ttu-id="65527-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="65527-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="65527-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65527-236">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="65527-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65527-237">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="65527-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65527-238">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="65527-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65527-239">Search-Flags</span></span>           | <span data-ttu-id="65527-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65527-240">0x00000000</span></span>                                                                           |
| <span data-ttu-id="65527-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65527-241">System-Flags</span></span>           | <span data-ttu-id="65527-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65527-242">0x00000010</span></span>                                                                           |
| <span data-ttu-id="65527-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="65527-243">Classes used in</span></span>        | [<span data-ttu-id="65527-244">**MS-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="65527-244">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="65527-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="65527-245">Windows Server 2012</span></span>



| <span data-ttu-id="65527-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="65527-246">Entry</span></span> | <span data-ttu-id="65527-247">Value</span><span class="sxs-lookup"><span data-stu-id="65527-247">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="65527-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="65527-248">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="65527-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65527-249">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="65527-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="65527-250">System-Only</span></span>            | <span data-ttu-id="65527-251">False</span><span class="sxs-lookup"><span data-stu-id="65527-251">False</span></span>                                                                                |
| <span data-ttu-id="65527-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="65527-252">Is-Single-Valued</span></span>       | <span data-ttu-id="65527-253">False</span><span class="sxs-lookup"><span data-stu-id="65527-253">False</span></span>                                                                                |
| <span data-ttu-id="65527-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="65527-254">Is Indexed</span></span>             | <span data-ttu-id="65527-255">False</span><span class="sxs-lookup"><span data-stu-id="65527-255">False</span></span>                                                                                |
| <span data-ttu-id="65527-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="65527-256">In Global Catalog</span></span>      | <span data-ttu-id="65527-257">False</span><span class="sxs-lookup"><span data-stu-id="65527-257">False</span></span>                                                                                |
| <span data-ttu-id="65527-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="65527-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="65527-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65527-259">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="65527-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65527-260">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="65527-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65527-261">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="65527-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65527-262">Search-Flags</span></span>           | <span data-ttu-id="65527-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65527-263">0x00000000</span></span>                                                                           |
| <span data-ttu-id="65527-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65527-264">System-Flags</span></span>           | <span data-ttu-id="65527-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65527-265">0x00000010</span></span>                                                                           |
| <span data-ttu-id="65527-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="65527-266">Classes used in</span></span>        | [<span data-ttu-id="65527-267">**MS-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="65527-267">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





