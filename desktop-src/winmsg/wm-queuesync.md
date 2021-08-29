---
description: Enviado por una aplicación de entrenamiento basado en equipos (CBT) para separar los mensajes de entrada del usuario de otros mensajes enviados a través del procedimiento \_ WH JOURNALPLAYBACK.
ms.assetid: 9ac265be-1fcc-476f-9dee-3e961340b5a1
title: WM_QUEUESYNC mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6db37a9e7eedc4d12c6750b150f31be1f77ad33da189c8333a4a2c788f45099d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710075"
---
# <a name="wm_queuesync-message"></a>Mensaje \_ QUEUESYNC de WM

Enviado por una aplicación de entrenamiento basado en equipos (CBT) para separar los mensajes de entrada del usuario de otros mensajes enviados a través del procedimiento [**\_ WH JOURNALPLAYBACK.**](about-hooks.md)


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

## <a name="remarks"></a>Comentarios

Cada vez que una aplicación CBT usa el [**procedimiento WH \_ JOURNALPLAYBACK,**](about-hooks.md) el primer y el último mensaje son **WM \_ QUEUESYNC.** Esto permite que la aplicación CBT intercepte y examine los mensajes iniciados por el usuario sin hacerlo para los eventos que envía.

Si una aplicación especifica un identificador de ventana **NULL,** el mensaje se publica en la cola de mensajes de la ventana activa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))
</dt> <dt>

[**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Enlaces](hooks.md)
</dt> </dl>

 

 
