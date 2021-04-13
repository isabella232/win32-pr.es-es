---
title: Recibir mensajes de Time-Stamped MIDI
description: Recibir mensajes de Time-Stamped MIDI
ms.assetid: a91c85fe-f9c4-4cf6-b0bb-49aa8ed45644
keywords:
- Interfaz digital de instrumentos musicales (MIDI), mensajes con marca de tiempo
- MIDI (interfaz digital de instrumentos musicales), mensajes con marca de tiempo
- grabar mensajes MIDI de audio y con marca de tiempo
- mensajes MIDI con marca de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ead268c6d022f67a3607bb8a43a3d773bd7325
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358883"
---
# <a name="receiving-time-stamped-midi-messages"></a><span data-ttu-id="c3dc6-107">Recibir mensajes de Time-Stamped MIDI</span><span class="sxs-lookup"><span data-stu-id="c3dc6-107">Receiving Time-Stamped MIDI Messages</span></span>

<span data-ttu-id="c3dc6-108">Debido al retraso entre el momento en que el controlador de dispositivo recibe un mensaje MIDI y el momento en que la aplicación recibe el mensaje, los controladores de dispositivos de entrada MIDI marcan el mensaje MIDI con la hora en que se recibió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="c3dc6-108">Because of the delay between when the device driver receives a MIDI message and the time the application receives the message, MIDI input device drivers time stamp the MIDI message with the time that the message was received.</span></span> <span data-ttu-id="c3dc6-109">Las marcas de tiempo MIDI, que se definen como la hora en que se recibió el primer byte del mensaje, se especifican en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="c3dc6-109">MIDI time stamps, which are defined as the time the first byte of the message was received, are specified in milliseconds.</span></span> <span data-ttu-id="c3dc6-110">La función [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) restablece las marcas de tiempo de un dispositivo a cero.</span><span class="sxs-lookup"><span data-stu-id="c3dc6-110">The [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function resets the time stamps for a device to zero.</span></span>

<span data-ttu-id="c3dc6-111">Como se indicó anteriormente, para recibir marcas de tiempo con entrada de MIDI, debe usar una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="c3dc6-111">As stated previously, to receive time stamps with MIDI input, you must use a callback function.</span></span> <span data-ttu-id="c3dc6-112">El parámetro *dwParam2* de la función de devolución de llamada especifica la marca de tiempo para los datos asociados a los [**\_ datos de MIM**](mim-data.md) y los mensajes [**\_ LONGDATA de MIM**](mim-longdata.md) .</span><span class="sxs-lookup"><span data-stu-id="c3dc6-112">The *dwParam2* parameter of the callback function specifies the time stamp for data associated with the [**MIM\_DATA**](mim-data.md) and [**MIM\_LONGDATA**](mim-longdata.md) messages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3dc6-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c3dc6-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3dc6-114">Grabación de audio MIDI</span><span class="sxs-lookup"><span data-stu-id="c3dc6-114">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 