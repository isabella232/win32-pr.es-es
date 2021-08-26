---
description: Protocolos admitidos
ms.assetid: 3c026426-c2b7-4909-9524-9cc0bd45347e
title: Protocolos admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cc5e47bddec9e00fbb62e853db5a492172da84
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468032"
---
# <a name="supported-protocols"></a>Protocolos admitidos

Media Foundation admite los siguientes protocolos:

-   Protocolo de streaming en tiempo real (RTSP)

    RTSP se usa principalmente para el streaming de contenido multimedia. Puede usar UDP o TCP como protocolos de transporte. UDP es el más eficaz para la entrega de contenido porque la sobrecarga de ancho de banda es menor que con los protocolos basados en TCP. Aunque el protocolo TCP garantiza la entrega confiable de paquetes, TCP no es adecuado para los flujos multimedia digitales, donde el uso eficaz del ancho de banda es más importante que los paquetes ocasionales perdidos.

-   Protocolo de transferencia de hipertexto (HTTP)

    HTTP usa TCP y lo usan los servidores web. El esquema "httpd://" indica que el origen se puede descargar desde un servidor web. HTTP también se usa en el caso de firewalls, que normalmente están configurados para aceptar solicitudes HTTP y normalmente rechazar otros protocolos de streaming.

La aplicación puede obtener los protocolos admitidos por Media Foundation mediante la interfaz [**IMFNetSchemeHandlerConfig.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) Para ello, la aplicación debe recuperar primero el número de protocolos mediante una llamada a [**IMFNetSchemeHandlerConfig::GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) y, a continuación, obtener el tipo de protocolo basado en el índice mediante una llamada a [**IMFNetSchemeHandlerConfig::GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype). Este método devuelve uno de los valores definidos en la [**enumeración MFNETSOURCE \_ PROTOCOL \_ TYPE.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type)

La aplicación también puede obtener los esquemas admitidos por la resolución de origen llamando a la [**función MFGetSupportedSchemes.**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes)

## <a name="protocol-rollover"></a>Suversión de protocolos

Cuando una aplicación especifica "mms://" como esquema de dirección URL, el solucionador de origen realiza una operación *de suversión de* protocolo. En este proceso, la resolución de origen determina el mejor protocolo para el origen de red que se usará para obtener el contenido. Normalmente, para el tráfico de medios, RTSP con UDP (RTSPU) es más eficaz que HTTP. Sin embargo, si el contenido se hospeda en un servidor web, HTTP es una mejor opción.

La suversión de protocolo también puede producirse cuando se produce un error al intentar usar el protocolo especificado en el esquema de dirección URL. Por ejemplo, un protocolo puede producir un error cuando un firewall bloquea paquetes UDP. En este caso, la resolución de origen cambia a HTTP.

La suversión del protocolo no se aplica si el esquema de dirección URL contiene un protocolo específico, como "rtspu://". Además, no se realiza la suversión si se produce un error en la autenticación o si el servidor ha alcanzado un límite de conexiones de cliente. Se recomienda que las aplicaciones especifiquen el esquema "mms://" y permitan que la resolución de origen seleccione el mejor protocolo para el escenario.

En la tabla siguiente se muestra el orden de suversión.




| Esquemas permitidos | Orden de succión de protocolo | 
|-----------------|-------------------------|
| mms:// o rtsp:// | Caché rápida habilitada:<br /><ol><li>RTSP con TCP (RTSPT)<br /></li><li>RTSP con UDP (RTSPU)<br /></li><li>HTTP Streaming<br /></li><li>Descarga HTTP (HTTPD)<br /></li></ol>Caché rápida deshabilitada:<br /><ol><li>RTSPU<br /></li><li>RTSPT<br /></li><li>HTTP Streaming<br /></li><li>Descarga de HTTP<br /></li></ol> | 
| rtspu:// | RTSPU | 
| rtspt:// | RTSPT | 
| https:// | <ol><li>HTTP<br /></li><li>HTTPD<br /></li></ol> | 
| httpd:// | HTTPD | 




 

## <a name="retrieving-the-current-protocol"></a>Recuperar el protocolo actual

Después de una operación de suización de protocolo, el origen de red podría usar un protocolo distinto del especificado por la aplicación en el esquema de dirección URL. El resultado de la sustitución del protocolo está disponible para la aplicación después de que el origen de red establezca la conexión con el servidor multimedia.

Para obtener el protocolo y el transporte que se usan para obtener el contenido, la aplicación puede recuperar los valores de propiedad de la propiedad [MFNETSOURCE \_ PROTOCOL](mfnetsource-protocol-property.md) y la propiedad [MFNETSOURCE \_ TRANSPORT](mfnetsource-transport-property.md) de un objeto **IPropertyStore** del origen de red.

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



En el código de ejemplo anterior, **IPropertyStore::GetValue** recupera el valor DE MFNETSOURCE PROTOCOL, que es miembro de la enumeración \_ [**MFNETSOURCE \_ PROTOCOL \_ TYPE.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) Para MFNETSOURCE \_ TRANSPORT, el valor es un miembro de la [**enumeración MFNETSOURCE \_ TRANSPORT \_ TYPE.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type)

Como alternativa, la aplicación puede obtener los mismos valores mediante el servicio MFNETSOURCE \_ STATISTICS \_ SERVICE. Para usar este servicio, la aplicación puede llamar a la [**función MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obtener el almacén de propiedades del origen de red. Este almacén de propiedades contiene estadísticas de red en la [propiedad MFNETSOURCE \_ STATISTICS.](mfnetsource-statistics-property.md) Los valores de protocolo y transporte se pueden recuperar especificando el id. de protocolo MFNETSOURCE y el id. de transporte de MFNETSOURCE, definidos en la enumeración \_ \_ \_ \_ [**MFNETSOURCE \_ STATISTICS \_ IDS.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) El código siguiente muestra cómo obtener los valores de protocolo y transporte mediante el servicio MFNETSOURCE \_ STATISTICS \_ SERVICE.


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

La aplicación puede configurar el origen de red para que se omita ciertos protocolos durante el proceso de sucesión. Para ello, las propiedades de origen de red se usan para deshabilitar protocolos específicos. En la tabla siguiente se muestran las propiedades y los protocolos que controlan.



| Propiedad                                                                    | Descripción                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [MFNETSOURCE \_ ENABLE \_ HTTP](mfnetsource-enable-http-property.md)           | Habilita o deshabilita HTTP y HTTPD.         |
| [MFNETSOURCE \_ ENABLE \_ RTSP](mfnetsource-enable-rtsp-property.md)           | Habilita o deshabilita RTSPU y RTSPT.        |
| [MFNETSOURCE \_ ENABLE \_ TCP](mfnetsource-enable-tcp-property.md)             | Habilita o deshabilita RTSPT.                  |
| [MFNETSOURCE \_ ENABLE \_ UDP](mfnetsource-enable-udp-property.md)             | Habilita o deshabilita RTSPU.                  |
| [MFNETSOURCE \_ ENABLE \_ DOWNLOAD](mfnetsource-enable-download-property.md)   | Habilita o deshabilita HTTPD.                  |
| [MFNETSOURCE \_ ENABLE \_ STREAMING](mfnetsource-enable-streaming-property.md) | Habilita o deshabilita RTSPU, RTSPT y HTTP. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




