---
title: Proveedores de moniker
description: Proveedores de moniker
ms.assetid: 4d4820d2-bf5f-4543-b318-59481dcc51de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde584e12daddacbc940b23b21a0386aa37de2c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775888"
---
# <a name="moniker-providers"></a>Proveedores de moniker

En general, un componente debe ser un proveedor de monikers cuando permite el acceso a uno de sus objetos mientras se controla el almacenamiento del objeto. Si un componente va a entregar monikers que identifican sus objetos, debe ser capaz de realizar las tareas siguientes:

-   En solicitud, cree un moniker que identifique un objeto.
-   Permite que el moniker se enlace cuando un cliente llama a [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) en él.

Un proveedor de moniker debe crear un moniker de una *clase de moniker* adecuada para identificar un objeto. La clase moniker hace referencia a una implementación específica de la interfaz [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) que define el tipo de moniker creado. Aunque puede implementar **IMoniker** para crear una nueva clase de moniker, a menudo no es necesario porque OLE proporciona implementaciones de varias clases de moniker diferentes, cada una con su propio CLSID. Vea [implementaciones de moniker OLE](ole-moniker-implementations.md) para obtener descripciones de las clases moniker que OLE proporciona.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clientes moniker](moniker-clients.md)
</dt> <dt>

[Implementaciones de moniker OLE](ole-moniker-implementations.md)
</dt> </dl>

 

 




