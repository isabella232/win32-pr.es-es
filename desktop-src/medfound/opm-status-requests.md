---
description: Solicitudes de estado de OPM
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: Solicitudes de estado de OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd994d7cb8d43db23fe59352dba830e741b74b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811587"
---
# <a name="opm-status-requests"></a><span data-ttu-id="08eb2-103">Solicitudes de estado de OPM</span><span class="sxs-lookup"><span data-stu-id="08eb2-103">OPM Status Requests</span></span>

<span data-ttu-id="08eb2-104">En esta sección se enumeran las solicitudes de estado disponibles para el [Administrador de protección de salida](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="08eb2-104">This section lists the available status requests for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span> <span data-ttu-id="08eb2-105">Para enviar una solicitud de estado de OPM, llame a [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span><span class="sxs-lookup"><span data-stu-id="08eb2-105">To send an OPM status request, call [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span></span> <span data-ttu-id="08eb2-106">Para cada solicitud, se muestra la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="08eb2-106">For each request, the following information is listed.</span></span>



|              |                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08eb2-107">GUID de solicitud</span><span class="sxs-lookup"><span data-stu-id="08eb2-107">Request GUID</span></span> | <span data-ttu-id="08eb2-108">Identifica la solicitud.</span><span class="sxs-lookup"><span data-stu-id="08eb2-108">Identifies the request.</span></span> <span data-ttu-id="08eb2-109">Establezca el miembro **guidSetting** de la estructura de parámetros de [**\_ obtención de \_ información \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) igual a este valor.</span><span class="sxs-lookup"><span data-stu-id="08eb2-109">Set the **guidSetting** member of the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="08eb2-110">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="08eb2-110">Input data</span></span>   | <span data-ttu-id="08eb2-111">Especifica cómo interpretar la matriz **abParameters** en la estructura [**de \_ \_ \_ parámetros de obtención de información de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) .</span><span class="sxs-lookup"><span data-stu-id="08eb2-111">Specifies how to interpret the **abParameters** array in the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure.</span></span>                      |
| <span data-ttu-id="08eb2-112">Datos de salida</span><span class="sxs-lookup"><span data-stu-id="08eb2-112">Output data</span></span>  | <span data-ttu-id="08eb2-113">Especifica cómo interpretar la matriz **abRequestedInformation** en la estructura [**de \_ \_ información solicitada de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) .</span><span class="sxs-lookup"><span data-stu-id="08eb2-113">Specifies how to interpret the **abRequestedInformation** array in the [**OPM\_REQUESTED\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) structure.</span></span>         |



 

<span data-ttu-id="08eb2-114">Se definen las siguientes solicitudes de estado:</span><span class="sxs-lookup"><span data-stu-id="08eb2-114">The following status requests are defined:</span></span>



| <span data-ttu-id="08eb2-115">Solicitud de estado</span><span class="sxs-lookup"><span data-stu-id="08eb2-115">Status request</span></span>                                                                                      | <span data-ttu-id="08eb2-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="08eb2-116">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08eb2-117">**la \_ \_ \_ señalización de OPM y \_ CGMSA de \_ OPM**</span><span class="sxs-lookup"><span data-stu-id="08eb2-117">**OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-get-acp-and-cgmsa-signaling.md)                     | <span data-ttu-id="08eb2-118">Devuelve la siguiente información sobre una salida de vídeo:</span><span class="sxs-lookup"><span data-stu-id="08eb2-118">Returns the following information about a video output:</span></span>                                                                                               |
| [<span data-ttu-id="08eb2-119">**\_formato de \_ \_ salida real \_ de OPM**</span><span class="sxs-lookup"><span data-stu-id="08eb2-119">**OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT**</span></span>](opm-get-actual-output-format.md)                            | <span data-ttu-id="08eb2-120">Devuelve una descripción de la señal de vídeo que se transmite a través del conector.</span><span class="sxs-lookup"><span data-stu-id="08eb2-120">Returns a description of the video signal that is being transmitted over the connector.</span></span>                                                               |
| [<span data-ttu-id="08eb2-121">**\_obtener \_ nivel de \_ protección \_ real de OPM**</span><span class="sxs-lookup"><span data-stu-id="08eb2-121">**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-actual-protection-level.md)                      | <span data-ttu-id="08eb2-122">Devuelve el nivel de protección global para un mecanismo de protección especificado.</span><span class="sxs-lookup"><span data-stu-id="08eb2-122">Returns the global protection level for a specified protection mechanism.</span></span>                                                                             |
| [<span data-ttu-id="08eb2-123">**\_tipo de \_ bus de adaptador OPM Get \_ \_**</span><span class="sxs-lookup"><span data-stu-id="08eb2-123">**OPM\_GET\_ADAPTER\_BUS\_TYPE**</span></span>](opm-get-adapter-bus-type.md)                                    | <span data-ttu-id="08eb2-124">Devuelve el tipo de bus de e/s utilizado por la salida del vídeo.</span><span class="sxs-lookup"><span data-stu-id="08eb2-124">Returns the type of I/O bus used by the video output.</span></span>                                                                                                 |
| [<span data-ttu-id="08eb2-125">**\_información del \_ códec de obtención de OPM \_**</span><span class="sxs-lookup"><span data-stu-id="08eb2-125">**OPM\_GET\_CODEC\_INFO**</span></span>](opm-get-codec-info.md)                                                 | <span data-ttu-id="08eb2-126">Obtiene el valor de mérito de un códec de hardware.</span><span class="sxs-lookup"><span data-stu-id="08eb2-126">Gets the merit value of a hardware codec.</span></span>                                                                                                             |
| [<span data-ttu-id="08eb2-127">**\_información de \_ \_ dispositivo HDCP \_ conectado \_ a OPM**</span><span class="sxs-lookup"><span data-stu-id="08eb2-127">**OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**</span></span>](opm-get-connected-hdcp-device-information.md) | <span data-ttu-id="08eb2-128">Obtiene información acerca de un dispositivo High-Bandwidth Digital Content Protection (HDCP) conectado a la salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="08eb2-128">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="08eb2-129">Se devuelve la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="08eb2-129">The following information is returned:</span></span> |
| [<span data-ttu-id="08eb2-130">**\_tipo de \_ conector de obtención de OPM \_**</span><span class="sxs-lookup"><span data-stu-id="08eb2-130">**OPM\_GET\_CONNECTOR\_TYPE**</span></span>](opm-get-connector-type.md)                                         | <span data-ttu-id="08eb2-131">Devuelve el tipo de conector físico de la salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="08eb2-131">Returns the physical connector type of the video output.</span></span>                                                                                              |
| [<span data-ttu-id="08eb2-132">**\_obtener la \_ versión actual de \_ HDCP de HDCP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="08eb2-132">**OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION**</span></span>](opm-get-current-hdcp-srm-version.md)                   | <span data-ttu-id="08eb2-133">Devuelve el número de versión del mensaje de renovación de sistema (SRM) que usa actualmente la salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="08eb2-133">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>                                               |
| [<span data-ttu-id="08eb2-134">**características de la \_ obtención de \_ DVI de OPM \_**</span><span class="sxs-lookup"><span data-stu-id="08eb2-134">**OPM\_GET\_DVI\_CHARACTERISTICS**</span></span>](opm-get-dvi-characteristics.md)                               | <span data-ttu-id="08eb2-135">Consulta si un conector de la interfaz de vídeo digital (DVI) admite DVI versión 1,1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="08eb2-135">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>                                                          |
| [<span data-ttu-id="08eb2-136">**\_obtener \_ \_ ID. de salida de OPM**</span><span class="sxs-lookup"><span data-stu-id="08eb2-136">**OPM\_GET\_OUTPUT\_ID**</span></span>](opm-get-output-id.md)                                                   | <span data-ttu-id="08eb2-137">Devuelve el identificador único del monitor asociado a esta salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="08eb2-137">Returns the unique identifier of the monitor associated with this video output.</span></span>                                                                       |
| [<span data-ttu-id="08eb2-138">**\_tipos de \_ protección compatible con OPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="08eb2-138">**OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES**</span></span>](opm-get-supported-protection-types.md)                | <span data-ttu-id="08eb2-139">Devuelve la lista de mecanismos de protección admitidos por el conector.</span><span class="sxs-lookup"><span data-stu-id="08eb2-139">Returns the list of protection mechanisms that are supported by the connector.</span></span>                                                                        |
| [<span data-ttu-id="08eb2-140">**\_nivel de \_ \_ protección virtual \_ de OPM**</span><span class="sxs-lookup"><span data-stu-id="08eb2-140">**OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-virtual-protection-level.md)                    | <span data-ttu-id="08eb2-141">Devuelve el nivel de protección virtual para un mecanismo de protección especificado.</span><span class="sxs-lookup"><span data-stu-id="08eb2-141">Returns the virtual protection level for a specified protection mechanism.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="08eb2-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="08eb2-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08eb2-143">Referencia de programación de OPM</span><span class="sxs-lookup"><span data-stu-id="08eb2-143">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="08eb2-144">Administrador de protección de salida</span><span class="sxs-lookup"><span data-stu-id="08eb2-144">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



