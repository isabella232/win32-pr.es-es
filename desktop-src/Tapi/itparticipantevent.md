---
description: La interfaz ITParticipantEvent contiene métodos que recuperan la descripción de los eventos de los participantes.
ms.assetid: 1199ec91-ee06-4e6c-8d8f-1585a3da3db0
title: Interfaz ITParticipantEvent (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac6e2b43a528bc041a71962e84b4e1be62152a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680320"
---
# <a name="itparticipantevent-interface"></a><span data-ttu-id="11def-103">Interfaz ITParticipantEvent</span><span class="sxs-lookup"><span data-stu-id="11def-103">ITParticipantEvent interface</span></span>

<span data-ttu-id="11def-104">\[**ITParticipantEvent** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="11def-104">\[**ITParticipantEvent** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="11def-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="11def-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="11def-106">La interfaz **ITParticipantEvent** contiene métodos que recuperan la descripción de los eventos de los participantes.</span><span class="sxs-lookup"><span data-stu-id="11def-106">The **ITParticipantEvent** interface contains methods that retrieve the description of participant events.</span></span> <span data-ttu-id="11def-107">Cuando la implementación de la aplicación del método [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) indica un [**\_ evento TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) igual a **te \_ Private**, el parámetro *pevent* del método es un puntero **IDispatch** para la interfaz **ITParticipantEvent** .</span><span class="sxs-lookup"><span data-stu-id="11def-107">When the application's implementation of the [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) method indicates a [**TAPI\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) equal to **TE\_PRIVATE**, the method's *pEvent* parameter is an **IDispatch** pointer for the **ITParticipantEvent** interface.</span></span> <span data-ttu-id="11def-108">Los métodos de esta interfaz se pueden usar para recuperar información relativa a un cambio de participante que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="11def-108">The methods of this interface can be used to retrieve information concerning a participant change that has occurred.</span></span>

> [!Note]  
> <span data-ttu-id="11def-109">Debe llamar al método [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) y establecer una máscara de filtro de eventos que incluya el evento de usuario **\_ privado** para habilitar la recepción de eventos de participantes.</span><span class="sxs-lookup"><span data-stu-id="11def-109">You must call the [**ITTAPI::put\_EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) method and set an event filter mask that includes the **TE\_PRIVATE** event to enable reception of participant events.</span></span> <span data-ttu-id="11def-110">Si no llama a **ITTAPI::p UT \_ EventFilter**, la aplicación no recibirá ningún evento.</span><span class="sxs-lookup"><span data-stu-id="11def-110">If you do not call **ITTAPI::put\_EventFilter**, your application will not receive any events.</span></span> <span data-ttu-id="11def-111">Para obtener más información, vea información general sobre [eventos](events.md) .</span><span class="sxs-lookup"><span data-stu-id="11def-111">For more information, see the [Events](events.md) overview.</span></span>

 

## <a name="members"></a><span data-ttu-id="11def-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="11def-112">Members</span></span>

<span data-ttu-id="11def-113">La interfaz **ITParticipantEvent** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="11def-113">The **ITParticipantEvent** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="11def-114">**ITParticipantEvent** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="11def-114">**ITParticipantEvent** also has these types of members:</span></span>

-   [<span data-ttu-id="11def-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="11def-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="11def-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="11def-116">Methods</span></span>

<span data-ttu-id="11def-117">La interfaz **ITParticipantEvent** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="11def-117">The **ITParticipantEvent** interface has these methods.</span></span>



| <span data-ttu-id="11def-118">Método</span><span class="sxs-lookup"><span data-stu-id="11def-118">Method</span></span>                                                         | <span data-ttu-id="11def-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="11def-119">Description</span></span>                                                                                                                                     |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11def-120">**obtener \_ evento**</span><span class="sxs-lookup"><span data-stu-id="11def-120">**get\_Event**</span></span>](itparticipantevent-get-event.md)             | <span data-ttu-id="11def-121">Obtiene el descriptor de [**\_ eventos del participante**](participant-event.md) del evento.</span><span class="sxs-lookup"><span data-stu-id="11def-121">Gets the [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the event.</span></span><br/>                                                    |
| [<span data-ttu-id="11def-122">**obtener \_ participante**</span><span class="sxs-lookup"><span data-stu-id="11def-122">**get\_Participant**</span></span>](itparticipantevent-get-participant.md) | <span data-ttu-id="11def-123">Obtiene un puntero a una matriz de interfaces [**ITParticipant**](itparticipant.md) que representan los participantes implicados en el evento.</span><span class="sxs-lookup"><span data-stu-id="11def-123">Gets a pointer to an array of [**ITParticipant**](itparticipant.md) interfaces representing the participants involved in the event.</span></span><br/> |
| [<span data-ttu-id="11def-124">**obtener \_ subflujo**</span><span class="sxs-lookup"><span data-stu-id="11def-124">**get\_SubStream**</span></span>](itparticipantevent-get-substream.md)     | <span data-ttu-id="11def-125">Obtiene un puntero a una matriz de interfaces [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) que representan las subsecuencias implicadas en el evento.</span><span class="sxs-lookup"><span data-stu-id="11def-125">Gets a pointer to an array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interfaces representing the substreams involved in the event.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="11def-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11def-126">Requirements</span></span>



| <span data-ttu-id="11def-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="11def-127">Requirement</span></span> | <span data-ttu-id="11def-128">Value</span><span class="sxs-lookup"><span data-stu-id="11def-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11def-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="11def-129">TAPI version</span></span><br/> | <span data-ttu-id="11def-130">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="11def-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="11def-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11def-131">Header</span></span><br/>       | <dl> <span data-ttu-id="11def-132"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="11def-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="11def-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11def-133">Library</span></span><br/>      | <dl> <span data-ttu-id="11def-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11def-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="11def-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="11def-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="11def-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11def-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="11def-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="11def-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11def-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="11def-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="11def-139">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="11def-139">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[<span data-ttu-id="11def-140">**ITCallInfo**</span><span class="sxs-lookup"><span data-stu-id="11def-140">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[<span data-ttu-id="11def-141">**evento de participante \_**</span><span class="sxs-lookup"><span data-stu-id="11def-141">**PARTICIPANT\_EVENT**</span></span>](participant-event.md)
</dt> <dt>

[<span data-ttu-id="11def-142">**ITTAPIEventNotification:: Event**</span><span class="sxs-lookup"><span data-stu-id="11def-142">**ITTAPIEventNotification::Event**</span></span>](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[<span data-ttu-id="11def-143">**\_evento TAPI**</span><span class="sxs-lookup"><span data-stu-id="11def-143">**TAPI\_EVENT**</span></span>](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[<span data-ttu-id="11def-144">Fragmento de código registrar eventos</span><span class="sxs-lookup"><span data-stu-id="11def-144">Register Events code snippet</span></span>](register-events.md)
</dt> </dl>

 

