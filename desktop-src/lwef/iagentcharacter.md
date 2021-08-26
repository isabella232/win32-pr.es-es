---
title: IAgentCharacter
description: IAgentCharacter
ms.assetid: 77d0ffc2-76a2-4a21-88e1-1ca85b8c5d2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d7144c6d3379a2237d3f14c955d8052ff4d20d1ff98d9c2f2637796f8b931b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962095"
---
# <a name="iagentcharacter"></a>IAgentCharacter

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

**IAgentCharacter define** una interfaz que permite a las aplicaciones consultar propiedades de caracteres y reproducir animaciones. Estas funciones también están disponibles en [**IAgentCharacterEx**](iagentcharacterex.md). Puede usar algunos iDs de solicitud de devolución de método para realizar un seguimiento de su estado en la cola del carácter y sincronizar el código con el estado de animación actual del carácter.

**Métodos en orden de Vtable**



| Métodos IAgentCharacter                                           | Descripción                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**GetVisible**](iagentcharacter--getvisible.md)                 | Devuelve si el carácter (marco) está visible actualmente.                       |
| [**SetPosition**](iagentcharacter--setposition.md)               | Establece la posición del marco de caracteres.                                         |
| [**GetPosition**](iagentcharacter--getposition.md)               | Devuelve la posición del marco de caracteres.                                      |
| [**SetSize**](iagentcharacter--setsize.md)                       | Establece el tamaño del marco de caracteres.                                             |
| [**GetSize**](iagentcharacter--getsize.md)                       | Devuelve el tamaño del marco de caracteres.                                          |
| [**GetName**](iagentcharacter--getname.md)                       | Devuelve el nombre del carácter.                                                |
| [**GetDescription**](iagentcharacter--getdescription.md)         | Devuelve la descripción del carácter.                                        |
| [**GetTTSSpeed**](iagentcharacter--getttsspeed.md)               | Devuelve el valor actual de velocidad de salida de TTS para el carácter.                   |
| [**GetTTSPitch**](iagentcharacter--getttspitch.md)               | Devuelve la configuración actual del tono de TTS para el carácter.                          |
| [**Activar**](iagentcharacter--activate.md)                     | Establece si un cliente está activo o si un carácter está en la parte superior.                        |
| [**SetIdleOn**](iagentcharacter--setidleon.md)                   | Establece el procesamiento inactivo del servidor.                                                |
| [**GetIdleOn**](iagentcharacter--getidleon.md)                   | Devuelve la configuración del procesamiento inactivo del servidor.                              |
| [**Preparar**](iagentcharacter--prepare.md)                       | Recupera los datos de animación del carácter.                                       |
| [**Reproducir**](iagentcharacter--play.md)                             | Reproduce una animación especificada.                                                      |
| [**Stop**](iagentcharacter--stop.md)                             | Detiene una animación de un carácter.                                               |
| [**Soundmixer.stopall**](iagentcharacter--stopall.md)                       | Detiene todas las animaciones de un carácter.                                             |
| [**Esperar**](iagentcharacter--wait.md)                             | Contiene la cola de animación del carácter.                                            |
| [**Interrupción**](iagentcharacter--interrupt.md)                   | Interrumpe la animación de un carácter.                                               |
| [**Mostrar**](iagentcharacter--show.md)                             | Muestra el carácter y reproduce la animación de estado **Mostrando** del carácter.     |
| [**Ocultar**](iagentcharacter--hide.md)                             | Reproduce la animación de estado **Ocultar** del carácter y oculta el marco del carácter. |
| [**Speak**](iagentcharacter--speak.md)                           | Reproduce la salida hablada para el carácter.                                            |
| [**Moveto**](iagentcharacter--moveto.md)                         | Mueve el marco de caracteres a la ubicación especificada.                              |
| [**GestureAt**](iagentcharacter--gestureat.md)                   | Reproduce una animación gestual basada en la ubicación especificada.                      |
| [**GetMoveCause**](iagentcharacter--getmovecause.md)             | Recupera la causa del último movimiento del carácter.                                 |
| [**GetVisibilityCause**](iagentcharacter--getvisibilitycause.md) | Recupera la causa del último cambio en el estado de visibilidad del carácter.       |
| [**HasOtherClients**](iagentcharacter--hasotherclients.md)       | Recupera si el carácter tiene otros clientes actuales.                        |
| [**SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md)   | Determina si se reproducen los efectos de sonido de una animación de caracteres.                    |
| [**GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md)   | Recupera si la configuración de efectos de sonido de un carácter está habilitada.                 |
| [**SetName**](iagentcharacter--setname.md)                       | Establece el nombre del carácter.                                                        |
| [**SetDescription**](iagentcharacter--setdescription.md)         | Establece la descripción del carácter.                                                 |
| [**GetExtraData**](iagentcharacter--getextradata.md)             | Recupera datos adicionales almacenados con el carácter .                              |



 

 

 




