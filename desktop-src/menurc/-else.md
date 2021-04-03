---
title: " else"
description: La Directiva \ else marca una cláusula opcional de un bloque de compilación condicional definido por una directiva \ ifdef, \ ifndef o \ if. La Directiva \ else debe ser la última Directiva antes de la Directiva \ endif.
ms.assetid: 982466d9-ae77-4e1c-89f3-511335165da7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086acd9e6323f7be11a65951a33b2b11b680ad46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776447"
---
# <a name="else"></a><span data-ttu-id="65274-104">\#else</span><span class="sxs-lookup"><span data-stu-id="65274-104">\#else</span></span>

<span data-ttu-id="65274-105">La directiva **\# else** marca una cláusula opcional de un bloque de compilación condicional definido por una directiva **\# ifdef**, **\# ifndef** o **\# If** .</span><span class="sxs-lookup"><span data-stu-id="65274-105">The **\#else** directive marks an optional clause of a conditional-compilation block defined by a **\#ifdef**, **\#ifndef**, or **\#if** directive.</span></span> <span data-ttu-id="65274-106">La directiva **\# else** debe ser la última Directiva antes de la directiva **\# endif** .</span><span class="sxs-lookup"><span data-stu-id="65274-106">The **\#else** directive must be the last directive before the **\#endif** directive.</span></span>

``` syntax
#else
```

<span data-ttu-id="65274-107">Esta Directiva no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="65274-107">This directive has no parameters.</span></span>

## <a name="example"></a><span data-ttu-id="65274-108">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="65274-108">Example</span></span>

<span data-ttu-id="65274-109">En este ejemplo se compila la segunda instrucción [**Bitmap**](bitmap-resource.md) solo si no se define DEBUG:</span><span class="sxs-lookup"><span data-stu-id="65274-109">This example compiles the second [**BITMAP**](bitmap-resource.md) statement only if DEBUG is not defined:</span></span>

``` syntax
#ifdef DEBUG
    BITMAP 1 errbox.bmp
#else
    BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="65274-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="65274-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65274-111">Directivas de preprocesador</span><span class="sxs-lookup"><span data-stu-id="65274-111">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




