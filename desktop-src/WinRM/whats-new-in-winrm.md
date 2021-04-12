---
title: Novedades de WinRM 2,0
description: Hay nuevas características disponibles en Administración remota de Windows versión 2,0. (WinRM 2,0).
ms.assetid: 402c179a-6dd7-4d75-9318-bb8194b5527d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54f4a4829bffdb816854de2a3ebe98106a5a65af
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420359"
---
# <a name="whats-new-in-winrm-20"></a>Novedades de WinRM 2,0

Hay nuevas características disponibles en Administración remota de Windows versión 2,0. (WinRM 2,0)

WinRM 2,0 se incluye en Windows Server 2008 R2 y Windows 7.

También puede descargar WinRM 2,0 para Windows Server 2008 con Service Pack 2 (SP2) y Windows Vista con Service Pack 2 (SP2). Para obtener información acerca de cómo descargar WinRM 2,0, vea [KB968929](https://support.microsoft.com/kb/968929).

En la tabla siguiente se muestra la documentación de WinRM 2,0.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="client-shell-api.md">API de Shell de cliente de WinRM</a><br/></td>
<td>La interfaz de programación de aplicaciones (API) de Shell de cliente de WinRM proporciona funcionalidad para crear y administrar shells, comandos y secuencias de datos en equipos remotos. <br/></td>
</tr>
<tr class="even">
<td><a href="winrm-plugin-api.md">API de complementos de WinRM</a><br/></td>
<td>La API del complemento WinRM proporciona una funcionalidad que permite a los usuarios escribir complementos implementando ciertas API para las operaciones y los <a href="windows-remote-management-glossary.md"><em>URI de recursos</em></a> admitidos.<br/></td>
</tr>
<tr class="odd">
<td><a href="winrm-application-hosting.md">Infraestructura para la administración de servicios hospedados</a><br/></td>
<td>WinRM 2,0 introduce un marco de hospedaje. Se admiten dos modelos de hospedaje. Una se basa en Internet Information Services (IIS) y la otra es WinRM – Service based. <br/> Para obtener más información acerca de la configuración del host, vea los temas siguientes:<br/>
<ul>
<li><a href="iis-host-plug-in-configuration.md">Configuración del complemento de host de IIS</a></li>
<li><a href="wsman-service-plug-in-configuration.md">Configuración del complemento de servicio WinRM</a></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="dmtf-association-traversal.md">Detección de perfiles DMTF a través de cruce seguro de asociaciones</a><br/></td>
<td>El cruce seguro de asociaciones permite a un usuario recuperar instancias de clases de asociación mediante un mecanismo de filtrado estándar.<br/></td>
</tr>
<tr class="odd">
<td><a href="remote-shell-infrastructure-improvements.md">Mejoras en la infraestructura de shell remoto</a><br/></td>
<td>En este tema se incluye información acerca de las mejoras de la infraestructura remota para WinRM. <br/></td>
</tr>
<tr class="even">
<td><a href="multi-hop-support.md">Compatibilidad con múltiples saltos</a><br/></td>
<td>Se ha agregado funcionalidad a WinRM 2,0 que admite la delegación de credenciales de usuario en varios equipos remotos. <br/> El tema <a href="authentication-constants.md"><strong>constantes de autenticación</strong></a> se actualizó para agregar la siguiente constante: <strong>WSManFlagUseCredSsp</strong>.<br/> La siguiente API de C++ se ha agregado para proporcionar compatibilidad con múltiples saltos: <a href="/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex3"><strong>IWSManEx3</strong></a>.<br/> Se ha agregado la siguiente API de scripting para proporcionar compatibilidad con múltiples saltos: <a href="wsman-sessionflagusecredssp.md"><strong>WSMan. SessionFlagUseCredSsp</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="quotas.md">Administración de cuotas para shells remotos</a><br/></td>
<td>En este tema se incluye información sobre la configuración de cuotas para la administración remota de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="winrm-powershell-commandlets.md">Referencia administrada para comandos de PowerShell de WS-Management</a><br/></td>
<td>Los usuarios de WinRM 2,0 pueden usar cmdlets de Windows PowerShell para la administración del sistema.<br/></td>
</tr>
</tbody>
</table>



 

 

 





