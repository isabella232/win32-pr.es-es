---
title: Recibir mensajes de Running-Status
description: Recibir mensajes de Running-Status
ms.assetid: 4f2e8e41-89f6-45e3-ae16-47b856f0e63e
keywords:
- Interfaz digital de instrumentos musicales (MIDI), estado de ejecución
- MIDI (interfaz digital de instrumentos musicales), estado de ejecución
- grabación de audio MIDI, estado de ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4d12a19f525a6fa673747063774bf4507d65b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418401"
---
# <a name="receiving-running-status-messages"></a><span data-ttu-id="12dc5-106">Recibir mensajes de Running-Status</span><span class="sxs-lookup"><span data-stu-id="12dc5-106">Receiving Running-Status Messages</span></span>

<span data-ttu-id="12dc5-107">La especificación de *los archivos MIDI estándar 1,0* permite el uso del *Estado de ejecución* cuando un mensaje tiene el mismo byte de estado que el mensaje anterior.</span><span class="sxs-lookup"><span data-stu-id="12dc5-107">The *Standard MIDI Files 1.0* specification allows the use of *running status* when a message has the same status byte as the previous message.</span></span> <span data-ttu-id="12dc5-108">Cuando se usa el estado de ejecución, se puede omitir el byte de estado de los mensajes posteriores.</span><span class="sxs-lookup"><span data-stu-id="12dc5-108">When running status is used, the status byte of subsequent messages can be omitted.</span></span> <span data-ttu-id="12dc5-109">Todos los controladores de dispositivos de entrada MIDI son necesarios para expandir mensajes con el estado de ejecución en mensajes completos, de modo que siempre reciba mensajes MIDI completos de un controlador de dispositivo de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="12dc5-109">All MIDI input device drivers are required to expand messages using running status into complete messages, so that you always receive complete MIDI messages from a MIDI input device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12dc5-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12dc5-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12dc5-111">Grabación de audio MIDI</span><span class="sxs-lookup"><span data-stu-id="12dc5-111">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 




