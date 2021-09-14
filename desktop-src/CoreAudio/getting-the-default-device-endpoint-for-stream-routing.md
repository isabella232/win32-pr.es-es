---
description: En Windows 7, las API de plataforma de alto nivel que usan api de audio principales, como las API de Media Foundation, Direct Sound y Wave, implementan la característica de enrutamiento de secuencias mediante el control de la conmutación de secuencias de un dispositivo existente a un nuevo punto de conexión de audio predeterminado.
ms.assetid: 4f36710c-c5a8-4f31-9b77-5253475c0715
title: Obtención del punto de conexión de dispositivo para el enrutamiento de flujos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed8c7546c2bd7437ed9705dc93c2a736bbb64e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164977"
---
# <a name="getting-the-device-endpoint-for-stream-routing"></a>Obtención del punto de conexión de dispositivo para el enrutamiento de flujos

En Windows 7, las API de plataforma de alto nivel que usan api de audio principales, como las API de Media Foundation, Direct Sound y Wave, implementan la característica de enrutamiento de secuencias mediante el control de la conmutación de secuencias de un dispositivo existente a un nuevo punto de conexión de audio predeterminado. Las aplicaciones multimedia que usan estas API (por ejemplo, una aplicación que activa un objeto **IDirect Sound** o **IBaseFilter** en un [**objeto IMMDevice)**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) usan el comportamiento de enrutamiento de secuencias sin modificaciones en el origen.

Las API de alto nivel implementan el enrutamiento de secuencias para el punto de conexión de dispositivo que se obtiene a través de [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Si una aplicación se transmite al dispositivo predeterminado, la característica de enrutamiento de flujos funciona según lo definido. Secuencias se cambian al nuevo dispositivo si se recupera mediante cualquier otro mecanismo, incluso si es igual que el dispositivo predeterminado.

Una aplicación multimedia que usa core Audio API directamente (cliente WASAPI) puede proporcionar una implementación de enrutamiento de secuencias personalizada para cualquier dispositivo de representación o captura. Un cliente WASAPI puede replicar la aplicación proporcionada por las API de alto nivel restringiendo a los flujos que se abren en los dispositivos que se establecen como dispositivos predeterminados. Para obtener una referencia al punto de conexión del dispositivo predeterminado, el cliente debe llamar a [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). En esta llamada, el cliente debe indicar si requiere un puntero al dispositivo predeterminado de representación o al dispositivo predeterminado de captura especificando el *parámetro dataFlow.* El cliente también debe especificar el rol adecuado para el punto de conexión en el atributo **ERole** (**eConsole** o **eCommunications**). No use **eMultimedia**.

Si la aplicación se transmite a cualquier otro dispositivo, la aplicación puede obtener el dispositivo especificando una cadena de identificador de punto de conexión (mediante una llamada a [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).

Una vez identificado el dispositivo, el cliente WASAPI puede proporcionar la implementación para el enrutamiento de secuencias controlando el dispositivo y las notificaciones de sesión de audio enviadas para el dispositivo. Para obtener más información sobre estas notificaciones, vea [Notificaciones pertinentes para el enrutamiento de secuencias.](relevant-device-notifications-for-stream-routing.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de MMDevice API](mmdevice-api.md)
</dt> <dt>

[Acerca de WASAPI](wasapi.md)
</dt> <dt>

[Enrutamiento de flujos](stream-routing.md)
</dt> </dl>

 

 



