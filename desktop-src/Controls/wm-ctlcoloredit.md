---
title: WM_CTLCOLOREDIT mensaje (Winuser.h)
description: Un control de edición que no es de solo lectura o está deshabilitado envía el mensaje WM CTLCOLOREDIT a su ventana primaria cuando el control está a punto \_ de dibujarse.
ms.assetid: 2294e3b8-00a7-43ef-b20a-fe0e46764055
keywords:
- WM_CTLCOLOREDIT controles de Windows mensaje
topic_type:
- apiref
api_name:
- WM_CTLCOLOREDIT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e100367f37018424fad33dc7cea30700183a0a2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165234"
---
# <a name="wm_ctlcoloredit-message"></a>Mensaje \_ CTLCOLOREDIT de WM

Un control de edición que no es de solo lectura o está deshabilitado envía el mensaje **\_ WM CTLCOLOREDIT** a su ventana primaria cuando el control está a punto de dibujarse. Al responder a este mensaje, la ventana primaria puede usar el identificador de contexto de dispositivo especificado para establecer el texto y los colores de fondo del control de edición.


```C++
WM_CTLCOLOREDIT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del contexto del dispositivo para la ventana de control de edición.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del control de edición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver el identificador de un pincel. El sistema usa el pincel para pintar el fondo del control de edición.

## <a name="remarks"></a>Observaciones

Si la aplicación devuelve un pincel que creó (por ejemplo, mediante la [**función CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect),**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) la aplicación debe liberar el pincel. Si la aplicación devuelve un pincel del sistema (por ejemplo, uno recuperado por la función [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush),**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) la aplicación no necesita liberar el pincel.

De forma predeterminada, [**la función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) selecciona los colores predeterminados del sistema para el control de edición.

Los controles de edición de solo lectura o deshabilitados no envían el mensaje **\_ CTLCOLOREDIT** de WM; en su lugar, envían el mensaje [**WM \_ CTLCOLORSTATIC.**](wm-ctlcolorstatic.md)

El **mensaje \_ WM CTLCOLOREDIT nunca** se envía entre subprocesos, solo se envía dentro del mismo subproceso.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en **int \_ PTR** y devolver el valor directamente. Si el procedimiento del cuadro de diálogo **devuelve FALSE,** se realiza el control de mensajes predeterminado. Se omite el valor MSGRESULT de DWL establecido por la función \_ [**SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

**Edición enriquecte:** No se admite este mensaje. Para establecer el color de fondo de un control de edición enriquecido, use el mensaje [**\_ EM SETBNDCOLOR.**](em-setbkgndcolor.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ SETBANDERNDCOLOR**](em-setbkgndcolor.md)
</dt> <dt>

[**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SeleccionarPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

