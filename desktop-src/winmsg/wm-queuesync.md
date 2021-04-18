---
description: Enviado por una aplicación de aprendizaje basado en PC (CBT) para separar los mensajes de entrada del usuario de otros mensajes enviados mediante el \_ procedimiento qu JOURNALPLAYBACK.
ms.assetid: 9ac265be-1fcc-476f-9dee-3e961340b5a1
title: Mensaje de WM_QUEUESYNC (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d859f858ab7cf8182282cc20dbf514cfc2d9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648387"
---
# <a name="wm_queuesync-message"></a>Mensaje de QUEUESYNC de WM \_

Enviado por una aplicación de aprendizaje basado en PC (CBT) para separar los mensajes de entrada del usuario de otros mensajes enviados mediante el procedimiento [**qu \_ JOURNALPLAYBACK**](about-hooks.md) .


```C++
#define WM_QUEUESYNC                    0x0023
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

## <a name="return-value"></a>Valor devuelto

Tipo: **void**

Una aplicación CBT debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Cada vez que una aplicación CBT usa el procedimiento [**qu \_ JOURNALPLAYBACK**](about-hooks.md) , el primero y el último mensaje son **WM \_ QUEUESYNC**. Esto permite que la aplicación CBT intercepte y examine los mensajes iniciados por el usuario sin necesidad de hacerlo para los eventos que envía.

Si una aplicación especifica un identificador de ventana **nulo** , el mensaje se envía a la cola de mensajes de la ventana activa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))
</dt> <dt>

[**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

**Vista**
</dt> <dt>

[Enlaces](hooks.md)
</dt> </dl>

 

 
