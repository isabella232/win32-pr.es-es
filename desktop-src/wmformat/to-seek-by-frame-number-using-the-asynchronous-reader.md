---
title: Para buscar por número de fotograma mediante el lector asincrónico
description: Para buscar por número de fotograma mediante el lector asincrónico
ms.assetid: faab6344-3afc-47ff-9107-d2ce36c0a2b8
keywords:
- Formato de sistemas avanzados (ASF), búsqueda por números de fotograma
- ASF (formato de sistemas avanzados), búsqueda por números de fotograma
- Formato de sistemas avanzados (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- lectores asincrónicos, búsqueda por números de fotograma
- secuencias de vídeo, búsqueda por números de fotograma
- secuencias de vídeo, lectores asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e218384b1a27bb3240ac74ad9af6d8298945bb57dfaf635531cb4cbb9aaa9611
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118432618"
---
# <a name="to-seek-by-frame-number-using-the-asynchronous-reader"></a>Para buscar por número de fotograma mediante el lector asincrónico

El objeto de lector asincrónico se puede usar para buscar los números de fotogramas de las secuencias de vídeo en un archivo ASF. Para usar la búsqueda basada en fotogramas, el archivo cargado en el lector se debe indexar por fotograma. Cada secuencia de vídeo individual se puede indexar. Para determinar si una secuencia se ha indexado por fotograma, puede comprobar el atributo g wszWMNumberOfFrames en el encabezado del archivo llamando a \_ [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).

Para buscar datos en un archivo ASF por número de fotograma mediante el lector asincrónico, realice los pasos siguientes.

1.  Obtenga un puntero a la [**interfaz IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) del objeto reader llamando a **IWMReader::QueryInterface**.
2.  Establezca el número de fotograma inicial y la duración llamando a [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition). Debe especificar el número de secuencia de una secuencia de vídeo indizada por fotogramas. El lector sincronizará el resto de las salidas con el tiempo de presentación del marco especificado de la secuencia especificada y comenzará a entregar ejemplos de salida.
3.  Controle los ejemplos como lo haría normalmente en la implementación del **método IWMReaderCallback::OnSample.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Leer archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Leer metadatos en reproducción**](reading-metadata-at-playback.md)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> </dl>

 

 




