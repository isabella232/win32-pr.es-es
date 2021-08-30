---
title: MachineAccessRestriction
description: Establece la directiva de restricción de todo el equipo para el acceso a componentes.
ms.assetid: aeb37e49-6425-4058-968e-f9d00acf4fc2
keywords:
- Valor com del Registro MachineAccessRestriction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce78aa749618b93dfe8cbe62fad5ec0e51504f4bad0067b17628ac0226c24b2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896201"
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

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ REG BINARY.**

Las entidades de seguridad a las que no se les han concedido permisos aquí no pueden obtenerlos incluso si los concede el valor del Registro [DefaultAccessPermission](defaultaccesspermission.md) o la [**función CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

De forma predeterminada, los miembros del grupo Todos pueden obtener permisos de acceso local y remoto, y los usuarios anónimos pueden obtener permisos de acceso local.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la seguridad para aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




