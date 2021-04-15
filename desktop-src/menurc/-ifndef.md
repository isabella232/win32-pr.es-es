---
title: " ifndef"
description: La Directiva \ ifndef controla la compilación condicional del archivo de recursos comprobando el nombre especificado.
ms.assetid: b83d7b0e-1a37-47a8-b495-0eab05ed3a9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 984a969123ea68fd68b14c1b98354b8bc5205aba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695324"
---
# <a name="ifndef"></a><span data-ttu-id="ba2f1-103">\#ifndef</span><span class="sxs-lookup"><span data-stu-id="ba2f1-103">\#ifndef</span></span>

<span data-ttu-id="ba2f1-104">La directiva **\# ifndef** controla la compilación condicional del archivo de recursos comprobando el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="ba2f1-104">The **\#ifndef** directive controls conditional compilation of the resource file by checking the specified name.</span></span> <span data-ttu-id="ba2f1-105">Si el nombre no se ha definido o si su definición se ha quitado mediante la directiva **\# UNDEF** , **\# ifndef** indica al compilador que continúe procesando las instrucciones hasta la siguiente directiva **\# endif**, **\# else** o **\# Elif** y, a continuación, vaya a la instrucción después de la directiva **\# endif** .</span><span class="sxs-lookup"><span data-stu-id="ba2f1-105">If the name has not been defined or if its definition has been removed by using the **\#undef** directive, **\#ifndef** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after the **\#endif** directive.</span></span> <span data-ttu-id="ba2f1-106">Si se define el nombre, **\# ifndef** indica al compilador que vaya a la siguiente directiva **\# endif**, **\# else** o **\# Elif** .</span><span class="sxs-lookup"><span data-stu-id="ba2f1-106">If the name is defined, **\#ifndef** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span>

``` syntax
#ifndef name
```

<dl> <dt>

<span data-ttu-id="ba2f1-107"><span id="name"></span><span id="NAME"></span>*Name*</span><span class="sxs-lookup"><span data-stu-id="ba2f1-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="ba2f1-108">Nombre que se va a comprobar mediante la Directiva.</span><span class="sxs-lookup"><span data-stu-id="ba2f1-108">Name to be checked by the directive.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="ba2f1-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ba2f1-109">Example</span></span>

<span data-ttu-id="ba2f1-110">En este ejemplo se compila la instrucción [**Bitmap**](bitmap-resource.md) solo si no se define Optimize:</span><span class="sxs-lookup"><span data-stu-id="ba2f1-110">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if Optimize is not defined:</span></span>

``` syntax
#ifndef Optimize
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="ba2f1-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ba2f1-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba2f1-112">Directivas de preprocesador</span><span class="sxs-lookup"><span data-stu-id="ba2f1-112">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




