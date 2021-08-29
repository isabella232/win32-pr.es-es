---
title: NM_CLICK (barra de herramientas) de notificación (Commctrl.h)
description: Enviado por un control de barra de herramientas cuando el usuario hace clic en un elemento con el botón izquierdo del mouse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: fa43c9bc-db2a-4460-b193-2b4694d06d83
keywords:
- NM_CLICK código de notificación (barra de herramientas) Windows controles
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b116ee8a47252b01713637cd8af8bbd484bf0c6cc26a34e1be882f805f501b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834495"
---
# <a name="nm_click-toolbar-notification-code"></a>Código de \_ notificación NM CLICK (barra de herramientas)

Enviado por un control de barra de herramientas cuando el usuario hace clic en un elemento con el botón izquierdo del mouse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información adicional sobre esta notificación. El **miembro dwItemSpec** contiene el índice de la sección en la que se hizo clic.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para indicar que el sistema controló el clic del mouse y suprime el procesamiento predeterminado. Devuelve **FALSE** para permitir el procesamiento predeterminado del clic.

## <a name="remarks"></a>Comentarios

Al hacer clic en un elemento con el botón izquierdo del mouse, la barra de herramientas envía un mensaje [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) con el código de [notificación BN \_ CLICKED](bn-clicked.md) a la ventana primaria. La notificación NM \_ CLICK se envía después del mensaje WM **\_ COMMAND.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

