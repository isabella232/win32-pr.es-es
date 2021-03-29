---
description: Las \_ constantes LINECALLORIGIN describen el origen de una llamada.
ms.assetid: b830a40e-62d9-4a6c-b43f-8318f30a7cd4
title: Constantes de LINECALLORIGIN_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00495d67dcff56ef7ee34cd85600a281e006ec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679339"
---
# <a name="linecallorigin_-constants"></a><span data-ttu-id="a8646-103">Constantes de LINECALLORIGIN \_</span><span class="sxs-lookup"><span data-stu-id="a8646-103">LINECALLORIGIN\_ Constants</span></span>

<span data-ttu-id="a8646-104">Las **constantes \_ LINECALLORIGIN** describen el origen de una llamada.</span><span class="sxs-lookup"><span data-stu-id="a8646-104">The **LINECALLORIGIN\_** constants describe the origin of a call.</span></span>

<dl> <dt>

<span data-ttu-id="a8646-105"><span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**Conferencia de LINECALLORIGIN \_**</span><span class="sxs-lookup"><span data-stu-id="a8646-105"><span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**LINECALLORIGIN\_CONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8646-106">El identificador de llamada es para una llamada de conferencia, es decir, es la conexión de la aplicación al puente de conferencia del conmutador.</span><span class="sxs-lookup"><span data-stu-id="a8646-106">The call handle is for a conference call, that is, it is the application's connection to the conference bridge in the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8646-107"><span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**LINECALLORIGIN \_ externo**</span><span class="sxs-lookup"><span data-stu-id="a8646-107"><span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**LINECALLORIGIN\_EXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8646-108">La llamada se originó como una llamada entrante en una línea externa.</span><span class="sxs-lookup"><span data-stu-id="a8646-108">The call originated as an incoming call on an external line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8646-109"><span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**LINECALLORIGIN \_ entrante**</span><span class="sxs-lookup"><span data-stu-id="a8646-109"><span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**LINECALLORIGIN\_INBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8646-110">La llamada se originó como una llamada entrante, pero el proveedor de servicios no puede determinar si proviene de otra estación en el mismo conmutador o de una línea externa.</span><span class="sxs-lookup"><span data-stu-id="a8646-110">The call originated as an incoming call, but the service provider is unable to determine whether it came from another station on the same switch or from an external line.</span></span> <span data-ttu-id="a8646-111">Los proveedores de servicios pueden usar esta constante solo cuando se ha negociado la versión 1,4 o posterior de TAPI.</span><span class="sxs-lookup"><span data-stu-id="a8646-111">Service providers can use this constant only when TAPI version 1.4 or later has been negotiated.</span></span> <span data-ttu-id="a8646-112">De lo contrario, el proveedor de servicios puede sustituir LINECALLORIGIN no \_ disponible.</span><span class="sxs-lookup"><span data-stu-id="a8646-112">Otherwise, the service provider can substitute LINECALLORIGIN\_UNAVAIL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8646-113"><span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**LINECALLORIGIN \_ interno**</span><span class="sxs-lookup"><span data-stu-id="a8646-113"><span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**LINECALLORIGIN\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8646-114">La llamada se originó como una llamada entrante en una estación interna al mismo entorno de conmutación.</span><span class="sxs-lookup"><span data-stu-id="a8646-114">The call originated as an incoming call at a station internal to the same switching environment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8646-115"><span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**LINECALLORIGIN de \_ salida**</span><span class="sxs-lookup"><span data-stu-id="a8646-115"><span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**LINECALLORIGIN\_OUTBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8646-116">La llamada se originó desde esta estación como una llamada saliente.</span><span class="sxs-lookup"><span data-stu-id="a8646-116">The call originated from this station as an outgoing call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8646-117"><span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**LINECALLORIGIN no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="a8646-117"><span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**LINECALLORIGIN\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8646-118">El origen de la llamada no está disponible y nunca se conocerá para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="a8646-118">The call origin is not available and will never become known for this call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8646-119"><span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**LINECALLORIGIN \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="a8646-119"><span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**LINECALLORIGIN\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8646-120">Actualmente, el origen de la llamada es desconocido, pero puede ser conocido más adelante.</span><span class="sxs-lookup"><span data-stu-id="a8646-120">The call origin is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8646-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8646-121">Remarks</span></span>

<span data-ttu-id="a8646-122">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="a8646-122">No extensibility.</span></span> <span data-ttu-id="a8646-123">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="a8646-123">All 32 bits are reserved.</span></span>

<span data-ttu-id="a8646-124">El origen de una llamada se almacena en el miembro **dwOrigin** de la estructura [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) de la llamada.</span><span class="sxs-lookup"><span data-stu-id="a8646-124">The origin of a call is stored in the **dwOrigin** member of the call's [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8646-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8646-125">Requirements</span></span>



| <span data-ttu-id="a8646-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8646-126">Requirement</span></span> | <span data-ttu-id="a8646-127">Value</span><span class="sxs-lookup"><span data-stu-id="a8646-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a8646-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="a8646-128">TAPI version</span></span><br/> | <span data-ttu-id="a8646-129">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a8646-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="a8646-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8646-130">Header</span></span><br/>       | <dl> <span data-ttu-id="a8646-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8646-131"><dt>Tapi.h</dt></span></span> </dl> |



 

 




