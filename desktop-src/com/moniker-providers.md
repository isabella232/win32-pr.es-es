---
title: Proveedores de moniker
description: Proveedores de moniker
ms.assetid: 4d4820d2-bf5f-4543-b318-59481dcc51de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde584e12daddacbc940b23b21a0386aa37de2c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775888"
---
# <a name="moniker-providers"></a><span data-ttu-id="f3657-103">Proveedores de moniker</span><span class="sxs-lookup"><span data-stu-id="f3657-103">Moniker Providers</span></span>

<span data-ttu-id="f3657-104">En general, un componente debe ser un proveedor de monikers cuando permite el acceso a uno de sus objetos mientras se controla el almacenamiento del objeto.</span><span class="sxs-lookup"><span data-stu-id="f3657-104">In general, a component should be a moniker provider when it allows access to one of its objects, while still controlling the object's storage.</span></span> <span data-ttu-id="f3657-105">Si un componente va a entregar monikers que identifican sus objetos, debe ser capaz de realizar las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="f3657-105">If a component is going to hand out monikers that identify its objects, it must be capable of performing the following tasks:</span></span>

-   <span data-ttu-id="f3657-106">En solicitud, cree un moniker que identifique un objeto.</span><span class="sxs-lookup"><span data-stu-id="f3657-106">On request, create a moniker that identifies an object.</span></span>
-   <span data-ttu-id="f3657-107">Permite que el moniker se enlace cuando un cliente llama a [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) en él.</span><span class="sxs-lookup"><span data-stu-id="f3657-107">Enable the moniker to be bound when a client calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on it.</span></span>

<span data-ttu-id="f3657-108">Un proveedor de moniker debe crear un moniker de una *clase de moniker* adecuada para identificar un objeto.</span><span class="sxs-lookup"><span data-stu-id="f3657-108">A moniker provider must create a moniker of an appropriate *moniker class* to identify an object.</span></span> <span data-ttu-id="f3657-109">La clase moniker hace referencia a una implementación específica de la interfaz [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) que define el tipo de moniker creado.</span><span class="sxs-lookup"><span data-stu-id="f3657-109">The moniker class refers to a specific implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface that defines the type of moniker created.</span></span> <span data-ttu-id="f3657-110">Aunque puede implementar **IMoniker** para crear una nueva clase de moniker, a menudo no es necesario porque OLE proporciona implementaciones de varias clases de moniker diferentes, cada una con su propio CLSID.</span><span class="sxs-lookup"><span data-stu-id="f3657-110">While you can implement **IMoniker** to create a new moniker class, it is frequently unnecessary because OLE provides implementations of several different moniker classes, each with its own CLSID.</span></span> <span data-ttu-id="f3657-111">Vea [implementaciones de moniker OLE](ole-moniker-implementations.md) para obtener descripciones de las clases moniker que OLE proporciona.</span><span class="sxs-lookup"><span data-stu-id="f3657-111">See [OLE Moniker Implementations](ole-moniker-implementations.md) for descriptions of moniker classes that OLE provides.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3657-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3657-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3657-113">Clientes moniker</span><span class="sxs-lookup"><span data-stu-id="f3657-113">Moniker Clients</span></span>](moniker-clients.md)
</dt> <dt>

[<span data-ttu-id="f3657-114">Implementaciones de moniker OLE</span><span class="sxs-lookup"><span data-stu-id="f3657-114">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)
</dt> </dl>

 

 




