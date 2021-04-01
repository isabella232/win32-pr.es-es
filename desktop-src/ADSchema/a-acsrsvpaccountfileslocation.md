---
title: Atributo ACS-RSVP-Account-files-Location
description: Ubicación del directorio de los archivos de cuenta RSVP. El valor predeterminado es \ 0034; system32 \ 0034; subdirectorio ubicado en el directorio predeterminado del sistema.
ms.assetid: 84303766-0d17-4728-aa61-6a5377b7de04
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de ubicación ACS-RSVP-Account-files
- aCSRSVPAccountFilesLocation esquema de AD de atributos
topic_type:
- apiref
api_name:
- ACS-RSVP-Account-Files-Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40876018ffeeacc49fe666ab1a9d69363edb73c4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906280"
---
# <a name="acs-rsvp-account-files-location-attribute"></a><span data-ttu-id="a9d64-106">Atributo ACS-RSVP-Account-files-Location</span><span class="sxs-lookup"><span data-stu-id="a9d64-106">ACS-RSVP-Account-Files-Location attribute</span></span>

<span data-ttu-id="a9d64-107">Ubicación del directorio de los archivos de cuenta RSVP.</span><span class="sxs-lookup"><span data-stu-id="a9d64-107">The directory location of RSVP account files.</span></span> <span data-ttu-id="a9d64-108">Tiene como valor predeterminado el subdirectorio "system32" que se encuentra en el directorio predeterminado del sistema.</span><span class="sxs-lookup"><span data-stu-id="a9d64-108">Defaults to the "system32" subdirectory located in the default system directory.</span></span>



| <span data-ttu-id="a9d64-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="a9d64-109">Entry</span></span> | <span data-ttu-id="a9d64-110">Value</span><span class="sxs-lookup"><span data-stu-id="a9d64-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a9d64-111">CN</span><span class="sxs-lookup"><span data-stu-id="a9d64-111">CN</span></span>                | <span data-ttu-id="a9d64-112">ACS-RSVP-Account-files-Location</span><span class="sxs-lookup"><span data-stu-id="a9d64-112">ACS-RSVP-Account-Files-Location</span></span>             |
| <span data-ttu-id="a9d64-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="a9d64-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a9d64-114">aCSRSVPAccountFilesLocation</span><span class="sxs-lookup"><span data-stu-id="a9d64-114">aCSRSVPAccountFilesLocation</span></span>                 |
| <span data-ttu-id="a9d64-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a9d64-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="a9d64-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="a9d64-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="a9d64-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="a9d64-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="a9d64-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a9d64-118">Attribute-Id</span></span>      | <span data-ttu-id="a9d64-119">1.2.840.113556.1.4.900</span><span class="sxs-lookup"><span data-stu-id="a9d64-119">1.2.840.113556.1.4.900</span></span>                      |
| <span data-ttu-id="a9d64-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a9d64-120">System-Id-Guid</span></span>    | <span data-ttu-id="a9d64-121">f072230f-aef5-11d1-bdcf-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a9d64-121">f072230f-aef5-11d1-bdcf-0000f80367c1</span></span>        |
| <span data-ttu-id="a9d64-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9d64-122">Syntax</span></span>            | [<span data-ttu-id="a9d64-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a9d64-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a9d64-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="a9d64-124">Implementations</span></span>

-   [<span data-ttu-id="a9d64-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a9d64-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a9d64-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a9d64-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a9d64-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a9d64-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a9d64-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a9d64-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a9d64-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a9d64-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a9d64-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a9d64-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a9d64-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a9d64-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a9d64-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="a9d64-132">Entry</span></span> | <span data-ttu-id="a9d64-133">Value</span><span class="sxs-lookup"><span data-stu-id="a9d64-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a9d64-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a9d64-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9d64-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9d64-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9d64-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9d64-136">System-Only</span></span>            | <span data-ttu-id="a9d64-137">False</span><span class="sxs-lookup"><span data-stu-id="a9d64-137">False</span></span>                                        |
| <span data-ttu-id="a9d64-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a9d64-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a9d64-139">True</span><span class="sxs-lookup"><span data-stu-id="a9d64-139">True</span></span>                                         |
| <span data-ttu-id="a9d64-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a9d64-140">Is Indexed</span></span>             | <span data-ttu-id="a9d64-141">False</span><span class="sxs-lookup"><span data-stu-id="a9d64-141">False</span></span>                                        |
| <span data-ttu-id="a9d64-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a9d64-142">In Global Catalog</span></span>      | <span data-ttu-id="a9d64-143">False</span><span class="sxs-lookup"><span data-stu-id="a9d64-143">False</span></span>                                        |
| <span data-ttu-id="a9d64-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a9d64-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9d64-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a9d64-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a9d64-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9d64-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a9d64-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9d64-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a9d64-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d64-148">Search-Flags</span></span>           | <span data-ttu-id="a9d64-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9d64-149">0x00000000</span></span>                                   |
| <span data-ttu-id="a9d64-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d64-150">System-Flags</span></span>           | <span data-ttu-id="a9d64-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9d64-151">0x00000010</span></span>                                   |
| <span data-ttu-id="a9d64-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a9d64-152">Classes used in</span></span>        | [<span data-ttu-id="a9d64-153">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="a9d64-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a9d64-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a9d64-154">Windows Server 2003</span></span>



| <span data-ttu-id="a9d64-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="a9d64-155">Entry</span></span> | <span data-ttu-id="a9d64-156">Value</span><span class="sxs-lookup"><span data-stu-id="a9d64-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a9d64-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a9d64-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9d64-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9d64-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9d64-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9d64-159">System-Only</span></span>            | <span data-ttu-id="a9d64-160">False</span><span class="sxs-lookup"><span data-stu-id="a9d64-160">False</span></span>                                        |
| <span data-ttu-id="a9d64-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a9d64-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a9d64-162">True</span><span class="sxs-lookup"><span data-stu-id="a9d64-162">True</span></span>                                         |
| <span data-ttu-id="a9d64-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a9d64-163">Is Indexed</span></span>             | <span data-ttu-id="a9d64-164">False</span><span class="sxs-lookup"><span data-stu-id="a9d64-164">False</span></span>                                        |
| <span data-ttu-id="a9d64-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a9d64-165">In Global Catalog</span></span>      | <span data-ttu-id="a9d64-166">False</span><span class="sxs-lookup"><span data-stu-id="a9d64-166">False</span></span>                                        |
| <span data-ttu-id="a9d64-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a9d64-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9d64-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a9d64-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a9d64-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9d64-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a9d64-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9d64-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a9d64-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d64-171">Search-Flags</span></span>           | <span data-ttu-id="a9d64-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9d64-172">0x00000000</span></span>                                   |
| <span data-ttu-id="a9d64-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d64-173">System-Flags</span></span>           | <span data-ttu-id="a9d64-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9d64-174">0x00000010</span></span>                                   |
| <span data-ttu-id="a9d64-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a9d64-175">Classes used in</span></span>        | [<span data-ttu-id="a9d64-176">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="a9d64-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a9d64-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a9d64-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a9d64-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="a9d64-178">Entry</span></span> | <span data-ttu-id="a9d64-179">Value</span><span class="sxs-lookup"><span data-stu-id="a9d64-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a9d64-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a9d64-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9d64-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9d64-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9d64-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9d64-182">System-Only</span></span>            | <span data-ttu-id="a9d64-183">False</span><span class="sxs-lookup"><span data-stu-id="a9d64-183">False</span></span>                                        |
| <span data-ttu-id="a9d64-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a9d64-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a9d64-185">True</span><span class="sxs-lookup"><span data-stu-id="a9d64-185">True</span></span>                                         |
| <span data-ttu-id="a9d64-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a9d64-186">Is Indexed</span></span>             | <span data-ttu-id="a9d64-187">False</span><span class="sxs-lookup"><span data-stu-id="a9d64-187">False</span></span>                                        |
| <span data-ttu-id="a9d64-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a9d64-188">In Global Catalog</span></span>      | <span data-ttu-id="a9d64-189">False</span><span class="sxs-lookup"><span data-stu-id="a9d64-189">False</span></span>                                        |
| <span data-ttu-id="a9d64-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a9d64-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9d64-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a9d64-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a9d64-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9d64-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a9d64-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9d64-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a9d64-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d64-194">Search-Flags</span></span>           | <span data-ttu-id="a9d64-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9d64-195">0x00000000</span></span>                                   |
| <span data-ttu-id="a9d64-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d64-196">System-Flags</span></span>           | <span data-ttu-id="a9d64-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9d64-197">0x00000010</span></span>                                   |
| <span data-ttu-id="a9d64-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a9d64-198">Classes used in</span></span>        | [<span data-ttu-id="a9d64-199">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="a9d64-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a9d64-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9d64-200">Windows Server 2008</span></span>



| <span data-ttu-id="a9d64-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="a9d64-201">Entry</span></span> | <span data-ttu-id="a9d64-202">Value</span><span class="sxs-lookup"><span data-stu-id="a9d64-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a9d64-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a9d64-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9d64-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9d64-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9d64-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9d64-205">System-Only</span></span>            | <span data-ttu-id="a9d64-206">False</span><span class="sxs-lookup"><span data-stu-id="a9d64-206">False</span></span>                                        |
| <span data-ttu-id="a9d64-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a9d64-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a9d64-208">True</span><span class="sxs-lookup"><span data-stu-id="a9d64-208">True</span></span>                                         |
| <span data-ttu-id="a9d64-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a9d64-209">Is Indexed</span></span>             | <span data-ttu-id="a9d64-210">False</span><span class="sxs-lookup"><span data-stu-id="a9d64-210">False</span></span>                                        |
| <span data-ttu-id="a9d64-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a9d64-211">In Global Catalog</span></span>      | <span data-ttu-id="a9d64-212">False</span><span class="sxs-lookup"><span data-stu-id="a9d64-212">False</span></span>                                        |
| <span data-ttu-id="a9d64-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a9d64-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9d64-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a9d64-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a9d64-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9d64-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a9d64-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9d64-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a9d64-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d64-217">Search-Flags</span></span>           | <span data-ttu-id="a9d64-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9d64-218">0x00000000</span></span>                                   |
| <span data-ttu-id="a9d64-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d64-219">System-Flags</span></span>           | <span data-ttu-id="a9d64-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9d64-220">0x00000010</span></span>                                   |
| <span data-ttu-id="a9d64-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a9d64-221">Classes used in</span></span>        | [<span data-ttu-id="a9d64-222">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="a9d64-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a9d64-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a9d64-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a9d64-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="a9d64-224">Entry</span></span> | <span data-ttu-id="a9d64-225">Value</span><span class="sxs-lookup"><span data-stu-id="a9d64-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a9d64-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a9d64-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9d64-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9d64-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9d64-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9d64-228">System-Only</span></span>            | <span data-ttu-id="a9d64-229">False</span><span class="sxs-lookup"><span data-stu-id="a9d64-229">False</span></span>                                        |
| <span data-ttu-id="a9d64-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a9d64-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a9d64-231">True</span><span class="sxs-lookup"><span data-stu-id="a9d64-231">True</span></span>                                         |
| <span data-ttu-id="a9d64-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a9d64-232">Is Indexed</span></span>             | <span data-ttu-id="a9d64-233">False</span><span class="sxs-lookup"><span data-stu-id="a9d64-233">False</span></span>                                        |
| <span data-ttu-id="a9d64-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a9d64-234">In Global Catalog</span></span>      | <span data-ttu-id="a9d64-235">False</span><span class="sxs-lookup"><span data-stu-id="a9d64-235">False</span></span>                                        |
| <span data-ttu-id="a9d64-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a9d64-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9d64-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a9d64-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a9d64-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9d64-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a9d64-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9d64-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a9d64-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d64-240">Search-Flags</span></span>           | <span data-ttu-id="a9d64-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9d64-241">0x00000000</span></span>                                   |
| <span data-ttu-id="a9d64-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d64-242">System-Flags</span></span>           | <span data-ttu-id="a9d64-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9d64-243">0x00000010</span></span>                                   |
| <span data-ttu-id="a9d64-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a9d64-244">Classes used in</span></span>        | [<span data-ttu-id="a9d64-245">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="a9d64-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a9d64-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9d64-246">Windows Server 2012</span></span>



| <span data-ttu-id="a9d64-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="a9d64-247">Entry</span></span> | <span data-ttu-id="a9d64-248">Value</span><span class="sxs-lookup"><span data-stu-id="a9d64-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a9d64-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a9d64-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9d64-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9d64-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9d64-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9d64-251">System-Only</span></span>            | <span data-ttu-id="a9d64-252">False</span><span class="sxs-lookup"><span data-stu-id="a9d64-252">False</span></span>                                        |
| <span data-ttu-id="a9d64-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a9d64-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a9d64-254">True</span><span class="sxs-lookup"><span data-stu-id="a9d64-254">True</span></span>                                         |
| <span data-ttu-id="a9d64-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a9d64-255">Is Indexed</span></span>             | <span data-ttu-id="a9d64-256">False</span><span class="sxs-lookup"><span data-stu-id="a9d64-256">False</span></span>                                        |
| <span data-ttu-id="a9d64-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a9d64-257">In Global Catalog</span></span>      | <span data-ttu-id="a9d64-258">False</span><span class="sxs-lookup"><span data-stu-id="a9d64-258">False</span></span>                                        |
| <span data-ttu-id="a9d64-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a9d64-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9d64-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a9d64-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a9d64-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9d64-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a9d64-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9d64-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a9d64-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d64-263">Search-Flags</span></span>           | <span data-ttu-id="a9d64-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9d64-264">0x00000000</span></span>                                   |
| <span data-ttu-id="a9d64-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d64-265">System-Flags</span></span>           | <span data-ttu-id="a9d64-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9d64-266">0x00000010</span></span>                                   |
| <span data-ttu-id="a9d64-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a9d64-267">Classes used in</span></span>        | [<span data-ttu-id="a9d64-268">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="a9d64-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





