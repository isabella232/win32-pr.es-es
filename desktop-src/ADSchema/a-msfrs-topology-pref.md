---
title: atributo MS-FRS-Topology-Pref
description: El atributo MS-FRS-Topology-Pref se usa para registrar la configuración de topología de NTFRS preferida.
ms.assetid: 2804ad8a-bec8-491b-84ea-bdff1c8635d0
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MS-FRS-Topology-Pref
- msFRS-Topology-atributo Pref AD Schema
topic_type:
- apiref
api_name:
- ms-FRS-Topology-Pref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de417b03385e51d6a97fd68097f81bcc0cb6b9db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804651"
---
# <a name="ms-frs-topology-pref-attribute"></a><span data-ttu-id="d0545-105">atributo MS-FRS-Topology-Pref</span><span class="sxs-lookup"><span data-stu-id="d0545-105">ms-FRS-Topology-Pref attribute</span></span>

<span data-ttu-id="d0545-106">El atributo **MS-FRS-Topology-Pref** se usa para registrar la configuración de topología de NTFRS preferida.</span><span class="sxs-lookup"><span data-stu-id="d0545-106">The **ms-FRS-Topology-Pref** attribute is used to record the preferred NTFRS topology settings.</span></span> <span data-ttu-id="d0545-107">Cuando se agrega o se elimina un miembro de FRS en el conjunto de réplicas, se hace referencia a estos atributos y se realizan ajustes en las conexiones entre el resto de los miembros FRS del conjunto de réplicas.</span><span class="sxs-lookup"><span data-stu-id="d0545-107">When an FRS member gets added or deleted to the replica set, these attributes are referred, and adjustments made to the connections between the rest of the FRS members in the replica set.</span></span>

<span data-ttu-id="d0545-108">Los valores válidos para este atributo son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="d0545-108">Valid values for this attribute are as follows.</span></span>

| <span data-ttu-id="d0545-109">Value</span><span class="sxs-lookup"><span data-stu-id="d0545-109">Value</span></span> | <span data-ttu-id="d0545-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0545-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="d0545-111">1</span><span class="sxs-lookup"><span data-stu-id="d0545-111">1</span></span>     | <span data-ttu-id="d0545-112">\_anillo RSTOPOLOGYPREF de FRS \_</span><span class="sxs-lookup"><span data-stu-id="d0545-112">FRS\_RSTOPOLOGYPREF\_RING</span></span><br/>     |
| <span data-ttu-id="d0545-113">2</span><span class="sxs-lookup"><span data-stu-id="d0545-113">2</span></span>     | <span data-ttu-id="d0545-114">FRS \_ RSTOPOLOGYPREF \_ HUBSPOKE</span><span class="sxs-lookup"><span data-stu-id="d0545-114">FRS\_RSTOPOLOGYPREF\_HUBSPOKE</span></span><br/> |
| <span data-ttu-id="d0545-115">3</span><span class="sxs-lookup"><span data-stu-id="d0545-115">3</span></span>     | <span data-ttu-id="d0545-116">FRS \_ RSTOPOLOGYPREF \_ FULLMESH</span><span class="sxs-lookup"><span data-stu-id="d0545-116">FRS\_RSTOPOLOGYPREF\_FULLMESH</span></span><br/> |
| <span data-ttu-id="d0545-117">4</span><span class="sxs-lookup"><span data-stu-id="d0545-117">4</span></span>     | <span data-ttu-id="d0545-118">FRS \_ RSTOPOLOGYPREF \_ personalizado</span><span class="sxs-lookup"><span data-stu-id="d0545-118">FRS\_RSTOPOLOGYPREF\_CUSTOM</span></span><br/>   |



 



| <span data-ttu-id="d0545-119">Entrada</span><span class="sxs-lookup"><span data-stu-id="d0545-119">Entry</span></span> | <span data-ttu-id="d0545-120">Value</span><span class="sxs-lookup"><span data-stu-id="d0545-120">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d0545-121">CN</span><span class="sxs-lookup"><span data-stu-id="d0545-121">CN</span></span>                | <span data-ttu-id="d0545-122">MS-FRS-Topology-Pref</span><span class="sxs-lookup"><span data-stu-id="d0545-122">ms-FRS-Topology-Pref</span></span>                                               |
| <span data-ttu-id="d0545-123">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="d0545-123">Ldap-Display-Name</span></span> | <span data-ttu-id="d0545-124">msFRS-Topology-Pref</span><span class="sxs-lookup"><span data-stu-id="d0545-124">msFRS-Topology-Pref</span></span>                                                |
| <span data-ttu-id="d0545-125">Tamaño</span><span class="sxs-lookup"><span data-stu-id="d0545-125">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="d0545-126">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="d0545-126">Update Privilege</span></span>  | <span data-ttu-id="d0545-127">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="d0545-127">Domain administrator</span></span>                                               |
| <span data-ttu-id="d0545-128">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="d0545-128">Update Frequency</span></span>  | <span data-ttu-id="d0545-129">Cuando se crea el conjunto de réplicas o se cambia la topología preferida.</span><span class="sxs-lookup"><span data-stu-id="d0545-129">When the replica set is created or the preferred topology changes.</span></span> |
| <span data-ttu-id="d0545-130">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d0545-130">Attribute-Id</span></span>      | <span data-ttu-id="d0545-131">1.2.840.113556.1.4.1692</span><span class="sxs-lookup"><span data-stu-id="d0545-131">1.2.840.113556.1.4.1692</span></span>                                            |
| <span data-ttu-id="d0545-132">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d0545-132">System-Id-Guid</span></span>    | <span data-ttu-id="d0545-133">92aa27e0-5c50-402d-9ec1-ee847def9788</span><span class="sxs-lookup"><span data-stu-id="d0545-133">92aa27e0-5c50-402d-9ec1-ee847def9788</span></span>                               |
| <span data-ttu-id="d0545-134">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0545-134">Syntax</span></span>            | [<span data-ttu-id="d0545-135">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d0545-135">**String(Unicode)**</span></span>](s-string-unicode.md)                        |



## <a name="implementations"></a><span data-ttu-id="d0545-136">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="d0545-136">Implementations</span></span>

-   [<span data-ttu-id="d0545-137">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d0545-137">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d0545-138">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d0545-138">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d0545-139">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d0545-139">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d0545-140">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d0545-140">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d0545-141">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d0545-141">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d0545-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d0545-142">Windows Server 2003</span></span>



| <span data-ttu-id="d0545-143">Entrada</span><span class="sxs-lookup"><span data-stu-id="d0545-143">Entry</span></span> | <span data-ttu-id="d0545-144">Value</span><span class="sxs-lookup"><span data-stu-id="d0545-144">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d0545-145">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d0545-145">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0545-146">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0545-146">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0545-147">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0545-147">System-Only</span></span>            | <span data-ttu-id="d0545-148">False</span><span class="sxs-lookup"><span data-stu-id="d0545-148">False</span></span>                                                     |
| <span data-ttu-id="d0545-149">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d0545-149">Is-Single-Valued</span></span>       | <span data-ttu-id="d0545-150">True</span><span class="sxs-lookup"><span data-stu-id="d0545-150">True</span></span>                                                      |
| <span data-ttu-id="d0545-151">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d0545-151">Is Indexed</span></span>             | <span data-ttu-id="d0545-152">False</span><span class="sxs-lookup"><span data-stu-id="d0545-152">False</span></span>                                                     |
| <span data-ttu-id="d0545-153">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d0545-153">In Global Catalog</span></span>      | <span data-ttu-id="d0545-154">False</span><span class="sxs-lookup"><span data-stu-id="d0545-154">False</span></span>                                                     |
| <span data-ttu-id="d0545-155">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d0545-155">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0545-156">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0545-156">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d0545-157">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0545-157">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d0545-158">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0545-158">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d0545-159">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0545-159">Search-Flags</span></span>           | <span data-ttu-id="d0545-160">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0545-160">0x00000000</span></span>                                                |
| <span data-ttu-id="d0545-161">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0545-161">System-Flags</span></span>           | <span data-ttu-id="d0545-162">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0545-162">0x00000000</span></span>                                                |
| <span data-ttu-id="d0545-163">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d0545-163">Classes used in</span></span>        | [<span data-ttu-id="d0545-164">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="d0545-164">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d0545-165">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d0545-165">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d0545-166">Entrada</span><span class="sxs-lookup"><span data-stu-id="d0545-166">Entry</span></span> | <span data-ttu-id="d0545-167">Value</span><span class="sxs-lookup"><span data-stu-id="d0545-167">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d0545-168">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d0545-168">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0545-169">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0545-169">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0545-170">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0545-170">System-Only</span></span>            | <span data-ttu-id="d0545-171">False</span><span class="sxs-lookup"><span data-stu-id="d0545-171">False</span></span>                                                     |
| <span data-ttu-id="d0545-172">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d0545-172">Is-Single-Valued</span></span>       | <span data-ttu-id="d0545-173">True</span><span class="sxs-lookup"><span data-stu-id="d0545-173">True</span></span>                                                      |
| <span data-ttu-id="d0545-174">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d0545-174">Is Indexed</span></span>             | <span data-ttu-id="d0545-175">False</span><span class="sxs-lookup"><span data-stu-id="d0545-175">False</span></span>                                                     |
| <span data-ttu-id="d0545-176">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d0545-176">In Global Catalog</span></span>      | <span data-ttu-id="d0545-177">False</span><span class="sxs-lookup"><span data-stu-id="d0545-177">False</span></span>                                                     |
| <span data-ttu-id="d0545-178">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d0545-178">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0545-179">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0545-179">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d0545-180">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0545-180">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d0545-181">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0545-181">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d0545-182">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0545-182">Search-Flags</span></span>           | <span data-ttu-id="d0545-183">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0545-183">0x00000000</span></span>                                                |
| <span data-ttu-id="d0545-184">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0545-184">System-Flags</span></span>           | <span data-ttu-id="d0545-185">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0545-185">0x00000000</span></span>                                                |
| <span data-ttu-id="d0545-186">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d0545-186">Classes used in</span></span>        | [<span data-ttu-id="d0545-187">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="d0545-187">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d0545-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0545-188">Windows Server 2008</span></span>



| <span data-ttu-id="d0545-189">Entrada</span><span class="sxs-lookup"><span data-stu-id="d0545-189">Entry</span></span> | <span data-ttu-id="d0545-190">Value</span><span class="sxs-lookup"><span data-stu-id="d0545-190">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d0545-191">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d0545-191">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0545-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0545-192">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0545-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0545-193">System-Only</span></span>            | <span data-ttu-id="d0545-194">False</span><span class="sxs-lookup"><span data-stu-id="d0545-194">False</span></span>                                                     |
| <span data-ttu-id="d0545-195">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d0545-195">Is-Single-Valued</span></span>       | <span data-ttu-id="d0545-196">True</span><span class="sxs-lookup"><span data-stu-id="d0545-196">True</span></span>                                                      |
| <span data-ttu-id="d0545-197">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d0545-197">Is Indexed</span></span>             | <span data-ttu-id="d0545-198">False</span><span class="sxs-lookup"><span data-stu-id="d0545-198">False</span></span>                                                     |
| <span data-ttu-id="d0545-199">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d0545-199">In Global Catalog</span></span>      | <span data-ttu-id="d0545-200">False</span><span class="sxs-lookup"><span data-stu-id="d0545-200">False</span></span>                                                     |
| <span data-ttu-id="d0545-201">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d0545-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0545-202">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0545-202">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d0545-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0545-203">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d0545-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0545-204">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d0545-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0545-205">Search-Flags</span></span>           | <span data-ttu-id="d0545-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0545-206">0x00000000</span></span>                                                |
| <span data-ttu-id="d0545-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0545-207">System-Flags</span></span>           | <span data-ttu-id="d0545-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0545-208">0x00000000</span></span>                                                |
| <span data-ttu-id="d0545-209">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d0545-209">Classes used in</span></span>        | [<span data-ttu-id="d0545-210">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="d0545-210">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d0545-211">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d0545-211">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d0545-212">Entrada</span><span class="sxs-lookup"><span data-stu-id="d0545-212">Entry</span></span> | <span data-ttu-id="d0545-213">Value</span><span class="sxs-lookup"><span data-stu-id="d0545-213">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d0545-214">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d0545-214">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0545-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0545-215">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0545-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0545-216">System-Only</span></span>            | <span data-ttu-id="d0545-217">False</span><span class="sxs-lookup"><span data-stu-id="d0545-217">False</span></span>                                                     |
| <span data-ttu-id="d0545-218">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d0545-218">Is-Single-Valued</span></span>       | <span data-ttu-id="d0545-219">True</span><span class="sxs-lookup"><span data-stu-id="d0545-219">True</span></span>                                                      |
| <span data-ttu-id="d0545-220">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d0545-220">Is Indexed</span></span>             | <span data-ttu-id="d0545-221">False</span><span class="sxs-lookup"><span data-stu-id="d0545-221">False</span></span>                                                     |
| <span data-ttu-id="d0545-222">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d0545-222">In Global Catalog</span></span>      | <span data-ttu-id="d0545-223">False</span><span class="sxs-lookup"><span data-stu-id="d0545-223">False</span></span>                                                     |
| <span data-ttu-id="d0545-224">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d0545-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0545-225">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0545-225">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d0545-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0545-226">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d0545-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0545-227">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d0545-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0545-228">Search-Flags</span></span>           | <span data-ttu-id="d0545-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0545-229">0x00000000</span></span>                                                |
| <span data-ttu-id="d0545-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0545-230">System-Flags</span></span>           | <span data-ttu-id="d0545-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0545-231">0x00000000</span></span>                                                |
| <span data-ttu-id="d0545-232">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d0545-232">Classes used in</span></span>        | [<span data-ttu-id="d0545-233">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="d0545-233">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d0545-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d0545-234">Windows Server 2012</span></span>



| <span data-ttu-id="d0545-235">Entrada</span><span class="sxs-lookup"><span data-stu-id="d0545-235">Entry</span></span> | <span data-ttu-id="d0545-236">Value</span><span class="sxs-lookup"><span data-stu-id="d0545-236">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d0545-237">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d0545-237">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0545-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0545-238">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0545-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0545-239">System-Only</span></span>            | <span data-ttu-id="d0545-240">False</span><span class="sxs-lookup"><span data-stu-id="d0545-240">False</span></span>                                                     |
| <span data-ttu-id="d0545-241">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d0545-241">Is-Single-Valued</span></span>       | <span data-ttu-id="d0545-242">True</span><span class="sxs-lookup"><span data-stu-id="d0545-242">True</span></span>                                                      |
| <span data-ttu-id="d0545-243">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d0545-243">Is Indexed</span></span>             | <span data-ttu-id="d0545-244">False</span><span class="sxs-lookup"><span data-stu-id="d0545-244">False</span></span>                                                     |
| <span data-ttu-id="d0545-245">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d0545-245">In Global Catalog</span></span>      | <span data-ttu-id="d0545-246">False</span><span class="sxs-lookup"><span data-stu-id="d0545-246">False</span></span>                                                     |
| <span data-ttu-id="d0545-247">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d0545-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0545-248">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0545-248">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d0545-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0545-249">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d0545-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0545-250">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d0545-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0545-251">Search-Flags</span></span>           | <span data-ttu-id="d0545-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0545-252">0x00000000</span></span>                                                |
| <span data-ttu-id="d0545-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0545-253">System-Flags</span></span>           | <span data-ttu-id="d0545-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0545-254">0x00000000</span></span>                                                |
| <span data-ttu-id="d0545-255">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d0545-255">Classes used in</span></span>        | [<span data-ttu-id="d0545-256">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="d0545-256">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





