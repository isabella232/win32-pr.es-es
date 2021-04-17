---
description: Funciones para establecer y recuperar un descriptor de seguridad de objetos.
ms.assetid: 22bf0d6b-3ec6-4c28-ace4-49e48714f4bf
title: 'Funciones de descriptor de seguridad de bajo nivel '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72406dc2481e4671d8d535327f416a2d003c3a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669918"
---
# <a name="low-level-security-descriptor-functions"></a>Funciones de descriptor de seguridad de bajo nivel 

Hay varios pares de funciones de bajo nivel para establecer y recuperar el [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly)de un objeto. Cada uno de estos pares solo funciona con un conjunto limitado de objetos de Windows. Por ejemplo, un par funciona con objetos de archivo y otro funciona con claves del registro. En la tabla siguiente se muestran las funciones de bajo nivel que se usan con los distintos tipos de objetos protegibles.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de objeto</th>
<th>Funciones de bajo nivel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/FileIO/file-security-and-access-rights">Archivos</a></li>
<li><a href="/windows/desktop/FileIO/file-security-and-access-rights">Directorios</a></li>
<li>Buzo</li>
<li><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Canalizaciones con nombre</a></li>
</ul></td>
<td>Use las funciones <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>GetFileSecurity</strong></a> y <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>SetFileSecurity</strong></a> . Estas funciones utilizan cadenas de caracteres para identificar el objeto protegible, en lugar de utilizar los identificadores.</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Procesos</a></li>
<li><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Subprocesos</a></li>
<li><a href="access-rights-for-access-token-objects.md">Tokens de acceso</a></li>
<li><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">Objetos de asignación de archivos</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Semáforos</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Eventos</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutexes</a> (Clases Mutex)</li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Temporizadores que esperan</a></li>
</ul></td>
<td>Use las funciones <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>GetKernelObjectSecurity</strong></a> y <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>SetKernelObjectSecurity</strong></a> .</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Estaciones de ventana</a></li>
<li><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Escritorios</a></li>
</ul></td>
<td>Use las funciones <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>GetUserObjectSecurity</strong></a> y <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>SetUserObjectSecurity</strong></a> .</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Claves del Registro</a></li>
</ul></td>
<td>Use las funciones <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>RegGetKeySecurity</strong></a> y <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>RegSetKeySecurity</strong></a> .</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/Services/service-security-and-access-rights">Objetos de servicio de Windows</a></li>
</ul></td>
<td>Use las funciones <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> y <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> .</td>
</tr>
<tr class="even">
<td><ul>
<li>Objetos de impresora</li>
</ul></td>
<td>Use la estructura <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> con las funciones <a href="/windows/desktop/printdocs/getprinter"><strong>GetPrinter</strong></a> y <a href="/windows/desktop/printdocs/setprinter"><strong>SetPrinter</strong></a> .</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Recursos compartidos de red</a></li>
</ul></td>
<td>Use el nivel 502 con las funciones <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> y <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> .</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="acl-based-access-control.md">Objetos privados (objetos privados para la aplicación de creación)</a></li>
</ul></td>
<td>Use las funciones <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>CreatePrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> y <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> .</td>
</tr>
</tbody>
</table>



 

 

 
