---
description: Interfaces de dispositivos externos para videocambaciones DV
ms.assetid: 001321c5-70c7-4baa-ba5a-1e424ca0d647
title: Interfaces de dispositivos externos para videocambaciones DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5e7106ec6e9b744da0d1f71958aeb895ec8df1a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909803"
---
# <a name="external-device-interfaces-for-dv-camcorders"></a><span data-ttu-id="30ddc-103">Interfaces de dispositivos externos para videocambaciones DV</span><span class="sxs-lookup"><span data-stu-id="30ddc-103">External Device Interfaces for DV Camcorders</span></span>

<span data-ttu-id="30ddc-104">El [filtro captura de vídeo de WDM](wdm-video-capture-filter.md) expone tres interfaces para controlar una cámara de vídeo.</span><span class="sxs-lookup"><span data-stu-id="30ddc-104">The [WDM Video Capture](wdm-video-capture-filter.md) filter exposes three interfaces for controlling a camcorder.</span></span>



| <span data-ttu-id="30ddc-105">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="30ddc-105">Label</span></span> | <span data-ttu-id="30ddc-106">Value</span><span class="sxs-lookup"><span data-stu-id="30ddc-106">Value</span></span> |
|------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="30ddc-107">**IAMExtDevice**</span><span class="sxs-lookup"><span data-stu-id="30ddc-107">**IAMExtDevice**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | <span data-ttu-id="30ddc-108">Interfaz base para el control de dispositivo externo.</span><span class="sxs-lookup"><span data-stu-id="30ddc-108">The base interface for external device control.</span></span> |
| [<span data-ttu-id="30ddc-109">**IAMExtTransport**</span><span class="sxs-lookup"><span data-stu-id="30ddc-109">**IAMExtTransport**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | <span data-ttu-id="30ddc-110">Controla las funciones de VCR.</span><span class="sxs-lookup"><span data-stu-id="30ddc-110">Controls the VCR functions.</span></span>                     |
| [<span data-ttu-id="30ddc-111">**IAMTimecodeReader**</span><span class="sxs-lookup"><span data-stu-id="30ddc-111">**IAMTimecodeReader**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | <span data-ttu-id="30ddc-112">Lee el código de tiempo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="30ddc-112">Reads timecode from the device.</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="30ddc-113">Para usar estas interfaces con el controlador de la cámara de vídeo MSDV, incluya el archivo de encabezado XPrtDefs.h en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="30ddc-113">To use these interfaces with the MSDV camcorder driver, include the header file XPrtDefs.h in your project.</span></span>

 

<span data-ttu-id="30ddc-114">Después de seleccionar un dispositivo de captura y crear una instancia del filtro de captura, consulte el filtro para estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="30ddc-114">After you select a capture device and create an instance of the capture filter, query the filter for these interfaces.</span></span> <span data-ttu-id="30ddc-115">En el ejemplo siguiente se declara una estructura personalizada que contiene los punteros de interfaz, junto con valores booleanos que especifican la disponibilidad de cada interfaz:</span><span class="sxs-lookup"><span data-stu-id="30ddc-115">The following example declares a custom structure that holds the interface pointers, along with Boolean values that specify the availability of each interface:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="30ddc-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="30ddc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30ddc-117">Control de una cámara dv</span><span class="sxs-lookup"><span data-stu-id="30ddc-117">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



