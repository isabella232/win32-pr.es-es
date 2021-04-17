---
title: DefaultLaunchPermission
description: Define la lista de Access Control (ACL) de las entidades de seguridad que pueden iniciar clases que no especifican su propia ACL a través del valor del registro LaunchPermission.
ms.assetid: 23ca87fc-7829-46a9-9fc3-2cd7f677bbff
keywords:
- Valor del registro DefaultLaunchPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599a0993a4a1238e57e357f428f7046331412cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704817"
---
# <a name="defaultlaunchpermission"></a>DefaultLaunchPermission

Define la lista de Access Control (ACL) de las entidades de seguridad que pueden iniciar clases que no especifican su propia ACL a través del valor del registro [**LaunchPermission**](launchpermission.md) .

> [!Caution]  
> No se recomienda cambiar este valor, ya que esto afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podrían impedir que funcionen correctamente. Si va a cambiar este valor para que afecte a la configuración de seguridad de una aplicación COM determinada, debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM en particular. Para obtener más información sobre cómo establecer la seguridad de todo el proceso, consulte [configuración de la seguridad de todo el proceso](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultLaunchPermission = ACL
```

## <a name="remarks"></a>Observaciones

Se trata de un valor **\_ binario de registro** .

Los permisos de acceso predeterminados son los siguientes:

-   Administradores: permitir el inicio
-   SISTEMA: permitir el inicio
-   INTERACTIVO: permitir el inicio

Si el valor [**LaunchPermission**](launchpermission.md) se establece para un servidor, tiene prioridad sobre el valor **DefaultLaunchPermission** . Al recibir una solicitud local o remota para iniciar un servidor cuya clave [**AppID**](appid-key.md) no tiene su propio valor de **LAUNCHPERMISSION** , la ACL descrita por este valor se comprueba durante la suplantación del cliente y su éxito permite o impide el inicio del código de clase.

Este valor proporciona un nivel simple de administración centralizada del acceso de inicio predeterminado a las clases no administradas de otro modo en un equipo. Por ejemplo, un administrador puede usar la herramienta DCOMCNFG para configurar el sistema de modo que permita el acceso de solo lectura a los usuarios avanzados. Por lo tanto, OLE restringiría las solicitudes de inicio de código de clase a los miembros del grupo usuarios avanzados. Después, un administrador puede configurar los permisos de inicio de clases individuales para conceder la capacidad de iniciar código de clase para otros grupos o usuarios individuales según sea necesario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**LaunchPermission**](launchpermission.md)
</dt> <dt>

[Registrar servidores COM](registering-com-servers.md)
</dt> <dt>

[Establecer la seguridad de todo el proceso](setting-processwide-security.md)
</dt> </dl>

 

 




