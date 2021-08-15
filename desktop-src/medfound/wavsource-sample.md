---
description: Ejemplo de WavSource
ms.assetid: 905fbba5-0a04-4048-80bd-f8707c4879da
title: Ejemplo de WavSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffba8ab5bfd5ae1ccfb4df4c90b447c412e9e835a403d496834224f012f8bad7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972544"
---
# <a name="wavsource-sample"></a>Ejemplo de WavSource

Muestra cómo crear un origen multimedia personalizado en Microsoft Media Foundation. El ejemplo implementa un origen multimedia que analiza archivos de audio .wav.

Este ejemplo es un ejemplo relativamente sencillo de un origen multimedia:

-   Solo hay una secuencia, por lo que no hay código para implementar la selección de secuencias.
-   El origen multimedia no implementa el control de velocidad (es decir, una reproducción hacia delante o hacia atrás rápida).
-   Todos los métodos de origen y flujo se implementan como métodos sincrónicos.
-   Dado que la parte de datos de un archivo .wav es un único bloque de audio PCM sin comprimir, el origen multimedia no necesita leer encabezados de paquetes ni analizar la secuencia durante la reproducción, aparte de leer el encabezado [**WAVEFORMAT inicial.**](/windows/win32/api/mmreg/ns-mmreg-waveformat)

Para obtener un ejemplo más avanzado de un origen multimedia, vea [el ejemplo MPEG1Source](mpeg1source-sample.md).

## <a name="apis-demonstrated"></a>API demostradas

En este ejemplo se muestran las siguientes Media Foundation interfaces:

-   [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

## <a name="usage"></a>Uso

El ejemplo WavSource compila un archivo DLL que es un servidor COM para el origen de medios y el controlador de flujo de bytes del origen de medios. Antes de usar el origen de medios, debe registrar el archivo DLL.

Para usar el origen multimedia, puede ejecutar [BasicPlayback](/previous-versions//bb970475(v=vs.85)). La resolución de origen cargará automáticamente el origen multimedia si selecciona un archivo .wav para la reproducción. (Si se produce un error, asegúrese de que ha registrado correctamente el archivo DLL de WavSource).

También puede usar la herramienta TopoEdit para crear una topología de reproducción que contenga el origen multimedia. Para obtener más información sobre TopoEdit, vea [TopoEdit](topoedit.md).

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el repositorio [de github Windows ejemplos clásicos](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Orígenes multimedia](media-sources.md)
</dt> <dt>

[Ejemplo MPEG1Source](mpeg1source-sample.md)
</dt> <dt>

[Controladores de esquema y Byte-Stream de esquema](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Escribir un origen multimedia personalizado](writing-a-custom-media-source.md)
</dt> </dl>

 

 
