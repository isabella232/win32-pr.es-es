---
title: Obtención de información de estado
description: Obtención de información de estado
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL, información de estado
- OpenGL, variables de estado
- información de estado OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfac92233e971104fd4d343970a9ecc79496ed54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775253"
---
# <a name="obtaining-state-information"></a><span data-ttu-id="6e031-106">Obtención de información de estado</span><span class="sxs-lookup"><span data-stu-id="6e031-106">Obtaining State Information</span></span>

<span data-ttu-id="6e031-107">OpenGL mantiene muchas variables de estado que afectan al comportamiento de muchas funciones.</span><span class="sxs-lookup"><span data-stu-id="6e031-107">OpenGL maintains many state variables that affect the behavior of many functions.</span></span> <span data-ttu-id="6e031-108">Algunas de estas variables tienen funciones de consulta especializadas.</span><span class="sxs-lookup"><span data-stu-id="6e031-108">Some of these variables have specialized query functions.</span></span>



|                                          |                                                    |                                                          |
|------------------------------------------|----------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="6e031-109">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="6e031-109">**glGetClipPlane**</span></span>](glgetclipplane.md) | [<span data-ttu-id="6e031-110">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="6e031-110">**glGetPixelMap**</span></span>](glgetpixelmap.md)             | [<span data-ttu-id="6e031-111">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="6e031-111">**glGetTexImage**</span></span>](glgetteximage.md)                   |
| [<span data-ttu-id="6e031-112">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="6e031-112">**glGetLight**</span></span>](glgetlight.md)         | [<span data-ttu-id="6e031-113">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="6e031-113">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md) | [<span data-ttu-id="6e031-114">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="6e031-114">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |
| [<span data-ttu-id="6e031-115">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="6e031-115">**glGetMap**</span></span>](glgetmap.md)             | [<span data-ttu-id="6e031-116">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="6e031-116">**glGetTexEnv**</span></span>](glgettexenv.md)                 | [<span data-ttu-id="6e031-117">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="6e031-117">**glGetTexParameter**</span></span>](glgettexparameter.md)           |
| [<span data-ttu-id="6e031-118">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="6e031-118">**glGetMaterial**</span></span>](glgetmaterial.md)   | [<span data-ttu-id="6e031-119">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="6e031-119">**glGetTexGen**</span></span>](glgettexgen.md)                 |                                                          |



 

<span data-ttu-id="6e031-120">Para obtener el valor de otras variables de estado, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md)o [**glGetIntegerv**](glgetintegerv.md), según corresponda.</span><span class="sxs-lookup"><span data-stu-id="6e031-120">To obtain the value of other state variables, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md), or [**glGetIntegerv**](glgetintegerv.md), as appropriate.</span></span> <span data-ttu-id="6e031-121">Consulte [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para obtener información sobre cómo usar estas funciones.</span><span class="sxs-lookup"><span data-stu-id="6e031-121">See [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) for information about how to use these functions.</span></span> <span data-ttu-id="6e031-122">Otras funciones de consulta que podría querer usar son [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md)y [**glIsEnabled**](glisenabled.md).</span><span class="sxs-lookup"><span data-stu-id="6e031-122">Other query functions you might want to use are [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md), and [**glIsEnabled**](glisenabled.md).</span></span> <span data-ttu-id="6e031-123">(Consulte [control de errores](handling-errors.md) para obtener más información acerca de las funciones relacionadas con el control de errores). Para guardar y restaurar conjuntos de variables de estado, use [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="6e031-123">(See [Handling Errors](handling-errors.md) for more information about functions related to error handling.) To save and restore sets of state variables, use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

-   [<span data-ttu-id="6e031-124">Usar las funciones de consulta</span><span class="sxs-lookup"><span data-stu-id="6e031-124">Using the Query Functions</span></span>](using-the-query-functions.md)
-   [<span data-ttu-id="6e031-125">Tratamiento de errores</span><span class="sxs-lookup"><span data-stu-id="6e031-125">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="6e031-126">Códigos de error de OpenGL</span><span class="sxs-lookup"><span data-stu-id="6e031-126">OpenGL Error Codes</span></span>](opengl-error-codes.md)
-   [<span data-ttu-id="6e031-127">Guardar y restaurar conjuntos de variables de estado</span><span class="sxs-lookup"><span data-stu-id="6e031-127">Saving and Restoring Sets of State Variables</span></span>](saving-and-restoring-sets-of-state-variables.md)
-   [<span data-ttu-id="6e031-128">Variables de estado de OpenGL</span><span class="sxs-lookup"><span data-stu-id="6e031-128">OpenGL State Variables</span></span>](opengl-state-variables.md)
-   [<span data-ttu-id="6e031-129">Referencia de información de estado</span><span class="sxs-lookup"><span data-stu-id="6e031-129">State Information Reference</span></span>](state-information-reference.md)

 

 




