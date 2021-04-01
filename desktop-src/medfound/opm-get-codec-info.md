---
description: Obtiene el valor de mérito de un códec de hardware.
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: OPM_GET_CODEC_INFO (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf310ae3dafee7823119b2d5d5bd2c6b61fe822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275834"
---
# <a name="opm_get_codec_info"></a><span data-ttu-id="ef1cc-103">\_información del \_ códec de obtención de OPM \_</span><span class="sxs-lookup"><span data-stu-id="ef1cc-103">OPM\_GET\_CODEC\_INFO</span></span>

<span data-ttu-id="ef1cc-104">Obtiene el valor de mérito de un códec de hardware.</span><span class="sxs-lookup"><span data-stu-id="ef1cc-104">Gets the merit value of a hardware codec.</span></span>



| <span data-ttu-id="ef1cc-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef1cc-105">Requirement</span></span> | <span data-ttu-id="ef1cc-106">Value</span><span class="sxs-lookup"><span data-stu-id="ef1cc-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1cc-107">GUID de solicitud</span><span class="sxs-lookup"><span data-stu-id="ef1cc-107">Request GUID</span></span> | <span data-ttu-id="ef1cc-108">**\_información del \_ códec de obtención de OPM \_**</span><span class="sxs-lookup"><span data-stu-id="ef1cc-108">**OPM\_GET\_CODEC\_INFO**</span></span>                                                                 |
| <span data-ttu-id="ef1cc-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="ef1cc-109">Input data</span></span>   | <span data-ttu-id="ef1cc-110">Una estructura de [**\_ parámetros de \_ \_ información \_ de códec de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)</span><span class="sxs-lookup"><span data-stu-id="ef1cc-110">An [**OPM\_GET\_CODEC\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) structure</span></span>   |
| <span data-ttu-id="ef1cc-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="ef1cc-111">Return data</span></span>  | <span data-ttu-id="ef1cc-112">Una estructura de [**\_ información del códec de obtención de \_ \_ \_ información de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information)</span><span class="sxs-lookup"><span data-stu-id="ef1cc-112">An [**OPM\_GET\_CODEC\_INFO\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ef1cc-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef1cc-113">Remarks</span></span>

<span data-ttu-id="ef1cc-114">Aunque este comando usa la interfaz del [Administrador de protección de salida](output-protection-manager.md) (OPM), solo se aplica a los codificadores y descodificadores de hardware.</span><span class="sxs-lookup"><span data-stu-id="ef1cc-114">Although this command uses the [Output Protection Manager](output-protection-manager.md) (OPM) interface, it applies only to hardware encoders and decoders.</span></span> <span data-ttu-id="ef1cc-115">No se aplica a los dispositivos de salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ef1cc-115">It does not apply to video output devices.</span></span>

<span data-ttu-id="ef1cc-116">Por lo general, no debe usar este comando directamente.</span><span class="sxs-lookup"><span data-stu-id="ef1cc-116">Generally, you should not use this command directly.</span></span> <span data-ttu-id="ef1cc-117">Para obtener el valor de mérito de un códec de hardware, llame a la función [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) .</span><span class="sxs-lookup"><span data-stu-id="ef1cc-117">To get the merit value for a hardware codec, call the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function.</span></span> <span data-ttu-id="ef1cc-118">Esta función realiza todas las llamadas OPM necesarias para enviar el comando **OPM \_ Get \_ codec \_ info** .</span><span class="sxs-lookup"><span data-stu-id="ef1cc-118">This function performs all of the OPM calls needed to send the **OPM\_GET\_CODEC\_INFO** command.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef1cc-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef1cc-119">Requirements</span></span>



| <span data-ttu-id="ef1cc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef1cc-120">Requirement</span></span> | <span data-ttu-id="ef1cc-121">Value</span><span class="sxs-lookup"><span data-stu-id="ef1cc-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1cc-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef1cc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ef1cc-123">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ef1cc-123">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ef1cc-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef1cc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ef1cc-125">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ef1cc-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ef1cc-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef1cc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef1cc-127"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef1cc-127"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef1cc-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef1cc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef1cc-129">Solicitudes de estado de OPM</span><span class="sxs-lookup"><span data-stu-id="ef1cc-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> <dt>

[<span data-ttu-id="ef1cc-130">Administrador de protección de salida</span><span class="sxs-lookup"><span data-stu-id="ef1cc-130">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> <dt>

[<span data-ttu-id="ef1cc-131">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="ef1cc-131">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 




