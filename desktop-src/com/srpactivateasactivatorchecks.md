---
title: SRPActivateAsActivatorChecks
description: Determina si los niveles de confianza de la directiva de restricción de software (SRP) se usan durante las activaciones de ActivateAsActivator.
ms.assetid: b0d616c3-1cb0-4854-a4f9-6635d61b0698
keywords:
- Valor del Registro COM de SRPActivateAsActivatorChecks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b66ae6b1c7f267f48f24441c04e95eea75e4345
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369643"
---
# <a name="srpactivateasactivatorchecks"></a>SRPActivateAsActivatorChecks

Determina si los niveles de confianza de la directiva de restricción de software (SRP) se usan durante las activaciones de ActivateAsActivator.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPActivateAsActivatorChecks = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG SZ.**

Los valores de cadena de {N, n, NO, No, no} indican que el objeto de servidor se ejecuta con el nivel de confianza SRP del objeto cliente, independientemente del nivel de confianza de SRP con el que se configuró. Si este valor del Registro se establece en cualquier otro valor o no existe, el nivel de confianza de SRP que está configurado para el objeto de servidor se compara con el nivel de confianza SRP del objeto de cliente y se usa el nivel de confianza más estricto para ejecutar el objeto de servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




