---
title: Diseño de Server-Side
description: Las funciones del lado servidor se comunican con el asistente del cliente a través del objeto Windows. external. El script de servidor proporciona estas funciones para responder a los eventos del asistente y para recuperar información acerca del asistente.
ms.assetid: 7cc8b814-f230-4326-a9df-a491ed35483e
keywords:
- asistentes para publicación, diseño del lado servidor
- Window. external, asistentes para publicación
- asistentes para publicación, Window. external
- asistentes para publicación, funciones de script de navegación
- scripts, asistentes para publicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b3b218bbca297be446016335d90fe717a88bba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995261"
---
# <a name="server-side-design"></a>Diseño de Server-Side

Las funciones del lado servidor se comunican con el asistente del cliente a través del objeto **Windows. external** . El script de servidor proporciona estas funciones para responder a los eventos del asistente y para recuperar información acerca del asistente.

Los temas siguientes se tratan en este documento.

-   [Implementar funciones de script de navegación](#implementing-navigation-script-functions)
    -   [Alback ()](#onback)
    -   [Siguiente ()](#onnext)
    -   [OnCancel ()](#oncancel)
-   [Otros métodos y propiedades](#other-methods-and-properties)
    -   [Métodos](#methods)
    -   [Propiedades](#properties)
-   [Temas relacionados](#related-topics)

## <a name="implementing-navigation-script-functions"></a>Implementar funciones de script de navegación

El script de servidor de cada página HTML responde a los botones de navegación a través de las funciones para **alback**, **Next** y **OnCancel**. Estas funciones deben ser accesibles a través de **IHTMLDocument:: get \_ script** en el cliente y no toman ningún parámetro.

### <a name="onback"></a>Alback ()

-   Responde cuando el usuario hace clic en **atrás** en el asistente.
-   Si la página del servidor actual es la primera página del servidor, llame a **window. external. FinalBack** para indicar al cliente que vaya a la página del lado cliente anterior.
-   Si la página del servidor actual no es la primera página del servidor, vaya a la página del servidor anterior.
-   Esta función se debe implementar para cada página. Cualquier página que no lo haga, se considera no válida y muestra una página de error.

### <a name="onnext"></a>Siguiente ()

-   Responde cuando el usuario hace clic en **siguiente** en el asistente.
-   Si la página del servidor actual es la última página del servidor, llame a **window. external. FinalNext** para indicar al cliente que vaya a la siguiente página del lado cliente o que complete el asistente.
-   Si la página del servidor actual no es la última página del servidor, vaya a la siguiente página del servidor.

### <a name="oncancel"></a>OnCancel ()

-   Responde cuando el usuario hace clic en **Cancelar** en el asistente.
-   La interfaz de usuario debe estar diseñada para que el usuario pueda cancelar en cualquier momento.
-   Una vez que se procesa cualquier procesamiento de la función **OnCancel** , el cliente cierra el asistente.

## <a name="other-methods-and-properties"></a>Otros métodos y propiedades

Se tiene acceso a las funciones implementadas por el cliente a través de **Windows. external**, como son las propiedades. Los servicios disponibles son los siguientes:

### <a name="methods"></a>Métodos

-   [**SetHeaderText**](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [**SetWizardButtons**](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [**PassportAuthenticate**](/windows/desktop/shell/inewwdevents-passportauthenticate)

### <a name="properties"></a>Propiedades

-   [**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))
-   [**Propiedad**](/windows/desktop/shell/iwebwizardhost-property)

En el ejemplo de código siguiente se muestra el código del lado servidor para una página del asistente simple que implementa la página de error del servicio Web.


```
<html>
    <head>
        <script language="JavaScript">
            function window.onload()
            {
                window.external.SetWizardButtons(1, 0, 0);    
                <!-- Back button enabled -->
            }

            function window.onback()
            {
                window.external.FinalBack();
            }
        </script>
    </head>
.
.
.
</html>
                    
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseño del lado cliente](pubwiz-client.md)
</dt> <dt>

[Registrar un servicio](pubwiz-reg.md)
</dt> </dl>

 

 