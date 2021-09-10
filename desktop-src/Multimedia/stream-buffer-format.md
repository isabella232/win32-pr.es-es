---
title: Formato de búfer de secuencia
description: Formato de búfer de secuencia
ms.assetid: 4b24c12e-b43f-492e-a000-af4f59d5e16f
keywords:
- Interfaz digital instrumentable (MIDI), búferes de secuencia
- MIDI (Interfaz digital instrumenta de música), búferes de secuencia
- búferes de flujo, formato
- Estructura DE MIDIHDR
- Estructura MIDIEVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a7f0dbeabd0d7aebeae0387af415a831e4658
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371047"
---
# <a name="stream-buffer-format"></a>Formato de búfer de secuencia

El **miembro lpData** de la [**estructura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) apunta a un búfer de secuencia y el **miembro dwBufferLength** especifica el tamaño real de este búfer. El **miembro dwBytesRecorded** de **MIDIHDR** especifica el número de bytes del búfer que los eventos MIDI usan realmente; este valor debe ser menor o igual que el valor especificado por **dwBufferLength**.

Cada uno de los eventos DE MIDI del búfer de flujo se especifica mediante una estructura [**MIDIEVENT,**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) que contiene la hora del evento, un identificador de flujo, un código de evento y, cuando corresponda, parámetros para el evento. Cada una de **estas estructuras DE MIDIEVENT** debe comenzar en un límite doubleword. Si es necesario, se deben agregar bytes de relleno al final de la estructura para asegurarse de que el siguiente se inicia en un límite de doble palabra.

 

 