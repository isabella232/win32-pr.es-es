---
title: ADSI y control de cuentas de usuario
description: Windows y Windows Server tienen control de cuentas de usuario, que tiene ramificaciones para las aplicaciones que usan Active Directory Service Interfaces (ADSI).
ms.assetid: 0b286252-8c24-4a18-9dc6-063ca158a8ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1d0163348356f83b64522c9b05607d0d094ceb8f0ad530a798e546021433ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023973"
---
# <a name="adsi-and-user-account-control"></a>ADSI y control de cuentas de usuario

Windows y Windows Server tienen control de cuentas de [usuario,](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10))que tiene ramificaciones para las aplicaciones que [usan Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI). En concreto, estas interfaces se diseñaron para que las ejecutara una cuenta de usuario con privilegios de administrador en el equipo local.

**Problema**

Cada vez que una aplicación se conecta al directorio e [](/windows/desktop/ADSchema/active-directory-schema) intenta crear un objeto ADSI, se comprueba si el esquema Active Directory cambios. Si ha cambiado desde la última conexión, el esquema se descarga y se almacena en una memoria caché en el equipo local. En versiones de Windows anteriores a Windows Vista, la ubicación predeterminada de esta caché era

`%systemroot%\SchCache\`

Sin embargo, las aplicaciones que se ejecutan de forma estándar (es decir, las cuentas que no son de administrador) no tendrán acceso a este directorio y, por consiguiente, las aplicaciones que usan interfaces ADSI que se ejecutan en este modo descargarán el esquema en cada conexión, lo que afectará al rendimiento y al rendimiento.

**Soluciones**

*Usuario único:* para resolver este problema, hay nuevas claves de control del Registro del proveedor ADSI que determinan las ubicaciones del Registro y las ubicaciones de los archivos para los objetos Active Directory esquema almacenados [en](/windows/desktop/ADSchema/active-directory-schema) caché. Si la clave del Registro

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

se establece en 0 (cero), cada usuario tendrá una ubicación de almacenamiento diferente para ADSI; las claves del Registro se almacenarán en

`HKEY_CURRENT_USER\Software\Microsoft\ADs\Providers\LDAP\`

y los archivos de caché se almacenarán en

`%LOCALAPPDATA%\Microsoft\Windows\SchCache`

Esta configuración es la configuración predeterminada en equipos que ejecutan Windows Server 2008 o Windows Vista.

Varios *usuarios:* si está ejecutando aplicaciones ADSI en un equipo con muchas cuentas de usuario (por ejemplo, un servidor web), es preferible no tener muchas copias de la caché de esquema de [Active Directory](/windows/desktop/ADSchema/active-directory-schema) con una gran cantidad de espacio en disco. Establecimiento de la clave del Registro

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

a 1 (uno) revertirá ADSI al comportamiento anterior; todos [Active Directory de esquema](/windows/desktop/ADSchema/active-directory-schema) se almacenarán en sus ubicaciones anteriores; la clave del Registro estará en

`HKEY_LOCAL_MACHINE\Software\Microsoft\ADs\Providers\LDAP`

y el archivo de caché estará en

`%systemroot%\SchCache`

En este caso, las cuentas de administrador deben ejecutar la aplicación, lo que hará que el archivo de esquema se almacene en caché en la ubicación global para que los usuarios con menos privilegios puedan usarlo en el futuro.

 

 