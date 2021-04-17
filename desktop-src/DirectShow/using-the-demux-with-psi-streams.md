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
# <a name="using-the-demux-with-psi-streams"></a><span data-ttu-id="a8399-103">Uso de Demux con secuencias de PSI</span><span class="sxs-lookup"><span data-stu-id="a8399-103">Using the Demux with PSI Streams</span></span>

<span data-ttu-id="a8399-104">Para obtener información de PSI de una secuencia de transporte MPEG-2 mediante el filtro MPEG-2 Demux, cree un PIN de salida en Demux con el siguiente tipo de medio:</span><span class="sxs-lookup"><span data-stu-id="a8399-104">To get PSI information from an MPEG-2 transport stream using the MPEG-2 demux filter, create an output pin on the demux with the following media type:</span></span>

-   <span data-ttu-id="a8399-105">Tipo principal: KSDATAFORMAT \_ tipo \_ MPEG2 \_ secciones</span><span class="sxs-lookup"><span data-stu-id="a8399-105">Major type: KSDATAFORMAT\_TYPE\_MPEG2\_SECTIONS</span></span>
-   <span data-ttu-id="a8399-106">Subtipo: MEDIASUBTYPE \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="a8399-106">Subtype: MEDIASUBTYPE\_None</span></span>
-   <span data-ttu-id="a8399-107">Tipo de formato: GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="a8399-107">Format type: GUID\_NULL</span></span>

<span data-ttu-id="a8399-108">Después, llame al método [**IMPEG2PIDMap:: MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) del terminal de salida con el PID deseado y la marca media \_ MPEG2 \_ PSI.</span><span class="sxs-lookup"><span data-stu-id="a8399-108">Then call the output pin's [**IMPEG2PIDMap::MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) method with the desired PID and the flag MEDIA\_MPEG2\_PSI.</span></span>


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



<span data-ttu-id="a8399-109">Cada sección de PSI completa se entrega en un ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="a8399-109">Each complete PSI section is delivered in one media sample.</span></span> <span data-ttu-id="a8399-110">Para recuperar el número de PID asociado a una sección de tabla, llame a [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) en el ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="a8399-110">To retrieve the PID number associated with a table section, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the media sample.</span></span> <span data-ttu-id="a8399-111">El PID se proporciona en los 13 bits inferiores de la marca **dwTypeSpecificFlags** en la estructura de **\_ \_ propiedades AM SAMPLE2** .</span><span class="sxs-lookup"><span data-stu-id="a8399-111">The PID is given in the low 13 bits of the **dwTypeSpecificFlags** flag in the **AM\_SAMPLE2\_PROPERTIES** structure.</span></span> <span data-ttu-id="a8399-112">Esto resulta útil si asigna varios PID de PSI al mismo pin de salida.</span><span class="sxs-lookup"><span data-stu-id="a8399-112">This is useful if you map multiple PSI PIDs to the same output pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8399-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8399-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8399-114">Usar el demultiplexador MPEG-2</span><span class="sxs-lookup"><span data-stu-id="a8399-114">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



