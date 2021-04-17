---
title: Código de notificación de TVN_SETDISPINFO (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que debe actualizar la información que mantiene sobre un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- TVN_SETDISPINFO controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656485"
---
# <a name="tvn_setdispinfo-notification-code"></a>Código de notificación de SETDISPINFO de TVN \_

Notifica a la ventana primaria de un control de vista de árbol que debe actualizar la información que mantiene sobre un elemento. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TVN_SETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) que describe el elemento que se está actualizando. El miembro **hItem** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) especifica el elemento que se va a actualizar y el miembro **Mask** especifica los atributos del elemento que se van a actualizar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

Si el miembro **miembros pszText** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) del elemento es el \_ valor LPSTR TEXTCALLBACK, el control envía esta notificación para establecer el texto del elemento. En este caso, el miembro de **máscara** de *lParam* tendrá establecido el \_ indicador de texto TVIF.

Si el miembro **iImage** o **iSelectedImage** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) del elemento es el \_ valor I IMAGECALLBACK, el control envía esta notificación para recuperar el índice de la imagen del icono que se va a mostrar. En este caso, el miembro de **máscara** de *lParam* tendrá la \_ marca TVIF o TVIF \_ SELECTEDIMAGE establecida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ SETDISPINFOW** (Unicode) y **TVN \_ SETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[TVN \_ GETDISPINFO](tvn-getdispinfo.md)
</dt> </dl>

 

 





