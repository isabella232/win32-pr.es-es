---
title: Uso de IConnectionPoint
description: Uso de IConnectionPoint
ms.assetid: afd50b84-1fd6-47ad-a3ef-e8b4a725b72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7aa758ec1bd40233b1cc41a6c375ed296fc167
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369812"
---
# <a name="using-iconnectionpoint"></a>Uso de IConnectionPoint

Cuando el cliente tiene un puntero a un punto de conexión, puede realizar las siguientes operaciones como se expresa a través [**de IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint):

-   En primer lugar, [**IConnectionPoint::GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) recupera el IID de interfaz saliente admitido por el punto de conexión. Cuando se usa junto con [**IEnumConnectionPoints,**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints)este método permite al cliente examinar los IID de todas las interfaces salientes admitidas en el objeto conectable.
-   En segundo lugar, un cliente puede navegar desde el punto de conexión hasta la interfaz [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) del objeto conectable a través del método [**IConnectionPoint::GetConnectionPointContainer.**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectionpointcontainer)
-   En tercer lugar, los métodos más interesantes para el cliente son [**IConnectionPoint::Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) e [**IConnectionPoint::Unadvise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise). Cuando un cliente desea conectar su propio objeto receptor al objeto conectable, el cliente pasa el puntero [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) del receptor (o cualquier otro puntero de interfaz en el mismo objeto) a **Advise**. El punto de conexión consulta al receptor para la interfaz de salida específica que se espera. Si esa interfaz está disponible en el receptor, el punto de conexión almacena el puntero de interfaz. Desde este punto hasta **que se llama a Unadvise,** el objeto conectable realizará llamadas al receptor a través de esta interfaz cuando se produzcan eventos. Para desconectar el receptor del punto de conexión, el cliente pasa una clave devuelta desde **Advise** al **método Unadvise.** **Unadvise debe** llamar a [**Release en**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) la interfaz del receptor.
-   Por último, un cliente puede pedir a un punto de conexión que enumere todas las conexiones que existen a través de [**IConnectionPoint::EnumConnections**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-enumconnections). Este método crea un objeto enumerador (con un recuento de referencias independiente) que devuelve un [**puntero IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) a él. El cliente debe llamar [**a Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) cuando el enumerador ya no sea necesario. Además, el enumerador devuelve una serie de estructuras [**CONNECTDATA,**](/windows/win32/api/ocidl/ns-ocidl-connectdata) una para cada conexión. Cada estructura describe una conexión mediante el puntero [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) del receptor, así como la clave de conexión devuelta originalmente desde [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise). Cuando haya terminado con estos punteros de interfaz de receptor, el cliente debe llamar a **Release** en cada puntero devuelto en una **estructura CONNECTDATA.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces de objetos conectables](connectable-object-interfaces.md)
</dt> </dl>

 

 