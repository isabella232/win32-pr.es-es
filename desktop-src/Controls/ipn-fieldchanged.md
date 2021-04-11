---
title: Código de notificación de IPN_FIELDCHANGED (commctrl. h)
description: Se envía cuando el usuario cambia un campo en el control o se mueve de un campo a otro. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- IPN_FIELDCHANGED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- IPN_FIELDCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e283d42d0aba3c237db51fe492a34ec93e8eb73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079619"
---
# <a name="ipn_fieldchanged-notification-code"></a>Código de notificación de FIELDCHANGED de IPN \_

Se envía cuando el usuario cambia un campo en el control o se mueve de un campo a otro. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
IPN_FIELDCHANGED

    lpnmipa = (LPNMIPADDRESS) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) que contiene información sobre la dirección modificada. El miembro **iValue** de esta estructura contendrá el valor especificado, aunque esté fuera del intervalo del campo. Puede modificar este miembro a cualquier valor que esté dentro del intervalo del campo en respuesta a este código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

Este código de notificación no se envía como respuesta a un mensaje [**\_ SETADDRESS de IPM**](ipm-setaddress.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





