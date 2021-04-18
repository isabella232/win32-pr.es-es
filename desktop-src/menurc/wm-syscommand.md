---
title: Mensaje de WM_SYSCOMMAND (Winuser. h)
description: Una ventana recibe este mensaje cuando el usuario elige un comando en el menú ventana (anteriormente conocido como el menú del sistema o el control) o cuando el usuario elige el botón maximizar, el botón minimizar, el botón Restaurar o el botón Cerrar.
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
ms.openlocfilehash: 25596f30457063bc90124f14489963507f85ff70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699960"
---
# <a name="wm_syscommand-message"></a>Mensaje de SYSCOMMAND de WM \_

Una ventana recibe este mensaje cuando el usuario elige un comando en el menú **ventana** (anteriormente conocido como el menú del sistema o el control) o cuando el usuario elige el botón maximizar, el botón minimizar, el botón Restaurar o el botón Cerrar.


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
Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) en github.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El tipo de comando del sistema solicitado. Este parámetro puede ser uno de los valores siguientes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SC_CLOSE"></span><span id="sc_close"></span><dl> <dt><strong>SC_CLOSE</strong></dt> <dt>0xF060</dt> </dl></td>
<td>Cierra la ventana.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_CONTEXTHELP"></span><span id="sc_contexthelp"></span><dl> <dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF180</dt> </dl></td>
<td>Cambia el cursor a un signo de interrogación con un puntero. Si el usuario hace clic en un control en el cuadro de diálogo, el control recibe un mensaje de <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_DEFAULT"></span><span id="sc_default"></span><dl> <dt><strong>SC_DEFAULT</strong></dt> <dt>0xF160</dt> </dl></td>
<td>Selecciona el elemento predeterminado; el usuario hizo doble clic en el menú ventana.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_HOTKEY"></span><span id="sc_hotkey"></span><dl> <dt><strong>SC_HOTKEY</strong></dt> <dt>0xF150</dt> </dl></td>
<td>Activa la ventana asociada a la tecla de acceso rápido especificada por la aplicación. El parámetro <em>lParam</em> identifica la ventana que se va a activar.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_HSCROLL"></span><span id="sc_hscroll"></span><dl> <dt><strong>SC_HSCROLL</strong></dt> <dt>0xF080</dt> </dl></td>
<td>Se desplaza horizontalmente.<br/></td>
</tr>
<tr class="even">
<td><span id="SCF_ISSECURE"></span><span id="scf_issecure"></span><dl> <dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </dl></td>
<td>Indica si el protector de pantalla es seguro. <br/></td>
</tr>
<tr class="odd">
<td><span id="SC_KEYMENU"></span><span id="sc_keymenu"></span><dl> <dt><strong>SC_KEYMENU</strong></dt> <dt>0xF100</dt> </dl></td>
<td>Recupera el menú ventana como resultado de una pulsación de tecla. Para obtener más información, vea la sección Comentarios.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_MAXIMIZE"></span><span id="sc_maximize"></span><dl> <dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF030</dt> </dl></td>
<td>Maximiza la ventana.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_MINIMIZE"></span><span id="sc_minimize"></span><dl> <dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF020</dt> </dl></td>
<td>Minimiza la ventana.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_MONITORPOWER"></span><span id="sc_monitorpower"></span><dl> <dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF170</dt> </dl></td>
<td>Establece el estado de la pantalla. Este comando admite dispositivos que tienen características de ahorro de energía, como un equipo personal con batería. <br/> El parámetro <em>lParam</em> puede tener los valores siguientes:<br/>
<ul>
<li>-1 (la pantalla se enciende)</li>
<li>1 (la pantalla va a baja energía)</li>
<li>2 (la pantalla se está apagando)</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SC_MOUSEMENU"></span><span id="sc_mousemenu"></span><dl> <dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF090</dt> </dl></td>
<td>Recupera el menú ventana como resultado de un clic del mouse.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_MOVE"></span><span id="sc_move"></span><dl> <dt><strong>SC_MOVE</strong></dt> <dt>0xF010</dt> </dl></td>
<td>Mueve la ventana.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_NEXTWINDOW"></span><span id="sc_nextwindow"></span><dl> <dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF040</dt> </dl></td>
<td>Se desplaza a la ventana siguiente.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_PREVWINDOW"></span><span id="sc_prevwindow"></span><dl> <dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF050</dt> </dl></td>
<td>Se desplaza a la ventana anterior.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_RESTORE"></span><span id="sc_restore"></span><dl> <dt><strong>SC_RESTORE</strong></dt> <dt>0xF120</dt> </dl></td>
<td>Restaura la ventana a su posición y tamaño normales.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_SCREENSAVE"></span><span id="sc_screensave"></span><dl> <dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF140</dt> </dl></td>
<td>Ejecuta la aplicación de protector de pantalla especificada en la sección [boot] del archivo de System.ini.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_SIZE"></span><span id="sc_size"></span><dl> <dt><strong>SC_SIZE</strong></dt> <dt>0xF000</dt> </dl></td>
<td>Ajusta el tamaño de la ventana.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_TASKLIST"></span><span id="sc_tasklist"></span><dl> <dt><strong>SC_TASKLIST</strong></dt> <dt>0xF130</dt> </dl></td>
<td>Activa el menú <strong>Inicio</strong> .<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_VSCROLL"></span><span id="sc_vscroll"></span><dl> <dt><strong>SC_VSCROLL</strong></dt> <dt>0xF070</dt> </dl></td>
<td>Se desplaza verticalmente.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior especifica la posición horizontal del cursor, en coordenadas de la pantalla, si se elige un comando de menú de ventana con el mouse. De lo contrario, este parámetro no se utiliza.

La palabra de orden superior especifica la posición vertical del cursor, en coordenadas de pantalla, si se elige un comando de menú de ventana con el mouse. Este parámetro es 1 si se elige el comando con un acelerador del sistema, o bien, cero si se usa una tecla de método abreviado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Para obtener las coordenadas de posición en coordenadas de pantalla, use el código siguiente:


```
xPos = GET_X_LPARAM(lParam);    // horizontal position 
yPos = GET_Y_LPARAM(lParam);    // vertical position
```



La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) lleva a cabo la solicitud de menú ventana para las acciones predefinidas especificadas en la tabla anterior.

En los mensajes de **\_ SYSCOMMAND de WM** , el sistema usa internamente los cuatro bits de orden inferior del parámetro *wParam* . Para obtener el resultado correcto al probar el valor de *wParam*, una aplicación debe combinar el valor 0xFFF0 con el valor *wParam* mediante el operador and bit a bit.

Los elementos de menú de un menú ventana se pueden modificar mediante las funciones [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)y [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) . Las aplicaciones que modifican el menú ventana deben procesar los mensajes de **WM \_ SYSCOMMAND** .

Una aplicación puede llevar a cabo cualquier comando del sistema en cualquier momento si se pasa un mensaje de **WM \_ SYSCOMMAND** a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Cualquier mensaje de **\_ SYSCOMMAND de WM** no controlado por la aplicación debe pasarse a **DefWindowProc**. Los valores de comando agregados por una aplicación deben ser procesados por la aplicación y no se pueden pasar a **DefWindowProc**.

Si la Directiva habilita la protección con contraseña, se inicia el protector de pantalla independientemente de lo que hace una aplicación con la notificación **SC \_ SCREENSAVE** aunque no se pase a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Las teclas de aceleración definidas para elegir elementos en el menú ventana se traducen en mensajes de **WM \_ SYSCOMMAND** ; todas las demás pulsaciones de teclas de aceleración se traducen en mensajes de [**\_ comandos de WM**](wm-command.md) .

Si el *wParam* es **SC \_ KEYMENU**, *lParam* contiene el código de carácter de la tecla que se usa con la tecla Alt para mostrar el menú emergente. Por ejemplo, si presiona ALT + F para mostrar el archivo emergente, se producirá un **\_ SYSCOMMAND de WM** con *wParam* igual a **SC \_ KEYMENU** y *lParam* igual a "F".

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

[**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**OBTENER \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**OBTENER \_ \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
</dt> <dt>

[**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
</dt> <dt>

[**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
</dt> <dt>

[**comando de WM \_**](wm-command.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

