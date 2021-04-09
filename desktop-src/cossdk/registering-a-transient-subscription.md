---
description: No se pueden establecer suscripciones transitorias mediante la herramienta de administración de servicios de componentes. Debe utilizar las interfaces administrativas de COM+ para crear o actualizar una suscripción transitoria.
ms.assetid: 28d48d59-abb2-4682-ab54-60b6aa7b31b1
title: Registro de una suscripción transitoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fc85f189d14fbe6220d6f3760509e1ba0248a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153064"
---
# <a name="registering-a-transient-subscription"></a><span data-ttu-id="9e4bf-104">Registro de una suscripción transitoria</span><span class="sxs-lookup"><span data-stu-id="9e4bf-104">Registering a Transient Subscription</span></span>

<span data-ttu-id="9e4bf-105">Las suscripciones transitorias solicitan un evento para un objeto de suscriptor específico que ya existe.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-105">Transient subscriptions request an event for a specific subscriber object that already exists.</span></span> <span data-ttu-id="9e4bf-106">Las suscripciones transitorias se almacenan en el catálogo de COM+, pero la suscripción se elimina si se detiene el sistema operativo o el sistema de eventos.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-106">Transient subscriptions are stored in the COM+ catalog, but the subscription is deleted if the event system or operating system is stopped.</span></span> <span data-ttu-id="9e4bf-107">A diferencia de las suscripciones persistentes, las suscripciones transitorias se asocian a un objeto determinado y solo se almacenan en el sistema de eventos.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-107">Unlike persistent subscriptions, transient subscriptions are tied to a particular object and are stored only in the event system.</span></span> <span data-ttu-id="9e4bf-108">Si hay un problema con el sistema operativo o el sistema de eventos, la suscripción desaparece.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-108">If there is a problem with the event system or operating system, the subscription disappears.</span></span> <span data-ttu-id="9e4bf-109">Las suscripciones transitorias pueden ser más eficaces que las suscripciones persistentes, pero debe administrar los ciclos de vida de los objetos.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-109">Transient subscriptions can be more efficient than persistent subscriptions, but you must manage their object life cycles.</span></span>

<span data-ttu-id="9e4bf-110">No se pueden establecer suscripciones transitorias mediante la herramienta de administración de servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-110">Transient subscriptions cannot be set by using the Component Services administration tool.</span></span> <span data-ttu-id="9e4bf-111">Debe utilizar las interfaces administrativas de COM+ para crear o actualizar una suscripción transitoria.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-111">You must use the COM+ administrative interfaces to create or update a transient subscription.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="9e4bf-112">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9e4bf-112">Visual Basic</span></span>

<span data-ttu-id="9e4bf-113">En el procedimiento siguiente se describe cómo crear una suscripción transitoria mediante Microsoft Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="9e4bf-113">The following procedure describes how to create a transient subscription using Microsoft Visual Basic:</span></span>

1.  <span data-ttu-id="9e4bf-114">Especifique una suscripción como transitoria agregando una nueva entrada a la colección [**TransientSubscriptions**](transientsubscriptions.md) y estableciendo la propiedad SubscriberInterface en la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) del objeto de suscriptor.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-114">Specify a subscription as transient by adding a new entry to the [**TransientSubscriptions**](transientsubscriptions.md) collection and setting the SubscriberInterface property to the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface of the subscriber object.</span></span> <span data-ttu-id="9e4bf-115">Los eventos COM+ no crean una nueva instancia del objeto de suscriptor al activar un evento, sino que utiliza la instancia que se especifique.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-115">COM+ Events does not create a new instance of the subscriber object when firing an event but instead uses the instance you specify.</span></span> <span data-ttu-id="9e4bf-116">Eventos COM+ contiene un recuento de referencias para el objeto de suscriptor hasta que se quite la suscripción del sistema.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-116">COM+ Events holds a reference count for the subscriber object until the subscription is removed from the system.</span></span>
2.  <span data-ttu-id="9e4bf-117">Cree una aplicación de servidor COM+ (un archivo. exe,. dll o. ocx) con un objeto que implemente las interfaces o los métodos a los que desea suscribirse.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-117">Create a COM+ server application (an .exe, a .dll, or an .ocx file) with an object that implements the interfaces or methods you want to subscribe to.</span></span>
3.  <span data-ttu-id="9e4bf-118">Cree su suscripción transitoria mediante el código siguiente, pasando el CLSID del objeto de la [clase de evento](the-com--event-class-object.md) y la instancia del objeto de suscriptor.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-118">Create your transient subscription using the following code, by passing in the CLSID of the [event class](the-com--event-class-object.md) object and the instance of the subscriber object.</span></span> <span data-ttu-id="9e4bf-119">Con la herramienta administrativa Servicios de componentes, puede obtener la propiedad EventCLSID haciendo clic con el botón secundario en el componente COM+, seleccionando **propiedades** y seleccionando la pestaña **General** .</span><span class="sxs-lookup"><span data-stu-id="9e4bf-119">Using the Component Services administrative tool, you can get the EventCLSID property by right-clicking the COM+ component, selecting **Properties**, and selecting the **General** tab.</span></span>

    ``` syntax
    Public Function CreateTransientSubscription( _
      ByVal clsid As String, ByVal objref As Object) As String 
        Dim oCOMAdminCatalog As COMAdmin.COMAdminCatalog
        Dim oTSCol As COMAdminCatalogCollection
        Dim oSubscription As ICatalogObject
        Dim objvar As Variant
        On Error GoTo CreateTransientSubscriptionError
        Set oCOMAdminCatalog = CreateObject("COMAdmin.COMAdminCatalog")
        'Gets the TransientSubscriptions collection
        Set oTSCol = oCOMAdminCatalog.GetCollection( _
          "TransientSubscriptions")
        Set oSubscription = oTSCol.Add
        Set objvar = objref
        oSubscription.Value("SubscriberInterface") = objref
        oSubscription.Value("EventCLSID") = clsid
        oSubscription.Value("Name") = "TransientSubscription"
        oTSCol.SaveChanges
        CreateTransientSubscription = oSubscription.Value("ID")
        Set oSubscription = Nothing
        Set oTSCol = Nothing
        Set oCOMAdminCatalog = Nothing
        Set objvar = Nothing
        Exit Function
    CreateTransientSubscriptionError:
        CreateTransientSubscription = ""
        Err.Raise Err.Number, "[CreateTransientSubscription]" & _
          Err.Source, Err.Description
    End Function
    ```

<span data-ttu-id="9e4bf-120">En el ejemplo siguiente se muestra cómo llamar a la función CreateTransientSubscription para suscribirse a una interfaz denominada IStockTicker, que tiene un método denominado UpdateStock.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-120">The following example illustrates how to call the CreateTransientSubscription function to subscribe to an interface called IStockTicker, which has a method called UpdateStock.</span></span>

1.  <span data-ttu-id="9e4bf-121">Cree una clase de eventos que admita la interfaz IStockTicker, que tiene un método, UpdateStock.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-121">Create an event class that supports the interface IStockTicker, which has one method, UpdateStock.</span></span>
2.  <span data-ttu-id="9e4bf-122">En el proyecto del suscriptor, agregue una clase que implemente la interfaz IStockTicker.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-122">In your subscriber project, add a class that implements the IStockTicker interface.</span></span>
3.  <span data-ttu-id="9e4bf-123">Cuando quiera suscribirse, ejecute el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="9e4bf-123">When you want to subscribe execute the following code:</span></span>

    ``` syntax
    Dim oMyTicker As Object
    Dim sSubscriptionID As String
    Set oMyTicker = CreateObject("TheProject.CMyTicker")
    sSubscriptionID = CreateTransientSubscription( _
      "{..CLSID for the Event Class..}", oMyTicker)
    ```

<span data-ttu-id="9e4bf-124">La función CreateTransientSubscription devuelve una cadena, que es un GUID que se puede usar como identificador o cookie para revocar la suscripción más adelante.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-124">The CreateTransientSubscription function returns a string, which is a GUID that can be used as a handle or a cookie to revoke the subscription later.</span></span> <span data-ttu-id="9e4bf-125">Para quitar la suscripción, llame al método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de [**COMAdminCatalogCollection**](comadmincatalogcollection.md) en la colección [**TransientSubscriptions**](transientsubscriptions.md) , pasando el índice correspondiente a la suscripción con el GUID recibido previamente.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-125">To remove the subscription, call the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of [**COMAdminCatalogCollection**](comadmincatalogcollection.md) on the [**TransientSubscriptions**](transientsubscriptions.md) collection, passing in the index corresponding to the subscription with the GUID previously received.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e4bf-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e4bf-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e4bf-127">Registro de una suscripción</span><span class="sxs-lookup"><span data-stu-id="9e4bf-127">Registering a Subscription</span></span>](registering-a-subscription.md)
</dt> </dl>

 

 
