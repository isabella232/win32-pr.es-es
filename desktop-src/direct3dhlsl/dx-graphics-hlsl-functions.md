---
title: Funciones (referencia de HLSL)
description: Las funciones encapsulan instrucciones HLSL.
ms.assetid: b6f934e5-eac7-4859-b1d0-698632011e1d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59b0bfcb2079329d4d7ad7c02e7e5a326d22c236
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104358518"
---
# <a name="functions-hlsl-reference"></a><span data-ttu-id="07d04-103">Funciones (referencia de HLSL)</span><span class="sxs-lookup"><span data-stu-id="07d04-103">Functions (HLSL reference)</span></span>

<span data-ttu-id="07d04-104">Las funciones encapsulan instrucciones HLSL.</span><span class="sxs-lookup"><span data-stu-id="07d04-104">Functions encapsulate HLSL statements.</span></span> <span data-ttu-id="07d04-105">Esto le permite depurar un conjunto de funciones y, a continuación, volver a usarlas en otros sombreadores o efectos.</span><span class="sxs-lookup"><span data-stu-id="07d04-105">This enables you to debug a set of functions and then reuse them across shaders or effects.</span></span> <span data-ttu-id="07d04-106">Puede que desee crear una función que encapsule la funcionalidad de un sombreador de vértices, un sombreador de píxeles o un sombreador de textura.</span><span class="sxs-lookup"><span data-stu-id="07d04-106">You may want to create a function that encapsulates the functionality of a vertex shader, pixel shader or texture shader.</span></span> <span data-ttu-id="07d04-107">Otras veces, es posible que desee escribir una función auxiliar que realice alguna tarea de uso frecuente y, a continuación, llamar a esa función auxiliar desde la función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="07d04-107">Other times, you may want to write a helper function that performs some commonly used task, and then call that helper function from your shader function.</span></span> <span data-ttu-id="07d04-108">Las reglas para escribir funciones de sombreador para HLSL son muy similares a la escritura de funciones de C.</span><span class="sxs-lookup"><span data-stu-id="07d04-108">The rules for writing shader functions for HLSL are very similar to writing C functions.</span></span>

-   [<span data-ttu-id="07d04-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07d04-109">Syntax</span></span>](dx-graphics-hlsl-function-syntax.md)
-   [<span data-ttu-id="07d04-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07d04-110">Parameters</span></span>](dx-graphics-hlsl-function-parameters.md)
-   [<span data-ttu-id="07d04-111">Instrucción return</span><span class="sxs-lookup"><span data-stu-id="07d04-111">Return Statement</span></span>](dx-graphics-hlsl-return.md)
-   [<span data-ttu-id="07d04-112">Firmas</span><span class="sxs-lookup"><span data-stu-id="07d04-112">Signatures</span></span>](dx-graphics-hlsl-signatures.md)

<span data-ttu-id="07d04-113">HLSL también tiene un número de [**funciones intrínsecas integradas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md).</span><span class="sxs-lookup"><span data-stu-id="07d04-113">HLSL also has a number of built-in [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md).</span></span> <span data-ttu-id="07d04-114">Dado que todas las funciones intrínsecas se prueban y optimizan el rendimiento, es recomendable usar una función intrínseca siempre que sea posible en lugar de crear su propia función.</span><span class="sxs-lookup"><span data-stu-id="07d04-114">Because all intrinsic functions are tested and performance optimized, it is good practice to use an intrinsic function where possible instead of creating your own function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07d04-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07d04-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07d04-116">Sintaxis del lenguaje (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07d04-116">Language Syntax (DirectX HLSL)</span></span>](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




