---
title: Reproducción de archivos de un origen de red
description: Reproducción de archivos de un origen de red
ms.assetid: 72f2d685-56fc-4da2-8372-3774cc65f59d
keywords:
- SDK de Windows Media Format, lectura de datos ASF
- SDK de Windows Media Format, reproducir archivos de orígenes de red
- Advanced Systems Format (ASF), lectura de datos
- ASF (formato de sistemas avanzados), lectura de datos
- Advanced Systems Format (ASF), reproducir archivos de orígenes de red
- ASF (formato de sistemas avanzados), reproducir archivos de orígenes de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f1e4e41ddf94498ddeddf90e64439c1b11b7ba8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "105704924"
---
# <a name="playing-files-from-a-network-source"></a>Reproducción de archivos de un origen de red

Leer desde una red no es fundamentalmente diferente de leer un archivo local. La aplicación pasa la dirección URL al método [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) del objeto lector y el objeto lector controla los detalles de los protocolos de red. El objeto lector utiliza la administración de búfer inteligente para proporcionar la reproducción más fluida posible. Si la aplicación necesita más control sobre la configuración de red del objeto del lector, estas están disponibles a través de las interfaces [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig) y [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) .

El contenido de un origen de red se divide en una de las dos categorías siguientes:

-   Difusión. Los datos se transmiten justo a tiempo para reproducirse en el equipo local. Los servidores que ejecutan Windows Media Services pueden proporcionar datos de streaming. Si el contenido de la velocidad de bits múltiple (MBR) se transmite, el cliente puede solicitar una velocidad de bits diferente del servidor a medida que progresa el streaming.
-   Fiere. Todos los datos se transmiten lo más rápido posible para que se puedan guardar como un archivo en el equipo local. Los servidores Web proporcionan datos descargados. No hay ninguna comunicación desde el cliente al servidor una vez iniciada la descarga.

Cuando el objeto lector descarga un archivo de un servidor Web, usa una técnica denominada transmisión por secuencias progresiva, que permite que un reproductor empiece a representar el contenido antes de que se complete la descarga. Los datos se almacenan en búfer para proporcionar un flujo de datos ininterrumpido al reproductor. La información como la velocidad de transferencia y la duración del contenido se usa para determinar durante cuánto tiempo se almacenan en búfer los datos antes de enviarlos al reproductor.

Para abrir un archivo o una secuencia a través de una red, llame al método **IWMReader:: Open** del objeto lector con la dirección URL adecuada. **Open** es una llamada asincrónica, por lo que se devuelve inmediatamente. Cuando el origen está listo para la lectura, el objeto de lectura envía una \_ notificación abierta de WMT al método de devolución de llamada [**IWMStatusCallback::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) en el estado de la aplicación. En este punto, la aplicación puede consultar el lector para el modo de entrega mediante una llamada a [**IWMReaderAdvanced2:: GetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode). Para el contenido de la red, este método devolverá la \_ \_ descarga del modo de reproducción WMT \_ , indicando el contenido descargado o el \_ \_ modo de reproducción WMT \_ , que indica el contenido transmitido por secuencias.

Para empezar a leer el archivo o la secuencia, llame al método [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) . El lector envía una notificación de inicio del almacenamiento en búfer de WMT \_ \_ cuando comienza a almacenar en búfer el contenido y una notificación de detención del almacenamiento en búfer de WMT \_ \_ cuando se completa el almacenamiento en búfer. Mientras el lector almacena en búfer el contenido (es decir, entre estas dos notificaciones), es posible que desee mostrar el progreso del almacenamiento en búfer al usuario. El método [**IWMReaderAdvanced2:: GetBufferProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress) devuelve el porcentaje de datos que se han almacenado en búfer y el tiempo estimado que queda. Para el contenido descargado, también puede llamar a [**IWMReaderAdvanced2:: GetDownloadProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress) para obtener el progreso de la descarga. Llame a estos métodos varias veces para actualizar la pantalla hasta que se haya completado el almacenamiento en búfer. El almacenamiento en búfer puede producirse de nuevo durante la reproducción, debido a factores como la congestión de la red. Si esto ocurre, la aplicación recibe otra notificación de inicio del almacenamiento en búfer de WMT \_ \_ .

Cuando el objeto lector comienza a reproducir el contenido, envía una notificación de \_ Inicio de WMT. Como cada ejemplo está descodificado y está disponible para la representación, el lector lo pasa a la aplicación a través del método de devolución de llamada [**IWMReaderCallback::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) OnRender. En este momento, el proceso es el mismo que para la reproducción de archivos locales. Cuando se detiene la reproducción, el lector envía un \_ final \_ de la \_ notificación de streaming de WMT.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Leer archivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




