---
title: NM_LDOWN de notificación (barra de herramientas) (Commctrl.h)
description: Notifica a la ventana primaria de una barra de herramientas que se ha presionado el botón izquierdo del mouse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: f5b356fb-265b-4eb0-a5a3-2a22d688f847
keywords:
- NM_LDOWN de notificación (barra de herramientas) de Windows controles
topic_type:
- apiref
api_name:
- NM_LDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf283e8b3e0d1ed780a80d5608849bc42f200b61a5a94692c0924cb2e6241a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919655"
---
# <a name="nm_ldown-toolbar-notification-code"></a>Código de \_ notificación de NM LDOWN (barra de herramientas)

Notifica a la ventana primaria de una barra de herramientas que se ha presionado el botón izquierdo del mouse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_LDOWN

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

## <a name="remarks"></a>Comentarios

Esta notificación se envía después de que se haya enviado el código de notificación DE LISTA DESPLEGABLE de [TBN. \_ ](tbn-dropdown.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





