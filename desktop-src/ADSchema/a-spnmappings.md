---
title: SPN-Mappings atributo)
description: Este atributo de varios valores contiene una lista de nombres de entidad de seguridad de servicio (SPN) para mostrar la equivalencia de los tipos de SPN.
ms.assetid: 6d37618d-426d-4e7b-8475-c912adb595ee
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de SPN-Mappings
- sPNMappings esquema de AD de atributos
topic_type:
- apiref
api_name:
- SPN-Mappings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ccb07e068a22d0a85928832890f0b66ebda016
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536136"
---
# <a name="spn-mappings-attribute"></a><span data-ttu-id="3b540-105">SPN-Mappings atributo)</span><span class="sxs-lookup"><span data-stu-id="3b540-105">SPN-Mappings attribute</span></span>

<span data-ttu-id="3b540-106">Este atributo de varios valores contiene una lista de nombres de entidad de seguridad de servicio (SPN) para mostrar la equivalencia de los tipos de SPN.</span><span class="sxs-lookup"><span data-stu-id="3b540-106">This multiple-valued attribute contains a list of service principal names (SPN) to show the equivalence of SPN types.</span></span> <span data-ttu-id="3b540-107">El SPN es el nombre que usa un cliente para identificar de forma única una instancia de un servicio.</span><span class="sxs-lookup"><span data-stu-id="3b540-107">The SPN is the name a client uses to uniquely identify an instance of a service.</span></span> <span data-ttu-id="3b540-108">Si instala varias instancias de un servicio en equipos a lo largo de un bosque, cada instancia debe tener su propio SPN.</span><span class="sxs-lookup"><span data-stu-id="3b540-108">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="3b540-109">Una instancia de servicio determinada puede tener varios SPN si hay varios nombres que los clientes pueden usar para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="3b540-109">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span> <span data-ttu-id="3b540-110">Por ejemplo, "LDAP/..." Los SPN se pueden asignar de forma que sean equivalentes a "host/..." Carece.</span><span class="sxs-lookup"><span data-stu-id="3b540-110">For example, "ldap/..." SPNs could be mapped so that they are equivalent to "host/..." SPNs.</span></span>



| <span data-ttu-id="3b540-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="3b540-111">Entry</span></span> | <span data-ttu-id="3b540-112">Value</span><span class="sxs-lookup"><span data-stu-id="3b540-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b540-113">CN</span><span class="sxs-lookup"><span data-stu-id="3b540-113">CN</span></span>                | <span data-ttu-id="3b540-114">SPN-Mappings</span><span class="sxs-lookup"><span data-stu-id="3b540-114">SPN-Mappings</span></span>                                                                                                       |
| <span data-ttu-id="3b540-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="3b540-115">Ldap-Display-Name</span></span> | <span data-ttu-id="3b540-116">sPNMappings</span><span class="sxs-lookup"><span data-stu-id="3b540-116">sPNMappings</span></span>                                                                                                        |
| <span data-ttu-id="3b540-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="3b540-117">Size</span></span>              | \-                                                                                                                 |
| <span data-ttu-id="3b540-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="3b540-118">Update Privilege</span></span>  | <span data-ttu-id="3b540-119">Este valor se establece durante la instalación del producto.</span><span class="sxs-lookup"><span data-stu-id="3b540-119">This value is set during the product installation.</span></span> <span data-ttu-id="3b540-120">Puede ser modificado por el administrador del sistema en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="3b540-120">It can be modified by the system administrator at a later time.</span></span> |
| <span data-ttu-id="3b540-121">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="3b540-121">Update Frequency</span></span>  | \-                                                                                                                 |
| <span data-ttu-id="3b540-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3b540-122">Attribute-Id</span></span>      | <span data-ttu-id="3b540-123">1.2.840.113556.1.4.1347</span><span class="sxs-lookup"><span data-stu-id="3b540-123">1.2.840.113556.1.4.1347</span></span>                                                                                            |
| <span data-ttu-id="3b540-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3b540-124">System-Id-Guid</span></span>    | <span data-ttu-id="3b540-125">2ab0e76c-7041-11d2-9905-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="3b540-125">2ab0e76c-7041-11d2-9905-0000f87a57d4</span></span>                                                                               |
| <span data-ttu-id="3b540-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b540-126">Syntax</span></span>            | [<span data-ttu-id="3b540-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3b540-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                        |



## <a name="implementations"></a><span data-ttu-id="3b540-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="3b540-128">Implementations</span></span>

-   [<span data-ttu-id="3b540-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3b540-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3b540-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3b540-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3b540-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3b540-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3b540-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3b540-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3b540-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3b540-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3b540-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3b540-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3b540-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3b540-135">Windows 2000 Server</span></span>



| <span data-ttu-id="3b540-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="3b540-136">Entry</span></span> | <span data-ttu-id="3b540-137">Value</span><span class="sxs-lookup"><span data-stu-id="3b540-137">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3b540-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="3b540-138">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b540-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b540-139">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b540-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b540-140">System-Only</span></span>            | <span data-ttu-id="3b540-141">False</span><span class="sxs-lookup"><span data-stu-id="3b540-141">False</span></span>                                            |
| <span data-ttu-id="3b540-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="3b540-142">Is-Single-Valued</span></span>       | <span data-ttu-id="3b540-143">False</span><span class="sxs-lookup"><span data-stu-id="3b540-143">False</span></span>                                            |
| <span data-ttu-id="3b540-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="3b540-144">Is Indexed</span></span>             | <span data-ttu-id="3b540-145">False</span><span class="sxs-lookup"><span data-stu-id="3b540-145">False</span></span>                                            |
| <span data-ttu-id="3b540-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3b540-146">In Global Catalog</span></span>      | <span data-ttu-id="3b540-147">False</span><span class="sxs-lookup"><span data-stu-id="3b540-147">False</span></span>                                            |
| <span data-ttu-id="3b540-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="3b540-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b540-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3b540-149">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3b540-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b540-150">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3b540-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b540-151">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3b540-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b540-152">Search-Flags</span></span>           | <span data-ttu-id="3b540-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b540-153">0x00000000</span></span>                                       |
| <span data-ttu-id="3b540-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b540-154">System-Flags</span></span>           | <span data-ttu-id="3b540-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b540-155">0x00000010</span></span>                                       |
| <span data-ttu-id="3b540-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="3b540-156">Classes used in</span></span>        | [<span data-ttu-id="3b540-157">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="3b540-157">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3b540-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3b540-158">Windows Server 2003</span></span>



| <span data-ttu-id="3b540-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="3b540-159">Entry</span></span> | <span data-ttu-id="3b540-160">Value</span><span class="sxs-lookup"><span data-stu-id="3b540-160">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3b540-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="3b540-161">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b540-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b540-162">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b540-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b540-163">System-Only</span></span>            | <span data-ttu-id="3b540-164">False</span><span class="sxs-lookup"><span data-stu-id="3b540-164">False</span></span>                                            |
| <span data-ttu-id="3b540-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="3b540-165">Is-Single-Valued</span></span>       | <span data-ttu-id="3b540-166">False</span><span class="sxs-lookup"><span data-stu-id="3b540-166">False</span></span>                                            |
| <span data-ttu-id="3b540-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="3b540-167">Is Indexed</span></span>             | <span data-ttu-id="3b540-168">False</span><span class="sxs-lookup"><span data-stu-id="3b540-168">False</span></span>                                            |
| <span data-ttu-id="3b540-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3b540-169">In Global Catalog</span></span>      | <span data-ttu-id="3b540-170">False</span><span class="sxs-lookup"><span data-stu-id="3b540-170">False</span></span>                                            |
| <span data-ttu-id="3b540-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="3b540-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b540-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3b540-172">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3b540-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b540-173">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3b540-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b540-174">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3b540-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b540-175">Search-Flags</span></span>           | <span data-ttu-id="3b540-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b540-176">0x00000000</span></span>                                       |
| <span data-ttu-id="3b540-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b540-177">System-Flags</span></span>           | <span data-ttu-id="3b540-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b540-178">0x00000010</span></span>                                       |
| <span data-ttu-id="3b540-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="3b540-179">Classes used in</span></span>        | [<span data-ttu-id="3b540-180">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="3b540-180">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3b540-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3b540-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3b540-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="3b540-182">Entry</span></span> | <span data-ttu-id="3b540-183">Value</span><span class="sxs-lookup"><span data-stu-id="3b540-183">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3b540-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="3b540-184">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b540-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b540-185">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b540-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b540-186">System-Only</span></span>            | <span data-ttu-id="3b540-187">False</span><span class="sxs-lookup"><span data-stu-id="3b540-187">False</span></span>                                            |
| <span data-ttu-id="3b540-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="3b540-188">Is-Single-Valued</span></span>       | <span data-ttu-id="3b540-189">False</span><span class="sxs-lookup"><span data-stu-id="3b540-189">False</span></span>                                            |
| <span data-ttu-id="3b540-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="3b540-190">Is Indexed</span></span>             | <span data-ttu-id="3b540-191">False</span><span class="sxs-lookup"><span data-stu-id="3b540-191">False</span></span>                                            |
| <span data-ttu-id="3b540-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3b540-192">In Global Catalog</span></span>      | <span data-ttu-id="3b540-193">False</span><span class="sxs-lookup"><span data-stu-id="3b540-193">False</span></span>                                            |
| <span data-ttu-id="3b540-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="3b540-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b540-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3b540-195">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3b540-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b540-196">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3b540-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b540-197">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3b540-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b540-198">Search-Flags</span></span>           | <span data-ttu-id="3b540-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b540-199">0x00000000</span></span>                                       |
| <span data-ttu-id="3b540-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b540-200">System-Flags</span></span>           | <span data-ttu-id="3b540-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b540-201">0x00000010</span></span>                                       |
| <span data-ttu-id="3b540-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="3b540-202">Classes used in</span></span>        | [<span data-ttu-id="3b540-203">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="3b540-203">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3b540-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b540-204">Windows Server 2008</span></span>



| <span data-ttu-id="3b540-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="3b540-205">Entry</span></span> | <span data-ttu-id="3b540-206">Value</span><span class="sxs-lookup"><span data-stu-id="3b540-206">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3b540-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="3b540-207">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b540-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b540-208">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b540-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b540-209">System-Only</span></span>            | <span data-ttu-id="3b540-210">False</span><span class="sxs-lookup"><span data-stu-id="3b540-210">False</span></span>                                            |
| <span data-ttu-id="3b540-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="3b540-211">Is-Single-Valued</span></span>       | <span data-ttu-id="3b540-212">False</span><span class="sxs-lookup"><span data-stu-id="3b540-212">False</span></span>                                            |
| <span data-ttu-id="3b540-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="3b540-213">Is Indexed</span></span>             | <span data-ttu-id="3b540-214">False</span><span class="sxs-lookup"><span data-stu-id="3b540-214">False</span></span>                                            |
| <span data-ttu-id="3b540-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3b540-215">In Global Catalog</span></span>      | <span data-ttu-id="3b540-216">False</span><span class="sxs-lookup"><span data-stu-id="3b540-216">False</span></span>                                            |
| <span data-ttu-id="3b540-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="3b540-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b540-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3b540-218">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3b540-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b540-219">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3b540-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b540-220">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3b540-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b540-221">Search-Flags</span></span>           | <span data-ttu-id="3b540-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b540-222">0x00000000</span></span>                                       |
| <span data-ttu-id="3b540-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b540-223">System-Flags</span></span>           | <span data-ttu-id="3b540-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b540-224">0x00000010</span></span>                                       |
| <span data-ttu-id="3b540-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="3b540-225">Classes used in</span></span>        | [<span data-ttu-id="3b540-226">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="3b540-226">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3b540-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3b540-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3b540-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="3b540-228">Entry</span></span> | <span data-ttu-id="3b540-229">Value</span><span class="sxs-lookup"><span data-stu-id="3b540-229">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3b540-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="3b540-230">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b540-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b540-231">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b540-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b540-232">System-Only</span></span>            | <span data-ttu-id="3b540-233">False</span><span class="sxs-lookup"><span data-stu-id="3b540-233">False</span></span>                                            |
| <span data-ttu-id="3b540-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="3b540-234">Is-Single-Valued</span></span>       | <span data-ttu-id="3b540-235">False</span><span class="sxs-lookup"><span data-stu-id="3b540-235">False</span></span>                                            |
| <span data-ttu-id="3b540-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="3b540-236">Is Indexed</span></span>             | <span data-ttu-id="3b540-237">False</span><span class="sxs-lookup"><span data-stu-id="3b540-237">False</span></span>                                            |
| <span data-ttu-id="3b540-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3b540-238">In Global Catalog</span></span>      | <span data-ttu-id="3b540-239">False</span><span class="sxs-lookup"><span data-stu-id="3b540-239">False</span></span>                                            |
| <span data-ttu-id="3b540-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="3b540-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b540-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3b540-241">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3b540-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b540-242">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3b540-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b540-243">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3b540-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b540-244">Search-Flags</span></span>           | <span data-ttu-id="3b540-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b540-245">0x00000000</span></span>                                       |
| <span data-ttu-id="3b540-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b540-246">System-Flags</span></span>           | <span data-ttu-id="3b540-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b540-247">0x00000010</span></span>                                       |
| <span data-ttu-id="3b540-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="3b540-248">Classes used in</span></span>        | [<span data-ttu-id="3b540-249">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="3b540-249">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3b540-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3b540-250">Windows Server 2012</span></span>



| <span data-ttu-id="3b540-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="3b540-251">Entry</span></span> | <span data-ttu-id="3b540-252">Value</span><span class="sxs-lookup"><span data-stu-id="3b540-252">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3b540-253">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="3b540-253">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b540-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b540-254">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b540-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b540-255">System-Only</span></span>            | <span data-ttu-id="3b540-256">False</span><span class="sxs-lookup"><span data-stu-id="3b540-256">False</span></span>                                            |
| <span data-ttu-id="3b540-257">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="3b540-257">Is-Single-Valued</span></span>       | <span data-ttu-id="3b540-258">False</span><span class="sxs-lookup"><span data-stu-id="3b540-258">False</span></span>                                            |
| <span data-ttu-id="3b540-259">Está indexado</span><span class="sxs-lookup"><span data-stu-id="3b540-259">Is Indexed</span></span>             | <span data-ttu-id="3b540-260">False</span><span class="sxs-lookup"><span data-stu-id="3b540-260">False</span></span>                                            |
| <span data-ttu-id="3b540-261">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3b540-261">In Global Catalog</span></span>      | <span data-ttu-id="3b540-262">False</span><span class="sxs-lookup"><span data-stu-id="3b540-262">False</span></span>                                            |
| <span data-ttu-id="3b540-263">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="3b540-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b540-264">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3b540-264">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3b540-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b540-265">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3b540-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b540-266">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3b540-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b540-267">Search-Flags</span></span>           | <span data-ttu-id="3b540-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b540-268">0x00000000</span></span>                                       |
| <span data-ttu-id="3b540-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b540-269">System-Flags</span></span>           | <span data-ttu-id="3b540-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b540-270">0x00000010</span></span>                                       |
| <span data-ttu-id="3b540-271">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="3b540-271">Classes used in</span></span>        | [<span data-ttu-id="3b540-272">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="3b540-272">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





