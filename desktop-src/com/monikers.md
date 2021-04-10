---
title: Monikers
description: Un moniker en COM no es solo una manera de identificar un objeto \ 8212; un moniker también se implementa como un objeto.
ms.assetid: ae0cd2f3-8ac0-4388-8781-e86fc4a26b3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf148d63611b5252eec9f5f5f69eacbcece8c65f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075155"
---
# <a name="monikers"></a>Monikers

Un moniker en COM no es solo una forma de identificar un objeto: un moniker también se implementa como un objeto. Este objeto proporciona servicios que permiten a un componente obtener un puntero al objeto identificado por el moniker. Este proceso se conoce como *enlace*.

Los monikers son objetos que implementan la interfaz [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) y que normalmente se implementan en archivos dll como objetos de componente. Hay dos maneras de ver el uso de monikers: como un cliente de moniker, un componente que utiliza un moniker para obtener un puntero a otro objeto. y como proveedor de moniker, componente que proporciona monikers que identifican sus objetos a los clientes moniker.

OLE usa monikers para conectarse a objetos y activarlos, tanto si están en el mismo equipo como en una red. Un uso muy importante es para las conexiones de red. También se usan para identificar, conectar y ejecutar objetos de vínculo de documento compuesto OLE. En este caso, el origen del vínculo actúa como el proveedor de moniker y el contenedor que contiene el objeto de vínculo actúa como el cliente de moniker.

Para obtener más información, vea los temas siguientes:

-   [Clientes moniker](moniker-clients.md)
-   [Proveedores de moniker](moniker-providers.md)
-   [Implementaciones de moniker OLE](ole-moniker-implementations.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[The Component Object Model](the-component-object-model.md) [Modelo de objetos componentes (COM)]
</dt> </dl>

 

 




