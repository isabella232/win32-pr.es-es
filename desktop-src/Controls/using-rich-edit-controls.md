---
title: Usar controles Rich Edit
description: Esta sección contiene temas que muestran cómo crear y usar controles Rich Edit.
ms.assetid: 2c4717c9-3257-42d5-9c36-89b7e524e788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0489660bb6849d0de76ae7fc2f4e21ca931662a8
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104488422"
---
# <a name="using-rich-edit-controls"></a><span data-ttu-id="c4dbb-103">Usar controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="c4dbb-103">Using Rich Edit Controls</span></span>

<span data-ttu-id="c4dbb-104">Esta sección contiene temas que muestran cómo crear y usar controles Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-104">This section contains topics that demonstrate how to create and use rich edit controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c4dbb-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c4dbb-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c4dbb-106">Tema</span><span class="sxs-lookup"><span data-stu-id="c4dbb-106">Topic</span></span></th>
<th><span data-ttu-id="c4dbb-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4dbb-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4dbb-108"><a href="create-rich-edit-controls.md">Cómo crear controles Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="c4dbb-108"><a href="create-rich-edit-controls.md">How to Create Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="c4dbb-109">Para crear un control Rich Edit, llame a la función <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> y especifique la clase Rich Edit Window.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-109">To create a rich edit control, call the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> function, specifying the rich edit window class.</span></span> <span data-ttu-id="c4dbb-110">Para Microsoft Rich Edit 4,1 (Msftedit.dll), especifique MSFTEDIT_CLASS como clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-110">For Microsoft Rich Edit 4.1 (Msftedit.dll), specify MSFTEDIT_CLASS as the window class.</span></span> <span data-ttu-id="c4dbb-111">En todas las versiones anteriores, especifique RICHEDIT_CLASS.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-111">For all previous versions, specify RICHEDIT_CLASS.</span></span> <span data-ttu-id="c4dbb-112">Para obtener más información, vea <a href="about-rich-edit-controls.md">versiones de Rich Edit</a>.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-112">For more information, see <a href="about-rich-edit-controls.md">Versions of Rich Edit</a>.</span></span> <br/> <span data-ttu-id="c4dbb-113">Los controles Rich Edit admiten la mayoría de los estilos de ventana que se usan con los controles de edición, así como estilos adicionales.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-113">Rich edit controls support most of the window styles used with edit controls as well as additional styles.</span></span> <span data-ttu-id="c4dbb-114">Debe especificar el estilo de ventana <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> si desea permitir más de una línea de texto en el control.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-114">You should specify the <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> window style if you want to allow more than one line of text in the control.</span></span> <span data-ttu-id="c4dbb-115">Para obtener más información, vea <a href="rich-edit-control-styles.md">estilos de control Rich Edit</a>.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-115">For more information, see <a href="rich-edit-control-styles.md">Rich Edit Control Styles</a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4dbb-116"><a href="format-text-in-rich-edit-controls.md">Cómo dar formato al texto en los controles Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="c4dbb-116"><a href="format-text-in-rich-edit-controls.md">How to Format Text in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="c4dbb-117">Una aplicación puede enviar mensajes a un control Rich Edit con el fin de dar formato a caracteres y párrafos y recuperar información de formato.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-117">An application can send messages to a rich edit control in order to format characters and paragraphs and retrieve formatting information.</span></span> <span data-ttu-id="c4dbb-118">Los atributos de formato de párrafo incluyen alineación, tabulaciones, sangrías, numeración y tablas simples.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-118">Paragraph formatting attributes include alignment, tabs, indents, numbering, and simple tables.</span></span> <span data-ttu-id="c4dbb-119">En el caso de los caracteres, puede especificar el nombre, el tamaño, el color y los efectos de la fuente, como Bold, Italic y protected.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-119">For characters, you can specify font name, size, color, and effects such as bold, italic, and protected.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4dbb-120"><a href="interact-with-the-current-selection.md">Cómo interactuar con la selección actual</a></span><span class="sxs-lookup"><span data-stu-id="c4dbb-120"><a href="interact-with-the-current-selection.md">How to Interact with the Current Selection</a></span></span><br/></td>
<td><span data-ttu-id="c4dbb-121">El usuario puede seleccionar texto en un control Rich Edit mediante el mouse o el teclado.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-121">The user can select text in a rich edit control by using the mouse or the keyboard.</span></span> <span data-ttu-id="c4dbb-122">La <em>selección actual</em> es el intervalo de caracteres seleccionados o la posición del punto de inserción si no se selecciona ningún carácter.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-122">The <em>current selection</em> is the range of selected characters, or the position of the insertion point if no characters are selected.</span></span> <span data-ttu-id="c4dbb-123">Una aplicación puede obtener información sobre la selección actual, establecerla, determinar cuándo cambia y mostrar u ocultar el resaltado de la selección.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-123">An application can get information about the current selection, set it, determine when it changes, and show or hide the selection highlight.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4dbb-124"><a href="use-rich-edit-text-operations.md">Cómo usar operaciones de edición de texto enriquecidas</a></span><span class="sxs-lookup"><span data-stu-id="c4dbb-124"><a href="use-rich-edit-text-operations.md">How to Use Rich Edit Text Operations</a></span></span><br/></td>
<td><span data-ttu-id="c4dbb-125">Una aplicación puede enviar mensajes para recuperar o buscar texto en un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-125">An application can send messages to retrieve or find text in a rich edit control.</span></span> <span data-ttu-id="c4dbb-126">Puede recuperar el texto seleccionado o un intervalo de texto especificado.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-126">You can retrieve either the selected text or a specified range of text.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4dbb-127"><a href="use-word-and-line-break-information.md">Cómo usar la información de saltos de línea y de palabra</a></span><span class="sxs-lookup"><span data-stu-id="c4dbb-127"><a href="use-word-and-line-break-information.md">How to Use Word and Line Break Information</a></span></span><br/></td>
<td><span data-ttu-id="c4dbb-128">Un control Rich Edit llama a una función denominada procedimiento de separación de palabras para buscar saltos entre palabras y para determinar dónde se pueden dividir las líneas.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-128">A rich edit control calls a function called a word-break procedure to find breaks between words and to determine where it can break lines.</span></span> <span data-ttu-id="c4dbb-129">El control utiliza esta información al realizar operaciones de ajuste de texto y al procesar las combinaciones de teclas CTRL + flecha izquierda y CTRL + flecha derecha.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-129">The control uses this information when performing word-wrap operations and when processing CTRL+LEFT ARROW key and CTRL+RIGHT ARROW key combinations.</span></span> <span data-ttu-id="c4dbb-130">Una aplicación puede enviar mensajes a un control Rich Edit para reemplazar el procedimiento predeterminado de separación de palabras, para recuperar información de separación de palabras y para determinar en qué línea cae un carácter determinado.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-130">An application can send messages to a rich edit control to replace the default word-break procedure, to retrieve word-break information, and to determine what line a given character falls on.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4dbb-131"><a href="use-rich-edit-clipboard-operations.md">Cómo usar las operaciones de edición enriquecida del portapapeles</a></span><span class="sxs-lookup"><span data-stu-id="c4dbb-131"><a href="use-rich-edit-clipboard-operations.md">How to Use Rich Edit Clipboard Operations</a></span></span><br/></td>
<td><span data-ttu-id="c4dbb-132">Una aplicación puede pegar el contenido del portapapeles en un control Rich Edit mediante el mejor formato de Portapapeles disponible o un formato específico del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-132">An application can paste the contents of the clipboard into a rich edit control by using either the best available clipboard format or a specific clipboard format.</span></span> <span data-ttu-id="c4dbb-133">También puede determinar si un control Rich Edit es capaz de pegar un formato de Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-133">You can also determine whether a rich edit control is capable of pasting a clipboard format.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4dbb-134"><a href="use-streams.md">Cómo usar secuencias</a></span><span class="sxs-lookup"><span data-stu-id="c4dbb-134"><a href="use-streams.md">How to Use Streams</a></span></span><br/></td>
<td><span data-ttu-id="c4dbb-135">Puede usar secuencias para transferir datos dentro o fuera de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-135">You can use streams to transfer data into or out of a rich edit control.</span></span> <span data-ttu-id="c4dbb-136">Una secuencia se define mediante una estructura <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>EDITSTREAM</strong></a> , que especifica un búfer y una función de devolución de llamada definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-136">A stream is defined by an <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>EDITSTREAM</strong></a> structure, which specifies a buffer and an application-defined callback function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4dbb-137"><a href="automatically-resize-rich-edit-controls.md">Cómo cambiar automáticamente el tamaño de los controles Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="c4dbb-137"><a href="automatically-resize-rich-edit-controls.md">How to Automatically Resize Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="c4dbb-138">Una aplicación puede cambiar el tamaño de un control Rich Edit según sea necesario para que tenga siempre el mismo tamaño que su contenido.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-138">An application can resize a rich edit control as needed so that it is always the same size as its contents.</span></span> <span data-ttu-id="c4dbb-139">Un control Rich Edit admite esto, lo que <em>se denomina funcionalidad</em> sin límite mediante el envío de su ventana primaria a un código de notificación de <a href="en-requestresize.md">EN_REQUESTRESIZE</a> cada vez que cambia el tamaño del contenido del control.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-139">A rich edit control supports this so-called <em>bottomless</em> functionality by sending its parent window an <a href="en-requestresize.md">EN_REQUESTRESIZE</a> notification code whenever the size of the control's content changes.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4dbb-140"><a href="use-rich-edit-control-notification-codes.md">Cómo usar los códigos de notificación de control Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="c4dbb-140"><a href="use-rich-edit-control-notification-codes.md">How to Use Rich Edit Control Notification Codes</a></span></span><br/></td>
<td><span data-ttu-id="c4dbb-141">La ventana primaria de un control Rich Edit puede procesar los códigos de notificación para supervisar los eventos que afectan al control.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-141">A rich edit control's parent window can process notification codes to monitor events that affect the control.</span></span> <span data-ttu-id="c4dbb-142">Los controles Rich Edit admiten todos los códigos de notificación que se usan con controles de edición, así como varios otros.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-142">Rich edit controls support all of the notification codes that are used with edit controls, as well as several additional ones.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4dbb-143"><a href="use-font-binding-in-rich-edit-controls.md">Cómo usar el enlace de fuentes en controles Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="c4dbb-143"><a href="use-font-binding-in-rich-edit-controls.md">How to Use Font Binding in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="c4dbb-144">Microsoft Rich Edit 3,0 asigna un juego de caracteres a caracteres de texto sin formato en función de su contexto.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-144">Microsoft Rich Edit 3.0 assigns a character set to plain-text characters depending on their context.</span></span> <span data-ttu-id="c4dbb-145">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="c4dbb-145">Some examples are:</span></span> <br/>
<ul>
<li><span data-ttu-id="c4dbb-146">Los caracteres griegos se asignan <strong>GREEK_CHARSET</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-146">Greek characters are assigned <strong>GREEK_CHARSET</strong>.</span></span></li>
<li><span data-ttu-id="c4dbb-147">Los símbolos hangul se asignan <strong>HANGUL_CHARSET</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-147">Hangul symbols are assigned <strong>HANGUL_CHARSET</strong>.</span></span></li>
<li><span data-ttu-id="c4dbb-148">Los caracteres chinos se asignan <strong>SHIFTJIS_CHARSET</strong> si los caracteres kana se encuentran cerca o <strong>GB2312_CHARSET</strong> si no se encuentra ningún Kana cerca.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-148">Chinese characters are assigned <strong>SHIFTJIS_CHARSET</strong> if kana characters are found nearby, or <strong>GB2312_CHARSET</strong> if no kana are found nearby.</span></span></li>
<li><span data-ttu-id="c4dbb-149">Los caracteres ANSI no neutros se asignan <strong>ANSI_CHARSET</strong> en cualquier evento.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-149">Non-neutral ANSI characters are assigned <strong>ANSI_CHARSET</strong> in any event.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4dbb-150"><a href="using-rich-edit-com.md">Cómo usar OLE en controles Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="c4dbb-150"><a href="using-rich-edit-com.md">How to Use OLE in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="c4dbb-151">Esta sección contiene información acerca del uso de la vinculación e incrustación de objetos (OLE) en controles Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-151">This section contains information about using object linking and embedding (OLE) in rich edit controls.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4dbb-152"><a href="printing-rich-edit-controls.md">Cómo imprimir el contenido de los controles Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="c4dbb-152"><a href="printing-rich-edit-controls.md">How to Print the Contents of Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="c4dbb-153">Esta sección contiene información sobre cómo imprimir el contenido de los controles Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-153">This section contains information about how to print the contents of rich edit controls.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

 

