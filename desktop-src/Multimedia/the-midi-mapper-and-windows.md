---
title: El asignador de MIDI y Windows
description: El asignador de MIDI y Windows
ms.assetid: a077f935-e085-4148-9975-7926ac018f0c
keywords:
- Interfaz digital de instrumentos musicales (MIDI), asignador MIDI
- MIDI (interfaz digital de instrumentos musicales), asignador MIDI
- Asignador de MIDI, arquitectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad3cee4fb37de6ecbfdc4f81860afcb9f589d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077685"
---
# <a name="the-midi-mapper-and-windows"></a><span data-ttu-id="61200-106">El asignador de MIDI y Windows</span><span class="sxs-lookup"><span data-stu-id="61200-106">The MIDI Mapper and Windows</span></span>

<span data-ttu-id="61200-107">El asignador MIDI forma parte del software del sistema.</span><span class="sxs-lookup"><span data-stu-id="61200-107">The MIDI Mapper is part of the system software.</span></span> <span data-ttu-id="61200-108">En la ilustración siguiente se muestra cómo se relaciona el asignador MIDI con otros elementos de los servicios de audio.</span><span class="sxs-lookup"><span data-stu-id="61200-108">The following illustration shows how the MIDI Mapper relates to other elements of the audio services.</span></span>

![Cómo se relaciona el asignador MIDI con otros elementos de la imagen de servicios de audio](images/mmap-a01.gif)

<span data-ttu-id="61200-110">Desde el punto de vista de una aplicación, el asignador MIDI es similar a otro dispositivo de salida MIDI.</span><span class="sxs-lookup"><span data-stu-id="61200-110">From the viewpoint of an application, the MIDI Mapper looks like another MIDI output device.</span></span> <span data-ttu-id="61200-111">El asignador MIDI recibe mensajes enviados por las funciones de salida MIDI de bajo nivel [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) y [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg).</span><span class="sxs-lookup"><span data-stu-id="61200-111">The MIDI Mapper receives messages sent to it by the low-level MIDI output functions [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) and [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg).</span></span> <span data-ttu-id="61200-112">El asignador MIDI modifica estos mensajes y los redirige a un dispositivo de salida MIDI según el mapa de configuración de MIDI actual.</span><span class="sxs-lookup"><span data-stu-id="61200-112">The MIDI Mapper modifies these messages and redirects them to a MIDI output device according to the current MIDI setup map.</span></span> <span data-ttu-id="61200-113">El usuario selecciona el mapa de configuración de MIDI actual por medio de la opción del panel de control de MIDI.</span><span class="sxs-lookup"><span data-stu-id="61200-113">The current MIDI setup map is selected by the user by means of the MIDI Control Panel option.</span></span> <span data-ttu-id="61200-114">Solo el usuario puede seleccionar el mapa de instalación actual; las aplicaciones no pueden cambiar el mapa de instalación actual.</span><span class="sxs-lookup"><span data-stu-id="61200-114">Only the user can select the current setup map; applications cannot change the current setup map.</span></span>

 

 