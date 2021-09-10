---
title: Interfaces de objetos conectables
description: Interfaces de objetos conectables
ms.assetid: 136fb7bd-7a38-4051-b47b-3d08f1dbee79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc2d747d7aabe25788c34d80bddb8ca1466e9c5
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369807"
---
# <a name="connectable-object-interfaces"></a>Interfaces de objetos conectables

La compatibilidad con objetos conectables requiere compatibilidad con cuatro interfaces:

-   [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) en el objeto conectable
-   [**IConnectionPoint en**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) el objeto de punto de conexión
-   [**IEnumConnectionPoints en**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) un objeto enumerador
-   [**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) en un objeto enumerador

Los dos últimos se definen como enumeradores estándar para los tipos **IConnectionPoint \** _ y [_ *CONNECTDATA* *](/windows/win32/api/ocidl/ns-ocidl-connectdata).

Además, el objeto conectable puede admitir opcionalmente [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) e [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) para proporcionar suficiente información a un cliente para que el cliente pueda proporcionar compatibilidad con la interfaz saliente en tiempo de ejecución.

Por último, el cliente debe proporcionar un objeto receptor que implemente la interfaz saliente, que es una interfaz COM personalizada definida por el objeto conectable.

Para obtener más información, vea los temas siguientes:

-   [Uso de IConnectionPointContainer](using-iconnectionpointcontainer.md)
-   [Uso de IConnectionPoint](using-iconnectionpoint.md)
-   [Uso de IProvideClassInfo](using-iprovideclassinfo.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Arquitectura de objetos conectables](architecture-of-connectable-objects.md)
</dt> </dl>

 

 




