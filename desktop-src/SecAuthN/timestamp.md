---
description: El tipo de datos TimeStamp contiene información sobre la validez de la hora de los tokens de seguridad. El formato del valor del tipo de datos TimeStamp es el mismo que el de la estructura FILETIME.
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: TimeStamp (Sspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e521818c9001213396c0046b92f8f0bd9727dddfeaf99b2e23b652a48f8ff95d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786370"
---
# <a name="timestamp"></a>TimeStamp

El **tipo de datos TimeStamp** contiene información sobre la validez de la hora de los tokens de seguridad. El formato del valor del tipo de datos **TimeStamp** es el mismo que el de la [**estructura FILETIME.**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Sspi.h (incluir Security.h)</dt> </dl> |



 

 
