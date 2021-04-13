---
title: Administrar la asignación de memoria
description: Administrar la asignación de memoria
ms.assetid: 8a189fe8-5555-44bb-968b-04408fa7fce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2af04b4ecc5b8480230b17ae710b84ce8e6ce5d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421487"
---
# <a name="managing-memory-allocation"></a><span data-ttu-id="b4fc5-103">Administrar la asignación de memoria</span><span class="sxs-lookup"><span data-stu-id="b4fc5-103">Managing Memory Allocation</span></span>

<span data-ttu-id="b4fc5-104">En COM, muchos, si no más, se llama a los métodos de interfaz mediante código escrito por una organización de programación y se implementa mediante código escrito por otro.</span><span class="sxs-lookup"><span data-stu-id="b4fc5-104">In COM, many, if not most, interface methods are called by code written by one programming organization and implemented by code written by another.</span></span> <span data-ttu-id="b4fc5-105">Muchos de los parámetros y valores devueltos de estas funciones son de tipos que se pueden pasar por valor.</span><span class="sxs-lookup"><span data-stu-id="b4fc5-105">Many of the parameters and return values of these functions are of types that can be passed around by value.</span></span> <span data-ttu-id="b4fc5-106">Sin embargo, a veces es necesario pasar estructuras de datos para las que este no es el caso, por lo que es necesario que el llamador y la llamada tengan una directiva de asignación y desasignación compatible.</span><span class="sxs-lookup"><span data-stu-id="b4fc5-106">Sometimes, however, it is necessary to pass data structures for which this is not the case, so it is necessary for both caller and called to have a compatible allocation and de-allocation policy.</span></span> <span data-ttu-id="b4fc5-107">COM define una Convención universal para la asignación de memoria, porque es más razonable que definir reglas de caso por caso y para que la implementación de llamadas a procedimientos remotos COM pueda administrar correctamente la memoria.</span><span class="sxs-lookup"><span data-stu-id="b4fc5-107">COM defines a universal convention for memory allocation, because it is more reasonable than defining case-by-case rules and so that the COM remote procedure call implementation can correctly manage memory.</span></span>

<span data-ttu-id="b4fc5-108">Los métodos de una interfaz COM siempre proporcionan administración de memoria de punteros a la interfaz llamando a las funciones [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) que se encuentran en la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , de la que derivan todas las demás interfaces com.</span><span class="sxs-lookup"><span data-stu-id="b4fc5-108">The methods of a COM interface always provide memory management of pointers to the interface by calling the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) functions found in the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, from which all other COM interfaces derive.</span></span> <span data-ttu-id="b4fc5-109">(Consulte [reglas para administrar recuentos de referencias](rules-for-managing-reference-counts.md) para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="b4fc5-109">(See [Rules for Managing Reference Counts](rules-for-managing-reference-counts.md) for more information.)</span></span>

<span data-ttu-id="b4fc5-110">En esta sección solo se describe cómo asignar memoria para los parámetros que no se pasan por valor, no punteros a las interfaces, sino aspectos más cotidianos, como cadenas, punteros a estructuras, etc.</span><span class="sxs-lookup"><span data-stu-id="b4fc5-110">This section describes only how to allocate memory for parameters that are not passed by value — not pointers to interfaces, but more mundane things like strings, pointers to structures, and so forth.</span></span>

<span data-ttu-id="b4fc5-111">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="b4fc5-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="b4fc5-112">Asignador de memoria OLE</span><span class="sxs-lookup"><span data-stu-id="b4fc5-112">The OLE Memory Allocator</span></span>](the-ole-memory-allocator.md)
-   [<span data-ttu-id="b4fc5-113">Reglas de administración de memoria</span><span class="sxs-lookup"><span data-stu-id="b4fc5-113">Memory Management Rules</span></span>](memory-management-rules.md)
-   [<span data-ttu-id="b4fc5-114">Depurar asignaciones de memoria</span><span class="sxs-lookup"><span data-stu-id="b4fc5-114">Debugging Memory Allocations</span></span>](debugging-memory-allocations.md)

 

 