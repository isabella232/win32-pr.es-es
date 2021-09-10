---
title: MachineLaunchRestriction
description: Establece la directiva de restricción de todo el equipo para el inicio y la activación de componentes.
ms.assetid: 274e3d08-1f38-4179-b7e7-b218d6e184ee
keywords:
- Valor del Registro MachineLaunchRestriction COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14dfcfe5535871c6b5b0fe310c94b920c522f05a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369668"
---
# <a name="machinelaunchrestriction"></a>MachineLaunchRestriction

Establece la directiva de restricción de todo el equipo para el inicio y la activación de componentes.

> [!Caution]  
> El cambio de este valor afectará a todas las aplicaciones de servidor COM y podría impedir que funcionen correctamente. Si hay aplicaciones de servidor COM que tienen restricciones menos estrictas que las restricciones de todo el equipo, la reducción de las restricciones de todo el equipo puede exponer estas aplicaciones al acceso no deseado. Por el contrario, si aumenta las restricciones de todo el equipo, es posible que algunas aplicaciones de servidor COM ya no sean accesibles mediante la llamada a aplicaciones.

 

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineLaunchRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG BINARY.**

Las entidades de seguridad a las que no se les conceden permisos aquí no pueden obtenerlos incluso si los concede el valor del Registro [DefaultAccessPermission](defaultaccesspermission.md) o la [**función CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

De forma predeterminada, los administradores pueden obtener permisos de inicio y activación locales y remotos, y los miembros del grupo Todos pueden obtener permisos de activación e inicio locales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer la seguridad para las aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




