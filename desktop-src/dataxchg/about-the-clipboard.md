---
title: Acerca del Portapapeles
description: En esta sección se describe el Portapapeles.
ms.assetid: 14c91730-a668-495b-9ec6-b835234821a5
keywords:
- clipboard,about
- clipboard,formats
- clipboard,commands
- clipboard,windows
- portapapeles, números de secuencia
- clipboard,viewers
- clipboard,viewer windows
- portapapeles, formatos de presentación
- clipboard, formatos de presentación de propietario
- mostrar formatos del Portapapeles
- formatos del Portapapeles para mostrar del propietario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86a3ddc96cbc1d440fda5e6484f1bc72a53b4b36b709c7ad80c77e203dadcef1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128637"
---
# <a name="about-the-clipboard"></a>Acerca del Portapapeles

El *Portapapeles* es un conjunto de funciones y mensajes que permiten a las aplicaciones transferir datos. Dado que todas las aplicaciones tienen acceso al Portapapeles, los datos se pueden transferir fácilmente entre aplicaciones o dentro de una aplicación.

El Portapapeles está controlado por el usuario. Una ventana debe transferir datos hacia o desde el Portapapeles solo en respuesta a un comando del usuario. Una ventana no debe usar el Portapapeles para transferir datos sin el conocimiento del usuario.

Un objeto de memoria en el Portapapeles puede estar en cualquier formato de datos, denominado formato del Portapapeles. Cada formato se identifica mediante un valor entero sin signo. Para los formatos estándar (predefinidos) del Portapapeles, este valor es una constante definida en Winuser.h; para los formatos registrados del Portapapeles, es el valor devuelto de [**la función RegisterClipboardFormat.**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata)

Excepto para registrar formatos del Portapapeles, las ventanas individuales realizan la mayoría de las operaciones del Portapapeles. Normalmente, un procedimiento de ventana transfiere información hacia o desde el Portapapeles en respuesta al [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)

En esta sección se describe lo siguiente:

-   [Comandos del Portapapeles](#clipboard-commands)
-   [Número de secuencia del Portapapeles](#clipboard-sequence-number)
-   [Visores del Portapapeles](#clipboard-viewers)
    -   [Visor del Portapapeles Windows](#clipboard-viewer-windows)
    -   [Formatos de presentación](#display-formats)
    -   [Formato de presentación del propietario](#owner-display-format)
-   [Temas relacionados](#related-topics)

## <a name="clipboard-commands"></a>Comandos del Portapapeles

Normalmente, un usuario realiza operaciones del Portapapeles eligiendo comandos en el menú Editar **de una** aplicación. A continuación se muestra una breve descripción de los comandos estándar del Portapapeles.



|  Get-Help        |  Descripción                                                                                                                                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Cortar**    | Coloca una copia de la selección actual en el Portapapeles y elimina la selección del documento. Se destruye el contenido anterior del Portapapeles.                                                          |
| **Copiar**   | Coloca una copia de la selección actual en el Portapapeles. El documento permanece sin cambios. Se destruye el contenido anterior del Portapapeles.                                                                      |
| **Pegar**  | Reemplaza la selección actual por el contenido del Portapapeles. No se cambia el contenido del Portapapeles.                                                                                                    |
| **Eliminar** | Elimina la selección actual del documento. No se cambia el contenido del Portapapeles. Este comando no implica el Portapapeles, pero debería aparecer con los comandos del Portapapeles en el **menú** Editar. |



 

## <a name="clipboard-sequence-number"></a>Número de secuencia del Portapapeles

El Portapapeles de cada estación de ventana tiene un número de secuencia del Portapapeles asociado. Este número se incrementa cada vez que cambia el contenido del Portapapeles. Para obtener el número de secuencia del Portapapeles, llame a [**la función GetClipboardSequenceNumber.**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber)

## <a name="clipboard-viewers"></a>Visores del Portapapeles

Un visor del Portapapeles es una ventana que muestra el contenido actual del Portapapeles. La ventana del visor del Portapapeles es una comodidad para el usuario y no afecta a las funciones de transacción de datos del Portapapeles.

Normalmente, una ventana del visor del Portapapeles puede mostrar al menos los tres formatos más comunes: **CF \_ TEXT,** **CF \_ BITMAP** y **CF \_ METAFILEPICT**. Si una ventana no hace que los datos estén disponibles en cualquiera de estos tres formatos, debe proporcionar datos en un formato de presentación o usar el formato de presentación del propietario.

Una *cadena de visor del Portapapeles* es la vinculación de dos o más entidades para que dependan unas de otras para su funcionamiento. Esta interdependencia (cadena) permite que todas las aplicaciones de visor del Portapapeles en ejecución reciban los mensajes enviados al Portapapeles actual.

En esta sección se tratan los temas siguientes.

-   [Visor del Portapapeles Windows](#clipboard-viewer-windows)
-   [Formatos de presentación](#display-formats)
-   [Formato de presentación del propietario](#owner-display-format)

### <a name="clipboard-viewer-windows"></a>Visor del Portapapeles Windows

Una ventana se agrega a la cadena del visor del Portapapeles mediante una llamada a la [**función SetClipboardViewer.**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) El valor devuelto es el identificador de la siguiente ventana de la cadena. Para recuperar el identificador en la primera ventana de la cadena, llame a la [**función GetClipboardViewer.**](/windows/desktop/api/Winuser/nf-winuser-getclipboardviewer)

Cada ventana del visor del Portapapeles debe realizar un seguimiento de la siguiente ventana de la cadena de visor del Portapapeles. Cuando cambia el contenido del Portapapeles, el sistema envía un mensaje [**\_ DRAWCLIPBOARD**](wm-drawclipboard.md) de WM a la primera ventana de la cadena. Después de actualizar su presentación, cada ventana del visor del Portapapeles debe pasar este mensaje a la siguiente ventana de la cadena.

Antes de cerrar, una ventana del visor del Portapapeles debe quitarse de la cadena del visor del Portapapeles mediante una llamada a [**la función ChangeClipboardChain.**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) A continuación, el sistema envía un [**\_ mensaje DE WM CHANGECBCHAIN**](wm-changecbchain.md) a la primera ventana de la cadena.

Para obtener más información sobre cómo procesar los [**mensajes WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) y [**WM \_ CHANGECBCHAIN,**](wm-changecbchain.md) vea Crear una [ventana del Visor del Portapapeles.](using-the-clipboard.md)

### <a name="display-formats"></a>Formatos de visualización

Un formato de presentación es un formato del Portapapeles que se usa para mostrar información en una ventana del visor del Portapapeles. Un propietario del Portapapeles que use un formato de Portapapeles privado o registrado, y ninguno de los formatos estándar más comunes, debe proporcionar datos en un formato de presentación para verlos en una ventana del visor del Portapapeles. Los formatos de presentación están diseñados solo para su visualización y no deben pegarse en un documento.

Los cuatro formatos de presentación son: **CF \_ DSPBITMAP,** **CF \_ DSPMETAFILEPICT,** **CF \_ DSPTEXT** y **CF \_ DSPENHMETAFILE**. Estos formatos de presentación se representan de la misma manera que los formatos estándar, que son: **CF \_ BITMAP**, **CF \_ TEXT**, **CF \_ METAFILEPICT** y **CF \_ ENHMETAFILE**.

### <a name="owner-display-format"></a>Formato de presentación del propietario

Para un propietario del Portapapeles que no usa ninguno de los formatos comunes del Portapapeles estándar, una alternativa a proporcionar un formato de presentación es usar el formato del Portapapeles owner-display **(CF \_ OWNERDISPLAY).**

Mediante el formato de presentación del propietario, un propietario del Portapapeles puede evitar la sobrecarga de representar los datos en un formato adicional al tomar el control directo sobre el dibujo de la ventana del visor del Portapapeles. La ventana del visor del Portapapeles envía mensajes al propietario del Portapapeles cada vez que se debe volver a dibujar una parte de la ventana o cuando se desplaza o cambia el tamaño de la ventana.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formatos estándar del Portapapeles](standard-clipboard-formats.md)
</dt> </dl>

 

 