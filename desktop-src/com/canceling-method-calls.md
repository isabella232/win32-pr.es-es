---
title: Cancelar llamadas a métodos
description: Con la introducción de aplicaciones distribuidas y basadas en Web, algunas llamadas a métodos pueden tardar un tiempo inaceptablemente largo en devolverse.
ms.assetid: 18228ff1-8c1c-430a-ae5f-0e9a56b0fe3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a78f042e528036135df4865e8a454cd687da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105714469"
---
# <a name="canceling-method-calls"></a><span data-ttu-id="b2024-103">Cancelar llamadas a métodos</span><span class="sxs-lookup"><span data-stu-id="b2024-103">Canceling Method Calls</span></span>

<span data-ttu-id="b2024-104">Con la introducción de aplicaciones distribuidas y basadas en Web, algunas llamadas a métodos pueden tardar un tiempo inaceptablemente largo en devolverse.</span><span class="sxs-lookup"><span data-stu-id="b2024-104">With the introduction of distributed and Web-based applications, some method calls can take an unacceptably long time to return.</span></span> <span data-ttu-id="b2024-105">La latencia de la conexión de red puede ser alta, el equipo del servidor puede estar atendiendo a muchos clientes, o el componente del servidor puede estar pasando una gran cantidad de datos, como un archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="b2024-105">The latency of the network connection may be high, the server machine may be serving many clients, or the server component may be passing a large amount of data, such as a multimedia file.</span></span> <span data-ttu-id="b2024-106">Los usuarios deben poder cancelar una solicitud que esté tardando mucho tiempo y la aplicación debe ser capaz de controlar las solicitudes de cancelación y continuar con su otro trabajo.</span><span class="sxs-lookup"><span data-stu-id="b2024-106">Users should be able to cancel a request that is taking too long, and the application should be able to handle cancellation requests and continue with its other work.</span></span> <span data-ttu-id="b2024-107">En COM, puede usar la interfaz [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) para cancelar una llamada pendiente que se origina a partir de un contenedor uniproceso.</span><span class="sxs-lookup"><span data-stu-id="b2024-107">In COM, you can use the [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) interface to cancel a pending call that originates from a single-threaded apartment.</span></span>

<span data-ttu-id="b2024-108">Cuando se calculan las referencias de una llamada, el proxy crea un objeto CANCEL, que implementa la interfaz [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) .</span><span class="sxs-lookup"><span data-stu-id="b2024-108">When a call is marshaled, the proxy creates a cancel object, which implements the [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) interface.</span></span> <span data-ttu-id="b2024-109">El objeto CANCEL está asociado a la llamada y al subproceso en el que está pendiente la llamada.</span><span class="sxs-lookup"><span data-stu-id="b2024-109">The cancel object is associated with both the call and the thread on which the call is pending.</span></span>

<span data-ttu-id="b2024-110">Para cancelar la llamada pendiente, el cliente pasa una solicitud de cancelación a través del objeto CANCEL, que controla los detalles de la notificación al objeto de servidor de que se ha cancelado la llamada.</span><span class="sxs-lookup"><span data-stu-id="b2024-110">To cancel the pending call, the client passes a cancellation request through the cancel object, which handles the details of notifying the server object that the call has been canceled.</span></span> <span data-ttu-id="b2024-111">Si no se devuelve el método llamado, el objeto de servidor, al detectar la solicitud de cancelación, limpia los recursos de programa que ha asignado y notifica a su cliente, devolviendo un valor **HRESULT** adecuado, que canceló la ejecución de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b2024-111">If the called method has not returned, the server object, on detecting the cancellation request, cleans up any program resources it has allocated and notifies its client, by returning an appropriate **HRESULT** value, that it canceled execution of the call.</span></span> <span data-ttu-id="b2024-112">Si ya se ha devuelto el método llamado, el objeto CANCEL notifica al cliente.</span><span class="sxs-lookup"><span data-stu-id="b2024-112">If the called method has already returned, the cancel object notifies the client.</span></span> <span data-ttu-id="b2024-113">En cualquier caso, el subproceso del cliente se desbloquea y puede continuar el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="b2024-113">In either case, the client thread is unblocked and can continue processing.</span></span>

<span data-ttu-id="b2024-114">La forma en que el objeto de servidor responde a una solicitud de cancelación es a discreción del implementador del servidor, pero el subproceso que realiza la llamada en el cliente siempre estará desbloqueado y omitirá los resultados que el servidor intente pasar a él.</span><span class="sxs-lookup"><span data-stu-id="b2024-114">How the server object responds to a cancellation request is at the discretion of the server implementer, but the calling thread on the client will always be unblocked and will ignore whatever results the server tries to pass to it.</span></span> <span data-ttu-id="b2024-115">Los objetos CANCEL proporcionan un medio para solicitar que se cancele un método que se está ejecutando actualmente, pero no hay ninguna garantía de que el objeto de servidor detenga el procesamiento de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b2024-115">Cancel objects provide a means to request that a currently running method be canceled, but there is no guarantee that the server object will stop processing the call.</span></span> <span data-ttu-id="b2024-116">Por ejemplo, puede que la llamada ya haya devuelto o que el objeto de servidor no admita objetos de cancelación.</span><span class="sxs-lookup"><span data-stu-id="b2024-116">For example, the call may have already returned, or the server object may not support cancel objects.</span></span>

<span data-ttu-id="b2024-117">COM proporciona automáticamente una implementación estándar de los objetos de cancelación para objetos de cliente e interfaces que usan el cálculo de referencias estándar.</span><span class="sxs-lookup"><span data-stu-id="b2024-117">COM automatically provides a standard implementation of cancel objects for client objects and interfaces that use standard marshaling.</span></span> <span data-ttu-id="b2024-118">En el caso de los objetos e interfaces que usan el cálculo de referencias personalizado, deberá implementar su propio objeto CANCEL.</span><span class="sxs-lookup"><span data-stu-id="b2024-118">For objects and interfaces that use custom marshaling, you will need to implement your own cancel object.</span></span>

<span data-ttu-id="b2024-119">En este momento, los objetos CANCEL solo administran llamadas sincrónicas.</span><span class="sxs-lookup"><span data-stu-id="b2024-119">At this time, cancel objects handle only synchronous calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2024-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b2024-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2024-121">Cancelar una llamada asincrónica</span><span class="sxs-lookup"><span data-stu-id="b2024-121">Canceling an Asynchronous Call</span></span>](canceling-an-asynchronous-call.md)
</dt> <dt>

[<span data-ttu-id="b2024-122">**CoGetCancelObject**</span><span class="sxs-lookup"><span data-stu-id="b2024-122">**CoGetCancelObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcancelobject)
</dt> <dt>

[<span data-ttu-id="b2024-123">**CoSetCancelObject**</span><span class="sxs-lookup"><span data-stu-id="b2024-123">**CoSetCancelObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cosetcancelobject)
</dt> <dt>

[<span data-ttu-id="b2024-124">**CoTestCancel**</span><span class="sxs-lookup"><span data-stu-id="b2024-124">**CoTestCancel**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotestcancel)
</dt> </dl>

 

 