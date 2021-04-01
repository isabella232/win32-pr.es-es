---
description: Protocolos admitidos
ms.assetid: 3c026426-c2b7-4909-9524-9cc0bd45347e
title: Protocolos admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e618f47a1ffc4a81c36e48407b93da54d7d532f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811528"
---
# <a name="supported-protocols"></a>Protocolos admitidos

Media Foundation admite los siguientes protocolos:

-   Protocolo de streaming en tiempo real (RTSP)

    RTSP se usa principalmente para el streaming de contenido multimedia. Puede usar UDP o TCP como protocolos de transporte. UDP es la más eficaz para la entrega de contenido porque la sobrecarga de ancho de banda es menor que con los protocolos basados en TCP. A pesar de que el protocolo TCP garantiza la entrega de paquetes confiable, TCP no es adecuado para flujos multimedia digitales, donde el uso eficaz del ancho de banda es más importante que los paquetes perdidos ocasionales.

-   Protocolo de transferencia de hipertexto (HTTP)

    HTTP usa TCP y lo usan los servidores Web. El esquema "httpd://" indica que el origen se descarga desde un servidor Web. HTTP también se usa en el caso de los firewalls, que normalmente se configuran para aceptar solicitudes HTTP y suelen rechazar otros protocolos de streaming.

La aplicación puede obtener los protocolos admitidos por Media Foundation mediante la interfaz [**IMFNetSchemeHandlerConfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) . Para ello, la aplicación debe recuperar primero el número de protocolos, llamando a [**IMFNetSchemeHandlerConfig:: GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) y, a continuación, obtener el tipo de protocolo basándose en el índice llamando a [**IMFNetSchemeHandlerConfig:: GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype). Este método devuelve uno de los valores definidos en la enumeración del [**\_ \_ tipo de protocolo MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .

La aplicación también puede obtener los esquemas admitidos por la resolución de origen mediante una llamada a la función [**MFGetSupportedSchemes**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) .

## <a name="protocol-rollover"></a>Sustitución de protocolo

Cuando una aplicación especifica "mms://" como el esquema de la dirección URL, la resolución de origen realiza una operación de *sustitución del protocolo* . En este proceso, la resolución de origen determina el mejor protocolo para que el origen de red lo use para obtener el contenido. Normalmente, para el streaming multimedia, RTSP con UDP (RTSPU) es más eficaz que HTTP. Sin embargo, si el contenido está hospedado en un servidor Web, HTTP es una mejor opción.

La sustitución del protocolo también puede producirse cuando se produce un error al intentar usar el protocolo especificado en el esquema de la dirección URL. Por ejemplo, se puede producir un error en un protocolo cuando un Firewall bloquea paquetes UDP. En este caso, la resolución de origen cambia a HTTP.

La sustitución de protocolos no se aplica si el esquema de direcciones URL contiene un protocolo específico, como "rtspu://". Además, la sustitución no se realiza si se produce un error de autenticación o el servidor ha alcanzado un límite de conexiones de cliente. Se recomienda que las aplicaciones especifiquen el esquema "mms://" y que la resolución de origen Seleccione el mejor protocolo para el escenario.

En la tabla siguiente se muestra el orden de sustitución incremental.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Esquemas permitidos</th>
<th>Orden de sustitución de protocolos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>mms://o rtsp://</td>
<td>Caché rápida habilitada:<br/>
<ol>
<li>RTSP con TCP (RTSPt)<br/></li>
<li>RTSP con UDP (RTSPU)<br/></li>
<li>Transmisión por secuencias HTTP<br/></li>
<li>Descarga HTTP (HTTPD)<br/></li>
</ol>
Caché rápida deshabilitada:<br/>
<ol>
<li>RTSPU<br/></li>
<li>RTSPt<br/></li>
<li>Transmisión por secuencias HTTP<br/></li>
<li>Descarga HTTP<br/></li>
</ol></td>
</tr>
<tr class="even">
<td>rtspu://</td>
<td>RTSPU</td>
</tr>
<tr class="odd">
<td>rtspt://</td>
<td>RTSPt</td>
</tr>
<tr class="even">
<td>https://</td>
<td><ol>
<li>HTTP<br/></li>
<li>HTTPD<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>httpd://</td>
<td>HTTPD</td>
</tr>
</tbody>
</table>



 

## <a name="retrieving-the-current-protocol"></a>Recuperación del protocolo actual

Después de una operación de sustitución de protocolo, el origen de red podría usar un protocolo distinto del especificado por la aplicación en el esquema de la dirección URL. El resultado de la sustitución del protocolo está disponible para la aplicación después de que el origen de red establezca la conexión con el servidor multimedia.

Para obtener el protocolo y el transporte que se usan para obtener el contenido, la aplicación puede recuperar los valores de propiedad de la propiedad de [ \_ Protocolo MFNETSOURCE](mfnetsource-protocol-property.md) y la propiedad de [ \_ transporte MFNETSOURCE](mfnetsource-transport-property.md) de un objeto **IPropertyStore** desde el origen de red.

En el código siguiente se muestra cómo obtener estos valores.


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    PROPVARIANT var;
    PropVariantInit(&var);

// Get the property store from the network source.
// The network source is created by the source resolver. Not shown.
    if (SUCCEEDED(hr))
    {
        hr = pNetworkSource->QueryInterface 
                (__uuidof(IPropertyStore), 
                (void**)&pProp);
    }
    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the MFNETSOURCE_PROTOCOL property value.
        key.fmtid = MFNETSOURCE_PROTOCOL;
        hr = pProp->GetValue (key, &var);

        // Get the MFNETSOURCE_TRANSPORT property value.
        key.fmtid = MFNETSOURCE_TRANSPORT;
        key.pid = 0;
        hr = pProp->GetValue (key, &var);

    }
```



En el código de ejemplo anterior, **IPropertyStore:: GetValue** recupera el \_ valor del protocolo MFNETSOURCE, que es miembro de la enumeración del [**\_ \_ tipo de protocolo MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) . En el caso del \_ transporte MFNETSOURCE, el valor es un miembro de la enumeración de [**\_ \_ tipo de transporte MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) .

Como alternativa, la aplicación puede obtener los mismos valores mediante el servicio MFNETSOURCE \_ Statistics \_ Service. Para usar este servicio, la aplicación puede llamar a la función [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obtener el almacén de propiedades del origen de red. Este almacén de propiedades contiene estadísticas de red en la propiedad [MFNETSOURCE \_ Statistics](mfnetsource-statistics-property.md) . Los valores de protocolo y transporte se pueden recuperar especificando \_ \_ el identificador de protocolo de MFNETSOURCE y \_ \_ el identificador de transporte de MFNETSOURCE, definidos en la enumeración de [**\_ \_ identificadores de MFNETSOURCE Statistics**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) . En el código siguiente se muestra cómo obtener el protocolo y los valores de transporte mediante el \_ servicio MFNETSOURCE Statistics \_ Service.


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    HRESULT hr = S_OK;

    hr = MFGetService(
        pMediaSource, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_IPropertyStore, 
        (void**) & pProp); 

    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the property value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_PROTOCOL_ID;
        hr = pProp->GetValue (key, &var);

        // Get the transport value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_TRANSPORT_ID;
        hr = pProp->GetValue (key, &var);

    }
```



## <a name="enabling-and-disabling-protocols"></a>Habilitar y deshabilitar protocolos

La aplicación puede configurar el origen de red para que se omitan determinados protocolos durante el proceso de sustitución incremental. Para ello, se usan las propiedades de origen de red para deshabilitar determinados protocolos. En la tabla siguiente se muestran las propiedades y los protocolos que controlan.



| Propiedad                                                                    | Descripción                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [MFNETSOURCE \_ habilitar \_ http](mfnetsource-enable-http-property.md)           | Habilita o deshabilita HTTP y HTTPD.         |
| [MFNETSOURCE \_ habilitar \_ RTSP](mfnetsource-enable-rtsp-property.md)           | Habilita o deshabilita RTSPU y RTSPt.        |
| [MFNETSOURCE \_ habilitar \_ TCP](mfnetsource-enable-tcp-property.md)             | Habilita o deshabilita RTSPt.                  |
| [MFNETSOURCE \_ habilitar \_ UDP](mfnetsource-enable-udp-property.md)             | Habilita o deshabilita RTSPU.                  |
| [MFNETSOURCE \_ habilitar \_ descarga](mfnetsource-enable-download-property.md)   | Habilita o deshabilita HTTPD.                  |
| [MFNETSOURCE \_ habilitar \_ streaming](mfnetsource-enable-streaming-property.md) | Habilita o deshabilita RTSPU, RTSPt y HTTP. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




