---
title: SRPTrustLevel
description: Establece el nivel de confianza de la directiva de restricción de software (SRP) para las aplicaciones.
ms.assetid: 2ec10eb5-f83a-4ce7-8e03-36cdafadf169
keywords:
- COM de valor del Registro SRPTrustLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c1e9290cbe04cfe33e1192b95b86ca03fd5ea5
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369640"
---
# <a name="srptrustlevel"></a>SRPTrustLevel

Establece el nivel de confianza de la directiva de restricción de software (SRP) para las aplicaciones.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      SRPTrustLevel = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG DWORD** que está disponible a partir de Windows XP.



| Value                                 | Descripción                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------|
| 0x0 \_ (LEVELID NO PERMITIDO MÁS \_ SEGURO)      | No se permite que la aplicación acceda a privilegios de usuario y que tengan en cuenta la seguridad. |
| 0x40000 \_ (SAFE LEVELID \_ FULLYTRUSTED) | La aplicación tiene acceso sin restricciones a los privilegios del usuario.                    |



 

Si el **valor SRPTrustLevel** no existe, se usa el valor predeterminado de SAFER \_ LEVELID \_ DISALLOWED. Si **SRPTrustLevel** es del tipo incorrecto o está fuera del intervalo, COM devuelve el error COMADMIN \_ E \_ SAFERINVALID. Si se produce un error en una activación de cualquier ordenación debido a comprobaciones de confianza de SRP, COM devuelve el error CO \_ E \_ ACTIVATIONFAILED.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> <dt>

[**SRPActivateAsActivatorChecks**](srpactivateasactivatorchecks.md)
</dt> <dt>

[**SRPRunningObjectChecks**](srprunningobjectchecks.md)
</dt> </dl>

 

 




