---
title: Mensaje de WM_DPICHANGED_BEFOREPARENT (Winuser. h)
description: En el caso de las ventanas de nivel superior de por monitor V2, este mensaje se envía a todos los HWND del árbol de HWDN secundario de la ventana que está experimentando un cambio de PPP. | Mensaje de WM_DPICHANGED_BEFOREPARENT (Winuser. h)
ms.assetid: EC8CC313-565F-451F-AE18-66F3B63303CE
keywords:
- WM_DPICHANGED_BEFOREPARENT máximo de PPP del mensaje
topic_type:
- apiref
api_name:
- WM_DPICHANGED_BEFOREPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16641916cb16b789f2349a53b09dbd2af5f520f3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003718"
---
# <a name="wm_dpichanged_beforeparent-message"></a>\_Mensaje BEFOREPARENT de DPICHANGED de WM \_

En el caso de las ventanas de nivel superior de [por monitor V2](dpi-awareness-context.md) , este mensaje se envía a todos los HWND del árbol de HWDN secundario de la ventana que está experimentando un cambio de PPP. Este mensaje se produce antes de que la ventana de nivel superior reciba [**WM \_ DPICHANGED**](wm-dpichanged.md)y recorra el árbol secundario de abajo.


```C++
#define WM_DPICHANGED_BEFOREPARENT       0x02E2
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este valor no se utiliza y será cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este valor no se utiliza y será cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El sistema no utiliza este valor y lo omite.

## <a name="remarks"></a>Observaciones

No hay ningún control predeterminado de este mensaje en [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).

Este mensaje solo se envía cuando la ventana de nivel superior tiene un contexto de reconocimiento de PPP de PMv2.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DPICHANGED de WM \_**](wm-dpichanged.md)
</dt> <dt>

[**\_AFTERPARENT DPICHANGED \_ WM**](wm-dpichanged-afterparent.md)
</dt> </dl>

 

