---
title: Anti-monikers
description: OLE proporciona una implementación de un tipo especial de moniker denominado anti-moniker.
ms.assetid: 3b52d3bd-8375-4463-a0e3-5117fa96a1c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d69c461268b486a040b36f59108bc8e8379656
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075861"
---
# <a name="anti-monikers"></a><span data-ttu-id="e1d0e-103">Anti-monikers</span><span class="sxs-lookup"><span data-stu-id="e1d0e-103">Anti-Monikers</span></span>

<span data-ttu-id="e1d0e-104">OLE proporciona una implementación de un tipo especial de moniker denominado *anti-moniker*.</span><span class="sxs-lookup"><span data-stu-id="e1d0e-104">OLE provides an implementation of a special type of moniker called an *anti-moniker*.</span></span> <span data-ttu-id="e1d0e-105">Este moniker se usa en la creación de nuevas clases moniker.</span><span class="sxs-lookup"><span data-stu-id="e1d0e-105">You use this moniker in the creation of new moniker classes.</span></span> <span data-ttu-id="e1d0e-106">Se usa como el inverso del moniker en el que se compone y, de hecho, se cancela el moniker de la misma manera que el operador ".." sube un nivel de directorio en un comando del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="e1d0e-106">You use it as the inverse of the moniker that it is composed onto, effectively canceling that moniker, in much the same way that the ".." operator moves up a directory level in a file system command.</span></span>

<span data-ttu-id="e1d0e-107">Es necesario tener un anti-moniker disponible, ya que una vez creado un moniker compuesto, no es posible eliminar partes del moniker si, por ejemplo, se mueve un objeto.</span><span class="sxs-lookup"><span data-stu-id="e1d0e-107">It is necessary to have an anti-moniker available, because once a composite moniker is created, it is not possible to delete parts of the moniker if, for example, an object moves.</span></span> <span data-ttu-id="e1d0e-108">En su lugar, se usa un anti-moniker para quitar una o varias entradas de un moniker compuesto.</span><span class="sxs-lookup"><span data-stu-id="e1d0e-108">Instead, you use an anti-moniker to remove one or more entries from a composite moniker.</span></span>

<span data-ttu-id="e1d0e-109">Los anti-monikers son una clase de moniker diseñada explícitamente para su uso como inversa.</span><span class="sxs-lookup"><span data-stu-id="e1d0e-109">Anti-monikers are a moniker class explicitly intended for use as an inverse.</span></span> <span data-ttu-id="e1d0e-110">COM define la función [**CreateAntiMoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) con nombre, que devuelve un anti-moniker.</span><span class="sxs-lookup"><span data-stu-id="e1d0e-110">COM defines the named [**CreateAntiMoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) function, which returns an anti-moniker.</span></span> <span data-ttu-id="e1d0e-111">Normalmente, se usa esta función para implementar el método [**IMoniker:: inverso**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) .</span><span class="sxs-lookup"><span data-stu-id="e1d0e-111">You generally use this function to implement the [**IMoniker::Inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) method.</span></span>

<span data-ttu-id="e1d0e-112">Un anti-moniker es solo un inverso para los tipos de monikers que se implementan para tratar los suavizadores como inversos.</span><span class="sxs-lookup"><span data-stu-id="e1d0e-112">An anti-moniker is only an inverse for those types of monikers that are implemented to treat anti-monikers as an inverse.</span></span> <span data-ttu-id="e1d0e-113">Por ejemplo, si desea quitar la última parte de un moniker compuesto, no debe crear un elemento anti-moniker y componerlo al final del compuesto.</span><span class="sxs-lookup"><span data-stu-id="e1d0e-113">For example, if you want to remove the last piece of a composite moniker, you should not create an anti-moniker and compose it to the end of the composite.</span></span> <span data-ttu-id="e1d0e-114">No puede estar seguro de que la última parte del compuesto considera que un moniker es su inversa.</span><span class="sxs-lookup"><span data-stu-id="e1d0e-114">You cannot be sure that the last piece of the composite considers an anti-moniker to be its inverse.</span></span> <span data-ttu-id="e1d0e-115">En su lugar, debe llamar a [**IMoniker:: enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) en el moniker compuesto, especificando **false** como primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="e1d0e-115">Instead, you should call [**IMoniker::Enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) on the composite moniker, specifying **FALSE** as the first parameter.</span></span> <span data-ttu-id="e1d0e-116">Esto crea un enumerador que devuelve los monikers del componente en orden inverso.</span><span class="sxs-lookup"><span data-stu-id="e1d0e-116">This creates an enumerator that returns the component monikers in reverse order.</span></span> <span data-ttu-id="e1d0e-117">Use el enumerador para recuperar la última parte del compuesto y llame a [**inverso**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) en ese moniker.</span><span class="sxs-lookup"><span data-stu-id="e1d0e-117">Use the enumerator to retrieve the last piece of the composite, and call [**Inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) on that moniker.</span></span> <span data-ttu-id="e1d0e-118">El moniker devuelto por **inverso** es lo que necesita para quitar la última parte del compuesto.</span><span class="sxs-lookup"><span data-stu-id="e1d0e-118">The moniker returned by **Inverse** is what you need to remove the last piece of the composite.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1d0e-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1d0e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1d0e-120">Monikers de clase</span><span class="sxs-lookup"><span data-stu-id="e1d0e-120">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="e1d0e-121">Monikers compuestos</span><span class="sxs-lookup"><span data-stu-id="e1d0e-121">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="e1d0e-122">Monikers de archivo</span><span class="sxs-lookup"><span data-stu-id="e1d0e-122">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="e1d0e-123">Monikers de elemento</span><span class="sxs-lookup"><span data-stu-id="e1d0e-123">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="e1d0e-124">Monikers de puntero</span><span class="sxs-lookup"><span data-stu-id="e1d0e-124">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




