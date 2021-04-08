---
description: .
ms.assetid: BE89E2E0-711F-4BD5-BB86-AA4CCA2D3E7F
title: Uso del escritor de receptor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46157eae6fe851468515f9d9653adb33918ebb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001581"
---
# <a name="using-the-sink-writer"></a>Uso del escritor de receptor

## <a name="overview"></a>Información general

### <a name="file-container-types"></a>Tipos de contenedor de archivos

El escritor de receptores tiene compatibilidad integrada con varios tipos de contenedor de archivos. Para obtener una lista completa, consulte [MF \_ Transcode \_ CONTAINERTYPE](mf-transcode-containertype.md). Puede admitir tipos de contenedor adicionales escribiendo un receptor de [multimedia](media-sinks.md)personalizado. El contenedor de archivos se especifica cuando se crea una nueva instancia del escritor del receptor.

### <a name="stream-formats"></a>Formatos de secuencia

Para cada flujo, la aplicación debe especificar lo siguiente.

-   El *formato de entrada* es el formato que la aplicación envía al escritor del receptor.
-   El *formato de salida* es el formato que se escribirá en el archivo.

Los formatos de entrada y salida se pueden comprimir o descomprimir. El escritor del receptor admite las siguientes combinaciones:

-   Entrada sin comprimir con salida comprimida. Este es el caso típico y se usa para codificar o transcodificar escenarios. Un codificador Microsoft Media Foundation debe estar disponible que acepte el tipo de entrada y codifique en el tipo de salida.
-   Entrada comprimida con salida idéntica. Use esta combinación para Remux un archivo sin transcodificar.
-   Entrada sin comprimir con salida idéntica. Use esta combinación para escribir audio sin comprimir o vídeo en un contenedor de archivos.

El escritor del receptor no admite el cambio de tamaño de vídeo, la conversión de velocidad de fotogramas o el remuestreo de audio, a menos que el codificador proporcione estas funciones. De lo contrario, la aplicación puede usar [procesadores de señal digital](windowsmediadigitalsignalprocessors.md) para convertir los datos de entrada, antes de enviar los datos al

## <a name="creating-the-sink-writer"></a>Creación del escritor de receptor

Hay dos funciones que crean el escritor del receptor:

-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) toma la dirección URL de un archivo de salida o un puntero a una secuencia de bytes. Esta función crea el receptor de medios internamente.
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) toma un puntero a un receptor de medios que ya ha creado la aplicación.

Si usa uno de los receptores de medios integrados, es preferible usar la función [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) , ya que el autor de la llamada no necesita configurar el receptor de medios.

El método [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) proporciona varias opciones para especificar el tipo de contenedor de archivos. En el caso más simple, la función usa la extensión de nombre de archivo en la dirección URL para seleccionar el contenedor de archivos. Para obtener más información, consulte la página de referencia de funciones.

Por ejemplo, el código siguiente especifica el nombre de archivo "Output. WMV" de la dirección URL. En función de la extensión de nombre de archivo, el escritor de receptores cargará el [receptor de medios ASF](asf-media-sinks.md) para crear un archivo de formato de sistema avanzado (ASF).


```C++
    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);
```



En el caso de [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink), el tipo de archivo viene determinado por el receptor de medios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escritor de receptor](sink-writer.md)
</dt> </dl>

 

 



