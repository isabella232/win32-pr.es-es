---
title: Código de notificación de NM_SETCURSOR (ComboBoxEx) (commctrl. h)
description: Notifica a la ventana primaria de un control ComboBoxEx que el control está estableciendo el cursor en respuesta a un \_ mensaje de SETCURSOR de WM. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: a1c617fa-8eb2-444f-88d1-9913de7a42d1
keywords:
- Controles de Windows de código de notificación de NM_SETCURSOR (ComboBoxEx)
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbd5e10f06e74af0778521d31c69e63586a6476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803151"
---
# <a name="nm_setcursor-comboboxex-notification-code"></a>Código de notificación de NM \_ SETCURSOR (ComboBoxEx)

Notifica a la ventana primaria de un control ComboBoxEx que el control está estableciendo el cursor en respuesta a un mensaje de [**\_ SETCURSOR de WM**](/windows/desktop/menurc/wm-setcursor) . Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para permitir que el control establezca el cursor o un valor distinto de cero para evitar que el control establezca el cursor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

