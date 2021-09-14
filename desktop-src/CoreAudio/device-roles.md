---
description: Roles de dispositivo
ms.assetid: aa787004-0d3e-448b-80dd-92055f841aee
title: Roles de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b7182e3af6bf76af500588546a1b7c0db9eea97
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165041"
---
# <a name="device-roles"></a>Roles de dispositivo

Si un sistema contiene dos o más dispositivos de punto de conexión de representación de audio, un dispositivo podría ser el mejor para reproducir un tipo de contenido de audio y otro dispositivo podría ser mejor para reproducir otro tipo de contenido. Por ejemplo, si un sistema tiene dos dispositivos de representación, el usuario podría optar por reproducir música en un dispositivo y reproducir sonidos de notificación del sistema en el otro.

Del mismo modo, si un sistema contiene dos o más dispositivos de punto de conexión de captura de audio, un dispositivo podría ser el mejor para capturar un tipo de contenido de audio y otro dispositivo podría ser mejor para capturar otro tipo de contenido. Por ejemplo, si un sistema tiene dos dispositivos de captura, el usuario podría optar por grabar música en directo en un dispositivo y usar el otro dispositivo para los comandos de voz.

Los dispositivos pueden tener tres roles: Consola, Comunicaciones y Multimedia. En la tabla siguiente se describen los roles de dispositivo identificados por las tres constantes (eConsole, eCommunications y eMultimedia) en la enumeración [**ERole.**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)



| Constante ERole  | Rol de dispositivo                              | Ejemplos de representación             | Ejemplos de captura                   |
|-----------------|------------------------------------------|--------------------------------|------------------------------------|
| eConsole        | Interacción con el equipo            | Juegos y notificaciones del sistema | Comandos de voz                     |
| eCommunications | Comunicaciones de voz con otra persona | Chat y VoIP                  | Chat y VoIP                      |
| eMultimedia     | Reproducción o grabación de contenido de audio       | Música y películas               | Narración y grabación de música en directo |



 

Un dispositivo de representación o captura determinado podría tener asignados ninguno, uno, algunos o todos los roles de la tabla anterior. En cualquier momento, cada rol de la tabla se asigna a un dispositivo de representación (y solo a uno) y a un único dispositivo de captura. Es decir, la asignación de roles a dispositivos de representación es independiente de la asignación de roles para capturar dispositivos.

Una aplicación puede optar por reproducir todos sus flujos de salida a través de un único dispositivo de punto de conexión de representación y registrar todos sus flujos de entrada desde un único dispositivo de punto de conexión de captura. Como alternativa, una aplicación podría optar por reproducir algunos de sus flujos de salida a través de un dispositivo de representación y reproducir otros flujos de salida a través de otro dispositivo de representación. De forma similar, podría optar por registrar algunos de sus flujos de entrada a través de un dispositivo de captura y registrar otros flujos de entrada a través de otro dispositivo de captura. En todos los casos, la aplicación puede asignar cada secuencia al dispositivo cuyo rol sea más adecuado para esa secuencia.

Por ejemplo, una aplicación VoIP podría asignar el flujo de salida que contiene la notificación de anillo al dispositivo de punto de conexión de representación con el rol eConsole.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos de punto de conexión de audio](audio-endpoint-devices.md)
</dt> <dt>

[Trabajar con roles de dispositivo](device-roles-in-windows-vista.md)
</dt> <dt>

[Interoperabilidad con las API de audio heredadas](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



