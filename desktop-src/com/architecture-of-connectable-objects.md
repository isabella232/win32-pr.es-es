---
title: Arquitectura de objetos conectables
description: Arquitectura de objetos conectables
ms.assetid: 69949a3b-3ab8-4054-84d8-9256fbf39c7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9d8d2909942d1c04aed972e7891a6f4ae3f730
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "105717318"
---
# <a name="architecture-of-connectable-objects"></a>Arquitectura de objetos conectables

El objeto conectable es solo una parte de la arquitectura general de los objetos conectables. Esta tecnología incluye los siguientes elementos:

-   **Objeto conectable.** Implementa la interfaz [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) ; crea al menos un objeto de punto de conexión; define una interfaz de salida para el cliente.
-   **Nº.** Consulta el objeto para que [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) determine si el objeto es conectable; crea un objeto de receptor para implementar la interfaz de salida definida por el objeto conectable.
-   **Objeto receptor.** Implementa la interfaz de salida; se utiliza para establecer una conexión con el objeto conectable.
-   **Objeto de punto de conexión.** Implementa la interfaz [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) y administra la conexión con el receptor del cliente.

En el diagrama siguiente se muestran las relaciones entre el cliente, el objeto conectable, un punto de conexión y un receptor:

![Diagrama que muestra los puntos de conexión entre el cliente y el objeto conectable.](images/1cd44fec-5d2c-4427-846b-ccab7ec0b08a.png)

Antes de que el objeto de punto de conexión llame a los métodos de la interfaz de receptor en el paso 3 del diagrama anterior, debe ejecutar [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para la interfaz específica necesaria, incluso si el puntero ya se pasó en la llamada de paso 2 al método [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) .

Aunque no se muestra en la ilustración, también hay dos objetos de enumerador implicados en esta arquitectura. Uno se crea mediante un método en [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) para enumerar los puntos de conexión dentro del objeto conectable. El otro se crea mediante un método en [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) para enumerar las conexiones establecidas actualmente a ese punto de conexión. Un punto de conexión puede admitir varias interfaces de receptor conectadas y debe recorrer en iteración la lista de conexiones cada vez que realiza una llamada al método en esa interfaz. Este proceso se conoce como multidifusión.

Al trabajar con objetos conectables, es importante comprender que el objeto conectable, cada punto de conexión, cada receptor y todos los enumeradores son objetos independientes con implementaciones [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) independientes, recuentos de referencias independientes y duraciones independientes. Un cliente que utiliza estos objetos siempre es responsable de liberar todos los recuentos de referencias que posee.

> [!Note]  
> Un objeto conectable puede admitir más de un cliente y puede admitir varios receptores dentro de un cliente. Del mismo modo, un receptor puede estar conectado a más de un objeto conectable.

 

Los pasos para establecer una conexión entre un cliente y un objeto conectable son los siguientes:

1.  El cliente consulta [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) en el objeto para determinar si el objeto es conectable. Si esta llamada es correcta, el cliente mantiene un puntero a la interfaz **IConnectionPointContainer** en el objeto conectable y se ha incrementado el contador de referencias de objetos conectables. De lo contrario, el objeto no es conectable y no admite interfaces de salida.
2.  Si el objeto es conectable, el cliente siguiente intenta obtener un puntero a la interfaz [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) en un punto de conexión dentro del objeto conectable. Hay dos métodos para obtener este puntero, tanto en [**IConnectionPointContainer:: FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) como en [**IConnectionPointContainer:: EnumConnectionPoints**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints). Se necesitan algunos pasos adicionales si se usa **EnumConnectionPoints** . (Consulte [usar IConnectionPointContainer](using-iconnectionpointcontainer.md) para obtener más información). Si es correcto, el objeto conectable y el cliente admiten la misma interfaz de salida. El objeto conectable lo define y lo llama, y el cliente lo implementa. A continuación, el cliente puede comunicarse a través del punto de conexión dentro del objeto conectable.
3.  Después, el cliente llama a [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) en el punto de conexión para establecer una conexión entre su interfaz receptora y el punto de conexión del objeto. Después de esta llamada, el punto de conexión del objeto contiene un puntero a la interfaz de salida en el receptor.
4.  El código incluido en [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) llama a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero de interfaz que se pasa, solicitando el identificador de interfaz específico al que se conecta.
5.  El objeto llama a los métodos en la interfaz del receptor según sea necesario, mediante el puntero mantenido por su punto de conexión.
6.  El cliente llama a [**unaconsej**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise) para finalizar la conexión. Después, el cliente llama a **IConnectionPoint:: Release** para liberar su retención en el punto de conexión y, por lo tanto, también el objeto connectable principal. El cliente también debe llamar a **IConnectionPointContainer:: Release** para liberar su suspensión en el objeto connectable principal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces de objeto conectables](connectable-object-interfaces.md)
</dt> </dl>

 

 




