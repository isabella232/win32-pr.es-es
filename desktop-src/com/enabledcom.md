---
title: EnableDCOM
description: Controla la activación global y las directivas de llamada de la máquina. Solo los administradores y el sistema tienen acceso total a esta parte del registro. El resto de usuarios tienen acceso de solo lectura.
ms.assetid: 8533270d-f1b0-42b9-a50d-b05a0dfeee22
keywords:
- Valor del registro EnableDCOM COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42cc95b24522e87e4b64f6feefc5c6c56ad5341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418546"
---
# <a name="enabledcom"></a>EnableDCOM

Controla la activación global y las directivas de llamada de la máquina. Solo los administradores y el sistema tienen acceso total a esta parte del registro. El resto de usuarios tienen acceso de solo lectura.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   EnableDCOM = value
```

## <a name="remarks"></a>Observaciones

Este es un valor de **reg \_ SZ** .



| Value    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| N (o n) | Ningún cliente remoto puede iniciar servidores o conectarse a objetos de este equipo. Los clientes locales no pueden tener acceso a servidores DCOM remotos. se bloquea todo el tráfico DCOM. El inicio local del código de clase y la conexión a objetos se permiten por clase según el valor y los permisos de acceso del valor del registro [**LaunchPermission**](launchpermission.md) de la clase y el valor del registro [**DefaultLaunchPermission**](defaultlaunchpermission.md) global. |
| Y (o y) | El inicio de servidores y la conexión a objetos por parte de clientes remotos se permite por clase según el valor y los permisos de acceso del valor del registro [**LaunchPermission**](launchpermission.md) de la clase y el valor del registro [**DefaultLaunchPermission**](defaultlaunchpermission.md) global.                                                                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[**LaunchPermission**](launchpermission.md)
</dt> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 




