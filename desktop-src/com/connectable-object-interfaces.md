---
title: Interfaces de objeto conectables
description: Interfaces de objeto conectables
ms.assetid: 136fb7bd-7a38-4051-b47b-3d08f1dbee79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc2d747d7aabe25788c34d80bddb8ca1466e9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903856"
---
# <a name="connectable-object-interfaces"></a>Interfaces de objeto conectables

La compatibilidad con objetos conectables requiere la compatibilidad con cuatro interfaces:

-   [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) en el objeto conectable
-   [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) en el objeto de punto de conexión
-   [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) en un objeto enumerador
-   [**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) en un objeto enumerador

Los dos últimos se definen como enumeradores estándar para los tipos **IConnectionPoint \*** y [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata).

Además, el objeto conectable puede admitir opcionalmente [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) y [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) para proporcionar suficiente información a un cliente para que el cliente pueda proporcionar compatibilidad con la interfaz de salida en tiempo de ejecución.

Por último, el cliente debe proporcionar un objeto de receptor que implementa la interfaz de salida, que es una interfaz COM personalizada definida por el objeto conectable.

Para obtener más información, vea los temas siguientes:

-   [Usar IConnectionPointContainer](using-iconnectionpointcontainer.md)
-   [Usar IConnectionPoint](using-iconnectionpoint.md)
-   [Usar IProvideClassInfo](using-iprovideclassinfo.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Arquitectura de objetos conectables](architecture-of-connectable-objects.md)
</dt> </dl>

 

 




