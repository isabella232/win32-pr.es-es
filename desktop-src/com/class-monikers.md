---
title: Monikers de clase
description: Aunque las clases normalmente se identifican directamente con CLID para funciones como CoCreateInstance o CoGetClassObject, las clases también se pueden identificar ahora con un moniker denominado moniker de clase.
ms.assetid: 63f5d256-cb61-4673-b5d6-da5c1d89dfa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80886ce49ea25d2fb5acbf4dddf550c9d2c3ae29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574112"
---
# <a name="class-monikers"></a>Monikers de clase

Aunque las clases normalmente se identifican directamente con CLID para funciones como [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoGetClassObject,**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)las clases también se pueden identificar ahora con un moniker denominado *moniker* de clase . Los monikers de clase se enlazan al objeto de clase de la clase para la que se crean.

La capacidad de identificar clases con un moniker admite operaciones útiles que, de lo contrario, no son difíciles de controlar. Por ejemplo, los monikers de archivos admiten tradicionalmente el enlace enriquecido solo a la clase asociada a la clase de archivo a la que hacen referencia. un moniker a un archivo Excel se enlazaría a una instancia de un objeto Excel y un moniker a una imagen GIF se enlazaría a una instancia del controlador GIF registrado actualmente. Un moniker de clase le permite indicar la clase que desea usar para manipular un archivo a través de la composición con un moniker de archivo. Un moniker de clase para una clase de gráficos 3D compuesta con un moniker a un archivo Excel produce un moniker que se enlaza a una instancia del objeto de gráfico 3D e inicializa el objeto con el contenido del archivo Excel.

Por lo tanto, los monikers de clase son más útiles en la composición con otros tipos de monikers, como monikers de archivo o monikers de elementos.

Los monikers de clase también se pueden componer a la derecha de monikers que admiten el enlace a la [**interfaz IClassActivator.**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) Cuando se compone de esta manera, **IClassActivator** simplemente proporciona acceso al objeto de clase y a las instancias de la clase a través de [**IClassActivator::GetClassObject**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject). Los monikers de clase se pueden identificar a través de [**IMoniker::IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker), que devuelve MKSYS \_ CLASSMONIKER en *pdwMksys*.

Los programadores suelen crear monikers de clase mediante [**la función CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) o [**mediante MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname). (Vea [**IMoniker::P arseDisplayName para**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) obtener más información).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Anti monikers](anti-monikers.md)
</dt> <dt>

[Monikers compuestos](composite-monikers.md)
</dt> <dt>

[Monikers de archivo](file-monikers.md)
</dt> <dt>

[Monikers de elementos](item-monikers.md)
</dt> <dt>

[Pointer Monikers](pointer-monikers.md)
</dt> </dl>

 

 




