---
title: Editar estilos de control (Winuser. h)
description: Para crear un control de edición mediante la función CreateWindow o CreateWindowEx, especifique la clase EDIT, las constantes de estilo de ventana apropiadas y una combinación de los siguientes estilos de control de edición.
ms.assetid: 336c69b7-bc23-4b93-8968-ad63a1703385
topic_type:
- apiref
api_name:
- ES_AUTOHSCROLL
- ES_AUTOVSCROLL
- ES_CENTER
- ES_LEFT
- ES_LOWERCASE
- ES_MULTILINE
- ES_NOHIDESEL
- ES_NUMBER
- ES_OEMCONVERT
- ES_PASSWORD
- ES_READONLY
- ES_RIGHT
- ES_UPPERCASE
- ES_WANTRETURN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 9b255aee665c32f9a14be4946dee0122dad626bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649721"
---
# <a name="edit-control-styles"></a>Editar estilos de control

Para crear un control de edición mediante la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especifique la clase Edit, las constantes de estilo de ventana apropiadas y una combinación de los siguientes estilos de control de edición. Una vez creado el control, estos estilos no se pueden modificar, salvo que se indique lo contrario.

## <a name="example"></a>Ejemplo

```cpp
LRESULT MsgCreate(HWND hwnd, UINT uMessage, WPARAM wparam, LPARAM lparam)
{
    lparam;
    wparam;
    uMessage;

    // Create Edit control for typing to be sent to server
    if (NULL == (hOutWnd = CreateWindow("EDIT",
                           NULL,
                           WS_BORDER | WS_CHILD | WS_VISIBLE | WS_VSCROLL | ES_LEFT | 
                           ES_MULTILINE | ES_AUTOVSCROLL,
                           0,0,0,0,
                           hwnd,
                           (HMENU) ID_OUTBOX,
                           (HINSTANCE) GetWindowLongPtr(hwnd, GWLP_HINSTANCE),
                           NULL)))
        return FALSE;
    return TRUE;
}
```

Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) en github.

## <a name="constants"></a>Constantes

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <dt><strong>ES_AUTOHSCROLL</strong></dt> </dl></td>
<td style="text-align: left;">Desplaza automáticamente el texto a la derecha 10 caracteres cuando el usuario escribe un carácter al final de la línea. Cuando el usuario presiona la tecla entrar, el control vuelve a desplazar todo el texto hasta la posición cero.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <dt><strong>ES_AUTOVSCROLL</strong></dt> </dl></td>
<td style="text-align: left;">Desplaza automáticamente el texto una página cuando el usuario presiona la tecla entrar en la última línea.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_CENTER"></span><span id="es_center"></span><dl> <dt><strong>ES_CENTER</strong></dt> </dl></td>
<td style="text-align: left;">Centra el texto en un control de edición de línea única o multilínea.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_LEFT"></span><span id="es_left"></span><dl> <dt><strong>ES_LEFT</strong></dt> </dl></td>
<td style="text-align: left;">Alinea el texto con el margen izquierdo.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_LOWERCASE"></span><span id="es_lowercase"></span><dl> <dt><strong>ES_LOWERCASE</strong></dt> </dl></td>
<td style="text-align: left;">Convierte todos los caracteres a minúsculas a medida que se escriben en el control de edición.<br/> Para cambiar este estilo una vez creado el control, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <dt><strong>ES_MULTILINE</strong></dt> </dl></td>
<td style="text-align: left;">Designa un control de edición multilínea. El valor predeterminado es el control de edición de una sola línea. <br/> Cuando el control de edición multilínea está en un cuadro de diálogo, la respuesta predeterminada a presionar la tecla entrar es activar el botón predeterminado. Para usar la tecla entrar como un retorno de carro, use el estilo <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> .<br/> Cuando el control de edición multilínea no está en un cuadro de diálogo y se especifica el estilo de <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> , el control de edición muestra tantas líneas como sea posible y se desplaza verticalmente cuando el usuario presiona la tecla entrar. Si no se especifica <strong>ES_AUTOVSCROLL</strong>, el control de edición muestra tantas líneas como sea posible y emite un pitido si el usuario presiona la tecla entrar cuando no se pueden mostrar más líneas.<br/> Si especifica el estilo de <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> , el control de edición de varias líneas se desplaza horizontalmente de forma automática cuando el símbolo de intercalación va más allá del borde derecho del control. Para iniciar una nueva línea, el usuario debe presionar la tecla entrar. Si no se especifica <strong>ES_AUTOHSCROLL</strong>, el control ajusta automáticamente las palabras al principio de la línea siguiente cuando sea necesario. También se inicia una nueva línea si el usuario presiona la tecla entrar. El tamaño de la ventana determina la posición del ajuste de la pantalla. Si cambia el tamaño de la ventana, la posición de aparecen cambia y se vuelve a mostrar el texto.<br/> Los controles de edición multilínea pueden tener barras de desplazamiento. Un control de edición con barras de desplazamiento procesa sus propios mensajes de barra de desplazamiento. Tenga en cuenta que los controles de edición sin barras de desplazamiento se desplazan como se describe en los párrafos anteriores y procesan los mensajes de desplazamiento enviados por la ventana primaria.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <dt><strong>ES_NOHIDESEL</strong></dt> </dl></td>
<td style="text-align: left;">Niega el comportamiento predeterminado de un control de edición. El comportamiento predeterminado oculta la selección cuando el control pierde el foco de entrada e invierte la selección cuando el control recibe el foco de entrada. Si especifica <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, se invierte el texto seleccionado, incluso si el control no tiene el foco.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_NUMBER"></span><span id="es_number"></span><dl> <dt><strong>ES_NUMBER</strong></dt> </dl></td>
<td style="text-align: left;">Permite que solo se escriban dígitos en el control de edición. Tenga en cuenta que, incluso con este conjunto, todavía es posible pegar no dígitos en el control de edición. <br/> Para cambiar este estilo una vez creado el control, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/> Para traducir el texto que se especificó en el control de edición a un valor entero, utilice la función <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>GetDlgItemInt</strong></a> . Para establecer el texto del control de edición en la representación de cadena de un entero especificado, utilice la función <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>SetDlgItemInt</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_OEMCONVERT"></span><span id="es_oemconvert"></span><dl> <dt><strong>ES_OEMCONVERT</strong></dt> </dl></td>
<td style="text-align: left;">Convierte el texto escrito en el control de edición. El texto se convierte del juego de caracteres de Windows al Juego de caracteres OEM y, a continuación, de nuevo al Juego de caracteres de Windows. Esto garantiza una conversión de caracteres adecuada cuando la aplicación llama a la función <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> para convertir una cadena de Windows del control de edición en caracteres OEM. Este estilo es muy útil para los controles de edición que contienen nombres de archivo que se utilizarán en sistemas de archivos que no admiten Unicode. <br/> Para cambiar este estilo una vez creado el control, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <dt><strong>ES_PASSWORD</strong></dt> </dl></td>
<td style="text-align: left;">Muestra un asterisco (*) para cada carácter que se escribe en el control de edición. Este estilo solo es válido para los controles de edición de una sola línea. <br/> Para cambiar los caracteres que se muestran, o para establecer o desactivar este estilo, utilice el mensaje de <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> . <br/>
<blockquote>
[!Note]<br />
Para usar Comctl32.dll versión 6, especifíquelo en un manifiesto. Para obtener más información sobre los manifiestos, vea <a href="cookbook-overview.md">habilitar estilos visuales</a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <dt><strong>ES_READONLY</strong></dt> </dl></td>
<td style="text-align: left;">Impide que el usuario escriba o modifique texto en el control de edición.<br/> Para cambiar este estilo una vez creado el control, utilice el mensaje de <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> . <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_RIGHT"></span><span id="es_right"></span><dl> <dt><strong>ES_RIGHT</strong></dt> </dl></td>
<td style="text-align: left;">Alinea a la derecha el texto en un control de edición de una sola línea o multilínea.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_UPPERCASE"></span><span id="es_uppercase"></span><dl> <dt><strong>ES_UPPERCASE</strong></dt> </dl></td>
<td style="text-align: left;">Convierte todos los caracteres a mayúsculas a medida que se escriben en el control de edición. <br/> Para cambiar este estilo una vez creado el control, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <dt><strong>ES_WANTRETURN</strong></dt> </dl></td>
<td style="text-align: left;">Especifica que se inserte un retorno de carro cuando el usuario presione la tecla entrar mientras escribe texto en un control de edición multilínea en un cuadro de diálogo. Si no especifica este estilo, presionar la tecla entrar tiene el mismo efecto que presionar el botón de opción predeterminado del cuadro de diálogo. Este estilo no tiene ningún efecto en un control de edición de una sola línea. <br/> Para cambiar este estilo una vez creado el control, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winuser. h</dt> </dl> |



