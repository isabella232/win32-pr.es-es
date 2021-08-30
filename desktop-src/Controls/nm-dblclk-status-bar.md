---
title: NM_DBLCLK de notificación (barra de estado) (Commctrl.h)
description: Notifica a la ventana primaria de un control de barra de estado que el usuario ha hecho doble clic en el botón izquierdo del mouse dentro del control. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 4c02c76d-2bdb-48ef-aa8e-635d0e200eb1
keywords:
- NM_DBLCLK (barra de estado) código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de3704d2a8674233d0cd5dce04849db6b0f794bc7fe5032b149de15411a3c068
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088835"
---
# <a name="nm_dblclk-status-bar-notification-code"></a>Código de notificación de NM \_ DBLCLK (barra de estado)

Notifica a la ventana primaria de un control de barra de estado que el usuario ha hecho doble clic en el botón izquierdo del mouse dentro del control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_DBLCLK
        
    LPNMMOUSE lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información adicional sobre esta notificación. El **miembro dwItemSpec** contiene el índice de la sección en la que se hizo clic.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para indicar que el sistema controló el clic del mouse y suprime el procesamiento predeterminado. Devuelve **FALSE** para permitir el procesamiento predeterminado del clic.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





