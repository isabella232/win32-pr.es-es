---
title: Registro de datos de flujo
description: Registro de datos de flujo
ms.assetid: c902a755-afdd-4dea-bc3e-036555fdff10
keywords:
- Windows Listas de reproducción de metarchivos multimedia, registro de datos de flujo
- listas de reproducción, registro de datos de flujo
- listas de reproducción de metarchivo, registro de datos de flujo
- Windows Listas de reproducción de metarchivo multimedia, registro de datos de flujo
- listas de reproducción, registro de datos de flujo
- listas de reproducción de metarchivo, registro de datos de flujo
- registro de datos de flujo
- registro de datos de flujo
- Reproductor de Windows Media datos de flujo de registro
- Reproductor de Windows Media,stream data logging
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f234851cabf071ed2308fb5c96df2b53b60b9d45
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967571"
---
# <a name="logging-stream-data"></a>Registro de datos de flujo

La información registrada se puede adquirir y usar para determinar el comportamiento del visor, por ejemplo, la frecuencia con la que se ve una secuencia o si un usuario específico ha visto una secuencia y durante cuánto tiempo con qué calidad.

La información de registro se envía automáticamente al servidor desde el que se originó la lista de reproducción. También puede enviar información de registro a servidores adicionales, incluidos los servidores web que usa exclusivamente para el registro. Para ello, use el **elemento LOGURL** y especifique una dirección URL válida para el **atributo HREF.** Puede incluir elementos **LOGURL como** elementos secundarios del **elemento ASX** y como elementos secundarios de elementos **ENTRY** individuales. Cuando se abre la lista de reproducción por primera vez, la información de registro se envía al servidor de origen y a cada dirección URL especificada en los elementos secundarios **LOGURL** del **elemento ASX.** A continuación, a medida que se alcanza cada entrada, la información de registro específica de esa entrada se envía a cada dirección URL especificada en los elementos secundarios **LOGURL** del **elemento ENTRY.**

El SDK Windows Media Format admite el **elemento LOGURL** a través de la **interfaz IWMSReaderNetworkConfig** y los métodos siguientes:


```XML
HRESULT AddLoggingUrl(LPCWSTR pwszUrl);
HRESULT GetLoggingUrl(DWORD dwIndex, LPCWSTR pwszUrl, DWORD *pcchUrl);
HRESULT GetLoggingUrlCount(DWORD *pdwUrlCount);
HRESULT ResetLoggingUrlList();

```



Además de la información que se registra automáticamente, una lista de reproducción de metarchivo puede registrar información personalizada mediante el uso del **elemento PARAM.** Para usar el **elemento PARAM** de esta manera, establezca el atributo **NAME** en "log:" seguido de un nombre de campo de registro y un espacio de nombres XML opcional separado del nombre del campo por otros dos puntos (":"). Todo lo que hay después del segundo signo de dos puntos se trata como un espacio de nombres, por lo que el nombre del campo no debe contener dos puntos.

El campo de registro especificado en el **atributo NAME** se establece en el valor del **atributo VALUE.** Si el registro aún no contiene un campo con el nombre especificado, se agregará.

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

[**Listas de reproducción de metarchivo**](metafile-playlists.md)
</dt> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




