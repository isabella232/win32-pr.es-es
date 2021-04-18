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
# <a name="edit-control-styles"></a><span data-ttu-id="12fa2-103">Editar estilos de control</span><span class="sxs-lookup"><span data-stu-id="12fa2-103">Edit Control Styles</span></span>

<span data-ttu-id="12fa2-104">Para crear un control de edición mediante la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especifique la clase Edit, las constantes de estilo de ventana apropiadas y una combinación de los siguientes estilos de control de edición.</span><span class="sxs-lookup"><span data-stu-id="12fa2-104">To create an edit control using the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specify the EDIT class, appropriate window style constants, and a combination of the following edit control styles.</span></span> <span data-ttu-id="12fa2-105">Una vez creado el control, estos estilos no se pueden modificar, salvo que se indique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="12fa2-105">After the control has been created, these styles cannot be modified, except as noted.</span></span>

## <a name="example"></a><span data-ttu-id="12fa2-106">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="12fa2-106">Example</span></span>

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

<span data-ttu-id="12fa2-107">Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) en github.</span><span class="sxs-lookup"><span data-stu-id="12fa2-107">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) on GitHub.</span></span>

## <a name="constants"></a><span data-ttu-id="12fa2-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="12fa2-108">Constants</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="12fa2-109">Constante</span><span class="sxs-lookup"><span data-stu-id="12fa2-109">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="12fa2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="12fa2-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <span data-ttu-id="12fa2-111"><dt><strong>ES_AUTOHSCROLL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="12fa2-111"><dt><strong>ES_AUTOHSCROLL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="12fa2-112">Desplaza automáticamente el texto a la derecha 10 caracteres cuando el usuario escribe un carácter al final de la línea.</span><span class="sxs-lookup"><span data-stu-id="12fa2-112">Automatically scrolls text to the right by 10 characters when the user types a character at the end of the line.</span></span> <span data-ttu-id="12fa2-113">Cuando el usuario presiona la tecla entrar, el control vuelve a desplazar todo el texto hasta la posición cero.</span><span class="sxs-lookup"><span data-stu-id="12fa2-113">When the user presses the ENTER key, the control scrolls all text back to position zero.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <span data-ttu-id="12fa2-114"><dt><strong>ES_AUTOVSCROLL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="12fa2-114"><dt><strong>ES_AUTOVSCROLL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="12fa2-115">Desplaza automáticamente el texto una página cuando el usuario presiona la tecla entrar en la última línea.</span><span class="sxs-lookup"><span data-stu-id="12fa2-115">Automatically scrolls text up one page when the user presses the ENTER key on the last line.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_CENTER"></span><span id="es_center"></span><dl> <span data-ttu-id="12fa2-116"><dt><strong>ES_CENTER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="12fa2-116"><dt><strong>ES_CENTER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="12fa2-117">Centra el texto en un control de edición de línea única o multilínea.</span><span class="sxs-lookup"><span data-stu-id="12fa2-117">Centers text in a single-line or multiline edit control.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_LEFT"></span><span id="es_left"></span><dl> <span data-ttu-id="12fa2-118"><dt><strong>ES_LEFT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="12fa2-118"><dt><strong>ES_LEFT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="12fa2-119">Alinea el texto con el margen izquierdo.</span><span class="sxs-lookup"><span data-stu-id="12fa2-119">Aligns text with the left margin.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_LOWERCASE"></span><span id="es_lowercase"></span><dl> <span data-ttu-id="12fa2-120"><dt><strong>ES_LOWERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="12fa2-120"><dt><strong>ES_LOWERCASE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="12fa2-121">Convierte todos los caracteres a minúsculas a medida que se escriben en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="12fa2-121">Converts all characters to lowercase as they are typed into the edit control.</span></span><br/> <span data-ttu-id="12fa2-122">Para cambiar este estilo una vez creado el control, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="12fa2-122">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <span data-ttu-id="12fa2-123"><dt><strong>ES_MULTILINE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="12fa2-123"><dt><strong>ES_MULTILINE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="12fa2-124">Designa un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="12fa2-124">Designates a multiline edit control.</span></span> <span data-ttu-id="12fa2-125">El valor predeterminado es el control de edición de una sola línea.</span><span class="sxs-lookup"><span data-stu-id="12fa2-125">The default is single-line edit control.</span></span> <br/> <span data-ttu-id="12fa2-126">Cuando el control de edición multilínea está en un cuadro de diálogo, la respuesta predeterminada a presionar la tecla entrar es activar el botón predeterminado.</span><span class="sxs-lookup"><span data-stu-id="12fa2-126">When the multiline edit control is in a dialog box, the default response to pressing the ENTER key is to activate the default button.</span></span> <span data-ttu-id="12fa2-127">Para usar la tecla entrar como un retorno de carro, use el estilo <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="12fa2-127">To use the ENTER key as a carriage return, use the <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> style.</span></span><br/> <span data-ttu-id="12fa2-128">Cuando el control de edición multilínea no está en un cuadro de diálogo y se especifica el estilo de <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> , el control de edición muestra tantas líneas como sea posible y se desplaza verticalmente cuando el usuario presiona la tecla entrar.</span><span class="sxs-lookup"><span data-stu-id="12fa2-128">When the multiline edit control is not in a dialog box and the <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> style is specified, the edit control shows as many lines as possible and scrolls vertically when the user presses the ENTER key.</span></span> <span data-ttu-id="12fa2-129">Si no se especifica <strong>ES_AUTOVSCROLL</strong>, el control de edición muestra tantas líneas como sea posible y emite un pitido si el usuario presiona la tecla entrar cuando no se pueden mostrar más líneas.</span><span class="sxs-lookup"><span data-stu-id="12fa2-129">If you do not specify <strong>ES_AUTOVSCROLL</strong>, the edit control shows as many lines as possible and beeps if the user presses the ENTER key when no more lines can be displayed.</span></span><br/> <span data-ttu-id="12fa2-130">Si especifica el estilo de <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> , el control de edición de varias líneas se desplaza horizontalmente de forma automática cuando el símbolo de intercalación va más allá del borde derecho del control.</span><span class="sxs-lookup"><span data-stu-id="12fa2-130">If you specify the <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> style, the multiline edit control automatically scrolls horizontally when the caret goes past the right edge of the control.</span></span> <span data-ttu-id="12fa2-131">Para iniciar una nueva línea, el usuario debe presionar la tecla entrar.</span><span class="sxs-lookup"><span data-stu-id="12fa2-131">To start a new line, the user must press the ENTER key.</span></span> <span data-ttu-id="12fa2-132">Si no se especifica <strong>ES_AUTOHSCROLL</strong>, el control ajusta automáticamente las palabras al principio de la línea siguiente cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="12fa2-132">If you do not specify <strong>ES_AUTOHSCROLL</strong>, the control automatically wraps words to the beginning of the next line when necessary.</span></span> <span data-ttu-id="12fa2-133">También se inicia una nueva línea si el usuario presiona la tecla entrar.</span><span class="sxs-lookup"><span data-stu-id="12fa2-133">A new line is also started if the user presses the ENTER key.</span></span> <span data-ttu-id="12fa2-134">El tamaño de la ventana determina la posición del ajuste de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="12fa2-134">The window size determines the position of the Wordwrap.</span></span> <span data-ttu-id="12fa2-135">Si cambia el tamaño de la ventana, la posición de aparecen cambia y se vuelve a mostrar el texto.</span><span class="sxs-lookup"><span data-stu-id="12fa2-135">If the window size changes, the Wordwrapping position changes and the text is redisplayed.</span></span><br/> <span data-ttu-id="12fa2-136">Los controles de edición multilínea pueden tener barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="12fa2-136">Multiline edit controls can have scroll bars.</span></span> <span data-ttu-id="12fa2-137">Un control de edición con barras de desplazamiento procesa sus propios mensajes de barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="12fa2-137">An edit control with scroll bars processes its own scroll bar messages.</span></span> <span data-ttu-id="12fa2-138">Tenga en cuenta que los controles de edición sin barras de desplazamiento se desplazan como se describe en los párrafos anteriores y procesan los mensajes de desplazamiento enviados por la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="12fa2-138">Note that edit controls without scroll bars scroll as described in the previous paragraphs and process any scroll messages sent by the parent window.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <span data-ttu-id="12fa2-139"><dt><strong>ES_NOHIDESEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="12fa2-139"><dt><strong>ES_NOHIDESEL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="12fa2-140">Niega el comportamiento predeterminado de un control de edición.</span><span class="sxs-lookup"><span data-stu-id="12fa2-140">Negates the default behavior for an edit control.</span></span> <span data-ttu-id="12fa2-141">El comportamiento predeterminado oculta la selección cuando el control pierde el foco de entrada e invierte la selección cuando el control recibe el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="12fa2-141">The default behavior hides the selection when the control loses the input focus and inverts the selection when the control receives the input focus.</span></span> <span data-ttu-id="12fa2-142">Si especifica <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, se invierte el texto seleccionado, incluso si el control no tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="12fa2-142">If you specify <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, the selected text is inverted, even if the control does not have the focus.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_NUMBER"></span><span id="es_number"></span><dl> <span data-ttu-id="12fa2-143"><dt><strong>ES_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="12fa2-143"><dt><strong>ES_NUMBER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="12fa2-144">Permite que solo se escriban dígitos en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="12fa2-144">Allows only digits to be entered into the edit control.</span></span> <span data-ttu-id="12fa2-145">Tenga en cuenta que, incluso con este conjunto, todavía es posible pegar no dígitos en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="12fa2-145">Note that, even with this set, it is still possible to paste non-digits into the edit control.</span></span> <br/> <span data-ttu-id="12fa2-146">Para cambiar este estilo una vez creado el control, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="12fa2-146">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/> <span data-ttu-id="12fa2-147">Para traducir el texto que se especificó en el control de edición a un valor entero, utilice la función <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>GetDlgItemInt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="12fa2-147">To translate text that was entered into the edit control to an integer value, use the <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>GetDlgItemInt</strong></a> function.</span></span> <span data-ttu-id="12fa2-148">Para establecer el texto del control de edición en la representación de cadena de un entero especificado, utilice la función <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>SetDlgItemInt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="12fa2-148">To set the text of the edit control to the string representation of a specified integer, use the <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>SetDlgItemInt</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_OEMCONVERT"></span><span id="es_oemconvert"></span><dl> <span data-ttu-id="12fa2-149"><dt><strong>ES_OEMCONVERT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="12fa2-149"><dt><strong>ES_OEMCONVERT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="12fa2-150">Convierte el texto escrito en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="12fa2-150">Converts text entered in the edit control.</span></span> <span data-ttu-id="12fa2-151">El texto se convierte del juego de caracteres de Windows al Juego de caracteres OEM y, a continuación, de nuevo al Juego de caracteres de Windows.</span><span class="sxs-lookup"><span data-stu-id="12fa2-151">The text is converted from the Windows character set to the OEM character set and then back to the Windows character set.</span></span> <span data-ttu-id="12fa2-152">Esto garantiza una conversión de caracteres adecuada cuando la aplicación llama a la función <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> para convertir una cadena de Windows del control de edición en caracteres OEM.</span><span class="sxs-lookup"><span data-stu-id="12fa2-152">This ensures proper character conversion when the application calls the <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> function to convert a Windows string in the edit control to OEM characters.</span></span> <span data-ttu-id="12fa2-153">Este estilo es muy útil para los controles de edición que contienen nombres de archivo que se utilizarán en sistemas de archivos que no admiten Unicode.</span><span class="sxs-lookup"><span data-stu-id="12fa2-153">This style is most useful for edit controls that contain file names that will be used on file systems that do not support Unicode.</span></span> <br/> <span data-ttu-id="12fa2-154">Para cambiar este estilo una vez creado el control, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="12fa2-154">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <span data-ttu-id="12fa2-155"><dt><strong>ES_PASSWORD</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="12fa2-155"><dt><strong>ES_PASSWORD</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="12fa2-156">Muestra un asterisco (\*) para cada carácter que se escribe en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="12fa2-156">Displays an asterisk (\*) for each character typed into the edit control.</span></span> <span data-ttu-id="12fa2-157">Este estilo solo es válido para los controles de edición de una sola línea.</span><span class="sxs-lookup"><span data-stu-id="12fa2-157">This style is valid only for single-line edit controls.</span></span> <br/> <span data-ttu-id="12fa2-158">Para cambiar los caracteres que se muestran, o para establecer o desactivar este estilo, utilice el mensaje de <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="12fa2-158">To change the characters that is displayed, or set or clear this style, use the <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> message.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="12fa2-159">Para usar Comctl32.dll versión 6, especifíquelo en un manifiesto.</span><span class="sxs-lookup"><span data-stu-id="12fa2-159">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="12fa2-160">Para obtener más información sobre los manifiestos, vea <a href="cookbook-overview.md">habilitar estilos visuales</a>.</span><span class="sxs-lookup"><span data-stu-id="12fa2-160">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <span data-ttu-id="12fa2-161"><dt><strong>ES_READONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="12fa2-161"><dt><strong>ES_READONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="12fa2-162">Impide que el usuario escriba o modifique texto en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="12fa2-162">Prevents the user from typing or editing text in the edit control.</span></span><br/> <span data-ttu-id="12fa2-163">Para cambiar este estilo una vez creado el control, utilice el mensaje de <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="12fa2-163">To change this style after the control has been created, use the <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> message.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_RIGHT"></span><span id="es_right"></span><dl> <span data-ttu-id="12fa2-164"><dt><strong>ES_RIGHT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="12fa2-164"><dt><strong>ES_RIGHT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="12fa2-165">Alinea a la derecha el texto en un control de edición de una sola línea o multilínea.</span><span class="sxs-lookup"><span data-stu-id="12fa2-165">Right-aligns text in a single-line or multiline edit control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_UPPERCASE"></span><span id="es_uppercase"></span><dl> <span data-ttu-id="12fa2-166"><dt><strong>ES_UPPERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="12fa2-166"><dt><strong>ES_UPPERCASE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="12fa2-167">Convierte todos los caracteres a mayúsculas a medida que se escriben en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="12fa2-167">Converts all characters to uppercase as they are typed into the edit control.</span></span> <br/> <span data-ttu-id="12fa2-168">Para cambiar este estilo una vez creado el control, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="12fa2-168">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <span data-ttu-id="12fa2-169"><dt><strong>ES_WANTRETURN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="12fa2-169"><dt><strong>ES_WANTRETURN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="12fa2-170">Especifica que se inserte un retorno de carro cuando el usuario presione la tecla entrar mientras escribe texto en un control de edición multilínea en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="12fa2-170">Specifies that a carriage return be inserted when the user presses the ENTER key while entering text into a multiline edit control in a dialog box.</span></span> <span data-ttu-id="12fa2-171">Si no especifica este estilo, presionar la tecla entrar tiene el mismo efecto que presionar el botón de opción predeterminado del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="12fa2-171">If you do not specify this style, pressing the ENTER key has the same effect as pressing the dialog box's default push button.</span></span> <span data-ttu-id="12fa2-172">Este estilo no tiene ningún efecto en un control de edición de una sola línea.</span><span class="sxs-lookup"><span data-stu-id="12fa2-172">This style has no effect on a single-line edit control.</span></span> <br/> <span data-ttu-id="12fa2-173">Para cambiar este estilo una vez creado el control, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="12fa2-173">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="12fa2-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12fa2-174">Requirements</span></span>



| <span data-ttu-id="12fa2-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="12fa2-175">Requirement</span></span> | <span data-ttu-id="12fa2-176">Value</span><span class="sxs-lookup"><span data-stu-id="12fa2-176">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="12fa2-177">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12fa2-177">Header</span></span><br/> | <dl> <span data-ttu-id="12fa2-178"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="12fa2-178"><dt>Winuser.h</dt></span></span> </dl> |



