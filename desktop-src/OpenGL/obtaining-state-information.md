---
title: Obtener información de estado
description: Obtener información de estado
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL, información de estado
- OpenGL, variables de estado
- información de estado OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8329fd34fc68122be8d63e4dc28756f88faf7797
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120690"
---
# <a name="obtaining-state-information"></a><span data-ttu-id="f0e80-106">Obtener información de estado</span><span class="sxs-lookup"><span data-stu-id="f0e80-106">Obtaining State Information</span></span>

<span data-ttu-id="f0e80-107">OpenGL mantiene muchas variables de estado que afectan al comportamiento de muchas funciones.</span><span class="sxs-lookup"><span data-stu-id="f0e80-107">OpenGL maintains many state variables that affect the behavior of many functions.</span></span> <span data-ttu-id="f0e80-108">Algunas de estas variables tienen funciones de consulta especializadas.</span><span class="sxs-lookup"><span data-stu-id="f0e80-108">Some of these variables have specialized query functions.</span></span>

:::row:::
    :::column:::
        [<span data-ttu-id="f0e80-109">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="f0e80-109">**glGetClipPlane**</span></span>](glgetclipplane.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="f0e80-110">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="f0e80-110">**glGetPixelMap**</span></span>](glgetpixelmap.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="f0e80-111">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="f0e80-111">**glGetTexImage**</span></span>](glgetteximage.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [<span data-ttu-id="f0e80-112">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="f0e80-112">**glGetLight**</span></span>](glgetlight.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="f0e80-113">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="f0e80-113">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="f0e80-114">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="f0e80-114">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [<span data-ttu-id="f0e80-115">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="f0e80-115">**glGetMap**</span></span>](glgetmap.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="f0e80-116">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="f0e80-116">**glGetTexEnv**</span></span>](glgettexenv.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="f0e80-117">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="f0e80-117">**glGetTexParameter**</span></span>](glgettexparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [<span data-ttu-id="f0e80-118">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="f0e80-118">**glGetMaterial**</span></span>](glgetmaterial.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="f0e80-119">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="f0e80-119">**glGetTexGen**</span></span>](glgettexgen.md)
    :::column-end:::
    :::column:::

    :::column-end:::
:::row-end:::

<span data-ttu-id="f0e80-120">Para obtener el valor de otras variables de estado, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md)o [**glGetIntegerv**](glgetintegerv.md), según corresponda.</span><span class="sxs-lookup"><span data-stu-id="f0e80-120">To obtain the value of other state variables, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md), or [**glGetIntegerv**](glgetintegerv.md), as appropriate.</span></span> <span data-ttu-id="f0e80-121">Consulte [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para obtener información sobre cómo usar estas funciones.</span><span class="sxs-lookup"><span data-stu-id="f0e80-121">See [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) for information about how to use these functions.</span></span> <span data-ttu-id="f0e80-122">Otras funciones de consulta que puede usar son [**glGetError,**](glgeterror.md) [**glGetString**](glgetstring.md)y [**glIsEnabled.**](glisenabled.md)</span><span class="sxs-lookup"><span data-stu-id="f0e80-122">Other query functions you might want to use are [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md), and [**glIsEnabled**](glisenabled.md).</span></span> <span data-ttu-id="f0e80-123">(Consulte [Control de errores](handling-errors.md) para obtener más información sobre las funciones relacionadas con el control de errores). Para guardar y restaurar conjuntos de variables de estado, use [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="f0e80-123">(See [Handling Errors](handling-errors.md) for more information about functions related to error handling.) To save and restore sets of state variables, use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

-   [<span data-ttu-id="f0e80-124">Uso de las funciones de consulta</span><span class="sxs-lookup"><span data-stu-id="f0e80-124">Using the Query Functions</span></span>](using-the-query-functions.md)
-   [<span data-ttu-id="f0e80-125">Tratamiento de errores</span><span class="sxs-lookup"><span data-stu-id="f0e80-125">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="f0e80-126">Códigos de error de OpenGL</span><span class="sxs-lookup"><span data-stu-id="f0e80-126">OpenGL Error Codes</span></span>](opengl-error-codes.md)
-   [<span data-ttu-id="f0e80-127">Guardar y restaurar conjuntos de variables de estado</span><span class="sxs-lookup"><span data-stu-id="f0e80-127">Saving and Restoring Sets of State Variables</span></span>](saving-and-restoring-sets-of-state-variables.md)
-   [<span data-ttu-id="f0e80-128">Variables de estado openGL</span><span class="sxs-lookup"><span data-stu-id="f0e80-128">OpenGL State Variables</span></span>](opengl-state-variables.md)
-   [<span data-ttu-id="f0e80-129">Referencia de información de estado</span><span class="sxs-lookup"><span data-stu-id="f0e80-129">State Information Reference</span></span>](state-information-reference.md)

 

 




