---
description: Consulta si un conector de la interfaz de vídeo digital (DVI) admite DVI versión 1,1 o posterior.
ms.assetid: b6c450c0-e97f-472d-ae09-fa1e062aeb9e
title: OPM_GET_DVI_CHARACTERISTICS (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6f996b0397db509a45af6e243359c581df333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082291"
---
# <a name="opm_get_dvi_characteristics"></a><span data-ttu-id="6d847-103">características de la \_ obtención de \_ DVI de OPM \_</span><span class="sxs-lookup"><span data-stu-id="6d847-103">OPM\_GET\_DVI\_CHARACTERISTICS</span></span>

<span data-ttu-id="6d847-104">Consulta si un conector de la interfaz de vídeo digital (DVI) admite DVI versión 1,1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="6d847-104">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>



| <span data-ttu-id="6d847-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d847-105">Requirement</span></span> | <span data-ttu-id="6d847-106">Value</span><span class="sxs-lookup"><span data-stu-id="6d847-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6d847-107">GUID de solicitud</span><span class="sxs-lookup"><span data-stu-id="6d847-107">Request GUID</span></span> | <span data-ttu-id="6d847-108">características de la \_ obtención de \_ DVI de OPM \_</span><span class="sxs-lookup"><span data-stu-id="6d847-108">OPM\_GET\_DVI\_CHARACTERISTICS</span></span>                                              |
| <span data-ttu-id="6d847-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="6d847-109">Input data</span></span>   | <span data-ttu-id="6d847-110">None</span><span class="sxs-lookup"><span data-stu-id="6d847-110">None</span></span>                                                                        |
| <span data-ttu-id="6d847-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="6d847-111">Return data</span></span>  | <span data-ttu-id="6d847-112">Una estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="6d847-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6d847-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d847-113">Remarks</span></span>

<span data-ttu-id="6d847-114">Si esta consulta se realiza correctamente, el miembro **ulInformation** de la estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="6d847-114">If this query succeeds, the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure contains one of the following values.</span></span>



| <span data-ttu-id="6d847-115">Value</span><span class="sxs-lookup"><span data-stu-id="6d847-115">Value</span></span>                                     | <span data-ttu-id="6d847-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d847-116">Description</span></span>               |
|-------------------------------------------|---------------------------|
| <span data-ttu-id="6d847-117">Característica de DVI de OPM \_ \_ \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6d847-117">OPM\_DVI\_CHARACTERISTIC\_1\_0</span></span>            | <span data-ttu-id="6d847-118">DVI versión 1,0.</span><span class="sxs-lookup"><span data-stu-id="6d847-118">DVI version 1.0.</span></span>          |
| <span data-ttu-id="6d847-119">\_ \_ Característica de DVI \_ de la versión 1 \_ 1 \_ o \_ superior de OPM</span><span class="sxs-lookup"><span data-stu-id="6d847-119">OPM\_DVI\_CHARACTERISTIC\_1\_1\_OR\_ABOVE</span></span> | <span data-ttu-id="6d847-120">DVI versión 1,1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="6d847-120">DVI version 1.1 or later.</span></span> |



 

<span data-ttu-id="6d847-121">Esta consulta solo se admite cuando el tipo de conector físico es el tipo de conector de OPM \_ \_ \_ DVI.</span><span class="sxs-lookup"><span data-stu-id="6d847-121">This query is supported only when the physical connector type is OPM\_CONNECTOR\_TYPE\_DVI.</span></span> <span data-ttu-id="6d847-122">Para obtener el tipo de conector, envíe la consulta de [**\_ tipo de \_ conector \_ OPM Get**](opm-get-connector-type.md) .</span><span class="sxs-lookup"><span data-stu-id="6d847-122">To get the connector type, send the [**OPM\_GET\_CONNECTOR\_TYPE**](opm-get-connector-type.md) query.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d847-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d847-123">Requirements</span></span>



| <span data-ttu-id="6d847-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d847-124">Requirement</span></span> | <span data-ttu-id="6d847-125">Value</span><span class="sxs-lookup"><span data-stu-id="6d847-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6d847-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d847-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6d847-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6d847-127">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6d847-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d847-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6d847-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6d847-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6d847-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d847-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d847-131"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d847-131"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d847-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d847-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d847-133">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="6d847-133">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="6d847-134">Solicitudes de estado de OPM</span><span class="sxs-lookup"><span data-stu-id="6d847-134">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




