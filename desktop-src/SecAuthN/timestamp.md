---
description: El tipo de datos TimeStamp contiene información sobre la validez temporal de los tokens de seguridad. El formato del valor del tipo de datos TimeStamp es el mismo que el de la estructura FILETIME.
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: Marca de tiempo (SSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4898e85b0c11f55e5bb0dba2dbdefe2a3b6a2e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648297"
---
# <a name="timestamp"></a>TimeStamp

El tipo de datos **timestamp** contiene información sobre la validez temporal de los tokens de seguridad. El formato del valor del tipo de datos **timestamp** es el mismo que el de la estructura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |



 

 
