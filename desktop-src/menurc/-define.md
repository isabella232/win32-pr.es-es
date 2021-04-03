---
title: " define"
description: La Directiva \ define asigna el valor dado al nombre especificado. Todas las repeticiones posteriores del nombre se reemplazan por el valor.
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557c6b486d9c2bd07b0b012c17e806f5d9eaae91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777485"
---
# <a name="define"></a><span data-ttu-id="14458-104">\#define</span><span class="sxs-lookup"><span data-stu-id="14458-104">\#define</span></span>

<span data-ttu-id="14458-105">La directiva **\# define** asigna el valor dado al nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="14458-105">The **\#define** directive assigns the given value to the specified name.</span></span> <span data-ttu-id="14458-106">Todas las repeticiones posteriores del nombre se reemplazan por el valor.</span><span class="sxs-lookup"><span data-stu-id="14458-106">All subsequent occurrences of the name are replaced by the value.</span></span>

``` syntax
#define name value
```

<dl> <dt>

<span data-ttu-id="14458-107"><span id="name"></span><span id="NAME"></span>*Name*</span><span class="sxs-lookup"><span data-stu-id="14458-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="14458-108">Nombre que se va a definir.</span><span class="sxs-lookup"><span data-stu-id="14458-108">Name to be defined.</span></span> <span data-ttu-id="14458-109">Este valor es cualquier combinación de letras, dígitos y puntuación que sea válida para el preprocesador de C/C++.</span><span class="sxs-lookup"><span data-stu-id="14458-109">This value is any combination of letters, digits, and punctuation that is valid for the C/C++ preprocessor.</span></span>

</dd> <dt>

<span data-ttu-id="14458-110"><span id="value"></span><span id="VALUE"></span>*valor*</span><span class="sxs-lookup"><span data-stu-id="14458-110"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="14458-111">Entero, cadena de caracteres o línea de texto.</span><span class="sxs-lookup"><span data-stu-id="14458-111">Integer, character string, or line of text.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="14458-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="14458-112">Example</span></span>

<span data-ttu-id="14458-113">Este ejemplo asigna valores a los nombres NonZero y USERCLASS:</span><span class="sxs-lookup"><span data-stu-id="14458-113">This example assigns values to the names NONZERO and USERCLASS:</span></span>

``` syntax
#define     NONZERO     1
#define     USERCLASS   "MyControlClass"
```

## <a name="related-topics"></a><span data-ttu-id="14458-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="14458-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14458-115">Directivas de preprocesador</span><span class="sxs-lookup"><span data-stu-id="14458-115">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




