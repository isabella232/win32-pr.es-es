---
title: Operaciones del Portapapeles
description: Una ventana debe usar el Portapapeles al cortar, copiar o pegar datos. Una ventana coloca datos en el Portapapeles para las operaciones de cortar y copiar y recupera datos del Portapapeles para las operaciones de pegado.
ms.assetid: 27f9142c-3154-4de5-aea6-3c53f7e940ec
keywords:
- Windows Interfaz de usuario,clipboard
- clipboard,windows
- portapapeles, cortar datos
- clipboard,copying data
- clipboard, pegar datos
- clipboard,owner window
- portapapeles, representación retrasada
- clipboard,memory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a0dfe82f6130f0435521ac4e17cf8e8b7162115074f7b3ff716187730f8bb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545439"
---
# <a name="clipboard-operations"></a>Operaciones del Portapapeles

Una ventana debe usar el Portapapeles al cortar, copiar o pegar datos. Una ventana coloca datos en el Portapapeles para las operaciones de cortar y copiar y recupera datos del Portapapeles para las operaciones de pegado. En las secciones siguientes se describen estas operaciones y problemas relacionados.

Para colocar o recuperar datos del Portapapeles, una ventana debe abrir primero el Portapapeles mediante la [**función OpenClipboard.**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) Solo una ventana puede tener el Portapapeles abierto a la vez. Para averiguar qué ventana tiene abierto el Portapapeles, llame a [**la función GetOpenClipboardWindow.**](/windows/desktop/api/Winuser/nf-winuser-getopenclipboardwindow) Cuando haya terminado, la ventana debe cerrar el Portapapeles mediante una llamada a [**la función CloseClipboard.**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard)

En esta sección se tratan los temas siguientes.

-   [Operaciones de cortar y copiar](#cut-and-copy-operations)
-   [Operaciones de pegado](#paste-operations)
-   [Propiedad del Portapapeles](#clipboard-ownership)
-   [Representación retrasada](#delayed-rendering)
-   [Memoria y portapapeles](#memory-and-the-clipboard)

## <a name="cut-and-copy-operations"></a>Operaciones de cortar y copiar

Para colocar información en el Portapapeles, una ventana borra primero cualquier contenido anterior del Portapapeles mediante la [**función EmptyClipboard.**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) Esta función envía el [**mensaje \_ WM DESTROYCLIPBOARD**](wm-destroyclipboard.md) al propietario del Portapapeles anterior, libera los recursos asociados con los datos del Portapapeles y asigna la propiedad del Portapapeles a la ventana que tiene abierto el Portapapeles. Para averiguar qué ventana posee el Portapapeles, llame a la [**función GetClipboardOwner.**](/windows/win32/api/winuser/nf-winuser-getclipboardowner)

Después de vaciar el Portapapeles, la ventana coloca los datos en el Portapapeles en tantos formatos de Portapapeles como sea posible, ordenados del formato más descriptivo al menos descriptivo. Para cada formato, la ventana llama a la [**función SetClipboardData,**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) especificando el identificador de formato y un identificador de memoria global. El identificador de memoria puede ser NULL, lo que indica que la ventana representa los datos a petición. Para obtener más información, vea [Representación retrasada.](#delayed-rendering)

## <a name="paste-operations"></a>Operaciones de pegado

Para recuperar la información de pegado del Portapapeles, una ventana determina primero el formato del Portapapeles que se debe recuperar. Normalmente, una ventana enumera los formatos del Portapapeles disponibles mediante la función [**EnumClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) y usa el primer formato que reconoce. Este método selecciona el mejor formato disponible según la prioridad establecida cuando los datos se colocaron en el Portapapeles.

Como alternativa, una ventana puede usar la [**función GetPriorityClipboardFormat.**](/windows/desktop/api/Winuser/nf-winuser-getpriorityclipboardformat) Esta función identifica el mejor formato de Portapapeles disponible según una prioridad especificada. Una ventana que reconoce solo un formato del Portapapeles puede determinar simplemente si ese formato está disponible mediante la [**función IsClipboardFormatAvailable.**](/windows/desktop/api/Winuser/nf-winuser-isclipboardformatavailable)

Después de determinar el formato del Portapapeles que se usará, una ventana llama a [**la función GetClipboardData.**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) Esta función devuelve el identificador a un objeto de memoria global que contiene datos en el formato especificado. Una ventana puede bloquear brevemente el objeto de memoria para examinar o copiar los datos. Sin embargo, una ventana no debe liberar el objeto ni dejarlo bloqueado durante un largo período de tiempo.

## <a name="clipboard-ownership"></a>Propiedad del Portapapeles

El *propietario del Portapapeles* es la ventana asociada a la información del Portapapeles. Una ventana se convierte en el propietario del Portapapeles cuando coloca datos en el Portapapeles, específicamente, cuando llama a la [**función EmptyClipboard.**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) La ventana sigue siendo el propietario del Portapapeles hasta que se cierra o otra ventana vacía el Portapapeles.

Cuando se vacía el Portapapeles, el propietario del Portapapeles recibe un [**mensaje \_ WM DESTROYCLIPBOARD.**](wm-destroyclipboard.md) Estos son algunos de los motivos por los que una ventana podría procesar este mensaje:

-   La ventana retrasó la representación de uno o varios formatos del Portapapeles. En respuesta al mensaje [**\_ WM DESTROYCLIPBOARD,**](wm-destroyclipboard.md) la ventana podría liberar los recursos que había asignado para representar los datos a petición. Para obtener más información sobre la representación de datos, vea [Representación retrasada.](#delayed-rendering)
-   La ventana coloca los datos en el Portapapeles en un formato de Portapapeles privado. El sistema no libera los datos de los formatos privados del Portapapeles cuando se vacía el Portapapeles. Por lo tanto, el propietario del Portapapeles debe liberar los datos al recibir el [**mensaje \_ WM DESTROYCLIPBOARD.**](wm-destroyclipboard.md) Para obtener más información sobre los formatos privados del Portapapeles, vea [Formatos del Portapapeles.](clipboard-formats.md)
-   La ventana coloca los datos en el Portapapeles con el formato del Portapapeles **\_ CF OWNERDISPLAY.** En respuesta al mensaje [**\_ WM DESTROYCLIPBOARD,**](wm-destroyclipboard.md) la ventana podría liberar los recursos que había usado para mostrar información en la ventana del visor del Portapapeles. Para obtener más información sobre este formato alternativo, vea [Formato de presentación del propietario.](about-the-clipboard.md)

## <a name="delayed-rendering"></a>Representación retrasada

Al colocar un formato de Portapapeles en el Portapapeles, una ventana puede retrasar la representación de los datos en ese formato hasta que se necesiten los datos. Para ello, una aplicación puede especificar **NULL para** el *parámetro hData* de la [**función SetClipboardData.**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) Esto resulta útil si la aplicación admite varios formatos del Portapapeles, algunos o todos, que tardan mucho tiempo en representarse. Al pasar un **identificador NULL,** una ventana representa formatos complejos del Portapapeles solo cuando y si son necesarios.

Si una ventana retrasa la representación de un formato del Portapapeles, debe estar preparada para representar el formato a petición, siempre y cuando sea el propietario del Portapapeles. El sistema envía al propietario del Portapapeles un mensaje [**\_ DE WM RENDERFORMAT**](wm-renderformat.md) cuando se recibe una solicitud para un formato específico que no se ha representado. Al recibir este mensaje, la ventana debe llamar a la función [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) para colocar un identificador de memoria global en el Portapapeles en el formato solicitado.

Una aplicación no debe abrir el Portapapeles antes de llamar a [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) en respuesta al [**mensaje \_ RENDERFORMAT de WM.**](wm-renderformat.md) No es necesario abrir el Portapapeles y se producirá un error en cualquier intento de hacerlo porque la aplicación que solicitó que se representara el formato mantiene abierto el Portapapeles.

Si el propietario del Portapapeles está a punto de destruirse y ha retrasado la representación de algunos o todos los formatos del Portapapeles, recibe el mensaje [**\_ RENDERALLFORMATS**](wm-renderallformats.md) de WM. Al recibir este mensaje, la ventana debe abrir el Portapapeles, comprobar que sigue siendo el propietario del Portapapeles con la función [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) y, a continuación, colocar identificadores de memoria válidos en el Portapapeles para todos los formatos del Portapapeles que proporciona. Esto garantiza que estos formatos permanecen disponibles después de destruir el propietario del Portapapeles.

A diferencia [**de WM \_ RENDERFORMAT,**](wm-renderformat.md)una aplicación que responde a [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) debe abrir el Portapapeles antes de llamar a [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) para colocar cualquier identificador de memoria global en el Portapapeles.

Los formatos del Portapapeles que no se representan en respuesta al mensaje [**\_ RENDERALLFORMATS**](wm-renderallformats.md) de WM dejan de estar disponibles para otras aplicaciones y las funciones del Portapapeles ya no las enumeran.

## <a name="memory-and-the-clipboard"></a>Memoria y portapapeles

Un objeto de memoria que se va a colocar en el Portapapeles debe asignarse mediante la [**función GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) con la **marca \_ GMEM MOVEABLE.**

Después de colocar un objeto de memoria en el Portapapeles, la propiedad de ese identificador de memoria se transfiere al sistema. Cuando se vacía el Portapapeles y el objeto de memoria tiene uno de los siguientes formatos del Portapapeles, el sistema libera el objeto de memoria mediante una llamada a la función especificada:



| Función para liberar objeto                             | Formato del Portapapeles                                                                                                                                               |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile)<br/> | **CF \_ DSPENHMETAFILE**<br/> **CF \_ DSPMETAFILEPICT**<br/> **CF \_ ENHMETAFILE**<br/> **CF \_ METAFILEPICT**<br/>                            |
| [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)<br/>     | **MAPA DE BITS DE CF \_**<br/> **CF \_ DSPBITMAP**<br/> **PALETA DE CF \_**<br/>                                                                              |
| [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree)<br/>        | **CF \_ DIB**<br/> **CF \_ DIBV5**<br/> **CF \_ DSPTEXT**<br/> **CF \_ OEMTEXT**<br/> **CF \_ TEXT**<br/> **CF \_ UNICODETEXT**<br/>   |
| ninguno<br/>                                     | **CF \_ OWNERDISPLAY**<br/> Cuando el Portapapeles se vacía de un objeto **\_ CF OWNERDISPLAY,** la propia aplicación debe liberar el objeto de memoria.<br/> |



 

 

