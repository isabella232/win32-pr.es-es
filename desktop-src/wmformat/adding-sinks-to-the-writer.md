---
title: Agregar receptores al escritor
description: Agregar receptores al escritor
ms.assetid: 714b84f0-5ad8-4e00-aa77-e866e65b43b0
keywords:
- Formato de sistemas avanzados (ASF), agregar receptores al escritor
- ASF (formato de sistemas avanzados), agregar receptores al escritor
- Formato de sistemas avanzados (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- Formato de sistemas avanzados (ASF), receptores de escritor
- ASF (formato de sistemas avanzados), receptores de escritor
- sinks,adding to the writer
- receptores de escritor, agregar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886a6630a02d1fea56ce387077484f173ddf4dd3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247412"
---
# <a name="adding-sinks-to-the-writer"></a>Agregar receptores al escritor

Los receptores de escritor son objetos independientes del escritor y deben agregarse al escritor que se va a usar. Si escribe en un archivo, simplemente puede llamar a [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename), que configurará automáticamente el receptor de archivos. De lo contrario, para agregar un receptor al escritor, llame al [**método IWMWriterAdvanced::AddSink.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) **AddSink** requiere un puntero a la [**interfaz IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) del receptor.

Cuando haya terminado de usar un receptor, debe cerrarlo llamando al método adecuado, en función del tipo de receptor, y, a continuación, quitarlo del escritor mediante una llamada a [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink).

En el código de ejemplo siguiente se muestra cómo crear un receptor de archivo de escritura y agregarlo al escritor. Para obtener más información sobre el uso de este código, vea [Usar los ejemplos de código](using-the-code-examples.md).


```C++
HRESULT AddFileSink(IWMWriterFileSink** ppFileSink, IWMWriter* pWriter)
{
    HRESULT hr = S_OK;
    IWMWriterSink*     pSinkBase       = NULL;
    IWMWriterAdvanced* pWriterAdvanced = NULL;

    hr = CreateWriterFileSink(ppFileSink);
    GOTO_EXIT_IF_FAILED(hr);

    hr = *ppFileSink->QueryInterface(IID_IWMWriterSink, 
                                     (void**) &pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced,
                                 (void**) &pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriterAdvanced->AddSink(pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

Exit:
    SAFE_RELEASE(pSinkBase);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Obtener mensajes de error de un receptor**](getting-error-messages-from-a-sink.md)
</dt> <dt>

[**IWMWriterAdvanced (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> </dl>

 

 




