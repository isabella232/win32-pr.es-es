---
title: Usar una devolución de llamada de evento para procesar mensajes de controlador
description: Usar una devolución de llamada de evento para procesar mensajes de controlador
ms.assetid: 5b17ff93-ed00-46ee-828c-baf716c9257c
keywords:
- audio de onda, devolución de llamada de evento
- bloques de datos de audio, devolución de llamada de evento
- audio de forma de onda, procesamiento de mensajes de controlador
- bloques de datos de audio, procesar mensajes de controlador
- procesar mensajes de controlador
- CreateEvent (función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbfeb95fcf0e5d83f9a54fc0cf3cd223ac6ce19
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790210"
---
# <a name="using-an-event-callback-to-process-driver-messages"></a>Usar una devolución de llamada de evento para procesar mensajes de controlador

Para utilizar una devolución de llamada de evento, utilice la función [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) para crear un evento de restablecimiento manual. En la llamada a la función [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) , especifique **el \_ evento de devolución de llamada** para el parámetro *fdwOpen* . Después de llamar a la función [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) , pero antes de enviar datos de audio de forma de onda al dispositivo, coloque el evento en un estado no señalizado mediante una llamada a la función [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) . Después, dentro de un bucle que comprueba si la marca de **WHDR \_ Done** está establecida en el miembro **DwFlags** de la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , llame a la función [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) y especifique como parámetros el identificador de evento y un valor de tiempo de espera.

Dado que las devoluciones de llamada de eventos no reciben notificaciones de cierre, listo o abierto específicas, es posible que una aplicación tenga que comprobar el estado del proceso que espera después de que se produzca el evento. Es posible que se haya completado una serie de tareas en el momento en que se devuelve [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Bloques de datos de audio](audio-data-blocks.md)
</dt> </dl>

 

 