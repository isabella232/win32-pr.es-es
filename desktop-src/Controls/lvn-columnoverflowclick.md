---
title: Código de notificación de LVN_COLUMNOVERFLOWCLICK (commctrl. h)
description: Se envía por un control de vista de lista cuando se hace clic en el botón de desbordamiento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 3d3bb7be-b598-450a-b829-a5aa5b1a0c5d
keywords:
- LVN_COLUMNOVERFLOWCLICK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_COLUMNOVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7938d28be337f7255a9b84422fa090da5a494cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493336"
---
# <a name="lvn_columnoverflowclick-notification-code"></a>Código de notificación de COLUMNOVERFLOWCLICK de LVN \_

Se envía por un control de vista de lista cuando se hace clic en el botón de desbordamiento. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
LVN_COLUMNOVERFLOWCLICK
     
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* \[ de\]
</dt> <dd>

Puntero a una estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que describe el código de notificación. El autor de la llamada es responsable de asignar esta estructura, incluida la estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenida. Establezca los miembros de la estructura **NMHDR** . El miembro de **código** debe establecerse en LVN \_ COLUMNOVERFLOWCLICK.

Establezca el miembro **iItem** de la estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) en-1. Establezca el miembro **iSubItem** en el índice del subelemento. Establezca los miembros **uNewState**, **uOldState** y **lParam** en cero. No se usan los miembros restantes de la estructura **NMLISTVIEW** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El receptor de notificaciones convierte *lParam* para recuperar la estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . El parámetro *wParam* contiene el identificador del control que envía el código de notificación.

Si un control de encabezado es un elemento secundario del control ListView, el control de encabezado debería enviar este código de notificación al control ListView cuando el control de encabezado reciba el código de notificación [ \_ OVERFLOWCLICK de HDN](hdn-overflowclick.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





