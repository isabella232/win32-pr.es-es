---
description: Ejemplo de WavSource
ms.assetid: 905fbba5-0a04-4048-80bd-f8707c4879da
title: Ejemplo de WavSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050edb9df75032384f93c6e1f37c52e89f14a748
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908627"
---
# <a name="wavsource-sample"></a>Ejemplo de WavSource

Muestra cómo crear un origen de medios personalizado en Microsoft Media Foundation. El ejemplo implementa un origen de medios que analiza los archivos de audio. wav.

Este ejemplo es un ejemplo relativamente sencillo de un origen multimedia:

-   Solo hay una secuencia, por lo que no hay ningún código para implementar la selección de la secuencia.
-   El origen multimedia no implementa el control de velocidad (es decir, reproducción rápida o inversa).
-   Todos los métodos de origen y de secuencia se implementan como métodos sincrónicos.
-   Dado que la parte de datos de un archivo. wav es un único bloque de audio PCM sin comprimir, el origen multimedia no necesita leer los encabezados de paquete o analizar la secuencia durante la reproducción, aparte de leer el encabezado [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) inicial.

Para obtener un ejemplo más avanzado de un origen multimedia, vea el [ejemplo MPEG1Source](mpeg1source-sample.md).

## <a name="apis-demonstrated"></a>API mostradas

Este ejemplo muestra las siguientes interfaces de Media Foundation:

-   [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

## <a name="usage"></a>Uso

En el ejemplo WavSource se crea un archivo DLL que es un servidor COM para el controlador de flujo de bytes del origen multimedia y el origen del medio. Antes de usar el origen de medios, debe registrar el archivo DLL.

Para usar el origen de medios, puede ejecutar [BasicPlayback](/previous-versions//bb970475(v=vs.85)). La resolución de origen cargará automáticamente el origen multimedia si selecciona un archivo. wav para la reproducción. (Si se produce un error, asegúrese de que ha registrado correctamente el archivo DLL de WavSource).

También puede usar la herramienta TopoEdit para crear una topología de reproducción que contenga el origen de medios. Para obtener más información sobre TopoEdit, consulte [TopoEdit](topoedit.md).

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Orígenes multimedia](media-sources.md)
</dt> <dt>

[Ejemplo de MPEG1Source](mpeg1source-sample.md)
</dt> <dt>

[Controladores de esquema y controladores de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Escritura de un origen de medios personalizado](writing-a-custom-media-source.md)
</dt> </dl>

 

 
