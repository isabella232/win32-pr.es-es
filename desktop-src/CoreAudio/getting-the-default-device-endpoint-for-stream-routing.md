---
description: En Windows 7, las API de plataforma de alto nivel que usan las API de audio principales como Media Foundation, DirectSound y las API de Wave, implementan la característica de enrutamiento de flujo mediante la administración del cambio de flujo desde un dispositivo existente a un nuevo punto de conexión de audio predeterminado.
ms.assetid: 4f36710c-c5a8-4f31-9b77-5253475c0715
title: Obtención del punto de conexión del dispositivo para el enrutamiento de flujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed8c7546c2bd7437ed9705dc93c2a736bbb64e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907269"
---
# <a name="getting-the-device-endpoint-for-stream-routing"></a>Obtención del punto de conexión del dispositivo para el enrutamiento de flujo

En Windows 7, las API de plataforma de alto nivel que usan las API de audio principales como Media Foundation, DirectSound y las API de Wave, implementan la característica de enrutamiento de flujo mediante la administración del cambio de flujo desde un dispositivo existente a un nuevo punto de conexión de audio predeterminado. Las aplicaciones multimedia que usan estas API (por ejemplo, una aplicación que activa un objeto **IDirectSound** o **IBaseFilter** en un objeto [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) ) usan el comportamiento de enrutamiento de flujo sin modificaciones en el origen.

Las API de alto nivel implementan el enrutamiento de flujos para el punto de conexión de dispositivo que se obtiene a través de [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Si una aplicación se transmite al dispositivo predeterminado, la característica de enrutamiento de flujo funciona como se define. Los flujos no se cambian al nuevo dispositivo si lo recupera cualquier otro mecanismo, aunque sea el mismo que el dispositivo predeterminado.

Una aplicación multimedia que usa las API de audio principales directamente (cliente WASAPI) puede proporcionar una implementación de enrutamiento de flujo personalizado para cualquier dispositivo de representación o captura. Un cliente de WASAPI puede replicar la implementación proporcionada por las API de alto nivel mediante su restricción a las secuencias que se abren en los dispositivos que se establecen como el dispositivo predeterminado. Para obtener una referencia al punto de conexión del dispositivo predeterminado, el cliente debe llamar a [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). En esta llamada, el cliente debe indicar si requiere un puntero al dispositivo predeterminado de representación o el dispositivo predeterminado de captura especificando el parámetro *DataFlow* . El cliente también debe especificar el rol adecuado para el punto de conexión en el atributo **ERole** (**eConsole** o **eCommunications**). No use **eMultimedia**.

Si la aplicación se transmite a cualquier otro dispositivo, la aplicación puede obtener el dispositivo mediante la especificación de una cadena de identificador de punto de conexión (mediante una llamada a [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).

Una vez identificado el dispositivo, el cliente de WASAPI puede proporcionar la implementación para el enrutamiento de flujo mediante el control de las notificaciones de sesión de dispositivo y de audio enviadas para el dispositivo. Para obtener más información sobre estas notificaciones, consulte [notificaciones relevantes para el enrutamiento de flujos](relevant-device-notifications-for-stream-routing.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la API de MMDevice](mmdevice-api.md)
</dt> <dt>

[Acerca de WASAPI](wasapi.md)
</dt> <dt>

[Enrutamiento de flujos](stream-routing.md)
</dt> </dl>

 

 



