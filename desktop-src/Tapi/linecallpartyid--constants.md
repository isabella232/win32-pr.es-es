---
description: Las \_ constantes de marcador de bits LINECALLPARTYID describen la naturaleza de la información disponible sobre las entidades implicadas en una llamada.
ms.assetid: e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db
title: Constantes de LINECALLPARTYID_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5dd8cca75fe6e91b97fac63dca6c0fdda554394
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690966"
---
# <a name="linecallpartyid_-constants"></a><span data-ttu-id="f3a42-103">Constantes de LINECALLPARTYID \_</span><span class="sxs-lookup"><span data-stu-id="f3a42-103">LINECALLPARTYID\_ Constants</span></span>

<span data-ttu-id="f3a42-104">Las constantes de marcador de bits **LINECALLPARTYID \_** describen la naturaleza de la información disponible sobre las entidades implicadas en una llamada.</span><span class="sxs-lookup"><span data-stu-id="f3a42-104">The **LINECALLPARTYID\_** bit-flag constants describe the nature of the information available about the parties involved in a call.</span></span>

<dl> <dt>

<span data-ttu-id="f3a42-105"><span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**Dirección de LINECALLPARTYID \_**</span><span class="sxs-lookup"><span data-stu-id="f3a42-105"><span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**LINECALLPARTYID\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3a42-106">La información del identificador de entidad consta de la dirección de la entidad en formato de dirección canónico o en formato de dirección de marcado.</span><span class="sxs-lookup"><span data-stu-id="f3a42-106">Party identifier information consists of the party's address in either canonical address format or dialable address format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3a42-107"><span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**LINECALLPARTYID \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="f3a42-107"><span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**LINECALLPARTYID\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3a42-108">La información del identificador de entidad no está disponible porque la parte remota la ha bloqueado.</span><span class="sxs-lookup"><span data-stu-id="f3a42-108">Party identifier information is not available because it has been blocked by the remote party.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3a42-109"><span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**nombre de LINECALLPARTYID \_**</span><span class="sxs-lookup"><span data-stu-id="f3a42-109"><span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**LINECALLPARTYID\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3a42-110">La información del identificador de entidad consta del nombre de la entidad (como, por ejemplo, de un directorio mantenido dentro del conmutador).</span><span class="sxs-lookup"><span data-stu-id="f3a42-110">Party identifier information consists of the party's name (as, for example, from a directory kept inside the switch).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3a42-111"><span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**LINECALLPARTYID \_ OUTOFAREA**</span><span class="sxs-lookup"><span data-stu-id="f3a42-111"><span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**LINECALLPARTYID\_OUTOFAREA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3a42-112">La información del identificador del autor de la llamada no está disponible porque la red no la propaga todo.</span><span class="sxs-lookup"><span data-stu-id="f3a42-112">Caller ID information for the call is not available because it is not propagated all the way by the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3a42-113"><span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**LINECALLPARTYID \_ parcial**</span><span class="sxs-lookup"><span data-stu-id="f3a42-113"><span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**LINECALLPARTYID\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3a42-114">La información del identificador de entidad es válida, pero solo se limita a la información parcial.</span><span class="sxs-lookup"><span data-stu-id="f3a42-114">Party identifier information is valid but it is limited to partial information only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3a42-115"><span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**LINECALLPARTYID no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="f3a42-115"><span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**LINECALLPARTYID\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3a42-116">La información del identificador de entidad no está disponible y no estará disponible más adelante.</span><span class="sxs-lookup"><span data-stu-id="f3a42-116">Party identifier information is not available and will not become available later.</span></span> <span data-ttu-id="f3a42-117">Es posible que la información no esté disponible por motivos no especificados.</span><span class="sxs-lookup"><span data-stu-id="f3a42-117">Information may be unavailable for unspecified reasons.</span></span> <span data-ttu-id="f3a42-118">Por ejemplo, la red no entregó la información, por lo que el proveedor de servicios la omitió, etc.</span><span class="sxs-lookup"><span data-stu-id="f3a42-118">For example, the information was not delivered by the network, it was ignored by the service provider, and so forth.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3a42-119"><span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**LINECALLPARTYID \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="f3a42-119"><span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**LINECALLPARTYID\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3a42-120">Actualmente, la información de identificador de entidad es desconocida, pero se puede conocer más adelante.</span><span class="sxs-lookup"><span data-stu-id="f3a42-120">Party identifier information is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3a42-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3a42-121">Remarks</span></span>

<span data-ttu-id="f3a42-122">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="f3a42-122">No extensibility.</span></span> <span data-ttu-id="f3a42-123">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="f3a42-123">All 32 bits are reserved.</span></span>

<span data-ttu-id="f3a42-124">Para cada una de las partes posibles implicadas en una llamada, las constantes de **LINECALLPARTYID \_** describen cómo se da formato a la información de identificador de entidad.</span><span class="sxs-lookup"><span data-stu-id="f3a42-124">For each of the possible parties involved in a call, the **LINECALLPARTYID\_** constants describe how the party identifier information is formatted.</span></span> <span data-ttu-id="f3a42-125">Esta información se proporciona en la estructura de datos [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="f3a42-125">This information is supplied in the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3a42-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3a42-126">Requirements</span></span>



| <span data-ttu-id="f3a42-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3a42-127">Requirement</span></span> | <span data-ttu-id="f3a42-128">Value</span><span class="sxs-lookup"><span data-stu-id="f3a42-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f3a42-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="f3a42-129">TAPI version</span></span><br/> | <span data-ttu-id="f3a42-130">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f3a42-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f3a42-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3a42-131">Header</span></span><br/>       | <dl> <span data-ttu-id="f3a42-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3a42-132"><dt>Tapi.h</dt></span></span> </dl> |



 

 




