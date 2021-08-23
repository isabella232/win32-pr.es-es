---
title: Inicialización de objetos persistentes
description: Inicialización de objetos persistentes
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee98b01c6c9eab28f8f96f98ea1a2980c9eb5d10988c2efbe495a920c98c51e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756185"
---
# <a name="initializing-persistent-objects"></a>Inicialización de objetos persistentes

Varias de las interfaces de objetos persistentes, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory e](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)) [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), permiten a los clientes inicializar objetos en un estado "nuevo" o "predeterminado". Este estado inicial es diferente del de un objeto recién creado, que no tiene ningún estado.

Inicializar el estado de un objeto, incluso en el estado predeterminado, puede ser una operación de proceso intensivo o de uso intensivo de recursos. Al separar la creación de la inicialización, la inicialización solo se puede realizar cuando realmente es necesaria y los clientes pueden evitar inicializar objetos en el estado predeterminado solo para cargar inmediatamente los datos almacenados previamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces de objetos persistentes](persistent-object-interfaces.md)
</dt> </dl>

 

 