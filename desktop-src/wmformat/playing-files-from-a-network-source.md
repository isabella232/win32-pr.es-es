---
title: Reproducir archivos desde un origen de red
description: Reproducir archivos desde un origen de red
ms.assetid: 72f2d685-56fc-4da2-8372-3774cc65f59d
keywords:
- Windows SDK de formato multimedia, lectura de datos de ASF
- Windows SDK de formato multimedia, reproducir archivos de orígenes de red
- Formato de sistemas avanzados (ASF), leer datos
- ASF (formato de sistemas avanzados), leer datos
- Formato de sistemas avanzados (ASF), reproducir archivos de orígenes de red
- ASF (formato de sistemas avanzados), reproducción de archivos desde orígenes de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8473a2feb4edd567c15d640dfd20e65c2893fe12de6c25a957cc5f730fde0baf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027383"
---
# <a name="playing-files-from-a-network-source"></a>Reproducir archivos desde un origen de red

Leer desde una red no es fundamentalmente diferente de leer un archivo local. La aplicación pasa la dirección URL al método [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) del objeto lector y el objeto reader controla los detalles de los protocolos de red. El objeto lector usa la administración de búfer inteligente para proporcionar la reproducción más fluida posible. Si la aplicación necesita más control sobre la configuración de red del objeto lector, están disponibles a través de las interfaces [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig) e [**IWMReaderNetworkConfig2.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2)

El contenido de un origen de red se divide en una de las dos categorías siguientes:

-   Streaming. Los datos se transmiten justo a tiempo para reproducirse en la máquina local. Los servidores que Servicios de Windows Media pueden proporcionar datos de streaming. Si se transmite contenido de velocidad de bits múltiple (MBR), el cliente puede solicitar una velocidad de bits diferente al servidor a medida que avanza el streaming.
-   Descargó. Todos los datos se transmiten lo más rápido posible para que se puedan guardar como un archivo en el equipo local. Los servidores web proporcionan datos descargados. No hay ninguna comunicación del cliente con el servidor después de que comience la descarga.

Cuando el objeto de lector descarga un archivo de un servidor web, usa una técnica denominada streaming progresiva, que permite a un reproductor empezar a representar el contenido antes de que se complete la descarga. Los datos se almacena en búfer para proporcionar un flujo ininterrumpido de datos al reproductor. Información como la velocidad de transferencia y la duración del contenido se usa para determinar cuánto tiempo se almacenarán en búfer los datos antes de entregarlo al jugador.

Para abrir un archivo o secuencia a través de una red, llame al método **IWMReader::Open** del objeto lector con la dirección URL adecuada. **Open** es una llamada asincrónica, por lo que se devuelve inmediatamente. Cuando el origen está listo para leerse, el objeto reader envía una notificación WMT OPENED al método de devolución de llamada \_ [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) de la aplicación. En este momento, la aplicación puede consultar al lector el modo de entrega llamando a [**IWMReaderAdvanced2::GetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode). Para el contenido de red, este método devolverá WMT PLAY MODE DOWNLOAD, que indica el contenido descargado, o \_ \_ \_ WMT \_ PLAY MODE \_ STREAMING, que indica el \_ contenido transmitido.

Para empezar a leer el archivo o la secuencia, llame al [**método IWMReader::Start.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) El lector envía una notificación WMT BUFFERING START cuando comienza a almacenar en búfer el contenido y una notificación WMT BUFFERING STOP cuando se completa \_ \_ el almacenamiento en \_ \_ búfer. Mientras el lector almacena en búfer el contenido (es decir, entre estas dos notificaciones), es posible que desee mostrar el progreso del almacenamiento en búfer al usuario. El [**método IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress) devuelve el porcentaje de datos almacenados en búfer y el tiempo estimado que permanece. Para el contenido descargado, también puede llamar a [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress) para obtener el progreso de la descarga. Llame a estos métodos varias veces para actualizar la pantalla, hasta que se haya completado el almacenamiento en búfer. El almacenamiento en búfer puede volver a producirse durante la reproducción, debido a factores como la congestión de la red. Si esto ocurre, la aplicación recibe otra notificación \_ WMT BUFFERING \_ START.

Cuando el objeto de lector comienza a reproducir el contenido, envía una notificación WMT \_ STARTED. A medida que cada ejemplo se descodifica y está disponible para su representación, el lector lo pasa a la aplicación a través del método de devolución de llamada [**IWMReaderCallback::OnSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) En este momento, el proceso es el mismo que para la reproducción de archivos locales. Cuando se detiene la reproducción, el lector envía una notificación \_ WMT END \_ OF \_ STREAMING.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Lectura de archivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




