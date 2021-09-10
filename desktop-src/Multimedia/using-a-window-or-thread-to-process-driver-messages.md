---
title: Usar una ventana o un subproceso para procesar mensajes del controlador
description: Usar una ventana o un subproceso para procesar mensajes del controlador
ms.assetid: 7a9eaaa1-d3b0-400e-8fbf-ee5fe59efc32
keywords:
- audio de forma de onda, devolución de llamada de ventana
- bloques de datos de audio, devolución de llamada de ventana
- audio de onda, devolución de llamada de subproceso
- bloques de datos de audio, devolución de llamada de subproceso
- audio de onda, procesamiento de mensajes del controlador
- bloques de datos de audio, procesamiento de mensajes del controlador
- procesar mensajes del controlador
- waveInOpen , función
- waveOutOpen , función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a147bd86b3c8045456ef9961039f645fd4023f13
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371270"
---
# <a name="using-a-window-or-thread-to-process-driver-messages"></a>Usar una ventana o un subproceso para procesar mensajes del controlador

Para usar una función de devolución de llamada de ventana, especifique la marca CALLBACK WINDOW en el parámetro fdwOpen y un identificador de ventana en la palabra de orden bajo del parámetro dwCallback de la función \_ [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) o [**waveOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)   Los mensajes del controlador se enviarán al procedimiento de ventana de la ventana identificada por el identificador en *dwCallback*.

Del mismo modo, para usar una devolución de llamada de subproceso, especifique CALLBACK THREAD y un identificador de subproceso en la llamada \_ a **waveInOpen** **o waveOutOpen.** En este caso, los mensajes se publican en el subproceso especificado en lugar de en una ventana.

Los mensajes enviados a la devolución de llamada de la ventana o subproceso son específicos del tipo de dispositivo de audio usado. Para obtener más información sobre estos mensajes, vea [Playing Waveform-Audio Files](playing-waveform-audio-files.md).

 

 