---
title: MachineAccessRestriction
description: Establece la directiva de restricción de todo el equipo para el acceso a componentes.
ms.assetid: aeb37e49-6425-4058-968e-f9d00acf4fc2
keywords:
- Valor com del Registro MachineAccessRestriction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d99e747b8a38dbb41cb8a6a8adc0935d3f9fa8
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369528"
---
# <a name="machineaccessrestriction"></a>MachineAccessRestriction

Establece la directiva de restricción de todo el equipo para el acceso a componentes.

> [!Caution]  
> El cambio de este valor afectará a todas las aplicaciones de servidor COM y podría impedir que funcionen correctamente. Si hay aplicaciones de servidor COM que tienen restricciones menos estrictas que las restricciones de todo el equipo, la reducción de las restricciones de todo el equipo puede exponer estas aplicaciones al acceso no deseado. Por el contrario, si aumenta las restricciones de todo el equipo, es posible que algunas aplicaciones de servidor COM ya no sean accesibles mediante una llamada a las aplicaciones.

 

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineAccessRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG BINARY.**

Las entidades de seguridad a las que no se les han concedido permisos aquí no pueden obtenerlos incluso si los concede el valor del Registro [DefaultAccessPermission](defaultaccesspermission.md) o la [**función CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

De forma predeterminada, los miembros del grupo Todos pueden obtener permisos de acceso local y remoto, y los usuarios anónimos pueden obtener permisos de acceso local.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la seguridad para aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




