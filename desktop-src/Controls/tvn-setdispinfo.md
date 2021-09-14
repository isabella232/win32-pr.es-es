---
title: TVN_SETDISPINFO de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de árbol que debe actualizar la información que mantiene sobre un elemento. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- TVN_SETDISPINFO código de notificación Windows controles
topic_type:
- apiref
api_name:
- TVN_SETDISPINFO
- TVN_SETDISPINFOA
- TVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b03e60ba7d8e6d7851c62fac030bd252cf957d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165530"
---
# <a name="tvn_setdispinfo-notification-code"></a>Código de notificación \_ SETDISPINFO de TVN

Notifica a la ventana primaria de un control de vista de árbol que debe actualizar la información que mantiene sobre un elemento. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_SETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) que describe el elemento que se está actualizando. El **miembro hItem** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) especifica el elemento que se está actualizando y el miembro **mask** especifica qué atributos del elemento se están actualizando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

Si el **miembro pszText** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) del elemento es el valor LPSTR TEXTCALLBACK, el control envía esta notificación para establecer el texto \_ del elemento. En este caso, el **miembro mask** de *lParam* tendrá establecida la marca TEXT de TVIF. \_

Si el **miembro iImage** o **iSelectedImage** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) del elemento es el valor I IMAGECALLBACK, el control envía esta notificación para recuperar el índice de la imagen de icono que se va a \_ mostrar. En este caso, el miembro **mask** de *lParam* tendrá establecida la marca TVIF IMAGE o \_ TVIF \_ SELECTEDIMAGE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ SETDISPINFOW** (Unicode) y **TVN \_ SETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[TVN \_ GETDISPINFO](tvn-getdispinfo.md)
</dt> </dl>

 

 





