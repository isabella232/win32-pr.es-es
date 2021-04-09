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
# <a name="registering-a-transient-subscription"></a>Registro de una suscripción transitoria

Las suscripciones transitorias solicitan un evento para un objeto de suscriptor específico que ya existe. Las suscripciones transitorias se almacenan en el catálogo de COM+, pero la suscripción se elimina si se detiene el sistema operativo o el sistema de eventos. A diferencia de las suscripciones persistentes, las suscripciones transitorias se asocian a un objeto determinado y solo se almacenan en el sistema de eventos. Si hay un problema con el sistema operativo o el sistema de eventos, la suscripción desaparece. Las suscripciones transitorias pueden ser más eficaces que las suscripciones persistentes, pero debe administrar los ciclos de vida de los objetos.

No se pueden establecer suscripciones transitorias mediante la herramienta de administración de servicios de componentes. Debe utilizar las interfaces administrativas de COM+ para crear o actualizar una suscripción transitoria.

## <a name="visual-basic"></a>Visual Basic

En el procedimiento siguiente se describe cómo crear una suscripción transitoria mediante Microsoft Visual Basic:

1.  Especifique una suscripción como transitoria agregando una nueva entrada a la colección [**TransientSubscriptions**](transientsubscriptions.md) y estableciendo la propiedad SubscriberInterface en la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) del objeto de suscriptor. Los eventos COM+ no crean una nueva instancia del objeto de suscriptor al activar un evento, sino que utiliza la instancia que se especifique. Eventos COM+ contiene un recuento de referencias para el objeto de suscriptor hasta que se quite la suscripción del sistema.
2.  Cree una aplicación de servidor COM+ (un archivo. exe,. dll o. ocx) con un objeto que implemente las interfaces o los métodos a los que desea suscribirse.
3.  Cree su suscripción transitoria mediante el código siguiente, pasando el CLSID del objeto de la [clase de evento](the-com--event-class-object.md) y la instancia del objeto de suscriptor. Con la herramienta administrativa Servicios de componentes, puede obtener la propiedad EventCLSID haciendo clic con el botón secundario en el componente COM+, seleccionando **propiedades** y seleccionando la pestaña **General** .

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

En el ejemplo siguiente se muestra cómo llamar a la función CreateTransientSubscription para suscribirse a una interfaz denominada IStockTicker, que tiene un método denominado UpdateStock.

1.  Cree una clase de eventos que admita la interfaz IStockTicker, que tiene un método, UpdateStock.
2.  En el proyecto del suscriptor, agregue una clase que implemente la interfaz IStockTicker.
3.  Cuando quiera suscribirse, ejecute el código siguiente:

    ``` syntax
    Dim oMyTicker As Object
    Dim sSubscriptionID As String
    Set oMyTicker = CreateObject("TheProject.CMyTicker")
    sSubscriptionID = CreateTransientSubscription( _
      "{..CLSID for the Event Class..}", oMyTicker)
    ```

La función CreateTransientSubscription devuelve una cadena, que es un GUID que se puede usar como identificador o cookie para revocar la suscripción más adelante. Para quitar la suscripción, llame al método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de [**COMAdminCatalogCollection**](comadmincatalogcollection.md) en la colección [**TransientSubscriptions**](transientsubscriptions.md) , pasando el índice correspondiente a la suscripción con el GUID recibido previamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de una suscripción](registering-a-subscription.md)
</dt> </dl>

 

 
