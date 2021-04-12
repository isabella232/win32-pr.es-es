---
title: Arquitectura de mezclador
description: Arquitectura de mezclador
ms.assetid: 11d650bf-c258-4818-88b7-9fdc71a8d859
keywords:
- audio multimedia, arquitectura de mezclador
- arquitectura de audio y mezclador
- Mezcladores de audio, arquitectura
- Mezcladores de audio, líneas de audio
- líneas de audio
- Mezcladores de audio, controles
- audio multimedia, controles de mezclador
- audio, controles de mezclador
- mezcladores, líneas de audio
- mezcladores, arquitectura
- mezcladores, controles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 447b0cdc44a33237aa7e0c726a5eb533b3bc7d0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357049"
---
# <a name="mixer-architecture"></a><span data-ttu-id="3eb40-114">Arquitectura de mezclador</span><span class="sxs-lookup"><span data-stu-id="3eb40-114">Mixer Architecture</span></span>

<span data-ttu-id="3eb40-115">El elemento básico de la arquitectura del mezclador es una *línea de audio*.</span><span class="sxs-lookup"><span data-stu-id="3eb40-115">The basic element of the mixer architecture is an *audio line*.</span></span> <span data-ttu-id="3eb40-116">Una línea de audio se compone de uno o varios canales de datos procedentes de un único origen o de un recurso del sistema.</span><span class="sxs-lookup"><span data-stu-id="3eb40-116">An audio line consists of one or more channels of data originating from a single source or a system resource.</span></span> <span data-ttu-id="3eb40-117">Por ejemplo, una línea de audio estéreo tiene dos canales de datos, pero se considera una sola línea de audio porque se origina a partir de un único origen.</span><span class="sxs-lookup"><span data-stu-id="3eb40-117">For example, a stereo audio line has two data channels, but it is considered a single audio line because it originates from a single source.</span></span>

<span data-ttu-id="3eb40-118">La arquitectura del mezclador proporciona servicios de enrutamiento para administrar las líneas de audio de un equipo.</span><span class="sxs-lookup"><span data-stu-id="3eb40-118">The mixer architecture provides routing services to manage audio lines on a computer.</span></span> <span data-ttu-id="3eb40-119">Puede usar los servicios de enrutamiento si tiene instalados los dispositivos de hardware y los controladores de software adecuados.</span><span class="sxs-lookup"><span data-stu-id="3eb40-119">You can use the routing services if you have adequate hardware devices and software drivers installed.</span></span> <span data-ttu-id="3eb40-120">La arquitectura del mezclador permite que varias líneas de origen de audio se asignen a una sola línea de audio de destino.</span><span class="sxs-lookup"><span data-stu-id="3eb40-120">The mixer architecture allows several audio source lines to map to a single destination audio line.</span></span>

<span data-ttu-id="3eb40-121">Cada línea de audio puede tener controles de mezclador asociados.</span><span class="sxs-lookup"><span data-stu-id="3eb40-121">Each audio line can have mixer controls associated with it.</span></span> <span data-ttu-id="3eb40-122">Un control de mezclador puede realizar cualquier número de funciones (como el volumen del control), en función de las características de la línea de audio asociada.</span><span class="sxs-lookup"><span data-stu-id="3eb40-122">A mixer control can perform any number of functions (such as control volume), depending on the characteristics of the associated audio line.</span></span>

 

 




