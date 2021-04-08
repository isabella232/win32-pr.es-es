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
# <a name="the-midi-mapper-and-windows"></a>El asignador de MIDI y Windows

El asignador MIDI forma parte del software del sistema. En la ilustración siguiente se muestra cómo se relaciona el asignador MIDI con otros elementos de los servicios de audio.

![Cómo se relaciona el asignador MIDI con otros elementos de la imagen de servicios de audio](images/mmap-a01.gif)

Desde el punto de vista de una aplicación, el asignador MIDI es similar a otro dispositivo de salida MIDI. El asignador MIDI recibe mensajes enviados por las funciones de salida MIDI de bajo nivel [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) y [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg). El asignador MIDI modifica estos mensajes y los redirige a un dispositivo de salida MIDI según el mapa de configuración de MIDI actual. El usuario selecciona el mapa de configuración de MIDI actual por medio de la opción del panel de control de MIDI. Solo el usuario puede seleccionar el mapa de instalación actual; las aplicaciones no pueden cambiar el mapa de instalación actual.

 

 