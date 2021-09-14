---
description: Obtenga información sobre el registro de cliente para Microsoft Media Foundation. El registro proporciona una manera de que el servidor multimedia realice un seguimiento de la actividad de los clientes que se conectan a él.
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Registro de cliente (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3874c413f61b3495dc7e67f082a83e789a7a1357
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269356"
---
# <a name="client-logging-microsoft-media-foundation"></a>Registro de cliente (Microsoft Media Foundation)

El origen de red admite el registro de cliente, que proporciona una manera de que el servidor multimedia realice un seguimiento de la actividad de los clientes que se conectan a él. Los registros de cliente permiten a un servidor registrar estadísticas de conexión, representación y streaming. Estos registros los pueden usar los proveedores de contenido en varios escenarios, como para realizar un seguimiento del uso del servidor multimedia y generar facturación, o para entregar contenido de calidad adecuada en función de la velocidad de la red del cliente.

Un archivo de registro contiene varias entradas de eventos de cliente. Cada entrada de registro contiene una serie de campos delimitados por espacios. Hay dos tipos de registros de cliente: *representación* (reproducción) y *streaming* (recepción). Dado que el contenido se puede reproducir y transmitir simultáneamente, el cliente puede enviar una combinación de ambos tipos de datos de registro. En algunos casos, pueden existir dos entradas de registro para la misma sesión. Por ejemplo, cuando Fast Cache está habilitado, el cliente puede terminar de recibir el contenido transmitido antes de terminar de representarlo. En ese caso, los datos de registro de streaming se enviarían antes que los datos de registro de representación.

El cliente envía los datos de registro de representación al servidor cuando el cliente cambia de cualquier estado de reproducción (reproducción, avance rápido o rebobinado) a un estado no reproduciendo (detenerse, pausar, finalizar la secuencia e iniciar la secuencia). Cuando se envían datos para un registro de representación, se realiza una conexión directamente al servidor multimedia o a un servidor proxy configurado.

Si el contenido se almacena en un archivo de caché local temporal en el equipo que ejecuta el cliente, el cliente puede leer un archivo de su caché local y enviar los datos de registro de representación para indicar que ha reproducdo el contenido. En este caso, el cliente lee un archivo de su caché local, la entrada del registro de representación no contiene estadísticas de red y el protocolo se establece en Caché.

El cliente envía datos de registro de streaming al servidor para indicar cómo el cliente recibió el contenido, pero no cómo se representó. El cliente puede enviar el registro de streaming mucho antes de que el cliente termine de representar el contenido.

En este tema no se proporciona información sobre todos los campos de registro. Para obtener una referencia completa, [vea Windows estructura de datos de registro multimedia](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).

## <a name="configuring-log-fields"></a>Configuración de campos de registro

Media Foundation permite al cliente configurar el origen de red mediante propiedades. La aplicación debe establecer las propiedades adecuadas en un almacén de propiedades y pasarla a uno de los métodos de resolución de origen. El solucionador de origen crea el origen de red como se solicitó y abre una conexión con el servidor. Si la conexión es correcta, el cliente envía información sobre sí mismo.

En la tabla siguiente se describen los campos de registro y las propiedades correspondientes que una aplicación puede establecer a través del solucionador de origen. Esta información no cambia durante la sesión.




| Campo De registro | Descripción | 
|---------------|-------------|
| c-playerid | Identificación única del jugador. Esta información se envía al principio de la conexión. Normalmente, se trata de un GUID del cliente. El cliente puede enviar esta información al servidor en la <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> propiedad .<br /> El cliente envía esta información al servidor al principio de la conexión.<br /> Valor de ejemplo: "{c579d042-cecc-11d1-bb31-00a0c9603954}"<br /> | 
| c-playerversion | Número de versión del reproductor que se envía al principio de la conexión. El cliente puede enviar esta información al servidor en la <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> propiedad .<br /> El cliente envía esta información al servidor al principio de la conexión.<br /> | 
| cs(User-Agent) | Tipo de explorador usado si el reproductor se insertó en un explorador. El cliente puede establecer este valor en la <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> propiedad .<br /> Si el reproductor no está incrustado, este campo hace referencia al agente de usuario del cliente que generó el registro. En este caso, el cliente debe establecer la <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> propiedad .<br /> El cliente envía esta información al servidor al principio de la conexión.<br /> Valor de ejemplo: "Mozilla/4.0_(compatible;_MSIE_4.01;_Windows_98)"<br /> | 
| cs(Referer) | Dirección URL de la página web en la que se insertó el reproductor (si se insertó). El cliente puede enviar esta información al servidor en la <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> propiedad .<br /> El cliente envía esta información al servidor al final de la conexión.<br /> Valor de ejemplo: " https://www.example.microsoft.com "<br /> | 
| c-hostexe | Para las entradas de registro del reproductor, el programa host (.exe) que se ha ejecutado. Por ejemplo, una página web en un explorador, un applet Visual Basic Microsoft o un reproductor independiente. El cliente puede enviar esta información al servidor en la <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> propiedad .<br /> El cliente envía esta información al servidor al final de la conexión.<br /> Valores de ejemplo:<br /><ul><li>"iexplore.exe"</li><li>"myplayer.exe"</li></ul> | 
| c-hostexever | Número de versión del programa host (.exe). El cliente puede enviar esta información al servidor en la <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> propiedad .<br /> El cliente envía esta información al servidor al final de la conexión.<br /> | 




 

En el ejemplo de código siguiente se muestra cómo una aplicación cliente configura el origen de red. En este ejemplo se establece el campo de registro "c-hostexe".


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set the MFNETSOURCE_HOSTEXE
// configuration property on the network source.

HRESULT CreateMediaSourceWithLogParams(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_HOSTEXE;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_LPWSTR;
        var.pwszVal = L"MyPlayer.exe";

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="retrieving-network-statistics"></a>Recuperar estadísticas de red

Cuando la aplicación llama a uno de los métodos de resolución de origen, crea el origen de red, establece las propiedades especificadas en el almacén de propiedades y abre una sesión con el servidor multimedia. Además de la información configurable descrita en la sección anterior, se transfieren datos adicionales entre el servidor y el cliente al principio de la sesión, durante el streaming y cuando se cierra la sesión.

La aplicación puede recuperar estadísticas de red mediante el identificador de servicio **MFNETSOURCE \_ STATISTICS \_ SERVICE.** Para usar este servicio, la aplicación puede llamar a la función [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obtener el almacén de propiedades que contiene estadísticas de red en la [**propiedad MFNETSOURCE \_ STATISTICS.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) Se pueden recuperar valores específicos proporcionando el identificador correspondiente definido en la enumeración **MFNETSOURCE \_ STATISTICS \_ IDS.**

En el ejemplo de código siguiente se muestra cómo usar el servicio para obtener el número de paquetes recibidos por el cliente.


```C++
HRESULT GetPacketsReceived(IMFMediaSession *pSession, DWORD *pcPackets)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    // Get the number of packets received by the client.

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_RECVPACKETS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pcPackets = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



En la lista siguiente se describen algunos de los identificadores de estadísticas de red definidos en [**MFNETSOURCE \_ \_ STATISTICS IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).



| Identificador de estadísticas de red              | Descripción                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ID. \_ DE AVGBANDWIDTHBPS DE \_ MFNETSOURCE**       | Ancho de banda medio (en bits por segundo) en el que el cliente estaba conectado al servidor. El valor se calcula a lo largo de toda la duración de la conexión.                                                              |
| **ID. \_ DE MFNETSOURCE \_ BUFFERINGCOUNT**        | Número de veces que el cliente se almacena en búfer mientras se reproduce la secuencia.                                                                                                                                                              |
| **MFNETSOURCE \_ BYTESRECEIVED \_ ID**         | Número de bytes recibidos por el cliente del servidor. El valor no incluye ninguna sobrecarga agregada por la pila de red. El mismo contenido transmitido mediante protocolos diferentes puede dar lugar a valores diferentes. |
| **ID. DE \_ MFNETSOURCE LINKBANDWIDTH \_**         | Ancho de banda máximo disponible del cliente en bits por segundo.                                                                                                                                                              |
| **ID. \_ DE LOSTPACKETS DE MFNETSOURCE \_**           | Número de paquetes enviados por el servidor pero perdidos durante la transmisión y nunca reproducida por el cliente. El valor no incluye paquetes TCP o UDP.                                                                          |
| **ID. \_ DE RECVPACKETS DE MFNETSOURCE \_**           | Número de paquetes recibidos del servidor El valor no incluye paquetes TCP o UDP.                                                                                                                                  |
| **ID. \_ DE MFNETSOURCE RECOVEREDBYECCPACKETS \_** | Paquetes perdidos en la red que se repararon y recuperaron en la capa de cliente. Este valor no incluye paquetes TCP o UDP.                                                                                          |
| **ID. \_ DE RESENDSREQUESTED DE \_ MFNETSOURCE**      | Número de solicitudes realizadas por el cliente para recibir nuevos paquetes. Este valor no incluye paquetes TCP o UDP.                                                                                                          |
| **MFNETSOURCE \_ RECOVEREDPACKETS \_ ID**      | Número de paquetes recuperados porque se han reenviado a través de UDP. Este valor no incluye paquetes TCP o UDP. Este campo contiene un cero a menos que el cliente use el reenenlaz de UDP.                                        |
| **ID. \_ DE BUFFERPROGRESS DE \_ MFNETSOURCE**        | Porcentaje del búfer de reproducción rellenado durante el almacenamiento en búfer.                                                                                                                                                              |
| **ID. DE \_ PROTOCOLO \_ MFNETSOURCE**              | Protocolo usado para acceder a la secuencia. Esto puede diferir del protocolo solicitado por el cliente.                                                                                                                             |
| **ID. DE \_ TRANSPORTE DE MFNETSOURCE \_**             | Protocolo de transporte usado para entregar la secuencia. Debe ser UDP o TCP.                                                                                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de origen de red](network-source-features.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

