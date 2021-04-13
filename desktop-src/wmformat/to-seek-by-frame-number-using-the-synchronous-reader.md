---
title: Para buscar por número de marco mediante el lector sincrónico
description: Para buscar por número de marco mediante el lector sincrónico
ms.assetid: 755e0124-de57-4699-af8e-c594567b5523
keywords:
- Advanced Systems Format (ASF), búsqueda por números de fotogramas
- ASF (formato de sistemas avanzados), búsqueda por números de fotogramas
- Advanced Systems Format (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- lectores sincrónicos, búsquedas por números de fotogramas
- secuencias de vídeo, búsqueda por números de fotogramas
- secuencias de vídeo, lectores sincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c26711d2d839e47279e7e52a50f5dc82c6e81da
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358684"
---
# <a name="to-seek-by-frame-number-using-the-synchronous-reader"></a>Para buscar por número de marco mediante el lector sincrónico

Para buscar datos por número de marco mediante el lector sincrónico, especifique un intervalo para la reproducción. Un intervalo se define mediante un número de fotograma inicial en un flujo de vídeo específico y un número de fotogramas que se van a reproducir.

Para buscar datos en un archivo ASF por número de marco mediante el lector sincrónico, realice los pasos siguientes.

1.  Establezca el número de fotograma inicial y el número de fotogramas que se van a leer para la entrega de ejemplo llamando a [**IWMSyncReader:: SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe). Debe especificar el número de secuencia de una secuencia de vídeo indexada por fotogramas. El lector sincronizará el resto de los resultados con el tiempo de presentación del marco especificado de la secuencia especificada y comenzará a entregar ejemplos de salida.
2.  Comience a recuperar ejemplos con llamadas a [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Continúe como lo haría normalmente con el lector sincrónico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Leer archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




