---
description: Las suscripciones transitorias no se pueden establecer mediante la herramienta de administración servicios de componentes. Debe usar las interfaces administrativas de COM+ para crear o actualizar una suscripción transitoria.
ms.assetid: 28d48d59-abb2-4682-ab54-60b6aa7b31b1
title: Registro de una suscripción transitoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f93b543a4602b0b4ed7ed4177133f3eb8f543a0db02750af8657ab36f310993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990445"
---
# <a name="registering-a-transient-subscription"></a>Registro de una suscripción transitoria

Las suscripciones transitorias solicitan un evento para un objeto de suscriptor específico que ya existe. Las suscripciones transitorias se almacenan en el catálogo de COM+, pero la suscripción se elimina si se detiene el sistema operativo o el sistema operativo. A diferencia de las suscripciones persistentes, las suscripciones transitorias están vinculadas a un objeto determinado y solo se almacenan en el sistema de eventos. Si hay un problema con el sistema de eventos o el sistema operativo, la suscripción desaparece. Las suscripciones transitorias pueden ser más eficaces que las suscripciones persistentes, pero debe administrar sus ciclos de vida de objetos.

Las suscripciones transitorias no se pueden establecer mediante la herramienta de administración servicios de componentes. Debe usar las interfaces administrativas de COM+ para crear o actualizar una suscripción transitoria.

## <a name="visual-basic"></a>Visual Basic

En el procedimiento siguiente se describe cómo crear una suscripción transitoria mediante Microsoft Visual Basic:

1.  Especifique una suscripción como transitoria agregando una nueva entrada a la colección [**TransientSubscriptions**](transientsubscriptions.md) y estableciendo la propiedad SubscriberInterface en la [**interfaz IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) del objeto de suscriptor. Eventos COM+ no crea una nueva instancia del objeto de suscriptor al activar un evento, sino que usa la instancia que especifique. Eventos COM+ contiene un recuento de referencias para el objeto de suscriptor hasta que la suscripción se quita del sistema.
2.  Cree una aplicación de servidor COM+ (un .exe, un .dll o un archivo .ocx) con un objeto que implemente las interfaces o métodos a los que desea suscribirse.
3.  Cree la suscripción transitoria con el código siguiente, pasando [](the-com--event-class-object.md) el CLSID del objeto de clase de eventos y la instancia del objeto de suscriptor. Con la herramienta administrativa Servicios de componentes, puede obtener la propiedad EventCLSID haciendo clic con el botón derecho en el componente COM+, seleccionando Propiedades y seleccionando la **pestaña General.**

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
2.  En el proyecto de suscriptor, agregue una clase que implemente la interfaz IStockTicker.
3.  Si desea suscribirse, ejecute el código siguiente:

    ``` syntax
    Dim oMyTicker As Object
    Dim sSubscriptionID As String
    Set oMyTicker = CreateObject("TheProject.CMyTicker")
    sSubscriptionID = CreateTransientSubscription( _
      "{..CLSID for the Event Class..}", oMyTicker)
    ```

La función CreateTransientSubscription devuelve una cadena, que es un GUID que se puede usar como identificador o una cookie para revocar la suscripción más adelante. Para quitar la suscripción, llame al método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de [**COMAdminCatalogCollection**](comadmincatalogcollection.md) en la colección [**TransientSubscriptions**](transientsubscriptions.md) y pase el índice correspondiente a la suscripción con el GUID recibido anteriormente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de una suscripción](registering-a-subscription.md)
</dt> </dl>

 

 
