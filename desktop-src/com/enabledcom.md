---
title: EnableDCOM
description: Controla las directivas globales de activación y llamada de la máquina. Solo los administradores y el sistema tienen acceso total a esta parte del registro. Todos los demás usuarios tienen acceso de solo lectura.
ms.assetid: 8533270d-f1b0-42b9-a50d-b05a0dfeee22
keywords:
- Valor del Registro ENABLEDCOM COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42cc95b24522e87e4b64f6feefc5c6c56ad5341
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369663"
---
# <a name="enabledcom"></a>EnableDCOM

Controla las directivas globales de activación y llamada de la máquina. Solo los administradores y el sistema tienen acceso total a esta parte del registro. Todos los demás usuarios tienen acceso de solo lectura.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   EnableDCOM = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG SZ.**



| Value    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| N (o n) | Ningún cliente remoto puede iniciar servidores ni conectarse a objetos en este equipo. Los clientes locales no pueden acceder a servidores DCOM remotos; se bloquea todo el tráfico DCOM. El inicio local del código de clase y la conexión a objetos se permiten por clase según el valor y los permisos de acceso del valor del Registro [**LaunchPermission**](launchpermission.md) de la clase y del valor global del Registro [**DefaultLaunchPermission.**](defaultlaunchpermission.md) |
| Y (o y) | El inicio de servidores y la conexión a objetos por parte de clientes remotos se permite por clase según el valor y los permisos de acceso del valor del Registro [**LaunchPermission**](launchpermission.md) de la clase y el valor global del Registro [**DefaultLaunchPermission.**](defaultlaunchpermission.md)                                                                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[**LaunchPermission**](launchpermission.md)
</dt> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 




