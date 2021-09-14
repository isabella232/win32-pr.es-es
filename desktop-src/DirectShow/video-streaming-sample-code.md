---
description: Código de ejemplo de streaming de vídeo
ms.assetid: 735af042-9800-4f75-a5c9-e1cf17b4a472
title: Código de ejemplo de streaming de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e9a738503174e7bcc6c0d0e7c1250e39348b4c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272876"
---
# <a name="video-streaming-sample-code"></a>Código de ejemplo de streaming de vídeo

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el [**filtro Sample Grabber**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un DirectShow gráfico de filtros.

 

Este código de ejemplo lee un archivo y lo representa en una superficie directDraw principal. Por brevedad, en este ejemplo se realiza una comprobación de errores mínima.


```C++
#include <stdio.h>
#include "ddraw.h"       // DirectDraw interfaces
#include "mmstream.h"    // multimedia stream interfaces
#include "amstream.h"    // DirectShow multimedia stream interfaces
#include "ddstream.h"    // DirectDraw multimedia stream interfaces

HRESULT RenderStreamToSurface(IDirectDrawSurface *pSurface, 
    IMultiMediaStream *pMMStream)
{    
    IMediaStream *pPrimaryVidStream;    
    IDirectDrawMediaStream *pDDStream;
    IDirectDrawStreamSample *pSample;
    RECT rect;
    DDSURFACEDESC ddsd;

    HRESULT hr;
    hr = pMMStream->GetMediaStream(MSPID_PrimaryVideo, &pPrimaryVidStream);
    if (FAILED(hr))
    {
        return hr;
    }
    pPrimaryVidStream->QueryInterface(IID_IDirectDrawMediaStream, (void **)&pDDStream);

    ddsd.dwSize = sizeof(ddsd);
    hr = pDDStream->GetFormat(&ddsd, NULL, NULL, NULL);
    if (SUCCEEDED(hr))
    {
        rect.top = rect.left = 0;
        rect.bottom = ddsd.dwHeight;
        rect.right = ddsd.dwWidth;
        hr = pDDStream->CreateSample(pSurface, &rect, 0, &pSample);
        if (SUCCEEDED(hr))
        {
            pMMStream->SetState(STREAMSTATE_RUN);
            while (pSample->Update(0, NULL, NULL, NULL) == S_OK)
            {
                // Empty loop.
            }
            pMMStream->SetState(STREAMSTATE_STOP);
            pSample->Release();    
        }
    }
    pDDStream->Release();
    pPrimaryVidStream->Release();
    return hr;
}

HRESULT RenderFileToMMStream(
    const char * szFileName, 
    IMultiMediaStream **ppMMStream,
    IDirectDraw *pDD)
{
    if (strlen(szFileName) > MAX_PATH)
    {
        return E_INVALIDARG;
    }

    IAMMultiMediaStream *pAMStream;
    HRESULT hr = CoCreateInstance(CLSID_AMMultiMediaStream, NULL, 
        CLSCTX_INPROC_SERVER, IID_IAMMultiMediaStream, 
        (void **)&pAMStream);
    if (FAILED(hr))
    {
        return hr;
    }

    WCHAR wPath[MAX_PATH + 1];
    MultiByteToWideChar(CP_ACP, 0, szFileName, -1, wPath, MAX_PATH + 1);

    pAMStream->Initialize(STREAMTYPE_READ, AMMSF_NOGRAPHTHREAD, NULL);
    pAMStream->AddMediaStream(pDD, &MSPID_PrimaryVideo, 0, NULL);
    pAMStream->AddMediaStream(NULL, &MSPID_PrimaryAudio, AMMSF_ADDDEFAULTRENDERER, NULL);
    hr = pAMStream->OpenFile(wPath, 0);
    if (SUCCEEDED(hr))
    {
        hr = pAMStream->QueryInterface(IID_IMultiMediaStream, 
            (void**)ppMMStream);
    }
    pAMStream->Release();
    return hr;
}

int __cdecl main(int argc, char *argv[])    
{    
    if (argc < 2) 
    {
        printf("Usage : showstrm movie.ext\n");
        exit(0);
    }    

    DDSURFACEDESC ddsd;
    IDirectDraw *pDD;    
    IDirectDrawSurface *pPrimarySurface;
    IMultiMediaStream *pMMStream;

    CoInitialize(NULL);

    DirectDrawCreate(NULL, &pDD, NULL);
    pDD->SetCooperativeLevel(GetDesktopWindow(), DDSCL_NORMAL);

    ddsd.dwSize = sizeof(ddsd);
    ddsd.dwFlags = DDSD_CAPS;
    ddsd.ddsCaps.dwCaps = DDSCAPS_PRIMARYSURFACE;
    pDD->CreateSurface(&ddsd, &pPrimarySurface, NULL);

    HRESULT hr = RenderFileToMMStream(argv[1], &pMMStream, pDD);
    if (SUCCEEDED(hr))
    {
        RenderStreamToSurface(pPrimarySurface, pMMStream);    
        pMMStream->Release();
    }
    pPrimarySurface->Release();    
    pDD->Release(); 
    
    CoUninitialize();
    return 0;
}
```



 

 



