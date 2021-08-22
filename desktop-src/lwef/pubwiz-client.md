---
title: Client-Side diseño
description: El script de las páginas HTML del lado servidor se comunica con el cliente del Asistente para ordenación de impresión en línea en el que se hospeda. Esta comunicación se realiza a través de métodos y propiedades a los que tiene acceso el objeto window.external.
ms.assetid: fa76ccee-0b94-41b5-8cc8-eb7e1818dbed
keywords:
- asistentes para publicación, diseño del lado cliente
- window.external, asistentes para publicación
- asistentes para publicación,window.external
- asistentes para publicación, consideraciones de diseño
- asistentes para publicación, Asistente para pedidos de impresión en línea
- Asistente para pedidos de impresión en línea, diseño del lado cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c40aafc7a08820125df222c1c6d911b0d2b4d0a1fb625b7c62fc6d4be8bebd7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665085"
---
# <a name="client-side-design"></a>Client-Side diseño

El script de las páginas HTML del lado servidor se comunica con el cliente del Asistente para ordenación de impresión en línea en el que se hospeda. Esta comunicación se realiza a través de métodos y propiedades a los que tiene acceso el **objeto window.external.**

En este documento se tratan los temas siguientes.

-   [Métodos y propiedades](#methods-and-properties)
-   [Consideraciones de diseño](#design-considerations)
-   [Temas relacionados](#related-topics)

## <a name="methods-and-properties"></a>Métodos y propiedades

Los siguientes métodos y propiedades están disponibles a través del **objeto window.external.**

-   [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback)
-   [**FinalNext**](/windows/desktop/shell/iwebwizardhost-finalnext)
-   [**Cancelar**](/windows/desktop/shell/iwebwizardhost-cancel)
-   [**PassportAuthenticate**](/windows/desktop/shell/inewwdevents-passportauthenticate)
-   [**SetHeaderText**](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [**SetWizardButtons**](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))
-   [**Propiedad**](/windows/desktop/shell/iwebwizardhost-property)

El script de la página del lado servidor llama a estos métodos para notificar al cliente de eventos durante el procedimiento de publicación. Echemos un vistazo a [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) como ejemplo. Cuando el asistente muestra la primera página HTML del lado servidor, lo hace con conocimiento de los identificadores de las páginas del asistente anteriores y adicionales a las páginas HTML hospedadas. En este punto del ejemplo, el usuario, sentado en esa primera página HTML, hace clic en el **botón** Atrás. El asistente envía una notificación de este evento al servidor. Al recibir este mensaje, el script del lado servidor hace referencia a su controlador **OnBack** para este evento, que, como esta es la primera página HTML, llama al **método FinalBack.** Esto hace que el asistente vaya a la página del asistente que se muestra antes de entrar en la interfaz de usuario del lado servidor.

Para obtener una explicación completa de estos métodos y propiedades, consulte la documentación de los objetos [**WebWizardHost**](/windows/desktop/shell/webwizardhost) y [**NewWDEvents.**](/windows/desktop/shell/newwdevents)

## <a name="design-considerations"></a>Consideraciones de diseño

El código HTML que crea cada página del lado servidor se muestra normalmente en el panel del asistente. Al diseñar estas páginas, tenga en cuenta que no se puede cambiar el tamaño de una ventana del asistente. Por lo tanto, las páginas se deben construir y cambiar de tamaño para que las barras de desplazamiento se eviten siempre que sea posible para proporcionar al usuario una navegación fluida a través del asistente.

Cada página HTML también debe proporcionar un controlador para los eventos **OnBack**, **OnNext** y **OnCancel.** El **controlador OnNext** también controlará el **evento Finish.** Una página que no implementa una función **OnBack** se considera no válida y hará que se muestre una página de error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**WebWizardHost**](/windows/desktop/shell/webwizardhost)
</dt> <dt>

[**NewWDEvents**](/windows/desktop/shell/newwdevents)
</dt> <dt>

[Diseño del lado servidor](pubwiz-server.md)
</dt> </dl>

 

 