---
title: Server-Side diseño
description: Las funciones del lado servidor se comunican con el asistente de cliente a través del objeto windows.external. El script del lado servidor proporciona estas funciones para responder a eventos del asistente y recuperar información sobre el asistente.
ms.assetid: 7cc8b814-f230-4326-a9df-a491ed35483e
keywords:
- asistentes para publicación, diseño del lado servidor
- window.external, asistentes para publicación
- asistentes para publicación,window.external
- asistentes para publicación, funciones de script de navegación
- scripts, asistentes para publicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b3b218bbca297be446016335d90fe717a88bba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168225"
---
# <a name="server-side-design"></a>Server-Side diseño

Las funciones del lado servidor se comunican con el asistente de cliente a través **del objeto windows.external.** El script del lado servidor proporciona estas funciones para responder a eventos del asistente y recuperar información sobre el asistente.

En este documento se tratan los temas siguientes.

-   [Implementar funciones de script de navegación](#implementing-navigation-script-functions)
    -   [OnBack()](#onback)
    -   [OnNext()](#onnext)
    -   [OnCancel()](#oncancel)
-   [Otros métodos y propiedades](#other-methods-and-properties)
    -   [Métodos](#methods)
    -   [Propiedades](#properties)
-   [Temas relacionados](#related-topics)

## <a name="implementing-navigation-script-functions"></a>Implementar funciones de script de navegación

El script del lado servidor de cada página HTML responde a los botones de navegación a través de funciones para **OnBack**, **OnNext** y **OnCancel**. Estas funciones deben ser accesibles a través **de IHTMLDocument::get \_ Script** en el cliente y no tomar ningún parámetro.

### <a name="onback"></a>OnBack()

-   Responde cuando el usuario hace clic en **Atrás** en el asistente.
-   Si la página del lado servidor actual es la primera página del lado servidor, llame a **window.external.FinalBack** para indicar al cliente que vaya a la página del lado cliente anterior.
-   Si la página del lado servidor actual no es la primera página del lado servidor, vaya a la página anterior del lado servidor.
-   Esta función debe implementarse para cada página. Cualquier página que no lo haga se considera no válida y muestra una página de error.

### <a name="onnext"></a>OnNext()

-   Responde cuando el usuario hace clic en **Siguiente** en el asistente.
-   Si la página del lado servidor actual es la última página del lado servidor, llame a **window.external.FinalNext** para indicar al cliente que vaya a la siguiente página del lado cliente o que complete el asistente.
-   Si la página del lado servidor actual no es la última página del lado servidor, vaya a la siguiente página del lado servidor.

### <a name="oncancel"></a>OnCancel()

-   Responde cuando el usuario hace clic en **Cancelar** en el asistente.
-   La interfaz de usuario debe diseñarse para que el usuario pueda cancelarla en cualquier momento.
-   Una vez que se procesa cualquier procesamiento en la **función OnCancel,** el cliente cierra el asistente.

## <a name="other-methods-and-properties"></a>Otros métodos y propiedades

Se accede a las funciones implementadas por el cliente a través **de windows.external,** al igual que las propiedades. Los servicios disponibles son los siguientes:

### <a name="methods"></a>Métodos

-   [**SetHeaderText**](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [**SetWizardButtons**](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [**PassportAuthenticate**](/windows/desktop/shell/inewwdevents-passportauthenticate)

### <a name="properties"></a>Propiedades

-   [**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))
-   [**Propiedad**](/windows/desktop/shell/iwebwizardhost-property)

En el ejemplo de código siguiente se muestra el código del lado servidor para una página del asistente simple que implementa la página de error del servicio web.


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

[Registro de un servicio](pubwiz-reg.md)
</dt> </dl>

 

 