---
description: Formato de señal
ms.assetid: 8684972c-3233-49bf-8c34-ca644aca432a
title: Formato de señal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6983328729e0dc72d93c0e00a74e7e65a7f237
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906664"
---
# <a name="signal-format"></a><span data-ttu-id="12263-103">Formato de señal</span><span class="sxs-lookup"><span data-stu-id="12263-103">Signal Format</span></span>

<span data-ttu-id="12263-104">El formato de señal de una videocámara DV puede ser NTSC o PAL, estándar o de larga ejecución.</span><span class="sxs-lookup"><span data-stu-id="12263-104">A DV camcorder's signal format can be NTSC or PAL, standard or long-play.</span></span>

<span data-ttu-id="12263-105">**Controlador MSDV**</span><span class="sxs-lookup"><span data-stu-id="12263-105">**MSDV Driver**</span></span>

<span data-ttu-id="12263-106">Para obtener el formato de la señal de entrada desde el controlador MSDV, llame al método [**IAMExtTransport:: GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) y pase la \_ marca Ed transbasic \_ Input \_ Signal.</span><span class="sxs-lookup"><span data-stu-id="12263-106">To get the input signal format from the MSDV driver, call the [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) method and pass in the ED\_TRANSBASIC\_INPUT\_SIGNAL flag.</span></span> <span data-ttu-id="12263-107">El método devuelve una constante definida, que indica el formato.</span><span class="sxs-lookup"><span data-stu-id="12263-107">The method returns a defined constant, indicating the format.</span></span>

<span data-ttu-id="12263-108">En el código siguiente se comprueba el formato de la señal y se usa este valor para calcular el tiempo medio por fotograma.</span><span class="sxs-lookup"><span data-stu-id="12263-108">The following code checks the signal format, and uses this value to calculates the average time per frame.</span></span> <span data-ttu-id="12263-109">El modo variable recibe la constante de formato de señal.</span><span class="sxs-lookup"><span data-stu-id="12263-109">The variable Mode receives the signal-format constant.</span></span>


```C++
LONG Mode, AvgTimePerFrame;
hr = MyDevCap.pTransport->GetTransportBasicParameters(
        ED_TRANSBASIC_INPUT_SIGNAL, &Mode, NULL);
if (SUCCEEDED(hr))
{
    switch (Mode)
    {
    case ED_TRANSBASIC_SIGNAL_525_60_SD: // NTSC SD
        AvgTimePerFrame = 33;  // 33 msec (29.97 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_525_60_SDL: // NTSC SDL
        AvgTimePerFrame = 33;  
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SD: // PAL SD
        AvgTimePerFrame = 40;  // 40 msec (25 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SDL: // PAL SDL
        AvgTimePerFrame = 40;  
        break;
    default: 
        // Unknown type
        AvgTimePerFrame = 33; // Default
        break;
    }
}
```



<span data-ttu-id="12263-110">Para obtener el formato de la señal de salida, llame al mismo método con la \_ marca Ed transbasic \_ Output \_ Signal.</span><span class="sxs-lookup"><span data-stu-id="12263-110">To get the output signal format, call the same method with the ED\_TRANSBASIC\_OUTPUT\_SIGNAL flag.</span></span>

<span data-ttu-id="12263-111">**Controlador UVC**</span><span class="sxs-lookup"><span data-stu-id="12263-111">**UVC Driver**</span></span>

<span data-ttu-id="12263-112">Para obtener el formato de señal de entrada o salida del controlador UVC, llame a [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) en el PIN y examine el bloque de formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="12263-112">To get the input or output signal format from the UVC driver, call [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) on the pin and examine the video format block.</span></span> <span data-ttu-id="12263-113">(En el caso de los dispositivos UVC, el código que se muestra en el ejemplo anterior suele devolver ED \_ \_Señal de transbasic \_ desconocida, por lo que no es confiable).</span><span class="sxs-lookup"><span data-stu-id="12263-113">(For UVC devices, the code shown in the previous example usually returns ED\_TRANSBASIC\_SIGNAL\_UNKNOWN, so it is not reliable.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="12263-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12263-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12263-115">Control de una videocámara DV</span><span class="sxs-lookup"><span data-stu-id="12263-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



