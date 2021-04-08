---
title: Usar IConnectionPoint
description: Usar IConnectionPoint
ms.assetid: afd50b84-1fd6-47ad-a3ef-e8b4a725b72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7aa758ec1bd40233b1cc41a6c375ed296fc167
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078395"
---
# <a name="using-iconnectionpoint"></a>Usar IConnectionPoint

Cuando el cliente tiene un puntero a un punto de conexión, puede realizar las siguientes operaciones, tal y como se expresa a través de [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint):

-   En primer lugar, [**IConnectionPoint:: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) recupera el IID de la interfaz de salida admitido por el punto de conexión. Cuando se usa junto con [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints), este método permite al cliente examinar los IID de todas las interfaces salientes admitidas en el objeto conectable.
-   En segundo lugar, un cliente puede desplazarse desde el punto de conexión a la interfaz [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) del objeto conectable a través del método [**IConnectionPoint:: GetConnectionPointContainer**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectionpointcontainer) .
-   En tercer lugar, los métodos más interesantes para el cliente son [**IConnectionPoint:: Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) e [**IConnectionPoint:: unvise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise). Cuando un cliente desea conectar su propio objeto receptor al objeto conectable, el cliente pasa el puntero [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) del receptor (o cualquier otro puntero de interfaz en el mismo objeto) para **avisar**. El punto de conexión consulta el receptor para la interfaz de salida específica que se espera. Si esa interfaz está disponible en el receptor, el punto de conexión almacena el puntero de interfaz. Desde este punto hasta que se llame a **unvise** , el objeto conectable realizará llamadas al receptor a través de esta interfaz cuando se produzcan eventos. Para desconectar el receptor del punto de conexión, el cliente pasa una clave devuelta desde **Advise** al método **unvise** . **Unadvise** debe llamar a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en la interfaz de receptor.
-   Por último, un cliente puede pedir a un punto de conexión que enumere todas las conexiones a él que existen a través de [**IConnectionPoint:: EnumConnections**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-enumconnections). Este método crea un objeto de enumerador (con un recuento de referencias independiente) que devuelve un puntero de [**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) a él. El cliente debe llamar a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) cuando el enumerador ya no se necesita. Además, el enumerador devuelve una serie de estructuras [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata) , una para cada conexión. Cada estructura describe una conexión mediante el puntero [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) del receptor, así como la clave de conexión que se devolvió originalmente desde [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise). Cuando se realizan estos punteros de interfaz de receptor, el cliente debe llamar a **Release** en cada puntero devuelto en una estructura **CONNECTDATA** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces de objeto conectables](connectable-object-interfaces.md)
</dt> </dl>

 

 