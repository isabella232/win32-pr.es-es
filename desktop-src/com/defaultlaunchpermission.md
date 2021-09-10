---
title: DefaultLaunchPermission
description: Define la Access Control lista de entidades de seguridad (ACL) de las entidades de seguridad que pueden iniciar clases que no especifican su propia ACL a través del valor del Registro LaunchPermission.
ms.assetid: 23ca87fc-7829-46a9-9fc3-2cd7f677bbff
keywords:
- Valor del Registro DEFAULTLaunchPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599a0993a4a1238e57e357f428f7046331412cc0
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369619"
---
# <a name="defaultlaunchpermission"></a>DefaultLaunchPermission

Define la Access Control lista de entidades de seguridad (ACL) de las entidades de seguridad que pueden iniciar clases que no especifican su propia ACL a través del valor del Registro [**LaunchPermission.**](launchpermission.md)

> [!Caution]  
> No se recomienda cambiar este valor, ya que esto afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podrían impedir que funcionen correctamente. Si va a cambiar este valor para que afecte a la configuración de seguridad de una aplicación COM determinada, en su lugar debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM concreta. Para obtener más información sobre cómo establecer la seguridad de todo el proceso, vea [Establecer la seguridad de todo el proceso.](setting-processwide-security.md)

 

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultLaunchPermission = ACL
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG BINARY.**

Los permisos de acceso predeterminados son los siguientes:

-   Administradores: permitir el inicio
-   SISTEMA: permitir el inicio
-   INTERACTIVO: permitir el inicio

Si el [**valor LaunchPermission**](launchpermission.md) se establece para un servidor, tiene prioridad sobre **el valor DefaultLaunchPermission.** Al recibir una solicitud local o remota para iniciar un servidor cuya clave [**AppID**](appid-key.md) no tiene ningún valor **LaunchPermission** propio, la ACL descrita por este valor se comprueba al suplantar al cliente y su éxito permite o no permite el inicio del código de clase.

Este valor proporciona un nivel simple de administración centralizada del acceso de inicio predeterminado a las clases no administradoras en un equipo. Por ejemplo, un administrador podría usar la herramienta DCOMCNFG para configurar el sistema para permitir el acceso de solo lectura a los usuarios avanzados. Por lo tanto, OLE restringiría las solicitudes para iniciar código de clase a los miembros del grupo Usuarios avanzados. Posteriormente, un administrador podría configurar permisos de inicio para clases individuales con el objeto de conceder la capacidad de iniciar código de clase a otros grupos o usuarios individuales según sea necesario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**LaunchPermission**](launchpermission.md)
</dt> <dt>

[Registro de servidores COM](registering-com-servers.md)
</dt> <dt>

[Establecer la seguridad de todo el proceso](setting-processwide-security.md)
</dt> </dl>

 

 




