---
title: Usar las funciones de consulta
description: Usar las funciones de consulta
ms.assetid: 5f874a0e-77c0-4009-a18f-a852d7ffe891
keywords:
- OpenGL, funciones de consulta
- funciones de consulta OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14804b260451d4b51b0146b1cb2f796ba6b6778e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665666"
---
# <a name="using-the-query-functions"></a><span data-ttu-id="136d3-105">Usar las funciones de consulta</span><span class="sxs-lookup"><span data-stu-id="136d3-105">Using the Query Functions</span></span>

<span data-ttu-id="136d3-106">Hay cuatro funciones de consulta para obtener variables de estado simples y otra para determinar si un estado determinado está habilitado o deshabilitado:</span><span class="sxs-lookup"><span data-stu-id="136d3-106">There are four query functions for obtaining simple state variables and one for determining whether a particular state is enabled or disabled:</span></span>

-   [<span data-ttu-id="136d3-107">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="136d3-107">**glGetBooleanv**</span></span>](glgetbooleanv.md)
-   [<span data-ttu-id="136d3-108">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="136d3-108">**glGetIntegerv**</span></span>](glgetintegerv.md)
-   [<span data-ttu-id="136d3-109">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="136d3-109">**glGetFloatv**</span></span>](glgetfloatv.md)
-   [<span data-ttu-id="136d3-110">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="136d3-110">**glGetDoublev**</span></span>](glgetdoublev.md)
-   [<span data-ttu-id="136d3-111">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="136d3-111">**glIsEnabled**</span></span>](glisenabled.md)

<span data-ttu-id="136d3-112">Los prototipos de las funciones de consulta son:</span><span class="sxs-lookup"><span data-stu-id="136d3-112">The prototypes for the query functions are:</span></span>

<span data-ttu-id="136d3-113">**void** **glGetBooleanv**(**GLenum** *PName* , **GLboolean \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="136d3-113">**void** **glGetBooleanv**(**GLenum** *pname* , **GLboolean \*** *params* );</span></span>

<span data-ttu-id="136d3-114">**void** **glGetIntegerv**(**GLenum** *PName* , **GLint \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="136d3-114">**void** **glGetIntegerv**(**GLenum** *pname* , **GLint \*** *params* );</span></span>

<span data-ttu-id="136d3-115">**void** **glGetFloatv**(**GLenum** *PName* , **GLfloat \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="136d3-115">**void** **glGetFloatv**(**GLenum** *pname* , **GLfloat \*** *params* );</span></span>

<span data-ttu-id="136d3-116">**void** **glGetDoublev**(**GLenum** *PName* , **GLdouble \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="136d3-116">**void** **glGetDoublev**(**GLenum** *pname* , **GLdouble \*** *params* );</span></span>

<span data-ttu-id="136d3-117">Respectivamente, las funciones de consulta obtienen variables de estado Boolean, integer, de punto flotante o de doble precisión.</span><span class="sxs-lookup"><span data-stu-id="136d3-117">Respectively, the query functions obtain Boolean, integer, floating-point, or double-precision state variables.</span></span> <span data-ttu-id="136d3-118">El parámetro *PName* es una constante simbólica que indica la variable de estado que se va a devolver y *params* es un puntero a una matriz del tipo indicado en el que se colocan los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="136d3-118">The *pname* parameter is a symbolic constant indicating the state variable to return, and *params* is a pointer to an array of the indicated type in which to place the returned data.</span></span> <span data-ttu-id="136d3-119">Los valores posibles de *PName* se enumeran en [variables de estado de OpenGL](opengl-state-variables.md).</span><span class="sxs-lookup"><span data-stu-id="136d3-119">The possible values for *pname* are listed in [OpenGL State Variables](opengl-state-variables.md).</span></span> <span data-ttu-id="136d3-120">Si es necesario, se realiza una conversión de tipos para devolver la variable deseada como el tipo de datos solicitado.</span><span class="sxs-lookup"><span data-stu-id="136d3-120">A type conversion is performed if necessary to return the desired variable as the requested data type.</span></span>

<span data-ttu-id="136d3-121">El prototipo para [**glIsEnabled**](glisenabled.md) es:</span><span class="sxs-lookup"><span data-stu-id="136d3-121">The prototype for [**glIsEnabled**](glisenabled.md) is:</span></span>

<span data-ttu-id="136d3-122">**GLboolean** **glIsEnabled**(GLenum *Cap* );</span><span class="sxs-lookup"><span data-stu-id="136d3-122">**GLboolean** **glIsEnabled**(GLenum *cap* );</span></span>

<span data-ttu-id="136d3-123">Si el modo especificado por *Cap* está habilitado, **glIsEnabled** devuelve GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="136d3-123">If the mode specified by *cap* is enabled, **glIsEnabled** returns GL\_TRUE.</span></span> <span data-ttu-id="136d3-124">Si el modo especificado por *Cap* está deshabilitado, **glIsEnabled** devuelve GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="136d3-124">If the mode specified by *cap* is disabled, **glIsEnabled** returns GL\_FALSE.</span></span> <span data-ttu-id="136d3-125">Los valores posibles para *Cap* se enumeran en [variables de estado de OpenGL](opengl-state-variables.md).</span><span class="sxs-lookup"><span data-stu-id="136d3-125">The possible values for *cap* are listed in [OpenGL State Variables](opengl-state-variables.md).</span></span>

<span data-ttu-id="136d3-126">Otras funciones especializadas devuelven variables de estado específicas.</span><span class="sxs-lookup"><span data-stu-id="136d3-126">Other specialized functions return specific state variables.</span></span> <span data-ttu-id="136d3-127">Para averiguar cuándo usar estas funciones, consulte las variables de estado de OpenGL y el *manual de referencia de OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="136d3-127">To find out when to use these functions, see OpenGL State Variables and the *OpenGL Reference Manual*.</span></span> <span data-ttu-id="136d3-128">Para obtener más información sobre la funcionalidad de control de errores de OpenGL y la función **glGetError** , vea [control de errores](error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="136d3-128">For more information on OpenGL's error handling facility and the **glGetError** function, see [Error Handling](error-handling.md).</span></span>

<span data-ttu-id="136d3-129">Las funciones que devuelven variables de estado específicas son:</span><span class="sxs-lookup"><span data-stu-id="136d3-129">The functions that return specific state variables are:</span></span>

-   [<span data-ttu-id="136d3-130">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="136d3-130">**glGetClipPlane**</span></span>](glgetclipplane.md)
-   [<span data-ttu-id="136d3-131">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="136d3-131">**glGetError**</span></span>](glgeterror.md)
-   [<span data-ttu-id="136d3-132">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="136d3-132">**glGetLight**</span></span>](glgetlight.md)
-   [<span data-ttu-id="136d3-133">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="136d3-133">**glGetMap**</span></span>](glgetmap.md)
-   [<span data-ttu-id="136d3-134">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="136d3-134">**glGetMaterial**</span></span>](glgetmaterial.md)
-   [<span data-ttu-id="136d3-135">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="136d3-135">**glGetPixelMap**</span></span>](glgetpixelmap.md)
-   [<span data-ttu-id="136d3-136">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="136d3-136">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
-   [<span data-ttu-id="136d3-137">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="136d3-137">**glGetString**</span></span>](glgetstring.md)
-   [<span data-ttu-id="136d3-138">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="136d3-138">**glGetTexEnv**</span></span>](glgettexenv.md)
-   [<span data-ttu-id="136d3-139">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="136d3-139">**glGetTexGen**</span></span>](glgettexgen.md)
-   [<span data-ttu-id="136d3-140">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="136d3-140">**glGetTexImage**</span></span>](glgetteximage.md)
-   [<span data-ttu-id="136d3-141">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="136d3-141">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
-   [<span data-ttu-id="136d3-142">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="136d3-142">**glGetTexParameter**</span></span>](glgettexparameter.md)

 

 




