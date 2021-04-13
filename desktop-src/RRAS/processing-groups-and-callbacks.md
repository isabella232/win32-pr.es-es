---
title: Procesar grupos y devoluciones de llamada
description: En la tabla siguiente se resume una serie de pasos en una interacción operativa entre un protocolo de enrutamiento y el administrador del grupo de multidifusión.
ms.assetid: 43c1dc12-70fd-4e02-a7b1-5818e6d7ddc6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2878ec15cfb663353f3dd0bc1dc5aeadbd2e1e7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104359474"
---
# <a name="processing-groups-and-callbacks"></a><span data-ttu-id="8e3cb-103">Procesar grupos y devoluciones de llamada</span><span class="sxs-lookup"><span data-stu-id="8e3cb-103">Processing Groups and Callbacks</span></span>

<span data-ttu-id="8e3cb-104">En la tabla siguiente se resume una serie de pasos en una interacción operativa entre un protocolo de enrutamiento y el administrador del grupo de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-104">The following table summarizes a series of steps in an operational interaction between a routing protocol and the multicast group manager.</span></span> <span data-ttu-id="8e3cb-105">En la primera columna se describen las acciones que realiza el protocolo de enrutamiento y las respuestas del Protocolo de enrutamiento al administrador del grupo de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-105">The first column describes the actions that the routing protocol performs and the routing protocol's responses to the multicast group manager.</span></span> <span data-ttu-id="8e3cb-106">En la segunda columna se describen las respuestas del administrador del grupo de multidifusión al Protocolo de enrutamiento y las acciones que realiza el administrador del grupo de multidifusión, como las devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-106">The second column describes the multicast group manager's responses to the routing protocol and any actions the multicast group manager performs such as callbacks.</span></span> <span data-ttu-id="8e3cb-107">La tercera columna presenta cualquier información adicional.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-107">The third column presents any additional information.</span></span>

<span data-ttu-id="8e3cb-108">Cada fila de la tabla representa un paso.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-108">Each row of the table represents one step.</span></span>

<span data-ttu-id="8e3cb-109">Las tareas que se muestran en esta tabla no se producen en ningún orden específico; en su lugar, se producen en función del estado de la pertenencia a grupos de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-109">The tasks listed in this table do not occur in any specific order; rather, they occur based on the status of multicast group memberships.</span></span> <span data-ttu-id="8e3cb-110">En la tabla siguiente se muestra un orden de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-110">The table below shows an example order.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e3cb-111">Acción del Protocolo de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="8e3cb-111">Routing protocol action</span></span></th>
<th><span data-ttu-id="8e3cb-112">Acción del administrador del grupo de multidifusión</span><span class="sxs-lookup"><span data-stu-id="8e3cb-112">Multicast group manager action</span></span></th>
<th><span data-ttu-id="8e3cb-113">Notas</span><span class="sxs-lookup"><span data-stu-id="8e3cb-113">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8e3cb-114">Administrar la pertenencia a grupos según la información de protocolo recibida en las interfaces que posee el protocolo.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-114">Manage group memberships based on protocol information received on those interfaces that the protocol owns.</span></span> <span data-ttu-id="8e3cb-115">La administración se realiza mediante las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="8e3cb-115">Management is performed using the following functions:</span></span>
<ul>
<li><span data-ttu-id="8e3cb-116"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></span><span class="sxs-lookup"><span data-stu-id="8e3cb-116"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></span></span></li>
<li><span data-ttu-id="8e3cb-117"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></span><span class="sxs-lookup"><span data-stu-id="8e3cb-117"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="8e3cb-118">Agregue y elimine de la lista de interfaces de salida para las entradas especificadas (s, g), (*, g) y (*, \*).</span><span class="sxs-lookup"><span data-stu-id="8e3cb-118">Add to and delete from the outgoing interface list for the specified (s, g), (*, g), and (*, \*) entries.</span></span> <span data-ttu-id="8e3cb-119">Esta lista representa el conjunto de interfaces en las que se reenvían los datos para este grupo.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-119">This list represents the set of interfaces on which data for this group is forwarded.</span></span> <span data-ttu-id="8e3cb-120">Los datos de este grupo proceden del origen especificado.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-120">The data for this group is from the specified source.</span></span></td>

</tr>
<tr class="even">

<td><span data-ttu-id="8e3cb-121">Enviar alertas a protocolos de enrutamiento en forma de devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-121">Send alerts to routing protocols in the form of callbacks.</span></span> <span data-ttu-id="8e3cb-122">Los siguientes eventos desencadenan el administrador del grupo de multidifusión para invocar una devolución de llamada:</span><span class="sxs-lookup"><span data-stu-id="8e3cb-122">The following events trigger the multicast group manager to invoke a callback:</span></span>
<ul>
<li><span data-ttu-id="8e3cb-123">Unirse a grupos o abandonarlos ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="8e3cb-123">Join or leave groups ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="8e3cb-124">La pertenencia a grupos cambiada por IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="8e3cb-124">Group membership changed by IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="8e3cb-125">Datos recibidos en una interfaz incorrecta ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="8e3cb-125">Data received on wrong interface ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="8e3cb-126">Datos recibidos de nuevos orígenes o de un nuevo grupo ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> y <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="8e3cb-126">Data received from new sources or to a new group ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> and <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</span></span></li>
</ul></td>
<td><span data-ttu-id="8e3cb-127">Con estas devoluciones de llamada, el administrador del grupo de multidifusión puede coordinar el reenvío de paquetes cuando hay varios protocolos de enrutamiento de multidifusión presentes en un enrutador.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-127">Using these callbacks, the multicast group manager is able to coordinate packet forwarding when several multicast routing protocols are present on a router.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e3cb-128">Enumerar las entradas de reenvío de multidifusión (MFEs) mediante las funciones <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>y <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8e3cb-128">Enumerate the multicast forwarding entries (MFEs), using the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>, and <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe</strong></a> functions.</span></span> <span data-ttu-id="8e3cb-129">Tomar decisiones sobre los datos de multidifusión en función de los resultados de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-129">Make decisions about multicast data based on the results of the enumeration.</span></span></td>
<td><span data-ttu-id="8e3cb-130">Devuelve el MFEs solicitado.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-130">Return the requested MFEs.</span></span> <span data-ttu-id="8e3cb-131">Devuelve ERROR_NO_MORE elementos cuando no hay más MFEs para devolver.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-131">Return ERROR_NO_MORE ITEMS when there are no more MFEs to return.</span></span><br/></td>
<td><span data-ttu-id="8e3cb-132">Use las funciones <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats</strong></a> para enumerar las estadísticas de MFE.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-132">Use the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats</strong></a> functions to enumerate MFE statistics.</span></span> <span data-ttu-id="8e3cb-133">Consulte <a href="administrative-application-scenario.md">escenario de aplicación administrativa</a> para obtener un ejemplo completo del uso de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-133">See <a href="administrative-application-scenario.md">Administrative Application Scenario</a> for a complete example of using these functions.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e3cb-134">Modifique el vecino ascendente en un MFE con la función <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8e3cb-134">Modify the upstream neighbor in an MFE using the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe</strong></a> function.</span></span></td>

<td><span data-ttu-id="8e3cb-135">Los clientes utilizan esta función para modificar la información relacionada con la interfaz entrante.</span><span class="sxs-lookup"><span data-stu-id="8e3cb-135">Clients use this function to modify the information regarding the incoming interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

