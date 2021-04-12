---
title: Restablecimiento de la salida MIDI
description: Restablecimiento de la salida MIDI
ms.assetid: 281a7cfa-f274-4c7a-b63a-c0573b9f1169
keywords:
- Interfaz digital de instrumentos musicales (MIDI), restablecimiento de dispositivos de salida
- MIDI (interfaz digital de instrumentos musicales), restablecimiento de dispositivos de salida
- reproducir archivos MIDI, restablecer los dispositivos de salida
- restablecimiento de dispositivos de salida
- Interfaz digital de instrumentos musicales (MIDI), dispositivos de salida
- MIDI (interfaz digital de instrumentos musicales), dispositivos de salida
- reproducir archivos MIDI, dispositivos de salida
- Dispositivos de salida MIDI
- EOX (final de exclusivo)
- fin de exclusivo (EOX)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15778fc8a1a48c34b69915aafb7e3139153b5882
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358824"
---
# <a name="resetting-midi-output"></a><span data-ttu-id="752e0-113">Restablecimiento de la salida MIDI</span><span class="sxs-lookup"><span data-stu-id="752e0-113">Resetting MIDI Output</span></span>

<span data-ttu-id="752e0-114">La función [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) desactiva todas las notas en todos los canales MIDI para un dispositivo MIDI especificado.</span><span class="sxs-lookup"><span data-stu-id="752e0-114">The [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) function turns off all notes on all MIDI channels for a specified MIDI device.</span></span> <span data-ttu-id="752e0-115">A continuación, la función marca todos los búferes exclusivos del sistema pendientes como terminados y los devuelve a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="752e0-115">Then, the function marks any pending system-exclusive buffers as done and returns them to the application.</span></span> <span data-ttu-id="752e0-116">Esta función puede ser útil en una aplicación que usa la salida MIDI para proporcionar al usuario la capacidad de restablecer la salida MIDI.</span><span class="sxs-lookup"><span data-stu-id="752e0-116">This function can be useful in an application that uses MIDI output to provide the user with the ability to reset MIDI output.</span></span>

> [!Note]  
> <span data-ttu-id="752e0-117">La finalización de un mensaje exclusivo del sistema sin enviar un byte de EOX (final de exclusión) puede causar problemas en el dispositivo receptor.</span><span class="sxs-lookup"><span data-stu-id="752e0-117">Terminating a system-exclusive message without sending an EOX (end-of-exclusive) byte can cause problems for the receiving device.</span></span> <span data-ttu-id="752e0-118">La función **midiOutReset** no envía un byte de EOX cuando finaliza un mensaje exclusivo del sistema, ya que las aplicaciones son responsables de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="752e0-118">The **midiOutReset** function does not send an EOX byte when it terminates a system-exclusive message, because applications are responsible for doing this.</span></span>

 

 

 