---
title: MachineAccessRestriction
description: Establece la Directiva de restricción para todo el equipo para el acceso a componentes.
ms.assetid: aeb37e49-6425-4058-968e-f9d00acf4fc2
keywords:
- Valor del registro MachineAccessRestriction COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d99e747b8a38dbb41cb8a6a8adc0935d3f9fa8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695420"
---
# <a name="machineaccessrestriction"></a>MachineAccessRestriction

Establece la Directiva de restricción para todo el equipo para el acceso a componentes.

> [!Caution]  
> Cambiar este valor afectará a todas las aplicaciones de servidor COM y puede impedir que funcionen correctamente. Si hay aplicaciones de servidor COM con restricciones que son menos rigurosas que las restricciones en todo el equipo, reducir las restricciones en todo el equipo puede exponer estas aplicaciones al acceso no deseado. Por el contrario, si aumenta las restricciones en todo el equipo, es posible que algunas aplicaciones de servidor COM dejen de ser accesibles mediante la llamada a aplicaciones.

 

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineAccessRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a>Observaciones

Se trata de un valor **\_ binario de registro** .

Las entidades de seguridad a las que no se conceden permisos aquí no pueden obtenerlas aunque el valor del registro [DefaultAccessPermission](defaultaccesspermission.md) o la función [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) concedan los permisos.

De forma predeterminada, los miembros del grupo todos pueden obtener permisos de acceso local y remoto, y los usuarios anónimos pueden obtener permisos de acceso local.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer la seguridad de las aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




