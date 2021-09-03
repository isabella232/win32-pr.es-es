---
description: En esta página se describe el comportamiento de las opciones de socket de multidifusión en función de los distintos estados de configuración de las opciones de socket.
ms.assetid: a411e831-7b28-4ab5-a09a-650db99a7cd5
title: Comportamiento de las opciones de socket de multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460b13fb710e86ef81fb64b48b697f7e73ccf392
ms.sourcegitcommit: 9942a888f172981e276def0c6b84fb0266fcb02d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2021
ms.locfileid: "123399771"
---
# <a name="multicast-socket-option-behavior"></a>Comportamiento de las opciones de socket de multidifusión

En esta página se describe el comportamiento de las opciones de socket de multidifusión en función de los distintos estados de configuración de las opciones de socket.

Por ejemplo, en esta página se describe el comportamiento cuando la opción de socket ADD SOURCE MEMBERSHIP de IP se establece en un socket para el que ya se ha establecido la opción ADD SOURCE MEMBERSHIP de IP con el par de origen/grupo especificado en la misma interfaz de \_ \_ \_ \_ \_ \_ red. Se permite llamar a IP \_ ADD SOURCE MEMBERSHIP en el mismo grupo en una interfaz de red \_ \_ diferente.

Esta página ayuda a diseñar y solucionar problemas correctamente en Windows multidifusión sockets. 

<table>
<thead>
<tr class="header">
<th>Opción de socket inicial</th>
<th>Opción de socket posterior en conflicto</th>
<th>Error devuelto</th>
<th>Observaciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4">IP_ADD_MEMBERSHIP<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>No llame a IP_ADD_MEMBERSHIP con el mismo grupo más de una vez en la misma interfaz de red.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>No llame a IP_ADD_SOURCE_MEMBERSHIP con el mismo grupo llamado anteriormente con IP_ADD_MEMBERSHIP en la misma interfaz de red.</td>

</tr>
<tr class="odd">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>Use IP_BLOCK_SOURCE en su lugar.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Devuelve un error al intentar desbloquear un par de grupo/origen que no se ha bloqueado previamente en la misma interfaz de red.</td>

</tr>
<tr class="odd">
<td>IP_DROP_MEMBERSHIP</td>
<td>Cualquier llamada posterior en el mismo grupo o grupo/par de origen</td>
<td>WSAEINVAL</td>
<td>La realización de llamadas de opción de socket en un grupo o grupo/par de origen que no se encuentra actualmente en la lista de inclusión (debido a la caída de la pertenencia o de lo contrario) produce un error.</td>
</tr>
<tr class="even">
<td rowspan="3">IP_ADD_SOURCE_MEMBERSHIP<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>No llame a IP_ADD_MEMBERSHIP con el mismo grupo llamado anteriormente con IP_ADD_SOURCE_MEMBERSHIP en la misma interfaz de red.</td>
</tr>
<tr class="odd">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>No llame a IP_ADD_SOURCE_MEMBERSHIP con el mismo par de grupo/origen llamado anteriormente con IP_ADD_SOURCE_MEMBERSHIP en la misma interfaz de red.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Devuelve un error al intentar desbloquear un par de grupo/origen que no se ha bloqueado previamente en la misma interfaz de red.</td>

</tr>
<tr class="odd">
<td rowspan="2">IP_DROP_SOURCE_MEMBERSHIP<br />
</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Devuelve un error al intentar desbloquear un par de grupo/origen que no se ha bloqueado previamente en la misma interfaz de red.</td>
</tr>
<tr class="even">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Devuelve un error al intentar quitar un par de grupo/origen que no está en la lista de inclusión en la misma interfaz de red.</td>

</tr>
<tr class="odd">
<td rowspan="3">IP_BLOCK_SOURCE<br />
</td>
<td>IP_BLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Devuelve un error al intentar bloquear un par de grupo/origen que ya está bloqueado en la misma interfaz de red.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>Use IP_UNBLOCK_SOURCE en su lugar.</td>

</tr>
<tr class="odd">
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>Use IP_UNBLOCK_SOURCE en su lugar.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Devuelve un error al intentar desbloquear un par de grupo/origen que no está en la lista de bloqueados en la misma interfaz de red.</td>
</tr>
</tbody>
</table>



 

 

 



