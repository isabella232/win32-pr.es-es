---
title: WTSLISTENERNAME (WtsApi32.h)
description: Representa el nombre de un agente Servicios de Escritorio remoto en un servidor Escritorio remoto host de sesión de Escritorio remoto.
ms.assetid: 3C41F507-6A67-4244-860F-E89B0F9E33B0
ms.tgt_platform: multiple
keywords:
- WTSLISTENERNAMEW
- WTSLISTENERNAMEA
- WTSLISTENERNAME
- PWTSLISTENERNAME
- WTSLISTENERNAME
- PWTSLISTENERNAME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce0df52229670cd090dd900dda3c2284437297bedc25c69f12c980b9cc40d92c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513845"
---
# <a name="wtslistenername"></a>WTSLISTENERNAME

Representa el nombre de un agente Servicios de Escritorio remoto en un servidor Escritorio remoto host de sesión de Escritorio remoto.


```C++
typedef WCHAR WTSLISTENERNAMEW[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEW;
typedef CHAR WTSLISTENERNAMEA[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEA;
#if UNICODE
typedef WTSLISTENERNAMEW WTSLISTENERNAME;
typedef PWTSLISTENERNAMEW PWTSLISTENERNAME;
#else 
typedef WTSLISTENERNAMEA WTSLISTENERNAME;
typedef PWTSLISTENERNAMEA PWTSLISTENERNAME;
#endif 
```



<dl> <dt>

**WTSLISTENERNAMEW**
</dt> <dd>

Nombre Unicode del agente de escucha.

</dd> <dt>

**WTSLISTENERNAMEA**
</dt> <dd>

Puntero al nombre ANSI del agente de escucha.

</dd> <dt>

**WTSLISTENERNAME**
</dt> <dd>

Nombre del agente de escucha.

</dd> <dt>

**PWTSLISTENERNAME**
</dt> <dd>

Puntero al nombre del agente de escucha.

</dd> <dt>

**WTSLISTENERNAME**
</dt> <dd>

Nombre del agente de escucha.

</dd> <dt>

**PWTSLISTENERNAME**
</dt> <dd>

Puntero al nombre del agente de escucha.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>WtsApi32.h</dt> </dl> |



 

 





