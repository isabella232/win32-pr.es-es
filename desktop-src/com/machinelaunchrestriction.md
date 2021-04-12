---
title: MachineLaunchRestriction
description: Establece la Directiva de restricción para todo el equipo para el inicio y activación de componentes.
ms.assetid: 274e3d08-1f38-4179-b7e7-b218d6e184ee
keywords:
- Valor del registro MachineLaunchRestriction COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14dfcfe5535871c6b5b0fe310c94b920c522f05a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269279"
---
# <a name="machinelaunchrestriction"></a>MachineLaunchRestriction

Establece la Directiva de restricción para todo el equipo para el inicio y activación de componentes.

> [!Caution]  
> Cambiar este valor afectará a todas las aplicaciones de servidor COM y puede impedir que funcionen correctamente. Si hay aplicaciones de servidor COM con restricciones que son menos rigurosas que las restricciones en todo el equipo, reducir las restricciones en todo el equipo puede exponer estas aplicaciones al acceso no deseado. Por el contrario, si aumenta las restricciones en todo el equipo, es posible que algunas aplicaciones de servidor COM dejen de ser accesibles mediante la llamada a aplicaciones.

 

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineLaunchRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a>Observaciones

Se trata de un valor **\_ binario de registro** .

Las entidades de seguridad a las que no se conceden permisos aquí no pueden obtenerlas aunque el valor del registro [DefaultAccessPermission](defaultaccesspermission.md) o la función [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) concedan los permisos.

De forma predeterminada, los administradores pueden obtener permisos de inicio y activación locales y remotos, y los miembros del grupo todos pueden obtener permisos de inicio y activación locales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer la seguridad de las aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




