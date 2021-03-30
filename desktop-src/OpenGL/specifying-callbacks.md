---
title: Especificar devoluciones de llamada
description: Puede especificar hasta cinco funciones de devolución de llamada para una teselación.
ms.assetid: b49a8400-8111-450d-a2d7-c313a898a213
keywords:
- Utilidad OpenGL (GLU), especificar funciones de devolución de llamada
- GLU (utilidad OpenGL), especificar funciones de devolución de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6086448cf6f4a71ea6a49359d5656f12f613d760
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532415"
---
# <a name="specifying-callbacks"></a><span data-ttu-id="98c7c-105">Especificar devoluciones de llamada</span><span class="sxs-lookup"><span data-stu-id="98c7c-105">Specifying Callbacks</span></span>

<span data-ttu-id="98c7c-106">Puede especificar hasta cinco funciones de devolución de llamada para una teselación.</span><span class="sxs-lookup"><span data-stu-id="98c7c-106">You can specify up to five callback functions for a tessellation.</span></span> <span data-ttu-id="98c7c-107">No se llama a las funciones que no se especifican durante la teselación y no se obtiene ninguna información que puedan haber devuelto.</span><span class="sxs-lookup"><span data-stu-id="98c7c-107">Any functions that you do not specify are not called during the tessellation, and you do not get any information they might have returned.</span></span> <span data-ttu-id="98c7c-108">Las funciones de devolución de llamada se especifican con [*gluTessCallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="98c7c-108">You specify the callback functions with [*gluTessCallback*](glutess.md).</span></span>

<span data-ttu-id="98c7c-109">La función **gluTessCallback** asocia la función de devolución de llamada *FN* con el objeto de teselación *tessobj*.</span><span class="sxs-lookup"><span data-stu-id="98c7c-109">The **gluTessCallback** function associates the callback function *fn* with the tessellation object *tessobj*.</span></span> <span data-ttu-id="98c7c-110">El tipo de la devolución de llamada viene determinado por el *tipo* de parámetro, que puede ser **Glu \_ Begin**, **Glu \_ Edge \_ Flag**, **Glu \_ Vertex**, **Glu \_ End** o **Glu \_ error**.</span><span class="sxs-lookup"><span data-stu-id="98c7c-110">The type of the callback is determined by the parameter *type*, which can be **GLU\_BEGIN**, **GLU\_EDGE\_FLAG**, **GLU\_VERTEX**, **GLU\_END**, or **GLU\_ERROR**.</span></span> <span data-ttu-id="98c7c-111">Las cinco funciones de devolución de llamada posibles tienen los siguientes prototipos.</span><span class="sxs-lookup"><span data-stu-id="98c7c-111">The five possible callback functions have the following prototypes.</span></span>



| <span data-ttu-id="98c7c-112">Función de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="98c7c-112">Callback function</span></span>   | <span data-ttu-id="98c7c-113">Prototipo</span><span class="sxs-lookup"><span data-stu-id="98c7c-113">Prototype</span></span>                                    |
|---------------------|----------------------------------------------|
| <span data-ttu-id="98c7c-114">**Inicio de GLU \_**</span><span class="sxs-lookup"><span data-stu-id="98c7c-114">**GLU\_BEGIN**</span></span>      | <span data-ttu-id="98c7c-115">**void** **Begin**(\*\*GLenum \* \*\* \*);</span><span class="sxs-lookup"><span data-stu-id="98c7c-115">**void** **begin**(\**GLenum\*\*\*type* );</span></span>       |
| <span data-ttu-id="98c7c-116">**\_marca de borde Glu \_**</span><span class="sxs-lookup"><span data-stu-id="98c7c-116">**GLU\_EDGE\_FLAG**</span></span> | <span data-ttu-id="98c7c-117">**void** **EdgeFlag**(\*\*GLboolean \*\* \* \*);</span><span class="sxs-lookup"><span data-stu-id="98c7c-117">**void** **edgeFlag**(\**GLboolean\*\*\*flag* );</span></span> |
| <span data-ttu-id="98c7c-118">**\_vértice Glu**</span><span class="sxs-lookup"><span data-stu-id="98c7c-118">**GLU\_VERTEX**</span></span>     | <span data-ttu-id="98c7c-119">**void** **Vertex**(\**void \* \* \* \* Data* );</span><span class="sxs-lookup"><span data-stu-id="98c7c-119">**void** **vertex**(\**void \*\*\*\*data* );</span></span>     |
| <span data-ttu-id="98c7c-120">**final de GLU \_**</span><span class="sxs-lookup"><span data-stu-id="98c7c-120">**GLU\_END**</span></span>        | <span data-ttu-id="98c7c-121">**void** **End**( *void* );</span><span class="sxs-lookup"><span data-stu-id="98c7c-121">**void** **end**( *void* );</span></span>                  |
| <span data-ttu-id="98c7c-122">**\_error Glu**</span><span class="sxs-lookup"><span data-stu-id="98c7c-122">**GLU\_ERROR**</span></span>      | <span data-ttu-id="98c7c-123"> **error** void \(**GLenum\ *\ * errno* );</span><span class="sxs-lookup"><span data-stu-id="98c7c-123">**void** **error**(\**GLenum\*\*\*errno* );</span></span>      |



 

<span data-ttu-id="98c7c-124">Para cambiar una función de devolución de llamada, llame a [*gluTessCallback*](glutess.md) con la nueva función.</span><span class="sxs-lookup"><span data-stu-id="98c7c-124">To change a callback function, call [*gluTessCallback*](glutess.md) with the new function.</span></span> <span data-ttu-id="98c7c-125">Para eliminar una función de devolución de llamada sin reemplazarla por una nueva, pase **gluTessCallback** un puntero NULL para la función adecuada.</span><span class="sxs-lookup"><span data-stu-id="98c7c-125">To eliminate a callback function without replacing it with a new one, pass **gluTessCallback** a null pointer for the appropriate function.</span></span>

<span data-ttu-id="98c7c-126">A medida que la teselación continúa, se llama a las funciones de devolución de llamada de forma similar a como se haría con las funciones de OpenGL [**glBegin**](glbegin.md), [glEdgeFlag](gledgeflag-functions.md), [glVertex](glvertex-functions.md)y [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="98c7c-126">As tessellation proceeds, the callback functions are called in a manner similar to the way you would use the OpenGL functions [**glBegin**](glbegin.md), [glEdgeFlag](gledgeflag-functions.md), [glVertex](glvertex-functions.md), and [**glEnd**](glend.md).</span></span>

<span data-ttu-id="98c7c-127">La función de devolución de llamada de **\_ Inicio Glu** se invoca con uno de los tres parámetros posibles:</span><span class="sxs-lookup"><span data-stu-id="98c7c-127">The **GLU\_BEGIN** callback function is invoked with one of three possible parameters:</span></span>

-   <span data-ttu-id="98c7c-128">\_ventilador de triángulo GL \_</span><span class="sxs-lookup"><span data-stu-id="98c7c-128">GL\_TRIANGLE\_FAN</span></span>
-   <span data-ttu-id="98c7c-129">\_franja de triángulo de GL \_</span><span class="sxs-lookup"><span data-stu-id="98c7c-129">GL\_TRIANGLE\_STRIP</span></span>
-   <span data-ttu-id="98c7c-130">triángulos de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="98c7c-130">GL\_TRIANGLES</span></span>

<span data-ttu-id="98c7c-131">Después de llamar a la función de devolución de llamada de **\_ Inicio de Glu** y antes de llamar a la función de devolución de llamada asociada al **\_ extremo de Glu**, se invoca una combinación de las devoluciones de llamada **\_ perimetral Glu \_** y **Glu \_ Vertex** .</span><span class="sxs-lookup"><span data-stu-id="98c7c-131">After calling the **GLU\_BEGIN** callback function, and before calling the callback function associated with **GLU\_END**, some combination of the **GLU\_EDGE\_FLAG** and **GLU\_VERTEX** callbacks is invoked.</span></span> <span data-ttu-id="98c7c-132">Los vértices asociados y las marcas de borde se interpretan exactamente como están en OpenGL entre **glBegin**(fan triangular GL \_ \_ ), **glBegin**(franja triangular de GL \_ \_ ) o **glBegin**( \_ triángulos de contabilidad **)** y la **glEnd** coincidente.</span><span class="sxs-lookup"><span data-stu-id="98c7c-132">The associated vertices and edge flags are interpreted exactly as they are in OpenGL between **glBegin**(GL\_TRIANGLE\_FAN), **glBegin**(GL\_TRIANGLE\_STRIP), or **glBegin**(GL\_TRIANGLES **)** and the matching **glEnd**.</span></span>

<span data-ttu-id="98c7c-133">Dado que las marcas de borde no tienen sentido en un ventilador de triángulo o en una franja de triángulo, si hay una función de devolución de llamada asociada con la **\_ \_ marca de borde de Glu**, la devolución de llamada de **\_ Inicio de Glu** solo se llama con **\_ triángulos de contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="98c7c-133">Because edge flags make no sense in a triangle fan or triangle strip, if there is a callback function associated with **GLU\_EDGE\_FLAG**, the **GLU\_BEGIN** callback is called only with **GL\_TRIANGLES**.</span></span> <span data-ttu-id="98c7c-134">La función de devolución de llamada de **\_ \_ marcador perimetral Glu** funciona de forma análoga a la función [glEdgeFlag](gledgeflag-functions.md) de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="98c7c-134">The **GLU\_EDGE\_FLAG** callback function works analogously to the OpenGL [glEdgeFlag](gledgeflag-functions.md) function.</span></span>

<span data-ttu-id="98c7c-135">Si se produce un error durante la teselación, se invoca la función de devolución de llamada de error.</span><span class="sxs-lookup"><span data-stu-id="98c7c-135">If there is an error during the tessellation, the error callback function is invoked.</span></span> <span data-ttu-id="98c7c-136">La función de devolución de llamada de error pasa un número de error GLU.</span><span class="sxs-lookup"><span data-stu-id="98c7c-136">The error callback function is passed a GLU error number.</span></span> <span data-ttu-id="98c7c-137">Puede obtener una cadena de caracteres que describa el error con la función [**gluErrorString**](gluerrorstring.md) .</span><span class="sxs-lookup"><span data-stu-id="98c7c-137">You can obtain a character string describing the error with the [**gluErrorString**](gluerrorstring.md) function.</span></span>

 

 




