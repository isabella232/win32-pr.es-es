---
title: " ifdef"
description: La Directiva \ ifdef controla la compilación condicional del archivo de recursos comprobando el nombre especificado.
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38170fb2140f8405a86529c0899c1e4d4e93c026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418736"
---
# <a name="ifdef"></a><span data-ttu-id="4e4f3-103">\#ifdef</span><span class="sxs-lookup"><span data-stu-id="4e4f3-103">\#ifdef</span></span>

<span data-ttu-id="4e4f3-104">La directiva **\# ifdef** controla la compilación condicional del archivo de recursos comprobando el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="4e4f3-104">The **\#ifdef** directive controls conditional compilation of the resource file by checking the specified name.</span></span> <span data-ttu-id="4e4f3-105">Si el nombre se ha definido mediante una directiva de **\# definición** o mediante la opción de línea de comandos **/d** con el compilador de recursos, **\# ifdef** indica al compilador que continúe con la instrucción inmediatamente después de la directiva **\# ifdef** .</span><span class="sxs-lookup"><span data-stu-id="4e4f3-105">If the name has been defined by using a **\#define** directive or by using the **/d** command-line option with the resource compiler, **\#ifdef** directs the compiler to continue with the statement immediately after the **\#ifdef** directive.</span></span> <span data-ttu-id="4e4f3-106">Si no se ha definido el nombre, **\# ifdef** indica al compilador que omita todas las instrucciones hasta la siguiente directiva **\# endif** .</span><span class="sxs-lookup"><span data-stu-id="4e4f3-106">If the name has not been defined, **\#ifdef** directs the compiler to skip all statements up to the next **\#endif** directive.</span></span>

``` syntax
#ifdef name
```

<dl> <dt>

<span data-ttu-id="4e4f3-107"><span id="name"></span><span id="NAME"></span>*Name*</span><span class="sxs-lookup"><span data-stu-id="4e4f3-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="4e4f3-108">Nombre que se va a comprobar mediante la Directiva.</span><span class="sxs-lookup"><span data-stu-id="4e4f3-108">Name to be checked by the directive.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="4e4f3-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4e4f3-109">Example</span></span>

<span data-ttu-id="4e4f3-110">En este ejemplo se compila la instrucción [**Bitmap**](bitmap-resource.md) solo si se define DEBUG:</span><span class="sxs-lookup"><span data-stu-id="4e4f3-110">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if Debug is defined:</span></span>

``` syntax
#ifdef Debug
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="4e4f3-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e4f3-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e4f3-112">Directivas de preprocesador</span><span class="sxs-lookup"><span data-stu-id="4e4f3-112">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




