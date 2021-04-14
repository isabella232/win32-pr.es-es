---
title: Para usar la vista previa del escritor
description: Para usar la vista previa del escritor
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- Advanced Systems Format (ASF), postview del escritor
- ASF (formato de sistemas avanzados), postview del escritor
- Advanced Systems Format (ASF), postview
- ASF (formato de sistemas avanzados), postview
- vista previa del escritor
- vista previa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb3c1c83ebd38ff04c2022e529693d3d43b8b35
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104533052"
---
# <a name="to-use-writer-postview"></a>Para usar la vista previa del escritor

El objeto escritor proporciona funciones de postview para que pueda comprobar el contenido escrito sin tener que configurar el objeto lector. El objeto de escritor no admite la postview para el contenido de audio.

El postvisor del escritor funciona de manera muy similar al objeto lector asincrónico, solo con menos características. Para obtener información detallada sobre cómo leer archivos multimedia digitales, consulte [lectura de archivos ASF](reading-asf-files.md).

Para implementar el postvisor, realice los pasos siguientes.

1.  Implemente la devolución de llamada [**IWMWriterPostViewCallback:: OnPostViewSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) . Este método es esencialmente el mismo que [**IWMReaderCallback::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) , salvo que especifica los números de secuencia en lugar de los resultados.
2.  Configure para escritura como de costumbre.
3.  Obtenga un puntero a la interfaz [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) del objeto de escritor llamando a **IWMWriter:: QueryInterface**.
4.  Establezca la devolución de llamada para que la use el postvisor mediante una llamada a [**IWMWriterPostView:: SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).
5.  Para cada secuencia para la que desea recibir ejemplos de postview, llame a [**IWMWriterPostView:: SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples). Puede comprobar si un flujo está configurado para recibir ejemplos de postview mediante una llamada a [**IWMWriterPostView:: GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).
6.  Puede manipular los formatos de ejemplo, del mismo modo que lo haría con los formatos de salida del objeto lector o del objeto lector sincrónico.
7.  Cuando empiece a escribir el archivo, comenzará a recibir ejemplos en su implementación del método de devolución de llamada **OnPostViewSample** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMWriterPostViewCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




