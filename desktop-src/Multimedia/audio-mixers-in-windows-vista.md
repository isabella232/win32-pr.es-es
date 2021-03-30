---
title: Mezcladores de audio en Windows Vista
description: Mezcladores de audio en Windows Vista
ms.assetid: 541cb5f3-b5ca-436f-88dd-6ef8459c6157
keywords:
- audio multimedia, mezcladores de audio de Windows Vista
- audio, mezcladores de audio de Windows Vista
- Mezcladores de audio, Windows Vista
- mezcladores, Windows Vista
- Mezcladores de audio de Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0610e9f16e13c19a253fbd9f6fac5ef452fa68ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104555495"
---
# <a name="audio-mixers-in-windows-vista"></a><span data-ttu-id="d0c4b-108">Mezcladores de audio en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0c4b-108">Audio Mixers in Windows Vista</span></span>

<span data-ttu-id="d0c4b-109">A partir de Windows Vista, algunos controles de mezclador se implementan en software en lugar de hardware.</span><span class="sxs-lookup"><span data-stu-id="d0c4b-109">Starting in Windows Vista, some mixer controls are implemented in software rather than hardware.</span></span> <span data-ttu-id="d0c4b-110">Por ejemplo, los controles de volumen se implementan mediante la API de sesión de audio de Windows (WASAPI).</span><span class="sxs-lookup"><span data-stu-id="d0c4b-110">For example, the volume controls are implemented using the Windows audio session API (WASAPI).</span></span> <span data-ttu-id="d0c4b-111">Estos controles no afectan directamente a la configuración de hardware.</span><span class="sxs-lookup"><span data-stu-id="d0c4b-111">These controls do not directly affect hardware settings.</span></span> <span data-ttu-id="d0c4b-112">Además, están asociados a una sesión de audio específica del proceso, por lo que los cambios afectan a la aplicación que realiza la llamada, pero no afectan a otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d0c4b-112">In addition, they are associated with a process-specific audio session, so changes affect the calling application but do not affect other applications.</span></span>

<span data-ttu-id="d0c4b-113">Cada dispositivo de punto de conexión de audio tiene un diseño de mezclador estándar, que se implementa en software.</span><span class="sxs-lookup"><span data-stu-id="d0c4b-113">Each audio endpoint device has a standard mixer layout, implemented in software.</span></span>

-   <span data-ttu-id="d0c4b-114">Cada extremo de representación de audio contiene una línea de destino que contiene lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d0c4b-114">Each audio rendering endpoint contains one destination line that contains the following:</span></span>
    -   <span data-ttu-id="d0c4b-115">Control de volumen</span><span class="sxs-lookup"><span data-stu-id="d0c4b-115">Volume control</span></span>
    -   <span data-ttu-id="d0c4b-116">Silenciar control</span><span class="sxs-lookup"><span data-stu-id="d0c4b-116">Mute control</span></span>
    -   <span data-ttu-id="d0c4b-117">Línea de código fuente: de onda-salida de audio.</span><span class="sxs-lookup"><span data-stu-id="d0c4b-117">Source line: Waveform-audio output.</span></span>
    -   <span data-ttu-id="d0c4b-118">Línea de código fuente: CD de audio.</span><span class="sxs-lookup"><span data-stu-id="d0c4b-118">Source line: Audio CD.</span></span>
-   <span data-ttu-id="d0c4b-119">Cada extremo de captura de audio contiene una línea de destino que contiene lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d0c4b-119">Each audio capture endpoint contains one destination line that contains the following:</span></span>
    -   <span data-ttu-id="d0c4b-120">Control de volumen</span><span class="sxs-lookup"><span data-stu-id="d0c4b-120">Volume control</span></span>
    -   <span data-ttu-id="d0c4b-121">Silenciar control</span><span class="sxs-lookup"><span data-stu-id="d0c4b-121">Mute control</span></span>
    -   <span data-ttu-id="d0c4b-122">Línea de código fuente: onda de entrada de audio.</span><span class="sxs-lookup"><span data-stu-id="d0c4b-122">Source line: Waveform-audio input.</span></span> <span data-ttu-id="d0c4b-123">El tipo de componente depende del dispositivo de entrada, por ejemplo, un micrófono.</span><span class="sxs-lookup"><span data-stu-id="d0c4b-123">The component type depends on the input device— for example, a microphone.</span></span>

<span data-ttu-id="d0c4b-124">Cada línea de código fuente contiene un control de volumen y un control de silencio.</span><span class="sxs-lookup"><span data-stu-id="d0c4b-124">Each source line contains a volume control and a mute control.</span></span> <span data-ttu-id="d0c4b-125">En el diagrama siguiente se muestran los componentes de los extremos de representación y de captura.</span><span class="sxs-lookup"><span data-stu-id="d0c4b-125">The following diagram shows the components of render endpoints and capture endpoints.</span></span>

![diseños de mezclador predeterminados](images/mixer1.gif)

<span data-ttu-id="d0c4b-127">Todos los controles de un extremo manipulan el mismo control de software subyacente.</span><span class="sxs-lookup"><span data-stu-id="d0c4b-127">All of the controls for an endpoint manipulate the same underlying software control.</span></span> <span data-ttu-id="d0c4b-128">Por lo tanto, si cambia la configuración de un control, recibirá una notificación de cambio de control en los otros controles.</span><span class="sxs-lookup"><span data-stu-id="d0c4b-128">Therefore, if you change the settings on one control, you will receive a control change notification on the other controls.</span></span> <span data-ttu-id="d0c4b-129">(Vea [**el \_ \_ \_ cambio de control mm MIXM**](mm-mixm-control-change.md)).</span><span class="sxs-lookup"><span data-stu-id="d0c4b-129">(See [**MM\_MIXM\_CONTROL\_CHANGE**](mm-mixm-control-change.md).)</span></span>

<span data-ttu-id="d0c4b-130">Este diseño estándar se proporciona por compatibilidad con las aplicaciones existentes que utilizan las funciones del mezclador de audio.</span><span class="sxs-lookup"><span data-stu-id="d0c4b-130">This standard layout is provided for compatibility with existing applications that use the audio mixer functions.</span></span> <span data-ttu-id="d0c4b-131">Las nuevas aplicaciones deben evitar el uso de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="d0c4b-131">New applications should avoid using these functions.</span></span>

 

 




