---
title: Para implementar la devolución de llamada OnSample
description: Para implementar la devolución de llamada OnSample
ms.assetid: 83bce8ee-6ce8-4079-9c87-2314824b1946
keywords:
- Formato de sistemas avanzados (ASF), implementación de devolución de llamada de OnStatus
- ASF (formato de sistemas avanzados), implementación de la devolución de llamada OnStatus
- Formato de sistemas avanzados (ASF), devolución de llamada de OnStatus
- ASF (formato de sistemas avanzados), devolución de llamada de OnStatus
- Formato de sistemas avanzados (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- lectores asincrónicos, implementación de devolución de llamada de OnStatus
- Método de devolución de llamada OnStatus, implementación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00523ae28ec14feefb8249ff86a2b1600629c84cb245eb627b59b619a28a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027293"
---
# <a name="to-implement-the-onsample-callback"></a>Para implementar la devolución de llamada OnSample

El lector asincrónico entrega ejemplos a la aplicación de control en tiempo de presentación mediante llamadas al método de devolución de llamada [**IWMReaderCallback::OnSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) Al crear una aplicación mediante el lector asincrónico, debe implementar **OnSample** para tratar con ejemplos sin comprimir. Normalmente, se llamará a funciones o métodos creados para representar contenido desde **OnSample.**

La implementación típica de la **devolución de llamada OnSample** incluye los pasos siguientes.

1.  Recupere la ubicación y el tamaño del búfer que contiene el ejemplo llamando a [**INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) en el búfer pasado *como pSample*.
2.  Bifurca la lógica en función del número de salida. El número de salida se pasa a **OnSample** como *dwOutputNumber*.
3.  Incluya la lógica de representación para cada número de salida que desee admitir. Si va a representar ejemplos de varias salidas, es posible que tenga que sincronizar la representación.

Las aplicaciones que entregan ejemplos comprimidos de archivos ASF deben implementar el método de devolución de llamada [**IWMReaderCallbackAdvanced::OnStreamSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) **OnStreamSample funciona** casi de forma idéntica a **OnSample,** salvo que recibe muestras comprimidas por número de secuencia en lugar de muestras sin comprimir por número de salida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMReaderCallback (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)
</dt> <dt>

[**IWMReaderCallbackAdvanced (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**Lectura de archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Usar los métodos de devolución de llamada**](using-the-callback-methods.md)
</dt> </dl>

 

 




