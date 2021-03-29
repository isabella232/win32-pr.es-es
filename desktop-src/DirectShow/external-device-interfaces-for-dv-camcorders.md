---
description: Interfaces de dispositivos externos para camascopios DV
ms.assetid: 001321c5-70c7-4baa-ba5a-1e424ca0d647
title: Interfaces de dispositivos externos para camascopios DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52b6d0fe00ff91ff87e9c810bbe7ecc319e9bfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906898"
---
# <a name="external-device-interfaces-for-dv-camcorders"></a><span data-ttu-id="553d6-103">Interfaces de dispositivos externos para camascopios DV</span><span class="sxs-lookup"><span data-stu-id="553d6-103">External Device Interfaces for DV Camcorders</span></span>

<span data-ttu-id="553d6-104">El filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) expone tres interfaces para controlar una videocámara.</span><span class="sxs-lookup"><span data-stu-id="553d6-104">The [WDM Video Capture](wdm-video-capture-filter.md) filter exposes three interfaces for controlling a camcorder.</span></span>



|                                                |                                                 |
|------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="553d6-105">**IAMExtDevice**</span><span class="sxs-lookup"><span data-stu-id="553d6-105">**IAMExtDevice**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | <span data-ttu-id="553d6-106">La interfaz base para el control de dispositivo externo.</span><span class="sxs-lookup"><span data-stu-id="553d6-106">The base interface for external device control.</span></span> |
| [<span data-ttu-id="553d6-107">**IAMExtTransport**</span><span class="sxs-lookup"><span data-stu-id="553d6-107">**IAMExtTransport**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | <span data-ttu-id="553d6-108">Controla las funciones de VCR.</span><span class="sxs-lookup"><span data-stu-id="553d6-108">Controls the VCR functions.</span></span>                     |
| [<span data-ttu-id="553d6-109">**IAMTimecodeReader**</span><span class="sxs-lookup"><span data-stu-id="553d6-109">**IAMTimecodeReader**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | <span data-ttu-id="553d6-110">Lee el código de tiempo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="553d6-110">Reads timecode from the device.</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="553d6-111">Para usar estas interfaces con el controlador de videocámara MSDV, incluya el archivo de encabezado XPrtDefs. h en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="553d6-111">To use these interfaces with the MSDV camcorder driver, include the header file XPrtDefs.h in your project.</span></span>

 

<span data-ttu-id="553d6-112">Después de seleccionar un dispositivo de captura y crear una instancia del filtro de captura, consulte el filtro para estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="553d6-112">After you select a capture device and create an instance of the capture filter, query the filter for these interfaces.</span></span> <span data-ttu-id="553d6-113">En el ejemplo siguiente se declara una estructura personalizada que contiene los punteros de interfaz, junto con valores booleanos que especifican la disponibilidad de cada interfaz:</span><span class="sxs-lookup"><span data-stu-id="553d6-113">The following example declares a custom structure that holds the interface pointers, along with Boolean values that specify the availability of each interface:</span></span>


```C++
struct _MyDevCap
{
    IAMExtDevice       *pDevice;
    IAMExtTransport    *pTransport;
    IAMTimecodeReader  *pTimecode;
    BOOL                bHasDevice;
    BOOL                bHasTransport;
    BOOL                bHasTimecode;
} MyDevCap;

HRESULT hr;
IBaseFilter *pDVCam;  // Pointer to the capture filter.

// Create an instance of the capture filter (not shown).

hr = pDVCam->QueryInterface(IID_IAMExtDevice, (void **)&MyDevCap.pDevice);
MyDevCap.bHasDevice = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMExtTransport, (void **)&MyDevCap.pTransport);
MyDevCap.bHasTransport = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMTimecodeReader, (void **)&MyDevCap.pTimecode);
MyDevCap.bHasTimecode = (SUCCEEDED(hr));
```



## <a name="related-topics"></a><span data-ttu-id="553d6-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="553d6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="553d6-115">Control de una videocámara DV</span><span class="sxs-lookup"><span data-stu-id="553d6-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



