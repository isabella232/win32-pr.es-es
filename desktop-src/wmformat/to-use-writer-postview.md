---
title: Para usar la vista posterior del escritor
description: Para usar la vista posterior del escritor
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- Formato de sistemas avanzados (ASF), vista posterior del escritor
- ASF (formato de sistemas avanzados), vista posterior del escritor
- Formato de sistemas avanzados (ASF), vista posterior
- ASF (formato de sistemas avanzados), vista posterior
- vista posterior del escritor
- vista posterior
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb3c1c83ebd38ff04c2022e529693d3d43b8b35
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247233"
---
# <a name="to-use-writer-postview"></a>Para usar la vista posterior del escritor

El objeto de escritor proporciona funcionalidades de visualización posterior para que pueda comprobar el contenido escrito sin tener que configurar el objeto de lector. El objeto de escritor no admite la vista posterior para el contenido de audio.

El postviewer de escritor funciona de la misma manera que el objeto de lector asincrónico, solo con menos características. Para obtener información detallada sobre la lectura de medios digitales, vea [Lectura de archivos ASF.](reading-asf-files.md)

Para implementar el postviewer, realice los pasos siguientes.

1.  Implemente la [**devolución de llamada IWMWriterPostViewCallback::OnPostViewSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) Este método es esencialmente el mismo que [**IWMReaderCallback::OnSample,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) salvo que especifica números de flujo en lugar de salidas.
2.  Configure para escribir como de costumbre.
3.  Obtenga un puntero a la [**interfaz IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) del objeto de escritor llamando a **IWMWriter::QueryInterface**.
4.  Establezca la devolución de llamada del postviewer que se usará mediante una llamada [**a IWMWriterPostView::SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).
5.  Para cada secuencia para la que quiera recibir ejemplos de vista posterior, llame a [**IWMWriterPostView::SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples). Puede comprobar si una secuencia está establecida para recibir ejemplos de vista post mediante una llamada a [**IWMWriterPostView::GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).
6.  Puede manipular los formatos de ejemplo, como lo haría con los formatos de salida en el objeto lector o en el objeto de lector sincrónico.
7.  Cuando empiece a escribir el archivo, comenzará a recibir ejemplos en la implementación del método de devolución de llamada **OnPostViewSample.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMWriterPostViewCallback (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




