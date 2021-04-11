---
description: Se puede usar un efecto para almacenar información o para representar mediante un grupo de estado.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Representar un efecto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfba9432412846e2dc634d6ab68be999b504e06f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274889"
---
# <a name="rendering-an-effect-direct3d-10"></a><span data-ttu-id="5ab44-103">Representar un efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="5ab44-103">Rendering an Effect (Direct3D 10)</span></span>

<span data-ttu-id="5ab44-104">Se puede usar un efecto para almacenar información o para representar mediante un grupo de estado.</span><span class="sxs-lookup"><span data-stu-id="5ab44-104">An effect can be used to store information, or to render using a group of state.</span></span> <span data-ttu-id="5ab44-105">Cada técnica especifica sombreadores de vértices, sombreadores de geometría, sombreadores de píxeles, estado del sombreador, estado de la muestra y textura y otro estado de la canalización.</span><span class="sxs-lookup"><span data-stu-id="5ab44-105">Each technique specifies vertex shaders, geometry shaders, pixel shaders, shader state, sampler and texture state and other pipeline state.</span></span> <span data-ttu-id="5ab44-106">Por tanto, una vez que haya organizado el estado en un efecto, puede encapsular el efecto de representación resultante de ese estado mediante la creación y representación del efecto.</span><span class="sxs-lookup"><span data-stu-id="5ab44-106">So once you have organized state into an effect, you can encapsulate the rendering effect that results from that state by creating and rendering the effect.</span></span>

<span data-ttu-id="5ab44-107">Hay algunos pasos para preparar un efecto para la representación.</span><span class="sxs-lookup"><span data-stu-id="5ab44-107">There are a few steps for preparing an effect for rendering.</span></span> <span data-ttu-id="5ab44-108">La primera es la compilación, que comprueba el código de HLSL como el código con la sintaxis del lenguaje HLSL y las reglas del marco de efecto.</span><span class="sxs-lookup"><span data-stu-id="5ab44-108">The first is compiling, which checks the HLSL like code against the HLSL language syntax and the effect framework rules.</span></span> <span data-ttu-id="5ab44-109">Puede compilar un efecto desde la aplicación mediante llamadas API o puede compilar un efecto sin conexión mediante la utilidad del compilador de efecto.</span><span class="sxs-lookup"><span data-stu-id="5ab44-109">You can compile an effect from your application using API calls or you can compile an effect offline using the effect compiler utility.</span></span> <span data-ttu-id="5ab44-110">Una vez que el efecto se ha compilado correctamente, créelo llamando a un conjunto de API diferente (pero muy similar).</span><span class="sxs-lookup"><span data-stu-id="5ab44-110">Once your effect has successfully compiled, create it by calling a different (but very similar) set of APIs.</span></span>

<span data-ttu-id="5ab44-111">Una vez creado el efecto, hay dos pasos restantes para usarlo.</span><span class="sxs-lookup"><span data-stu-id="5ab44-111">After the effect is created, there are two remaining steps for using it.</span></span> <span data-ttu-id="5ab44-112">En primer lugar, debe inicializar los valores de estado del efecto (los valores de las variables de efecto) mediante una serie de métodos para establecer el estado.</span><span class="sxs-lookup"><span data-stu-id="5ab44-112">First, you must initialize the effect state values (the values of the effect variables) using a number of methods for setting state.</span></span> <span data-ttu-id="5ab44-113">En el caso de algunas variables, esto se puede hacer una vez cuando se crea un efecto; otros deben actualizarse cada vez que la aplicación llame al bucle de representación.</span><span class="sxs-lookup"><span data-stu-id="5ab44-113">For some variables this can be done once when an effect is created; others must be updated each time your application calls the render loop.</span></span> <span data-ttu-id="5ab44-114">Una vez establecidas las variables de efecto, se indica al tiempo de ejecución que represente el efecto aplicando una técnica.</span><span class="sxs-lookup"><span data-stu-id="5ab44-114">Once the effect variables are set, you tell the runtime to render the affect by applying a technique.</span></span> <span data-ttu-id="5ab44-115">Estos temas se describen con más detalle a continuación.</span><span class="sxs-lookup"><span data-stu-id="5ab44-115">These topics are all discussed in further detail below.</span></span>

-   [<span data-ttu-id="5ab44-116">Compilación de un efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="5ab44-116">Compile an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-compile.md)
-   [<span data-ttu-id="5ab44-117">Crear un efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="5ab44-117">Create an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-create.md)
-   [<span data-ttu-id="5ab44-118">Establecer el estado del efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="5ab44-118">Set Effect State (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-set-state.md)
-   [<span data-ttu-id="5ab44-119">Aplicar una técnica (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="5ab44-119">Apply a Technique (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-apply-technique.md)

<span data-ttu-id="5ab44-120">Naturalmente, existen [consideraciones de rendimiento](d3d10-graphics-programming-guide-effects-performance.md) para el uso de efectos.</span><span class="sxs-lookup"><span data-stu-id="5ab44-120">Naturally there are [performance considerations](d3d10-graphics-programming-guide-effects-performance.md) for using effects.</span></span> <span data-ttu-id="5ab44-121">Estas consideraciones son en gran medida las mismas si no está utilizando un efecto.</span><span class="sxs-lookup"><span data-stu-id="5ab44-121">These considerations are largely the same if you are not using an effect.</span></span> <span data-ttu-id="5ab44-122">Cosas como, minimizar la cantidad de cambios de estado u organizar las variables que deben actualizarse por frecuencia.</span><span class="sxs-lookup"><span data-stu-id="5ab44-122">Things like, minimizing the amount of state changes, or organizing the variables that need to be updated by frequency.</span></span> <span data-ttu-id="5ab44-123">Estas tácticas se usan para minimizar la cantidad de datos que deben enviarse desde la CPU a la GPU y, por tanto, minimizar los posibles problemas de sincronización.</span><span class="sxs-lookup"><span data-stu-id="5ab44-123">These tactics are used to minimize the amount of data that needs to be sent from the CPU to the GPU, and therefore minimize potential synchronization problems.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ab44-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ab44-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ab44-125">Efectos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="5ab44-125">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



