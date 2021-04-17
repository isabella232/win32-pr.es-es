---
title: Introducción a DirectX para Windows
description: Crear un juego de Microsoft DirectX para Windows es un reto para un nuevo desarrollador. Aquí se revisan rápidamente los conceptos implicados y los pasos que debe seguir para empezar a desarrollar un juego con DirectX y C++.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae09cd127a30401ae0493f5dd770fe1e67607b45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704975"
---
# <a name="get-started-with-directx-for-windows"></a><span data-ttu-id="d898e-104">Introducción a DirectX para Windows</span><span class="sxs-lookup"><span data-stu-id="d898e-104">Get started with DirectX for Windows</span></span>

<span data-ttu-id="d898e-105">Crear un juego de Microsoft DirectX para Windows es un reto para un nuevo desarrollador.</span><span class="sxs-lookup"><span data-stu-id="d898e-105">Creating a Microsoft DirectX game for Windows is a challenge for a new developer.</span></span> <span data-ttu-id="d898e-106">Aquí se revisan rápidamente los conceptos implicados y los pasos que debe seguir para empezar a desarrollar un juego con DirectX y C++.</span><span class="sxs-lookup"><span data-stu-id="d898e-106">Here we quickly review the concepts involved and the steps you must take to begin developing a game using DirectX and C++.</span></span>

<span data-ttu-id="d898e-107">Empecemos.</span><span class="sxs-lookup"><span data-stu-id="d898e-107">Let's get started.</span></span>

## <a name="what-skills-do-you-need"></a><span data-ttu-id="d898e-108">¿Qué conocimientos necesita?</span><span class="sxs-lookup"><span data-stu-id="d898e-108">What skills do you need?</span></span>

<span data-ttu-id="d898e-109">Para desarrollar un juego en DirectX para Windows, debe tener unos conocimientos básicos.</span><span class="sxs-lookup"><span data-stu-id="d898e-109">To develop a game in DirectX for Windows, you must have a few basic skills.</span></span> <span data-ttu-id="d898e-110">En concreto, debe ser capaz de:</span><span class="sxs-lookup"><span data-stu-id="d898e-110">Specifically, you must be able to:</span></span>

-   <span data-ttu-id="d898e-111">Lea y escriba código moderno de C++ (C++ 11 ayuda a la mayoría) y familiarícese con los principios básicos y patrones de diseño de C++, como las plantillas y el modelo de fábrica.</span><span class="sxs-lookup"><span data-stu-id="d898e-111">Read and write modern C++ code (C++11 helps the most), and be familiar with basic C++ design principles and patterns like templates and the factory model.</span></span> <span data-ttu-id="d898e-112">También debe estar familiarizado con las bibliotecas comunes de C++ como la biblioteca de plantillas estándar y, en concreto, con los operadores de conversión, los tipos de puntero y las estructuras de datos de la biblioteca de plantillas estándar (como STD:: Vector).</span><span class="sxs-lookup"><span data-stu-id="d898e-112">You must also be familiar with common C++ libraries like the Standard Template Library, and specifically with the casting operators, pointer types, and the standard template library data structures (such as std::vector).</span></span>
-   <span data-ttu-id="d898e-113">Comprenda la geometría básica, las trigonometría y el álgebra lineal.</span><span class="sxs-lookup"><span data-stu-id="d898e-113">Understand basic geometry, trigonometry, and linear algebra.</span></span> <span data-ttu-id="d898e-114">Gran parte del código que encontrará en los ejemplos supone que comprende estas formas de matemáticas y sus reglas comunes.</span><span class="sxs-lookup"><span data-stu-id="d898e-114">Much of the code you will find in the examples assumes you understand these forms of mathematics and their common rules.</span></span>
-   <span data-ttu-id="d898e-115">Familiarícese con COM, especialmente [**Microsoft:: WRL:: ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (puntero inteligente).</span><span class="sxs-lookup"><span data-stu-id="d898e-115">Have familiarity with COM—especially [**Microsoft::WRL::ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (smart pointer).</span></span>
-   <span data-ttu-id="d898e-116">Comprenda las bases de la tecnología de gráficos y gráficos, especialmente los gráficos 3D.</span><span class="sxs-lookup"><span data-stu-id="d898e-116">Understand the foundations of graphics and graphics technology, particularly 3D graphics.</span></span> <span data-ttu-id="d898e-117">Aunque DirectX tiene su propia terminología, todavía se basa en una comprensión bien establecida de los principios generales de gráficos 3D.</span><span class="sxs-lookup"><span data-stu-id="d898e-117">While DirectX itself has its own terminology, it still builds upon a well-established understanding of general 3D graphics principles.</span></span>
-   <span data-ttu-id="d898e-118">Comprenda el concepto de un bucle de mensajes, ya que va a implementar un bucle que realiza escuchas en el sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="d898e-118">Understand the concept of a message loop, because you'll be implementing a loop that listens to the Windows operating system.</span></span>

## <a name="and-were-off"></a><span data-ttu-id="d898e-119">Y estamos desactivados.</span><span class="sxs-lookup"><span data-stu-id="d898e-119">And we're off!</span></span>

<span data-ttu-id="d898e-120">¿Estás listo para empezar?</span><span class="sxs-lookup"><span data-stu-id="d898e-120">Ready to start?</span></span> <span data-ttu-id="d898e-121">Vamos a revisar antes de empezar.</span><span class="sxs-lookup"><span data-stu-id="d898e-121">Let's review before we head on.</span></span> <span data-ttu-id="d898e-122">Ha:</span><span class="sxs-lookup"><span data-stu-id="d898e-122">You have:</span></span>

-   <span data-ttu-id="d898e-123">Instalación actualizada y en funcionamiento de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="d898e-123">An updated and working installation of Windows 8.1.</span></span>
-   <span data-ttu-id="d898e-124">Instalación de [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span><span class="sxs-lookup"><span data-stu-id="d898e-124">An installation of [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span></span>
-   <span data-ttu-id="d898e-125">Un espíritu Intrepid y el deseo de obtener más información sobre el desarrollo de juegos de DirectX.</span><span class="sxs-lookup"><span data-stu-id="d898e-125">An intrepid spirit and a desire to learn more about DirectX game development!</span></span>

## <a name="next-steps"></a><span data-ttu-id="d898e-126">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="d898e-126">Next steps</span></span>



|                                                                                                    |                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d898e-127">Trabajar con recursos de dispositivos DirectX</span><span class="sxs-lookup"><span data-stu-id="d898e-127">Work with DirectX device resources</span></span>](work-with-dxgi.md)                                           | <span data-ttu-id="d898e-128">Obtenga información sobre cómo usar DXGI para crear un dispositivo de gráficos virtualizado y crear y configurar una cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="d898e-128">Learn how to use DXGI to create a virtualized graphics device, and create and configure a swap chain.</span></span>     |
| [<span data-ttu-id="d898e-129">Descripción de la canalización de representación de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d898e-129">Understand the Direct3D 11 rendering pipeline</span></span>](understand-the-directx-11-2-graphics-pipeline.md) | <span data-ttu-id="d898e-130">Obtenga información sobre cómo enlazar a la clase de recursos de dispositivo DirectX y cómo dibujar mediante la canalización de gráficos Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d898e-130">Learn how to hook into the DirectX device resources class, and draw using the Direct3D graphics pipeline.</span></span> |
| [<span data-ttu-id="d898e-131">Trabajar con sombreadores y recursos del sombreador</span><span class="sxs-lookup"><span data-stu-id="d898e-131">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)               | <span data-ttu-id="d898e-132">Obtenga información sobre cómo escribir programas de sombreador HLSL para las fases de canalización de gráficos de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d898e-132">Learn how to write HLSL shader programs for Direct3D graphics pipeline stages.</span></span>                            |



 

 

 