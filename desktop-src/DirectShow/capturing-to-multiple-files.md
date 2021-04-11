---
description: Capturar en varios archivos
ms.assetid: 6073a891-e9f5-442d-a2d9-3a7b97f7f735
title: Capturar en varios archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b40091acff8edffbe84550b03d1ccd4073ddb6b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152192"
---
# <a name="capturing-to-multiple-files"></a>Capturar en varios archivos

Después de haber capturado el vídeo en un archivo, puede cambiar a un archivo nuevo si detiene el gráfico y establece el nombre de archivo en el filtro del [escritor de archivos](file-writer-filter.md) . Llame al método [**IFileSinkFilter:: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) en el escritor de archivos. Puede obtener un puntero a la interfaz [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) al compilar el gráfico, a través del parámetro *PSink* del método SetOutputFileName. El código siguiente muestra cómo hacerlo:


```C++
IBaseFilter *pMux;
IFileSinkFilter *pSink
hr = pBuild->SetOutputFileName(&MEDIASUBTYPE_Avi, L"C:\\YourFileName.avi", 
    &pMux, &pSink);
if (SUCCEEDED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
        pCap, NULL, pMux);

    if (SUCCEEDED(hr))
    {
        pControl->Run();
        /* Wait awhile, then stop the graph. */
        pControl->Stop();
        // Change the file name and run the graph again.
        pSink->SetFileName(L"YourFileName02.avi", 0);
        pControl->Run();
    }
    pMux->Release();
    pSink->Release();
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Capturar vídeo en un archivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



