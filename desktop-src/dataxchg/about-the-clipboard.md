---
title: Acerca del portapapeles
description: En esta sección se describe el portapapeles.
ms.assetid: 14c91730-a668-495b-9ec6-b835234821a5
keywords:
- portapapeles, acerca de
- portapapeles, formatos
- portapapeles, comandos
- portapapeles, Windows
- portapapeles, números de secuencia
- portapapeles, visores
- portapapeles, ventanas del visor
- portapapeles, formatos de presentación
- formato de presentación del portapapeles y propietarios
- Mostrar formatos del portapapeles
- presentación de los formatos del portapapeles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94757a95fb8c40152a0018d04cef64e8efae624
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359296"
---
# <a name="about-the-clipboard"></a>Acerca del portapapeles

El *portapapeles* es un conjunto de funciones y mensajes que permiten a las aplicaciones transferir datos. Dado que todas las aplicaciones tienen acceso al portapapeles, los datos se pueden transferir fácilmente entre aplicaciones o dentro de una aplicación.

El Portapapeles está controlado por el usuario. Una ventana debe transferir datos a o desde el portapapeles solo en respuesta a un comando del usuario. Una ventana no debe usar el portapapeles para transferir datos sin el conocimiento del usuario.

Un objeto de memoria del portapapeles puede estar en cualquier formato de datos, denominado formato del portapapeles. Cada formato se identifica mediante un valor entero sin signo. En el caso de los formatos de Portapapeles estándar (predefinidos), este valor es una constante definida en Winuser. h; en el caso de los formatos de Portapapeles registrados, es el valor devuelto de la función [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) .

Excepto para registrar formatos del portapapeles, las ventanas individuales realizan la mayoría de las operaciones del portapapeles. Normalmente, un procedimiento de ventana transfiere información hacia o desde el portapapeles en respuesta al mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .

En esta sección se trata lo siguiente:

-   [Comandos del portapapeles](#clipboard-commands)
-   [Número de secuencia del portapapeles](#clipboard-sequence-number)
-   [Visores del portapapeles](#clipboard-viewers)
    -   [Ventanas del visor del portapapeles](#clipboard-viewer-windows)
    -   [Formatos de presentación](#display-formats)
    -   [Formato de presentación del propietario](#owner-display-format)
-   [Temas relacionados](#related-topics)

## <a name="clipboard-commands"></a>Comandos del portapapeles

Normalmente, un usuario lleva a cabo operaciones del portapapeles eligiendo comandos en el menú **edición** de una aplicación. A continuación se describe una breve descripción de los comandos estándar del portapapeles.



|            |                                                                                                                                                                                                                   |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Cortar**    | Coloca una copia de la selección actual en el portapapeles y elimina la selección del documento. Se destruye el contenido anterior del portapapeles.                                                          |
| **Copiar**   | Coloca una copia de la selección actual en el portapapeles. El documento permanece inalterado. Se destruye el contenido anterior del portapapeles.                                                                      |
| **Pegar**  | Reemplaza la selección actual por el contenido del portapapeles. No se cambia el contenido del portapapeles.                                                                                                    |
| **Eliminar** | Elimina la selección actual del documento. No se cambia el contenido del portapapeles. Este comando no implica el portapapeles, pero debe aparecer con los comandos del portapapeles en el menú **edición** . |



 

## <a name="clipboard-sequence-number"></a>Número de secuencia del portapapeles

El portapapeles de cada estación de ventana tiene un número de secuencia de Portapapeles asociado. Este número se incrementa cada vez que cambia el contenido del portapapeles. Para obtener el número de secuencia del portapapeles, llame a la función [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) .

## <a name="clipboard-viewers"></a>Visores del portapapeles

Un visor del portapapeles es una ventana que muestra el contenido actual del portapapeles. La ventana Visor del portapapeles es una comodidad para el usuario y no afecta a las funciones de transacción de datos del portapapeles.

Normalmente, una ventana del visor del portapapeles puede mostrar al menos los tres formatos más comunes: **CF \_ Text**, **CF \_ Bitmap** y **CF \_ METAFILEPICT**. Si una ventana no hace que los datos estén disponibles en ninguno de estos tres formatos, debe proporcionar los datos en formato de presentación o usar el formato de presentación del propietario.

Una *cadena del visor del portapapeles* es la vinculación de dos o más entidades, por lo que dependen unas de otras para la operación. Esta interdependencia (cadena) permite que todas las aplicaciones del visor del portapapeles en ejecución reciban los mensajes enviados al portapapeles actual.

Los temas siguientes se describen en esta sección.

-   [Ventanas del visor del portapapeles](#clipboard-viewer-windows)
-   [Formatos de presentación](#display-formats)
-   [Formato de presentación del propietario](#owner-display-format)

### <a name="clipboard-viewer-windows"></a>Ventanas del visor del portapapeles

Una ventana se agrega a la cadena del visor del portapapeles mediante una llamada a la función [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) . El valor devuelto es el identificador de la siguiente ventana de la cadena. Para recuperar el identificador de la primera ventana de la cadena, llame a la función [**GetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-getclipboardviewer) .

Cada ventana del visor del portapapeles debe realizar un seguimiento de la siguiente ventana de la cadena del visor del portapapeles. Cuando cambia el contenido del portapapeles, el sistema envía un mensaje de [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) a la primera ventana de la cadena. Después de actualizar su presentación, cada ventana del visor del portapapeles debe pasar este mensaje a la siguiente ventana de la cadena.

Antes de cerrar, una ventana del visor del portapapeles debe quitarse de la cadena del visor del portapapeles mediante una llamada a la función [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) . Después, el sistema envía un mensaje de [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) a la primera ventana de la cadena.

Para obtener más información sobre el procesamiento de los mensajes de [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) y [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) , vea [crear una ventana del visor del portapapeles](using-the-clipboard.md).

### <a name="display-formats"></a>Formatos de visualización

Un formato de presentación es un formato de Portapapeles que se usa para mostrar información en una ventana del visor del portapapeles. Un propietario del portapapeles que usa un formato de Portapapeles privado o registrado, y ninguno de los formatos estándar más comunes, debe proporcionar los datos en un formato de presentación para verlos en una ventana del visor del portapapeles. Los formatos de presentación están pensados para su visualización únicamente y no deben pegarse en un documento.

Los cuatro formatos de presentación son **: \_ CF DSPBITMAP**, **CF \_ DSPMETAFILEPICT**, **CF \_ DSPTEXT** y **CF \_ DSPENHMETAFILE**. Estos formatos de presentación se representan de la misma manera que los formatos estándar, que son: **CF \_ Bitmap**, **CF \_ Text**, **CF \_ METAFILEPICT** y **CF \_ ENHMETAFILE**.

### <a name="owner-display-format"></a>Formato de presentación del propietario

En el caso de un propietario del portapapeles que no usa ninguno de los formatos estándar comunes del portapapeles, una alternativa a proporcionar un formato de presentación es usar el formato del portapapeles de la presentación del propietario (**CF \_ OWNERDISPLAY**).

Al utilizar el formato de presentación del propietario, el propietario del portapapeles puede evitar la sobrecarga de representar los datos en un formato adicional mediante el control directo sobre cómo pintar la ventana del visor del portapapeles. La ventana Visor del portapapeles envía mensajes al propietario del portapapeles cuando se debe volver a dibujar una parte de la ventana o cuando la ventana se desplaza o se cambia de tamaño.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formatos de Portapapeles estándar](standard-clipboard-formats.md)
</dt> </dl>

 

 