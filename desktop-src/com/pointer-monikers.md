---
title: Monikers de puntero
description: Un moniker de puntero identifica un objeto que solo puede existir en el estado activo o en ejecución. Esto difiere de otras clases de monikers, que identifican los objetos que pueden existir en el estado pasivo o activo.
ms.assetid: 9895f03d-7110-41c1-a934-87010f9ad380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebebfce908571b69a5b8ce05f589a4ca4b30977
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "104420138"
---
# <a name="pointer-monikers"></a><span data-ttu-id="4d969-104">Monikers de puntero</span><span class="sxs-lookup"><span data-stu-id="4d969-104">Pointer Monikers</span></span>

<span data-ttu-id="4d969-105">Un *moniker de puntero* identifica un objeto que solo puede existir en el estado activo o en ejecución.</span><span class="sxs-lookup"><span data-stu-id="4d969-105">A *pointer moniker* identifies an object that can exist only in the active or running state.</span></span> <span data-ttu-id="4d969-106">Esto difiere de otras clases de monikers, que identifican los objetos que pueden existir en el estado pasivo o activo.</span><span class="sxs-lookup"><span data-stu-id="4d969-106">This differs from other classes of monikers, which identify objects that can exist in either the passive or the active state.</span></span>

<span data-ttu-id="4d969-107">Supongamos, por ejemplo, que una aplicación tiene un objeto que no tiene ninguna representación persistente.</span><span class="sxs-lookup"><span data-stu-id="4d969-107">Suppose, for example, an application has an object that has no persistent representation.</span></span> <span data-ttu-id="4d969-108">Normalmente, si un cliente de la aplicación necesita tener acceso a ese objeto, podría simplemente pasar al cliente un puntero al objeto.</span><span class="sxs-lookup"><span data-stu-id="4d969-108">Normally, if a client of your application needs access to that object, you could simply pass the client a pointer to the object.</span></span> <span data-ttu-id="4d969-109">Sin embargo, suponga que el cliente espera un moniker.</span><span class="sxs-lookup"><span data-stu-id="4d969-109">However, suppose your client is expecting a moniker.</span></span> <span data-ttu-id="4d969-110">No se puede identificar el objeto con un moniker de archivo porque no está almacenado en un archivo ni con un moniker de elemento, porque no está incluido en otro objeto.</span><span class="sxs-lookup"><span data-stu-id="4d969-110">The object cannot be identified with a file moniker, because it isn't stored in a file, nor with an item moniker, because it isn't contained in another object.</span></span>

<span data-ttu-id="4d969-111">En su lugar, la aplicación puede crear un moniker de puntero, que es un moniker que simplemente contiene un puntero internamente, y pasarlo al cliente.</span><span class="sxs-lookup"><span data-stu-id="4d969-111">Instead, your application can create a pointer moniker, which is a moniker that simply contains a pointer internally, and pass that to the client.</span></span> <span data-ttu-id="4d969-112">El cliente puede tratar este moniker como cualquier otro.</span><span class="sxs-lookup"><span data-stu-id="4d969-112">The client can treat this moniker like any other.</span></span> <span data-ttu-id="4d969-113">Sin embargo, cuando el cliente llama a [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) en el moniker de puntero, el código de moniker no comprueba la tabla de objetos en ejecución (Rot) ni carga nada desde el almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="4d969-113">However, when the client calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on the pointer moniker, the moniker code does not check the running object table (ROT) or load anything from storage.</span></span> <span data-ttu-id="4d969-114">En su lugar, el código de moniker simplemente llama a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero almacenado dentro del moniker.</span><span class="sxs-lookup"><span data-stu-id="4d969-114">Instead, the moniker code simply calls [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) on the pointer stored inside the moniker.</span></span>

<span data-ttu-id="4d969-115">Los monikers de puntero permiten que los objetos que solo existen en el estado activo o en ejecución participen en las operaciones de moniker y que los clientes moniker lo utilicen.</span><span class="sxs-lookup"><span data-stu-id="4d969-115">Pointer monikers allow objects that exist only in the active or running state to participate in moniker operations and be used by moniker clients.</span></span> <span data-ttu-id="4d969-116">Una diferencia importante entre los monikers de puntero y otras clases de monikers es que los monikers de puntero no se pueden guardar en el almacenamiento persistente.</span><span class="sxs-lookup"><span data-stu-id="4d969-116">One important difference between pointer monikers and other classes of monikers is that pointer monikers cannot be saved to persistent storage.</span></span> <span data-ttu-id="4d969-117">Si lo hace, al llamar al método [**IMoniker:: Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="4d969-117">If you do, calling the [**IMoniker::Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) method returns an error.</span></span> <span data-ttu-id="4d969-118">Esto significa que los monikers de puntero solo son útiles en situaciones especializadas.</span><span class="sxs-lookup"><span data-stu-id="4d969-118">This means that pointer monikers are useful only in specialized situations.</span></span> <span data-ttu-id="4d969-119">Puede usar la función [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) si necesita utilizar un moniker de puntero.</span><span class="sxs-lookup"><span data-stu-id="4d969-119">You can use the [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) function if you need to use a pointer moniker.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d969-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d969-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d969-121">Anti-monikers</span><span class="sxs-lookup"><span data-stu-id="4d969-121">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="4d969-122">Monikers de clase</span><span class="sxs-lookup"><span data-stu-id="4d969-122">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="4d969-123">Monikers compuestos</span><span class="sxs-lookup"><span data-stu-id="4d969-123">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="4d969-124">Monikers de archivo</span><span class="sxs-lookup"><span data-stu-id="4d969-124">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="4d969-125">Monikers de elemento</span><span class="sxs-lookup"><span data-stu-id="4d969-125">Item Monikers</span></span>](item-monikers.md)
</dt> </dl>

 

 




