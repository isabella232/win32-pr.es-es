---
description: Indica una solicitud para finalizar una aplicación y se genera cuando la aplicación llama a la función PostQuitMessage. Este mensaje hace que la función GetMessage devuelva cero.
ms.assetid: a9bff5dc-cab8-4e08-838e-d92c87c265d6
title: WM_QUIT mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f6b999ff23d964c1998fe1cc2a9991e11ecfe71760800b1d678e2f71b89273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881525"
---
# <a name="wm_quit-message"></a>Mensaje DE SALIDA DE WM \_

Indica una solicitud para finalizar una aplicación y se genera cuando la aplicación llama a la [**función PostQuitMessage.**](/windows/win32/api/winuser/nf-winuser-postquitmessage) Este mensaje hace que [**la función GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) devuelva cero.


```C++
#define WM_QUIT                         0x0012
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Código de salida dado en la [**función PostQuitMessage.**](/windows/win32/api/winuser/nf-winuser-postquitmessage)

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Este mensaje no tiene un valor devuelto porque hace que el bucle de mensajes finalice antes de que el mensaje se envíe al procedimiento de ventana de la aplicación.

## <a name="remarks"></a>Comentarios

El **mensaje DE SALIDA \_ de WM** no está asociado a una ventana y, por tanto, nunca se recibirá a través del procedimiento de ventana de una ventana. Solo la recuperan las funciones [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) [**o PeekMessage.**](/windows/win32/api/winuser/nf-winuser-peekmessagea)

No publique el mensaje **WM \_ QUIT** mediante la [**función PostMessage;**](/windows/win32/api/winuser/nf-winuser-postmessagea) use [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
