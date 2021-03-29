---
description: En este artículo se describe cómo actualizar una implementación de WASAPI para aprovechar el enrutamiento automático de flujos.
ms.assetid: 718CBEB9-A7A0-4898-81B7-CBD76AFA3A06
title: Enrutamiento automático de flujos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a9848c5fd764ee49e485fc112c35c347a0f84d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000801"
---
# <a name="automatic-stream-routing"></a><span data-ttu-id="88bf6-103">Enrutamiento automático de flujos</span><span class="sxs-lookup"><span data-stu-id="88bf6-103">Automatic Stream Routing</span></span>

<span data-ttu-id="88bf6-104">En este artículo se describe cómo actualizar una implementación de WASAPI para aprovechar el enrutamiento automático de flujos.</span><span class="sxs-lookup"><span data-stu-id="88bf6-104">This article describes how to update a WASAPI implementation to take advantage of automatic stream routing.</span></span>

<span data-ttu-id="88bf6-105">A partir de Windows 7, cada vez que cambia el dispositivo de audio predeterminado, el flujo de reproducción de audio de una aplicación se transfiere sin problemas desde el dispositivo de audio predeterminado anterior al nuevo dispositivo de audio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="88bf6-105">Starting with Windows 7, whenever the default audio device changes, an app's audio playback stream is seamlessly transferred from the previous default audio device to the new default audio device .</span></span> <span data-ttu-id="88bf6-106">Esta transferencia se produce automáticamente sin ningún código de aplicación adicional.</span><span class="sxs-lookup"><span data-stu-id="88bf6-106">This transfer occurs automatically without any additional application code.</span></span> <span data-ttu-id="88bf6-107">Sin embargo, antes de Windows 10, versión 1607, las aplicaciones que usaban la API de sesión de audio de bajo nivel de Windows (WASAPI) no podían participar en esta funcionalidad de enrutamiento de flujo automatizado.</span><span class="sxs-lookup"><span data-stu-id="88bf6-107">However, prior to Windows 10, version 1607, apps that used the low-level Windows Audio Session API (WASAPI) could not participate in this automated stream routing functionality.</span></span> <span data-ttu-id="88bf6-108">Las aplicaciones que usan WASAPI eran necesarias para implementar su propia forma de enrutamiento de flujo agregando código adicional para detectar la llegada y eliminación de dispositivos de audio y cambiar la secuencia a esos dispositivos según corresponda.</span><span class="sxs-lookup"><span data-stu-id="88bf6-108">Apps using WASAPI were required to implement their own form of stream routing by adding additional code to detect the arrival and removal of audio devices and switch the stream to those devices as appropriate.</span></span> <span data-ttu-id="88bf6-109">Las aplicaciones que usan WASAPI que no implementaron su propio mecanismo de enrutamiento de flujo en la llegada o la eliminación de dispositivos arriesgaron a proporcionar una experiencia de usuario menos que la ideal.</span><span class="sxs-lookup"><span data-stu-id="88bf6-109">Applications using WASAPI that did not implement their own stream routing mechanism on device arrival or removal risked providing a less than ideal user experience.</span></span>

<span data-ttu-id="88bf6-110">A partir de la versión 1607 de Windows 10, las aplicaciones que usan WASAPI pueden aprovechar el enrutamiento automático de flujos.</span><span class="sxs-lookup"><span data-stu-id="88bf6-110">Starting with the Windows 10, version 1607, apps that use WASAPI can take advantage of automatic stream routing.</span></span> <span data-ttu-id="88bf6-111">Si su aplicación usa WASAPI, se recomienda encarecidamente que actualice la aplicación para aprovechar esta nueva funcionalidad mediante los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="88bf6-111">If your application uses WASAPI it is highly recommended that you update your application to take advantage of this new capability using the following steps:</span></span>

1.  <span data-ttu-id="88bf6-112">Windows 10, versión 1607, define dos nuevos GUID que se pueden usar para activar una interfaz de representación y presentación de audio con el enrutamiento automático de flujos, [DEVINTERFACE \_ audio \_ Render](/windows/desktop/CoreAudio/devinterface-xxx-guids) y [DEVINTERFACE \_ audio \_ Capture](/windows/desktop/CoreAudio/devinterface-xxx-guids).</span><span class="sxs-lookup"><span data-stu-id="88bf6-112">Windows 10, version 1607, defines two new GUIDs that can be used to activate an audio render or capture interface with automatic stream routing, [DEVINTERFACE\_AUDIO\_RENDER](/windows/desktop/CoreAudio/devinterface-xxx-guids) and [DEVINTERFACE\_AUDIO\_CAPTURE](/windows/desktop/CoreAudio/devinterface-xxx-guids).</span></span> <span data-ttu-id="88bf6-113">Obtenga una representación de cadena de estos GUID llamando a [**StringFromIID**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid).</span><span class="sxs-lookup"><span data-stu-id="88bf6-113">Get a string representation of these GUIDs by calling [**StringFromIID**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid).</span></span> <span data-ttu-id="88bf6-114">En el ejemplo siguiente se muestra esta llamada para el GUID de representación de audio.</span><span class="sxs-lookup"><span data-stu-id="88bf6-114">The following example shows this call for the audio render GUID.</span></span>

    ```C++
    PWSTR audioRenderGuidString;
    StringFromIID(DEVINTERFACE_AUDIO_RENDER, &audioRenderGuidString);
    ```

    

2.  <span data-ttu-id="88bf6-115">Active el punto de conexión de audio pasando la cadena de identificador a la función [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) de WASAPI.</span><span class="sxs-lookup"><span data-stu-id="88bf6-115">Activate the audio endpoint by passing the identifier string to the WASAPI [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) function.</span></span> <span data-ttu-id="88bf6-116">En el ejemplo siguiente se pasa el identificador de representación de audio obtenido en el paso 1:</span><span class="sxs-lookup"><span data-stu-id="88bf6-116">The following example passes in the audio render identifier obtained in step 1:</span></span>

    ```C++
    //Activate the default audio interface
    ActivateAudioInterfaceAsync(audioRenderGuidString
                                __uuidof(IAudioClient),
                                NULL,
                                completionHandler.Get(),
                                operation.GetAddressOf()));
    ```

    

3.  <span data-ttu-id="88bf6-117">Libere la memoria asignada para contener el identificador del punto de conexión:</span><span class="sxs-lookup"><span data-stu-id="88bf6-117">Free the memory allocated for holding the endpoint identifier:</span></span>

    ```C++
    CoTaskMemFree(audioRenderGuidString);  //free the string memory
    ```

    

<span data-ttu-id="88bf6-118">Una vez que haya modificado la aplicación para activar la interfaz de audio de la manera descrita anteriormente, participará en la característica de enrutamiento automático de flujo.</span><span class="sxs-lookup"><span data-stu-id="88bf6-118">After you have modified your app to activate the audio interface in the manner described above, it will participate in the automatic stream routing feature.</span></span>

<span data-ttu-id="88bf6-119">Para demostrar el enrutamiento automático de flujos, use un equipo portátil o tableta equipado con altavoces internos para reproducir audio.</span><span class="sxs-lookup"><span data-stu-id="88bf6-119">To demonstrate automatic stream routing, use a laptop or tablet equipped with internal speakers to play back audio.</span></span> <span data-ttu-id="88bf6-120">Debe oír que el audio se reproduce a través de los altavoces internos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="88bf6-120">You should hear the audio playing through the device's internal speakers.</span></span> <span data-ttu-id="88bf6-121">Mientras se reproduce el audio, conecte un par de auriculares.</span><span class="sxs-lookup"><span data-stu-id="88bf6-121">While audio is playing, connect a pair of headphones.</span></span> <span data-ttu-id="88bf6-122">Ahora debería oír la reproducción de audio a través de los auriculares.</span><span class="sxs-lookup"><span data-stu-id="88bf6-122">You should now hear audio playing through the headphones.</span></span> <span data-ttu-id="88bf6-123">A continuación, desconecte los auriculares y el audio debe redirigirse automáticamente a los altavoces internos.</span><span class="sxs-lookup"><span data-stu-id="88bf6-123">Then, unplug the headphones and audio should automatically route back to the internal speakers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88bf6-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="88bf6-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88bf6-125">Enrutamiento de flujos</span><span class="sxs-lookup"><span data-stu-id="88bf6-125">Stream Routing</span></span>](stream-routing.md)
</dt> <dt>

[<span data-ttu-id="88bf6-126">**MediaDevice.GetDefaultAudioRenderId**</span><span class="sxs-lookup"><span data-stu-id="88bf6-126">**MediaDevice.GetDefaultAudioRenderId**</span></span>](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiorenderid)
</dt> <dt>

[<span data-ttu-id="88bf6-127">**MediaDevice.GetDefaultAudioCaptureId**</span><span class="sxs-lookup"><span data-stu-id="88bf6-127">**MediaDevice.GetDefaultAudioCaptureId**</span></span>](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiocaptureid)
</dt> <dt>

[<span data-ttu-id="88bf6-128">**ActivateAudioInterfaceAsync**</span><span class="sxs-lookup"><span data-stu-id="88bf6-128">**ActivateAudioInterfaceAsync**</span></span>](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)
</dt> </dl>

 

 
