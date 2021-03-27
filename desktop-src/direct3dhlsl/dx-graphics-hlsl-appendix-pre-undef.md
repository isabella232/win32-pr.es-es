---
title: " UNDEF (Directiva)"
description: Directiva de preprocesador que quita la definición actual de una constante o macro que se definió anteriormente mediante la Directiva \ define.
ms.assetid: ba6bbe6b-ecfa-40cb-887f-e42b6e22c7bd
keywords:
- UNDEF (Directiva HLSL)
topic_type:
- apiref
api_name:
- undef Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7358dc60d002e784394f64773934a18f7413e493
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358111"
---
# <a name="undef-directive"></a><span data-ttu-id="922d6-104">\#UNDEF (Directiva)</span><span class="sxs-lookup"><span data-stu-id="922d6-104">\#undef Directive</span></span>

<span data-ttu-id="922d6-105">Directiva de preprocesador que quita la definición actual de una constante o macro que se definió anteriormente mediante la directiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) .</span><span class="sxs-lookup"><span data-stu-id="922d6-105">Preprocessor directive that removes the current definition of a constant or macro that was previously defined using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive.</span></span>



| <span data-ttu-id="922d6-106">\#UNDEF ( *identificador* )</span><span class="sxs-lookup"><span data-stu-id="922d6-106">\#undef *identifier*</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="922d6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="922d6-107">Parameters</span></span>



| <span data-ttu-id="922d6-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="922d6-108">Item</span></span>                                                                              | <span data-ttu-id="922d6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="922d6-109">Description</span></span>                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="922d6-110"><span id="identifier"></span><span id="IDENTIFIER"></span>*identificador*</span><span class="sxs-lookup"><span data-stu-id="922d6-110"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/> | <span data-ttu-id="922d6-111">Identificador de la constante o macro para la que se va a quitar la definición.</span><span class="sxs-lookup"><span data-stu-id="922d6-111">Identifier of the constant or macro to remove the definition of.</span></span> <span data-ttu-id="922d6-112">Si va a desdefinir una macro, proporcione solo el identificador, no la lista de parámetros.</span><span class="sxs-lookup"><span data-stu-id="922d6-112">If you are undefining a macro, provide only the identifier, not the parameter list.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="922d6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="922d6-113">Remarks</span></span>

<span data-ttu-id="922d6-114">Puede aplicar la \# Directiva UNDEF a un identificador que no tiene ninguna definición anterior; esto garantiza que el identificador no esté definido.</span><span class="sxs-lookup"><span data-stu-id="922d6-114">You can apply the \#undef directive to an identifier that has no previous definition; this ensures that the identifier is undefined.</span></span> <span data-ttu-id="922d6-115">La sustitución de macros no se realiza dentro de las \# instrucciones UNDEF.</span><span class="sxs-lookup"><span data-stu-id="922d6-115">Macro replacement is not performed within \#undef statements.</span></span>

<span data-ttu-id="922d6-116">\#Normalmente, la Directiva UNDEF se empareja con una directiva de [ \# definición](dx-graphics-hlsl-appendix-pre-define.md) para crear una región en un programa de origen en el que un identificador tiene un significado especial.</span><span class="sxs-lookup"><span data-stu-id="922d6-116">The \#undef directive is typically paired with a [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive to create a region in a source program in which an identifier has a special meaning.</span></span> <span data-ttu-id="922d6-117">Por ejemplo, una función específica del programa de origen puede utilizar constantes de manifiesto para definir valores específicos del entorno que no afecten al resto del programa.</span><span class="sxs-lookup"><span data-stu-id="922d6-117">For example, a specific function of the source program can use manifest constants to define environment-specific values that do not affect the rest of the program.</span></span> <span data-ttu-id="922d6-118">La \# Directiva UNDEF también funciona con la Directiva [) para controlar la compilación condicional del programa de origen.</span><span class="sxs-lookup"><span data-stu-id="922d6-118">The \#undef directive also works with the [) directive to control conditional compilation of the source program.</span></span>

<span data-ttu-id="922d6-119">Las constantes y macros pueden estar sin definir desde la línea de comandos mediante la opción/U, seguido de los identificadores para que no estén definidos.</span><span class="sxs-lookup"><span data-stu-id="922d6-119">Constants and macros can be undefined from the command line using the /U option, followed by the identifiers to be undefined.</span></span> <span data-ttu-id="922d6-120">Esto es equivalente a agregar una secuencia de \# directivas UNDEF al principio del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="922d6-120">This is equivalent to adding a sequence of \#undef directives at the beginning of the source file.</span></span>

## <a name="examples"></a><span data-ttu-id="922d6-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="922d6-121">Examples</span></span>

<span data-ttu-id="922d6-122">En el ejemplo siguiente se muestra cómo usar la \# Directiva UNDEF para quitar definiciones de una constante simbólica y una macro.</span><span class="sxs-lookup"><span data-stu-id="922d6-122">The following example shows how to use the \#undef directive to remove definitions of a symbolic constant and a macro.</span></span>


```
#define WIDTH           80
#define ADD( X, Y )     (X) + (Y)

#undef WIDTH
#undef ADD
```



## <a name="see-also"></a><span data-ttu-id="922d6-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="922d6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="922d6-124">Directivas de preprocesador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="922d6-124">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="922d6-125">\#define (Directiva) (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="922d6-125">\#define Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="922d6-126">\#Si,)</span><span class="sxs-lookup"><span data-stu-id="922d6-126">\#if, )</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





