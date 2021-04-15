---
description: El mensaje de DEVMODECHANGE de WM \_ se envía a todas las ventanas de nivel superior cada vez que el usuario cambia la configuración del modo de dispositivo.
ms.assetid: 06b625a8-7584-4a98-b8e7-f1de668c274e
title: Mensaje de WM_DEVMODECHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 068e74264a7492bbb1e685fe6de110e909698374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985806"
---
# <a name="wm_devmodechange-message"></a>Mensaje de DEVMODECHANGE de WM \_

El mensaje de **\_ DEVMODECHANGE de WM** se envía a todas las ventanas de nivel superior cada vez que el usuario cambia la configuración del modo de dispositivo.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

*identificador* 
</dt> <dd>

Identificador a una ventana.

</dd> <dt>

*uMsg* 
</dt> <dd>

DEVMODECHANGE de WM \_

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

Este mensaje no se puede enviar directamente a una ventana. Para enviar el mensaje de **\_ DEVMODECHANGE de WM** a todas las ventanas de nivel superior, use la función [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) con el parámetro *hWnd* establecido en la \_ difusión HWND.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción a los contextos de dispositivo](device-contexts.md)
</dt> <dt>

[Mensajes de contexto de dispositivo](device-context-messages.md)
</dt> </dl>

 

 
