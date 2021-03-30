---
title: SRPRunningObjectChecks
description: Determina si los intentos de conexión a objetos en ejecución se filtran para los niveles de confianza de la Directiva de restricción de software (SRP) compatible.
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- Valor del registro SRPRunningObjectChecks COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ad307856bcfdd30cfaa6c731551ac6570d2bec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774965"
---
# <a name="srprunningobjectchecks"></a>SRPRunningObjectChecks

Determina si los intentos de conexión a objetos en ejecución se filtran para los niveles de confianza de la Directiva de restricción de software (SRP) compatible.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPRunningObjectChecks = value
```

## <a name="remarks"></a>Observaciones

Este es un valor de **reg \_ SZ** .

Los valores de cadena de {N, n, NO, no, no} indican que los intentos de conexión a objetos en ejecución no se filtran por niveles de confianza de SRP compatibles. Si este valor del registro se establece en cualquier otro valor o no existe, el objeto en ejecución no puede tener un nivel de confianza SRP menos estricto que el objeto cliente. Por ejemplo, el objeto en ejecución no puede tener un nivel de confianza no permitido si el objeto de cliente tiene un nivel de confianza no restringido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




