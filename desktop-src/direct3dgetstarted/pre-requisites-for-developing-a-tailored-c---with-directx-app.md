---
title: Requisitos previos para el desarrollo con DirectX
description: Cuando empiece a desarrollar una aplicación de Windows con DirectX, tenga en cuenta los requisitos previos de esta página. Esto incluye las tecnologías que debe conocer antes de profundizar.
ms.assetid: 93f566cf-0c16-4487-9d53-dc59746e4d00
keywords:
- Aplicación DirectX, requisitos previos
- Aplicación DirectX, aplicación de la tienda Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5e09484bef67546047214702fab7d2d0a5c48d
ms.sourcegitcommit: 6394972f1e8b01229db602469df6bb137e31d776
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/16/2020
ms.locfileid: "104488609"
---
# <a name="prerequisites-for-developing-with-directx"></a><span data-ttu-id="8282b-106">Requisitos previos para el desarrollo con DirectX</span><span class="sxs-lookup"><span data-stu-id="8282b-106">Prerequisites for developing with DirectX</span></span>

<span data-ttu-id="8282b-107">Cuando empiece a desarrollar una aplicación de Windows con DirectX, tenga en cuenta los requisitos previos de esta página.</span><span class="sxs-lookup"><span data-stu-id="8282b-107">When you start to develop a Windows app using DirectX, keep the prerequisites on this page in mind.</span></span> <span data-ttu-id="8282b-108">Esto incluye las tecnologías que debe conocer antes de profundizar.</span><span class="sxs-lookup"><span data-stu-id="8282b-108">This includes the technologies you need to know before you dive in.</span></span>

## <a name="what-should-i-know-to-develop-a-windows-game-using-directx"></a><span data-ttu-id="8282b-109">¿Qué debo saber para desarrollar un juego de Windows con DirectX?</span><span class="sxs-lookup"><span data-stu-id="8282b-109">What should I know to develop a Windows game using DirectX?</span></span>

<span data-ttu-id="8282b-110">Antes de empezar a desarrollar una aplicación de la tienda Windows con DirectX, debe saber cómo programar en Windows con C++.</span><span class="sxs-lookup"><span data-stu-id="8282b-110">Before you start to develop a Windows Store app using DirectX, you need to know how to program in Windows with C++.</span></span> <span data-ttu-id="8282b-111">Las aplicaciones de Windows que usan DirectX se desarrollan en un nivel bajo de programación, lo que significa que se expondrán a muchas características del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8282b-111">Windows apps using DirectX are developed at a low level of programming, which means that you will be exposed to many features of the operating system.</span></span> <span data-ttu-id="8282b-112">Entre ellas se incluyen la administración de memoria y recursos, y la interfaz para el propio dispositivo de gráficos.</span><span class="sxs-lookup"><span data-stu-id="8282b-112">These include memory and resource management, and the interface for the graphics device itself.</span></span> <span data-ttu-id="8282b-113">Si no está familiarizado con el desarrollo de aplicaciones de juegos o gráficos, puede encontrar este desafío.</span><span class="sxs-lookup"><span data-stu-id="8282b-113">If you are new to game or graphics app development, you may find this challenging.</span></span> <span data-ttu-id="8282b-114">Sin embargo, también encontrará recompensas, ya que el desarrollo de juegos en este nivel crea muchas más posibilidades para el diseño y el desarrollo de aplicaciones de juegos y gráficos.</span><span class="sxs-lookup"><span data-stu-id="8282b-114">But you will also find it rewarding, because learning game development at this level creates far, far greater possibilities for game and graphics app design and development.</span></span>

<span data-ttu-id="8282b-115">También necesitará comprender los aspectos básicos de la programación de gráficos 2D y 3D y de las matemáticas, ya que muchas de las API que va a usar se desarrollaron teniendo en cuenta estos principios.</span><span class="sxs-lookup"><span data-stu-id="8282b-115">You'll also need to understand the basics of 2D and 3D graphics programming and mathematics, because many of the APIs you'll use were developed with these principles in mind.</span></span> <span data-ttu-id="8282b-116">Le resultará más fácil comprender sus parámetros y resultados si está familiarizado con las operaciones subyacentes.</span><span class="sxs-lookup"><span data-stu-id="8282b-116">It'll be easier for you to understand their parameters and results if you are familiar with the operations behind them.</span></span>

<span data-ttu-id="8282b-117">Como mínimo, debe tener una idea de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8282b-117">At a minimum, you should have a grasp of the following:</span></span>

-   <span data-ttu-id="8282b-118">Programación de Windows C/C++.</span><span class="sxs-lookup"><span data-stu-id="8282b-118">Windows C/C++ programming.</span></span> <span data-ttu-id="8282b-119">Esto significa que comprende los punteros y referencias, eventos y devoluciones de llamada, y quizás algunas de las bibliotecas comunes, como ATL.</span><span class="sxs-lookup"><span data-stu-id="8282b-119">This means that you understand pointers and references, events and callbacks, and perhaps a few of the common libraries like ATL.</span></span>
-   <span data-ttu-id="8282b-120">Programación de Win32.</span><span class="sxs-lookup"><span data-stu-id="8282b-120">Win32 programming.</span></span> <span data-ttu-id="8282b-121">Comprende cómo se crean las ventanas y cómo se procesan los eventos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="8282b-121">You understand how windows are created, and how user interface events are processed.</span></span> <span data-ttu-id="8282b-122">También comprende un poco más acerca de las API de Win32 y las API de Win32 esenciales.</span><span class="sxs-lookup"><span data-stu-id="8282b-122">You also understand a little bit about COM and essential Win32 APIs.</span></span>
-   <span data-ttu-id="8282b-123">Álgebra lineal y trigonometría.</span><span class="sxs-lookup"><span data-stu-id="8282b-123">Linear algebra and trigonometry.</span></span> <span data-ttu-id="8282b-124">Aunque no es esencial, tendrá un tiempo más sencillo si está familiarizado con los conceptos de estas dos disciplinas matemáticas, ya que son la base de gran parte de la programación de gráficos 3D.</span><span class="sxs-lookup"><span data-stu-id="8282b-124">While not essential, you'll have an easier time if you are familiar with concepts from these two math disciplines, because they are the foundation of much of 3D graphics programming.</span></span>
-   <span data-ttu-id="8282b-125">Terminología y conceptos básicos de los gráficos, como mapas de bits, texturas, vértices, mallas y ventanillas.</span><span class="sxs-lookup"><span data-stu-id="8282b-125">Basic graphics terminology and concepts, such as bitmaps, textures, vertices, meshes, and viewports.</span></span>

## <a name="what-does-directx-provide-me"></a><span data-ttu-id="8282b-126">¿Qué me proporciona DirectX?</span><span class="sxs-lookup"><span data-stu-id="8282b-126">What does DirectX provide me?</span></span>

<span data-ttu-id="8282b-127">DirectX es el conjunto principal de API de gráficos que se usará para desarrollar juegos de Windows.</span><span class="sxs-lookup"><span data-stu-id="8282b-127">DirectX is the primary set of graphics APIs you'll use to develop Windows games.</span></span> <span data-ttu-id="8282b-128">Estas son las categorías de características con las que debe familiarizarse al decidir cómo desarrollar el juego.</span><span class="sxs-lookup"><span data-stu-id="8282b-128">Here are the categories of features that you must become familiar with when you decide how to develop your game.</span></span>



| <span data-ttu-id="8282b-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8282b-129">Library</span></span>     | <span data-ttu-id="8282b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="8282b-130">Description</span></span>                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8282b-131">Direct3D</span><span class="sxs-lookup"><span data-stu-id="8282b-131">Direct3D</span></span>    | <span data-ttu-id="8282b-132">Un conjunto de bibliotecas eficaces y con aceleración de rendimiento y orientado al rendimiento para representar gráficos 3D.</span><span class="sxs-lookup"><span data-stu-id="8282b-132">A powerful, performance-oriented, hardware-accelerated set of libraries for rendering 3D graphics.</span></span>                                              |
| <span data-ttu-id="8282b-133">Direct2D</span><span class="sxs-lookup"><span data-stu-id="8282b-133">Direct2D</span></span>    | <span data-ttu-id="8282b-134">Un conjunto de bibliotecas de gráficos 2D para el dibujo acelerado por hardware y el dibujo 2D vectorial.</span><span class="sxs-lookup"><span data-stu-id="8282b-134">A set of 2D graphics libraries for hardware-accelerated bitmap and vector 2D drawing.</span></span>                                                           |
| <span data-ttu-id="8282b-135">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="8282b-135">DirectXMath</span></span> | <span data-ttu-id="8282b-136">Biblioteca de operaciones matemáticas comunes y optimizadas utilizadas en gráficos 2D y 3D, como operaciones de vector y matriz.</span><span class="sxs-lookup"><span data-stu-id="8282b-136">A library of common, optimized math operations used in 2D and 3D graphics, such as vector and matrix operations.</span></span>                                |
| <span data-ttu-id="8282b-137">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="8282b-137">DirectWrite</span></span> | <span data-ttu-id="8282b-138">Biblioteca de API de representación y presentación de texto 2D.</span><span class="sxs-lookup"><span data-stu-id="8282b-138">A library of 2D text rendering and layout APIs.</span></span> <span data-ttu-id="8282b-139">Admite la aceleración de hardware y la rasterización de software.</span><span class="sxs-lookup"><span data-stu-id="8282b-139">It supports both hardware acceleration and software rasterization.</span></span>                              |
| <span data-ttu-id="8282b-140">XAudio2</span><span class="sxs-lookup"><span data-stu-id="8282b-140">XAudio2</span></span>     | <span data-ttu-id="8282b-141">Una API de audio de bajo nivel multiplataforma para Microsoft Windows que proporciona una base de procesamiento de señal y combinación de audio para el desarrollo de juegos.</span><span class="sxs-lookup"><span data-stu-id="8282b-141">A low-level, cross-platform audio API for Microsoft Windows that provides a signal processing and audio mixing foundation for game development.</span></span> |
| <span data-ttu-id="8282b-142">XInput</span><span class="sxs-lookup"><span data-stu-id="8282b-142">XInput</span></span>      | <span data-ttu-id="8282b-143">Una biblioteca que admite varios controles de juego tradicionales, con énfasis en el modelo de controladora Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="8282b-143">A library that supports various traditional gaming controls, with an emphasis on the Xbox 360 controller model.</span></span>                                 |



 

## <a name="what-tools-do-i-need-to-develop-a-windows-game-with-directx"></a><span data-ttu-id="8282b-144">¿Qué herramientas necesito para desarrollar un juego de Windows con DirectX?</span><span class="sxs-lookup"><span data-stu-id="8282b-144">What tools do I need to develop a Windows game with DirectX?</span></span>

<span data-ttu-id="8282b-145">Para empezar a trabajar con este tutorial, necesitará lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8282b-145">To get started with this tutorial, you need:</span></span>

-   <span data-ttu-id="8282b-146">Windows 8.1 o superior</span><span class="sxs-lookup"><span data-stu-id="8282b-146">Windows 8.1 or greater</span></span>
-   <span data-ttu-id="8282b-147">Microsoft Visual Studio 2013 o superior</span><span class="sxs-lookup"><span data-stu-id="8282b-147">Microsoft Visual Studio 2013 or greater</span></span>

 

 




