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
# <a name="automatic-stream-routing"></a>Enrutamiento automático de flujos

En este artículo se describe cómo actualizar una implementación de WASAPI para aprovechar el enrutamiento automático de flujos.

A partir de Windows 7, cada vez que cambia el dispositivo de audio predeterminado, el flujo de reproducción de audio de una aplicación se transfiere sin problemas desde el dispositivo de audio predeterminado anterior al nuevo dispositivo de audio predeterminado. Esta transferencia se produce automáticamente sin ningún código de aplicación adicional. Sin embargo, antes de Windows 10, versión 1607, las aplicaciones que usaban la API de sesión de audio de bajo nivel de Windows (WASAPI) no podían participar en esta funcionalidad de enrutamiento de flujo automatizado. Las aplicaciones que usan WASAPI eran necesarias para implementar su propia forma de enrutamiento de flujo agregando código adicional para detectar la llegada y eliminación de dispositivos de audio y cambiar la secuencia a esos dispositivos según corresponda. Las aplicaciones que usan WASAPI que no implementaron su propio mecanismo de enrutamiento de flujo en la llegada o la eliminación de dispositivos arriesgaron a proporcionar una experiencia de usuario menos que la ideal.

A partir de la versión 1607 de Windows 10, las aplicaciones que usan WASAPI pueden aprovechar el enrutamiento automático de flujos. Si su aplicación usa WASAPI, se recomienda encarecidamente que actualice la aplicación para aprovechar esta nueva funcionalidad mediante los pasos siguientes:

1.  Windows 10, versión 1607, define dos nuevos GUID que se pueden usar para activar una interfaz de representación y presentación de audio con el enrutamiento automático de flujos, [DEVINTERFACE \_ audio \_ Render](/windows/desktop/CoreAudio/devinterface-xxx-guids) y [DEVINTERFACE \_ audio \_ Capture](/windows/desktop/CoreAudio/devinterface-xxx-guids). Obtenga una representación de cadena de estos GUID llamando a [**StringFromIID**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid). En el ejemplo siguiente se muestra esta llamada para el GUID de representación de audio.

    ```C++
    PWSTR audioRenderGuidString;
    StringFromIID(DEVINTERFACE_AUDIO_RENDER, &audioRenderGuidString);
    ```

    

2.  Active el punto de conexión de audio pasando la cadena de identificador a la función [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) de WASAPI. En el ejemplo siguiente se pasa el identificador de representación de audio obtenido en el paso 1:

    ```C++
    //Activate the default audio interface
    ActivateAudioInterfaceAsync(audioRenderGuidString
                                __uuidof(IAudioClient),
                                NULL,
                                completionHandler.Get(),
                                operation.GetAddressOf()));
    ```

    

3.  Libere la memoria asignada para contener el identificador del punto de conexión:

    ```C++
    CoTaskMemFree(audioRenderGuidString);  //free the string memory
    ```

    

Una vez que haya modificado la aplicación para activar la interfaz de audio de la manera descrita anteriormente, participará en la característica de enrutamiento automático de flujo.

Para demostrar el enrutamiento automático de flujos, use un equipo portátil o tableta equipado con altavoces internos para reproducir audio. Debe oír que el audio se reproduce a través de los altavoces internos del dispositivo. Mientras se reproduce el audio, conecte un par de auriculares. Ahora debería oír la reproducción de audio a través de los auriculares. A continuación, desconecte los auriculares y el audio debe redirigirse automáticamente a los altavoces internos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enrutamiento de flujos](stream-routing.md)
</dt> <dt>

[**MediaDevice.GetDefaultAudioRenderId**](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiorenderid)
</dt> <dt>

[**MediaDevice.GetDefaultAudioCaptureId**](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiocaptureid)
</dt> <dt>

[**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)
</dt> </dl>

 

 
