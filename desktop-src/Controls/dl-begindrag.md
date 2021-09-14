---
title: DL_BEGINDRAG de notificación (Commctrl.h)
description: Notifica a la ventana primaria del cuadro de lista de arrastre que el usuario ha hecho clic en el botón izquierdo del mouse en un elemento. Un cuadro de lista de arrastre envía este código de notificación en forma de mensaje de lista de arrastre. Para obtener más información, vea Arrastrar mensajes de cuadro de lista.
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
ms.openlocfilehash: 0f2d3ee211641c5b5e02482f914145fdf2e119f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174158"
---
# <a name="dl_begindrag-notification-code"></a>Código \_ de notificación BEGINDRAG de DL

Notifica a la ventana primaria del cuadro de lista de arrastre que el usuario ha hecho clic en el botón izquierdo del mouse en un elemento. Un cuadro de lista de arrastre envía este código de notificación en forma de mensaje de lista de arrastre. Para obtener más información, vea [Arrastrar mensajes de cuadro de lista.](about-list-boxes.md)


```C++
DL_BEGINDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contiene el código de notificación DL BEGINDRAG, el identificador del cuadro de lista de arrastre y la \_ posición del cursor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE para** comenzar la operación de arrastre o **FALSE** para evitar la operación de arrastre.

## <a name="remarks"></a>Observaciones

Al procesar este código de notificación, un procedimiento de ventana normalmente determina el elemento de lista en la posición de cursor especificada mediante la [**función LBItemFromPt.**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) A continuación, **devuelve TRUE** **o FALSE,** dependiendo de si se debe arrastrar el elemento. Antes de **devolver TRUE,** el procedimiento de ventana debe guardar el índice del elemento de lista para que la aplicación sepa qué elemento se debe mover o copiar cuando se complete la operación de arrastre.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





