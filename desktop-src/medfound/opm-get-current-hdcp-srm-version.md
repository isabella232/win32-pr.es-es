---
description: Devuelve el número de versión del mensaje de renovación de sistema (SRM) que usa actualmente la salida de vídeo.
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: OPM_GET_CURRENT_HDCP_SRM_VERSION (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e05ad53ae58e2141c63179c84a90f90cea86fb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715527"
---
# <a name="opm_get_current_hdcp_srm_version"></a><span data-ttu-id="31168-103">\_obtener la \_ versión actual de \_ HDCP de HDCP \_ \_</span><span class="sxs-lookup"><span data-stu-id="31168-103">OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION</span></span>

<span data-ttu-id="31168-104">Devuelve el número de versión del mensaje de renovación de sistema (SRM) que usa actualmente la salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="31168-104">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>



| <span data-ttu-id="31168-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="31168-105">Requirement</span></span> | <span data-ttu-id="31168-106">Value</span><span class="sxs-lookup"><span data-stu-id="31168-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="31168-107">GUID de solicitud</span><span class="sxs-lookup"><span data-stu-id="31168-107">Request GUID</span></span> | <span data-ttu-id="31168-108">\_obtener la \_ versión actual de \_ HDCP de HDCP \_ \_</span><span class="sxs-lookup"><span data-stu-id="31168-108">OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION</span></span>                                       |
| <span data-ttu-id="31168-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="31168-109">Input data</span></span>   | <span data-ttu-id="31168-110">None</span><span class="sxs-lookup"><span data-stu-id="31168-110">None</span></span>                                                                        |
| <span data-ttu-id="31168-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="31168-111">Return data</span></span>  | <span data-ttu-id="31168-112">Una estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="31168-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="31168-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31168-113">Remarks</span></span>

<span data-ttu-id="31168-114">Si esta consulta se realiza correctamente, el miembro **ulInformation** de la estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contiene el número de versión de SRM, en formato Little-Endian.</span><span class="sxs-lookup"><span data-stu-id="31168-114">If this query succeeds, the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure contains the SRM version number, in little-endian format.</span></span>

<span data-ttu-id="31168-115">SRMs se usan para actualizar la lista de dispositivos revocados High-Bandwidth Digital Content Protection (HDCP).</span><span class="sxs-lookup"><span data-stu-id="31168-115">SRMs are used to update the list of revoked High-Bandwidth Digital Content Protection (HDCP) devices.</span></span> <span data-ttu-id="31168-116">SRMs se entregan con el contenido del vídeo.</span><span class="sxs-lookup"><span data-stu-id="31168-116">SRMs are delivered with the video content.</span></span> <span data-ttu-id="31168-117">Para establecer el SRM, envíe el comando [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .</span><span class="sxs-lookup"><span data-stu-id="31168-117">To set the SRM, send the [**OPM\_SET\_HDCP\_SRM**](opm-set-hdcp-srm.md) command.</span></span>

<span data-ttu-id="31168-118">Esta consulta puede hacer que el método [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) devuelva cualquiera de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="31168-118">This query can cause the [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method to return any of the following error codes.</span></span>



| <span data-ttu-id="31168-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="31168-119">Return code</span></span>                                            | <span data-ttu-id="31168-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="31168-120">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="31168-121">gráficos de ERROR: no se ha \_ \_ \_ \_ \_ establecido nunca la SRM de HDCP \_</span><span class="sxs-lookup"><span data-stu-id="31168-121">ERROR\_GRAPHICS\_OPM\_HDCP\_SRM\_NEVER\_SET</span></span>            | <span data-ttu-id="31168-122">La aplicación no estableció una SRM.</span><span class="sxs-lookup"><span data-stu-id="31168-122">The application did not set an SRM.</span></span>     |
| <span data-ttu-id="31168-123">el resultado de los gráficos de ERROR \_ \_ OPM \_ no es \_ \_ \_ compatible con \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="31168-123">ERROR\_GRAPHICS\_OPM\_OUTPUT\_DOES\_NOT\_SUPPORT\_HDCP</span></span> | <span data-ttu-id="31168-124">La salida de vídeo no es compatible con HDCP.</span><span class="sxs-lookup"><span data-stu-id="31168-124">The video output does not support HDCP.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="31168-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31168-125">Requirements</span></span>



| <span data-ttu-id="31168-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="31168-126">Requirement</span></span> | <span data-ttu-id="31168-127">Value</span><span class="sxs-lookup"><span data-stu-id="31168-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="31168-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31168-128">Minimum supported client</span></span><br/> | <span data-ttu-id="31168-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="31168-129">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="31168-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31168-130">Minimum supported server</span></span><br/> | <span data-ttu-id="31168-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="31168-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="31168-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31168-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="31168-133"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="31168-133"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31168-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="31168-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31168-135">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="31168-135">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="31168-136">Solicitudes de estado de OPM</span><span class="sxs-lookup"><span data-stu-id="31168-136">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




