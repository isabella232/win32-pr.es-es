---
description: Las \_ constantes de marcador de bits LINECONNECTEDMODE describen diferentes subestados de una llamada conectada.
ms.assetid: d75a5989-3f4e-4e5d-90b1-4e450def017e
title: Constantes de LINECONNECTEDMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5191d3a575ef353c54c91c0e53b3228621b703cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690502"
---
# <a name="lineconnectedmode_-constants"></a><span data-ttu-id="26c6b-103">Constantes de LINECONNECTEDMODE \_</span><span class="sxs-lookup"><span data-stu-id="26c6b-103">LINECONNECTEDMODE\_ Constants</span></span>

<span data-ttu-id="26c6b-104">Las constantes de marcador de bits **LINECONNECTEDMODE \_** describen diferentes subestados de una llamada conectada.</span><span class="sxs-lookup"><span data-stu-id="26c6b-104">The **LINECONNECTEDMODE\_** bit-flag constants describe different substates of a connected call.</span></span> <span data-ttu-id="26c6b-105">Un modo está disponible como estado de la llamada a la aplicación después de que el estado de la llamada cambie a conectado y en el mensaje de línea \_ CALLSTATE que indica que la llamada está en LINECALLSTATE \_ conectado.</span><span class="sxs-lookup"><span data-stu-id="26c6b-105">A mode is available as call status to the application after the call state transitions to connected, and within the LINE\_CALLSTATE message indicating the call is in LINECALLSTATE\_CONNECTED.</span></span> <span data-ttu-id="26c6b-106">Estos valores se usan cuando la llamada se realiza en una dirección compartida (con puentes) con otras estaciones (para obtener más información, consulte [**\_ constantes de LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalmente sistemas de claves electrónicas.</span><span class="sxs-lookup"><span data-stu-id="26c6b-106">These values are used when the call is on an address that is shared (bridged) with other stations (for more information, see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="26c6b-107">Las **\_ constantes LINECONNECTEDMODE** tienen los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="26c6b-107">The **LINECONNECTEDMODE\_constants** have the following values:</span></span>

<dl> <dt>

<span data-ttu-id="26c6b-108"><span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**LINECONNECTEDMODE \_ activo**</span><span class="sxs-lookup"><span data-stu-id="26c6b-108"><span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**LINECONNECTEDMODE\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="26c6b-109">Indica que la llamada está conectada a la estación actual (la estación actual es un participante en la llamada).</span><span class="sxs-lookup"><span data-stu-id="26c6b-109">Indicates that the call is connected at the current station (the current station is a participant in the call).</span></span> <span data-ttu-id="26c6b-110">Si el modo de estado de la llamada es 0 (cero), la aplicación debe suponer que el valor es "Active" (que sería la situación en una dirección no puente).</span><span class="sxs-lookup"><span data-stu-id="26c6b-110">If the call state mode is 0 (zero), the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="26c6b-111">El modo puede cambiar entre activo e inactivo durante una llamada si el usuario se une y deja la llamada a través de la acción manual.</span><span class="sxs-lookup"><span data-stu-id="26c6b-111">The mode can switch between ACTIVE and INACTIVE during a call if the user joins and leaves the call through manual action.</span></span> <span data-ttu-id="26c6b-112">En una situación de puente, es posible que una operación de [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) o [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) no elimine realmente la llamada o la ponga en espera, ya que el estado de otras estaciones de la llamada puede regir (por ejemplo, si se intenta "mantener" una llamada cuando no se pueden participar otras estaciones); en su lugar, la llamada puede cambiar al modo inactivo si permanece conectado en otras estaciones.</span><span class="sxs-lookup"><span data-stu-id="26c6b-112">In such a bridged situation, a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) or [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) operation may possibly not actually drop the call or place it on hold, because the status of other stations on the call may govern (for example, attempting to "hold" a call when other stations are participating is not possible); instead, the call may be changed to the INACTIVE mode if it remains CONNECTED at other stations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="26c6b-113"><span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**LINECONNECTEDMODE \_ ACTIVEHELD**</span><span class="sxs-lookup"><span data-stu-id="26c6b-113"><span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**LINECONNECTEDMODE\_ACTIVEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="26c6b-114">Indica que la estación es un participante activo en la llamada, pero que la parte remota ha realizado la llamada en espera (la otra parte considera que la llamada está en estado de suspensión).</span><span class="sxs-lookup"><span data-stu-id="26c6b-114">Indicates that the station is an active participant in the call, but that the remote party has placed the call on hold (the other party considers the call to be in the onhold state).</span></span> <span data-ttu-id="26c6b-115">Normalmente, esta información solo está disponible cuando ambos extremos de la llamada se encuentran en el mismo dominio de cambio.</span><span class="sxs-lookup"><span data-stu-id="26c6b-115">Normally, such information is available only when both endpoints of the call fall within the same switching domain.</span></span> <span data-ttu-id="26c6b-116">Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="26c6b-116">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="26c6b-117">(Versiones de TAPI 2,0 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="26c6b-117">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="26c6b-118"><span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**LINECONNECTEDMODE \_ confirmado**</span><span class="sxs-lookup"><span data-stu-id="26c6b-118"><span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**LINECONNECTEDMODE\_CONFIRMED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="26c6b-119">Indica que el proveedor de servicios ha recibido una notificación afirmativa de que la llamada ha entrado en el estado conectado (por ejemplo, a través de la supervisión de respuestas o mecanismos similares).</span><span class="sxs-lookup"><span data-stu-id="26c6b-119">Indicates that the service provider received affirmative notification that the call has entered the connected state (for example, through answer supervision or similar mechanisms).</span></span> <span data-ttu-id="26c6b-120">Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="26c6b-120">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="26c6b-121">(Versiones de TAPI 2,0 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="26c6b-121">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="26c6b-122"><span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**LINECONNECTEDMODE \_ INactivo**</span><span class="sxs-lookup"><span data-stu-id="26c6b-122"><span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**LINECONNECTEDMODE\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="26c6b-123">Indica que la llamada está activa en una o varias estaciones, pero la estación actual no es un participante de la llamada.</span><span class="sxs-lookup"><span data-stu-id="26c6b-123">Indicates that the call is active at one or more other stations, but the current station is not a participant in the call.</span></span> <span data-ttu-id="26c6b-124">Si el modo de estado de la llamada es cero, la aplicación debe suponer que el valor es "Active" (que sería la situación en una dirección no puente).</span><span class="sxs-lookup"><span data-stu-id="26c6b-124">If the call state mode is ZERO, the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="26c6b-125">Una llamada en el estado inactivo se puede combinar con [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="26c6b-125">A call in the INACTIVE state can be joined using [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span> <span data-ttu-id="26c6b-126">Muchas operaciones que son válidas en llamadas en el estado CONNECTed pueden ser imposibles en el modo inactivo, como la supervisión de tonos y dígitos, ya que la estación no participa realmente en la llamada; Normalmente, la supervisión se suspende (aunque no se cancela) mientras la llamada está en modo inactivo.</span><span class="sxs-lookup"><span data-stu-id="26c6b-126">Many operations that are valid in calls in the CONNECTED state can be impossible in the INACTIVE mode, such as monitoring for tones and digits, because the station is not actually participating in the call; monitoring is usually suspended (although not canceled) while the call is in the INACTIVE mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="26c6b-127"><span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**LINECONNECTEDMODE \_ INACTIVEHELD**</span><span class="sxs-lookup"><span data-stu-id="26c6b-127"><span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**LINECONNECTEDMODE\_INACTIVEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="26c6b-128">Indica que la estación no es un participante activo en la llamada y que la parte remota ha realizado la llamada en espera.</span><span class="sxs-lookup"><span data-stu-id="26c6b-128">Indicates that the station is not an active participant in the call, and that the remote party has placed the call on hold.</span></span> <span data-ttu-id="26c6b-129">Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="26c6b-129">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="26c6b-130">(Versiones de TAPI 2,0 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="26c6b-130">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26c6b-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26c6b-131">Remarks</span></span>

<span data-ttu-id="26c6b-132">No extensible.</span><span class="sxs-lookup"><span data-stu-id="26c6b-132">Not extensible.</span></span> <span data-ttu-id="26c6b-133">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="26c6b-133">All 32 bits are reserved.</span></span>

<span data-ttu-id="26c6b-134">Por compatibilidad con versiones anteriores, es responsabilidad del proveedor de servicios examinar la versión de la API negociada en la línea y no utilizar los valores de LINECONNECTEDMODE \_ que no se admiten en la versión negociada.</span><span class="sxs-lookup"><span data-stu-id="26c6b-134">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use those LINECONNECTEDMODE\_ values that are not supported on the negotiated version.</span></span> <span data-ttu-id="26c6b-135">Las aplicaciones que no son Cognizant de LINECONNECTEDMODE \_ probablemente suponen que una llamada que está en LINECALLSTATE \_ conectada está activa en LINECONNECTEDMODE \_ .</span><span class="sxs-lookup"><span data-stu-id="26c6b-135">Applications that are not cognizant of LINECONNECTEDMODE\_ will most likely assume that a call that is in LINECALLSTATE\_CONNECTED is in LINECONNECTEDMODE\_ACTIVE.</span></span>

<span data-ttu-id="26c6b-136">Los \_ valores INactivos de LINECONNECTEDMODE activo y LINECONNECTEDMODE \_ se usan cuando la llamada está en una dirección que se comparte con otras estaciones (puente; [**vea \_ constantes de LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalmente sistemas de claves electrónicas.</span><span class="sxs-lookup"><span data-stu-id="26c6b-136">The LINECONNECTEDMODE\_ACTIVE and LINECONNECTEDMODE\_INACTIVE values are used when the call is on an address that is shared with other stations (bridged; see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="26c6b-137">Si el modo de estado de llamada conectado es "activo", significa que la llamada está conectada a la estación actual (la estación actual es un participante en la llamada).</span><span class="sxs-lookup"><span data-stu-id="26c6b-137">If the connected call state mode is "active," it means that the call is connected at the current station (the current station is a participant in the call).</span></span> <span data-ttu-id="26c6b-138">Si el modo de estado de la llamada es "inactivo", la llamada está activa en una o varias estaciones, pero la estación actual no es un participante de la llamada.</span><span class="sxs-lookup"><span data-stu-id="26c6b-138">If the call state mode is "inactive," the call is active at one or more other stations, but the current station is not a participant in the call.</span></span> <span data-ttu-id="26c6b-139">Si el modo de estado de la llamada es cero, la aplicación debe suponer que el valor es "Active" (que sería la situación en una dirección no puente).</span><span class="sxs-lookup"><span data-stu-id="26c6b-139">If the call state mode is ZERO, the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="26c6b-140">El modo puede cambiar entre activo e inactivo durante una llamada si el usuario se une y deja la llamada a través de la acción manual.</span><span class="sxs-lookup"><span data-stu-id="26c6b-140">The mode can switch between ACTIVE and INACTIVE during a call if the user joins and leaves the call through manual action.</span></span>

<span data-ttu-id="26c6b-141">En una situación de puente, es posible que una operación de [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) o [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) no elimine realmente la llamada o la ponga en espera, ya que el estado de otras estaciones de la llamada puede regir (por ejemplo, si se intenta "mantener" una llamada cuando no se pueden participar otras estaciones). en su lugar, la llamada solo se puede cambiar al modo inactivo si permanece conectado en otras estaciones.</span><span class="sxs-lookup"><span data-stu-id="26c6b-141">In such a bridged situation, a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) or [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) operation may possibly not actually drop the call or place it on hold, because the status of other stations on the call may govern (for example, attempting to "hold" a call when other stations are participating will not be possible); instead, the call can simply be changed to the INACTIVE mode if it remains connected at other stations.</span></span> <span data-ttu-id="26c6b-142">Una llamada en el estado inactivo puede combinarse mediante [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="26c6b-142">A call in the INACTIVE state can be joined using the [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span>

<span data-ttu-id="26c6b-143">Muchas operaciones que son válidas en llamadas en el estado Connected pueden ser imposibles en el modo inactivo, como la supervisión de tonos y dígitos, ya que la estación no participa realmente en la llamada; Normalmente, la supervisión se suspende (aunque no se cancela) mientras la llamada está en modo inactivo.</span><span class="sxs-lookup"><span data-stu-id="26c6b-143">Many operations that are valid in calls in the connected state can be impossible in the INACTIVE mode, such as monitoring for tones and digits, because the station is not actually participating in the call; monitoring is usually suspended (although not canceled) while the call is in the INACTIVE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="26c6b-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26c6b-144">Requirements</span></span>



| <span data-ttu-id="26c6b-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="26c6b-145">Requirement</span></span> | <span data-ttu-id="26c6b-146">Value</span><span class="sxs-lookup"><span data-stu-id="26c6b-146">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="26c6b-147">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="26c6b-147">TAPI version</span></span><br/> | <span data-ttu-id="26c6b-148">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="26c6b-148">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="26c6b-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26c6b-149">Header</span></span><br/>       | <dl> <span data-ttu-id="26c6b-150"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="26c6b-150"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26c6b-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="26c6b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26c6b-152">**lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="26c6b-152">**lineAnswer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineanswer)
</dt> <dt>

[<span data-ttu-id="26c6b-153">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="26c6b-153">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="26c6b-154">**lineHold**</span><span class="sxs-lookup"><span data-stu-id="26c6b-154">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> </dl>

 

 




