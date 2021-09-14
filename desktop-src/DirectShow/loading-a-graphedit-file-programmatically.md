---
description: Carga de un archivo GraphEdit mediante programación
ms.assetid: 0e1cff4e-43f8-4d0a-b7a7-b6d0278e9e4a
title: Carga de un archivo GraphEdit mediante programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a4780ead7b65d883bdd48917c6372425612435
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063208"
---
# <a name="loading-a-graphedit-file-programmatically"></a>Carga de un archivo GraphEdit mediante programación

Una aplicación puede usar la **interfaz IPersistStream** para cargar un archivo GraphEdit (.grf). Use el código siguiente:


```C++
HRESULT LoadGraphFile(IGraphBuilder *pGraph, const WCHAR* wszName)
{
    IStorage *pStorage = 0;
    if (S_OK != StgIsStorageFile(wszName))
    {
        return E_FAIL;
    }
    HRESULT hr = StgOpenStorage(wszName, 0, 
        STGM_TRANSACTED | STGM_READ | STGM_SHARE_DENY_WRITE, 
        0, 0, &pStorage);
    if (FAILED(hr))
    {
        return hr;
    }
    IPersistStream *pPersistStream = 0;
    hr = pGraph->QueryInterface(IID_IPersistStream,
             reinterpret_cast<void**>(&pPersistStream));
    if (SUCCEEDED(hr))
    {
        IStream *pStream = 0;
        hr = pStorage->OpenStream(L"ActiveMovieGraph", 0, 
            STGM_READ | STGM_SHARE_EXCLUSIVE, 0, &pStream);
        if(SUCCEEDED(hr))
        {
            hr = pPersistStream->Load(pStream);
            pStream->Release();
        }
        pPersistStream->Release();
    }
    pStorage->Release();
    return hr;
}

```



> [!Note]  
> La llamada a **IPersistStream::Load** en el ejemplo de código anterior puede devolver un error DirectShow código correcto. Para obtener una lista de posibles valores devueltos, vea [Códigos de error y de éxito.](error-and-success-codes.md)

 

Los archivos GraphEdit solo están pensados para pruebas y depuración. No están diseñados para su uso por las aplicaciones de usuario final.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Simulación Graph building con GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[**StgIsStorageFile**](/windows/win32/api/coml2api/nf-coml2api-stgisstoragefile)
</dt> <dt>

[**StgOpenStorage**](/windows/win32/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 
