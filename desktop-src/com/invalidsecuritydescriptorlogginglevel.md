---
title: InvalidSecurityDescriptorLoggingLevel
description: Establece el nivel de detalle de las entradas del registro de eventos sobre descriptores de seguridad no válidos para los permisos de inicio y acceso de componentes.
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- Valor del Registro COM InvalidSecurityDescriptorLoggingLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ac333a7cb8b54f383f93a71131cbb0a9314466
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369664"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a>InvalidSecurityDescriptorLoggingLevel

Establece el nivel de detalle de las entradas del registro de eventos sobre descriptores de seguridad no válidos para los permisos de inicio y acceso de componentes.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG DWORD.**



| Value | Descripción                                                                                                                                                                    |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Registra siempre errores cuando COM encuentra un descriptor de seguridad no válido. Este es el valor predeterminado.                                                                                  |
| 2     | Nunca registre errores cuando COM encuentre un descriptor de seguridad no válido. No se recomienda deshabilitar el registro de eventos, ya que puede dificultar el diagnóstico de problemas. |



 

Si establece directamente descriptores de seguridad de permisos de inicio y acceso (normalmente denominados ACL), es posible construir un descriptor de seguridad cuyo significado no se puede interpretar de forma inequívoca. COM realiza una entrada del registro de eventos cuando encuentra un descriptor de seguridad no válido.

Tenga en [**cuenta que ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) [**y CallFailureLoggingLevel**](callfailurelogginglevel.md) no tienen control sobre el registro de errores de descriptores de seguridad no válidos. Use **InvalidSecurityDescriptorLoggingLevel para** obtener control total sobre esta funcionalidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la seguridad para aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




