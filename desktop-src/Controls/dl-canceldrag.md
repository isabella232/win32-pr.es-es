---
title: Código de notificación de DL_CANCELDRAG (commctrl. h)
description: Indica que el usuario ha cancelado una operación de arrastrar haciendo clic con el botón secundario del mouse o presionando la tecla ESC.
ms.assetid: 62c1377f-41b6-449f-a95e-2689dc1913c6
keywords:
- DL_CANCELDRAG controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151289"
---
# <a name="dl_canceldrag-notification-code"></a>Código de notificación de DL \_ CANCELDRAG

Indica que el usuario ha cancelado una operación de arrastrar haciendo clic con el botón secundario del mouse o presionando la tecla ESC. Un cuadro de lista de arrastre envía este código de notificación a su ventana primaria en forma de mensaje de la lista de arrastre. Para obtener más información, vea [arrastrar mensajes de cuadro de lista](about-list-boxes.md).


```C++
DL_CANCELDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Un puntero a una estructura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contiene el \_ código de notificación DL CANCELDRAG, el identificador del cuadro de lista de arrastre y la posición del cursor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Al procesar el \_ código de notificación DL CANCELDRAG, una aplicación puede restablecer su estado interno para indicar que el arrastre no está en vigor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





