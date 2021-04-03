---
title: " elif"
description: La Directiva \ Elif marca una cláusula opcional de un bloque de compilación condicional definido por una directiva \ ifdef, \ ifndef o \ if.
ms.assetid: 432b8543-7e1a-411a-8191-cc0f0e4a2e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a548cff74151dadf4a83a1e7d91ceedeafe07e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075857"
---
# <a name="elif"></a><span data-ttu-id="88451-103">\#elif</span><span class="sxs-lookup"><span data-stu-id="88451-103">\#elif</span></span>

<span data-ttu-id="88451-104">La directiva **\# Elif** marca una cláusula opcional de un bloque de compilación condicional definido por una directiva **\# ifdef**, **\# ifndef** o **\# If** .</span><span class="sxs-lookup"><span data-stu-id="88451-104">The **\#elif** directive marks an optional clause of a conditional-compilation block defined by a **\#ifdef**, **\#ifndef**, or **\#if** directive.</span></span> <span data-ttu-id="88451-105">La directiva controla la compilación condicional del archivo de recursos comprobando la expresión constante especificada.</span><span class="sxs-lookup"><span data-stu-id="88451-105">The directive controls conditional compilation of the resource file by checking the specified constant expression.</span></span> <span data-ttu-id="88451-106">Si la expresión constante es distinta de cero, **\# Elif** indica al compilador que continúe con el procesamiento de las instrucciones hasta la siguiente directiva **\# endif**, **\# else** o **\# Elif** y, a continuación, vaya a la instrucción después de **\# endif**.</span><span class="sxs-lookup"><span data-stu-id="88451-106">If the constant expression is nonzero, **\#elif** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after **\#endif**.</span></span> <span data-ttu-id="88451-107">Si la expresión constante es cero, **\# Elif** indica al compilador que vaya a la siguiente directiva **\# endif**, **\# else** o **\# Elif** .</span><span class="sxs-lookup"><span data-stu-id="88451-107">If the constant expression is zero, **\#elif** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span> <span data-ttu-id="88451-108">Puede usar cualquier número de directivas **\# Elif** en un bloque condicional.</span><span class="sxs-lookup"><span data-stu-id="88451-108">You can use any number of **\#elif** directives in a conditional block.</span></span>

``` syntax
#elif constant-expression
```

<dl> <dt>

<span data-ttu-id="88451-109"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*expresión constante*</span><span class="sxs-lookup"><span data-stu-id="88451-109"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*</span></span>
</dt> <dd>

<span data-ttu-id="88451-110">Expresión que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="88451-110">Expression to be checked.</span></span> <span data-ttu-id="88451-111">Este valor es un nombre definido, una constante de tipo entero o una expresión que consta de nombres, enteros y operadores aritméticos y relacionales.</span><span class="sxs-lookup"><span data-stu-id="88451-111">This value is a defined name, an integer constant, or an expression consisting of names, integers, and arithmetic and relational operators.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="88451-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="88451-112">Example</span></span>

<span data-ttu-id="88451-113">En este ejemplo, **\# Elif** indica al compilador que procese la segunda instrucción de [**mapa de bits**](bitmap-resource.md) solo si el valor asignado a la versión de nombre es inferior a 7.</span><span class="sxs-lookup"><span data-stu-id="88451-113">In this example, **\#elif** directs the compiler to process the second [**BITMAP**](bitmap-resource.md) statement only if the value assigned to the name Version is less than 7.</span></span> <span data-ttu-id="88451-114">La propia directiva **\# Elif** solo se procesa si la versión es mayor o igual que 3.</span><span class="sxs-lookup"><span data-stu-id="88451-114">The **\#elif** directive itself is processed only if Version is greater than or equal to 3.</span></span>

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#elif Version < 7
BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="88451-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="88451-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88451-116">Directivas de preprocesador</span><span class="sxs-lookup"><span data-stu-id="88451-116">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




