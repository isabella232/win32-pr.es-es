---
description: El tipo de datos HCRYPTHASH se usa para representar identificadores a objetos hash.
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: HCRYPTHASH (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a009350ed910627c1e6ec9ae33997ed20c7fec2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171021"
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
| Encabezado<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
