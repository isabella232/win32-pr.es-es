---
description: Obtenga información sobre cómo representar un efecto para Direct3D 10. Un efecto se puede usar para almacenar información o para representar mediante un grupo de estado.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Representación de un efecto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79db595585c6587648fba12afa5fbb22ff33e845
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262577"
---
# <a name="rendering-an-effect-direct3d-10"></a><span data-ttu-id="03b2a-104">Representación de un efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="03b2a-104">Rendering an Effect (Direct3D 10)</span></span>

<span data-ttu-id="03b2a-105">Un efecto se puede usar para almacenar información o para representar mediante un grupo de estado.</span><span class="sxs-lookup"><span data-stu-id="03b2a-105">An effect can be used to store information, or to render using a group of state.</span></span> <span data-ttu-id="03b2a-106">Cada técnica especifica sombreadores de vértices, sombreadores de geometría, sombreadores de píxeles, estado del sombreador, muestreador y estado de textura y otro estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="03b2a-106">Each technique specifies vertex shaders, geometry shaders, pixel shaders, shader state, sampler and texture state and other pipeline state.</span></span> <span data-ttu-id="03b2a-107">Por lo tanto, una vez que haya organizado el estado en un efecto, puede encapsular el efecto de representación que resulta de ese estado mediante la creación y representación del efecto.</span><span class="sxs-lookup"><span data-stu-id="03b2a-107">So once you have organized state into an effect, you can encapsulate the rendering effect that results from that state by creating and rendering the effect.</span></span>

<span data-ttu-id="03b2a-108">Hay algunos pasos para preparar un efecto para la representación.</span><span class="sxs-lookup"><span data-stu-id="03b2a-108">There are a few steps for preparing an effect for rendering.</span></span> <span data-ttu-id="03b2a-109">La primera es la compilación, que comprueba la HLSL como el código con la sintaxis del lenguaje HLSL y las reglas del marco de trabajo de efecto.</span><span class="sxs-lookup"><span data-stu-id="03b2a-109">The first is compiling, which checks the HLSL like code against the HLSL language syntax and the effect framework rules.</span></span> <span data-ttu-id="03b2a-110">Puede compilar un efecto desde la aplicación mediante llamadas API o puede compilar un efecto sin conexión mediante la utilidad del compilador effect.</span><span class="sxs-lookup"><span data-stu-id="03b2a-110">You can compile an effect from your application using API calls or you can compile an effect offline using the effect compiler utility.</span></span> <span data-ttu-id="03b2a-111">Una vez que el efecto se haya compilado correctamente, puede crearlo mediante una llamada a un conjunto diferente (pero muy similar) de API.</span><span class="sxs-lookup"><span data-stu-id="03b2a-111">Once your effect has successfully compiled, create it by calling a different (but very similar) set of APIs.</span></span>

<span data-ttu-id="03b2a-112">Una vez creado el efecto, hay dos pasos restantes para usarlo.</span><span class="sxs-lookup"><span data-stu-id="03b2a-112">After the effect is created, there are two remaining steps for using it.</span></span> <span data-ttu-id="03b2a-113">En primer lugar, debe inicializar los valores de estado de efecto (los valores de las variables de efecto) mediante una serie de métodos para establecer el estado.</span><span class="sxs-lookup"><span data-stu-id="03b2a-113">First, you must initialize the effect state values (the values of the effect variables) using a number of methods for setting state.</span></span> <span data-ttu-id="03b2a-114">Para algunas variables, esto se puede hacer una vez cuando se crea un efecto. otros deben actualizarse cada vez que la aplicación llama al bucle de representación.</span><span class="sxs-lookup"><span data-stu-id="03b2a-114">For some variables this can be done once when an effect is created; others must be updated each time your application calls the render loop.</span></span> <span data-ttu-id="03b2a-115">Una vez establecidas las variables de efecto, se le dice al tiempo de ejecución que represente el efecto mediante la aplicación de una técnica.</span><span class="sxs-lookup"><span data-stu-id="03b2a-115">Once the effect variables are set, you tell the runtime to render the affect by applying a technique.</span></span> <span data-ttu-id="03b2a-116">Estos temas se tratan con más detalle a continuación.</span><span class="sxs-lookup"><span data-stu-id="03b2a-116">These topics are all discussed in further detail below.</span></span>

-   [<span data-ttu-id="03b2a-117">Compilación de un efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="03b2a-117">Compile an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-compile.md)
-   [<span data-ttu-id="03b2a-118">Crear un efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="03b2a-118">Create an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-create.md)
-   [<span data-ttu-id="03b2a-119">Establecer estado de efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="03b2a-119">Set Effect State (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-set-state.md)
-   [<span data-ttu-id="03b2a-120">Aplicar una técnica (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="03b2a-120">Apply a Technique (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-apply-technique.md)

<span data-ttu-id="03b2a-121">Naturalmente, hay [consideraciones de rendimiento para](d3d10-graphics-programming-guide-effects-performance.md) usar efectos.</span><span class="sxs-lookup"><span data-stu-id="03b2a-121">Naturally there are [performance considerations](d3d10-graphics-programming-guide-effects-performance.md) for using effects.</span></span> <span data-ttu-id="03b2a-122">Estas consideraciones son en gran medida las mismas si no usa ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="03b2a-122">These considerations are largely the same if you are not using an effect.</span></span> <span data-ttu-id="03b2a-123">Aspectos como minimizar la cantidad de cambios de estado o organizar las variables que deben actualizarse por frecuencia.</span><span class="sxs-lookup"><span data-stu-id="03b2a-123">Things like, minimizing the amount of state changes, or organizing the variables that need to be updated by frequency.</span></span> <span data-ttu-id="03b2a-124">Estas tácticas se usan para minimizar la cantidad de datos que se deben enviar desde la CPU a la GPU y, por tanto, minimizar los posibles problemas de sincronización.</span><span class="sxs-lookup"><span data-stu-id="03b2a-124">These tactics are used to minimize the amount of data that needs to be sent from the CPU to the GPU, and therefore minimize potential synchronization problems.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03b2a-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="03b2a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03b2a-126">Efectos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="03b2a-126">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



