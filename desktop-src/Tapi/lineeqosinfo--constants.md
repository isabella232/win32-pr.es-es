---
description: Un TSP usa estas constantes para identificar el resultado de una solicitud QoS (calidad de servicio).
ms.assetid: 617ddbf4-212f-4990-93c2-f38f04b035ab
title: Constantes de LINEEQOSINFO_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423cc6172a1c6c87c1f3bb38929f727a15dad5c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680910"
---
# <a name="lineeqosinfo_-constants"></a><span data-ttu-id="4c327-103">Constantes de LINEEQOSINFO \_</span><span class="sxs-lookup"><span data-stu-id="4c327-103">LINEEQOSINFO\_ Constants</span></span>

<span data-ttu-id="4c327-104">Un TSP usa estas constantes para identificar el resultado de una solicitud QoS (calidad de servicio).</span><span class="sxs-lookup"><span data-stu-id="4c327-104">These constants are used by a TSP to identify the result of a QoS (Quality of Service) request.</span></span>

<dl> <dt>

<span data-ttu-id="4c327-105"><span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**LINEEQOSINFO \_ NOQOS**</span><span class="sxs-lookup"><span data-stu-id="4c327-105"><span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**LINEEQOSINFO\_NOQOS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="4c327-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4c327-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="4c327-107">QoS no está disponible.</span><span class="sxs-lookup"><span data-stu-id="4c327-107">QoS is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c327-108"><span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**LINEEQOSINFO \_ ADMISSIONFAILURE**</span><span class="sxs-lookup"><span data-stu-id="4c327-108"><span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**LINEEQOSINFO\_ADMISSIONFAILURE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="4c327-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4c327-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="4c327-110">No se pudo cumplir la solicitud QoS.</span><span class="sxs-lookup"><span data-stu-id="4c327-110">The QoS request could not be met.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c327-111"><span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**LINEEQOSINFO \_ POLICYFAILURE**</span><span class="sxs-lookup"><span data-stu-id="4c327-111"><span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**LINEEQOSINFO\_POLICYFAILURE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="4c327-112">0x00000003</span><span class="sxs-lookup"><span data-stu-id="4c327-112">0x00000003</span></span>
</dt> <dt>



<span data-ttu-id="4c327-113">No se admite el tipo de QoS solicitado.</span><span class="sxs-lookup"><span data-stu-id="4c327-113">The type of QoS requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c327-114"><span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**LINEEQOSINFO \_ GENERICERROR**</span><span class="sxs-lookup"><span data-stu-id="4c327-114"><span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**LINEEQOSINFO\_GENERICERROR**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="4c327-115">0x00000004</span><span class="sxs-lookup"><span data-stu-id="4c327-115">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="4c327-116">Error de QoS no especificado.</span><span class="sxs-lookup"><span data-stu-id="4c327-116">Unspecified QoS error.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c327-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c327-117">Requirements</span></span>



| <span data-ttu-id="4c327-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c327-118">Requirement</span></span> | <span data-ttu-id="4c327-119">Value</span><span class="sxs-lookup"><span data-stu-id="4c327-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4c327-120">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="4c327-120">TAPI version</span></span><br/> | <span data-ttu-id="4c327-121">Requiere TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="4c327-121">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="4c327-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c327-122">Header</span></span><br/>       | <dl> <span data-ttu-id="4c327-123"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c327-123"><dt>Tspi.h</dt></span></span> </dl> |



 

 




