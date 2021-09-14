---
title: Asignador y Windows
description: Asignador y Windows
ms.assetid: a077f935-e085-4148-9975-7926ac018f0c
keywords:
- Interfaz digital de instrumentador de música (MIDI),Asignador de MIDI
- MIDI (Interfaz digital de instrumentador de música),Asignador DE MES
- Asignador de MIDI, arquitectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad3cee4fb37de6ecbfdc4f81860afcb9f589d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260735"
---
# <a name="the-midi-mapper-and-windows"></a>Asignador y Windows

El asignador de MIDI forma parte del software del sistema. En la ilustración siguiente se muestra cómo se relaciona el asignador DE LÍNEA con otros elementos de los servicios de audio.

![cómo se relaciona el asignador de midi con otros elementos de la imagen de servicios de audio](images/mmap-a01.gif)

Desde el punto de vista de una aplicación, el asignador de MIDI tiene el aspecto de otro dispositivo de salida DE MIDI. El asignador de MIDI recibe los mensajes que le envían las funciones de salida DE NIVEL INFERIOR DE [**MIDI, midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) y [**midiOutLongMsg.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) El asignador de MIDI modifica estos mensajes y los redirige a un dispositivo de salida DE MIDI según el mapa de configuración actual de MIDI. El usuario selecciona el mapa de configuración actual de MIDI mediante la opción de configuración Panel de control MIDI. Solo el usuario puede seleccionar el mapa de configuración actual; las aplicaciones no pueden cambiar el mapa de configuración actual.

 

 