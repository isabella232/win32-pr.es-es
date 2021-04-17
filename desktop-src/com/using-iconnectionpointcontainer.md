---
title: Usar IConnectionPointContainer
description: Usar IConnectionPointContainer
ms.assetid: a87afb25-4d45-4ce2-9b27-840da5107bce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d0b7c691e1ba6a8445af56978b43a2ccbf33e7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "105714321"
---
# <a name="using-iconnectionpointcontainer"></a>Usar IConnectionPointContainer

Un objeto conectable implementa [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) (y lo expone a través de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))) para indicar la existencia de interfaces de salida. Para cada interfaz de salida, el objeto conectable administra un subobjeto de punto de conexión, que a su vez implementa [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint). Por lo tanto, el objeto conectable contiene los puntos de conexión, de ahí el nombre de **IConnectionPointContainer** e **IConnectionPoint**.

Mediante [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer), un cliente puede realizar dos operaciones. En primer lugar, si el cliente ya tiene el IID para una interfaz de salida que admite, puede localizar el punto de conexión correspondiente para el IID mediante [**IConnectionPointContainer:: FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint). El cliente no puede consultar el punto de conexión directamente debido a la relación contenedor/contenido entre el objeto conectable y sus puntos de conexión contenidos. Básicamente, **FindConnectionPoint** es el [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para las interfaces de salida cuando el cliente conoce el IID.

En segundo lugar, el cliente puede enumerar todos los puntos de conexión dentro del objeto conectable a través de [**IConnectionPointContainer:: EnumConnectionPoints**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints). Este método devuelve un puntero de interfaz [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) para un objeto de enumerador independiente. Mediante [**IEnumConnectionPoints:: Next**](/windows/desktop/api/ocidl/nf-ocidl-ienumconnectionpoints-next), el cliente puede obtener punteros de interfaz [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) a cada punto de conexión.

Una vez que el cliente obtiene la interfaz [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) , debe llamar a [**IConnectionPoint:: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) para determinar el IID de la interfaz de salida compatible con cada punto de conexión. Si el cliente ya es compatible con esa interfaz de salida, puede establecer una conexión. De lo contrario, puede que aún sea capaz de admitir la interfaz de salida mediante la información de la biblioteca de tipos del objeto conectable para proporcionar compatibilidad en tiempo de ejecución. Esta técnica requiere que el objeto conectable admita la interfaz [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) . (Consulte [uso de IProvideClassInfo](using-iprovideclassinfo.md)).

Dado que el enumerador es un objeto independiente, el cliente debe llamar a **IEnumConnectionPoints:: Release** cuando el enumerador ya no se necesita. Además, cada punto de conexión es un objeto con un recuento de referencias independiente del objeto que se va a conectar. Por lo tanto, el cliente también debe llamar a IConnectionPoint:: release para cada punto de conexión al que se tiene acceso mediante el enumerador o a través de [**FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces de objeto conectables](connectable-object-interfaces.md)
</dt> </dl>

 

 




