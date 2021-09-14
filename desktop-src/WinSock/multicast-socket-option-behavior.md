---
description: En esta página se describe el comportamiento de las opciones de socket de multidifusión basadas en varios estados de configuración de opciones de socket.
ms.assetid: a411e831-7b28-4ab5-a09a-650db99a7cd5
title: Comportamiento de la opción de socket de multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460b13fb710e86ef81fb64b48b697f7e73ccf392
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172585"
---
# <a name="multicast-socket-option-behavior"></a>Comportamiento de la opción de socket de multidifusión

En esta página se describe el comportamiento de las opciones de socket de multidifusión basadas en varios estados de configuración de opciones de socket.

Por ejemplo, en esta página se describe el comportamiento cuando se establece la opción de socket IP ADD SOURCE MEMBERSHIP en un socket para el que ya se ha establecido la opción IP ADD SOURCE MEMBERSHIP con el par de \_ \_ \_ \_ \_ grupo/origen especificado en la misma interfaz de \_ red. Se permite llamar a IP \_ ADD SOURCE MEMBERSHIP en el mismo grupo en una interfaz de red \_ \_ diferente.

Esta página ayuda a diseñar y solucionar problemas correctamente de Windows multidifusión sockets. 

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
<td rowspan="4">IP_ADD_MEMBERSHIP<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>No llame a IP_ADD_MEMBERSHIP con el mismo grupo más de una vez en la misma interfaz de red.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>No llame a IP_ADD_SOURCE_MEMBERSHIP con el mismo grupo llamado previamente con IP_ADD_MEMBERSHIP en la misma interfaz de red.</td>

</tr>
<tr class="odd">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>Use IP_BLOCK_SOURCE en su lugar.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Devuelve un error al intentar desbloquear un par de grupo y origen que no se ha bloqueado previamente en la misma interfaz de red.</td>

</tr>
<tr class="odd">
<td>IP_DROP_MEMBERSHIP</td>
<td>Cualquier llamada posterior en el mismo grupo o grupo/par de origen</td>
<td>WSAEINVAL</td>
<td>La realización de llamadas a la opción de socket en un par de grupo o grupo/origen que no se encuentra actualmente en la lista de inclusión (debido a la caída de la pertenencia o de otro modo) produce un error.</td>
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
<td>Devuelve un error al intentar desbloquear un par de grupo y origen que no se ha bloqueado previamente en la misma interfaz de red.</td>

</tr>
<tr class="odd">
<td rowspan="2">IP_DROP_SOURCE_MEMBERSHIP<br />
</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Devuelve un error al intentar desbloquear un par de grupo y origen que no se ha bloqueado previamente en la misma interfaz de red.</td>
</tr>
<tr class="even">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Devuelve un error al intentar quitar un par de grupo y origen que no está en la lista de inclusión en la misma interfaz de red.</td>

</tr>
<tr class="odd">
<td rowspan="3">IP_BLOCK_SOURCE<br />
</td>
<td>IP_BLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Devuelve un error al intentar bloquear un par de grupo y origen que ya está bloqueado en la misma interfaz de red.</td>
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
<td>Devuelve un error al intentar desbloquear un par de grupo y origen que no está en la lista de bloqueados en la misma interfaz de red.</td>
</tr>
</tbody>
</table>



 

 

 



