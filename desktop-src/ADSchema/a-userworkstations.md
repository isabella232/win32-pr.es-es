---
title: User-Workstations atributo)
description: Contiene los nombres NetBIOS o DNS de los equipos que ejecutan Windows NT Workstation o Windows 2000 Professional desde los que el usuario puede iniciar sesión.
ms.assetid: 92af070b-dadd-404d-8305-d85974639958
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de User-Workstations
- userWorkstations esquema de AD de atributos
topic_type:
- apiref
api_name:
- User-Workstations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cad59905dbf24c8baa13969d9a2ce5452767163
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905903"
---
# <a name="user-workstations-attribute"></a><span data-ttu-id="8436c-105">User-Workstations atributo)</span><span class="sxs-lookup"><span data-stu-id="8436c-105">User-Workstations attribute</span></span>

<span data-ttu-id="8436c-106">Contiene los nombres NetBIOS o DNS de los equipos que ejecutan Windows NT Workstation o Windows 2000 Professional desde los que el usuario puede iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="8436c-106">Contains the NetBIOS or DNS names of the computers running Windows NT Workstation or Windows 2000 Professional from which the user can log on.</span></span> <span data-ttu-id="8436c-107">Cada nombre NetBIOS está separado por una coma.</span><span class="sxs-lookup"><span data-stu-id="8436c-107">Each NetBIOS name is separated by a comma.</span></span> <span data-ttu-id="8436c-108">Los nombres múltiples deben separarse con comas.</span><span class="sxs-lookup"><span data-stu-id="8436c-108">Multiple names should be separated by commas.</span></span>

>[!Note]
><span data-ttu-id="8436c-109">Este atributo de usuario ya no se debe usar.</span><span class="sxs-lookup"><span data-stu-id="8436c-109">This user attribute should not be used anymore.</span></span> <span data-ttu-id="8436c-110">Para administrar qué cuentas pueden iniciar sesión en cada estación de trabajo, se recomienda usar "permitir el inicio de sesión local" y "denegar el inicio de sesión local" o "permitir el inicio de sesión a través de Servicios de Escritorio remoto" y "denegar el inicio de sesión a través de Servicios de Escritorio remoto".</span><span class="sxs-lookup"><span data-stu-id="8436c-110">To manage what accounts can logon to which workstations, we recommend using the “Allow Log on locally” and “Deny Log on locally” or “Allow log on through Remote Desktop Services” and “Deny log on through Remote Desktop Services”.</span></span>

| <span data-ttu-id="8436c-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="8436c-111">Entry</span></span> | <span data-ttu-id="8436c-112">Value</span><span class="sxs-lookup"><span data-stu-id="8436c-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8436c-113">CN</span><span class="sxs-lookup"><span data-stu-id="8436c-113">CN</span></span>                | <span data-ttu-id="8436c-114">User-Workstations</span><span class="sxs-lookup"><span data-stu-id="8436c-114">User-Workstations</span></span>                                                                          |
| <span data-ttu-id="8436c-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="8436c-115">Ldap-Display-Name</span></span> | <span data-ttu-id="8436c-116">userWorkstations</span><span class="sxs-lookup"><span data-stu-id="8436c-116">userWorkstations</span></span>                                                                           |
| <span data-ttu-id="8436c-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="8436c-117">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="8436c-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="8436c-118">Update Privilege</span></span>  | <span data-ttu-id="8436c-119">Administrador de dominio o propietario de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="8436c-119">Domain administrator or account owner.</span></span>                                                     |
| <span data-ttu-id="8436c-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="8436c-120">Update Frequency</span></span>  | <span data-ttu-id="8436c-121">Cuando se crea el registro del usuario y cada vez que es necesario cambiar el privilegio de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="8436c-121">When the user's record is created and whenever the user's login privilege needs to change.</span></span> |
| <span data-ttu-id="8436c-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8436c-122">Attribute-Id</span></span>      | <span data-ttu-id="8436c-123">1.2.840.113556.1.4.86</span><span class="sxs-lookup"><span data-stu-id="8436c-123">1.2.840.113556.1.4.86</span></span>                                                                      |
| <span data-ttu-id="8436c-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8436c-124">System-Id-Guid</span></span>    | <span data-ttu-id="8436c-125">bf9679d7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8436c-125">bf9679d7-0de6-11d0-a285-00aa003049e2</span></span>                                                       |
| <span data-ttu-id="8436c-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8436c-126">Syntax</span></span>            | [<span data-ttu-id="8436c-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="8436c-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="8436c-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="8436c-128">Implementations</span></span>

-   [<span data-ttu-id="8436c-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8436c-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8436c-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8436c-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8436c-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8436c-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8436c-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8436c-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8436c-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8436c-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8436c-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8436c-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8436c-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8436c-135">Windows 2000 Server</span></span>



| <span data-ttu-id="8436c-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="8436c-136">Entry</span></span> | <span data-ttu-id="8436c-137">Value</span><span class="sxs-lookup"><span data-stu-id="8436c-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8436c-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8436c-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8436c-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8436c-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8436c-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="8436c-140">System-Only</span></span>            | <span data-ttu-id="8436c-141">False</span><span class="sxs-lookup"><span data-stu-id="8436c-141">False</span></span>                             |
| <span data-ttu-id="8436c-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8436c-142">Is-Single-Valued</span></span>       | <span data-ttu-id="8436c-143">True</span><span class="sxs-lookup"><span data-stu-id="8436c-143">True</span></span>                              |
| <span data-ttu-id="8436c-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8436c-144">Is Indexed</span></span>             | <span data-ttu-id="8436c-145">False</span><span class="sxs-lookup"><span data-stu-id="8436c-145">False</span></span>                             |
| <span data-ttu-id="8436c-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8436c-146">In Global Catalog</span></span>      | <span data-ttu-id="8436c-147">False</span><span class="sxs-lookup"><span data-stu-id="8436c-147">False</span></span>                             |
| <span data-ttu-id="8436c-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8436c-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="8436c-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8436c-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8436c-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8436c-150">Range-Lower</span></span>            | <span data-ttu-id="8436c-151">0</span><span class="sxs-lookup"><span data-stu-id="8436c-151">0</span></span>                                 |
| <span data-ttu-id="8436c-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8436c-152">Range-Upper</span></span>            | <span data-ttu-id="8436c-153">1024</span><span class="sxs-lookup"><span data-stu-id="8436c-153">1024</span></span>                              |
| <span data-ttu-id="8436c-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8436c-154">Search-Flags</span></span>           | <span data-ttu-id="8436c-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8436c-155">0x00000010</span></span>                        |
| <span data-ttu-id="8436c-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8436c-156">System-Flags</span></span>           | <span data-ttu-id="8436c-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8436c-157">0x00000010</span></span>                        |
| <span data-ttu-id="8436c-158">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8436c-158">Classes used in</span></span>        | [<span data-ttu-id="8436c-159">**User**</span><span class="sxs-lookup"><span data-stu-id="8436c-159">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8436c-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8436c-160">Windows Server 2003</span></span>



| <span data-ttu-id="8436c-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="8436c-161">Entry</span></span> | <span data-ttu-id="8436c-162">Value</span><span class="sxs-lookup"><span data-stu-id="8436c-162">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8436c-163">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8436c-163">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8436c-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8436c-164">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8436c-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="8436c-165">System-Only</span></span>            | <span data-ttu-id="8436c-166">False</span><span class="sxs-lookup"><span data-stu-id="8436c-166">False</span></span>                             |
| <span data-ttu-id="8436c-167">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8436c-167">Is-Single-Valued</span></span>       | <span data-ttu-id="8436c-168">True</span><span class="sxs-lookup"><span data-stu-id="8436c-168">True</span></span>                              |
| <span data-ttu-id="8436c-169">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8436c-169">Is Indexed</span></span>             | <span data-ttu-id="8436c-170">False</span><span class="sxs-lookup"><span data-stu-id="8436c-170">False</span></span>                             |
| <span data-ttu-id="8436c-171">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8436c-171">In Global Catalog</span></span>      | <span data-ttu-id="8436c-172">False</span><span class="sxs-lookup"><span data-stu-id="8436c-172">False</span></span>                             |
| <span data-ttu-id="8436c-173">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8436c-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="8436c-174">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8436c-174">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8436c-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8436c-175">Range-Lower</span></span>            | <span data-ttu-id="8436c-176">0</span><span class="sxs-lookup"><span data-stu-id="8436c-176">0</span></span>                                 |
| <span data-ttu-id="8436c-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8436c-177">Range-Upper</span></span>            | <span data-ttu-id="8436c-178">1024</span><span class="sxs-lookup"><span data-stu-id="8436c-178">1024</span></span>                              |
| <span data-ttu-id="8436c-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8436c-179">Search-Flags</span></span>           | <span data-ttu-id="8436c-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8436c-180">0x00000010</span></span>                        |
| <span data-ttu-id="8436c-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8436c-181">System-Flags</span></span>           | <span data-ttu-id="8436c-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8436c-182">0x00000010</span></span>                        |
| <span data-ttu-id="8436c-183">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8436c-183">Classes used in</span></span>        | [<span data-ttu-id="8436c-184">**User**</span><span class="sxs-lookup"><span data-stu-id="8436c-184">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8436c-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8436c-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8436c-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="8436c-186">Entry</span></span> | <span data-ttu-id="8436c-187">Value</span><span class="sxs-lookup"><span data-stu-id="8436c-187">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8436c-188">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8436c-188">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8436c-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8436c-189">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8436c-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="8436c-190">System-Only</span></span>            | <span data-ttu-id="8436c-191">False</span><span class="sxs-lookup"><span data-stu-id="8436c-191">False</span></span>                             |
| <span data-ttu-id="8436c-192">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8436c-192">Is-Single-Valued</span></span>       | <span data-ttu-id="8436c-193">True</span><span class="sxs-lookup"><span data-stu-id="8436c-193">True</span></span>                              |
| <span data-ttu-id="8436c-194">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8436c-194">Is Indexed</span></span>             | <span data-ttu-id="8436c-195">False</span><span class="sxs-lookup"><span data-stu-id="8436c-195">False</span></span>                             |
| <span data-ttu-id="8436c-196">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8436c-196">In Global Catalog</span></span>      | <span data-ttu-id="8436c-197">False</span><span class="sxs-lookup"><span data-stu-id="8436c-197">False</span></span>                             |
| <span data-ttu-id="8436c-198">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8436c-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="8436c-199">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8436c-199">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8436c-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8436c-200">Range-Lower</span></span>            | <span data-ttu-id="8436c-201">0</span><span class="sxs-lookup"><span data-stu-id="8436c-201">0</span></span>                                 |
| <span data-ttu-id="8436c-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8436c-202">Range-Upper</span></span>            | <span data-ttu-id="8436c-203">1024</span><span class="sxs-lookup"><span data-stu-id="8436c-203">1024</span></span>                              |
| <span data-ttu-id="8436c-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8436c-204">Search-Flags</span></span>           | <span data-ttu-id="8436c-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8436c-205">0x00000010</span></span>                        |
| <span data-ttu-id="8436c-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8436c-206">System-Flags</span></span>           | <span data-ttu-id="8436c-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8436c-207">0x00000010</span></span>                        |
| <span data-ttu-id="8436c-208">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8436c-208">Classes used in</span></span>        | [<span data-ttu-id="8436c-209">**User**</span><span class="sxs-lookup"><span data-stu-id="8436c-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8436c-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8436c-210">Windows Server 2008</span></span>



| <span data-ttu-id="8436c-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="8436c-211">Entry</span></span> | <span data-ttu-id="8436c-212">Value</span><span class="sxs-lookup"><span data-stu-id="8436c-212">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8436c-213">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8436c-213">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8436c-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8436c-214">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8436c-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="8436c-215">System-Only</span></span>            | <span data-ttu-id="8436c-216">False</span><span class="sxs-lookup"><span data-stu-id="8436c-216">False</span></span>                             |
| <span data-ttu-id="8436c-217">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8436c-217">Is-Single-Valued</span></span>       | <span data-ttu-id="8436c-218">True</span><span class="sxs-lookup"><span data-stu-id="8436c-218">True</span></span>                              |
| <span data-ttu-id="8436c-219">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8436c-219">Is Indexed</span></span>             | <span data-ttu-id="8436c-220">False</span><span class="sxs-lookup"><span data-stu-id="8436c-220">False</span></span>                             |
| <span data-ttu-id="8436c-221">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8436c-221">In Global Catalog</span></span>      | <span data-ttu-id="8436c-222">False</span><span class="sxs-lookup"><span data-stu-id="8436c-222">False</span></span>                             |
| <span data-ttu-id="8436c-223">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8436c-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="8436c-224">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8436c-224">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8436c-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8436c-225">Range-Lower</span></span>            | <span data-ttu-id="8436c-226">0</span><span class="sxs-lookup"><span data-stu-id="8436c-226">0</span></span>                                 |
| <span data-ttu-id="8436c-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8436c-227">Range-Upper</span></span>            | <span data-ttu-id="8436c-228">1024</span><span class="sxs-lookup"><span data-stu-id="8436c-228">1024</span></span>                              |
| <span data-ttu-id="8436c-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8436c-229">Search-Flags</span></span>           | <span data-ttu-id="8436c-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8436c-230">0x00000010</span></span>                        |
| <span data-ttu-id="8436c-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8436c-231">System-Flags</span></span>           | <span data-ttu-id="8436c-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8436c-232">0x00000010</span></span>                        |
| <span data-ttu-id="8436c-233">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8436c-233">Classes used in</span></span>        | [<span data-ttu-id="8436c-234">**User**</span><span class="sxs-lookup"><span data-stu-id="8436c-234">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8436c-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8436c-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8436c-236">Entrada</span><span class="sxs-lookup"><span data-stu-id="8436c-236">Entry</span></span> | <span data-ttu-id="8436c-237">Value</span><span class="sxs-lookup"><span data-stu-id="8436c-237">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8436c-238">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8436c-238">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8436c-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8436c-239">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8436c-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="8436c-240">System-Only</span></span>            | <span data-ttu-id="8436c-241">False</span><span class="sxs-lookup"><span data-stu-id="8436c-241">False</span></span>                             |
| <span data-ttu-id="8436c-242">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8436c-242">Is-Single-Valued</span></span>       | <span data-ttu-id="8436c-243">True</span><span class="sxs-lookup"><span data-stu-id="8436c-243">True</span></span>                              |
| <span data-ttu-id="8436c-244">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8436c-244">Is Indexed</span></span>             | <span data-ttu-id="8436c-245">False</span><span class="sxs-lookup"><span data-stu-id="8436c-245">False</span></span>                             |
| <span data-ttu-id="8436c-246">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8436c-246">In Global Catalog</span></span>      | <span data-ttu-id="8436c-247">False</span><span class="sxs-lookup"><span data-stu-id="8436c-247">False</span></span>                             |
| <span data-ttu-id="8436c-248">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8436c-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="8436c-249">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8436c-249">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8436c-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8436c-250">Range-Lower</span></span>            | <span data-ttu-id="8436c-251">0</span><span class="sxs-lookup"><span data-stu-id="8436c-251">0</span></span>                                 |
| <span data-ttu-id="8436c-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8436c-252">Range-Upper</span></span>            | <span data-ttu-id="8436c-253">1024</span><span class="sxs-lookup"><span data-stu-id="8436c-253">1024</span></span>                              |
| <span data-ttu-id="8436c-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8436c-254">Search-Flags</span></span>           | <span data-ttu-id="8436c-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8436c-255">0x00000010</span></span>                        |
| <span data-ttu-id="8436c-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8436c-256">System-Flags</span></span>           | <span data-ttu-id="8436c-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8436c-257">0x00000010</span></span>                        |
| <span data-ttu-id="8436c-258">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8436c-258">Classes used in</span></span>        | [<span data-ttu-id="8436c-259">**User**</span><span class="sxs-lookup"><span data-stu-id="8436c-259">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8436c-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8436c-260">Windows Server 2012</span></span>



| <span data-ttu-id="8436c-261">Entrada</span><span class="sxs-lookup"><span data-stu-id="8436c-261">Entry</span></span> | <span data-ttu-id="8436c-262">Value</span><span class="sxs-lookup"><span data-stu-id="8436c-262">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8436c-263">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8436c-263">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8436c-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8436c-264">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8436c-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="8436c-265">System-Only</span></span>            | <span data-ttu-id="8436c-266">False</span><span class="sxs-lookup"><span data-stu-id="8436c-266">False</span></span>                             |
| <span data-ttu-id="8436c-267">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8436c-267">Is-Single-Valued</span></span>       | <span data-ttu-id="8436c-268">True</span><span class="sxs-lookup"><span data-stu-id="8436c-268">True</span></span>                              |
| <span data-ttu-id="8436c-269">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8436c-269">Is Indexed</span></span>             | <span data-ttu-id="8436c-270">False</span><span class="sxs-lookup"><span data-stu-id="8436c-270">False</span></span>                             |
| <span data-ttu-id="8436c-271">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8436c-271">In Global Catalog</span></span>      | <span data-ttu-id="8436c-272">False</span><span class="sxs-lookup"><span data-stu-id="8436c-272">False</span></span>                             |
| <span data-ttu-id="8436c-273">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8436c-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="8436c-274">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8436c-274">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8436c-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8436c-275">Range-Lower</span></span>            | <span data-ttu-id="8436c-276">0</span><span class="sxs-lookup"><span data-stu-id="8436c-276">0</span></span>                                 |
| <span data-ttu-id="8436c-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8436c-277">Range-Upper</span></span>            | <span data-ttu-id="8436c-278">1024</span><span class="sxs-lookup"><span data-stu-id="8436c-278">1024</span></span>                              |
| <span data-ttu-id="8436c-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8436c-279">Search-Flags</span></span>           | <span data-ttu-id="8436c-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8436c-280">0x00000010</span></span>                        |
| <span data-ttu-id="8436c-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8436c-281">System-Flags</span></span>           | <span data-ttu-id="8436c-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8436c-282">0x00000010</span></span>                        |
| <span data-ttu-id="8436c-283">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8436c-283">Classes used in</span></span>        | [<span data-ttu-id="8436c-284">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="8436c-284">**User**</span></span>](c-user.md)<br/> |



 

 





