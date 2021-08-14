---
title: Para buscar por número de fotograma mediante el lector sincrónico
description: Para buscar por número de fotograma mediante el lector sincrónico
ms.assetid: 755e0124-de57-4699-af8e-c594567b5523
keywords:
- Formato de sistemas avanzados (ASF), búsqueda por números de fotograma
- ASF (formato de sistemas avanzados), búsqueda por números de fotograma
- Formato de sistemas avanzados (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- lectores sincrónicos, búsqueda por números de fotograma
- secuencias de vídeo, búsqueda por números de fotograma
- secuencias de vídeo, lectores sincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1b2da615f23e5c1d17046f08310d0aeda49200d5c4ba9fba890d7ba4951e0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699116"
---
# <a name="to-seek-by-frame-number-using-the-synchronous-reader"></a>Para buscar por número de fotograma mediante el lector sincrónico

Para buscar datos por número de fotograma mediante el lector sincrónico, especifique un intervalo para la reproducción. Un intervalo se define mediante un número de fotograma inicial en una secuencia de vídeo específica y un número de fotogramas para reproducir.

Para buscar datos en un archivo ASF por número de fotograma mediante el lector sincrónico, realice los pasos siguientes.

1.  Establezca el número de fotogramas inicial y el número de fotogramas que se leerán para la entrega de ejemplo mediante una llamada a [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe). Debe especificar el número de secuencia de una secuencia de vídeo indizada por fotogramas. El lector sincronizará el resto de las salidas con el tiempo de presentación del marco especificado de la secuencia especificada y comenzará a entregar ejemplos de salida.
2.  Comience a recuperar ejemplos con llamadas a [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Continúe como lo haría normalmente con el lector sincrónico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMSyncReader (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lectura de archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




