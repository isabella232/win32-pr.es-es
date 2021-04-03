---
title: Nombres de funciones OpenGL
description: Muchas funciones de OpenGL son variaciones entre sí, que se diferencian principalmente en los tipos de datos de sus argumentos.
ms.assetid: 2d30e2e4-9671-4e57-962d-0328b13159f3
keywords:
- OpenGL, nombres de función
- nombres de función OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e06d04d1acde3ddf9baebd4c5ab44b4f55cb126
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776141"
---
# <a name="opengl-function-names"></a><span data-ttu-id="ec04f-105">Nombres de funciones OpenGL</span><span class="sxs-lookup"><span data-stu-id="ec04f-105">OpenGL Function Names</span></span>

<span data-ttu-id="ec04f-106">Muchas funciones de OpenGL son variaciones entre sí, que se diferencian principalmente en los tipos de datos de sus argumentos.</span><span class="sxs-lookup"><span data-stu-id="ec04f-106">Many OpenGL functions are variations of each other, differing mostly in the data types of their arguments.</span></span> <span data-ttu-id="ec04f-107">Algunas funciones difieren en el número de argumentos relacionados y si esos argumentos se pueden especificar como vector o se deben especificar por separado en una lista.</span><span class="sxs-lookup"><span data-stu-id="ec04f-107">Some functions differ in the number of related arguments and whether those arguments can be specified as a vector or must be specified separately in a list.</span></span> <span data-ttu-id="ec04f-108">Por ejemplo, si usa la función **glVertex2f** , debe proporcionar coordenadas x e y como números de punto flotante de 32 bits; con **glVertex3sv**, debe proporcionar una matriz de tres valores enteros cortos (de 16 bits) para x, y y z.</span><span class="sxs-lookup"><span data-stu-id="ec04f-108">For example, if you use the **glVertex2f** function, you need to supply x- and y-coordinates as 32-bit floating-point numbers; with **glVertex3sv**, you must supply an array of three short (16-bit) integer values for x, y, and z.</span></span> <span data-ttu-id="ec04f-109">En los temas siguientes solo se usa el nombre base de la función.</span><span class="sxs-lookup"><span data-stu-id="ec04f-109">Only the base name of the function is used in the topics that follow.</span></span> <span data-ttu-id="ec04f-110">Un asterisco indica que puede haber más en el nombre de función real que el que se muestra.</span><span class="sxs-lookup"><span data-stu-id="ec04f-110">An asterisk indicates that there may be more to the actual function name than is shown.</span></span> <span data-ttu-id="ec04f-111">Por ejemplo, [glVertex \*](glvertex-functions.md) representa todas las variaciones de la función que se usan para especificar vértices: **glVertex2d**, **glVertex2f**, **glVertex2i**, etc.</span><span class="sxs-lookup"><span data-stu-id="ec04f-111">For example, [glVertex\*](glvertex-functions.md) stands for all the variations of the function you use to specify vertices: **glVertex2d**, **glVertex2f**, **glVertex2i**, and so on.</span></span>

<span data-ttu-id="ec04f-112">El efecto de una función de OpenGL puede variar en función de si están habilitados determinados modos.</span><span class="sxs-lookup"><span data-stu-id="ec04f-112">The effect of an OpenGL function can vary depending on whether certain modes are enabled.</span></span> <span data-ttu-id="ec04f-113">Por ejemplo, debe habilitar la iluminación si las funciones relacionadas con la iluminación producen un objeto iluminado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ec04f-113">For example, you need to enable lighting if the lighting-related functions are to produce a properly lit object.</span></span> <span data-ttu-id="ec04f-114">Para habilitar un modo determinado, use la función [**glEnable**](glenable.md) y proporcione la constante adecuada para identificar el modo (por ejemplo, iluminación de GL \_ ).</span><span class="sxs-lookup"><span data-stu-id="ec04f-114">To enable a particular mode, use the [**glEnable**](glenable.md) function and supply the appropriate constant to identify the mode (for example, GL\_LIGHTING).</span></span> <span data-ttu-id="ec04f-115">Para deshabilitar un modo, use [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="ec04f-115">To disable a mode, use [**glDisable**](gldisable.md).</span></span> <span data-ttu-id="ec04f-116">Consulte **glEnable** para obtener una lista completa de los modos que se pueden habilitar.</span><span class="sxs-lookup"><span data-stu-id="ec04f-116">See **glEnable** for a complete list of the modes that can be enabled.</span></span>

 

 




