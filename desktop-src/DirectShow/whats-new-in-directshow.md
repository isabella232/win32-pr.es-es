---
description: Novedades de DirectShow
ms.assetid: 675a34d4-7a33-4125-86af-cd4ed73ad430
title: Novedades de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd05d11931d7c23a078643724b99dfed84b65e3a7db3e4ed60df9cd2a3273f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071889"
---
# <a name="whats-new-in-directshow"></a>Novedades de DirectShow

## <a name="whats-new-for-directshow-in-windows-7"></a>Novedades de DirectShow en Windows 7

Nuevas interfaces:

-   [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling)
-   [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol)

Filtros nuevos o actualizados:

-   [**Descodificador de audio Microsoft MPEG-1/DD/AAC**](microsoft-mpeg-1-dd-audio-decoder.md)
-   [**Descodificador de vídeo MPEG-2 de Microsoft**](microsoft-mpeg-2-video-decoder.md)

Los algoritmos de "conexión inteligente" se han modificado para admitir filtros preferidos y bloqueados. Para más información, consulte [Intelligent Conectar](intelligent-connect.md).

Reproducción de DVD: nuevas opciones para [**el método IDvdControl2::SetOption.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption)

## <a name="whats-new-for-directshow-in-windows-vista"></a>Novedades de DirectShow en Windows Vista

-   DirectShow ahora forma parte del SDK de Windows. Los DirectShow, bibliotecas, ejemplos y herramientas ya no se incluyen en el SDK de DirectX.
-   DirectX Video Acceleration (DXVA) 2.0 contiene muchas mejoras de DXVA 1.0.

    -   La canalización de vídeo de hardware se ha mejorado significativamente.
    -   Los componentes como los descodificadores pueden acceder a DXVA 2.0 directamente sin comunicarse a través del representador de vídeo.
    -   El Administrador de dispositivos Direct3D permite que los componentes compartan el mismo dispositivo Direct3D.

    Para más información sobre DXVA 2.0, consulte la documentación de [DirectX Video Acceleration 2.0,](../medfound/directx-video-acceleration-2-0.md) que forma parte de la [documentación Microsoft Media Foundation](../medfound/microsoft-media-foundation-sdk.md) vídeo.

-   El [**representador de**](enhanced-video-renderer-filter.md) vídeo mejorado (EVR) es un nuevo representador de vídeo eficaz, que comparte el mismo modelo de complemento que la versión Media Foundation del EVR. Para obtener más información sobre evr, consulte la [documentación Microsoft Media Foundation.](../medfound/microsoft-media-foundation-sdk.md)
-   Compatibilidad con la Windows vista Display Driver Model (WDDM). Esta característica permite que los filtros aprovechen al máximo las tarjetas de vídeo con la captura de vídeo integrada para reducir las copias innecesarias entre la memoria de vídeo y la memoria del sistema. Para obtener más información, [vea Using WDDM Capture in DirectShow](using-wddm-capture-in-directshow.md).
-   El descodificador de audio mpeg-1 capa II ahora usa aritmética de punto flotante para mejorar la calidad de descodificación.
-   Mejoras de reproducción de DVD. Para obtener más información, [vea Mejoras de reproducción de DVD Windows Vista](dvd-playback-enhancements-in-windows-vista.md).
    -   Mejor compatibilidad con el modo de truco: transiciones fluidas entre tasas; transiciones entre la reproducción hacia delante y la inversa; compatibilidad con la reproducción de audio durante el avance rápido y el retroceso.
    -   Almacenamiento en caché mejorado. Las aplicaciones pueden establecer la cantidad de datos que el navegador de DVD lee de antemano. El establecimiento de una memoria caché mayor puede extender la duración de la batería y habilitar la reproducción silenciosa (después de que la unidad se desvía). Para obtener más información, vea [**DVD \_ OPTION \_ FLAG**](/windows/win32/api/strmif/ne-strmif-dvd_option_flag).
-   Dispositivos de punto de conexión de audio: las aplicaciones pueden asociar el filtro [de representador de DirectSound](directsound-renderer-filter.md) con un dispositivo de punto de conexión de audio determinado. Las aplicaciones pueden usar la API de dispositivo multimedia (MMDevice) para enumerar y seleccionar el dispositivo de punto de conexión. Para obtener más información, consulte la documentación de Core Audio API en el SDK Windows.
-   Los siguientes filtros se han quitado de Windows Vista:
    -   [Filtro de receptor ip de BDA](/previous-versions/windows/desktop/mstv/bda-ip-sink-filter)
    -   [Filtro de deframer BDA SLIP](/previous-versions/windows/desktop/mstv/bda-slip-deframer-filter)
    -   [Filtro de descodificador CC](cc-decoder-filter.md)
    -   [Filtro de códecs VBI de MPEGTS/FEC](/previous-versions/windows/desktop/mstv/nabts-fec-vbi-codec-filter)
    -   [Filtro de descompresión QT](qt-decompressor-filter.md)
    -   [Filtro de analizador de películas de QuickTime](quicktime-movie-parser-filter.md)
    -   [Filtro de códec WST](wst-codec-filter.md)
    -   [Filtro de descodificador de WST](wst-decoder-filter.md)
-   El código proxy/stub para muchas de las interfaces DirectShow se ha movido de quartz.dll a proppage.dll. Este código se quitó de quartz.dll porque no estaba diseñado para su uso por las aplicaciones. Sin embargo, es útil para la depuración, ya que permite que una aplicación de prueba se conecte de forma remota a un DirectShow de filtro en otro proceso. Para usar esta característica en Windows Vista, primero debe registrar proppage.dll. Este archivo DLL está disponible en el directorio Windows herramientas del SDK. (Para obtener más información, vea [Carga de Graph desde un proceso externo).](loading-a-graph-from-an-external-process.md)

 

 
