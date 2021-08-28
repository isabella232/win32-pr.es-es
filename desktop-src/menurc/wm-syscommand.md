---
title: WM_SYSCOMMAND mensaje (Winuser.h)
description: Una ventana recibe este mensaje cuando el usuario elige un comando en el menú Ventana (anteriormente conocido como el menú del sistema o control) o cuando el usuario elige el botón maximizar, minimizar, restaurar o cerrar.
ms.assetid: 82c7cc95-82d5-4f0f-8c78-ab325561b04e
keywords:
- WM_SYSCOMMAND menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_SYSCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 5458a9acfa6c166764b47a2d49a5ddcc181e38ee
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482181"
---
# <a name="wm_syscommand-message"></a>Mensaje \_ SYSCOMMAND de WM

Una ventana recibe este mensaje cuando el  usuario elige un comando en el menú Ventana (anteriormente conocido como menú del sistema o control) o cuando el usuario elige el botón maximizar, minimizar, restaurar o cerrar.


```C++
#define WM_SYSCOMMAND                   0x0112
```

## <a name="example"></a>Ejemplo

```cpp
 case WM_SYSCOMMAND:
        if (wParam == SC_CLOSE)
        {
            EndDialog (hDlg, TRUE);
            return(TRUE);
        }
        break;

```
Ejemplo de [Windows ejemplos clásicos](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) en GitHub.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de comando del sistema solicitado. Este parámetro puede ser uno de los valores siguientes.




| Valor | Significado | 
|-------|---------|
| <span id="SC_CLOSE"></span><span id="sc_close"></span><dl><dt><strong>SC_CLOSE</strong></dt><dt>0xF060</dt></dl> | Cierra la ventana.<br /> | 
| <span id="SC_CONTEXTHELP"></span><span id="sc_contexthelp"></span><dl><dt><strong>SC_CONTEXTHELP</strong></dt><dt>0xF180</dt></dl> | Cambia el cursor a un signo de interrogación con un puntero. Si el usuario hace clic en un control en el cuadro de diálogo, el control recibe un <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> mensaje.<br /> | 
| <span id="SC_DEFAULT"></span><span id="sc_default"></span><dl><dt><strong>SC_DEFAULT</strong></dt><dt>0xF160</dt></dl> | Selecciona el elemento predeterminado; El usuario hizo doble clic en el menú de la ventana.<br /> | 
| <span id="SC_HOTKEY"></span><span id="sc_hotkey"></span><dl><dt><strong>SC_HOTKEY</strong></dt><dt>0xF150</dt></dl> | Activa la ventana asociada a la tecla de acceso activa especificada por la aplicación. El <em>parámetro lParam</em> identifica la ventana que se debe activar.<br /> | 
| <span id="SC_HSCROLL"></span><span id="sc_hscroll"></span><dl><dt><strong>SC_HSCROLL</strong></dt><dt>0xF080</dt></dl> | Se desplaza horizontalmente.<br /> | 
| <span id="SCF_ISSECURE"></span><span id="scf_issecure"></span><dl><dt><strong>SCF_ISSECURE</strong></dt><dt>0x00000001</dt></dl> | Indica si el protector de pantalla es seguro. <br /> | 
| <span id="SC_KEYMENU"></span><span id="sc_keymenu"></span><dl><dt><strong>SC_KEYMENU</strong></dt><dt>0xF100</dt></dl> | Recupera el menú de la ventana como resultado de una pulsación de tecla. Para obtener más información, vea la sección Comentarios.<br /> | 
| <span id="SC_MAXIMIZE"></span><span id="sc_maximize"></span><dl><dt><strong>SC_MAXIMIZE</strong></dt><dt>0xF030</dt></dl> | Maximiza la ventana.<br /> | 
| <span id="SC_MINIMIZE"></span><span id="sc_minimize"></span><dl><dt><strong>SC_MINIMIZE</strong></dt><dt>0xF020</dt></dl> | Minimiza la ventana.<br /> | 
| <span id="SC_MONITORPOWER"></span><span id="sc_monitorpower"></span><dl><dt><strong>SC_MONITORPOWER</strong></dt><dt>0xF170</dt></dl> | Establece el estado de la pantalla. Este comando admite dispositivos que tienen características de ahorro de energía, como un equipo personal con batería. <br /> El <em>parámetro lParam</em> puede tener los siguientes valores:<br /><ul><li>-1 (la pantalla está encendido)</li><li>1 (la pantalla va a tener poca potencia)</li><li>2 (la pantalla se está apagando)</li></ul> | 
| <span id="SC_MOUSEMENU"></span><span id="sc_mousemenu"></span><dl><dt><strong>SC_MOUSEMENU</strong></dt><dt>0xF090</dt></dl> | Recupera el menú de la ventana como resultado de un clic del mouse.<br /> | 
| <span id="SC_MOVE"></span><span id="sc_move"></span><dl><dt><strong>SC_MOVE</strong></dt><dt>0xF010</dt></dl> | Mueve la ventana.<br /> | 
| <span id="SC_NEXTWINDOW"></span><span id="sc_nextwindow"></span><dl><dt><strong>SC_NEXTWINDOW</strong></dt><dt>0xF040</dt></dl> | Se desplaza a la ventana siguiente.<br /> | 
| <span id="SC_PREVWINDOW"></span><span id="sc_prevwindow"></span><dl><dt><strong>SC_PREVWINDOW</strong></dt><dt>0xF050</dt></dl> | Se desplaza a la ventana anterior.<br /> | 
| <span id="SC_RESTORE"></span><span id="sc_restore"></span><dl><dt><strong>SC_RESTORE</strong></dt><dt>0xF120</dt></dl> | Restaura la ventana a su posición y tamaño normales.<br /> | 
| <span id="SC_SCREENSAVE"></span><span id="sc_screensave"></span><dl><dt><strong>SC_SCREENSAVE</strong></dt><dt>0xF140</dt></dl> | Ejecuta la aplicación de protector de pantalla especificada en la sección [boot] del archivo System.ini pantalla.<br /> | 
| <span id="SC_SIZE"></span><span id="sc_size"></span><dl><dt><strong>SC_SIZE</strong></dt><dt>0xF000</dt></dl> | Tamaños de la ventana.<br /> | 
| <span id="SC_TASKLIST"></span><span id="sc_tasklist"></span><dl><dt><strong>SC_TASKLIST</strong></dt><dt>0xF130</dt></dl> | Activa el <strong>menú</strong> Inicio.<br /> | 
| <span id="SC_VSCROLL"></span><span id="sc_vscroll"></span><dl><dt><strong>SC_VSCROLL</strong></dt><dt>0xF070</dt></dl> | Se desplaza verticalmente.<br /> | 




 

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden bajo especifica la posición horizontal del cursor, en coordenadas de pantalla, si se elige un comando de menú de ventana con el mouse. De lo contrario, no se usa este parámetro.

La palabra de orden superior especifica la posición vertical del cursor, en coordenadas de pantalla, si se elige un comando de menú de ventana con el mouse. Este parámetro es 1 si el comando se elige mediante un acelerador del sistema, o cero si se usa un mnemotécnico.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Comentarios

Para obtener las coordenadas de posición en coordenadas de pantalla, use el código siguiente:


```
xPos = GET_X_LPARAM(lParam);    // horizontal position 
yPos = GET_Y_LPARAM(lParam);    // vertical position
```



La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) lleva a cabo la solicitud de menú de ventana para las acciones predefinidas especificadas en la tabla anterior.

En **los mensajes \_ SYSCOMMAND** de WM, el sistema usa internamente los cuatro bits de orden inferior del parámetro *wParam.* Para obtener el resultado correcto al probar el valor de *wParam*, una aplicación debe combinar el valor 0xFFF0 con el *valor wParam* mediante el operador AND bit a bit.

Los elementos de menú de un menú de ventana se pueden modificar mediante las funciones [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**ModifyMenu,**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)y [**SetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) Las aplicaciones que modifican el menú de ventana deben procesar **mensajes \_ SYSCOMMAND de WM.**

Una aplicación puede llevar a cabo cualquier comando del sistema en cualquier momento pasando un **mensaje \_ SYSCOMMAND de WM** a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Todos **los \_ mensajes SYSCOMMAND de WM** que no controle la aplicación deben pasarse a **DefWindowProc**. Cualquier valor de comando agregado por una aplicación debe ser procesado por la aplicación y no se puede pasar **a DefWindowProc**.

Si la directiva habilita la protección con contraseña, el protector de pantalla se inicia independientemente de lo que haga una aplicación con la notificación **SC \_ SCREENSAVE,** incluso si no se puede pasar a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Las teclas de aceleración que se definen para elegir elementos del menú de la ventana se traducen en mensajes **\_ SYSCOMMAND** de WM; todas las demás pulsaciones de teclas del acelerador se traducen en [**mensajes WM \_ COMMAND.**](wm-command.md)

Si *wParam* es **SC \_ KEYMENU,** *lParam* contiene el código de carácter de la clave que se usa con la tecla ALT para mostrar el menú emergente. Por ejemplo, al presionar ALT+F para mostrar el elemento emergente Archivo, se provocará un **COMANDO \_ SYSCOMMAND wm** con *wParam* igual a **SC \_ KEYMENU** y *lParam* igual a "f".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
</dt> <dt>

[**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
</dt> <dt>

[**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
</dt> <dt>

[**COMANDO \_ WM**](wm-command.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

