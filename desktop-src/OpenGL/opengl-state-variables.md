---
title: Variables de estado de OpenGL
description: En los temas siguientes se enumeran los nombres de las variables de estado que se pueden consultar
ms.assetid: f4bc4ec1-a529-4b9e-84af-94caa0ef7131
keywords:
- Variables de estado de OpenGL
- variables de estado, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36dee51ba7726277832d94eaf336d03d3c579189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665652"
---
# <a name="opengl-state-variables"></a><span data-ttu-id="c90ef-105">Variables de estado de OpenGL</span><span class="sxs-lookup"><span data-stu-id="c90ef-105">OpenGL State Variables</span></span>

<span data-ttu-id="c90ef-106">En los temas siguientes se enumeran los nombres de las variables de estado que se pueden consultar:</span><span class="sxs-lookup"><span data-stu-id="c90ef-106">The following topics list the names of state variables that can be queried:</span></span>

-   [<span data-ttu-id="c90ef-107">**Variables de estado para los valores actuales y los datos asociados**</span><span class="sxs-lookup"><span data-stu-id="c90ef-107">**State Variables for Current Values and Associated Data**</span></span>](state-variables-for-current-values-and-associated-data.md)
-   [<span data-ttu-id="c90ef-108">**Variables de estado de transformación**</span><span class="sxs-lookup"><span data-stu-id="c90ef-108">**Transformation State Variables**</span></span>](transformation-state-variables.md)
-   [<span data-ttu-id="c90ef-109">**Colorear variables de estado**</span><span class="sxs-lookup"><span data-stu-id="c90ef-109">**Coloring State Variables**</span></span>](coloring-state-variables.md)
-   [<span data-ttu-id="c90ef-110">**Variables de estado de iluminación**</span><span class="sxs-lookup"><span data-stu-id="c90ef-110">**Lighting State Variables**</span></span>](lighting-state-variables.md)
-   [<span data-ttu-id="c90ef-111">**Variables de estado de rasterización**</span><span class="sxs-lookup"><span data-stu-id="c90ef-111">**Rasterization State Variables**</span></span>](rasterization-state-variables.md)
-   [<span data-ttu-id="c90ef-112">**Variables de estado de texturización**</span><span class="sxs-lookup"><span data-stu-id="c90ef-112">**Texturing State Variables**</span></span>](texturing-state-variables.md)
-   [<span data-ttu-id="c90ef-113">**Operaciones de píxeles**</span><span class="sxs-lookup"><span data-stu-id="c90ef-113">**Pixel Operations**</span></span>](pixel-operations.md)
-   [<span data-ttu-id="c90ef-114">**Variables de estado del control fotogramas**</span><span class="sxs-lookup"><span data-stu-id="c90ef-114">**Framebuffer Control State Variables**</span></span>](framebuffer-control-state-variables.md)
-   [<span data-ttu-id="c90ef-115">**Variables de estado de píxeles**</span><span class="sxs-lookup"><span data-stu-id="c90ef-115">**Pixel State Variables**</span></span>](pixel-state-variables.md)
-   [<span data-ttu-id="c90ef-116">**Variables de estado del evaluador**</span><span class="sxs-lookup"><span data-stu-id="c90ef-116">**Evaluator State Variables**</span></span>](evaluator-state-variables.md)
-   [<span data-ttu-id="c90ef-117">**Variables de estado de sugerencia**</span><span class="sxs-lookup"><span data-stu-id="c90ef-117">**Hint State Variables**</span></span>](hint-state-variables.md)
-   [<span data-ttu-id="c90ef-118">**Variables de estado dependiente de la implementación**</span><span class="sxs-lookup"><span data-stu-id="c90ef-118">**Implementation-Dependent State Variables**</span></span>](implementation-dependent-state-variables.md)
-   [<span data-ttu-id="c90ef-119">**Variables de estado de Pixel-Depth dependiente de la implementación**</span><span class="sxs-lookup"><span data-stu-id="c90ef-119">**Implementation-Dependent Pixel-Depth State Variables**</span></span>](implementation-dependent-pixel-depth-state-variables.md)
-   [<span data-ttu-id="c90ef-120">**Variables de estado misceláneas**</span><span class="sxs-lookup"><span data-stu-id="c90ef-120">**Miscellaneous State Variables**</span></span>](miscellaneous-state-variables.md)

<span data-ttu-id="c90ef-121">Para cada variable, en el tema se muestra una descripción, un grupo de atributos, un valor inicial o mínimo y la función [**glGet \***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) sugerida que se va a usar para obtenerlo.</span><span class="sxs-lookup"><span data-stu-id="c90ef-121">For each variable, the topic lists a description, attribute group, initial or minimum value, and the suggested [**glGet\***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) function to use for obtaining it.</span></span>

<span data-ttu-id="c90ef-122">Las variables de estado que puede obtener con [**glGetBooleanv**](glgetbooleanv.md), [**glGetIntegerv**](glgetintegerv.md), [**glGetFloatv**](glgetfloatv.md)o [**glGetDoublev**](glgetdoublev.md) se enumeran solo con uno de estos functionsthe, que es más adecuado para el tipo de datos que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="c90ef-122">State variables that you can obtain using [**glGetBooleanv**](glgetbooleanv.md), [**glGetIntegerv**](glgetintegerv.md), [**glGetFloatv**](glgetfloatv.md), or [**glGetDoublev**](glgetdoublev.md) are listed with just one of these functionsthe one that is most appropriate for the type of data to be returned.</span></span> <span data-ttu-id="c90ef-123">No se pueden obtener estas variables de estado mediante [**glIsEnabled**](glisenabled.md).</span><span class="sxs-lookup"><span data-stu-id="c90ef-123">You cannot obtain these state variables using [**glIsEnabled**](glisenabled.md).</span></span> <span data-ttu-id="c90ef-124">Sin embargo, puede obtener las variables de estado para las que **glIsEnabled** aparece como la función de consulta con **glGetBooleanv**, **glGetIntegerv**, **glGetFloatv** y **glGetDoublev**.</span><span class="sxs-lookup"><span data-stu-id="c90ef-124">However, you can obtain state variables for which **glIsEnabled** is listed as the query function with **glGetBooleanv**, **glGetIntegerv**, **glGetFloatv**, and **glGetDoublev**.</span></span> <span data-ttu-id="c90ef-125">Puede obtener las variables de estado para las que cualquier otra función aparece como la función de consulta solo mediante esa función.</span><span class="sxs-lookup"><span data-stu-id="c90ef-125">You can obtain state variables for which any other function is listed as the query function only by using that function.</span></span> <span data-ttu-id="c90ef-126">Si no aparece ningún grupo de atributos, la variable no pertenece a ningún grupo.</span><span class="sxs-lookup"><span data-stu-id="c90ef-126">If no attribute group is listed, the variable doesn't belong to any group.</span></span> <span data-ttu-id="c90ef-127">Todas las variables de estado que puede consultar, excepto las que dependen de la implementación, tienen valores iniciales.</span><span class="sxs-lookup"><span data-stu-id="c90ef-127">All state variables that you can query, except those that are implementation dependent, have initial values.</span></span> <span data-ttu-id="c90ef-128">Para determinar el valor inicial de una variable para la que no aparece ningún valor inicial, vea la referencia de la variable o el</span><span class="sxs-lookup"><span data-stu-id="c90ef-128">To determine the initial value of a variable for which no initial value is listed, see that variable's reference or the</span></span>

<span data-ttu-id="c90ef-129">*Manual de referencia de OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="c90ef-129">*OpenGL Reference Manual*.</span></span>

 

 




