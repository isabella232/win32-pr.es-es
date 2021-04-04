---
title: Para proporcionar ejemplos comprimidos con el lector asincrónico
description: Para proporcionar ejemplos comprimidos con el lector asincrónico
ms.assetid: 488baa3c-8863-4afc-89b2-fe55823e5db9
keywords:
- Advanced Systems Format (ASF), entrega de muestras comprimidas
- ASF (formato de sistemas avanzados), entrega de muestras comprimidas
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Advanced Systems Format (ASF), ejemplos comprimidos
- ASF (formato de sistemas avanzados), ejemplos comprimidos
- lectores asincrónicos, entrega de muestras comprimidas
- lectores asincrónicos, ejemplos comprimidos
- ejemplos comprimidos, entrega
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ce835075f5bd760014a3b1b776ba3627adb076
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788793"
---
# <a name="to-deliver-compressed-samples-with-the-asynchronous-reader"></a>Para proporcionar ejemplos comprimidos con el lector asincrónico

El lector asincrónico puede proporcionar ejemplos comprimidos de secuencias en archivos ASF. Normalmente, las aplicaciones proporcionan ejemplos comprimidos al copiar una secuencia de un archivo a otro. No es aconsejable volver a comprimir los datos que se han reconstruido a partir de un flujo comprimido, ya que los datos se pierden en el proceso de codificación. Los medios digitales que se han comprimido más de una vez tendrán una disminución apreciable de la calidad.

El SDK de Windows Media Format no proporciona ningún método para descodificar los datos una vez extraídos de un archivo ASF. Si recibe ejemplos comprimidos y posteriormente desea descomprimirlos, tendrá que proporcionar su propio código para hacerlo. Una manera de solucionar esta limitación es escribir los ejemplos comprimidos en un nuevo archivo ASF y, a continuación, volver a leerlos en ejemplos normales y sin comprimir.

Para recibir ejemplos comprimidos con el lector asincrónico, realice los pasos siguientes.

1.  Implemente la devolución de llamada [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) . Esta devolución de llamada es básicamente idéntica en función a [**IWMReaderCallback::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) en el ejemplo, salvo que proporciona muestras por número de secuencia y los ejemplos siguen estando comprimidos.
2.  Antes de iniciar la reproducción, obtenga un puntero a la interfaz [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) del objeto lector llamando a **IWMReader:: QueryInterface**.
3.  Configure el lector para proporcionar ejemplos comprimidos para el flujo deseado llamando a [**IWMReaderAdvanced:: SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples).
4.  Repita el paso 3 para cada flujo para el que desee la entrega de ejemplo comprimida.

> [!Note]  
> Los flujos de imagen no son válidos para la entrega de secuencias comprimidas. Si copia una secuencia de imágenes de un archivo a otro, no funcionará en el nuevo archivo. Para copiar un flujo de imagen de archivo a archivo, recupere los ejemplos de flujo de imagen por número de salida e inclúyalo en el nuevo archivo como si se incluira una nueva secuencia de imágenes.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMReaderCallbackAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**Leer archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




