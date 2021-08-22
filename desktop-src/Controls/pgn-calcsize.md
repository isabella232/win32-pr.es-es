---
title: PGN_CALCSIZE de notificación (Commctrl.h)
description: Enviado por un control de paginación para obtener las dimensiones desplazables de la ventana independiente.
ms.assetid: a15f4191-2f26-4139-bdaf-bab219449b78
keywords:
- PGN_CALCSIZE código de notificación Windows controles
topic_type:
- apiref
api_name:
- PGN_CALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c2f6da5153457a871918afea60ac1251496454831a09426f16579ac47342406
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078879"
---
# <a name="pgn_calcsize-notification-code"></a>Código de notificación \_ PGN CALCSIZE

Enviado por un control de paginación para obtener las dimensiones desplazables de la ventana independiente. El control de paginación usa estas dimensiones para determinar el tamaño desplazable de la ventana independiente. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PGN_CALCSIZE

    lpnmcs = (LPNMPGCALCSIZE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) que contiene y recibe información sobre el código de notificación. El **miembro dwFlag** de esta estructura indica qué dimensión se está calculando. Según el valor de **dwFlag**, debe colocar la dimensión deseada en el **miembro iWidth** o **iHeight** de esta estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





