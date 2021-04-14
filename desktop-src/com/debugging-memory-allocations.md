---
title: Depurar asignaciones de memoria
description: Depurar asignaciones de memoria
ms.assetid: 522adb1f-0e3e-4dfb-8836-f539a79a3d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb6a7dbe313cfe571fa6b4d244df35407fa331e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359437"
---
# <a name="debugging-memory-allocations"></a><span data-ttu-id="79c9a-103">Depurar asignaciones de memoria</span><span class="sxs-lookup"><span data-stu-id="79c9a-103">Debugging Memory Allocations</span></span>

<span data-ttu-id="79c9a-104">COM proporciona la interfaz [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) para que los desarrolladores puedan usar para depurar las asignaciones de memoria.</span><span class="sxs-lookup"><span data-stu-id="79c9a-104">COM provides the [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) interface for developers to use to debug their memory allocations.</span></span> <span data-ttu-id="79c9a-105">Para cada método de [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc), hay dos métodos en **IMallocSpy**, un método "pre" y un método "post".</span><span class="sxs-lookup"><span data-stu-id="79c9a-105">For each method in [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc), there are two methods in **IMallocSpy**, a "pre" method and a "post" method.</span></span> <span data-ttu-id="79c9a-106">Después de que un desarrollador lo implemente y lo publique en el sistema, el sistema llama al método "pre" de **IMallocSpy** justo antes del método **IMalloc** correspondiente, permitiendo de forma eficaz el código de depuración a "Spy" en la operación de asignación y llama al método "post" para liberar el espía.</span><span class="sxs-lookup"><span data-stu-id="79c9a-106">After a developer implements it and publishes it to the system, the system calls the **IMallocSpy** "pre" method just before the corresponding **IMalloc** method, effectively allowing the debug code to "spy" on the allocation operation, and calls the "post" method to release the spy.</span></span>

<span data-ttu-id="79c9a-107">Por ejemplo, cuando COM detecta que la siguiente llamada es una llamada a [**IMalloc:: Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), llama a [**IMallocSpy::P realloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), ejecuta las operaciones de depuración que el desarrollador desea durante la ejecución de la **asignación** y, a continuación, cuando la llamada de **asignación** vuelve, llama a [**IMallocSpy::P ostalloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) para liberar el Spy y devolver el control al código.</span><span class="sxs-lookup"><span data-stu-id="79c9a-107">For example, when COM detects that the next call is a call to [**IMalloc::Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), it calls [**IMallocSpy::PreAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), executing whatever debug operations the developer wants during the **Alloc** execution, and then, when the **Alloc** call returns, calls [**IMallocSpy::PostAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) to release the spy and return control to the code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79c9a-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="79c9a-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79c9a-109">Administrar la asignación de memoria</span><span class="sxs-lookup"><span data-stu-id="79c9a-109">Managing Memory Allocation</span></span>](managing-memory-allocation.md)
</dt> </dl>

 

 