---
title: Apertura de Waveform-Audio dispositivos de entrada
description: Apertura de Waveform-Audio dispositivos de entrada
ms.assetid: 46cdbce6-2433-433a-abd2-39e4146aa2e9
keywords:
- audio de onda, abrir dispositivos de entrada
- 'onda: interfaz de audio, abrir dispositivos de entrada'
- grabar audio de onda, abrir dispositivos de entrada
- apertura de dispositivos de entrada de audio de onda
- waveInOpen función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92b7f49b9d170ceb8ebce287025ce0e0c1c5530
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105676357"
---
# <a name="opening-waveform-audio-input-devices"></a><span data-ttu-id="211fb-108">Apertura de Waveform-Audio dispositivos de entrada</span><span class="sxs-lookup"><span data-stu-id="211fb-108">Opening Waveform-Audio Input Devices</span></span>

<span data-ttu-id="211fb-109">Use la función [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) para abrir un dispositivo de entrada de onda-audio para grabar.</span><span class="sxs-lookup"><span data-stu-id="211fb-109">Use the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function to open a waveform-audio input device for recording.</span></span> <span data-ttu-id="211fb-110">Esta función abre el dispositivo asociado al identificador de dispositivo especificado y devuelve un identificador del dispositivo abierto escribiendo el identificador de una ubicación de memoria especificada.</span><span class="sxs-lookup"><span data-stu-id="211fb-110">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle of a specified memory location.</span></span>

<span data-ttu-id="211fb-111">Algunos equipos multimedia tienen varios dispositivos de entrada de audio de onda.</span><span class="sxs-lookup"><span data-stu-id="211fb-111">Some multimedia computers have multiple waveform-audio input devices.</span></span> <span data-ttu-id="211fb-112">A menos que sepa que desea abrir un dispositivo de entrada de audio de forma de onda específico en un sistema, debe usar la \_ constante asignador de onda para el identificador de dispositivo al abrir un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="211fb-112">Unless you know you want to open a specific waveform-audio input device in a system, you should use the WAVE\_MAPPER constant for the device identifier when you open a device.</span></span> <span data-ttu-id="211fb-113">La función [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) elegirá el dispositivo en el sistema que mejor se puede registrar en el formato de datos especificado.</span><span class="sxs-lookup"><span data-stu-id="211fb-113">The [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function will choose the device in the system best able to record in the specified data format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="211fb-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="211fb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="211fb-115">Grabación de audio de onda</span><span class="sxs-lookup"><span data-stu-id="211fb-115">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 