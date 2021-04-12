---
description: DDE de red proporciona funciones que permiten eliminar un recurso compartido, obtener o establecer información de recursos compartidos, o enumerar recursos compartidos.
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: Administrar recursos compartidos DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcc8c7d2eb3983aaabd054b9b729daea176bb10
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104361789"
---
# <a name="managing-dde-shares"></a>Administrar recursos compartidos DDE

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

DDE de red proporciona funciones que permiten eliminar un recurso compartido, obtener o establecer información de recursos compartidos, o enumerar recursos compartidos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tarea</th>
<th>Procedimiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Eliminar un recurso compartido DDE</td>
<td>Utilice la función <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> .</td>
</tr>
<tr class="even">
<td>Obtener información de recursos compartidos DDE</td>
<td>Utilice la función <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> .</td>
</tr>
<tr class="odd">
<td>Establecer información de recursos compartidos DDE</td>
<td>Utilice la función <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> .</td>
</tr>
<tr class="even">
<td>Enumerar recursos compartidos DDE</td>
<td>Utilice la función <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> . También puede enumerar los recursos compartidos DDE de confianza mediante la función <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td>Enumerar usuarios conectados</td>
<td>Utilice la función <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> .</td>
</tr>
<tr class="even">
<td>Cambiar el nombre del recurso compartido DDE</td>
<td>Elimine el recurso compartido anterior y cree un nuevo recurso compartido.
<ol>
<li>Recupere la información del recurso compartido mediante <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</li>
<li>Quite el recurso compartido mediante <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>.</li>
<li>Cambie el miembro <strong>lpszShareName</strong> de la estructura <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> devuelta por <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</li>
<li>Pase la estructura <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> modificada a <a href="nddeshareadd.md"><strong>NDdeShareAdd</strong></a>.</li>
</ol></td>
</tr>
</tbody>
</table>



 

 

