---
title: Formato de búfer de flujo
description: Formato de búfer de flujo
ms.assetid: 4b24c12e-b43f-492e-a000-af4f59d5e16f
keywords:
- Interfaz digital de instrumentar música (MIDI), búferes de flujo
- MIDI (Interfaz digital de instrumentar música), búferes de flujo
- búferes de flujo, formato
- Estructura DE MIDIHDR
- Estructura MIDIEVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072c2541ab6b731686fc63c59b11b0dfff529ef9cab347d41fbddf13e9b60b04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688505"
---
# <a name="stream-buffer-format"></a>Formato de búfer de flujo

El **miembro lpData** de la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) apunta a un búfer de secuencia y el **miembro dwBufferLength** especifica el tamaño real de este búfer. El **miembro dwBytesRecorded** de **MIDIHDR** especifica el número de bytes del búfer que realmente usan los eventos MIDI; este valor debe ser menor o igual que el valor especificado por **dwBufferLength.**

Cada uno de los eventos DE MIDI del búfer de flujo se especifica mediante una estructura [**MIDIEVENT,**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) que contiene la hora del evento, un identificador de flujo, un código de evento y, cuando corresponda, parámetros para el evento. Cada una de estas **estructuras DE MIDIEVENT** debe comenzar en un límite doubleword. Si es necesario, se deben agregar bytes de relleno al final de la estructura para asegurarse de que el siguiente se inicia en un límite doubleword.

 

 