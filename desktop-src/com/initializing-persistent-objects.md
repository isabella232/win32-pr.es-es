---
title: Inicialización de objetos persistentes
description: Inicialización de objetos persistentes
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29bcb32bc049b5e0d5c2dab13e5ded6a743957e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549201"
---
# <a name="initializing-persistent-objects"></a><span data-ttu-id="56c57-103">Inicialización de objetos persistentes</span><span class="sxs-lookup"><span data-stu-id="56c57-103">Initializing Persistent Objects</span></span>

<span data-ttu-id="56c57-104">Varias de las interfaces de objetos persistentes, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory e](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)) [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), permiten a los clientes inicializar objetos en un estado "nuevo" o "predeterminado".</span><span class="sxs-lookup"><span data-stu-id="56c57-104">Several of the persistent object interfaces, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), and [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), allow clients to initialize objects to a "fresh" or "default" state.</span></span> <span data-ttu-id="56c57-105">Este estado inicial es diferente del de un objeto recién creado, que no tiene ningún estado.</span><span class="sxs-lookup"><span data-stu-id="56c57-105">This initial state is different from that of a newly created object, which has no state.</span></span>

<span data-ttu-id="56c57-106">Inicializar el estado de un objeto, incluso en el estado predeterminado, puede ser una operación de proceso intensivo o de uso intensivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="56c57-106">Initializing an object's state, even to the default state, may be a compute-intensive or resource-intensive operation.</span></span> <span data-ttu-id="56c57-107">Al separar la creación de la inicialización, la inicialización solo se puede realizar cuando realmente es necesaria y los clientes pueden evitar inicializar objetos en el estado predeterminado solo para cargar inmediatamente los datos almacenados previamente.</span><span class="sxs-lookup"><span data-stu-id="56c57-107">By separating creation from initialization, the initialization can be performed only when it is actually needed and clients can avoid initializing objects to the default state only to immediately load previously stored data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56c57-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56c57-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56c57-109">Interfaces de objetos persistentes</span><span class="sxs-lookup"><span data-stu-id="56c57-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
</dt> </dl>

 

 