---
title: Inicializar objetos persistentes
description: Inicializar objetos persistentes
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211d9d89b7a8f36ab06d9930e45f365e0fb5d4dc
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421455"
---
# <a name="initializing-persistent-objects"></a>Inicializar objetos persistentes

Varias de las interfaces de objeto persistentes, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))y [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), permiten a los clientes inicializar objetos en un estado "nuevo" o "predeterminado". Este estado inicial es diferente del de un objeto recién creado, que no tiene ningún Estado.

Inicializar el estado de un objeto, incluso con el estado predeterminado, puede ser una operación que consume muchos recursos de proceso. Al separar la creación de la inicialización, la inicialización solo puede realizarse cuando realmente se necesita y los clientes pueden evitar la inicialización de objetos en el estado predeterminado para cargar inmediatamente los datos almacenados previamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces de objeto persistentes](persistent-object-interfaces.md)
</dt> </dl>

 

 