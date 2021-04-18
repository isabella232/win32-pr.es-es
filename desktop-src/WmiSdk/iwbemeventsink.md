---
description: Inicia la comunicación con un proveedor de eventos mediante un conjunto restringido de consultas.
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.tgt_platform: multiple
title: Interfaz IWbemEventSink (Wbemprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemEventSink
api_type:
- COM
api_location:
- Wbemsvc.dll
ms.openlocfilehash: 22a3a15920d26f482cedfa3a596fd439ea70c2f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706843"
---
# <a name="iwbemeventsink-interface"></a><span data-ttu-id="31411-103">Interfaz IWbemEventSink</span><span class="sxs-lookup"><span data-stu-id="31411-103">IWbemEventSink interface</span></span>

<span data-ttu-id="31411-104">La interfaz **IWbemEventSink** inicia la comunicación con un proveedor de eventos mediante un conjunto restringido de consultas.</span><span class="sxs-lookup"><span data-stu-id="31411-104">The **IWbemEventSink** interface initiates communication with an event provider using a restricted set of queries.</span></span> <span data-ttu-id="31411-105">Esta interfaz extiende [**IWbemObjectSink**](iwbemobjectsink.md), lo que proporciona nuevos métodos que se ocupan de la seguridad y el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="31411-105">This interface extends [**IWbemObjectSink**](iwbemobjectsink.md), providing new methods dealing with security and performance.</span></span> <span data-ttu-id="31411-106">Para obtener más información sobre el uso de esta interfaz, vea [escribir un proveedor de eventos](writing-an-event-provider.md) y [proteger eventos de WMI](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="31411-106">For more information about using this interface, see [Writing an Event Provider](writing-an-event-provider.md) and [Securing WMI Events](securing-wmi-events.md).</span></span>

## <a name="members"></a><span data-ttu-id="31411-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="31411-107">Members</span></span>

<span data-ttu-id="31411-108">La interfaz **IWbemEventSink** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="31411-108">The **IWbemEventSink** interface has these types of members:</span></span>

-   [<span data-ttu-id="31411-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="31411-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="31411-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="31411-110">Methods</span></span>

<span data-ttu-id="31411-111">La interfaz **IWbemEventSink** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="31411-111">The **IWbemEventSink** interface has these methods.</span></span>



| <span data-ttu-id="31411-112">Método</span><span class="sxs-lookup"><span data-stu-id="31411-112">Method</span></span>                                                                | <span data-ttu-id="31411-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="31411-113">Description</span></span>                                                           |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="31411-114">**GetRestrictedSink**</span><span class="sxs-lookup"><span data-stu-id="31411-114">**GetRestrictedSink**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)         | <span data-ttu-id="31411-115">Lo llama el consumidor para configurar consultas de eventos restringidos.</span><span class="sxs-lookup"><span data-stu-id="31411-115">Called by the consumer to set up restricted event queries.</span></span><br/> |
| [<span data-ttu-id="31411-116">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="31411-116">**IsActive**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-isactive)                           | <span data-ttu-id="31411-117">Comprueba el estado del receptor de eventos.</span><span class="sxs-lookup"><span data-stu-id="31411-117">Checks status of event sink.</span></span><br/>                               |
| [<span data-ttu-id="31411-118">**SetBatchingParameters**</span><span class="sxs-lookup"><span data-stu-id="31411-118">**SetBatchingParameters**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setbatchingparameters) | <span data-ttu-id="31411-119">Lo llama el consumidor para establecer los parámetros de procesamiento por lotes.</span><span class="sxs-lookup"><span data-stu-id="31411-119">Called by the consumer to set batching parameters.</span></span><br/>         |
| [<span data-ttu-id="31411-120">**SetSinkSecurity**</span><span class="sxs-lookup"><span data-stu-id="31411-120">**SetSinkSecurity**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)             | <span data-ttu-id="31411-121">Se utiliza para actualizar el descriptor de seguridad de un receptor de eventos.</span><span class="sxs-lookup"><span data-stu-id="31411-121">Used to update the security descriptor on an event sink.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="31411-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31411-122">Remarks</span></span>

<span data-ttu-id="31411-123">Al implementar un receptor de suscripciones de eventos ([**IWbemObjectSink**](iwbemobjectsink.md) o **IWbemEventSink**), no llame a WMI desde los métodos del objeto receptor.</span><span class="sxs-lookup"><span data-stu-id="31411-123">When implementing an event subscription sink ([**IWbemObjectSink**](iwbemobjectsink.md) or **IWbemEventSink**), do not call into WMI from within the methods on the sink object.</span></span> <span data-ttu-id="31411-124">Por ejemplo, la llamada a [**IWbemServices:: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) para cancelar el receptor desde una implementación de [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) puede interferir con el estado de WMI.</span><span class="sxs-lookup"><span data-stu-id="31411-124">For example, calling [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) to cancel the sink from within an implementation of [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) can interfere with the WMI state.</span></span> <span data-ttu-id="31411-125">Para cancelar una suscripción de eventos, establezca una marca y llame a **IWbemServices:: CancelAsyncCall** desde otro subproceso u objeto.</span><span class="sxs-lookup"><span data-stu-id="31411-125">To cancel an event subscription, set a flag and call **IWbemServices::CancelAsyncCall** from another thread or object.</span></span> <span data-ttu-id="31411-126">En el caso de las implementaciones que no están relacionadas con un receptor de eventos, como las recuperaciones de objetos, enumeraciones y consultas, puede volver a llamar a WMI.</span><span class="sxs-lookup"><span data-stu-id="31411-126">For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.</span></span>

<span data-ttu-id="31411-127">Las implementaciones de receptores deben procesar la notificación de eventos en un plazo de 100 MS, ya que el subproceso de WMI que entrega la notificación de eventos no puede realizar otras tareas hasta que el objeto receptor haya completado el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="31411-127">Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing.</span></span> <span data-ttu-id="31411-128">Si la notificación requiere una gran cantidad de procesamiento, el receptor puede utilizar una cola interna para que otro subproceso controle el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="31411-128">If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="31411-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31411-129">Requirements</span></span>



| <span data-ttu-id="31411-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="31411-130">Requirement</span></span> | <span data-ttu-id="31411-131">Value</span><span class="sxs-lookup"><span data-stu-id="31411-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31411-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31411-132">Minimum supported client</span></span><br/> | <span data-ttu-id="31411-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31411-133">Windows Vista</span></span><br/>                                                                                  |
| <span data-ttu-id="31411-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31411-134">Minimum supported server</span></span><br/> | <span data-ttu-id="31411-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31411-135">Windows Server 2008</span></span><br/>                                                                            |
| <span data-ttu-id="31411-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31411-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="31411-137"><dt>Wbemprov. h (incluye Wbemidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31411-137"><dt>Wbemprov.h (include Wbemidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="31411-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31411-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="31411-139"><dt>Wbemuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31411-139"><dt>Wbemuuid.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="31411-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="31411-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31411-141"><dt>Wbemsvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31411-141"><dt>Wbemsvc.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="31411-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="31411-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31411-143">API COM para WMI</span><span class="sxs-lookup"><span data-stu-id="31411-143">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> </dl>

 

 




