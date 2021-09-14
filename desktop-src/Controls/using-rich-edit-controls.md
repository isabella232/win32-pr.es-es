---
title: Usar controles Rich Edit
description: Esta sección contiene temas que muestran cómo crear y usar controles de edición enriquecidos.
ms.assetid: 2c4717c9-3257-42d5-9c36-89b7e524e788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce4d6565160babc896ea9affe2d5c0c772c5b77e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165302"
---
# <a name="using-rich-edit-controls"></a>Usar controles Rich Edit

Esta sección contiene temas que muestran cómo crear y usar controles de edición enriquecidos.

## <a name="in-this-section"></a>En esta sección




| Tema | Descripción | 
|-------|-------------|
| <a href="create-rich-edit-controls.md">Cómo crear controles rich edit</a><br /> | Para crear un control de edición enriquecido, llame a <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>la función CreateWindowEx</strong></a> y especifique la clase de ventana rich edit. Para Microsoft Rich Edit 4.1 (Msftedit.dll), especifique MSFTEDIT_CLASS como clase de ventana. Para todas las versiones anteriores, especifique RICHEDIT_CLASS. Para obtener más información, vea <a href="about-rich-edit-controls.md">Versions of Rich Edit</a>. <br /> Los controles de edición enriquecciones admiten la mayoría de los estilos de ventana usados con controles de edición, así como estilos adicionales. Debe especificar el estilo <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> de ventana si desea permitir más de una línea de texto en el control . Para obtener más información, vea <a href="rich-edit-control-styles.md">Rich Edit Control Styles</a>. <br /> | 
| <a href="format-text-in-rich-edit-controls.md">Cómo dar formato al texto en controles Rich Edit</a><br /> | Una aplicación puede enviar mensajes a un control de edición enriquecido para dar formato a caracteres y párrafos y recuperar información de formato. Los atributos de formato de párrafo incluyen alineación, pestañas, sangrías, numeración y tablas simples. En el caso de los caracteres, puede especificar el nombre, el tamaño, el color y los efectos de la fuente, como negrita, cursiva y protegido. <br /> | 
| <a href="interact-with-the-current-selection.md">Cómo interactuar con la selección actual</a><br /> | El usuario puede seleccionar texto en un control de edición enriquecido mediante el mouse o el teclado. La <em>selección actual es</em> el intervalo de caracteres seleccionados o la posición del punto de inserción si no se selecciona ningún carácter. Una aplicación puede obtener información sobre la selección actual, establecerla, determinar cuándo cambia y mostrar u ocultar el resaltado de selección. <br /> | 
| <a href="use-rich-edit-text-operations.md">Cómo usar operaciones de edición de texto enriquecido</a><br /> | Una aplicación puede enviar mensajes para recuperar o buscar texto en un control de edición enriquecido. Puede recuperar el texto seleccionado o un intervalo de texto especificado. <br /> | 
| <a href="use-word-and-line-break-information.md">Cómo usar la información de saltos de línea y palabras</a><br /> | Un control de edición enriquecido llama a una función denominada procedimiento de salto de palabras para buscar saltos entre palabras y determinar dónde puede interrumpir líneas. El control usa esta información al realizar operaciones de ajuste de palabras y al procesar las combinaciones de teclas CTRL+FLECHA IZQUIERDA y CTRL+FLECHA DERECHA. Una aplicación puede enviar mensajes a un control de edición enriquecido para reemplazar el procedimiento predeterminado de salto de palabras, recuperar información de salto de palabras y determinar en qué línea se encuentra un carácter determinado. <br /> | 
| <a href="use-rich-edit-clipboard-operations.md">Cómo usar las operaciones de edición enriquecte del Portapapeles</a><br /> | Una aplicación puede pegar el contenido del Portapapeles en un control de edición enriquecido mediante el mejor formato de Portapapeles disponible o un formato de Portapapeles específico. También puede determinar si un control de edición enriquecido es capaz de pegar un formato del Portapapeles. <br /> | 
| <a href="use-streams.md">Uso de Secuencias</a><br /> | Puede usar secuencias para transferir datos dentro o fuera de un control de edición enriquecido. Una secuencia se define mediante una <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>estructura EDITSTREAM,</strong></a> que especifica un búfer y una función de devolución de llamada definida por la aplicación. <br /> | 
| <a href="automatically-resize-rich-edit-controls.md">Cómo cambiar automáticamente el tamaño de los controles Rich Edit</a><br /> | Una aplicación puede cambiar el tamaño de un control de edición enriquecido según sea necesario para que siempre sea del mismo tamaño que su contenido. Un control de edición <em></em> enriquecido admite esta funcionalidad denominada sin fondo al enviar <a href="en-requestresize.md">a</a> su ventana primaria un código de notificación EN_REQUESTRESIZE cada vez que cambia el tamaño del contenido del control. <br /> | 
| <a href="use-rich-edit-control-notification-codes.md">Cómo usar los códigos de notificación del control Rich Edit</a><br /> | La ventana primaria de un control de edición enriquecido puede procesar códigos de notificación para supervisar los eventos que afectan al control. Los controles de edición enriquecciones admiten todos los códigos de notificación que se usan con los controles de edición, así como varios más. <br /> | 
| <a href="use-font-binding-in-rich-edit-controls.md">Cómo usar el enlace de fuentes en controles Rich Edit</a><br /> | Microsoft Rich Edit 3.0 asigna un juego de caracteres a caracteres de texto sin formato en función de su contexto. Ejemplos: <br /><ul><li>Se asignan caracteres griegos <strong>GREEK_CHARSET</strong>.</li><li>Los símbolos hangul se <strong>asignan HANGUL_CHARSET</strong>.</li><li>Los caracteres en <strong>chino se SHIFTJIS_CHARSET</strong> si se encuentran caracteres kana cerca o GB2312_CHARSET si no se encuentra ningún kana cerca. <strong></strong></li><li>Los caracteres ANSI no neutros se <strong>asignan ANSI_CHARSET</strong> en cualquier evento.</li></ul> | 
| <a href="using-rich-edit-com.md">Cómo usar OLE en controles rich edit</a><br /> | Esta sección contiene información sobre el uso de la vinculación e inserción de objetos (OLE) en controles rich edit. <br /> | 
| <a href="printing-rich-edit-controls.md">Cómo imprimir el contenido de los controles Rich Edit</a><br /> | Esta sección contiene información sobre cómo imprimir el contenido de controles de edición enriquecidos. <br /> | 




 

 

