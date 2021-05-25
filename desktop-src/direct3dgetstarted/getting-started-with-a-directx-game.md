---
title: Introducción a DirectX para Windows
description: Crear un juego de Microsoft DirectX para Windows es un desafío para un nuevo desarrollador. Aquí se revisan rápidamente los conceptos implicados y los pasos que debe seguir para empezar a desarrollar un juego con DirectX y C++.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bac8ca2805fed9ec42faf9deda9ddd51da39685
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343590"
---
# <a name="get-started-with-directx-for-windows"></a><span data-ttu-id="d645e-104">Introducción a DirectX para Windows</span><span class="sxs-lookup"><span data-stu-id="d645e-104">Get started with DirectX for Windows</span></span>

<span data-ttu-id="d645e-105">Crear un juego de Microsoft DirectX para Windows es un desafío para un nuevo desarrollador.</span><span class="sxs-lookup"><span data-stu-id="d645e-105">Creating a Microsoft DirectX game for Windows is a challenge for a new developer.</span></span> <span data-ttu-id="d645e-106">Aquí se revisan rápidamente los conceptos implicados y los pasos que debe seguir para empezar a desarrollar un juego con DirectX y C++.</span><span class="sxs-lookup"><span data-stu-id="d645e-106">Here we quickly review the concepts involved and the steps you must take to begin developing a game using DirectX and C++.</span></span>

<span data-ttu-id="d645e-107">Comencemos.</span><span class="sxs-lookup"><span data-stu-id="d645e-107">Let's get started.</span></span>

## <a name="what-skills-do-you-need"></a><span data-ttu-id="d645e-108">¿Qué aptitudes necesita?</span><span class="sxs-lookup"><span data-stu-id="d645e-108">What skills do you need?</span></span>

<span data-ttu-id="d645e-109">Para desarrollar un juego en DirectX para Windows, debe tener algunas aptitudes básicas.</span><span class="sxs-lookup"><span data-stu-id="d645e-109">To develop a game in DirectX for Windows, you must have a few basic skills.</span></span> <span data-ttu-id="d645e-110">En concreto, debe poder:</span><span class="sxs-lookup"><span data-stu-id="d645e-110">Specifically, you must be able to:</span></span>

-   <span data-ttu-id="d645e-111">Lea y escriba código C++ moderno (C++11 ayuda al máximo) y familiarícese con los principios y patrones básicos de diseño de C++, como las plantillas y el modelo de fábrica.</span><span class="sxs-lookup"><span data-stu-id="d645e-111">Read and write modern C++ code (C++11 helps the most), and be familiar with basic C++ design principles and patterns like templates and the factory model.</span></span> <span data-ttu-id="d645e-112">También debe estar familiarizado con las bibliotecas comunes de C++, como la biblioteca de plantillas estándar, y específicamente con los operadores de conversión, los tipos de puntero y las estructuras de datos de la biblioteca de plantillas estándar (como std::vector).</span><span class="sxs-lookup"><span data-stu-id="d645e-112">You must also be familiar with common C++ libraries like the Standard Template Library, and specifically with the casting operators, pointer types, and the standard template library data structures (such as std::vector).</span></span>
-   <span data-ttu-id="d645e-113">Comprenda la geometría básica, la trigonometría y el álgebra lineal.</span><span class="sxs-lookup"><span data-stu-id="d645e-113">Understand basic geometry, trigonometry, and linear algebra.</span></span> <span data-ttu-id="d645e-114">Gran parte del código que encontrará en los ejemplos supone que comprende estas formas de matemáticas y sus reglas comunes.</span><span class="sxs-lookup"><span data-stu-id="d645e-114">Much of the code you will find in the examples assumes you understand these forms of mathematics and their common rules.</span></span>
-   <span data-ttu-id="d645e-115">Familiarícese con COM, especialmente [**Microsoft::WRL::ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (puntero inteligente).</span><span class="sxs-lookup"><span data-stu-id="d645e-115">Have familiarity with COM—especially [**Microsoft::WRL::ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (smart pointer).</span></span>
-   <span data-ttu-id="d645e-116">Comprenda los fundamentos de la tecnología de gráficos y gráficos, especialmente los gráficos 3D.</span><span class="sxs-lookup"><span data-stu-id="d645e-116">Understand the foundations of graphics and graphics technology, particularly 3D graphics.</span></span> <span data-ttu-id="d645e-117">Aunque DirectX tiene su propia terminología, todavía se basa en una comprensión bien establecida de los principios generales de gráficos 3D.</span><span class="sxs-lookup"><span data-stu-id="d645e-117">While DirectX itself has its own terminology, it still builds upon a well-established understanding of general 3D graphics principles.</span></span>
-   <span data-ttu-id="d645e-118">Comprenda el concepto de bucle de mensajes, ya que implementará un bucle que escucha el sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="d645e-118">Understand the concept of a message loop, because you'll be implementing a loop that listens to the Windows operating system.</span></span>

## <a name="and-were-off"></a><span data-ttu-id="d645e-119">Y estamos apagados.</span><span class="sxs-lookup"><span data-stu-id="d645e-119">And we're off!</span></span>

<span data-ttu-id="d645e-120">¿Estás listo para empezar?</span><span class="sxs-lookup"><span data-stu-id="d645e-120">Ready to start?</span></span> <span data-ttu-id="d645e-121">Vamos a revisar antes de empezar.</span><span class="sxs-lookup"><span data-stu-id="d645e-121">Let's review before we head on.</span></span> <span data-ttu-id="d645e-122">Ha:</span><span class="sxs-lookup"><span data-stu-id="d645e-122">You have:</span></span>

-   <span data-ttu-id="d645e-123">Una instalación actualizada y en funcionamiento de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="d645e-123">An updated and working installation of Windows 8.1.</span></span>
-   <span data-ttu-id="d645e-124">Una instalación de [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span><span class="sxs-lookup"><span data-stu-id="d645e-124">An installation of [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span></span>
-   <span data-ttu-id="d645e-125">Un miedo intrépido y un deseo de obtener más información sobre el desarrollo de juegos de DirectX.</span><span class="sxs-lookup"><span data-stu-id="d645e-125">An intrepid spirit and a desire to learn more about DirectX game development!</span></span>

## <a name="next-steps"></a><span data-ttu-id="d645e-126">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="d645e-126">Next steps</span></span>



| <span data-ttu-id="d645e-127">Tema</span><span class="sxs-lookup"><span data-stu-id="d645e-127">Topic</span></span>                                                                                                   | <span data-ttu-id="d645e-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="d645e-128">Description</span></span>                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d645e-129">Trabajar con recursos de dispositivo DirectX</span><span class="sxs-lookup"><span data-stu-id="d645e-129">Work with DirectX device resources</span></span>](work-with-dxgi.md)                                           | <span data-ttu-id="d645e-130">Obtenga información sobre cómo usar DXGI para crear un dispositivo gráfico virtualizado y crear y configurar una cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="d645e-130">Learn how to use DXGI to create a virtualized graphics device, and create and configure a swap chain.</span></span>     |
| [<span data-ttu-id="d645e-131">Información sobre la canalización de representación de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d645e-131">Understand the Direct3D 11 rendering pipeline</span></span>](understand-the-directx-11-2-graphics-pipeline.md) | <span data-ttu-id="d645e-132">Obtenga información sobre cómo enlazar a la clase de recursos de dispositivo DirectX y dibujar mediante la canalización de gráficos de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d645e-132">Learn how to hook into the DirectX device resources class, and draw using the Direct3D graphics pipeline.</span></span> |
| [<span data-ttu-id="d645e-133">Trabajar con sombreadores y recursos de sombreador</span><span class="sxs-lookup"><span data-stu-id="d645e-133">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)               | <span data-ttu-id="d645e-134">Aprenda a escribir programas de sombreador HLSL para las fases de canalización de gráficos de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d645e-134">Learn how to write HLSL shader programs for Direct3D graphics pipeline stages.</span></span>                            |



 

 

 