---
title: WM_ACTIVATE mensaje (Winuser.h)
description: Se envía tanto a la ventana que se activa como a la ventana que se está desactivando.
ms.assetid: a62bb9f7-f286-4d0d-a1ca-370950c188b2
keywords:
- WM_ACTIVATE entrada de teclado y mouse
topic_type:
- apiref
api_name:
- WM_ACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec28662aa2219ee9b3ad2e8cc8efac861d292f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468834"
---
# <a name="wm_activate-message"></a>Mensaje \_ DE WM ACTIVATE

Se envía tanto a la ventana que se activa como a la ventana que se está desactivando. Si las ventanas usan la misma cola de entrada, el mensaje se envía sincrónicamente, primero al procedimiento de ventana de la ventana de nivel superior que se desactiva y, a continuación, al procedimiento de ventana de la ventana de nivel superior que se está activando. Si las ventanas usan colas de entrada diferentes, el mensaje se envía de forma asincrónica, por lo que la ventana se activa inmediatamente.


```C++
#define WM_ACTIVATE                     0x0006
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden bajo especifica si la ventana se está activando o desactivando. Este parámetro puede ser uno de los valores siguientes. La palabra de orden superior especifica el estado minimizado de la ventana que se está activando o desactivando. Un valor distinto de cero indica que la ventana está minimizada.



| Value                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WA_ACTIVE"></span><span id="wa_active"></span><dl> <dt>**WA \_ ACTIVE**</dt> <dt>1</dt> </dl>                | Activado por algún método que no sea un clic del mouse (por ejemplo, mediante una llamada a la función [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) o mediante el uso de la interfaz de teclado para seleccionar la ventana).<br/> |
| <span id="WA_CLICKACTIVE"></span><span id="wa_clickactive"></span><dl> <dt>**WA \_ CLICKACTIVE**</dt> <dt>2</dt> </dl> | Activado con un clic del mouse.<br/>                                                                                                                                                                     |
| <span id="WA_INACTIVE"></span><span id="wa_inactive"></span><dl> <dt>**WA \_ INACTIVO**</dt> <dt>0</dt> </dl>          | Desactivado.<br/>                                                                                                                                                                                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la ventana que se activa o desactiva, en función del valor del *parámetro wParam.* Si la palabra de orden bajo de *wParam* es **WA \_ INACTIVE,** *lParam* es el identificador de la ventana que se está activando. Si la palabra de orden bajo de *wParam* es **WA \_ ACTIVE** o **WA \_ CLICKACTIVE,** *lParam* es el identificador de la ventana que se desactiva. Este identificador puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Si la ventana se activa y no se minimiza, la [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) establece el foco del teclado en la ventana. Si la ventana se activa con un clic del mouse, también recibe un [**mensaje \_ WM MOUSEACTIVATE.**](wm-mouseactivate.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow)
</dt> <dt>

[**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md)
</dt> <dt>

[**WM \_ NCACTIVATE**](/windows/desktop/winmsg/wm-ncactivate)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

