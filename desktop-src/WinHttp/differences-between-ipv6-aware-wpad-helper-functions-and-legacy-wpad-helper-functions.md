---
title: IPv6-Aware y funciones auxiliares de WPAD heredadas
description: Diferencias entre las IPv6-Aware auxiliares de WPAD y las funciones auxiliares WPAD heredadas
ms.assetid: ea4b1c0d-ce02-477b-85c8-44e1beef90c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511b7f04aa0a2abe04b99562c15aeb3a53bdaadf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474538"
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
<td>administrador de flujos de trabajo</td>
<td>Dirección IPv4</td>
<td rowspan="2">La función ex devolverá una lista de IPv6/IPv4. Necesario, ya que las direcciones IPv6 o IPv4 pueden tener varias direcciones de unidifusión para una sola interfaz.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>dnsResolveEx*</td>
<td>administrador de flujos de trabajo</td>
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



 



| Functions           | Entrada                       | Output                             | Motivo del cambio                                                                                                                           |
|---------------------|-----------------------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| sortIPAddressList\* | Lista de direcciones IPv6/IPv4 | Lista ordenada de direcciones IPv6/IPv4 | No hay ninguna función heredada equivalente porque las funciones heredadas solo devolvieron una única dirección IPv4, por lo que no era necesario ordenar . |



 



| Functions          | Entrada | Output                     | Motivo del cambio                                                                                                                                                                                                           |
|--------------------|-------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| getClientVersion\* | ninguno  | Número de versión del motor WPAD | Actualmente, esta función devuelve la versión 1.0. Hemos agregado esta función para permitir que los administradores de TI actualicen su WPAD para que funcione con distintas versiones del motor de WPAD sin provocar interrupciones en su implementación existente. |



 

> [!Note]  
> Esta funcionalidad requiere Windows Internet Explorer 7 o superior.

 

 

 



