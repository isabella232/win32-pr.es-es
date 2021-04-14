---
description: La \_ propiedad PKEY AudioEndpoint \_ FormFactor especifica el factor de forma del dispositivo de extremo de audio. El factor de forma indica los atributos físicos del dispositivo de extremo de audio que manipula el usuario.
ms.assetid: f49cb7da-3b50-47e2-90b4-1a885001b5d7
title: PKEY_AudioEndpoint_FormFactor (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5833470e2a2848f9454f3b5eefbf852f452f033
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496516"
---
# <a name="pkey_audioendpoint_formfactor"></a><span data-ttu-id="652c9-104">PKEY \_ AudioEndpoint \_ FormFactor</span><span class="sxs-lookup"><span data-stu-id="652c9-104">PKEY\_AudioEndpoint\_FormFactor</span></span>

<span data-ttu-id="652c9-105">La propiedad **PKEY \_ AudioEndpoint \_ FormFactor** especifica el factor de forma del dispositivo de extremo de audio.</span><span class="sxs-lookup"><span data-stu-id="652c9-105">The **PKEY\_AudioEndpoint\_FormFactor** property specifies the form factor of the audio endpoint device.</span></span> <span data-ttu-id="652c9-106">El factor de forma indica los atributos físicos del dispositivo de extremo de audio que manipula el usuario.</span><span class="sxs-lookup"><span data-stu-id="652c9-106">The form factor indicates the physical attributes of the audio endpoint device that the user manipulates.</span></span>

<span data-ttu-id="652c9-107">El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="652c9-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="652c9-108">El miembro **uintVal** de la estructura **PROPVARIANT** contiene un valor de enumeración que se convierte al tipo uint.</span><span class="sxs-lookup"><span data-stu-id="652c9-108">The **uintVal** member of the **PROPVARIANT** structure contains an enumeration value that is cast to type UINT.</span></span> <span data-ttu-id="652c9-109">Se establece en uno de los siguientes valores de enumeración [**EndpointFormFactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) :</span><span class="sxs-lookup"><span data-stu-id="652c9-109">It is set to one of the following [**EndpointFormFactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) enumeration values:</span></span>

-   <span data-ttu-id="652c9-110">RemoteNetworkDevice</span><span class="sxs-lookup"><span data-stu-id="652c9-110">RemoteNetworkDevice</span></span>
-   <span data-ttu-id="652c9-111">Altavoces</span><span class="sxs-lookup"><span data-stu-id="652c9-111">Speakers</span></span>
-   <span data-ttu-id="652c9-112">LineLevel</span><span class="sxs-lookup"><span data-stu-id="652c9-112">LineLevel</span></span>
-   <span data-ttu-id="652c9-113">Auriculares</span><span class="sxs-lookup"><span data-stu-id="652c9-113">Headphones</span></span>
-   <span data-ttu-id="652c9-114">Micrófono</span><span class="sxs-lookup"><span data-stu-id="652c9-114">Microphone</span></span>
-   <span data-ttu-id="652c9-115">Auriculares</span><span class="sxs-lookup"><span data-stu-id="652c9-115">Headset</span></span>
-   <span data-ttu-id="652c9-116">Auricular</span><span class="sxs-lookup"><span data-stu-id="652c9-116">Handset</span></span>
-   <span data-ttu-id="652c9-117">UnknownDigitalPassthrough</span><span class="sxs-lookup"><span data-stu-id="652c9-117">UnknownDigitalPassthrough</span></span>
-   <span data-ttu-id="652c9-118">SALIDA</span><span class="sxs-lookup"><span data-stu-id="652c9-118">SPDIF</span></span>
-   <span data-ttu-id="652c9-119">HDMI</span><span class="sxs-lookup"><span data-stu-id="652c9-119">HDMI</span></span>
-   <span data-ttu-id="652c9-120">UnknownFormFactor</span><span class="sxs-lookup"><span data-stu-id="652c9-120">UnknownFormFactor</span></span>

## <a name="requirements"></a><span data-ttu-id="652c9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="652c9-121">Requirements</span></span>



| <span data-ttu-id="652c9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="652c9-122">Requirement</span></span> | <span data-ttu-id="652c9-123">Value</span><span class="sxs-lookup"><span data-stu-id="652c9-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="652c9-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="652c9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="652c9-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="652c9-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="652c9-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="652c9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="652c9-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="652c9-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="652c9-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="652c9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="652c9-129"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="652c9-129"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="652c9-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="652c9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="652c9-131">**Propiedades de punto de conexión de audio**</span><span class="sxs-lookup"><span data-stu-id="652c9-131">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="652c9-132">Propiedades de audio principales</span><span class="sxs-lookup"><span data-stu-id="652c9-132">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




