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
# <a name="using-rich-edit-controls"></a>Usar controles Rich Edit

Esta sección contiene temas que muestran cómo crear y usar controles Rich Edit.

## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="create-rich-edit-controls.md">Cómo crear controles Rich Edit</a><br/></td>
<td>Para crear un control Rich Edit, llame a la función <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> y especifique la clase Rich Edit Window. Para Microsoft Rich Edit 4,1 (Msftedit.dll), especifique MSFTEDIT_CLASS como clase de ventana. En todas las versiones anteriores, especifique RICHEDIT_CLASS. Para obtener más información, vea <a href="about-rich-edit-controls.md">versiones de Rich Edit</a>. <br/> Los controles Rich Edit admiten la mayoría de los estilos de ventana que se usan con los controles de edición, así como estilos adicionales. Debe especificar el estilo de ventana <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> si desea permitir más de una línea de texto en el control. Para obtener más información, vea <a href="rich-edit-control-styles.md">estilos de control Rich Edit</a>. <br/></td>
</tr>
<tr class="even">
<td><a href="format-text-in-rich-edit-controls.md">Cómo dar formato al texto en los controles Rich Edit</a><br/></td>
<td>Una aplicación puede enviar mensajes a un control Rich Edit con el fin de dar formato a caracteres y párrafos y recuperar información de formato. Los atributos de formato de párrafo incluyen alineación, tabulaciones, sangrías, numeración y tablas simples. En el caso de los caracteres, puede especificar el nombre, el tamaño, el color y los efectos de la fuente, como Bold, Italic y protected. <br/></td>
</tr>
<tr class="odd">
<td><a href="interact-with-the-current-selection.md">Cómo interactuar con la selección actual</a><br/></td>
<td>El usuario puede seleccionar texto en un control Rich Edit mediante el mouse o el teclado. La <em>selección actual</em> es el intervalo de caracteres seleccionados o la posición del punto de inserción si no se selecciona ningún carácter. Una aplicación puede obtener información sobre la selección actual, establecerla, determinar cuándo cambia y mostrar u ocultar el resaltado de la selección. <br/></td>
</tr>
<tr class="even">
<td><a href="use-rich-edit-text-operations.md">Cómo usar operaciones de edición de texto enriquecidas</a><br/></td>
<td>Una aplicación puede enviar mensajes para recuperar o buscar texto en un control Rich Edit. Puede recuperar el texto seleccionado o un intervalo de texto especificado. <br/></td>
</tr>
<tr class="odd">
<td><a href="use-word-and-line-break-information.md">Cómo usar la información de saltos de línea y de palabra</a><br/></td>
<td>Un control Rich Edit llama a una función denominada procedimiento de separación de palabras para buscar saltos entre palabras y para determinar dónde se pueden dividir las líneas. El control utiliza esta información al realizar operaciones de ajuste de texto y al procesar las combinaciones de teclas CTRL + flecha izquierda y CTRL + flecha derecha. Una aplicación puede enviar mensajes a un control Rich Edit para reemplazar el procedimiento predeterminado de separación de palabras, para recuperar información de separación de palabras y para determinar en qué línea cae un carácter determinado. <br/></td>
</tr>
<tr class="even">
<td><a href="use-rich-edit-clipboard-operations.md">Cómo usar las operaciones de edición enriquecida del portapapeles</a><br/></td>
<td>Una aplicación puede pegar el contenido del portapapeles en un control Rich Edit mediante el mejor formato de Portapapeles disponible o un formato específico del portapapeles. También puede determinar si un control Rich Edit es capaz de pegar un formato de Portapapeles. <br/></td>
</tr>
<tr class="odd">
<td><a href="use-streams.md">Cómo usar secuencias</a><br/></td>
<td>Puede usar secuencias para transferir datos dentro o fuera de un control Rich Edit. Una secuencia se define mediante una estructura <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>EDITSTREAM</strong></a> , que especifica un búfer y una función de devolución de llamada definida por la aplicación. <br/></td>
</tr>
<tr class="even">
<td><a href="automatically-resize-rich-edit-controls.md">Cómo cambiar automáticamente el tamaño de los controles Rich Edit</a><br/></td>
<td>Una aplicación puede cambiar el tamaño de un control Rich Edit según sea necesario para que tenga siempre el mismo tamaño que su contenido. Un control Rich Edit admite esto, lo que <em>se denomina funcionalidad</em> sin límite mediante el envío de su ventana primaria a un código de notificación de <a href="en-requestresize.md">EN_REQUESTRESIZE</a> cada vez que cambia el tamaño del contenido del control. <br/></td>
</tr>
<tr class="odd">
<td><a href="use-rich-edit-control-notification-codes.md">Cómo usar los códigos de notificación de control Rich Edit</a><br/></td>
<td>La ventana primaria de un control Rich Edit puede procesar los códigos de notificación para supervisar los eventos que afectan al control. Los controles Rich Edit admiten todos los códigos de notificación que se usan con controles de edición, así como varios otros. <br/></td>
</tr>
<tr class="even">
<td><a href="use-font-binding-in-rich-edit-controls.md">Cómo usar el enlace de fuentes en controles Rich Edit</a><br/></td>
<td>Microsoft Rich Edit 3,0 asigna un juego de caracteres a caracteres de texto sin formato en función de su contexto. Ejemplos: <br/>
<ul>
<li>Los caracteres griegos se asignan <strong>GREEK_CHARSET</strong>.</li>
<li>Los símbolos hangul se asignan <strong>HANGUL_CHARSET</strong>.</li>
<li>Los caracteres chinos se asignan <strong>SHIFTJIS_CHARSET</strong> si los caracteres kana se encuentran cerca o <strong>GB2312_CHARSET</strong> si no se encuentra ningún Kana cerca.</li>
<li>Los caracteres ANSI no neutros se asignan <strong>ANSI_CHARSET</strong> en cualquier evento.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="using-rich-edit-com.md">Cómo usar OLE en controles Rich Edit</a><br/></td>
<td>Esta sección contiene información acerca del uso de la vinculación e incrustación de objetos (OLE) en controles Rich Edit. <br/></td>
</tr>
<tr class="even">
<td><a href="printing-rich-edit-controls.md">Cómo imprimir el contenido de los controles Rich Edit</a><br/></td>
<td>Esta sección contiene información sobre cómo imprimir el contenido de los controles Rich Edit. <br/></td>
</tr>
</tbody>
</table>



 

 

