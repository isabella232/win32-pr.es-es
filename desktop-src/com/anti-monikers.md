---
title: Anti-monikers
description: OLE proporciona una implementación de un tipo especial de moniker denominado anti-moniker.
ms.assetid: 3b52d3bd-8375-4463-a0e3-5117fa96a1c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d69c461268b486a040b36f59108bc8e8379656
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075861"
---
# <a name="anti-monikers"></a>Anti-monikers

OLE proporciona una implementación de un tipo especial de moniker denominado *anti-moniker*. Este moniker se usa en la creación de nuevas clases moniker. Se usa como el inverso del moniker en el que se compone y, de hecho, se cancela el moniker de la misma manera que el operador ".." sube un nivel de directorio en un comando del sistema de archivos.

Es necesario tener un anti-moniker disponible, ya que una vez creado un moniker compuesto, no es posible eliminar partes del moniker si, por ejemplo, se mueve un objeto. En su lugar, se usa un anti-moniker para quitar una o varias entradas de un moniker compuesto.

Los anti-monikers son una clase de moniker diseñada explícitamente para su uso como inversa. COM define la función [**CreateAntiMoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) con nombre, que devuelve un anti-moniker. Normalmente, se usa esta función para implementar el método [**IMoniker:: inverso**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) .

Un anti-moniker es solo un inverso para los tipos de monikers que se implementan para tratar los suavizadores como inversos. Por ejemplo, si desea quitar la última parte de un moniker compuesto, no debe crear un elemento anti-moniker y componerlo al final del compuesto. No puede estar seguro de que la última parte del compuesto considera que un moniker es su inversa. En su lugar, debe llamar a [**IMoniker:: enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) en el moniker compuesto, especificando **false** como primer parámetro. Esto crea un enumerador que devuelve los monikers del componente en orden inverso. Use el enumerador para recuperar la última parte del compuesto y llame a [**inverso**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) en ese moniker. El moniker devuelto por **inverso** es lo que necesita para quitar la última parte del compuesto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Monikers de clase](class-monikers.md)
</dt> <dt>

[Monikers compuestos](composite-monikers.md)
</dt> <dt>

[Monikers de archivo](file-monikers.md)
</dt> <dt>

[Monikers de elemento](item-monikers.md)
</dt> <dt>

[Monikers de puntero](pointer-monikers.md)
</dt> </dl>

 

 




