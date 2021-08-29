---
title: Anti monikers
description: OLE proporciona una implementación de un tipo especial de moniker denominado antimoniker.
ms.assetid: 3b52d3bd-8375-4463-a0e3-5117fa96a1c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a0fb6183ff29a223ccf3a51f6f7e10a0a5c7670952354f7c917655e40d16d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071195"
---
# <a name="anti-monikers"></a>Anti monikers

OLE proporciona una implementación de un tipo especial de moniker denominado *antimoniker*. Este moniker se usa en la creación de nuevas clases de moniker. Se usa como el inverso del moniker en el que se compone, cancelando eficazmente ese moniker, de la misma manera que el operador ".." sube un nivel de directorio en un comando del sistema de archivos.

Es necesario tener disponible un antimoniker, ya que una vez creado un moniker compuesto, no es posible eliminar partes del moniker si, por ejemplo, se mueve un objeto. En su lugar, se usa un antimoniker para quitar una o varias entradas de un moniker compuesto.

Los anti monikers son una clase de moniker diseñada explícitamente para su uso como inverso. COM define la [**función CreateAntiMoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) con nombre, que devuelve un antimoniker. Normalmente, esta función se usa para implementar el [**método IMoniker::Inverse.**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse)

Un antimoniker es solo un inverso para los tipos de monikers que se implementan para tratar los anti monikers como inversos. Por ejemplo, si desea quitar la última parte de un moniker compuesto, no debe crear un antimoniker y crearlo al final del compuesto. No puede estar seguro de que la última parte del compuesto considere que un antimoniker es inverso. En su lugar, debe llamar a [**IMoniker::Enum en**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) el moniker compuesto, **especificando FALSE** como primer parámetro. Esto crea un enumerador que devuelve los monikers del componente en orden inverso. Use el enumerador para recuperar el último fragmento del compuesto y llame a [**Inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) en ese moniker. El moniker devuelto por **Inverse** es lo que necesita para quitar la última parte del compuesto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Monikers de clase](class-monikers.md)
</dt> <dt>

[Monikers compuestos](composite-monikers.md)
</dt> <dt>

[Monikers de archivo](file-monikers.md)
</dt> <dt>

[Monikers de elementos](item-monikers.md)
</dt> <dt>

[Monikers de puntero](pointer-monikers.md)
</dt> </dl>

 

 




