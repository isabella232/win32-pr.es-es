---
title: Monikers
description: Un moniker en COM no es solo una manera de identificar un objeto \ 8212; un moniker también se implementa como un objeto.
ms.assetid: ae0cd2f3-8ac0-4388-8781-e86fc4a26b3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf148d63611b5252eec9f5f5f69eacbcece8c65f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075155"
---
# <a name="monikers"></a><span data-ttu-id="4f05a-103">Monikers</span><span class="sxs-lookup"><span data-stu-id="4f05a-103">Monikers</span></span>

<span data-ttu-id="4f05a-104">Un moniker en COM no es solo una forma de identificar un objeto: un moniker también se implementa como un objeto.</span><span class="sxs-lookup"><span data-stu-id="4f05a-104">A moniker in COM is not only a way to identify an object—a moniker is also implemented as an object.</span></span> <span data-ttu-id="4f05a-105">Este objeto proporciona servicios que permiten a un componente obtener un puntero al objeto identificado por el moniker.</span><span class="sxs-lookup"><span data-stu-id="4f05a-105">This object provides services allowing a component to obtain a pointer to the object identified by the moniker.</span></span> <span data-ttu-id="4f05a-106">Este proceso se conoce como *enlace*.</span><span class="sxs-lookup"><span data-stu-id="4f05a-106">This process is referred to as *binding*.</span></span>

<span data-ttu-id="4f05a-107">Los monikers son objetos que implementan la interfaz [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) y que normalmente se implementan en archivos dll como objetos de componente.</span><span class="sxs-lookup"><span data-stu-id="4f05a-107">Monikers are objects that implement the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface and are generally implemented in DLLs as component objects.</span></span> <span data-ttu-id="4f05a-108">Hay dos maneras de ver el uso de monikers: como un cliente de moniker, un componente que utiliza un moniker para obtener un puntero a otro objeto. y como proveedor de moniker, componente que proporciona monikers que identifican sus objetos a los clientes moniker.</span><span class="sxs-lookup"><span data-stu-id="4f05a-108">There are two ways of viewing the use of monikers: as a moniker client, a component that uses a moniker to get a pointer to another object; and as a moniker provider, a component that supplies monikers identifying its objects to moniker clients.</span></span>

<span data-ttu-id="4f05a-109">OLE usa monikers para conectarse a objetos y activarlos, tanto si están en el mismo equipo como en una red.</span><span class="sxs-lookup"><span data-stu-id="4f05a-109">OLE uses monikers to connect to and activate objects, whether they are in the same machine or across a network.</span></span> <span data-ttu-id="4f05a-110">Un uso muy importante es para las conexiones de red.</span><span class="sxs-lookup"><span data-stu-id="4f05a-110">A very important use is for network connections.</span></span> <span data-ttu-id="4f05a-111">También se usan para identificar, conectar y ejecutar objetos de vínculo de documento compuesto OLE.</span><span class="sxs-lookup"><span data-stu-id="4f05a-111">They are also used to identify, connect to, and run OLE compound document link objects.</span></span> <span data-ttu-id="4f05a-112">En este caso, el origen del vínculo actúa como el proveedor de moniker y el contenedor que contiene el objeto de vínculo actúa como el cliente de moniker.</span><span class="sxs-lookup"><span data-stu-id="4f05a-112">In this case, the link source acts as the moniker provider and the container holding the link object acts as the moniker client.</span></span>

<span data-ttu-id="4f05a-113">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="4f05a-113">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="4f05a-114">Clientes moniker</span><span class="sxs-lookup"><span data-stu-id="4f05a-114">Moniker Clients</span></span>](moniker-clients.md)
-   [<span data-ttu-id="4f05a-115">Proveedores de moniker</span><span class="sxs-lookup"><span data-stu-id="4f05a-115">Moniker Providers</span></span>](moniker-providers.md)
-   [<span data-ttu-id="4f05a-116">Implementaciones de moniker OLE</span><span class="sxs-lookup"><span data-stu-id="4f05a-116">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)

## <a name="related-topics"></a><span data-ttu-id="4f05a-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4f05a-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4f05a-118">[The Component Object Model](the-component-object-model.md) [Modelo de objetos componentes (COM)]</span><span class="sxs-lookup"><span data-stu-id="4f05a-118">[The Component Object Model](the-component-object-model.md)</span></span>
</dt> </dl>

 

 




