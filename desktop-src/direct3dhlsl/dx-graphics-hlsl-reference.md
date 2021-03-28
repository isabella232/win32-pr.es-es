---
title: Referencia de HLSL
description: La documentación de referencia de HLSL especifica las características del lenguaje. Se divide en varias secciones.
ms.assetid: 1d0e12ff-8559-4e5c-9914-6ed313ea5464
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce0bb59dd26bd8bb9723bcdff23bbc79ee810253
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076109"
---
# <a name="reference-for-hlsl"></a><span data-ttu-id="3f7e9-104">Referencia de HLSL</span><span class="sxs-lookup"><span data-stu-id="3f7e9-104">Reference for HLSL</span></span>

<span data-ttu-id="3f7e9-105">La documentación de referencia de HLSL especifica las características del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-105">The HLSL reference documentation specifies the language characteristics.</span></span> <span data-ttu-id="3f7e9-106">Se divide en varias secciones.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-106">It is broken into several sections.</span></span>

-   <span data-ttu-id="3f7e9-107">[Sintaxis del lenguaje (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md) : los sombreadores de programación en HLSL requieren que comprenda la sintaxis del lenguaje, es decir, cómo se escribe el código HLSL.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-107">[Language Syntax (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md) - Programming shaders in HLSL requires that you understand the language syntax, that is, how you write HLSL code.</span></span> <span data-ttu-id="3f7e9-108">Esto incluye el código para declarar e inicializar variables, escribir funciones de sombreador definidas por el usuario y agregar instrucciones de control de flujo para que las funciones sean más eficaces.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-108">This includes code to declare and initialize variables, write user-defined shader functions, and add flow control statements to make your functions more powerful.</span></span>
-   <span data-ttu-id="3f7e9-109">[Modelos de sombreador frente a perfiles de sombreador](dx-graphics-hlsl-models.md) : el compilador de HLSL implementa reglas y restricciones basadas en modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-109">[Shader Models vs Shader Profiles](dx-graphics-hlsl-models.md) - The HLSL compiler implements rules and restrictions based on shader models.</span></span> <span data-ttu-id="3f7e9-110">El código de cada sombreador de vértices, sombreador de geometría (si se usa Direct3D 10) y sombreador de píxeles se validan con respecto a un modelo de sombreador, que se proporciona en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-110">The code in each vertex shader, geometry shader (if you are using Direct3D 10) and pixel shader are validated against a shader model, which you supply at compile time.</span></span>
-   <span data-ttu-id="3f7e9-111">[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) : HLSL tiene muchas funciones intrínsecas.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-111">[**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) - HLSL has many intrinsic functions.</span></span> <span data-ttu-id="3f7e9-112">Estas se implementan y prueban para que pueda usarlas sabiendo que ya están depuradas y funcionan bien.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-112">These are implemented and tested so that you can use them knowing that they are already debugged and they perform well.</span></span> <span data-ttu-id="3f7e9-113">Si decide escribir sus propias funciones, consulte la sección sintaxis del lenguaje para escribir funciones definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-113">If you choose to write your own functions, see the language syntax section for writing user-defined functions.</span></span>
-   <span data-ttu-id="3f7e9-114">[Referencia del sombreador de ASM](dx9-graphics-reference-asm.md) : instrucciones de ensamblado que puede usar para programar y depurar sombreadores.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-114">[Asm Shader Reference](dx9-graphics-reference-asm.md) - Assembly instructions that you can use to program and debug shaders.</span></span>
-   <span data-ttu-id="3f7e9-115">[Referencia de D3DCompiler](dx-graphics-d3dcompiler-reference.md) : compila el origen HLSL sin formato.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-115">[D3DCompiler Reference](dx-graphics-d3dcompiler-reference.md) - Compiles raw HLSL source.</span></span>
-   <span data-ttu-id="3f7e9-116">[Referencia de conversión de formato en línea](inline-format-conversion-reference.md) : el \_ archivo D3DX DXGIFormatConvert. INL contiene funciones de conversión de formato en línea que puede usar en el sombreador de cálculo o en el sombreador de píxeles en el hardware de Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-116">[Inline Format Conversion Reference](inline-format-conversion-reference.md) - The D3DX\_DXGIFormatConvert.inl file contains inline format conversion functions that you can use in the compute shader or pixel shader on Direct3D 11 hardware.</span></span> <span data-ttu-id="3f7e9-117">Puede usar estas funciones en la aplicación para leer y escribir simultáneamente en una textura.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-117">You can use these functions in your application to simultaneously both read from and write to a texture.</span></span> <span data-ttu-id="3f7e9-118">Es decir, puede realizar la edición en contexto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-118">That is, you can perform in-place image editing.</span></span> <span data-ttu-id="3f7e9-119">Para usar estas funciones de conversión de formato en línea, incluya el \_ archivo D3DX DXGIFormatConvert. INL en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-119">To use these inline format conversion functions, include the D3DX\_DXGIFormatConvert.inl file in your application.</span></span>
-   <span data-ttu-id="3f7e9-120">[Apéndice (DirectX HLSL)](dx-graphics-hlsl-appendix.md) : el apéndice está incluido para la integridad.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-120">[Appendix (DirectX HLSL)](dx-graphics-hlsl-appendix.md) - The appendix is included for completeness.</span></span> <span data-ttu-id="3f7e9-121">Incluye una lista de las palabras clave y las palabras reservadas; estas palabras no se pueden usar como identificadores en los programas.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-121">It includes a listing of the keywords and reserved words; these words cannot be used as identifiers in your programs.</span></span> <span data-ttu-id="3f7e9-122">También incluye una lista de gramática de idioma para referencia.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-122">It also includes a listing of the language grammar for reference.</span></span>
-   <span data-ttu-id="3f7e9-123">[**Advertencias y errores de HLSL**](hlsl-errors-and-warnings.md) : proporciona códigos de error y de advertencia que un sombreador puede devolver.</span><span class="sxs-lookup"><span data-stu-id="3f7e9-123">[**HLSL errors and warnings**](hlsl-errors-and-warnings.md) - Provides error and warning codes that a shader can return.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f7e9-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3f7e9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f7e9-125">HLSL</span><span class="sxs-lookup"><span data-stu-id="3f7e9-125">HLSL</span></span>](dx-graphics-hlsl.md)
</dt> <dt>

[<span data-ttu-id="3f7e9-126">Guía de programación para HLSL</span><span class="sxs-lookup"><span data-stu-id="3f7e9-126">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




