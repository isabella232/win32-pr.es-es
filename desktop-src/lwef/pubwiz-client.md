---
title: Diseño de Client-Side
description: El script en páginas HTML del lado servidor se comunica con el cliente del Asistente para orden de impresión en línea en el que se hospeda. Esta comunicación se logra a través de métodos y propiedades a los que tiene acceso el objeto Window. external.
ms.assetid: fa76ccee-0b94-41b5-8cc8-eb7e1818dbed
keywords:
- asistentes para publicación, diseño del lado cliente
- Window. external, asistentes para publicación
- asistentes para publicación, Window. external
- asistentes para la publicación, consideraciones de diseño
- asistentes para publicación, Asistente para impresión en línea
- Asistente para orden de impresión en línea, diseño del lado cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f794ee5f576077e0523f9a21101205ec789d4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995231"
---
# <a name="client-side-design"></a>Diseño de Client-Side

El script en páginas HTML del lado servidor se comunica con el cliente del Asistente para orden de impresión en línea en el que se hospeda. Esta comunicación se logra a través de métodos y propiedades a los que tiene acceso el objeto **window. external** .

Los temas siguientes se tratan en este documento.

-   [Métodos y propiedades](#methods-and-properties)
-   [Consideraciones de diseño](#design-considerations)
-   [Temas relacionados](#related-topics)

## <a name="methods-and-properties"></a>Métodos y propiedades

Los siguientes métodos y propiedades están disponibles a través del objeto **window. external** .

-   [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback)
-   [**FinalNext**](/windows/desktop/shell/iwebwizardhost-finalnext)
-   [**Cancelar**](/windows/desktop/shell/iwebwizardhost-cancel)
-   [**PassportAuthenticate**](/windows/desktop/shell/inewwdevents-passportauthenticate)
-   [**SetHeaderText**](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [**SetWizardButtons**](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))
-   [**Propiedad**](/windows/desktop/shell/iwebwizardhost-property)

El script de la página del servidor llama a estos métodos para notificar al cliente los eventos durante el procedimiento de publicación. Echemos un vistazo a [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) como ejemplo. Cuando el asistente muestra la primera página HTML del servidor, lo hace con el conocimiento de los identificadores de las páginas del asistente anteriores y después de las páginas HTML hospedadas. En este punto del ejemplo, el usuario, sentado en la primera página HTML, hace clic en el botón **atrás** . El asistente envía una notificación de este evento al servidor. Al recibir este mensaje, el script de servidor hace referencia a su controlador de **retroceso** para este evento, que, como es la primera página HTML, llama al método **FinalBack** . Esto hace que el asistente navegue hasta la página del asistente que se muestra antes de escribir la interfaz de usuario del lado servidor.

Para obtener una descripción completa de estos métodos y propiedades, vea la documentación de los objetos [**WebWizardHost**](/windows/desktop/shell/webwizardhost) y [**NewWDEvents**](/windows/desktop/shell/newwdevents) .

## <a name="design-considerations"></a>Consideraciones de diseño

El HTML que conforman cada página del servidor se muestra normalmente en el panel del asistente. Al diseñar estas páginas, tenga en cuenta que no se puede cambiar el tamaño de una ventana del asistente. Por tanto, las páginas se deben construir y ajustar para que las barras de desplazamiento se eviten siempre que sea posible para proporcionar al usuario una navegación fluida a través del asistente.

Cada página HTML también debe proporcionar un controlador para los eventos **alback**, **alnext** y **OnCancel** . El controlador en el **siguiente** control también controlará el evento de **finalización** . Una página que no implementa una función **alback** se considera no válida y provocará que se muestre una página de error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**WebWizardHost**](/windows/desktop/shell/webwizardhost)
</dt> <dt>

[**NewWDEvents**](/windows/desktop/shell/newwdevents)
</dt> <dt>

[Diseño del lado servidor](pubwiz-server.md)
</dt> </dl>

 

 