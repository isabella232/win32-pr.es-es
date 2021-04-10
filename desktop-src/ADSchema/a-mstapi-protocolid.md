---
title: atributo MS-TAPI-Protocol-ID
description: Este atributo indica el tipo de conferencia TAPI.
ms.assetid: 6114efc3-4201-4f20-81ca-4f90a9e44f60
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-TAPI-Protocol-ID
- msTAPI-ProtocolId atributo AD Schema
topic_type:
- apiref
api_name:
- ms-TAPI-Protocol-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10538f66b98988fafa69d4fe2f3e70b47348c999
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151774"
---
# <a name="ms-tapi-protocol-id-attribute"></a><span data-ttu-id="e8641-105">atributo MS-TAPI-Protocol-ID</span><span class="sxs-lookup"><span data-stu-id="e8641-105">ms-TAPI-Protocol-Id attribute</span></span>

<span data-ttu-id="e8641-106">Este atributo indica el tipo de conferencia TAPI.</span><span class="sxs-lookup"><span data-stu-id="e8641-106">This attribute indicates the TAPI conference type.</span></span> <span data-ttu-id="e8641-107">Este atributo se usa para determinar cómo se interpreta el BLOB binario en el atributo [**MS-TAPI-Conference-BLOB**](a-mstapi-conferenceblob.md) .</span><span class="sxs-lookup"><span data-stu-id="e8641-107">This attribute is used to determine how the binary BLOB in the [**ms-TAPI-Conference-Blob**](a-mstapi-conferenceblob.md) attribute is to be interpreted.</span></span> <span data-ttu-id="e8641-108">Este atributo es una cadena arbitraria, normalmente con menos de 100 caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="e8641-108">This attribute is an arbitrary string, typically less than 100 characters in length.</span></span>



| <span data-ttu-id="e8641-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="e8641-109">Entry</span></span> | <span data-ttu-id="e8641-110">Value</span><span class="sxs-lookup"><span data-stu-id="e8641-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="e8641-111">CN</span><span class="sxs-lookup"><span data-stu-id="e8641-111">CN</span></span>                | <span data-ttu-id="e8641-112">Identificador de protocolo MS-TAPI</span><span class="sxs-lookup"><span data-stu-id="e8641-112">ms-TAPI-Protocol-Id</span></span>                                        |
| <span data-ttu-id="e8641-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="e8641-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e8641-114">msTAPI-ProtocolId</span><span class="sxs-lookup"><span data-stu-id="e8641-114">msTAPI-ProtocolId</span></span>                                          |
| <span data-ttu-id="e8641-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="e8641-115">Size</span></span>              | \-                                                         |
| <span data-ttu-id="e8641-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="e8641-116">Update Privilege</span></span>  | <span data-ttu-id="e8641-117">No se requieren privilegios especiales.</span><span class="sxs-lookup"><span data-stu-id="e8641-117">No special privileges required.</span></span>                            |
| <span data-ttu-id="e8641-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="e8641-118">Update Frequency</span></span>  | <span data-ttu-id="e8641-119">Se establece una vez en el momento de crear el objeto de Rt-Conference.</span><span class="sxs-lookup"><span data-stu-id="e8641-119">Set once at the time of creating the Rt-Conference object.</span></span> |
| <span data-ttu-id="e8641-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e8641-120">Attribute-Id</span></span>      | <span data-ttu-id="e8641-121">1.2.840.113556.1.4.1699</span><span class="sxs-lookup"><span data-stu-id="e8641-121">1.2.840.113556.1.4.1699</span></span>                                    |
| <span data-ttu-id="e8641-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e8641-122">System-Id-Guid</span></span>    | <span data-ttu-id="e8641-123">89c1ebcf-7a5f-41fd-99ca-c900b32299ab</span><span class="sxs-lookup"><span data-stu-id="e8641-123">89c1ebcf-7a5f-41fd-99ca-c900b32299ab</span></span>                       |
| <span data-ttu-id="e8641-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8641-124">Syntax</span></span>            | [<span data-ttu-id="e8641-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e8641-125">**String(Unicode)**</span></span>](s-string-unicode.md)                |



## <a name="implementations"></a><span data-ttu-id="e8641-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="e8641-126">Implementations</span></span>

-   [<span data-ttu-id="e8641-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e8641-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e8641-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e8641-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e8641-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e8641-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e8641-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e8641-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e8641-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e8641-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e8641-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e8641-132">Windows Server 2003</span></span>



| <span data-ttu-id="e8641-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="e8641-133">Entry</span></span> | <span data-ttu-id="e8641-134">Value</span><span class="sxs-lookup"><span data-stu-id="e8641-134">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="e8641-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e8641-135">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e8641-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8641-136">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e8641-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8641-137">System-Only</span></span>            | <span data-ttu-id="e8641-138">False</span><span class="sxs-lookup"><span data-stu-id="e8641-138">False</span></span>                                                             |
| <span data-ttu-id="e8641-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e8641-139">Is-Single-Valued</span></span>       | <span data-ttu-id="e8641-140">True</span><span class="sxs-lookup"><span data-stu-id="e8641-140">True</span></span>                                                              |
| <span data-ttu-id="e8641-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e8641-141">Is Indexed</span></span>             | <span data-ttu-id="e8641-142">False</span><span class="sxs-lookup"><span data-stu-id="e8641-142">False</span></span>                                                             |
| <span data-ttu-id="e8641-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e8641-143">In Global Catalog</span></span>      | <span data-ttu-id="e8641-144">False</span><span class="sxs-lookup"><span data-stu-id="e8641-144">False</span></span>                                                             |
| <span data-ttu-id="e8641-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e8641-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8641-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e8641-146">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="e8641-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8641-147">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="e8641-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8641-148">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="e8641-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8641-149">Search-Flags</span></span>           | <span data-ttu-id="e8641-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8641-150">0x00000000</span></span>                                                        |
| <span data-ttu-id="e8641-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8641-151">System-Flags</span></span>           | <span data-ttu-id="e8641-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8641-152">0x00000010</span></span>                                                        |
| <span data-ttu-id="e8641-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e8641-153">Classes used in</span></span>        | [<span data-ttu-id="e8641-154">**Microsoft-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="e8641-154">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e8641-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e8641-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e8641-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="e8641-156">Entry</span></span> | <span data-ttu-id="e8641-157">Value</span><span class="sxs-lookup"><span data-stu-id="e8641-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="e8641-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e8641-158">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e8641-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8641-159">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e8641-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8641-160">System-Only</span></span>            | <span data-ttu-id="e8641-161">False</span><span class="sxs-lookup"><span data-stu-id="e8641-161">False</span></span>                                                             |
| <span data-ttu-id="e8641-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e8641-162">Is-Single-Valued</span></span>       | <span data-ttu-id="e8641-163">True</span><span class="sxs-lookup"><span data-stu-id="e8641-163">True</span></span>                                                              |
| <span data-ttu-id="e8641-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e8641-164">Is Indexed</span></span>             | <span data-ttu-id="e8641-165">False</span><span class="sxs-lookup"><span data-stu-id="e8641-165">False</span></span>                                                             |
| <span data-ttu-id="e8641-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e8641-166">In Global Catalog</span></span>      | <span data-ttu-id="e8641-167">False</span><span class="sxs-lookup"><span data-stu-id="e8641-167">False</span></span>                                                             |
| <span data-ttu-id="e8641-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e8641-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8641-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e8641-169">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="e8641-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8641-170">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="e8641-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8641-171">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="e8641-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8641-172">Search-Flags</span></span>           | <span data-ttu-id="e8641-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8641-173">0x00000000</span></span>                                                        |
| <span data-ttu-id="e8641-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8641-174">System-Flags</span></span>           | <span data-ttu-id="e8641-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8641-175">0x00000010</span></span>                                                        |
| <span data-ttu-id="e8641-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e8641-176">Classes used in</span></span>        | [<span data-ttu-id="e8641-177">**Microsoft-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="e8641-177">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e8641-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8641-178">Windows Server 2008</span></span>



| <span data-ttu-id="e8641-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="e8641-179">Entry</span></span> | <span data-ttu-id="e8641-180">Value</span><span class="sxs-lookup"><span data-stu-id="e8641-180">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="e8641-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e8641-181">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e8641-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8641-182">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e8641-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8641-183">System-Only</span></span>            | <span data-ttu-id="e8641-184">False</span><span class="sxs-lookup"><span data-stu-id="e8641-184">False</span></span>                                                             |
| <span data-ttu-id="e8641-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e8641-185">Is-Single-Valued</span></span>       | <span data-ttu-id="e8641-186">True</span><span class="sxs-lookup"><span data-stu-id="e8641-186">True</span></span>                                                              |
| <span data-ttu-id="e8641-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e8641-187">Is Indexed</span></span>             | <span data-ttu-id="e8641-188">False</span><span class="sxs-lookup"><span data-stu-id="e8641-188">False</span></span>                                                             |
| <span data-ttu-id="e8641-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e8641-189">In Global Catalog</span></span>      | <span data-ttu-id="e8641-190">False</span><span class="sxs-lookup"><span data-stu-id="e8641-190">False</span></span>                                                             |
| <span data-ttu-id="e8641-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e8641-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8641-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e8641-192">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="e8641-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8641-193">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="e8641-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8641-194">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="e8641-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8641-195">Search-Flags</span></span>           | <span data-ttu-id="e8641-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8641-196">0x00000000</span></span>                                                        |
| <span data-ttu-id="e8641-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8641-197">System-Flags</span></span>           | <span data-ttu-id="e8641-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8641-198">0x00000010</span></span>                                                        |
| <span data-ttu-id="e8641-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e8641-199">Classes used in</span></span>        | [<span data-ttu-id="e8641-200">**Microsoft-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="e8641-200">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e8641-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e8641-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e8641-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="e8641-202">Entry</span></span> | <span data-ttu-id="e8641-203">Value</span><span class="sxs-lookup"><span data-stu-id="e8641-203">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="e8641-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e8641-204">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e8641-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8641-205">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e8641-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8641-206">System-Only</span></span>            | <span data-ttu-id="e8641-207">False</span><span class="sxs-lookup"><span data-stu-id="e8641-207">False</span></span>                                                             |
| <span data-ttu-id="e8641-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e8641-208">Is-Single-Valued</span></span>       | <span data-ttu-id="e8641-209">True</span><span class="sxs-lookup"><span data-stu-id="e8641-209">True</span></span>                                                              |
| <span data-ttu-id="e8641-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e8641-210">Is Indexed</span></span>             | <span data-ttu-id="e8641-211">False</span><span class="sxs-lookup"><span data-stu-id="e8641-211">False</span></span>                                                             |
| <span data-ttu-id="e8641-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e8641-212">In Global Catalog</span></span>      | <span data-ttu-id="e8641-213">False</span><span class="sxs-lookup"><span data-stu-id="e8641-213">False</span></span>                                                             |
| <span data-ttu-id="e8641-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e8641-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8641-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e8641-215">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="e8641-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8641-216">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="e8641-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8641-217">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="e8641-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8641-218">Search-Flags</span></span>           | <span data-ttu-id="e8641-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8641-219">0x00000000</span></span>                                                        |
| <span data-ttu-id="e8641-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8641-220">System-Flags</span></span>           | <span data-ttu-id="e8641-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8641-221">0x00000010</span></span>                                                        |
| <span data-ttu-id="e8641-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e8641-222">Classes used in</span></span>        | [<span data-ttu-id="e8641-223">**Microsoft-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="e8641-223">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e8641-224">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e8641-224">Windows Server 2012</span></span>



| <span data-ttu-id="e8641-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="e8641-225">Entry</span></span> | <span data-ttu-id="e8641-226">Value</span><span class="sxs-lookup"><span data-stu-id="e8641-226">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="e8641-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e8641-227">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e8641-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8641-228">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e8641-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8641-229">System-Only</span></span>            | <span data-ttu-id="e8641-230">False</span><span class="sxs-lookup"><span data-stu-id="e8641-230">False</span></span>                                                             |
| <span data-ttu-id="e8641-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e8641-231">Is-Single-Valued</span></span>       | <span data-ttu-id="e8641-232">True</span><span class="sxs-lookup"><span data-stu-id="e8641-232">True</span></span>                                                              |
| <span data-ttu-id="e8641-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e8641-233">Is Indexed</span></span>             | <span data-ttu-id="e8641-234">False</span><span class="sxs-lookup"><span data-stu-id="e8641-234">False</span></span>                                                             |
| <span data-ttu-id="e8641-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e8641-235">In Global Catalog</span></span>      | <span data-ttu-id="e8641-236">False</span><span class="sxs-lookup"><span data-stu-id="e8641-236">False</span></span>                                                             |
| <span data-ttu-id="e8641-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e8641-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8641-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e8641-238">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="e8641-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8641-239">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="e8641-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8641-240">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="e8641-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8641-241">Search-Flags</span></span>           | <span data-ttu-id="e8641-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8641-242">0x00000000</span></span>                                                        |
| <span data-ttu-id="e8641-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8641-243">System-Flags</span></span>           | <span data-ttu-id="e8641-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8641-244">0x00000010</span></span>                                                        |
| <span data-ttu-id="e8641-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e8641-245">Classes used in</span></span>        | [<span data-ttu-id="e8641-246">**Microsoft-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="e8641-246">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



 

 





