---
title: Usar una ventana o un subproceso para procesar mensajes de controlador
description: Usar una ventana o un subproceso para procesar mensajes de controlador
ms.assetid: 7a9eaaa1-d3b0-400e-8fbf-ee5fe59efc32
keywords:
- audio de onda, devolución de llamada de ventana
- bloques de datos de audio, devolución de llamada de ventana
- audio de onda, devolución de llamada de subproceso
- bloques de datos de audio, devolución de llamada de subproceso
- audio de forma de onda, procesamiento de mensajes de controlador
- bloques de datos de audio, procesar mensajes de controlador
- procesar mensajes de controlador
- waveInOpen función)
- waveOutOpen función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a147bd86b3c8045456ef9961039f645fd4023f13
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995249"
---
# <a name="using-a-window-or-thread-to-process-driver-messages"></a><span data-ttu-id="2ebaf-112">Usar una ventana o un subproceso para procesar mensajes de controlador</span><span class="sxs-lookup"><span data-stu-id="2ebaf-112">Using a Window or Thread to Process Driver Messages</span></span>

<span data-ttu-id="2ebaf-113">Para usar una función de devolución de llamada de ventana, especifique la marca de la ventana de devolución de llamada \_ en el parámetro *fdwOpen* y un identificador de ventana en la palabra de orden inferior del parámetro *DwCallback* de la función [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) o [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .</span><span class="sxs-lookup"><span data-stu-id="2ebaf-113">To use a window callback function, specify the CALLBACK\_WINDOW flag in the *fdwOpen* parameter and a window handle in the low-order word of the *dwCallback* parameter of the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) or [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span> <span data-ttu-id="2ebaf-114">Los mensajes del controlador se enviarán al procedimiento de ventana de la ventana identificada por el identificador de *dwCallback*.</span><span class="sxs-lookup"><span data-stu-id="2ebaf-114">Driver messages will be sent to the window procedure for the window identified by the handle in *dwCallback*.</span></span>

<span data-ttu-id="2ebaf-115">Del mismo modo, para usar una devolución de llamada de subproceso, especifique \_ el subproceso de devolución de llamada y un identificador de subproceso en la llamada a **WaveInOpen** o **waveOutOpen**.</span><span class="sxs-lookup"><span data-stu-id="2ebaf-115">Similarly, to use a thread callback, specify CALLBACK\_THREAD and a thread handle in the call to **waveInOpen** or **waveOutOpen**.</span></span> <span data-ttu-id="2ebaf-116">En este caso, los mensajes se publican en el subproceso especificado en lugar de en una ventana.</span><span class="sxs-lookup"><span data-stu-id="2ebaf-116">In this case, messages are posted to the specified thread instead of to a window.</span></span>

<span data-ttu-id="2ebaf-117">Los mensajes enviados a la devolución de llamada de la ventana o del subproceso son específicos del tipo de dispositivo de audio usado.</span><span class="sxs-lookup"><span data-stu-id="2ebaf-117">Messages sent to the window or thread callback are specific to the audio device type used.</span></span> <span data-ttu-id="2ebaf-118">Para obtener más información acerca de estos mensajes, vea [reproducir archivos Waveform-Audio](playing-waveform-audio-files.md).</span><span class="sxs-lookup"><span data-stu-id="2ebaf-118">For more information about these messages, see [Playing Waveform-Audio Files](playing-waveform-audio-files.md).</span></span>

 

 