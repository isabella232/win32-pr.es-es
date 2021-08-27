---
title: LVN_MARQUEEBEGIN de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de lista que ha comenzado una selección de rectángulo de selección (marquesina). Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
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
ms.openlocfilehash: d8012981883564450603d11d0eb243375f48b46cdb14a14984a19415c84dab3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109535"
---
# <a name="lvn_marqueebegin-notification-code"></a>Código de notificación \_ LVN MARQUEEBEGIN

Notifica a la ventana primaria de un control de vista de lista que ha comenzado una selección de rectángulo de selección (marquesina). Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


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

## <a name="remarks"></a>Comentarios

Una *selección de cuadro de límite* es el proceso de hacer clic en el área cliente de la ventana de vista de lista y arrastrar para seleccionar varios elementos simultáneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





