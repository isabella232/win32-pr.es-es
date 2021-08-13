---
title: Para entregar ejemplos comprimidos con el lector asincrónico
description: Para entregar ejemplos comprimidos con el lector asincrónico
ms.assetid: 488baa3c-8863-4afc-89b2-fe55823e5db9
keywords:
- Formato de sistemas avanzados (ASF), entrega de ejemplos comprimidos
- ASF (formato de sistemas avanzados), entrega de ejemplos comprimidos
- Formato de sistemas avanzados (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Formato de sistemas avanzados (ASF), ejemplos comprimidos
- ASF (formato de sistemas avanzados), ejemplos comprimidos
- lectores asincrónicos, entrega de ejemplos comprimidos
- lectores asincrónicos, ejemplos comprimidos
- ejemplos comprimidos, entrega
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9199fb1deefdd3c7408bc9039639bd723b06c380c03d249c9c71a1d792c1e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699935"
---
# <a name="to-deliver-compressed-samples-with-the-asynchronous-reader"></a>Para entregar ejemplos comprimidos con el lector asincrónico

El lector asincrónico puede entregar muestras comprimidas de secuencias en archivos ASF. Las aplicaciones suelen entregar muestras comprimidas al copiar una secuencia de un archivo a otro. No es aconsejable volver a comprimir los datos que se han reconstruido a partir de una secuencia comprimida, ya que los datos se pierden en el proceso de codificación. Los medios digitales que se han comprimido más de una vez tendrán una disminución notable de la calidad.

El SDK Windows media format no proporciona ningún método para la decodificación de datos una vez extraídos de un archivo ASF. Si recibe ejemplos comprimidos y posteriormente quiere descomprimirlos, tendrá que proporcionar su propio código para hacerlo. Una manera de evitar esta limitación es escribir las muestras comprimidas en un nuevo archivo ASF y, a continuación, volver a leerlas en muestras normales sin comprimir.

Para recibir muestras comprimidas con el lector asincrónico, realice los pasos siguientes.

1.  Implemente la [**devolución de llamada IWMReaderCallbackAdvanced::OnStreamSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) Esta devolución de llamada es básicamente idéntica en función a [**IWMReaderCallback::OnSample,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) salvo que entrega muestras por número de secuencia y las muestras siguen comprimidas.
2.  Antes de iniciar la reproducción, obtenga un puntero a la [**interfaz IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) del objeto reader llamando a **IWMReader::QueryInterface**.
3.  Configure el lector para entregar ejemplos comprimidos para la secuencia deseada llamando a [**IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples).
4.  Repita el paso 3 para cada secuencia para la que se desee la entrega de muestras comprimidas.

> [!Note]  
> Los flujos de imágenes no son válidos para la entrega de secuencias comprimidas. Si copia una secuencia de imágenes de un archivo a otro, no funcionará en el nuevo archivo. Para copiar una secuencia de imagen de un archivo a otro, recupere los ejemplos de secuencia de imágenes por número de salida e incluyéndolos en el nuevo archivo como si incluyese una nueva secuencia de imágenes.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMReaderCallbackAdvanced (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**Leer archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




