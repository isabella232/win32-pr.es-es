---
title: LVN_COLUMNOVERFLOWCLICK de notificación (Commctrl.h)
description: Enviado por un control de vista de lista cuando se hace clic en el botón de desbordamiento. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 3d3bb7be-b598-450a-b829-a5aa5b1a0c5d
keywords:
- LVN_COLUMNOVERFLOWCLICK código de notificación Windows controles
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
ms.openlocfilehash: edb28deb3dd98542791b4c8daf350e618e43db57d5090a93d49af5e55e8b39ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077125"
---
# <a name="lvn_columnoverflowclick-notification-code"></a>Código de notificación \_ LVN COLUMNOVERFLOWCLICK

Enviado por un control de vista de lista cuando se hace clic en el botón de desbordamiento. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_COLUMNOVERFLOWCLICK
     
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* \[ En\]
</dt> <dd>

Puntero a una [**estructura NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que describe el código de notificación. El autor de la llamada es responsable de asignar esta estructura, incluida la estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenida. Establezca los miembros de la **estructura NMHDR.** El **miembro** de código debe establecerse en LVN \_ COLUMNOVERFLOWCLICK.

Establezca el **miembro iItem** de la [**estructura NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) en -1. Establezca el **miembro iSubItem** en el índice del subelemento. Establezca los **miembros uNewState**, **uOldState** y **lParam** en cero. No se usan los miembros restantes de la estructura **NMLISTVIEW.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El receptor de notificaciones convierte *lParam* para recuperar la [**estructura NMLISTVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) El *parámetro wParam* contiene el identificador del control que envía el código de notificación.

Si un control de encabezado es un elemento secundario de la vista de lista, el control de encabezado debe enviar este código de notificación al control listview cuando el control de encabezado recibe el código de [notificación DE HDN \_ OVERFLOWCLICK.](hdn-overflowclick.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





