---
description: Acerca del filtro de captura de audio
ms.assetid: ff345670-5a75-40d3-a228-8bc22aa76708
title: Acerca del filtro de captura de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5e28bef37ca52f0a33fc95b6d2a387cbbe2fb3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152589"
---
# <a name="about-the-audio-capture-filter"></a><span data-ttu-id="df88a-103">Acerca del filtro de captura de audio</span><span class="sxs-lookup"><span data-stu-id="df88a-103">About the Audio Capture Filter</span></span>

<span data-ttu-id="df88a-104">DirectShow habilita la captura de las entradas analógicas en una tarjeta de sonido a través del [filtro de captura de audio](audio-capture-filter.md).</span><span class="sxs-lookup"><span data-stu-id="df88a-104">DirectShow enables capture from the analog inputs on a sound card through the [Audio Capture Filter](audio-capture-filter.md).</span></span> <span data-ttu-id="df88a-105">Este filtro usa las API de Wave *XXX* para controlar cualquier dispositivo cuyo controlador admita estas API.</span><span class="sxs-lookup"><span data-stu-id="df88a-105">This filter uses the waveIn *XXX* APIs to control any device whose driver supports these APIs.</span></span> <span data-ttu-id="df88a-106">Cada tarjeta del sistema se representa mediante una instancia independiente del filtro.</span><span class="sxs-lookup"><span data-stu-id="df88a-106">Each card on the system is represented by a separate instance of the filter.</span></span>

<span data-ttu-id="df88a-107">El filtro de captura de audio expone cada entrada de la tarjeta, como el micrófono o la entrada MIDI, como un PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="df88a-107">The Audio Capture filter exposes each input on the card, such as the microphone or the MIDI input, as an input pin.</span></span> <span data-ttu-id="df88a-108">Los pin de entrada representan lo que el controlador expone como líneas de origen de audio.</span><span class="sxs-lookup"><span data-stu-id="df88a-108">The input pins represent what the driver exposes as audio source lines.</span></span> <span data-ttu-id="df88a-109">Sin embargo, los datos no viajan a través de estos PIN de entrada y no se conectan a otros filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="df88a-109">No data travels through these input pins, however, and they do not connect to other DirectShow filters.</span></span> <span data-ttu-id="df88a-110">Simplemente proporcionan una manera para que una aplicación controle las entradas.</span><span class="sxs-lookup"><span data-stu-id="df88a-110">They simply provide a way for an application to control the inputs.</span></span> <span data-ttu-id="df88a-111">La aplicación puede usar un PIN de entrada para habilitar o deshabilitar la entrada, o para establecer propiedades de mezcla como la ecualización de graves, la ecualización de agudos, la panorámica, etc.</span><span class="sxs-lookup"><span data-stu-id="df88a-111">The application can use an input pin to enable or disable the input, or to set mixing properties such as bass equalization, treble equalization, pan, and so forth.</span></span> <span data-ttu-id="df88a-112">La cantidad de control que está disponible depende del controlador.</span><span class="sxs-lookup"><span data-stu-id="df88a-112">The amount of control that is available depends on the driver.</span></span> <span data-ttu-id="df88a-113">Para comprender completamente y aprovechar las capacidades de una tarjeta de sonido determinada, necesitará la documentación del fabricante de la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="df88a-113">To fully understand and exploit the capabilities of a particular sound card, you will need the documentation from the card's manufacturer.</span></span>

> [!Note]  
> <span data-ttu-id="df88a-114">Puede capturar desde el CD-Audio entrada, pero esta secuencia de audio ya ha pasado por el convertidor digital a analógico, por lo que se producirá una pérdida de calidad de sonido del CD original.</span><span class="sxs-lookup"><span data-stu-id="df88a-114">You can capture from the CD-Audio input, but this audio stream has already gone through the digital-to-analog converter, so there will be a loss of sound quality from the original CD.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="df88a-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="df88a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df88a-116">Captura de audio</span><span class="sxs-lookup"><span data-stu-id="df88a-116">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



