---
title: Transformar coordenadas
description: La biblioteca de utilidades OpenGL (GLU) proporciona varias funciones de transformación de matriz de uso frecuente.
ms.assetid: 9ca32be8-3bc0-4fca-a58c-69a4800c3c55
keywords:
- Utilidad OpenGL (GLU), funciones de transformación de matriz
- GLU (utilidad OpenGL), funciones de transformación de matriz
- funciones de transformación de matriz OpenGL
- Utilidad OpenGL (GLU), transformar coordenadas
- GLU (utilidad OpenGL), transformar coordenadas
- transformación de coordenadas OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a5a58c723dcccfc54ce2f47a01710133ccc30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779471"
---
# <a name="transforming-coordinates"></a><span data-ttu-id="51883-109">Transformar coordenadas</span><span class="sxs-lookup"><span data-stu-id="51883-109">Transforming Coordinates</span></span>

<span data-ttu-id="51883-110">La biblioteca de utilidades OpenGL (GLU) proporciona varias funciones de transformación de matriz de uso frecuente.</span><span class="sxs-lookup"><span data-stu-id="51883-110">The OpenGL Utility library (GLU) provides several commonly used matrix transformation functions.</span></span> <span data-ttu-id="51883-111">Puede configurar una región de visualización ortográfica bidimensional con [**gluOrtho2D**](gluortho2d.md), un volumen de vista de perspectiva estándar con [**gluPerspective**](gluperspective.md), o un volumen de vista centrado en un eyepoint especificado con [**gluLookAt**](glulookat.md).</span><span class="sxs-lookup"><span data-stu-id="51883-111">You can set up a two-dimensional orthographic viewing region with [**gluOrtho2D**](gluortho2d.md), a standard perspective view volume using [**gluPerspective**](gluperspective.md), or a view volume that is centered on a specified eyepoint with [**gluLookAt**](glulookat.md).</span></span> <span data-ttu-id="51883-112">Cada una de estas funciones crea la matriz deseada y la aplica a la matriz actual mediante [**glMultMatrix**](glmultmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="51883-112">Each of these functions creates the desired matrix and applies it to the current matrix using [**glMultMatrix**](glmultmatrix.md).</span></span>

<span data-ttu-id="51883-113">La función [**gluPickMatrix**](glupickmatrix.md) simplifica la selección de una matriz de picking mediante la creación de una matriz que restringe el dibujo a una región pequeña de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="51883-113">The [**gluPickMatrix**](glupickmatrix.md) function simplifies selection of a picking matrix by creating a matrix that restricts drawing to a small region of the viewport.</span></span> <span data-ttu-id="51883-114">Si vuelve a representar la escena en el modo de selección después de aplicar esta matriz, se seleccionarán todos los objetos que se dibujen cerca del cursor y la información sobre ellos se almacenará en el búfer de selección.</span><span class="sxs-lookup"><span data-stu-id="51883-114">If you re-render the scene in selection mode after this matrix has been applied, all objects that would be drawn near the cursor will be selected, and information about them will be stored in the selection buffer.</span></span> <span data-ttu-id="51883-115">Para obtener más información sobre el modo de selección, vea el tema sobre cómo realizar [la selección y los comentarios.](performing-selection-and-feedback.md)</span><span class="sxs-lookup"><span data-stu-id="51883-115">For more information about selection mode, see "Performing Selection and Feedback" [Performing Selection and Feedback](performing-selection-and-feedback.md).</span></span>

<span data-ttu-id="51883-116">Para determinar dónde se dibuja un objeto en la ventana, use [**gluProject**](gluproject.md), que convierte las coordenadas del objeto especificado *objx*, *objy* y *Objz* en coordenadas de la ventana mediante *modelMatrix*, *projMatrix* y *viewport*.</span><span class="sxs-lookup"><span data-stu-id="51883-116">To determine where in the window an object is being drawn, use [**gluProject**](gluproject.md), which converts the specified object coordinates *objx*, *objy*, and *objz* into window coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="51883-117">El resultado se almacena en *Winx*, *Winy* y *Winz*.</span><span class="sxs-lookup"><span data-stu-id="51883-117">The result is stored in *winx*, *winy*, and *winz*.</span></span> <span data-ttu-id="51883-118">Si la función se ejecuta correctamente, el valor devuelto es GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="51883-118">If the function succeeds, the return value is GL\_TRUE.</span></span> <span data-ttu-id="51883-119">Si se produce un error en la función, el valor devuelto es GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="51883-119">If the function fails, the return value is GL\_FALSE.</span></span>

<span data-ttu-id="51883-120">La función [**gluUnProject**](gluunproject.md) realiza la conversión inversa: transforma las coordenadas de ventana especificadas *Winx*, *Winy* y *Winz* en coordenadas de objeto mediante *modelMatrix*, *projMatrix* y *viewport*.</span><span class="sxs-lookup"><span data-stu-id="51883-120">The [**gluUnProject**](gluunproject.md) function performs the inverse conversion: it transforms the specified window coordinates *winx*, *winy*, and *winz* into object coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="51883-121">El resultado se almacena en *objx*, *objy* y *objz*.</span><span class="sxs-lookup"><span data-stu-id="51883-121">The result is stored in *objx*, *objy*, and *objz*.</span></span> <span data-ttu-id="51883-122">Si la función se ejecuta correctamente, el valor devuelto es GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="51883-122">If the function succeeds, the return value is GL\_TRUE.</span></span> <span data-ttu-id="51883-123">Si se produce un error en la función, el valor devuelto es GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="51883-123">If the function fails, the return value is GL\_FALSE.</span></span>

 

 




