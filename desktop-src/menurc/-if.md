---
title: " if"
description: La Directiva \ if controla la compilación condicional del archivo de recursos comprobando la expresión constante especificada.
ms.assetid: 4d0f26a0-1a2d-4fad-b5ce-b9441397d2c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364d6f5eb818813f61f6428446effb4793b96b2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704653"
---
# <a name="if"></a><span data-ttu-id="b43d3-103">\#if</span><span class="sxs-lookup"><span data-stu-id="b43d3-103">\#if</span></span>

<span data-ttu-id="b43d3-104">La directiva **\# If** controla la compilación condicional del archivo de recursos comprobando la expresión constante especificada.</span><span class="sxs-lookup"><span data-stu-id="b43d3-104">The **\#if** directive controls conditional compilation of the resource file by checking the specified constant expression.</span></span> <span data-ttu-id="b43d3-105">Si la expresión constante es distinta de cero, **\# si** indica al compilador que continúe procesando instrucciones hasta la siguiente directiva **\# endif**, **\# else** o **\# Elif** y, a continuación, vaya a la instrucción después de la directiva **\# endif** .</span><span class="sxs-lookup"><span data-stu-id="b43d3-105">If the constant expression is nonzero, **\#if** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after the **\#endif** directive.</span></span> <span data-ttu-id="b43d3-106">Si la expresión constante es cero, **\# si** indica al compilador que vaya a la siguiente directiva **\# endif**, **\# else** o **\# Elif** .</span><span class="sxs-lookup"><span data-stu-id="b43d3-106">If the constant expression is zero, **\#if** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span>

``` syntax
#if constant-expression
```

<dl> <dt>

<span data-ttu-id="b43d3-107"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*expresión constante*</span><span class="sxs-lookup"><span data-stu-id="b43d3-107"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*</span></span>
</dt> <dd>

<span data-ttu-id="b43d3-108">Expresión que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="b43d3-108">Expression to be checked.</span></span> <span data-ttu-id="b43d3-109">Este valor es un nombre definido, una constante de tipo entero o una expresión que consta de nombres, enteros y operadores aritméticos y relacionales.</span><span class="sxs-lookup"><span data-stu-id="b43d3-109">This value is a defined name, an integer constant, or an expression consisting of names, integers, and arithmetic and relational operators.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="b43d3-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b43d3-110">Example</span></span>

<span data-ttu-id="b43d3-111">Este ejemplo compila la instrucción [**Bitmap**](bitmap-resource.md) solo si el valor asignado a la versión es inferior a 3:</span><span class="sxs-lookup"><span data-stu-id="b43d3-111">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if the value assigned Version is less than 3:</span></span>

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="b43d3-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b43d3-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b43d3-113">Directivas de preprocesador</span><span class="sxs-lookup"><span data-stu-id="b43d3-113">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




