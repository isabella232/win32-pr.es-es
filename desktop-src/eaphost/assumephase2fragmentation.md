---
title: AssumePhase2Fragmentation
description: La clave del registro AssumePhase2Fragmentation determina si el servidor y el cliente suponen una fragmentación de la fase 2.
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0fa35692ec3ac741e2bd2fdb43607dfe1cb948
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104420029"
---
# <a name="assumephase2fragmentation"></a>AssumePhase2Fragmentation

La clave del registro AssumePhase2Fragmentation determina si el servidor y el cliente suponen una fragmentación de la fase 2.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   AssumePhase2Fragmentation = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **Registro \_ DWORD** .



| Value   | Descripción                                                                                                  |
|---------|--------------------------------------------------------------------------------------------------------------|
| 0       | El servidor y el cliente suponen que la otra parte no es capaz de fragmentar la fase 2 durante la autenticación PEAP. |
| distinto | El servidor y el cliente suponen que la otra parte es capaz de fragmentar la fase 2 durante la autenticación PEAP.     |



 

Si este valor del registro no está presente, el servidor y el cliente suponen que la otra entidad es capaz de fragmentar la fase 2 durante la autenticación PEAP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del registro de EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




