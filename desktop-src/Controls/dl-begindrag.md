---
title: Código de notificación de DL_BEGINDRAG (commctrl. h)
description: Notifica a la ventana primaria del cuadro de lista de arrastre que el usuario hizo clic con el botón primario del mouse en un elemento. Un cuadro de lista de arrastre envía este código de notificación en forma de mensaje de la lista de arrastre. Para obtener más información, vea arrastrar mensajes de cuadro de lista.
ms.assetid: ccf66818-e5f7-4165-8d0d-4d279944f70e
keywords:
- DL_BEGINDRAG controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- DL_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2d3ee211641c5b5e02482f914145fdf2e119f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905705"
---
# <a name="dl_begindrag-notification-code"></a>Código de notificación de DL \_ BEGINDRAG

Notifica a la ventana primaria del cuadro de lista de arrastre que el usuario hizo clic con el botón primario del mouse en un elemento. Un cuadro de lista de arrastre envía este código de notificación en forma de mensaje de la lista de arrastre. Para obtener más información, vea [arrastrar mensajes de cuadro de lista](about-list-boxes.md).


```C++
DL_BEGINDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Un puntero a una estructura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contiene el \_ código de notificación DL BEGINDRAG, el identificador del cuadro de lista de arrastre y la posición del cursor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelva **true** para comenzar la operación de arrastre o **false** para evitar la operación de arrastre.

## <a name="remarks"></a>Observaciones

Al procesar este código de notificación, un procedimiento de ventana normalmente determina el elemento de lista en la posición del cursor especificada mediante la función [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) . Después, devuelve **true** o **false**, en función de si se debe arrastrar el elemento. Antes de devolver **true**, el procedimiento de ventana debe guardar el índice del elemento de lista para que la aplicación sepa qué elemento se va a deshacer o copiar cuando se complete la operación de arrastre.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





