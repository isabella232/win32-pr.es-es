---
description: 'Más información acerca de: PKEY_AudioEndpoint_PhysicalSpeakers'
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: PKEY_AudioEndpoint_PhysicalSpeakers (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a627ec97dc329f50cc58a15d0df516f598af86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539213"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a><span data-ttu-id="a6230-103">PKEY \_ AudioEndpoint \_ PhysicalSpeakers</span><span class="sxs-lookup"><span data-stu-id="a6230-103">PKEY\_AudioEndpoint\_PhysicalSpeakers</span></span>

<span data-ttu-id="a6230-104">La **propiedad \_ \_ PhysicalSpeakers de AudioEndpoint de PKEY** especifica la máscara de configuración de canal para el dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="a6230-104">The **PKEY\_AudioEndpoint\_PhysicalSpeakers** property specifies the channel-configuration mask for the audio endpoint device.</span></span> <span data-ttu-id="a6230-105">La máscara indica la configuración física de un conjunto de oradores y especifica la asignación de canales a los altavoces.</span><span class="sxs-lookup"><span data-stu-id="a6230-105">The mask indicates the physical configuration of a set of speakers and specifies the assignment of channels to speakers.</span></span> <span data-ttu-id="a6230-106">Para obtener más información acerca de las máscaras de configuración de canal, consulte lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a6230-106">For more information about channel-configuration masks, see the following:</span></span>

1.  <span data-ttu-id="a6230-107">La descripción de la \_ propiedad de configuración de canal de audio KSPROPERTY \_ \_ en la documentación de DDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="a6230-107">The description of the KSPROPERTY\_AUDIO\_CHANNEL\_CONFIG property in the Windows DDK documentation.</span></span>
2.  <span data-ttu-id="a6230-108">Las notas del producto titulada "compatibilidad con controladores de audio para las configuraciones de altavoz de Home Theater" en el sitio Web [de tecnologías de dispositivos de audio para Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="a6230-108">The white paper titled "Audio Driver Support for Home Theater Speaker Configurations" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="a6230-109">El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="a6230-109">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="a6230-110">El miembro **uintVal** de la estructura **PROPVARIANT** contiene una máscara de configuración de canal que se convierte al tipo **uint**.</span><span class="sxs-lookup"><span data-stu-id="a6230-110">The **uintVal** member of the **PROPVARIANT** structure contains a channel-configuration mask that is cast to type **UINT**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6230-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6230-111">Requirements</span></span>



| <span data-ttu-id="a6230-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6230-112">Requirement</span></span> | <span data-ttu-id="a6230-113">Value</span><span class="sxs-lookup"><span data-stu-id="a6230-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6230-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6230-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a6230-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a6230-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a6230-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6230-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a6230-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6230-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a6230-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6230-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6230-119"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6230-119"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6230-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6230-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6230-121">**Propiedades de punto de conexión de audio**</span><span class="sxs-lookup"><span data-stu-id="a6230-121">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="a6230-122">Propiedades de audio principales</span><span class="sxs-lookup"><span data-stu-id="a6230-122">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




