---
title: Para implementar la devolución de llamada de ejemplo
description: Para implementar la devolución de llamada de ejemplo
ms.assetid: 83bce8ee-6ce8-4079-9c87-2314824b1946
keywords:
- Advanced Systems Format (ASF), implementación de la devolución de llamada en estado
- ASF (formato de sistemas avanzados), implementación de la devolución de llamada en estado
- Advanced Systems Format (ASF), alstatus callback
- ASF (formato de sistemas avanzados), devolución de llamada en estado
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- lectores asincrónicos, implementar la devolución de llamada en estado
- Método de devolución de llamada en estado, implementar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f19e81df5ee4769e1353c299a14626cb1a9aed
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104358766"
---
# <a name="to-implement-the-onsample-callback"></a>Para implementar la devolución de llamada de ejemplo

El lector asincrónico proporciona ejemplos a la aplicación de control en el orden en tiempo de presentación realizando llamadas al método de devolución de llamada [**IWMReaderCallback::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) MyMethod. Al crear una aplicación mediante el lector asincrónico, debe implementar el **ejemplo** para tratar con ejemplos sin comprimir. Normalmente, las funciones o los métodos creados para representar el contenido se llamarán desde en el **ejemplo**.

La implementación típica de la devolución de llamada de **ejemplo** incluye los pasos siguientes.

1.  Recupere la ubicación y el tamaño del búfer que contiene el ejemplo llamando a [**INSSBuffer:: GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) en el búfer pasado como *pSample*.
2.  Bifurcar la lógica según el número de salida. El número de salida se pasa a la **muestra** como *dwOutputNumber*.
3.  Incluya la lógica de representación para cada número de salida que desee admitir. Si está representando ejemplos de varias salidas, puede que necesite sincronizar la representación.

Las aplicaciones que proporcionan ejemplos comprimidos de archivos ASF deben implementar el método de devolución de llamada [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) . **OnStreamSample** funciona de forma casi idéntica al **ejemplo**, salvo que recibe muestras comprimidas por número de secuencia en lugar de muestras sin comprimir por número de salida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)
</dt> <dt>

[**Interfaz IWMReaderCallbackAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**Leer archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Usar los métodos de devolución de llamada**](using-the-callback-methods.md)
</dt> </dl>

 

 




