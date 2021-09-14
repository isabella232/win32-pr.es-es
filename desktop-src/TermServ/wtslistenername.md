---
title: WTSLISTENERNAME (WtsApi32.h)
description: Representa el nombre de un agente Servicios de Escritorio remoto escuchas en un servidor Escritorio remoto de sesión de escritorio remoto ( Host de sesión de Escritorio remoto).
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
ms.openlocfilehash: a82576fc9f4490b133916852441c50dcf77e849d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890564"
---
# <a name="wtslistenername"></a>WTSLISTENERNAME

Representa el nombre de un agente Servicios de Escritorio remoto escuchas en un servidor Escritorio remoto de sesión de escritorio remoto ( Host de sesión de Escritorio remoto).


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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>WtsApi32.h</dt> </dl> |



 

 





