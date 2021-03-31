---
title: Trasladar objetos de NURBS
description: OpenGL trata a NURBS como objetos, de forma similar al modo en que trata Quadrics crea un objeto NURBS y, a continuación, especifica cómo se debe representar. En la tabla siguiente se enumeran las funciones de OpenGL GLU para administrar objetos de NURBS.
ms.assetid: baddf81b-219f-44bb-aa17-37404028b258
keywords:
- Migración de GL de IRIS, objetos de NURBS
- portabilidad de IRIS GL, objetos de NURBS
- trasladar a OpenGL desde IRIS GL, objetos de NURBS
- Exportación de OpenGL desde IRIS GL, objetos de NURBS
- Objetos NURBS
- NURBS (no uniforme, B-spline racional)
- B-spline racional no uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0e56c06eea4e4a9a48f9062205277f8b999499
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418877"
---
# <a name="porting-nurbs-objects"></a><span data-ttu-id="ac577-111">Trasladar objetos de NURBS</span><span class="sxs-lookup"><span data-stu-id="ac577-111">Porting NURBS Objects</span></span>

<span data-ttu-id="ac577-112">OpenGL trata a NURBS como objetos, de forma similar al modo en que trata Quadrics: se crea un objeto NURBS y, a continuación, se especifica cómo se debe representar.</span><span class="sxs-lookup"><span data-stu-id="ac577-112">OpenGL treats NURBS as objects, similar to the way it treats quadrics: you create a NURBS object and then specify how it should be rendered.</span></span> <span data-ttu-id="ac577-113">En la tabla siguiente se enumeran las funciones de OpenGL GLU para administrar objetos de NURBS.</span><span class="sxs-lookup"><span data-stu-id="ac577-113">The following table lists the OpenGL GLU functions for managing NURBS objects.</span></span>



| <span data-ttu-id="ac577-114">Función GLU de OpenGL</span><span class="sxs-lookup"><span data-stu-id="ac577-114">OpenGL GLU function</span></span>                                      | <span data-ttu-id="ac577-115">Significado</span><span class="sxs-lookup"><span data-stu-id="ac577-115">Meaning</span></span>                                                        |
|----------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="ac577-116">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="ac577-116">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)       | <span data-ttu-id="ac577-117">Crea un nuevo objeto NURBS.</span><span class="sxs-lookup"><span data-stu-id="ac577-117">Creates a new NURBS object.</span></span>                                    |
| [<span data-ttu-id="ac577-118">**gluDeleteNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="ac577-118">**gluDeleteNurbsRenderer**</span></span>](gludeletenurbsrenderer.md) | <span data-ttu-id="ac577-119">Elimina un objeto NURBS.</span><span class="sxs-lookup"><span data-stu-id="ac577-119">Deletes a NURBS object.</span></span>                                        |
| [<span data-ttu-id="ac577-120">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="ac577-120">*gluNurbsCallback*</span></span>](glunurbs.md)                       | <span data-ttu-id="ac577-121">Asocia una devolución de llamada a un objeto NURBS para el control de errores.</span><span class="sxs-lookup"><span data-stu-id="ac577-121">Associates a callback with a NURBS object, for error handling.</span></span> |



 

<span data-ttu-id="ac577-122">Al migrar el código NURBS de GL de IRIS a OpenGL, tenga en cuenta los puntos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ac577-122">When porting IRIS GL NURBS code to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="ac577-123">Los puntos de control de NURBS son Float, no dobles.</span><span class="sxs-lookup"><span data-stu-id="ac577-123">NURBS control points are floats, not doubles.</span></span>
-   <span data-ttu-id="ac577-124">El parámetro STRIDE se cuenta en Float, no en bytes.</span><span class="sxs-lookup"><span data-stu-id="ac577-124">The stride parameter is counted in floats, not bytes.</span></span>
-   <span data-ttu-id="ac577-125">Si usa la iluminación y no está especificando las normales, llame a [**glEnable**](glenable.md) con GL \_ auto \_ normal como parámetro para generar las normales automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ac577-125">If you're using lighting and you're not specifying normals, call [**glEnable**](glenable.md) with GL\_AUTO\_NORMAL as the parameter to generate normals automatically.</span></span>

<span data-ttu-id="ac577-126">??</span><span class="sxs-lookup"><span data-stu-id="ac577-126">??</span></span>

 

 




