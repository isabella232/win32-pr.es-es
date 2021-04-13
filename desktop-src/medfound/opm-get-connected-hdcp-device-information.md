---
description: 'Más información acerca de: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION'
ms.assetid: 71fa9a99-83e4-4b27-9fd1-5a9dc3070820
title: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561a348588b1244a6763eb447affa2b330e9c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543870"
---
# <a name="opm_get_connected_hdcp_device_information"></a><span data-ttu-id="0d65f-103">\_información de \_ \_ dispositivo HDCP \_ conectado \_ a OPM</span><span class="sxs-lookup"><span data-stu-id="0d65f-103">OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION</span></span>

<span data-ttu-id="0d65f-104">Obtiene información acerca de un dispositivo High-Bandwidth Digital Content Protection (HDCP) conectado a la salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0d65f-104">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="0d65f-105">Se devuelve la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="0d65f-105">The following information is returned:</span></span>

-   <span data-ttu-id="0d65f-106">Vector de selección de clave de HDCP del dispositivo (KSV).</span><span class="sxs-lookup"><span data-stu-id="0d65f-106">The device's HDCP key selection vector (KSV).</span></span>
-   <span data-ttu-id="0d65f-107">Si el dispositivo es un repetidor de HDCP.</span><span class="sxs-lookup"><span data-stu-id="0d65f-107">Whether the device is an HDCP repeater.</span></span>



| <span data-ttu-id="0d65f-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d65f-108">Requirement</span></span> | <span data-ttu-id="0d65f-109">Value</span><span class="sxs-lookup"><span data-stu-id="0d65f-109">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d65f-110">GUID de solicitud</span><span class="sxs-lookup"><span data-stu-id="0d65f-110">Request GUID</span></span> | <span data-ttu-id="0d65f-111">\_información de \_ \_ dispositivo HDCP \_ conectado \_ a OPM</span><span class="sxs-lookup"><span data-stu-id="0d65f-111">OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION</span></span>                                                          |
| <span data-ttu-id="0d65f-112">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="0d65f-112">Input data</span></span>   | <span data-ttu-id="0d65f-113">None</span><span class="sxs-lookup"><span data-stu-id="0d65f-113">None</span></span>                                                                                                    |
| <span data-ttu-id="0d65f-114">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="0d65f-114">Return data</span></span>  | <span data-ttu-id="0d65f-115">Una estructura de [**\_ \_ \_ \_ información del dispositivo HDCP conectada a OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information)</span><span class="sxs-lookup"><span data-stu-id="0d65f-115">An [**OPM\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0d65f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d65f-116">Remarks</span></span>

<span data-ttu-id="0d65f-117">Esta consulta solo se puede usar con el *modo de emulación de COPP*.</span><span class="sxs-lookup"><span data-stu-id="0d65f-117">This query can be used only with *COPP emulation mode*.</span></span> <span data-ttu-id="0d65f-118">Si la interfaz [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) usa la semántica de administrador de protección de salida (OPM), esta solicitud de estado no se admite.</span><span class="sxs-lookup"><span data-stu-id="0d65f-118">If the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface uses Output Protection Manager (OPM) semantics, this status request is not supported.</span></span>

<span data-ttu-id="0d65f-119">KSV es un identificador proporcionado al fabricante del dispositivo y se usa en el proceso de autenticación y configuración de HDCP.</span><span class="sxs-lookup"><span data-stu-id="0d65f-119">The KSV is an identifier provided to the device manufacturer, and is used in the HDCP authentication and setup process.</span></span> <span data-ttu-id="0d65f-120">En el modo de emulación de COPP, la aplicación usa KSV para determinar si el dispositivo HDCP está revocado.</span><span class="sxs-lookup"><span data-stu-id="0d65f-120">In COPP emulation mode, the application uses the KSV to determine whether the HDCP device is revoked.</span></span> <span data-ttu-id="0d65f-121">Si es así, la aplicación no debería reproducir contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="0d65f-121">If it is, the application should not play protected content.</span></span> <span data-ttu-id="0d65f-122">Además, la aplicación no debe reproducir contenido protegido si el dispositivo es un repetidor de HDCP, porque COPP no admite repetidores de HDCP.</span><span class="sxs-lookup"><span data-stu-id="0d65f-122">Also, the application should not play protected content if the device is an HDCP repeater, because COPP does not support HDCP repeaters.</span></span>

<span data-ttu-id="0d65f-123">Esta consulta no es necesaria cuando se usan semánticas de OPM, porque OPM admite repetidores de devocación de dispositivos y de HDCP.</span><span class="sxs-lookup"><span data-stu-id="0d65f-123">This query is not needed when OPM semantics are used, because OPM supports device revocation and HDCP repeaters.</span></span>

<span data-ttu-id="0d65f-124">Esta consulta es equivalente a la \_ consulta COPPQueryHDCPKeyData de DXVA usada en el protocolo de protección de la salida certificada (COPP).</span><span class="sxs-lookup"><span data-stu-id="0d65f-124">This query is equivalent to the DXVA\_COPPQueryHDCPKeyData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d65f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d65f-125">Requirements</span></span>



| <span data-ttu-id="0d65f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d65f-126">Requirement</span></span> | <span data-ttu-id="0d65f-127">Value</span><span class="sxs-lookup"><span data-stu-id="0d65f-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0d65f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d65f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0d65f-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0d65f-129">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0d65f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d65f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0d65f-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d65f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0d65f-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d65f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d65f-133"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d65f-133"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d65f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d65f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d65f-135">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="0d65f-135">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="0d65f-136">Solicitudes de estado de OPM</span><span class="sxs-lookup"><span data-stu-id="0d65f-136">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




