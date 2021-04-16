---
title: Abrir dispositivos de salida MIDI
description: Abrir dispositivos de salida MIDI
ms.assetid: 0a06611b-c0cd-4884-bc17-761c4aec4418
keywords:
- Interfaz digital de instrumentos musicales (MIDI), dispositivos de salida
- MIDI (interfaz digital de instrumentos musicales), dispositivos de salida
- reproducir archivos MIDI, dispositivos de salida
- Dispositivos de salida MIDI
- Interfaz digital de instrumentos musicales (MIDI), abrir dispositivos de salida
- MIDI (interfaz digital de instrumentos musicales), abrir dispositivos de salida
- reproducir archivos MIDI, abrir dispositivos de salida
- abrir dispositivos de salida MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca7a7e1db461b29700ec7c7c61ee140073bc345
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487643"
---
# <a name="opening-midi-output-devices"></a><span data-ttu-id="eb24f-111">Abrir dispositivos de salida MIDI</span><span class="sxs-lookup"><span data-stu-id="eb24f-111">Opening MIDI Output Devices</span></span>

<span data-ttu-id="eb24f-112">Para abrir un dispositivo de salida MIDI para la reproducción, utilice la función [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="eb24f-112">To open a MIDI output device for playback, use the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span> <span data-ttu-id="eb24f-113">Esta función abre el dispositivo asociado al identificador de dispositivo especificado y devuelve un identificador del dispositivo abierto escribiendo el identificador en una ubicación de memoria especificada.</span><span class="sxs-lookup"><span data-stu-id="eb24f-113">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle to a specified memory location.</span></span>

<span data-ttu-id="eb24f-114">Uno de los parámetros de **midiOutOpen** es un valor de palabra.</span><span class="sxs-lookup"><span data-stu-id="eb24f-114">One of the parameters of **midiOutOpen** is a doubleword value.</span></span> <span data-ttu-id="eb24f-115">Este valor especifica un identificador de ventana o de subproceso, un identificador de evento o la dirección de una función de devolución de llamada que se usa para supervisar el progreso de la reproducción de datos y búferes de secuencia exclusivos del sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="eb24f-115">This value specifies a window or thread handle, an event handle, or the address of a callback function that is used to monitor the progress of the playback of MIDI system-exclusive data and stream buffers.</span></span> <span data-ttu-id="eb24f-116">La supervisión permite a la aplicación determinar cuándo se deben enviar bloques de datos adicionales y cuándo liberar los bloques de datos que se han enviado.</span><span class="sxs-lookup"><span data-stu-id="eb24f-116">Monitoring enables the application to determine when to send additional data blocks and when to free data blocks that have been sent.</span></span> <span data-ttu-id="eb24f-117">Para obtener más información acerca de estos métodos, consulte [administrar bloques de datos MIDI](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="eb24f-117">For more information about these methods, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

 

 