---
title: Usar evaluadores
description: Usar evaluadores
ms.assetid: a5a99d0a-526e-4492-90c4-a6b9fdbdff16
keywords:
- OpenGL, evaluadores
- los evaluadores OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1aef70a7a854e16cf4992d9dd44c4931ad4d044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356904"
---
# <a name="using-evaluators"></a><span data-ttu-id="c832d-105">Usar evaluadores</span><span class="sxs-lookup"><span data-stu-id="c832d-105">Using Evaluators</span></span>

<span data-ttu-id="c832d-106">Las funciones del evaluador de OpenGL permiten usar una asignación polinómica para generar vértices, normales, coordenadas de textura y colores.</span><span class="sxs-lookup"><span data-stu-id="c832d-106">The OpenGL evaluator functions allow you to use a polynomial mapping to produce vertices, normals, texture coordinates, and colors.</span></span> <span data-ttu-id="c832d-107">Después, estos valores calculados se pasan a la canalización de procesamiento como si hubieran sido especificados directamente.</span><span class="sxs-lookup"><span data-stu-id="c832d-107">These calculated values are then passed on to the processing pipeline as if they had been directly specified.</span></span> <span data-ttu-id="c832d-108">Las funciones del evaluador también son la base de las funciones de NURBS (no uniforme B-spline racional), que permiten definir curvas y superficies, tal y como se describe en [biblioteca de utilidades de OpenGL](opengl-utility-library.md).</span><span class="sxs-lookup"><span data-stu-id="c832d-108">The evaluator functions are also the basis for the NURBS (Non-Uniform Rational B-Spline) functions, which allow you to define curves and surfaces, as described under [OpenGL Utility library](opengl-utility-library.md).</span></span>

<span data-ttu-id="c832d-109">El primer paso en el uso de evaluadores es definir la asignación polinómica de una o dos dimensiones adecuada [**mediante \* glMap**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="c832d-109">The first step in using evaluators is to define the appropriate one- or two-dimensional polynomial mapping using [**glMap\***](glmap1.md).</span></span> <span data-ttu-id="c832d-110">Después, puede especificar y evaluar los valores de dominio para esta asignación de una de estas dos maneras:</span><span class="sxs-lookup"><span data-stu-id="c832d-110">You can then specify and evaluate the domain values for this map in one of two ways:</span></span>

-   <span data-ttu-id="c832d-111">Defina una serie de valores de dominio equidistantemente espaciados que se van a asignar mediante [**glMapGrid**](glmapgrid-functions.md) y, a continuación, evalúe un subconjunto rectangular de esa cuadrícula con [**glEvalMesh**](glevalmesh-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c832d-111">Define a series of evenly spaced domain values to be mapped using [**glMapGrid**](glmapgrid-functions.md) and then evaluate a rectangular subset of that grid with [**glEvalMesh**](glevalmesh-functions.md).</span></span> <span data-ttu-id="c832d-112">Se puede evaluar un solo punto de la cuadrícula mediante [**glEvalPoint**](glevalpoint.md).</span><span class="sxs-lookup"><span data-stu-id="c832d-112">A single point of the grid can be evaluated using [**glEvalPoint**](glevalpoint.md).</span></span>
-   <span data-ttu-id="c832d-113">Especifique explícitamente un valor de dominio deseado como argumento, que evalúa las asignaciones en ese valor.</span><span class="sxs-lookup"><span data-stu-id="c832d-113">Explicitly specify a desired domain value as an argument, which evaluates the maps at that value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c832d-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c832d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c832d-115">Referencia de evaluadores</span><span class="sxs-lookup"><span data-stu-id="c832d-115">Evaluators Reference</span></span>](evaluators-reference.md)
</dt> </dl>

 

 




