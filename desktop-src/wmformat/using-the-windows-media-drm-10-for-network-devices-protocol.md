---
title: Usar el protocolo DRM 10 de Windows Media para dispositivos de red
description: Usar el protocolo DRM 10 de Windows Media para dispositivos de red
ms.assetid: dec88d72-718c-42ab-8d48-eddf906051ef
keywords:
- Windows Media Format SDK, Windows Media DRM 10 para dispositivos de red
- Windows Media Format SDK, DRM 10 para dispositivos de red
- Advanced Systems Format (ASF), Windows Media DRM 10 para dispositivos de red
- ASF (formato de sistemas avanzados), Windows Media DRM 10 para dispositivos de red
- Advanced Systems Format (ASF), DRM 10 para dispositivos de red
- ASF (formato de sistemas avanzados), DRM 10 para dispositivos de red
- Administración de derechos digitales (DRM), Windows Media DRM 10 para dispositivos de red
- DRM (administración de derechos digitales), Windows Media DRM 10 para dispositivos de red
- Administración de derechos digitales (DRM), DRM 10 para dispositivos de red
- DRM (administración de derechos digitales), DRM 10 para dispositivos de red
- Windows Media DRM 10 para dispositivos de red, protocolos
- DRM 10 para dispositivos de red, protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73908c66dbffe7f50f4f28beb520861611d59962
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357026"
---
# <a name="using-the-windows-media-drm-10-for-network-devices-protocol"></a>Usar el protocolo DRM 10 de Windows Media para dispositivos de red

El SDK de Windows Media Format proporciona algunas características para admitir el protocolo de dispositivo de red seguro, Windows Media DRM 10 para dispositivos de red. Este protocolo define los mensajes que se envían entre un dispositivo de reproducción de medios digitales, como un reproductor de vídeo de un conjunto y el equipo que atiende los datos en el dispositivo. Los datos multimedia enviados entre el servidor y el dispositivo están cifrados para protegerse de la interceptación.

La comunicación entre la aplicación y los dispositivos que admiten Windows Media DRM 10 para dispositivos de red puede usar cualquier protocolo de red que prefiera. El SDK de Windows Media Format no proporciona ningún objeto que lleve a cabo las comunicaciones de red. En su lugar, los objetos de este SDK procesan algunos mensajes de Windows Media DRM 10 para dispositivos de red después de que la aplicación los haya recibido.

Las características que admiten Windows Media DRM 10 para dispositivos de red son el registro de dispositivos, la detección de proximidad y la conversión de archivos protegidos con DRM. Estas características se describen en las secciones siguientes.



| Sección                                                                                                                                                                          | Descripción                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Registro de dispositivos](device-registration.md)                                                                                                                                   | Describe cómo procesar los mensajes de solicitud de registro de los dispositivos.                                                                       |
| [Realización de la detección de proximidad](performing-proximity-detection.md)                                                                                                             | Describe el proceso de detección de proximidad.                                                                                                 |
| [Convertir un archivo de DRM-Protected en un flujo de Windows Media DRM 10 para dispositivos de red](converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream.md) | Describe cómo convertir un archivo protegido con DRM en una secuencia que se puede enviar a un dispositivo que usa Windows Media DRM 10 para dispositivos de red. |



 

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Habilitar la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




