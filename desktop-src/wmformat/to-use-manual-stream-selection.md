---
title: Para usar la selección manual de secuencias
description: Para usar la selección manual de secuencias
ms.assetid: 49ec283f-670a-4a0e-9477-c60a80919a1e
keywords:
- Formato de sistemas avanzados (ASF), selección manual de secuencias
- ASF (formato de sistemas avanzados), selección manual de secuencias
- Formato de sistemas avanzados (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Formato de sistemas avanzados (ASF), selección de secuencias
- ASF (formato de sistemas avanzados), selección de secuencias
- Formato de sistemas avanzados (ASF), exclusión mutua
- ASF (formato de sistemas avanzados), exclusión mutua
- lectores asincrónicos, selección manual de secuencias
- lectores asincrónicos, selección de secuencias
- streams,manual selection
- exclusión mutua, selección manual de flujos
- streams,asynchronous readers
- exclusión mutua, lectores asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87c493bc8f41bc2a03ba15832ed402939adbeff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256208"
---
# <a name="to-use-manual-stream-selection"></a>Para usar la selección manual de secuencias

Al entregar muestras sin comprimir con el objeto lector, solo puede entregarlas por número de salida. En el caso de secuencias mutuamente excluyentes, esto significa que solo puede recibir muestras de una secuencia en la exclusión mutua a la vez. El proceso de elección de la secuencia mutuamente excluyente que se va a entregar se denomina selección de secuencia.

Para la exclusión mutua de velocidad de bits, el lector realiza selecciones de secuencias automáticamente en función de las condiciones del equipo host durante la reproducción. Para otros tipos de exclusión mutua, el lector entregará ejemplos de la secuencia predeterminada a menos que seleccione manualmente otra secuencia. También puede haber instancias cuando quiera seleccionar manualmente una secuencia de una exclusión mutua de velocidad de bits.

La selección manual de secuencias está on o off para todo el archivo. Si un archivo contiene la exclusión mutua de velocidad de bits y algún otro tipo de exclusión mutua, debe seleccionar manualmente las secuencias basadas en velocidad de bits.

Para seleccionar manualmente una secuencia mutuamente excluyente, debe realizar los pasos siguientes.

1.  Recupere un puntero a la [**interfaz IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) del objeto reader llamando a **IWMReader::QueryInterface**.
2.  Habilite la selección manual de secuencias llamando a [**IWMReaderAdvanced::SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).
3.  Para averiguar si se selecciona una secuencia determinada, llame a [**IWMReaderAdvanced::GetStreamSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected). Debe pasar un puntero a una variable del tipo de [**enumeración WMT \_ STREAM \_ SELECTION.**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) Cuando se devuelve la llamada, el valor de la variable describirá el tipo de selección actual de la secuencia.
4.  Para seleccionar una secuencia, llame a [**IWMReaderAdvanced::SetStreamsSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected). Este método permite especificar varias secuencias al mismo tiempo para el cambio de flujo sincronizado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Leer archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




