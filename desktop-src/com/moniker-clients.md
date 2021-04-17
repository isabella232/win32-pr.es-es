---
title: Clientes moniker
description: Los clientes moniker deben empezar por obtener un moniker y hay varias maneras de que un cliente de moniker obtenga un moniker.
ms.assetid: ab1758c4-8dfc-47f6-8e1b-875e033a54d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8435389539f39d8ce71246267cd265c3e4edb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685472"
---
# <a name="moniker-clients"></a>Clientes moniker

Los clientes moniker deben empezar por obtener un moniker y hay varias maneras de que un cliente de moniker obtenga un moniker. Por ejemplo, en los documentos compuestos OLE, cuando el usuario final crea un elemento vinculado (mediante el cuadro de diálogo **Insertar objeto** , el portapapeles o arrastrar y colocar), un moniker se incrusta como parte del elemento vinculado. En ese caso, el programador tiene un contacto mínimo con monikers. Mediante programación, si tiene un puntero de interfaz a un objeto que implementa la interfaz [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) , puede utilizarlo para obtener un moniker y hay métodos en otras interfaces que se definen para devolver monikers.

Hay diferentes tipos de monikers, que se usan para identificar diferentes tipos de objetos, pero en un cliente de moniker, todos los monikers tienen el mismo aspecto. Un cliente de moniker simplemente llama a [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) en un moniker y obtiene un puntero de interfaz al objeto que identifica el moniker. Si el moniker identifica un objeto tan grande como una hoja de cálculo completa o tan pequeño como una sola celda de una hoja de cálculo, al llamar a **BindToObject** se devolverá un puntero a ese objeto. Si el objeto ya se está ejecutando, **BindToObject** lo encontrará en la memoria. Si el objeto se almacena de forma pasiva en el disco, **BindToObject** buscará un servidor para ese objeto, ejecutará el servidor y hará que el objeto ponga el objeto en el estado en ejecución. Todos los detalles del proceso de enlace están ocultos en el cliente de moniker. Por lo tanto, para un cliente de moniker, el uso del moniker es muy sencillo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedores de moniker](moniker-providers.md)
</dt> <dt>

[Implementaciones de moniker OLE](ole-moniker-implementations.md)
</dt> </dl>

 

 




