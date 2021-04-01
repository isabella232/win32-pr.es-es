---
description: Actualiza el mensaje de renovación de sistema (SRM) para High-Bandwidth Digital Content Protection (HDCP).
ms.assetid: ea18baba-0e03-4471-af0e-a588773c98d2
title: OPM_SET_HDCP_SRM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9283c493598f22a1715f687eccea985a27e0e6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275828"
---
# <a name="opm_set_hdcp_srm"></a><span data-ttu-id="15803-103">OPM \_ set \_ HDCP \_ SRM</span><span class="sxs-lookup"><span data-stu-id="15803-103">OPM\_SET\_HDCP\_SRM</span></span>

<span data-ttu-id="15803-104">Actualiza el mensaje de renovación de sistema (SRM) para High-Bandwidth Digital Content Protection (HDCP).</span><span class="sxs-lookup"><span data-stu-id="15803-104">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span>



| <span data-ttu-id="15803-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="15803-105">Requirement</span></span> | <span data-ttu-id="15803-106">Value</span><span class="sxs-lookup"><span data-stu-id="15803-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="15803-107">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="15803-107">Command GUID</span></span> | <span data-ttu-id="15803-108">OPM \_ set \_ HDCP \_ SRM</span><span class="sxs-lookup"><span data-stu-id="15803-108">OPM\_SET\_HDCP\_SRM</span></span>                                                                 |
| <span data-ttu-id="15803-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="15803-109">Input data</span></span>   | <span data-ttu-id="15803-110">Una estructura de [**\_ parámetros de SRM de set \_ HDCP \_ \_ de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)</span><span class="sxs-lookup"><span data-stu-id="15803-110">An [**OPM\_SET\_HDCP\_SRM\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) structure</span></span> |



 

<span data-ttu-id="15803-111">El parámetro *pbAdditionalParameters* de [**IOPMVideoOutput:: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) debe apuntar a un búfer que contenga la SRM.</span><span class="sxs-lookup"><span data-stu-id="15803-111">The *pbAdditionalParameters* parameter of [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) must point to a buffer that contains the SRM.</span></span> <span data-ttu-id="15803-112">El formato de una SRM de HDCP se documenta en la especificación de HDCP.</span><span class="sxs-lookup"><span data-stu-id="15803-112">The format of an HDCP SRM is documented in the HDCP specification.</span></span> <span data-ttu-id="15803-113">Establezca el parámetro *ulAdditionalParametersSize* en el tamaño del búfer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="15803-113">Set the *ulAdditionalParametersSize* parameter equal to the size of the buffer, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="15803-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15803-114">Remarks</span></span>

<span data-ttu-id="15803-115">SRMs se usan para actualizar la lista de dispositivos HDCP revocados.</span><span class="sxs-lookup"><span data-stu-id="15803-115">SRMs are used to update the list of revoked HDCP devices.</span></span> <span data-ttu-id="15803-116">SRMs se entregan con el contenido del vídeo.</span><span class="sxs-lookup"><span data-stu-id="15803-116">SRMs are delivered with the video content.</span></span>

<span data-ttu-id="15803-117">Este comando actualiza el SRM actual de la salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="15803-117">This command updates the video output's current SRM.</span></span> <span data-ttu-id="15803-118">Si se habilita HDCP en el momento del comando, la salida de vídeo usa el nuevo SRM para comprobar si alguno de los dispositivos HDCP conectados está revocado.</span><span class="sxs-lookup"><span data-stu-id="15803-118">If HDCP is enabled at the time of the command, the video output uses the new SRM to check whether any of the connected HDCP devices are revoked.</span></span> <span data-ttu-id="15803-119">Si la salida de vídeo detecta un dispositivo revocado, deja de mostrar vídeo.</span><span class="sxs-lookup"><span data-stu-id="15803-119">If the video output detects a revoked device, it stops displaying video.</span></span> <span data-ttu-id="15803-120">Si envía este comando mientras HDCP está deshabilitado, la salida de vídeo valida el SRM y lo almacena.</span><span class="sxs-lookup"><span data-stu-id="15803-120">If you send this command while HDCP is disabled, the video output validates the SRM and stores it.</span></span> <span data-ttu-id="15803-121">Más adelante, si la aplicación habilita HDCP, la salida de vídeo usa el nuevo SRM para comprobar el estado de revocación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15803-121">Later, if the application enables HDCP, the video output uses the new SRM to check the device's revocation status.</span></span>

<span data-ttu-id="15803-122">Este comando puede hacer que el método **Configure** devuelva alguno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="15803-122">This command can cause the **Configure** method to return any of the following error codes.</span></span>



| <span data-ttu-id="15803-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="15803-123">Return code</span></span>                                            | <span data-ttu-id="15803-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="15803-124">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="15803-125">ERROR en el \_ \_ \_ SRM no válido de los gráficos OPM \_</span><span class="sxs-lookup"><span data-stu-id="15803-125">ERROR\_GRAPHICS\_OPM\_INVALID\_SRM</span></span>                     | <span data-ttu-id="15803-126">El SRM no es válido.</span><span class="sxs-lookup"><span data-stu-id="15803-126">The SRM is not valid.</span></span>                   |
| <span data-ttu-id="15803-127">el resultado de los gráficos de ERROR \_ \_ OPM \_ no es \_ \_ \_ compatible con \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="15803-127">ERROR\_GRAPHICS\_OPM\_OUTPUT\_DOES\_NOT\_SUPPORT\_HDCP</span></span> | <span data-ttu-id="15803-128">La salida de vídeo no es compatible con HDCP.</span><span class="sxs-lookup"><span data-stu-id="15803-128">The video output does not support HDCP.</span></span> |



 

<span data-ttu-id="15803-129">Este comando no se admite cuando la interfaz **IOPMVideoOutput** emula el protocolo de protección de la salida (COPP).</span><span class="sxs-lookup"><span data-stu-id="15803-129">This command is not supported when the **IOPMVideoOutput** interface emulates Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="15803-130">Cuando se usan semánticas de COPP, la aplicación es responsable de analizar SRMs y comprobar el estado de revocación del dispositivo HDCP.</span><span class="sxs-lookup"><span data-stu-id="15803-130">When COPP semantics are used, the application is responsible for parsing SRMs and checking the revocation status of the HDCP device.</span></span> <span data-ttu-id="15803-131">Use la solicitud de estado de [ \_ \_ \_ \_ \_ información del dispositivo HDCP Get Connected HDCP](opm-get-connected-hdcp-device-information.md) para obtener el vector de selección de clave (KSV) del dispositivo, que es necesario para comprobar el estado de revocación.</span><span class="sxs-lookup"><span data-stu-id="15803-131">Use the [OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION](opm-get-connected-hdcp-device-information.md) status request to get the device's key selection vector (KSV), which is needed to check the revocation status.</span></span> <span data-ttu-id="15803-132">Para obtener más información sobre SRMs, consulte la especificación de HDCP.</span><span class="sxs-lookup"><span data-stu-id="15803-132">For more information about SRMs, refer to the HDCP specification.</span></span>

## <a name="requirements"></a><span data-ttu-id="15803-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15803-133">Requirements</span></span>



| <span data-ttu-id="15803-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="15803-134">Requirement</span></span> | <span data-ttu-id="15803-135">Value</span><span class="sxs-lookup"><span data-stu-id="15803-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="15803-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15803-136">Minimum supported client</span></span><br/> | <span data-ttu-id="15803-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="15803-137">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="15803-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15803-138">Minimum supported server</span></span><br/> | <span data-ttu-id="15803-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="15803-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="15803-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15803-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="15803-141"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="15803-141"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15803-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="15803-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15803-143">**IOPMVideoOutput:: configure**</span><span class="sxs-lookup"><span data-stu-id="15803-143">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="15803-144">Comandos OPM</span><span class="sxs-lookup"><span data-stu-id="15803-144">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




