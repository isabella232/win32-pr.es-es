---
title: Bloques de datos de audio
description: Bloques de datos de audio
ms.assetid: 9646e18c-294b-4532-bd5e-709d66ad31f4
keywords:
- audio multimedia, bloques de datos
- audio, bloques de datos
- audio de forma de onda, bloques de datos
- bloques de datos de audio, acerca de
- Estructura WAVEHDR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a81a5a29ec9718e7c11306b6bafc1aa20369e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062986"
---
# <a name="audio-data-blocks"></a>Bloques de datos de audio

Las [**funciones waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) y [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) requieren que las aplicaciones asignen bloques de datos para pasar a los controladores de dispositivos con fines de grabación o reproducción. Ambas funciones usan la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para describir su bloque de datos.

Antes de usar una de estas funciones para pasar un bloque de datos a un controlador de dispositivo, debe asignar memoria para el bloque de datos y la estructura de encabezado que describe el bloque de datos. Los encabezados se pueden preparar y despreparar mediante las funciones siguientes.



| Función                                                 | Descripción                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)       | Prepara un bloque de datos de entrada de audio de forma de onda.                      |
| [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)   | Limpia la preparación en un bloque de datos de entrada de audio de forma de onda.  |
| [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)     | Prepara un bloque de datos de salida de audio de forma de onda.                     |
| [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) | Limpia la preparación en un bloque de datos de salida de audio de forma de onda. |



 

Antes de pasar un bloque de datos de audio a un controlador de dispositivo, debe preparar el bloque de datos pasandolo a [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) o [**waveOutPrepareHeader.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) Cuando el controlador de dispositivo termina con el bloque de datos y lo devuelve, debe limpiar esta preparación pasando el bloque de datos a [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) o [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) antes de que se pueda liberar cualquier memoria asignada.

A menos que los datos de entrada y salida de audio de forma de onda sean lo suficientemente pequeños como para incluirse en un único bloque de datos, las aplicaciones deben proporcionar continuamente bloques de datos al controlador de dispositivo hasta que se complete la reproducción o grabación.

Incluso si se usa un único bloque de datos, una aplicación debe ser capaz de determinar cuándo finaliza un controlador de dispositivo con el bloque de datos para que la aplicación pueda liberar la memoria asociada con el bloque de datos y la estructura de encabezado. Hay varias maneras de determinar cuándo un controlador de dispositivo ha finalizado con un bloque de datos:

-   Especificando una función de devolución de llamada para recibir un mensaje enviado por el controlador cuando termine con un bloque de datos
-   Mediante una devolución de llamada de eventos
-   Especificando una ventana o subproceso para recibir un mensaje enviado por el controlador cuando termine con un bloque de datos
-   Sondear el bit WHDR \_ DONE en el miembro **dwFlags** de la [**estructura WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) enviada con cada bloque de datos

Si una aplicación no obtiene un bloque de datos para el controlador de dispositivo cuando es necesario, puede haber una brecha en la reproducción o una pérdida de información registrada entrante. Esto requiere al menos un esquema de almacenamiento en búfer doble, que se mantiene al menos un bloque de datos delante del controlador del dispositivo.

En los temas siguientes se describen maneras de determinar cuándo un controlador de dispositivo ha finalizado con un bloque de datos:

Usar una función de devolución de llamada para procesar mensajes de controlador

-   [Usar una función de devolución de llamada para procesar mensajes de controlador](using-a-callback-function-to-process-driver-messages.md)
-   [Usar una devolución de llamada de eventos para procesar mensajes del controlador](using-an-callback-to-process-driver-messages.md)
-   [Usar una ventana o un subproceso para procesar mensajes del controlador](using-a-window-or-thread-to-process-driver-messages.md)
-   [Administración de bloques de datos mediante sondeo](managing-data-blocks-by-polling.md)

 

 