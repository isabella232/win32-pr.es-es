---
title: Usar una devolución de llamada de eventos para procesar mensajes del controlador
description: Usar una devolución de llamada de eventos para procesar mensajes del controlador
ms.assetid: 5b17ff93-ed00-46ee-828c-baf716c9257c
keywords:
- audio de onda, devolución de llamada de eventos
- bloques de datos de audio, devolución de llamada de eventos
- audio de onda, procesamiento de mensajes del controlador
- bloques de datos de audio, procesamiento de mensajes del controlador
- procesar mensajes del controlador
- Función CreateEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c5bdbfe46fed9fa9124a031e90af3bfefb983caf6743415d90c645afc42c6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801205"
---
# <a name="using-an-event-callback-to-process-driver-messages"></a>Usar una devolución de llamada de eventos para procesar mensajes del controlador

Para usar una devolución de llamada de eventos, use [**la función CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) para crear un evento de restablecimiento manual. En la llamada a la [**función waveOutOpen,**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) especifique **CALLBACK \_ EVENT** para el *parámetro fdwOpen.* Después de llamar a la función [**waveOutPrepareHeader,**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) pero antes de enviar datos de audio de forma de onda al dispositivo, ponga el evento en un estado sin signo llamando a la [**función ResetEvent.**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) A continuación, dentro de un bucle que comprueba si la marca **WHDR \_ DONE** está establecida en el **miembro dwFlags** de la estructura [**WAVEHDR,**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) llame a la función [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) y especifique como parámetros el identificador del evento y un valor de tiempo de espera.

Dado que las devoluciones de llamada de eventos no reciben notificaciones específicas de cierre, realización o apertura, es posible que una aplicación tenga que comprobar el estado del proceso que está esperando después de que se produzca el evento. Es posible que se hayan completado varias tareas en el momento en que [**waitForSingleObject devuelve.**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Bloques de datos de audio](audio-data-blocks.md)
</dt> </dl>

 

 