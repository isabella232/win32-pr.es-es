---
description: En esta página se describe el comportamiento de las opciones de socket de multidifusión en función de los distintos Estados de configuración de opciones de socket.
ms.assetid: a411e831-7b28-4ab5-a09a-650db99a7cd5
title: Comportamiento de la opción de socket de multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd10094750bea59b844ad1fcdac70be0c7f9646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082116"
---
# <a name="multicast-socket-option-behavior"></a>Comportamiento de la opción de socket de multidifusión

En esta página se describe el comportamiento de las opciones de socket de multidifusión en función de los distintos Estados de configuración de opciones de socket.

Por ejemplo, en esta página se describe el comportamiento cuando \_ \_ se establece la opción de socket de pertenencia de origen de adición \_ de IP en un socket para el que ya se ha establecido la opción de pertenencia a un origen de código IP \_ \_ \_ con el par de grupo/origen especificado en la misma interfaz de red. Se permite llamar a \_ \_ la pertenencia al origen de la adición de IP \_ en el mismo grupo en una interfaz de red diferente.

Esta página ayuda a diseñar y solucionar problemas de aplicaciones de multidifusión de Windows Sockets correctamente. 

<table>
<thead>
<tr class="header">
<th>Opción de socket inicial</th>
<th>Opción de socket subsiguiente en conflicto</th>
<th>Error devuelto</th>
<th>Observaciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4">IP_ADD_MEMBERSHIP $ {REMOVE} $<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>No llame a IP_ADD_MEMBERSHIP con el mismo grupo más de una vez en la misma interfaz de red.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>No llame a IP_ADD_SOURCE_MEMBERSHIP con el mismo grupo previamente llamado con IP_ADD_MEMBERSHIP en la misma interfaz de red.</td>

</tr>
<tr class="odd">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>En su lugar, use IP_BLOCK_SOURCE.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Devuelve un error al intentar desbloquear un par de grupo/origen que no se ha bloqueado previamente en la misma interfaz de red.</td>

</tr>
<tr class="odd">
<td>IP_DROP_MEMBERSHIP</td>
<td>Cualquier llamada posterior en el mismo grupo o grupo/origen</td>
<td>WSAEINVAL</td>
<td>La realización de llamadas a opciones de socket en un par de grupo o grupo/origen no se encuentra actualmente en la lista de inclusión (debido a la eliminación de la pertenencia, o de otro modo) produce un error.</td>
</tr>
<tr class="even">
<td rowspan="3">IP_ADD_SOURCE_MEMBERSHIP $ {REMOVE} $<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>No llame a IP_ADD_MEMBERSHIP con el mismo grupo previamente llamado con IP_ADD_SOURCE_MEMBERSHIP en la misma interfaz de red.</td>
</tr>
<tr class="odd">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>No llame a IP_ADD_SOURCE_MEMBERSHIP con el mismo par de grupo/origen llamado previamente con IP_ADD_SOURCE_MEMBERSHIP en la misma interfaz de red.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Devuelve un error al intentar desbloquear un par de grupo/origen que no se ha bloqueado previamente en la misma interfaz de red.</td>

</tr>
<tr class="odd">
<td rowspan="2">IP_DROP_SOURCE_MEMBERSHIP $ {REMOVE} $<br />
</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Devuelve un error al intentar desbloquear un par de grupo/origen que no se ha bloqueado previamente en la misma interfaz de red.</td>
</tr>
<tr class="even">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Devuelve un error al intentar quitar un par de grupo/origen que no está en la lista de inclusión de la misma interfaz de red.</td>

</tr>
<tr class="odd">
<td rowspan="3">IP_BLOCK_SOURCE $ {REMOVE} $<br />
</td>
<td>IP_BLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Devuelve un error al intentar bloquear un par de grupo/origen que ya está bloqueado en la misma interfaz de red.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>En su lugar, use IP_UNBLOCK_SOURCE.</td>

</tr>
<tr class="odd">
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>En su lugar, use IP_UNBLOCK_SOURCE.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Devuelve un error al intentar desbloquear un par de grupo/origen que no está en la lista de bloqueados en la misma interfaz de red.</td>
</tr>
</tbody>
</table>



 

 

 



