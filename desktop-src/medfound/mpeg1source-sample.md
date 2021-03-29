---
description: Ejemplo de MPEG1Source
ms.assetid: c9f131ff-0b79-487c-9a46-a9b1350553a1
title: Ejemplo de MPEG1Source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c71bd541a7bd01621ca7359eb9e229a08e91a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652515"
---
# <a name="mpeg1source-sample"></a>Ejemplo de MPEG1Source

Muestra cómo escribir un origen multimedia personalizado en Microsoft Media Foundation. En el ejemplo se implementa un origen multimedia que analiza los flujos de capas de sistemas MPEG-1 y genera ejemplos que contienen cargas MPEG-1.

## <a name="apis-demonstrated"></a>API mostradas

Este ejemplo muestra las siguientes interfaces de Media Foundation:

-   [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

Antes de examinar este ejemplo, es posible que desee revisar el [ejemplo WavSource](wavsource-sample.md), que proporciona una implementación más sencilla de un origen multimedia. En el ejemplo MPEG1Source se agregan algunas características que se encuentran en la mayoría de las implementaciones reales de un origen multimedia:

-   Varios flujos
-   Métodos asincrónicos
-   E/s asincrónica

En el Windows SDK para Windows Server 2008, este ejemplo también incluye un descodificador de vídeo MPEG-1 de ejemplo que muestra el código de tiempo para cada fotograma de vídeo. (En realidad, no descodifica MPEG-1 fragmentada).

A partir de la Windows SDK para Windows 7, el descodificador se ha pasado a un ejemplo independiente. Consulte [ejemplo de descodificador](decoder-sample.md).

## <a name="usage"></a>Uso

En el ejemplo MPEG1Source se crea un archivo DLL que es un servidor COM para el origen de medios, el controlador de flujo de bytes del origen multimedia y la MFT del descodificador. Antes de usar el origen de medios, debe registrar el archivo DLL.

Para usar el origen de medios, puede ejecutar el [ejemplo BasicPlayback](/previous-versions//bb970475(v=vs.85)). La resolución de origen cargará automáticamente el origen multimedia si selecciona un archivo MPEG-1 para la reproducción. (Si se produce un error, asegúrese de que ha registrado correctamente el archivo DLL de MPEG1Source).

También puede usar la herramienta TopoEdit para crear una topología de reproducción que contenga el origen de medios. Para obtener más información sobre TopoEdit, consulte [TopoEdit](topoedit.md).

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Orígenes multimedia](media-sources.md)
</dt> <dt>

[Controladores de esquema y controladores de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Tutorial: escribir un origen de medios personalizado](tutorial--writing-a-custom-media-source.md)
</dt> <dt>

[Ejemplo de WavSource](wavsource-sample.md)
</dt> </dl>

 

 
