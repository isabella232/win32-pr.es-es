---
title: Usar una función de devolución de llamada para procesar mensajes del controlador
description: Usar una función de devolución de llamada para procesar mensajes del controlador
ms.assetid: 7fef400f-5040-4d33-9a2f-bb12aa9369e0
keywords:
- audio de forma de onda, funciones de devolución de llamada
- bloques de datos de audio, funciones de devolución de llamada
- audio de forma de onda, procesamiento de mensajes del controlador
- bloques de datos de audio, procesamiento de mensajes del controlador
- procesar mensajes del controlador
- función waveInOpen
- waveOutOpen ( Función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf386c517d900fc4b0450f169060c6be6365df57ab0fcb3e6953337f4f67fbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892435"
---
# <a name="using-a-callback-function-to-process-driver-messages"></a>Usar una función de devolución de llamada para procesar mensajes del controlador

Puede escribir su propia función de devolución de llamada para procesar los mensajes enviados por el controlador de dispositivo. Para usar una función de devolución de llamada, especifique la marca CALLBACK FUNCTION en el parámetro fdwOpen y la dirección de la devolución de llamada en el parámetro dwCallback de la función \_ [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) o [**waveOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)  

Los mensajes enviados a una función de devolución de llamada son similares a los mensajes enviados a una ventana, salvo que tienen dos parámetros **DWORD** en lugar de **un UINT** y un **parámetro DWORD.** Para obtener más información sobre estos mensajes, vea [Playing Waveform-Audio Files](playing-waveform-audio-files.md).

Para pasar datos de instancia de una aplicación a una función de devolución de llamada, use una de las técnicas siguientes:

-   Pase los datos de instancia mediante el *parámetro dwInstance* de la función que abre el controlador de dispositivo.
-   Pase los datos de instancia mediante el **miembro dwUser** de la [**estructura WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica un bloque de datos de audio que se envía a un controlador de dispositivo.

Si necesita más de 32 bits de datos de instancia, pase un puntero a una estructura que contenga la información adicional.

 

 