---
description: Recuperar eventos
ms.assetid: 18c5892d-7e33-497c-ab7d-d17fea5df17e
title: Recuperar eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d23cf4f8060c15db564e718ba3a2fa4a660022
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422736"
---
# <a name="retrieving-events"></a><span data-ttu-id="785f9-103">Recuperar eventos</span><span class="sxs-lookup"><span data-stu-id="785f9-103">Retrieving Events</span></span>

<span data-ttu-id="785f9-104">El administrador de gráficos de filtro expone tres interfaces que admiten la notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="785f9-104">The Filter Graph Manager exposes three interfaces that support event notification.</span></span>

-   <span data-ttu-id="785f9-105">[**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) contiene el método para los filtros para publicar eventos.</span><span class="sxs-lookup"><span data-stu-id="785f9-105">[**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) contains the method for filters to post events.</span></span>
-   <span data-ttu-id="785f9-106">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) contiene métodos para que las aplicaciones recuperen eventos.</span><span class="sxs-lookup"><span data-stu-id="785f9-106">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) contains methods for applications to retrieve events.</span></span>
-   <span data-ttu-id="785f9-107">[**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) hereda de y extiende la interfaz [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .</span><span class="sxs-lookup"><span data-stu-id="785f9-107">[**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) inherits from and extends the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface.</span></span>

<span data-ttu-id="785f9-108">Los filtros envían notificaciones de eventos mediante una llamada al método [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) en el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="785f9-108">Filters post event notifications by calling the [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) method on the Filter Graph Manager.</span></span> <span data-ttu-id="785f9-109">Una notificación de eventos consta de un código de evento, que define el tipo de evento y dos parámetros que proporcionan información adicional.</span><span class="sxs-lookup"><span data-stu-id="785f9-109">An event notification consists of an event code, which defines the type of event, and two parameters that give additional information.</span></span> <span data-ttu-id="785f9-110">Dependiendo del código de evento, los parámetros pueden contener punteros, códigos de retorno, tiempos de referencia u otra información.</span><span class="sxs-lookup"><span data-stu-id="785f9-110">Depending on the event code, the parameters might contain pointers, return codes, reference times, or other information.</span></span> <span data-ttu-id="785f9-111">Para obtener una lista completa de los códigos de evento y los parámetros, vea [códigos de notificación de eventos](event-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="785f9-111">For a complete list of event codes and parameters, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="785f9-112">Para recuperar un evento de la cola, la aplicación llama al método [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) en el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="785f9-112">To retrieve an event from the queue, the application calls the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method on the Filter Graph Manager.</span></span> <span data-ttu-id="785f9-113">Este método se bloquea hasta que hay un evento que se va a devolver o hasta que transcurre un tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="785f9-113">This method blocks until there is an event to return or until a specified time elapses.</span></span> <span data-ttu-id="785f9-114">Suponiendo que haya un evento en cola, el método devuelve con el código de evento y los dos parámetros de evento.</span><span class="sxs-lookup"><span data-stu-id="785f9-114">Assuming there is a queued event, the method returns with the event code and the two event parameters.</span></span> <span data-ttu-id="785f9-115">Después de llamar a **GetEvent**, una aplicación siempre debe llamar al método [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) para liberar los recursos asociados a los parámetros de evento.</span><span class="sxs-lookup"><span data-stu-id="785f9-115">After calling **GetEvent**, an application should always call the [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) method to release any resources associated with the event parameters.</span></span> <span data-ttu-id="785f9-116">Por ejemplo, un parámetro puede ser un valor **BSTR** asignado por el gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="785f9-116">For example, a parameter might be a **BSTR** value that was allocated by the filter graph.</span></span>

<span data-ttu-id="785f9-117">En el ejemplo de código siguiente se proporciona un esquema de cómo recuperar eventos de la cola.</span><span class="sxs-lookup"><span data-stu-id="785f9-117">The following code example provides an outline of how to retrieve events from the queue.</span></span>


```C++
long evCode;
LONG_PTR param1, param2;
HRESULT hr;
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch(evCode) 
    { 
        // Call application-defined functions for each 
        // type of event that you want to handle.
    } 
    hr = pEvent->FreeEventParams(evCode, param1, param2);
}
```



<span data-ttu-id="785f9-118">Para invalidar el control predeterminado del administrador de gráficos de filtro para un evento, llame al método [**IMediaEvent:: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) con el código de evento como parámetro.</span><span class="sxs-lookup"><span data-stu-id="785f9-118">To override the Filter Graph Manager's default handling for an event, call the [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) method with the event code as a parameter.</span></span> <span data-ttu-id="785f9-119">Puede restablecer el control predeterminado llamando al método [**IMediaEvent:: RestoreDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) .</span><span class="sxs-lookup"><span data-stu-id="785f9-119">You can reinstate the default handling by calling the [**IMediaEvent::RestoreDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) method.</span></span> <span data-ttu-id="785f9-120">Si el gráfico de filtros no realiza ningún control predeterminado para el código de evento especificado, la llamada a estos métodos no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="785f9-120">If the filter graph performs no default handling for the specified event code, calling these methods has no effect.</span></span>

## <a name="related-topics"></a><span data-ttu-id="785f9-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="785f9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="785f9-122">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="785f9-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



