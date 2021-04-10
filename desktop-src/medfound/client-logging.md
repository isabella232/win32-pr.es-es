---
description: Registro de cliente
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Registro de clientes (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3cb03c8026e91acd567358e7004211b7fdde4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275144"
---
# <a name="client-logging-microsoft-media-foundation"></a>Registro de clientes (Microsoft Media Foundation)

El origen de red es compatible con el registro de cliente, que proporciona una manera para que el servidor multimedia realice un seguimiento de la actividad de los clientes que se conectan a él. Los registros de cliente permiten que un servidor registre las estadísticas de conexión, representación y transmisión por secuencias. Los proveedores de contenido pueden utilizar estos registros en varios escenarios, como, para realizar un seguimiento del uso del servidor multimedia y generar la facturación, o para proporcionar contenido de calidad adecuada en función de la velocidad de la red del cliente.

Un archivo de registro contiene varias entradas de eventos de cliente. Cada entrada de registro contiene varios campos delimitados por espacios. Hay dos tipos de registros de cliente: *representación* (reproducción) y *transmisión por secuencias* (recepción). Dado que el contenido se puede reproducir y transmitir simultáneamente, el cliente puede enviar una combinación de ambos tipos de datos de registro. En algunos casos, pueden existir dos entradas de registro para la misma sesión. Por ejemplo, cuando la memoria caché rápida está habilitada, el cliente puede terminar de recibir el contenido transmitido antes de que termine de presentarlo. En ese caso, los datos del registro de streaming se enviarían antes que los datos de registro de representación.

El cliente envía los datos de registro de representación al servidor cuando el cliente cambia de cualquier estado de reproducción (reproducción, avance rápido o rebobinado) a un estado de no reproducción (detención, pausa, finalización del flujo y comienzo de la secuencia). Cuando se envían datos para un registro de representación, se establece una conexión directamente con el servidor multimedia o un servidor proxy configurado.

Si el contenido se almacena en un archivo de caché local temporal en el equipo que ejecuta el cliente de, el cliente puede leer un archivo de su caché local y enviar los datos de registro de representación para indicar que ha reproducido el contenido. En este caso, el cliente Lee un archivo de la memoria caché local, la entrada del registro de representación no contiene ninguna estadística de red y el protocolo se establece en caché.

El cliente envía datos de registro de streaming al servidor para indicar cómo el cliente recibió el contenido, pero no cómo se representó. El cliente puede enviar el registro de streaming durante el tiempo antes de que el cliente termine de representar el contenido.

En este tema no se proporciona información sobre todos los campos de registro. Para obtener una referencia completa, vea [estructura de datos del registro de Windows Media](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).

## <a name="configuring-log-fields"></a>Configuración de campos de registro

Media Foundation permite al cliente configurar el origen de red mediante propiedades. La aplicación debe establecer las propiedades adecuadas en un almacén de propiedades y pasarlo a uno de los métodos de resolución de origen. La resolución de origen crea el origen de red tal y como se solicitó y abre una conexión con el servidor. Si la conexión se realiza correctamente, el cliente envía información sobre sí misma.

En la tabla siguiente se describen los campos de registro y las propiedades correspondientes que una aplicación puede establecer a través de la resolución de origen. Esta información no cambia durante la sesión.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo de registro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>c-playerid</td>
<td>Identificación única del reproductor. Esta información se envía al principio de la conexión. Normalmente, se trata de un GUID del cliente de. El cliente puede enviar esta información al servidor en la <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> propiedad.<br/> El cliente envía esta información al servidor al principio de la conexión.<br/> Valor de ejemplo: &quot; {c579d042-CECC-11D1-BB31-00a0c9603954}&quot;<br/></td>
</tr>
<tr class="even">
<td>c-playerversion</td>
<td>Número de versión del reproductor que se envía al principio de la conexión. El cliente puede enviar esta información al servidor en la <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> propiedad.<br/> El cliente envía esta información al servidor al principio de la conexión.<br/></td>
</tr>
<tr class="odd">
<td>CS (User-Agent)</td>
<td>Tipo de explorador que se usa si el reproductor estaba incrustado en un explorador. El cliente puede establecer este valor en la propiedad <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> .<br/> Si no se incrustó el reproductor, este campo hace referencia al agente de usuario del cliente que generó el registro. En este caso, el cliente debe establecer la propiedad <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> .<br/> El cliente envía esta información al servidor al principio de la conexión.<br/> Valor de ejemplo: &quot; Mozilla/4.0 _ (compatible; _MSIE_4.01; _Windows_98)&quot;<br/></td>
</tr>
<tr class="even">
<td>CS (referer)</td>
<td>Dirección URL de la página web en la que se incrustó el reproductor (si se incrustó). El cliente puede enviar esta información al servidor en la <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> propiedad.<br/> El cliente envía esta información al servidor al final de la conexión.<br/> Valor de ejemplo: &quot; https://www.example.microsoft.com&quot ;<br/></td>
</tr>
<tr class="odd">
<td>c-hostexe</td>
<td>Para las entradas de registro del reproductor, el programa host (. exe) que se ejecutó. Por ejemplo, una página web en un explorador, un applet de Microsoft Visual Basic o un reproductor independiente. El cliente puede enviar esta información al servidor en la <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> propiedad.<br/> El cliente envía esta información al servidor al final de la conexión.<br/> Valores de ejemplo:<br/>
<ul>
<li>&quot;iexplore.exe&quot;</li>
<li>&quot;myplayer.exe&quot;</li>
</ul></td>
</tr>
<tr class="even">
<td>c-hostexever</td>
<td>Número de versión del programa host (. exe). El cliente puede enviar esta información al servidor en la <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> propiedad.<br/> El cliente envía esta información al servidor al final de la conexión.<br/></td>
</tr>
</tbody>
</table>



 

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



## <a name="retrieving-network-statistics"></a>Recuperando estadísticas de red

Cuando la aplicación llama a uno de los métodos de resolución de origen, crea el origen de red, establece las propiedades especificadas en el almacén de propiedades y abre una sesión con el servidor multimedia. Además de la información configurable descrita en la sección anterior, los datos adicionales se transfieren entre el servidor y el cliente al principio de la sesión, durante el streaming y cuando se cierra la sesión.

La aplicación puede recuperar estadísticas de red mediante el identificador del servicio **MFNETSOURCE \_ Statistics \_ Service** . Para usar este servicio, la aplicación puede llamar a la función [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obtener el almacén de propiedades que contiene las estadísticas de red en la propiedad [**MFNETSOURCE \_ Statistics**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) . Los valores específicos se pueden recuperar proporcionando el identificador correspondiente definido en la enumeración de **\_ \_ identificadores de estadísticas de MFNETSOURCE** .

En el ejemplo de código siguiente se muestra cómo utilizar el servicio para obtener el número de paquetes recibidos por el cliente.


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



En la lista siguiente se describen algunos de los identificadores de estadísticas de red definidos en los [**\_ \_ identificadores de estadísticas de MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).



| Identificador de estadísticas de red              | Descripción                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFNETSOURCE \_ \_ ID AVGBANDWIDTHBPS**       | Promedio de ancho de banda (en bits por segundo) en el que el cliente se conectó al servidor. El valor se calcula a lo largo de toda la duración de la conexión.                                                              |
| **MFNETSOURCE \_ \_ ID BUFFERINGCOUNT**        | Número de veces que el cliente ha almacenado en búfer mientras se reproduce la secuencia.                                                                                                                                                              |
| **MFNETSOURCE \_ \_ ID BYTESRECEIVED**         | Número de bytes recibidos por el cliente desde el servidor. El valor no incluye ninguna sobrecarga agregada por la pila de red. El mismo contenido transmitido mediante distintos protocolos puede dar lugar a valores diferentes. |
| **MFNETSOURCE \_ \_ ID LINKBANDWIDTH**         | Ancho de banda máximo disponible del cliente en bits por segundo.                                                                                                                                                              |
| **MFNETSOURCE \_ \_ ID LOSTPACKETS**           | Número de paquetes enviados por el servidor, que se han perdido durante la transmisión y nunca lo reproduce el cliente. El valor no incluye los paquetes TCP o UDP.                                                                          |
| **MFNETSOURCE \_ \_ ID RECVPACKETS**           | Número de paquetes recibidos del servidor. el valor no incluye los paquetes TCP o UDP.                                                                                                                                  |
| **MFNETSOURCE \_ \_ ID RECOVEREDBYECCPACKETS** | Paquetes perdidos en la red que se reparó y se recuperaron en el nivel de cliente. Este valor no incluye los paquetes TCP o UDP.                                                                                          |
| **MFNETSOURCE \_ \_ ID RESENDSREQUESTED**      | El número de solicitudes realizadas por el cliente para recibir nuevos paquetes. Este valor no incluye los paquetes TCP o UDP.                                                                                                          |
| **MFNETSOURCE \_ \_ ID RECOVEREDPACKETS**      | Número de paquetes recuperados porque se reenviaron a través de UDP. Este valor no incluye los paquetes TCP o UDP. Este campo contiene un cero a menos que el cliente use el reenvío de UDP.                                        |
| **MFNETSOURCE \_ \_ ID BUFFERPROGRESS**        | Porcentaje del búfer de emisión rellenado durante el almacenamiento en búfer.                                                                                                                                                              |
| **\_identificador de protocolo MFNETSOURCE \_**              | Protocolo utilizado para tener acceso a la secuencia. Esto puede diferir del protocolo solicitado por el cliente.                                                                                                                             |
| **\_identificador de transporte de MFNETSOURCE \_**             | Protocolo de transporte que se usa para proporcionar la secuencia. Debe ser UDP o TCP.                                                                                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de origen de red](network-source-features.md)
</dt> <dt>

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

