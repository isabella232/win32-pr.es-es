---
description: Una aplicación envía el mensaje DE WM FONTCHANGE a todas las ventanas de nivel superior del sistema después de \_ cambiar el grupo de recursos de fuente.
ms.assetid: 4774308e-2f18-4a35-a769-56871f3c29a2
title: WM_FONTCHANGE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b40650f0077ed854b87a6fd10e1dae610f0c3f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168330"
---
# <a name="wm_fontchange-message"></a>Mensaje \_ DE WM FONTCHANGE

Una aplicación envía el **mensaje \_ DE WM FONTCHANGE** a todas las ventanas de nivel superior del sistema después de cambiar el grupo de recursos de fuente.

Para enviar este mensaje, llame a la [**función SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con los parámetros siguientes.


```C++
SendMessage( 
  (HWND)  hWnd,              
  WM_FONTCHANGE,            
  (WPARAM)  wParam,          
  (LPARAM)  lParam            
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una aplicación que agrega o quita fuentes del sistema (por ejemplo, mediante la función [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) o [**RemoveFontResource)**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) debe enviar este mensaje a todas las ventanas de nivel superior.

Para enviar el **mensaje \_ DE WM FONTCHANGE** a todas las ventanas de nivel superior, una aplicación puede llamar a la función **SendMessage** con el parámetro *hwnd* establecido en HWND \_ BROADCAST.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre fuentes y texto](fonts-and-text.md)
</dt> <dt>

[Mensajes de fuente y texto](font-and-text-messages.md)
</dt> <dt>

[**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)
</dt> <dt>

[**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)
</dt> </dl>

 

 
