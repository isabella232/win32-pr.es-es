---
title: Monikers
description: Un moniker en COM no es solo una manera de identificar un objeto \ 8212; un moniker también se implementa como un objeto .
ms.assetid: ae0cd2f3-8ac0-4388-8781-e86fc4a26b3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce557fe06ee6f4f5ce2ee08093c93934c9d060b8d4bc24e318a815ad6f95a4a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730955"
---
# <a name="monikers"></a>Monikers

Un moniker en COM no es solo una manera de identificar un objeto: un moniker también se implementa como un objeto . Este objeto proporciona servicios que permiten a un componente obtener un puntero al objeto identificado por el moniker. Este proceso se conoce como *enlace*.

Los monikers son objetos que implementan la [**interfaz IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) y, por lo general, se implementan en archivos DLL como objetos de componente. Hay dos maneras de ver el uso de monikers: como un cliente de moniker, un componente que usa un moniker para obtener un puntero a otro objeto; y como proveedor de moniker, un componente que proporciona monikers que identifican sus objetos a los clientes de moniker.

OLE usa monikers para conectarse a objetos y activarlos, ya sea en la misma máquina o a través de una red. Un uso muy importante es para las conexiones de red. También se usan para identificar, conectarse y ejecutar objetos de vínculo de documento compuesto OLE. En este caso, el origen del vínculo actúa como proveedor de moniker y el contenedor que contiene el objeto de vínculo actúa como el cliente de moniker.

Para obtener más información, vea los temas siguientes:

-   [Clientes de Moniker](moniker-clients.md)
-   [Proveedores de moniker](moniker-providers.md)
-   [Implementaciones de Moniker OLE](ole-moniker-implementations.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[The Component Object Model](the-component-object-model.md) [Modelo de objetos componentes (COM)]
</dt> </dl>

 

 




