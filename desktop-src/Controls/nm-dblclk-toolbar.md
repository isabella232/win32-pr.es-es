---
title: NM_DBLCLK de notificación (barra de herramientas) (Commctrl.h)
description: Notifica a la ventana primaria de un control de barra de herramientas que el usuario ha hecho doble clic en el botón izquierdo del mouse dentro del control. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: c6198245-cfd4-4e1f-877d-94c1d47e09d2
keywords:
- NM_DBLCLK (barra de herramientas) de notificación de Windows Controles
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
ms.openlocfilehash: 75abaf61938fbf377dbe8b6c5eaca99ff5ab027abe08c670de72a218dd51f1b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919665"
---
# <a name="nm_dblclk-toolbar-notification-code"></a>Código de \_ notificación de NM DBLCLK (barra de herramientas)

Notifica a la ventana primaria de un control de barra de herramientas que el usuario ha hecho doble clic en el botón izquierdo del mouse dentro del control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_DBLCLK

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
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





