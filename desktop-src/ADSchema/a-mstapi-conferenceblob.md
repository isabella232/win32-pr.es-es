---
title: atributo MS-TAPI-Conference-BLOB
description: Un BLOB binario de datos que describe diversas propiedades de una conferencia de multidifusión de TAPI. El formato y el contenido vienen determinados por el valor del atributo Protocol-Id en el mismo objeto. Normalmente, los datos de este BLOB se ajustan a RFC2327.
ms.assetid: f1d5baed-df3f-423e-aa2f-005e77e79725
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MS-TAPI-Conference-BLOB
- msTAPI-ConferenceBlob atributo AD Schema
topic_type:
- apiref
api_name:
- ms-TAPI-Conference-Blob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f4e3ec8b74144daca7af1788c08270d998c139c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659049"
---
# <a name="ms-tapi-conference-blob-attribute"></a><span data-ttu-id="cd625-107">atributo MS-TAPI-Conference-BLOB</span><span class="sxs-lookup"><span data-stu-id="cd625-107">ms-TAPI-Conference-Blob attribute</span></span>

<span data-ttu-id="cd625-108">Un BLOB binario de datos que describe diversas propiedades de una conferencia de multidifusión de TAPI.</span><span class="sxs-lookup"><span data-stu-id="cd625-108">A binary BLOB of data that describes various properties of a TAPI multicast conference.</span></span> <span data-ttu-id="cd625-109">El formato y el contenido vienen determinados por el valor del atributo Protocol-Id en el mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="cd625-109">Its format and content are determined by the value of the attribute Protocol-Id in the same object.</span></span> <span data-ttu-id="cd625-110">Normalmente, los datos de este BLOB se ajustan a RFC2327.</span><span class="sxs-lookup"><span data-stu-id="cd625-110">Typically, the data in this BLOB conforms to RFC2327.</span></span>



| <span data-ttu-id="cd625-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="cd625-111">Entry</span></span> | <span data-ttu-id="cd625-112">Value</span><span class="sxs-lookup"><span data-stu-id="cd625-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd625-113">CN</span><span class="sxs-lookup"><span data-stu-id="cd625-113">CN</span></span>                | <span data-ttu-id="cd625-114">MS-TAPI-Conference-BLOB</span><span class="sxs-lookup"><span data-stu-id="cd625-114">ms-TAPI-Conference-Blob</span></span>                                                                                      |
| <span data-ttu-id="cd625-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="cd625-115">Ldap-Display-Name</span></span> | <span data-ttu-id="cd625-116">msTAPI-ConferenceBlob</span><span class="sxs-lookup"><span data-stu-id="cd625-116">msTAPI-ConferenceBlob</span></span>                                                                                        |
| <span data-ttu-id="cd625-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="cd625-117">Size</span></span>              | <span data-ttu-id="cd625-118">Puede ser de longitud arbitraria.</span><span class="sxs-lookup"><span data-stu-id="cd625-118">Can be of arbitrary length.</span></span>                                                                                  |
| <span data-ttu-id="cd625-119">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="cd625-119">Update Privilege</span></span>  | <span data-ttu-id="cd625-120">No se requieren privilegios especiales.</span><span class="sxs-lookup"><span data-stu-id="cd625-120">No special privileges required.</span></span>                                                                              |
| <span data-ttu-id="cd625-121">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="cd625-121">Update Frequency</span></span>  | <span data-ttu-id="cd625-122">Puede cambiar a discreción de un propietario de la Conferencia TAPI cuando algunos datos sobre la Conferencia deben cambiar.</span><span class="sxs-lookup"><span data-stu-id="cd625-122">Can change at the discretion of a TAPI conference owner when some data about the conference needs to change.</span></span> |
| <span data-ttu-id="cd625-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cd625-123">Attribute-Id</span></span>      | <span data-ttu-id="cd625-124">1.2.840.113556.1.4.1700</span><span class="sxs-lookup"><span data-stu-id="cd625-124">1.2.840.113556.1.4.1700</span></span>                                                                                      |
| <span data-ttu-id="cd625-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cd625-125">System-Id-Guid</span></span>    | <span data-ttu-id="cd625-126">4cc4601e-7201-4141-abc8-3e529ae88863</span><span class="sxs-lookup"><span data-stu-id="cd625-126">4cc4601e-7201-4141-abc8-3e529ae88863</span></span>                                                                         |
| <span data-ttu-id="cd625-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd625-127">Syntax</span></span>            | [<span data-ttu-id="cd625-128">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="cd625-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                                        |



## <a name="implementations"></a><span data-ttu-id="cd625-129">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="cd625-129">Implementations</span></span>

-   [<span data-ttu-id="cd625-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cd625-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cd625-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cd625-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cd625-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cd625-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cd625-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cd625-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cd625-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cd625-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="cd625-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cd625-135">Windows Server 2003</span></span>



| <span data-ttu-id="cd625-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="cd625-136">Entry</span></span> | <span data-ttu-id="cd625-137">Value</span><span class="sxs-lookup"><span data-stu-id="cd625-137">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="cd625-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cd625-138">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cd625-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd625-139">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cd625-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd625-140">System-Only</span></span>            | <span data-ttu-id="cd625-141">False</span><span class="sxs-lookup"><span data-stu-id="cd625-141">False</span></span>                                                             |
| <span data-ttu-id="cd625-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cd625-142">Is-Single-Valued</span></span>       | <span data-ttu-id="cd625-143">True</span><span class="sxs-lookup"><span data-stu-id="cd625-143">True</span></span>                                                              |
| <span data-ttu-id="cd625-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cd625-144">Is Indexed</span></span>             | <span data-ttu-id="cd625-145">False</span><span class="sxs-lookup"><span data-stu-id="cd625-145">False</span></span>                                                             |
| <span data-ttu-id="cd625-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cd625-146">In Global Catalog</span></span>      | <span data-ttu-id="cd625-147">False</span><span class="sxs-lookup"><span data-stu-id="cd625-147">False</span></span>                                                             |
| <span data-ttu-id="cd625-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cd625-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd625-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd625-149">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="cd625-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd625-150">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="cd625-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd625-151">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="cd625-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd625-152">Search-Flags</span></span>           | <span data-ttu-id="cd625-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd625-153">0x00000000</span></span>                                                        |
| <span data-ttu-id="cd625-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd625-154">System-Flags</span></span>           | <span data-ttu-id="cd625-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd625-155">0x00000010</span></span>                                                        |
| <span data-ttu-id="cd625-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cd625-156">Classes used in</span></span>        | [<span data-ttu-id="cd625-157">**Microsoft-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="cd625-157">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cd625-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cd625-158">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cd625-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="cd625-159">Entry</span></span> | <span data-ttu-id="cd625-160">Value</span><span class="sxs-lookup"><span data-stu-id="cd625-160">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="cd625-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cd625-161">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cd625-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd625-162">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cd625-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd625-163">System-Only</span></span>            | <span data-ttu-id="cd625-164">False</span><span class="sxs-lookup"><span data-stu-id="cd625-164">False</span></span>                                                             |
| <span data-ttu-id="cd625-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cd625-165">Is-Single-Valued</span></span>       | <span data-ttu-id="cd625-166">True</span><span class="sxs-lookup"><span data-stu-id="cd625-166">True</span></span>                                                              |
| <span data-ttu-id="cd625-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cd625-167">Is Indexed</span></span>             | <span data-ttu-id="cd625-168">False</span><span class="sxs-lookup"><span data-stu-id="cd625-168">False</span></span>                                                             |
| <span data-ttu-id="cd625-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cd625-169">In Global Catalog</span></span>      | <span data-ttu-id="cd625-170">False</span><span class="sxs-lookup"><span data-stu-id="cd625-170">False</span></span>                                                             |
| <span data-ttu-id="cd625-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cd625-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd625-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd625-172">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="cd625-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd625-173">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="cd625-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd625-174">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="cd625-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd625-175">Search-Flags</span></span>           | <span data-ttu-id="cd625-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd625-176">0x00000000</span></span>                                                        |
| <span data-ttu-id="cd625-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd625-177">System-Flags</span></span>           | <span data-ttu-id="cd625-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd625-178">0x00000010</span></span>                                                        |
| <span data-ttu-id="cd625-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cd625-179">Classes used in</span></span>        | [<span data-ttu-id="cd625-180">**Microsoft-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="cd625-180">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cd625-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd625-181">Windows Server 2008</span></span>



| <span data-ttu-id="cd625-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="cd625-182">Entry</span></span> | <span data-ttu-id="cd625-183">Value</span><span class="sxs-lookup"><span data-stu-id="cd625-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="cd625-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cd625-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cd625-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd625-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cd625-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd625-186">System-Only</span></span>            | <span data-ttu-id="cd625-187">False</span><span class="sxs-lookup"><span data-stu-id="cd625-187">False</span></span>                                                             |
| <span data-ttu-id="cd625-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cd625-188">Is-Single-Valued</span></span>       | <span data-ttu-id="cd625-189">True</span><span class="sxs-lookup"><span data-stu-id="cd625-189">True</span></span>                                                              |
| <span data-ttu-id="cd625-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cd625-190">Is Indexed</span></span>             | <span data-ttu-id="cd625-191">False</span><span class="sxs-lookup"><span data-stu-id="cd625-191">False</span></span>                                                             |
| <span data-ttu-id="cd625-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cd625-192">In Global Catalog</span></span>      | <span data-ttu-id="cd625-193">False</span><span class="sxs-lookup"><span data-stu-id="cd625-193">False</span></span>                                                             |
| <span data-ttu-id="cd625-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cd625-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd625-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd625-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="cd625-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd625-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="cd625-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd625-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="cd625-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd625-198">Search-Flags</span></span>           | <span data-ttu-id="cd625-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd625-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="cd625-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd625-200">System-Flags</span></span>           | <span data-ttu-id="cd625-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd625-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="cd625-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cd625-202">Classes used in</span></span>        | [<span data-ttu-id="cd625-203">**Microsoft-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="cd625-203">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cd625-204">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cd625-204">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cd625-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="cd625-205">Entry</span></span> | <span data-ttu-id="cd625-206">Value</span><span class="sxs-lookup"><span data-stu-id="cd625-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="cd625-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cd625-207">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cd625-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd625-208">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cd625-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd625-209">System-Only</span></span>            | <span data-ttu-id="cd625-210">False</span><span class="sxs-lookup"><span data-stu-id="cd625-210">False</span></span>                                                             |
| <span data-ttu-id="cd625-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cd625-211">Is-Single-Valued</span></span>       | <span data-ttu-id="cd625-212">True</span><span class="sxs-lookup"><span data-stu-id="cd625-212">True</span></span>                                                              |
| <span data-ttu-id="cd625-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cd625-213">Is Indexed</span></span>             | <span data-ttu-id="cd625-214">False</span><span class="sxs-lookup"><span data-stu-id="cd625-214">False</span></span>                                                             |
| <span data-ttu-id="cd625-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cd625-215">In Global Catalog</span></span>      | <span data-ttu-id="cd625-216">False</span><span class="sxs-lookup"><span data-stu-id="cd625-216">False</span></span>                                                             |
| <span data-ttu-id="cd625-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cd625-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd625-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd625-218">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="cd625-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd625-219">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="cd625-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd625-220">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="cd625-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd625-221">Search-Flags</span></span>           | <span data-ttu-id="cd625-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd625-222">0x00000000</span></span>                                                        |
| <span data-ttu-id="cd625-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd625-223">System-Flags</span></span>           | <span data-ttu-id="cd625-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd625-224">0x00000010</span></span>                                                        |
| <span data-ttu-id="cd625-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cd625-225">Classes used in</span></span>        | [<span data-ttu-id="cd625-226">**Microsoft-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="cd625-226">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cd625-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd625-227">Windows Server 2012</span></span>



| <span data-ttu-id="cd625-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="cd625-228">Entry</span></span> | <span data-ttu-id="cd625-229">Value</span><span class="sxs-lookup"><span data-stu-id="cd625-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="cd625-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cd625-230">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cd625-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd625-231">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cd625-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd625-232">System-Only</span></span>            | <span data-ttu-id="cd625-233">False</span><span class="sxs-lookup"><span data-stu-id="cd625-233">False</span></span>                                                             |
| <span data-ttu-id="cd625-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cd625-234">Is-Single-Valued</span></span>       | <span data-ttu-id="cd625-235">True</span><span class="sxs-lookup"><span data-stu-id="cd625-235">True</span></span>                                                              |
| <span data-ttu-id="cd625-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cd625-236">Is Indexed</span></span>             | <span data-ttu-id="cd625-237">False</span><span class="sxs-lookup"><span data-stu-id="cd625-237">False</span></span>                                                             |
| <span data-ttu-id="cd625-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cd625-238">In Global Catalog</span></span>      | <span data-ttu-id="cd625-239">False</span><span class="sxs-lookup"><span data-stu-id="cd625-239">False</span></span>                                                             |
| <span data-ttu-id="cd625-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cd625-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd625-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd625-241">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="cd625-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd625-242">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="cd625-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd625-243">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="cd625-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd625-244">Search-Flags</span></span>           | <span data-ttu-id="cd625-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd625-245">0x00000000</span></span>                                                        |
| <span data-ttu-id="cd625-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd625-246">System-Flags</span></span>           | <span data-ttu-id="cd625-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd625-247">0x00000010</span></span>                                                        |
| <span data-ttu-id="cd625-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cd625-248">Classes used in</span></span>        | [<span data-ttu-id="cd625-249">**Microsoft-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="cd625-249">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



 

 





