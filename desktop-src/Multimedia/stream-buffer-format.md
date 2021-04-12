---
title: Formato de búfer de secuencia
description: Formato de búfer de secuencia
ms.assetid: 4b24c12e-b43f-492e-a000-af4f59d5e16f
keywords:
- Interfaz digital de instrumentos musicales (MIDI), búferes de secuencia
- MIDI (interfaz digital de instrumentos musicales), búferes de secuencia
- búferes de secuencia, formato
- Estructura MIDIHDR
- Estructura MIDIEVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a7f0dbeabd0d7aebeae0387af415a831e4658
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420543"
---
# <a name="stream-buffer-format"></a>Formato de búfer de secuencia

El miembro **lpData** de la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) apunta a un búfer de flujo y el miembro **dwBufferLength** especifica el tamaño real de este búfer. El miembro **dwBytesRecorded** de **MIDIHDR** especifica el número de bytes en el búfer que se usan realmente en los eventos MIDI; Este valor debe ser menor o igual que el valor especificado por **dwBufferLength**.

Cada uno de los eventos MIDI del búfer de secuencia se especifica mediante una estructura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) , que contiene la hora del evento, un identificador de flujo, un código de evento y, cuando corresponde, parámetros para el evento. Cada una de estas estructuras **MIDIEVENT** debe comenzar en un límite palabra. Si es necesario, se deben agregar los bytes de relleno al final de la estructura para asegurarse de que el siguiente se inicia en un límite de palabra.

 

 