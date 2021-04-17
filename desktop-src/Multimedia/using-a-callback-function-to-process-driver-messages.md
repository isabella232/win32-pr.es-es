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
# <a name="using-a-callback-function-to-process-driver-messages"></a><span data-ttu-id="dd266-110">Usar una función de devolución de llamada para procesar mensajes de controlador</span><span class="sxs-lookup"><span data-stu-id="dd266-110">Using a Callback Function to Process Driver Messages</span></span>

<span data-ttu-id="dd266-111">Puede escribir su propia función de devolución de llamada para procesar los mensajes enviados por el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd266-111">You can write your own callback function to process messages sent by the device driver.</span></span> <span data-ttu-id="dd266-112">Para usar una función de devolución de llamada, especifique la marca de función de devolución de llamada \_ en el parámetro *fdwOpen* y la dirección de la devolución de llamada en el parámetro *DwCallback* de la función [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) o [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .</span><span class="sxs-lookup"><span data-stu-id="dd266-112">To use a callback function, specify the CALLBACK\_FUNCTION flag in the *fdwOpen* parameter and the address of the callback in the *dwCallback* parameter of the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) or [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span>

<span data-ttu-id="dd266-113">Los mensajes enviados a una función de devolución de llamada son similares a los mensajes enviados a una ventana, salvo que tienen dos parámetros **DWORD** en lugar de un valor de **uint** y un parámetro **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="dd266-113">Messages sent to a callback function are similar to messages sent to a window, except they have two **DWORD** parameters instead of a **UINT** and a **DWORD** parameter.</span></span> <span data-ttu-id="dd266-114">Para obtener más información sobre estos mensajes, consulte [reproducir archivos Waveform-Audio](playing-waveform-audio-files.md).</span><span class="sxs-lookup"><span data-stu-id="dd266-114">For details on these messages, see [Playing Waveform-Audio Files](playing-waveform-audio-files.md).</span></span>

<span data-ttu-id="dd266-115">Para pasar datos de instancia de una aplicación a una función de devolución de llamada, use una de las técnicas siguientes:</span><span class="sxs-lookup"><span data-stu-id="dd266-115">To pass instance data from an application to a callback function, use one of the following techniques:</span></span>

-   <span data-ttu-id="dd266-116">Pase los datos de instancia mediante el parámetro *dwInstance* de la función que abre el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd266-116">Pass the instance data using the *dwInstance* parameter of the function that opens the device driver.</span></span>
-   <span data-ttu-id="dd266-117">Pase los datos de instancia mediante el miembro **dwUser** de la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica un bloque de datos de audio que se envía a un controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd266-117">Pass the instance data using the **dwUser** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies an audio data block being sent to a device driver.</span></span>

<span data-ttu-id="dd266-118">Si necesita más de 32 bits de datos de instancia, pase un puntero a una estructura que contenga la información adicional.</span><span class="sxs-lookup"><span data-stu-id="dd266-118">If you need more than 32 bits of instance data, pass a pointer to a structure containing the additional information.</span></span>

 

 