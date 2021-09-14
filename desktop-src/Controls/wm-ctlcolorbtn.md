---
title: WM_CTLCOLORBTN mensaje (Winuser.h)
description: El mensaje \_ WM CTLCOLORBTN se envía a la ventana primaria de un botón antes de dibujar el botón. La ventana primaria puede cambiar los colores de texto y fondo del botón. Sin embargo, solo los botones dibujados por el propietario responden a la ventana primaria que procesa este mensaje.
ms.assetid: fd2ab917-ffd6-4f71-9b1c-0ecdfe53ae8b
keywords:
- WM_CTLCOLORBTN controles de Windows mensaje
topic_type:
- apiref
api_name:
- WM_CTLCOLORBTN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfdaed4682cbd87bfd86d7829f7c828494ec46fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165237"
---
# <a name="wm_ctlcolorbtn-message"></a>Mensaje \_ CTLCOLORBTN de WM

El **mensaje \_ WM CTLCOLORBTN** se envía a la ventana primaria de un botón antes de dibujar el botón. La ventana primaria puede cambiar los colores de texto y fondo del botón. Sin embargo, solo los botones dibujados por el propietario responden a la ventana primaria que procesa este mensaje.


```C++
WM_CTLCOLORBTN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

HDC **que** especifica el identificador del contexto de presentación del botón.

</dd> <dt>

*lParam* 
</dt> <dd>

HWND **que** especifica el identificador del botón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver un identificador a un pincel. El sistema usa el pincel para pintar el fondo del botón.

## <a name="remarks"></a>Observaciones

Si la aplicación devuelve un pincel que creó (por ejemplo, mediante las funciones [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect),**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) la aplicación debe liberar el pincel. Si la aplicación devuelve un pincel del sistema (por ejemplo, uno recuperado por la función [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush),**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) la aplicación no necesita liberar el pincel.

De forma predeterminada, [**la función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) selecciona los colores predeterminados del sistema para el botón. Los [**botones con los estilos \_ BS PUSHBUTTON**](button-styles.md), [**BS \_ DEFPUSHBUTTON**](button-styles.md)o [**BS \_ PUSHLIKE**](button-styles.md) no usan el pincel devuelto. Los botones con estos estilos siempre se dibujan con los colores predeterminados del sistema. Los botones de inserción de dibujo requieren varios pinceles diferentes(cara, resaltado y sombra), pero el mensaje **\_ WM CTLCOLORBTN solo** permite devolver un pincel. Para proporcionar una apariencia personalizada para los botones de inserción, use un botón dibujado por el propietario. Para obtener más información, vea [Creating Owner-Drawn Controls](user-controls-intro.md).

El **mensaje \_ WM CTLCOLORBTN** nunca se envía entre subprocesos. Solo se envía dentro de un subproceso.

El color de texto de una casilla o botón de radio se aplica a la casilla o botón, a su marca de verificación y al texto. El rectángulo de foco de estos botones sigue siendo el color predeterminado del sistema (normalmente negro). El color de texto de un cuadro de grupo se aplica al texto, pero no a la línea que define el cuadro. El color de texto de un botón de inserción solo se aplica a su rectángulo de foco; no afecta al color del texto.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en **int \_ PTR** y devolver el valor directamente. Si el procedimiento del cuadro de diálogo **devuelve FALSE**, se realiza el control de mensajes predeterminado. Se omite el valor MSGRESULT de DWL establecido por la función \_ [**SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Otros recursos**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SeleccionePalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

