---
title: Funciones de Windows Defender
description: Funciones a las que llaman las aplicaciones para solicitar exámenes, actualizaciones de firmas o información de Windows Defender.
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225530c9d0c2970930d0bc38e23f7907f588e89e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420185"
---
# <a name="windows-defender-functions"></a>Funciones de Windows Defender

Funciones a las que llaman las aplicaciones para solicitar exámenes, actualizaciones de firmas o información de Windows Defender.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Función</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a></td>
<td>Devuelve un mensaje de error con formato basado en un código de error.<br/></td>
</tr>
<tr class="even">
<td><a href="mpfreememory.md"><strong>MpFreeMemory</strong></a></td>
<td>Libera memoria para el administrador de protección contra malware de.<br/></td>
</tr>
<tr class="odd">
<td><a href="mphandleclose.md"><strong>MpHandleClose</strong></a></td>
<td>Cierra el identificador devuelto por <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>, <a href="mpscanstart.md"><strong>MpScanStart</strong></a>, <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>o <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a></td>
<td>Establece una conexión con el administrador de protección contra malware en el equipo local.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a></td>
<td><strong>No compatible.</strong> Devuelve información de estado sobre los distintos componentes del administrador de protección contra malware de.<br/></td>
</tr>
<tr class="even">
<td><a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a></td>
<td>Devuelve información de estado sobre los distintos componentes del administrador de protección contra malware de.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a></td>
<td>Devuelve información de versión sobre varios componentes del administrador de protección contra malware de.<br/></td>
</tr>
<tr class="even">
<td><a href="mpscancontrol.md"><strong>MpScanControl</strong></a></td>
<td>Permite el control de un examen que se inició de forma asincrónica a través de <a href="mpscanstart.md"><strong>MpScanStart</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpscanstart.md"><strong>MpScanStart</strong></a></td>
<td>Inicia una operación de digitalización.<br/></td>
</tr>
<tr class="even">
<td><a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a></td>
<td>Devuelve información sobre la siguiente amenaza en la lista de enumeración. Se puede llamar a esta función varias veces hasta que se complete la enumeración de todas las amenazas.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a></td>
<td>Devuelve un identificador de enumeración con el fin de recuperar las amenazas. Esta función se puede usar para abrir amenazas detectadas por un análisis específico, todas las amenazas activas del sistema, el historial de la desinfección de amenazas o todas las amenazas presentes en la base de datos de firmas.<br/></td>
</tr>
<tr class="even">
<td><a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a></td>
<td>Se usa para consultar información estática (como gravedad y categoría) o localizada (como descripción de la categoría y consejos) sobre una amenaza determinada.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a></td>
<td>Permite el control de una operación de actualización de firmas que se inició de forma asincrónica a través de <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a></td>
<td>Inicia una operación de actualización de firma.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a></td>
<td>Cambia el estado de Windows Defender a activado o desactivado.<br/>
<blockquote>
[!Note]<br />
A partir de Windows 10, versión 1607 y Windows Server 2016, la función <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> siempre devuelve <strong>E_NOTIMPL</strong>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a></td>
<td>Devuelve el estado actual de Windows Defender.<br/></td>
</tr>
</tbody>
</table>



 

 

 





