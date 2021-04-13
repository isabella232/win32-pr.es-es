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
# <a name="processing-groups-and-callbacks"></a>Procesar grupos y devoluciones de llamada

En la tabla siguiente se resume una serie de pasos en una interacción operativa entre un protocolo de enrutamiento y el administrador del grupo de multidifusión. En la primera columna se describen las acciones que realiza el protocolo de enrutamiento y las respuestas del Protocolo de enrutamiento al administrador del grupo de multidifusión. En la segunda columna se describen las respuestas del administrador del grupo de multidifusión al Protocolo de enrutamiento y las acciones que realiza el administrador del grupo de multidifusión, como las devoluciones de llamada. La tercera columna presenta cualquier información adicional.

Cada fila de la tabla representa un paso.

Las tareas que se muestran en esta tabla no se producen en ningún orden específico; en su lugar, se producen en función del estado de la pertenencia a grupos de multidifusión. En la tabla siguiente se muestra un orden de ejemplo.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Acción del Protocolo de enrutamiento</th>
<th>Acción del administrador del grupo de multidifusión</th>
<th>Notas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Administrar la pertenencia a grupos según la información de protocolo recibida en las interfaces que posee el protocolo. La administración se realiza mediante las siguientes funciones:
<ul>
<li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></li>
<li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></li>
</ul></td>
<td>Agregue y elimine de la lista de interfaces de salida para las entradas especificadas (s, g), (*, g) y (*, *). Esta lista representa el conjunto de interfaces en las que se reenvían los datos para este grupo. Los datos de este grupo proceden del origen especificado.</td>

</tr>
<tr class="even">

<td>Enviar alertas a protocolos de enrutamiento en forma de devoluciones de llamada. Los siguientes eventos desencadenan el administrador del grupo de multidifusión para invocar una devolución de llamada:
<ul>
<li>Unirse a grupos o abandonarlos ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</li>
<li>La pertenencia a grupos cambiada por IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</li>
<li>Datos recibidos en una interfaz incorrecta ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</li>
<li>Datos recibidos de nuevos orígenes o de un nuevo grupo ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> y <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</li>
</ul></td>
<td>Con estas devoluciones de llamada, el administrador del grupo de multidifusión puede coordinar el reenvío de paquetes cuando hay varios protocolos de enrutamiento de multidifusión presentes en un enrutador.</td>
</tr>
<tr class="odd">
<td>Enumerar las entradas de reenvío de multidifusión (MFEs) mediante las funciones <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>y <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe</strong></a> . Tomar decisiones sobre los datos de multidifusión en función de los resultados de la enumeración.</td>
<td>Devuelve el MFEs solicitado. Devuelve ERROR_NO_MORE elementos cuando no hay más MFEs para devolver.<br/></td>
<td>Use las funciones <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats</strong></a> para enumerar las estadísticas de MFE. Consulte <a href="administrative-application-scenario.md">escenario de aplicación administrativa</a> para obtener un ejemplo completo del uso de estas funciones.<br/></td>
</tr>
<tr class="even">
<td>Modifique el vecino ascendente en un MFE con la función <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe</strong></a> .</td>

<td>Los clientes utilizan esta función para modificar la información relacionada con la interfaz entrante.</td>
</tr>
</tbody>
</table>



 

 

