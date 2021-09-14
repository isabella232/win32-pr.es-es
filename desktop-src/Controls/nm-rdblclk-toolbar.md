---
title: NM_RDBLCLK de notificación (barra de herramientas) (Commctrl.h)
description: Notifica a la ventana primaria de un control que el usuario ha hecho doble clic en el botón derecho del mouse dentro del control. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 0281a687-3f1c-4fc1-bf1d-19c7ac920cd3
keywords:
- NM_RDBLCLK de notificación (barra de herramientas) Windows controles
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec2129b6400c60bd59e441ff8af2083e781ba22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167914"
---
# <a name="nm_rdblclk-toolbar-notification-code"></a>Código de \_ notificación DE NM RDBLCLK (barra de herramientas)

Notifica a la ventana primaria de un control que el usuario ha hecho doble clic en el botón derecho del mouse dentro del control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RDBLCLK

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información sobre este código de notificación. Si se hizo clic con el mouse en un elemento de la barra de herramientas, el **miembro dwItemSpec** contiene el identificador del elemento y el **miembro dwItemData** contiene los datos del elemento. Si se hizo clic con el mouse en un separador o un espacio en blanco en la barra de herramientas, el **miembro dwItemSpec** contendrá -1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **FALSE** para permitir que el control de barra de herramientas realice el procesamiento predeterminado del evento o **TRUE** para evitar que el control procese el evento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





