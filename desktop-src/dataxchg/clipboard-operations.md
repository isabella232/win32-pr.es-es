---
title: Operaciones del portapapeles
description: Una ventana debe usar el Portapapeles al cortar, copiar o pegar datos. Una ventana coloca los datos en el portapapeles para las operaciones de cortar y copiar y recupera los datos del portapapeles para las operaciones de pegado.
ms.assetid: 27f9142c-3154-4de5-aea6-3c53f7e940ec
keywords:
- Interfaz de usuario de Windows, Portapapeles
- portapapeles, Windows
- portapapeles, cortar datos
- portapapeles, copiar datos
- portapapeles, pegar datos
- portapapeles, ventana propietaria
- portapapeles, representación diferida
- portapapeles, memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cb2c3451cf562b35b976e137a974e19892acbb3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359333"
---
# <a name="clipboard-operations"></a>Operaciones del portapapeles

Una ventana debe usar el Portapapeles al cortar, copiar o pegar datos. Una ventana coloca los datos en el portapapeles para las operaciones de cortar y copiar y recupera los datos del portapapeles para las operaciones de pegado. En las secciones siguientes se describen estas operaciones y problemas relacionados.

Para colocar datos o recuperar datos del portapapeles, una ventana debe abrir primero el portapapeles mediante la función [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) . Solo una ventana puede tener el portapapeles abierto a la vez. Para averiguar qué ventana tiene abierto el portapapeles, llame a la función [**GetOpenClipboardWindow**](/windows/desktop/api/Winuser/nf-winuser-getopenclipboardwindow) . Cuando haya terminado, la ventana debe cerrar el portapapeles mediante una llamada a la función [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .

Los temas siguientes se describen en esta sección.

-   [Operaciones de cortar y copiar](#cut-and-copy-operations)
-   [Operaciones de pegar](#paste-operations)
-   [Propiedad del portapapeles](#clipboard-ownership)
-   [Representación diferida](#delayed-rendering)
-   [Memoria y Portapapeles](#memory-and-the-clipboard)

## <a name="cut-and-copy-operations"></a>Operaciones de cortar y copiar

Para colocar información en el portapapeles, una ventana borra primero cualquier contenido anterior del portapapeles mediante la función [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) . Esta función envía el mensaje de [**\_ DESTROYCLIPBOARD de WM**](wm-destroyclipboard.md) al propietario anterior del portapapeles, libera los recursos asociados a los datos del portapapeles y asigna la propiedad del portapapeles a la ventana que tiene el portapapeles abierto. Para averiguar qué ventana es propietaria del portapapeles, llame a la función [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) .

Después de vaciar el portapapeles, la ventana coloca los datos en el portapapeles en tantos formatos del portapapeles como sea posible, ordenados desde el formato de Portapapeles más descriptivo hasta el menos descriptivo. Para cada formato, la ventana llama a la función [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) , especificando el identificador de formato y un identificador de memoria global. El identificador de memoria puede ser NULL, lo que indica que la ventana representa los datos a petición. Para obtener más información, consulte [representación diferida](#delayed-rendering).

## <a name="paste-operations"></a>Operaciones de pegar

Para recuperar la información de pegado del portapapeles, una ventana determina primero el formato del portapapeles que se va a recuperar. Normalmente, una ventana enumera los formatos de Portapapeles disponibles mediante la función [**EnumClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) y usa el primer formato que reconozca. Este método selecciona el mejor formato disponible según la prioridad establecida cuando se colocan los datos en el portapapeles.

Como alternativa, una ventana puede utilizar la función [**GetPriorityClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-getpriorityclipboardformat) . Esta función identifica el mejor formato de Portapapeles disponible según una prioridad especificada. Una ventana que solo reconoce un formato de Portapapeles puede determinar simplemente si ese formato está disponible mediante la función [**IsClipboardFormatAvailable**](/windows/desktop/api/Winuser/nf-winuser-isclipboardformatavailable) .

Después de determinar el formato del portapapeles que se va a usar, una ventana llama a la función [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) . Esta función devuelve el identificador de un objeto de memoria global que contiene datos con el formato especificado. Una ventana puede bloquear brevemente el objeto de memoria para examinar o copiar los datos. Sin embargo, una ventana no debe liberar el objeto ni dejarlo bloqueado durante un largo período de tiempo.

## <a name="clipboard-ownership"></a>Propiedad del portapapeles

El *propietario del portapapeles* es la ventana asociada a la información del portapapeles. Una ventana se convierte en el propietario del portapapeles cuando coloca datos en el portapapeles, en concreto, cuando llama a la función [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) . La ventana sigue siendo el propietario del Portapapeles hasta que se cierra o hasta que otra ventana vacía el portapapeles.

Cuando se vacía el portapapeles, el propietario del portapapeles recibe un mensaje de [**\_ DESTROYCLIPBOARD de WM**](wm-destroyclipboard.md) . A continuación se indican algunos de los motivos por los que una ventana podría procesar este mensaje:

-   La representación retrasada de una o varias formatos del portapapeles. En respuesta al mensaje [**de \_ DESTROYCLIPBOARD de WM**](wm-destroyclipboard.md) , es posible que la ventana libere recursos asignados para representar los datos a petición. Para obtener más información sobre la representación de datos, vea [retardo](#delayed-rendering)en la representación.
-   La ventana colocó los datos en el portapapeles en un formato privado del portapapeles. El sistema no libera los datos para los formatos privados del portapapeles cuando se vacía el portapapeles. Por lo tanto, el propietario del portapapeles debe liberar los datos al recibir el mensaje de [**\_ DESTROYCLIPBOARD de WM**](wm-destroyclipboard.md) . Para obtener más información acerca de los formatos privados del portapapeles, vea [formatos del portapapeles](clipboard-formats.md).
-   La ventana colocó datos en el Portapapeles con el formato de Portapapeles de **\_ OWNERDISPLAY de CF** . En respuesta al mensaje [**de \_ DESTROYCLIPBOARD de WM**](wm-destroyclipboard.md) , es posible que la ventana libere los recursos que se utilizaron para mostrar información en la ventana del visor del portapapeles. Para obtener más información acerca de este formato alternativo, consulte [formato de presentación de propietario](about-the-clipboard.md).

## <a name="delayed-rendering"></a>Representación diferida

Al colocar un formato de Portapapeles en el portapapeles, una ventana puede retrasar la representación de los datos en ese formato hasta que se necesiten los datos. Para ello, una aplicación puede especificar **null** para el parámetro *hData* de la función [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) . Esto resulta útil si la aplicación admite varios formatos del portapapeles, algunos o todos ellos requieren mucho tiempo para representarse. Al pasar un identificador **nulo** , una ventana solo presenta formatos complejos del portapapeles cuando y si son necesarios.

Si una ventana retrasa la representación del formato del portapapeles, debe estar preparada para que represente el formato cuando se solicite, siempre y cuando sea el propietario del portapapeles. El sistema envía el propietario del portapapeles a un mensaje de [**WM \_ RENDERFORMAT**](wm-renderformat.md) cuando se recibe una solicitud para un formato específico que no se ha representado. Al recibir este mensaje, la ventana debe llamar a la función [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) para colocar un identificador de memoria global en el portapapeles en el formato solicitado.

Una aplicación no debe abrir el portapapeles antes de llamar a [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) en respuesta al mensaje de [**\_ RENDERFORMAT de WM**](wm-renderformat.md) . No es necesario abrir el portapapeles y cualquier intento de hacerlo producirá un error porque el Portapapeles está siendo abierto actualmente por la aplicación que solicitó el formato que se va a representar.

Si el propietario del Portapapeles está a punto de ser destruido y ha retrasado la representación de algunos o todos los formatos del portapapeles, recibe el mensaje de [**\_ RENDERALLFORMATS de WM**](wm-renderallformats.md) . Al recibir este mensaje, la ventana debe abrir el portapapeles, comprobar que sigue siendo el propietario del Portapapeles con la función [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) y, a continuación, colocar los identificadores de memoria válidos en el portapapeles para todos los formatos del portapapeles que proporciona. Esto garantiza que estos formatos permanecen disponibles una vez destruido el propietario del portapapeles.

A diferencia de [**\_ RENDERFORMAT de WM**](wm-renderformat.md), una aplicación que responde a [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) debe abrir el portapapeles antes de llamar a [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) para colocar los controladores de memoria globales en el portapapeles.

Los formatos del portapapeles que no se representen en respuesta al mensaje de [**\_ RENDERALLFORMATS de WM**](wm-renderallformats.md) dejan de estar disponibles para otras aplicaciones y ya no se enumeran en las funciones del portapapeles.

## <a name="memory-and-the-clipboard"></a>Memoria y Portapapeles

Se debe asignar un objeto de memoria que se va a colocar en el portapapeles mediante la función [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) con la marca **\_ móvil GMEM** .

Después de colocar un objeto de memoria en el portapapeles, la propiedad de ese identificador de memoria se transfiere al sistema. Cuando se vacía el portapapeles y el objeto de memoria tiene uno de los siguientes formatos del portapapeles, el sistema libera el objeto de memoria mediante una llamada a la función especificada:



| Función para liberar el objeto                             | Formato del portapapeles                                                                                                                                               |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile)<br/> | **CF \_ DSPENHMETAFILE**<br/> **CF \_ DSPMETAFILEPICT**<br/> **CF \_ ENHMETAFILE**<br/> **CF \_ METAFILEPICT**<br/>                            |
| [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)<br/>     | **mapa de bits de CF \_**<br/> **CF \_ DSPBITMAP**<br/> **\_paleta CF**<br/>                                                                              |
| [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree)<br/>        | **DIB de CF \_**<br/> **CF \_ DIBV5**<br/> **CF \_ DSPTEXT**<br/> **CF \_ OEMTEXT**<br/> **\_texto CF**<br/> **CF \_ UNICODETEXT**<br/>   |
| ninguno<br/>                                     | **CF \_ OWNERDISPLAY**<br/> Cuando el Portapapeles está vacío de un objeto **\_ OWNERDISPLAY de CF** , la propia aplicación debe liberar el objeto de memoria.<br/> |



 

 

