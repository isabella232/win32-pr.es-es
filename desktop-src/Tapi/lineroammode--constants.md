---
description: Las \_ constantes de marcador de bits LINEROAMMODE describen el estado de itinerancia de un dispositivo de línea.
ms.assetid: af0eb263-8deb-44ab-8acb-00e4ff7930ab
title: Constantes de LINEROAMMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e40c40291567e7800b53070f882bf1e0bdac93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690260"
---
# <a name="lineroammode_-constants"></a><span data-ttu-id="7279d-103">Constantes de LINEROAMMODE \_</span><span class="sxs-lookup"><span data-stu-id="7279d-103">LINEROAMMODE\_ Constants</span></span>

<span data-ttu-id="7279d-104">Las constantes de marcador de bits **LINEROAMMODE \_** describen el estado de itinerancia de un dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="7279d-104">The **LINEROAMMODE\_** bit-flag constants describe the roaming status of a line device.</span></span>

<dl> <dt>

<span data-ttu-id="7279d-105"><span id="LINEROAMMODE_HOME"></span><span id="lineroammode_home"></span>**\_Página principal de LINEROAMMODE**</span><span class="sxs-lookup"><span data-stu-id="7279d-105"><span id="LINEROAMMODE_HOME"></span><span id="lineroammode_home"></span>**LINEROAMMODE\_HOME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7279d-106">La línea está conectada al nodo de red doméstica.</span><span class="sxs-lookup"><span data-stu-id="7279d-106">The line is connected to the home network node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7279d-107"><span id="LINEROAMMODE_ROAMA"></span><span id="lineroammode_roama"></span>**LINEROAMMODE \_ roaming**</span><span class="sxs-lookup"><span data-stu-id="7279d-107"><span id="LINEROAMMODE_ROAMA"></span><span id="lineroammode_roama"></span>**LINEROAMMODE\_ROAMA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7279d-108">La línea está conectada a la portadora itinerancia y las llamadas se cobran en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="7279d-108">The line is connected to the Roam-A carrier and calls are charged accordingly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7279d-109"><span id="LINEROAMMODE_ROAMB"></span><span id="lineroammode_roamb"></span>**LINEROAMMODE \_ ROAMB**</span><span class="sxs-lookup"><span data-stu-id="7279d-109"><span id="LINEROAMMODE_ROAMB"></span><span id="lineroammode_roamb"></span>**LINEROAMMODE\_ROAMB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7279d-110">La línea está conectada a la portadora de itinerancia y las llamadas se cobran en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="7279d-110">The line is connected to the Roam-B carrier and calls are charged accordingly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7279d-111"><span id="LINEROAMMODE_UNAVAIL"></span><span id="lineroammode_unavail"></span>**LINEROAMMODE no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="7279d-111"><span id="LINEROAMMODE_UNAVAIL"></span><span id="lineroammode_unavail"></span>**LINEROAMMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7279d-112">El modo de itinerancia no está disponible y no se conocerá.</span><span class="sxs-lookup"><span data-stu-id="7279d-112">The roam mode is unavailable and will not be known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7279d-113"><span id="LINEROAMMODE_UNKNOWN"></span><span id="lineroammode_unknown"></span>**LINEROAMMODE \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="7279d-113"><span id="LINEROAMMODE_UNKNOWN"></span><span id="lineroammode_unknown"></span>**LINEROAMMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7279d-114">El modo de itinerancia es desconocido actualmente, pero se puede conocer más adelante.</span><span class="sxs-lookup"><span data-stu-id="7279d-114">The roam mode is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7279d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7279d-115">Remarks</span></span>

<span data-ttu-id="7279d-116">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="7279d-116">No extensibility.</span></span> <span data-ttu-id="7279d-117">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="7279d-117">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="7279d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7279d-118">Requirements</span></span>



| <span data-ttu-id="7279d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7279d-119">Requirement</span></span> | <span data-ttu-id="7279d-120">Value</span><span class="sxs-lookup"><span data-stu-id="7279d-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7279d-121">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="7279d-121">TAPI version</span></span><br/> | <span data-ttu-id="7279d-122">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="7279d-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7279d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7279d-123">Header</span></span><br/>       | <dl> <span data-ttu-id="7279d-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7279d-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




