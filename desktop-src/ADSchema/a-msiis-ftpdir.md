---
title: atributo MS-IIS-FTP-dir
description: Este atributo determina el directorio principal del usuario en relación con el recurso compartido del servidor de archivos. Se usa junto con MS-IIS-FTP-root para determinar el directorio particular del usuario FTP.
ms.assetid: 99b22b79-1d42-440d-b92b-33bac3e811cb
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-IIS-FTP-dir
- msIIS-FTPDir atributo AD Schema
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Dir
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3067476e7dc275dbe14471d6c3c98fa5445a9dfe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535986"
---
# <a name="ms-iis-ftp-dir-attribute"></a><span data-ttu-id="f465b-106">atributo MS-IIS-FTP-dir</span><span class="sxs-lookup"><span data-stu-id="f465b-106">ms-IIS-FTP-Dir attribute</span></span>

<span data-ttu-id="f465b-107">Este atributo determina el directorio principal del usuario en relación con el recurso compartido del servidor de archivos.</span><span class="sxs-lookup"><span data-stu-id="f465b-107">This attribute determines the user home directory relative to the file server share.</span></span> <span data-ttu-id="f465b-108">Se usa junto con MS-IIS-FTP-root para determinar el directorio particular del usuario FTP.</span><span class="sxs-lookup"><span data-stu-id="f465b-108">It is used in conjunction with ms-IIS-FTP-Root to determine the FTP user home directory.</span></span>



| <span data-ttu-id="f465b-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="f465b-109">Entry</span></span> | <span data-ttu-id="f465b-110">Value</span><span class="sxs-lookup"><span data-stu-id="f465b-110">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f465b-111">CN</span><span class="sxs-lookup"><span data-stu-id="f465b-111">CN</span></span>                | <span data-ttu-id="f465b-112">MS-IIS-FTP-dir</span><span class="sxs-lookup"><span data-stu-id="f465b-112">ms-IIS-FTP-Dir</span></span>                                                                                                                  |
| <span data-ttu-id="f465b-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="f465b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f465b-114">msIIS-FTPDir</span><span class="sxs-lookup"><span data-stu-id="f465b-114">msIIS-FTPDir</span></span>                                                                                                                    |
| <span data-ttu-id="f465b-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f465b-115">Size</span></span>              | <span data-ttu-id="f465b-116">30-50 caracteres (15-25 caracteres Unicode para cada propiedad)</span><span class="sxs-lookup"><span data-stu-id="f465b-116">30-50 characters (15-25 Unicode characters for each property)</span></span>                                                                   |
| <span data-ttu-id="f465b-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="f465b-117">Update Privilege</span></span>  | <span data-ttu-id="f465b-118">Administrador de dominio & sistema local</span><span class="sxs-lookup"><span data-stu-id="f465b-118">Domain administrator & local system</span></span>                                                                                             |
| <span data-ttu-id="f465b-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="f465b-119">Update Frequency</span></span>  | <span data-ttu-id="f465b-120">Esta propiedad se establece cuando el administrador crea el sitio web y establece el aislamiento FTP.</span><span class="sxs-lookup"><span data-stu-id="f465b-120">This property is set when the administrator creates the website and sets FTP isolation.</span></span> <span data-ttu-id="f465b-121">Rara vez va a cambiar después de eso.</span><span class="sxs-lookup"><span data-stu-id="f465b-121">It's rarely going to change after that.</span></span> |
| <span data-ttu-id="f465b-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f465b-122">Attribute-Id</span></span>      | <span data-ttu-id="f465b-123">1.2.840.113556.1.4.1786</span><span class="sxs-lookup"><span data-stu-id="f465b-123">1.2.840.113556.1.4.1786</span></span>                                                                                                         |
| <span data-ttu-id="f465b-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f465b-124">System-Id-Guid</span></span>    | <span data-ttu-id="f465b-125">8a5c99e9-2230-46eb-b8e8-e59d712eb9ee</span><span class="sxs-lookup"><span data-stu-id="f465b-125">8a5c99e9-2230-46eb-b8e8-e59d712eb9ee</span></span>                                                                                            |
| <span data-ttu-id="f465b-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f465b-126">Syntax</span></span>            | [<span data-ttu-id="f465b-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f465b-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                     |



## <a name="implementations"></a><span data-ttu-id="f465b-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="f465b-128">Implementations</span></span>

-   [<span data-ttu-id="f465b-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f465b-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f465b-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f465b-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f465b-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f465b-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f465b-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f465b-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f465b-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f465b-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f465b-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f465b-134">Windows Server 2003</span></span>



| <span data-ttu-id="f465b-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="f465b-135">Entry</span></span> | <span data-ttu-id="f465b-136">Value</span><span class="sxs-lookup"><span data-stu-id="f465b-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f465b-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f465b-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f465b-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f465b-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f465b-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="f465b-139">System-Only</span></span>            | <span data-ttu-id="f465b-140">False</span><span class="sxs-lookup"><span data-stu-id="f465b-140">False</span></span>                             |
| <span data-ttu-id="f465b-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f465b-141">Is-Single-Valued</span></span>       | <span data-ttu-id="f465b-142">True</span><span class="sxs-lookup"><span data-stu-id="f465b-142">True</span></span>                              |
| <span data-ttu-id="f465b-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f465b-143">Is Indexed</span></span>             | <span data-ttu-id="f465b-144">False</span><span class="sxs-lookup"><span data-stu-id="f465b-144">False</span></span>                             |
| <span data-ttu-id="f465b-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f465b-145">In Global Catalog</span></span>      | <span data-ttu-id="f465b-146">False</span><span class="sxs-lookup"><span data-stu-id="f465b-146">False</span></span>                             |
| <span data-ttu-id="f465b-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f465b-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="f465b-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f465b-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f465b-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f465b-149">Range-Lower</span></span>            | <span data-ttu-id="f465b-150">1</span><span class="sxs-lookup"><span data-stu-id="f465b-150">1</span></span>                                 |
| <span data-ttu-id="f465b-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f465b-151">Range-Upper</span></span>            | <span data-ttu-id="f465b-152">256</span><span class="sxs-lookup"><span data-stu-id="f465b-152">256</span></span>                               |
| <span data-ttu-id="f465b-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f465b-153">Search-Flags</span></span>           | <span data-ttu-id="f465b-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f465b-154">0x00000000</span></span>                        |
| <span data-ttu-id="f465b-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f465b-155">System-Flags</span></span>           | <span data-ttu-id="f465b-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f465b-156">0x00000010</span></span>                        |
| <span data-ttu-id="f465b-157">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f465b-157">Classes used in</span></span>        | [<span data-ttu-id="f465b-158">**User**</span><span class="sxs-lookup"><span data-stu-id="f465b-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f465b-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f465b-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f465b-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="f465b-160">Entry</span></span> | <span data-ttu-id="f465b-161">Value</span><span class="sxs-lookup"><span data-stu-id="f465b-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f465b-162">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f465b-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f465b-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f465b-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f465b-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="f465b-164">System-Only</span></span>            | <span data-ttu-id="f465b-165">False</span><span class="sxs-lookup"><span data-stu-id="f465b-165">False</span></span>                             |
| <span data-ttu-id="f465b-166">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f465b-166">Is-Single-Valued</span></span>       | <span data-ttu-id="f465b-167">True</span><span class="sxs-lookup"><span data-stu-id="f465b-167">True</span></span>                              |
| <span data-ttu-id="f465b-168">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f465b-168">Is Indexed</span></span>             | <span data-ttu-id="f465b-169">False</span><span class="sxs-lookup"><span data-stu-id="f465b-169">False</span></span>                             |
| <span data-ttu-id="f465b-170">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f465b-170">In Global Catalog</span></span>      | <span data-ttu-id="f465b-171">False</span><span class="sxs-lookup"><span data-stu-id="f465b-171">False</span></span>                             |
| <span data-ttu-id="f465b-172">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f465b-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="f465b-173">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f465b-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f465b-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f465b-174">Range-Lower</span></span>            | <span data-ttu-id="f465b-175">1</span><span class="sxs-lookup"><span data-stu-id="f465b-175">1</span></span>                                 |
| <span data-ttu-id="f465b-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f465b-176">Range-Upper</span></span>            | <span data-ttu-id="f465b-177">256</span><span class="sxs-lookup"><span data-stu-id="f465b-177">256</span></span>                               |
| <span data-ttu-id="f465b-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f465b-178">Search-Flags</span></span>           | <span data-ttu-id="f465b-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f465b-179">0x00000000</span></span>                        |
| <span data-ttu-id="f465b-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f465b-180">System-Flags</span></span>           | <span data-ttu-id="f465b-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f465b-181">0x00000010</span></span>                        |
| <span data-ttu-id="f465b-182">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f465b-182">Classes used in</span></span>        | [<span data-ttu-id="f465b-183">**User**</span><span class="sxs-lookup"><span data-stu-id="f465b-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f465b-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f465b-184">Windows Server 2008</span></span>



| <span data-ttu-id="f465b-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="f465b-185">Entry</span></span> | <span data-ttu-id="f465b-186">Value</span><span class="sxs-lookup"><span data-stu-id="f465b-186">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f465b-187">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f465b-187">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f465b-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f465b-188">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f465b-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="f465b-189">System-Only</span></span>            | <span data-ttu-id="f465b-190">False</span><span class="sxs-lookup"><span data-stu-id="f465b-190">False</span></span>                             |
| <span data-ttu-id="f465b-191">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f465b-191">Is-Single-Valued</span></span>       | <span data-ttu-id="f465b-192">True</span><span class="sxs-lookup"><span data-stu-id="f465b-192">True</span></span>                              |
| <span data-ttu-id="f465b-193">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f465b-193">Is Indexed</span></span>             | <span data-ttu-id="f465b-194">False</span><span class="sxs-lookup"><span data-stu-id="f465b-194">False</span></span>                             |
| <span data-ttu-id="f465b-195">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f465b-195">In Global Catalog</span></span>      | <span data-ttu-id="f465b-196">False</span><span class="sxs-lookup"><span data-stu-id="f465b-196">False</span></span>                             |
| <span data-ttu-id="f465b-197">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f465b-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="f465b-198">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f465b-198">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f465b-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f465b-199">Range-Lower</span></span>            | <span data-ttu-id="f465b-200">1</span><span class="sxs-lookup"><span data-stu-id="f465b-200">1</span></span>                                 |
| <span data-ttu-id="f465b-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f465b-201">Range-Upper</span></span>            | <span data-ttu-id="f465b-202">256</span><span class="sxs-lookup"><span data-stu-id="f465b-202">256</span></span>                               |
| <span data-ttu-id="f465b-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f465b-203">Search-Flags</span></span>           | <span data-ttu-id="f465b-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f465b-204">0x00000000</span></span>                        |
| <span data-ttu-id="f465b-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f465b-205">System-Flags</span></span>           | <span data-ttu-id="f465b-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f465b-206">0x00000010</span></span>                        |
| <span data-ttu-id="f465b-207">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f465b-207">Classes used in</span></span>        | [<span data-ttu-id="f465b-208">**User**</span><span class="sxs-lookup"><span data-stu-id="f465b-208">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f465b-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f465b-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f465b-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="f465b-210">Entry</span></span> | <span data-ttu-id="f465b-211">Value</span><span class="sxs-lookup"><span data-stu-id="f465b-211">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f465b-212">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f465b-212">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f465b-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f465b-213">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f465b-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="f465b-214">System-Only</span></span>            | <span data-ttu-id="f465b-215">False</span><span class="sxs-lookup"><span data-stu-id="f465b-215">False</span></span>                             |
| <span data-ttu-id="f465b-216">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f465b-216">Is-Single-Valued</span></span>       | <span data-ttu-id="f465b-217">True</span><span class="sxs-lookup"><span data-stu-id="f465b-217">True</span></span>                              |
| <span data-ttu-id="f465b-218">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f465b-218">Is Indexed</span></span>             | <span data-ttu-id="f465b-219">False</span><span class="sxs-lookup"><span data-stu-id="f465b-219">False</span></span>                             |
| <span data-ttu-id="f465b-220">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f465b-220">In Global Catalog</span></span>      | <span data-ttu-id="f465b-221">False</span><span class="sxs-lookup"><span data-stu-id="f465b-221">False</span></span>                             |
| <span data-ttu-id="f465b-222">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f465b-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="f465b-223">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f465b-223">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f465b-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f465b-224">Range-Lower</span></span>            | <span data-ttu-id="f465b-225">1</span><span class="sxs-lookup"><span data-stu-id="f465b-225">1</span></span>                                 |
| <span data-ttu-id="f465b-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f465b-226">Range-Upper</span></span>            | <span data-ttu-id="f465b-227">256</span><span class="sxs-lookup"><span data-stu-id="f465b-227">256</span></span>                               |
| <span data-ttu-id="f465b-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f465b-228">Search-Flags</span></span>           | <span data-ttu-id="f465b-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f465b-229">0x00000000</span></span>                        |
| <span data-ttu-id="f465b-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f465b-230">System-Flags</span></span>           | <span data-ttu-id="f465b-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f465b-231">0x00000010</span></span>                        |
| <span data-ttu-id="f465b-232">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f465b-232">Classes used in</span></span>        | [<span data-ttu-id="f465b-233">**User**</span><span class="sxs-lookup"><span data-stu-id="f465b-233">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f465b-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f465b-234">Windows Server 2012</span></span>



| <span data-ttu-id="f465b-235">Entrada</span><span class="sxs-lookup"><span data-stu-id="f465b-235">Entry</span></span> | <span data-ttu-id="f465b-236">Value</span><span class="sxs-lookup"><span data-stu-id="f465b-236">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f465b-237">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f465b-237">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f465b-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f465b-238">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f465b-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="f465b-239">System-Only</span></span>            | <span data-ttu-id="f465b-240">False</span><span class="sxs-lookup"><span data-stu-id="f465b-240">False</span></span>                             |
| <span data-ttu-id="f465b-241">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f465b-241">Is-Single-Valued</span></span>       | <span data-ttu-id="f465b-242">True</span><span class="sxs-lookup"><span data-stu-id="f465b-242">True</span></span>                              |
| <span data-ttu-id="f465b-243">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f465b-243">Is Indexed</span></span>             | <span data-ttu-id="f465b-244">False</span><span class="sxs-lookup"><span data-stu-id="f465b-244">False</span></span>                             |
| <span data-ttu-id="f465b-245">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f465b-245">In Global Catalog</span></span>      | <span data-ttu-id="f465b-246">False</span><span class="sxs-lookup"><span data-stu-id="f465b-246">False</span></span>                             |
| <span data-ttu-id="f465b-247">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f465b-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="f465b-248">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f465b-248">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f465b-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f465b-249">Range-Lower</span></span>            | <span data-ttu-id="f465b-250">1</span><span class="sxs-lookup"><span data-stu-id="f465b-250">1</span></span>                                 |
| <span data-ttu-id="f465b-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f465b-251">Range-Upper</span></span>            | <span data-ttu-id="f465b-252">256</span><span class="sxs-lookup"><span data-stu-id="f465b-252">256</span></span>                               |
| <span data-ttu-id="f465b-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f465b-253">Search-Flags</span></span>           | <span data-ttu-id="f465b-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f465b-254">0x00000000</span></span>                        |
| <span data-ttu-id="f465b-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f465b-255">System-Flags</span></span>           | <span data-ttu-id="f465b-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f465b-256">0x00000010</span></span>                        |
| <span data-ttu-id="f465b-257">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f465b-257">Classes used in</span></span>        | [<span data-ttu-id="f465b-258">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="f465b-258">**User**</span></span>](c-user.md)<br/> |



 

 





