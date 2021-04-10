---
description: Las \_ \_ \_ constantes XXX de compatibilidad de hardware de punto de conexión son marcas de compatibilidad de hardware para un dispositivo de punto de conexión de audio.
ms.assetid: 54032f75-2287-4589-bda5-e005ee077c41
title: Constantes de ENDPOINT_HARDWARE_SUPPORT_XXX (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffb5b2255330b205519ce3065ccb5f7eebb6b65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153520"
---
# <a name="endpoint_hardware_support_xxx-constants"></a><span data-ttu-id="2e809-103">Compatibilidad de hardware de punto de conexión \_ \_ \_ XXX constantes</span><span class="sxs-lookup"><span data-stu-id="2e809-103">ENDPOINT\_HARDWARE\_SUPPORT\_XXX Constants</span></span>

<span data-ttu-id="2e809-104">Las \_ \_ \_ constantes XXX de compatibilidad de hardware de punto de conexión son marcas de compatibilidad de hardware para un dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="2e809-104">The ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants are hardware support flags for an audio endpoint device.</span></span>



| <span data-ttu-id="2e809-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="2e809-105">Constant/value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="2e809-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e809-106">Description</span></span>                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="ENDPOINT_HARDWARE_SUPPORT_VOLUME"></span><span id="endpoint_hardware_support_volume"></span><dl> <span data-ttu-id="2e809-107"><dt>**Punto de conexión \_ \_ \_ Volumen de soporte de hardware**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="2e809-107"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_VOLUME**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="2e809-108">El dispositivo de punto de conexión de audio admite un control de volumen de hardware.</span><span class="sxs-lookup"><span data-stu-id="2e809-108">The audio endpoint device supports a hardware volume control.</span></span><br/> |
| <span id="ENDPOINT_HARDWARE_SUPPORT_MUTE"></span><span id="endpoint_hardware_support_mute"></span><dl> <span data-ttu-id="2e809-109"><dt>**Punto de conexión \_ Compatibilidad de HARDWARE \_ \_ silenciar**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="2e809-109"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_MUTE**</dt> <dt>0x00000002</dt></span></span> </dl>       | <span data-ttu-id="2e809-110">El dispositivo de punto de conexión de audio admite un control de silencio de hardware.</span><span class="sxs-lookup"><span data-stu-id="2e809-110">The audio endpoint device supports a hardware mute control.</span></span><br/>   |
| <span id="ENDPOINT_HARDWARE_SUPPORT_METER"></span><span id="endpoint_hardware_support_meter"></span><dl> <span data-ttu-id="2e809-111"><dt>**Punto de conexión \_ \_ \_ Medidor de compatibilidad de hardware**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="2e809-111"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_METER**</dt> <dt>0x00000004</dt></span></span> </dl>    | <span data-ttu-id="2e809-112">El dispositivo de punto de conexión de audio admite un medidor de picos de hardware.</span><span class="sxs-lookup"><span data-stu-id="2e809-112">The audio endpoint device supports a hardware peak meter.</span></span><br/>     |



## <a name="remarks"></a><span data-ttu-id="2e809-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e809-113">Remarks</span></span>

<span data-ttu-id="2e809-114">Los métodos [**IAudioEndpointVolume:: QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) y [**IAudioMeterInformation:: QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) usan las \_ \_ constantes XXX de compatibilidad de hardware del punto de conexión \_ .</span><span class="sxs-lookup"><span data-stu-id="2e809-114">The [**IAudioEndpointVolume::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) and [**IAudioMeterInformation::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) methods use the ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants.</span></span>

<span data-ttu-id="2e809-115">Una máscara de compatibilidad de hardware indica qué funciones implementa un dispositivo de punto de conexión de audio en el hardware.</span><span class="sxs-lookup"><span data-stu-id="2e809-115">A hardware support mask indicates which functions an audio endpoint device implements in hardware.</span></span> <span data-ttu-id="2e809-116">La máscara puede ser 0 o la combinación OR bit a bit de una o varias \_ constantes XXX de compatibilidad de hardware de extremo \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2e809-116">The mask can be either 0 or the bitwise-OR combination of one or more ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants.</span></span> <span data-ttu-id="2e809-117">Si un bit que corresponde a una \_ \_ \_ constante de compatibilidad de hardware de punto de conexión en particular se establece en la máscara, el significado es que el dispositivo implementa la función representada por esa constante en el hardware.</span><span class="sxs-lookup"><span data-stu-id="2e809-117">If a bit that corresponds to a particular ENDPOINT\_HARDWARE\_SUPPORT\_XXX constant is set in the mask, then the meaning is that the function represented by that constant is implemented in hardware by the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e809-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e809-118">Requirements</span></span>



| <span data-ttu-id="2e809-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e809-119">Requirement</span></span> | <span data-ttu-id="2e809-120">Value</span><span class="sxs-lookup"><span data-stu-id="2e809-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e809-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e809-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2e809-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2e809-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2e809-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e809-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2e809-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e809-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2e809-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e809-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e809-126"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e809-126"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e809-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e809-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e809-128">Constantes de audio principales</span><span class="sxs-lookup"><span data-stu-id="2e809-128">Core Audio Constants</span></span>](core-audio-constants.md)
</dt> <dt>

[<span data-ttu-id="2e809-129">**IAudioEndpointVolume::QueryHardwareSupport**</span><span class="sxs-lookup"><span data-stu-id="2e809-129">**IAudioEndpointVolume::QueryHardwareSupport**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)
</dt> <dt>

[<span data-ttu-id="2e809-130">**IAudioMeterInformation::QueryHardwareSupport**</span><span class="sxs-lookup"><span data-stu-id="2e809-130">**IAudioMeterInformation::QueryHardwareSupport**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)
</dt> </dl>

 

 




