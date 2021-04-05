---
title: Código de notificación de LVN_SETDISPINFO (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que debe actualizar la información que mantiene para un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 1ea51d50-4a57-4662-972e-89e916fa9b16
keywords:
- LVN_SETDISPINFO controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_SETDISPINFO
- LVN_SETDISPINFOA
- LVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659623d892f0f5a556f4890703d4e0dd725536b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996744"
---
# <a name="lvn_setdispinfo-notification-code"></a>Código de notificación de SETDISPINFO de LVN \_

Notifica a la ventana primaria de un control de vista de lista que debe actualizar la información que mantiene para un elemento. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
LVN_SETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) que especifica información del elemento modificado. El miembro del **elemento** de esta estructura es una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que contiene información sobre el elemento que se ha cambiado. El miembro **miembros pszText** del **elemento** contiene un valor válido, independientemente de si la \_ marca de texto LVIF se establece en el miembro de **máscara** de esta estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El receptor de notificaciones convierte *lParam* para recuperar la estructura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . El parámetro *wParam* contiene el código de mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVN \_ SETDISPINFOW** (Unicode) y **LVN \_ SETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[LVN \_ GETDISPINFO](lvn-getdispinfo.md)
</dt> </dl>

 

 





