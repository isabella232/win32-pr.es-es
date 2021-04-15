---
title: Atributo Manager
description: Contiene el nombre distintivo del usuario que es el administrador del usuario. El objeto de usuario del administrador contiene una propiedad directReports que contiene referencias a todos los objetos de usuario que tienen sus propiedades de administrador establecidas en este nombre distintivo.
ms.assetid: 40743784-a99c-4ec0-9140-9f865c073244
ms.tgt_platform: multiple
keywords:
- Atributo de administrador esquema de AD
- atributo de administrador esquema de AD
topic_type:
- apiref
api_name:
- Manager
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f42c659a436f9798861f5c37df19f8d10db91127
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104422689"
---
# <a name="manager-attribute"></a><span data-ttu-id="80bf0-106">Atributo Manager</span><span class="sxs-lookup"><span data-stu-id="80bf0-106">Manager attribute</span></span>

<span data-ttu-id="80bf0-107">Contiene el nombre distintivo del usuario que es el administrador del usuario.</span><span class="sxs-lookup"><span data-stu-id="80bf0-107">Contains the distinguished name of the user who is the user's manager.</span></span> <span data-ttu-id="80bf0-108">El objeto de usuario del administrador contiene una propiedad directReports que contiene referencias a todos los objetos de usuario que tienen sus propiedades de administrador establecidas en este nombre distintivo.</span><span class="sxs-lookup"><span data-stu-id="80bf0-108">The manager's user object contains a directReports property that contains references to all user objects that have their manager properties set to this distinguished name.</span></span>



| <span data-ttu-id="80bf0-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="80bf0-109">Entry</span></span> | <span data-ttu-id="80bf0-110">Value</span><span class="sxs-lookup"><span data-stu-id="80bf0-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="80bf0-111">CN</span><span class="sxs-lookup"><span data-stu-id="80bf0-111">CN</span></span>                | <span data-ttu-id="80bf0-112">Manager</span><span class="sxs-lookup"><span data-stu-id="80bf0-112">Manager</span></span>                                                                     |
| <span data-ttu-id="80bf0-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="80bf0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="80bf0-114">manager</span><span class="sxs-lookup"><span data-stu-id="80bf0-114">manager</span></span>                                                                     |
| <span data-ttu-id="80bf0-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="80bf0-115">Size</span></span>              | \-                                                                          |
| <span data-ttu-id="80bf0-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="80bf0-116">Update Privilege</span></span>  | <span data-ttu-id="80bf0-117">Administrador de dominio o propietario de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="80bf0-117">Domain administrator or account owner.</span></span>                                      |
| <span data-ttu-id="80bf0-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="80bf0-118">Update Frequency</span></span>  | <span data-ttu-id="80bf0-119">Cuando se crea el registro del usuario y cada vez que el administrador tiene que cambiar.</span><span class="sxs-lookup"><span data-stu-id="80bf0-119">When the user's record is created and whenever the manager needs to change.</span></span> |
| <span data-ttu-id="80bf0-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="80bf0-120">Attribute-Id</span></span>      | <span data-ttu-id="80bf0-121">0.9.2342.19200300.100.1.10</span><span class="sxs-lookup"><span data-stu-id="80bf0-121">0.9.2342.19200300.100.1.10</span></span>                                                  |
| <span data-ttu-id="80bf0-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="80bf0-122">System-Id-Guid</span></span>    | <span data-ttu-id="80bf0-123">bf9679b5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="80bf0-123">bf9679b5-0de6-11d0-a285-00aa003049e2</span></span>                                        |
| <span data-ttu-id="80bf0-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80bf0-124">Syntax</span></span>            | [<span data-ttu-id="80bf0-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="80bf0-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                                     |



## <a name="implementations"></a><span data-ttu-id="80bf0-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="80bf0-126">Implementations</span></span>

-   [<span data-ttu-id="80bf0-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="80bf0-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="80bf0-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="80bf0-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="80bf0-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="80bf0-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="80bf0-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="80bf0-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="80bf0-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="80bf0-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="80bf0-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="80bf0-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="80bf0-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="80bf0-133">Windows 2000 Server</span></span>



| <span data-ttu-id="80bf0-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="80bf0-134">Entry</span></span> | <span data-ttu-id="80bf0-135">Value</span><span class="sxs-lookup"><span data-stu-id="80bf0-135">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="80bf0-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="80bf0-136">Link-Id</span></span>                | <span data-ttu-id="80bf0-137">42</span><span class="sxs-lookup"><span data-stu-id="80bf0-137">42</span></span>                                                                 |
| <span data-ttu-id="80bf0-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80bf0-138">MAPI-Id</span></span>                | <span data-ttu-id="80bf0-139">0x8005</span><span class="sxs-lookup"><span data-stu-id="80bf0-139">0x8005</span></span>                                                             |
| <span data-ttu-id="80bf0-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="80bf0-140">System-Only</span></span>            | <span data-ttu-id="80bf0-141">False</span><span class="sxs-lookup"><span data-stu-id="80bf0-141">False</span></span>                                                              |
| <span data-ttu-id="80bf0-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="80bf0-142">Is-Single-Valued</span></span>       | <span data-ttu-id="80bf0-143">True</span><span class="sxs-lookup"><span data-stu-id="80bf0-143">True</span></span>                                                               |
| <span data-ttu-id="80bf0-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="80bf0-144">Is Indexed</span></span>             | <span data-ttu-id="80bf0-145">False</span><span class="sxs-lookup"><span data-stu-id="80bf0-145">False</span></span>                                                              |
| <span data-ttu-id="80bf0-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="80bf0-146">In Global Catalog</span></span>      | <span data-ttu-id="80bf0-147">True</span><span class="sxs-lookup"><span data-stu-id="80bf0-147">True</span></span>                                                               |
| <span data-ttu-id="80bf0-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="80bf0-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="80bf0-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80bf0-149">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="80bf0-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80bf0-150">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="80bf0-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80bf0-151">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="80bf0-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80bf0-152">Search-Flags</span></span>           | <span data-ttu-id="80bf0-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80bf0-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="80bf0-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80bf0-154">System-Flags</span></span>           | <span data-ttu-id="80bf0-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80bf0-155">0x00000010</span></span>                                                         |
| <span data-ttu-id="80bf0-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="80bf0-156">Classes used in</span></span>        | [<span data-ttu-id="80bf0-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="80bf0-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="80bf0-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="80bf0-158">Windows Server 2003</span></span>



| <span data-ttu-id="80bf0-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="80bf0-159">Entry</span></span> | <span data-ttu-id="80bf0-160">Value</span><span class="sxs-lookup"><span data-stu-id="80bf0-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80bf0-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="80bf0-161">Link-Id</span></span>                | <span data-ttu-id="80bf0-162">42</span><span class="sxs-lookup"><span data-stu-id="80bf0-162">42</span></span>                                                                                                                     |
| <span data-ttu-id="80bf0-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80bf0-163">MAPI-Id</span></span>                | <span data-ttu-id="80bf0-164">0x8005</span><span class="sxs-lookup"><span data-stu-id="80bf0-164">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="80bf0-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="80bf0-165">System-Only</span></span>            | <span data-ttu-id="80bf0-166">False</span><span class="sxs-lookup"><span data-stu-id="80bf0-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="80bf0-167">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="80bf0-167">Is-Single-Valued</span></span>       | <span data-ttu-id="80bf0-168">True</span><span class="sxs-lookup"><span data-stu-id="80bf0-168">True</span></span>                                                                                                                   |
| <span data-ttu-id="80bf0-169">Está indexado</span><span class="sxs-lookup"><span data-stu-id="80bf0-169">Is Indexed</span></span>             | <span data-ttu-id="80bf0-170">False</span><span class="sxs-lookup"><span data-stu-id="80bf0-170">False</span></span>                                                                                                                  |
| <span data-ttu-id="80bf0-171">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="80bf0-171">In Global Catalog</span></span>      | <span data-ttu-id="80bf0-172">True</span><span class="sxs-lookup"><span data-stu-id="80bf0-172">True</span></span>                                                                                                                   |
| <span data-ttu-id="80bf0-173">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="80bf0-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="80bf0-174">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80bf0-174">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="80bf0-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80bf0-175">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="80bf0-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80bf0-176">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="80bf0-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80bf0-177">Search-Flags</span></span>           | <span data-ttu-id="80bf0-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80bf0-178">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="80bf0-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80bf0-179">System-Flags</span></span>           | <span data-ttu-id="80bf0-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80bf0-180">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="80bf0-181">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="80bf0-181">Classes used in</span></span>        | [<span data-ttu-id="80bf0-182">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="80bf0-182">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="80bf0-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="80bf0-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="80bf0-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="80bf0-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="80bf0-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="80bf0-185">Entry</span></span> | <span data-ttu-id="80bf0-186">Value</span><span class="sxs-lookup"><span data-stu-id="80bf0-186">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80bf0-187">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="80bf0-187">Link-Id</span></span>                | <span data-ttu-id="80bf0-188">42</span><span class="sxs-lookup"><span data-stu-id="80bf0-188">42</span></span>                                                                                                                     |
| <span data-ttu-id="80bf0-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80bf0-189">MAPI-Id</span></span>                | <span data-ttu-id="80bf0-190">0x8005</span><span class="sxs-lookup"><span data-stu-id="80bf0-190">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="80bf0-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="80bf0-191">System-Only</span></span>            | <span data-ttu-id="80bf0-192">False</span><span class="sxs-lookup"><span data-stu-id="80bf0-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="80bf0-193">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="80bf0-193">Is-Single-Valued</span></span>       | <span data-ttu-id="80bf0-194">True</span><span class="sxs-lookup"><span data-stu-id="80bf0-194">True</span></span>                                                                                                                   |
| <span data-ttu-id="80bf0-195">Está indexado</span><span class="sxs-lookup"><span data-stu-id="80bf0-195">Is Indexed</span></span>             | <span data-ttu-id="80bf0-196">False</span><span class="sxs-lookup"><span data-stu-id="80bf0-196">False</span></span>                                                                                                                  |
| <span data-ttu-id="80bf0-197">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="80bf0-197">In Global Catalog</span></span>      | <span data-ttu-id="80bf0-198">True</span><span class="sxs-lookup"><span data-stu-id="80bf0-198">True</span></span>                                                                                                                   |
| <span data-ttu-id="80bf0-199">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="80bf0-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="80bf0-200">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80bf0-200">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="80bf0-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80bf0-201">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="80bf0-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80bf0-202">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="80bf0-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80bf0-203">Search-Flags</span></span>           | <span data-ttu-id="80bf0-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80bf0-204">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="80bf0-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80bf0-205">System-Flags</span></span>           | <span data-ttu-id="80bf0-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80bf0-206">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="80bf0-207">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="80bf0-207">Classes used in</span></span>        | [<span data-ttu-id="80bf0-208">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="80bf0-208">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="80bf0-209">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="80bf0-209">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="80bf0-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80bf0-210">Windows Server 2008</span></span>



| <span data-ttu-id="80bf0-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="80bf0-211">Entry</span></span> | <span data-ttu-id="80bf0-212">Value</span><span class="sxs-lookup"><span data-stu-id="80bf0-212">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80bf0-213">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="80bf0-213">Link-Id</span></span>                | <span data-ttu-id="80bf0-214">42</span><span class="sxs-lookup"><span data-stu-id="80bf0-214">42</span></span>                                                                                                                     |
| <span data-ttu-id="80bf0-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80bf0-215">MAPI-Id</span></span>                | <span data-ttu-id="80bf0-216">0x8005</span><span class="sxs-lookup"><span data-stu-id="80bf0-216">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="80bf0-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="80bf0-217">System-Only</span></span>            | <span data-ttu-id="80bf0-218">False</span><span class="sxs-lookup"><span data-stu-id="80bf0-218">False</span></span>                                                                                                                  |
| <span data-ttu-id="80bf0-219">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="80bf0-219">Is-Single-Valued</span></span>       | <span data-ttu-id="80bf0-220">True</span><span class="sxs-lookup"><span data-stu-id="80bf0-220">True</span></span>                                                                                                                   |
| <span data-ttu-id="80bf0-221">Está indexado</span><span class="sxs-lookup"><span data-stu-id="80bf0-221">Is Indexed</span></span>             | <span data-ttu-id="80bf0-222">False</span><span class="sxs-lookup"><span data-stu-id="80bf0-222">False</span></span>                                                                                                                  |
| <span data-ttu-id="80bf0-223">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="80bf0-223">In Global Catalog</span></span>      | <span data-ttu-id="80bf0-224">True</span><span class="sxs-lookup"><span data-stu-id="80bf0-224">True</span></span>                                                                                                                   |
| <span data-ttu-id="80bf0-225">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="80bf0-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="80bf0-226">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80bf0-226">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="80bf0-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80bf0-227">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="80bf0-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80bf0-228">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="80bf0-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80bf0-229">Search-Flags</span></span>           | <span data-ttu-id="80bf0-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80bf0-230">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="80bf0-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80bf0-231">System-Flags</span></span>           | <span data-ttu-id="80bf0-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80bf0-232">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="80bf0-233">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="80bf0-233">Classes used in</span></span>        | [<span data-ttu-id="80bf0-234">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="80bf0-234">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="80bf0-235">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="80bf0-235">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="80bf0-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="80bf0-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="80bf0-237">Entrada</span><span class="sxs-lookup"><span data-stu-id="80bf0-237">Entry</span></span> | <span data-ttu-id="80bf0-238">Value</span><span class="sxs-lookup"><span data-stu-id="80bf0-238">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80bf0-239">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="80bf0-239">Link-Id</span></span>                | <span data-ttu-id="80bf0-240">42</span><span class="sxs-lookup"><span data-stu-id="80bf0-240">42</span></span>                                                                                                                     |
| <span data-ttu-id="80bf0-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80bf0-241">MAPI-Id</span></span>                | <span data-ttu-id="80bf0-242">0x8005</span><span class="sxs-lookup"><span data-stu-id="80bf0-242">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="80bf0-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="80bf0-243">System-Only</span></span>            | <span data-ttu-id="80bf0-244">False</span><span class="sxs-lookup"><span data-stu-id="80bf0-244">False</span></span>                                                                                                                  |
| <span data-ttu-id="80bf0-245">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="80bf0-245">Is-Single-Valued</span></span>       | <span data-ttu-id="80bf0-246">True</span><span class="sxs-lookup"><span data-stu-id="80bf0-246">True</span></span>                                                                                                                   |
| <span data-ttu-id="80bf0-247">Está indexado</span><span class="sxs-lookup"><span data-stu-id="80bf0-247">Is Indexed</span></span>             | <span data-ttu-id="80bf0-248">False</span><span class="sxs-lookup"><span data-stu-id="80bf0-248">False</span></span>                                                                                                                  |
| <span data-ttu-id="80bf0-249">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="80bf0-249">In Global Catalog</span></span>      | <span data-ttu-id="80bf0-250">True</span><span class="sxs-lookup"><span data-stu-id="80bf0-250">True</span></span>                                                                                                                   |
| <span data-ttu-id="80bf0-251">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="80bf0-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="80bf0-252">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80bf0-252">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="80bf0-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80bf0-253">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="80bf0-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80bf0-254">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="80bf0-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80bf0-255">Search-Flags</span></span>           | <span data-ttu-id="80bf0-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80bf0-256">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="80bf0-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80bf0-257">System-Flags</span></span>           | <span data-ttu-id="80bf0-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80bf0-258">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="80bf0-259">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="80bf0-259">Classes used in</span></span>        | [<span data-ttu-id="80bf0-260">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="80bf0-260">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="80bf0-261">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="80bf0-261">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="80bf0-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="80bf0-262">Windows Server 2012</span></span>



| <span data-ttu-id="80bf0-263">Entrada</span><span class="sxs-lookup"><span data-stu-id="80bf0-263">Entry</span></span> | <span data-ttu-id="80bf0-264">Value</span><span class="sxs-lookup"><span data-stu-id="80bf0-264">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80bf0-265">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="80bf0-265">Link-Id</span></span>                | <span data-ttu-id="80bf0-266">42</span><span class="sxs-lookup"><span data-stu-id="80bf0-266">42</span></span>                                                                                                                     |
| <span data-ttu-id="80bf0-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80bf0-267">MAPI-Id</span></span>                | <span data-ttu-id="80bf0-268">0x8005</span><span class="sxs-lookup"><span data-stu-id="80bf0-268">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="80bf0-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="80bf0-269">System-Only</span></span>            | <span data-ttu-id="80bf0-270">False</span><span class="sxs-lookup"><span data-stu-id="80bf0-270">False</span></span>                                                                                                                  |
| <span data-ttu-id="80bf0-271">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="80bf0-271">Is-Single-Valued</span></span>       | <span data-ttu-id="80bf0-272">True</span><span class="sxs-lookup"><span data-stu-id="80bf0-272">True</span></span>                                                                                                                   |
| <span data-ttu-id="80bf0-273">Está indexado</span><span class="sxs-lookup"><span data-stu-id="80bf0-273">Is Indexed</span></span>             | <span data-ttu-id="80bf0-274">False</span><span class="sxs-lookup"><span data-stu-id="80bf0-274">False</span></span>                                                                                                                  |
| <span data-ttu-id="80bf0-275">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="80bf0-275">In Global Catalog</span></span>      | <span data-ttu-id="80bf0-276">True</span><span class="sxs-lookup"><span data-stu-id="80bf0-276">True</span></span>                                                                                                                   |
| <span data-ttu-id="80bf0-277">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="80bf0-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="80bf0-278">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80bf0-278">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="80bf0-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80bf0-279">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="80bf0-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80bf0-280">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="80bf0-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80bf0-281">Search-Flags</span></span>           | <span data-ttu-id="80bf0-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80bf0-282">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="80bf0-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80bf0-283">System-Flags</span></span>           | <span data-ttu-id="80bf0-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80bf0-284">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="80bf0-285">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="80bf0-285">Classes used in</span></span>        | [<span data-ttu-id="80bf0-286">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="80bf0-286">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="80bf0-287">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="80bf0-287">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





