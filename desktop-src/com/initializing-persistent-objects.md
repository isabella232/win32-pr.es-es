---
title: Inicialización de objetos persistentes
description: Inicialización de objetos persistentes
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29bcb32bc049b5e0d5c2dab13e5ded6a743957e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060922"
---
# <a name="initializing-persistent-objects"></a>Inicialización de objetos persistentes

Varias de las interfaces de objetos persistentes, [**IPersistStreamInit,**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) [**IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) [IPersistMemory e](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)) [IPersistPropertyBag,](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)permiten a los clientes inicializar objetos en un estado "nuevo" o "predeterminado". Este estado inicial es diferente del de un objeto recién creado, que no tiene ningún estado.

La inicialización del estado de un objeto, incluso en el estado predeterminado, puede ser una operación de proceso intensivo o de uso intensivo de recursos. Al separar la creación de la inicialización, la inicialización solo se puede realizar cuando realmente es necesaria y los clientes pueden evitar inicializar objetos en el estado predeterminado solo para cargar inmediatamente los datos almacenados previamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces de objetos persistentes](persistent-object-interfaces.md)
</dt> </dl>

 

 