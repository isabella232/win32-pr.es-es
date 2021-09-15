---
title: SRPRunningObjectChecks
description: Determina si los intentos de conectarse a objetos en ejecución se han proyectado para los niveles de confianza de la directiva de restricción de software (SRP) compatible.
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- Valor del Registro COM de SRPRunningObjectChecks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ad307856bcfdd30cfaa6c731551ac6570d2bec6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466616"
---
# <a name="srprunningobjectchecks"></a>SRPRunningObjectChecks

Determina si los intentos de conectarse a objetos en ejecución se han proyectado para los niveles de confianza de la directiva de restricción de software (SRP) compatible.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPRunningObjectChecks = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ SZ reg.**

Los valores de cadena de {N, n, NO, No, no} indican que los intentos de conectarse a objetos en ejecución no se han proyectado para niveles de confianza SRP compatibles. Si este valor del Registro se establece en cualquier otro valor o no existe, el objeto en ejecución no puede tener un nivel de confianza SRP menos estricto que el objeto de cliente. Por ejemplo, el objeto en ejecución no puede tener un nivel de confianza No permitido si el objeto de cliente tiene un nivel de confianza Sin restricciones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




