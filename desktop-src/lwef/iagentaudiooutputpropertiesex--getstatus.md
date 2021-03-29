---
title: IAgentAudioOutputPropertiesEx GetStatus
description: IAgentAudioOutputPropertiesEx GetStatus
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd89f4b3d8101ff15b868551626775e6f2e341f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418865"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a>IAgentAudioOutputPropertiesEx:: GetStatus

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

Recupera el estado del canal de audio.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*
</dt> <dd>

Estado del canal de salida de audio, que puede ser uno de los siguientes valores:



| Value                                                                         | Descripción                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| **const unsigned short** **audio \_ status \_ disponible = 0;**<br/>         | El canal de salida de audio está disponible (no está ocupado).                                                              |
| **const unsigned short** **audio \_ status \_ = 1;**<br/>           | No se admite la salida de audio; por ejemplo, dado que no hay ninguna tarjeta de sonido.                             |
| **const unsigned short** **audio \_ status \_ CANTOPENAUDIO = 2;**<br/>     | No se puede abrir el canal de salida de audio (está ocupado). por ejemplo, debido a que otra aplicación está reproduciendo audio. |
| **const unsigned short** **audio \_ status \_ USERSPEAKING = 3;**<br/>      | El canal de salida de audio está ocupado porque el servidor está procesando la entrada de voz del usuario                            |
| **const unsigned short** **audio \_ status \_ CHARACTERSPEAKING = 4;**<br/> | El canal de salida de audio está ocupado porque un carácter está hablando actualmente.                                    |
| **const unsigned short** **audio \_ status \_ SROVERRIDEABLE = 5;**<br/>    | El canal de salida de audio no está ocupado, pero está esperando la entrada de voz de usuario.                                 |
| **const unsigned short** **audio \_ status \_ error = 6;**<br/>             | Hubo otro problema (desconocido) al intentar acceder al canal de salida de audio.                       |



 

</dd> </dl>

Esta configuración permite que la aplicación cliente consulte el estado del canal de salida de audio. Puede usar esta opción para determinar si el carácter debe hablar o intentar activar el modo de escucha (mediante [**IAgentCharacterEx:: Listen**](lwef.iagentcharacterex::listen_method)).

 

 





