---
description: Devuelve el tipo de bus de e/s utilizado por la salida del vídeo.
ms.assetid: 1aff4c81-ffa0-4116-b7ea-60b1b83042df
title: OPM_GET_ADAPTER_BUS_TYPE (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde3611eb00977670c59c4326f793c1cb9037fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715528"
---
# <a name="opm_get_adapter_bus_type"></a><span data-ttu-id="52605-103">\_tipo de \_ bus de adaptador OPM Get \_ \_</span><span class="sxs-lookup"><span data-stu-id="52605-103">OPM\_GET\_ADAPTER\_BUS\_TYPE</span></span>

<span data-ttu-id="52605-104">Devuelve el tipo de bus de e/s utilizado por la salida del vídeo.</span><span class="sxs-lookup"><span data-stu-id="52605-104">Returns the type of I/O bus used by the video output.</span></span>



| <span data-ttu-id="52605-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="52605-105">Requirement</span></span> | <span data-ttu-id="52605-106">Value</span><span class="sxs-lookup"><span data-stu-id="52605-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="52605-107">GUID de solicitud</span><span class="sxs-lookup"><span data-stu-id="52605-107">Request GUID</span></span> | <span data-ttu-id="52605-108">\_tipo de \_ bus de adaptador OPM Get \_ \_</span><span class="sxs-lookup"><span data-stu-id="52605-108">OPM\_GET\_ADAPTER\_BUS\_TYPE</span></span>                                                |
| <span data-ttu-id="52605-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="52605-109">Input data</span></span>   | <span data-ttu-id="52605-110">None</span><span class="sxs-lookup"><span data-stu-id="52605-110">None</span></span>                                                                        |
| <span data-ttu-id="52605-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="52605-111">Return data</span></span>  | <span data-ttu-id="52605-112">Una estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="52605-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="52605-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52605-113">Remarks</span></span>

<span data-ttu-id="52605-114">El tipo de bus se devuelve en el miembro **ulInformation** de la estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="52605-114">The bus type is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="52605-115">El valor es **una operación OR bit a bit** de marcas de tipo de [**bus OPM**](opm-bus-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="52605-115">The value is a bitwise **OR** of [**OPM Bus Type Flags**](opm-bus-type-flags.md).</span></span>

<span data-ttu-id="52605-116">Esta consulta es equivalente a la \_ consulta COPPQueryBusData de DXVA usada en el protocolo de protección de la salida certificada (COPP).</span><span class="sxs-lookup"><span data-stu-id="52605-116">This query is equivalent to the DXVA\_COPPQueryBusData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="52605-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52605-117">Requirements</span></span>



| <span data-ttu-id="52605-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="52605-118">Requirement</span></span> | <span data-ttu-id="52605-119">Value</span><span class="sxs-lookup"><span data-stu-id="52605-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="52605-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52605-120">Minimum supported client</span></span><br/> | <span data-ttu-id="52605-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="52605-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="52605-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52605-122">Minimum supported server</span></span><br/> | <span data-ttu-id="52605-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="52605-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="52605-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52605-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="52605-125"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="52605-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52605-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="52605-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52605-127">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="52605-127">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="52605-128">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="52605-128">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="52605-129">Solicitudes de estado de OPM</span><span class="sxs-lookup"><span data-stu-id="52605-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




