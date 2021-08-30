---
title: DL_CANCELDRAG de notificación (Commctrl.h)
description: Indica que el usuario ha cancelado una operación de arrastrar haciendo clic con el botón derecho del mouse o presionando la tecla ESC.
ms.assetid: 62c1377f-41b6-449f-a95e-2689dc1913c6
keywords:
- DL_CANCELDRAG código de notificación Windows controles
topic_type:
- apiref
api_name:
- DL_CANCELDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88651dc7c9f048929eecfcde33127ecb38197580cc17e458a86f8c28c6ab6065
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088995"
---
# <a name="dl_canceldrag-notification-code"></a>Código \_ de notificación CANCELDRAG de DL

Indica que el usuario ha cancelado una operación de arrastrar haciendo clic con el botón derecho del mouse o presionando la tecla ESC. Un cuadro de lista de arrastre envía este código de notificación a su ventana primaria en forma de mensaje de lista de arrastre. Para obtener más información, vea [Arrastrar mensajes de cuadro de lista.](about-list-boxes.md)


```C++
DL_CANCELDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contiene el código de notificación DL CANCELDRAG, el identificador del cuadro de lista de arrastre y la \_ posición del cursor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Al procesar el código de notificación CANCELDRAG de DL, una aplicación puede restablecer su estado interno para indicar que el arrastre \_ no está en vigor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





