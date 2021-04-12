---
title: Uso de mensajes de ventana para administrar Waveform-Audio la reproducción
description: Uso de mensajes de ventana para administrar Waveform-Audio la reproducción
ms.assetid: 217968fd-4bb3-405d-a371-c129e29637ab
keywords:
- audio de onda, administración de la reproducción con mensajes
- 'onda: interfaz de audio, administración de la reproducción con mensajes'
- reproducir archivos de audio de onda, administrar la reproducción con mensajes
- audio de una onda, mensajes
- 'onda: interfaz de audio, mensajes'
- reproducción de onda-archivos de audio, mensajes
- Mensaje MM_WOM_CLOSE
- Mensaje MM_WOM_DONE
- Mensaje MM_WOM_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce02794222274e10498e31e0f38939d930ef3745
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358880"
---
# <a name="using-window-messages-to-manage-waveform-audio-playback"></a>Uso de mensajes de ventana para administrar Waveform-Audio la reproducción

Los siguientes mensajes se pueden enviar a una función de procedimiento de ventana para administrar la reproducción de audio de onda.



| Message                                | Descripción                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**cierre de MM \_ WOM \_**](mm-wom-close.md) | Se envía cuando el dispositivo se cierra con la función [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) .                                 |
| [**MM \_ WOM \_ listo**](mm-wom-done.md)   | Se envía cuando el controlador de dispositivo finaliza con un bloque de datos enviado mediante la función [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) . |
| [**MM \_ WOM \_ abierto**](mm-wom-open.md)   | Se envía cuando el dispositivo se abre con la función [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .                                   |



 

Un parámetro *wParam* y *lParam* está asociado a cada uno de estos mensajes. El parámetro *wParam* siempre especifica un identificador del dispositivo de audio de onda abierto. Para el mensaje [**mm \_ WOM \_ Done**](mm-wom-done.md) , *lParam* especifica un puntero a una estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica el bloque de datos completado. El parámetro *lParam* no se utiliza para los mensajes de apertura de [**mm \_ WOM \_**](mm-wom-close.md) y [**\_ WOM \_**](mm-wom-open.md) .

El mensaje más útil es probablemente MM \_ WOM \_ done. Cuando este mensaje indica que se ha completado la reproducción de un bloque de datos, puede limpiar y liberar el bloque de datos. A menos que necesite asignar memoria o inicializar variables, es probable que no necesite procesar los \_ mensajes mm WOM \_ Open y mm \_ WOM \_ Close.

La aplicación proporciona la función de devolución de llamada para dispositivos de salida de onda-audio. Para obtener información sobre esta función de devolución de llamada, vea la función [**waveOutProc**](/previous-versions//dd743869(v=vs.85)) .

 

 