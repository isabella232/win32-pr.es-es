---
title: Presentación
description: La presentación es el paso final del proceso de UPnP.
ms.assetid: e8d20ae6-2dd8-4de2-b07b-6cf4e725735e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92f8457a881dc0414713e996d230261330c10911f2aea285a2e365ad0d59320
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137198"
---
# <a name="presentation"></a>Presentación

La presentación es el paso final del proceso de UPnP. Si un dispositivo tiene una dirección URL para la presentación, un punto de control puede recuperar una página de esta dirección URL y cargar la página en un explorador. En función de las funcionalidades de la página de presentación y del dispositivo, el punto de control puede controlar el dispositivo y ver el estado del dispositivo.

La ruta de acceso del recurso, que se pasa a [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) durante el registro, es donde se encuentran todos los archivos pertinentes para la presentación del dispositivo. Los desarrolladores de dispositivos pueden proporcionar páginas independientes para cada dispositivo incrustado. La dirección URL de presentación de la plantilla de descripción del dispositivo puede ser una dirección URL absoluta o una dirección URL relativa. Para las direcciones URL relativas, que son relativas a la ruta de acceso del recurso, la plantilla de descripción del dispositivo debe contener un nombre de archivo. **IUPnPRegistrar** convierte esto en una dirección URL con la ubicación real. Para las direcciones URL absolutas, la ubicación no se modifica.

Para admitir scripts del lado cliente dentro de una página de presentación, normalmente se anexa información adicional a la dirección URL en forma de "cadena de consulta". La información adicional que se anexa es la dirección URL al documento de descripción del dispositivo y el UDN del dispositivo o dispositivo incrustado. La dirección URL de descripción del dispositivo se puede usar para cargar un documento de descripción en el script y, a continuación, controlar el dispositivo a través de sus servicios. El UDN se usa para seleccionar un dispositivo incrustado del dispositivo raíz.

El formato de la dirección URL de presentación modificada es: la dirección URL de presentación real, un signo de interrogación ("?"), la dirección URL de descripción del dispositivo, un signo más ("+"), el UDN del dispositivo. El signo de interrogación indica el inicio de la cadena de consulta.

Si la dirección URL de presentación de la plantilla de descripción del dispositivo era una dirección URL absoluta y ya contenía un signo de interrogación ("?"), la información adicional no se agrega a la dirección URL de presentación.



| Descripción                        | URL                                                                                                                                               |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| En la plantilla de descripción del dispositivo | **presentationURL** MyDevice.html **/presentationURL**                                                                                              |
| Generado por el host de dispositivo       | **presentationURL** https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394 ... + UDN **/presentationURL** |



 

Es posible que un script del lado cliente tenga que extraer la dirección URL de descripción del dispositivo de la dirección URL de presentación para cargar el [**objeto IUPnPDescriptionDocument.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) Para ello, se toma la cadena de consulta y se termina en el signo más ("+").


```VB
Dim QueryString
QueryString = window.location.search
Dim DescURLString
DescURLString = Trim(Mid(QueryString,2,Instr(QueryString,"+")-2))& vbCrLf

    Dim LightDesc
    Set LightDesc = CreateObject("UPnP.DescriptionDocument.1")
    LightDesc.Load(DescURLString)
```



En el caso de una página de presentación para un dispositivo incrustado, se requiere algún trabajo adicional. Después de cargar [**UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument), el script debe obtener la colección de dispositivos incrustados y, a continuación, seleccionar el dispositivo que coincida con el UDN en la cadena de consulta. El siguiente script muestra cómo seleccionar el dispositivo incrustado para la página de presentación actual. Se supone que LightDesc ya está cargado.


```VB
Dim LightDevice
Set LightDevice = LightDesc.RootDevice

Dim EmbeddedDevices 
set EmbeddedDevices = LightDevice.Children

Dim DeviceUdnString
DeviceUdnString = Trim(Mid(QueryString,Instr(QueryString,"+")+1,Len(QueryString)))

Dim Item
set Item = EmbeddedDevices.Item(DeviceUdnString)
```



 

 




