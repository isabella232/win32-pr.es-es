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
# <a name="initializing-persistent-objects"></a><span data-ttu-id="9d2ca-103">Inicializar objetos persistentes</span><span class="sxs-lookup"><span data-stu-id="9d2ca-103">Initializing Persistent Objects</span></span>

<span data-ttu-id="9d2ca-104">Varias de las interfaces de objeto persistentes, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))y [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), permiten a los clientes inicializar objetos en un estado "nuevo" o "predeterminado".</span><span class="sxs-lookup"><span data-stu-id="9d2ca-104">Several of the persistent object interfaces, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), and [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), allow clients to initialize objects to a "fresh" or "default" state.</span></span> <span data-ttu-id="9d2ca-105">Este estado inicial es diferente del de un objeto recién creado, que no tiene ningún Estado.</span><span class="sxs-lookup"><span data-stu-id="9d2ca-105">This initial state is different from that of a newly created object, which has no state.</span></span>

<span data-ttu-id="9d2ca-106">Inicializar el estado de un objeto, incluso con el estado predeterminado, puede ser una operación que consume muchos recursos de proceso.</span><span class="sxs-lookup"><span data-stu-id="9d2ca-106">Initializing an object's state, even to the default state, may be a compute-intensive or resource-intensive operation.</span></span> <span data-ttu-id="9d2ca-107">Al separar la creación de la inicialización, la inicialización solo puede realizarse cuando realmente se necesita y los clientes pueden evitar la inicialización de objetos en el estado predeterminado para cargar inmediatamente los datos almacenados previamente.</span><span class="sxs-lookup"><span data-stu-id="9d2ca-107">By separating creation from initialization, the initialization can be performed only when it is actually needed and clients can avoid initializing objects to the default state only to immediately load previously stored data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d2ca-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9d2ca-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d2ca-109">Interfaces de objeto persistentes</span><span class="sxs-lookup"><span data-stu-id="9d2ca-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
</dt> </dl>

 

 