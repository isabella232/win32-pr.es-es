---
title: Usar una devolución de llamada de evento para procesar mensajes del controlador
description: Usar una devolución de llamada de evento para procesar mensajes del controlador
ms.assetid: 5b17ff93-ed00-46ee-828c-baf716c9257c
keywords:
- audio de forma de onda, devolución de llamada de eventos
- bloques de datos de audio, devolución de llamada de eventos
- audio de forma de onda, procesamiento de mensajes del controlador
- bloques de datos de audio, procesamiento de mensajes del controlador
- procesar mensajes del controlador
- Función CreateEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbfeb95fcf0e5d83f9a54fc0cf3cd223ac6ce19
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371269"
---
# <a name="using-an-event-callback-to-process-driver-messages"></a>Usar una devolución de llamada de evento para procesar mensajes del controlador

Para usar una devolución de llamada de evento, use [**la función CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) para crear un evento de restablecimiento manual. En la llamada a la [**función waveOutOpen,**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) especifique **CALLBACK \_ EVENT** para el *parámetro fdwOpen.* Después de llamar a la función [**waveOutPrepareHeader,**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) pero antes de enviar datos de audio de forma de onda al dispositivo, coloque el evento en un estado sin signo llamando a la [**función ResetEvent.**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) A continuación, dentro de un bucle que comprueba si la marca **WHDR \_ DONE** está establecida en el **miembro dwFlags** de la estructura [**WAVEHDR,**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) llame a la [función WaitForSingleObject,](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) especificando como parámetros el identificador del evento y un valor de tiempo de espera.

Dado que las devoluciones de llamada de eventos no reciben notificaciones específicas de cierre, realización o apertura, es posible que una aplicación tenga que comprobar el estado del proceso que está esperando después de que se produzca el evento. Es posible que se hayan completado varias tareas en el momento en que [**waitForSingleObject devuelve**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Bloques de datos de audio](audio-data-blocks.md)
</dt> </dl>

 

 