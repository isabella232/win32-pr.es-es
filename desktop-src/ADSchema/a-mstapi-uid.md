---
title: atributo de identificador único de MS-TAPI
description: Proporciona el nombre de una conferencia de multidifusión de TAPI. Es el atributo de nomenclatura de la clase Rt-Conference.
ms.assetid: a8162af7-0169-4381-8edc-3dbbf178e8ed
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de identificador único de MS-TAPI
- msTAPI-UID atributo AD Schema
topic_type:
- apiref
api_name:
- ms-TAPI-Unique-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 528d34d9d4282dac3f5bd5a41231094fd2666c2c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104422675"
---
# <a name="ms-tapi-unique-identifier-attribute"></a><span data-ttu-id="99c09-106">atributo de identificador único de MS-TAPI</span><span class="sxs-lookup"><span data-stu-id="99c09-106">ms-TAPI-Unique-Identifier attribute</span></span>

<span data-ttu-id="99c09-107">Proporciona el nombre de una conferencia de multidifusión de TAPI.</span><span class="sxs-lookup"><span data-stu-id="99c09-107">Provides the name of a TAPI multicast conference.</span></span> <span data-ttu-id="99c09-108">Es el atributo de nomenclatura de la clase Rt-Conference.</span><span class="sxs-lookup"><span data-stu-id="99c09-108">It is the naming attribute of the Rt-Conference class.</span></span>



| <span data-ttu-id="99c09-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="99c09-109">Entry</span></span> | <span data-ttu-id="99c09-110">Value</span><span class="sxs-lookup"><span data-stu-id="99c09-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="99c09-111">CN</span><span class="sxs-lookup"><span data-stu-id="99c09-111">CN</span></span>                | <span data-ttu-id="99c09-112">Identificador único de MS-TAPI</span><span class="sxs-lookup"><span data-stu-id="99c09-112">ms-TAPI-Unique-Identifier</span></span>                                             |
| <span data-ttu-id="99c09-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="99c09-113">Ldap-Display-Name</span></span> | <span data-ttu-id="99c09-114">msTAPI: UID</span><span class="sxs-lookup"><span data-stu-id="99c09-114">msTAPI-uid</span></span>                                                            |
| <span data-ttu-id="99c09-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="99c09-115">Size</span></span>              | <span data-ttu-id="99c09-116">Puede ser una cadena arbitraria, normalmente menos de 100 caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="99c09-116">Can be an arbitrary string, typically under 100 characters in length.</span></span> |
| <span data-ttu-id="99c09-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="99c09-117">Update Privilege</span></span>  | <span data-ttu-id="99c09-118">No se requieren privilegios especiales.</span><span class="sxs-lookup"><span data-stu-id="99c09-118">No special privileges required.</span></span>                                       |
| <span data-ttu-id="99c09-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="99c09-119">Update Frequency</span></span>  | <span data-ttu-id="99c09-120">Se establece una vez en el momento de crear el objeto de Rt-Conference.</span><span class="sxs-lookup"><span data-stu-id="99c09-120">Set once at the time of creating the Rt-Conference object.</span></span>            |
| <span data-ttu-id="99c09-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="99c09-121">Attribute-Id</span></span>      | <span data-ttu-id="99c09-122">1.2.840.113556.1.4.1698</span><span class="sxs-lookup"><span data-stu-id="99c09-122">1.2.840.113556.1.4.1698</span></span>                                               |
| <span data-ttu-id="99c09-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="99c09-123">System-Id-Guid</span></span>    | <span data-ttu-id="99c09-124">70a4e7ea-b3b9-4643-8918-e6dd2471bfd4</span><span class="sxs-lookup"><span data-stu-id="99c09-124">70a4e7ea-b3b9-4643-8918-e6dd2471bfd4</span></span>                                  |
| <span data-ttu-id="99c09-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99c09-125">Syntax</span></span>            | [<span data-ttu-id="99c09-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="99c09-126">**String(Unicode)**</span></span>](s-string-unicode.md)                           |



## <a name="implementations"></a><span data-ttu-id="99c09-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="99c09-127">Implementations</span></span>

-   [<span data-ttu-id="99c09-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="99c09-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="99c09-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="99c09-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="99c09-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="99c09-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="99c09-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="99c09-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="99c09-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="99c09-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="99c09-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="99c09-133">Windows Server 2003</span></span>



| <span data-ttu-id="99c09-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="99c09-134">Entry</span></span> | <span data-ttu-id="99c09-135">Value</span><span class="sxs-lookup"><span data-stu-id="99c09-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99c09-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="99c09-136">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="99c09-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99c09-137">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="99c09-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="99c09-138">System-Only</span></span>            | <span data-ttu-id="99c09-139">False</span><span class="sxs-lookup"><span data-stu-id="99c09-139">False</span></span>                                                                                                                       |
| <span data-ttu-id="99c09-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="99c09-140">Is-Single-Valued</span></span>       | <span data-ttu-id="99c09-141">True</span><span class="sxs-lookup"><span data-stu-id="99c09-141">True</span></span>                                                                                                                        |
| <span data-ttu-id="99c09-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="99c09-142">Is Indexed</span></span>             | <span data-ttu-id="99c09-143">False</span><span class="sxs-lookup"><span data-stu-id="99c09-143">False</span></span>                                                                                                                       |
| <span data-ttu-id="99c09-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="99c09-144">In Global Catalog</span></span>      | <span data-ttu-id="99c09-145">False</span><span class="sxs-lookup"><span data-stu-id="99c09-145">False</span></span>                                                                                                                       |
| <span data-ttu-id="99c09-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="99c09-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="99c09-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="99c09-147">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="99c09-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99c09-148">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="99c09-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99c09-149">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="99c09-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99c09-150">Search-Flags</span></span>           | <span data-ttu-id="99c09-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99c09-151">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="99c09-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99c09-152">System-Flags</span></span>           | <span data-ttu-id="99c09-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99c09-153">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="99c09-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="99c09-154">Classes used in</span></span>        | [<span data-ttu-id="99c09-155">**Microsoft-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="99c09-155">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="99c09-156">**MS-TAPI-RT-persona**</span><span class="sxs-lookup"><span data-stu-id="99c09-156">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="99c09-157">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="99c09-157">Windows Server 2003 R2</span></span>



| <span data-ttu-id="99c09-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="99c09-158">Entry</span></span> | <span data-ttu-id="99c09-159">Value</span><span class="sxs-lookup"><span data-stu-id="99c09-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99c09-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="99c09-160">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="99c09-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99c09-161">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="99c09-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="99c09-162">System-Only</span></span>            | <span data-ttu-id="99c09-163">False</span><span class="sxs-lookup"><span data-stu-id="99c09-163">False</span></span>                                                                                                                       |
| <span data-ttu-id="99c09-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="99c09-164">Is-Single-Valued</span></span>       | <span data-ttu-id="99c09-165">True</span><span class="sxs-lookup"><span data-stu-id="99c09-165">True</span></span>                                                                                                                        |
| <span data-ttu-id="99c09-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="99c09-166">Is Indexed</span></span>             | <span data-ttu-id="99c09-167">False</span><span class="sxs-lookup"><span data-stu-id="99c09-167">False</span></span>                                                                                                                       |
| <span data-ttu-id="99c09-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="99c09-168">In Global Catalog</span></span>      | <span data-ttu-id="99c09-169">False</span><span class="sxs-lookup"><span data-stu-id="99c09-169">False</span></span>                                                                                                                       |
| <span data-ttu-id="99c09-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="99c09-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="99c09-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="99c09-171">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="99c09-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99c09-172">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="99c09-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99c09-173">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="99c09-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99c09-174">Search-Flags</span></span>           | <span data-ttu-id="99c09-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99c09-175">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="99c09-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99c09-176">System-Flags</span></span>           | <span data-ttu-id="99c09-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99c09-177">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="99c09-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="99c09-178">Classes used in</span></span>        | [<span data-ttu-id="99c09-179">**Microsoft-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="99c09-179">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="99c09-180">**MS-TAPI-RT-persona**</span><span class="sxs-lookup"><span data-stu-id="99c09-180">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="99c09-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99c09-181">Windows Server 2008</span></span>



| <span data-ttu-id="99c09-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="99c09-182">Entry</span></span> | <span data-ttu-id="99c09-183">Value</span><span class="sxs-lookup"><span data-stu-id="99c09-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99c09-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="99c09-184">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="99c09-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99c09-185">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="99c09-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="99c09-186">System-Only</span></span>            | <span data-ttu-id="99c09-187">False</span><span class="sxs-lookup"><span data-stu-id="99c09-187">False</span></span>                                                                                                                       |
| <span data-ttu-id="99c09-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="99c09-188">Is-Single-Valued</span></span>       | <span data-ttu-id="99c09-189">True</span><span class="sxs-lookup"><span data-stu-id="99c09-189">True</span></span>                                                                                                                        |
| <span data-ttu-id="99c09-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="99c09-190">Is Indexed</span></span>             | <span data-ttu-id="99c09-191">False</span><span class="sxs-lookup"><span data-stu-id="99c09-191">False</span></span>                                                                                                                       |
| <span data-ttu-id="99c09-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="99c09-192">In Global Catalog</span></span>      | <span data-ttu-id="99c09-193">False</span><span class="sxs-lookup"><span data-stu-id="99c09-193">False</span></span>                                                                                                                       |
| <span data-ttu-id="99c09-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="99c09-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="99c09-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="99c09-195">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="99c09-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99c09-196">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="99c09-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99c09-197">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="99c09-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99c09-198">Search-Flags</span></span>           | <span data-ttu-id="99c09-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99c09-199">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="99c09-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99c09-200">System-Flags</span></span>           | <span data-ttu-id="99c09-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99c09-201">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="99c09-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="99c09-202">Classes used in</span></span>        | [<span data-ttu-id="99c09-203">**Microsoft-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="99c09-203">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="99c09-204">**MS-TAPI-RT-persona**</span><span class="sxs-lookup"><span data-stu-id="99c09-204">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="99c09-205">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="99c09-205">Windows Server 2008 R2</span></span>



| <span data-ttu-id="99c09-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="99c09-206">Entry</span></span> | <span data-ttu-id="99c09-207">Value</span><span class="sxs-lookup"><span data-stu-id="99c09-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99c09-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="99c09-208">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="99c09-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99c09-209">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="99c09-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="99c09-210">System-Only</span></span>            | <span data-ttu-id="99c09-211">False</span><span class="sxs-lookup"><span data-stu-id="99c09-211">False</span></span>                                                                                                                       |
| <span data-ttu-id="99c09-212">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="99c09-212">Is-Single-Valued</span></span>       | <span data-ttu-id="99c09-213">True</span><span class="sxs-lookup"><span data-stu-id="99c09-213">True</span></span>                                                                                                                        |
| <span data-ttu-id="99c09-214">Está indexado</span><span class="sxs-lookup"><span data-stu-id="99c09-214">Is Indexed</span></span>             | <span data-ttu-id="99c09-215">False</span><span class="sxs-lookup"><span data-stu-id="99c09-215">False</span></span>                                                                                                                       |
| <span data-ttu-id="99c09-216">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="99c09-216">In Global Catalog</span></span>      | <span data-ttu-id="99c09-217">False</span><span class="sxs-lookup"><span data-stu-id="99c09-217">False</span></span>                                                                                                                       |
| <span data-ttu-id="99c09-218">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="99c09-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="99c09-219">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="99c09-219">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="99c09-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99c09-220">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="99c09-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99c09-221">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="99c09-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99c09-222">Search-Flags</span></span>           | <span data-ttu-id="99c09-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99c09-223">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="99c09-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99c09-224">System-Flags</span></span>           | <span data-ttu-id="99c09-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99c09-225">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="99c09-226">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="99c09-226">Classes used in</span></span>        | [<span data-ttu-id="99c09-227">**Microsoft-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="99c09-227">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="99c09-228">**MS-TAPI-RT-persona**</span><span class="sxs-lookup"><span data-stu-id="99c09-228">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="99c09-229">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="99c09-229">Windows Server 2012</span></span>



| <span data-ttu-id="99c09-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="99c09-230">Entry</span></span> | <span data-ttu-id="99c09-231">Value</span><span class="sxs-lookup"><span data-stu-id="99c09-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99c09-232">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="99c09-232">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="99c09-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99c09-233">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="99c09-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="99c09-234">System-Only</span></span>            | <span data-ttu-id="99c09-235">False</span><span class="sxs-lookup"><span data-stu-id="99c09-235">False</span></span>                                                                                                                       |
| <span data-ttu-id="99c09-236">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="99c09-236">Is-Single-Valued</span></span>       | <span data-ttu-id="99c09-237">True</span><span class="sxs-lookup"><span data-stu-id="99c09-237">True</span></span>                                                                                                                        |
| <span data-ttu-id="99c09-238">Está indexado</span><span class="sxs-lookup"><span data-stu-id="99c09-238">Is Indexed</span></span>             | <span data-ttu-id="99c09-239">False</span><span class="sxs-lookup"><span data-stu-id="99c09-239">False</span></span>                                                                                                                       |
| <span data-ttu-id="99c09-240">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="99c09-240">In Global Catalog</span></span>      | <span data-ttu-id="99c09-241">False</span><span class="sxs-lookup"><span data-stu-id="99c09-241">False</span></span>                                                                                                                       |
| <span data-ttu-id="99c09-242">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="99c09-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="99c09-243">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="99c09-243">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="99c09-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99c09-244">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="99c09-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99c09-245">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="99c09-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99c09-246">Search-Flags</span></span>           | <span data-ttu-id="99c09-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99c09-247">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="99c09-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99c09-248">System-Flags</span></span>           | <span data-ttu-id="99c09-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99c09-249">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="99c09-250">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="99c09-250">Classes used in</span></span>        | [<span data-ttu-id="99c09-251">**Microsoft-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="99c09-251">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="99c09-252">**MS-TAPI-RT-persona**</span><span class="sxs-lookup"><span data-stu-id="99c09-252">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



 

 





