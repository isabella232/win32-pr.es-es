---
title: Atributo User-Shared-Folder
description: Especifica una ruta de acceso UNC a la carpeta de documentos compartidos del usuario. La ruta de acceso debe ser una ruta de acceso UNC de red con el formato \\ \\ servidor \\ recurso compartido \\ directorio. Este valor puede ser una cadena nula.
ms.assetid: 23b4177a-0a05-4111-affe-d81bc115580d
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de carpeta compartida de usuario
- userSharedFolder esquema de AD de atributos
topic_type:
- apiref
api_name:
- User-Shared-Folder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a20e9772302e79837fccd301943554191cf3b862
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997489"
---
# <a name="user-shared-folder-attribute"></a><span data-ttu-id="ec5bb-107">Atributo User-Shared-Folder</span><span class="sxs-lookup"><span data-stu-id="ec5bb-107">User-Shared-Folder attribute</span></span>

<span data-ttu-id="ec5bb-108">Especifica una ruta de acceso UNC a la carpeta de documentos compartidos del usuario.</span><span class="sxs-lookup"><span data-stu-id="ec5bb-108">Specifies a UNC path to the user's shared documents folder.</span></span> <span data-ttu-id="ec5bb-109">La ruta de acceso debe ser una ruta de acceso UNC de red con el formato **\\\\** _servidor_ *_\\_* _recurso compartido_ *_\\_* _directorio_.</span><span class="sxs-lookup"><span data-stu-id="ec5bb-109">The path must be a network UNC path of the form **\\\\**_Server_*_\\_*_Share_*_\\_*_Directory_.</span></span> <span data-ttu-id="ec5bb-110">Este valor puede ser una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="ec5bb-110">This value can be a null string.</span></span>



| <span data-ttu-id="ec5bb-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec5bb-111">Entry</span></span> | <span data-ttu-id="ec5bb-112">Value</span><span class="sxs-lookup"><span data-stu-id="ec5bb-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ec5bb-113">CN</span><span class="sxs-lookup"><span data-stu-id="ec5bb-113">CN</span></span>                | <span data-ttu-id="ec5bb-114">User-Shared-Folder</span><span class="sxs-lookup"><span data-stu-id="ec5bb-114">User-Shared-Folder</span></span>                                                                |
| <span data-ttu-id="ec5bb-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="ec5bb-115">Ldap-Display-Name</span></span> | <span data-ttu-id="ec5bb-116">userSharedFolder</span><span class="sxs-lookup"><span data-stu-id="ec5bb-116">userSharedFolder</span></span>                                                                  |
| <span data-ttu-id="ec5bb-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="ec5bb-117">Size</span></span>              | \-                                                                                |
| <span data-ttu-id="ec5bb-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="ec5bb-118">Update Privilege</span></span>  | <span data-ttu-id="ec5bb-119">Administrador de dominio o propietario de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="ec5bb-119">Domain administrator or account owner.</span></span>                                            |
| <span data-ttu-id="ec5bb-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="ec5bb-120">Update Frequency</span></span>  | <span data-ttu-id="ec5bb-121">Cuando se crea el registro del usuario y cada vez que es necesario cambiar la carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="ec5bb-121">When the user's record is created and whenever the shared folder needs to change.</span></span> |
| <span data-ttu-id="ec5bb-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ec5bb-122">Attribute-Id</span></span>      | <span data-ttu-id="ec5bb-123">1.2.840.113556.1.4.751</span><span class="sxs-lookup"><span data-stu-id="ec5bb-123">1.2.840.113556.1.4.751</span></span>                                                            |
| <span data-ttu-id="ec5bb-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ec5bb-124">System-Id-Guid</span></span>    | <span data-ttu-id="ec5bb-125">9a9a021f-4a5b-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ec5bb-125">9a9a021f-4a5b-11d1-a9c3-0000f80367c1</span></span>                                              |
| <span data-ttu-id="ec5bb-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec5bb-126">Syntax</span></span>            | [<span data-ttu-id="ec5bb-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ec5bb-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="ec5bb-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="ec5bb-128">Implementations</span></span>

-   [<span data-ttu-id="ec5bb-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ec5bb-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ec5bb-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ec5bb-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ec5bb-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ec5bb-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ec5bb-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ec5bb-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ec5bb-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ec5bb-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ec5bb-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ec5bb-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ec5bb-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ec5bb-135">Windows 2000 Server</span></span>



| <span data-ttu-id="ec5bb-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec5bb-136">Entry</span></span> | <span data-ttu-id="ec5bb-137">Value</span><span class="sxs-lookup"><span data-stu-id="ec5bb-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ec5bb-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ec5bb-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ec5bb-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec5bb-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ec5bb-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec5bb-140">System-Only</span></span>            | <span data-ttu-id="ec5bb-141">False</span><span class="sxs-lookup"><span data-stu-id="ec5bb-141">False</span></span>                             |
| <span data-ttu-id="ec5bb-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ec5bb-142">Is-Single-Valued</span></span>       | <span data-ttu-id="ec5bb-143">True</span><span class="sxs-lookup"><span data-stu-id="ec5bb-143">True</span></span>                              |
| <span data-ttu-id="ec5bb-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ec5bb-144">Is Indexed</span></span>             | <span data-ttu-id="ec5bb-145">False</span><span class="sxs-lookup"><span data-stu-id="ec5bb-145">False</span></span>                             |
| <span data-ttu-id="ec5bb-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ec5bb-146">In Global Catalog</span></span>      | <span data-ttu-id="ec5bb-147">False</span><span class="sxs-lookup"><span data-stu-id="ec5bb-147">False</span></span>                             |
| <span data-ttu-id="ec5bb-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ec5bb-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec5bb-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec5bb-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ec5bb-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec5bb-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ec5bb-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec5bb-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ec5bb-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5bb-152">Search-Flags</span></span>           | <span data-ttu-id="ec5bb-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec5bb-153">0x00000000</span></span>                        |
| <span data-ttu-id="ec5bb-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5bb-154">System-Flags</span></span>           | <span data-ttu-id="ec5bb-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec5bb-155">0x00000010</span></span>                        |
| <span data-ttu-id="ec5bb-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ec5bb-156">Classes used in</span></span>        | [<span data-ttu-id="ec5bb-157">**User**</span><span class="sxs-lookup"><span data-stu-id="ec5bb-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ec5bb-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ec5bb-158">Windows Server 2003</span></span>



| <span data-ttu-id="ec5bb-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec5bb-159">Entry</span></span> | <span data-ttu-id="ec5bb-160">Value</span><span class="sxs-lookup"><span data-stu-id="ec5bb-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ec5bb-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ec5bb-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ec5bb-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec5bb-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ec5bb-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec5bb-163">System-Only</span></span>            | <span data-ttu-id="ec5bb-164">False</span><span class="sxs-lookup"><span data-stu-id="ec5bb-164">False</span></span>                             |
| <span data-ttu-id="ec5bb-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ec5bb-165">Is-Single-Valued</span></span>       | <span data-ttu-id="ec5bb-166">True</span><span class="sxs-lookup"><span data-stu-id="ec5bb-166">True</span></span>                              |
| <span data-ttu-id="ec5bb-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ec5bb-167">Is Indexed</span></span>             | <span data-ttu-id="ec5bb-168">False</span><span class="sxs-lookup"><span data-stu-id="ec5bb-168">False</span></span>                             |
| <span data-ttu-id="ec5bb-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ec5bb-169">In Global Catalog</span></span>      | <span data-ttu-id="ec5bb-170">False</span><span class="sxs-lookup"><span data-stu-id="ec5bb-170">False</span></span>                             |
| <span data-ttu-id="ec5bb-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ec5bb-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec5bb-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec5bb-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ec5bb-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec5bb-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ec5bb-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec5bb-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ec5bb-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5bb-175">Search-Flags</span></span>           | <span data-ttu-id="ec5bb-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec5bb-176">0x00000000</span></span>                        |
| <span data-ttu-id="ec5bb-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5bb-177">System-Flags</span></span>           | <span data-ttu-id="ec5bb-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec5bb-178">0x00000010</span></span>                        |
| <span data-ttu-id="ec5bb-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ec5bb-179">Classes used in</span></span>        | [<span data-ttu-id="ec5bb-180">**User**</span><span class="sxs-lookup"><span data-stu-id="ec5bb-180">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ec5bb-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ec5bb-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ec5bb-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec5bb-182">Entry</span></span> | <span data-ttu-id="ec5bb-183">Value</span><span class="sxs-lookup"><span data-stu-id="ec5bb-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ec5bb-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ec5bb-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ec5bb-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec5bb-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ec5bb-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec5bb-186">System-Only</span></span>            | <span data-ttu-id="ec5bb-187">False</span><span class="sxs-lookup"><span data-stu-id="ec5bb-187">False</span></span>                             |
| <span data-ttu-id="ec5bb-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ec5bb-188">Is-Single-Valued</span></span>       | <span data-ttu-id="ec5bb-189">True</span><span class="sxs-lookup"><span data-stu-id="ec5bb-189">True</span></span>                              |
| <span data-ttu-id="ec5bb-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ec5bb-190">Is Indexed</span></span>             | <span data-ttu-id="ec5bb-191">False</span><span class="sxs-lookup"><span data-stu-id="ec5bb-191">False</span></span>                             |
| <span data-ttu-id="ec5bb-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ec5bb-192">In Global Catalog</span></span>      | <span data-ttu-id="ec5bb-193">False</span><span class="sxs-lookup"><span data-stu-id="ec5bb-193">False</span></span>                             |
| <span data-ttu-id="ec5bb-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ec5bb-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec5bb-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec5bb-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ec5bb-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec5bb-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ec5bb-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec5bb-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ec5bb-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5bb-198">Search-Flags</span></span>           | <span data-ttu-id="ec5bb-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec5bb-199">0x00000000</span></span>                        |
| <span data-ttu-id="ec5bb-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5bb-200">System-Flags</span></span>           | <span data-ttu-id="ec5bb-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec5bb-201">0x00000010</span></span>                        |
| <span data-ttu-id="ec5bb-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ec5bb-202">Classes used in</span></span>        | [<span data-ttu-id="ec5bb-203">**User**</span><span class="sxs-lookup"><span data-stu-id="ec5bb-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ec5bb-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec5bb-204">Windows Server 2008</span></span>



| <span data-ttu-id="ec5bb-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec5bb-205">Entry</span></span> | <span data-ttu-id="ec5bb-206">Value</span><span class="sxs-lookup"><span data-stu-id="ec5bb-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ec5bb-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ec5bb-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ec5bb-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec5bb-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ec5bb-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec5bb-209">System-Only</span></span>            | <span data-ttu-id="ec5bb-210">False</span><span class="sxs-lookup"><span data-stu-id="ec5bb-210">False</span></span>                             |
| <span data-ttu-id="ec5bb-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ec5bb-211">Is-Single-Valued</span></span>       | <span data-ttu-id="ec5bb-212">True</span><span class="sxs-lookup"><span data-stu-id="ec5bb-212">True</span></span>                              |
| <span data-ttu-id="ec5bb-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ec5bb-213">Is Indexed</span></span>             | <span data-ttu-id="ec5bb-214">False</span><span class="sxs-lookup"><span data-stu-id="ec5bb-214">False</span></span>                             |
| <span data-ttu-id="ec5bb-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ec5bb-215">In Global Catalog</span></span>      | <span data-ttu-id="ec5bb-216">False</span><span class="sxs-lookup"><span data-stu-id="ec5bb-216">False</span></span>                             |
| <span data-ttu-id="ec5bb-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ec5bb-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec5bb-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec5bb-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ec5bb-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec5bb-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ec5bb-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec5bb-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ec5bb-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5bb-221">Search-Flags</span></span>           | <span data-ttu-id="ec5bb-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec5bb-222">0x00000000</span></span>                        |
| <span data-ttu-id="ec5bb-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5bb-223">System-Flags</span></span>           | <span data-ttu-id="ec5bb-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec5bb-224">0x00000010</span></span>                        |
| <span data-ttu-id="ec5bb-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ec5bb-225">Classes used in</span></span>        | [<span data-ttu-id="ec5bb-226">**User**</span><span class="sxs-lookup"><span data-stu-id="ec5bb-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ec5bb-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ec5bb-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ec5bb-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec5bb-228">Entry</span></span> | <span data-ttu-id="ec5bb-229">Value</span><span class="sxs-lookup"><span data-stu-id="ec5bb-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ec5bb-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ec5bb-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ec5bb-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec5bb-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ec5bb-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec5bb-232">System-Only</span></span>            | <span data-ttu-id="ec5bb-233">False</span><span class="sxs-lookup"><span data-stu-id="ec5bb-233">False</span></span>                             |
| <span data-ttu-id="ec5bb-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ec5bb-234">Is-Single-Valued</span></span>       | <span data-ttu-id="ec5bb-235">True</span><span class="sxs-lookup"><span data-stu-id="ec5bb-235">True</span></span>                              |
| <span data-ttu-id="ec5bb-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ec5bb-236">Is Indexed</span></span>             | <span data-ttu-id="ec5bb-237">False</span><span class="sxs-lookup"><span data-stu-id="ec5bb-237">False</span></span>                             |
| <span data-ttu-id="ec5bb-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ec5bb-238">In Global Catalog</span></span>      | <span data-ttu-id="ec5bb-239">False</span><span class="sxs-lookup"><span data-stu-id="ec5bb-239">False</span></span>                             |
| <span data-ttu-id="ec5bb-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ec5bb-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec5bb-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec5bb-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ec5bb-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec5bb-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ec5bb-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec5bb-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ec5bb-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5bb-244">Search-Flags</span></span>           | <span data-ttu-id="ec5bb-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec5bb-245">0x00000000</span></span>                        |
| <span data-ttu-id="ec5bb-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5bb-246">System-Flags</span></span>           | <span data-ttu-id="ec5bb-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec5bb-247">0x00000010</span></span>                        |
| <span data-ttu-id="ec5bb-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ec5bb-248">Classes used in</span></span>        | [<span data-ttu-id="ec5bb-249">**User**</span><span class="sxs-lookup"><span data-stu-id="ec5bb-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ec5bb-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec5bb-250">Windows Server 2012</span></span>



| <span data-ttu-id="ec5bb-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec5bb-251">Entry</span></span> | <span data-ttu-id="ec5bb-252">Value</span><span class="sxs-lookup"><span data-stu-id="ec5bb-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ec5bb-253">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ec5bb-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ec5bb-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec5bb-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ec5bb-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec5bb-255">System-Only</span></span>            | <span data-ttu-id="ec5bb-256">False</span><span class="sxs-lookup"><span data-stu-id="ec5bb-256">False</span></span>                             |
| <span data-ttu-id="ec5bb-257">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ec5bb-257">Is-Single-Valued</span></span>       | <span data-ttu-id="ec5bb-258">True</span><span class="sxs-lookup"><span data-stu-id="ec5bb-258">True</span></span>                              |
| <span data-ttu-id="ec5bb-259">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ec5bb-259">Is Indexed</span></span>             | <span data-ttu-id="ec5bb-260">False</span><span class="sxs-lookup"><span data-stu-id="ec5bb-260">False</span></span>                             |
| <span data-ttu-id="ec5bb-261">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ec5bb-261">In Global Catalog</span></span>      | <span data-ttu-id="ec5bb-262">False</span><span class="sxs-lookup"><span data-stu-id="ec5bb-262">False</span></span>                             |
| <span data-ttu-id="ec5bb-263">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ec5bb-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec5bb-264">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec5bb-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ec5bb-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec5bb-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ec5bb-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec5bb-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ec5bb-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5bb-267">Search-Flags</span></span>           | <span data-ttu-id="ec5bb-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec5bb-268">0x00000000</span></span>                        |
| <span data-ttu-id="ec5bb-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5bb-269">System-Flags</span></span>           | <span data-ttu-id="ec5bb-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec5bb-270">0x00000010</span></span>                        |
| <span data-ttu-id="ec5bb-271">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ec5bb-271">Classes used in</span></span>        | [<span data-ttu-id="ec5bb-272">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="ec5bb-272">**User**</span></span>](c-user.md)<br/> |



 

 





