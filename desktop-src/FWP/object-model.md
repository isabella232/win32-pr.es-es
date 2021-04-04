---
title: Modelo de objetos
description: En la tabla siguiente se enumeran los tipos de objeto que se pueden manipular a través de los distintos conjuntos de API proporcionados por la plataforma de filtrado de Windows (WFP).
ms.assetid: 6931583f-785c-4e27-b5e4-d185d23a54ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa90b4757a39617616c6f83b6b79fe322b2e64c8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104077360"
---
# <a name="object-model"></a><span data-ttu-id="30fb9-103">Modelo de objetos</span><span class="sxs-lookup"><span data-stu-id="30fb9-103">Object Model</span></span>

<span data-ttu-id="30fb9-104">En la tabla siguiente se enumeran los tipos de objeto que se pueden manipular a través de los distintos conjuntos de API proporcionados por la plataforma de filtrado de Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="30fb9-104">The following table lists the object types that can be manipulated through the various API sets supplied by the Windows Filtering Platform (WFP).</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30fb9-105">Tipo de objeto</span><span class="sxs-lookup"><span data-stu-id="30fb9-105">Object Type</span></span></th>
<th><span data-ttu-id="30fb9-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="30fb9-106">Description</span></span></th>
<th><span data-ttu-id="30fb9-107">Propiedades de ejemplo</span><span class="sxs-lookup"><span data-stu-id="30fb9-107">Sample Properties</span></span></th>
<th><span data-ttu-id="30fb9-108">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="30fb9-108">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30fb9-109">Filter</span><span class="sxs-lookup"><span data-stu-id="30fb9-109">Filter</span></span></td>
<td><span data-ttu-id="30fb9-110">Una regla que rige la clasificación.</span><span class="sxs-lookup"><span data-stu-id="30fb9-110">A rule that governs classification.</span></span> <span data-ttu-id="30fb9-111">Si se cumplen las condiciones, se invoca la acción.</span><span class="sxs-lookup"><span data-stu-id="30fb9-111">If the conditions are met, the action is invoked.</span></span> <br/> <span data-ttu-id="30fb9-112">Este es el objeto más complejo expuesto por WFP, ya que une todos los demás tipos de objeto.</span><span class="sxs-lookup"><span data-stu-id="30fb9-112">This is the most complex object exposed by WFP since it ties together all the other object types.</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="30fb9-113">Matriz de condiciones</span><span class="sxs-lookup"><span data-stu-id="30fb9-113">Array of conditions</span></span></li>
<li><span data-ttu-id="30fb9-114">Acción (permitir, bloquear, llamada)</span><span class="sxs-lookup"><span data-stu-id="30fb9-114">Action (Permit, Block, Callout)</span></span></li>
<li><span data-ttu-id="30fb9-115"><a href="filter-weight-assignment.md">Peso</a></span><span class="sxs-lookup"><span data-stu-id="30fb9-115"><a href="filter-weight-assignment.md">Weight</a></span></span></li>
<li><span data-ttu-id="30fb9-116">Context</span><span class="sxs-lookup"><span data-stu-id="30fb9-116">Context</span></span></li>
</ul></td>
<td><span data-ttu-id="30fb9-117">&quot;Bloquee el tráfico con un puerto TCP superior a 1024.&quot;</span><span class="sxs-lookup"><span data-stu-id="30fb9-117">&quot;Block traffic with a TCP port greater than 1024.&quot;</span></span> <br/> <span data-ttu-id="30fb9-118">&quot;Llamada a los IDENTIFICADOres para todo el tráfico que no está protegido.&quot;</span><span class="sxs-lookup"><span data-stu-id="30fb9-118">&quot;Callout to IDS for all traffic that is not secured.&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30fb9-119">Llamada</span><span class="sxs-lookup"><span data-stu-id="30fb9-119">Callout</span></span></td>
<td><span data-ttu-id="30fb9-120">Conjunto de funciones que participan en el proceso de clasificación.</span><span class="sxs-lookup"><span data-stu-id="30fb9-120">A set of functions that participate in the classification process.</span></span><br/> <span data-ttu-id="30fb9-121">Permite que se realice el procesamiento personalizado de paquetes cuando se cumplen determinadas condiciones.</span><span class="sxs-lookup"><span data-stu-id="30fb9-121">It allows for custom packet processing to be done when certain conditions are met.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="30fb9-122">id</span><span class="sxs-lookup"><span data-stu-id="30fb9-122">ID</span></span></li>
<li><span data-ttu-id="30fb9-123">Nivel aplicable</span><span class="sxs-lookup"><span data-stu-id="30fb9-123">Applicable layer</span></span></li>
</ul></td>
<td><span data-ttu-id="30fb9-124">El controlador NAT</span><span class="sxs-lookup"><span data-stu-id="30fb9-124">The NAT driver</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30fb9-125">Nivel</span><span class="sxs-lookup"><span data-stu-id="30fb9-125">Layer</span></span></td>
<td><span data-ttu-id="30fb9-126">Un contenedor de filtros en el motor de filtro.</span><span class="sxs-lookup"><span data-stu-id="30fb9-126">A filter container in the filter engine.</span></span> <br/> <span data-ttu-id="30fb9-127">Representa un punto específico en el procesamiento del tráfico de red donde se invoca el motor de filtro.</span><span class="sxs-lookup"><span data-stu-id="30fb9-127">Represents a specific point in network traffic processing where the filter engine is invoked.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="30fb9-128">Esquema para los filtros que se pueden agregar a la capa</span><span class="sxs-lookup"><span data-stu-id="30fb9-128">Schema for filters that can be added to the layer</span></span></li>
</ul></td>
<td><span data-ttu-id="30fb9-129">La capa de transporte de entrada</span><span class="sxs-lookup"><span data-stu-id="30fb9-129">The Inbound Transport Layer</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30fb9-130">Capa secundaria</span><span class="sxs-lookup"><span data-stu-id="30fb9-130">Sub-layer</span></span></td>
<td><span data-ttu-id="30fb9-131">Un subcomponente de una capa, que se usa en el <a href="filter-arbitration.md">arbitraje de filtros</a>.</span><span class="sxs-lookup"><span data-stu-id="30fb9-131">A sub-component of a layer, used in <a href="filter-arbitration.md">filter arbitration</a>.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="30fb9-132">Peso</span><span class="sxs-lookup"><span data-stu-id="30fb9-132">Weight</span></span></li>
</ul></td>
<td><span data-ttu-id="30fb9-133">La subcapa del túnel IPsec</span><span class="sxs-lookup"><span data-stu-id="30fb9-133">The IPsec Tunnel sub-layer</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30fb9-134">Proveedor</span><span class="sxs-lookup"><span data-stu-id="30fb9-134">Provider</span></span></td>
<td><span data-ttu-id="30fb9-135">Un proveedor de directivas que ha compilado una solución en WFP.</span><span class="sxs-lookup"><span data-stu-id="30fb9-135">A policy provider that has built a solution on WFP.</span></span><br/> <span data-ttu-id="30fb9-136">Se utiliza únicamente para la administración; no afecta al procesamiento de paquetes en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="30fb9-136">It is used solely for management; it does not affect run-time packet processing.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="30fb9-137">id</span><span class="sxs-lookup"><span data-stu-id="30fb9-137">ID</span></span></li>
<li><span data-ttu-id="30fb9-138">Nombre del servicio</span><span class="sxs-lookup"><span data-stu-id="30fb9-138">Service name</span></span></li>
</ul></td>
<td><span data-ttu-id="30fb9-139">Firewall de Windows con seguridad avanzada</span><span class="sxs-lookup"><span data-stu-id="30fb9-139">Windows Firewall with Advanced Security</span></span><br/> <span data-ttu-id="30fb9-140">Una aplicación de filtrado de direcciones URL de terceros</span><span class="sxs-lookup"><span data-stu-id="30fb9-140">A 3rd-party URL filtering application</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30fb9-141">Contexto de proveedor</span><span class="sxs-lookup"><span data-stu-id="30fb9-141">Provider Context</span></span></td>
<td><span data-ttu-id="30fb9-142">Un BLOB de datos utilizado por un proveedor de directivas para almacenar información de contexto arbitrario.</span><span class="sxs-lookup"><span data-stu-id="30fb9-142">A data blob used by a policy provider to store arbitrary context information.</span></span> <br/> <span data-ttu-id="30fb9-143">Se usa para pasar información de configuración personalizada a una llamada.</span><span class="sxs-lookup"><span data-stu-id="30fb9-143">It is used to pass custom configuration information to a callout.</span></span><br/> <span data-ttu-id="30fb9-144">La forma más común de usar la información de contexto es que los filtros hagan referencia a un contexto de proveedor.</span><span class="sxs-lookup"><span data-stu-id="30fb9-144">The most common way to use the context information is to have filters reference a provider context.</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="30fb9-145">id</span><span class="sxs-lookup"><span data-stu-id="30fb9-145">ID</span></span></li>
<li><span data-ttu-id="30fb9-146">BLOB de datos</span><span class="sxs-lookup"><span data-stu-id="30fb9-146">Data blob</span></span></li>
</ul></td>
<td><span data-ttu-id="30fb9-147">IPsec almacena la configuración de autenticación en el motor de filtrado de base (BFE).</span><span class="sxs-lookup"><span data-stu-id="30fb9-147">IPsec stores authentication settings in the Base Filtering Engine ( BFE).</span></span> <span data-ttu-id="30fb9-148">La &quot; &quot; propiedad de contexto de un filtro indica la configuración de autenticación que se va a usar para el tráfico que describe el filtro.</span><span class="sxs-lookup"><span data-stu-id="30fb9-148">The &quot;Context&quot; property of a filter indicates the authentication settings to use for the traffic that the filter describes.</span></span><br/> <span data-ttu-id="30fb9-149">La corrección de compatibilidad de la selección de certificación SSL almacenará la información de certificación en un contexto de proveedor.</span><span class="sxs-lookup"><span data-stu-id="30fb9-149">The SSL certification selection shim will store certification information in a provider context.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="30fb9-150">Los tipos de objeto expuestos por la API de WFP tienen una semántica coherente.</span><span class="sxs-lookup"><span data-stu-id="30fb9-150">The object types exposed by WFP API have consistent semantics.</span></span> <span data-ttu-id="30fb9-151">Las acciones de agregar, enumerar, suscribir, etc., son similares para todos los tipos de objeto.</span><span class="sxs-lookup"><span data-stu-id="30fb9-151">The actions of add, enumerate, subscribe, and so on are similar for all object types.</span></span>

<span data-ttu-id="30fb9-152">Cada tipo de objeto se representa mediante una estructura de datos (por ejemplo, [**FWPM \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)).</span><span class="sxs-lookup"><span data-stu-id="30fb9-152">Each object type is represented by a data structure (for example, [**FWPM\_FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)).</span></span> <span data-ttu-id="30fb9-153">Con el fin de minimizar el número de estructuras de datos diferentes que expone la API de WFP, se usa la misma estructura de datos para agregar nuevos objetos y recuperar los existentes.</span><span class="sxs-lookup"><span data-stu-id="30fb9-153">In order to minimize the number of different data structures exposed by the WFP API, the same data structure is used for both adding new objects and retrieving existing ones.</span></span> <span data-ttu-id="30fb9-154">Por lo tanto, puede haber campos en cada estructura de datos que se omitan al agregar un nuevo objeto, ya que estos campos los rellenará el motor de filtrado de base (BFE), y no el llamador.</span><span class="sxs-lookup"><span data-stu-id="30fb9-154">Thus, there may be fields in each data structure that are ignored when adding a new object since these fields are filled in by the Base Filtering Engine (BFE), and not by the caller.</span></span> <span data-ttu-id="30fb9-155">Por ejemplo, una estructura de datos de **FWPM \_ FILTER0** tiene un campo **FilterId** que contiene el **LUID** del **FWPS \_ FILTER0** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="30fb9-155">For example, an **FWPM\_FILTER0** data structure has a **filterId** field that contains the **LUID** of the corresponding **FWPS\_FILTER0**.</span></span> <span data-ttu-id="30fb9-156">BFE asigna este **LUID** y, por lo tanto, este campo se omite en la llamada a [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).</span><span class="sxs-lookup"><span data-stu-id="30fb9-156">This **LUID** is assigned by BFE, and thus, this field is ignored in the call to [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).</span></span>

## <a name="related-topics"></a><span data-ttu-id="30fb9-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="30fb9-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30fb9-158">Administración de objetos</span><span class="sxs-lookup"><span data-stu-id="30fb9-158">Object Management</span></span>](object-management.md)
</dt> </dl>

 

 





