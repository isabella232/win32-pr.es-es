---
description: Especifica información sobre la señal de vídeo, excepto el nivel de protección.
ms.assetid: ed78b7eb-bf15-4068-ab86-ae42a5e62096
title: OPM_SET_ACP_AND_CGMSA_SIGNALING (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02247c48b89e61d49afe7f8f6f3821da68ff050b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543859"
---
# <a name="opm_set_acp_and_cgmsa_signaling"></a><span data-ttu-id="e4f12-103">\_configuración \_ de la \_ \_ señalización de CGMSA de OPM y ACP \_</span><span class="sxs-lookup"><span data-stu-id="e4f12-103">OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>

<span data-ttu-id="e4f12-104">Especifica información sobre la señal de vídeo, excepto el nivel de protección.</span><span class="sxs-lookup"><span data-stu-id="e4f12-104">Specifies information about the video signal, other than the protection level.</span></span>



| <span data-ttu-id="e4f12-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4f12-105">Requirement</span></span> | <span data-ttu-id="e4f12-106">Value</span><span class="sxs-lookup"><span data-stu-id="e4f12-106">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f12-107">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="e4f12-107">Command GUID</span></span> | <span data-ttu-id="e4f12-108">\_configuración \_ de la \_ \_ señalización de CGMSA de OPM y ACP \_</span><span class="sxs-lookup"><span data-stu-id="e4f12-108">OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>                                                                                |
| <span data-ttu-id="e4f12-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="e4f12-109">Input data</span></span>   | <span data-ttu-id="e4f12-110">Una [**estructura \_ \_ \_ de \_ \_ \_ parámetros de señalización de CGMSA de OPM y set ACP**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters)</span><span class="sxs-lookup"><span data-stu-id="e4f12-110">An [**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e4f12-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e4f12-111">Remarks</span></span>

<span data-ttu-id="e4f12-112">Este comando es equivalente al comando DXVA \_ COPPSetSignaling usado en el protocolo de protección de la salida certificada (COPP).</span><span class="sxs-lookup"><span data-stu-id="e4f12-112">This command is equivalent to the DXVA\_COPPSetSignaling command used in Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="e4f12-113">En el caso de CGMS-A, determinados estándares de protección requieren que la señal de televisión contenga información dentro de los mismos paquetes de forma de onda de VBI que los bits de CGMS-A.</span><span class="sxs-lookup"><span data-stu-id="e4f12-113">For CGMS-A, certain protection standards require that the television signal contain information within the same VBI waveform packets as the CGMS-A bits.</span></span> <span data-ttu-id="e4f12-114">Entre otras cosas, esta información incluye la relación de aspecto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="e4f12-114">Among other things, this information includes the picture aspect ratio.</span></span> <span data-ttu-id="e4f12-115">Los televisores pueden mostrarse mal si la información de la relación de aspecto no es coherente con el flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e4f12-115">Televisions may display poorly if the aspect ratio information is not consistent with the video stream.</span></span> <span data-ttu-id="e4f12-116">La aplicación puede usar este comando para especificar la relación de aspecto de modo que el controlador de gráficos pueda generar los paquetes VBI correctos.</span><span class="sxs-lookup"><span data-stu-id="e4f12-116">The application can use this command to specify the aspect ratio so that the graphics driver can generate the correct VBI packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4f12-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4f12-117">Requirements</span></span>



| <span data-ttu-id="e4f12-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4f12-118">Requirement</span></span> | <span data-ttu-id="e4f12-119">Value</span><span class="sxs-lookup"><span data-stu-id="e4f12-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f12-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4f12-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e4f12-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e4f12-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e4f12-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4f12-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e4f12-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4f12-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e4f12-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4f12-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4f12-125"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4f12-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4f12-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4f12-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4f12-127">**IOPMVideoOutput:: configure**</span><span class="sxs-lookup"><span data-stu-id="e4f12-127">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="e4f12-128">Comandos OPM</span><span class="sxs-lookup"><span data-stu-id="e4f12-128">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




