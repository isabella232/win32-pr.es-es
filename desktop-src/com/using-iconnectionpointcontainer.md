---
title: Uso de IConnectionPointContainer
description: Uso de IConnectionPointContainer
ms.assetid: a87afb25-4d45-4ce2-9b27-840da5107bce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d0b7c691e1ba6a8445af56978b43a2ccbf33e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973595"
---
# <a name="using-iconnectionpointcontainer"></a>Uso de IConnectionPointContainer

Un objeto conectable implementa [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) (y lo expone a través de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))) para indicar la existencia de interfaces salientes. Para cada interfaz saliente, el objeto conectable administra un subelemento de punto de conexión, que a su vez implementa [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint). Por lo tanto, el objeto conectable contiene los puntos de conexión, de ahí el nombre **de IConnectionPointContainer** e **IConnectionPoint**.

A [**través de IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer), un cliente puede realizar dos operaciones. En primer lugar, si el cliente ya tiene el IID de una interfaz saliente que admite, puede buscar el punto de conexión correspondiente para el IID mediante [**IConnectionPointContainer::FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint). El cliente no puede consultar el punto de conexión directamente debido a la relación contenedor/independiente entre el objeto conectable y sus puntos de conexión contenidos. Básicamente, **FindConnectionPoint es** [**queryinterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para las interfaces salientes cuando el cliente conoce el IID.

En segundo lugar, el cliente puede enumerar todos los puntos de conexión dentro del objeto conectable a través [**de IConnectionPointContainer::EnumConnectionPoints**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints). Este método devuelve un puntero [**de interfaz IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) para un objeto enumerador independiente. A [**través de IEnumConnectionPoints::Next**](/windows/desktop/api/ocidl/nf-ocidl-ienumconnectionpoints-next), el cliente puede obtener punteros de interfaz [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) a cada punto de conexión.

Una vez que el cliente obtiene la [**interfaz IConnectionPoint,**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) debe llamar a [**IConnectionPoint::GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) para determinar el IID de la interfaz saliente admitida por cada punto de conexión. Si el cliente ya admite esa interfaz saliente, puede establecer una conexión. De lo contrario, puede seguir siendo capaz de admitir la interfaz saliente mediante la información de la biblioteca de tipos del objeto conectable para proporcionar compatibilidad en tiempo de ejecución. Esta técnica requiere que el objeto conectable admita la [**interfaz IProvideClassInfo.**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) (Vea [Uso de IProvideClassInfo).](using-iprovideclassinfo.md)

Dado que el enumerador es un objeto independiente, el cliente debe llamar a **IEnumConnectionPoints::Release** cuando el enumerador ya no sea necesario. Además, cada punto de conexión es un objeto con un recuento de referencias independiente del objeto conectable que lo contiene. Por lo tanto, el cliente también debe llamar a IConnectionPoint::Release para cada punto de conexión al que se accede a través del enumerador o a través [**de FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces de objetos conectables](connectable-object-interfaces.md)
</dt> </dl>

 

 




