---
title: InvalidSecurityDescriptorLoggingLevel
description: Establece el nivel de detalle de las entradas del registro de eventos acerca de los descriptores de seguridad no válidos para el inicio y los permisos de acceso de los componentes.
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- Valor del registro InvalidSecurityDescriptorLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ac333a7cb8b54f383f93a71131cbb0a9314466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356673"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a>InvalidSecurityDescriptorLoggingLevel

Establece el nivel de detalle de las entradas del registro de eventos acerca de los descriptores de seguridad no válidos para el inicio y los permisos de acceso de los componentes.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **Registro \_ DWORD** .



| Value | Descripción                                                                                                                                                                    |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Registre siempre los errores cuando COM encuentre un descriptor de seguridad no válido. Este es el valor predeterminado.                                                                                  |
| 2     | Nunca Registre errores cuando COM encuentre un descriptor de seguridad no válido. No se recomienda deshabilitar el registro de eventos, ya que puede dificultar el diagnóstico de problemas. |



 

Si establece los descriptores de seguridad de permisos de inicio y acceso (normalmente denominados ACL) directamente, es posible crear un descriptor de seguridad cuyo significado no se pueda interpretar de forma no ambigua. COM realiza una entrada en el registro de eventos cuando encuentra un descriptor de seguridad no válido.

Tenga en cuenta que [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) y [**CallFailureLoggingLevel**](callfailurelogginglevel.md) no tienen ningún control sobre el registro de errores de descriptor de seguridad no válidos. Use **InvalidSecurityDescriptorLoggingLevel** para tener un control total sobre esta funcionalidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer la seguridad de las aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




