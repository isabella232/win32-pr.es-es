---
description: En este tema se describe cómo una aplicación puede cambiar mediante programación la configuración de la cámara y la imagen en un dispositivo de captura de vídeo.
ms.assetid: f789db78-292e-4092-a5dc-1906845fb1dd
title: Configurar la calidad del vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cb8d2d28e39f0083aac521f1953ebbb1ca8d5b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805690"
---
# <a name="configure-the-video-quality"></a><span data-ttu-id="86732-103">Configurar la calidad del vídeo</span><span class="sxs-lookup"><span data-stu-id="86732-103">Configure the Video Quality</span></span>

<span data-ttu-id="86732-104">En este tema se describe cómo una aplicación puede cambiar mediante programación la configuración de la cámara y la imagen en un dispositivo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="86732-104">This topic describes how an application can programmatically change the image and camera settings on a video capture device.</span></span>

-   [<span data-ttu-id="86732-105">Configuración de ProcAmp</span><span class="sxs-lookup"><span data-stu-id="86732-105">ProcAmp Settings</span></span>](#procamp-settings)
-   [<span data-ttu-id="86732-106">Configuración de la cámara</span><span class="sxs-lookup"><span data-stu-id="86732-106">Camera Settings</span></span>](#camera-settings)
-   [<span data-ttu-id="86732-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="86732-107">Related topics</span></span>](#related-topics)

## <a name="procamp-settings"></a><span data-ttu-id="86732-108">Configuración de ProcAmp</span><span class="sxs-lookup"><span data-stu-id="86732-108">ProcAmp Settings</span></span>

<span data-ttu-id="86732-109">Las cámaras de vídeo Modelo de controlador de Windows (WDM) pueden admitir propiedades que controlan la calidad de la imagen:</span><span class="sxs-lookup"><span data-stu-id="86732-109">Windows Driver Model (WDM) video cameras can support properties that control the quality of the image:</span></span>

-   <span data-ttu-id="86732-110">Compensación de contraluz</span><span class="sxs-lookup"><span data-stu-id="86732-110">Backlight compensation</span></span>
-   <span data-ttu-id="86732-111">Luminosidad</span><span class="sxs-lookup"><span data-stu-id="86732-111">Brightness</span></span>
-   <span data-ttu-id="86732-112">Compare</span><span class="sxs-lookup"><span data-stu-id="86732-112">Contrast</span></span>
-   <span data-ttu-id="86732-113">Beneficios</span><span class="sxs-lookup"><span data-stu-id="86732-113">Gain</span></span>
-   <span data-ttu-id="86732-114">Gamma</span><span class="sxs-lookup"><span data-stu-id="86732-114">Gamma</span></span>
-   <span data-ttu-id="86732-115">Matiz</span><span class="sxs-lookup"><span data-stu-id="86732-115">Hue</span></span>
-   <span data-ttu-id="86732-116">Saturación</span><span class="sxs-lookup"><span data-stu-id="86732-116">Saturation</span></span>
-   <span data-ttu-id="86732-117">Nitidez</span><span class="sxs-lookup"><span data-stu-id="86732-117">Sharpness</span></span>
-   <span data-ttu-id="86732-118">Balance de blancos</span><span class="sxs-lookup"><span data-stu-id="86732-118">White balance</span></span>

<span data-ttu-id="86732-119">Estas propiedades se controlan a través de la interfaz [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) .</span><span class="sxs-lookup"><span data-stu-id="86732-119">These properties are controlled through the [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) interface.</span></span> <span data-ttu-id="86732-120">Use esta interfaz como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="86732-120">Use this interface as follows:</span></span>

1.  <span data-ttu-id="86732-121">Llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el filtro de captura para la interfaz [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) .</span><span class="sxs-lookup"><span data-stu-id="86732-121">Call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the capture filter for the [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) interface.</span></span>
2.  <span data-ttu-id="86732-122">Para cada propiedad que desee establecer, llame al método [**IAMVideoProcAmp:: GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) .</span><span class="sxs-lookup"><span data-stu-id="86732-122">For each property that you want to set, call the [**IAMVideoProcAmp::GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) method.</span></span> <span data-ttu-id="86732-123">Las propiedades se especifican mediante la enumeración [**VideoProcAmpProperty**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) .</span><span class="sxs-lookup"><span data-stu-id="86732-123">Properties are specified by the [**VideoProcAmpProperty**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) enumeration.</span></span> <span data-ttu-id="86732-124">Si se produce un error en el método **GetRange** , significa que la cámara no es compatible con esa propiedad determinada.</span><span class="sxs-lookup"><span data-stu-id="86732-124">If the **GetRange** method fails, it means the camera does not support that particular property.</span></span>
3.  <span data-ttu-id="86732-125">Si [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) se ejecuta correctamente, devuelve el intervalo de valores admitidos para la propiedad, el valor predeterminado y el incremento mínimo.</span><span class="sxs-lookup"><span data-stu-id="86732-125">If [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) succeeds, it returns the range of supported values for the property, the default value, and the minimum increment.</span></span>
4.  <span data-ttu-id="86732-126">Para obtener el valor actual de una propiedad, llame a [**IAMVideoProcAmp:: get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).</span><span class="sxs-lookup"><span data-stu-id="86732-126">To get the current value of a property, call [**IAMVideoProcAmp::Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).</span></span>
5.  <span data-ttu-id="86732-127">Para establecer una propiedad, llame al método [**IAMVideoProcAmp:: set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) .</span><span class="sxs-lookup"><span data-stu-id="86732-127">To set a property, call the [**IAMVideoProcAmp::Set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) method.</span></span> <span data-ttu-id="86732-128">Para restaurar una propiedad a su valor predeterminado, llame a [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) para buscar el valor predeterminado y pasarlo al método **set** .</span><span class="sxs-lookup"><span data-stu-id="86732-128">To restore a property to its default value, call [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) to find the default and pass that value to the **Set** method.</span></span>

<span data-ttu-id="86732-129">No es necesario detener el gráfico de filtros al establecer las propiedades.</span><span class="sxs-lookup"><span data-stu-id="86732-129">You do not have to stop the filter graph when you set the properties.</span></span>

<span data-ttu-id="86732-130">En el código siguiente se configura un control TrackBar para que se pueda usar para establecer el brillo.</span><span class="sxs-lookup"><span data-stu-id="86732-130">The following code configures a trackbar control so that it can be used to set the brightness.</span></span> <span data-ttu-id="86732-131">El intervalo de la barra de inicio corresponde al intervalo de brillo que admite el dispositivo y la posición de la barra de inicio corresponde a la configuración de brillo inicial del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="86732-131">The range of the trackbar corresponds to the brightness range that the device supports, and position of the trackbar corresponds to the device's initial brightness setting.</span></span>


```C++
HWND hTrackbar; // Handle to the trackbar control. 
// Initialize hTrackbar (not shown).

// Query the capture filter for the IAMVideoProcAmp interface.
IAMVideoProcAmp *pProcAmp = 0;
hr = pCap->QueryInterface(IID_IAMVideoProcAmp, (void**)&pProcAmp);
if (FAILED(hr))
{
    // The device does not support IAMVideoProcAmp, so disable the control.
    EnableWindow(hTrackbar, FALSE);
}
else
{
    long Min, Max, Step, Default, Flags, Val;

    // Get the range and default value. 
    hr = m_pProcAmp->GetRange(VideoProcAmp_Brightness, &Min, &Max, &Step,
        &Default, &Flags);
    if (SUCCEEDED(hr))
    {
        // Get the current value.
        hr = m_pProcAmp->Get(VideoProcAmp_Brightness, &Val, &Flags);
    }
    if (SUCCEEDED(hr))
    {
        // Set the trackbar range and position.
        SendMessage(hTrackbar, TBM_SETRANGE, TRUE, MAKELONG(Min, Max));
        SendMessage(hTrackbar, TBM_SETPOS, TRUE, Val);
        EnableWindow(hTrackbar, TRUE);
    }
    else
    {
        // This property is not supported, so disable the control.
        EnableWindow(hTrackbar, FALSE);
    }
}
```



## <a name="camera-settings"></a><span data-ttu-id="86732-132">Configuración de la cámara</span><span class="sxs-lookup"><span data-stu-id="86732-132">Camera Settings</span></span>

<span data-ttu-id="86732-133">La interfaz [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) es similar a [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp), pero controla diversas configuraciones en la propia cámara:</span><span class="sxs-lookup"><span data-stu-id="86732-133">The [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) interface is similar to [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp), but controls various setttings on the camera itself:</span></span>

-   <span data-ttu-id="86732-134">Exposure</span><span class="sxs-lookup"><span data-stu-id="86732-134">Exposure</span></span>
-   <span data-ttu-id="86732-135">Foco</span><span class="sxs-lookup"><span data-stu-id="86732-135">Focus</span></span>
-   <span data-ttu-id="86732-136">Iris</span><span class="sxs-lookup"><span data-stu-id="86732-136">Iris</span></span>
-   <span data-ttu-id="86732-137">Movimiento panorámico</span><span class="sxs-lookup"><span data-stu-id="86732-137">Pan</span></span>
-   <span data-ttu-id="86732-138">Volver</span><span class="sxs-lookup"><span data-stu-id="86732-138">Roll</span></span>
-   <span data-ttu-id="86732-139">Cline</span><span class="sxs-lookup"><span data-stu-id="86732-139">Tilt</span></span>
-   <span data-ttu-id="86732-140">Zoom</span><span class="sxs-lookup"><span data-stu-id="86732-140">Zoom</span></span>

<span data-ttu-id="86732-141">Para usar esta interfaz, siga los mismos pasos que se usan para [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp):</span><span class="sxs-lookup"><span data-stu-id="86732-141">To use this interface, follow the same steps used for [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp):</span></span>

1.  <span data-ttu-id="86732-142">Consulte el filtro de captura para el [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol).</span><span class="sxs-lookup"><span data-stu-id="86732-142">Query the capture filter for the [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol).</span></span>
2.  <span data-ttu-id="86732-143">Llame a [**IAMCameraControl:: GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) para averiguar qué valores de configuración se admiten y el intervalo posible para cada configuración.</span><span class="sxs-lookup"><span data-stu-id="86732-143">Call [**IAMCameraControl::GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) to find which settings are supported, and the possible range for each settings.</span></span>
3.  <span data-ttu-id="86732-144">Llame a [**IAMCameraControl:: get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) para obtener el valor actual de una configuración.</span><span class="sxs-lookup"><span data-stu-id="86732-144">Call [**IAMCameraControl::Get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) to get the current value of a setting.</span></span>
4.  <span data-ttu-id="86732-145">Llame a [**IAMCameraControl:: set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) para establecer el valor.</span><span class="sxs-lookup"><span data-stu-id="86732-145">Call [**IAMCameraControl::Set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) to set the value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86732-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="86732-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86732-147">Configuración de un dispositivo de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="86732-147">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 
