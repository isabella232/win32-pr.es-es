---
title: IPv6-Aware y funciones auxiliares de WPAD heredadas
description: Diferencias entre las funciones auxiliares de WPAD IPv6-Aware y las funciones auxiliares de WPAD heredadas
ms.assetid: ea4b1c0d-ce02-477b-85c8-44e1beef90c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511b7f04aa0a2abe04b99562c15aeb3a53bdaadf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716647"
---
# <a name="ipv6-aware-and-legacy-wpad-helper-functions"></a>IPv6-Aware y funciones auxiliares de WPAD heredadas

En las tablas siguientes se explican las diferencias entre las nuevas funciones auxiliares de WPAD y las funciones auxiliares de WPAD heredadas. Las nuevas funciones se marcan con un asterisco.



<table>
<thead>
<tr class="header">
<th>Functions</th>
<th>Entrada</th>
<th>Output</th>
<th>Motivo del cambio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>dnsResolve</td>
<td>Host</td>
<td>Dirección IPv4</td>
<td rowspan="2">La función ex devolverá una lista de IPv6/IPv4. Necesario porque las direcciones IPv6 o IPv4 pueden tener varias direcciones de unidifusión para una sola interfaz. $ {REMOVE} $<br />
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
<th>Functions</th>
<th>Entrada</th>
<th>Output</th>
<th>Motivo del cambio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>isResolveable</td>
<td>Host IPv4</td>
<td>TRUE/FALSE</td>
<td rowspan="2">La función ex devolverá TRUE si un host se puede resolver en una dirección IPv6 o IPv4. La función heredada solo devuelve TRUE si el host se resuelve en una dirección IPv4. $ {REMOVE} $<br />
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
<th>Functions</th>
<th>Entrada</th>
<th>Output</th>
<th>Motivo del cambio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>myIPAddress</td>
<td>ninguno</td>
<td>Dirección IPv4</td>
<td rowspan="2">La función ex devolverá una lista de IPv6/IPv4. Necesario porque las direcciones IPv6 o IPv4 pueden tener varias direcciones de unidifusión para una sola interfaz $ {REMOVE} $<br />
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
<th>Functions</th>
<th>Entrada</th>
<th>Output</th>
<th>Motivo del cambio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>isInNet</td>
<td>Host, patrón de dirección IP separada por puntos, máscara de dirección IP</td>
<td>TRUE/FALSE</td>
<td rowspan="2">Proporcione una manera independiente de la versión de IP para buscar si una dirección IP se encuentra en una subred determinada. Además, la notación de máscara de IPv4 está en desuso. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>isInNetEx*</td>
<td>Prefijo IP de dirección IP</td>
<td>TRUE/FALSE</td>

</tr>
</tbody>
</table>



 



| Functions           | Entrada                       | Output                             | Motivo del cambio                                                                                                                           |
|---------------------|-----------------------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| sortIPAddressList\* | Lista de direcciones IPv6/IPv4 | Lista ordenada de direcciones IPv6/IPv4 | No hay ninguna función heredada equivalente porque las funciones heredadas solo devolvían una única dirección IPv4, por lo que no era necesario ordenar. |



 



| Functions          | Entrada | Output                     | Motivo del cambio                                                                                                                                                                                                           |
|--------------------|-------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| getClientVersion\* | ninguno  | Número de versión del motor WPAD | Actualmente, esta función devuelve la versión 1,0. Hemos agregado esta función para permitir que los administradores de ti actualicen su WPAD para trabajar con versiones diferentes del motor WPAD sin causar interrupciones en su implementación existente. |



 

> [!Note]  
> Esta funcionalidad requiere Windows Internet Explorer 7 o posterior.

 

 

 



