---
title: Usar listas de visualización
description: Usar listas de visualización
ms.assetid: f5edff21-0928-4ec9-9718-5189bf8ce2d7
keywords:
- OpenGL, mostrar listas
- Mostrar listas OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793ec78af0b19ac437e44f16e13b93db6eab32a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903310"
---
# <a name="using-display-lists"></a><span data-ttu-id="de842-105">Usar listas de visualización</span><span class="sxs-lookup"><span data-stu-id="de842-105">Using Display Lists</span></span>

<span data-ttu-id="de842-106">Una lista de visualización es un grupo de funciones OpenGL que se ha almacenado para su posterior ejecución.</span><span class="sxs-lookup"><span data-stu-id="de842-106">A display list is a group of OpenGL functions that has been stored for subsequent execution.</span></span> <span data-ttu-id="de842-107">La función [**glNewList**](glnewlist.md) inicia la creación de una lista de visualización y [**glEndList**](glendlist.md) la finaliza.</span><span class="sxs-lookup"><span data-stu-id="de842-107">The [**glNewList**](glnewlist.md) function begins the creation of a display list, and [**glEndList**](glendlist.md) ends it.</span></span> <span data-ttu-id="de842-108">Con pocas excepciones, las funciones de OpenGL llamadas entre **glNewList** y **glEndList** se anexan a la lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="de842-108">With few exceptions, OpenGL functions called between **glNewList** and **glEndList** are appended to the display list.</span></span> <span data-ttu-id="de842-109">(Consulte **glNewList** para obtener una lista de las funciones que no se pueden almacenar y ejecutar desde dentro de una lista de visualización). Para desencadenar la ejecución de una lista o un conjunto de listas, use [**glCallList**](glcalllist.md) o [**glCallLists**](glcalllists.md) y proporcione el número de identificación de una lista o listas determinadas.</span><span class="sxs-lookup"><span data-stu-id="de842-109">(See **glNewList** for a list of the functions that you can't store and execute from within a display list.) To trigger the execution of a list or set of lists, use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) and supply the identifying number of a particular list or lists.</span></span> <span data-ttu-id="de842-110">Los índices que se usan para identificar las listas de visualización se administran con [**glGenLists**](glgenlists.md), [**glListBase**](gllistbase.md)y [**glIsList**](glislist.md).</span><span class="sxs-lookup"><span data-stu-id="de842-110">You manage the indexes used to identify display lists with [**glGenLists**](glgenlists.md), [**glListBase**](gllistbase.md), and [**glIsList**](glislist.md).</span></span> <span data-ttu-id="de842-111">Para eliminar un conjunto de listas de visualización, use [**glDeleteLists**](gldeletelists.md).</span><span class="sxs-lookup"><span data-stu-id="de842-111">To delete a set of display lists, use [**glDeleteLists**](gldeletelists.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="de842-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="de842-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de842-113">Referencia de listas de visualización</span><span class="sxs-lookup"><span data-stu-id="de842-113">Display Lists Reference</span></span>](display-lists-reference.md)
</dt> </dl>

 

 




