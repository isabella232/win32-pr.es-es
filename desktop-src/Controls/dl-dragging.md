---
title: Código de notificación de DL_DRAGGING (commctrl. h)
description: Indica que el usuario ha desplazado el mouse mientras arrastra un elemento.
ms.assetid: 87fc4c24-8e88-4e3c-8f54-ecc7f80de5d7
keywords:
- DL_DRAGGING controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- DL_DRAGGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c9f3f6cec3ef95745eed88ec0208dff581ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535650"
---
# <a name="dl_dragging-notification-code"></a>Código de notificación de arrastre de DL \_

Indica que el usuario ha desplazado el mouse mientras arrastra un elemento. \_La acción de arrastrar DL también se envía periódicamente durante el arrastre incluso si el mouse no se mueve. Un cuadro de lista de arrastre envía este código de notificación a su ventana primaria en forma de mensaje de la lista de arrastre. Para obtener más información, vea [arrastrar mensajes de cuadro de lista](about-list-boxes.md).


```C++
DL_DRAGGING

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del control del cuadro de lista de arrastre.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contiene el código de \_ notificación de arrastre DL, el identificador del cuadro de lista de arrastre y la posición del cursor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto determina el tipo de cursor del mouse que debe establecer la lista de arrastre; puede ser el valor DL \_ STOPCURSOR, DL \_ COPYCURSOR o DL \_ MOVECURSOR. Si se devuelve cualquier otro valor, el cursor no cambia.

## <a name="remarks"></a>Observaciones

Un procedimiento de ventana normalmente procesa el código de la notificación de arrastre de la DL \_ determinando el elemento bajo el cursor y dibujando un icono de inserción. Para recuperar el elemento bajo el cursor, utilice la función [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) , especificando **true** para el parámetro *bAutoScroll* . Esta opción hace que el cuadro de lista de arrastre se desplace periódicamente si el cursor está por encima o por debajo de su área de cliente. Para dibujar el icono de inserción, utilice la función [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





