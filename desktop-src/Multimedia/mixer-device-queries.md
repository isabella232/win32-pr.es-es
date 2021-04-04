---
title: Consultas de dispositivos de mezclador
description: Consultas de dispositivos de mezclador
ms.assetid: 3b453802-954b-4356-9ad5-0f8376b6199d
keywords:
- audio multimedia, consultas de dispositivo de mezclador
- consultas de audio y de dispositivo de mezclador
- Mezcladores de audio, consultas de dispositivos
- mezcladores, consultas de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02acc3d5c7e418d14412c60a2e28e32849497c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077691"
---
# <a name="mixer-device-queries"></a><span data-ttu-id="2109d-107">Consultas de dispositivos de mezclador</span><span class="sxs-lookup"><span data-stu-id="2109d-107">Mixer Device Queries</span></span>

<span data-ttu-id="2109d-108">Los servicios de mezclador proporcionan funciones para determinar el número de dispositivos de mezclador presentes en el sistema y las capacidades de los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="2109d-108">The mixer services provide functions for determining the number of mixer devices present in the system and the capabilities of the devices.</span></span> <span data-ttu-id="2109d-109">También puede usar una función de servicios de mezclador para determinar el identificador de dispositivo para un dispositivo de mezclador.</span><span class="sxs-lookup"><span data-stu-id="2109d-109">You can also use a mixer services function to determine the device identifier for a mixer device.</span></span>

<span data-ttu-id="2109d-110">Puede usar la función [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) para determinar el número de dispositivos de mezclador presentes en el sistema.</span><span class="sxs-lookup"><span data-stu-id="2109d-110">You can use the [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) function to determine how many mixer devices are present in the system.</span></span> <span data-ttu-id="2109d-111">Los dispositivos de mezclador se identifican mediante un identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2109d-111">Mixer devices are identified by a device identifier.</span></span> <span data-ttu-id="2109d-112">Los identificadores de dispositivo se determinan implícitamente a partir del número de dispositivos presentes en un sistema determinado.</span><span class="sxs-lookup"><span data-stu-id="2109d-112">Device identifiers are determined implicitly from the number of devices present in a given system.</span></span> <span data-ttu-id="2109d-113">Van desde cero hasta uno menos que el número de dispositivos presentes.</span><span class="sxs-lookup"><span data-stu-id="2109d-113">They range from zero through one less than the number of devices present.</span></span>

<span data-ttu-id="2109d-114">Antes de usar un dispositivo de mezclador, debe determinar sus capacidades.</span><span class="sxs-lookup"><span data-stu-id="2109d-114">Before using a mixer device, you must determine its capabilities.</span></span> <span data-ttu-id="2109d-115">Las capacidades de audio pueden variar de un equipo multimedia a otro, por lo que las aplicaciones deben trabajar con una variedad de hardware de audio.</span><span class="sxs-lookup"><span data-stu-id="2109d-115">Audio capabilities can vary from one multimedia computer to another, so applications need to work with a variety of audio hardware.</span></span>

<span data-ttu-id="2109d-116">Puede usar la función [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) para determinar las capacidades de los dispositivos de mezclador.</span><span class="sxs-lookup"><span data-stu-id="2109d-116">You can use the [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) function to determine the capabilities of mixer devices.</span></span> <span data-ttu-id="2109d-117">Esta función rellena una estructura [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) con información sobre las capacidades de un dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="2109d-117">This function fills a [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) structure with information about the capabilities of a specified device.</span></span>

<span data-ttu-id="2109d-118">La función [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) recupera el identificador de dispositivo del mezclador de audio asociado a un identificador de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="2109d-118">The [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) function retrieves the audio mixer device identifier associated with a specified device handle.</span></span> <span data-ttu-id="2109d-119">Por ejemplo, puede usar esta función para recuperar el identificador de dispositivo de un mezclador de audio y, a continuación, usar el identificador de dispositivo para ajustar el volumen o para mostrar otro control.</span><span class="sxs-lookup"><span data-stu-id="2109d-119">For example, you could use this function to retrieve the device identifier for an audio mixer and then use the device identifier to adjust the volume or to display another control.</span></span>

 

 