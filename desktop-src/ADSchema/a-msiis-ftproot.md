---
title: atributo MS-IIS-FTP-root
description: Este atributo determina el recurso compartido de servidor de archivos. Se usa junto con MS-IIS-FTP-DIR para determinar el directorio particular del usuario FTP.
ms.assetid: b86dcafb-0b0d-4225-924c-690f739092a8
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MS-IIS-FTP-root
- msIIS-FTPRoot atributo AD Schema
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e7c55980b8b08865889f7567fa6bdb4dcf7bde1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493997"
---
# <a name="ms-iis-ftp-root-attribute"></a><span data-ttu-id="cfff4-106">atributo MS-IIS-FTP-root</span><span class="sxs-lookup"><span data-stu-id="cfff4-106">ms-IIS-FTP-Root attribute</span></span>

<span data-ttu-id="cfff4-107">Este atributo determina el recurso compartido de servidor de archivos.</span><span class="sxs-lookup"><span data-stu-id="cfff4-107">This attribute determines the file server share.</span></span> <span data-ttu-id="cfff4-108">Se usa junto con MS-IIS-FTP-DIR para determinar el directorio particular del usuario FTP.</span><span class="sxs-lookup"><span data-stu-id="cfff4-108">It is used in conjunction with ms-IIS-FTP-Dir to determine the FTP user home directory.</span></span>



| <span data-ttu-id="cfff4-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="cfff4-109">Entry</span></span> | <span data-ttu-id="cfff4-110">Value</span><span class="sxs-lookup"><span data-stu-id="cfff4-110">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfff4-111">CN</span><span class="sxs-lookup"><span data-stu-id="cfff4-111">CN</span></span>                | <span data-ttu-id="cfff4-112">MS-IIS-FTP-root</span><span class="sxs-lookup"><span data-stu-id="cfff4-112">ms-IIS-FTP-Root</span></span>                                                                                                                 |
| <span data-ttu-id="cfff4-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="cfff4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="cfff4-114">msIIS-FTPRoot</span><span class="sxs-lookup"><span data-stu-id="cfff4-114">msIIS-FTPRoot</span></span>                                                                                                                   |
| <span data-ttu-id="cfff4-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="cfff4-115">Size</span></span>              | <span data-ttu-id="cfff4-116">30-50 caracteres (15-25 caracteres Unicode para cada propiedad)</span><span class="sxs-lookup"><span data-stu-id="cfff4-116">30-50 characters (15-25 Unicode characters for each property)</span></span>                                                                   |
| <span data-ttu-id="cfff4-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="cfff4-117">Update Privilege</span></span>  | <span data-ttu-id="cfff4-118">Administrador de dominio & sistema local</span><span class="sxs-lookup"><span data-stu-id="cfff4-118">Domain administrator & local system</span></span>                                                                                             |
| <span data-ttu-id="cfff4-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="cfff4-119">Update Frequency</span></span>  | <span data-ttu-id="cfff4-120">Esta propiedad se establece cuando el administrador crea el sitio web y establece el aislamiento FTP.</span><span class="sxs-lookup"><span data-stu-id="cfff4-120">This property is set when the administrator creates the website and sets FTP isolation.</span></span> <span data-ttu-id="cfff4-121">Rara vez va a cambiar después de eso.</span><span class="sxs-lookup"><span data-stu-id="cfff4-121">It's rarely going to change after that.</span></span> |
| <span data-ttu-id="cfff4-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cfff4-122">Attribute-Id</span></span>      | <span data-ttu-id="cfff4-123">1.2.840.113556.1.4.1785</span><span class="sxs-lookup"><span data-stu-id="cfff4-123">1.2.840.113556.1.4.1785</span></span>                                                                                                         |
| <span data-ttu-id="cfff4-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cfff4-124">System-Id-Guid</span></span>    | <span data-ttu-id="cfff4-125">2a7827a4-1483-49a5-9d84-52e3812156b4</span><span class="sxs-lookup"><span data-stu-id="cfff4-125">2a7827a4-1483-49a5-9d84-52e3812156b4</span></span>                                                                                            |
| <span data-ttu-id="cfff4-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cfff4-126">Syntax</span></span>            | [<span data-ttu-id="cfff4-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="cfff4-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                     |



## <a name="implementations"></a><span data-ttu-id="cfff4-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="cfff4-128">Implementations</span></span>

-   [<span data-ttu-id="cfff4-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cfff4-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cfff4-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cfff4-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cfff4-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cfff4-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cfff4-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cfff4-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cfff4-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cfff4-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="cfff4-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cfff4-134">Windows Server 2003</span></span>



| <span data-ttu-id="cfff4-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="cfff4-135">Entry</span></span> | <span data-ttu-id="cfff4-136">Value</span><span class="sxs-lookup"><span data-stu-id="cfff4-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cfff4-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cfff4-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cfff4-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfff4-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cfff4-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfff4-139">System-Only</span></span>            | <span data-ttu-id="cfff4-140">False</span><span class="sxs-lookup"><span data-stu-id="cfff4-140">False</span></span>                             |
| <span data-ttu-id="cfff4-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cfff4-141">Is-Single-Valued</span></span>       | <span data-ttu-id="cfff4-142">True</span><span class="sxs-lookup"><span data-stu-id="cfff4-142">True</span></span>                              |
| <span data-ttu-id="cfff4-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cfff4-143">Is Indexed</span></span>             | <span data-ttu-id="cfff4-144">False</span><span class="sxs-lookup"><span data-stu-id="cfff4-144">False</span></span>                             |
| <span data-ttu-id="cfff4-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cfff4-145">In Global Catalog</span></span>      | <span data-ttu-id="cfff4-146">False</span><span class="sxs-lookup"><span data-stu-id="cfff4-146">False</span></span>                             |
| <span data-ttu-id="cfff4-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cfff4-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfff4-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cfff4-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cfff4-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfff4-149">Range-Lower</span></span>            | <span data-ttu-id="cfff4-150">1</span><span class="sxs-lookup"><span data-stu-id="cfff4-150">1</span></span>                                 |
| <span data-ttu-id="cfff4-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfff4-151">Range-Upper</span></span>            | <span data-ttu-id="cfff4-152">256</span><span class="sxs-lookup"><span data-stu-id="cfff4-152">256</span></span>                               |
| <span data-ttu-id="cfff4-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfff4-153">Search-Flags</span></span>           | <span data-ttu-id="cfff4-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfff4-154">0x00000000</span></span>                        |
| <span data-ttu-id="cfff4-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfff4-155">System-Flags</span></span>           | <span data-ttu-id="cfff4-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cfff4-156">0x00000010</span></span>                        |
| <span data-ttu-id="cfff4-157">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cfff4-157">Classes used in</span></span>        | [<span data-ttu-id="cfff4-158">**User**</span><span class="sxs-lookup"><span data-stu-id="cfff4-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cfff4-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cfff4-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cfff4-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="cfff4-160">Entry</span></span> | <span data-ttu-id="cfff4-161">Value</span><span class="sxs-lookup"><span data-stu-id="cfff4-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cfff4-162">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cfff4-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cfff4-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfff4-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cfff4-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfff4-164">System-Only</span></span>            | <span data-ttu-id="cfff4-165">False</span><span class="sxs-lookup"><span data-stu-id="cfff4-165">False</span></span>                             |
| <span data-ttu-id="cfff4-166">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cfff4-166">Is-Single-Valued</span></span>       | <span data-ttu-id="cfff4-167">True</span><span class="sxs-lookup"><span data-stu-id="cfff4-167">True</span></span>                              |
| <span data-ttu-id="cfff4-168">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cfff4-168">Is Indexed</span></span>             | <span data-ttu-id="cfff4-169">False</span><span class="sxs-lookup"><span data-stu-id="cfff4-169">False</span></span>                             |
| <span data-ttu-id="cfff4-170">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cfff4-170">In Global Catalog</span></span>      | <span data-ttu-id="cfff4-171">False</span><span class="sxs-lookup"><span data-stu-id="cfff4-171">False</span></span>                             |
| <span data-ttu-id="cfff4-172">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cfff4-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfff4-173">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cfff4-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cfff4-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfff4-174">Range-Lower</span></span>            | <span data-ttu-id="cfff4-175">1</span><span class="sxs-lookup"><span data-stu-id="cfff4-175">1</span></span>                                 |
| <span data-ttu-id="cfff4-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfff4-176">Range-Upper</span></span>            | <span data-ttu-id="cfff4-177">256</span><span class="sxs-lookup"><span data-stu-id="cfff4-177">256</span></span>                               |
| <span data-ttu-id="cfff4-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfff4-178">Search-Flags</span></span>           | <span data-ttu-id="cfff4-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfff4-179">0x00000000</span></span>                        |
| <span data-ttu-id="cfff4-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfff4-180">System-Flags</span></span>           | <span data-ttu-id="cfff4-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cfff4-181">0x00000010</span></span>                        |
| <span data-ttu-id="cfff4-182">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cfff4-182">Classes used in</span></span>        | [<span data-ttu-id="cfff4-183">**User**</span><span class="sxs-lookup"><span data-stu-id="cfff4-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cfff4-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfff4-184">Windows Server 2008</span></span>



| <span data-ttu-id="cfff4-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="cfff4-185">Entry</span></span> | <span data-ttu-id="cfff4-186">Value</span><span class="sxs-lookup"><span data-stu-id="cfff4-186">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cfff4-187">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cfff4-187">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cfff4-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfff4-188">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cfff4-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfff4-189">System-Only</span></span>            | <span data-ttu-id="cfff4-190">False</span><span class="sxs-lookup"><span data-stu-id="cfff4-190">False</span></span>                             |
| <span data-ttu-id="cfff4-191">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cfff4-191">Is-Single-Valued</span></span>       | <span data-ttu-id="cfff4-192">True</span><span class="sxs-lookup"><span data-stu-id="cfff4-192">True</span></span>                              |
| <span data-ttu-id="cfff4-193">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cfff4-193">Is Indexed</span></span>             | <span data-ttu-id="cfff4-194">False</span><span class="sxs-lookup"><span data-stu-id="cfff4-194">False</span></span>                             |
| <span data-ttu-id="cfff4-195">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cfff4-195">In Global Catalog</span></span>      | <span data-ttu-id="cfff4-196">False</span><span class="sxs-lookup"><span data-stu-id="cfff4-196">False</span></span>                             |
| <span data-ttu-id="cfff4-197">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cfff4-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfff4-198">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cfff4-198">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cfff4-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfff4-199">Range-Lower</span></span>            | <span data-ttu-id="cfff4-200">1</span><span class="sxs-lookup"><span data-stu-id="cfff4-200">1</span></span>                                 |
| <span data-ttu-id="cfff4-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfff4-201">Range-Upper</span></span>            | <span data-ttu-id="cfff4-202">256</span><span class="sxs-lookup"><span data-stu-id="cfff4-202">256</span></span>                               |
| <span data-ttu-id="cfff4-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfff4-203">Search-Flags</span></span>           | <span data-ttu-id="cfff4-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfff4-204">0x00000000</span></span>                        |
| <span data-ttu-id="cfff4-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfff4-205">System-Flags</span></span>           | <span data-ttu-id="cfff4-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cfff4-206">0x00000010</span></span>                        |
| <span data-ttu-id="cfff4-207">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cfff4-207">Classes used in</span></span>        | [<span data-ttu-id="cfff4-208">**User**</span><span class="sxs-lookup"><span data-stu-id="cfff4-208">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cfff4-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cfff4-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cfff4-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="cfff4-210">Entry</span></span> | <span data-ttu-id="cfff4-211">Value</span><span class="sxs-lookup"><span data-stu-id="cfff4-211">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cfff4-212">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cfff4-212">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cfff4-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfff4-213">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cfff4-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfff4-214">System-Only</span></span>            | <span data-ttu-id="cfff4-215">False</span><span class="sxs-lookup"><span data-stu-id="cfff4-215">False</span></span>                             |
| <span data-ttu-id="cfff4-216">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cfff4-216">Is-Single-Valued</span></span>       | <span data-ttu-id="cfff4-217">True</span><span class="sxs-lookup"><span data-stu-id="cfff4-217">True</span></span>                              |
| <span data-ttu-id="cfff4-218">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cfff4-218">Is Indexed</span></span>             | <span data-ttu-id="cfff4-219">False</span><span class="sxs-lookup"><span data-stu-id="cfff4-219">False</span></span>                             |
| <span data-ttu-id="cfff4-220">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cfff4-220">In Global Catalog</span></span>      | <span data-ttu-id="cfff4-221">False</span><span class="sxs-lookup"><span data-stu-id="cfff4-221">False</span></span>                             |
| <span data-ttu-id="cfff4-222">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cfff4-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfff4-223">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cfff4-223">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cfff4-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfff4-224">Range-Lower</span></span>            | <span data-ttu-id="cfff4-225">1</span><span class="sxs-lookup"><span data-stu-id="cfff4-225">1</span></span>                                 |
| <span data-ttu-id="cfff4-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfff4-226">Range-Upper</span></span>            | <span data-ttu-id="cfff4-227">256</span><span class="sxs-lookup"><span data-stu-id="cfff4-227">256</span></span>                               |
| <span data-ttu-id="cfff4-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfff4-228">Search-Flags</span></span>           | <span data-ttu-id="cfff4-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfff4-229">0x00000000</span></span>                        |
| <span data-ttu-id="cfff4-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfff4-230">System-Flags</span></span>           | <span data-ttu-id="cfff4-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cfff4-231">0x00000010</span></span>                        |
| <span data-ttu-id="cfff4-232">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cfff4-232">Classes used in</span></span>        | [<span data-ttu-id="cfff4-233">**User**</span><span class="sxs-lookup"><span data-stu-id="cfff4-233">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cfff4-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cfff4-234">Windows Server 2012</span></span>



| <span data-ttu-id="cfff4-235">Entrada</span><span class="sxs-lookup"><span data-stu-id="cfff4-235">Entry</span></span> | <span data-ttu-id="cfff4-236">Value</span><span class="sxs-lookup"><span data-stu-id="cfff4-236">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cfff4-237">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cfff4-237">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cfff4-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfff4-238">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cfff4-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfff4-239">System-Only</span></span>            | <span data-ttu-id="cfff4-240">False</span><span class="sxs-lookup"><span data-stu-id="cfff4-240">False</span></span>                             |
| <span data-ttu-id="cfff4-241">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cfff4-241">Is-Single-Valued</span></span>       | <span data-ttu-id="cfff4-242">True</span><span class="sxs-lookup"><span data-stu-id="cfff4-242">True</span></span>                              |
| <span data-ttu-id="cfff4-243">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cfff4-243">Is Indexed</span></span>             | <span data-ttu-id="cfff4-244">False</span><span class="sxs-lookup"><span data-stu-id="cfff4-244">False</span></span>                             |
| <span data-ttu-id="cfff4-245">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cfff4-245">In Global Catalog</span></span>      | <span data-ttu-id="cfff4-246">False</span><span class="sxs-lookup"><span data-stu-id="cfff4-246">False</span></span>                             |
| <span data-ttu-id="cfff4-247">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cfff4-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfff4-248">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cfff4-248">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cfff4-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfff4-249">Range-Lower</span></span>            | <span data-ttu-id="cfff4-250">1</span><span class="sxs-lookup"><span data-stu-id="cfff4-250">1</span></span>                                 |
| <span data-ttu-id="cfff4-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfff4-251">Range-Upper</span></span>            | <span data-ttu-id="cfff4-252">256</span><span class="sxs-lookup"><span data-stu-id="cfff4-252">256</span></span>                               |
| <span data-ttu-id="cfff4-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfff4-253">Search-Flags</span></span>           | <span data-ttu-id="cfff4-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfff4-254">0x00000000</span></span>                        |
| <span data-ttu-id="cfff4-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfff4-255">System-Flags</span></span>           | <span data-ttu-id="cfff4-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cfff4-256">0x00000010</span></span>                        |
| <span data-ttu-id="cfff4-257">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cfff4-257">Classes used in</span></span>        | [<span data-ttu-id="cfff4-258">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="cfff4-258">**User**</span></span>](c-user.md)<br/> |



 

 





