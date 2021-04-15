---
title: Componentes
description: Componentes
ms.assetid: 9fbd957d-ee6b-475f-8a04-51effa206ad5
keywords:
- OpenGL en Windows, componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c1294745938e245deda8296f2ce4d1df386b9f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676215"
---
# <a name="components"></a><span data-ttu-id="e3a4b-104">Componentes</span><span class="sxs-lookup"><span data-stu-id="e3a4b-104">Components</span></span>

<span data-ttu-id="e3a4b-105">La implementación de OpenGL en Windows de Microsoft incluye los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="e3a4b-105">Microsoft's implementation of OpenGL in Windows includes the following components:</span></span>

-   <span data-ttu-id="e3a4b-106">Conjunto completo de comandos OpenGL actuales</span><span class="sxs-lookup"><span data-stu-id="e3a4b-106">The full set of current OpenGL commands</span></span>

    <span data-ttu-id="e3a4b-107">OpenGL contiene una biblioteca de funciones básicas para las operaciones de gráficos 3D.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-107">OpenGL contains a library of core functions for 3-D graphics operations.</span></span> <span data-ttu-id="e3a4b-108">Estas funciones básicas se usan para administrar la descripción de la forma de objeto, la transformación de matriz, la iluminación, el color, la textura, el recorte, los mapas de bits, la niebla y el suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-108">These basic functions are used to manage object shape description, matrix transformation, lighting, coloring, texture, clipping, bitmaps, fog, and antialiasing.</span></span> <span data-ttu-id="e3a4b-109">Los nombres de estas funciones principales tienen un prefijo "GL".</span><span class="sxs-lookup"><span data-stu-id="e3a4b-109">The names for these core functions have a "gl" prefix.</span></span>

    <span data-ttu-id="e3a4b-110">Muchos de los comandos OpenGL tienen varias variantes, que difieren en el número y tipo de sus parámetros.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-110">Many of the OpenGL commands have several variants, which differ in the number and type of their parameters.</span></span> <span data-ttu-id="e3a4b-111">Contando todas las variantes, hay más de 300 comandos OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-111">Counting all the variants, there are more than 300 OpenGL commands.</span></span>

-   <span data-ttu-id="e3a4b-112">La biblioteca de la utilidad OpenGL (GLU)</span><span class="sxs-lookup"><span data-stu-id="e3a4b-112">The OpenGL Utility (GLU) library</span></span>

    <span data-ttu-id="e3a4b-113">Esta biblioteca de funciones auxiliares complementa las funciones básicas de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-113">This library of auxiliary functions complements the core OpenGL functions.</span></span> <span data-ttu-id="e3a4b-114">Los comandos administran la compatibilidad con texturas, la transformación de coordenadas, la teselación de polígonos, las esferas de representación, los cilindros y los discos, las curvas y superficies de NURBS (no uniforme B-spline racional) y el control de errores.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-114">The commands manage texture support, coordinate transformation, polygon tessellation, rendering spheres, cylinders and disks, NURBS (Non-Uniform Rational B-Spline) curves and surfaces, and error handling.</span></span>

-   <span data-ttu-id="e3a4b-115">Biblioteca auxiliar de la guía de programación de OpenGL</span><span class="sxs-lookup"><span data-stu-id="e3a4b-115">The OpenGL Programming Guide Auxiliary library</span></span>

    <span data-ttu-id="e3a4b-116">Se trata de una biblioteca sencilla, independiente de la plataforma, de funciones para administrar ventanas, controlar los eventos de entrada, dibujar objetos 3D clásicos, administrar un proceso en segundo plano y ejecutar un programa.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-116">This is a simple, platform-independent library of functions for managing windows, handling input events, drawing classic 3-D objects, managing a background process, and running a program.</span></span> <span data-ttu-id="e3a4b-117">Las rutinas de entrada y administración de ventanas proporcionan un nivel básico de funcionalidad con el que puede comenzar a programar rápidamente en OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-117">The window management and input routines provide a base level of functionality with which you can quickly get started programming in OpenGL.</span></span>

    <span data-ttu-id="e3a4b-118">No las use, sin embargo, en una aplicación de producción.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-118">Do not use them, however, in a production application.</span></span> <span data-ttu-id="e3a4b-119">Estas son algunas de las razones de esta ADVERTENCIA:</span><span class="sxs-lookup"><span data-stu-id="e3a4b-119">Here are some reasons for this warning:</span></span>

    -   <span data-ttu-id="e3a4b-120">El bucle de mensajes está en el código de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-120">The message loop is in the library code.</span></span>
    -   <span data-ttu-id="e3a4b-121">No hay ninguna manera de agregar controladores para mensajes de WM adicionales \* .</span><span class="sxs-lookup"><span data-stu-id="e3a4b-121">There is no way to add handlers for additional WM\* messages.</span></span>
    -   <span data-ttu-id="e3a4b-122">Hay muy poca compatibilidad con las paletas lógicas.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-122">There is very little support for logical palettes.</span></span>

    <span data-ttu-id="e3a4b-123">La biblioteca se describe y se usa en la *Guía de programación de OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-123">The library is described and used in the *OpenGL Programming Guide*.</span></span>

-   <span data-ttu-id="e3a4b-124">Las funciones WGL</span><span class="sxs-lookup"><span data-stu-id="e3a4b-124">The WGL functions</span></span>

    <span data-ttu-id="e3a4b-125">Este conjunto de funciones conecta OpenGL al sistema de ventanas de Windows.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-125">This set of functions connects OpenGL to the Windows windowing system.</span></span> <span data-ttu-id="e3a4b-126">Las funciones administran los contextos de representación, las listas de visualización, las funciones de extensión y los mapas de bits de fuente.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-126">The functions manage rendering contexts, display lists, extension functions, and font bitmaps.</span></span> <span data-ttu-id="e3a4b-127">Las funciones WGL son análogas a las extensiones GLX que conectan OpenGL con el sistema de ventana X.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-127">The WGL functions are analogous to the GLX extensions that connect OpenGL to the X Window System.</span></span> <span data-ttu-id="e3a4b-128">Los nombres de estas funciones tienen un prefijo "WGL".</span><span class="sxs-lookup"><span data-stu-id="e3a4b-128">The names for these functions have a "wgl" prefix.</span></span>

-   <span data-ttu-id="e3a4b-129">Nuevas funciones de Windows para formatos de píxeles y almacenamiento en búfer doble</span><span class="sxs-lookup"><span data-stu-id="e3a4b-129">New Windows functions for pixel formats and double buffering</span></span>

    <span data-ttu-id="e3a4b-130">Estas funciones admiten formatos de píxel por ventana y doble búfer (para cambios de imagen suaves) de Windows.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-130">These functions support per-window pixel formats and double buffering (for smooth image changes) of windows.</span></span> <span data-ttu-id="e3a4b-131">Estas nuevas funciones solo se aplican a las ventanas de gráficos OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-131">These new functions apply only to OpenGL graphics windows.</span></span>

 

 




