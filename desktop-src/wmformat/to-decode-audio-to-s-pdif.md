---
title: Para descodificar audio en S/PDIF
description: Para descodificar audio en S/PDIF
ms.assetid: b56c2d0a-a7c6-44f8-832a-bbbe7ae053e6
keywords:
- Windows SDK de formato multimedia, codificación de audio en S/PDIF
- Windows Sdk de formato multimedia, formato de interconexión digital de Sony/Digital Digital Desconecto (S/PDIF)
- Formato de sistemas avanzados (ASF), codificación de audio en S/PDIF
- ASF (formato de sistemas avanzados), codificación de audio en S/PDIF
- Formato de sistemas avanzados (ASF), formato de interconexión digital de Sony/Unix (S/PDIF)
- ASF (formato de sistemas avanzados), formato de interconexión digital de Sony/Unix (S/PDIF)
- Formato de interconexión digital (S/PDIF) de Sonái/Resalte, codificación de audio
- S/PDIF (formato de interconexión digital Descoding)
- decoding audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84bd4fdbafd5685882f34b698c0745b998b6cee2e63514041db17fed2195346c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845593"
---
# <a name="to-decode-audio-to-spdif"></a>Para descodificar audio en S/PDIF

El audio codificado con el códec Windows media audio 9 Professional se puede descodificar al formato de interconexión digital de Audio Multimedia 9 (S/PDIF). Para generar la salida de S/PDIF, realice los pasos siguientes:

1.  Abra un archivo que contenga una secuencia Windows Media Audio Professional 9 mediante una llamada al método [**IWMReader::Open.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
2.  Identifique el número de salida de la secuencia que desea. Para obtener más información, vea [Para identificar números de salida.](to-identify-output-numbers.md)
3.  Llame al [**método IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) para configurar la salida de S/PDIF. Use g \_ wszEnableWMAProSPDIFOutput como nombre de la configuración. El tipo de datos es **WMT \_ TYPE \_ BOOL;** establezca el valor en **TRUE** para habilitar la salida de S/PDIF.
4.  Obtenga la interfaz de propiedades de salida ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) del formato de salida deseado llamando al [**método IWMReader::GetOutputFormat.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) Para obtener más información sobre cómo enumerar los formatos de salida, vea [Asignación de formatos de salida.](assigning-output-formats.md)
5.  Establezca el formato de salida llamando al [**método IWMReader::SetOutputProps.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) Pase un puntero a la **interfaz IWMOutputMediaProps** obtenida en el paso 4.
6.  Realice cualquier otro cambio de configuración y comience la reproducción.

> [!Note]  
> Puede realizar los pasos anteriores en el lector sincrónico mediante los métodos correspondientes de la [**interfaz IWMSyncReader.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)

 

El código de ejemplo siguiente muestra cómo establecer una secuencia de audio para generar audio como datos S/PDIF. Esta función supone que ya se ha cargado un archivo en el lector y que se ha identificado el número de salida. Para obtener más información sobre el uso de este código, vea [Usar los ejemplos de código](using-the-code-examples.md).


```C++
HRESULT SetSPDIF(DWORD dwOutputNum, IWMReader* pReader)
{
    HRESULT hr = S_OK;

    IWMReaderAdvanced2*  pReaderAdv   = NULL;
    IWMOutputMediaProps* pOutputProps = NULL; 

    BOOL fValue = TRUE;

    // Get the advanced reader interface.
    hr = pReader->QueryInterface(IID_IWMReaderAdvanced2,
                                 (void**)&pReaderAdv);
    GOTO_EXIT_IF_FAILED(hr);

    // Set S/PDIF output.
    hr = pReaderAdv->SetOutputSetting(dwOutputNum, 
                                      g_wszEnableWMAProSPDIFOutput, 
                                      WMT_TYPE_BOOL, 
                                      (BYTE*)&fValue, 
                                      sizeof(BOOL));
    GOTO_EXIT_IF_FAILED(hr);

    // Get the first output format for the stream.
    // NOTE: You could also enumerate the available output formats
    // and pick one to use.

    hr = pReader->GetOutputFormat(dwOutputNum, 0, &pOutputProps);
    GOTO_EXIT_IF_FAILED(hr);

    // Set the output properties back on the reader.
    hr = pReader->SetOutputProps(dwOutputNum, pOutputProps);

Exit:
    SAFE_RELEASE(pReaderAdv);
    SAFE_RELEASE(pOutputProps);

    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Temas avanzados**](advanced-topics.md)
</dt> <dt>

[**Lectura de archivos ASF**](reading-asf-files.md)
</dt> <dt>

[**IWMReader (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMReaderAdvanced2 (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**IWMSyncReader (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> </dl>

 

 




