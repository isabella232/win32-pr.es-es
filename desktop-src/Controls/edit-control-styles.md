---
title: Editar estilos de control (Winuser.h)
description: Para crear un control de edición mediante las funciones CreateWindow o CreateWindowEx, especifique la clase EDIT, las constantes de estilo de ventana adecuadas y una combinación de los siguientes estilos de control de edición.
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
ms.openlocfilehash: 5e1a62dba617f73efdec992f843856d80a5b39bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246927"
---
# <a name="edit-control-styles"></a>Editar estilos de control

Para crear un control de edición mediante las funciones [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) especifique la clase EDIT, las constantes de estilo de ventana adecuadas y una combinación de los siguientes estilos de control de edición. Una vez creado el control, estos estilos no se pueden modificar, excepto como se indicó.

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

Ejemplo de [Windows ejemplos clásicos](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) en GitHub.

## <a name="constants"></a>Constantes


| Constante | Descripción | 
|----------|-------------|
| <span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl><dt><strong>ES_AUTOHSCROLL</strong></dt></dl> | Desplaza automáticamente el texto a la derecha en 10 caracteres cuando el usuario tipos un carácter al final de la línea. Cuando el usuario presiona la tecla ENTRAR, el control vuelve a desplazar todo el texto hasta la posición cero.<br /> | 
| <span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl><dt><strong>ES_AUTOVSCROLL</strong></dt></dl> | Desplaza automáticamente el texto hacia arriba una página cuando el usuario presiona la tecla ENTRAR en la última línea.<br /> | 
| <span id="ES_CENTER"></span><span id="es_center"></span><dl><dt><strong>ES_CENTER</strong></dt></dl> | Centra el texto en un control de edición de una o varias líneas.<br /> | 
| <span id="ES_LEFT"></span><span id="es_left"></span><dl><dt><strong>ES_LEFT</strong></dt></dl> | Alinea el texto con el margen izquierdo.<br /> | 
| <span id="ES_LOWERCASE"></span><span id="es_lowercase"></span><dl><dt><strong>ES_LOWERCASE</strong></dt></dl> | Convierte todos los caracteres a minúsculas a medida que se escriben en el control de edición.<br /> Para cambiar este estilo una vez creado el control, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br /> | 
| <span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl><dt><strong>ES_MULTILINE</strong></dt></dl> | Designa un control de edición multilínea. El valor predeterminado es el control de edición de una sola línea. <br /> Cuando el control de edición multilínea está en un cuadro de diálogo, la respuesta predeterminada para presionar la tecla ENTRAR es activar el botón predeterminado. Para usar la tecla ENTRAR como retorno de carro, use <a href="rich-edit-control-styles.md"><strong>el ES_WANTRETURN</strong></a> de carro.<br /> Cuando el control de edición multilínea no está en un cuadro de diálogo y se especifica el estilo <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL,</strong></a> el control de edición muestra tantas líneas como sea posible y se desplaza verticalmente cuando el usuario presiona la tecla ENTRAR. Si no especifica ES_AUTOVSCROLL <strong>,</strong>el control de edición muestra tantas líneas como sea posible y bips si el usuario presiona la tecla ENTRAR cuando no se pueden mostrar más líneas.<br /> Si especifica el estilo <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL,</strong></a> el control de edición multilínea se desplaza automáticamente horizontalmente cuando el icono de diálogo pasa por el borde derecho del control. Para iniciar una nueva línea, el usuario debe presionar la tecla ENTRAR. Si no especifica <strong>ES_AUTOHSCROLL</strong>, el control encapsula automáticamente las palabras al principio de la línea siguiente cuando sea necesario. También se inicia una nueva línea si el usuario presiona la tecla ENTRAR. El tamaño de la ventana determina la posición del wordwrap. Si cambia el tamaño de la ventana, cambia la posición de wordwrapping y se vuelve a mostrar el texto.<br /> Los controles de edición multilínea pueden tener barras de desplazamiento. Un control de edición con barras de desplazamiento procesa sus propios mensajes de barra de desplazamiento. Tenga en cuenta que los controles de edición sin barras de desplazamiento se desplazan como se describe en los párrafos anteriores y procesan los mensajes de desplazamiento enviados por la ventana primaria.<br /> | 
| <span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl><dt><strong>ES_NOHIDESEL</strong></dt></dl> | Nega el comportamiento predeterminado de un control de edición. El comportamiento predeterminado oculta la selección cuando el control pierde el foco de entrada e invierte la selección cuando el control recibe el foco de entrada. Si especifica <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, el texto seleccionado se invierte, incluso si el control no tiene el foco.<br /> | 
| <span id="ES_NUMBER"></span><span id="es_number"></span><dl><dt><strong>ES_NUMBER</strong></dt></dl> | Permite especificar solo dígitos en el control de edición. Tenga en cuenta que, incluso con este conjunto, todavía es posible pegar sin dígitos en el control de edición. <br /> Para cambiar este estilo una vez creado el control, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br /> Para convertir el texto especificado en el control de edición en un valor entero, use la <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>función GetDlgItemInt.</strong></a> Para establecer el texto del control de edición en la representación de cadena de un entero especificado, use la <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>función SetDlgItemInt.</strong></a><br /> | 
| <span id="ES_OEMCONVERT"></span><span id="es_oemconvert"></span><dl><dt><strong>ES_OEMCONVERT</strong></dt></dl> | Convierte el texto especificado en el control de edición. El texto se convierte del juego de caracteres Windows al juego de caracteres OEM y, a continuación, vuelve al juego de Windows caracteres. Esto garantiza una conversión adecuada de caracteres cuando la aplicación llama a la función <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> para convertir una cadena Windows en el control de edición en caracteres OEM. Este estilo es muy útil para los controles de edición que contienen nombres de archivo que se usarán en sistemas de archivos que no admiten Unicode. <br /> Para cambiar este estilo una vez creado el control, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>. <br /> | 
| <span id="ES_PASSWORD"></span><span id="es_password"></span><dl><dt><strong>ES_PASSWORD</strong></dt></dl> | Muestra un asterisco (*) para cada carácter que se escribe en el control de edición. Este estilo solo es válido para controles de edición de una sola línea. <br /> Para cambiar los caracteres que se muestran, o bien establecer o borrar este estilo, use <a href="em-setpasswordchar.md"><strong>el EM_SETPASSWORDCHAR</strong></a> mensaje. <br /><blockquote>[!Note]<br />Para usar Comctl32.dll versión 6, es especificarlo en un manifiesto. Para obtener más información sobre los manifiestos, vea <a href="cookbook-overview.md">Habilitar estilos visuales.</a></blockquote><br /> | 
| <span id="ES_READONLY"></span><span id="es_readonly"></span><dl><dt><strong>ES_READONLY</strong></dt></dl> | Impide que el usuario escriba o edite texto en el control de edición.<br /> Para cambiar este estilo una vez creado el control, use el <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> mensaje. <br /> | 
| <span id="ES_RIGHT"></span><span id="es_right"></span><dl><dt><strong>ES_RIGHT</strong></dt></dl> | Alinea a la derecha el texto en un control de edición de una o varias líneas.<br /> | 
| <span id="ES_UPPERCASE"></span><span id="es_uppercase"></span><dl><dt><strong>ES_UPPERCASE</strong></dt></dl> | Convierte todos los caracteres en mayúsculas a medida que se escriben en el control de edición. <br /> Para cambiar este estilo una vez creado el control, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br /> | 
| <span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl><dt><strong>ES_WANTRETURN</strong></dt></dl> | Especifica que se inserte un retorno de carro cuando el usuario presione la tecla ENTRAR mientras escribe texto en un control de edición multilínea en un cuadro de diálogo. Si no especifica este estilo, presionar la tecla ENTRAR tiene el mismo efecto que presionar el botón de inserción predeterminado del cuadro de diálogo. Este estilo no tiene ningún efecto en un control de edición de una sola línea. <br /> Para cambiar este estilo una vez creado el control, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winuser.h</dt> </dl> |



