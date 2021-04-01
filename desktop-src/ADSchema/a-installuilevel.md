---
title: Atributo install-UI-LEVEL
description: Este atributo contiene información sobre el tipo (nivel) de instalación que se usa para la interfaz de usuario.
ms.assetid: 718e04c7-ea96-4519-b312-12534ffd66df
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo install-UI-LEVEL
- installUiLevel esquema de AD de atributos
topic_type:
- apiref
api_name:
- Install-Ui-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b93900bb401d1bdcd72f8881fb78026745c4e8f6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997262"
---
# <a name="install-ui-level-attribute"></a><span data-ttu-id="f32cc-105">Atributo install-UI-LEVEL</span><span class="sxs-lookup"><span data-stu-id="f32cc-105">Install-Ui-Level attribute</span></span>

<span data-ttu-id="f32cc-106">Este atributo contiene información sobre el tipo (nivel) de instalación que se usa para la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="f32cc-106">This attribute contains information for the type (level) of installation that is used for the user interface.</span></span> <span data-ttu-id="f32cc-107">Los niveles de instalación posibles son los siguientes: 2 INSTALLUILEVEL \_ ninguno (instalación silenciosa) 3 INSTALLUILEVEL \_ básico (instalación simple con control de errores) 4 INSTALLUILEVEL \_ reducida (IU creada, cuadros de diálogo del asistente suprimidos) 5 INSTALLUILEVEL \_ completo (interfaz de usuario creada con asistentes, progreso, errores)</span><span class="sxs-lookup"><span data-stu-id="f32cc-107">Possible installation levels are as follows: 2 INSTALLUILEVEL\_NONE (silent installation) 3 INSTALLUILEVEL\_BASIC (simple installation with error handling) 4 INSTALLUILEVEL\_REDUCED (authored UI, wizard dialog boxes suppressed) 5 INSTALLUILEVEL\_FULL (authored UI with wizards, progress, errors)</span></span>



| <span data-ttu-id="f32cc-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="f32cc-108">Entry</span></span> | <span data-ttu-id="f32cc-109">Value</span><span class="sxs-lookup"><span data-stu-id="f32cc-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f32cc-110">CN</span><span class="sxs-lookup"><span data-stu-id="f32cc-110">CN</span></span>                | <span data-ttu-id="f32cc-111">Instalar: nivel de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="f32cc-111">Install-Ui-Level</span></span>                     |
| <span data-ttu-id="f32cc-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="f32cc-112">Ldap-Display-Name</span></span> | <span data-ttu-id="f32cc-113">installUiLevel</span><span class="sxs-lookup"><span data-stu-id="f32cc-113">installUiLevel</span></span>                       |
| <span data-ttu-id="f32cc-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f32cc-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="f32cc-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="f32cc-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f32cc-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="f32cc-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f32cc-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f32cc-117">Attribute-Id</span></span>      | <span data-ttu-id="f32cc-118">1.2.840.113556.1.4.847</span><span class="sxs-lookup"><span data-stu-id="f32cc-118">1.2.840.113556.1.4.847</span></span>               |
| <span data-ttu-id="f32cc-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f32cc-119">System-Id-Guid</span></span>    | <span data-ttu-id="f32cc-120">96a7dd64-9118-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="f32cc-120">96a7dd64-9118-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="f32cc-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f32cc-121">Syntax</span></span>            | [<span data-ttu-id="f32cc-122">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="f32cc-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="f32cc-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="f32cc-123">Implementations</span></span>

-   [<span data-ttu-id="f32cc-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f32cc-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f32cc-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f32cc-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f32cc-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f32cc-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f32cc-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f32cc-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f32cc-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f32cc-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f32cc-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f32cc-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f32cc-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f32cc-130">Windows 2000 Server</span></span>



| <span data-ttu-id="f32cc-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="f32cc-131">Entry</span></span> | <span data-ttu-id="f32cc-132">Value</span><span class="sxs-lookup"><span data-stu-id="f32cc-132">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f32cc-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f32cc-133">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f32cc-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f32cc-134">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f32cc-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="f32cc-135">System-Only</span></span>            | <span data-ttu-id="f32cc-136">False</span><span class="sxs-lookup"><span data-stu-id="f32cc-136">False</span></span>                                                            |
| <span data-ttu-id="f32cc-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f32cc-137">Is-Single-Valued</span></span>       | <span data-ttu-id="f32cc-138">True</span><span class="sxs-lookup"><span data-stu-id="f32cc-138">True</span></span>                                                             |
| <span data-ttu-id="f32cc-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f32cc-139">Is Indexed</span></span>             | <span data-ttu-id="f32cc-140">False</span><span class="sxs-lookup"><span data-stu-id="f32cc-140">False</span></span>                                                            |
| <span data-ttu-id="f32cc-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f32cc-141">In Global Catalog</span></span>      | <span data-ttu-id="f32cc-142">False</span><span class="sxs-lookup"><span data-stu-id="f32cc-142">False</span></span>                                                            |
| <span data-ttu-id="f32cc-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f32cc-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="f32cc-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f32cc-144">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f32cc-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f32cc-145">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f32cc-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f32cc-146">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f32cc-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f32cc-147">Search-Flags</span></span>           | <span data-ttu-id="f32cc-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f32cc-148">0x00000000</span></span>                                                       |
| <span data-ttu-id="f32cc-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f32cc-149">System-Flags</span></span>           | <span data-ttu-id="f32cc-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f32cc-150">0x00000010</span></span>                                                       |
| <span data-ttu-id="f32cc-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f32cc-151">Classes used in</span></span>        | [<span data-ttu-id="f32cc-152">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="f32cc-152">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f32cc-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f32cc-153">Windows Server 2003</span></span>



| <span data-ttu-id="f32cc-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="f32cc-154">Entry</span></span> | <span data-ttu-id="f32cc-155">Value</span><span class="sxs-lookup"><span data-stu-id="f32cc-155">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f32cc-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f32cc-156">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f32cc-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f32cc-157">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f32cc-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="f32cc-158">System-Only</span></span>            | <span data-ttu-id="f32cc-159">False</span><span class="sxs-lookup"><span data-stu-id="f32cc-159">False</span></span>                                                            |
| <span data-ttu-id="f32cc-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f32cc-160">Is-Single-Valued</span></span>       | <span data-ttu-id="f32cc-161">True</span><span class="sxs-lookup"><span data-stu-id="f32cc-161">True</span></span>                                                             |
| <span data-ttu-id="f32cc-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f32cc-162">Is Indexed</span></span>             | <span data-ttu-id="f32cc-163">False</span><span class="sxs-lookup"><span data-stu-id="f32cc-163">False</span></span>                                                            |
| <span data-ttu-id="f32cc-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f32cc-164">In Global Catalog</span></span>      | <span data-ttu-id="f32cc-165">False</span><span class="sxs-lookup"><span data-stu-id="f32cc-165">False</span></span>                                                            |
| <span data-ttu-id="f32cc-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f32cc-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="f32cc-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f32cc-167">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f32cc-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f32cc-168">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f32cc-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f32cc-169">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f32cc-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f32cc-170">Search-Flags</span></span>           | <span data-ttu-id="f32cc-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f32cc-171">0x00000000</span></span>                                                       |
| <span data-ttu-id="f32cc-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f32cc-172">System-Flags</span></span>           | <span data-ttu-id="f32cc-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f32cc-173">0x00000010</span></span>                                                       |
| <span data-ttu-id="f32cc-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f32cc-174">Classes used in</span></span>        | [<span data-ttu-id="f32cc-175">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="f32cc-175">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f32cc-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f32cc-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f32cc-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="f32cc-177">Entry</span></span> | <span data-ttu-id="f32cc-178">Value</span><span class="sxs-lookup"><span data-stu-id="f32cc-178">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f32cc-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f32cc-179">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f32cc-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f32cc-180">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f32cc-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="f32cc-181">System-Only</span></span>            | <span data-ttu-id="f32cc-182">False</span><span class="sxs-lookup"><span data-stu-id="f32cc-182">False</span></span>                                                            |
| <span data-ttu-id="f32cc-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f32cc-183">Is-Single-Valued</span></span>       | <span data-ttu-id="f32cc-184">True</span><span class="sxs-lookup"><span data-stu-id="f32cc-184">True</span></span>                                                             |
| <span data-ttu-id="f32cc-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f32cc-185">Is Indexed</span></span>             | <span data-ttu-id="f32cc-186">False</span><span class="sxs-lookup"><span data-stu-id="f32cc-186">False</span></span>                                                            |
| <span data-ttu-id="f32cc-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f32cc-187">In Global Catalog</span></span>      | <span data-ttu-id="f32cc-188">False</span><span class="sxs-lookup"><span data-stu-id="f32cc-188">False</span></span>                                                            |
| <span data-ttu-id="f32cc-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f32cc-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="f32cc-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f32cc-190">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f32cc-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f32cc-191">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f32cc-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f32cc-192">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f32cc-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f32cc-193">Search-Flags</span></span>           | <span data-ttu-id="f32cc-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f32cc-194">0x00000000</span></span>                                                       |
| <span data-ttu-id="f32cc-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f32cc-195">System-Flags</span></span>           | <span data-ttu-id="f32cc-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f32cc-196">0x00000010</span></span>                                                       |
| <span data-ttu-id="f32cc-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f32cc-197">Classes used in</span></span>        | [<span data-ttu-id="f32cc-198">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="f32cc-198">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f32cc-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f32cc-199">Windows Server 2008</span></span>



| <span data-ttu-id="f32cc-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="f32cc-200">Entry</span></span> | <span data-ttu-id="f32cc-201">Value</span><span class="sxs-lookup"><span data-stu-id="f32cc-201">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f32cc-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f32cc-202">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f32cc-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f32cc-203">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f32cc-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="f32cc-204">System-Only</span></span>            | <span data-ttu-id="f32cc-205">False</span><span class="sxs-lookup"><span data-stu-id="f32cc-205">False</span></span>                                                            |
| <span data-ttu-id="f32cc-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f32cc-206">Is-Single-Valued</span></span>       | <span data-ttu-id="f32cc-207">True</span><span class="sxs-lookup"><span data-stu-id="f32cc-207">True</span></span>                                                             |
| <span data-ttu-id="f32cc-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f32cc-208">Is Indexed</span></span>             | <span data-ttu-id="f32cc-209">False</span><span class="sxs-lookup"><span data-stu-id="f32cc-209">False</span></span>                                                            |
| <span data-ttu-id="f32cc-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f32cc-210">In Global Catalog</span></span>      | <span data-ttu-id="f32cc-211">False</span><span class="sxs-lookup"><span data-stu-id="f32cc-211">False</span></span>                                                            |
| <span data-ttu-id="f32cc-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f32cc-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="f32cc-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f32cc-213">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f32cc-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f32cc-214">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f32cc-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f32cc-215">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f32cc-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f32cc-216">Search-Flags</span></span>           | <span data-ttu-id="f32cc-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f32cc-217">0x00000000</span></span>                                                       |
| <span data-ttu-id="f32cc-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f32cc-218">System-Flags</span></span>           | <span data-ttu-id="f32cc-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f32cc-219">0x00000010</span></span>                                                       |
| <span data-ttu-id="f32cc-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f32cc-220">Classes used in</span></span>        | [<span data-ttu-id="f32cc-221">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="f32cc-221">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f32cc-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f32cc-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f32cc-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="f32cc-223">Entry</span></span> | <span data-ttu-id="f32cc-224">Value</span><span class="sxs-lookup"><span data-stu-id="f32cc-224">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f32cc-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f32cc-225">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f32cc-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f32cc-226">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f32cc-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="f32cc-227">System-Only</span></span>            | <span data-ttu-id="f32cc-228">False</span><span class="sxs-lookup"><span data-stu-id="f32cc-228">False</span></span>                                                            |
| <span data-ttu-id="f32cc-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f32cc-229">Is-Single-Valued</span></span>       | <span data-ttu-id="f32cc-230">True</span><span class="sxs-lookup"><span data-stu-id="f32cc-230">True</span></span>                                                             |
| <span data-ttu-id="f32cc-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f32cc-231">Is Indexed</span></span>             | <span data-ttu-id="f32cc-232">False</span><span class="sxs-lookup"><span data-stu-id="f32cc-232">False</span></span>                                                            |
| <span data-ttu-id="f32cc-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f32cc-233">In Global Catalog</span></span>      | <span data-ttu-id="f32cc-234">False</span><span class="sxs-lookup"><span data-stu-id="f32cc-234">False</span></span>                                                            |
| <span data-ttu-id="f32cc-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f32cc-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="f32cc-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f32cc-236">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f32cc-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f32cc-237">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f32cc-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f32cc-238">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f32cc-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f32cc-239">Search-Flags</span></span>           | <span data-ttu-id="f32cc-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f32cc-240">0x00000000</span></span>                                                       |
| <span data-ttu-id="f32cc-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f32cc-241">System-Flags</span></span>           | <span data-ttu-id="f32cc-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f32cc-242">0x00000010</span></span>                                                       |
| <span data-ttu-id="f32cc-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f32cc-243">Classes used in</span></span>        | [<span data-ttu-id="f32cc-244">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="f32cc-244">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f32cc-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f32cc-245">Windows Server 2012</span></span>



| <span data-ttu-id="f32cc-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="f32cc-246">Entry</span></span> | <span data-ttu-id="f32cc-247">Value</span><span class="sxs-lookup"><span data-stu-id="f32cc-247">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f32cc-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f32cc-248">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f32cc-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f32cc-249">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f32cc-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="f32cc-250">System-Only</span></span>            | <span data-ttu-id="f32cc-251">False</span><span class="sxs-lookup"><span data-stu-id="f32cc-251">False</span></span>                                                            |
| <span data-ttu-id="f32cc-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f32cc-252">Is-Single-Valued</span></span>       | <span data-ttu-id="f32cc-253">True</span><span class="sxs-lookup"><span data-stu-id="f32cc-253">True</span></span>                                                             |
| <span data-ttu-id="f32cc-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f32cc-254">Is Indexed</span></span>             | <span data-ttu-id="f32cc-255">False</span><span class="sxs-lookup"><span data-stu-id="f32cc-255">False</span></span>                                                            |
| <span data-ttu-id="f32cc-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f32cc-256">In Global Catalog</span></span>      | <span data-ttu-id="f32cc-257">False</span><span class="sxs-lookup"><span data-stu-id="f32cc-257">False</span></span>                                                            |
| <span data-ttu-id="f32cc-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f32cc-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="f32cc-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f32cc-259">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f32cc-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f32cc-260">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f32cc-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f32cc-261">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f32cc-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f32cc-262">Search-Flags</span></span>           | <span data-ttu-id="f32cc-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f32cc-263">0x00000000</span></span>                                                       |
| <span data-ttu-id="f32cc-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f32cc-264">System-Flags</span></span>           | <span data-ttu-id="f32cc-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f32cc-265">0x00000010</span></span>                                                       |
| <span data-ttu-id="f32cc-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f32cc-266">Classes used in</span></span>        | [<span data-ttu-id="f32cc-267">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="f32cc-267">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





