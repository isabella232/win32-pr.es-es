---
title: Mensaje de WM_GETDLGCODE (Winuser. h)
description: Se envía al procedimiento de ventana asociado a un control.
ms.assetid: 96d2caee-be6e-46e9-98b3-bffc3af1c003
keywords:
- WM_GETDLGCODE cuadros de diálogo de mensaje
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
ms.openlocfilehash: 89d6e1ddb3be21e227c4dad404a06113f5c50a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695974"
---
# <a name="wm_getdlgcode-message"></a>Mensaje de GETDLGCODE de WM \_

Se envía al procedimiento de ventana asociado a un control. De forma predeterminada, el sistema controla todas las entradas de teclado del control; el sistema interpreta determinados tipos de entradas de teclado como teclas de navegación de cuadros de diálogo. Para invalidar este comportamiento predeterminado, el control puede responder al mensaje de **\_ GETDLGCODE de WM** para indicar los tipos de entrada que desea procesar.


```C++
#define WM_GETDLGCODE                   0x0087
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La clave virtual, presionada por el usuario, que solicitó que Windows emita esta notificación. El controlador debe administrar estas claves de forma selectiva. Por ejemplo, el controlador podría aceptar y procesar **VK \_ devolver** , pero delegar **VK \_ Tab** en la ventana propietaria. Para obtener una lista de valores, vea [**códigos de tecla virtual**](/windows/desktop/inputdev/virtual-key-codes).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) (o **null** si el sistema está realizando una consulta).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es uno o varios de los siguientes valores, que indica qué tipo de entrada procesa la aplicación.



| Código o valor devuelto                                                                                                                                                | Descripción                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DLGC \_ BOTÓN**</dt> <dt>0x2000</dt> </dl>          | Botón.<br/>                                                                                                         |
| <dl> <dt>**DLGC \_ DEFPUSHBUTTON**</dt> <dt>0x0010</dt> </dl>   | Botón de opción predeterminado.<br/>                                                                                            |
| <dl> <dt>**DLGC \_ HASSETSEL**</dt> <dt>0x0008</dt> </dl>       | [**Em \_ Mensajes SETSEL**](/windows/desktop/Controls/em-setsel) .<br/>                                                           |
| <dl> <dt>**DLGC \_ RADIOBUTTON**</dt> <dt>0x0040</dt> </dl>     | Botón de radio.<br/>                                                                                                   |
| <dl> <dt>**DLGC \_**</dt> <dt>0x0100</dt> estática </dl>          | Control estático.<br/>                                                                                                 |
| <dl> <dt>**DLGC \_ UNDEFPUSHBUTTON**</dt> <dt>0x0020</dt> </dl> | Botón de extracción no predeterminado.<br/>                                                                                        |
| <dl> <dt>**DLGC \_ WANTALLKEYS**</dt> <dt>0x0004</dt> </dl>     | Todas las entradas de teclado.<br/>                                                                                             |
| <dl> <dt>**DLGC \_ WANTARROWS**</dt> <dt>0x0001</dt> </dl>      | Teclas de dirección.<br/>                                                                                                 |
| <dl> <dt>**DLGC \_ WANTCHARS**</dt> <dt>0x0080</dt> </dl>       | [**WM \_ Mensajes CHAR**](/windows/desktop/inputdev/wm-char) .<br/>                                                                      |
| <dl> <dt>**DLGC \_ WANTMESSAGE**</dt> <dt>0x0004</dt> </dl>     | Toda la entrada del teclado (la aplicación pasa este mensaje en la estructura [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) al control).<br/> |
| <dl> <dt>**DLGC \_ WANTTAB**</dt> <dt>0x0002</dt> </dl>         | Tecla TAB.<br/>                                                                                                        |



 

## <a name="remarks"></a>Observaciones

Aunque la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) siempre devuelve cero en respuesta al mensaje **de \_ GETDLGCODE de WM** , el procedimiento de ventana para las clases de control predefinidas devuelve un código adecuado para cada clase.

El **mensaje \_ GETDLGCODE de WM** y los valores devueltos solo son útiles en los controles de cuadro de diálogo definidos por el usuario o en los controles estándar modificados por subclase.

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

[**\_SETSEL em**](/windows/desktop/Controls/em-setsel)
</dt> <dt>

[**MENSAJE**](/windows/win32/api/winuser/ns-winuser-msg)
</dt> <dt>

[**carácter de WM \_**](/windows/desktop/inputdev/wm-char)
</dt> <dt>

**Vista**
</dt> <dt>

[Cuadros de diálogo](dialog-boxes.md)
</dt> </dl>

 

