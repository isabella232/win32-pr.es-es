---
title: Mensaje de WM_DPICHANGED_AFTERPARENT (Winuser. h)
description: En el caso de las ventanas de nivel superior de por monitor V2, este mensaje se envía a todos los HWND del árbol de HWDN secundario de la ventana que está experimentando un cambio de PPP. | Mensaje de WM_DPICHANGED_AFTERPARENT (Winuser. h)
ms.assetid: FEA1BF07-55B6-4584-ABD3-340515831E0A
keywords:
- WM_DPICHANGED_AFTERPARENT máximo de PPP del mensaje
topic_type:
- apiref
api_name:
- WM_DPICHANGED_AFTERPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cc76602662cefba42f62bd3ed85913ade40f15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689844"
---
# <a name="wm_dpichanged_afterparent-message"></a>\_Mensaje AFTERPARENT de DPICHANGED de WM \_

En el caso de las ventanas de nivel superior de [por monitor V2](dpi-awareness-context.md) , este mensaje se envía a todos los HWND del árbol de HWDN secundario de la ventana que está experimentando un cambio de PPP. Este mensaje se produce después de que la ventana de nivel superior reciba [**WM \_ DPICHANGED**](wm-dpichanged.md)y recorra el árbol secundario de arriba abajo.


```C++
#define WM_DPICHANGED_AFTERPARENT       0x02E3
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

[**\_BEFOREPARENT DPICHANGED \_ WM**](wm-dpichanged-beforeparent.md)
</dt> </dl>

 

