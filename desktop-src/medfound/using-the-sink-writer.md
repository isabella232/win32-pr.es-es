---
description: Uso del escritor de receptores
ms.assetid: BE89E2E0-711F-4BD5-BB86-AA4CCA2D3E7F
title: Uso del escritor de receptores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0585f52276e280d548e5180afc945ef99b046a7b6cd20c044c0e2262da3813b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012245"
---
# <a name="using-the-sink-writer"></a>Uso del escritor de receptores

## <a name="overview"></a>Información general

### <a name="file-container-types"></a>Tipos de contenedor de archivos

El escritor de receptores tiene compatibilidad integrada con varios tipos de contenedor de archivos. Para obtener una lista completa, vea [MF \_ TRANSCODE \_ CONTAINERTYPE](mf-transcode-containertype.md). Puede admitir tipos de contenedor adicionales escribiendo un receptor [de medios personalizado.](media-sinks.md) El contenedor de archivos se especifica cuando se crea una nueva instancia del escritor de receptores.

### <a name="stream-formats"></a>Formatos de secuencia

Para cada secuencia, la aplicación debe especificar lo siguiente.

-   El *formato de entrada* es el formato que la aplicación envía al escritor receptor.
-   El *formato de* salida es el formato que se escribirá en el archivo.

Los formatos de entrada y salida se pueden comprimir o descomprimir. El escritor de receptores admite las siguientes combinaciones:

-   Entrada sin comprimir con salida comprimida. Este es el caso típico y se usa para escenarios de codificación o transcodificación. Debe Microsoft Media Foundation codificador que acepte el tipo de entrada y se codifica en el tipo de salida.
-   Entrada comprimida con salida idéntica. Use esta combinación para volver a experienciar un archivo sin transcodificación.
-   Entrada sin comprimir con una salida idéntica. Use esta combinación para escribir audio o vídeo sin comprimir en un contenedor de archivos.

El sistema de escritura del receptor no admite el cambio de tamaño de vídeo, la conversión de velocidad de fotogramas ni el remuestreo de audio, a menos que el codificador las proporciona. De lo contrario, la aplicación puede usar [procesadores de señal digital](windowsmediadigitalsignalprocessors.md) para convertir los datos de entrada, antes de enviar los datos a

## <a name="creating-the-sink-writer"></a>Creación del escritor de receptores

Hay dos funciones que crean el escritor de receptores:

-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) toma la dirección URL de un archivo de salida o un puntero a una secuencia de bytes. Esta función crea internamente el receptor multimedia.
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) toma un puntero a un receptor multimedia que ya ha creado la aplicación.

Si usa uno de los receptores multimedia integrados, es preferible la función [**MFCreateSinkWriterFromURL,**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) ya que el autor de la llamada no necesita configurar el receptor multimedia.

El [**método MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) proporciona varias opciones para especificar el tipo de contenedor de archivos. En el caso más sencillo, la función usa la extensión de nombre de archivo en la dirección URL para seleccionar el contenedor de archivos. Para obtener más información, consulte la página de referencia de función.

Por ejemplo, el código siguiente especifica el nombre de archivo "output.wmv" para la dirección URL. En función de la extensión de nombre de archivo, el escritor de receptores cargará el receptor de medios [de ASF](asf-media-sinks.md) para crear un archivo de formato de sistemas avanzados (ASF).


```C++
    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);
```



En el caso de [**MFCreateSinkWriterFromMediaSink,**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)el tipo de archivo viene determinado por el receptor de medios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escritor de receptores](sink-writer.md)
</dt> </dl>

 

 



