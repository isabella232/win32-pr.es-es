---
title: NM_CHAR de notificación (barra de herramientas) (Commctrl.h)
description: Enviado por una barra de herramientas cuando recibe un mensaje \_ WM CHAR. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 7bf0b046-da8e-448f-94e1-62ba0989f7ba
keywords:
- NM_CHAR código de notificación (barra de herramientas) Windows controles
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
ms.openlocfilehash: a318c7385e9d7205ad0fa159e1f987c5d650d27414eefeed4d915c5544cb4564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018943"
---
# <a name="nm_char-toolbar-notification-code"></a>Código de \_ notificación NM CHAR (barra de herramientas)

Enviado por una barra de herramientas cuando recibe un [**mensaje \_ WM CHAR.**](/windows/desktop/inputdev/wm-char) Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) que contiene información adicional sobre el carácter que produjo el código de notificación. El **miembro dwItemPrev** de esta estructura contiene el identificador de comando del elemento que está activo actualmente o -1 si ningún elemento está activo actualmente. El **miembro dwItemNext** de esta estructura contiene el identificador de comando del elemento que se volverá activo o -1 si la clave no coincide con el acelerador de ningún elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE para** indicar que la barra de herramientas no debe procesar el carácter y **FALSE** para que la barra de herramientas procese el carácter.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

