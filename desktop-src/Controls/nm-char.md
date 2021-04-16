---
title: Código de notificación de NM_CHAR (commctrl. h)
description: '\_Un control envía el código de notificación nm char cuando se procesa una tecla de carácter. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.'
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- NM_CHAR controles de código de notificación de Windows
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
ms.openlocfilehash: e0910736bcb174c2f3ddb16174c153f4b22ac5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658412"
---
# <a name="nm_char-notification-code"></a>\_Código de notificación nm Char

\_Un control envía el código de notificación nm char cuando se procesa una tecla de carácter. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) que contiene información adicional sobre el carácter que causó el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La mayoría de los controles omiten el valor devuelto. Para obtener más información, consulte la documentación de los controles individuales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[NM \_ Char (barra de herramientas)](nm-char-toolbar.md)
</dt> </dl>

 

 





