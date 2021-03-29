---
description: El tipo de datos HCRYPTHASH se usa para representar los identificadores de los objetos hash.
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: HCRYPTHASH (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a009350ed910627c1e6ec9ae33997ed20c7fec2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912030"
---
# <a name="hcrypthash"></a>HCRYPTHASH

El tipo de datos **HCRYPTHASH** se usa para representar los identificadores de los [*objetos hash*](../secgloss/h-gly.md). Estos identificadores indican al módulo CSP qué hash se usa en una operación determinada. El módulo CSP no habilita la manipulación directa de los valores hash. En su lugar, el usuario manipula los valores hash a través del identificador hash.


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
