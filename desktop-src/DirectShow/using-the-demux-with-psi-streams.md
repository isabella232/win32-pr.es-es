---
description: Uso de Demux con psi Secuencias
ms.assetid: 355e905e-ff21-4bde-a018-ed9631ef5ed5
title: Uso de Demux con psi Secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659e4a12bfef25f24a5e6cac38d191f86ab80b4a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891628"
---
# <a name="using-the-demux-with-psi-streams"></a>Uso de Demux con psi Secuencias

Para obtener información de PSI de una secuencia de transporte MPEG-2 mediante el filtro demux MPEG-2, cree una patilla de salida en la demux con el siguiente tipo de medio:

-   Tipo principal: KSDATAFORMAT \_ TYPE \_ MPEG2 \_ SECTIONS
-   Subtipo: MEDIASUBTYPE \_ None
-   Tipo de formato: GUID \_ NULL

A continuación, llame al método [**IMPEG2PIDMap::MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) de la patilla de salida con el PID deseado y la marca MEDIA \_ MPEG2 \_ PSI.


```C++
// Query the demux filter for IMpeg2Demultiplexer.
IMpeg2Demultiplexer *pDemux = NULL;
hr = pFilter->QueryInterface(IID_IMpeg2Demultiplexer, (void**)&pDemux);
if (SUCCEEDED(hr))
{
    // Define the media type.
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
    mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;
    mt.subtype = MEDIASUBTYPE_None;

    // Create a new output pin.
    IPin *pPin;
    hr = pDemux->CreateOutputPin(&mt, L"PSI Pin", &pPin);
    if (SUCCEEDED(hr))
    {
        // Map the PID.
        IMPEG2PIDMap *pPidMap = NULL;
        hr = pPin->QueryInterface(IID_IMPEG2PIDMap, (void**)&pPidMap);
        if (SUCCEEDED(hr))
        {
            ULONG Pid[] = { 0x00 }; // Map any desired PIDs. 
            ULONG cPid = 1;
            hr = pPidMap->MapPID(cPid, Pid, MEDIA_MPEG2_PSI);
            pPidMap->Release();
        }
        pPin->Release();
    }
    pDemux->Release();
}
```



Cada sección completa de PSI se entrega en un ejemplo multimedia. Para recuperar el número de PID asociado a una sección de tabla, llame a [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) en el ejemplo multimedia. El PID se proporciona en los 13 bits inferiores de la **marca dwTypeSpecificFlags** en la **estructura PROPIEDADES DE AM \_ SAMPLE2. \_** Esto resulta útil si asigna varios PIN de PSI al mismo pin de salida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del demultiplexor MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



