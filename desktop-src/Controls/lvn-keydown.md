---
title: Código de notificación de LVN_KEYDOWN (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que se ha presionado una tecla. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 3aa3d165-7227-41c4-8bc2-3e51a0f52ee3
keywords:
- LVN_KEYDOWN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 516c64e9050a6946d3a135ecc0d00d7e384e9844
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997183"
---
# <a name="lvn_keydown-notification-code"></a>\_Código de notificación KEYDOWN de LVN

Notifica a la ventana primaria de un control de vista de lista que se ha presionado una tecla. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
LVN_KEYDOWN

    pnkd = (LPNMLVKEYDOWN) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMLVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





