---
title: Pointer Monikers
description: Un moniker de puntero identifica un objeto que solo puede existir en el estado activo o en ejecución. Esto difiere de otras clases de monikers, que identifican objetos que pueden existir en el estado pasivo o activo.
ms.assetid: 9895f03d-7110-41c1-a934-87010f9ad380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebebfce908571b69a5b8ce05f589a4ca4b30977
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369512"
---
# <a name="pointer-monikers"></a>Pointer Monikers

Un *moniker de puntero* identifica un objeto que solo puede existir en el estado activo o en ejecución. Esto difiere de otras clases de monikers, que identifican objetos que pueden existir en el estado pasivo o activo.

Supongamos, por ejemplo, que una aplicación tiene un objeto que no tiene ninguna representación persistente. Normalmente, si un cliente de la aplicación necesita acceso a ese objeto, simplemente podría pasar al cliente un puntero al objeto . Sin embargo, supongamos que el cliente espera un moniker. El objeto no se puede identificar con un moniker de archivo, porque no está almacenado en un archivo, ni con un moniker de elemento, porque no está contenido en otro objeto.

En su lugar, la aplicación puede crear un moniker de puntero, que es un moniker que simplemente contiene un puntero internamente, y pasarlo al cliente. El cliente puede tratar este moniker como cualquier otro. Sin embargo, cuando el cliente llama a [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) en el moniker de puntero, el código del moniker no comprueba la tabla de objetos en ejecución (ROT) ni carga nada desde el almacenamiento. En su lugar, el código de moniker simplemente llama [**a QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero almacenado dentro del moniker.

Los monikers de puntero permiten a los objetos que solo existen en el estado activo o en ejecución participar en operaciones de moniker y que los clientes de moniker usan. Una diferencia importante entre los monikers de puntero y otras clases de monikers es que los monikers de puntero no se pueden guardar en el almacenamiento persistente. Si lo hace, al llamar al [**método IMoniker::Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) se devuelve un error. Esto significa que los monikers de puntero solo son útiles en situaciones especializadas. Puede usar la [**función CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) si necesita usar un moniker de puntero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Anti monikers](anti-monikers.md)
</dt> <dt>

[Monikers de clase](class-monikers.md)
</dt> <dt>

[Monikers compuestos](composite-monikers.md)
</dt> <dt>

[File Monikers](file-monikers.md)
</dt> <dt>

[Monikers de elementos](item-monikers.md)
</dt> </dl>

 

 




