---
description: Protocolos admitidos
ms.assetid: 3c026426-c2b7-4909-9524-9cc0bd45347e
title: Protocolos admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b086b48b73c0412968c00091e6353d134006f45fa9c8b8f229ea3f9e695bf99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238132"
---
# <a name="supported-protocols"></a>Protocolos admitidos

Media Foundation admite los siguientes protocolos:

-   Protocolo de streaming en tiempo real (RTSP)

    RTSP se usa principalmente para el streaming de contenido multimedia. Puede usar UDP o TCP como protocolos de transporte. UDP es el más eficaz para la entrega de contenido porque la sobrecarga de ancho de banda es menor que con los protocolos basados en TCP. Aunque el protocolo TCP garantiza la entrega confiable de paquetes, TCP no es adecuado para los flujos multimedia digitales, donde el uso eficaz del ancho de banda es más importante que los paquetes ocasionales perdidos.

-   Protocolo de transferencia de hipertexto (HTTP)

    HTTP usa TCP y lo usan los servidores web. El esquema "httpd://" indica que el origen se puede descargar desde un servidor web. HTTP también se usa en el caso de los firewalls, que normalmente están configurados para aceptar solicitudes HTTP y normalmente rechazar otros protocolos de streaming.

La aplicación puede obtener los protocolos admitidos por Media Foundation mediante la interfaz [**IMFNetSchemeHandlerConfig.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) Para ello, la aplicación debe recuperar primero el número de protocolos mediante una llamada a [**IMFNetSchemeHandlerConfig::GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) y, a continuación, obtener el tipo de protocolo basado en el índice mediante una llamada a [**IMFNetSchemeHandlerConfig::GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype). Este método devuelve uno de los valores definidos en la enumeración [**MFNETSOURCE \_ PROTOCOL \_ TYPE.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type)

La aplicación también puede obtener los esquemas admitidos por el solucionador de origen llamando a la [**función MFGetSupportedSchemes.**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes)

## <a name="protocol-rollover"></a>Suversión de protocolo

Cuando una aplicación especifica "mms://" como esquema de dirección URL, el solucionador de origen realiza una operación *de suversión de* protocolo. En este proceso, la resolución de origen determina el mejor protocolo para el origen de red que se usará para obtener el contenido. Normalmente, para el transporte de medios, RTSP con UDP (RTSPU) es más eficaz que HTTP. Sin embargo, si el contenido se hospeda en un servidor web, HTTP es una mejor opción.

La suversión de protocolo también puede producirse cuando se produce un error al intentar usar el protocolo especificado en el esquema de dirección URL. Por ejemplo, un protocolo puede producir un error cuando un firewall bloquea los paquetes UDP. En este caso, la resolución de origen cambia a HTTP.

La suversión de protocolo no se aplica si el esquema de dirección URL contiene un protocolo específico, como "rtspu://". Además, la suversión no se realiza si se produce un error en la autenticación o el servidor ha alcanzado un límite de conexiones de cliente. Se recomienda que las aplicaciones especifiquen el esquema "mms://" y permitan que el solucionador de origen seleccione el mejor protocolo para el escenario.

En la tabla siguiente se muestra el orden de suversión.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Esquemas permitidos</th>
<th>Orden de suversión de protocolo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>mms:// o rtsp://</td>
<td>Caché rápida habilitada:<br/>
<ol>
<li>RTSP con TCP (RTSPT)<br/></li>
<li>RTSP con UDP (RTSPU)<br/></li>
<li>HTTP Streaming<br/></li>
<li>Descarga HTTP (HTTPD)<br/></li>
</ol>
Caché rápida deshabilitada:<br/>
<ol>
<li>Rtspu<br/></li>
<li>RTSPT<br/></li>
<li>HTTP Streaming<br/></li>
<li>Descarga de HTTP<br/></li>
</ol></td>
</tr>
<tr class="even">
<td>rtspu://</td>
<td>Rtspu</td>
</tr>
<tr class="odd">
<td>rtspt://</td>
<td>RTSPT</td>
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



 

## <a name="retrieving-the-current-protocol"></a>Recuperar el protocolo actual

Después de una operación de suversión de protocolo, el origen de red podría usar un protocolo distinto del especificado por la aplicación en el esquema de dirección URL. El resultado de la sustitución del protocolo está disponible para la aplicación después de que el origen de red establezca la conexión con el servidor multimedia.

Para obtener el protocolo y el transporte que se usan para obtener el contenido, la aplicación puede recuperar los valores de propiedad para la propiedad [MFNETSOURCE \_ PROTOCOL](mfnetsource-protocol-property.md) y la propiedad [MFNETSOURCE \_ TRANSPORT](mfnetsource-transport-property.md) de un objeto **IPropertyStore** del origen de red.

El código siguiente muestra cómo obtener estos valores.


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



En el código de ejemplo anterior, **IPropertyStore::GetValue** recupera el valor MFNETSOURCE PROTOCOL, que es miembro de la enumeración \_ [**MFNETSOURCE \_ PROTOCOL \_ TYPE.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) Para MFNETSOURCE TRANSPORT, el valor es miembro de la \_ enumeración [**MFNETSOURCE \_ TRANSPORT \_ TYPE.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type)

Como alternativa, la aplicación puede obtener los mismos valores mediante el servicio MFNETSOURCE \_ STATISTICS \_ SERVICE. Para usar este servicio, la aplicación puede llamar a [**la función MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obtener el almacén de propiedades del origen de red. Este almacén de propiedades contiene estadísticas de red en [la propiedad MFNETSOURCE \_ STATISTICS.](mfnetsource-statistics-property.md) Los valores de protocolo y transporte se pueden recuperar especificando MFNETSOURCE PROTOCOL ID y MFNETSOURCE TRANSPORT ID, definidos en la enumeración \_ \_ \_ \_ [**MFNETSOURCE \_ STATISTICS \_ IDS.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) El código siguiente muestra cómo obtener los valores de protocolo y transporte mediante el servicio MFNETSOURCE \_ STATISTICS \_ SERVICE.


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

La aplicación puede configurar el origen de red para que determinados protocolos se omitieron durante el proceso de suversión. Para ello, las propiedades de origen de red se usan para deshabilitar protocolos específicos. En la tabla siguiente se muestran las propiedades y los protocolos que controlan.



| Propiedad                                                                    | Descripción                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [MFNETSOURCE \_ HABILITAR \_ HTTP](mfnetsource-enable-http-property.md)           | Habilita o deshabilita HTTP y HTTPD.         |
| [MFNETSOURCE \_ ENABLE \_ RTSP](mfnetsource-enable-rtsp-property.md)           | Habilita o deshabilita RTSPU y RTSPT.        |
| [MFNETSOURCE \_ ENABLE \_ TCP](mfnetsource-enable-tcp-property.md)             | Habilita o deshabilita RTSPT.                  |
| [MFNETSOURCE \_ ENABLE \_ UDP](mfnetsource-enable-udp-property.md)             | Habilita o deshabilita RTSPU.                  |
| [MFNETSOURCE \_ HABILITAR DESCARGA \_](mfnetsource-enable-download-property.md)   | Habilita o deshabilita HTTPD.                  |
| [MFNETSOURCE \_ ENABLE \_ STREAMING](mfnetsource-enable-streaming-property.md) | Habilita o deshabilita RTSPU, RTSPT y HTTP. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




