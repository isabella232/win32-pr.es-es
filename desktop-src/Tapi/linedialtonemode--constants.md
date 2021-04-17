---
description: Las \_ constantes de marcador de bits LINEDIALTONEMODE describen diferentes tipos de tonos de marcado. Un tono de marcado especial suele tener un significado especial (como en el mensaje en espera).
ms.assetid: 0b040482-35cf-42e8-84bc-33002635b591
title: Constantes de LINEDIALTONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5128f2a176f3aeaf92bc3487b131b7720568085e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690040"
---
# <a name="linedialtonemode_-constants"></a><span data-ttu-id="49cf6-104">Constantes de LINEDIALTONEMODE \_</span><span class="sxs-lookup"><span data-stu-id="49cf6-104">LINEDIALTONEMODE\_ Constants</span></span>

<span data-ttu-id="49cf6-105">Las constantes de marcador de bits **LINEDIALTONEMODE \_** describen diferentes tipos de tonos de marcado.</span><span class="sxs-lookup"><span data-stu-id="49cf6-105">The **LINEDIALTONEMODE\_** bit-flag constants describe different types of dial tones.</span></span> <span data-ttu-id="49cf6-106">Un tono de marcado especial suele tener un significado especial (como en el mensaje en espera).</span><span class="sxs-lookup"><span data-stu-id="49cf6-106">A special dial tone typically carries a special meaning (as with message waiting).</span></span>

<dl> <dt>

<span data-ttu-id="49cf6-107"><span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE \_ externo**</span><span class="sxs-lookup"><span data-stu-id="49cf6-107"><span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE\_EXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49cf6-108">Se trata de un tono de marcado externo (red pública).</span><span class="sxs-lookup"><span data-stu-id="49cf6-108">This is an external (public network) dial tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49cf6-109"><span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE \_ interno**</span><span class="sxs-lookup"><span data-stu-id="49cf6-109"><span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49cf6-110">Se trata de un tono de marcado interno, como en una PBX.</span><span class="sxs-lookup"><span data-stu-id="49cf6-110">This is an internal dial tone, as within a PBX.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49cf6-111"><span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE \_ normal**</span><span class="sxs-lookup"><span data-stu-id="49cf6-111"><span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE\_NORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49cf6-112">Se trata de un tono de marcado normal, que normalmente es un tono continuo.</span><span class="sxs-lookup"><span data-stu-id="49cf6-112">This is a normal dial tone, which typically is a continuous tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49cf6-113"><span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE \_ especial**</span><span class="sxs-lookup"><span data-stu-id="49cf6-113"><span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE\_SPECIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49cf6-114">Se trata de un tono de marcado especial que indica que una condición determinada (conocida por el conmutador o la red) está actualmente en vigor.</span><span class="sxs-lookup"><span data-stu-id="49cf6-114">This is a special dial tone indicating that a certain condition (known by the switch or network) is currently in effect.</span></span> <span data-ttu-id="49cf6-115">Los tonos de marcado especiales suelen usar un tono interrumpido.</span><span class="sxs-lookup"><span data-stu-id="49cf6-115">Special dial tones typically use an interrupted tone.</span></span> <span data-ttu-id="49cf6-116">Al igual que con un tono de marcado normal, esto indica que el conmutador está listo para recibir el número que se va a marcar.</span><span class="sxs-lookup"><span data-stu-id="49cf6-116">As with a normal dial tone, this indicates that the switch is ready to receive the number to be dialed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49cf6-117"><span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="49cf6-117"><span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49cf6-118">El modo de tono de marcado no está disponible y no se conocerá.</span><span class="sxs-lookup"><span data-stu-id="49cf6-118">The dial tone mode is unavailable and will not become known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49cf6-119"><span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="49cf6-119"><span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49cf6-120">El modo de tono de marcado no se conoce actualmente, pero puede ser conocido más adelante.</span><span class="sxs-lookup"><span data-stu-id="49cf6-120">The dial tone mode is not currently known but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49cf6-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49cf6-121">Remarks</span></span>

<span data-ttu-id="49cf6-122">Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="49cf6-122">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="49cf6-123">Los 16 bits de orden inferior están reservados.</span><span class="sxs-lookup"><span data-stu-id="49cf6-123">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="49cf6-124">Las **\_ constantes LINEDIALTONEMODE** se usan dentro de la estructura de datos [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) para una llamada en el estado de marcado.</span><span class="sxs-lookup"><span data-stu-id="49cf6-124">The **LINEDIALTONEMODE\_constants** are used within the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) data structure for a call in the dialtone state.</span></span>

## <a name="requirements"></a><span data-ttu-id="49cf6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49cf6-125">Requirements</span></span>



| <span data-ttu-id="49cf6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="49cf6-126">Requirement</span></span> | <span data-ttu-id="49cf6-127">Value</span><span class="sxs-lookup"><span data-stu-id="49cf6-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="49cf6-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="49cf6-128">TAPI version</span></span><br/> | <span data-ttu-id="49cf6-129">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="49cf6-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="49cf6-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49cf6-130">Header</span></span><br/>       | <dl> <span data-ttu-id="49cf6-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="49cf6-131"><dt>Tapi.h</dt></span></span> </dl> |



 

 




