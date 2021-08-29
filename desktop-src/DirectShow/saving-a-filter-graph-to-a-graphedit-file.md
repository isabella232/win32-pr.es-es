---
description: Guardar un filtro Graph un archivo GraphEdit
ms.assetid: f7eeae3c-506b-484c-8fe5-ddd391af5a59
title: Guardar un filtro Graph un archivo GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b007dfef4a6e00ba4b3d94828da1652a2299b3f21f966cba7717452df57faa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951984"
---
# <a name="saving-a-filter-graph-to-a-graphedit-file"></a>Guardar un filtro Graph un archivo GraphEdit

En el ejemplo de código siguiente se muestra cómo guardar un gráfico de filtro en un archivo GraphEdit (.grf). Esto puede ser útil para depurar las aplicaciones.


```C++
HRESULT SaveGraphFile(IGraphBuilder *pGraph, WCHAR *wszPath) 
{
    const WCHAR wszStreamName[] = L"ActiveMovieGraph"; 
    HRESULT hr;
    
    IStorage *pStorage = NULL;
    hr = StgCreateDocfile(
        wszPath,
        STGM_CREATE | STGM_TRANSACTED | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
        0, &pStorage);
    if(FAILED(hr)) 
    {
        return hr;
    }

    IStream *pStream;
    hr = pStorage->CreateStream(
        wszStreamName,
        STGM_WRITE | STGM_CREATE | STGM_SHARE_EXCLUSIVE,
        0, 0, &pStream);
    if (FAILED(hr)) 
    {
        pStorage->Release();    
        return hr;
    }

    IPersistStream *pPersist = NULL;
    pGraph->QueryInterface(IID_IPersistStream, (void**)&pPersist);
    hr = pPersist->Save(pStream, TRUE);
    pStream->Release();
    pPersist->Release();
    if (SUCCEEDED(hr)) 
    {
        hr = pStorage->Commit(STGC_DEFAULT);
    }
    pStorage->Release();
    return hr;
}
```



Por ejemplo, el código siguiente compila un gráfico de reproducción de archivos y lo guarda en un archivo denominado MyGraph.grf:


```C++
void __cdecl main(void)
{
    HRESULT hr;
    IGraphBuilder *pGraph;
    CoInitialize(NULL);
    
    // Create the Filter Graph Manager and render a file.
    CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
        IID_IGraphBuilder, reinterpret_cast<void**>(&pGraph));
    hr = pGraph->RenderFile(L"C:\\Video.avi", NULL);

    if (SUCCEEDED(hr))
    {
        hr = SaveGraphFile(pGraph, L"C:\\MyGraph.grf");
    }
    
    pGraph->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Simulación de Graph building con GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[**StgCreateDocfile**](/windows/win32/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> </dl>

 

 
