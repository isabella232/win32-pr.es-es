---
description: Solicitudes de estado de OPM
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: Solicitudes de estado de OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbf7338fe1309feb49fd191e3f4a1a22f3639b4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120180"
---
# <a name="opm-status-requests"></a><span data-ttu-id="fbecd-103">Solicitudes de estado de OPM</span><span class="sxs-lookup"><span data-stu-id="fbecd-103">OPM Status Requests</span></span>

<span data-ttu-id="fbecd-104">En esta sección se enumeran las solicitudes de estado disponibles para [Output Protection Manager](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="fbecd-104">This section lists the available status requests for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span> <span data-ttu-id="fbecd-105">Para enviar una solicitud de estado de OPM, llame a [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span><span class="sxs-lookup"><span data-stu-id="fbecd-105">To send an OPM status request, call [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span></span> <span data-ttu-id="fbecd-106">Para cada solicitud, se muestra la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="fbecd-106">For each request, the following information is listed.</span></span>



| <span data-ttu-id="fbecd-107">Valor</span><span class="sxs-lookup"><span data-stu-id="fbecd-107">Value</span></span>             | <span data-ttu-id="fbecd-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbecd-108">Description</span></span>                                                                                                                                                           |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbecd-109">GUID de solicitud</span><span class="sxs-lookup"><span data-stu-id="fbecd-109">Request GUID</span></span> | <span data-ttu-id="fbecd-110">Identifica la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fbecd-110">Identifies the request.</span></span> <span data-ttu-id="fbecd-111">Establezca el **miembro guidSetting** de la estructura [**OPM \_ GET INFO \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) igual a este valor.</span><span class="sxs-lookup"><span data-stu-id="fbecd-111">Set the **guidSetting** member of the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="fbecd-112">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="fbecd-112">Input data</span></span>   | <span data-ttu-id="fbecd-113">Especifica cómo interpretar la matriz **abParameters** en la [**estructura OPM \_ GET INFO \_ \_ PARAMETERS.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)</span><span class="sxs-lookup"><span data-stu-id="fbecd-113">Specifies how to interpret the **abParameters** array in the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure.</span></span>                      |
| <span data-ttu-id="fbecd-114">Datos de salida</span><span class="sxs-lookup"><span data-stu-id="fbecd-114">Output data</span></span>  | <span data-ttu-id="fbecd-115">Especifica cómo interpretar la matriz **abRequestedInformation** en la [**estructura OPM \_ REQUESTED \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)</span><span class="sxs-lookup"><span data-stu-id="fbecd-115">Specifies how to interpret the **abRequestedInformation** array in the [**OPM\_REQUESTED\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) structure.</span></span>         |



 

<span data-ttu-id="fbecd-116">Se definen las siguientes solicitudes de estado:</span><span class="sxs-lookup"><span data-stu-id="fbecd-116">The following status requests are defined:</span></span>



| <span data-ttu-id="fbecd-117">Solicitud de estado</span><span class="sxs-lookup"><span data-stu-id="fbecd-117">Status request</span></span>                                                                                      | <span data-ttu-id="fbecd-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbecd-118">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fbecd-119">**OPM \_ GET \_ ACP \_ AND \_ CGMSA \_ SIGNALING**</span><span class="sxs-lookup"><span data-stu-id="fbecd-119">**OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-get-acp-and-cgmsa-signaling.md)                     | <span data-ttu-id="fbecd-120">Devuelve la siguiente información sobre una salida de vídeo:</span><span class="sxs-lookup"><span data-stu-id="fbecd-120">Returns the following information about a video output:</span></span>                                                                                               |
| [<span data-ttu-id="fbecd-121">**OPM \_ GET REAL OUTPUT \_ \_ \_ FORMAT**</span><span class="sxs-lookup"><span data-stu-id="fbecd-121">**OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT**</span></span>](opm-get-actual-output-format.md)                            | <span data-ttu-id="fbecd-122">Devuelve una descripción de la señal de vídeo que se transmite a través del conector.</span><span class="sxs-lookup"><span data-stu-id="fbecd-122">Returns a description of the video signal that is being transmitted over the connector.</span></span>                                                               |
| [<span data-ttu-id="fbecd-123">**OPM \_ GET REAL PROTECTION \_ \_ \_ LEVEL**</span><span class="sxs-lookup"><span data-stu-id="fbecd-123">**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-actual-protection-level.md)                      | <span data-ttu-id="fbecd-124">Devuelve el nivel de protección global para un mecanismo de protección especificado.</span><span class="sxs-lookup"><span data-stu-id="fbecd-124">Returns the global protection level for a specified protection mechanism.</span></span>                                                                             |
| [<span data-ttu-id="fbecd-125">**OPM GET ADAPTER BUS TYPE (TIPO DE BUS DEL ADAPTADOR DE OPM \_ \_ \_ \_ GET)**</span><span class="sxs-lookup"><span data-stu-id="fbecd-125">**OPM\_GET\_ADAPTER\_BUS\_TYPE**</span></span>](opm-get-adapter-bus-type.md)                                    | <span data-ttu-id="fbecd-126">Devuelve el tipo de bus de E/S utilizado por la salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fbecd-126">Returns the type of I/O bus used by the video output.</span></span>                                                                                                 |
| [<span data-ttu-id="fbecd-127">**OPM \_ GET \_ CODEC \_ INFO**</span><span class="sxs-lookup"><span data-stu-id="fbecd-127">**OPM\_GET\_CODEC\_INFO**</span></span>](opm-get-codec-info.md)                                                 | <span data-ttu-id="fbecd-128">Obtiene el valor de la propiedad de un códec de hardware.</span><span class="sxs-lookup"><span data-stu-id="fbecd-128">Gets the merit value of a hardware codec.</span></span>                                                                                                             |
| [<span data-ttu-id="fbecd-129">**OPM \_ GET \_ CONNECTED \_ HDCP \_ DEVICE \_ INFORMATION**</span><span class="sxs-lookup"><span data-stu-id="fbecd-129">**OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**</span></span>](opm-get-connected-hdcp-device-information.md) | <span data-ttu-id="fbecd-130">Obtiene información sobre un High-Bandwidth digital Content Protection (HDCP) conectado a la salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fbecd-130">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="fbecd-131">Se devuelve la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="fbecd-131">The following information is returned:</span></span> |
| [<span data-ttu-id="fbecd-132">**OPM \_ GET \_ CONNECTOR \_ TYPE**</span><span class="sxs-lookup"><span data-stu-id="fbecd-132">**OPM\_GET\_CONNECTOR\_TYPE**</span></span>](opm-get-connector-type.md)                                         | <span data-ttu-id="fbecd-133">Devuelve el tipo de conector físico de la salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fbecd-133">Returns the physical connector type of the video output.</span></span>                                                                                              |
| [<span data-ttu-id="fbecd-134">**OPM \_ GET \_ CURRENT \_ HDCP \_ SRM \_ VERSION**</span><span class="sxs-lookup"><span data-stu-id="fbecd-134">**OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION**</span></span>](opm-get-current-hdcp-srm-version.md)                   | <span data-ttu-id="fbecd-135">Devuelve el número de versión del mensaje de renovación del sistema (SRM) utilizado actualmente por la salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fbecd-135">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>                                               |
| [<span data-ttu-id="fbecd-136">**OPM \_ GET \_ DVI \_ CHARACTERISTICS**</span><span class="sxs-lookup"><span data-stu-id="fbecd-136">**OPM\_GET\_DVI\_CHARACTERISTICS**</span></span>](opm-get-dvi-characteristics.md)                               | <span data-ttu-id="fbecd-137">Consulta si un conector de interfaz de vídeo digital (DVI) admite DVI versión 1.1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="fbecd-137">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>                                                          |
| [<span data-ttu-id="fbecd-138">**OPM \_ GET \_ OUTPUT \_ ID**</span><span class="sxs-lookup"><span data-stu-id="fbecd-138">**OPM\_GET\_OUTPUT\_ID**</span></span>](opm-get-output-id.md)                                                   | <span data-ttu-id="fbecd-139">Devuelve el identificador único del monitor asociado a esta salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fbecd-139">Returns the unique identifier of the monitor associated with this video output.</span></span>                                                                       |
| [<span data-ttu-id="fbecd-140">**OPM \_ OBTIENE TIPOS DE PROTECCIÓN \_ \_ \_ ADMITIDOS**</span><span class="sxs-lookup"><span data-stu-id="fbecd-140">**OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES**</span></span>](opm-get-supported-protection-types.md)                | <span data-ttu-id="fbecd-141">Devuelve la lista de mecanismos de protección admitidos por el conector.</span><span class="sxs-lookup"><span data-stu-id="fbecd-141">Returns the list of protection mechanisms that are supported by the connector.</span></span>                                                                        |
| [<span data-ttu-id="fbecd-142">**OPM \_ GET \_ VIRTUAL \_ PROTECTION \_ LEVEL**</span><span class="sxs-lookup"><span data-stu-id="fbecd-142">**OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-virtual-protection-level.md)                    | <span data-ttu-id="fbecd-143">Devuelve el nivel de protección virtual para un mecanismo de protección especificado.</span><span class="sxs-lookup"><span data-stu-id="fbecd-143">Returns the virtual protection level for a specified protection mechanism.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="fbecd-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fbecd-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbecd-145">Referencia de programación de OPM</span><span class="sxs-lookup"><span data-stu-id="fbecd-145">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="fbecd-146">Administrador de protección de salida</span><span class="sxs-lookup"><span data-stu-id="fbecd-146">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



