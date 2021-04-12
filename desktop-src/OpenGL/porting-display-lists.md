---
title: Portabilidad de listas de presentación
description: La implementación de OpenGL de las listas de visualización es similar a la implementación de la contabilidad de IRIS, con dos excepciones en OpenGL no se pueden editar las listas de visualización una vez creadas y no se pueden llamar a funciones desde las listas de visualización.
ms.assetid: 617e19ff-6a55-4f7c-b229-075cdee8f1cf
keywords:
- Migración de la contabilidad de IRIS, mostrar listas
- trasladar de IRIS GL, mostrar listas
- trasladar a OpenGL desde IRIS GL, mostrar listas
- Exportación de OpenGL desde IRIS GL, mostrar listas
- Mostrar listas, trasladar de IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461000e6d785f0d03bbbc8f738eba60768bc5d74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356808"
---
# <a name="porting-display-lists"></a><span data-ttu-id="30c32-108">Portabilidad de listas de presentación</span><span class="sxs-lookup"><span data-stu-id="30c32-108">Porting Display Lists</span></span>

<span data-ttu-id="30c32-109">La implementación de OpenGL de las listas de visualización es similar a la implementación de la contabilidad de IRIS, con dos excepciones: en OpenGL no se pueden editar listas de visualización una vez creadas y no se puede llamar a funciones desde las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="30c32-109">The OpenGL implementation of display lists is similar to the IRIS GL implementation, with two exceptions: in OpenGL you can't edit display lists once you've created them and you can't call functions from within display lists.</span></span>

<span data-ttu-id="30c32-110">Dado que no puede editar ni llamar a funciones desde las listas de visualización, estas funciones de la contabilidad de IRIS no tienen ningún equivalente en OpenGL:</span><span class="sxs-lookup"><span data-stu-id="30c32-110">Because you can't edit or call functions from within display lists, these IRIS GL functions have no equivalent in OpenGL:</span></span>

-   <span data-ttu-id="30c32-111">**editobj**</span><span class="sxs-lookup"><span data-stu-id="30c32-111">**editobj**</span></span>
-   <span data-ttu-id="30c32-112">**objdelete**, **objinsert** y **objreplace**</span><span class="sxs-lookup"><span data-stu-id="30c32-112">**objdelete**, **objinsert**, and **objreplace**</span></span>
-   <span data-ttu-id="30c32-113">**maketag**, **gentag**, **ISTAG** y **DelTag**</span><span class="sxs-lookup"><span data-stu-id="30c32-113">**maketag**, **gentag**, **istag**, and **deltag**</span></span>
-   <span data-ttu-id="30c32-114">**callfunc**</span><span class="sxs-lookup"><span data-stu-id="30c32-114">**callfunc**</span></span>

<span data-ttu-id="30c32-115">En IRIS GL, se usan las funciones **Makeobj** y **closeobj** para crear listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="30c32-115">In IRIS GL, you use the **makeobj** and **closeobj** functions to create display lists.</span></span> <span data-ttu-id="30c32-116">En OpenGL, se usa [**glNewList**](glnewlist.md) y [**glEndList**](glendlist.md).</span><span class="sxs-lookup"><span data-stu-id="30c32-116">In OpenGL, you use [**glNewList**](glnewlist.md) and [**glEndList**](glendlist.md).</span></span>

<span data-ttu-id="30c32-117">En la tabla siguiente se enumeran las funciones de lista de visualización de IRIS GL con sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="30c32-117">The following table lists the IRIS GL display list functions with their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="30c32-118">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="30c32-118">IRIS GL function</span></span> | <span data-ttu-id="30c32-119">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="30c32-119">OpenGL function</span></span>                                                      | <span data-ttu-id="30c32-120">Significado</span><span class="sxs-lookup"><span data-stu-id="30c32-120">Meaning</span></span>                                                       |
|------------------|----------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="30c32-121">**makeobj**</span><span class="sxs-lookup"><span data-stu-id="30c32-121">**makeobj**</span></span>      | <span data-ttu-id="30c32-122">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="30c32-122">**glNewList**</span></span>                                                        | <span data-ttu-id="30c32-123">Crea una nueva lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="30c32-123">Creates a new display list.</span></span>                                   |
| <span data-ttu-id="30c32-124">**closeobj**</span><span class="sxs-lookup"><span data-stu-id="30c32-124">**closeobj**</span></span>     | <span data-ttu-id="30c32-125">**glEndList**</span><span class="sxs-lookup"><span data-stu-id="30c32-125">**glEndList**</span></span>                                                        | <span data-ttu-id="30c32-126">Señala el final de la lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="30c32-126">Signals end of display list.</span></span>                                  |
| <span data-ttu-id="30c32-127">**callobj**</span><span class="sxs-lookup"><span data-stu-id="30c32-127">**callobj**</span></span>      | <span data-ttu-id="30c32-128">[**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md)</span><span class="sxs-lookup"><span data-stu-id="30c32-128">[**glCallList**](glcalllist.md), [**glCallLists**](glcalllists.md)</span></span> | <span data-ttu-id="30c32-129">Ejecuta Mostrar lista o listas.</span><span class="sxs-lookup"><span data-stu-id="30c32-129">Executes display list or lists.</span></span>                               |
| <span data-ttu-id="30c32-130">**isobj**</span><span class="sxs-lookup"><span data-stu-id="30c32-130">**isobj**</span></span>        | [<span data-ttu-id="30c32-131">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="30c32-131">**glIsList**</span></span>](glislist.md)                                         | <span data-ttu-id="30c32-132">Comprueba la existencia de la lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="30c32-132">Tests for display list existence.</span></span>                             |
| <span data-ttu-id="30c32-133">**delobj**</span><span class="sxs-lookup"><span data-stu-id="30c32-133">**delobj**</span></span>       | [<span data-ttu-id="30c32-134">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="30c32-134">**glDeleteLists**</span></span>](gldeletelists.md)                               | <span data-ttu-id="30c32-135">Elimina un grupo contiguo de listas de presentación.</span><span class="sxs-lookup"><span data-stu-id="30c32-135">Deletes contiguous group of display lists.</span></span>                    |
| <span data-ttu-id="30c32-136">**genobj**</span><span class="sxs-lookup"><span data-stu-id="30c32-136">**genobj**</span></span>       | [<span data-ttu-id="30c32-137">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="30c32-137">**glGenLists**</span></span>](glgenlists.md)                                     | <span data-ttu-id="30c32-138">Genera el número especificado de listas de presentación vacías contiguas.</span><span class="sxs-lookup"><span data-stu-id="30c32-138">Generates the given number of contiguous empty display lists.</span></span> |



 

<span data-ttu-id="30c32-139">En este tema se incluye información sobre lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="30c32-139">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="30c32-140">Trasladar la función bbox2</span><span class="sxs-lookup"><span data-stu-id="30c32-140">Porting the bbox2 Function</span></span>](porting-the-bbox2-function.md)
-   [<span data-ttu-id="30c32-141">Trasladar listas de visualización editadas</span><span class="sxs-lookup"><span data-stu-id="30c32-141">Porting Edited Display Lists</span></span>](porting-edited-display-lists.md)
-   [<span data-ttu-id="30c32-142">Un puerto de ejemplo de una lista de visualización</span><span class="sxs-lookup"><span data-stu-id="30c32-142">A Sample Port of a Display List</span></span>](a-sample-port-of-a-display-list.md)

 

 




