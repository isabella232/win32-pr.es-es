---
description: Captura en varios archivos
ms.assetid: 6073a891-e9f5-442d-a2d9-3a7b97f7f735
title: Captura en varios archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79ce7a1b4b91a0f78031a661e2c2e10895b4a21b1cfb068ca505429468a3af1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017583"
---
# <a name="capturing-to-multiple-files"></a>Captura en varios archivos

Después de capturar vídeo en un archivo, puede cambiar a un nuevo archivo deteniendo el gráfico y estableciendo el nombre de archivo en el filtro [Escritor de](file-writer-filter.md) archivos. Llame al [**método IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) en el escritor de archivos. Puede obtener un puntero a la interfaz [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) al compilar el gráfico, a través del *parámetro pSink* del método SetOutputFileName. El código siguiente muestra cómo hacerlo:


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

[Captura de vídeo en un archivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



