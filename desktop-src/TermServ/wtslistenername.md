---
title: WTSLISTENERNAME (WtsApi32. h)
description: Representa el nombre de una Servicios de Escritorio remoto agentes de escucha en un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422460"
---
# <a name="wtslistenername"></a>WTSLISTENERNAME

Representa el nombre de una Servicios de Escritorio remoto agentes de escucha en un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).


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
| Encabezado<br/>                   | <dl> <dt>WtsApi32. h</dt> </dl> |



 

 





