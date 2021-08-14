---
title: Para usar la vista posterior del escritor
description: Para usar la vista posterior del escritor
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- Advanced Systems Format (ASF),writer postview
- ASF (formato de sistemas avanzados), vista posterior del escritor
- Formato de sistemas avanzados (ASF), vista posterior
- ASF (formato de sistemas avanzados), vistas posteriores
- vista posterior del escritor
- vista posterior
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7800f3ba50f9f1d61793a0d2ada2db0c03d6b88551ac1147e17872aa8e428c39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196409"
---
# <a name="to-use-writer-postview"></a>Para usar la vista posterior del escritor

El objeto de escritor proporciona funcionalidades de visualización posterior para que pueda comprobar el contenido escrito sin tener que configurar el objeto de lector. El objeto de escritor no admite la vista posterior para el contenido de audio.

El postviewer de escritor funciona de la misma manera que el objeto de lector asincrónico, solo con menos características. Para obtener información detallada sobre la lectura de medios digitales, vea [Lectura de archivos ASF.](reading-asf-files.md)

Para implementar el postviewer, realice los pasos siguientes.

1.  Implemente la [**devolución de llamada IWMWriterPostViewCallback::OnPostViewSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) Este método es básicamente el mismo que [**IWMReaderCallback::OnSample,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) salvo que especifica números de flujo en lugar de salidas.
2.  Configure para escribir como de costumbre.
3.  Obtenga un puntero a la [**interfaz IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) del objeto de escritor llamando a **IWMWriter::QueryInterface**.
4.  Establezca la devolución de llamada del postviewer que se usará mediante una llamada [**a IWMWriterPostView::SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).
5.  Para cada secuencia para la que quiera recibir ejemplos de vista posterior, llame a [**IWMWriterPostView::SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples). Puede comprobar si una secuencia está establecida para recibir ejemplos de vista posterior llamando a [**IWMWriterPostView::GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).
6.  Puede manipular los formatos de ejemplo, del mismo modo que lo haría con los formatos de salida en el objeto de lector o en el objeto de lector sincrónico.
7.  Cuando empiece a escribir el archivo, comenzará a recibir ejemplos en la implementación del método de devolución de llamada **OnPostViewSample.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMWriterPostViewCallback (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




