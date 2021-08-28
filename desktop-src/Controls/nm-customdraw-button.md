---
title: NM_CUSTOMDRAW de notificación (botón) (Commctrl.h)
description: Notifica a la ventana primaria de un control de botón las operaciones de dibujo personalizadas en el botón. El control de botón envía este código de notificación en forma de mensaje WM \_ NOTIFY.
ms.assetid: cabe5515-ba64-4c53-8746-7a0559df8989
keywords:
- NM_CUSTOMDRAW (botón) de notificación de Windows controles
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5930dd9023bac636fb645b7309c17cb4d70902b88a2b4f8a8ba857984a54ac1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061745"
---
# <a name="nm_customdraw-button-notification-code"></a>Código \_ de notificación DE NM CUSTOMDRAW (botón)

Notifica a la ventana primaria de un control de botón las operaciones de dibujo personalizadas en el botón.

El control de botón envía este código de notificación en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contiene información sobre la operación de dibujo. El **miembro dwItemSpec** de esta estructura contiene el índice del elemento que se está dibujando y el miembro **lItemlParam** de esta estructura contiene el *lParam del elemento.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor que la aplicación puede devolver depende de la fase de dibujo actual. El **miembro dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada contiene un valor que especifica la fase de dibujo. Debe devolver uno de los siguientes valores.



| Código devuelto                                                                                          | Descripción                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl> | El control notificará al elemento primario después de borrar un elemento. Esto solo se puede usar si **dwDrawStage** es igual a CDDS \_ PREERASE.<br/>                                  |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl> | El control notificará al elemento primario después de pintar un elemento. Esto solo se puede usar si **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                 |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>     | La aplicación ha dibujado el elemento manualmente. El control no dibujará el elemento. Se puede usar cuando **dwDrawStage** es igual a PREERASE de CDDS \_ o PREPAINT de CDDS. \_<br/> |



 

## <a name="remarks"></a>Comentarios

Si el control de botón está marcado como ownerdraw (BS OWNERDRAW), no se envía el código de notificación \_ \_ NM CUSTOMDRAW.

Consulte [Uso del dibujo personalizado para](custom-draw.md) obtener más información.

> [!Note]  
> Para usar este código de notificación, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Commctrl.h (incluir Windows.h)</dt> </dl> |



 

 





