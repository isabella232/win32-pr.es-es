---
title: Monikers de clase
description: Aunque las clases se identifican normalmente directamente con CLSID en funciones como CoCreateInstance o CoGetClassObject, las clases también pueden identificarse con un moniker denominado moniker de clase.
ms.assetid: 63f5d256-cb61-4673-b5d6-da5c1d89dfa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80886ce49ea25d2fb5acbf4dddf550c9d2c3ae29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357652"
---
# <a name="class-monikers"></a>Monikers de clase

Aunque las clases se identifican normalmente directamente con CLSID en funciones como [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), las clases también pueden identificarse con un moniker denominado *moniker de clase*. Los monikers de clase se enlazan al objeto de clase de la clase para la que se crean.

La capacidad de identificar clases con un moniker admite operaciones útiles que, de lo contrario, son difíciles de manejar. Por ejemplo, los monikers de archivo tradicionalmente admitía el enlace enriquecido solo a la clase asociada a la clase de archivo a la que hacía referencia; un moniker a un archivo de Excel se enlazaría a una instancia de un objeto de Excel y un moniker a una imagen GIF se enlazaría a una instancia del controlador GIF registrado actualmente. Un moniker de clase le permite indicar la clase que desea utilizar para manipular un archivo a través de la composición con un moniker de archivo. Un moniker de clase para una clase de gráficos 3D compuesto con un moniker para un archivo de Excel produce un moniker que se enlaza a una instancia del objeto de gráfico 3D e inicializa el objeto con el contenido del archivo de Excel.

Por lo tanto, los monikers de clase son más útiles en la composición con otros tipos de monikers, como monikers de archivo o monikers de elemento.

Los monikers de clase también se pueden componer a la derecha de monikers que admiten enlaces a la interfaz [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) . Cuando se componen de esta manera, **IClassActivator** simplemente proporciona acceso al objeto de clase y a las instancias de la clase a través de [**IClassActivator:: getclassobject (**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject). Los monikers de clase se pueden identificar mediante [**IMoniker:: IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker), que devuelve MKSYS \_ CLASSMONIKER en *pdwMksys*.

Normalmente, los programadores crean monikers de clase mediante la función [**CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) o a través de [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname). (Consulte [**IMoniker::P arsedisplayname**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) para obtener más información).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Anti-monikers](anti-monikers.md)
</dt> <dt>

[Monikers compuestos](composite-monikers.md)
</dt> <dt>

[Monikers de archivo](file-monikers.md)
</dt> <dt>

[Monikers de elemento](item-monikers.md)
</dt> <dt>

[Monikers de puntero](pointer-monikers.md)
</dt> </dl>

 

 




