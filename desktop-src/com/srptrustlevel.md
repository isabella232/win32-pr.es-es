---
title: SRPTrustLevel
description: Establece el nivel de confianza de la Directiva de restricción de software (SRP) para las aplicaciones.
ms.assetid: 2ec10eb5-f83a-4ce7-8e03-36cdafadf169
keywords:
- Valor del registro SRPTrustLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c1e9290cbe04cfe33e1192b95b86ca03fd5ea5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418539"
---
# <a name="srptrustlevel"></a>SRPTrustLevel

Establece el nivel de confianza de la Directiva de restricción de software (SRP) para las aplicaciones.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      SRPTrustLevel = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **Registro \_ DWORD** que está disponible a partir de Windows XP.



| Value                                 | Descripción                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------|
| 0X0 (LEVELID más seguro no \_ \_ permitido)      | No se permite el acceso a la aplicación y los privilegios de usuario que tienen en cuenta la seguridad. |
| 0x40000 ( \_ LEVELID seguro \_ FULLYTRUSTED) | La aplicación tiene acceso ilimitado a los privilegios del usuario.                    |



 

Si el valor de **SRPTrustLevel** no existe, se usa el valor predeterminado de LEVELID Safe no \_ \_ permitido. Si **SRPTrustLevel** es del tipo incorrecto o está fuera del intervalo, com devuelve el error COMAdmin \_ E \_ SAFERINVALID. Si se produce un error en la activación de cualquier orden debido a las comprobaciones de confianza de SRP, COM devuelve el error CO \_ E \_ ACTIVATIONFAILED.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> <dt>

[**SRPActivateAsActivatorChecks**](srpactivateasactivatorchecks.md)
</dt> <dt>

[**SRPRunningObjectChecks**](srprunningobjectchecks.md)
</dt> </dl>

 

 




