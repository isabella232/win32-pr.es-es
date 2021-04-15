---
title: " undef"
description: La Directiva \ UNDEF quita la definición actual del nombre especificado. Todas las repeticiones posteriores del nombre se procesan sin reemplazo.
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b14eeea18a05795cd8ebbb94d81d0aead6a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714177"
---
# <a name="undef"></a><span data-ttu-id="3f4f0-104">\#undef</span><span class="sxs-lookup"><span data-stu-id="3f4f0-104">\#undef</span></span>

<span data-ttu-id="3f4f0-105">La directiva **\# UNDEF** quita la definición actual del nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="3f4f0-105">The **\#undef** directive removes the current definition of the specified name.</span></span> <span data-ttu-id="3f4f0-106">Todas las repeticiones posteriores del nombre se procesan sin reemplazo.</span><span class="sxs-lookup"><span data-stu-id="3f4f0-106">All subsequent occurrences of the name are processed without replacement.</span></span>

``` syntax
#undef name
```

<dl> <dt>

<span data-ttu-id="3f4f0-107"><span id="name"></span><span id="NAME"></span>*Name*</span><span class="sxs-lookup"><span data-stu-id="3f4f0-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="3f4f0-108">Nombre que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="3f4f0-108">Name to be removed.</span></span> <span data-ttu-id="3f4f0-109">Este valor es cualquier combinación de letras, dígitos y puntuación que sea válida para el preprocesador de C/C++.</span><span class="sxs-lookup"><span data-stu-id="3f4f0-109">This value is any combination of letters, digits, and punctuation that is valid for the C/C++ preprocessor.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="3f4f0-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3f4f0-110">Example</span></span>

<span data-ttu-id="3f4f0-111">En este ejemplo se quitan las definiciones de los nombres distintos de cero y USERCLASS:</span><span class="sxs-lookup"><span data-stu-id="3f4f0-111">This example removes the definitions for the names nonzero and USERCLASS:</span></span>

``` syntax
#undef     nonzero
#undef     USERCLASS
```

## <a name="related-topics"></a><span data-ttu-id="3f4f0-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3f4f0-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f4f0-113">Directivas de preprocesador</span><span class="sxs-lookup"><span data-stu-id="3f4f0-113">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




