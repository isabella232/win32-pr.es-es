---
title: InvalidSecurityDescriptorLoggingLevel
description: Establece el nivel de detalle de las entradas del registro de eventos sobre descriptores de seguridad no válidos para los permisos de inicio y acceso de componentes.
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- Valor del Registro COM InvalidSecurityDescriptorLoggingLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c2362b38c19acd8d895e5fa9640475fa401a7d5bd88c8016056df2d22c3a579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854345"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a>InvalidSecurityDescriptorLoggingLevel

Establece el nivel de detalle de las entradas del registro de eventos sobre descriptores de seguridad no válidos para los permisos de inicio y acceso de componentes.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ REG DWORD.**



| Valor | Descripción                                                                                                                                                                    |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Registra siempre errores cuando COM encuentra un descriptor de seguridad no válido. Este es el valor predeterminado.                                                                                  |
| 2     | Nunca registre errores cuando COM encuentre un descriptor de seguridad no válido. No se recomienda deshabilitar el registro de eventos, ya que puede dificultar el diagnóstico de problemas. |



 

Si establece directamente descriptores de seguridad de permisos de inicio y acceso (normalmente denominados ACL), es posible construir un descriptor de seguridad cuyo significado no se puede interpretar de forma inequívoca. COM realiza una entrada del registro de eventos cuando encuentra un descriptor de seguridad no válido.

Tenga en [**cuenta que ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) [**y CallFailureLoggingLevel**](callfailurelogginglevel.md) no tienen control sobre el registro de errores de descriptores de seguridad no válidos. Use **InvalidSecurityDescriptorLoggingLevel para** obtener control total sobre esta funcionalidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la seguridad para aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




