---
title: Mensaje de WM_SETCURSOR (Winuser. h)
description: Se envía a una ventana si el mouse hace que el cursor se mueva dentro de una ventana y no se captura la entrada del mouse.
ms.assetid: b722689e-925f-40ac-ba4a-55be9dc6a8f8
keywords:
- WM_SETCURSOR menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_SETCURSOR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e941919b447659e67fdcdd9e4e5f4ff2630f8bf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079460"
---
# <a name="wm_setcursor-message"></a>Mensaje de SETCURSOR de WM \_

Se envía a una ventana si el mouse hace que el cursor se mueva dentro de una ventana y no se captura la entrada del mouse.


```C++
#define WM_SETCURSOR                    0x0020
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana que contiene el cursor.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior de *lParam* especifica el resultado de la prueba de posicionamiento para la posición del cursor. Vea los valores devueltos de [WM_NCHITTEST](../inputdev/wm-nchittest.md) para ver los valores posibles.

La palabra de orden superior de *lParam* especifica el mensaje de la ventana del mouse que desencadenó este evento, como [WM_MOUSEMOVE](../inputdev/wm-mousemove.md). Cuando la ventana entra en el modo de menú, este valor es cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver **true** para detener el procesamiento más o **false** para continuar.

## <a name="remarks"></a>Observaciones

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) pasa el mensaje de **\_ SETCURSOR de WM** a una ventana primaria antes del procesamiento. Si la ventana primaria devuelve **true**, se detiene el procesamiento. Al pasar el mensaje a la ventana primaria de una ventana, se proporciona al control de ventana primaria sobre la configuración del cursor en una ventana secundaria. La función **DefWindowProc** también usa este mensaje para establecer el cursor en una flecha si no está en el área cliente, o en el cursor de clase registrado si está en el área cliente. Si la palabra de orden inferior del parámetro *lParam* es **HTERROR** y la palabra de orden superior de *lParam* especifica que uno de los botones del mouse está presionado, **DefWindowProc** llama a la función [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) .

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Vista**
</dt> <dt>

[Cursores](cursors.md)
</dt> </dl>

 

