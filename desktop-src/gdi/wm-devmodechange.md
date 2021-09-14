---
description: El mensaje WM DEVMODECHANGE se envía a todas las ventanas de nivel superior cada vez que \_ el usuario cambia la configuración del modo de dispositivo.
ms.assetid: 06b625a8-7584-4a98-b8e7-f1de668c274e
title: WM_DEVMODECHANGE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 068e74264a7492bbb1e685fe6de110e909698374
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072445"
---
# <a name="wm_devmodechange-message"></a>Mensaje \_ WM DEVMODECHANGE

El **mensaje \_ WM DEVMODECHANGE** se envía a todas las ventanas de nivel superior cada vez que el usuario cambia la configuración del modo de dispositivo.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador a una ventana.

</dd> <dt>

*uMsg* 
</dt> <dd>

WM \_ DEVMODECHANGE

</dd> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una cadena que especifica el nombre del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Este mensaje no se puede enviar directamente a una ventana. Para enviar el **mensaje \_ WM DEVMODECHANGE** a todas las ventanas de nivel superior, use la función [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) con el parámetro *hWnd* establecido en HWND \_ BROADCAST.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Introducción a los contextos de dispositivo](device-contexts.md)
</dt> <dt>

[Mensajes de contexto de dispositivo](device-context-messages.md)
</dt> </dl>

 

 
