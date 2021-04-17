---
description: Publicación de un evento
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: Publicación de un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c060d8bf67e12fc7429b2afc768794468a1c49ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705320"
---
# <a name="publishing-an-event"></a><span data-ttu-id="c1215-103">Publicación de un evento</span><span class="sxs-lookup"><span data-stu-id="c1215-103">Publishing an Event</span></span>

<span data-ttu-id="c1215-104">Para publicar un evento, basta con crear una instancia de un objeto de evento llamando a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o el método **CreateObject** de Microsoft Visual Basic mediante EventClassID o EventClassName como argumento.</span><span class="sxs-lookup"><span data-stu-id="c1215-104">To publish an event, just instantiate an event object by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or the Microsoft Visual Basic **CreateObject** method using EventClassID or EventClassName as an argument.</span></span> <span data-ttu-id="c1215-105">El publicador llama a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el objeto de evento para obtener las interfaces admitidas por el objeto de la clase de evento e invoca un método en el objeto de evento a través de la interfaz para publicar el evento.</span><span class="sxs-lookup"><span data-stu-id="c1215-105">The publisher calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the event object to obtain the interfaces supported by the event class object and invokes a method on the event object through the interface to publish the event.</span></span> <span data-ttu-id="c1215-106">Después, el sistema de eventos publica eventos en la clase de evento CLSID \_ EventObjectChange con el identificador de interfaz IID \_ IEventObjectChange.</span><span class="sxs-lookup"><span data-stu-id="c1215-106">The event system then publishes events on the event class CLSID\_EventObjectChange with the interface ID IID\_IEventObjectChange.</span></span>

<span data-ttu-id="c1215-107">Para admitir la entrega de eventos a varios suscriptores, los métodos de la clase de evento solo deben contener parámetros in.</span><span class="sxs-lookup"><span data-stu-id="c1215-107">To support delivery of events to multiple subscribers, event class methods should contain only in parameters.</span></span>

<span data-ttu-id="c1215-108">Mediante el uso de la propiedad FireInParallel del objeto de la [clase de eventos](the-com--event-class-object.md) , los publicadores pueden solicitar que el sistema de eventos utilice varios subprocesos para proporcionar un evento a más de un suscriptor.</span><span class="sxs-lookup"><span data-stu-id="c1215-108">By using the FireInParallel property of the [event class](the-com--event-class-object.md) object, publishers can request that the event system use multiple threads to deliver an event to more than one subscriber.</span></span> <span data-ttu-id="c1215-109">La selección de un mecanismo de entrega en paralelo no garantiza la entrega simultánea del evento a varios suscriptores, pero indica al servicio de eventos COM+ que le permita que esto suceda.</span><span class="sxs-lookup"><span data-stu-id="c1215-109">Selecting an in-parallel delivery mechanism does not guarantee simultaneous delivery of the event to multiple subscribers, but it instructs the COM+ events service to permit this to happen.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1215-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c1215-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1215-111">Publicar y entregar eventos en COM+</span><span class="sxs-lookup"><span data-stu-id="c1215-111">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 
