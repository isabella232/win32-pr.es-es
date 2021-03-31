---
description: Después de haber registrado una clase de eventos en el catálogo de COM+, puede Agregar suscriptores a la clase de eventos y las suscripciones a los suscriptores.
ms.assetid: 101b1075-3724-4508-9c9e-2f12ac6ab65d
title: Registro de una suscripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03d5710fc792cad6282683d51df21d2ede10451
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423443"
---
# <a name="registering-a-subscription"></a><span data-ttu-id="9e851-103">Registro de una suscripción</span><span class="sxs-lookup"><span data-stu-id="9e851-103">Registering a Subscription</span></span>

<span data-ttu-id="9e851-104">Después de haber registrado una clase de eventos en el catálogo de COM+, puede Agregar suscriptores a la clase de eventos y las suscripciones a los suscriptores.</span><span class="sxs-lookup"><span data-stu-id="9e851-104">After you have registered an event class in the COM+ catalog, you can add subscribers to the event class and subscriptions to the subscribers.</span></span> <span data-ttu-id="9e851-105">Las suscripciones se pueden suscribir a un único método o a todos los métodos de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="9e851-105">Subscriptions can subscribe to a single method or to all the methods of an interface.</span></span> <span data-ttu-id="9e851-106">Para recibir llamadas en más de un método, pero no en todos los métodos, de una interfaz, debe agregar una suscripción para cada método al que desee recibir una llamada.</span><span class="sxs-lookup"><span data-stu-id="9e851-106">To receive calls on more than one method—but not to every method—of an interface, you must add a subscription for each method to which you want to receive a call.</span></span> <span data-ttu-id="9e851-107">La herramienta de administración de servicios de componentes puede buscar en el catálogo de COM+ las clases de eventos registradas que admiten las interfaces implementadas por el suscriptor y le ofrece la opción de suscribirse.</span><span class="sxs-lookup"><span data-stu-id="9e851-107">The Component Services administration tool can search the COM+ catalog for registered event classes that support the interfaces implemented by the subscriber and offers you the choice to subscribe.</span></span> <span data-ttu-id="9e851-108">Elija el publicador que le ofrezca los eventos deseados.</span><span class="sxs-lookup"><span data-stu-id="9e851-108">Choose the publisher that offers you the desired events.</span></span>

<span data-ttu-id="9e851-109">Para agregar suscriptores al componente suscriptor, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="9e851-109">To add subscribers to the subscriber component, use the following steps:</span></span>

1.  <span data-ttu-id="9e851-110">Después de crear una nueva aplicación COM+ e instalar el componente de suscriptor, haga clic con el botón secundario en la carpeta **suscripciones** para habilitar el Asistente para nueva suscripción com+.</span><span class="sxs-lookup"><span data-stu-id="9e851-110">After creating a new COM+ application and installing the subscriber component, right-click the **Subscriptions** folder to enable the COM+ New Subscription Wizard.</span></span>

2.  <span data-ttu-id="9e851-111">Elija la clase de eventos de la que desea recibir eventos.</span><span class="sxs-lookup"><span data-stu-id="9e851-111">Choose the event class from which you want to receive events.</span></span>

3.  <span data-ttu-id="9e851-112">Escriba el nombre de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="9e851-112">Enter a name for the subscription.</span></span>

4.  <span data-ttu-id="9e851-113">Habilite la suscripción.</span><span class="sxs-lookup"><span data-stu-id="9e851-113">Enable the subscription.</span></span>

5.  <span data-ttu-id="9e851-114">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e851-114">Click **OK**.</span></span>

<span data-ttu-id="9e851-115">Cuando una aplicación de publicador desea activar un evento, el publicador crea una instancia del objeto de la clase de evento y llama a un método en él.</span><span class="sxs-lookup"><span data-stu-id="9e851-115">When a publisher application wants to fire an event, the publisher instantiates the event class object and calls a method on it.</span></span> <span data-ttu-id="9e851-116">COM+ busca en el catálogo de COM+ para encontrar todos los suscriptores.</span><span class="sxs-lookup"><span data-stu-id="9e851-116">COM+ searches the COM+ catalog to find all the subscribers.</span></span> <span data-ttu-id="9e851-117">Crea el objeto de suscriptor (directamente, en cola o con un moniker) y pasa la llamada al método realizada originalmente por el publicador.</span><span class="sxs-lookup"><span data-stu-id="9e851-117">It creates the subscriber object (directly, queued, or with a moniker) and passes on the method call originally made by the publisher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e851-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e851-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e851-119">Registrar una clase de eventos</span><span class="sxs-lookup"><span data-stu-id="9e851-119">Registering an Event Class</span></span>](registering-an-event-class.md)
</dt> </dl>

 

 



