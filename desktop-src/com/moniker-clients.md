---
title: Clientes moniker
description: Los clientes moniker deben empezar por obtener un moniker y hay varias maneras de que un cliente de moniker obtenga un moniker.
ms.assetid: ab1758c4-8dfc-47f6-8e1b-875e033a54d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8435389539f39d8ce71246267cd265c3e4edb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685472"
---
# <a name="moniker-clients"></a><span data-ttu-id="0ec0b-103">Clientes moniker</span><span class="sxs-lookup"><span data-stu-id="0ec0b-103">Moniker Clients</span></span>

<span data-ttu-id="0ec0b-104">Los clientes moniker deben empezar por obtener un moniker y hay varias maneras de que un cliente de moniker obtenga un moniker.</span><span class="sxs-lookup"><span data-stu-id="0ec0b-104">Moniker clients must start by getting a moniker, and there are several ways for a moniker client to get a moniker.</span></span> <span data-ttu-id="0ec0b-105">Por ejemplo, en los documentos compuestos OLE, cuando el usuario final crea un elemento vinculado (mediante el cuadro de diálogo **Insertar objeto** , el portapapeles o arrastrar y colocar), un moniker se incrusta como parte del elemento vinculado.</span><span class="sxs-lookup"><span data-stu-id="0ec0b-105">For example, in OLE compound documents, when the end user creates a linked item (either using **Insert Object** dialog, the clipboard, or drag-and drop), a moniker is embedded as part of the linked item.</span></span> <span data-ttu-id="0ec0b-106">En ese caso, el programador tiene un contacto mínimo con monikers.</span><span class="sxs-lookup"><span data-stu-id="0ec0b-106">In that case, the programmer has minimal contact with monikers.</span></span> <span data-ttu-id="0ec0b-107">Mediante programación, si tiene un puntero de interfaz a un objeto que implementa la interfaz [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) , puede utilizarlo para obtener un moniker y hay métodos en otras interfaces que se definen para devolver monikers.</span><span class="sxs-lookup"><span data-stu-id="0ec0b-107">Programmatically, if you have an interface pointer to an object that implements the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface, you can use that to get a moniker, and there are methods on other interfaces that are defined to return monikers.</span></span>

<span data-ttu-id="0ec0b-108">Hay diferentes tipos de monikers, que se usan para identificar diferentes tipos de objetos, pero en un cliente de moniker, todos los monikers tienen el mismo aspecto.</span><span class="sxs-lookup"><span data-stu-id="0ec0b-108">There are different kinds of monikers, which are used to identify different kinds of objects, but to a moniker client, all monikers look the same.</span></span> <span data-ttu-id="0ec0b-109">Un cliente de moniker simplemente llama a [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) en un moniker y obtiene un puntero de interfaz al objeto que identifica el moniker.</span><span class="sxs-lookup"><span data-stu-id="0ec0b-109">A moniker client simply calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on a moniker and gets an interface pointer to the object that the moniker identifies.</span></span> <span data-ttu-id="0ec0b-110">Si el moniker identifica un objeto tan grande como una hoja de cálculo completa o tan pequeño como una sola celda de una hoja de cálculo, al llamar a **BindToObject** se devolverá un puntero a ese objeto.</span><span class="sxs-lookup"><span data-stu-id="0ec0b-110">Whether the moniker identifies an object as large as an entire spreadsheet or as small as a single cell within a spreadsheet, calling **BindToObject** will return a pointer to that object.</span></span> <span data-ttu-id="0ec0b-111">Si el objeto ya se está ejecutando, **BindToObject** lo encontrará en la memoria.</span><span class="sxs-lookup"><span data-stu-id="0ec0b-111">If the object is already running, **BindToObject** will find it in memory.</span></span> <span data-ttu-id="0ec0b-112">Si el objeto se almacena de forma pasiva en el disco, **BindToObject** buscará un servidor para ese objeto, ejecutará el servidor y hará que el objeto ponga el objeto en el estado en ejecución.</span><span class="sxs-lookup"><span data-stu-id="0ec0b-112">If the object is stored passively on disk, **BindToObject** will locate a server for that object, run the server, and have the server bring the object into the running state.</span></span> <span data-ttu-id="0ec0b-113">Todos los detalles del proceso de enlace están ocultos en el cliente de moniker.</span><span class="sxs-lookup"><span data-stu-id="0ec0b-113">All the details of the binding process are hidden from the moniker client.</span></span> <span data-ttu-id="0ec0b-114">Por lo tanto, para un cliente de moniker, el uso del moniker es muy sencillo.</span><span class="sxs-lookup"><span data-stu-id="0ec0b-114">Thus, for a moniker client, using the moniker is very simple.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ec0b-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0ec0b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ec0b-116">Proveedores de moniker</span><span class="sxs-lookup"><span data-stu-id="0ec0b-116">Moniker Providers</span></span>](moniker-providers.md)
</dt> <dt>

[<span data-ttu-id="0ec0b-117">Implementaciones de moniker OLE</span><span class="sxs-lookup"><span data-stu-id="0ec0b-117">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)
</dt> </dl>

 

 




