---
title: Código de notificación de EN_LINK (RichEdit. h)
description: Un control Rich Edit envía \_ códigos de notificación en vínculo cuando recibe varios mensajes, por ejemplo, cuando el usuario hace clic con el mouse o cuando el puntero del mouse se encuentra sobre texto que tiene el \_ efecto de vínculo CFE.
ms.assetid: 67f02908-957e-4d91-8a70-70399ce9cf2e
keywords:
- EN_LINK controles de código de notificación de Windows
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
ms.openlocfilehash: ec0eeb134804f671502d4cd3abbe2cb6995194af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492448"
---
# <a name="en_link-notification-code"></a>\_Código de notificación en vínculo

Un control Rich Edit envía \_ códigos de notificación en vínculo cuando recibe varios mensajes, por ejemplo, cuando el usuario hace clic con el mouse o cuando el puntero del mouse se encuentra sobre texto que tiene el efecto de **\_ vínculo CFE** . Un control Rich Edit sin ventanas envía esta notificación mediante el método [**ITextHost:: TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) . La ventana primaria del control recibe este código de notificación a través de un mensaje de notificación de [**WM \_**](wm-notify.md) .


```C++
EN_LINK

    penLink = (ENLINK *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

IDENTIFICADOR de ventana que se ha recuperado mediante una llamada a la función [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) con el valor de identificador de GWL \_ .

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura de [**vínculo**](/windows/desktop/api/Richedit/ns-richedit-enlink) . La estructura contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , información sobre el código de notificación y una estructura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) que indica el intervalo de caracteres que tienen el efecto **CFE \_ Link** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para permitir que el control continúe con su control normal del mensaje.

Devuelve un valor distinto de cero para evitar que el control controle el mensaje.

**Windows 8**: de **\_ \_ \_ forma predeterminada** , el vínculo devuelto en es dirigir el control Rich Edit para realizar la acción predeterminada.

## <a name="remarks"></a>Observaciones

Para recibir los códigos de notificación en **\_ vínculo** cuando el vínculo tenga el foco, especifique la marca de [**\_ vínculo ENM**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .

Si el vínculo no tiene el foco, para recibir los códigos de notificación **en el \_ vínculo** , especifique la marca **SES \_ NOFOCUSLINKNOTIFY** en la máscara enviada con el mensaje [**\_ SETEDITSTYLE em**](em-seteditstyle.md) .

Un control Rich Edit envía códigos de notificación **en \_ vínculos** cuando recibe los mensajes siguientes mientras el puntero del mouse se encuentra sobre el texto que tiene el efecto de **\_ vínculo CFE** :

-   [**LBUTTONDBLCLK de WM \_**](/windows/desktop/inputdev/wm-lbuttondblclk)
-   [**LBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-lbuttondown)
-   [**LBUTTONUP de WM \_**](/windows/desktop/inputdev/wm-lbuttonup)
-   [**MOUSEMOVE de WM \_**](/windows/desktop/inputdev/wm-mousemove)
-   [**RBUTTONDBLCLK de WM \_**](/windows/desktop/inputdev/wm-rbuttondblclk)
-   [**RBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-rbuttondown)
-   [**RBUTTONUP de WM \_**](/windows/desktop/inputdev/wm-rbuttonup)
-   [**SETCURSOR de WM \_**](/windows/desktop/menurc/wm-setcursor)

El efecto de **\_ vínculo CFE** normalmente identifica un intervalo de texto que contiene una dirección URL. Las aplicaciones pueden controlar el \_ código de notificación de vínculo en el vínculo en el puntero del mouse cuando está sobre la dirección URL o iniciando un explorador para ver la ubicación identificada por la dirección URL.

Si envía el mensaje [**\_ AUTOURLDETECT em**](em-autourldetect.md) para habilitar la detección automática de direcciones URL, el control Rich Edit establece automáticamente el efecto **CFE \_ Link** para el texto modificado que identifica como dirección URL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> <dt>

[**\_AUTOURLDETECT em**](em-autourldetect.md)
</dt> <dt>

[**VÍNCULO**](/windows/desktop/api/Richedit/ns-richedit-enlink)
</dt> <dt>

[**ITextRange2:: SetURL**](/windows/desktop/api/Tom/nf-tom-itextrange2-seturl)
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> </dl>

 

