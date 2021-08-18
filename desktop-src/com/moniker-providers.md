---
title: Proveedores de Moniker
description: Proveedores de Moniker
ms.assetid: 4d4820d2-bf5f-4543-b318-59481dcc51de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8fab6c5a84d7020b8bcb02979471cb2fbd76df7e66fc9909eec2121926827df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130107"
---
# <a name="moniker-providers"></a>Proveedores de Moniker

En general, un componente debe ser un proveedor de moniker cuando permite el acceso a uno de sus objetos, mientras sigue controlando el almacenamiento del objeto. Si un componente va a entregar monikers que identifican sus objetos, debe ser capaz de realizar las siguientes tareas:

-   A petición, cree un moniker que identifique un objeto .
-   Habilite el moniker para enlazarlo cuando un cliente llame a [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) en él.

Un proveedor de moniker debe crear un moniker de una clase *de moniker adecuada* para identificar un objeto. La clase moniker hace referencia a una implementación específica de la [**interfaz IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) que define el tipo de moniker creado. Aunque puede implementar **IMoniker** para crear una nueva clase de moniker, con frecuencia no es necesario porque OLE proporciona implementaciones de varias clases de moniker diferentes, cada una con su propio CLSID. Vea [Implementaciones de Moniker OLE](ole-moniker-implementations.md) para obtener descripciones de las clases de moniker que proporciona OLE.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clientes de Moniker](moniker-clients.md)
</dt> <dt>

[Implementaciones de Moniker OLE](ole-moniker-implementations.md)
</dt> </dl>

 

 




