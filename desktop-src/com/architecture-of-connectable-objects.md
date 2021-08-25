---
title: Arquitectura de objetos conectables
description: Arquitectura de objetos conectables
ms.assetid: 69949a3b-3ab8-4054-84d8-9256fbf39c7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1215b013c3db751e90b07ed21d5f897ef0332000ce2cd2b3b167cbe86798927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993965"
---
# <a name="architecture-of-connectable-objects"></a>Arquitectura de objetos conectables

El objeto conectable es solo una parte de la arquitectura general de los objetos conectables. Esta tecnología incluye los siguientes elementos:

-   **Objeto conectable.** Implementa la [**interfaz IConnectionPointContainer;**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) crea al menos un objeto de punto de conexión; define una interfaz saliente para el cliente.
-   **Cliente.** Consulta el objeto para [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) para determinar si el objeto es conectable; crea un objeto receptor para implementar la interfaz saliente definida por el objeto conectable.
-   **Objeto receptor.** Implementa la interfaz saliente; se usa para establecer una conexión con el objeto conectable.
-   **Objeto de punto de conexión.** Implementa la interfaz [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) y administra la conexión con el receptor del cliente.

Las relaciones entre el cliente, el objeto conectable, un punto de conexión y un receptor se ilustran en el diagrama siguiente:

![Diagrama que muestra los puntos de conexión entre el cliente y el objeto conectable.](images/1cd44fec-5d2c-4427-846b-ccab7ec0b08a.png)

Antes de que el objeto de punto de conexión llame a métodos en la interfaz receptora en el paso 3 del diagrama anterior, debe [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para la interfaz específica necesaria, incluso si el puntero ya se pasó en la llamada del paso 2 al método [**Advise.**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise)

También hay dos objetos enumerador implicados en esta arquitectura, aunque no se muestran en la ilustración. Un método de [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) crea uno para enumerar los puntos de conexión dentro del objeto conectable. El otro se crea mediante un método en [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) para enumerar las conexiones establecidas actualmente a ese punto de conexión. Un punto de conexión puede admitir varias interfaces de receptor conectadas y debe recorrer en iteración la lista de conexiones cada vez que realiza una llamada de método en esa interfaz. Este proceso se conoce como multidifusión.

Al trabajar con objetos conectables, es importante comprender que el objeto conectable, cada punto de conexión, cada receptor y todos los enumeradores son objetos independientes con implementaciones [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) independientes, recuentos de referencias independientes y duraciones independientes. Un cliente que usa estos objetos siempre es responsable de liberar todos los recuentos de referencias que posee.

> [!Note]  
> Un objeto conectable puede admitir más de un cliente y puede admitir varios receptores dentro de un cliente. Del mismo modo, un receptor se puede conectar a más de un objeto conectable.

 

Los pasos para establecer una conexión entre un cliente y un objeto conectable son los siguientes:

1.  El cliente consulta [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) en el objeto para determinar si el objeto es conectable. Si esta llamada se realiza correctamente, el cliente contiene un puntero a la interfaz **IConnectionPointContainer** en el objeto conectable y se ha incrementado el contador de referencia de objeto conectable. De lo contrario, el objeto no es conectable y no admite interfaces salientes.
2.  Si el objeto es conectable, el cliente intenta obtener un puntero a la interfaz [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) en un punto de conexión dentro del objeto conectable. Hay dos métodos para obtener este puntero, tanto en [**IConnectionPointContainer::FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) como en [**IConnectionPointContainer::EnumConnectionPoints**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints). Si se usa **EnumConnectionPoints,** se necesitan algunos pasos adicionales. (Vea [Uso de IConnectionPointContainer para](using-iconnectionpointcontainer.md) obtener más información). Si se realiza correctamente, tanto el objeto conectable como el cliente admiten la misma interfaz saliente. El objeto conectable lo define y lo llama, y el cliente lo implementa. A continuación, el cliente puede comunicarse a través del punto de conexión dentro del objeto conectable.
3.  A continuación, el cliente llama a [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) en el punto de conexión para establecer una conexión entre su interfaz receptora y el punto de conexión del objeto. Después de esta llamada, el punto de conexión del objeto contiene un puntero a la interfaz saliente en el receptor.
4.  El código de [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) llama [**a QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero de interfaz que se pasa, solicitando el identificador de interfaz específico al que se conecta.
5.  El objeto llama a métodos en la interfaz del receptor según sea necesario, utilizando el puntero que mantiene su punto de conexión.
6.  El cliente llama [**a Unadvise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise) para finalizar la conexión. A continuación, el cliente llama a **IConnectionPoint::Release para** liberar su retención en el punto de conexión y, por lo tanto, el objeto conectable principal también. El cliente también debe llamar a **IConnectionPointContainer::Release para** liberar su retención en el objeto conectable principal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces de objetos conectables](connectable-object-interfaces.md)
</dt> </dl>

 

 




