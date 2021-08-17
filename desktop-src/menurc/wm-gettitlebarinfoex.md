---
title: WM_GETTITLEBARINFOEX mensaje (Winuser.h)
description: Se envía para solicitar información extendida de la barra de título. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 0760dbf1-5b20-471c-bfd9-b8d28b52074b
keywords:
- WM_GETTITLEBARINFOEX menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_GETTITLEBARINFOEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1acbe85afa1871caf796c70a9535f5646d2511317a0e9ee0564db55101a16449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869671"
---
# <a name="wm_gettitlebarinfoex-message"></a>Mensaje \_ GETTITLEBARINFOEX de WM

Se envía para solicitar información extendida de la barra de título. Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_GETTITLEBARINFOEX            0x033F
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa y debe ser 0.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TITLEBARINFOEX.**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) El remitente del mensaje es responsable de asignar memoria para esta estructura. Establezca el **miembro cbSize** de esta estructura en `sizeof(TITLEBARINFOEX)` antes de pasar esta estructura con el mensaje .

</dd> </dl>

## <a name="remarks"></a>Comentarios

En el ejemplo siguiente se muestra cómo el receptor del mensaje convierte un **valor LPARAM** para recuperar la [**estructura TITLEBARINFOEX.**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex)

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción a los menús](menus.md)
</dt> </dl>

 

