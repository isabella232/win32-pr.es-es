---
description: Establece el nivel de protección de HDCP para la reproducción de DVD, siguiendo las reglas del sistema de cifrado de contenido (CSS) de DVD.
ms.assetid: 8d9ecb9b-8528-4b23-ab2f-234ba2cb7ed0
title: OPM_SET_PROTECTION_LEVEL_ACCORDING_TO_CSS_DVD (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971d288367bdc5c59e11bdfd5b86fb233755c95e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155340"
---
# <a name="opm_set_protection_level_according_to_css_dvd"></a><span data-ttu-id="6f670-103">\_configuración \_ \_ \_ de nivel de protección de OPM según el \_ \_ DVD de CSS \_</span><span class="sxs-lookup"><span data-stu-id="6f670-103">OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD</span></span>

<span data-ttu-id="6f670-104">Establece el nivel de protección de HDCP para la reproducción de DVD, siguiendo las reglas del sistema de cifrado de contenido (CSS) de DVD.</span><span class="sxs-lookup"><span data-stu-id="6f670-104">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span>



| <span data-ttu-id="6f670-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f670-105">Requirement</span></span> | <span data-ttu-id="6f670-106">Value</span><span class="sxs-lookup"><span data-stu-id="6f670-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f670-107">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="6f670-107">Command GUID</span></span> | <span data-ttu-id="6f670-108">\_configuración \_ \_ \_ de nivel de protección de OPM según el \_ \_ DVD de CSS \_</span><span class="sxs-lookup"><span data-stu-id="6f670-108">OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD</span></span>                                                |
| <span data-ttu-id="6f670-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="6f670-109">Input data</span></span>   | <span data-ttu-id="6f670-110">Una estructura de [**parámetros de nivel de protección de \_ configuración \_ \_ \_ de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)</span><span class="sxs-lookup"><span data-stu-id="6f670-110">An [**OPM\_SET\_PROTECTION\_LEVEL\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6f670-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f670-111">Remarks</span></span>

<span data-ttu-id="6f670-112">Este comando se usa para establecer High-Bandwidth Content Protection digital (HDCP) al reproducir DVDs estándar.</span><span class="sxs-lookup"><span data-stu-id="6f670-112">This command is used to set High-Bandwidth Digital Content Protection (HDCP) when playing standard DVDs.</span></span> <span data-ttu-id="6f670-113">A diferencia del [**comando \_ set \_ PROTECTION \_ LEVEL de OPM**](opm-set-protection-level.md) , si no se puede establecer HDCP por alguna razón, este comando no detiene la reproducción.</span><span class="sxs-lookup"><span data-stu-id="6f670-113">Unlike the [**OPM\_SET\_PROTECTION\_LEVEL**](opm-set-protection-level.md) command, if HDCP cannot be set for some reason, this command does not stop playback.</span></span> <span data-ttu-id="6f670-114">(Las reglas de CSS de DVD contienen un aprovisionamiento de "mejor esfuerzo" para los reproductores). De lo contrario, este comando es idéntico al comando de **nivel de protección de set de OPM \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="6f670-114">(DVD CSS rules contain a "best effort" provision for players.) Otherwise, this command is identical to the **OPM\_SET\_PROTECTION\_LEVEL** command.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f670-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f670-115">Requirements</span></span>



| <span data-ttu-id="6f670-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f670-116">Requirement</span></span> | <span data-ttu-id="6f670-117">Value</span><span class="sxs-lookup"><span data-stu-id="6f670-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6f670-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f670-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6f670-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6f670-119">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6f670-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f670-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6f670-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f670-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6f670-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f670-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f670-123"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f670-123"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f670-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f670-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f670-125">**IOPMVideoOutput:: configure**</span><span class="sxs-lookup"><span data-stu-id="6f670-125">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="6f670-126">Comandos OPM</span><span class="sxs-lookup"><span data-stu-id="6f670-126">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




