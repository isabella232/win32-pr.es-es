---
title: IPv6-Aware y funciones auxiliares de WPAD heredadas
description: Diferencias entre las IPv6-Aware auxiliares de WPAD y las funciones auxiliares heredadas de WPAD
ms.assetid: ea4b1c0d-ce02-477b-85c8-44e1beef90c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6423b9bcb6a609cf21b8399ca03d7da1e0b19450994eb78a66f4c7aaad7d31d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861005"
---
# <a name="ipv6-aware-and-legacy-wpad-helper-functions"></a>IPv6-Aware y funciones auxiliares de WPAD heredadas

En las tablas siguientes se explican las diferencias entre las nuevas funciones auxiliares de WPAD y las funciones auxiliares de WPAD heredadas. Las nuevas funciones se marcan con un asterisco.



<table>
<thead>
<tr class="header">
<th>Funciones</th>
<th>Entrada</th>
<th>Salida</th>
<th>Motivo del cambio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>dnsResolve</td>
<td>Host</td>
<td>Dirección IPv4</td>
<td rowspan="2">La función ex devolverá una lista de IPv6/IPv4. Necesario, ya que las direcciones IPv6 o IPv4 pueden tener varias direcciones de unidifusión para una sola interfaz.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>dnsResolveEx*</td>
<td>Host</td>
<td>Lista de direcciones IPv6/IPv4</td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Funciones</th>
<th>Entrada</th>
<th>Salida</th>
<th>Motivo del cambio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>isResolveable</td>
<td>Host IPv4</td>
<td>TRUE/FALSE</td>
<td rowspan="2">La función Ex devolverá TRUE si un host puede resolverse en una dirección IPv6 o IPv4. La función heredada solo devuelve TRUE si el host se resuelve en una dirección IPv4.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>isResolveableEx*</td>
<td>Host IPv6/IPv4</td>
<td>TRUE/FALSE</td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Funciones</th>
<th>Entrada</th>
<th>Salida</th>
<th>Motivo del cambio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>myIPAddress</td>
<td>ninguno</td>
<td>Dirección IPv4</td>
<td rowspan="2">La función ex devolverá una lista de IPv6/IPv4. Necesario, ya que las direcciones IPv6 o IPv4 pueden tener varias direcciones de unidifusión para una sola interfaz ${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>myIPAddressEx*</td>
<td>ninguno</td>
<td>Lista de direcciones IPv6/IPv4</td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Funciones</th>
<th>Entrada</th>
<th>Salida</th>
<th>Motivo del cambio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>isInNet</td>
<td>Host, patrón de dirección IP separada por puntos, máscara de dirección IP</td>
<td>TRUE/FALSE</td>
<td rowspan="2">Proporcione una forma independiente de la versión de IP para averiguar si una dirección IP está en una subred determinada. Además, la notación de máscara en IPv4 está en desuso.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>isInNetEx*</td>
<td>Prefijo IP de dirección IP</td>
<td>TRUE/FALSE</td>

</tr>
</tbody>
</table>



 



| Funciones           | Entrada                       | Salida                             | Motivo del cambio                                                                                                                           |
|---------------------|-----------------------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| sortIPAddressList\* | Lista de direcciones IPv6/IPv4 | Lista ordenada de direcciones IPv6/IPv4 | No hay ninguna función heredada equivalente porque las funciones heredadas solo devolvieron una única dirección IPv4, por lo que no era necesario ordenar . |



 



| Funciones          | Entrada | Salida                     | Motivo del cambio                                                                                                                                                                                                           |
|--------------------|-------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| getClientVersion\* | ninguno  | Número de versión del motor WPAD | Actualmente, esta función devuelve la versión 1.0. Hemos agregado esta función para permitir que los administradores de TI actualicen su WPAD para que funcione con diferentes versiones del motor de WPAD sin provocar interrupciones en su implementación existente. |



 

> [!Note]  
> Esta funcionalidad requiere Windows Internet Explorer 7 o superior.

 

 

 



