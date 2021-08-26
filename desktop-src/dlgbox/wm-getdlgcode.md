---
title: WM_GETDLGCODE mensaje (Winuser.h)
description: Se envía al procedimiento de ventana asociado a un control .
ms.assetid: 96d2caee-be6e-46e9-98b3-bffc3af1c003
keywords:
- WM_GETDLGCODE cuadro de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_GETDLGCODE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10d9ef69c2a6e89154cd6d931e05f9e52b4c51b214319bca8dffa9f86786a3da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022195"
---
# <a name="wm_getdlgcode-message"></a>Mensaje \_ GETDLGCODE de WM

Se envía al procedimiento de ventana asociado a un control . De forma predeterminada, el sistema controla toda la entrada de teclado al control; el sistema interpreta determinados tipos de entrada de teclado como teclas de navegación del cuadro de diálogo. Para invalidar este comportamiento predeterminado, el control puede responder al mensaje **\_ GETDLGCODE de WM** para indicar los tipos de entrada que quiere procesar.


```C++
#define WM_GETDLGCODE                   0x0087
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tecla virtual, presionada por el usuario, que Windows para emitir esta notificación. El controlador debe controlar de forma selectiva estas claves. Por ejemplo, el controlador podría aceptar y procesar **VK \_ RETURN,** pero delegar **la pestaña VK \_** en la ventana del propietario. Para obtener una lista de valores, [**vea Códigos de clave virtual**](/windows/desktop/inputdev/virtual-key-codes).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura MSG**](/windows/win32/api/winuser/ns-winuser-msg) (o **NULL** si el sistema realiza una consulta).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es uno o varios de los siguientes valores, lo que indica qué tipo de entrada procesa la aplicación.



| Código o valor devuelto                                                                                                                                                | Descripción                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DLGC \_ Botón**</dt> <dt>0x2000</dt> </dl>          | Botón.<br/>                                                                                                         |
| <dl> <dt>**DLGC \_ DeFPUSHBUTTON**</dt> <dt>0x0010</dt> </dl>   | Botón de inserción predeterminado.<br/>                                                                                            |
| <dl> <dt>**DLGC \_ HASSETSEL**</dt> <dt>0x0008</dt> </dl>       | [**EM \_ Mensajes SETSEL.**](/windows/desktop/Controls/em-setsel)<br/>                                                           |
| <dl> <dt>**DLGC \_ RadioBUTTON**</dt> <dt>0x0040</dt> </dl>     | Botón de radio.<br/>                                                                                                   |
| <dl> <dt>**DLGC \_ Static**</dt> <dt>0x0100</dt> </dl>          | Control estático.<br/>                                                                                                 |
| <dl> <dt>**DLGC \_ UnDEFPUSHBUTTON**</dt> <dt>0x0020</dt> </dl> | Botón de inserción no predeterminado.<br/>                                                                                        |
| <dl> <dt>**DLGC \_ 0x0004 WANTALLKEYS**</dt> <dt></dt> </dl>     | Todas las entradas de teclado.<br/>                                                                                             |
| <dl> <dt>**DLGC \_ WantARROWS**</dt> <dt>0x0001</dt> </dl>      | Teclas de dirección.<br/>                                                                                                 |
| <dl> <dt>**DLGC \_ 0x0080 WANTCHARS**</dt> <dt></dt> </dl>       | [**WM \_ Mensajes CHAR.**](/windows/desktop/inputdev/wm-char)<br/>                                                                      |
| <dl> <dt>**DLGC \_ WantMESSAGE**</dt> <dt>0x0004</dt> </dl>     | Todas las entradas de teclado (la aplicación pasa este mensaje en la estructura [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) al control ).<br/> |
| <dl> <dt>**DLGC \_ 0x0002 WANTTAB**</dt> <dt></dt> </dl>         | Tecla TAB.<br/>                                                                                                        |



 

## <a name="remarks"></a>Comentarios

Aunque la [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) siempre devuelve cero en respuesta al mensaje **\_ GETDLGCODE** de WM, el procedimiento de ventana para las clases de control predefinidas devuelve un código adecuado para cada clase.

El **mensaje \_ GETDLGCODE** de WM y los valores devueltos solo son útiles con controles de cuadro de diálogo definidos por el usuario o controles estándar modificados por subclases.

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

[**EM \_ SETSEL**](/windows/desktop/Controls/em-setsel)
</dt> <dt>

[**Msg**](/windows/win32/api/winuser/ns-winuser-msg)
</dt> <dt>

[**WM \_ CHAR**](/windows/desktop/inputdev/wm-char)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Cuadros de diálogo](dialog-boxes.md)
</dt> </dl>

 

