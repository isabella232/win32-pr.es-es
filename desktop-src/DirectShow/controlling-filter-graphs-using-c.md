---
description: Controlar gráficos de filtros mediante C
ms.assetid: 56e41f0a-2ea6-422c-8d3f-7849e91e3731
title: Controlar gráficos de filtros mediante C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce6d78875c6b0d5f028ea89dfbd2b061285f1c1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422988"
---
# <a name="controlling-filter-graphs-using-c"></a><span data-ttu-id="45993-103">Controlar gráficos de filtros mediante C</span><span class="sxs-lookup"><span data-stu-id="45993-103">Controlling Filter Graphs Using C</span></span>

<span data-ttu-id="45993-104">Si está escribiendo una aplicación de DirectShow en C (en lugar de C++), debe usar un puntero vtable para llamar a métodos.</span><span class="sxs-lookup"><span data-stu-id="45993-104">If you are writing a DirectShow application in C (rather than C++), you must use a vtable pointer to call methods.</span></span> <span data-ttu-id="45993-105">En el ejemplo siguiente se muestra cómo llamar al método **IUnknown:: QueryInterface** desde una aplicación escrita en C:</span><span class="sxs-lookup"><span data-stu-id="45993-105">The following example illustrates how to call the **IUnknown::QueryInterface** method from an application written in C:</span></span>


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="45993-106">A continuación se muestra la llamada equivalente en C++:</span><span class="sxs-lookup"><span data-stu-id="45993-106">The following shows the equivalent call in C++:</span></span>


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="45993-107">En C, las interfaces COM se definen como estructuras.</span><span class="sxs-lookup"><span data-stu-id="45993-107">In C, COM interfaces are defined as structures.</span></span> <span data-ttu-id="45993-108">El miembro **lpVtbl** es un puntero a una tabla de métodos de interfaz (vtable).</span><span class="sxs-lookup"><span data-stu-id="45993-108">The **lpVtbl** member is a pointer to a table of interface methods (the vtable).</span></span> <span data-ttu-id="45993-109">Todos los métodos toman un parámetro adicional, que es un puntero a la interfaz.</span><span class="sxs-lookup"><span data-stu-id="45993-109">All methods take an additional parameter, which is a pointer to the interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45993-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="45993-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45993-111">Apéndices</span><span class="sxs-lookup"><span data-stu-id="45993-111">Appendixes</span></span>](appendixes.md)
</dt> </dl>

 

 



