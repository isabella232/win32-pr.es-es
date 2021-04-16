---
title: Código de notificación de TVN_GETDISPINFO (commctrl. h)
description: Solicita que la ventana primaria de un control de vista de árbol proporcione la información necesaria para mostrar u ordenar un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 2dfe41d8-1164-481b-ac07-8faba43c562a
keywords:
- TVN_GETDISPINFO controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534215"
---
# <a name="tvn_getdispinfo-notification-code"></a>Código de notificación de GETDISPINFO de TVN \_

Solicita que la ventana primaria de un control de vista de árbol proporcione la información necesaria para mostrar u ordenar un elemento. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TVN_GETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) . El miembro del **elemento** es una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) cuyos miembros **Mask**, **hItem**, **State** e **lParam** especifican el tipo de información necesaria. Debe rellenar los miembros de la estructura con la información adecuada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

Este código de notificación se envía en las siguientes circunstancias:

-   Si el miembro **miembros pszText** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) del elemento es el \_ valor LPSTR TEXTCALLBACK, el control envía este código de notificación para recuperar el texto del elemento. En este caso, el miembro de **máscara** de *lParam* tendrá establecido el \_ indicador de texto TVIF.
-   Si el miembro **iImage** o **iSelectedImage** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) del elemento es el \_ valor I IMAGECALLBACK, el control envía este código de notificación para recuperar el índice de los iconos de un elemento en la lista de imágenes del control. En este caso, si el elemento está seleccionado, el miembro de **máscara** de *lParam* tendrá la \_ marca TVIF SELECTEDIMAGE establecida. Si el elemento no está seleccionado, el miembro de **máscara** de *lParam* tendrá establecido el \_ indicador de imagen TVIF.
-   Si el miembro **cChildren** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) del elemento es el \_ valor I CHILDRENCALLBACK, el control envía este código de notificación para recuperar un valor que indica si el elemento tiene elementos secundarios. En este caso, el miembro de **máscara** de *lParam* tendrá establecido el \_ marcador de TVIF Children.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ GETDISPINFOW** (Unicode) y **TVN \_ GETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[TVN \_ SETDISPINFO](tvn-setdispinfo.md)
</dt> </dl>

 

 





