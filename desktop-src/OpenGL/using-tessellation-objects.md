---
title: Usar objetos de teselación
description: Como un polígono complejo se describe y se tesela, requiere datos asociados, como los vértices, los bordes y las funciones de devolución de llamada.
ms.assetid: b6102e25-280c-4d0d-9350-d0038d1a0306
keywords:
- Utilidad OpenGL (GLU), objetos de teselación
- GLU (utilidad OpenGL), objetos de teselación
- objetos de teselación OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590ab571e656fcd346da265bfa921cb965fdf540
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356902"
---
# <a name="using-tessellation-objects"></a><span data-ttu-id="62c2e-106">Usar objetos de teselación</span><span class="sxs-lookup"><span data-stu-id="62c2e-106">Using Tessellation Objects</span></span>

<span data-ttu-id="62c2e-107">Como un polígono complejo se describe y se tesela, requiere datos asociados, como los vértices, los bordes y las funciones de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="62c2e-107">As a complex polygon is being described and tessellated, it requires associated data, such as the vertices, edges, and callback functions.</span></span> <span data-ttu-id="62c2e-108">Todos estos datos están asociados a un único objeto de teselación.</span><span class="sxs-lookup"><span data-stu-id="62c2e-108">All this data is tied to a single tessellation object.</span></span> <span data-ttu-id="62c2e-109">Para dividirlas un polígono, primero se usa la función [**gluNewTess**](glunewtess.md) , que crea un nuevo objeto de teselación y devuelve un puntero a él.</span><span class="sxs-lookup"><span data-stu-id="62c2e-109">To tessellate a polygon, you first use the [**gluNewTess**](glunewtess.md) function which creates a new tessellation object and returns a pointer to it.</span></span> <span data-ttu-id="62c2e-110">Si se produce un error en la función, se devuelve un puntero NULL.</span><span class="sxs-lookup"><span data-stu-id="62c2e-110">A null pointer is returned if the function fails.</span></span>

<span data-ttu-id="62c2e-111">Si ya no necesita un objeto de teselación, puede eliminarlo y liberar toda la memoria asociada con [**gluDeleteTess**](gludeletetess.md).</span><span class="sxs-lookup"><span data-stu-id="62c2e-111">If you no longer need a tessellation object, you can delete it and free all associated memory with [**gluDeleteTess**](gludeletetess.md).</span></span>

<span data-ttu-id="62c2e-112">Puede reutilizar un solo objeto de teselación para todas las teselaciones.</span><span class="sxs-lookup"><span data-stu-id="62c2e-112">You can reuse a single tessellation object for all your tessellations.</span></span> <span data-ttu-id="62c2e-113">Este objeto solo es necesario porque las funciones de biblioteca pueden necesitar realizar sus propias teselaciones y deben poder hacerlo sin interferir con ninguna teselación que el programa esté realizando.</span><span class="sxs-lookup"><span data-stu-id="62c2e-113">This object is required only because library functions may need to do their own tessellations, and they should be able to do so without interfering with any tessellation that your program is performing.</span></span> <span data-ttu-id="62c2e-114">Los objetos de teselación múltiples también son útiles si desea utilizar diferentes conjuntos de devoluciones de llamada para diferentes teselaciones.</span><span class="sxs-lookup"><span data-stu-id="62c2e-114">Multiple tessellation objects are also useful if you want to use different sets of callbacks for different tessellations.</span></span> <span data-ttu-id="62c2e-115">Sin embargo, normalmente se asigna un único objeto de teselación y se usa para todas las teselaciones.</span><span class="sxs-lookup"><span data-stu-id="62c2e-115">Typically, however, you allocate a single tessellation object and use it for all the tessellations.</span></span> <span data-ttu-id="62c2e-116">No hay ninguna necesidad real de liberarla, ya que utiliza una pequeña cantidad de memoria.</span><span class="sxs-lookup"><span data-stu-id="62c2e-116">There's no real need to free it, because it uses a small amount of memory.</span></span> <span data-ttu-id="62c2e-117">Por otro lado, si está escribiendo una función de biblioteca que usa teselación GLU, tenga cuidado de liberar cualquier objeto de teselación que cree.</span><span class="sxs-lookup"><span data-stu-id="62c2e-117">On the other hand, if you're writing a library function that uses GLU tessellation, be careful to free any tessellation objects you create.</span></span>

 

 




