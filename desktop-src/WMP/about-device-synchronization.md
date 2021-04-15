---
title: Acerca de la sincronización de dispositivos
description: Acerca de la sincronización de dispositivos
ms.assetid: 87976357-f819-41ac-9645-36e799876881
keywords:
- Windows Media Player, sincronizar dispositivos
- Modelo de objetos de Windows Media Player, sincronizar dispositivos
- modelo de objetos, sincronizar dispositivos
- Control ActiveX de Windows Media Player, sincronizar dispositivos
- Control ActiveX, sincronizar dispositivos
- Control ActiveX móvil de Windows Media Player, sincronizar dispositivos
- Windows Media Player Mobile, sincronizar dispositivos
- sincronizar dispositivos, acerca de
- sincronización de dispositivos, acerca de
- sincronización de dispositivos, transferencia manual
- sincronización de dispositivos, transferencia manual
- sincronizar dispositivos, sincronización automática
- sincronización de dispositivos, sincronización automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ad6b6526698def2f7d58ec7afc04c8e22e89c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695294"
---
# <a name="about-device-synchronization"></a>Acerca de la sincronización de dispositivos

Windows Media Player 10 presentó un nuevo modelo para sincronizar contenido multimedia digital con dispositivos portátiles. Desde la perspectiva del usuario, esto significa que puede especificar qué listas de reproducción (incluidas las listas de reproducción automáticas) se sincronizan automáticamente con los dispositivos. También puede transferir manualmente contenido multimedia digital a los dispositivos. Desde la perspectiva del desarrollador, esto significa que hay nuevas funcionalidades expuestas que puede aprovechar en sus aplicaciones. Para ello, debe crear una instancia remota del control Media Player de Windows.

Hay dos maneras en que un usuario puede copiar contenido multimedia digital en un dispositivo:

-   **Transferencia manual.** El usuario selecciona el contenido multimedia digital en la biblioteca y, a continuación, inicia una transferencia del contenido al dispositivo. Esto es similar a la funcionalidad proporcionada por las versiones anteriores de Windows Media Player. El SDK de Windows Media Player no proporciona métodos para transferir medios digitales a un dispositivo.
-   **Sincronización automática.** El usuario especifica las listas de reproducción que se sincronizan automáticamente con el dispositivo. Esta es una característica de Windows Media Player 10 o posterior. El SDK de Windows Media Player proporciona funcionalidad para administrar la sincronización automática. Esta funcionalidad está diseñada para permitirle crear una interfaz de usuario personalizada para la aplicación con el fin de especificar cómo se produce la sincronización de dispositivos y proporcionar información de estado a los usuarios.

Para que la sincronización automática funcione, debe establecerse una relación especial entre Windows Media Player y el dispositivo. Esta relación se denomina *Asociación*.

En las secciones siguientes se proporciona más información sobre la sincronización de dispositivos.

-   [Acerca de los dispositivos](about-devices.md)
-   [Acerca de las asociaciones](about-partnerships.md)
-   [Acerca del motor de sincronización](about-the-synchronization-engine.md)
-   [Acerca de la sincronización de listas de reproducción](about-playlist-synchronization.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos de Player**](about-the-player-object-model.md)
</dt> <dt>

[**Control remoto del Reproductor de Windows Media**](remoting-the-windows-media-player-control.md)
</dt> <dt>

[**Trabajar con dispositivos portátiles**](working-with-portable-devices.md)
</dt> </dl>

 

 




