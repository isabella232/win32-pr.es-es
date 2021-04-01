---
title: Mensaje de WM_ACTIVATE (Winuser. h)
description: Se envía a la ventana que se está activando y la ventana que se está desactivando.
ms.assetid: a62bb9f7-f286-4d0d-a1ca-370950c188b2
keywords:
- Entrada de mouse y teclado de mensaje de WM_ACTIVATE
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150157"
---
# <a name="wm_activate-message"></a>Mensaje de activación de WM \_

Se envía a la ventana que se está activando y la ventana que se está desactivando. Si las ventanas utilizan la misma cola de entrada, el mensaje se envía de forma sincrónica, primero en el procedimiento de ventana de la ventana de nivel superior que se va a desactivar y, a continuación, en el procedimiento de ventana de la ventana de nivel superior que se va a activar. Si Windows usa colas de entrada diferentes, el mensaje se envía de forma asincrónica, por lo que la ventana se activa inmediatamente.


```C++
#define WM_ACTIVATE                     0x0006
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden inferior especifica si la ventana se está activando o desactivando. Este parámetro puede ser uno de los valores siguientes. La palabra de orden superior especifica el estado minimizado de la ventana que se está activando o desactivando. Un valor distinto de cero indica que la ventana está minimizada.



| Value                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WA_ACTIVE"></span><span id="wa_active"></span><dl> <dt>**Wa \_ ACTIVO**</dt> <dt>1</dt> </dl>                | Activado por algún método que no sea un clic del mouse (por ejemplo, mediante una llamada a la función [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) o mediante el uso de la interfaz de teclado para seleccionar la ventana).<br/> |
| <span id="WA_CLICKACTIVE"></span><span id="wa_clickactive"></span><dl> <dt>**Wa \_ CLICKACTIVE**</dt> <dt>2</dt> </dl> | Activado con un clic del mouse.<br/>                                                                                                                                                                     |
| <span id="WA_INACTIVE"></span><span id="wa_inactive"></span><dl> <dt>**Wa \_ Inactivo**</dt> <dt>0</dt> </dl>          | Desactivado.<br/>                                                                                                                                                                                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la ventana que se va a activar o desactivar, dependiendo del valor del parámetro *wParam* . Si la palabra de orden inferior de *wParam* es **wa \_ inactiva**, *lParam* es el identificador de la ventana que se está activando. Si la palabra de orden inferior de *wParam* es **wa \_ Active** o **wa \_ CLICKACTIVE**, *lParam* es el identificador de la ventana que se está desactivando. Este identificador puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Si la ventana se está activando y no está minimizada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) establece el foco de teclado en la ventana. Si la ventana se activa con un clic del mouse, también recibe un mensaje de [**\_ MOUSEACTIVATE de WM**](wm-mouseactivate.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow)
</dt> <dt>

[**MOUSEACTIVATE de WM \_**](wm-mouseactivate.md)
</dt> <dt>

[**NCACTIVATE de WM \_**](/windows/desktop/winmsg/wm-ncactivate)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

