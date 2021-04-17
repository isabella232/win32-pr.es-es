---
description: Obtención de código de tiempo desde el dispositivo
ms.assetid: e3d06e0c-a595-4bc3-be62-168bd5122397
title: Obtención de código de tiempo desde el dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5787cf328214c1a266b7f129e4e517716b1d04f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105652307"
---
# <a name="getting-timecode-from-the-device"></a><span data-ttu-id="09ddd-103">Obtención de código de tiempo desde el dispositivo</span><span class="sxs-lookup"><span data-stu-id="09ddd-103">Getting Timecode from the Device</span></span>

<span data-ttu-id="09ddd-104">Mientras se reproduce una cinta DV o está en modo de grabación y pausa, puede recuperar el código de tiempo SMPTE o el número de pista absoluto.</span><span class="sxs-lookup"><span data-stu-id="09ddd-104">While a DV tape is playing or is in record-pause mode, you can retrieve the SMPTE timecode or the absolute track number.</span></span> <span data-ttu-id="09ddd-105">Para ello, llame al método [**IAMTimecodeReader:: GetTimecode**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) .</span><span class="sxs-lookup"><span data-stu-id="09ddd-105">To do this, call the [**IAMTimecodeReader::GetTimecode**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) method.</span></span> <span data-ttu-id="09ddd-106">Este método toma un puntero a una estructura de [**\_ ejemplo de código de tiempo**](/windows/win32/api/strmif/ns-strmif-timecode_sample) , que describe el código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="09ddd-106">This method takes a pointer to a [**TIMECODE\_SAMPLE**](/windows/win32/api/strmif/ns-strmif-timecode_sample) structure, which describes the timecode.</span></span> <span data-ttu-id="09ddd-107">Antes de llamar al método, inicialice el miembro **dwFlags** de la estructura.</span><span class="sxs-lookup"><span data-stu-id="09ddd-107">Before calling the method, initialize the **dwFlags** member of the structure.</span></span> <span data-ttu-id="09ddd-108">Use el valor de \_ DEVCAP de \_ código de tiempo de \_ lectura para recuperar el código de tiempo o el valor Ed \_ DEVCAP \_ ATN \_ Read para recuperar el número de pista absoluto.</span><span class="sxs-lookup"><span data-stu-id="09ddd-108">Use the value ED\_DEVCAP\_TIMECODE\_READ to retrieve the timecode or the value ED\_DEVCAP\_ATN\_READ to retrieve the absolute track number.</span></span>

<span data-ttu-id="09ddd-109">El miembro de **código** de tiempo de la estructura de **\_ ejemplo de código** de tiempo es una estructura de código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="09ddd-109">The **timecode** member of the **TIMECODE\_SAMPLE** structure is a TIMECODE structure.</span></span> <span data-ttu-id="09ddd-110">Cuando el método devuelve, el miembro **dwFrames** de la estructura de código de tiempo contiene el número de la pista o el código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="09ddd-110">When the method returns, the **dwFrames** member of the TIMECODE structure contains the timecode or track number.</span></span> <span data-ttu-id="09ddd-111">En el código de tiempo, las horas, los minutos, los segundos y los marcos se empaquetan en un valor DWORD como valores decimales codificados binarios (BCD), con el formato *hhmmssff*.</span><span class="sxs-lookup"><span data-stu-id="09ddd-111">For timecode, the hours, minutes, seconds, and frames are packed into a DWORD as binary coded decimal (BCD) values, with the format *hhmmssff*.</span></span> <span data-ttu-id="09ddd-112">Use máscaras de y para extraer los valores individuales.</span><span class="sxs-lookup"><span data-stu-id="09ddd-112">Use bitmasks to extract the individual values.</span></span>

<span data-ttu-id="09ddd-113">En el ejemplo siguiente se recupera el código de tiempo y el número de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="09ddd-113">The following example retrieves the timecode and track number.</span></span>


```C++
if (MyDevCap.bHasTimecode)
{
    TIMECODE_SAMPLE TimecodeSample;
    TimecodeSample.timecode.dwFrames = 0;
    char szBuf[32];

    TimecodeSample.dwFlags = ED_DEVCAP_TIMECODE_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample),  SUCCEEDED(hr)) 
    {
        DWORD dwTime = TimecodeSample.timecode.dwFrames; // Packed BCD value.
        int hour  = ((dwTime & 0x0F000000) >> 24) + 
                    (10 * ((dwTime & 0xF0000000) >> 28));
        int min   = ((dwTime & 0x0F0000) >> 16) + 
                    (10 * ((dwTime & 0xF00000) >> 20));
        int sec   = ((dwTime & 0x0F00) >> 8) + 
                    (10 * ((dwTime & 0xF000) >> 12));
        int frame = (dwTime & 0x0F) + 
                    (10 * ((dwTime & 0xF0) >> 4));
    }

    TimecodeSample.dwFlags = ED_DEVCAP_ATN_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample), SUCCEEDED(hr)) 
    {
        DWORD dwTrackNumber = TimecodeSample.timecode.dwFrames;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="09ddd-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09ddd-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09ddd-115">Control de una videocámara DV</span><span class="sxs-lookup"><span data-stu-id="09ddd-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 
