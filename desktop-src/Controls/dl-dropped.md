---
title: DL_DROPPED de notificación (Commctrl.h)
description: Indica que el usuario ha completado una operación de arrastrar al soltar el botón izquierdo del mouse. Un cuadro de lista de arrastrar envía este código de notificación a su ventana primaria en forma de mensaje de lista de arrastre. Para obtener más información, vea Arrastrar mensajes de cuadro de lista.
ms.assetid: 81b9b424-2735-407d-bac9-f03ea2f48b4e
keywords:
- DL_DROPPED código de notificación Windows controles
topic_type:
- apiref
api_name:
- DL_DROPPED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b2480360ea38a00c4dd8efe6eb84eed8999890
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174141"
---
# <a name="dl_dropped-notification-code"></a>Código \_ de notificación DL DROPPED

Indica que el usuario ha completado una operación de arrastrar al soltar el botón izquierdo del mouse. Un cuadro de lista de arrastrar envía este código de notificación a su ventana primaria en forma de mensaje de lista de arrastre. Para obtener más información, vea [Arrastrar mensajes de cuadro de lista.](about-list-boxes.md)


```C++
DL_DROPPED

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contiene el código de notificación DL DROPPED, el identificador del cuadro de lista de arrastre \_ y la posición del cursor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este código de notificación se procesa normalmente insertando el elemento que se arrastra a la lista delante del elemento bajo el cursor. Para recuperar el índice del elemento en la posición del cursor, use la [**función LBItemFromPt.**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) Tenga en cuenta que el código de \_ notificación DL DROPPED se envía incluso si el cursor no está en un elemento de lista. En ese caso, **LBItemFromPt** devuelve -1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





