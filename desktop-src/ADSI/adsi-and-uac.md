---
title: ADSI y control de cuentas de usuario
description: Windows y Windows Server tienen control de cuentas de usuario, que tiene ramificaciones para aplicaciones que usan interfaces de servicio de Active Directory (ADSI).
ms.assetid: 0b286252-8c24-4a18-9dc6-063ca158a8ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36fc88169a8710228a3bf70283aaccd4b4ac42e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078364"
---
# <a name="adsi-and-user-account-control"></a>ADSI y control de cuentas de usuario

Windows y Windows Server tienen [control de cuentas de usuario](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), que tiene ramificaciones para aplicaciones que usan [interfaces de servicio de Active Directory](active-directory-service-interfaces-adsi.md) (ADSI). En concreto, estas interfaces se diseñaron para ejecutarse mediante una cuenta de usuario con privilegios de administrador en el equipo local.

**Problema**

Cada vez que una aplicación se conecta al directorio e intenta crear un objeto ADSI, se comprueba si hay cambios en el [esquema de Active Directory](/windows/desktop/ADSchema/active-directory-schema) . Si ha cambiado desde la última conexión, el esquema se descarga y se almacena en una caché del equipo local. En versiones de Windows anteriores a Windows Vista, la ubicación predeterminada de esta caché era

`%systemroot%\SchCache\`

Sin embargo, las aplicaciones que se ejecutan con cuentas estándar (es decir, sin administrador) no tendrán acceso a este directorio y, por lo tanto, las aplicaciones que usen interfaces ADSI que se ejecuten en este modo descargarán el esquema en cada conexión, lo que afectará al rendimiento y al rendimiento.

**Soluciones**

*Usuario único* : para resolver este problema, hay nuevas claves de control del registro del proveedor ADSI que determinan las ubicaciones del registro y las ubicaciones de los archivos para los objetos de [esquema Active Directory](/windows/desktop/ADSchema/active-directory-schema) almacenados en caché. Si la clave del registro

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

está establecido en 0 (cero), cada usuario tendrá una ubicación de almacenamiento diferente para ADSI; las claves del registro se almacenarán en

`HKEY_CURRENT_USER\Software\Microsoft\ADs\Providers\LDAP\`

y los archivos de caché se almacenarán en

`%LOCALAPPDATA%\Microsoft\Windows\SchCache`

Esta configuración es la predeterminada en los equipos que ejecutan Windows Server 2008 o Windows Vista.

*Multiusuario* : Si está ejecutando aplicaciones ADSI en un equipo con muchas cuentas de usuario (por ejemplo, un servidor Web), es preferible no tener muchas copias de la memoria caché del [esquema de Active Directory](/windows/desktop/ADSchema/active-directory-schema) con grandes cantidades de espacio en disco. Establecimiento de la clave del registro

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

a 1 (uno) revertirá ADSI al comportamiento anterior; todos los objetos de [esquema de Active Directory](/windows/desktop/ADSchema/active-directory-schema) se almacenarán en sus ubicaciones anteriores; la clave del registro estará en

`HKEY_LOCAL_MACHINE\Software\Microsoft\ADs\Providers\LDAP`

y el archivo de caché estará en

`%systemroot%\SchCache`

En este caso, las cuentas de administrador deben ejecutar la aplicación, lo que hará que el archivo de esquema se almacene en caché en la ubicación global para un uso futuro por parte de los usuarios con menos privilegios.

 

 