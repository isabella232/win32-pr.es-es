---
title: EN_LINK de notificación (Richedit.h)
description: Un control rich edit envía códigos de notificación EN LINK cuando recibe varios mensajes, por ejemplo, cuando el usuario hace clic en el mouse o cuando el puntero del mouse está sobre el texto que tiene el efecto \_ CFE \_ LINK.
ms.assetid: 67f02908-957e-4d91-8a70-70399ce9cf2e
keywords:
- EN_LINK código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_LINK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3398f79a94982a8b7c843747f38f16431cad6a061388367037d259cfe862d468
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047665"
---
# <a name="en_link-notification-code"></a>Código de notificación de EN \_ LINK

Un control rich edit envía códigos de notificación EN LINK cuando recibe varios mensajes, por ejemplo, cuando el usuario hace clic en el mouse o cuando el puntero del mouse está sobre el texto que tiene el efecto \_ **CFE \_ LINK.** Un control rich edit sin ventanas envía esta notificación mediante el [**método ITextHost::TxNotify.**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) La ventana primaria del control recibe este código de notificación a través de un [**mensaje \_ WM NOTIFY.**](wm-notify.md)


```C++
EN_LINK

    penLink = (ENLINK *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de ventana recuperado mediante una llamada a [**la función GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) con el valor de identificador de GWL. \_

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura ENLINK.**](/windows/desktop/api/Richedit/ns-richedit-enlink) La estructura contiene una estructura [**NMHDR,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) información sobre el código de notificación y una estructura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) que indica el intervalo de caracteres que tienen el **efecto CFE \_ LINK.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para permitir que el control continúe con su control normal del mensaje.

Devuelve un valor distinto de cero para evitar que el control controle el mensaje.

**Windows 8:** devuelve **EN \_ LINK DO \_ \_ DEFAULT** para dirigir el control rich edit para realizar la acción predeterminada.

## <a name="remarks"></a>Comentarios

Para recibir **códigos de notificación de EN \_ LINK** cuando el vínculo tiene el foco, especifique la marca [**ENM \_ LINK**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**EM \_ SETEVENTMASK.**](em-seteventmask.md)

Si el vínculo no tiene foco, para recibir códigos de notificación **EN \_ LINK,** especifique la marca **SES \_ NOFOCUSLINKNOTIFY** en la máscara enviada con el mensaje [**EM \_ SETEDITSTYLE.**](em-seteditstyle.md)

Un control rich edit envía códigos de notificación **EN \_ LINK** cuando recibe los mensajes siguientes mientras el puntero del mouse está sobre el texto que tiene el **efecto CFE \_ LINK:**

-   [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk)
-   [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)
-   [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)
-   [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)
-   [**WM \_ RBUTTONDBLCLK**](/windows/desktop/inputdev/wm-rbuttondblclk)
-   [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown)
-   [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)
-   [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor)

El **efecto CFE \_ LINK** normalmente identifica un intervalo de texto que contiene una dirección URL. Las aplicaciones pueden controlar el código de notificación de EN LINK cambiando el puntero del mouse cuando está sobre la dirección URL o iniciando un explorador para ver la ubicación identificada \_ por la dirección URL.

Si envía el mensaje [**EM \_ AUTOURLDETECT**](em-autourldetect.md) para habilitar la detección automática de direcciones URL, el control de edición enriquecido establece automáticamente el efecto **CFE \_ LINK** para el texto modificado que identifica como una dirección URL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> <dt>

[**EM \_ AUTOURLDETECT**](em-autourldetect.md)
</dt> <dt>

[**ENLINK**](/windows/desktop/api/Richedit/ns-richedit-enlink)
</dt> <dt>

[**ITextRange2::SetURL**](/windows/desktop/api/Tom/nf-tom-itextrange2-seturl)
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> </dl>

 

