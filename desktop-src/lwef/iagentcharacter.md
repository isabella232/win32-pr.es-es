---
title: IAgentCharacter
description: IAgentCharacter
ms.assetid: 77d0ffc2-76a2-4a21-88e1-1ca85b8c5d2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f0a56272ba095f244e48e335049ec5b88b64855
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704741"
---
# <a name="iagentcharacter"></a>IAgentCharacter

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

**IAgentCharacter** define una interfaz que permite a las aplicaciones consultar propiedades de caracteres y reproducir animaciones. Estas funciones también están disponibles en [**IAgentCharacterEx**](iagentcharacterex.md). Puede usar algunos identificadores de solicitud de devolución de método para realizar un seguimiento de su estado en la cola del carácter y sincronizar el código con el estado de animación actual del carácter.

**Métodos en orden de Vtable**



| Métodos IAgentCharacter                                           | Descripción                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**GetVisible**](iagentcharacter--getvisible.md)                 | Devuelve si el carácter (marco) está actualmente visible.                       |
| [**SetPosition**](iagentcharacter--setposition.md)               | Establece la posición del marco de caracteres.                                         |
| [**GetPosition**](iagentcharacter--getposition.md)               | Devuelve la posición del marco de caracteres.                                      |
| [**SetSize**](iagentcharacter--setsize.md)                       | Establece el tamaño del marco de caracteres.                                             |
| [**GetSize (**](iagentcharacter--getsize.md)                       | Devuelve el tamaño del marco de caracteres.                                          |
| [**GetName**](iagentcharacter--getname.md)                       | Devuelve el nombre del carácter.                                                |
| [**GetDescription**](iagentcharacter--getdescription.md)         | Devuelve la descripción del carácter.                                        |
| [**GetTTSSpeed**](iagentcharacter--getttsspeed.md)               | Devuelve la configuración de velocidad de salida TTS actual para el carácter.                   |
| [**GetTTSPitch**](iagentcharacter--getttspitch.md)               | Devuelve el valor actual del tono TTS para el carácter.                          |
| [**Activar**](iagentcharacter--activate.md)                     | Establece si un cliente está activo o un carácter es el nivel superior.                        |
| [**SetIdleOn**](iagentcharacter--setidleon.md)                   | Establece el procesamiento inactivo del servidor.                                                |
| [**GetIdleOn**](iagentcharacter--getidleon.md)                   | Devuelve el valor del procesamiento inactivo del servidor.                              |
| [**Preparación**](iagentcharacter--prepare.md)                       | Recupera los datos de animación para el carácter.                                       |
| [**Reproducir**](iagentcharacter--play.md)                             | Reproduce una animación especificada.                                                      |
| [**Stop**](iagentcharacter--stop.md)                             | Detiene una animación para un carácter.                                               |
| [**StopAll**](iagentcharacter--stopall.md)                       | Detiene todas las animaciones de un carácter.                                             |
| [**Esperar**](iagentcharacter--wait.md)                             | Contiene la cola de animaciones del carácter.                                            |
| [**Interrupción**](iagentcharacter--interrupt.md)                   | Interrumpe la animación de un carácter.                                               |
| [**Feria**](iagentcharacter--show.md)                             | Muestra el carácter y reproduce la animación de estado **que muestra** el carácter.     |
| [**Ocultar**](iagentcharacter--hide.md)                             | Reproduce la animación del estado **ocultando** del carácter y oculta el fotograma del carácter. |
| [**Speak**](iagentcharacter--speak.md)                           | Reproduce la salida de voz para el carácter.                                            |
| [**MoveTo**](iagentcharacter--moveto.md)                         | Mueve el marco de caracteres a la ubicación especificada.                              |
| [**GestureAt**](iagentcharacter--gestureat.md)                   | Reproduce una animación gesturing basándose en la ubicación especificada.                      |
| [**GetMoveCause**](iagentcharacter--getmovecause.md)             | Recupera la causa del último movimiento del carácter.                                 |
| [**GetVisibilityCause**](iagentcharacter--getvisibilitycause.md) | Recupera la causa del último cambio en el estado de visibilidad del carácter.       |
| [**HasOtherClients**](iagentcharacter--hasotherclients.md)       | Recupera si el carácter tiene otros clientes actuales.                        |
| [**SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md)   | Determina si se reproducen los efectos sonoros de una animación de caracteres.                    |
| [**GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md)   | Recupera si está habilitada la configuración de efectos sonoros de un carácter.                 |
| [**SetName**](iagentcharacter--setname.md)                       | Establece el nombre del carácter.                                                        |
| [**SetDescription**](iagentcharacter--setdescription.md)         | Establece la descripción del carácter.                                                 |
| [**GetExtraData**](iagentcharacter--getextradata.md)             | Recupera datos adicionales almacenados con el carácter.                              |



 

 

 




