---
title: User-Shared-Folder-Other (atributo)
description: Especifica una ruta de acceso UNC a la carpeta de documentos compartidos adicionales del usuario. La ruta de acceso debe ser una ruta de acceso UNC de red con el formato \\ \\ servidor \\ recurso compartido \\ directorio. Este valor puede ser una cadena nula.
ms.assetid: 7d546cda-b2c1-46a6-a3cf-a7c78ddb1422
ms.tgt_platform: multiple
keywords:
- Usuario-compartido-carpeta-otro esquema de AD de atributos
- userSharedFolderOther esquema de AD de atributos
topic_type:
- apiref
api_name:
- User-Shared-Folder-Other
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6087a28df474ff06c1d8bf54d694176df8591b5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804537"
---
# <a name="user-shared-folder-other-attribute"></a><span data-ttu-id="9491e-107">User-Shared-Folder-Other (atributo)</span><span class="sxs-lookup"><span data-stu-id="9491e-107">User-Shared-Folder-Other attribute</span></span>

<span data-ttu-id="9491e-108">Especifica una ruta de acceso UNC a la carpeta de documentos compartidos adicionales del usuario.</span><span class="sxs-lookup"><span data-stu-id="9491e-108">Specifies a UNC path to the user's additional shared documents folder.</span></span> <span data-ttu-id="9491e-109">La ruta de acceso debe ser una ruta de acceso UNC de red con el formato **\\\\** _servidor_ *_\\_* _recurso compartido_ *_\\_* _directorio_.</span><span class="sxs-lookup"><span data-stu-id="9491e-109">The path must be a network UNC path of the form **\\\\**_Server_*_\\_*_Share_*_\\_*_Directory_.</span></span> <span data-ttu-id="9491e-110">Este valor puede ser una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="9491e-110">This value can be a null string.</span></span>



| <span data-ttu-id="9491e-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="9491e-111">Entry</span></span> | <span data-ttu-id="9491e-112">Value</span><span class="sxs-lookup"><span data-stu-id="9491e-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9491e-113">CN</span><span class="sxs-lookup"><span data-stu-id="9491e-113">CN</span></span>                | <span data-ttu-id="9491e-114">User-Shared-Folder-Other</span><span class="sxs-lookup"><span data-stu-id="9491e-114">User-Shared-Folder-Other</span></span>                                                          |
| <span data-ttu-id="9491e-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="9491e-115">Ldap-Display-Name</span></span> | <span data-ttu-id="9491e-116">userSharedFolderOther</span><span class="sxs-lookup"><span data-stu-id="9491e-116">userSharedFolderOther</span></span>                                                             |
| <span data-ttu-id="9491e-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="9491e-117">Size</span></span>              | \-                                                                                |
| <span data-ttu-id="9491e-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="9491e-118">Update Privilege</span></span>  | <span data-ttu-id="9491e-119">Administrador de dominio o propietario de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="9491e-119">Domain administrator or account owner.</span></span>                                            |
| <span data-ttu-id="9491e-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="9491e-120">Update Frequency</span></span>  | <span data-ttu-id="9491e-121">Cuando se crea el registro del usuario y cada vez que es necesario cambiar la carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="9491e-121">When the user's record is created and whenever the shared folder needs to change.</span></span> |
| <span data-ttu-id="9491e-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9491e-122">Attribute-Id</span></span>      | <span data-ttu-id="9491e-123">1.2.840.113556.1.4.752</span><span class="sxs-lookup"><span data-stu-id="9491e-123">1.2.840.113556.1.4.752</span></span>                                                            |
| <span data-ttu-id="9491e-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9491e-124">System-Id-Guid</span></span>    | <span data-ttu-id="9491e-125">9a9a0220-4a5b-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="9491e-125">9a9a0220-4a5b-11d1-a9c3-0000f80367c1</span></span>                                              |
| <span data-ttu-id="9491e-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9491e-126">Syntax</span></span>            | [<span data-ttu-id="9491e-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9491e-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="9491e-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="9491e-128">Implementations</span></span>

-   [<span data-ttu-id="9491e-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9491e-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9491e-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9491e-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9491e-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9491e-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9491e-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9491e-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9491e-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9491e-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9491e-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9491e-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9491e-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9491e-135">Windows 2000 Server</span></span>



| <span data-ttu-id="9491e-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="9491e-136">Entry</span></span> | <span data-ttu-id="9491e-137">Value</span><span class="sxs-lookup"><span data-stu-id="9491e-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9491e-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9491e-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9491e-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9491e-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9491e-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="9491e-140">System-Only</span></span>            | <span data-ttu-id="9491e-141">False</span><span class="sxs-lookup"><span data-stu-id="9491e-141">False</span></span>                             |
| <span data-ttu-id="9491e-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9491e-142">Is-Single-Valued</span></span>       | <span data-ttu-id="9491e-143">False</span><span class="sxs-lookup"><span data-stu-id="9491e-143">False</span></span>                             |
| <span data-ttu-id="9491e-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9491e-144">Is Indexed</span></span>             | <span data-ttu-id="9491e-145">False</span><span class="sxs-lookup"><span data-stu-id="9491e-145">False</span></span>                             |
| <span data-ttu-id="9491e-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9491e-146">In Global Catalog</span></span>      | <span data-ttu-id="9491e-147">False</span><span class="sxs-lookup"><span data-stu-id="9491e-147">False</span></span>                             |
| <span data-ttu-id="9491e-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9491e-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="9491e-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9491e-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9491e-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9491e-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9491e-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9491e-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9491e-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9491e-152">Search-Flags</span></span>           | <span data-ttu-id="9491e-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9491e-153">0x00000000</span></span>                        |
| <span data-ttu-id="9491e-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9491e-154">System-Flags</span></span>           | <span data-ttu-id="9491e-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9491e-155">0x00000010</span></span>                        |
| <span data-ttu-id="9491e-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9491e-156">Classes used in</span></span>        | [<span data-ttu-id="9491e-157">**User**</span><span class="sxs-lookup"><span data-stu-id="9491e-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9491e-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9491e-158">Windows Server 2003</span></span>



| <span data-ttu-id="9491e-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="9491e-159">Entry</span></span> | <span data-ttu-id="9491e-160">Value</span><span class="sxs-lookup"><span data-stu-id="9491e-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9491e-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9491e-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9491e-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9491e-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9491e-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="9491e-163">System-Only</span></span>            | <span data-ttu-id="9491e-164">False</span><span class="sxs-lookup"><span data-stu-id="9491e-164">False</span></span>                             |
| <span data-ttu-id="9491e-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9491e-165">Is-Single-Valued</span></span>       | <span data-ttu-id="9491e-166">False</span><span class="sxs-lookup"><span data-stu-id="9491e-166">False</span></span>                             |
| <span data-ttu-id="9491e-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9491e-167">Is Indexed</span></span>             | <span data-ttu-id="9491e-168">False</span><span class="sxs-lookup"><span data-stu-id="9491e-168">False</span></span>                             |
| <span data-ttu-id="9491e-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9491e-169">In Global Catalog</span></span>      | <span data-ttu-id="9491e-170">False</span><span class="sxs-lookup"><span data-stu-id="9491e-170">False</span></span>                             |
| <span data-ttu-id="9491e-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9491e-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="9491e-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9491e-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9491e-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9491e-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9491e-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9491e-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9491e-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9491e-175">Search-Flags</span></span>           | <span data-ttu-id="9491e-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9491e-176">0x00000000</span></span>                        |
| <span data-ttu-id="9491e-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9491e-177">System-Flags</span></span>           | <span data-ttu-id="9491e-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9491e-178">0x00000010</span></span>                        |
| <span data-ttu-id="9491e-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9491e-179">Classes used in</span></span>        | [<span data-ttu-id="9491e-180">**User**</span><span class="sxs-lookup"><span data-stu-id="9491e-180">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9491e-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9491e-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9491e-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="9491e-182">Entry</span></span> | <span data-ttu-id="9491e-183">Value</span><span class="sxs-lookup"><span data-stu-id="9491e-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9491e-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9491e-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9491e-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9491e-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9491e-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="9491e-186">System-Only</span></span>            | <span data-ttu-id="9491e-187">False</span><span class="sxs-lookup"><span data-stu-id="9491e-187">False</span></span>                             |
| <span data-ttu-id="9491e-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9491e-188">Is-Single-Valued</span></span>       | <span data-ttu-id="9491e-189">False</span><span class="sxs-lookup"><span data-stu-id="9491e-189">False</span></span>                             |
| <span data-ttu-id="9491e-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9491e-190">Is Indexed</span></span>             | <span data-ttu-id="9491e-191">False</span><span class="sxs-lookup"><span data-stu-id="9491e-191">False</span></span>                             |
| <span data-ttu-id="9491e-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9491e-192">In Global Catalog</span></span>      | <span data-ttu-id="9491e-193">False</span><span class="sxs-lookup"><span data-stu-id="9491e-193">False</span></span>                             |
| <span data-ttu-id="9491e-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9491e-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="9491e-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9491e-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9491e-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9491e-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9491e-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9491e-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9491e-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9491e-198">Search-Flags</span></span>           | <span data-ttu-id="9491e-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9491e-199">0x00000000</span></span>                        |
| <span data-ttu-id="9491e-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9491e-200">System-Flags</span></span>           | <span data-ttu-id="9491e-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9491e-201">0x00000010</span></span>                        |
| <span data-ttu-id="9491e-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9491e-202">Classes used in</span></span>        | [<span data-ttu-id="9491e-203">**User**</span><span class="sxs-lookup"><span data-stu-id="9491e-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9491e-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9491e-204">Windows Server 2008</span></span>



| <span data-ttu-id="9491e-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="9491e-205">Entry</span></span> | <span data-ttu-id="9491e-206">Value</span><span class="sxs-lookup"><span data-stu-id="9491e-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9491e-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9491e-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9491e-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9491e-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9491e-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="9491e-209">System-Only</span></span>            | <span data-ttu-id="9491e-210">False</span><span class="sxs-lookup"><span data-stu-id="9491e-210">False</span></span>                             |
| <span data-ttu-id="9491e-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9491e-211">Is-Single-Valued</span></span>       | <span data-ttu-id="9491e-212">False</span><span class="sxs-lookup"><span data-stu-id="9491e-212">False</span></span>                             |
| <span data-ttu-id="9491e-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9491e-213">Is Indexed</span></span>             | <span data-ttu-id="9491e-214">False</span><span class="sxs-lookup"><span data-stu-id="9491e-214">False</span></span>                             |
| <span data-ttu-id="9491e-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9491e-215">In Global Catalog</span></span>      | <span data-ttu-id="9491e-216">False</span><span class="sxs-lookup"><span data-stu-id="9491e-216">False</span></span>                             |
| <span data-ttu-id="9491e-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9491e-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="9491e-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9491e-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9491e-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9491e-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9491e-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9491e-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9491e-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9491e-221">Search-Flags</span></span>           | <span data-ttu-id="9491e-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9491e-222">0x00000000</span></span>                        |
| <span data-ttu-id="9491e-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9491e-223">System-Flags</span></span>           | <span data-ttu-id="9491e-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9491e-224">0x00000010</span></span>                        |
| <span data-ttu-id="9491e-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9491e-225">Classes used in</span></span>        | [<span data-ttu-id="9491e-226">**User**</span><span class="sxs-lookup"><span data-stu-id="9491e-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9491e-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9491e-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9491e-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="9491e-228">Entry</span></span> | <span data-ttu-id="9491e-229">Value</span><span class="sxs-lookup"><span data-stu-id="9491e-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9491e-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9491e-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9491e-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9491e-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9491e-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="9491e-232">System-Only</span></span>            | <span data-ttu-id="9491e-233">False</span><span class="sxs-lookup"><span data-stu-id="9491e-233">False</span></span>                             |
| <span data-ttu-id="9491e-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9491e-234">Is-Single-Valued</span></span>       | <span data-ttu-id="9491e-235">False</span><span class="sxs-lookup"><span data-stu-id="9491e-235">False</span></span>                             |
| <span data-ttu-id="9491e-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9491e-236">Is Indexed</span></span>             | <span data-ttu-id="9491e-237">False</span><span class="sxs-lookup"><span data-stu-id="9491e-237">False</span></span>                             |
| <span data-ttu-id="9491e-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9491e-238">In Global Catalog</span></span>      | <span data-ttu-id="9491e-239">False</span><span class="sxs-lookup"><span data-stu-id="9491e-239">False</span></span>                             |
| <span data-ttu-id="9491e-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9491e-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="9491e-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9491e-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9491e-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9491e-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9491e-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9491e-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9491e-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9491e-244">Search-Flags</span></span>           | <span data-ttu-id="9491e-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9491e-245">0x00000000</span></span>                        |
| <span data-ttu-id="9491e-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9491e-246">System-Flags</span></span>           | <span data-ttu-id="9491e-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9491e-247">0x00000010</span></span>                        |
| <span data-ttu-id="9491e-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9491e-248">Classes used in</span></span>        | [<span data-ttu-id="9491e-249">**User**</span><span class="sxs-lookup"><span data-stu-id="9491e-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9491e-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9491e-250">Windows Server 2012</span></span>



| <span data-ttu-id="9491e-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="9491e-251">Entry</span></span> | <span data-ttu-id="9491e-252">Value</span><span class="sxs-lookup"><span data-stu-id="9491e-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9491e-253">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9491e-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9491e-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9491e-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9491e-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="9491e-255">System-Only</span></span>            | <span data-ttu-id="9491e-256">False</span><span class="sxs-lookup"><span data-stu-id="9491e-256">False</span></span>                             |
| <span data-ttu-id="9491e-257">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9491e-257">Is-Single-Valued</span></span>       | <span data-ttu-id="9491e-258">False</span><span class="sxs-lookup"><span data-stu-id="9491e-258">False</span></span>                             |
| <span data-ttu-id="9491e-259">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9491e-259">Is Indexed</span></span>             | <span data-ttu-id="9491e-260">False</span><span class="sxs-lookup"><span data-stu-id="9491e-260">False</span></span>                             |
| <span data-ttu-id="9491e-261">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9491e-261">In Global Catalog</span></span>      | <span data-ttu-id="9491e-262">False</span><span class="sxs-lookup"><span data-stu-id="9491e-262">False</span></span>                             |
| <span data-ttu-id="9491e-263">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9491e-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="9491e-264">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9491e-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9491e-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9491e-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9491e-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9491e-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9491e-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9491e-267">Search-Flags</span></span>           | <span data-ttu-id="9491e-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9491e-268">0x00000000</span></span>                        |
| <span data-ttu-id="9491e-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9491e-269">System-Flags</span></span>           | <span data-ttu-id="9491e-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9491e-270">0x00000010</span></span>                        |
| <span data-ttu-id="9491e-271">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9491e-271">Classes used in</span></span>        | [<span data-ttu-id="9491e-272">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="9491e-272">**User**</span></span>](c-user.md)<br/> |



 

 





