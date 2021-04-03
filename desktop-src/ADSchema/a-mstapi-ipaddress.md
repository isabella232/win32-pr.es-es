---
title: atributo MS-TAPI-IP-address
description: Direcciones IP de un equipo cliente TAPI en el que un usuario ha iniciado sesión. Este atributo se puede utilizar como atributo genérico para almacenar las direcciones IP del equipo.
ms.assetid: 4ea850ad-d54a-4b5f-a37d-68817432d874
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-TAPI-IP-address
- msTAPI-IpAddress Attribute AD Schema
topic_type:
- apiref
api_name:
- ms-TAPI-Ip-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078afde8200468df7e996e096deeef4bfd1b7ec0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997407"
---
# <a name="ms-tapi-ip-address-attribute"></a><span data-ttu-id="5e408-106">atributo MS-TAPI-IP-address</span><span class="sxs-lookup"><span data-stu-id="5e408-106">ms-TAPI-Ip-Address attribute</span></span>

<span data-ttu-id="5e408-107">Direcciones IP de un equipo cliente TAPI en el que un usuario ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="5e408-107">IP addresses of a TAPI client computer that a user is logged into.</span></span> <span data-ttu-id="5e408-108">Este atributo se puede utilizar como atributo genérico para almacenar las direcciones IP del equipo.</span><span class="sxs-lookup"><span data-stu-id="5e408-108">This attribute can be used as a generic attribute to hold computer IP addresses.</span></span>



| <span data-ttu-id="5e408-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="5e408-109">Entry</span></span> | <span data-ttu-id="5e408-110">Value</span><span class="sxs-lookup"><span data-stu-id="5e408-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="5e408-111">CN</span><span class="sxs-lookup"><span data-stu-id="5e408-111">CN</span></span>                | <span data-ttu-id="5e408-112">Dirección IP de MS-TAPI</span><span class="sxs-lookup"><span data-stu-id="5e408-112">ms-TAPI-Ip-Address</span></span>                                         |
| <span data-ttu-id="5e408-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="5e408-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5e408-114">msTAPI-IpAddress</span><span class="sxs-lookup"><span data-stu-id="5e408-114">msTAPI-IpAddress</span></span>                                           |
| <span data-ttu-id="5e408-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="5e408-115">Size</span></span>              | <span data-ttu-id="5e408-116">Cada dirección IP se almacena como una cadena en una notación. B. C. D.</span><span class="sxs-lookup"><span data-stu-id="5e408-116">Each IP address is stored as a string in A.B.C.D notation.</span></span> |
| <span data-ttu-id="5e408-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="5e408-117">Update Privilege</span></span>  | <span data-ttu-id="5e408-118">No se requieren privilegios especiales.</span><span class="sxs-lookup"><span data-stu-id="5e408-118">No special privileges required.</span></span>                            |
| <span data-ttu-id="5e408-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="5e408-119">Update Frequency</span></span>  | <span data-ttu-id="5e408-120">Normalmente es muy baja.</span><span class="sxs-lookup"><span data-stu-id="5e408-120">Typically very low.</span></span>                                        |
| <span data-ttu-id="5e408-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5e408-121">Attribute-Id</span></span>      | <span data-ttu-id="5e408-122">1.2.840.113556.1.4.1701</span><span class="sxs-lookup"><span data-stu-id="5e408-122">1.2.840.113556.1.4.1701</span></span>                                    |
| <span data-ttu-id="5e408-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5e408-123">System-Id-Guid</span></span>    | <span data-ttu-id="5e408-124">efd7d7f7-178e-4767-87fa-f8a16b840544</span><span class="sxs-lookup"><span data-stu-id="5e408-124">efd7d7f7-178e-4767-87fa-f8a16b840544</span></span>                       |
| <span data-ttu-id="5e408-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e408-125">Syntax</span></span>            | [<span data-ttu-id="5e408-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5e408-126">**String(Unicode)**</span></span>](s-string-unicode.md)                |



## <a name="implementations"></a><span data-ttu-id="5e408-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="5e408-127">Implementations</span></span>

-   [<span data-ttu-id="5e408-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5e408-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5e408-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5e408-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5e408-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5e408-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5e408-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5e408-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5e408-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5e408-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="5e408-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5e408-133">Windows Server 2003</span></span>



| <span data-ttu-id="5e408-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="5e408-134">Entry</span></span> | <span data-ttu-id="5e408-135">Value</span><span class="sxs-lookup"><span data-stu-id="5e408-135">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="5e408-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5e408-136">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="5e408-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5e408-137">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="5e408-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="5e408-138">System-Only</span></span>            | <span data-ttu-id="5e408-139">False</span><span class="sxs-lookup"><span data-stu-id="5e408-139">False</span></span>                                                     |
| <span data-ttu-id="5e408-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5e408-140">Is-Single-Valued</span></span>       | <span data-ttu-id="5e408-141">False</span><span class="sxs-lookup"><span data-stu-id="5e408-141">False</span></span>                                                     |
| <span data-ttu-id="5e408-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5e408-142">Is Indexed</span></span>             | <span data-ttu-id="5e408-143">False</span><span class="sxs-lookup"><span data-stu-id="5e408-143">False</span></span>                                                     |
| <span data-ttu-id="5e408-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5e408-144">In Global Catalog</span></span>      | <span data-ttu-id="5e408-145">False</span><span class="sxs-lookup"><span data-stu-id="5e408-145">False</span></span>                                                     |
| <span data-ttu-id="5e408-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5e408-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="5e408-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5e408-147">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="5e408-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5e408-148">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="5e408-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5e408-149">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="5e408-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5e408-150">Search-Flags</span></span>           | <span data-ttu-id="5e408-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5e408-151">0x00000000</span></span>                                                |
| <span data-ttu-id="5e408-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5e408-152">System-Flags</span></span>           | <span data-ttu-id="5e408-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5e408-153">0x00000010</span></span>                                                |
| <span data-ttu-id="5e408-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5e408-154">Classes used in</span></span>        | [<span data-ttu-id="5e408-155">**MS-TAPI-RT-persona**</span><span class="sxs-lookup"><span data-stu-id="5e408-155">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5e408-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5e408-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5e408-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="5e408-157">Entry</span></span> | <span data-ttu-id="5e408-158">Value</span><span class="sxs-lookup"><span data-stu-id="5e408-158">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="5e408-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5e408-159">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="5e408-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5e408-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="5e408-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="5e408-161">System-Only</span></span>            | <span data-ttu-id="5e408-162">False</span><span class="sxs-lookup"><span data-stu-id="5e408-162">False</span></span>                                                     |
| <span data-ttu-id="5e408-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5e408-163">Is-Single-Valued</span></span>       | <span data-ttu-id="5e408-164">False</span><span class="sxs-lookup"><span data-stu-id="5e408-164">False</span></span>                                                     |
| <span data-ttu-id="5e408-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5e408-165">Is Indexed</span></span>             | <span data-ttu-id="5e408-166">False</span><span class="sxs-lookup"><span data-stu-id="5e408-166">False</span></span>                                                     |
| <span data-ttu-id="5e408-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5e408-167">In Global Catalog</span></span>      | <span data-ttu-id="5e408-168">False</span><span class="sxs-lookup"><span data-stu-id="5e408-168">False</span></span>                                                     |
| <span data-ttu-id="5e408-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5e408-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="5e408-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5e408-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="5e408-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5e408-171">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="5e408-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5e408-172">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="5e408-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5e408-173">Search-Flags</span></span>           | <span data-ttu-id="5e408-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5e408-174">0x00000000</span></span>                                                |
| <span data-ttu-id="5e408-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5e408-175">System-Flags</span></span>           | <span data-ttu-id="5e408-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5e408-176">0x00000010</span></span>                                                |
| <span data-ttu-id="5e408-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5e408-177">Classes used in</span></span>        | [<span data-ttu-id="5e408-178">**MS-TAPI-RT-persona**</span><span class="sxs-lookup"><span data-stu-id="5e408-178">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5e408-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e408-179">Windows Server 2008</span></span>



| <span data-ttu-id="5e408-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="5e408-180">Entry</span></span> | <span data-ttu-id="5e408-181">Value</span><span class="sxs-lookup"><span data-stu-id="5e408-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="5e408-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5e408-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="5e408-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5e408-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="5e408-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="5e408-184">System-Only</span></span>            | <span data-ttu-id="5e408-185">False</span><span class="sxs-lookup"><span data-stu-id="5e408-185">False</span></span>                                                     |
| <span data-ttu-id="5e408-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5e408-186">Is-Single-Valued</span></span>       | <span data-ttu-id="5e408-187">False</span><span class="sxs-lookup"><span data-stu-id="5e408-187">False</span></span>                                                     |
| <span data-ttu-id="5e408-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5e408-188">Is Indexed</span></span>             | <span data-ttu-id="5e408-189">False</span><span class="sxs-lookup"><span data-stu-id="5e408-189">False</span></span>                                                     |
| <span data-ttu-id="5e408-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5e408-190">In Global Catalog</span></span>      | <span data-ttu-id="5e408-191">False</span><span class="sxs-lookup"><span data-stu-id="5e408-191">False</span></span>                                                     |
| <span data-ttu-id="5e408-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5e408-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="5e408-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5e408-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="5e408-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5e408-194">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="5e408-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5e408-195">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="5e408-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5e408-196">Search-Flags</span></span>           | <span data-ttu-id="5e408-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5e408-197">0x00000000</span></span>                                                |
| <span data-ttu-id="5e408-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5e408-198">System-Flags</span></span>           | <span data-ttu-id="5e408-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5e408-199">0x00000010</span></span>                                                |
| <span data-ttu-id="5e408-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5e408-200">Classes used in</span></span>        | [<span data-ttu-id="5e408-201">**MS-TAPI-RT-persona**</span><span class="sxs-lookup"><span data-stu-id="5e408-201">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5e408-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5e408-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5e408-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="5e408-203">Entry</span></span> | <span data-ttu-id="5e408-204">Value</span><span class="sxs-lookup"><span data-stu-id="5e408-204">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="5e408-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5e408-205">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="5e408-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5e408-206">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="5e408-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="5e408-207">System-Only</span></span>            | <span data-ttu-id="5e408-208">False</span><span class="sxs-lookup"><span data-stu-id="5e408-208">False</span></span>                                                     |
| <span data-ttu-id="5e408-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5e408-209">Is-Single-Valued</span></span>       | <span data-ttu-id="5e408-210">False</span><span class="sxs-lookup"><span data-stu-id="5e408-210">False</span></span>                                                     |
| <span data-ttu-id="5e408-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5e408-211">Is Indexed</span></span>             | <span data-ttu-id="5e408-212">False</span><span class="sxs-lookup"><span data-stu-id="5e408-212">False</span></span>                                                     |
| <span data-ttu-id="5e408-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5e408-213">In Global Catalog</span></span>      | <span data-ttu-id="5e408-214">False</span><span class="sxs-lookup"><span data-stu-id="5e408-214">False</span></span>                                                     |
| <span data-ttu-id="5e408-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5e408-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="5e408-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5e408-216">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="5e408-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5e408-217">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="5e408-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5e408-218">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="5e408-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5e408-219">Search-Flags</span></span>           | <span data-ttu-id="5e408-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5e408-220">0x00000000</span></span>                                                |
| <span data-ttu-id="5e408-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5e408-221">System-Flags</span></span>           | <span data-ttu-id="5e408-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5e408-222">0x00000010</span></span>                                                |
| <span data-ttu-id="5e408-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5e408-223">Classes used in</span></span>        | [<span data-ttu-id="5e408-224">**MS-TAPI-RT-persona**</span><span class="sxs-lookup"><span data-stu-id="5e408-224">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5e408-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5e408-225">Windows Server 2012</span></span>



| <span data-ttu-id="5e408-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="5e408-226">Entry</span></span> | <span data-ttu-id="5e408-227">Value</span><span class="sxs-lookup"><span data-stu-id="5e408-227">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="5e408-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5e408-228">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="5e408-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5e408-229">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="5e408-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="5e408-230">System-Only</span></span>            | <span data-ttu-id="5e408-231">False</span><span class="sxs-lookup"><span data-stu-id="5e408-231">False</span></span>                                                     |
| <span data-ttu-id="5e408-232">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5e408-232">Is-Single-Valued</span></span>       | <span data-ttu-id="5e408-233">False</span><span class="sxs-lookup"><span data-stu-id="5e408-233">False</span></span>                                                     |
| <span data-ttu-id="5e408-234">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5e408-234">Is Indexed</span></span>             | <span data-ttu-id="5e408-235">False</span><span class="sxs-lookup"><span data-stu-id="5e408-235">False</span></span>                                                     |
| <span data-ttu-id="5e408-236">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5e408-236">In Global Catalog</span></span>      | <span data-ttu-id="5e408-237">False</span><span class="sxs-lookup"><span data-stu-id="5e408-237">False</span></span>                                                     |
| <span data-ttu-id="5e408-238">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5e408-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="5e408-239">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5e408-239">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="5e408-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5e408-240">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="5e408-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5e408-241">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="5e408-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5e408-242">Search-Flags</span></span>           | <span data-ttu-id="5e408-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5e408-243">0x00000000</span></span>                                                |
| <span data-ttu-id="5e408-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5e408-244">System-Flags</span></span>           | <span data-ttu-id="5e408-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5e408-245">0x00000010</span></span>                                                |
| <span data-ttu-id="5e408-246">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5e408-246">Classes used in</span></span>        | [<span data-ttu-id="5e408-247">**MS-TAPI-RT-persona**</span><span class="sxs-lookup"><span data-stu-id="5e408-247">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



 

 





