---
title: DL_DRAGGING de notificación (Commctrl.h)
description: Indica que el usuario ha movido el mouse mientras arrastra un elemento.
ms.assetid: 87fc4c24-8e88-4e3c-8f54-ecc7f80de5d7
keywords:
- DL_DRAGGING código de notificación Windows controles
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
ms.openlocfilehash: cfe07cbf2cce3ad639af94055a2d1eab1f4fc3d6ce576c1c5467310809858843
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878525"
---
# <a name="dl_dragging-notification-code"></a>Código \_ de notificación DRAG de DL

Indica que el usuario ha movido el mouse mientras arrastra un elemento. DL \_ DRAGGING también se envía periódicamente durante el arrastre, incluso si no se mueve el mouse. Un cuadro de lista de arrastrar envía este código de notificación a su ventana primaria en forma de mensaje de lista de arrastre. Para obtener más información, vea [Arrastrar mensajes de cuadro de lista.](about-list-boxes.md)


```C++
DL_DRAGGING

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de control del cuadro de lista de arrastre.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contiene el código de notificación DRAG DRAG de DL, el identificador del cuadro de lista de arrastre \_ y la posición del cursor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto determina el tipo de cursor del mouse que debe establecer la lista de arrastre; puede ser el valor \_ DL STOPCURSOR, DL \_ COPYCURSOR o \_ DL MOVECURSOR. Si se devuelve cualquier otro valor, el cursor no cambia.

## <a name="remarks"></a>Comentarios

Normalmente, un procedimiento de ventana procesa el código de notificación DRAG de DL determinando el elemento bajo el cursor y \_ dibujando un icono de inserción. Para recuperar el elemento bajo el cursor, use la función [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) y especifique **TRUE** para el *parámetro bAutoScroll.* Esta opción hace que el cuadro de lista de arrastre se desplace periódicamente si el cursor está por encima o por debajo de su área de cliente. Para dibujar el icono de inserción, use [**la función DrawInsert.**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





