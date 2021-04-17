---
description: El mensaje de línea de \_ CALLINFO TAPI se envía cuando ha cambiado la información de llamada sobre la llamada especificada. La aplicación puede invocar lineGetCallInfo para determinar la información de la llamada actual.
ms.assetid: eb882409-6842-434e-9f93-61cf0c11d1d0
title: Mensaje de LINE_CALLINFO (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6005ab5383816ead440f5a1a7d580bfaccb5c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690401"
---
# <a name="line_callinfo-message"></a><span data-ttu-id="6c0b8-104">Mensaje de línea \_ CALLINFO</span><span class="sxs-lookup"><span data-stu-id="6c0b8-104">LINE\_CALLINFO message</span></span>

<span data-ttu-id="6c0b8-105">El mensaje de **línea de \_ CALLINFO** TAPI se envía cuando ha cambiado la información de llamada sobre la llamada especificada.</span><span class="sxs-lookup"><span data-stu-id="6c0b8-105">The TAPI **LINE\_CALLINFO** message is sent when the call information about the specified call has changed.</span></span> <span data-ttu-id="6c0b8-106">La aplicación puede invocar [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) para determinar la información de la llamada actual.</span><span class="sxs-lookup"><span data-stu-id="6c0b8-106">The application can invoke [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) to determine the current call information.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="6c0b8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c0b8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c0b8-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="6c0b8-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="6c0b8-109">Identificador de la llamada.</span><span class="sxs-lookup"><span data-stu-id="6c0b8-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="6c0b8-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="6c0b8-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="6c0b8-111">Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.</span><span class="sxs-lookup"><span data-stu-id="6c0b8-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="6c0b8-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="6c0b8-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="6c0b8-113">Elemento de información de llamada que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="6c0b8-113">The call information item that has changed.</span></span> <span data-ttu-id="6c0b8-114">Puede ser una o varias de las [**\_ constantes LINECALLINFOSTATE**](linecallinfostate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="6c0b8-114">Can be one or more of the [**LINECALLINFOSTATE\_ constants**](linecallinfostate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c0b8-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="6c0b8-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="6c0b8-116">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="6c0b8-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="6c0b8-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="6c0b8-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="6c0b8-118">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="6c0b8-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c0b8-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c0b8-119">Return value</span></span>

<span data-ttu-id="6c0b8-120">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6c0b8-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c0b8-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c0b8-121">Remarks</span></span>

<span data-ttu-id="6c0b8-122">Se envía un mensaje **line \_ CALLINFO** con una indicación *NumOwnersIncr*, *NumOwnersDecr* y/o *NumMonitorsChanged* a las aplicaciones que ya tienen un identificador para la llamada.</span><span class="sxs-lookup"><span data-stu-id="6c0b8-122">A **LINE\_CALLINFO** message with a *NumOwnersIncr*, *NumOwnersDecr*, and/or *NumMonitorsChanged* indication is sent to applications that already have a handle for the call.</span></span> <span data-ttu-id="6c0b8-123">Esto puede ser el resultado de que otra aplicación cambie la propiedad o supervise una llamada con [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)y [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls).</span><span class="sxs-lookup"><span data-stu-id="6c0b8-123">This can be the result of another application changing ownership or monitorship to a call with [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls), and [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls).</span></span>

<span data-ttu-id="6c0b8-124">Estos mensajes de **línea \_ CALLINFO** no se envían cuando se proporciona una notificación de una nueva llamada en un mensaje de [**línea \_ CALLSTATE**](line-callstate.md) , ya que la información de la llamada ya refleja el número correcto de propietarios y monitores en el momento en que \_ se envían los mensajes de CALLSTATE de línea.</span><span class="sxs-lookup"><span data-stu-id="6c0b8-124">These **LINE\_CALLINFO** messages are not sent when a notification of a new call is provided in a [**LINE\_CALLSTATE**](line-callstate.md) message, because the call information already reflects the correct number of owners and monitors at the time the LINE\_CALLSTATE messages are sent.</span></span> <span data-ttu-id="6c0b8-125">**Línea \_ de** Los mensajes CALLINFO también se suprimen en el caso de que TAPI ofrezca una llamada para que supervise a través del \_ mecanismo desconocido de LINECALLSTATE.</span><span class="sxs-lookup"><span data-stu-id="6c0b8-125">**LINE\_CALLINFO** messages are also suppressed in the case where a call is offered by TAPI to monitors through the LINECALLSTATE\_UNKNOWN mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="6c0b8-126">La aplicación que provoca un cambio en el número de propietarios o monitores (por ejemplo, mediante la invocación de [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) o [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)) no recibe un mensaje que indica que se ha realizado el cambio.</span><span class="sxs-lookup"><span data-stu-id="6c0b8-126">The application that causes a change in the number of owners or monitors (for example, by invoking [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) or [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)) does not itself receive a message indicating that the change has been done.</span></span>

 

<span data-ttu-id="6c0b8-127">No se envía ningún mensaje de **línea \_ CALLINFO** para una llamada después de que la llamada haya entrado en el estado de *inactividad* .</span><span class="sxs-lookup"><span data-stu-id="6c0b8-127">No **LINE\_CALLINFO** messages are sent for a call after the call has entered the *idle* state.</span></span> <span data-ttu-id="6c0b8-128">En concreto, los cambios en el número de propietarios y monitores no se informan como aplicaciones que desasignan sus identificadores para la llamada inactiva.</span><span class="sxs-lookup"><span data-stu-id="6c0b8-128">Specifically, changes in the number of owners and monitors are not reported as applications deallocate their handles for the idle call.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c0b8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c0b8-129">Requirements</span></span>



| <span data-ttu-id="6c0b8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c0b8-130">Requirement</span></span> | <span data-ttu-id="6c0b8-131">Value</span><span class="sxs-lookup"><span data-stu-id="6c0b8-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6c0b8-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="6c0b8-132">TAPI version</span></span><br/> | <span data-ttu-id="6c0b8-133">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="6c0b8-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6c0b8-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c0b8-134">Header</span></span><br/>       | <dl> <span data-ttu-id="6c0b8-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c0b8-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c0b8-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c0b8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c0b8-137">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="6c0b8-137">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="6c0b8-138">**lineDeallocateCall**</span><span class="sxs-lookup"><span data-stu-id="6c0b8-138">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[<span data-ttu-id="6c0b8-139">**lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="6c0b8-139">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[<span data-ttu-id="6c0b8-140">**lineGetConfRelatedCalls**</span><span class="sxs-lookup"><span data-stu-id="6c0b8-140">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[<span data-ttu-id="6c0b8-141">**lineGetNewCalls**</span><span class="sxs-lookup"><span data-stu-id="6c0b8-141">**lineGetNewCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)
</dt> <dt>

[<span data-ttu-id="6c0b8-142">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="6c0b8-142">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="6c0b8-143">**lineSetCallPrivilege**</span><span class="sxs-lookup"><span data-stu-id="6c0b8-143">**lineSetCallPrivilege**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)
</dt> <dt>

[<span data-ttu-id="6c0b8-144">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="6c0b8-144">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




