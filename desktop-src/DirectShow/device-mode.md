---
description: Modo de dispositivo
ms.assetid: d56021be-616b-41cd-8cf0-9e0d314f62cd
title: Modo de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4657fbb49e2619d75911c18185109805116b9647
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495779"
---
# <a name="device-mode"></a><span data-ttu-id="2db7c-103">Modo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="2db7c-103">Device Mode</span></span>

<span data-ttu-id="2db7c-104">Las videocámaras IEEE 1394 y USB pueden cambiar entre el modo de cámara y el modo de grabadora de cintas de vídeo (VTR).</span><span class="sxs-lookup"><span data-stu-id="2db7c-104">IEEE 1394 and USB camcorders can switch between camera mode and video tape recorder (VTR) mode.</span></span> <span data-ttu-id="2db7c-105">Cuando una videocámara IEEE 1394 cambia de modo, el dispositivo se restablece y la aplicación debe volver a enumerarlo.</span><span class="sxs-lookup"><span data-stu-id="2db7c-105">When an IEEE 1394 camcorder switches modes, the device resets and the application must enumerate it again.</span></span> <span data-ttu-id="2db7c-106">No hay ninguna manera de que una aplicación cambie el modo mediante programación.</span><span class="sxs-lookup"><span data-stu-id="2db7c-106">There is no way for an application to switch the mode programmatically.</span></span> <span data-ttu-id="2db7c-107">Por otro lado, las videocámaras USB pueden cambiar entre los modos de cámara y VTR sin tener que restablecer y la aplicación puede cambiar el modo.</span><span class="sxs-lookup"><span data-stu-id="2db7c-107">USB camcorders, on the other hand, can switch between camera and VTR modes without resetting, and the application can change the mode.</span></span>

<span data-ttu-id="2db7c-108">**Controlador MSDV**</span><span class="sxs-lookup"><span data-stu-id="2db7c-108">**MSDV Driver**</span></span>

<span data-ttu-id="2db7c-109">Para obtener el modo actual en un dispositivo IEEE 1394, llame al método [**IAMExtDevice:: GetCapability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) con el tipo de dispositivo de valor Ed \_ DEVCAP \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2db7c-109">To get the current mode on an IEEE 1394 device, call the [**IAMExtDevice::GetCapability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) method with the value ED\_DEVCAP\_DEVICE\_TYPE.</span></span> <span data-ttu-id="2db7c-110">Si el método devuelve el valor ED \_ DEVTYPE \_ VCR, el dispositivo está en modo VTR y tiene funciones como pausa, detener, avance rápido y rebobinado.</span><span class="sxs-lookup"><span data-stu-id="2db7c-110">If the method returns the value ED\_DEVTYPE\_VCR, the device is in VTR mode and has functions such as pause, stop, fast-forward, and rewind.</span></span> <span data-ttu-id="2db7c-111">De lo contrario, si el método devuelve ED \_ DEVTYPE \_ Camera, el dispositivo está en modo de cámara.</span><span class="sxs-lookup"><span data-stu-id="2db7c-111">Otherwise, if the method returns ED\_DEVTYPE\_CAMERA, the device is in camera mode.</span></span> <span data-ttu-id="2db7c-112">En el ejemplo de código siguiente se muestra cómo consultar el tipo de dispositivo:</span><span class="sxs-lookup"><span data-stu-id="2db7c-112">The following code example shows how to query the device type:</span></span>


```C++
if (MyDevCap.bHasDevice) 
{
    LONG lDeviceType = 0;
    MyDevCap.pDevice->GetCapability(ED_DEVCAP_DEVICE_TYPE, &lDeviceType, 0);

    if (lDeviceType == ED_DEVTYPE_VCR) 
    {
        // Device is a VTR. Enable all VTR functions.
    }
    else 
    {
        // Device is a camera. 
        // Enable record and record-pause; disable other functions.
    }
}
```



<span data-ttu-id="2db7c-113">Si el camcorder se queda sin conexión, debe volver a consultarlo cuando esté disponible.</span><span class="sxs-lookup"><span data-stu-id="2db7c-113">If the camcorder goes offline, you should query it again when it next becomes available.</span></span> <span data-ttu-id="2db7c-114">El administrador de gráficos de filtros envía un evento de [**\_ dispositivo EC \_ perdido**](ec-device-lost.md) cuando se quita el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2db7c-114">The filter graph manager posts an [**EC\_DEVICE\_LOST**](ec-device-lost.md) event when the device is removed.</span></span>

<span data-ttu-id="2db7c-115">**Controlador UVC**</span><span class="sxs-lookup"><span data-stu-id="2db7c-115">**UVC Driver**</span></span>

<span data-ttu-id="2db7c-116">Dado que los dispositivos de vídeo USB pueden cambiar de modo sin restablecer, el código que se muestra en los ejemplos anteriores no es confiable para dispositivos USB.</span><span class="sxs-lookup"><span data-stu-id="2db7c-116">Because USB video devices can switch modes without resetting, the code shown in the previous examples is not reliable for USB devices.</span></span> <span data-ttu-id="2db7c-117">En su lugar, use la interfaz [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) para obtener el modo actual.</span><span class="sxs-lookup"><span data-stu-id="2db7c-117">Instead, use the [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) interface to get the current mode.</span></span> <span data-ttu-id="2db7c-118">También puede usar esta interfaz para cambiar los modos mediante programación si el dispositivo lo admite.</span><span class="sxs-lookup"><span data-stu-id="2db7c-118">You can also use this interface to switch modes programmatically if the device supports it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2db7c-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2db7c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2db7c-120">Control de una videocámara DV</span><span class="sxs-lookup"><span data-stu-id="2db7c-120">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



