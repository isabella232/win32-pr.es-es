---
title: TBN_RESET de notificación (Commctrl.h)
description: Notifica a la ventana primaria de la barra de herramientas que el usuario ha restablecido el contenido del cuadro de diálogo Personalizar barra de herramientas. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 55efba85-b453-48b9-83df-76820249e7a8
keywords:
- TBN_RESET código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_RESET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 117ee2a50445ffe4dd8cd23d952fde7836bcf023
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166322"
---
# <a name="tbn_reset-notification-code"></a>Código de notificación \_ DE RESTABLECIMIENTO DE TBN

Notifica a la ventana primaria de la barra de herramientas que el usuario ha restablecido el contenido del cuadro de diálogo Personalizar barra de herramientas. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_RESET 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve TBNRF \_ ENDCUSTOMIZE para cerrar el cuadro de diálogo Personalizar barra de herramientas. Se omiten todos los demás valores devueltos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





