---
title: Presentación
description: La presentación es el último paso del proceso de UPnP.
ms.assetid: e8d20ae6-2dd8-4de2-b07b-6cf4e725735e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195399316882de71c148f2369dd2978c4cfbd728
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903381"
---
# <a name="presentation"></a>Presentación

La presentación es el último paso del proceso de UPnP. Si un dispositivo tiene una dirección URL para la presentación, un punto de control puede recuperar una página de esta dirección URL y cargar la página en un explorador. En función de las capacidades de la página de presentación y del dispositivo, el punto de control puede controlar el dispositivo y ver el estado del dispositivo.

La ruta de acceso del recurso, que se pasa a [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) durante el registro, es donde se encuentran todos los archivos relevantes para la presentación del dispositivo. Los desarrolladores de dispositivos pueden proporcionar páginas independientes para cada dispositivo incrustado. La dirección URL de la presentación en la plantilla Descripción del dispositivo puede ser una dirección URL absoluta o relativa. En el caso de las direcciones URL relativas, que son relativas a la ruta de acceso del recurso, la plantilla de Descripción del dispositivo debe contener un nombre de archivo. **IUPnPRegistrar** lo convierte en una dirección URL con la ubicación real. En el caso de las direcciones URL absolutas, la ubicación no se modifica.

Para admitir los scripts del lado cliente dentro de una página de presentación, normalmente se anexa información adicional a la dirección URL en forma de "cadena de consulta". La información adicional que se anexa es la dirección URL del documento de Descripción del dispositivo y el UDN del dispositivo o del dispositivo incrustado. La dirección URL de Descripción del dispositivo se puede usar para cargar un documento de descripción en el script y, a continuación, controlar el dispositivo a través de sus servicios. El UDN se usa para seleccionar un dispositivo incrustado desde el dispositivo raíz.

El formato de la dirección URL de presentación modificada es: la dirección URL de presentación real, un signo de interrogación ("?"), la dirección URL de la descripción del dispositivo, un signo más ("+"), el dispositivo UDN. El signo de interrogación denota el inicio de la cadena de consulta.

Si la dirección URL de la presentación en la plantilla de Descripción del dispositivo era una dirección URL absoluta y ya contenía un signo de interrogación ("?"), la información adicional no se agrega a la dirección URL de la presentación.



| Descripción                        | URL                                                                                                                                               |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| En la plantilla de Descripción del dispositivo | **presentationURL** MyDevice.html **/presentationURL**                                                                                              |
| Generado por el host del dispositivo       | **presentationURL** https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394 ... + UDN **/presentationURL** |



 

Es posible que un script del lado cliente tenga que extraer la dirección URL de la descripción del dispositivo de la dirección URL de presentación para cargar el objeto [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) . Para ello, se toma la cadena de consulta y se termina en el signo más ("+").


```VB
Dim QueryString
QueryString = window.location.search
Dim DescURLString
DescURLString = Trim(Mid(QueryString,2,Instr(QueryString,"+")-2))& vbCrLf

    Dim LightDesc
    Set LightDesc = CreateObject("UPnP.DescriptionDocument.1")
    LightDesc.Load(DescURLString)
```



En el caso de una página de presentación de un dispositivo incrustado, se requiere algún trabajo adicional. Después de cargar el [**UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument), el script debe obtener la colección de dispositivos incrustados y, a continuación, seleccionar el dispositivo que coincida con el valor de UDN en la cadena de consulta. El siguiente script muestra cómo seleccionar el dispositivo incrustado para la página de presentación actual. Supone que LightDesc ya está cargado.


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



 

 




