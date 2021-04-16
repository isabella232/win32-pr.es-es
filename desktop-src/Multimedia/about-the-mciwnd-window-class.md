---
title: Acerca de la clase de ventana MCIWnd
description: Acerca de la clase de ventana MCIWnd
ms.assetid: 7dde7346-5853-4c8f-8788-bf74d01ece83
keywords:
- Clase de ventana MCIWnd, acerca de
- MCIWndCreate función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e459a0e7d93543af126287a776b64130595ad11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418745"
---
# <a name="about-the-mciwnd-window-class"></a><span data-ttu-id="c3261-105">Acerca de la clase de ventana MCIWnd</span><span class="sxs-lookup"><span data-stu-id="c3261-105">About the MCIWnd Window Class</span></span>

<span data-ttu-id="c3261-106">La clase de ventana MCIWnd es fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="c3261-106">The MCIWnd Window class is easy to use.</span></span> <span data-ttu-id="c3261-107">Mediante el uso de una única función, [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) la aplicación puede crear un control que reproduzca cualquier dispositivo que use la interfaz de control de medios (MCI).</span><span class="sxs-lookup"><span data-stu-id="c3261-107">By using a single function, [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) your application can create a control that plays any device that uses the media control interface (MCI).</span></span> <span data-ttu-id="c3261-108">Estos dispositivos incluyen dispositivos de audio de CD, audio de onda, MIDI y vídeo.</span><span class="sxs-lookup"><span data-stu-id="c3261-108">These devices include CD audio, waveform-audio, MIDI, and video devices.</span></span>

<span data-ttu-id="c3261-109">La automatización de la reproducción también es rápida y sencilla.</span><span class="sxs-lookup"><span data-stu-id="c3261-109">Automating playback is also quick and easy.</span></span> <span data-ttu-id="c3261-110">Con solo una función y dos macros, una aplicación puede crear una ventana de MCIWnd con el dispositivo multimedia adecuado, reproducir el dispositivo y cerrar el dispositivo y la ventana cuando el contenido haya terminado de reproducirse.</span><span class="sxs-lookup"><span data-stu-id="c3261-110">Using only one function and two macros, an application can create an MCIWnd window with the appropriate media device, play the device, and close both the device and the window when the content has finished playing.</span></span>

> [!Note]  
> <span data-ttu-id="c3261-111">Algunos dispositivos reproducen contenido almacenado en archivos.</span><span class="sxs-lookup"><span data-stu-id="c3261-111">Some devices play content that is stored in files.</span></span> <span data-ttu-id="c3261-112">Otros dispositivos, como los dispositivos de audio de CD, reproducen el contenido que se almacena en otro medio.</span><span class="sxs-lookup"><span data-stu-id="c3261-112">Other devices, such as CD audio devices, play content that is stored in another medium.</span></span> <span data-ttu-id="c3261-113">A efectos de claridad, en esta información general se hace referencia a ambas circunstancias como "reproduciendo el dispositivo".</span><span class="sxs-lookup"><span data-stu-id="c3261-113">For purposes of clarity, this overview refers to both circumstances as "playing the device."</span></span>

 

 

 




