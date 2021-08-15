---
title: NM_RCLICK de notificación (barra de herramientas) (Commctrl.h)
description: Enviado por un control de barra de herramientas cuando el usuario hace clic en la barra de herramientas con el botón derecho del mouse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: e9d2d871-e922-444d-a76c-e73f249ed410
keywords:
- NM_RCLICK código de notificación (barra de herramientas) Windows controles
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52fde315a3c68712c58b7e9466c351c6ac9a9117710ee6f285bd9ba9521ba56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958074"
---
# <a name="nm_rclick-toolbar-notification-code"></a>Código de notificación de NM \_ RCLICK (barra de herramientas)

Enviado por un control de barra de herramientas cuando el usuario hace clic en la barra de herramientas con el botón derecho del mouse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RCLICK

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información sobre este código de notificación. Si se hizo clic con el mouse en un elemento de la barra de herramientas, el **miembro dwItemSpec** contiene el identificador del elemento y el **miembro dwItemData** contiene los datos del elemento. Si se hizo clic con el mouse en un separador o un espacio en blanco en la barra de herramientas, el **miembro dwItemSpec** contendrá -1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **FALSE** para permitir que el control de la barra de herramientas realice el procesamiento predeterminado del evento o **TRUE** para evitar que el control procese el evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





