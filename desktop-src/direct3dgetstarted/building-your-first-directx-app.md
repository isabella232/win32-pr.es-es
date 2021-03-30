---
title: Creación de la primera aplicación de Windows con DirectX
description: En esta sección se describe por qué usaría el modelo de C++ para el desarrollo de aplicaciones de la tienda Windows y proporciona tutoriales y procedimientos básicos para empezar a trabajar con el desarrollo de aplicaciones de DirectX.
ms.assetid: b632ba9c-1c30-4d21-ac79-7f2a193956fe
keywords:
- Aplicación DirectX, introducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5e3afed57244789c0e3e06ab71ec39e581305c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772690"
---
# <a name="create-your-first-windows-app-using-directx"></a><span data-ttu-id="13491-104">Creación de la primera aplicación de Windows con DirectX</span><span class="sxs-lookup"><span data-stu-id="13491-104">Create your first Windows app using DirectX</span></span>

<span data-ttu-id="13491-105">Si conoce DirectX, puede desarrollar una aplicación de DirectX con C++ nativo y HLSL para sacar el máximo partido del hardware de gráficos.</span><span class="sxs-lookup"><span data-stu-id="13491-105">If you know DirectX, you can develop a DirectX app using native C++ and HLSL to take full advantage of graphics hardware.</span></span>

<span data-ttu-id="13491-106">Use este tutorial básico para empezar a trabajar con el desarrollo de aplicaciones de DirectX y luego use el mapa de ruta para seguir explorando DirectX.</span><span class="sxs-lookup"><span data-stu-id="13491-106">Use this basic tutorial to get started with DirectX app development, then use the roadmap to continue exploring DirectX.</span></span>

## <a name="windows-desktop-app-with-c-and-directx"></a><span data-ttu-id="13491-107">Aplicación de escritorio de Windows con C++ y DirectX</span><span class="sxs-lookup"><span data-stu-id="13491-107">Windows desktop app with C++ and DirectX</span></span>

<span data-ttu-id="13491-108">Una aplicación de escritorio de Windows con DirectX es una aplicación desarrollada mediante las API nativas de C++ y DirectX.</span><span class="sxs-lookup"><span data-stu-id="13491-108">A Windows desktop app with DirectX is an app developed using native C++ and DirectX APIs.</span></span> <span data-ttu-id="13491-109">Este modelo es más complejo que una aplicación escrita en un marco administrado, pero proporciona mayor flexibilidad y mayor acceso a los recursos del sistema, especialmente a los dispositivos gráficos.</span><span class="sxs-lookup"><span data-stu-id="13491-109">This model is more complex than an app written in a managed framework, but it provides greater flexibility and greater access to system resources especially graphics devices.</span></span> <span data-ttu-id="13491-110">Por lo tanto, es un buen modelo para el desarrollador experimentado.</span><span class="sxs-lookup"><span data-stu-id="13491-110">So, it is a good model for the experienced developer.</span></span>

## <a name="why-develop-a-windows-app-with-directx"></a><span data-ttu-id="13491-111">¿Por qué desarrollar una aplicación de Windows con DirectX?</span><span class="sxs-lookup"><span data-stu-id="13491-111">Why develop a Windows app with DirectX?</span></span>

<span data-ttu-id="13491-112">La respuesta es sencilla: desea crear un juego que sea intensivo de gráficos o multimedia, y puede usar las características que admiten muchos dispositivos de gráficos.</span><span class="sxs-lookup"><span data-stu-id="13491-112">The answer is simple: you want to make a game that is graphics- or multimedia-intensive, and can use the features that many graphics devices support.</span></span> <span data-ttu-id="13491-113">Esto no será fácil si no está familiarizado con el desarrollo de juegos o con el desarrollo de Windows y C/C++, pero hay algunas buenas noticias: DirectX 11 es la versión más sencilla y coherente de Microsoft DirectX todavía.</span><span class="sxs-lookup"><span data-stu-id="13491-113">This won't be easy if you are new to game development or to Windows development and C/C++, but there's some good news: DirectX 11 is the simplest and most cohesive version of Microsoft DirectX yet.</span></span> <span data-ttu-id="13491-114">También es el más eficaz y con características enriquecidas.</span><span class="sxs-lookup"><span data-stu-id="13491-114">It's also the most powerful and feature-rich.</span></span> <span data-ttu-id="13491-115">Si su objetivo es el desarrollo de juegos maestros y aprende las técnicas de representación más avanzadas, DirectX puede proporcionarle la oportunidad de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="13491-115">If your goal is to master game development and learn the most advanced rendering techniques, then DirectX can provide the opportunity for you to do that.</span></span>

<span data-ttu-id="13491-116">Dicho esto, es esencial planear el juego (o la aplicación interactiva y en tiempo real).</span><span class="sxs-lookup"><span data-stu-id="13491-116">That said, planning your game (or interactive, real-time app) is essential.</span></span> <span data-ttu-id="13491-117">Si no está familiarizado con el desarrollo de juegos y el juego no tiene requisitos gráficos exigentes, considere la posibilidad de desarrollarlo con .NET Framework en su lugar.</span><span class="sxs-lookup"><span data-stu-id="13491-117">If you are new to game development, and your game doesn't have demanding graphics requirements, consider developing it with the .NET framework instead.</span></span> <span data-ttu-id="13491-118">Además, muchos de los paquetes de desarrollo de juegos y gráficos de "middleware" están disponibles para las plataformas Windows y otros no requieren conocimientos de programación significativos.</span><span class="sxs-lookup"><span data-stu-id="13491-118">Also, many "middleware" graphics and game development packages are available for Windows platforms, and some do not require significant programming skills.</span></span>

<span data-ttu-id="13491-119">Si está seguro o simplemente tiene un sueño de crear un juego con gráficos de alta fidelidad (o una aplicación con contenido de gráficos complejos), siga leyendo.</span><span class="sxs-lookup"><span data-stu-id="13491-119">If you are confident, or simply have a dream of making a game with high-fidelity graphics (or an app with complex graphics content), then read on!</span></span>

## <a name="in-this-section"></a><span data-ttu-id="13491-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="13491-120">In this section</span></span>



| <span data-ttu-id="13491-121">Tema</span><span class="sxs-lookup"><span data-stu-id="13491-121">Topic</span></span>                                                                                                                     | <span data-ttu-id="13491-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="13491-122">Description</span></span>                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13491-123">Requisitos previos para el desarrollo con DirectX</span><span class="sxs-lookup"><span data-stu-id="13491-123">Prerequisites for developing with DirectX</span></span>](pre-requisites-for-developing-a-tailored-c---with-directx-app.md)<br/> | <span data-ttu-id="13491-124">Cuando empiece a desarrollar una aplicación de Windows con DirectX, tenga en cuenta los requisitos previos de esta página.</span><span class="sxs-lookup"><span data-stu-id="13491-124">When you start to develop a Windows app using DirectX, keep the prerequisites on this page in mind.</span></span> <span data-ttu-id="13491-125">Esto incluye las tecnologías que debe conocer antes de profundizar.</span><span class="sxs-lookup"><span data-stu-id="13491-125">This includes the technologies you need to know before you dive in.</span></span><br/>                            |
| [<span data-ttu-id="13491-126">Introducción a DirectX para Windows</span><span class="sxs-lookup"><span data-stu-id="13491-126">Get started with DirectX for Windows</span></span>](getting-started-with-a-directx-game.md)<br/>                                | <span data-ttu-id="13491-127">Crear un juego de DirectX para Windows es un reto para un nuevo desarrollador.</span><span class="sxs-lookup"><span data-stu-id="13491-127">Creating a DirectX game for Windows is a challenge for a new developer.</span></span> <span data-ttu-id="13491-128">Aquí se revisan rápidamente los conceptos implicados y los pasos que debe seguir para empezar a desarrollar un juego con DirectX y C++.</span><span class="sxs-lookup"><span data-stu-id="13491-128">Here we quickly review the concepts involved and the steps you must take to begin developing a game using DirectX and C++.</span></span><br/> |
| [<span data-ttu-id="13491-129">Hoja de ruta para aplicaciones DirectX de escritorio</span><span class="sxs-lookup"><span data-stu-id="13491-129">Roadmap for Desktop DirectX apps</span></span>](roadmap-for-metro-style-apps-using-directx.md)<br/>                             | <span data-ttu-id="13491-130">Estos son los recursos clave que le ayudarán a empezar a usar DirectX y C++ para desarrollar aplicaciones de escritorio con un uso intensivo de gráficos, como los juegos.</span><span class="sxs-lookup"><span data-stu-id="13491-130">Here are key resources to help you get started with using DirectX and C++ to develop graphics-intensive Desktop apps, like games.</span></span> <br/>                                                                 |



 

 

 





