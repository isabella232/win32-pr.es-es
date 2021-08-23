---
description: El tipo de datos HCRYPTHASH se usa para representar identificadores a objetos hash.
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: HCRYPTHASH (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99b2d20d7aeb46adda162f8d5ec380143164690bad8ee88139f9653753f1e290
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006563"
---
# <a name="hcrypthash"></a>HCRYPTHASH

El **tipo de datos HCRYPTHASH** se usa para representar identificadores para los objetos [*hash*](../secgloss/h-gly.md). Estos identificadores indican al módulo CSP qué hash se usa en una operación determinada. El módulo CSP no permite la manipulación directa de los valores hash. En su lugar, el usuario manipula los valores hash a través del identificador hash.


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
