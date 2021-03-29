---
title: Monikers de puntero
description: Un moniker de puntero identifica un objeto que solo puede existir en el estado activo o en ejecución. Esto difiere de otras clases de monikers, que identifican los objetos que pueden existir en el estado pasivo o activo.
ms.assetid: 9895f03d-7110-41c1-a934-87010f9ad380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebebfce908571b69a5b8ce05f589a4ca4b30977
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "104420138"
---
# <a name="pointer-monikers"></a>Monikers de puntero

Un *moniker de puntero* identifica un objeto que solo puede existir en el estado activo o en ejecución. Esto difiere de otras clases de monikers, que identifican los objetos que pueden existir en el estado pasivo o activo.

Supongamos, por ejemplo, que una aplicación tiene un objeto que no tiene ninguna representación persistente. Normalmente, si un cliente de la aplicación necesita tener acceso a ese objeto, podría simplemente pasar al cliente un puntero al objeto. Sin embargo, suponga que el cliente espera un moniker. No se puede identificar el objeto con un moniker de archivo porque no está almacenado en un archivo ni con un moniker de elemento, porque no está incluido en otro objeto.

En su lugar, la aplicación puede crear un moniker de puntero, que es un moniker que simplemente contiene un puntero internamente, y pasarlo al cliente. El cliente puede tratar este moniker como cualquier otro. Sin embargo, cuando el cliente llama a [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) en el moniker de puntero, el código de moniker no comprueba la tabla de objetos en ejecución (Rot) ni carga nada desde el almacenamiento. En su lugar, el código de moniker simplemente llama a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero almacenado dentro del moniker.

Los monikers de puntero permiten que los objetos que solo existen en el estado activo o en ejecución participen en las operaciones de moniker y que los clientes moniker lo utilicen. Una diferencia importante entre los monikers de puntero y otras clases de monikers es que los monikers de puntero no se pueden guardar en el almacenamiento persistente. Si lo hace, al llamar al método [**IMoniker:: Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) se devuelve un error. Esto significa que los monikers de puntero solo son útiles en situaciones especializadas. Puede usar la función [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) si necesita utilizar un moniker de puntero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Anti-monikers](anti-monikers.md)
</dt> <dt>

[Monikers de clase](class-monikers.md)
</dt> <dt>

[Monikers compuestos](composite-monikers.md)
</dt> <dt>

[Monikers de archivo](file-monikers.md)
</dt> <dt>

[Monikers de elemento](item-monikers.md)
</dt> </dl>

 

 




