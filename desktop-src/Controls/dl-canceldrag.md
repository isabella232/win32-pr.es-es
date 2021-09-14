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
ms.openlocfilehash: ab10f7c31184c44fabdffd4f611847e550b62cc7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174146"
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

## <a name="remarks"></a>Observaciones

Al procesar el código de notificación CANCELDRAG de DL, una aplicación puede restablecer su estado interno para indicar que el arrastre \_ no está en vigor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





