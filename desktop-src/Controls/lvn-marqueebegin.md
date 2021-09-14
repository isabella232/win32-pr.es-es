---
title: LVN_MARQUEEBEGIN de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de lista que ha comenzado una selección de rectángulo delimitador (marquesina). Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: e9daa264-1861-4791-9a12-cf95d86a688e
keywords:
- LVN_MARQUEEBEGIN código de notificación Windows controles
topic_type:
- apiref
api_name:
- LVN_MARQUEEBEGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d46d399b8355bea0ddb2054340d52db59c3ad27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362574"
---
# <a name="lvn_marqueebegin-notification-code"></a>Código de notificación \_ LVN MARQUEEBEGIN

Notifica a la ventana primaria de un control de vista de lista que ha comenzado una selección de rectángulo delimitador (marquesina). Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_MARQUEEBEGIN

    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR.**](/windows/desktop/api/richedit/ns-richedit-nmhdr)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para aceptar el código de notificación, devuelva cero. Para salir de la selección del cuadro de límite, devuelva distinto de cero.

## <a name="remarks"></a>Observaciones

Una *selección de cuadro de límite* es el proceso de hacer clic en el área de cliente de la ventana de vista de lista y arrastrar para seleccionar varios elementos simultáneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





