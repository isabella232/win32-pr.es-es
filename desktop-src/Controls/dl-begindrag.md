---
title: DL_BEGINDRAG de notificación (Commctrl.h)
description: Notifica a la ventana primaria del cuadro de lista de arrastre que el usuario ha hecho clic en el botón izquierdo del mouse en un elemento. Un cuadro de lista de arrastrar envía este código de notificación en forma de mensaje de lista de arrastre. Para obtener más información, vea Arrastrar mensajes de cuadro de lista.
ms.assetid: ccf66818-e5f7-4165-8d0d-4d279944f70e
keywords:
- DL_BEGINDRAG código de notificación Windows controles
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
ms.openlocfilehash: 5e2c843398b21ad51df51ae706a515c2e6f9831b89d32092b87148598b4bed5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968335"
---
# <a name="dl_begindrag-notification-code"></a>Código \_ de notificación BEGINDRAG de DL

Notifica a la ventana primaria del cuadro de lista de arrastre que el usuario ha hecho clic en el botón izquierdo del mouse en un elemento. Un cuadro de lista de arrastrar envía este código de notificación en forma de mensaje de lista de arrastre. Para obtener más información, vea [Arrastrar mensajes de cuadro de lista.](about-list-boxes.md)


```C++
DL_BEGINDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contiene el código de notificación BEGINDRAG de DL, el identificador del cuadro de lista de arrastre \_ y la posición del cursor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para comenzar la operación de arrastre o **FALSE** para evitar la operación de arrastre.

## <a name="remarks"></a>Comentarios

Al procesar este código de notificación, un procedimiento de ventana normalmente determina el elemento de lista en la posición de cursor especificada mediante la [**función LBItemFromPt.**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) A continuación, **devuelve TRUE** **o FALSE,** dependiendo de si se debe arrastrar el elemento. Antes de **devolver TRUE**, el procedimiento de ventana debe guardar el índice del elemento de lista para que la aplicación sepa qué elemento mover o copiar cuando se complete la operación de arrastre.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





