---
title: Para descodificar el audio a S/PDIF
description: Para descodificar el audio a S/PDIF
ms.assetid: b56c2d0a-a7c6-44f8-832a-bbbe7ae053e6
keywords:
- SDK de Windows Media Format, descodificación de audio a S/PDIF
- Windows Media Format SDK, formato de interconexión digital de Sony/Philips (S/PDIF)
- Advanced Systems Format (ASF), descodificar audio para S/PDIF
- ASF (formato de sistemas avanzados), descodificación de audio a S/PDIF
- Formato de sistemas avanzados (ASF), formato de interconexión digital de Sony/Philips (S/PDIF)
- ASF (formato de sistemas avanzados), formato de interconexión digital de Sony/Philips (S/PDIF)
- Formato de interconexión digital de Sony/Philips (S/PDIF), descodificación de audio
- S/PDIF (formato Sony/Philips digital Interconnect), descodificar audio
- descodificación de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa063baa8e9a88c2fb7a4d9c67375965282167
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789225"
---
# <a name="to-decode-audio-to-spdif"></a>Para descodificar el audio a S/PDIF

El audio codificado con el códec Windows Media Audio 9 Professional se puede descodificar en formato de interconexión digital de Sony/Philips (S/PDIF). Para generar la salida S/PDIF, realice los pasos siguientes:

1.  Abra un archivo que contenga una secuencia Windows Media Audio 9 Professional llamando al método [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) .
2.  Identifique el número de salida de la secuencia que desee. Para obtener más información, consulte [para identificar los números de salida](to-identify-output-numbers.md).
3.  Llame al método [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) para configurar la salida S/PDIF. Use g \_ wszEnableWMAProSPDIFOutput para el nombre de la configuración. El tipo de datos es el **\_ tipo WMT \_ bool**; establezca el valor en **true** para habilitar la salida S/PDIF.
4.  Obtenga la interfaz de propiedades de salida ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) del formato de salida deseado llamando al método [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) . Para obtener más información sobre cómo enumerar los formatos de salida, vea [asignar formatos de salida](assigning-output-formats.md).
5.  Establezca el formato de salida llamando al método [**IWMReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) . Pase un puntero a la interfaz **IWMOutputMediaProps** obtenida en el paso 4.
6.  Realice cualquier otro cambio de configuración y comience la reproducción.

> [!Note]  
> Puede realizar los pasos anteriores en el lector sincrónico mediante los métodos correspondientes de la interfaz [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .

 

En el ejemplo de código siguiente se muestra cómo establecer una secuencia de audio para generar audio como datos S/PDIF. Esta función supone que ya se ha cargado un archivo en el lector y que se ha identificado el número de salida. Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).


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

[**Leer archivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Interfaz IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interfaz IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**Interfaz IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> </dl>

 

 




