---
title: Atributo Well-Known-Objects
description: Este atributo contiene una lista de contenedores de objetos conocidos por GUID y nombre distintivo.
ms.assetid: e3c2d243-6734-4c2f-9ead-bc4ec071d1f1
ms.tgt_platform: multiple
keywords:
- Well-know-Attributes Schema AD Schema
- wellKnownObjects esquema de AD de atributos
topic_type:
- apiref
api_name:
- Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e21df3db14a29de137af4792f0e9ca6df27b90
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493900"
---
# <a name="well-known-objects-attribute"></a><span data-ttu-id="46417-105">Atributo Well-Known-Objects</span><span class="sxs-lookup"><span data-stu-id="46417-105">Well-Known-Objects attribute</span></span>

<span data-ttu-id="46417-106">Este atributo contiene una lista de contenedores de objetos conocidos por GUID y nombre distintivo.</span><span class="sxs-lookup"><span data-stu-id="46417-106">This attribute contains a list of well-known object containers by GUID and distinguished name.</span></span> <span data-ttu-id="46417-107">Los objetos conocidos son contenedores del sistema.</span><span class="sxs-lookup"><span data-stu-id="46417-107">The well-known objects are system containers.</span></span> <span data-ttu-id="46417-108">Esta información se usa para recuperar un objeto una vez que se ha colocado usando solo el GUID y el nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="46417-108">This information is used to retrieve an object after it has been moved by using just the GUID and the domain name.</span></span> <span data-ttu-id="46417-109">Cada vez que se mueve el objeto, el sistema actualiza automáticamente la parte del nombre distintivo de los valores de objetos conocidos que hacía referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="46417-109">Whenever the object is moved, the system automatically updates the Distinguished Name portion of the Well-Known-Objects values that referred to the object.</span></span> <span data-ttu-id="46417-110">El archivo ntdsapi. h contiene las siguientes definiciones, que se pueden usar para recuperar un objeto (los GUID que están asociados a estos objetos están contenidos en ntdsapi. h):</span><span class="sxs-lookup"><span data-stu-id="46417-110">The file Ntdsapi.h contains the following definitions, which can be used to retrieve an object (the GUIDs that are associated to these objects are contained in Ntdsapi.h):</span></span>

-   <span data-ttu-id="46417-111">contenedor de usuarios de GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="46417-111">GUID\_USERS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="46417-112">\_contenedor de calculadores GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="46417-112">GUID\_COMPUTRS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="46417-113">\_contenedor de sistemas GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="46417-113">GUID\_SYSTEMS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="46417-114">\_contenedor de controladores de dominio GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="46417-114">GUID\_DOMAIN\_CONTROLLERS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="46417-115">\_contenedor de infraestructura GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="46417-115">GUID\_INFRASTRUCTURE\_CONTAINER\_W</span></span>
-   <span data-ttu-id="46417-116">\_contenedor de objetos eliminados de GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="46417-116">GUID\_DELETED\_OBJECTS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="46417-117">contenedor de GUID \_ LOSTANDFOUND \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="46417-117">GUID\_LOSTANDFOUND\_CONTAINER\_W</span></span>
-   <span data-ttu-id="46417-118">GUID \_ FOREIGNSECURITYPRINCIPALS \_ contenedor \_ W</span><span class="sxs-lookup"><span data-stu-id="46417-118">GUID\_FOREIGNSECURITYPRINCIPALS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="46417-119">\_contenedor de datos de programa GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="46417-119">GUID\_PROGRAM\_DATA\_CONTAINER\_W</span></span>
-   <span data-ttu-id="46417-120">GUID de \_ Microsoft \_ Program \_ Data \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="46417-120">GUID\_MICROSOFT\_PROGRAM\_DATA\_CONTAINER\_W</span></span>
-   <span data-ttu-id="46417-121">\_contenedor de cuotas de NTDS GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="46417-121">GUID\_NTDS\_QUOTAS\_CONTAINER\_W</span></span>



| <span data-ttu-id="46417-122">Entrada</span><span class="sxs-lookup"><span data-stu-id="46417-122">Entry</span></span> | <span data-ttu-id="46417-123">Value</span><span class="sxs-lookup"><span data-stu-id="46417-123">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="46417-124">CN</span><span class="sxs-lookup"><span data-stu-id="46417-124">CN</span></span>                | <span data-ttu-id="46417-125">Well-Known-Objects</span><span class="sxs-lookup"><span data-stu-id="46417-125">Well-Known-Objects</span></span>                              |
| <span data-ttu-id="46417-126">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="46417-126">Ldap-Display-Name</span></span> | <span data-ttu-id="46417-127">wellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="46417-127">wellKnownObjects</span></span>                                |
| <span data-ttu-id="46417-128">Tamaño</span><span class="sxs-lookup"><span data-stu-id="46417-128">Size</span></span>              | \-                                              |
| <span data-ttu-id="46417-129">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="46417-129">Update Privilege</span></span>  | <span data-ttu-id="46417-130">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="46417-130">This value is set by the system.</span></span>                |
| <span data-ttu-id="46417-131">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="46417-131">Update Frequency</span></span>  | <span data-ttu-id="46417-132">Siempre que se mueva uno de los contenedores del sistema.</span><span class="sxs-lookup"><span data-stu-id="46417-132">Whenever one of the system containers is moved.</span></span> |
| <span data-ttu-id="46417-133">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="46417-133">Attribute-Id</span></span>      | <span data-ttu-id="46417-134">1.2.840.113556.1.4.618</span><span class="sxs-lookup"><span data-stu-id="46417-134">1.2.840.113556.1.4.618</span></span>                          |
| <span data-ttu-id="46417-135">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="46417-135">System-Id-Guid</span></span>    | <span data-ttu-id="46417-136">05308983-7688-11d1-aded-00c04fd8d5cd</span><span class="sxs-lookup"><span data-stu-id="46417-136">05308983-7688-11d1-aded-00c04fd8d5cd</span></span>            |
| <span data-ttu-id="46417-137">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46417-137">Syntax</span></span>            | [<span data-ttu-id="46417-138">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="46417-138">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md) |



## <a name="implementations"></a><span data-ttu-id="46417-139">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="46417-139">Implementations</span></span>

-   [<span data-ttu-id="46417-140">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="46417-140">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="46417-141">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="46417-141">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="46417-142">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="46417-142">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="46417-143">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="46417-143">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="46417-144">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="46417-144">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="46417-145">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="46417-145">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="46417-146">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="46417-146">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="46417-147">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="46417-147">Windows 2000 Server</span></span>



| <span data-ttu-id="46417-148">Entrada</span><span class="sxs-lookup"><span data-stu-id="46417-148">Entry</span></span> | <span data-ttu-id="46417-149">Value</span><span class="sxs-lookup"><span data-stu-id="46417-149">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="46417-150">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="46417-150">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="46417-151">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46417-151">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="46417-152">System-Only</span><span class="sxs-lookup"><span data-stu-id="46417-152">System-Only</span></span>            | <span data-ttu-id="46417-153">True</span><span class="sxs-lookup"><span data-stu-id="46417-153">True</span></span>                            |
| <span data-ttu-id="46417-154">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="46417-154">Is-Single-Valued</span></span>       | <span data-ttu-id="46417-155">False</span><span class="sxs-lookup"><span data-stu-id="46417-155">False</span></span>                           |
| <span data-ttu-id="46417-156">Está indexado</span><span class="sxs-lookup"><span data-stu-id="46417-156">Is Indexed</span></span>             | <span data-ttu-id="46417-157">False</span><span class="sxs-lookup"><span data-stu-id="46417-157">False</span></span>                           |
| <span data-ttu-id="46417-158">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="46417-158">In Global Catalog</span></span>      | <span data-ttu-id="46417-159">True</span><span class="sxs-lookup"><span data-stu-id="46417-159">True</span></span>                            |
| <span data-ttu-id="46417-160">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="46417-160">NT-Security-Descriptor</span></span> | <span data-ttu-id="46417-161">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46417-161">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="46417-162">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46417-162">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="46417-163">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46417-163">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="46417-164">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46417-164">Search-Flags</span></span>           | <span data-ttu-id="46417-165">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46417-165">0x00000000</span></span>                      |
| <span data-ttu-id="46417-166">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46417-166">System-Flags</span></span>           | <span data-ttu-id="46417-167">0x00000012</span><span class="sxs-lookup"><span data-stu-id="46417-167">0x00000012</span></span>                      |
| <span data-ttu-id="46417-168">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="46417-168">Classes used in</span></span>        | [<span data-ttu-id="46417-169">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="46417-169">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="46417-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="46417-170">Windows Server 2003</span></span>



| <span data-ttu-id="46417-171">Entrada</span><span class="sxs-lookup"><span data-stu-id="46417-171">Entry</span></span> | <span data-ttu-id="46417-172">Value</span><span class="sxs-lookup"><span data-stu-id="46417-172">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="46417-173">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="46417-173">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="46417-174">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46417-174">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="46417-175">System-Only</span><span class="sxs-lookup"><span data-stu-id="46417-175">System-Only</span></span>            | <span data-ttu-id="46417-176">True</span><span class="sxs-lookup"><span data-stu-id="46417-176">True</span></span>                            |
| <span data-ttu-id="46417-177">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="46417-177">Is-Single-Valued</span></span>       | <span data-ttu-id="46417-178">False</span><span class="sxs-lookup"><span data-stu-id="46417-178">False</span></span>                           |
| <span data-ttu-id="46417-179">Está indexado</span><span class="sxs-lookup"><span data-stu-id="46417-179">Is Indexed</span></span>             | <span data-ttu-id="46417-180">False</span><span class="sxs-lookup"><span data-stu-id="46417-180">False</span></span>                           |
| <span data-ttu-id="46417-181">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="46417-181">In Global Catalog</span></span>      | <span data-ttu-id="46417-182">True</span><span class="sxs-lookup"><span data-stu-id="46417-182">True</span></span>                            |
| <span data-ttu-id="46417-183">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="46417-183">NT-Security-Descriptor</span></span> | <span data-ttu-id="46417-184">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46417-184">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="46417-185">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46417-185">Range-Lower</span></span>            | <span data-ttu-id="46417-186">16</span><span class="sxs-lookup"><span data-stu-id="46417-186">16</span></span>                              |
| <span data-ttu-id="46417-187">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46417-187">Range-Upper</span></span>            | <span data-ttu-id="46417-188">16</span><span class="sxs-lookup"><span data-stu-id="46417-188">16</span></span>                              |
| <span data-ttu-id="46417-189">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46417-189">Search-Flags</span></span>           | <span data-ttu-id="46417-190">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46417-190">0x00000000</span></span>                      |
| <span data-ttu-id="46417-191">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46417-191">System-Flags</span></span>           | <span data-ttu-id="46417-192">0x00000012</span><span class="sxs-lookup"><span data-stu-id="46417-192">0x00000012</span></span>                      |
| <span data-ttu-id="46417-193">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="46417-193">Classes used in</span></span>        | [<span data-ttu-id="46417-194">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="46417-194">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="46417-195">ADAM</span><span class="sxs-lookup"><span data-stu-id="46417-195">ADAM</span></span>



| <span data-ttu-id="46417-196">Entrada</span><span class="sxs-lookup"><span data-stu-id="46417-196">Entry</span></span> | <span data-ttu-id="46417-197">Value</span><span class="sxs-lookup"><span data-stu-id="46417-197">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="46417-198">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="46417-198">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="46417-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46417-199">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="46417-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="46417-200">System-Only</span></span>            | <span data-ttu-id="46417-201">True</span><span class="sxs-lookup"><span data-stu-id="46417-201">True</span></span>                            |
| <span data-ttu-id="46417-202">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="46417-202">Is-Single-Valued</span></span>       | <span data-ttu-id="46417-203">False</span><span class="sxs-lookup"><span data-stu-id="46417-203">False</span></span>                           |
| <span data-ttu-id="46417-204">Está indexado</span><span class="sxs-lookup"><span data-stu-id="46417-204">Is Indexed</span></span>             | <span data-ttu-id="46417-205">False</span><span class="sxs-lookup"><span data-stu-id="46417-205">False</span></span>                           |
| <span data-ttu-id="46417-206">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="46417-206">In Global Catalog</span></span>      | <span data-ttu-id="46417-207">True</span><span class="sxs-lookup"><span data-stu-id="46417-207">True</span></span>                            |
| <span data-ttu-id="46417-208">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="46417-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="46417-209">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46417-209">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="46417-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46417-210">Range-Lower</span></span>            | <span data-ttu-id="46417-211">16</span><span class="sxs-lookup"><span data-stu-id="46417-211">16</span></span>                              |
| <span data-ttu-id="46417-212">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46417-212">Range-Upper</span></span>            | <span data-ttu-id="46417-213">16</span><span class="sxs-lookup"><span data-stu-id="46417-213">16</span></span>                              |
| <span data-ttu-id="46417-214">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46417-214">Search-Flags</span></span>           | <span data-ttu-id="46417-215">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46417-215">0x00000000</span></span>                      |
| <span data-ttu-id="46417-216">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46417-216">System-Flags</span></span>           | <span data-ttu-id="46417-217">0x00000012</span><span class="sxs-lookup"><span data-stu-id="46417-217">0x00000012</span></span>                      |
| <span data-ttu-id="46417-218">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="46417-218">Classes used in</span></span>        | [<span data-ttu-id="46417-219">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="46417-219">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="46417-220">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="46417-220">Windows Server 2003 R2</span></span>



| <span data-ttu-id="46417-221">Entrada</span><span class="sxs-lookup"><span data-stu-id="46417-221">Entry</span></span> | <span data-ttu-id="46417-222">Value</span><span class="sxs-lookup"><span data-stu-id="46417-222">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="46417-223">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="46417-223">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="46417-224">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46417-224">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="46417-225">System-Only</span><span class="sxs-lookup"><span data-stu-id="46417-225">System-Only</span></span>            | <span data-ttu-id="46417-226">True</span><span class="sxs-lookup"><span data-stu-id="46417-226">True</span></span>                            |
| <span data-ttu-id="46417-227">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="46417-227">Is-Single-Valued</span></span>       | <span data-ttu-id="46417-228">False</span><span class="sxs-lookup"><span data-stu-id="46417-228">False</span></span>                           |
| <span data-ttu-id="46417-229">Está indexado</span><span class="sxs-lookup"><span data-stu-id="46417-229">Is Indexed</span></span>             | <span data-ttu-id="46417-230">False</span><span class="sxs-lookup"><span data-stu-id="46417-230">False</span></span>                           |
| <span data-ttu-id="46417-231">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="46417-231">In Global Catalog</span></span>      | <span data-ttu-id="46417-232">True</span><span class="sxs-lookup"><span data-stu-id="46417-232">True</span></span>                            |
| <span data-ttu-id="46417-233">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="46417-233">NT-Security-Descriptor</span></span> | <span data-ttu-id="46417-234">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46417-234">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="46417-235">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46417-235">Range-Lower</span></span>            | <span data-ttu-id="46417-236">16</span><span class="sxs-lookup"><span data-stu-id="46417-236">16</span></span>                              |
| <span data-ttu-id="46417-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46417-237">Range-Upper</span></span>            | <span data-ttu-id="46417-238">16</span><span class="sxs-lookup"><span data-stu-id="46417-238">16</span></span>                              |
| <span data-ttu-id="46417-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46417-239">Search-Flags</span></span>           | <span data-ttu-id="46417-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46417-240">0x00000000</span></span>                      |
| <span data-ttu-id="46417-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46417-241">System-Flags</span></span>           | <span data-ttu-id="46417-242">0x00000012</span><span class="sxs-lookup"><span data-stu-id="46417-242">0x00000012</span></span>                      |
| <span data-ttu-id="46417-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="46417-243">Classes used in</span></span>        | [<span data-ttu-id="46417-244">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="46417-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="46417-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46417-245">Windows Server 2008</span></span>



| <span data-ttu-id="46417-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="46417-246">Entry</span></span> | <span data-ttu-id="46417-247">Value</span><span class="sxs-lookup"><span data-stu-id="46417-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="46417-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="46417-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="46417-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46417-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="46417-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="46417-250">System-Only</span></span>            | <span data-ttu-id="46417-251">True</span><span class="sxs-lookup"><span data-stu-id="46417-251">True</span></span>                            |
| <span data-ttu-id="46417-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="46417-252">Is-Single-Valued</span></span>       | <span data-ttu-id="46417-253">False</span><span class="sxs-lookup"><span data-stu-id="46417-253">False</span></span>                           |
| <span data-ttu-id="46417-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="46417-254">Is Indexed</span></span>             | <span data-ttu-id="46417-255">False</span><span class="sxs-lookup"><span data-stu-id="46417-255">False</span></span>                           |
| <span data-ttu-id="46417-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="46417-256">In Global Catalog</span></span>      | <span data-ttu-id="46417-257">True</span><span class="sxs-lookup"><span data-stu-id="46417-257">True</span></span>                            |
| <span data-ttu-id="46417-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="46417-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="46417-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46417-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="46417-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46417-260">Range-Lower</span></span>            | <span data-ttu-id="46417-261">16</span><span class="sxs-lookup"><span data-stu-id="46417-261">16</span></span>                              |
| <span data-ttu-id="46417-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46417-262">Range-Upper</span></span>            | <span data-ttu-id="46417-263">16</span><span class="sxs-lookup"><span data-stu-id="46417-263">16</span></span>                              |
| <span data-ttu-id="46417-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46417-264">Search-Flags</span></span>           | <span data-ttu-id="46417-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46417-265">0x00000000</span></span>                      |
| <span data-ttu-id="46417-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46417-266">System-Flags</span></span>           | <span data-ttu-id="46417-267">0x00000012</span><span class="sxs-lookup"><span data-stu-id="46417-267">0x00000012</span></span>                      |
| <span data-ttu-id="46417-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="46417-268">Classes used in</span></span>        | [<span data-ttu-id="46417-269">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="46417-269">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="46417-270">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="46417-270">Windows Server 2008 R2</span></span>



| <span data-ttu-id="46417-271">Entrada</span><span class="sxs-lookup"><span data-stu-id="46417-271">Entry</span></span> | <span data-ttu-id="46417-272">Value</span><span class="sxs-lookup"><span data-stu-id="46417-272">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="46417-273">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="46417-273">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="46417-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46417-274">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="46417-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="46417-275">System-Only</span></span>            | <span data-ttu-id="46417-276">True</span><span class="sxs-lookup"><span data-stu-id="46417-276">True</span></span>                            |
| <span data-ttu-id="46417-277">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="46417-277">Is-Single-Valued</span></span>       | <span data-ttu-id="46417-278">False</span><span class="sxs-lookup"><span data-stu-id="46417-278">False</span></span>                           |
| <span data-ttu-id="46417-279">Está indexado</span><span class="sxs-lookup"><span data-stu-id="46417-279">Is Indexed</span></span>             | <span data-ttu-id="46417-280">False</span><span class="sxs-lookup"><span data-stu-id="46417-280">False</span></span>                           |
| <span data-ttu-id="46417-281">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="46417-281">In Global Catalog</span></span>      | <span data-ttu-id="46417-282">True</span><span class="sxs-lookup"><span data-stu-id="46417-282">True</span></span>                            |
| <span data-ttu-id="46417-283">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="46417-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="46417-284">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46417-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="46417-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46417-285">Range-Lower</span></span>            | <span data-ttu-id="46417-286">16</span><span class="sxs-lookup"><span data-stu-id="46417-286">16</span></span>                              |
| <span data-ttu-id="46417-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46417-287">Range-Upper</span></span>            | <span data-ttu-id="46417-288">16</span><span class="sxs-lookup"><span data-stu-id="46417-288">16</span></span>                              |
| <span data-ttu-id="46417-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46417-289">Search-Flags</span></span>           | <span data-ttu-id="46417-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46417-290">0x00000000</span></span>                      |
| <span data-ttu-id="46417-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46417-291">System-Flags</span></span>           | <span data-ttu-id="46417-292">0x00000012</span><span class="sxs-lookup"><span data-stu-id="46417-292">0x00000012</span></span>                      |
| <span data-ttu-id="46417-293">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="46417-293">Classes used in</span></span>        | [<span data-ttu-id="46417-294">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="46417-294">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="46417-295">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="46417-295">Windows Server 2012</span></span>



| <span data-ttu-id="46417-296">Entrada</span><span class="sxs-lookup"><span data-stu-id="46417-296">Entry</span></span> | <span data-ttu-id="46417-297">Value</span><span class="sxs-lookup"><span data-stu-id="46417-297">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="46417-298">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="46417-298">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="46417-299">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46417-299">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="46417-300">System-Only</span><span class="sxs-lookup"><span data-stu-id="46417-300">System-Only</span></span>            | <span data-ttu-id="46417-301">True</span><span class="sxs-lookup"><span data-stu-id="46417-301">True</span></span>                            |
| <span data-ttu-id="46417-302">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="46417-302">Is-Single-Valued</span></span>       | <span data-ttu-id="46417-303">False</span><span class="sxs-lookup"><span data-stu-id="46417-303">False</span></span>                           |
| <span data-ttu-id="46417-304">Está indexado</span><span class="sxs-lookup"><span data-stu-id="46417-304">Is Indexed</span></span>             | <span data-ttu-id="46417-305">False</span><span class="sxs-lookup"><span data-stu-id="46417-305">False</span></span>                           |
| <span data-ttu-id="46417-306">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="46417-306">In Global Catalog</span></span>      | <span data-ttu-id="46417-307">True</span><span class="sxs-lookup"><span data-stu-id="46417-307">True</span></span>                            |
| <span data-ttu-id="46417-308">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="46417-308">NT-Security-Descriptor</span></span> | <span data-ttu-id="46417-309">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="46417-309">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="46417-310">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46417-310">Range-Lower</span></span>            | <span data-ttu-id="46417-311">16</span><span class="sxs-lookup"><span data-stu-id="46417-311">16</span></span>                              |
| <span data-ttu-id="46417-312">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46417-312">Range-Upper</span></span>            | <span data-ttu-id="46417-313">16</span><span class="sxs-lookup"><span data-stu-id="46417-313">16</span></span>                              |
| <span data-ttu-id="46417-314">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46417-314">Search-Flags</span></span>           | <span data-ttu-id="46417-315">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46417-315">0x00000000</span></span>                      |
| <span data-ttu-id="46417-316">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46417-316">System-Flags</span></span>           | <span data-ttu-id="46417-317">0x00000012</span><span class="sxs-lookup"><span data-stu-id="46417-317">0x00000012</span></span>                      |
| <span data-ttu-id="46417-318">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="46417-318">Classes used in</span></span>        | [<span data-ttu-id="46417-319">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="46417-319">**Top**</span></span>](c-top.md)<br/> |



 

 





