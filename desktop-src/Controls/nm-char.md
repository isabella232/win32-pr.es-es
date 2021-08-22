---
title: NM_CHAR de notificación (Commctrl.h)
description: Un control envía el código de notificación NM CHAR cuando se procesa \_ una clave de carácter. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- NM_CHAR código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73c35871410244bfb69f67c7e0b2c960d0dd50d432ad9cdcfd8765c7df449bf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018953"
---
# <a name="nm_char-notification-code"></a>Código \_ de notificación NM CHAR

Un control envía el código de notificación NM CHAR cuando se procesa \_ una clave de carácter. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) que contiene información adicional sobre el carácter que produjo el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La mayoría de los controles omiten el valor devuelto. Para obtener más información, consulte la documentación de los controles individuales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[NM \_ CHAR (barra de herramientas)](nm-char-toolbar.md)
</dt> </dl>

 

 





