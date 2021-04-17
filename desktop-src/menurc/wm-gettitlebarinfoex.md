---
title: Mensaje de WM_GETTITLEBARINFOEX (Winuser. h)
description: Se envía para solicitar información de la barra de título extendida. Una ventana recibe este mensaje a través de su función WindowProc.
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
ms.openlocfilehash: fea31326faf5953df0facf34b58b06d7766c2e7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422053"
---
# <a name="wm_gettitlebarinfoex-message"></a>Mensaje de GETTITLEBARINFOEX de WM \_

Se envía para solicitar información de la barra de título extendida. Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_GETTITLEBARINFOEX            0x033F
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser 0.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) . El remitente del mensaje es responsable de la asignación de memoria para esta estructura. Establezca el miembro **cbSize** de esta estructura en `sizeof(TITLEBARINFOEX)` antes de pasar esta estructura con el mensaje.

</dd> </dl>

## <a name="remarks"></a>Observaciones

En el ejemplo siguiente se muestra cómo el receptor del mensaje convierte un valor **lParam** para recuperar la estructura [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) .

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre menús](menus.md)
</dt> </dl>

 

