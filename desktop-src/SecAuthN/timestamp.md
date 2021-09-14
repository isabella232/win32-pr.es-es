---
description: El tipo de datos TimeStamp contiene información sobre la validez temporal de los tokens de seguridad. El formato del valor del tipo de datos TimeStamp es el mismo que el de la estructura FILETIME.
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: TimeStamp (Sspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4898e85b0c11f55e5bb0dba2dbdefe2a3b6a2e4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160940"
---
# <a name="timestamp"></a>TimeStamp

El **tipo de datos TimeStamp** contiene información sobre la validez temporal de los tokens de seguridad. El formato del valor del tipo de datos **TimeStamp** es el mismo que el de la [**estructura FILETIME.**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Sspi.h (incluir Security.h)</dt> </dl> |



 

 
