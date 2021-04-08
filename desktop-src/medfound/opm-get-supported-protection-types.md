---
description: Devuelve la lista de mecanismos de protección admitidos por el conector.
ms.assetid: dd4cdd3c-6bb5-4427-827d-f3e909e752e5
title: OPM_GET_SUPPORTED_PROTECTION_TYPES (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc79b33673e34d00914b84165d915baa0d8f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001447"
---
# <a name="opm_get_supported_protection_types"></a><span data-ttu-id="8e438-103">\_tipos de \_ protección compatible con OPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="8e438-103">OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES</span></span>

<span data-ttu-id="8e438-104">Devuelve la lista de mecanismos de protección admitidos por el conector.</span><span class="sxs-lookup"><span data-stu-id="8e438-104">Returns the list of protection mechanisms that are supported by the connector.</span></span>



| <span data-ttu-id="8e438-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e438-105">Requirement</span></span> | <span data-ttu-id="8e438-106">Value</span><span class="sxs-lookup"><span data-stu-id="8e438-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8e438-107">GUID de solicitud</span><span class="sxs-lookup"><span data-stu-id="8e438-107">Request GUID</span></span> | <span data-ttu-id="8e438-108">\_tipos de \_ protección compatible con OPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="8e438-108">OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES</span></span>                                      |
| <span data-ttu-id="8e438-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="8e438-109">Input data</span></span>   | <span data-ttu-id="8e438-110">None</span><span class="sxs-lookup"><span data-stu-id="8e438-110">None</span></span>                                                                        |
| <span data-ttu-id="8e438-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="8e438-111">Return data</span></span>  | <span data-ttu-id="8e438-112">Una estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="8e438-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8e438-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e438-113">Remarks</span></span>

<span data-ttu-id="8e438-114">Los mecanismos de protección se devuelven en el miembro **ulInformation** de la estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="8e438-114">The protection mechanisms are returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="8e438-115">El valor es **una operación OR bit a bit** de marcas de tipo de [protección OPM](opm-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="8e438-115">The value is a bitwise **OR** of [OPM Protection Type Flags](opm-protection-type-flags.md).</span></span>

<span data-ttu-id="8e438-116">Esta consulta es equivalente a la \_ consulta COPPQueryProtectionType de DXVA usada en el protocolo de protección de la salida certificada (COPP).</span><span class="sxs-lookup"><span data-stu-id="8e438-116">This query is equivalent to the DXVA\_COPPQueryProtectionType query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e438-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e438-117">Requirements</span></span>



| <span data-ttu-id="8e438-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e438-118">Requirement</span></span> | <span data-ttu-id="8e438-119">Value</span><span class="sxs-lookup"><span data-stu-id="8e438-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8e438-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e438-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8e438-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8e438-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8e438-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e438-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8e438-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e438-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8e438-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e438-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e438-125"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e438-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e438-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e438-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e438-127">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="8e438-127">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="8e438-128">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="8e438-128">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="8e438-129">Solicitudes de estado de OPM</span><span class="sxs-lookup"><span data-stu-id="8e438-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




