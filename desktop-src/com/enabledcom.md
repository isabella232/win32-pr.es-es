---
title: EnableDCOM
description: Controla la activación global y las directivas de llamada de la máquina. Solo los administradores y el sistema tienen acceso total a esta parte del registro. Todos los demás usuarios tienen acceso de solo lectura.
ms.assetid: 8533270d-f1b0-42b9-a50d-b05a0dfeee22
keywords:
- Valor del Registro EnableDCOM COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74aea79cf600aad4407b96b5c4a10e8f44633a1c928f8b7e376c192b108cb75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793614"
---
# <a name="enabledcom"></a>EnableDCOM

Controla la activación global y las directivas de llamada de la máquina. Solo los administradores y el sistema tienen acceso total a esta parte del registro. Todos los demás usuarios tienen acceso de solo lectura.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   EnableDCOM = value
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ SZ reg.**



| Value    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| N (o n) | Ningún cliente remoto puede iniciar servidores ni conectarse a objetos en este equipo. Los clientes locales no pueden acceder a servidores DCOM remotos; se bloquea todo el tráfico DCOM. El inicio local del código de clase y la conexión a objetos se permiten por clase según el valor y los permisos de acceso del valor del registro [**LaunchPermission**](launchpermission.md) de la clase y del valor global del Registro [**DefaultLaunchPermission.**](defaultlaunchpermission.md) |
| Y (o y) | El inicio de servidores y la conexión a objetos por parte de clientes remotos se permite por clase según el valor y los permisos de acceso del valor del Registro [**LaunchPermission**](launchpermission.md) de la clase y del valor global del Registro [**DefaultLaunchPermission.**](defaultlaunchpermission.md)                                                                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[**LaunchPermission**](launchpermission.md)
</dt> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 




