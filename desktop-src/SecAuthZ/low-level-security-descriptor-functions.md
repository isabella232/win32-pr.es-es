---
description: Funciones para establecer y recuperar un descriptor de seguridad de objetos.
ms.assetid: 22bf0d6b-3ec6-4c28-ace4-49e48714f4bf
title: 'Funciones de descriptor de seguridad de bajo nivel '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d77c717b554a670eebed4e7df67760fe7e08eb8a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069104"
---
# <a name="low-level-security-descriptor-functions"></a>Funciones de descriptor de seguridad de bajo nivel 

Hay varios pares de funciones de bajo nivel para establecer y recuperar el descriptor de seguridad [*de un objeto*](/windows/desktop/SecGloss/s-gly). Cada uno de estos pares solo funciona con un conjunto limitado de Windows objetos. Por ejemplo, un par funciona con objetos de archivo y otro funciona con claves del Registro. En la tabla siguiente se muestran las funciones de bajo nivel que se usarán con los distintos tipos de objetos protegibles.




| Tipo de objeto | Funciones de bajo nivel | 
|-------------|---------------------|
| <ul><li><a href="/windows/desktop/FileIO/file-security-and-access-rights">Archivos</a></li><li><a href="/windows/desktop/FileIO/file-security-and-access-rights">Directorios</a></li><li>Mailslots</li><li><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Canalizaciones</a></li></ul> | Use las <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>funciones GetFileSecurity</strong></a> <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>y SetFileSecurity.</strong></a> Estas funciones usan cadenas de caracteres para identificar el objeto protegible, en lugar de usar identificadores. | 
| <ul><li><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Procesos</a></li><li><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Subprocesos</a></li><li><a href="access-rights-for-access-token-objects.md">Tokens de acceso</a></li><li><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">Objetos de asignación de archivos</a></li><li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Semáforos</a></li><li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Eventos</a></li><li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutexes</a> (Clases Mutex)</li><li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Temporizadores que se pueden esperar</a></li></ul> | Use las <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>funciones GetKernelObjectSecurity</strong></a> <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>y SetKernelObjectSecurity.</strong></a> | 
| <ul><li><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Estaciones de ventana</a></li><li><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Escritorios</a></li></ul> | Use las <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>funciones GetUserObjectSecurity</strong></a> <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>y SetUserObjectSecurity.</strong></a> | 
| <ul><li><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Claves del Registro</a></li></ul> | Use las <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>funciones RegGetKeySecurity</strong></a> <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>y RegSetKeySecurity.</strong></a> | 
| <ul><li><a href="/windows/desktop/Services/service-security-and-access-rights">Windows de servicio</a></li></ul> | Use las <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>funciones QueryServiceObjectSecurity</strong></a> <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>y SetServiceObjectSecurity.</strong></a> | 
| <ul><li>Objetos de impresora</li></ul> | Use la <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> con las <a href="/windows/desktop/printdocs/getprinter"><strong>funciones GetPrinter</strong></a> y <a href="/windows/desktop/printdocs/setprinter"><strong>SetPrinter.</strong></a> | 
| <ul><li><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Recursos compartidos de red</a></li></ul> | Use el nivel 502 con las <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>funciones NetShareGetInfo</strong></a> <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>y NetShareSetInfo.</strong></a> | 
| <ul><li><a href="acl-based-access-control.md">Objetos privados (objetos privados para la aplicación de creación)</a></li></ul> | Use las <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>funciones CreatePrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity,</strong></a> <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>y SetPrivateObjectSecurity.</strong></a> | 




 

 

 
