---
title: WM_SETCURSOR mensaje (Winuser.h)
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
ms.openlocfilehash: 19dccc4fab0d24dd233133e97b3ddcc71f615d9abb27a4684821099b6ad15802
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846875"
---
# <a name="wm_setcursor-message"></a>Mensaje \_ SETCURSOR de WM

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

La palabra de orden bajo *de lParam* especifica el resultado de la prueba de posicionamiento para la posición del cursor. Consulte los valores devueltos para [WM_NCHITTEST](../inputdev/wm-nchittest.md) para ver los valores posibles.

La palabra de orden superior *de lParam* especifica el mensaje de ventana del mouse que desencadenó este [evento, como WM_MOUSEMOVE](../inputdev/wm-mousemove.md). Cuando la ventana entra en modo de menú, este valor es cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver **TRUE** para detener el procesamiento adicional o **FALSE** para continuar.

## <a name="remarks"></a>Comentarios

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) pasa el mensaje **\_ SETCURSOR de WM** a una ventana primaria antes del procesamiento. Si la ventana primaria devuelve **TRUE,** se detiene el procesamiento adicional. Pasar el mensaje a la ventana primaria de una ventana proporciona a la ventana primaria el control sobre la configuración del cursor en una ventana secundaria. La **función DefWindowProc** también usa este mensaje para establecer el cursor en una flecha si no está en el área de cliente o en el cursor de clase registrada si está en el área de cliente. Si la palabra de orden bajo del parámetro *lParam* es **HTERROR** y la palabra de orden superior *de lParam* especifica que se presiona uno de los botones del mouse, **DefWindowProc** llama a la función [**MessageBeep.**](/windows/desktop/api/winuser/nf-winuser-messagebeep)

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Conceptual**
</dt> <dt>

[Cursores](cursors.md)
</dt> </dl>

 

