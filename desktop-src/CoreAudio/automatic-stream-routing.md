---
description: En este artículo se describe cómo actualizar una implementación de WASAPI para aprovechar el enrutamiento automático de flujos.
ms.assetid: 718CBEB9-A7A0-4898-81B7-CBD76AFA3A06
title: Enrutamiento automático de flujos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd152db35c580d93cf76ccfaffd66b37225f2be7fae11f217a6895b289a58e12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957394"
---
# <a name="automatic-stream-routing"></a>Enrutamiento automático de flujos

En este artículo se describe cómo actualizar una implementación de WASAPI para aprovechar el enrutamiento automático de flujos.

A partir de Windows 7, cada vez que cambia el dispositivo de audio predeterminado, la secuencia de reproducción de audio de una aplicación se transfiere sin problemas desde el dispositivo de audio predeterminado anterior al nuevo dispositivo de audio predeterminado. Esta transferencia se produce automáticamente sin ningún código de aplicación adicional. Sin embargo, antes de Windows 10, versión 1607, las aplicaciones que usaban la API de sesión de audio de Windows de bajo nivel (WASAPI) no podían participar en esta funcionalidad de enrutamiento de flujo automatizado. Las aplicaciones que usan WASAPI tenían que implementar su propia forma de enrutamiento de secuencias mediante la adición de código adicional para detectar la llegada y eliminación de dispositivos de audio y cambiar la secuencia a esos dispositivos según corresponda. Las aplicaciones que usan WASAPI que no implementaron su propio mecanismo de enrutamiento de flujos en la llegada o eliminación del dispositivo se arriesgaban a proporcionar una experiencia de usuario inferior a la ideal.

A partir de la Windows 10, versión 1607, las aplicaciones que usan WASAPI pueden aprovechar el enrutamiento automático de flujos. Si la aplicación usa WASAPI, se recomienda encarecidamente que actualice la aplicación para aprovechar esta nueva funcionalidad mediante los pasos siguientes:

1.  Windows 10, versión 1607, define dos GUID nuevos que se pueden usar para activar una interfaz de representación o captura de audio con enrutamiento automático de secuencias, [DEVINTERFACE \_ AUDIO \_ RENDER](/windows/desktop/CoreAudio/devinterface-xxx-guids) y [DEVINTERFACE \_ AUDIO \_ CAPTURE](/windows/desktop/CoreAudio/devinterface-xxx-guids). Obtenga una representación de cadena de estos GUID mediante una llamada [**a StringFromIID**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid). En el ejemplo siguiente se muestra esta llamada para el GUID de representación de audio.

    ```C++
    PWSTR audioRenderGuidString;
    StringFromIID(DEVINTERFACE_AUDIO_RENDER, &audioRenderGuidString);
    ```

    

2.  Active el punto de conexión de audio pasando la cadena de identificador a la función [**WASAPI ActivateAudioInterfaceAsync.**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) En el ejemplo siguiente se pasa el identificador de representación de audio obtenido en el paso 1:

    ```C++
    //Activate the default audio interface
    ActivateAudioInterfaceAsync(audioRenderGuidString
                                __uuidof(IAudioClient),
                                NULL,
                                completionHandler.Get(),
                                operation.GetAddressOf()));
    ```

    

3.  Liberar la memoria asignada para contener el identificador del punto de conexión:

    ```C++
    CoTaskMemFree(audioRenderGuidString);  //free the string memory
    ```

    

Después de modificar la aplicación para activar la interfaz de audio de la manera descrita anteriormente, participará en la característica de enrutamiento automático de secuencias.

Para demostrar el enrutamiento automático de secuencias, use un portátil o tableta equipado con altavoces internos para reproducir audio. Debe escuchar el audio que se reproduce a través de los altavoces internos del dispositivo. Mientras se reproduce el audio, conecte un par de auriculares. Ahora debería escuchar audio reproduciendo a través de los auriculares. A continuación, desconecte los auriculares y el audio debería enrutar automáticamente a los altavoces internos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enrutamiento de secuencias](stream-routing.md)
</dt> <dt>

[**MediaDevice.GetDefaultAudioRenderId**](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiorenderid)
</dt> <dt>

[**MediaDevice.GetDefaultAudioCaptureId**](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiocaptureid)
</dt> <dt>

[**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)
</dt> </dl>

 

 
