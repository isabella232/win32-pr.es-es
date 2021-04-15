---
title: Código de notificación de NM_CUSTOMDRAW (Button) (commctrl. h)
description: Notifica a la ventana primaria de un control de botón sobre las operaciones de dibujo personalizadas en el botón. El control de botón envía este código de notificación en forma de mensaje de notificación de WM \_ .
ms.assetid: cabe5515-ba64-4c53-8746-7a0559df8989
keywords:
- Controles de Windows de código de notificación de NM_CUSTOMDRAW (botón)
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
ms.openlocfilehash: ab3cc4eb73c3a0185131bb6ef2198458888ec89d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493318"
---
# <a name="nm_customdraw-button-notification-code"></a>Código de notificación de NM \_ CUSTOMDRAW (Button)

Notifica a la ventana primaria de un control de botón sobre las operaciones de dibujo personalizadas en el botón.

El control de botón envía este código de notificación en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contiene información sobre la operación de dibujo. El miembro **dwItemSpec** de esta estructura contiene el índice del elemento que se está dibujando y el miembro **lItemlParam** de esta estructura contiene el *lParam* del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor que la aplicación puede devolver depende de la fase de dibujo actual. El miembro **dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada contiene un valor que especifica la fase de dibujo. Debe devolver uno de los valores siguientes.



| Código devuelto                                                                                          | Descripción                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl> | El control notificará al elemento primario después de borrar un elemento. Solo se puede usar si **dwDrawStage** es igual a CDDS \_ preerase.<br/>                                  |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl> | El control notificará al elemento primario después de que se dibuje un elemento. Solo se puede usar si **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                 |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>     | La aplicación dibujó el elemento manualmente. El control no dibujará el elemento. Se puede usar cuando **dwDrawStage** es igual a CDDS \_ preerase o CDDS \_ PREPAINT.<br/> |



 

## <a name="remarks"></a>Observaciones

Si el control de botón está marcado como OwnerDraw (BS \_ OwnerDraw), el código de notificación de nm \_ CUSTOMDRAW no se envía.

Consulte [uso de Draw personalizado](custom-draw.md) para obtener más información.

> [!Note]  
> Para usar este código de notificación, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h (incluir Windows. h)</dt> </dl> |



 

 





