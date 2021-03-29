---
title: Cuándo usar la tabla de interfaz global
description: Cuándo usar la tabla de interfaz global
ms.assetid: def8f7f8-9d0d-49a4-9d5c-40233903eea5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89bbd7437b65c85abe89e8d647cbd73555c2d6a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078413"
---
# <a name="when-to-use-the-global-interface-table"></a><span data-ttu-id="23522-103">Cuándo usar la tabla de interfaz global</span><span class="sxs-lookup"><span data-stu-id="23522-103">When to Use the Global Interface Table</span></span>

<span data-ttu-id="23522-104">Si va a calcular las referencias de un puntero de interfaz varias veces entre apartamentos en un proceso, puede usar la interfaz [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) .</span><span class="sxs-lookup"><span data-stu-id="23522-104">If you are unmarshaling an interface pointer multiple times between apartments in a process, you might use the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="23522-105">Con otras técnicas, tendría que volver a calcular las referencias de cada vez.</span><span class="sxs-lookup"><span data-stu-id="23522-105">With other techniques, you would have to remarshal each time.</span></span>

> [!Note]  
> <span data-ttu-id="23522-106">Si el puntero de interfaz no se calcula una sola vez, puede que desee usar la función [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) .</span><span class="sxs-lookup"><span data-stu-id="23522-106">If the interface pointer is unmarshaled only once, you may want to use the [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) function.</span></span> <span data-ttu-id="23522-107">También se puede usar para pasar un puntero de interfaz de un subproceso a otro subproceso en el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="23522-107">It can also be used to pass an interface pointer from one thread to another thread in the same process.</span></span>

 

<span data-ttu-id="23522-108">La interfaz [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) también hace que otro problema con anterioridad difícil sea más sencillo para el programador.</span><span class="sxs-lookup"><span data-stu-id="23522-108">The [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface also makes another previously difficult problem simpler for the programmer.</span></span> <span data-ttu-id="23522-109">Este problema se produce cuando se cumplen las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="23522-109">This problem occurs when the following conditions apply:</span></span>

-   <span data-ttu-id="23522-110">Un objeto ágil en proceso agrega el contador de referencias de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="23522-110">An in-process agile object aggregates the free-threaded marshaler.</span></span>
-   <span data-ttu-id="23522-111">Este mismo objeto ágil también contiene punteros de interfaz (como variables de miembro) a otros objetos que no son ágiles y no agregan el contador de referencias de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="23522-111">This same agile object also holds (as member variables) interface pointers to other objects that are not agile and do not aggregate the free-threaded marshaler.</span></span>

<span data-ttu-id="23522-112">En esta situación, si el objeto externo obtiene las referencias a otro apartamento y la aplicación llama a en él, y el objeto intenta llamar a en cualquiera de sus punteros de interfaz de variable miembro que no son de subprocesamiento libre o que son proxies a objetos de otros apartamentos, podría obtener resultados incorrectos o el \_ subproceso RPC E incorrecto de error \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="23522-112">In this situation, if the outer object gets marshaled to another apartment and the application calls on it, and the object tries to call on any of its member variable interface pointers that are not free-threaded or are proxies to objects in other apartments, it might get incorrect results or the error RPC\_E\_WRONG\_THREAD.</span></span> <span data-ttu-id="23522-113">Este error se produce porque la interfaz interna está diseñada para que solo se pueda llamar desde el apartamento en el que se almacenó por primera vez en la variable miembro.</span><span class="sxs-lookup"><span data-stu-id="23522-113">This error occurs because the inner interface is designed to be callable only from the apartment in which it was first stored in the member variable.</span></span>

<span data-ttu-id="23522-114">Para solucionar este problema, el objeto externo que agrega el contador de referencias de subprocesamiento libre debe llamar a [**IGlobalInterfaceTable:: RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) en la interfaz interna y almacenar la cookie resultante en su variable miembro, en lugar de almacenar el puntero de interfaz real.</span><span class="sxs-lookup"><span data-stu-id="23522-114">To solve this problem, the outer object aggregating the free-threaded marshaler should call [**IGlobalInterfaceTable::RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) on the inner interface and store the resulting cookie in its member variable, instead of storing the actual interface pointer.</span></span> <span data-ttu-id="23522-115">Cuando el objeto externo desea llamar a en el puntero de interfaz de un objeto interno, debe llamar a [**IGlobalInterfaceTable:: GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal), usar el puntero de interfaz devuelto y, a continuación, liberarlo.</span><span class="sxs-lookup"><span data-stu-id="23522-115">When the outer object wants to call on an inner object's interface pointer, it should call [**IGlobalInterfaceTable::GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal), use the returned interface pointer, and then release it.</span></span> <span data-ttu-id="23522-116">Cuando el objeto externo desaparece, debe llamar a [**IGlobalInterfaceTable:: RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) para quitar la interfaz de la tabla de interfaz global.</span><span class="sxs-lookup"><span data-stu-id="23522-116">When the outer object goes away, it should call [**IGlobalInterfaceTable::RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) to remove the interface from the global interface table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23522-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23522-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23522-118">Crear la tabla de interfaz global</span><span class="sxs-lookup"><span data-stu-id="23522-118">Creating the Global Interface Table</span></span>](creating-the-global-interface-table.md)
</dt> </dl>

 

 