---
title: Datos de la secuencia de registro
description: Datos de la secuencia de registro
ms.assetid: c902a755-afdd-4dea-bc3e-036555fdff10
keywords:
- Listas de reproducción de metarchivos de Windows Media, datos de flujo de registro
- listas de reproducción, datos de flujo de registro
- listas de reproducción de metarchivos, datos de secuencias de registro
- Listas de reproducción de metarchivos de Windows Media, registro de datos de flujo
- listas de reproducción, registro de datos de secuencias
- listas de reproducción de metarchivos, registro de datos de secuencias
- datos de la secuencia de registro
- registro de datos de flujo
- Windows Media Player, registro de datos de flujo
- Media Player de Windows, registro de datos de flujo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f234851cabf071ed2308fb5c96df2b53b60b9d45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148859"
---
# <a name="logging-stream-data"></a>Datos de la secuencia de registro

La información registrada puede adquirirse y usarse para determinar el comportamiento del visor, por ejemplo, la frecuencia con la que se ve un flujo o si un usuario específico vio un flujo y el tiempo de calidad.

La información de registro se envía automáticamente al servidor desde el que se originó la lista de reproducción. También puede enviar información de registro a servidores adicionales, incluidos los servidores web que usa exclusivamente para el registro. Para ello, use el elemento **LOGURL** y especifique una dirección URL válida para el atributo **href** . Puede incluir elementos **LOGURL** como elementos secundarios del elemento **ASX** y como elementos secundarios de los elementos de **entrada** individuales. Cuando se abre la lista de reproducción por primera vez, la información de registro se envía al servidor de origen y a cada dirección URL especificada en **LOGURL** elementos secundarios del elemento **ASX** . A continuación, a medida que se alcanza cada entrada, la información de registro específica de esa entrada se envía a cada dirección URL especificada en **LOGURL** elementos secundarios del elemento de **entrada** .

El SDK de Windows Media Format admite el elemento **LOGURL** a través de la interfaz **IWMSReaderNetworkConfig** y los métodos siguientes:


```XML
HRESULT AddLoggingUrl(LPCWSTR pwszUrl);
HRESULT GetLoggingUrl(DWORD dwIndex, LPCWSTR pwszUrl, DWORD *pcchUrl);
HRESULT GetLoggingUrlCount(DWORD *pdwUrlCount);
HRESULT ResetLoggingUrlList();

```



Además de la información que se registra automáticamente, una lista de reproducción de metarchivo puede registrar información personalizada mediante el uso del elemento **param** . Para usar el elemento **param** de esta manera, establezca el atributo **Name** en "log:" seguido de un nombre de campo de registro y un espacio de nombres XML opcional separado del nombre del campo por otro signo de dos puntos (":"). Todo lo que va después del segundo signo de dos puntos se trata como un espacio de nombres, por lo que el nombre del campo no debe contener un signo de dos puntos.

El campo de registro especificado en el atributo **Name** se establece en el valor del atributo **Value** . Si el registro todavía no contiene un campo con el nombre especificado, se agregará.

**Código de ejemplo**


```XML

    <ASX version="3.0">
      <LOGURL href="https://www.proseware.com/log.asp?SomeArg=SomeVal" />
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media1.wma" />
        <LOGURL href="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal" />
        <LOGURL href="https://www.proseware.com/WMLogging.dll?SomeArg=SomeVal" />
        <PARAM name="log:cs-media-role" value="Advertisement"/>
        <PARAM name="log:cs-media-name:namespace" value="Music"/>
        <REF href=rtsp://ucast.proseware.com/Media1.wma"/>
      </ENTRY>
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media2.wma"/>
      </ENTRY>
    </ASX>
    

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Listas de reproducción de metarchivos**](metafile-playlists.md)
</dt> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




