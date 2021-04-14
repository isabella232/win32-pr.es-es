---
title: Uso de mensajes de ventana para administrar la grabación de Waveform-Audio
description: Uso de mensajes de ventana para administrar la grabación de Waveform-Audio
ms.assetid: 65637d51-9d30-48db-8681-48332442130e
keywords:
- audio de onda, administración de grabaciones con mensajes
- 'onda: interfaz de audio, administración de grabaciones con mensajes'
- grabación de audio de onda y administración de grabaciones con mensajes
- audio de una onda, mensajes
- 'onda: interfaz de audio, mensajes'
- grabar audio de onda de onda, mensajes
- Mensaje MM_WIM_CLOSE
- Mensaje MM_WIM_DATA
- Mensaje MM_WIM_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70bb1cfe1ed0f7ba6052fc1eb6af8fca8355d87d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487579"
---
# <a name="using-window-messages-to-manage-waveform-audio-recording"></a>Uso de mensajes de ventana para administrar la grabación de Waveform-Audio

Los siguientes mensajes se pueden enviar a una función de procedimiento de ventana para la administración de la grabación de audio de onda.



| Message                                | Descripción                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ - \_ cerrar Wim**](mm-wim-close.md) | Se envía cuando el dispositivo se cierra con la función [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) .                                     |
| [**\_datos Wim \_ mm**](mm-wim-data.md)   | Se envía cuando el controlador de dispositivo finaliza con un búfer enviado mediante la función [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) . |
| [**MM \_ Wim \_ abierto**](mm-wim-open.md)   | Se envía cuando el dispositivo se abre con la función [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) .                                       |



 

El parámetro *lParam* de [**\_ \_ datos Wim mm**](mm-wim-data.md) especifica un puntero a una estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica el búfer. Este búfer no se puede rellenar completamente con datos de audio de forma de onda; la grabación puede detenerse antes de que se llene el búfer. Use el miembro **dwBytesRecorded** de la estructura **WAVEHDR** para determinar la cantidad de datos válidos presentes en el búfer.

El mensaje más útil es probablemente [**\_ \_ datos Wim de mm**](mm-wim-data.md). Cuando la aplicación termina de usar el bloque de datos enviado por el controlador de dispositivo, puede limpiar y liberar el bloque de datos. A menos que necesite asignar memoria o inicializar variables, es probable que no necesite usar los mensajes [**mm \_ Wim \_ Open**](mm-wim-open.md) y [**mm \_ \_ Close**](mm-wim-close.md) .

La aplicación proporciona la función de devolución de llamada para dispositivos de entrada de audio de forma de onda. Para obtener información sobre esta función de devolución de llamada, vea la función [**waveInProc**](/previous-versions//dd743849(v=vs.85)) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio de onda](recording-waveform-audio.md)
</dt> </dl>

 

 