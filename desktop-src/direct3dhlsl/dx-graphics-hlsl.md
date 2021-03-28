---
title: Lenguaje de sombreador de alto nivel (HLSL)
description: HLSL es el lenguaje de sombreador de alto nivel de C que se usa con los sombreadores programables en DirectX.
ms.assetid: 09cdd8d6-0cf5-4f7e-b480-f748d2fa9ca9
ms.topic: article
ms.date: 01/11/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.custom: contperf-fy21q3
ms.openlocfilehash: c0876cda302d4c6215b640c210e880795273cd6c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104986182"
---
# <a name="high-level-shader-language-hlsl"></a><span data-ttu-id="88087-103">Lenguaje de sombreador de alto nivel (HLSL)</span><span class="sxs-lookup"><span data-stu-id="88087-103">High-level shader language (HLSL)</span></span>

<span data-ttu-id="88087-104">HLSL es el lenguaje de sombreador de alto nivel de C que se usa con los sombreadores programables en DirectX.</span><span class="sxs-lookup"><span data-stu-id="88087-104">HLSL is the C-like high-level shader language that you use with programmable shaders in DirectX.</span></span>

<span data-ttu-id="88087-105">Por ejemplo, puede usar HLSL para escribir un [sombreador de vértices](../direct3d11/vertex-shader-stage.md), un [sombreador de píxeles](../direct3d11/pixel-shader-stage.md)y usar esos sombreadores en la implementación del representador en la aplicación [Direct3D](../direct3d12/directx-12-programming-guide.md) .</span><span class="sxs-lookup"><span data-stu-id="88087-105">For example, you can use HLSL to write a [vertex shader](../direct3d11/vertex-shader-stage.md), or a [pixel shader](../direct3d11/pixel-shader-stage.md), and use those shaders in the implementation of the renderer in your [Direct3D](../direct3d12/directx-12-programming-guide.md) application.</span></span>

<span data-ttu-id="88087-106">O bien, puede usar HLSL para escribir un sombreador de cálculo, quizás para implementar una simulación física.</span><span class="sxs-lookup"><span data-stu-id="88087-106">Or you could use HLSL to write a compute shader, perhaps to implement a physics simulation.</span></span> <span data-ttu-id="88087-107">Sin embargo, si, por ejemplo, está inclinado por escribir su propio operador de circunvolución (para el procesamiento de imágenes) como HLSL en un sombreador de cálculo, obtendrá un mejor rendimiento en ese escenario si usa [machine learning directo (DirectML)](../direct3d12/dml.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="88087-107">However, if for example you're inclined to write your own convolution operator (for image processing) as HLSL in a compute shader, then you'll get better performance in that scenario if you use [Direct Machine Learning (DirectML)](../direct3d12/dml.md) instead.</span></span>

<span data-ttu-id="88087-108">Se creó HLSL (a partir de DirectX 9) para configurar la [canalización](../direct3d11/overviews-direct3d-11-graphics-pipeline.md)3D programable.</span><span class="sxs-lookup"><span data-stu-id="88087-108">HLSL was created (starting with DirectX 9) to set up the programmable 3D [pipeline](../direct3d11/overviews-direct3d-11-graphics-pipeline.md).</span></span> <span data-ttu-id="88087-109">Puede programar toda la canalización con instrucciones de HLSL.</span><span class="sxs-lookup"><span data-stu-id="88087-109">You can program the entire pipeline with HLSL instructions.</span></span>

## <a name="where-to-go-next"></a><span data-ttu-id="88087-110">Dónde ir siguiente</span><span class="sxs-lookup"><span data-stu-id="88087-110">Where to go next</span></span>

* [<span data-ttu-id="88087-111">Guía de programación para HLSL</span><span class="sxs-lookup"><span data-stu-id="88087-111">Programming guide for HLSL</span></span>](./dx-graphics-hlsl-pguide.md)
* [<span data-ttu-id="88087-112">Referencia de HLSL</span><span class="sxs-lookup"><span data-stu-id="88087-112">Reference for HLSL</span></span>](./dx-graphics-hlsl-reference.md)

### <a name="programming-guide-for-hlsl"></a><span data-ttu-id="88087-113">Guía de programación para HLSL</span><span class="sxs-lookup"><span data-stu-id="88087-113">Programming guide for HLSL</span></span>

<span data-ttu-id="88087-114">Para obtener una introducción conceptual a HLSL, consulte la [Guía de programación para HLSL](./dx-graphics-hlsl-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="88087-114">For a conceptual introduction to HLSL, see the [Programming guide for HLSL](./dx-graphics-hlsl-pguide.md).</span></span>

<span data-ttu-id="88087-115">En la guía de programación se describen los diferentes tipos de fases del sombreador y cómo crear, compilar, optimizar, enlazar y vincular sombreadores.</span><span class="sxs-lookup"><span data-stu-id="88087-115">The programming guide discusses the different kinds of shader stages, and how to create, compile, optimize, bind, and link shaders.</span></span>

<span data-ttu-id="88087-116">Allí también encontrará información general y notas de la versión sobre las generaciones sucesivas de la versión del modelo de sombreador que se han lanzado, volviendo al modelo de sombreador de HLSL 5.</span><span class="sxs-lookup"><span data-stu-id="88087-116">There you'll also find overviews of, and release notes about, the successive generations of shader model version that have been released, going back as far as HLSL shader model 5.</span></span>

### <a name="reference-for-hlsl"></a><span data-ttu-id="88087-117">Referencia de HLSL</span><span class="sxs-lookup"><span data-stu-id="88087-117">Reference for HLSL</span></span>

<span data-ttu-id="88087-118">Para obtener documentación de referencia de HLSL, consulte la [referencia de HLSL](./dx-graphics-hlsl-reference.md).</span><span class="sxs-lookup"><span data-stu-id="88087-118">For HLSL reference documentation, see the [Reference for HLSL](./dx-graphics-hlsl-reference.md).</span></span>

<span data-ttu-id="88087-119">La sección de referencia contiene una lista completa de la sintaxis del lenguaje y de las funciones intrínsecas integradas en HLSL para simplificar los requisitos de codificación.</span><span class="sxs-lookup"><span data-stu-id="88087-119">The reference section has a complete listing of the language syntax and of the intrinsic functions that are built into HLSL in order to simplify your coding requirements.</span></span>

<span data-ttu-id="88087-120">También encontrará una descripción de los modelos de sombreador frente a los perfiles y el contenido de referencia del modelo de sombreador que vuelve a pasar hasta el modelo de sombreador de HLSL 1.</span><span class="sxs-lookup"><span data-stu-id="88087-120">There also you'll find a discussion of shader models versus profiles, and shader model reference content going back as far as HLSL shader model 1.</span></span> <span data-ttu-id="88087-121">También hay contenido que abarca las instrucciones de ensamblado, la herramienta D3DCompiler y la información sobre los errores y advertencias que puede devolver un sombreador.</span><span class="sxs-lookup"><span data-stu-id="88087-121">There's also content covering assembly instructions, the D3DCompiler tool, and info about the errors and warnings that a shader can return.</span></span>