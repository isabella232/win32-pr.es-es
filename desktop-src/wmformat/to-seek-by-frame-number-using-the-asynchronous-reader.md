---
title: Para buscar por número de fotograma mediante el lector asincrónico
description: Para buscar por número de fotograma mediante el lector asincrónico
ms.assetid: faab6344-3afc-47ff-9107-d2ce36c0a2b8
keywords:
- Formato de sistemas avanzados (ASF), búsqueda por números de fotograma
- ASF (formato de sistemas avanzados), búsqueda por números de fotograma
- Formato de sistemas avanzados (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- lectores asincrónicos, buscando por números de fotograma
- secuencias de vídeo, búsquedas por números de fotograma
- secuencias de vídeo, lectores asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 169f5e1ac1e6034bc1db6f610e80af50dd3a0215
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360584"
---
# <a name="to-seek-by-frame-number-using-the-asynchronous-reader"></a>Para buscar por número de fotograma mediante el lector asincrónico

El objeto de lector asincrónico se puede usar para buscar los números de fotogramas de las secuencias de vídeo en un archivo ASF. Para usar búsquedas basadas en fotogramas, el archivo cargado en el lector se debe indexar por fotograma. Cada secuencia de vídeo individual se puede indexar. Para determinar si una secuencia se ha indexado por marco, puede comprobar el atributo g wszWMNumberOfFrames en el encabezado del archivo llamando a \_ [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).

Para buscar datos en un archivo ASF por número de fotograma mediante el lector asincrónico, realice los pasos siguientes.

1.  Obtenga un puntero a [**la interfaz IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) del objeto lector llamando a **IWMReader::QueryInterface**.
2.  Establezca el número de fotograma inicial y la duración llamando [**a IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition). Debe especificar el número de secuencia de una secuencia de vídeo indizada por fotogramas. El lector sincronizará el resto de las salidas con el tiempo de presentación del marco especificado de la secuencia especificada y comenzará a entregar ejemplos de salida.
3.  Controle los ejemplos como lo haría normalmente en la implementación del **método IWMReaderCallback::OnSample.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Lectura de archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lectura de metadatos durante la reproducción**](reading-metadata-at-playback.md)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> </dl>

 

 




