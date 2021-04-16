---
title: Para usar la selección de flujo manual
description: Para usar la selección de flujo manual
ms.assetid: 49ec283f-670a-4a0e-9477-c60a80919a1e
keywords:
- Advanced Systems Format (ASF), selección de secuencias manual
- ASF (formato de sistemas avanzados), selección de flujo manual
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Advanced Systems Format (ASF), selección de secuencias
- ASF (formato de sistemas avanzados), selección de secuencias
- Advanced Systems Format (ASF), exclusión mutua
- ASF (formato de sistemas avanzados), exclusión mutua
- lectores asincrónicos, selección de secuencias manual
- lectores asincrónicos, selección de secuencias
- flujos, selección manual
- exclusión mutua, selección de secuencia manual
- flujos, lectores asincrónicos
- exclusión mutua, lectores asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87c493bc8f41bc2a03ba15832ed402939adbeff
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695554"
---
# <a name="to-use-manual-stream-selection"></a>Para usar la selección de flujo manual

Al entregar ejemplos sin comprimir con el objeto lector, solo puede entregarlos por número de salida. En el caso de las secuencias mutuamente excluyentes, esto significa que solo se pueden recibir muestras de un flujo en la exclusión mutua a la vez. El proceso de elección de la secuencia mutuamente excluyente que se va a proporcionar se denomina selección de flujo.

Para la exclusión mutua de velocidad de bits, el lector realiza las selecciones de transmisión automáticamente en función de las condiciones del equipo host en la reproducción. Para otros tipos de exclusión mutua, el lector entregará muestras de la secuencia predeterminada a menos que seleccione manualmente otro flujo. También puede haber instancias si desea seleccionar una secuencia manualmente desde una exclusión mutua de velocidad de bits.

La selección de secuencias manual está activada o desactivada para todo el archivo. Si un archivo contiene una exclusión mutua de velocidad de bits y algún otro tipo de exclusión mutua, debe seleccionar manualmente las secuencias basadas en la velocidad de bits.

Para seleccionar manualmente una secuencia mutuamente excluyente, debe realizar los siguientes pasos.

1.  Recupere un puntero a la interfaz [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) del objeto lector llamando a **IWMReader:: QueryInterface**.
2.  Habilite la selección de flujo manual llamando a [**IWMReaderAdvanced:: SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).
3.  Para averiguar si una secuencia determinada está seleccionada, llame a [**IWMReaderAdvanced:: GetStreamSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected). Debe pasar un puntero a una variable del tipo de enumeración de la [**\_ \_ selección de flujo WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) . Cuando se devuelve la llamada, el valor de la variable describe el tipo de selección actual de la secuencia.
4.  Para seleccionar un flujo, llame a [**IWMReaderAdvanced:: SetStreamsSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected). Este método permite especificar varias secuencias al mismo tiempo para la conmutación de flujos sincronizada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Leer archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




