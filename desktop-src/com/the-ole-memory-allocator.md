---
title: Asignador de memoria OLE
description: Asignador de memoria OLE
ms.assetid: 026c62e5-c296-4059-b028-77c98fdb77ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64fedd610fd8fd6dab0bcd14deb37e04f6df74d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149652"
---
# <a name="the-ole-memory-allocator"></a><span data-ttu-id="578cb-103">Asignador de memoria OLE</span><span class="sxs-lookup"><span data-stu-id="578cb-103">The OLE Memory Allocator</span></span>

<span data-ttu-id="578cb-104">La biblioteca COM proporciona una implementación de un asignador de memoria que es segura para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="578cb-104">The COM library provides an implementation of a memory allocator that is thread-safe.</span></span> <span data-ttu-id="578cb-105">(Es decir, no puede producir problemas en situaciones multiproceso). Siempre que la propiedad de un fragmento de memoria asignado se pasa a través de una interfaz COM o entre un cliente y la biblioteca COM, debe utilizar este asignador COM para asignar la memoria.</span><span class="sxs-lookup"><span data-stu-id="578cb-105">(That is, it cannot cause problems in multithreaded situations.) Whenever ownership of an allocated chunk of memory is passed through a COM interface or between a client and the COM library, you must use this COM allocator to allocate the memory.</span></span> <span data-ttu-id="578cb-106">La asignación interna a un objeto puede usar cualquier esquema de asignación deseado, pero el asignador de memoria COM es un asignador práctico, eficaz y seguro para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="578cb-106">Allocation internal to an object can use any allocation scheme desired, but the COM memory allocator is a handy, efficient, and thread-safe allocator.</span></span>

<span data-ttu-id="578cb-107">Una llamada a la función de API [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) proporciona un puntero al asignador OLE, que es una implementación de la interfaz [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) .</span><span class="sxs-lookup"><span data-stu-id="578cb-107">A call to the API function [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) provides a pointer to the OLE allocator, which is an implementation of the [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) interface.</span></span> <span data-ttu-id="578cb-108">Sin embargo, es más eficaz llamar a las funciones auxiliares de [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**CoTaskMemRealloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc)y [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree), que encapsulan la obtención de un puntero al asignador de memoria de la tarea, llamando al método **IMalloc** correspondiente y, a continuación, liberando el puntero al asignador.</span><span class="sxs-lookup"><span data-stu-id="578cb-108">However, it is more efficient to call the helper functions [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**CoTaskMemRealloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc), and [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree), which wrap getting a pointer to the task memory allocator, calling the corresponding **IMalloc** method, and then releasing the pointer to the allocator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="578cb-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="578cb-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="578cb-110">Administrar la asignación de memoria</span><span class="sxs-lookup"><span data-stu-id="578cb-110">Managing Memory Allocation</span></span>](managing-memory-allocation.md)
</dt> <dt>

[<span data-ttu-id="578cb-111">Biblioteca COM</span><span class="sxs-lookup"><span data-stu-id="578cb-111">The COM Library</span></span>](the-com-library.md)
</dt> </dl>

 

 