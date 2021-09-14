---
title: WM_DPICHANGED_BEFOREPARENT mensaje (Winuser.h)
description: Para las ventanas de nivel superior por monitor v2, este mensaje se envía a todos los HWND del árbol HWDN secundario de la ventana que está experimentando un cambio de PPP. | WM_DPICHANGED_BEFOREPARENT mensaje (Winuser.h)
ms.assetid: EC8CC313-565F-451F-AE18-66F3B63303CE
keywords:
- WM_DPICHANGED_BEFOREPARENT con valores altos de PPP
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170250"
---
# <a name="wm_dpichanged_beforeparent-message"></a>Mensaje \_ WM PPPCHANGED \_ BEFOREPARENT

Para las ventanas de nivel superior por monitor [v2,](dpi-awareness-context.md) este mensaje se envía a todos los HWND del árbol HWDN secundario de la ventana que está experimentando un cambio de PPP. Este mensaje se produce antes de que la ventana de nivel superior reciba [**WM \_ PPPCHANGED**](wm-dpichanged.md)y recorre el árbol secundario desde abajo hacia arriba.


```C++
#define WM_DPICHANGED_BEFOREPARENT       0x02E2
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este valor no se usa y será cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este valor no se usa y será cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El sistema no usa este valor y lo omite.

## <a name="remarks"></a>Observaciones

No hay ningún control predeterminado de este mensaje en [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).

Este mensaje solo se envía cuando la ventana de nivel superior tiene un contexto de reconocimiento de PPP PMv2.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]<br/>                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WM \_ PPPCHANGED**](wm-dpichanged.md)
</dt> <dt>

[**WM \_ PPPCHANGED \_ AFTERPARENT**](wm-dpichanged-afterparent.md)
</dt> </dl>

 

