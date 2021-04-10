---
title: msSFU-30-Order-número atributo
description: Contiene un valor que usa NIS para comprobar si el mapa ha cambiado.
ms.assetid: b2e83980-2de4-4001-b65a-8073c9258b27
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de número msSFU-30-Order-
- msSFU30OrderNumber esquema de AD de atributos
topic_type:
- apiref
api_name:
- msSFU-30-Order-Number
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af67f1b5d6fdff8ca4a7739276443d67fa35679f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151627"
---
# <a name="mssfu-30-order-number-attribute"></a><span data-ttu-id="6c2b3-105">msSFU-30-Order-número atributo</span><span class="sxs-lookup"><span data-stu-id="6c2b3-105">msSFU-30-Order-Number attribute</span></span>

<span data-ttu-id="6c2b3-106">Contiene un valor que usa NIS para comprobar si el mapa ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-106">Contains a value that is used by NIS to check if the map has changed.</span></span> <span data-ttu-id="6c2b3-107">Cada vez que los datos almacenados en el objeto [**msSFU-30-Domain-info**](c-mssfu30domaininfo.md) cambian, se incrementa este valor.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-107">Every time the data stored in the [**msSFU-30-Domain-Info**](c-mssfu30domaininfo.md) object changes, this value is incremented.</span></span> <span data-ttu-id="6c2b3-108">Este valor se usa para realizar el seguimiento de los cambios de datos entre llamadas a **ypxfer** .</span><span class="sxs-lookup"><span data-stu-id="6c2b3-108">This value is used to track data changes between **ypxfer** calls.</span></span>



| <span data-ttu-id="6c2b3-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c2b3-109">Entry</span></span> | <span data-ttu-id="6c2b3-110">Value</span><span class="sxs-lookup"><span data-stu-id="6c2b3-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6c2b3-111">CN</span><span class="sxs-lookup"><span data-stu-id="6c2b3-111">CN</span></span>                | <span data-ttu-id="6c2b3-112">msSFU-30-número de orden</span><span class="sxs-lookup"><span data-stu-id="6c2b3-112">msSFU-30-Order-Number</span></span>                       |
| <span data-ttu-id="6c2b3-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="6c2b3-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6c2b3-114">msSFU30OrderNumber</span><span class="sxs-lookup"><span data-stu-id="6c2b3-114">msSFU30OrderNumber</span></span>                          |
| <span data-ttu-id="6c2b3-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="6c2b3-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="6c2b3-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="6c2b3-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="6c2b3-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="6c2b3-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="6c2b3-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6c2b3-118">Attribute-Id</span></span>      | <span data-ttu-id="6c2b3-119">1.2.840.113556.1.6.18.1.308</span><span class="sxs-lookup"><span data-stu-id="6c2b3-119">1.2.840.113556.1.6.18.1.308</span></span>                 |
| <span data-ttu-id="6c2b3-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6c2b3-120">System-Id-Guid</span></span>    | <span data-ttu-id="6c2b3-121">02625f05-d1ee-4f9f-b366-55266becb95c</span><span class="sxs-lookup"><span data-stu-id="6c2b3-121">02625f05-d1ee-4f9f-b366-55266becb95c</span></span>        |
| <span data-ttu-id="6c2b3-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c2b3-122">Syntax</span></span>            | [<span data-ttu-id="6c2b3-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6c2b3-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6c2b3-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="6c2b3-124">Implementations</span></span>

-   [<span data-ttu-id="6c2b3-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6c2b3-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6c2b3-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6c2b3-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6c2b3-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6c2b3-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6c2b3-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6c2b3-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003-r2"></a><span data-ttu-id="6c2b3-129">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6c2b3-129">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6c2b3-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c2b3-130">Entry</span></span> | <span data-ttu-id="6c2b3-131">Value</span><span class="sxs-lookup"><span data-stu-id="6c2b3-131">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="6c2b3-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6c2b3-132">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="6c2b3-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c2b3-133">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="6c2b3-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c2b3-134">System-Only</span></span>            | <span data-ttu-id="6c2b3-135">False</span><span class="sxs-lookup"><span data-stu-id="6c2b3-135">False</span></span>                                                          |
| <span data-ttu-id="6c2b3-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6c2b3-136">Is-Single-Valued</span></span>       | <span data-ttu-id="6c2b3-137">True</span><span class="sxs-lookup"><span data-stu-id="6c2b3-137">True</span></span>                                                           |
| <span data-ttu-id="6c2b3-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6c2b3-138">Is Indexed</span></span>             | <span data-ttu-id="6c2b3-139">True</span><span class="sxs-lookup"><span data-stu-id="6c2b3-139">True</span></span>                                                           |
| <span data-ttu-id="6c2b3-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6c2b3-140">In Global Catalog</span></span>      | <span data-ttu-id="6c2b3-141">False</span><span class="sxs-lookup"><span data-stu-id="6c2b3-141">False</span></span>                                                          |
| <span data-ttu-id="6c2b3-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6c2b3-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c2b3-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c2b3-143">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="6c2b3-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c2b3-144">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="6c2b3-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c2b3-145">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="6c2b3-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c2b3-146">Search-Flags</span></span>           | <span data-ttu-id="6c2b3-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6c2b3-147">0x00000001</span></span>                                                     |
| <span data-ttu-id="6c2b3-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c2b3-148">System-Flags</span></span>           | <span data-ttu-id="6c2b3-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c2b3-149">0x00000000</span></span>                                                     |
| <span data-ttu-id="6c2b3-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6c2b3-150">Classes used in</span></span>        | [<span data-ttu-id="6c2b3-151">**msSFU-30-Domain-info**</span><span class="sxs-lookup"><span data-stu-id="6c2b3-151">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6c2b3-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c2b3-152">Windows Server 2008</span></span>



| <span data-ttu-id="6c2b3-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c2b3-153">Entry</span></span> | <span data-ttu-id="6c2b3-154">Value</span><span class="sxs-lookup"><span data-stu-id="6c2b3-154">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="6c2b3-155">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6c2b3-155">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="6c2b3-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c2b3-156">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="6c2b3-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c2b3-157">System-Only</span></span>            | <span data-ttu-id="6c2b3-158">False</span><span class="sxs-lookup"><span data-stu-id="6c2b3-158">False</span></span>                                                          |
| <span data-ttu-id="6c2b3-159">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6c2b3-159">Is-Single-Valued</span></span>       | <span data-ttu-id="6c2b3-160">True</span><span class="sxs-lookup"><span data-stu-id="6c2b3-160">True</span></span>                                                           |
| <span data-ttu-id="6c2b3-161">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6c2b3-161">Is Indexed</span></span>             | <span data-ttu-id="6c2b3-162">True</span><span class="sxs-lookup"><span data-stu-id="6c2b3-162">True</span></span>                                                           |
| <span data-ttu-id="6c2b3-163">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6c2b3-163">In Global Catalog</span></span>      | <span data-ttu-id="6c2b3-164">False</span><span class="sxs-lookup"><span data-stu-id="6c2b3-164">False</span></span>                                                          |
| <span data-ttu-id="6c2b3-165">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6c2b3-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c2b3-166">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c2b3-166">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="6c2b3-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c2b3-167">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="6c2b3-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c2b3-168">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="6c2b3-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c2b3-169">Search-Flags</span></span>           | <span data-ttu-id="6c2b3-170">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6c2b3-170">0x00000001</span></span>                                                     |
| <span data-ttu-id="6c2b3-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c2b3-171">System-Flags</span></span>           | <span data-ttu-id="6c2b3-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c2b3-172">0x00000000</span></span>                                                     |
| <span data-ttu-id="6c2b3-173">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6c2b3-173">Classes used in</span></span>        | [<span data-ttu-id="6c2b3-174">**msSFU-30-Domain-info**</span><span class="sxs-lookup"><span data-stu-id="6c2b3-174">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6c2b3-175">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6c2b3-175">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6c2b3-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c2b3-176">Entry</span></span> | <span data-ttu-id="6c2b3-177">Value</span><span class="sxs-lookup"><span data-stu-id="6c2b3-177">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="6c2b3-178">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6c2b3-178">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="6c2b3-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c2b3-179">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="6c2b3-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c2b3-180">System-Only</span></span>            | <span data-ttu-id="6c2b3-181">False</span><span class="sxs-lookup"><span data-stu-id="6c2b3-181">False</span></span>                                                          |
| <span data-ttu-id="6c2b3-182">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6c2b3-182">Is-Single-Valued</span></span>       | <span data-ttu-id="6c2b3-183">True</span><span class="sxs-lookup"><span data-stu-id="6c2b3-183">True</span></span>                                                           |
| <span data-ttu-id="6c2b3-184">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6c2b3-184">Is Indexed</span></span>             | <span data-ttu-id="6c2b3-185">True</span><span class="sxs-lookup"><span data-stu-id="6c2b3-185">True</span></span>                                                           |
| <span data-ttu-id="6c2b3-186">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6c2b3-186">In Global Catalog</span></span>      | <span data-ttu-id="6c2b3-187">False</span><span class="sxs-lookup"><span data-stu-id="6c2b3-187">False</span></span>                                                          |
| <span data-ttu-id="6c2b3-188">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6c2b3-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c2b3-189">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c2b3-189">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="6c2b3-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c2b3-190">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="6c2b3-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c2b3-191">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="6c2b3-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c2b3-192">Search-Flags</span></span>           | <span data-ttu-id="6c2b3-193">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6c2b3-193">0x00000001</span></span>                                                     |
| <span data-ttu-id="6c2b3-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c2b3-194">System-Flags</span></span>           | <span data-ttu-id="6c2b3-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c2b3-195">0x00000000</span></span>                                                     |
| <span data-ttu-id="6c2b3-196">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6c2b3-196">Classes used in</span></span>        | [<span data-ttu-id="6c2b3-197">**msSFU-30-Domain-info**</span><span class="sxs-lookup"><span data-stu-id="6c2b3-197">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6c2b3-198">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6c2b3-198">Windows Server 2012</span></span>



| <span data-ttu-id="6c2b3-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c2b3-199">Entry</span></span> | <span data-ttu-id="6c2b3-200">Value</span><span class="sxs-lookup"><span data-stu-id="6c2b3-200">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="6c2b3-201">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6c2b3-201">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="6c2b3-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c2b3-202">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="6c2b3-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c2b3-203">System-Only</span></span>            | <span data-ttu-id="6c2b3-204">False</span><span class="sxs-lookup"><span data-stu-id="6c2b3-204">False</span></span>                                                          |
| <span data-ttu-id="6c2b3-205">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6c2b3-205">Is-Single-Valued</span></span>       | <span data-ttu-id="6c2b3-206">True</span><span class="sxs-lookup"><span data-stu-id="6c2b3-206">True</span></span>                                                           |
| <span data-ttu-id="6c2b3-207">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6c2b3-207">Is Indexed</span></span>             | <span data-ttu-id="6c2b3-208">True</span><span class="sxs-lookup"><span data-stu-id="6c2b3-208">True</span></span>                                                           |
| <span data-ttu-id="6c2b3-209">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6c2b3-209">In Global Catalog</span></span>      | <span data-ttu-id="6c2b3-210">False</span><span class="sxs-lookup"><span data-stu-id="6c2b3-210">False</span></span>                                                          |
| <span data-ttu-id="6c2b3-211">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6c2b3-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c2b3-212">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c2b3-212">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="6c2b3-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c2b3-213">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="6c2b3-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c2b3-214">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="6c2b3-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c2b3-215">Search-Flags</span></span>           | <span data-ttu-id="6c2b3-216">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6c2b3-216">0x00000001</span></span>                                                     |
| <span data-ttu-id="6c2b3-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c2b3-217">System-Flags</span></span>           | <span data-ttu-id="6c2b3-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c2b3-218">0x00000000</span></span>                                                     |
| <span data-ttu-id="6c2b3-219">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6c2b3-219">Classes used in</span></span>        | [<span data-ttu-id="6c2b3-220">**msSFU-30-Domain-info**</span><span class="sxs-lookup"><span data-stu-id="6c2b3-220">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



 

 





