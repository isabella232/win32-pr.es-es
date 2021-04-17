---
title: Información general del ejemplo echo
description: Información general del ejemplo echo
ms.assetid: df9ad8f4-8c17-44b8-b5ee-c86de44788cf
keywords:
- Complementos de Media Player de Windows, información general de ejemplo de eco
- complementos, información general de ejemplo de eco
- Complementos de procesamiento de señal digital, información general de ejemplo de eco
- Complementos DSP, información general de ejemplo de eco
- Ejemplo de complemento DSP de eco, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1081b6d54ce34581bb6231d5617dd300e392ad71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695391"
---
# <a name="echo-sample-overview"></a><span data-ttu-id="54c70-108">Información general del ejemplo echo</span><span class="sxs-lookup"><span data-stu-id="54c70-108">Echo Sample Overview</span></span>

<span data-ttu-id="54c70-109">En esta guía se crea un complemento DSP de Windows Media Player que crea un efecto de eco en audio PCM durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="54c70-109">This guide builds a Windows Media Player DSP plug-in that creates an echo effect in PCM audio during playback.</span></span> <span data-ttu-id="54c70-110">Los objetivos del complemento son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="54c70-110">The goals for the plug-in are as follows:</span></span>

-   <span data-ttu-id="54c70-111">El complemento procesa únicamente audio PCM de 8 o 16 bits.</span><span class="sxs-lookup"><span data-stu-id="54c70-111">The plug-in processes 8-bit or 16-bit PCM audio only.</span></span>
-   <span data-ttu-id="54c70-112">Admite un tiempo de retraso entre 10 milisegundos (MS) y 2000 MS (2 segundos).</span><span class="sxs-lookup"><span data-stu-id="54c70-112">It supports a delay time between 10 milliseconds (ms) and 2000 ms (2 seconds).</span></span> <span data-ttu-id="54c70-113">Esto representa un intervalo práctico para la mayoría de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="54c70-113">This represents a practical range for most applications.</span></span>
-   <span data-ttu-id="54c70-114">Permite mezclar la señal original con la señal de retraso.</span><span class="sxs-lookup"><span data-stu-id="54c70-114">It supports mixing of the original signal with the delay signal.</span></span>
-   <span data-ttu-id="54c70-115">Proporciona una implementación de página de propiedades que permite al usuario proporcionar un valor para el tiempo de retraso y un valor para el porcentaje de la señal de retraso en relación con el nivel de señal de audio general.</span><span class="sxs-lookup"><span data-stu-id="54c70-115">It provides a property page implementation that allows the user to provide a value for the delay time and a value for the percentage of delay signal relative to the overall audio signal level.</span></span>
-   <span data-ttu-id="54c70-116">El código se crea modificando el ejemplo de complemento de audio DSP del Asistente para Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="54c70-116">The code is created by modifying the Windows Media Player Plug-in Wizard audio DSP plug-in sample.</span></span>

<span data-ttu-id="54c70-117">El ejemplo echo no se incluye en el SDK de Windows Media Player; es un ejemplo que se crea.</span><span class="sxs-lookup"><span data-stu-id="54c70-117">The Echo sample is not included with the Windows Media Player SDK; it is a sample that you create.</span></span> <span data-ttu-id="54c70-118">Para crear el ejemplo echo, debe empezar con el proyecto predeterminado del Asistente para complementos de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="54c70-118">To create the Echo sample, you must start with the default project from the Windows Media Player Plug-in Wizard.</span></span> <span data-ttu-id="54c70-119">Puede asignar al proyecto el nombre que desee; en esta documentación se supone que el proyecto se denomina echo.</span><span class="sxs-lookup"><span data-stu-id="54c70-119">You can name the project whatever you like; this documentation assumes the project is named Echo.</span></span> <span data-ttu-id="54c70-120">Para obtener más información acerca del uso del asistente, consulte [crear un complemento DSP](building-a-dsp-plug-in.md).</span><span class="sxs-lookup"><span data-stu-id="54c70-120">For details about using the wizard, see [Building a DSP Plug-in](building-a-dsp-plug-in.md).</span></span>

<span data-ttu-id="54c70-121">En la sección siguiente se proporciona información general sobre cómo el ejemplo crea un efecto de eco:</span><span class="sxs-lookup"><span data-stu-id="54c70-121">The following section provides an overview of how the sample creates an echo effect:</span></span>

-   [<span data-ttu-id="54c70-122">Cómo funciona el ejemplo echo</span><span class="sxs-lookup"><span data-stu-id="54c70-122">How the Echo Sample Works</span></span>](how-the-echo-sample-works.md)

## <a name="related-topics"></a><span data-ttu-id="54c70-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="54c70-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54c70-124">**El ejemplo echo**</span><span class="sxs-lookup"><span data-stu-id="54c70-124">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




