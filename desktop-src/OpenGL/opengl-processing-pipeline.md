---
title: Canalización de procesamiento de OpenGL
description: Canalización de procesamiento de OpenGL
ms.assetid: 98ac89d1-0d7b-45b2-8d6e-c421b9289d60
keywords:
- OpenGL, canalización de procesamiento
- procesamiento de la canalización OpenGL
- OpenGL de canalización
- framebuffers, canalización de procesamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d67447066b9d397bbb272932f51c6d3003f11e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104552886"
---
# <a name="opengl-processing-pipeline"></a><span data-ttu-id="bc984-107">Canalización de procesamiento de OpenGL</span><span class="sxs-lookup"><span data-stu-id="bc984-107">OpenGL Processing Pipeline</span></span>

<span data-ttu-id="bc984-108">Muchas funciones de OpenGL se utilizan específicamente para dibujar objetos como puntos, líneas, polígonos y mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="bc984-108">Many OpenGL functions are used specifically for drawing objects such as points, lines, polygons, and bitmaps.</span></span> <span data-ttu-id="bc984-109">Algunas funciones controlan la forma en que se produce parte de este dibujo (como los que habilitan el suavizado de contorno o la texturización).</span><span class="sxs-lookup"><span data-stu-id="bc984-109">Some functions control the way that some of this drawing occurs (such as those that enable antialiasing or texturing).</span></span> <span data-ttu-id="bc984-110">Otras funciones están especialmente preocupadas por la manipulación de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="bc984-110">Other functions are specifically concerned with framebuffer manipulation.</span></span> <span data-ttu-id="bc984-111">En los temas de esta sección se describe el funcionamiento conjunto de todas las funciones de OpenGL para crear la canalización de procesamiento de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="bc984-111">The topics in this section describe how all of the OpenGL functions work together to create the OpenGL processing pipeline.</span></span> <span data-ttu-id="bc984-112">En esta sección también se examinan con más detalle las fases en las que se procesan los datos y se vinculan estas fases a las funciones de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="bc984-112">This section also takes a closer look at the stages in which data is actually processed, and ties these stages to OpenGL functions.</span></span>

<span data-ttu-id="bc984-113">En el siguiente diagrama se detalla la canalización de procesamiento de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="bc984-113">The following diagram details the OpenGL processing pipeline.</span></span> <span data-ttu-id="bc984-114">Para la mayor parte de la canalización, puede ver tres flechas verticales entre las fases principales.</span><span class="sxs-lookup"><span data-stu-id="bc984-114">For most of the pipeline, you can see three vertical arrows between the major stages.</span></span> <span data-ttu-id="bc984-115">Estas flechas representan los vértices y los dos tipos principales de datos que se pueden asociar a los vértices: valores de color y coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="bc984-115">These arrows represent vertices and the two primary types of data that can be associated with vertices: color values and texture coordinates.</span></span> <span data-ttu-id="bc984-116">Tenga en cuenta también que los vértices se ensamblan en primitivos, luego en fragmentos y, por último, en píxeles en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="bc984-116">Also note that vertices are assembled into primitives, then into fragments, and finally into pixels in the framebuffer.</span></span> <span data-ttu-id="bc984-117">Esta progresión se describe con más detalle en [vértices](vertices.md), [primitivas](primitives.md), [fragmentos](fragments.md)y [píxeles](pixels.md).</span><span class="sxs-lookup"><span data-stu-id="bc984-117">This progression is discussed in more detail in [Vertices](vertices.md), [Primitives](primitives.md), [Fragments](fragments.md), and [Pixels](pixels.md).</span></span>

![Diagrama que muestra la canalización de procesamiento de OpenGL.](images/proc01.png)

 

 




