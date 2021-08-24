---
title: Para buscar marcadores
description: Para buscar marcadores
ms.assetid: 2d5efebf-dcbd-4fb8-933e-cc6d3a99adf8
keywords:
- Formato de sistemas avanzados (ASF), buscar marcadores
- ASF (formato de sistemas avanzados), buscar marcadores
- Formato de sistemas avanzados (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Formato de sistemas avanzados (ASF), marcadores
- ASF (formato de sistemas avanzados),marcadores
- lectores asincrónicos, buscar marcadores
- lectores asincrónicos, marcadores
- marcadores, buscar
- marcadores, lectores asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3361546f4087e0c2104809435d9d75e8711560ec4f3c55855d14b05ef4dfb8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807355"
---
# <a name="to-seek-to-markers"></a>Para buscar marcadores

Un marcador es una ubicación con nombre en un archivo ASF. Solo puede iniciar la reproducción desde la ubicación de un marcador mediante el lector asincrónico. Puede comenzar la reproducción en un marcador siguiendo estos pasos.

1.  Llame **a IWMReader::QueryInterface** para obtener un puntero a la [**interfaz IWMHeaderInfo.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
2.  Recupere el número total de marcadores del archivo llamando a [**IWMHeaderInfo::GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount).
3.  Recorrer en bucle los marcadores mediante el recuento de marcadores recuperado en el paso 2. Recupere el nombre y la hora de cada marcador mediante una [**llamada a IWMHeaderInfo::GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) para cada uno. Guarde el índice del marcador deseado.
4.  Llame **a IWMReader::QueryInterface para** obtener un puntero a la interfaz [**IWMReaderAdvanced2.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
5.  Especifique el marcador en el que se va a iniciar la reproducción llamando [**a IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker). Debe pasar el índice del marcador deseado, que guardó en el paso 3.
6.  Controle los ejemplos como lo haría normalmente en la implementación del [**método IWMReaderCallback::OnSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Marcadores**](markers.md)
</dt> <dt>

[**Leer archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> </dl>

 

 




