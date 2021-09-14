---
title: TVN_GETDISPINFO de notificación (Commctrl.h)
description: Solicita que la ventana primaria de un control de vista de árbol proporcione la información necesaria para mostrar u ordenar un elemento. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 2dfe41d8-1164-481b-ac07-8faba43c562a
keywords:
- TVN_GETDISPINFO de notificación Windows controles
topic_type:
- apiref
api_name:
- TVN_GETDISPINFO
- TVN_GETDISPINFOA
- TVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a09bcc683ba9cf2d89a796e63812381254588a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165569"
---
# <a name="tvn_getdispinfo-notification-code"></a>Código de notificación \_ GETDISPINFO de TVN

Solicita que la ventana primaria de un control de vista de árbol proporcione la información necesaria para mostrar u ordenar un elemento. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_GETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) El **miembro** de elemento es una [**estructura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) cuyos miembros **mask**, **hItem**, **state** y **lParam** especifican el tipo de información necesaria. Debe rellenar los miembros de la estructura con la información adecuada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

Este código de notificación se envía en las siguientes circunstancias:

-   Si el **miembro pszText** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) del elemento es el valor LPSTR TEXTCALLBACK, el control envía este código de notificación para recuperar el \_ texto del elemento. En este caso, el **miembro mask** de *lParam* tendrá establecida la marca TEXT de TVIF. \_
-   Si el **miembro iImage** o **iSelectedImage** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) del elemento es el valor I IMAGECALLBACK, el control envía este código de notificación para recuperar el índice de los iconos de un elemento en la lista de imágenes del \_ control. En este caso, si el elemento está seleccionado, el miembro **mask** de *lParam* tendrá establecida la marca \_ TVIF SELECTEDIMAGE. Si el elemento no está seleccionado, el miembro **mask** de *lParam* tendrá establecida la marca DE IMAGEN DE TVIF. \_
-   Si el **miembro cChildren** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) del elemento es el valor I CHILDRENCALLBACK, el control envía este código de notificación para recuperar un valor que indica si el elemento tiene elementos \_ secundarios. En este caso, el **miembro mask** de *lParam* tendrá establecida la marca CHILDREN de TVIF. \_

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ GETDISPINFOW** (Unicode) y **TVN \_ GETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[TVN \_ SETDISPINFO](tvn-setdispinfo.md)
</dt> </dl>

 

 





