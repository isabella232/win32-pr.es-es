---
title: Acerca de la sincronización de dispositivos
description: Acerca de la sincronización de dispositivos
ms.assetid: 87976357-f819-41ac-9645-36e799876881
keywords:
- Reproductor de Windows Media, sincronizar dispositivos
- Reproductor de Windows Media modelo de objetos, sincronizar dispositivos
- modelo de objetos, sincronizar dispositivos
- Reproductor de Windows Media ActiveX control, sincronización de dispositivos
- ActiveX control, sincronización de dispositivos
- Reproductor de Windows Media Control de ActiveX móviles, sincronización de dispositivos
- Reproductor de Windows Media Móvil, sincronización de dispositivos
- sincronizar dispositivos, acerca de
- sincronización de dispositivos, acerca de
- sincronizar dispositivos, transferencia manual
- sincronización de dispositivos, transferencia manual
- sincronizar dispositivos, sincronización automática
- sincronización de dispositivos, sincronización automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed6a03781121a58bee36fd9ff1f74bf21a85347f81384f30c2db5afb4ef3e1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903565"
---
# <a name="about-device-synchronization"></a>Acerca de la sincronización de dispositivos

Reproductor de Windows Media 10 introdujo un nuevo modelo para sincronizar el contenido multimedia digital con dispositivos portátiles. Desde la perspectiva del usuario, esto significa que puede especificar qué listas de reproducción (incluidas las listas de reproducción automáticas) se sincronizan automáticamente con los dispositivos. También puede transferir manualmente contenido multimedia digital a los dispositivos. Desde la perspectiva del desarrollador, esto significa que hay una nueva funcionalidad expuesta que puede aprovechar en sus aplicaciones. Para ello, debe crear una instancia remota del control Reproductor de Windows Media remoto.

Hay dos maneras en que un usuario puede copiar contenido multimedia digital en un dispositivo:

-   **Transferencia manual.** El usuario selecciona contenido multimedia digital en la biblioteca y, a continuación, inicia una transferencia del contenido al dispositivo. Esto es similar a la funcionalidad proporcionada por versiones anteriores de Reproductor de Windows Media. El SDK Reproductor de Windows Media no proporciona métodos para transferir medios digitales a un dispositivo.
-   **Sincronización automática.** El usuario especifica listas de reproducción que se sincronizan automáticamente con el dispositivo. Esta es una característica de Reproductor de Windows Media 10 o posterior. El SDK Reproductor de Windows Media proporciona funcionalidad para administrar la sincronización automática. Esta funcionalidad está diseñada para que pueda crear una interfaz de usuario personalizada para la aplicación con el fin de especificar cómo se produce la sincronización de dispositivos y proporcionar información de estado a los usuarios.

Para que la sincronización automática funcione, debe establecerse una relación especial entre Reproductor de Windows Media y el dispositivo. Esta relación se denomina *asociación*.

En las secciones siguientes se proporciona más información sobre la sincronización de dispositivos.

-   [Acerca de los dispositivos](about-devices.md)
-   [Acerca de las asociaciones](about-partnerships.md)
-   [Acerca del motor de sincronización](about-the-synchronization-engine.md)
-   [Acerca de la sincronización de listas de reproducción](about-playlist-synchronization.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos del reproductor**](about-the-player-object-model.md)
</dt> <dt>

[**Control remoto del Reproductor de Windows Media**](remoting-the-windows-media-player-control.md)
</dt> <dt>

[**Trabajar con dispositivos portátiles**](working-with-portable-devices.md)
</dt> </dl>

 

 




