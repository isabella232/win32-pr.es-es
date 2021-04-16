---
description: Novedades de DirectShow
ms.assetid: 675a34d4-7a33-4125-86af-cd4ed73ad430
title: Novedades de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74747349848a7b370cd4766113085c84d0c7a1d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669953"
---
# <a name="whats-new-in-directshow"></a>Novedades de DirectShow

## <a name="whats-new-for-directshow-in-windows-7"></a>Novedades de DirectShow en Windows 7

Nuevas interfaces:

-   [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling)
-   [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol)

Filtros nuevos o actualizados:

-   [**Descodificador de audio MPEG-1/DD/AAC de Microsoft**](microsoft-mpeg-1-dd-audio-decoder.md)
-   [**Descodificador de vídeo MPEG-2 de Microsoft**](microsoft-mpeg-2-video-decoder.md)

Los algoritmos de "conexión inteligente" se han modificado para admitir los filtros preferidos y bloqueados. Para obtener más información, consulte [Intelligent Connect](intelligent-connect.md).

Reproducción de DVD: nuevas opciones para el método [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) .

## <a name="whats-new-for-directshow-in-windows-vista"></a>Novedades de DirectShow en Windows Vista

-   DirectShow ahora forma parte de la Windows SDK. Los encabezados, las bibliotecas, los ejemplos y las herramientas de DirectShow ya no se incluyen en el SDK de DirectX.
-   DirectX video Acceleration (DXVA) 2,0 contiene muchas mejoras de DXVA 1,0.

    -   La canalización de vídeo de hardware se ha mejorado significativamente.
    -   Los componentes como descodificadores pueden acceder a DXVA 2,0 directamente sin comunicarse a través del representador de vídeo.
    -   La Administrador de dispositivos de Direct3D permite que los componentes compartan el mismo dispositivo Direct3D.

    Para obtener más información acerca de DXVA 2,0, consulte la documentación de [DirectX video Acceleration 2,0](../medfound/directx-video-acceleration-2-0.md) , que forma parte de la documentación de [Microsoft Media Foundation](../medfound/microsoft-media-foundation-sdk.md) .

-   El [**representador de vídeo mejorado**](enhanced-video-renderer-filter.md) (EVR) es un nuevo representador de vídeo eficaz, que comparte el mismo modelo de complemento que la versión media Foundation de EVR. Para obtener más información sobre EVR, consulte la documentación de [Microsoft Media Foundation](../medfound/microsoft-media-foundation-sdk.md) .
-   Compatibilidad con la captura del modelo de controladores de pantalla (WDDM) de Windows Vista. Esta característica permite a los filtros sacar el máximo partido de las tarjetas de vídeo con la captura de vídeo integrada para reducir las copias innecesarias entre la memoria de vídeo y la memoria del sistema. Para obtener más información, vea [uso de la captura de WDDM en DirectShow](using-wddm-capture-in-directshow.md).
-   El descodificador de audio MPEG-1 capa II ahora usa aritmética de punto flotante para mejorar la calidad de la descodificación.
-   Mejoras en la reproducción de DVD. Para obtener más información, consulte [mejoras en la reproducción de DVD en Windows Vista](dvd-playback-enhancements-in-windows-vista.md).
    -   Mejor compatibilidad con el modo de truco: transiciones suaves entre tasas; transiciones entre la reproducción hacia delante y hacia atrás; compatibilidad con la reproducción de audio durante el avance rápido y el retroceso.
    -   Almacenamiento en caché mejorado. Las aplicaciones pueden establecer la cantidad de datos que el navegador de DVD Lee de antemano. La configuración de una caché mayor puede ampliar la duración de la batería y habilitar la reproducción silenciosa (después de que la unidad gire hacia abajo). Para obtener más información, [**consulte \_ \_ marca de opción de DVD**](/windows/win32/api/strmif/ne-strmif-dvd_option_flag).
-   Dispositivos de punto de conexión de audio: las aplicaciones pueden asociar el [filtro de representador de DirectSound](directsound-renderer-filter.md) con un dispositivo de punto de conexión de audio determinado. Las aplicaciones pueden usar la API de dispositivo multimedia (MMDevice) para enumerar y seleccionar el dispositivo de punto final. Para obtener más información, consulte la documentación de la API de audio básica en el Windows SDK.
-   Los siguientes filtros se han quitado de Windows Vista:
    -   [Filtro de receptor de IP BDA](/previous-versions/windows/desktop/mstv/bda-ip-sink-filter)
    -   [Filtro de destramador de SLIP de BDA](/previous-versions/windows/desktop/mstv/bda-slip-deframer-filter)
    -   [Filtro del descodificador de CC](cc-decoder-filter.md)
    -   [Filtro de códecs de NABTS/FEC VBI](/previous-versions/windows/desktop/mstv/nabts-fec-vbi-codec-filter)
    -   [Filtro de descompresor de QT](qt-decompressor-filter.md)
    -   [Filtro de analizador de películas QuickTime](quicktime-movie-parser-filter.md)
    -   [Filtro de códec de elemento WST](wst-codec-filter.md)
    -   [Filtro de descodificador de elemento WST](wst-decoder-filter.md)
-   El código de proxy o stub para muchas de las interfaces de DirectShow se ha pasado de quartz.dll a proppage.dll. Este código se quitó de quartz.dll porque no estaba pensado para que lo usen las aplicaciones. Sin embargo, resulta útil para depurar, ya que permite que una aplicación de prueba se conecte de forma remota a un gráfico de filtros de DirectShow en otro proceso. Para usar esta característica en Windows Vista, primero debe registrar proppage.dll. Este archivo DLL está disponible en el directorio de herramientas de Windows SDK. (Para obtener más información, vea [cargar un grafo desde un proceso externo](loading-a-graph-from-an-external-process.md)).

 

 
