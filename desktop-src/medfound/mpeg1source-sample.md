---
description: Ejemplo MPEG1Source
ms.assetid: c9f131ff-0b79-487c-9a46-a9b1350553a1
title: Ejemplo MPEG1Source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 652a58877267eaa92f906de88d40e614ce5b598220d4b76030caffa2187c8626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058843"
---
# <a name="mpeg1source-sample"></a>Ejemplo MPEG1Source

Muestra cómo escribir un origen multimedia personalizado en Microsoft Media Foundation. El ejemplo implementa un origen multimedia que analiza secuencias de capa de sistemas MPEG-1 y genera ejemplos que contienen cargas MPEG-1.

## <a name="apis-demonstrated"></a>API demostradas

En este ejemplo se muestran las siguientes Media Foundation interfaces:

-   [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

Antes de examinar este ejemplo, es posible que quiera revisar el ejemplo [WavSource](wavsource-sample.md), que proporciona una implementación más sencilla de un origen multimedia. El ejemplo MPEG1Source agrega algunas características que se encontrarían en la mayoría de las implementaciones del mundo real de un origen multimedia:

-   Varios flujos
-   Métodos asincrónicos
-   E/S asincrónica

En Windows SDK para Windows Server 2008, este ejemplo también incluye un descodificador de vídeo MPEG-1 de ejemplo que muestra el código de hora de cada fotograma de vídeo. (Realmente no descodifica la secuencia de bits MPEG-1).

A partir del SDK Windows para Windows 7, el descodificador se ha movido a un ejemplo independiente. Vea [Ejemplo de descodificador](decoder-sample.md).

## <a name="usage"></a>Uso

El ejemplo MPEG1Source compila un archivo DLL que es un servidor COM para el origen multimedia, el controlador de flujo de bytes del origen de medios y el descodificador MFT. Antes de usar el origen de medios, debe registrar el archivo DLL.

Para usar el origen multimedia, puede ejecutar [basicPlayback Sample](/previous-versions//bb970475(v=vs.85)). La resolución de origen cargará automáticamente el origen multimedia si selecciona un archivo MPEG-1 para la reproducción. (Si se produce un error, asegúrese de que ha registrado correctamente el archivo DLL MPEG1Source).

También puede usar la herramienta TopoEdit para crear una topología de reproducción que contenga el origen multimedia. Para obtener más información sobre TopoEdit, vea [TopoEdit](topoedit.md).

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el repositorio [de GitHub Windows ejemplos clásicos.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Orígenes multimedia](media-sources.md)
</dt> <dt>

[Controladores de esquema y Byte-Stream de esquema](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Tutorial: Escritura de un origen multimedia personalizado](tutorial--writing-a-custom-media-source.md)
</dt> <dt>

[Ejemplo de WavSource](wavsource-sample.md)
</dt> </dl>

 

 
