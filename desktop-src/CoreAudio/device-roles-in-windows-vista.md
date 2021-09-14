---
description: Trabajar con roles de dispositivo
ms.assetid: 3b2cb1fe-0f11-4509-a6f3-513d2755cd29
title: Trabajar con roles de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c21ea667a6974634c1f9f0657dd02c13a621641c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165046"
---
# <a name="working-with-device-roles"></a>Trabajar con roles de dispositivo

MMDevice [API admite roles](mmdevice-api.md) de dispositivo. La [**enumeración ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) define los roles de dispositivo admitidos por MMDevice API.

> [!Note]  
> Aunque [MMDevice API admite](mmdevice-api.md) roles de dispositivo, la interfaz de usuario de Windows Vista no implementa compatibilidad con esta característica.

 

Una aplicación puede usar MMDevice API para admitir [roles](device-roles.md) de dispositivo mediante los métodos [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) [**e IMMNotificationClient::OnDefaultDeviceChanged.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) Sin embargo, la interfaz de usuario Windows Vista no admite la asignación de roles individuales a distintos dispositivos. En Windows Vista, la interfaz de usuario permite al usuario seleccionar un dispositivo de audio predeterminado para la representación y un dispositivo de audio predeterminado para la captura. Cuando el usuario selecciona un dispositivo de representación o captura predeterminado, el sistema asigna los tres roles de dispositivo (eConsole, eMultimedia y eCommunications) a ese dispositivo. Las aplicaciones no pueden cambiar los roles asignados a los dispositivos de punto de conexión de audio. El sistema operativo solo permite al usuario asignar roles de dispositivo.

Un cliente puede registrarse para recibir una notificación de MMDevice API cada vez que se produce un cambio en la asignación de roles a dispositivos de punto de conexión de audio. Cuando un rol cambia de un dispositivo a otro, el cliente puede elegir si continuar reproduciendo (o grabando) sus secuencias a través del mismo dispositivo o cambiar las secuencias a otro dispositivo. De forma predeterminada, las secuencias se siguen reproducendo (o se graban) a través del dispositivo original. En Windows Vista, para cambiar las secuencias a otro dispositivo, el cliente debe eliminar las secuencias del dispositivo original y crear secuencias de reemplazo en el nuevo dispositivo. En Windows 7, el cliente puede escuchar nuevas notificaciones para implementar un conmutador sin problemas sin interrumpir la reproducción o la sesión de captura. Para obtener más información, vea [Stream Routing](stream-routing.md).

Si tiene previsto usar Windows Vista para probar la aplicación, puede configurar un entorno de prueba para comprobar que la aplicación se comporta según lo previsto cuando el usuario puede asignar roles de dispositivo individuales a distintos dispositivos. Para más información, envíe un correo electrónico a uaa@microsoft.com.

## <a name="communication-devices"></a>Dispositivos de comunicación

La Windows de usuario 7 tiene la capacidad de agregar dispositivos *de comunicaciones*. El **panel** de control Sonido permite al usuario seleccionar un dispositivo de comunicación predeterminado para representar y capturar secuencias de audio. De forma predeterminada, cuando un nuevo dispositivo está conectado al equipo, el sistema operativo realiza la detección automática de roles y determina si el dispositivo es adecuado para el rol de comunicación electrónica. Al dirigirse a dispositivos de comunicación, puede desarrollar aplicaciones que usan Core Audio API para implementar soluciones de comunicación de pc-phone. Por ejemplo, una aplicación VoIP podría asignar sus flujos de entrada y salida de voz a los dispositivos de punto de conexión de captura y representación predeterminados con el rol eCommunications. Al igual que cualquier otra secuencia, una aplicación de comunicación debe obtener una referencia al punto de conexión del dispositivo de comunicación llamando a [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). En esta llamada, la aplicación debe especificar **eCommunications** en el *parámetro Role.* Las operaciones de secuencia WASAPI en una secuencia, abiertas en un dispositivo de comunicación, son similares a cualquier otra secuencia de audio. La aplicación de comunicación puede mejorar la experiencia del usuario mediante la implementación de comportamientos como el agachamiento mediante el control de las notificaciones desde el punto de conexión del dispositivo. Para obtener más información, consulte [Uso de un dispositivo de comunicación.](using-the-communication-device.md)

## <a name="automatic-device-role-detection"></a>Detección automática de roles de dispositivo

Considere un escenario en el que un equipo tiene un dispositivo de representación predeterminado, los altavoces y un dispositivo de captura predeterminado, un micrófono. El usuario conecta un casco USB al equipo. Una vez instalados los controladores adecuados, el sistema operativo intenta detectar un rol que se asignará para el nuevo dispositivo de audio.

En Windows 7, la característica de detección de roles de dispositivo se ha mejorado significativamente para determinar los roles adecuados adecuados para dispositivos de audio. Todos los dispositivos de audio contienen un conjunto de opciones de configuración rellenadas por el OEM del dispositivo, lo que ayuda al sistema a decidir cómo usar el dispositivo. Esta configuración incluye información como la ubicación física del conector de audio del tipo de dispositivo, el subtipo de conector y las funcionalidades de detección para que el sistema pueda determinar si el dispositivo está conectado. Al recuperar estos valores del dispositivo, el sistema operativo determina el rol que se asignará al dispositivo. En este escenario, el sistema ha consultado el dispositivo de casco USB, ha realizado la detección automática de roles y ha decidido que el dispositivo es más adecuado para ser un dispositivo de comunicación.

Una aplicación también puede obtener información sobre el conector mediante core Audio API. Para obtener más información, [**vea IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription) e [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Roles de dispositivo](device-roles.md)
</dt> </dl>

 

 



