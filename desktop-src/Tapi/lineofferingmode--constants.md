---
description: Las \_ constantes de marca de bits LINEOFFERINGMODE (versiones de TAPI 1,4 y posteriores) describen los distintos subestados de una llamada de oferta.
ms.assetid: a6c6d30f-fdc4-4ba5-b1a2-3c709445aedc
title: Constantes de LINEOFFERINGMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b9e04720b4ea79f5b169e4a279a3af2e0cdda39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690754"
---
# <a name="lineofferingmode_-constants"></a><span data-ttu-id="6a21b-103">Constantes de LINEOFFERINGMODE \_</span><span class="sxs-lookup"><span data-stu-id="6a21b-103">LINEOFFERINGMODE\_ Constants</span></span>

<span data-ttu-id="6a21b-104">Las constantes de marca de bits **LINEOFFERINGMODE \_** (versiones de TAPI 1,4 y posteriores) describen los distintos subestados de una llamada de oferta.</span><span class="sxs-lookup"><span data-stu-id="6a21b-104">The **LINEOFFERINGMODE\_** bit-flag constants (TAPI versions 1.4 and later) describe different substates of an offering call.</span></span> <span data-ttu-id="6a21b-105">Un modo está disponible como estado de la llamada a la aplicación después del estado de la llamada trdansitions a la oferta y dentro del mensaje de la [**línea \_ CALLSTATE**](line-callstate.md) que indica que la llamada está en la \_ oferta LINECALLSTATE.</span><span class="sxs-lookup"><span data-stu-id="6a21b-105">A mode is available as call status to the application after the call state trdansitions to offering, and within the [**LINE\_CALLSTATE**](line-callstate.md) message indicating the call is in LINECALLSTATE\_OFFERING.</span></span> <span data-ttu-id="6a21b-106">Estos valores se usan cuando la llamada se realiza en una dirección compartida (puente) con otras estaciones (consulte [**LINEADDRESSSHARING \_ constantes**](lineaddresssharing--constants.md)), principalmente sistemas de claves electrónicas.</span><span class="sxs-lookup"><span data-stu-id="6a21b-106">These values are used when the call is on an address that is shared (bridged) with other stations (see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span>

<dl> <dt>

<span data-ttu-id="6a21b-107"><span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE \_ activo**</span><span class="sxs-lookup"><span data-stu-id="6a21b-107"><span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a21b-108">Indica que la llamada se notifica en la estación actual (irá acompañada de mensajes LINEDEVSTATE \_ Ringing) y, si alguna aplicación está configurada para responder automáticamente, puede hacerlo.</span><span class="sxs-lookup"><span data-stu-id="6a21b-108">Indicates that the call is alerting at the current station (will be accompanied by LINEDEVSTATE\_RINGING messages), and if any application is set up to automatically answer, it can do so.</span></span> <span data-ttu-id="6a21b-109">Si el modo de estado de la llamada es cero, la aplicación debe suponer que el valor está activo (que sería la situación en una dirección no puente).</span><span class="sxs-lookup"><span data-stu-id="6a21b-109">If the call state mode is ZERO, the application should assume that the value is active (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="6a21b-110">(Versiones de TAPI 1,4 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="6a21b-110">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a21b-111"><span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE \_ INactivo**</span><span class="sxs-lookup"><span data-stu-id="6a21b-111"><span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a21b-112">Indica que la llamada se está ofreciendo en más de una estación, pero la estación actual no es de alerta (por ejemplo, puede ser una estación de operador en la que el estado de la oferta es consultivo, como parpadear una luz). el software del conjunto de estaciones para la respuesta automática no debe responder a la llamada, ya que debe ser prerrogativa en la estación principal (de alertas), pero [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) se puede usar para conectar la llamada.</span><span class="sxs-lookup"><span data-stu-id="6a21b-112">Indicates that the call is being offered at more than one station, but the current station is not alerting (for example, it may be an attendant station where the offering status is advisory, such as blinking a light); software at the station set for automatic answering should preferably not answer the call, because this should be the prerogative at the primary (alerting) station, but [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) may be used to connect the call.</span></span> <span data-ttu-id="6a21b-113">(Versiones de TAPI 1,4 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="6a21b-113">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a21b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a21b-114">Remarks</span></span>

<span data-ttu-id="6a21b-115">No extensible.</span><span class="sxs-lookup"><span data-stu-id="6a21b-115">Not extensible.</span></span> <span data-ttu-id="6a21b-116">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="6a21b-116">All 32 bits are reserved.</span></span>

<span data-ttu-id="6a21b-117">Por compatibilidad con versiones anteriores, es responsabilidad del proveedor de servicios examinar la versión de la API negociada en la línea y no utilizar estos \_ valores de LINEOFFERINGMODE si no se admiten en la versión negociada.</span><span class="sxs-lookup"><span data-stu-id="6a21b-117">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use these LINEOFFERINGMODE\_ values if they are not supported on the negotiated version.</span></span> <span data-ttu-id="6a21b-118">Las aplicaciones que no son Cognizant de LINEOFFERINGMODE \_ probablemente suponen que una llamada que está en la \_ oferta LINECALLSTATE está \_ activa en LINEOFFERINGMODE.</span><span class="sxs-lookup"><span data-stu-id="6a21b-118">Applications that are not cognizant of LINEOFFERINGMODE\_ will most likely assume that a call that is in LINECALLSTATE\_OFFERING is in LINEOFFERINGMODE\_ACTIVE.</span></span>

<span data-ttu-id="6a21b-119">Los \_ valores INactivos de LINEOFFERINGMODE activo y LINEOFFERINGMODE \_ se usan cuando la llamada está en una dirección que se comparte con otras estaciones (puente; [vea \_ constantes de LINEADDRESSSHARING](lineaddresssharing--constants.md)), principalmente sistemas de claves electrónicas.</span><span class="sxs-lookup"><span data-stu-id="6a21b-119">The LINEOFFERINGMODE\_ACTIVE and LINEOFFERINGMODE\_INACTIVE values are used when the call is on an address that is shared with other stations (bridged; see [LINEADDRESSSHARING\_ Constants](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="6a21b-120">Si el modo de estado de la llamada de la oferta es "activo", significa que la llamada se notifica en la estación actual (irá acompañada de \_ los mensajes LINEDEVSTATE Ringing) y, si alguna aplicación está configurada para responder automáticamente, puede hacerlo.</span><span class="sxs-lookup"><span data-stu-id="6a21b-120">If the offering call state mode is "active," it means that the call is alerting at the current station (will be accompanied by LINEDEVSTATE\_RINGING messages), and if any application is set up to automatically answer, it can do so.</span></span> <span data-ttu-id="6a21b-121">Si el modo de estado de la llamada es "inactivo", la llamada se ofrece en más de una estación, pero la estación actual no se alerta (por ejemplo, puede ser una estación de operador en la que el estado de la oferta es aviso, como parpadear una luz). el software del conjunto de estaciones para la respuesta automática no debe responder a la llamada, ya que debe ser prerrogativa en la estación principal (de alertas), pero [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) se puede usar para conectar la llamada.</span><span class="sxs-lookup"><span data-stu-id="6a21b-121">If the call state mode is "inactive," the call is being offered at more than one station, but the current station is not alerting (for example, it may be an attendant station where the offering status is advisory, such as blinking a light); software at the station set for automatic answering should preferably not answer the call, because this should be the prerogative at the primary (alerting) station, but [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) can be used to connect the call.</span></span> <span data-ttu-id="6a21b-122">Si el modo de estado de la llamada es cero, la aplicación debe suponer que el valor está activo (que sería la situación en una dirección no puente).</span><span class="sxs-lookup"><span data-stu-id="6a21b-122">If the call state mode is ZERO, the application should assume that the value is active (which would be the situation on a non-bridged address).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a21b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a21b-123">Requirements</span></span>



| <span data-ttu-id="6a21b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a21b-124">Requirement</span></span> | <span data-ttu-id="6a21b-125">Value</span><span class="sxs-lookup"><span data-stu-id="6a21b-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6a21b-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="6a21b-126">TAPI version</span></span><br/> | <span data-ttu-id="6a21b-127">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="6a21b-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6a21b-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a21b-128">Header</span></span><br/>       | <dl> <span data-ttu-id="6a21b-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a21b-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




