---
title: Interfaces de objetos persistentes (COM)
description: Un objeto persistente implementa una o más interfaces de objeto persistentes.
ms.assetid: 8c8e44e4-f564-4af5-9a8a-ac6883862cae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df8920f1242d077044654d1090adcc0e3f3f05c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995686"
---
# <a name="persistent-object-interfaces"></a>Interfaces de objeto persistentes

Un objeto persistente implementa una o más *interfaces de objeto persistentes*. Los clientes usan interfaces de objeto persistentes para indicar a esos objetos Cuándo y dónde almacenar su estado. Todas las interfaces de objeto persistentes se derivan de [**IPersist**](/windows/desktop/api/ObjIdl/nn-objidl-ipersist), por lo que cualquier objeto que implemente cualquier interfaz de objeto persistente también implementa **IPersist**.

Las siguientes interfaces de objeto persistentes están definidas actualmente:

-   [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)
-   [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)
-   [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)
-   [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)
-   [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))
-   [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))
-   [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))

Los implementadores eligen qué interfaces de objeto persistentes admite un objeto, en función de cómo se utilice el objeto. Si no se admiten las interfaces de objeto persistentes, el implementador está diciendo realmente: "el estado de este objeto no se puede almacenar de forma persistente". Al admitir una o más interfaces de objeto persistentes, el implementador está diciendo realmente: "el estado de este objeto se puede almacenar de forma persistente en uno o más medios del almacén de datos".

Por ejemplo, en la tabla siguiente se enumeran varios tipos de objetos que permiten la compatibilidad con diferentes interfaces de objetos persistentes.



| Category                            | Interfaces de objeto persistentes admitidas normalmente                                                                                                                                                         |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Monikers<br/>                 | [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)<br/>                                                                                                                                                      |
| Objetos que se van a incrustar OLE<br/>   | [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |
| Controles ActiveX<br/>         | [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), IPersistMemory, IPersistPropertyBag, [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/> |
| Objetos de documento ActiveX<br/> | [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |



 

Los implementadores de cliente también pueden elegir qué interfaces de objeto persistentes puede usar el cliente. Normalmente, las interfaces que utiliza un cliente se determinan por la ubicación en la que el cliente puede almacenar sus propios datos. Un cliente que pueda almacenar sus datos solo en un archivo plano probablemente usará solo [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))y IPersistPropertyBag. (**IPersistStreamInit** puede reemplazar [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) en la mayoría de las aplicaciones, porque contiene esa definición y agrega un método de inicialización). Un cliente que pueda guardar sus datos en un archivo de almacenamiento estructurado, también usará [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Inicializar objetos persistentes](initializing-persistent-objects.md)
</dt> </dl>

 

