---
title: Usar una función de devolución de llamada para procesar mensajes de controlador
description: Usar una función de devolución de llamada para procesar mensajes de controlador
ms.assetid: 7fef400f-5040-4d33-9a2f-bb12aa9369e0
keywords:
- audio de onda, funciones de devolución de llamada
- bloques de datos de audio, funciones de devolución de llamada
- audio de forma de onda, procesamiento de mensajes de controlador
- bloques de datos de audio, procesar mensajes de controlador
- procesar mensajes de controlador
- waveInOpen función)
- waveOutOpen función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3e7541a00b43b5fb2267a17d4de8bb017823c3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665805"
---
# <a name="using-a-callback-function-to-process-driver-messages"></a>Usar una función de devolución de llamada para procesar mensajes de controlador

Puede escribir su propia función de devolución de llamada para procesar los mensajes enviados por el controlador de dispositivo. Para usar una función de devolución de llamada, especifique la marca de función de devolución de llamada \_ en el parámetro *fdwOpen* y la dirección de la devolución de llamada en el parámetro *DwCallback* de la función [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) o [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .

Los mensajes enviados a una función de devolución de llamada son similares a los mensajes enviados a una ventana, salvo que tienen dos parámetros **DWORD** en lugar de un valor de **uint** y un parámetro **DWORD** . Para obtener más información sobre estos mensajes, consulte [reproducir archivos Waveform-Audio](playing-waveform-audio-files.md).

Para pasar datos de instancia de una aplicación a una función de devolución de llamada, use una de las técnicas siguientes:

-   Pase los datos de instancia mediante el parámetro *dwInstance* de la función que abre el controlador de dispositivo.
-   Pase los datos de instancia mediante el miembro **dwUser** de la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica un bloque de datos de audio que se envía a un controlador de dispositivo.

Si necesita más de 32 bits de datos de instancia, pase un puntero a una estructura que contenga la información adicional.

 

 