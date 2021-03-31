---
title: Asignación de dispositivos Waveform-Audio
description: Asignación de dispositivos Waveform-Audio
ms.assetid: e23919c9-c5fa-4406-920c-1fdbeea4821d
keywords:
- audio multimedia, asignación de los dispositivos de audio de onda
- audio, asignación de los dispositivos de audio de onda
- Administrador de compresión de audio (ACM), asignar dispositivos de audio de onda
- ACM (Administrador de compresión de audio), asignar dispositivos de audio de onda
- asignación de dispositivos de audio de onda
- audio multimedia, asignador
- audio, asignador
- Administrador de compresión de audio (ACM), asignador
- ACM (Administrador de compresión de audio), asignador
- mapper
- audio de onda, dispositivos de asignación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9cdd269e21eb992244dd0e5979c7e0d193ba92b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903333"
---
# <a name="mapping-waveform-audio-devices"></a><span data-ttu-id="ec8bc-114">Asignación de dispositivos Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="ec8bc-114">Mapping Waveform-Audio Devices</span></span>

<span data-ttu-id="ec8bc-115">Windows proporciona un conjunto de funciones estándar para dispositivos de audio.</span><span class="sxs-lookup"><span data-stu-id="ec8bc-115">Windows provides a set of standard functions for audio devices.</span></span> <span data-ttu-id="ec8bc-116">Estas funciones emiten llamadas a controladores de dispositivos que administran los dispositivos de hardware.</span><span class="sxs-lookup"><span data-stu-id="ec8bc-116">These functions issue calls to device drivers that manage hardware devices.</span></span> <span data-ttu-id="ec8bc-117">El sistema utiliza un módulo denominado "asignador" para administrar los dispositivos instalados.</span><span class="sxs-lookup"><span data-stu-id="ec8bc-117">The system uses a module called a "mapper" to manage installed devices.</span></span> <span data-ttu-id="ec8bc-118">El asignador usa enlaces especiales en la interfaz del controlador para interceptar las llamadas y actuar como intermediario entre el sistema y los controladores instalados en el sistema.</span><span class="sxs-lookup"><span data-stu-id="ec8bc-118">The mapper uses special hooks in the driver interface to intercept calls and to act as an intermediary between the system and the drivers installed in the system.</span></span> <span data-ttu-id="ec8bc-119">El asignador es responsable de hacer coincidir las solicitudes de una aplicación para el acceso a un dispositivo con los dispositivos disponibles y para buscar un dispositivo que cumpla los requisitos de audio de la aplicación actual.</span><span class="sxs-lookup"><span data-stu-id="ec8bc-119">The mapper is responsible for matching an application's requests for access to a device with the available devices and for finding a device that meets the current application's audio requirements.</span></span> <span data-ttu-id="ec8bc-120">El sistema proporciona asignadores para tipos de controlador estándar: audio de onda de onda, MIDI (interfaz digital de instrumentos musicales) y dispositivos auxiliares.</span><span class="sxs-lookup"><span data-stu-id="ec8bc-120">The system provides mappers for standard driver types: waveform-audio, MIDI (Musical Instrument Digital Interface), and auxiliary devices.</span></span>

<span data-ttu-id="ec8bc-121">ACM es una extensión del sistema multimedia básico y se instala como un asignador.</span><span class="sxs-lookup"><span data-stu-id="ec8bc-121">The ACM is an extension of the basic multimedia system and is installed as a mapper.</span></span> <span data-ttu-id="ec8bc-122">Esto significa que ACM usa los enlaces del asignador de interfaz de controlador para dispositivos de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="ec8bc-122">This means the ACM uses the driver-interface mapper hooks for waveform-audio devices.</span></span> <span data-ttu-id="ec8bc-123">El uso de estos enlaces permite a ACM descodificar o codificar los datos de audio de forma de onda antes de pasarlos a o desde un controlador de dispositivo de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="ec8bc-123">Using these hooks allows the ACM to decode or encode waveform-audio data before passing it to or from a waveform-audio device driver.</span></span> <span data-ttu-id="ec8bc-124">La diferencia entre el sistema ACM y el asignador estándar es que ACM puede buscar un dispositivo de audio de forma de onda que admita un formato especificado o buscar una combinación de un dispositivo de audio de forma de onda y un compresor o descompresor de ACM que admita un formato especificado.</span><span class="sxs-lookup"><span data-stu-id="ec8bc-124">The difference between the ACM and the standard system mapper is that the ACM can search for a waveform-audio device that supports a specified format or find a combination of a waveform-audio device and an ACM compressor or decompressor that supports a specified format.</span></span>

<span data-ttu-id="ec8bc-125">Cuando una aplicación solicita que el sistema abra un dispositivo de audio de forma de onda para entrada o salida, la solicitud especifica el formato y el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ec8bc-125">When an application requests that the system open a waveform-audio device for input or output, the request specifies the format and device.</span></span> <span data-ttu-id="ec8bc-126">Cuando el dispositivo especificado es el asignador, el asignador debe encontrar un dispositivo que admita el formato especificado.</span><span class="sxs-lookup"><span data-stu-id="ec8bc-126">When the specified device is the mapper, the mapper must find a device that supports the specified format.</span></span> <span data-ttu-id="ec8bc-127">El asignador implementado en ACM busca un dispositivo de audio de forma de onda instalado que admita el formato especificado.</span><span class="sxs-lookup"><span data-stu-id="ec8bc-127">The mapper implemented in the ACM searches for an installed waveform-audio device that supports the specified format.</span></span> <span data-ttu-id="ec8bc-128">Si ACM no puede encontrar este dispositivo, busca un dispositivo de audio de forma de onda y un compresor o descompresor que admitan el formato.</span><span class="sxs-lookup"><span data-stu-id="ec8bc-128">If the ACM cannot find such a device, it searches for a waveform-audio device and a compressor or decompressor that together support the format.</span></span> <span data-ttu-id="ec8bc-129">En concreto, ACM busca un compresor o descompresor que convierte el formato especificado en un formato compatible con un dispositivo de audio de forma de onda instalado.</span><span class="sxs-lookup"><span data-stu-id="ec8bc-129">Specifically, the ACM searches for a compressor or decompressor that converts the specified format into a format that is supported by an installed waveform-audio device.</span></span> <span data-ttu-id="ec8bc-130">Una vez que ACM encuentra un dispositivo que admite el formato convertido, puede aceptar solicitudes para reproducir o grabar el formato solicitado originalmente, aunque ningún dispositivo de audio de forma de onda instalado admita directamente ese formato.</span><span class="sxs-lookup"><span data-stu-id="ec8bc-130">After the ACM finds a device that supports the converted format, it can honor requests to play or record the format originally requested, even though no installed waveform-audio device directly supports that format.</span></span>

<span data-ttu-id="ec8bc-131">Además de la conversión de formato, el ACM también ofrece servicios para admitir la compresión, la descompresión, el filtrado, la selección de formato y la selección de filtro.</span><span class="sxs-lookup"><span data-stu-id="ec8bc-131">In addition to format conversion, the ACM also offers services to support compression, decompression, filtering, format selection, and filter selection.</span></span> <span data-ttu-id="ec8bc-132">Proporciona una API estándar que admite mediante la llamada a sus propios controladores.</span><span class="sxs-lookup"><span data-stu-id="ec8bc-132">It provides a standard API that it supports by calling its own drivers.</span></span>

 

 




