---
description: Un TSP usa estas constantes para identificar el tipo de nivel de QoS (calidad de servicio) necesario.
ms.assetid: 9fc3f6eb-7103-43c5-84f8-3842757e5be7
title: Constantes de LINEQOSSERVICELEVEL_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c0629715e461a15e21e1730f86edb61d83d60db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690750"
---
# <a name="lineqosservicelevel_-constants"></a><span data-ttu-id="ce32e-103">Constantes de LINEQOSSERVICELEVEL \_</span><span class="sxs-lookup"><span data-stu-id="ce32e-103">LINEQOSSERVICELEVEL\_ Constants</span></span>

<span data-ttu-id="ce32e-104">Un TSP usa estas constantes para identificar el tipo de nivel de QoS (calidad de servicio) necesario.</span><span class="sxs-lookup"><span data-stu-id="ce32e-104">These constants are used by a TSP to identify the type of a QoS (Quality of Service) level required.</span></span>

<dl> <dt>

<span data-ttu-id="ce32e-105"><span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**LINEQOSSERVICELEVEL \_ necesaria**</span><span class="sxs-lookup"><span data-stu-id="ce32e-105"><span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**LINEQOSSERVICELEVEL\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="ce32e-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ce32e-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="ce32e-107">El nivel de calidad de servicio solicitado es un requisito.</span><span class="sxs-lookup"><span data-stu-id="ce32e-107">The quality of service level requested is a requirement.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce32e-108"><span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**LINEQOSSERVICELEVEL \_ IFAVAILABLE**</span><span class="sxs-lookup"><span data-stu-id="ce32e-108"><span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**LINEQOSSERVICELEVEL\_IFAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="ce32e-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ce32e-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="ce32e-110">El nivel de calidad de servicio necesario, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="ce32e-110">The quality of service level required, if available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce32e-111"><span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**LINEQOSSERVICELEVEL \_ BESTEFFORT**</span><span class="sxs-lookup"><span data-stu-id="ce32e-111"><span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**LINEQOSSERVICELEVEL\_BESTEFFORT**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="ce32e-112">0x00000003</span><span class="sxs-lookup"><span data-stu-id="ce32e-112">0x00000003</span></span>
</dt> <dt>



<span data-ttu-id="ce32e-113">El nivel de calidad de servicio necesario es "mejor esfuerzo".</span><span class="sxs-lookup"><span data-stu-id="ce32e-113">The quality of service level required is "best effort."</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce32e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce32e-114">Requirements</span></span>



| <span data-ttu-id="ce32e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce32e-115">Requirement</span></span> | <span data-ttu-id="ce32e-116">Value</span><span class="sxs-lookup"><span data-stu-id="ce32e-116">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ce32e-117">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="ce32e-117">TAPI version</span></span><br/> | <span data-ttu-id="ce32e-118">Requiere TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="ce32e-118">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="ce32e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce32e-119">Header</span></span><br/>       | <dl> <span data-ttu-id="ce32e-120"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce32e-120"><dt>Tspi.h</dt></span></span> </dl> |



 

 




