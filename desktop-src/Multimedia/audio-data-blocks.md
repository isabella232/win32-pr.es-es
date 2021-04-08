---
title: Bloques de datos de audio
description: Bloques de datos de audio
ms.assetid: 9646e18c-294b-4532-bd5e-709d66ad31f4
keywords:
- audio multimedia, bloques de datos
- audio, bloques de datos
- audio de onda, bloques de datos
- bloques de datos de audio, acerca de
- Estructura WAVEHDR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a81a5a29ec9718e7c11306b6bafc1aa20369e5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995141"
---
# <a name="audio-data-blocks"></a>Bloques de datos de audio

Las funciones [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) y [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) requieren que las aplicaciones asignen bloques de datos para pasarlos a los controladores de dispositivos con fines de grabación o reproducción. Ambas funciones usan la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para describir su bloque de datos.

Antes de usar una de estas funciones para pasar un bloque de datos a un controlador de dispositivo, debe asignar memoria para el bloque de datos y la estructura de encabezado que describe el bloque de datos. Los encabezados se pueden preparar y no preparar mediante las siguientes funciones.



| Función                                                 | Descripción                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)       | Prepara un bloque de datos de entrada de onda-audio.                      |
| [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)   | Limpia la preparación en un bloque de datos de entrada de audio de forma de onda.  |
| [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)     | Prepara un bloque de datos de salida de onda-audio.                     |
| [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) | Limpia la preparación en un bloque de datos de salida de onda-audio. |



 

Antes de pasar un bloque de datos de audio a un controlador de dispositivo, debe preparar el bloque de datos pasándolo a [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) o [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader). Cuando el controlador de dispositivo finaliza con el bloque de datos y lo devuelve, debe limpiar esta preparación pasando el bloque de datos a [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) o [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) antes de que se pueda liberar cualquier memoria asignada.

A menos que los datos de entrada y salida de la forma de onda sean lo suficientemente pequeños como para que se incluyan en un único bloque de datos, las aplicaciones deben proporcionar continuamente el controlador de dispositivo con bloqueos de datos hasta que se complete la reproducción o grabación.

Incluso si se usa un solo bloque de datos, una aplicación debe ser capaz de determinar si un controlador de dispositivo ha terminado con el bloque de datos para que la aplicación pueda liberar la memoria asociada al bloque de datos y la estructura de encabezado. Hay varias maneras de determinar cuándo un controlador de dispositivo ha terminado con un bloque de datos:

-   Al especificar una función de devolución de llamada para recibir un mensaje enviado por el controlador cuando ha terminado con un bloque de datos
-   Mediante el uso de una devolución de llamada de evento
-   Mediante la especificación de una ventana o un subproceso para recibir un mensaje enviado por el controlador cuando ha terminado con un bloque de datos
-   Sondeando el bit WHDR \_ done en el miembro **dwFlags** de la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) enviada con cada bloque de datos

Si una aplicación no obtiene un bloque de datos para el controlador de dispositivo cuando sea necesario, puede haber un hueco audible en la reproducción o una pérdida de la información registrada entrante. Esto requiere al menos un esquema de almacenamiento en búfer doble, lo que mantiene al menos un bloque de datos antes que el controlador de dispositivo.

En los temas siguientes se describen las distintas formas de determinar cuándo un controlador de dispositivo ha terminado con un bloque de datos:

Usar una función de devolución de llamada para procesar mensajes de controlador

-   [Usar una función de devolución de llamada para procesar mensajes de controlador](using-a-callback-function-to-process-driver-messages.md)
-   [Usar una devolución de llamada de evento para procesar mensajes de controlador](using-an-callback-to-process-driver-messages.md)
-   [Usar una ventana o un subproceso para procesar mensajes de controlador](using-a-window-or-thread-to-process-driver-messages.md)
-   [Administrar bloques de datos mediante sondeo](managing-data-blocks-by-polling.md)

 

 