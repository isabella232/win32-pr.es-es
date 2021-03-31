---
title: SRPActivateAsActivatorChecks
description: Determina si los niveles de confianza de la Directiva de restricción de software (SRP) se usan durante las activaciones de ActivateAsActivator.
ms.assetid: b0d616c3-1cb0-4854-a4f9-6635d61b0698
keywords:
- Valor del registro SRPActivateAsActivatorChecks COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b66ae6b1c7f267f48f24441c04e95eea75e4345
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774970"
---
# <a name="srpactivateasactivatorchecks"></a>SRPActivateAsActivatorChecks

Determina si los niveles de confianza de la Directiva de restricción de software (SRP) se usan durante las activaciones de ActivateAsActivator.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPActivateAsActivatorChecks = value
```

## <a name="remarks"></a>Observaciones

Este es un valor de **reg \_ SZ** .

Los valores de cadena de {N, n, NO, no, no} indican que el objeto de servidor se ejecuta con el nivel de confianza de SRP del objeto de cliente, independientemente del nivel de confianza de SRP con el que se configuró. Si este valor del registro se establece en cualquier otro valor o no existe, el nivel de confianza de SRP configurado para el objeto de servidor se compara con el nivel de confianza de SRP del objeto de cliente y se utiliza el nivel de confianza más riguroso para ejecutar el objeto de servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




