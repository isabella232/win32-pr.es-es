---
description: Uso de Demux con secuencias de PSI
ms.assetid: 355e905e-ff21-4bde-a018-ed9631ef5ed5
title: Uso de Demux con secuencias de PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659e4a12bfef25f24a5e6cac38d191f86ab80b4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667857"
---
# <a name="using-the-demux-with-psi-streams"></a>Uso de Demux con secuencias de PSI

Para obtener información de PSI de una secuencia de transporte MPEG-2 mediante el filtro MPEG-2 Demux, cree un PIN de salida en Demux con el siguiente tipo de medio:

-   Tipo principal: KSDATAFORMAT \_ tipo \_ MPEG2 \_ secciones
-   Subtipo: MEDIASUBTYPE \_ ninguno
-   Tipo de formato: GUID \_ null

Después, llame al método [**IMPEG2PIDMap:: MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) del terminal de salida con el PID deseado y la marca media \_ MPEG2 \_ PSI.


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



Cada sección de PSI completa se entrega en un ejemplo multimedia. Para recuperar el número de PID asociado a una sección de tabla, llame a [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) en el ejemplo multimedia. El PID se proporciona en los 13 bits inferiores de la marca **dwTypeSpecificFlags** en la estructura de **\_ \_ propiedades AM SAMPLE2** . Esto resulta útil si asigna varios PID de PSI al mismo pin de salida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el demultiplexador MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



