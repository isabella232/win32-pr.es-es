---
title: Interfaces de objetos persistentes (COM)
description: Un objeto persistente implementa una o varias interfaces de objeto persistentes.
ms.assetid: 8c8e44e4-f564-4af5-9a8a-ac6883862cae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df8920f1242d077044654d1090adcc0e3f3f05c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369795"
---
# <a name="persistent-object-interfaces"></a>Interfaces de objetos persistentes

Un objeto persistente implementa una o varias interfaces *de objeto persistentes*. Los clientes usan interfaces de objetos persistentes para decir a esos objetos cuándo y dónde almacenar su estado. Todas las interfaces de objetos persistentes se derivan de [**IPersist,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersist)por lo que cualquier objeto que implemente cualquier interfaz de objeto persistente también **implementa IPersist**.

Actualmente se definen las siguientes interfaces de objeto persistentes:

-   [**Ipersiststream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)
-   [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)
-   [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)
-   [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)
-   [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))
-   [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))
-   [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))

Los implementadores eligen qué interfaces de objeto persistente admite un objeto en función de cómo se va a usar el objeto. Al no admitir ninguna interfaz de objeto persistente, el implementador dice de forma eficaz: "El estado de este objeto no se puede almacenar de forma persistente". Al admitir una o varias interfaces de objeto persistentes, el implementador dice de forma eficaz: "El estado de este objeto se puede almacenar de forma persistente en uno o varios medios de almacén de datos".

Por ejemplo, en la tabla siguiente se enumeran varios tipos de objeto que permiten la compatibilidad con diferentes interfaces de objetos persistentes.



| Category                            | Interfaces de objetos persistentes admitidas normalmente                                                                                                                                                         |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Monikers<br/>                 | [**Ipersiststream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)<br/>                                                                                                                                                      |
| Objetos insertables ole<br/>   | [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |
| Controles ActiveX<br/>         | [**IPersistStreamInit,**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) [**IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)IPersistMemory, IPersistPropertyBag, [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/> |
| ActiveX objetos de documento<br/> | [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |



 

Los implementadores de cliente también pueden elegir qué interfaces de objeto persistente puede usar el cliente. Las interfaces que usa un cliente normalmente se determinan por dónde el cliente puede almacenar sus propios datos. Un cliente que pueda almacenar sus datos solo en un archivo plano probablemente solo usará [**IPersistStreamInit,**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))e IPersistPropertyBag. (**IPersistStreamInit puede reemplazar** [**IPersistStream en**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) la mayoría de las aplicaciones, porque contiene esa definición y agrega un método de inicialización). Un cliente que pueda guardar sus datos en un archivo de almacenamiento estructurado usará, además, [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Inicialización de objetos persistentes](initializing-persistent-objects.md)
</dt> </dl>

 

