---
title: Para buscar por número de marco mediante el lector asincrónico
description: Para buscar por número de marco mediante el lector asincrónico
ms.assetid: faab6344-3afc-47ff-9107-d2ce36c0a2b8
keywords:
- Advanced Systems Format (ASF), búsqueda por números de fotogramas
- ASF (formato de sistemas avanzados), búsqueda por números de fotogramas
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- lectores asincrónicos, búsqueda por números de fotogramas
- secuencias de vídeo, búsqueda por números de fotogramas
- secuencias de vídeo, lectores asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 169f5e1ac1e6034bc1db6f610e80af50dd3a0215
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077299"
---
# <a name="to-seek-by-frame-number-using-the-asynchronous-reader"></a>Para buscar por número de marco mediante el lector asincrónico

El objeto lector asincrónico se puede usar para buscar los números de fotogramas de las secuencias de vídeo en un archivo ASF. Para usar búsquedas basadas en marcos, el archivo cargado en el lector debe estar indexado por marco. Cada flujo de vídeo individual se puede indexar. Para determinar si un flujo se ha indizado mediante Frame, puede comprobar el \_ atributo g wszWMNumberOfFrames en el encabezado del archivo llamando a [**IWMHeaderInfo:: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).

Para buscar datos en un archivo ASF por número de marco mediante el lector asincrónico, realice los pasos siguientes.

1.  Obtenga un puntero a la interfaz [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) del objeto lector llamando a **IWMReader:: QueryInterface**.
2.  Establezca el número de fotograma inicial y la duración mediante una llamada a [**IWMReaderAdvanced3:: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition). Debe especificar el número de secuencia de una secuencia de vídeo indexada por fotogramas. El lector sincronizará el resto de los resultados con el tiempo de presentación del marco especificado de la secuencia especificada y comenzará a entregar ejemplos de salida.
3.  Controle los ejemplos como lo haría normalmente en su implementación del método **IWMReaderCallback::** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Leer archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Leer metadatos en la reproducción**](reading-metadata-at-playback.md)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> </dl>

 

 




