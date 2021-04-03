---
description: Trabajar con roles de dispositivo
ms.assetid: 3b2cb1fe-0f11-4509-a6f3-513d2755cd29
title: Trabajar con roles de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c21ea667a6974634c1f9f0657dd02c13a621641c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998067"
---
# <a name="working-with-device-roles"></a>Trabajar con roles de dispositivo

La [API de MMDevice](mmdevice-api.md) admite roles de dispositivo. La enumeración [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) define los roles de dispositivo admitidos por la API de MMDevice.

> [!Note]  
> Aunque la [API de MMDevice](mmdevice-api.md) admite roles de dispositivo, la interfaz de usuario de Windows Vista no implementa la compatibilidad con esta característica.

 

Una aplicación puede usar la API de MMDevice para admitir [roles de dispositivo](device-roles.md) a través de los métodos [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) y [**IMMNotificationClient:: OnDefaultDeviceChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) . Sin embargo, la interfaz de usuario de Windows Vista no admite la asignación de roles individuales a distintos dispositivos. En Windows Vista, la interfaz de usuario permite al usuario seleccionar un dispositivo de audio predeterminado para su representación y un dispositivo de audio predeterminado para la captura. Cuando el usuario selecciona un dispositivo de representación o captura predeterminado, el sistema asigna los tres roles de dispositivo (eConsole, eMultimedia y eCommunications) a ese dispositivo. Las aplicaciones no pueden cambiar los roles asignados a los dispositivos de punto de conexión de audio. El sistema operativo solo permite al usuario asignar roles de dispositivo.

Un cliente puede registrarse para recibir una notificación de la API de MMDevice cada vez que se produce un cambio en la asignación de roles a los dispositivos de punto de conexión de audio. Cuando un rol se desplaza de un dispositivo a otro, el cliente puede elegir si desea continuar jugando (o grabando) sus flujos a través del mismo dispositivo o cambiar los flujos a otro dispositivo. De forma predeterminada, las secuencias continúan reproduciéndose (o grabadas) a través del dispositivo original. En Windows Vista, para cambiar los flujos a otro dispositivo, el cliente debe eliminar las secuencias en el dispositivo original y crear secuencias de reemplazo en el nuevo dispositivo. En Windows 7, el cliente puede escuchar nuevas notificaciones para implementar un modificador sin problemas sin interrumpir la reproducción o la sesión de captura. Para obtener más información, vea [enrutamiento de flujo](stream-routing.md).

Si tiene previsto usar Windows Vista para probar la aplicación, puede configurar un entorno de prueba para comprobar que la aplicación se comporta según lo esperado cuando el usuario puede asignar roles de dispositivo individuales a distintos dispositivos. Para más información, envíe un correo electrónico a uaa@microsoft.com.

## <a name="communication-devices"></a>Dispositivos de comunicación

La interfaz de usuario de Windows 7 tiene la capacidad de agregar *dispositivos de comunicaciones*. El panel de control de **sonido** permite al usuario seleccionar un dispositivo de comunicación predeterminado para representar y capturar el flujo de audio. De forma predeterminada, cuando se conecta un nuevo dispositivo al equipo, el sistema operativo realiza la detección automática de roles y determina si el dispositivo es adecuado para el rol eCommunication. Al dirigirse a los dispositivos de comunicación, puede desarrollar aplicaciones que usen las API de audio básicas para implementar soluciones de comunicación de teléfono móvil. Por ejemplo, una aplicación de VoIP podría asignar sus flujos de entrada y salida de voz a los dispositivos de punto de conexión de captura y representación predeterminados con el rol eCommunications. Al igual que cualquier otro flujo, una aplicación de comunicación debe obtener una referencia al punto de conexión del dispositivo de comunicación llamando a [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). En esta llamada, la aplicación debe especificar **eCommunications** en el parámetro *role* . Las operaciones de Stream WASAPI en una secuencia, abierta en un dispositivo de comunicación, son similares a cualquier otra secuencia de audio. La aplicación de comunicación puede mejorar la experiencia del usuario mediante la implementación de comportamientos como la perdedoncia mediante el control de notificaciones desde el punto de conexión del dispositivo. Para obtener más información, vea [uso de un dispositivo de comunicación](using-the-communication-device.md).

## <a name="automatic-device-role-detection"></a>Detección automática de roles de dispositivo

Considere un escenario en el que un equipo tiene un dispositivo de representación predeterminado, los altavoces y un dispositivo de captura predeterminado, un micrófono. El usuario conecta un auricular USB al equipo. Una vez instalados los controladores adecuados, el sistema operativo intenta detectar un rol para asignarlo al nuevo dispositivo de audio.

En Windows 7, la característica de detección de roles de dispositivo se ha mejorado significativamente para determinar los roles adecuados para los dispositivos de audio. Todos los dispositivos de audio contienen un conjunto de opciones de configuración que se rellenan con el OEM del dispositivo, que ayudan al sistema a decidir cómo usar el dispositivo. Esta configuración incluye información como la ubicación física del conector de audio, el tipo de dispositivo, el subtipo de conector y las capacidades de detección para que el sistema pueda determinar si el dispositivo está conectado. Al recuperar estos valores del dispositivo, el sistema operativo determina el rol que se va a asignar al dispositivo. En este escenario, el sistema ha consultado el dispositivo USB con auriculares, ha realizado la detección automática de roles y ha decidido que el dispositivo es más adecuado para ser un dispositivo de comunicación.

Una aplicación también puede obtener información de los conectores mediante las API de audio principales. Para obtener más información, vea [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription) y [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Roles de dispositivo](device-roles.md)
</dt> </dl>

 

 



